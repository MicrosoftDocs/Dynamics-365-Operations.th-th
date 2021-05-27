---
title: ตั้งค่าคอนฟิกรูปแบบ ER เพื่อใช้พารามิเตอร์ที่ระบุสำหรับแต่ละนิติบุคคล
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้พารามิเตอร์ที่ระบุไว้สำหรับแต่ละนิติบุคคล
author: NickSelin
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 0af3e1d589fd99cc722d8aedeb9596388a9e2e8c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018297"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="baea0-103">ตั้งค่าคอนฟิกรูปแบบ ER เพื่อใช้พารามิเตอร์ที่ระบุสำหรับแต่ละนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="baea0-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="baea0-104">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="baea0-104">Overview</span></span>

<span data-ttu-id="baea0-105">ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) หลายรูปแบบที่คุณจะออกแบบ คุณต้องกรองข้อมูลโดยใช้ชุดของค่าที่เกี่ยวข้องกับแต่ละนิติบุคคลของอินสแตนซ์ของคุณ (ตัวอย่าง เช่น ชุดของรหัสภาษีที่จะกรองข้อมูลธุรกรรมภาษี)</span><span class="sxs-lookup"><span data-stu-id="baea0-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="baea0-106">ในขณะนี้ เมื่อกรองชนิดนี้มีการตั้งค่าคอนฟิกในรูปแบบ ER ค่าที่ขึ้นอยู่กับนิติบุคคล (ตัวอย่าง เช่น รหัสภาษี) จะใช้ในนิพจน์ของรูปแบบ ER เพื่อระบุกฎการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="baea0-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="baea0-107">ดังนั้น รูปแบบ ER จึงทำให้นิติบุคคล–เฉพาะเจาะจง และเพื่อสร้างรายงานที่จำเป็น คุณต้องสร้างสำเนาที่สืบทอดมาของรูปแบบ ER ดั้งเดิม สำหรับแต่ละนิติบุคคลที่คุณต้องรันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="baea0-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="baea0-108">แต่ละรูปแบบ ER ที่สืบทอดมาต้องได้รับการแก้ไข เพื่อดึงข้อมูลค่านิติบุคคล–เฉพาะ ข้างใน ปรับใช้เมื่อใดก็ตามที่มีการอัพเดตเวอร์ชันดั้งเดิม (พื้นฐาน) แล้วส่งออกจากสภาพแวดล้อมการทดสอบ และนำเข้าไปยังสภาพแวดล้อมการใช้งานจริง เมื่อต้องปรับใช้สำหรับการใช้งานจริง และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="baea0-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment, and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="baea0-109">ดังนั้น การบำรุงรักษาชนิดของโซลูชัน ER ที่ตั้งค่าคอนฟิกนี้ซับซ้อนและใช้เวลานานหลายประการดังนี้:</span><span class="sxs-lookup"><span data-stu-id="baea0-109">Therefore, maintenance of this type of configured ER solution is complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="baea0-110">ยิ่งเป็นนิติบุคคลมากเท่าไร ยิ่งต้องรักษาการกำหนดค่ารูปแบบ ER มากเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="baea0-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="baea0-111">การบำรุงรักษาของการตั้งค่าคอนฟิก ER กำหนดให้ผู้ใช้ที่เป็นธุรกิจต้องมีความรู้ ER</span><span class="sxs-lookup"><span data-stu-id="baea0-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="baea0-112">คุณลักษณะพารามิเตอร์เฉพาะของโปรแกรมประยุกต์ ER ให้ผู้ใช้ระดับสูงตั้งค่าคอนฟิกการกรองข้อมูลในรูปแบบ ER ซึ่งขึ้นอยู่กับชุดของกฎนามธรรม</span><span class="sxs-lookup"><span data-stu-id="baea0-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="baea0-113">ชุดของกฎนี้สามารถตั้งค่าคอนฟิกให้ใช้แหล่งข้อมูลที่มีอยู่ในรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="baea0-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="baea0-114">ผู้ใช้ทางธุรกิจสามารถระบุกฎจริงนอกเหนือจากกรอบงาน ER โดยใช้อินเทอร์เฟสผู้ใช้ (UI) ซึ่งสร้างขึ้นโดยอัตโนมัติตามการตั้งค่าของรูปแบบ ER ที่สอดคล้องกัน และข้อมูลนิติบุคคลปัจจุบัน ที่จะเข้าถึงโดยแหล่งข้อมูลของรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="baea0-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="baea0-115">ชุดของกฎที่ระบุสำหรับรูปแบบ ER สามารถส่งออกจากนิติบุคคลปัจจุบันของอินสแตนซ์ Dynamics 365 Finance (การเงิน)</span><span class="sxs-lookup"><span data-stu-id="baea0-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="baea0-116">จากนั้นจึงสามารถนำเข้าไปยังนิติบุคคลอื่นของอินสแตนซ์ทางการเงินเดียวกัน หรืออินสแตนซ์ที่แตกต่างกัน เป็นชุดของกฎสำหรับรูปแบบ ER เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="baea0-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="baea0-117">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="baea0-117">Prerequisites</span></span>

<span data-ttu-id="baea0-118">การทำตัวอย่างในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณต้องเข้าถึงอินสแตนซ์ของ Regulatory Configuration Services (RCS) ที่ได้เตรียมใช้งานสำหรับผู้เช่ารายเดียวกันกับ Finance สำหรับหนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="baea0-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="baea0-119">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="baea0-119">Electronic reporting developer</span></span>
- <span data-ttu-id="baea0-120">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="baea0-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="baea0-121">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="baea0-121">System administrator</span></span>

<span data-ttu-id="baea0-122">เราขอแนะนำให้คุณทำตามขั้นตอนให้สำเร็จ ในหัวข้อ [สนับสนุนการเรียกแบบใช้พารามิเตอร์ของแหล่งข้อมูล ER ของชนิดฟิลด์ที่คำนวณได้](er-calculated-field-type.md)</span><span class="sxs-lookup"><span data-stu-id="baea0-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="baea0-123">ถ้าคุณดำเนินการขั้นตอนดังกล่าวเสร็จเรียบร้อยแล้ วคุณสามารถข้ามขั้นตอนในส่วน **นำเข้าการตั้งค่าคอนฟิก ER ลงใน RCS** ที่ตามมา</span><span class="sxs-lookup"><span data-stu-id="baea0-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="baea0-124">นำเข้าการตั้งค่าคอนฟิก ER ลงใน RCS</span><span class="sxs-lookup"><span data-stu-id="baea0-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="baea0-125">ดาวน์โหลดและจัดเก็บการตั้งค่าคอนฟิก ER ต่อไปนี้ไว้ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="baea0-125">Download and locally store the following ER configurations.</span></span>

| <span data-ttu-id="baea0-126">**คำอธิบายเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="baea0-126">**Content description**</span></span>                        | <span data-ttu-id="baea0-127">**ชื่อไฟล์**</span><span class="sxs-lookup"><span data-stu-id="baea0-127">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="baea0-128">ไฟล์การตั้งค่าคอนฟิก **แบบจำลองข้อมูล ER** ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="baea0-128">Sample **ER data model** configuration file</span></span>    | [<span data-ttu-id="baea0-129">แบบจำลองเพื่อเรียนรู้การเรียกแบบพารามิเตอร์.เวอร์ชั่น.1.xml</span><span class="sxs-lookup"><span data-stu-id="baea0-129">Model to learn parameterized calls.version.1.xml</span></span>](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| <span data-ttu-id="baea0-130">ไฟล์การตั้งค่าคอนฟิก **ข้อมูลเมตา ER** ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="baea0-130">Sample **ER metadata** configuration file</span></span>      | [<span data-ttu-id="baea0-131">ข้อมูลเมตาเพื่อเรียนรู้การเรียกแบบพารามิเตอร์.เวอร์ชั่น.1.xml</span><span class="sxs-lookup"><span data-stu-id="baea0-131">Metadata to learn parameterized calls.version.1.xml</span></span>](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| <span data-ttu-id="baea0-132">ไฟล์การตั้งค่าคอนฟิก **การแม็ปแบบจำลอง ER** ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="baea0-132">Sample **ER model mapping** configuration file</span></span> | [<span data-ttu-id="baea0-133">การแม็ปเพื่อเรียนรู้การเรียกแบบพารามิเตอร์.เวอร์ชั่น.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="baea0-133">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| <span data-ttu-id="baea0-134">การตั้งค่าคอนฟิก **รูปแบบ ER** ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="baea0-134">Sample **ER format** configuration</span></span>             | [<span data-ttu-id="baea0-135">รูปแบบเพื่อเรียนรู้การเรียกแบบพารามิเตอร์.เวอร์ชั่น.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="baea0-135">Format to learn parameterized calls.version.1.1.xml</span></span>](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

<span data-ttu-id="baea0-136">ถัดไป ลงชื่อเข้าใช้อินสแตนซ์ RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="baea0-136">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="baea0-137">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="baea0-137">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="baea0-138">ก่อนที่คุณจะสามารถเพื่อทำตามขั้นตอนเหล่านี้ในกระบวนงาน คุณต้องทำขั้นตอนในหัวข้อ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md) ใน RCS ให้เสร็จสมบูรณ์ก่อน</span><span class="sxs-lookup"><span data-stu-id="baea0-138">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="baea0-139">บนแดชบอร์ดเริ่มต้น ให้เลือก **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="baea0-139">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="baea0-140">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="baea0-140">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="baea0-141">นำเข้าการตั้งค่าคอนฟิก ER ที่คุณดาวน์โหลดก่อนหน้านี้ ไปยัง RCS ในคำสั่งต่อไปนี้: แบบจำลองข้อมูล ข้อมูลเมตา การแม็ปแบบจำลอง และ รูปแบบ</span><span class="sxs-lookup"><span data-stu-id="baea0-141">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="baea0-142">สำหรับการตั้งค่าคอนฟิก ER แต่ละรายการ ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="baea0-142">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="baea0-143">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="baea0-143">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="baea0-144">เลือก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="baea0-144">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="baea0-145">เลือก **เรียกดู** เพื่อเลือกไฟล์สำหรับการตั้งค่าคอนฟิก ER ที่จำเป็นในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="baea0-145">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="baea0-146">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="baea0-146">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="baea0-147">ตรวจทานโซลูชัน ER ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="baea0-147">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="baea0-148">ในแผนภูมิการตั้งค่าคอนฟิก ให้ขยายเนื้อหาของรายการ **แบบจำลองเพื่อเรียนรู้การเรียกแบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="baea0-148">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="baea0-149">เลือกรายการ **รูปแบบเพื่อเรียนรู้การเรียกใช้แบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="baea0-149">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="baea0-150">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="baea0-150">Select **Designer**.</span></span>
4.  <span data-ttu-id="baea0-151">เลือก **ขยาย/ยุบ**</span><span class="sxs-lookup"><span data-stu-id="baea0-151">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="baea0-152">รูปแบบ ER **รูปแบบเพื่อเรียนรู้การเรียกใช้แบบพารามิเตอร์** ถูกออกแบบมาเพื่อสร้างใบแจ้งยอดภาษีในรูปแบบ XML ซึ่งแสดงให้ทราบถึงระดับของภาษีต่างๆ (ปกติ ลดลง และ ไม่มี)</span><span class="sxs-lookup"><span data-stu-id="baea0-152">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="baea0-153">แต่ละระดับมีจำนวนรายละเอียดแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="baea0-153">Each level has a different number of details.</span></span>

    ![รูปแบบ ER หลายระดับ รูปแบบในการเรียนรู้การเรียกแบบใช้พารามิเตอร์](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="baea0-155">บนแท็บ **การแม็ป** ให้ขยายรายการ **แบบจำลอง** **ข้อมูล** และ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="baea0-155">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="baea0-156">แหล่งข้อมูล **Model.Data.Summary** ส่งคืนรายการของธุรกรรมภาษี</span><span class="sxs-lookup"><span data-stu-id="baea0-156">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="baea0-157">ธุรกรรมเหล่านี้ถูกสรุปโดยรหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="baea0-157">These transactions are summarized by tax code.</span></span> <span data-ttu-id="baea0-158">สำหรับแหล่งข้อมูลนี้ ฟิลด์ที่คำนวณได้ **Model.Data.Summary.Level** ถูกกำหนดค่าให้ส่งคืนรหัสสำหรับระดับภาษี ของเรกคอร์ดสรุปแต่ละเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="baea0-158">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="baea0-159">สำหรับรหัสภาษีที่สามารถดึงข้อมูลจากแหล่งข้อมูลในช่วงรันไทม์ **Model.Data.Summary** ฟิลด์ที่คำนวณได้จะส่งคืนค่ารหัสระดับภาษี (**ทั่วไป** **ลดลง** **ไม่มี** หรือ **อื่นๆ**) เป็นค่าข้อความ</span><span class="sxs-lookup"><span data-stu-id="baea0-159">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="baea0-160">ฟิลด์ที่คำนวณได้ **Model.Data.Summary.Level** จะใช้เพื่อกรองข้อมูลเรกคอร์ดของแหล่งข้อมูล **Model.Data.Summary** และป้อนข้อมูลที่ถูกกรองในแต่ละองค์ประกอบ XML ที่แสดงถึงระดับภาษีโดยใช้ฟิลด์ **Model.Data2.Level1** **Model.Data2.Level2** และ **Model.Data2.Level3**</span><span class="sxs-lookup"><span data-stu-id="baea0-160">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![รายการแหล่งข้อมูล Model.Data.Summary ของธุรกรรมภาษี](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="baea0-162">ฟิลด์ที่คำนวณได้ **Model.Data.Summary.Level** ซึ่งตั้งค่าคอนฟิก เพื่อให้มีนิพจน์ ER</span><span class="sxs-lookup"><span data-stu-id="baea0-162">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="baea0-163">รหัสภาษี (**VAT19** **InVAT19** **VAT7** **InVAT7** **THIRD** และ **InVAT0**) เป็นฮาร์ดโค้ด ในการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="baea0-163">Tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="baea0-164">ดังนั้น รูปแบบ ER นี้ขึ้นอยู่กับนิติบุคคลที่มีการตั้งค่าคอนฟิกรหัสภาษีเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="baea0-164">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![ฟิลด์ที่คํานวณได้ของ Model.Data.Summary.Level ที่มีรหัสภาษีแบบฮาร์ดโค้ด](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="baea0-166">การสนับสนุนชุดของรหัสภาษีที่แตกต่างกันสำหรับแต่ละนิติบุคคล คุณต้องปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="baea0-166">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="baea0-167">สร้างเวอร์ชันที่สืบทอดมาของรูปแบบ ER สำหรับแต่ละนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="baea0-167">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="baea0-168">อัพเดตรหัสภาษีในฟิลด์ที่คำนวณได้ **Model.Data.Summary.Level** ตามการตั้งค่านิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="baea0-168">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="baea0-169">ปิดหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="baea0-169">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="baea0-170">สร้างรูปแบบที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="baea0-170">Create a derived format</span></span>

<span data-ttu-id="baea0-171">ถัดไป คุณจะใช้คุณลักษณะการทำงานของพารามิเตอร์เฉพาะโปรแกรมประยุกต์ ER เพื่อสนับสนุนชุดของรหัสภาษีที่แตกต่างกัน สำหรับแต่ละนิติบุคคลในรูปแบบ ER เดียว</span><span class="sxs-lookup"><span data-stu-id="baea0-171">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="baea0-172">ในแผนภูมิการตั้งค่าคอนฟิก ให้ขยายเนื้อหาของรายการ **แบบจำลองเพื่อเรียนรู้การเรียกแบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="baea0-172">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="baea0-173">เลือกรายการ **รูปแบบเพื่อเรียนรู้การเรียกใช้แบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="baea0-173">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="baea0-174">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="baea0-174">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="baea0-175">เลือกตัวเลือก **ได้รับมาจากชื่อ: รูปแบบเพื่อเรียนรู้การเรียกแบบพารามิเตอร์, Microsoft**</span><span class="sxs-lookup"><span data-stu-id="baea0-175">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="baea0-176">ในฟิลด์ **ชื่อ** ป้อน **รูปแบบเพื่อเรียนรู้การค้นหาข้อมูล LE**</span><span class="sxs-lookup"><span data-stu-id="baea0-176">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="baea0-177">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="baea0-177">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="baea0-178">ตั้งค่าคอนฟิกรูปแบบที่สืบทอดมา</span><span class="sxs-lookup"><span data-stu-id="baea0-178">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="baea0-179">เพิ่มการแจงนับรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="baea0-179">Add a format enumeration</span></span>

<span data-ttu-id="baea0-180">ถัดไป คุณจะเพิ่มการแจงนับรูปแบบ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="baea0-180">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="baea0-181">ค่าของการแจงนับรูปแบบนี้ จะนำเสนอให้กับผู้ใช้ทางธุรกิจ ซึ่งจะระบุชุดที่ไม่ขึ้นอยู่กับรหัสภาษีสำหรับระดับภาษีต่างๆ ที่ใช้ในรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="baea0-181">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="baea0-182">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="baea0-182">Select **Designer**.</span></span>
2.  <span data-ttu-id="baea0-183">เลือก **รูปแบบการแจงนับ**</span><span class="sxs-lookup"><span data-stu-id="baea0-183">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="baea0-184">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="baea0-184">Select **Add**.</span></span>
4.  <span data-ttu-id="baea0-185">ในฟิลด์ **ชื่อ** ป้อน **รายการของระดับภาษี**</span><span class="sxs-lookup"><span data-stu-id="baea0-185">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="baea0-186">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="baea0-186">Select **Save**.</span></span>
6.  <span data-ttu-id="baea0-187">บนแท็บ **ค่ารูปแบบการแจงนับ** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="baea0-187">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="baea0-188">ในฟิลด์ **ชื่อ** ป้อน **ภาษีปกติ**</span><span class="sxs-lookup"><span data-stu-id="baea0-188">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="baea0-189">เลือก **เพิ่ม** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="baea0-189">Select **Add** again.</span></span>
9.  <span data-ttu-id="baea0-190">ในฟิลด์ **ชื่อ** ป้อน **ภาษีที่ลดลง**</span><span class="sxs-lookup"><span data-stu-id="baea0-190">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="baea0-191">เลือก **เพิ่ม** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="baea0-191">Select **Add** again.</span></span>
11. <span data-ttu-id="baea0-192">ในฟิลด์ **ชื่อ** ป้อน **ไม่มีภาษี**</span><span class="sxs-lookup"><span data-stu-id="baea0-192">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="baea0-193">เลือก **เพิ่ม** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="baea0-193">Select **Add** again.</span></span>
13. <span data-ttu-id="baea0-194">ในฟิลด์ **ชื่อ** ให้ป้อน **อื่นๆ**</span><span class="sxs-lookup"><span data-stu-id="baea0-194">In the **Name** field, enter **Other**.</span></span>

    ![เรกคอร์ดใหม่ในหน้าการแจงนับรูปแบบ](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="baea0-196">เนื่องจากผู้ใช้ที่เป็นธุรกิจอาจใช้ภาษาต่างๆ เพื่อระบุชุดของรหัสภาษีที่ไม่ขึ้นอยู่กับค่าที่เป็นของนิติบุคคล เราขอแนะนำให้คุณแปลค่าของการแจงนับนี้เป็นภาษาที่ได้รับการตั้งค่าคอนฟิกเป็นภาษาที่ต้องการสำหรับผู้ใช้เหล่านั้นในการเงิน</span><span class="sxs-lookup"><span data-stu-id="baea0-196">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="baea0-197">เลือกเรกคอร์ด **ไม่มีภาษี**</span><span class="sxs-lookup"><span data-stu-id="baea0-197">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="baea0-198">คลิก ในฟิลด์ **ป้ายชื่อ**</span><span class="sxs-lookup"><span data-stu-id="baea0-198">Click in the **Label** field.</span></span>
16. <span data-ttu-id="baea0-199">เลือก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="baea0-199">Select **Translate**.</span></span>
17. <span data-ttu-id="baea0-200">ในบานหน้าต่าง **การแปลข้อความ** ในฟิลด์ **รหัสป้ายชื่อ** ให้ป้อน **LBL_LEVELENUM_NO**</span><span class="sxs-lookup"><span data-stu-id="baea0-200">In the **Text translation** pane, in the **Label ID** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="baea0-201">ในฟิลด์ **ข้อความในภาษาเริ่มต้น** ให้ป้อน **ไม่มีภาษี**</span><span class="sxs-lookup"><span data-stu-id="baea0-201">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="baea0-202">ในฟิลด์ **ภาษา** เลือก **DE**</span><span class="sxs-lookup"><span data-stu-id="baea0-202">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="baea0-203">ในฟิลด์ **ข้อความที่แปล** ให้ป้อน **ไม่มีภาษี**</span><span class="sxs-lookup"><span data-stu-id="baea0-203">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="baea0-204">เลือก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="baea0-204">Select **Translate**.</span></span>

    ![slide out ของการแปลข้อความ](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="baea0-206">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="baea0-206">Select **Save**.</span></span>
23. <span data-ttu-id="baea0-207">ปิดหน้า **การแจงนับรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="baea0-207">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="baea0-208">เพิ่มแหล่งข้อมูลการค้นหาใหม่</span><span class="sxs-lookup"><span data-stu-id="baea0-208">Add a new lookup data source</span></span>

<span data-ttu-id="baea0-209">ถัดไป คุณจะเพิ่มแหล่งข้อมูลใหม่เพื่อระบุวิธีการที่ผู้ใช้ทางธุรกิจจะระบุกฎที่เป็นไปตามนิติบุคคล เพื่อจดจำระดับภาษีที่ถูกต้อง สำหรับแต่ละเรกคอร์ดธุรกรรมสรุป</span><span class="sxs-lookup"><span data-stu-id="baea0-209">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="baea0-210">บนแท็บ **การแม็ป** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="baea0-210">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="baea0-211">เลือก **รูปแบบการแจงนับ\การค้นหา**</span><span class="sxs-lookup"><span data-stu-id="baea0-211">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="baea0-212">คุณสามารถระบุได้ว่ากฎแต่ละกฎที่ผู้ใช้ธุรกิจระบุสำหรับการรับรู้ระดับภาษี จะส่งคืนค่าของการแจงนับรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="baea0-212">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="baea0-213">โปรดสังเกตว่าชนิดแหล่งข้อมูล **การค้นหา** สามารถเข้าถึงได้ภายใต้ **แบบจำลองข้อมูล** และบล็อค **Dynamics 365 for Operations** ที่เพิ่มมา ไปยังบล็อค **การแจงนับของรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="baea0-213">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="baea0-214">ดังนั้น การแจงนับแบบจำลองข้อมูล ER และการแจงนับของโปรแกรมประยุกต์ สามารถใช้เพื่อระบุชนิดของค่าที่ส่งคืน สำหรับแหล่งข้อมูลของชนิดนั้น</span><span class="sxs-lookup"><span data-stu-id="baea0-214">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that are returned for data sources of that type.</span></span> <span data-ttu-id="baea0-215">หากต้องการทราบเกี่ยวกับแหล่งข้อมูล **การค้นหา** ให้ดูที่ [ตั้งค่าคอนฟิกแหล่งข้อมูลการค้นหา เพื่อใช้ลักษณะการเช่น พารามิเตอร์เฉพาะโปรแกรมประยุกต์ ER](er-lookup-data-sources.md)</span><span class="sxs-lookup"><span data-stu-id="baea0-215">To learn more about the **Lookup** data sources, see [Configure Lookup data sources to use the ER application-specific parameters feature](er-lookup-data-sources.md).</span></span>
    
3.  <span data-ttu-id="baea0-216">ในฟิลด์ **ชื่อ** ให้ป้อน **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="baea0-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="baea0-217">ในฟิลด์ **การแจงนับรูปแบบ** ป้อน **รายการของระดับภาษี**</span><span class="sxs-lookup"><span data-stu-id="baea0-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="baea0-218">คุณได้ระบุ สำหรับแต่ละกฎที่ระบุไว้ในแหล่งข้อมูลนี้ ผู้ใช้ที่เป็นธุรกิจต้องเลือกค่าของการแจงนับรูปแบบ **รายการของระดับภาษี** เป็นค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="baea0-218">You specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="baea0-219">เลือก **แก้ไขการค้นหา**</span><span class="sxs-lookup"><span data-stu-id="baea0-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="baea0-220">เลือก **คอลัมน์**</span><span class="sxs-lookup"><span data-stu-id="baea0-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="baea0-221">ขยายรายการ **Model**</span><span class="sxs-lookup"><span data-stu-id="baea0-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="baea0-222">ขยายรายการ **ข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="baea0-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="baea0-223">ขยายรายการ **ภาษี**</span><span class="sxs-lookup"><span data-stu-id="baea0-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="baea0-224">เลือกรายการ **Model.Data.Tax.Code**</span><span class="sxs-lookup"><span data-stu-id="baea0-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="baea0-225">เลือกปุ่ม **เพิ่ม** (ลูกศรขวา)</span><span class="sxs-lookup"><span data-stu-id="baea0-225">Select the **Add** button (the right arrow).</span></span>

    ![slide out ของคอลัมน์](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="baea0-227">คุณได้ระบุ สำหรับแต่ละกฎที่ระบุไว้ในแหล่งข้อมูลนี้สำหรับการรับรู้ระดับภาษี ผู้ใช้ที่เป็นธุรกิจต้องเลือกค่ารหัสภาษีเป็นเงี่อนไข</span><span class="sxs-lookup"><span data-stu-id="baea0-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="baea0-228">รายการของรหัสภาษีที่ผู้ใช้ทางธุรกิจสามารถเลือกได้จะถูกส่งคืนโดยแหล่งข้อมูล **Model.Data.Tax**</span><span class="sxs-lookup"><span data-stu-id="baea0-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="baea0-229">เนื่องจากแหล่งข้อมูลนี้มีฟิลด์ **ชื่อ** ชื่อรหัสภาษีจะแสดงขึ้นสำหรับแต่ละค่ารหัสภาษี ในการค้นหาที่นำเสนอให้แก่ผู้ใช้ทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="baea0-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="baea0-230">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="baea0-230">Select **OK**.</span></span>

    ![หน้าตัวออกแบบการค้นหา](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="baea0-232">ผู้ใช้ทางธุรกิจสามารถเพิ่มกฎหลายกฎเป็นเรกคอร์ดของแหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="baea0-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="baea0-233">แต่ละเรกคอร์ดจะมีการกำหนดหมายเลขโดยรหัสบรรทัด</span><span class="sxs-lookup"><span data-stu-id="baea0-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="baea0-234">กฎจะถูกประเมินตามลำดับหมายเลขบรรทัดที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="baea0-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="baea0-235">เนื่องจากคุณเลือกฟิลด์ **รหัสภาษี** เป็นเงื่อนไขสำหรับกฎในแหล่งข้อมูลการค้นหานี้ และเนื่องจาก **รหัสภาษี** ถูกตั้งค่าเป็นฟิลด์ของชนิดข้อมูล **สตริง** แต่ละกฎจะถูกประเมินที่รันไทม์ โดยการเปรียบเทียบรหัสภาษีที่ส่งผ่านไปยังแหล่งข้อมูลที่มีรหัสภาษีที่กำหนดไว้ในเรกคอร์ดนี้ของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="baea0-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="baea0-236">เมื่อพบกฎที่เป็นไปตามเงื่อนไขที่ตั้งค่าคอนฟิก แหล่งข้อมูลนี้จะส่งคืนค่าการค้นหาของกฎที่กำหนดไว้ในฟิลด์ **ผลการค้นหา**</span><span class="sxs-lookup"><span data-stu-id="baea0-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="baea0-237">ถ้าไม่พบกฎ ข้อยกเว้นจะถูกโยนเพื่อแจ้งให้ผู้ใช้ทราบว่าแหล่งข้อมูลปัจจุบันไม่สามารถส่งคืนค่าที่ถูกต้องได้</span><span class="sxs-lookup"><span data-stu-id="baea0-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="baea0-238">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="baea0-238">Select **Save**.</span></span>
14. <span data-ttu-id="baea0-239">ปิดหน้า **ตัวออกแบบการค้นหา**</span><span class="sxs-lookup"><span data-stu-id="baea0-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="baea0-240">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="baea0-240">Select **OK**.</span></span>

    <span data-ttu-id="baea0-241">โปรดสังเกตว่าคุณได้เพิ่มแหล่งข้อมูลใหม่ที่จะส่งคืนระดับภาษีเป็นค่าของการแจงนับรูปแบบ **รายการของระดับภาษี** สำหรับรหัสภาษีใดๆ ที่ส่งผ่านไปยังแหล่งข้อมูลเป็นอาร์กิวเมนต์ของพารามิเตอร์ **รหัส** ของชนิดข้อมูล **สตริง**</span><span class="sxs-lookup"><span data-stu-id="baea0-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![หน้าตัวออกแบบรูปแบบที่มีแหล่งข้อมูลใหม่](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="baea0-243">การประเมินกฎที่ตั้งค่าคอนฟิก จะขึ้นอยู่กับชนิดข้อมูลของฟิลด์ที่เลือกเพื่อกำหนดเงื่อนไขของกฎเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="baea0-243">The evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="baea0-244">เมื่อคุณเลือกฟิลด์ที่มีการตั้งค่าคอนฟิกเป็นฟิลด์ของชนิดข้อมูล **ตัวเลข** หรือ **วันที่** เกณฑ์จะแตกต่างจากเงื่อนไขที่อธิบายไว้ก่อนหน้านี้สำหรับชนิดข้อมูล **สตริง**</span><span class="sxs-lookup"><span data-stu-id="baea0-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="baea0-245">สำหรับฟิลด์ **ตัวเลข** และ **วันที่** กฎต้องมีการระบุเป็นช่วงของค่า</span><span class="sxs-lookup"><span data-stu-id="baea0-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="baea0-246">เงื่อนไขของกฎจะถูกพิจารณาความพึงพอใจ เมื่อค่าที่ส่งผ่านไปยังแหล่งข้อมูลอยู่ในช่วงที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="baea0-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="baea0-247">ภาพประกอบต่อไปนี้ แสดงตัวอย่างของการตั้งค่าของชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="baea0-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="baea0-248">นอกจากฟิลด์ **Model.Data.Tax.Code** ของชนิดข้อมูล **สตริง** ฟิลด์ **Model.Tax.Summary.Base** ของชนิดข้อมูล **จริง** จะใช้เพื่อระบุเงื่อนไขสำหรับแหล่งข้อมูลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="baea0-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![หน้าตัวออกแบบการค้นหาที่มีคอลัมน์เพิ่มเติม](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="baea0-250">เนื่องจากฟิลด์ **Model.Data.Tax.Code** และ **Model.Tax.Summary.Base** ถูกเลือกสำหรับแหล่งข้อมูลการค้นหานี้ แต่ละกฎของแหล่งข้อมูลนี้จะได้รับการตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="baea0-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="baea0-251">ในรายการที่แสดง ค่าของการแจงนับรูปแบบ **รายการของระดับภาษี** ต้องถูกเลือกเป็นค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="baea0-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="baea0-252">รหัสภาษีต้องถูแป้อน เป็นเงื่อนไขของกฎนี้</span><span class="sxs-lookup"><span data-stu-id="baea0-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="baea0-253">เฉพาะรหัสภาษีที่ได้รับมาจากแหล่งข้อมูล **Model.Data.Tax** เท่านั้น ที่สามารถใช้แหล่งข้อมูลภาษีได้</span><span class="sxs-lookup"><span data-stu-id="baea0-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="baea0-254">ค่าต่ำสุดและสูงสุดของจำนวนเงินฐานภาษี ต้องถูกป้อนค่าตามเงื่อนไขของกฎนี้</span><span class="sxs-lookup"><span data-stu-id="baea0-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="baea0-255">ต่อไปนี้เป็นวิธีการประเมินแต่ละกฎของแหล่งข้อมูลนี้เมื่อรันไทม์:</span><span class="sxs-lookup"><span data-stu-id="baea0-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="baea0-256">รหัสของชนิดข้อมูล **สตริง** ที่ส่งผ่านไปยังแหล่งข้อมูลนี้ เท่ากับรหัสภาษีของกฎหรือไม่</span><span class="sxs-lookup"><span data-stu-id="baea0-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="baea0-257">ค่าของชนิดข้อมูล **จริง** ที่ส่งผ่านไปยังแหล่งข้อมูลนี้ อยู่ระหว่างค่าต่ำสุดและค่าสูงสุดที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="baea0-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="baea0-258">กฎจะมีผลบังคับใช้เมื่อเงื่อนไขทั้งสองเป็นที่น่าพอใจ</span><span class="sxs-lookup"><span data-stu-id="baea0-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="baea0-259">แปลป้ายชื่อของแหล่งข้อมูลการค้นหาที่ถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="baea0-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="baea0-260">เนื่องจากผู้ใช้ทางธุรกิจอาจใช้ภาษาต่างๆ เพื่อระบุชุดของรหัสภาษีที่ไม่ขึ้นอยู่กับนิติบุคคล เราขอแนะนำให้คุณแปลป้ายชื่อของแหล่งข้อมูลการค้นหาใดๆ ที่คุณเพิ่ม ซึ่งจะแสดงในแต่ละภาษีที่ผู้ใช้ต้องการบนหน้าที่สัมพันธ์กัน</span><span class="sxs-lookup"><span data-stu-id="baea0-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="baea0-261">เลือกแหล่งข้อมูล **Model.Data.Selector**</span><span class="sxs-lookup"><span data-stu-id="baea0-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="baea0-262">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="baea0-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="baea0-263">คลิก ในฟิลด์ **ป้ายชื่อ**</span><span class="sxs-lookup"><span data-stu-id="baea0-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="baea0-264">เลือก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="baea0-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="baea0-265">ในบานหน้าต่าง **การแปลข้อความ** ในฟิลด์ **รหัสป้ายชื่อ** ให้ป้อน **LBL_SELECTOR_DS**</span><span class="sxs-lookup"><span data-stu-id="baea0-265">In the **Text translation** pane, in the **Label ID** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="baea0-266">ในฟิลด์ **ข้อความในภาษาเริ่มต้น** ป้อน **เลือกระดับภาษีตามรหัสภาษี**</span><span class="sxs-lookup"><span data-stu-id="baea0-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="baea0-267">ในฟิลด์ **ภาษา** เลือก **DE**</span><span class="sxs-lookup"><span data-stu-id="baea0-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="baea0-268">ในฟิลด์ **ข้อความที่แปล** ให้ป้อน **เลือกระดับภาษีสำหรับรหัสภาษี**</span><span class="sxs-lookup"><span data-stu-id="baea0-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="baea0-269">เลือก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="baea0-269">Select **Translate**.</span></span>
10. <span data-ttu-id="baea0-270">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="baea0-270">Select **OK**.</span></span>

    ![slide out ของคุณสมบัติแหล่งข้อมูล](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="baea0-272">เพิ่มฟิลด์ใหม่เพื่อใช้การค้นหาที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="baea0-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="baea0-273">ขยายรายการ **Model.Data**</span><span class="sxs-lookup"><span data-stu-id="baea0-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="baea0-274">เลือกรายการ **Model.Data.Summary**</span><span class="sxs-lookup"><span data-stu-id="baea0-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="baea0-275">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="baea0-275">Select **Add**.</span></span>
4.  <span data-ttu-id="baea0-276">เลือก **ฟังก์ชัน/ฟิลด์ที่คำนวณได้**</span><span class="sxs-lookup"><span data-stu-id="baea0-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="baea0-277">ในฟิลด์ **ชื่อ** ให้ป้อน **LevelByLookup**</span><span class="sxs-lookup"><span data-stu-id="baea0-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="baea0-278">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="baea0-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="baea0-279">ใน **ฟิลด์สูตร** ให้ป้อน **Model.Selector(Model.Data.Summary.Code)**</span><span class="sxs-lookup"><span data-stu-id="baea0-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="baea0-280">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="baea0-280">Select **Save**.</span></span>

    ![การเพิ่ม Model.Selector (Model.Data.Summary.Code) ลงในหน้าตัวออกแบบสูตร](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="baea0-282">ปิดหน้า **ตัวแก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="baea0-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="baea0-283">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="baea0-283">Select **OK**.</span></span>

    ![หน้าตัวออกแบบรูปแบบที่มีการเพิ่มสูตรใหม่](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="baea0-285&quot;>โปรดสังเกตว่าฟิลด์ที่คำนวณได้ **LevelByLookup** ที่คุณเพิ่ม จะส่งคืนระดับภาษีเป็นค่าของการแจงนับรูปแบบ **รายการของระดับภาษี** สำหรับเรกคอร์ดธุรกรรมภาษีแบบสรุปแต่ละเรกคอร์ด</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-285&quot;>Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id=&quot;baea0-286&quot;>รหัสภาษีของเรกคอร์ดจะถูกส่งผ่านไปยังแหล่งข้อมูลการค้นหา **Model.Selector** และชุดของกฎสำหรับแหล่งข้อมูลนี้จะใช้ในการเลือกระดับภาษีที่ถูกต้อง</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-286&quot;>The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name=&quot;add-a-new-format-enumeration-based-data-source&quot;></a><span data-ttu-id=&quot;baea0-287&quot;>เพิ่มแหล่งข้อมูลตามการแจงนับรูปแบบใหม่</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-287&quot;>Add a new format enumeration-based data source</span></span>

<span data-ttu-id=&quot;baea0-288&quot;>ถัดไป คุณจะเพิ่มแหล่งข้อมูลใหม่ที่อ้างอิงถึงการแจงนับรูปแบบที่คุณเพิ่มไว้ก่อนหน้านี้</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-288&quot;>Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id=&quot;baea0-289&quot;>ค่าของแหล่งข้อมูลนี้จะใช้ในนิพจน์รูปแบบ ER ในภายหลัง</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-289&quot;>Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id=&quot;baea0-290&quot;>เลือก **เพิ่มราก**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-290&quot;>Select **Add root**.</span></span>
2.  <span data-ttu-id=&quot;baea0-291&quot;>เลือก **การแจงนับรูปแบบ\การแจงนับ**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-291&quot;>Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id=&quot;baea0-292&quot;>ในฟิลด์ **ชื่อ** ป้อน **TaxationLevel**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-292&quot;>In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id=&quot;baea0-293&quot;>ในฟิลด์ **การแจงนับรูปแบบ** ป้อน **รายการของระดับภาษี**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-293&quot;>In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id=&quot;baea0-294&quot;>เลือก **บันทึก**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-294&quot;>Select **Save**.</span></span>

### <a name=&quot;modify-an-existing-field-to-start-to-use-the-lookup&quot;></a><span data-ttu-id=&quot;baea0-295&quot;>แก้ไขฟิลด์ที่มีอยู่เพื่อเริ่มต้นใช้งานการค้นหา</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-295&quot;>Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id=&quot;baea0-296&quot;>ถัดไป คุณจะแก้ไขฟิลด์ที่คำนวณที่มีอยู่เพื่อให้ใช้แหล่งข้อมูลการค้นหาที่ตั้งค่าคอนฟิก เพื่อส่งคืนค่าระดับภาษีที่ถูกต้อง ทั้งนี้ขึ้นอยู่กับรหัสภาษี</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-296&quot;>Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id=&quot;baea0-297&quot;>เลือกรายการ **Model.Data.Summary.Level**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-297&quot;>Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id=&quot;baea0-298&quot;>เลือก **แก้ไข**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-298&quot;>Select **Edit**.</span></span>
3.  <span data-ttu-id=&quot;baea0-299&quot;>เลือก **แก้ไขสูตร**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-299&quot;>Select **Edit formula**.</span></span>

    <span data-ttu-id=&quot;baea0-300&quot;>โปรดสังเกตว่านิพจน์ปัจจุบันของฟิลด์ **Model.Data.Summary.Level** จะรวมรหัสภาษีที่มีรหัสแบบตายตัวต่อไปนี้:</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;baea0-300&quot;>Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id=&quot;baea0-301&quot;>CASE (@.Code, &quot;VAT19&quot;, &quot;Regular&quot;, &quot;InVAT19&quot;, &quot;Regular&quot;, &quot;VAT7&quot;, &quot;Reduced&quot;, &quot;InVAT7&quot;, &quot;Reduced&quot;, &quot;THIRD&quot;, &quot;None&quot;, &quot;InVAT0&quot;, &quot;None&quot;, &quot;Other")</span><span class="sxs-lookup"><span data-stu-id="baea0-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="baea0-302">ในฟิลด์ **สูตร** ให้ป้อน **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**</span><span class="sxs-lookup"><span data-stu-id="baea0-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="baea0-304">โปรดสังเกตว่านิพจน์ของฟิลด์ **Model.Data.Summary.Level** จะส่งคืนระดับภาษี ขึ้นอยู่กับรหัสภาษีของเรกคอร์ดปัจจุบัน และชุดของกฎที่ผู้ใช้ทางธุรกิจมีการตั้งค่าคอนฟิกในแหล่งข้อมูลการค้นหา **Model.Data.Selector**</span><span class="sxs-lookup"><span data-stu-id="baea0-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="baea0-305">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="baea0-305">Select **Save**.</span></span>
6.  <span data-ttu-id="baea0-306">ปิดหน้า **ตัวออกแบบสูตร**</span><span class="sxs-lookup"><span data-stu-id="baea0-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="baea0-307">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="baea0-307">Select **OK**.</span></span>
8.  <span data-ttu-id="baea0-308">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="baea0-308">Select **Save**.</span></span>
9.  <span data-ttu-id="baea0-309">ปิดหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="baea0-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="baea0-310">เวอร์ชันแบบร่างเสร็จสมบูรณ์ของรูปแบบที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="baea0-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="baea0-311">บน FastTab **เวอร์ชัน** เลือก **เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="baea0-311">On the **Versions** FastTab, select **Change status**.</span></span>
2.  <span data-ttu-id="baea0-312">เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="baea0-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="baea0-313">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="baea0-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="baea0-314">ส่งออกเวอร์ชันที่เสร็จสมบูรณ์ของรูปแบบที่แก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="baea0-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="baea0-315">ในแผนภูมิการตั้งค่าคอนฟิก ให้เลือกรายการ **รูปแบบเพื่อเรียนรู้วิธีการค้นหาข้อมูล LE**</span><span class="sxs-lookup"><span data-stu-id="baea0-315">In the configuration tree, select the **Format to learn how to look up LE data** item.</span></span>
2.  <span data-ttu-id="baea0-316">บน FastTab **เวอร์ชัน** ให้เลือกเรกคอร์ดที่มีสถานะเป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="baea0-316">On the **Versions** FastTab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="baea0-317">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="baea0-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="baea0-318">เลือก **ส่งออกเป็นไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="baea0-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="baea0-319">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="baea0-319">Select **OK**.</span></span>
6.  <span data-ttu-id="baea0-320">เว็บเบราเซอร์จะดาวน์โหลดไฟล์ **รูปแบบเพื่อเรียนรู้วิธีการค้นหา LE data.xml**</span><span class="sxs-lookup"><span data-stu-id="baea0-320">The web browser downloads a **Format to learn how to look up LE data.xml** file.</span></span> <span data-ttu-id="baea0-321">จัดเก็บไฟล์นี้ไว้ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="baea0-321">Store this file locally.</span></span>

<span data-ttu-id="baea0-322">ทำซ้ำขั้นตอนในส่วนนี้ สำหรับรายการหลักของรูปแบบ **รูปแบบเพื่อเรียนรู้วิธีการค้นหารูปแบบข้อมูล LE** และจัดเก็บไฟล์ต่อไปนี้ในเครื่อง:</span><span class="sxs-lookup"><span data-stu-id="baea0-322">Repeat steps in this section for parent items of the **Format to learn how to look up LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="baea0-323">รูปแบบเพื่อเรียนรู้ calls.xml แบบพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="baea0-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="baea0-324">การแม็ปเพื่อเรียนรู้ calls.xml แบบพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="baea0-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="baea0-325">แบบจำลองเพื่อเรียนรู้ calls.xml แบบพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="baea0-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="baea0-326">การเรียนรู้วิธีการรูปแบบ ER **เรียนรู้วิธีการค้นหาข้อมูล LE** ที่ตั้งค่าคอนฟิก เพื่อตั้งค่ารหัสภาษีของชุดที่ขึ้นกับนิติบุคคล เพื่อกรองธุรกรรมภาษี โดยระดับภาษีที่ต่างกัน ให้ทำตามขั้นต่อนในหัวข้อ [ตั้งค่าพารามิเตอร์ของรูปแบบ ER สำหรับแต่ละนิติบุคคล](er-app-specific-parameters-set-up.md) ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="baea0-326">To learn how to use the configured **Format to learn how to look up LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="baea0-327">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="baea0-327">Additional resources</span></span>

[<span data-ttu-id="baea0-328">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="baea0-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="baea0-329">ตั้งค่าพารามิเตอร์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์สำหรับนิติบุคคลแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="baea0-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)

[<span data-ttu-id="baea0-330">ตั้งค่าคอนฟิกแหล่งข้อมูลการค้นหาเพื่อใช้คุณลักษณะพารามิเตอร์เฉพาะโปรแกรมประยุกต์ ER</span><span class="sxs-lookup"><span data-stu-id="baea0-330">Configure Lookup data sources to use the ER application-specific parameters feature</span></span>](er-lookup-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
