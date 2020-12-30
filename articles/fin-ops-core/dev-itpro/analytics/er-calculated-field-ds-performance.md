---
title: ปรับปรุงประสิทธิภาพการทำงานของโซลูชัน ER โดยการเพิ่มแหล่งข้อมูลฟิลด์ที่มีการคำนวณแบบพารามิเตอร์
description: หัวข้อนี้จะอธิบายวิธีการที่คุณสามารถช่วยปรับปรุงประสิทธิภาพการทำงานของโซลูชันการรายงานทางอิเล็กทรอนิกส์ (ER) โดยการเพิ่มแหล่งข้อมูลฟิลด์ที่มีการคำนวณแบบพารามิเตอร์
author: NickSelin
manager: AnnBe
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 940b696a06fb46bcd0557f059327cd4340448137
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681291"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="9536f-103">ปรับปรุงประสิทธิภาพการทำงานของโซลูชัน ER โดยการเพิ่มแหล่งข้อมูลฟิลด์ที่มีการคำนวณแบบพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="9536f-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9536f-104">หัวข้อนี้จะอธิบายวิธีการที่คุณสามารถดำเนิน [การติดตามประสิทธิภาพ](trace-execution-er-troubleshoot-perf.md) ของรูปแบบ [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) ที่ทำงาน แล้วใช้ข้อมูลจากการติดตามเพื่อช่วยปรับปรุงประสิทธิภาพการทำงานได้โดยการตั้งค่าคอนฟิกแหล่งข้อมูลของ **ฟิลด์ที่มีการคำนวณ** แบบพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="9536f-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="9536f-105">ในฐานะที่เป็นส่วนหนึ่งของกระบวนการในการออกแบบการตั้งค่าคอนฟิก ER เพื่อสร้างเอกสารทางธุรกิจ คุณกำหนดวิธีการที่จะใช้ในการดึงข้อมูลออกจากแอปพลิเคชัน และป้อนข้อมูลในผลลัพธ์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="9536f-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="9536f-106">โดยการออกแบบแหล่งข้อมูล ER แบบพารามิเตอร์ของชนิด **ฟิลด์ที่มีการคำนวณ** คุณจะสามารถลดจำนวนการเรียกฐานข้อมูล และลดเวลาและต้นทุนที่เกี่ยวข้องในการรวบรวมรายละเอียดของการดำเนินการของรูปแบบ ER ได้อย่างมาก</span><span class="sxs-lookup"><span data-stu-id="9536f-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9536f-107">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9536f-107">Prerequisites</span></span>

- <span data-ttu-id="9536f-108">เมื่อต้องการดำเนินการตัวอย่างในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณต้องเข้าถึงหนึ่งใน [บทบาท](../sysadmin/tasks/assign-users-security-roles.md) ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9536f-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="9536f-109">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="9536f-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="9536f-110">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="9536f-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="9536f-111">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="9536f-111">System administrator</span></span>

- <span data-ttu-id="9536f-112">บริษัทต้องตั้งค่าเป็น **DEMF**</span><span class="sxs-lookup"><span data-stu-id="9536f-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="9536f-113">ทําตามขั้นตอนใน [ภาคผนวก 1](#appendix1) ของหัวข้อนี้ เพื่อดาวน์โหลดส่วนประกอบของโซลูชัน Microsoft ER ตัวอย่างที่จําเป็นเพื่อทำตัวอย่างในหัวข้อนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9536f-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="9536f-114">ทำตามขั้นตอนใน [ภาคผนวก 2](#appendix2) ของหัวข้อนี้เพื่อตั้งค่าคอนฟิกชุดพารามิเตอร์ ER น้อยที่สุดที่จำเป็นสำหรับการใช้กรอบงาน ER เพื่อช่วยปรับปรุงประสิทธิภาพการทำงานของโซลูชัน Microsoft ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="9536f-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="9536f-115">นำเข้าโซลูชัน ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="9536f-115">Import the sample ER solution</span></span>

<span data-ttu-id="9536f-116">สมมติว่าคุณต้องออกแบบโซลูชัน ER ใหม่เพื่อสร้างรายงานใหม่ที่แสดงธุรกรรมผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9536f-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="9536f-117">ในปัจจุบัน คุณสามารถค้นหาธุรกรรมสำหรับผู้จัดจำหน่ายที่เลือกบนหน้า **ธุรกรรมผู้จัดจำหน่าย** (ไปยัง **บัญชีเจ้าหนี้** \> **ผู้จัดจำหน่าย** \> **ผู้จัดจำหน่ายทั้งหมด** ให้เลือกผู้จัดจำหน่าย และจากนั้น ในบานหน้าต่างการดำเนินการ บนแท็บ **ผู้จัดจำหน่าย** ในกลุ่ม **ธุรกรรม** ให้เลือก **ธุรกรรม**)</span><span class="sxs-lookup"><span data-stu-id="9536f-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="9536f-118">อย่างไรก็ตาม คุณต้องการให้มีธุรกรรมผู้จัดจำหน่ายทั้งหมดพร้อมกันในเอกสารอิเล็กทรอนิกส์หนึ่งรายการในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="9536f-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="9536f-119">โซลูชันนี้จะประกอบด้วยการตั้งค่าคอนฟิก ER ต่างๆ ที่มีรูปแบบข้อมูลที่จำเป็นต้องใช้ การแม็ปแบบจำลอง และส่วนประกอบรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="9536f-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="9536f-120">ขั้นตอนแรกคือนำเข้าโซลูชัน ER ตัวอย่างเพื่อสร้างรายงานธุรกรรมผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9536f-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="9536f-121">ลงชื่อเข้าใช้อินสแตนซ์ของ Microsoft Dynamics 365 Finance ที่ได้เตรียมใช้งานสำหรับบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="9536f-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="9536f-122">ในหัวข้อนี้ คุณจะสร้างและปรับเปลี่ยนการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="9536f-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="9536f-123">ตรวจสอบให้แน่ใจว่าได้เพิ่มตัวให้บริการการตั้งค่าคอนฟิกนี้ลงในอินสแตนซ์ Finance และทำเครื่องหมายเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="9536f-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="9536f-124">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="9536f-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="9536f-125">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** เลือกไทล์ **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="9536f-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="9536f-126">ในหน้า **การตั้งค่าคอนฟิก** นำเข้าการตั้งค่าคอนฟิก ER ที่คุณดาวน์โหลดเป็นข้อกำหนดเบื้องต้นลงใน Finance ตามลำดับต่อไปนี้: รูปแบบข้อมูล การแม็ปแบบจำลอง รูปแบบ</span><span class="sxs-lookup"><span data-stu-id="9536f-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="9536f-127">สำหรับการตั้งค่าคอนฟิกแต่ละรายการ ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="9536f-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="9536f-128">ในบานหน้าต่างการดำเนินการ เลือก **แลกเปลี่ยน** \> **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="9536f-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="9536f-129">เลือก **เรียกดู** และเลือกไฟล์ที่เหมาะสมสำหรับการตั้งค่าคอนฟิก ER ในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="9536f-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="9536f-130">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9536f-130">Select **OK**.</span></span>

![การตั้งค่าคอนฟิกที่นำเข้าบนหน้าการตั้งค่าคอนฟิก](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="9536f-132">ตรวจทานโซลูชัน ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="9536f-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="9536f-133">ตรวจทานการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="9536f-133">Review the model mapping</span></span>

1. <span data-ttu-id="9536f-134">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **รูปแบบการปรับปรุงประสิทธิภาพ** จากนั้นเลือก **การแม็ปการปรับปรุงประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="9536f-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="9536f-135">บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="9536f-136">บนหน้า **การแม็ปแบบจำลองกับแหล่งข้อมูล** บนแผงการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="9536f-137">การแม็ปแบบจำลอง ER นี้ ได้รับการออกแบบมาให้ทำสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9536f-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="9536f-138">ดึงข้อมูลรายการธุรกรรมของผู้จัดจำหน่ายที่จัดเก็บอยู่ในตาราง VendTrans (แหล่งข้อมูล **Trans**)</span><span class="sxs-lookup"><span data-stu-id="9536f-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="9536f-139">สำหรับธุรกรรมทั้งหมด ให้ดึงข้อมูลมาจากตาราง VendTable, เรกคอร์ดของผู้จัดจำหน่ายที่มีการลงรายการบัญชีธุรกรรมสำหรับ (แหล่งข้อมูล **\#Vend**)</span><span class="sxs-lookup"><span data-stu-id="9536f-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="9536f-140">แหล่งข้อมูล **\#Vend** ถูกตั้งค่าคอนฟิกเพื่อดึงข้อมูลเรกคอร์ดผู้จัดจำหน่ายที่สอดคล้องกันโดยใช้ความสัมพันธ์แบบกลุ่มต่อหนึ่งที่มีอยู่ **\@.'\>Relations'.VendTable\_AccountNum**</span><span class="sxs-lookup"><span data-stu-id="9536f-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="9536f-141">การแม็ปแบบจำลองในการตั้งค่าคอนฟิกนี้จะใช้รูปแบบข้อมูลพื้นฐาน สำหรับรูปแบบ ER ใดๆ ที่สร้างขึ้นสำหรับรูปแบบนี้และเรียกใช้ใน Finance</span><span class="sxs-lookup"><span data-stu-id="9536f-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="9536f-142">ดังนั้นจึงมีการเปิดเผยเนื้อหาของแหล่งข้อมูล **Trans** สำหรับรูปแบบ ER เช่น แหล่งข้อมูล **รูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![เพิ่มแหล่งข้อมูล Trans ในหน้าตัวออกแบบการแม็ปแบบจำลอง](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="9536f-144">ปิดหน้า **ตัวออกแบบการแม็ปรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="9536f-145">ปิดหน้า **การแม็ปแบบจำลองกับแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="9536f-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="9536f-146">ตรวจทานรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="9536f-146">Review format</span></span>

1. <span data-ttu-id="9536f-147">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **รูปแบบการปรับปรุงประสิทธิภาพ** จากนั้นเลือก **รูปแบบการปรับปรุงประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="9536f-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="9536f-148">บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="9536f-149">ในหน้า **ตัวออกแบบรูปแบบ** ในแท็บ **การแม็ป** ให้เลือก **ขยาย/ยุบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="9536f-150">ขยายรายการ **รูปแบบ** **ข้อมูล** และ **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="9536f-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="9536f-151">รูปแบบ ER นี้ได้รับการออกแบบมาเพื่อสร้างรายงานธุรกรรมของผู้จัดจำหน่ายในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="9536f-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![จัดรูปแบบแหล่งข้อมูลและการรวมขององค์ประกอบรูปแบบที่ตั้งค่าคอนฟิกบนหน้าตัวออกแบบรูปแบบ](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="9536f-153">ปิดหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="9536f-154">เรียกใช้โซลูชัน ER ตัวอย่างเพื่อติดตามการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9536f-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="9536f-155">สมมติว่าคุณได้ออกแบบโซลูชัน ER รุ่นแรกเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="9536f-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="9536f-156">ขณะนี้คุณต้องการทดสอบโซลูชันในอินสแตนซ์ Finance ของคุณ และวิเคราะห์ประสิทธิภาพในการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="9536f-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="9536f-157">เปิดการติดตามประสิทธิภาพ ER</span><span class="sxs-lookup"><span data-stu-id="9536f-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="9536f-158">เลือกบริษัท **DEMF**</span><span class="sxs-lookup"><span data-stu-id="9536f-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="9536f-159">ทำตามขั้นตอนใน [เปิดการติดตามประสิทธิภาพของ ER](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) เพื่อสร้างการติดตามประสิทธิภาพในขณะที่มีการเรียกใช้รูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="9536f-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![กล่องโต้ตอบพารามิเตอร์ผู้ใช้](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="9536f-161">รันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="9536f-161">Run the ER format</span></span>

1. <span data-ttu-id="9536f-162">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="9536f-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9536f-163">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **รูปแบบการปรับปรุงประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="9536f-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="9536f-164">บนบานหน้าต่างการดำเนินการ เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="9536f-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="9536f-165">ใช้การติดตามประสิทธิภาพเพื่อวิเคราะห์ประสิทธิภาพของการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="9536f-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="9536f-166">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การแม็ปการปรับปรุงประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="9536f-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="9536f-167">บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="9536f-168">บนหน้า **การแม็ปแบบจำลอง** บนแผงการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="9536f-169">บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** บนบานหน้าต่างการดำเนินการ ให้เลือก **การติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="9536f-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="9536f-170">เลือกการติดตามล่าสุดที่สร้างขึ้น แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9536f-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="9536f-171">ข้อมูลใหม่จะกลายเป็นพร้อมใช้งานสำหรับรายการแหล่งข้อมูลบางอย่างของการแม็ปแบบจำลองปัจจุบัน:</span><span class="sxs-lookup"><span data-stu-id="9536f-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="9536f-172">เวลาจริงที่ใช้ในการเรียกข้อมูลโดยใช้แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9536f-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="9536f-173">เวลาเดียวกันที่แสดงเป็นเปอร์เซ็นต์ของเวลาทั้งหมดที่ใช้ในการรันการแม็ปแบบจำลองทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9536f-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![รายละเอียดเวลาการดำเนินการบนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="9536f-175">ตาราง **สถิติประสิทธิภาพ** แสดงให้เห็นว่าแหล่งข้อมูล **Trans** เรียกตาราง VendTrans หนึ่งครั้ง</span><span class="sxs-lookup"><span data-stu-id="9536f-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="9536f-176">ค่า **\[265\]\[Q:265\]** ของแหล่งข้อมูล **Trans** บ่งชี้ว่ามีการดึงข้อมูลธุรกรรมของผู้จัดจำหน่าย 265 รายการจากตารางของแอปพลิเคชันและส่งคืนเป็นรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9536f-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="9536f-177">ตาราง **สถิติประสิทธิภาพ** ยังแสดงว่าการแม็ปแบบจำลองปัจจุบันทำซ้ำคำขอฐานข้อมูลในขณะที่มีการเรียกใช้แหล่งข้อมูล **\#Vend**</span><span class="sxs-lookup"><span data-stu-id="9536f-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="9536f-178">การทำซ้ำนี้เกิดขึ้นเนื่องจากเหตุผลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9536f-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="9536f-179">ตารางผู้จัดจำหน่ายถูกเรียกสองครั้งสำหรับธุรกรรมผู้จัดจำหน่าย 265 รายการ สำหรับการเรียกทั้งหมด 530 รายการ:</span><span class="sxs-lookup"><span data-stu-id="9536f-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="9536f-180">ทำการเรียกหนึ่งครั้งเพื่อป้อนหมายเลขบัญชีของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9536f-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="9536f-181">ทำการเรียกหนึ่งครั้งเพื่อป้อนชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9536f-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="9536f-182">มีการเรียกตารางผู้จัดจำหน่ายสำหรับธุรกรรมผู้จัดจำหน่ายแต่ละราย ถึงแม้ว่าจะมีการลงรายการบัญชีธุรกรรมที่นำเข้าสำหรับผู้จัดจำหน่ายห้ารายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9536f-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="9536f-183">การเรียก 530 รายการ ซ้ำกัน 525 รายการ</span><span class="sxs-lookup"><span data-stu-id="9536f-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="9536f-184">ภาพประกอบต่อไปนี้แสดงข้อความที่คุณได้รับเกี่ยวกับการเรียกที่ซ้ำ (การร้องขอฐานข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="9536f-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![ข้อความเกี่ยวกับการร้องขอฐานข้อมูลที่ซ้ำกันบนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="9536f-186">เวลาที่ใช้ในการดำเนินการแม็ปแบบจำลองรวม (ประมาณแปดวินาที) โปรดสังเกตว่าเวลาที่ใช้ในการดึงข้อมูลจากตารางแอปพลิเคชัน VendTable มากกว่า 80 เปอร์เซ็นต์ (ประมาณหกวินาที)</span><span class="sxs-lookup"><span data-stu-id="9536f-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="9536f-187">เปอร์เซ็นต์ดังกล่าวมากเกินกว่าสำหรับสองแอททริบิวต์ของผู้จัดจำหน่ายห้าราย โดยเปรียบเทียบกับปริมาณของข้อมูลจากตารางแอปพลิเคชัน VendTrans</span><span class="sxs-lookup"><span data-stu-id="9536f-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="9536f-188">เมื่อต้องการลดจำนวนการเรียกที่จะทำเพื่อดูรายละเอียดผู้จัดจำหน่ายสำหรับแต่ละธุรกรรม และเพื่อปรับปรุงประสิทธิภาพการทำงานของการแม็ปแบบจำลอง คุณสามารถใช้การแคชสำหรับแหล่งข้อมูล **\#Vend**</span><span class="sxs-lookup"><span data-stu-id="9536f-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="9536f-189">แหล่งข้อมูล **Trans\\\#Vend** จะถูกแคชในขอบเขตของธุรกรรมปัจจุบันของแหล่งข้อมูล **Trans** ขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9536f-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="9536f-190">โดยการแคชแหล่งข้อมูล **\#Vend** คุณจะลดจำนวนครั้งของการเรียกที่ซ้ำจาก 525 เป็น 260 แต่คุณจะไม่สามารถขจัดการทำซ้ำได้อย่างสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9536f-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="9536f-191">เมื่อต้องการตัดการทำซ้ำอย่างสมบูรณ์ คุณสามารถตั้งค่าคอนฟิกแหล่งข้อมูลแบบพารามิเตอร์ใหม่ของชนิด **ฟิลด์ที่มีการคำนวณ** ได้</span><span class="sxs-lookup"><span data-stu-id="9536f-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="9536f-192">ปรับปรุงการแม็ปแบบจำลองตามข้อมูลจากการติดตามการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9536f-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="9536f-193">เปลี่ยนตรรกะของการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="9536f-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="9536f-194">ทำตามขั้นตอนต่อไปนี้เพื่อใช้การแคชและแหล่งข้อมูลของชนิด **ฟิลด์ที่มีการคำนวณ** เพื่อช่วยป้องกันการเรียกที่ซ้ำไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9536f-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="9536f-195">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การแม็ปการปรับปรุงประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="9536f-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="9536f-196">บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="9536f-197">บนหน้า **การแม็ปแบบจำลอง** บนแผงการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="9536f-198">บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** ให้ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มแหล่งข้อมูลของชนิด **เรกคอร์ดตาราง** เพื่อเข้าถึงเรกคอร์ดในตารางแอปพลิเคชัน VendTable:</span><span class="sxs-lookup"><span data-stu-id="9536f-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="9536f-199">ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** ให้ขยาย **Dynamics 365 for Operations** และเลือก **เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="9536f-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="9536f-200">เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="9536f-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="9536f-201">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **Vend**</span><span class="sxs-lookup"><span data-stu-id="9536f-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="9536f-202">ในฟิลด์ **ตาราง** ให้ป้อน **VendTable**</span><span class="sxs-lookup"><span data-stu-id="9536f-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="9536f-203">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9536f-203">Select **OK**.</span></span>

5. <span data-ttu-id="9536f-204">คุณสามารถเรียกพารามิเตอร์เรียกไปยังแหล่งข้อมูลของชนิด **ฟิลด์ที่มีการคำนวณ** เฉพาะเมื่อแหล่งข้อมูลเหล่านั้นอยู่ในคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="9536f-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="9536f-205">ดังนั้น ให้ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มแหล่งข้อมูลชนิด **คอนเทนเนอร์เปล่า** เพื่อจัดเก็บแหล่งข้อมูลแบบพารามิเตอร์ใหม่ของชนิด **ฟิลด์ที่มีการคำนวณ**:</span><span class="sxs-lookup"><span data-stu-id="9536f-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="9536f-206">ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** ให้ขยาย **ทั่วไป** และเลือก **คอนเทอนเนอร์เปล่า**</span><span class="sxs-lookup"><span data-stu-id="9536f-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="9536f-207">เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="9536f-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="9536f-208">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **Box**</span><span class="sxs-lookup"><span data-stu-id="9536f-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="9536f-209">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9536f-209">Select **OK**.</span></span>

    ![แหล่งข้อมูล Box ในหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="9536f-211">ทำตามขั้นตอนต่อไปนี้เมื่อต้องการเพิ่มแหล่งข้อมูลแบบพารามิเตอร์ชนิด **ฟิลด์ที่มีการคำนวณ**:</span><span class="sxs-lookup"><span data-stu-id="9536f-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="9536f-212">ในบานหน้าต่าง **แหล่งข้อมูล** ให้เลือก **Box**</span><span class="sxs-lookup"><span data-stu-id="9536f-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="9536f-213">ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** ให้ขยาย **ฟังก์ชัน** และเลือกรายการ **ฟิลด์ที่มีการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="9536f-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="9536f-214">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9536f-214">Select **Add**.</span></span>
    4. <span data-ttu-id="9536f-215">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **Vend**</span><span class="sxs-lookup"><span data-stu-id="9536f-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="9536f-216">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="9536f-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="9536f-217">บนหน้า **ตัวออกแบบสูตร** ให้เลือก **พารามิเตอร์** เพื่อระบุพารามิเตอร์ที่ต้องระบุเมื่อมีการเรียกแหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="9536f-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="9536f-218">ในกล่องโต้ตอบ **พารามิเตอร์** ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="9536f-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="9536f-219">ในฟิลด์ **ชื่อ** ให้ป้อน **parmVendAccNumber**</span><span class="sxs-lookup"><span data-stu-id="9536f-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="9536f-220">ในฟิลด์ **ชนิด** เลือก **สตริง**</span><span class="sxs-lookup"><span data-stu-id="9536f-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="9536f-221">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9536f-221">Select **OK**.</span></span>
    11. <span data-ttu-id="9536f-222">ในฟิลด์ **สูตร** ให้ป้อน **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**</span><span class="sxs-lookup"><span data-stu-id="9536f-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="9536f-223">เลือก **บันทึก** และปิดหน้า **ตัวออกแบบสูตร**</span><span class="sxs-lookup"><span data-stu-id="9536f-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="9536f-224">เลือก **ตกลง** เพื่อเพิ่มแหล่งข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="9536f-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="9536f-225">ทำตามขั้นตอนต่อไปนี้เพื่อทำเครื่องหมายแหล่งข้อมูลที่เพิ่มเป็นแคชในระหว่างการดำเนินการ:</span><span class="sxs-lookup"><span data-stu-id="9536f-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="9536f-226">ในบานหน้าต่าง **แหล่งข้อมูล** ให้เลือก **Box\\Vend**</span><span class="sxs-lookup"><span data-stu-id="9536f-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="9536f-227">เลือก **แคช**</span><span class="sxs-lookup"><span data-stu-id="9536f-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9536f-228">แหล่งข้อมูล **Box\\Vend** จะถูกแคชในขอบเขตของธุรกรรมของผู้จัดจำหน่ายทั้งหมดของแหล่งข้อมูล **Trans** ขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9536f-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="9536f-229">ทำตามขั้นตอนต่อไปนี้เพื่ออัปเดตแหล่งข้อมูล **Trans\\\#Vend** ที่ซ้อนกันเพื่อให้สามารถใช้แหล่งข้อมูล **Box\\Vend** :</span><span class="sxs-lookup"><span data-stu-id="9536f-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="9536f-230">ในบานหน้าต่าง **แหล่งข้อมูล** ให้ขยาย **Trans**</span><span class="sxs-lookup"><span data-stu-id="9536f-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="9536f-231">เลือกแหล่งข้อมูล **Trans\\\#Vend** แล้วเลือก **แก้ไข** \> **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="9536f-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="9536f-232">ในหน้า **ตัวออกแบบสูตร** ในฟิลด์ **สูตร** ให้ป้อน **Box.Vend(\@.AccountNum)**</span><span class="sxs-lookup"><span data-stu-id="9536f-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="9536f-233">เลือก **บันทึก** แล้วปิดหน้า **ตัวออกแบบสูตร**</span><span class="sxs-lookup"><span data-stu-id="9536f-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="9536f-234">เลือก **ตกลง** เพื่อทำการเปลี่ยนแปลงในแหล่งข้อมูลที่เลือกให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9536f-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="9536f-235">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="9536f-235">Select **Save**.</span></span>

    ![แหล่งข้อมูล Vend ในหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="9536f-237">ปิดหน้า **ตัวออกแบบการแม็ปรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="9536f-238">ปิดหน้า **การแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="9536f-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="9536f-239">ดำเนินการรุ่นที่แก้ไขของการแม็ปแบบจำลอง ER ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9536f-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="9536f-240">บนหน้า **การตั้งค่าคอนฟิก** บนแท็บด่วน **รุ่น** ให้เลือกรุ่น **1.2** ของการตั้งค่าคอนฟิก **การแม็ปการปรับปรุงประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="9536f-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="9536f-241">เลือก **เปลี่ยนสถานะ** \> **เสร็จสมบูรณ์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9536f-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="9536f-242">รันโซลูชัน ER ที่แก้ไขเพื่อติดตามการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9536f-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="9536f-243">ทำซ้ำขั้นตอนในส่วน [รันรูปแบบ ER](#run-format) ก่อนหน้าในหัวข้อนี้ เพื่อสร้างการติดตามประสิทธิภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="9536f-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="9536f-244">ใช้การติดตามประสิทธิภาพเพื่อวิเคราะห์การปรับปรุงการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="9536f-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="9536f-245">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การแม็ปการปรับปรุงประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="9536f-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="9536f-246">บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="9536f-247">บนหน้า **การแม็ปแบบจำลอง** บนแผงการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="9536f-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="9536f-248">บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** บนบานหน้าต่างการดำเนินการ ให้เลือก **การติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="9536f-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="9536f-249">เลือกการติดตามล่าสุดที่สร้างขึ้น แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9536f-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="9536f-250">โปรดสังเกตว่าการปรับปรุงที่คุณทำไปยังการแม็ปแบบจำลอง มีการตัดการสอบถามที่ซ้ำกันไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9536f-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="9536f-251">นอกจากนี้ ยังมีการลดจำนวนของการเรียกไปยังตารางฐานข้อมูลและแหล่งข้อมูลสำหรับการแม็ปแบบจำลองนี้ด้วย</span><span class="sxs-lookup"><span data-stu-id="9536f-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![ข้อมูลสืบย้อนกลับในหน้าตัวออกแบบการแม็ปแบบจำลอง 1](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="9536f-253">เวลาที่ใช้ในการดำเนินการทั้งหมดลดลงประมาณ 20 เท่า (จากประมาณ 8 วินาทีเป็นประมาณ 400 มิลลิวินาที)</span><span class="sxs-lookup"><span data-stu-id="9536f-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="9536f-254">ดังนั้น ประสิทธิภาพการทำงานของโซลูชัน ER ทั้งหมดได้รับการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="9536f-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![ข้อมูลสืบย้อนกลับในหน้าตัวออกแบบการแม็ปแบบจำลอง 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="9536f-256">ภาคผนวก 1: ดาวน์โหลดส่วนประกอบของโซลูชัน Microsoft ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="9536f-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="9536f-257">คุณต้องดาวน์โหลดและจัดเก็บไฟล์ต่อไปนี้ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="9536f-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="9536f-258">ไฟล์</span><span class="sxs-lookup"><span data-stu-id="9536f-258">File</span></span>                                        | <span data-ttu-id="9536f-259">ปริมาณความจุ</span><span class="sxs-lookup"><span data-stu-id="9536f-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="9536f-260">แบบจำลองการปรับปรุงประสิทธิภาพ.รุ่น.1</span><span class="sxs-lookup"><span data-stu-id="9536f-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="9536f-261">การตั้งค่าคอนฟิกรูปแบบข้อมูล ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="9536f-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="9536f-262">การแม็ปการปรับปรุงประสิทธิภาพ.รุ่น.1.1</span><span class="sxs-lookup"><span data-stu-id="9536f-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="9536f-263">การตั้งค่าคอนฟิกการแม็ปรูปแบบ ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="9536f-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="9536f-264">รูปแบบการปรับปรุงประสิทธิภาพ.รุ่น.1.1</span><span class="sxs-lookup"><span data-stu-id="9536f-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="9536f-265">การตั้งค่าคอนฟิกรูปแบบ ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="9536f-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="9536f-266">ภาคผนวก 2: ตั้งค่าคอนฟิกกรอบงาน ER</span><span class="sxs-lookup"><span data-stu-id="9536f-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="9536f-267">ก่อนที่คุณจะสามารถเริ่มต้นการใช้กรอบงาน ER เพื่อปรับปรุงประสิทธิภาพการทำงานของโซลูชัน Microsoft ER ตัวอย่าง คุณต้องตั้งค่าคอนฟิกชุดพารามิเตอร์ ER ให้น้อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="9536f-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="9536f-268">ตั้งค่าคอนฟิกพารามิเตอร์ ER</span><span class="sxs-lookup"><span data-stu-id="9536f-268">Configure ER parameters</span></span>

1. <span data-ttu-id="9536f-269">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="9536f-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9536f-270">บนหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="9536f-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="9536f-271">ในหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์** บนแท็บ **ทั่วไป** ตั้งค่าตัวเลือก **เปิดใช้งานโหมดการออกแบบ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9536f-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="9536f-272">บนแท็บ **เอกสารแนบ** ให้ตั้งค่าพารามิเตอร์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9536f-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="9536f-273">ในฟิลด์ **การตั้งค่าคอนฟิก** ให้เลือกชนิด **ไฟล์** สำหรับบริษัท **DEMF**</span><span class="sxs-lookup"><span data-stu-id="9536f-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="9536f-274">ในฟิลด์ **ที่เก็บงานถาวร** **ชั่วคราว** **พื้นฐาน** และ **อื่นๆ** ให้เลือกชนิด **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="9536f-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="9536f-275">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับพารามิเตอร์ ER ให้ดูที่ [ตั้งค่าคอนฟิกกรอบงาน ER](electronic-reporting-er-configure-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="9536f-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="9536f-276">เปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="9536f-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="9536f-277">มีการทำเครื่องหมายการตั้งค่าคอนฟิก ER ทั้งหมดที่มีการเพิ่มเป็นเจ้าของโดยผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="9536f-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="9536f-278">ผู้ให้บริการการตั้งค่าคอนฟิก ER ที่เปิดใช้งานในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** จะใช้เพื่อวัตถุประสงค์นี้</span><span class="sxs-lookup"><span data-stu-id="9536f-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="9536f-279">ดังนั้นคุณต้องเรียกใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ก่อนที่คุณจะเริ่มต้นการเพิ่มหรือแก้ไขการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="9536f-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="9536f-280">เฉพาะเจ้าของที่มีการตั้งค่าคอนฟิก ER เท่านั้นที่สามารถแก้ไขการตั้งค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="9536f-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="9536f-281">ดังนั้นก่อนที่จะแก้ไขการตั้งค่าคอนฟิก ER ต้องมีการเรียกใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9536f-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="9536f-282">ตรวจทานรายการของผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="9536f-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="9536f-283">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="9536f-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9536f-284">บนหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **ผู้ให้บริการการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="9536f-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="9536f-285">บนหน้า **ตารางของผู้ให้บริการการตั้งค่าคอนฟิก** แต่ละเรกคอร์ดผู้ให้บริการจะมีชื่อและ URL ที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="9536f-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="9536f-286">ตรวจทานเนื้อหาของหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9536f-286">Review the contents of this page.</span></span> <span data-ttu-id="9536f-287">ถ้ามีเรกคอร์ดสำหรับ **Litware, Inc.** อยู่แล้ว ให้ข้ามขั้นตอนถัดไป [เพิ่มผู้ให้บริการการตั้งค่าคอนฟิก ER ใหม่](#ActivateProvider)</span><span class="sxs-lookup"><span data-stu-id="9536f-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="9536f-288">เพิ่มผู้ให้บริการการตั้งค่าคอนฟิก ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="9536f-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="9536f-289">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="9536f-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9536f-290">บนหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **ผู้ให้บริการการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="9536f-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="9536f-291">ในหน้า **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="9536f-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="9536f-292">ในฟิลด์ **ชื่อ** ให้ป้อน **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="9536f-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="9536f-293">ในฟิลด์ **ที่อยู่อินเทอร์เน็ต** ให้ป้อน `https://www.litware.com`</span><span class="sxs-lookup"><span data-stu-id="9536f-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="9536f-294">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="9536f-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="9536f-295">เปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="9536f-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="9536f-296">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="9536f-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9536f-297">ในหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** ให้เลือกไทล์ **Litware, inc.** แล้วเลือก **กำหนดเป็นใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="9536f-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="9536f-298">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับผู้ให้บริการการตั้งค่าคอนฟิก ER ให้ดูที่ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="9536f-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9536f-299">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9536f-299">Additional resources</span></span>

- [<span data-ttu-id="9536f-300">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="9536f-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="9536f-301">ติดตามการดำเนินการของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="9536f-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="9536f-302">สนับสนุนการเรียกแบบพารามิเตอร์ ของแหล่งข้อมูล ER ของชนิดฟิลด์ที่มีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="9536f-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)
