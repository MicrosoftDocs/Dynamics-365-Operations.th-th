---
title: ตั้งค่าคอนฟิกรูปแบบ ER เพื่อใช้พารามิเตอร์ที่ระบุสำหรับแต่ละนิติบุคคล
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้พารามิเตอร์ที่ระบุไว้สำหรับแต่ละนิติบุคคล
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 0ed1442403ae82dfc820212e3e235737f37f21a4
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679737"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="8ae40-103">ตั้งค่าคอนฟิกรูปแบบ ER เพื่อใช้พารามิเตอร์ที่ระบุสำหรับแต่ละนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ae40-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="8ae40-104">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="8ae40-104">Overview</span></span>

<span data-ttu-id="8ae40-105">ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) หลายรูปแบบที่คุณจะออกแบบ คุณต้องกรองข้อมูลโดยใช้ชุดของค่าที่เกี่ยวข้องกับแต่ละนิติบุคคลของอินสแตนซ์ของคุณ (ตัวอย่าง เช่น ชุดของรหัสภาษีที่จะกรองข้อมูลธุรกรรมภาษี)</span><span class="sxs-lookup"><span data-stu-id="8ae40-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="8ae40-106">ในขณะนี้ เมื่อกรองชนิดนี้มีการตั้งค่าคอนฟิกในรูปแบบ ER ค่าที่ขึ้นอยู่กับนิติบุคคล (ตัวอย่าง เช่น รหัสภาษี) จะใช้ในนิพจน์ของรูปแบบ ER เพื่อระบุกฎการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8ae40-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="8ae40-107">ดังนั้น รูปแบบ ER จึงทำให้นิติบุคคล–เฉพาะเจาะจง และเพื่อสร้างรายงานที่จำเป็น คุณต้องสร้างสำเนาที่สืบทอดมาของรูปแบบ ER ดั้งเดิม สำหรับแต่ละนิติบุคคลที่คุณต้องรันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="8ae40-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="8ae40-108">แต่ละรูปแบบ ER ที่สืบทอดมาต้องได้รับการแก้ไข เพื่อดึงข้อมูลค่านิติบุคคล–เฉพาะ ข้างใน ปรับใช้เมื่อใดก็ตามที่มีการอัพเดตเวอร์ชันดั้งเดิม (พื้นฐาน) แล้วส่งออกจากสภาพแวดล้อมการทดสอบ และนำเข้าไปยังสภาพแวดล้อมการใช้งานจริง เมื่อต้องปรับใช้สำหรับการใช้งานจริง และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="8ae40-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="8ae40-109">ดังนั้น การบำรุงรักษาชนิดของโซลูชัน ER ที่ตั้งค่าคอนฟิกนี้ ค่อนข้างจะซับซ้อนและใช้เวลานานหลายประการดังนี้:</span><span class="sxs-lookup"><span data-stu-id="8ae40-109">Therefore, maintenance of this type of configured ER solution is quite complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="8ae40-110">ยิ่งเป็นนิติบุคคลมากเท่าไร ยิ่งต้องรักษาการกำหนดค่ารูปแบบ ER มากเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8ae40-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="8ae40-111">การบำรุงรักษาของการตั้งค่าคอนฟิก ER กำหนดให้ผู้ใช้ที่เป็นธุรกิจต้องมีความรู้ ER</span><span class="sxs-lookup"><span data-stu-id="8ae40-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="8ae40-112">คุณลักษณะพารามิเตอร์เฉพาะของโปรแกรมประยุกต์ ER ให้ผู้ใช้ระดับสูงตั้งค่าคอนฟิกการกรองข้อมูลในรูปแบบ ER ซึ่งขึ้นอยู่กับชุดของกฎนามธรรม</span><span class="sxs-lookup"><span data-stu-id="8ae40-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="8ae40-113">ชุดของกฎนี้สามารถตั้งค่าคอนฟิกให้ใช้แหล่งข้อมูลที่มีอยู่ในรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="8ae40-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="8ae40-114">ผู้ใช้ทางธุรกิจสามารถระบุกฎจริงนอกเหนือจากกรอบงาน ER โดยใช้อินเทอร์เฟสผู้ใช้ (UI) ซึ่งสร้างขึ้นโดยอัตโนมัติตามการตั้งค่าของรูปแบบ ER ที่สอดคล้องกัน และข้อมูลนิติบุคคลปัจจุบัน ที่จะเข้าถึงโดยแหล่งข้อมูลของรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="8ae40-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="8ae40-115">ชุดของกฎที่ระบุสำหรับรูปแบบ ER สามารถส่งออกจากนิติบุคคลปัจจุบันของอินสแตนซ์ Dynamics 365 Finance (การเงิน)</span><span class="sxs-lookup"><span data-stu-id="8ae40-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="8ae40-116">จากนั้นจึงสามารถนำเข้าไปยังนิติบุคคลอื่นของอินสแตนซ์ทางการเงินเดียวกัน หรืออินสแตนซ์ที่แตกต่างกัน เป็นชุดของกฎสำหรับรูปแบบ ER เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8ae40-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8ae40-117">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8ae40-117">Prerequisites</span></span>

<span data-ttu-id="8ae40-118">การทำตัวอย่างในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณต้องเข้าถึงอินสแตนซ์ของ Regulatory Configuration Services (RCS) ที่ได้เตรียมใช้งานสำหรับผู้เช่ารายเดียวกันกับ Finance สำหรับหนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8ae40-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="8ae40-119">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="8ae40-119">Electronic reporting developer</span></span>
- <span data-ttu-id="8ae40-120">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="8ae40-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="8ae40-121">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="8ae40-121">System administrator</span></span>

<span data-ttu-id="8ae40-122">เราขอแนะนำให้คุณทำตามขั้นตอนให้สำเร็จ ในหัวข้อ [สนับสนุนการเรียกแบบใช้พารามิเตอร์ของแหล่งข้อมูล ER ของชนิดฟิลด์ที่คำนวณได้](er-calculated-field-type.md)</span><span class="sxs-lookup"><span data-stu-id="8ae40-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="8ae40-123">ถ้าคุณดำเนินการขั้นตอนดังกล่าวเสร็จเรียบร้อยแล้ วคุณสามารถข้ามขั้นตอนในส่วน **นำเข้าการตั้งค่าคอนฟิก ER ลงใน RCS** ที่ตามมา</span><span class="sxs-lookup"><span data-stu-id="8ae40-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="8ae40-124">นำเข้าการตั้งค่าคอนฟิก ER ลงใน RCS</span><span class="sxs-lookup"><span data-stu-id="8ae40-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="8ae40-125">จาก [ศูนย์ดาวน์โหลดของ Microsoft](https://go.microsoft.com/fwlink/?linkid=851448) ดาวน์โหลดไฟล์ zip **สนับสนุนการเรียกแบบพารามิเตอร์ของแหล่งข้อมูล ER ของชนิดฟิลด์ที่คำนวณได้**</span><span class="sxs-lookup"><span data-stu-id="8ae40-125">From [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448), download the **Support parameterized calls of ER data sources of CALCULATED FIELD type** zip file.</span></span> <span data-ttu-id="8ae40-126">ไฟล์ zip นี้ประกอบด้วยการตั้งค่าคอนฟิก ER ต่อไปนี้ ที่ต้องถูกแยกและจัดเก็บไว้ภายใน</span><span class="sxs-lookup"><span data-stu-id="8ae40-126">This zip file contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="8ae40-127">**คำอธิบายเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="8ae40-127">**Content description**</span></span>                        | <span data-ttu-id="8ae40-128">**ชื่อไฟล์**</span><span class="sxs-lookup"><span data-stu-id="8ae40-128">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ae40-129">ไฟล์การตั้งค่าคอนฟิก **แบบจำลองข้อมูล ER** ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8ae40-129">Sample **ER data model** configuration file</span></span>    | <span data-ttu-id="8ae40-130">แบบจำลองเพื่อเรียนรู้การเรียกแบบพารามิเตอร์.เวอร์ชั่น.1.xml</span><span class="sxs-lookup"><span data-stu-id="8ae40-130">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="8ae40-131">ไฟล์การตั้งค่าคอนฟิก **ข้อมูลเมตา ER** ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8ae40-131">Sample **ER metadata** configuration file</span></span>      | <span data-ttu-id="8ae40-132">ข้อมูลเมตาเพื่อเรียนรู้การเรียกแบบพารามิเตอร์.เวอร์ชั่น.1.xml</span><span class="sxs-lookup"><span data-stu-id="8ae40-132">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="8ae40-133">ไฟล์การตั้งค่าคอนฟิก **การแม็ปแบบจำลอง ER** ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8ae40-133">Sample **ER model mapping** configuration file</span></span> | <span data-ttu-id="8ae40-134">การแม็ปเพื่อเรียนรู้การเรียกแบบพารามิเตอร์.เวอร์ชั่น.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="8ae40-134">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="8ae40-135">การตั้งค่าคอนฟิก **รูปแบบ ER** ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8ae40-135">Sample **ER format** configuration</span></span>             | <span data-ttu-id="8ae40-136">รูปแบบเพื่อเรียนรู้การเรียกแบบพารามิเตอร์.เวอร์ชั่น.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="8ae40-136">Format to learn parameterized calls.version.1.1.xml</span></span>  |

<span data-ttu-id="8ae40-137">ถัดไป ลงชื่อเข้าใช้อินสแตนซ์ RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8ae40-137">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="8ae40-138">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="8ae40-138">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="8ae40-139">ก่อนที่คุณจะสามารถเพื่อทำตามขั้นตอนเหล่านี้ในกระบวนงาน คุณต้องทำขั้นตอนในหัวข้อ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md) ใน RCS ให้เสร็จสมบูรณ์ก่อน</span><span class="sxs-lookup"><span data-stu-id="8ae40-139">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="8ae40-140">บนแดชบอร์ดเริ่มต้น ให้เลือก **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="8ae40-140">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="8ae40-141">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="8ae40-141">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="8ae40-142">นำเข้าการตั้งค่าคอนฟิก ER ที่คุณดาวน์โหลดก่อนหน้านี้ ไปยัง RCS ในคำสั่งต่อไปนี้: แบบจำลองข้อมูล ข้อมูลเมตา การแม็ปแบบจำลอง และ รูปแบบ</span><span class="sxs-lookup"><span data-stu-id="8ae40-142">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="8ae40-143">สำหรับการตั้งค่าคอนฟิก ER แต่ละรายการ ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="8ae40-143">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="8ae40-144">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="8ae40-144">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="8ae40-145">เลือก **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="8ae40-145">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="8ae40-146">เลือก **เรียกดู** เพื่อเลือกไฟล์สำหรับการตั้งค่าคอนฟิก ER ที่จำเป็นในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="8ae40-146">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="8ae40-147">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8ae40-147">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="8ae40-148">ตรวจทานโซลูชัน ER ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="8ae40-148">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="8ae40-149">ในแผนภูมิการตั้งค่าคอนฟิก ให้ขยายเนื้อหาของรายการ **แบบจำลองเพื่อเรียนรู้การเรียกแบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="8ae40-149">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="8ae40-150">เลือกรายการ **รูปแบบเพื่อเรียนรู้การเรียกใช้แบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="8ae40-150">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="8ae40-151">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-151">Select **Designer**.</span></span>
4.  <span data-ttu-id="8ae40-152">เลือก **ขยาย/ยุบ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-152">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="8ae40-153">รูปแบบ ER **รูปแบบเพื่อเรียนรู้การเรียกใช้แบบพารามิเตอร์** ถูกออกแบบมาเพื่อสร้างใบแจ้งยอดภาษีในรูปแบบ XML ซึ่งแสดงให้ทราบถึงระดับของภาษีต่างๆ (ปกติ ลดลง และ ไม่มี)</span><span class="sxs-lookup"><span data-stu-id="8ae40-153">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="8ae40-154">แต่ละระดับมีจำนวนรายละเอียดแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="8ae40-154">Each level has a different number of details.</span></span>

    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="8ae40-156">บนแท็บ **การแม็ป** ให้ขยายรายการ **แบบจำลอง** **ข้อมูล** และ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="8ae40-156">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="8ae40-157">แหล่งข้อมูล **Model.Data.Summary** ส่งคืนรายการของธุรกรรมภาษี</span><span class="sxs-lookup"><span data-stu-id="8ae40-157">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="8ae40-158">ธุรกรรมเหล่านี้ถูกสรุปโดยรหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="8ae40-158">These transactions are summarized by tax code.</span></span> <span data-ttu-id="8ae40-159">สำหรับแหล่งข้อมูลนี้ ฟิลด์ที่คำนวณได้ **Model.Data.Summary.Level** ถูกกำหนดค่าให้ส่งคืนรหัสสำหรับระดับภาษี ของเรกคอร์ดสรุปแต่ละเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="8ae40-159">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="8ae40-160">สำหรับรหัสภาษีที่สามารถดึงข้อมูลจากแหล่งข้อมูลในช่วงรันไทม์ **Model.Data.Summary** ฟิลด์ที่คำนวณได้จะส่งคืนค่ารหัสระดับภาษี (**ทั่วไป** **ลดลง** **ไม่มี** หรือ **อื่นๆ**) เป็นค่าข้อความ</span><span class="sxs-lookup"><span data-stu-id="8ae40-160">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="8ae40-161">ฟิลด์ที่คำนวณได้ **Model.Data.Summary.Level** จะใช้เพื่อกรองข้อมูลเรกคอร์ดของแหล่งข้อมูล **Model.Data.Summary** และป้อนข้อมูลที่ถูกกรองในแต่ละองค์ประกอบ XML ที่แสดงถึงระดับภาษีโดยใช้ฟิลด์ **Model.Data2.Level1** **Model.Data2.Level2** และ **Model.Data2.Level3**</span><span class="sxs-lookup"><span data-stu-id="8ae40-161">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="8ae40-163">ฟิลด์ที่คำนวณได้ **Model.Data.Summary.Level** ซึ่งตั้งค่าคอนฟิก เพื่อให้มีนิพจน์ ER</span><span class="sxs-lookup"><span data-stu-id="8ae40-163">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="8ae40-164">โปรดทราบว่ารหัสภาษี (**VAT19** **InVAT19** **VAT7** **InVAT7** **THIRD** และ **InVAT0**) เป็นฮาร์ดโค้ด ในการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="8ae40-164">Note that tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="8ae40-165">ดังนั้น รูปแบบ ER นี้ขึ้นอยู่กับนิติบุคคลที่มีการตั้งค่าคอนฟิกรหัสภาษีเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8ae40-165">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="8ae40-167">การสนับสนุนชุดของรหัสภาษีที่แตกต่างกันสำหรับแต่ละนิติบุคคล คุณต้องปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8ae40-167">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="8ae40-168">สร้างเวอร์ชันที่สืบทอดมาของรูปแบบ ER สำหรับแต่ละนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ae40-168">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="8ae40-169">อัพเดตรหัสภาษีในฟิลด์ที่คำนวณได้ **Model.Data.Summary.Level** ตามการตั้งค่านิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ae40-169">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="8ae40-170">ปิดหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-170">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="8ae40-171">สร้างรูปแบบที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="8ae40-171">Create a derived format</span></span>

<span data-ttu-id="8ae40-172">ถัดไป คุณจะใช้คุณลักษณะการทำงานของพารามิเตอร์เฉพาะโปรแกรมประยุกต์ ER เพื่อสนับสนุนชุดของรหัสภาษีที่แตกต่างกัน สำหรับแต่ละนิติบุคคลในรูปแบบ ER เดียว</span><span class="sxs-lookup"><span data-stu-id="8ae40-172">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="8ae40-173">ในแผนภูมิการตั้งค่าคอนฟิก ให้ขยายเนื้อหาของรายการ **แบบจำลองเพื่อเรียนรู้การเรียกแบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="8ae40-173">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="8ae40-174">เลือกรายการ **รูปแบบเพื่อเรียนรู้การเรียกใช้แบบพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="8ae40-174">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="8ae40-175">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="8ae40-175">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="8ae40-176">เลือกตัวเลือก **ได้รับมาจากชื่อ: รูปแบบเพื่อเรียนรู้การเรียกแบบพารามิเตอร์, Microsoft**</span><span class="sxs-lookup"><span data-stu-id="8ae40-176">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="8ae40-177">ในฟิลด์ **ชื่อ** ป้อน **รูปแบบเพื่อเรียนรู้การค้นหาข้อมูล LE**</span><span class="sxs-lookup"><span data-stu-id="8ae40-177">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="8ae40-178">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="8ae40-178">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="8ae40-179">ตั้งค่าคอนฟิกรูปแบบที่สืบทอดมา</span><span class="sxs-lookup"><span data-stu-id="8ae40-179">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="8ae40-180">เพิ่มการแจงนับรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="8ae40-180">Add a format enumeration</span></span>

<span data-ttu-id="8ae40-181">ถัดไป คุณจะเพิ่มการแจงนับรูปแบบ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="8ae40-181">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="8ae40-182">ค่าของการแจงนับรูปแบบนี้ จะนำเสนอให้กับผู้ใช้ทางธุรกิจ ซึ่งจะระบุชุดที่ไม่ขึ้นอยู่กับรหัสภาษีสำหรับระดับภาษีต่างๆ ที่ใช้ในรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="8ae40-182">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="8ae40-183">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-183">Select **Designer**.</span></span>
2.  <span data-ttu-id="8ae40-184">เลือก **รูปแบบการแจงนับ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-184">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="8ae40-185">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="8ae40-185">Select **Add**.</span></span>
4.  <span data-ttu-id="8ae40-186">ในฟิลด์ **ชื่อ** ป้อน **รายการของระดับภาษี**</span><span class="sxs-lookup"><span data-stu-id="8ae40-186">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="8ae40-187">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8ae40-187">Select **Save**.</span></span>
6.  <span data-ttu-id="8ae40-188">บนแท็บ **ค่ารูปแบบการแจงนับ** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="8ae40-188">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="8ae40-189">ในฟิลด์ **ชื่อ** ป้อน **ภาษีปกติ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-189">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="8ae40-190">เลือก **เพิ่ม** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="8ae40-190">Select **Add** again.</span></span>
9.  <span data-ttu-id="8ae40-191">ในฟิลด์ **ชื่อ** ป้อน **ภาษีที่ลดลง**</span><span class="sxs-lookup"><span data-stu-id="8ae40-191">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="8ae40-192">เลือก **เพิ่ม** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="8ae40-192">Select **Add** again.</span></span>
11. <span data-ttu-id="8ae40-193">ในฟิลด์ **ชื่อ** ป้อน **ไม่มีภาษี**</span><span class="sxs-lookup"><span data-stu-id="8ae40-193">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="8ae40-194">เลือก **เพิ่ม** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="8ae40-194">Select **Add** again.</span></span>
13. <span data-ttu-id="8ae40-195">ในฟิลด์ **ชื่อ** ให้ป้อน **อื่นๆ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-195">In the **Name** field, enter **Other**.</span></span>

    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="8ae40-197">เนื่องจากผู้ใช้ที่เป็นธุรกิจอาจใช้ภาษาต่างๆ เพื่อระบุชุดของรหัสภาษีที่ไม่ขึ้นอยู่กับค่าที่เป็นของนิติบุคคล เราขอแนะนำให้คุณแปลค่าของการแจงนับนี้เป็นภาษาที่ได้รับการตั้งค่าคอนฟิกเป็นภาษาที่ต้องการสำหรับผู้ใช้เหล่านั้นในการเงิน</span><span class="sxs-lookup"><span data-stu-id="8ae40-197">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="8ae40-198">เลือกเรกคอร์ด **ไม่มีภาษี**</span><span class="sxs-lookup"><span data-stu-id="8ae40-198">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="8ae40-199">คลิก ในฟิลด์ **ป้ายชื่อ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-199">Click in the **Label** field.</span></span>
16. <span data-ttu-id="8ae40-200">เลือก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="8ae40-200">Select **Translate**.</span></span>
17. <span data-ttu-id="8ae40-201">ในบานหน้าต่าง **การแปลข้อความ** ในฟิลด์ **รหัสป้ายชื่อ** ให้ป้อน **LBL_LEVELENUM_NO**</span><span class="sxs-lookup"><span data-stu-id="8ae40-201">In the **Text translation** pane, in the **Label Id** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="8ae40-202">ในฟิลด์ **ข้อความในภาษาเริ่มต้น** ให้ป้อน **ไม่มีภาษี**</span><span class="sxs-lookup"><span data-stu-id="8ae40-202">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="8ae40-203">ในฟิลด์ **ภาษา** เลือก **DE**</span><span class="sxs-lookup"><span data-stu-id="8ae40-203">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="8ae40-204">ในฟิลด์ **ข้อความที่แปล** ให้ป้อน **ไม่มีภาษี**</span><span class="sxs-lookup"><span data-stu-id="8ae40-204">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="8ae40-205">เลือก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="8ae40-205">Select **Translate**.</span></span>

    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="8ae40-207">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8ae40-207">Select **Save**.</span></span>
23. <span data-ttu-id="8ae40-208">ปิดหน้า **การแจงนับรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-208">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="8ae40-209">เพิ่มแหล่งข้อมูลการค้นหาใหม่</span><span class="sxs-lookup"><span data-stu-id="8ae40-209">Add a new lookup data source</span></span>

<span data-ttu-id="8ae40-210">ถัดไป คุณจะเพิ่มแหล่งข้อมูลใหม่เพื่อระบุวิธีการที่ผู้ใช้ทางธุรกิจจะระบุกฎที่เป็นไปตามนิติบุคคล เพื่อจดจำระดับภาษีที่ถูกต้อง สำหรับแต่ละเรกคอร์ดธุรกรรมสรุป</span><span class="sxs-lookup"><span data-stu-id="8ae40-210">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="8ae40-211">บนแท็บ **การแม็ป** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="8ae40-211">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="8ae40-212">เลือก **รูปแบบการแจงนับ\การค้นหา**</span><span class="sxs-lookup"><span data-stu-id="8ae40-212">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="8ae40-213">คุณสามารถระบุได้ว่ากฎแต่ละกฎที่ผู้ใช้ธุรกิจระบุสำหรับการรับรู้ระดับภาษี จะส่งคืนค่าของการแจงนับรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="8ae40-213">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="8ae40-214">โปรดสังเกตว่าชนิดแหล่งข้อมูล **การค้นหา** สามารถเข้าถึงได้ภายใต้ **แบบจำลองข้อมูล** และบล็อค **Dynamics 365 for Operations** ที่เพิ่มมา ไปยังบล็อค **การแจงนับของรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-214">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="8ae40-215">ดังนั้น การแจงนับแบบจำลองข้อมูล ER และการแจงนับของโปรแกรมประยุกต์ สามารถใช้เพื่อระบุชนิดของค่าที่ส่งคืน สำหรับแหล่งข้อมูลของชนิดนั้น</span><span class="sxs-lookup"><span data-stu-id="8ae40-215">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that is are returned for data sources of that type.</span></span>
    
3.  <span data-ttu-id="8ae40-216">ในฟิลด์ **ชื่อ** ให้ป้อน **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="8ae40-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="8ae40-217">ในฟิลด์ **การแจงนับรูปแบบ** ป้อน **รายการของระดับภาษี**</span><span class="sxs-lookup"><span data-stu-id="8ae40-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="8ae40-218">คุณได้ระบุ สำหรับแต่ละกฎที่ระบุไว้ในแหล่งข้อมูลนี้ ผู้ใช้ที่เป็นธุรกิจต้องเลือกค่าของการแจงนับรูปแบบ **รายการของระดับภาษี** เป็นค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="8ae40-218">You just specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="8ae40-219">เลือก **แก้ไขการค้นหา**</span><span class="sxs-lookup"><span data-stu-id="8ae40-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="8ae40-220">เลือก **คอลัมน์**</span><span class="sxs-lookup"><span data-stu-id="8ae40-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="8ae40-221">ขยายรายการ **Model**</span><span class="sxs-lookup"><span data-stu-id="8ae40-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="8ae40-222">ขยายรายการ **ข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="8ae40-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="8ae40-223">ขยายรายการ **ภาษี**</span><span class="sxs-lookup"><span data-stu-id="8ae40-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="8ae40-224">เลือกรายการ **Model.Data.Tax.Code**</span><span class="sxs-lookup"><span data-stu-id="8ae40-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="8ae40-225">เลือกปุ่ม **เพิ่ม** (ลูกศรขวา)</span><span class="sxs-lookup"><span data-stu-id="8ae40-225">Select the **Add** button (the right arrow).</span></span>

    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="8ae40-227">คุณได้ระบุ สำหรับแต่ละกฎที่ระบุไว้ในแหล่งข้อมูลนี้สำหรับการรับรู้ระดับภาษี ผู้ใช้ที่เป็นธุรกิจต้องเลือกค่ารหัสภาษีเป็นเงี่อนไข</span><span class="sxs-lookup"><span data-stu-id="8ae40-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="8ae40-228">รายการของรหัสภาษีที่ผู้ใช้ทางธุรกิจสามารถเลือกได้จะถูกส่งคืนโดยแหล่งข้อมูล **Model.Data.Tax**</span><span class="sxs-lookup"><span data-stu-id="8ae40-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="8ae40-229">เนื่องจากแหล่งข้อมูลนี้มีฟิลด์ **ชื่อ** ชื่อรหัสภาษีจะแสดงขึ้นสำหรับแต่ละค่ารหัสภาษี ในการค้นหาที่นำเสนอให้แก่ผู้ใช้ทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="8ae40-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="8ae40-230">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8ae40-230">Select **OK**.</span></span>

    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="8ae40-232">ผู้ใช้ทางธุรกิจสามารถเพิ่มกฎหลายกฎเป็นเรกคอร์ดของแหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="8ae40-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="8ae40-233">แต่ละเรกคอร์ดจะมีการกำหนดหมายเลขโดยรหัสบรรทัด</span><span class="sxs-lookup"><span data-stu-id="8ae40-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="8ae40-234">กฎจะถูกประเมินตามลำดับหมายเลขบรรทัดที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="8ae40-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="8ae40-235">เนื่องจากคุณเลือกฟิลด์ **รหัสภาษี** เป็นเงื่อนไขสำหรับกฎในแหล่งข้อมูลการค้นหานี้ และเนื่องจาก **รหัสภาษี** ถูกตั้งค่าเป็นฟิลด์ของชนิดข้อมูล **สตริง** แต่ละกฎจะถูกประเมินที่รันไทม์ โดยการเปรียบเทียบรหัสภาษีที่ส่งผ่านไปยังแหล่งข้อมูลที่มีรหัสภาษีที่กำหนดไว้ในเรกคอร์ดนี้ของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8ae40-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="8ae40-236">เมื่อพบกฎที่เป็นไปตามเงื่อนไขที่ตั้งค่าคอนฟิก แหล่งข้อมูลนี้จะส่งคืนค่าการค้นหาของกฎที่กำหนดไว้ในฟิลด์ **ผลการค้นหา**</span><span class="sxs-lookup"><span data-stu-id="8ae40-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="8ae40-237">ถ้าไม่พบกฎ ข้อยกเว้นจะถูกโยนเพื่อแจ้งให้ผู้ใช้ทราบว่าแหล่งข้อมูลปัจจุบันไม่สามารถส่งคืนค่าที่ถูกต้องได้</span><span class="sxs-lookup"><span data-stu-id="8ae40-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="8ae40-238">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8ae40-238">Select **Save**.</span></span>
14. <span data-ttu-id="8ae40-239">ปิดหน้า **ตัวออกแบบการค้นหา**</span><span class="sxs-lookup"><span data-stu-id="8ae40-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="8ae40-240">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8ae40-240">Select **OK**.</span></span>

    <span data-ttu-id="8ae40-241">โปรดสังเกตว่าคุณได้เพิ่มแหล่งข้อมูลใหม่ที่จะส่งคืนระดับภาษีเป็นค่าของการแจงนับรูปแบบ **รายการของระดับภาษี** สำหรับรหัสภาษีใดๆ ที่ส่งผ่านไปยังแหล่งข้อมูลเป็นอาร์กิวเมนต์ของพารามิเตอร์ **รหัส** ของชนิดข้อมูล **สตริง**</span><span class="sxs-lookup"><span data-stu-id="8ae40-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="8ae40-243">โปรดทราบว่าการประเมินกฎที่ตั้งค่าคอนฟิก จะขึ้นอยู่กับชนิดข้อมูลของฟิลด์ที่เลือกเพื่อกำหนดเงื่อนไขของกฎเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="8ae40-243">Note that the evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="8ae40-244">เมื่อคุณเลือกฟิลด์ที่มีการตั้งค่าคอนฟิกเป็นฟิลด์ของชนิดข้อมูล **ตัวเลข** หรือ **วันที่** เกณฑ์จะแตกต่างจากเงื่อนไขที่อธิบายไว้ก่อนหน้านี้สำหรับชนิดข้อมูล **สตริง**</span><span class="sxs-lookup"><span data-stu-id="8ae40-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="8ae40-245">สำหรับฟิลด์ **ตัวเลข** และ **วันที่** กฎต้องมีการระบุเป็นช่วงของค่า</span><span class="sxs-lookup"><span data-stu-id="8ae40-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="8ae40-246">เงื่อนไขของกฎจะถูกพิจารณาความพึงพอใจ เมื่อค่าที่ส่งผ่านไปยังแหล่งข้อมูลอยู่ในช่วงที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="8ae40-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="8ae40-247">ภาพประกอบต่อไปนี้ แสดงตัวอย่างของการตั้งค่าของชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="8ae40-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="8ae40-248">นอกจากฟิลด์ **Model.Data.Tax.Code** ของชนิดข้อมูล **สตริง** ฟิลด์ **Model.Tax.Summary.Base** ของชนิดข้อมูล **จริง** จะใช้เพื่อระบุเงื่อนไขสำหรับแหล่งข้อมูลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8ae40-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="8ae40-250">เนื่องจากฟิลด์ **Model.Data.Tax.Code** และ **Model.Tax.Summary.Base** ถูกเลือกสำหรับแหล่งข้อมูลการค้นหานี้ แต่ละกฎของแหล่งข้อมูลนี้จะได้รับการตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8ae40-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="8ae40-251">ในรายการที่แสดง ค่าของการแจงนับรูปแบบ **รายการของระดับภาษี** ต้องถูกเลือกเป็นค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="8ae40-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="8ae40-252">รหัสภาษีต้องถูแป้อน เป็นเงื่อนไขของกฎนี้</span><span class="sxs-lookup"><span data-stu-id="8ae40-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="8ae40-253">เฉพาะรหัสภาษีที่ได้รับมาจากแหล่งข้อมูล **Model.Data.Tax** เท่านั้น ที่สามารถใช้แหล่งข้อมูลภาษีได้</span><span class="sxs-lookup"><span data-stu-id="8ae40-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="8ae40-254">ค่าต่ำสุดและสูงสุดของจำนวนเงินฐานภาษี ต้องถูกป้อนค่าตามเงื่อนไขของกฎนี้</span><span class="sxs-lookup"><span data-stu-id="8ae40-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="8ae40-255">ต่อไปนี้เป็นวิธีการประเมินแต่ละกฎของแหล่งข้อมูลนี้เมื่อรันไทม์:</span><span class="sxs-lookup"><span data-stu-id="8ae40-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="8ae40-256">รหัสของชนิดข้อมูล **สตริง** ที่ส่งผ่านไปยังแหล่งข้อมูลนี้ เท่ากับรหัสภาษีของกฎหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8ae40-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="8ae40-257">ค่าของชนิดข้อมูล **จริง** ที่ส่งผ่านไปยังแหล่งข้อมูลนี้ อยู่ระหว่างค่าต่ำสุดและค่าสูงสุดที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8ae40-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="8ae40-258">กฎจะมีผลบังคับใช้เมื่อเงื่อนไขทั้งสองเป็นที่น่าพอใจ</span><span class="sxs-lookup"><span data-stu-id="8ae40-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="8ae40-259">แปลป้ายชื่อของแหล่งข้อมูลการค้นหาที่ถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="8ae40-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="8ae40-260">เนื่องจากผู้ใช้ทางธุรกิจอาจใช้ภาษาต่างๆ เพื่อระบุชุดของรหัสภาษีที่ไม่ขึ้นอยู่กับนิติบุคคล เราขอแนะนำให้คุณแปลป้ายชื่อของแหล่งข้อมูลการค้นหาใดๆ ที่คุณเพิ่ม ซึ่งจะแสดงในแต่ละภาษีที่ผู้ใช้ต้องการบนหน้าที่สัมพันธ์กัน</span><span class="sxs-lookup"><span data-stu-id="8ae40-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="8ae40-261">เลือกแหล่งข้อมูล **Model.Data.Selector**</span><span class="sxs-lookup"><span data-stu-id="8ae40-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="8ae40-262">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8ae40-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="8ae40-263">คลิก ในฟิลด์ **ป้ายชื่อ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="8ae40-264">เลือก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="8ae40-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="8ae40-265">ในบานหน้าต่าง **การแปลข้อความ** ในฟิลด์ **รหัสป้ายชื่อ** ให้ป้อน **LBL_SELECTOR_DS**</span><span class="sxs-lookup"><span data-stu-id="8ae40-265">In the **Text translation** pane, in the **Label Id** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="8ae40-266">ในฟิลด์ **ข้อความในภาษาเริ่มต้น** ป้อน **เลือกระดับภาษีตามรหัสภาษี**</span><span class="sxs-lookup"><span data-stu-id="8ae40-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="8ae40-267">ในฟิลด์ **ภาษา** เลือก **DE**</span><span class="sxs-lookup"><span data-stu-id="8ae40-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="8ae40-268">ในฟิลด์ **ข้อความที่แปล** ให้ป้อน **เลือกระดับภาษีสำหรับรหัสภาษี**</span><span class="sxs-lookup"><span data-stu-id="8ae40-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="8ae40-269">เลือก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="8ae40-269">Select **Translate**.</span></span>
10. <span data-ttu-id="8ae40-270">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8ae40-270">Select **OK**.</span></span>

    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="8ae40-272">เพิ่มฟิลด์ใหม่เพื่อใช้การค้นหาที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="8ae40-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="8ae40-273">ขยายรายการ **Model.Data**</span><span class="sxs-lookup"><span data-stu-id="8ae40-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="8ae40-274">เลือกรายการ **Model.Data.Summary**</span><span class="sxs-lookup"><span data-stu-id="8ae40-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="8ae40-275">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="8ae40-275">Select **Add**.</span></span>
4.  <span data-ttu-id="8ae40-276">เลือก **ฟังก์ชัน/ฟิลด์ที่คำนวณได้**</span><span class="sxs-lookup"><span data-stu-id="8ae40-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="8ae40-277">ในฟิลด์ **ชื่อ** ให้ป้อน **LevelByLookup**</span><span class="sxs-lookup"><span data-stu-id="8ae40-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="8ae40-278">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="8ae40-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="8ae40-279">ใน **ฟิลด์สูตร** ให้ป้อน **Model.Selector(Model.Data.Summary.Code)**</span><span class="sxs-lookup"><span data-stu-id="8ae40-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="8ae40-280">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8ae40-280">Select **Save**.</span></span>

    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="8ae40-282">ปิดหน้า **ตัวแก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="8ae40-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="8ae40-283">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8ae40-283">Select **OK**.</span></span>

    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="8ae40-285">โปรดสังเกตว่าฟิลด์ที่คำนวณได้ **LevelByLookup** ที่คุณเพิ่ม จะส่งคืนระดับภาษีเป็นค่าของการแจงนับรูปแบบ **รายการของระดับภาษี** สำหรับเรกคอร์ดธุรกรรมภาษีแบบสรุปแต่ละเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="8ae40-285">Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id="8ae40-286">รหัสภาษีของเรกคอร์ดจะถูกส่งผ่านไปยังแหล่งข้อมูลการค้นหา **Model.Selector** และชุดของกฎสำหรับแหล่งข้อมูลนี้จะใช้ในการเลือกระดับภาษีที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8ae40-286">The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name="add-a-new-format-enumeration-based-data-source"></a><span data-ttu-id="8ae40-287">เพิ่มแหล่งข้อมูลตามการแจงนับรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="8ae40-287">Add a new format enumeration-based data source</span></span>

<span data-ttu-id="8ae40-288">ถัดไป คุณจะเพิ่มแหล่งข้อมูลใหม่ที่อ้างอิงถึงการแจงนับรูปแบบที่คุณเพิ่มไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="8ae40-288">Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id="8ae40-289">ค่าของแหล่งข้อมูลนี้จะใช้ในนิพจน์รูปแบบ ER ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="8ae40-289">Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id="8ae40-290">เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="8ae40-290">Select **Add root**.</span></span>
2.  <span data-ttu-id="8ae40-291">เลือก **การแจงนับรูปแบบ\การแจงนับ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-291">Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id="8ae40-292">ในฟิลด์ **ชื่อ** ป้อน **TaxationLevel**</span><span class="sxs-lookup"><span data-stu-id="8ae40-292">In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id="8ae40-293">ในฟิลด์ **การแจงนับรูปแบบ** ป้อน **รายการของระดับภาษี**</span><span class="sxs-lookup"><span data-stu-id="8ae40-293">In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id="8ae40-294">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8ae40-294">Select **Save**.</span></span>

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a><span data-ttu-id="8ae40-295">แก้ไขฟิลด์ที่มีอยู่เพื่อเริ่มต้นใช้งานการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8ae40-295">Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id="8ae40-296">ถัดไป คุณจะแก้ไขฟิลด์ที่คำนวณที่มีอยู่เพื่อให้ใช้แหล่งข้อมูลการค้นหาที่ตั้งค่าคอนฟิก เพื่อส่งคืนค่าระดับภาษีที่ถูกต้อง ทั้งนี้ขึ้นอยู่กับรหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="8ae40-296">Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id="8ae40-297">เลือกรายการ **Model.Data.Summary.Level**</span><span class="sxs-lookup"><span data-stu-id="8ae40-297">Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id="8ae40-298">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8ae40-298">Select **Edit**.</span></span>
3.  <span data-ttu-id="8ae40-299">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="8ae40-299">Select **Edit formula**.</span></span>

    <span data-ttu-id="8ae40-300">โปรดสังเกตว่านิพจน์ปัจจุบันของฟิลด์ **Model.Data.Summary.Level** จะรวมรหัสภาษีที่มีรหัสแบบตายตัวต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8ae40-300">Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id="8ae40-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span><span class="sxs-lookup"><span data-stu-id="8ae40-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="8ae40-302">ในฟิลด์ **สูตร** ให้ป้อน **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**</span><span class="sxs-lookup"><span data-stu-id="8ae40-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![เพจตัวออกแบบการดำเนินงาน ER](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="8ae40-304">โปรดสังเกตว่านิพจน์ของฟิลด์ **Model.Data.Summary.Level** จะส่งคืนระดับภาษี ขึ้นอยู่กับรหัสภาษีของเรกคอร์ดปัจจุบัน และชุดของกฎที่ผู้ใช้ทางธุรกิจมีการตั้งค่าคอนฟิกในแหล่งข้อมูลการค้นหา **Model.Data.Selector**</span><span class="sxs-lookup"><span data-stu-id="8ae40-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="8ae40-305">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8ae40-305">Select **Save**.</span></span>
6.  <span data-ttu-id="8ae40-306">ปิดหน้า **ตัวออกแบบสูตร**</span><span class="sxs-lookup"><span data-stu-id="8ae40-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="8ae40-307">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8ae40-307">Select **OK**.</span></span>
8.  <span data-ttu-id="8ae40-308">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8ae40-308">Select **Save**.</span></span>
9.  <span data-ttu-id="8ae40-309">ปิดหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="8ae40-310">เวอร์ชันแบบร่างเสร็จสมบูรณ์ของรูปแบบที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="8ae40-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="8ae40-311">บนแท็บด่วน **เวอร์ชัน** เลือก **เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="8ae40-311">On the **Versions** fast tab, select **Change status**.</span></span>
2.  <span data-ttu-id="8ae40-312">เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="8ae40-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="8ae40-313">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8ae40-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="8ae40-314">ส่งออกเวอร์ชันที่เสร็จสมบูรณ์ของรูปแบบที่แก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="8ae40-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="8ae40-315">ในแผนภูมิการตั้งค่าคอนฟิก ให้เลือกรายการ **รูปแบบเพื่อเรียนรู้วิธีการค้นหาข้อมูล LE**</span><span class="sxs-lookup"><span data-stu-id="8ae40-315">In the configuration tree, select the **Format to learn how to lookup LE data** item.</span></span>
2.  <span data-ttu-id="8ae40-316">บนแท็บด่วน **เวอร์ชัน** ให้เลือกเรกคอร์ดที่มีสถานะเป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="8ae40-316">On the **Versions** fast tab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="8ae40-317">เลือก **แลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="8ae40-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="8ae40-318">เลือก **ส่งออกเป็นไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="8ae40-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="8ae40-319">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8ae40-319">Select **OK**.</span></span>
6.  <span data-ttu-id="8ae40-320">เว็บเบราเซอร์จะดาวน์โหลดไฟล์ **รูปแบบเพื่อเรียนรู้วิธีการค้นหา LE data.xml**</span><span class="sxs-lookup"><span data-stu-id="8ae40-320">The web browser downloads a **Format to learn how to lookup LE data.xml** file.</span></span> <span data-ttu-id="8ae40-321">จัดเก็บไฟล์นี้ไว้ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="8ae40-321">Store this file locally.</span></span>

<span data-ttu-id="8ae40-322">ทำซ้ำขั้นตอนในส่วนนี้ สำหรับรายการหลักของรูปแบบ **รูปแบบเพื่อเรียนรู้วิธีการค้นหารูปแบบข้อมูล LE** และจัดเก็บไฟล์ต่อไปนี้ในเครื่อง:</span><span class="sxs-lookup"><span data-stu-id="8ae40-322">Repeat steps in this section for parent items of the **Format to learn how to lookup LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="8ae40-323">รูปแบบเพื่อเรียนรู้ calls.xml แบบพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="8ae40-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="8ae40-324">การแม็ปเพื่อเรียนรู้ calls.xml แบบพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="8ae40-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="8ae40-325">แบบจำลองเพื่อเรียนรู้ calls.xml แบบพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="8ae40-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="8ae40-326">การเรียนรู้วิธีการรูปแบบ ER **เรียนรู้วิธีการค้นหาข้อมูล LE** ที่ตั้งค่าคอนฟิก เพื่อตั้งค่ารหัสภาษีของชุดที่ขึ้นกับนิติบุคคล เพื่อกรองธุรกรรมภาษี โดยระดับภาษีที่ต่างกัน ให้ทำตามขั้นต่อนในหัวข้อ [ตั้งค่าพารามิเตอร์ของรูปแบบ ER สำหรับแต่ละนิติบุคคล](er-app-specific-parameters-set-up.md) ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="8ae40-326">To learn how to use the configured **Format to learn how to lookup LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ae40-327">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8ae40-327">Additional resources</span></span>

[<span data-ttu-id="8ae40-328">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="8ae40-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="8ae40-329">ตั้งค่าพารามิเตอร์ของรูปแบบ ER สำหรับแต่ละนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ae40-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)
