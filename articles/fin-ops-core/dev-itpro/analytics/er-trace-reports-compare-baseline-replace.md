---
title: การปรับปรุงในการสืบค้นกลับผลลัพธ์ของรายงาน ER ที่สร้างขึ้น และเปรียบเทียบกับค่าพื้นฐาน
description: หัวข้อนี้จะอธิบายถึงการปรับปรุงคุณลักษณะเกณฑ์พื้นฐานของ ER ใน Microsoft Dynamics 365 for Finance and Operations เวอร์ชัน 10.0.3 (มิถุนายน 2019)
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 1c00a5d9e2804f6ec0f6cb4c544029a1235ee58d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094015"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="0f04c-103">การปรับปรุงในการสืบค้นกลับผลลัพธ์ของรายงาน ER ที่สร้างขึ้น และเปรียบเทียบกับค่าพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="0f04c-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0f04c-104">หัวข้อนี้จะอธิบายถึงชุดของการปรับปรุงแรกที่ได้ทำไว้กับคุณลักษณะพื้นฐานของกรอบงานการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="0f04c-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="0f04c-105">การปรับปรุงเหล่านี้พร้อมใช้งานใน Microsoft Dynamics 365 for Finance and Operations รุ่น 10.0.3 (มิถุนายน 2019) และใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="0f04c-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="0f04c-106">ทำให้การตั้งค่าของกฎพื้นฐานเป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0f04c-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="0f04c-107">หัวข้อ [สืบค้นกลับผลลัพธ์ของรายงานที่สร้างและเปรียบเทียบกับข้อมูลพื้นฐาน](er-trace-reports-compare-baseline.md) อธิบายถึงวิธีการตั้งค่าคอนฟิกกรอบงาน ER เพื่อรวบรวมข้อมูลเกี่ยวกับการดำเนินการรูปแบบ ER และประเมินผลลัพธ์ของการดำเนินการเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="0f04c-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="0f04c-108">ตัวอย่างของหัวข้อนี้แสดงขั้นตอนที่ต้องทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0f04c-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="0f04c-109">ต่อไปนี้เป็นขั้นตอนบางรายการ:</span><span class="sxs-lookup"><span data-stu-id="0f04c-109">Here are some of the steps:</span></span>

- <span data-ttu-id="0f04c-110">รันรูปแบบ ER เพื่อสร้างไฟล์ขาออก และจัดเก็บไฟล์เฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="0f04c-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="0f04c-111">เพิ่มไฟล์ที่จัดเก็บเฉพาะที่เป็นเอกสารแนบของข้อมูลพื้นฐานที่ถูกเพิ่มสำหรับรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="0f04c-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="0f04c-112">ตั้งค่าคอนฟิกกฎพื้นฐานสำหรับข้อมูลพื้นฐานที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="0f04c-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="0f04c-113">การตั้งค่าคอนฟิกนี้ประกอบด้วยขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0f04c-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="0f04c-114">ระบุองค์ประกอบรูปแบบ ER ซึ่งใช้ในการสร้างไฟล์ขาออก</span><span class="sxs-lookup"><span data-stu-id="0f04c-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="0f04c-115">เลือกเอกสารแนบซึ่งอ้างอิงถึงไฟล์ขาออกที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0f04c-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="0f04c-116">ขั้นตอนเหล่านี้ต้องดำเนินการด้วยตนเอง ถึงแม้ว่าความสามารถของ ER ใหม่จะเปิดใช้งานให้เป็นระบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0f04c-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="0f04c-117">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ให้ดำเนินการตัวอย่างต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0f04c-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="0f04c-118">ตัวอย่าง: ทำให้การตั้งค่าของกฎพื้นฐานเป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0f04c-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="0f04c-119">เมื่อต้องการดำเนินการตามขั้นตอนต่างๆ ในตัวอย่างนี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องดำเนินการขั้นตอนต่างๆ ในตัวอย่างให้เสร็จสมบูรณ์ในหัวข้อ [สืบค้นกลับรายงานที่สร้างและเปรียบเทียบกับค่าพื้นฐาน](er-trace-reports-compare-baseline.md) จนถึงส่วน "เพิ่มข้อมูลพื้นฐานใหม่สำหรับรูปแบบ ER ที่ได้รับการออกแบบ"</span><span class="sxs-lookup"><span data-stu-id="0f04c-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="0f04c-120">ตรวจทานพื้นฐานที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="0f04c-120">Review added baseline</span></span>

1. <span data-ttu-id="0f04c-121">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="0f04c-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0f04c-122">เลือก **ข้อมูลพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="0f04c-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f04c-123">ปุ่ม **ข้อมูลพื้นฐาน** ในบานหน้าต่างการดำเนินการ จะพร้อมใช้งานเฉพาะเมื่อพารามิเตอร์ผู้ใช้ ER **รันในโหมดดีบัก** ถูกเปิดสำหรับบริษัทปัจจุบันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0f04c-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="0f04c-124">มีการเพิ่มข้อมูลพื้นฐานสำหรับรูปแบบ **รูปแบบเพื่อเรียนรู้ข้อมูลพื้นฐาน ER** ที่เลือก แต่ยังไม่มีการเพิ่มกฎพื้นฐานสำหรับข้อมูลพื้นฐานนี้</span><span class="sxs-lookup"><span data-stu-id="0f04c-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="0f04c-125">![หน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์ ยังไม่มีกฎ](media/GER-BaselineSample-AddBaseline2.PNG "ภาพหน้าจอของหน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์")</span><span class="sxs-lookup"><span data-stu-id="0f04c-125">![Electronic reporting format baselines page, no rules yet](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="0f04c-126">สร้างกฎพื้นฐานใหม่</span><span class="sxs-lookup"><span data-stu-id="0f04c-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="0f04c-127">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="0f04c-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0f04c-128">ในแผนภูมิ ให้ขยาย **แบบจำลองเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**</span><span class="sxs-lookup"><span data-stu-id="0f04c-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="0f04c-129">ในแผนภูมิ ให้เลือก **แบบจำลองเพื่อเรียนรู้ข้อมูลพื้นฐาน ER\\รูปแบบเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**</span><span class="sxs-lookup"><span data-stu-id="0f04c-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="0f04c-130">บน FastTab **รุ่น** เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="0f04c-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="0f04c-131">ในฟิลด์ **ป้อน Id** ป้อน **1**</span><span class="sxs-lookup"><span data-stu-id="0f04c-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="0f04c-132">ตั้งค่าตัวเลือก **สร้างไฟล์พื้นฐาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="0f04c-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="0f04c-133">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0f04c-133">Select **OK**.</span></span>
8. <span data-ttu-id="0f04c-134">เลือก **ข้อมูลพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="0f04c-134">Select **Baselines**.</span></span>

    <span data-ttu-id="0f04c-135">![หน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์ เกณฑ์พื้นฐานที่เลือก](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "ภาพหน้าจอของหน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์")</span><span class="sxs-lookup"><span data-stu-id="0f04c-135">![Electronic reporting format baselines page, baselines selected](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="0f04c-136">มีการแนบไฟล์ขาออกที่สร้างขึ้นโดยอัตโนมัติไปยังข้อมูลพื้นฐานของรูปแบบ ER ที่ดำเนินการแล้ว</span><span class="sxs-lookup"><span data-stu-id="0f04c-136">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="0f04c-137">กฎพื้นฐานถูกเพิ่มโดยอัตโนมัติไปยังข้อมูลพื้นฐานนี้ และนอกจากนี้ ยังมีการอ้างอิงไปยังไฟล์ที่แนบด้วย</span><span class="sxs-lookup"><span data-stu-id="0f04c-137">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="0f04c-138">ในฟิลด์ **ชื่อ** ให้ป้อน **พื้นฐาน 1**</span><span class="sxs-lookup"><span data-stu-id="0f04c-138">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="0f04c-139">ในฟิลด์ **ตัวพรางชื่อไฟล์** ป้อน **.xml**</span><span class="sxs-lookup"><span data-stu-id="0f04c-139">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="0f04c-140">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0f04c-140">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="0f04c-141">รันรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="0f04c-141">Run the format</span></span>

<span data-ttu-id="0f04c-142">ขณะนี้คุณพร้อมที่จะดำเนินการขั้นตอนที่เหลือในตัวอย่างให้เสร็จสมบูรณ์ในหัวข้อ [สืบค้นกลับรายงานผลลัพธ์ที่สร้างและเปรียบเทียบกับค่าพื้นฐาน](er-trace-reports-compare-baseline.md) ซึ่งเริ่มต้นจากส่วน "รันรูปแบบ ER ที่มีการออกแบบ และตรวจสอบล็อกเพื่อวิเคราะห์ผลลัพธ์"</span><span class="sxs-lookup"><span data-stu-id="0f04c-142">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="0f04c-143">เมื่อคุณลบกฎพื้นฐานที่เพิ่มโดยอัตโนมัติบน FastTab **ข้อมูลพื้นฐาน** เอกสารแนบที่อ้างอิงจะไม่ถูกลบโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0f04c-143">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="0f04c-144">ตั้งค่าคอนฟิกข้อมูลพื้นฐานเพื่อให้ละเว้นส่วนที่เปลี่ยนแปลงอยู่เสมอของเอาท์พุท ER</span><span class="sxs-lookup"><span data-stu-id="0f04c-144">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="0f04c-145">เมื่อรูปแบบ ER ได้รับการออกแบบมาเพื่อให้มีข้อมูลที่มีการเปลี่ยนแปลงเมื่อรันรูปแบบ จึงจำเป็นต้องใช้คุณลักษณะพื้นฐานของ ER เพื่อเปรียบเทียบผลลัพธ์ที่สร้างขึ้นกับค่าพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="0f04c-145">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="0f04c-146">ตัวอย่างเช่น ข้อมูลนี้อาจเป็นวันที่และเวลาที่ใช้ในการประมวลผล หรือตัวระบุเฉพาะของเอกสารที่สร้างขึ้นในรูปแบบที่แตกต่างกัน (ตัวระบุที่ไม่ซ้ำกันส่วนกลาง \[GUID\] และอื่นๆ)</span><span class="sxs-lookup"><span data-stu-id="0f04c-146">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="0f04c-147">ความสามารถของ ER ใหม่ช่วยให้คุณสามารถตั้งค่าคอนฟิกกฎพื้นฐาน เพื่อให้ละเว้นองค์ประกอบที่สามารถเปลี่ยนแปลงได้ของรูปแบบ ER เมื่อมีการรันรูปแบบ โดยมีวัตถุประสงค์ของการเปรียบเทียบค่าพื้นฐานกับผลลัพธ์ของการดำเนินการของรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="0f04c-147">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="0f04c-148">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ให้ดำเนินการตัวอย่างต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0f04c-148">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="0f04c-149">ตัวอย่าง: ตั้งค่าคอนฟิกข้อมูลพื้นฐานเพื่อให้ละเว้นส่วนที่เปลี่ยนแปลงอยู่เสมอของเอาท์พุท ER</span><span class="sxs-lookup"><span data-stu-id="0f04c-149">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="0f04c-150">เมื่อต้องการดำเนินการขั้นตอนต่างๆ ในตัวอย่างนี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องดำเนินการขั้นตอนต่างๆ ในตัวอย่างให้เสร็จสมบูรณ์ในหัวข้อ [สืบค้นกลับรายงานที่สร้างและเปรียบเทียบกับค่าพื้นฐาน](er-trace-reports-compare-baseline.md)</span><span class="sxs-lookup"><span data-stu-id="0f04c-150">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="0f04c-151">ปรับเปลี่ยนรูปแบบ ER ที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="0f04c-151">Modify a configured ER format</span></span>

1. <span data-ttu-id="0f04c-152">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="0f04c-152">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0f04c-153">ในแผนภูมิ ให้ขยาย **แบบจำลองเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**</span><span class="sxs-lookup"><span data-stu-id="0f04c-153">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="0f04c-154">ในแผนภูมิ ให้เลือก **แบบจำลองเพื่อเรียนรู้ข้อมูลพื้นฐาน ER\\รูปแบบเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**</span><span class="sxs-lookup"><span data-stu-id="0f04c-154">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="0f04c-155">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="0f04c-155">Select **Designer**.</span></span>
5. <span data-ttu-id="0f04c-156">ในแผนภูมิ ให้เลือก **เอาท์พุท\\เอกสาร**</span><span class="sxs-lookup"><span data-stu-id="0f04c-156">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="0f04c-157">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="0f04c-157">Select **Add**.</span></span>
7. <span data-ttu-id="0f04c-158">ในกล่องโต้ตอบรายการแบบหล่นลง ในแผนภูมิ ให้เลือก **XML\\แอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="0f04c-158">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="0f04c-159">ในฟิลด์ **ชื่อ** ให้ป้อน **ProcessingDateTime**</span><span class="sxs-lookup"><span data-stu-id="0f04c-159">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="0f04c-160">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0f04c-160">Select **OK**.</span></span>
10. <span data-ttu-id="0f04c-161">บนแท็บ **การแม็ป** ในแผนภูมิ ให้เลือก **เอาท์พุท\\เอกสาร\\ProcessingDateTime**</span><span class="sxs-lookup"><span data-stu-id="0f04c-161">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="0f04c-162">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="0f04c-162">Select **Edit formula**.</span></span>
12. <span data-ttu-id="0f04c-163">ในฟิลด์ **สูตร** ให้ป้อนนิพจน์ต่อไปนี้: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="0f04c-163">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="0f04c-164">เลือก **บันทึก** แล้วจากนั้น เลือก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="0f04c-164">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="0f04c-165">เลือก **ทดสอบ** อีกครั้ง เพื่อทดสอบนิพจน์ที่ตั้งค่าคอนฟิกอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="0f04c-165">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="0f04c-166">![หน้าโปรแกรมออกแบบสูตร](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "ภาพหน้าจอของหน้าโปรแกรมออกแบบสูตร")</span><span class="sxs-lookup"><span data-stu-id="0f04c-166">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f04c-167">แท็บ **ผลลัพธ์การทดสอบ** แสดงให้เห็นว่านิพจน์ที่ตั้งค่าคอนฟิกจะส่งคืนค่าวันที่และเวลาที่แตกต่างกัน เมื่อใดก็ตามที่มีการเรียก</span><span class="sxs-lookup"><span data-stu-id="0f04c-167">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="0f04c-168">ปิดหน้า **ตัวออกแบบสูตร** และจากนั้น เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0f04c-168">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="0f04c-169">![หน้าตัวออกแบบรูปแบบ](media/GER-BaselineSample-FormatMappingDesign2.PNG "ภาพหน้าจอของหน้าโปรแกรมออกแบบรูปแบบ")</span><span class="sxs-lookup"><span data-stu-id="0f04c-169">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="0f04c-170">ปิดหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="0f04c-170">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="0f04c-171">ลบกฎพื้นฐานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="0f04c-171">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="0f04c-172">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="0f04c-172">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0f04c-173">เลือก **ข้อมูลพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="0f04c-173">Select **Baselines**.</span></span>
3. <span data-ttu-id="0f04c-174">ในรายการของข้อมูลพื้นฐาน ให้เลือกข้อมูลพื้นฐานที่มีการตั้งค่าคอนฟิกสำหรับรูปแบบ **รูปแบบเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**</span><span class="sxs-lookup"><span data-stu-id="0f04c-174">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="0f04c-175">บน FastTab **ข้อมูลพื้นฐาน** ให้เลือก **ลบ** เพื่อลบกฎพื้นฐานที่คุณตั้งค่าคอนฟิกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="0f04c-175">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="0f04c-176">![หน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์ ที่ลบ](media/GER-BaselineSample-AddBaseline3.PNG "ภาพหน้าจอของหน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์")</span><span class="sxs-lookup"><span data-stu-id="0f04c-176">![Electronic reporting format baselines page, deleted](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="0f04c-177">กำหนดการแทนที่สำหรับการผูกรูปแบบ ER ที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="0f04c-177">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="0f04c-178">บนหน้า **การตั้งค่าคอนฟิก** บน FastTab **การแทนที่** ให้เลือก **เลือกส่วนประกอบ**</span><span class="sxs-lookup"><span data-stu-id="0f04c-178">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="0f04c-179">ในแผนภูมิส่วนประกอบของรูปแบบ ขยาย **เอาท์พุท** ขยาย **เอาท์พุท\\เอกสาร** และจากนั้น เลือกกล่องกาเครื่องหมายสำหรับ **เอาท์พุท\\เอกสาร\\ProcessingDateTime**</span><span class="sxs-lookup"><span data-stu-id="0f04c-179">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>
3. <span data-ttu-id="0f04c-180">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0f04c-180">Select **OK**.</span></span>

<span data-ttu-id="0f04c-181">![หน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์ ส่วนประกอบ](media/GER-BaselineSample-AddBaseline4.PNG "ภาพหน้าจอของหน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์")</span><span class="sxs-lookup"><span data-stu-id="0f04c-181">![Electronic reporting format baselines page, components](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="0f04c-182">มีการเพิ่มส่วนประกอบของรูปแบบ ER ที่เลือกลงในรายการของส่วนประกอบบน FastTab **การแทนที่**</span><span class="sxs-lookup"><span data-stu-id="0f04c-182">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="0f04c-183">เมื่อมีการรันรูปแบบ ER ฐานในโหมดดีบัก การผูกข้อมูลของรูปแบบสำหรับแต่ละส่วนประกอบจะถูกแทนที่ด้วยการผูกที่แสดงในคอลัมน์ **การผูก**</span><span class="sxs-lookup"><span data-stu-id="0f04c-183">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="0f04c-184">เมื่อต้องการเปลี่ยนการผูกข้อมูลเริ่มต้นสำหรับส่วนประกอบที่แสดงรายการอยู่บน FastTab **การแทนที่** เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="0f04c-184">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="0f04c-185">สร้างกฎพื้นฐานใหม่</span><span class="sxs-lookup"><span data-stu-id="0f04c-185">Make a new baseline rule</span></span>

<span data-ttu-id="0f04c-186">ทำตามขั้นตอนในส่วน "ตัวอย่าง: ทำให้การตั้งค่าของกฎพื้นฐานเป็นระบบอัตโนมัติ" ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="0f04c-186">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="0f04c-187">การแจ้งเตือนจะเตือนคุณว่าไฟล์ขาออกถูกสร้างขึ้นโดยใช้การตั้งค่าพื้นฐาน และมีการแทนที่ที่บังคับของการผูกรูปแบบเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="0f04c-187">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="0f04c-188">![การแจ้งเตือนบนหน้าการตั้งค่าคอนฟิก](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "ภาพหน้าจอของการแจ้งเตือนบนหน้าการตั้งค่าคอนฟิก")</span><span class="sxs-lookup"><span data-stu-id="0f04c-188">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="0f04c-189">ระงับคำเตือนเกี่ยวกับการแทนที่ของการผูกรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="0f04c-189">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="0f04c-190">ด้วยการตั้งค่าพารามิเตอร์ ER เฉพาะ คุณสามารถระงับการแจ้งเตือนที่เตือนเกี่ยวกับการแทนที่ของการผูกรูปแบบได้</span><span class="sxs-lookup"><span data-stu-id="0f04c-190">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="0f04c-191">การระงับนี้อาจเป็นประโยชน์ เมื่อมีการแทนที่การผูกรูปแบบในโหมดการทำงานอัตโนมัติโดยใช้ Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="0f04c-191">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="0f04c-192">ในกรณีนี้ การเตือนอาจถือเป็นความล้มเหลวของกรณีทดสอบที่กำลังรันอยู่</span><span class="sxs-lookup"><span data-stu-id="0f04c-192">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="0f04c-193">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="0f04c-193">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="0f04c-194">ตั้งค่าตัวเลือก **ระงับคำเตือนพื้นฐาน** เป็น **ใช่** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0f04c-194">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="0f04c-195">ตรวจทานไฟล์พื้นฐานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0f04c-195">Review the generated baseline file</span></span>

1. <span data-ttu-id="0f04c-196">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="0f04c-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0f04c-197">เลือก **ข้อมูลพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="0f04c-197">Select **Baselines**.</span></span>
3. <span data-ttu-id="0f04c-198">เลือก **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="0f04c-198">Select **Attachments**.</span></span>
    > [!NOTE]
    > <span data-ttu-id="0f04c-199">ไฟล์ที่สร้างขึ้นประกอบด้วย ข้อความการประมวลผลวันที่และเวลา (**"#"**) จากการผูกที่มีการตั้งค่าคอนฟิกในกฎพื้นฐานที่เพิ่มเข้ามา ไม่ใช่จากการผูกข้อมูลของรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="0f04c-199">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>
    
4. <span data-ttu-id="0f04c-200">ปิดหน้า **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="0f04c-200">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="0f04c-201">รันรูปแบบ ER ที่ออกแบบ และตรวจสอบล็อกเพื่อวิเคราะห์ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="0f04c-201">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="0f04c-202">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="0f04c-202">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0f04c-203">ในแผนภูมิ ให้ขยาย **แบบจำลองเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**</span><span class="sxs-lookup"><span data-stu-id="0f04c-203">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="0f04c-204">ในแผนภูมิ ให้เลือก **แบบจำลองเพื่อเรียนรู้ข้อมูลพื้นฐาน ER\\รูปแบบเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**</span><span class="sxs-lookup"><span data-stu-id="0f04c-204">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="0f04c-205">บน FastTab **รุ่น** เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="0f04c-205">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="0f04c-206">ในฟิลด์ **ป้อน Id** พิมพ์ **1**</span><span class="sxs-lookup"><span data-stu-id="0f04c-206">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="0f04c-207">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0f04c-207">Select **OK**.</span></span>
7. <span data-ttu-id="0f04c-208">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **ล็อกดีบักการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="0f04c-208">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="0f04c-209">ล็อกการดำเนินการประกอบด้วย ข้อมูลเกี่ยวกับผลลัพธ์ของการเปรียบเทียบของไฟล์ที่สร้างขึ้นโดยใช้ข้อมูลพื้นฐานที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="0f04c-209">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="0f04c-210">ล็อกจะบ่งชี้ว่าไฟล์ที่สร้างและข้อมูลพื้นฐานเท่ากัน ถึงแม้ว่ารูปแบบที่ดำเนินการจะมีการผูกข้อมูลเพื่อป้อนค่าวันที่และเวลาที่เปลี่ยนแปลงอย่างต่อเนื่องในไฟล์ขาออก</span><span class="sxs-lookup"><span data-stu-id="0f04c-210">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="0f04c-211">ถึงแม้ว่าไฟล์ขาออกถูกสร้างขึ้นโดยใช้การตั้งค่าพื้นฐานที่บังคับการแทนที่ของการผูกของรูปแบบ คุณจะไม่ได้รับคำเตือนใดๆ เกี่ยวกับการแทนที่</span><span class="sxs-lookup"><span data-stu-id="0f04c-211">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="0f04c-212">แลกเปลี่ยนการตั้งค่าพื้นฐานระหว่างสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="0f04c-212">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="0f04c-213">ส่งออกการตั้งค่าพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="0f04c-213">Export baseline settings</span></span>

<span data-ttu-id="0f04c-214">ความสามารถ ER ใหม่ช่วยให้คุณสามารถส่งออกการตั้งค่าพื้นฐานสำหรับรูปแบบ ER ที่เลือกจากสภาพแวดล้อมปัจจุบัน และจัดเก็บเป็นไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="0f04c-214">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="0f04c-215">เมื่อต้องการส่งออกการตั้งค่าพื้นฐานบนหน้า **ข้อมูลพื้นฐานรูปแบบการรายงานทางอิเล็กทรอนิกส์** เลือก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="0f04c-215">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="0f04c-216">การตั้งค่านำเข้าเกณฑ์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="0f04c-216">Import baseline settings</span></span>

<span data-ttu-id="0f04c-217">มีการนำเข้าการตั้งค่าพื้นฐานที่ส่งออกไปยังสภาพแวดล้อมที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="0f04c-217">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="0f04c-218">ต้องมีการนำเข้าสภาพแวดล้อมเป็นรูปแบบ ER ก่อน</span><span class="sxs-lookup"><span data-stu-id="0f04c-218">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="0f04c-219">จากนั้น คุณสามารถนำเข้าการตั้งค่าพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="0f04c-219">You can then import the baseline settings.</span></span>

<span data-ttu-id="0f04c-220">เมื่อต้องการนำเข้าการตั้งค่าพื้นฐานจากไฟล์ XML ที่จัดเก็บไว้เฉพาะที่ บนหน้า **ข้อมูลพื้นฐานรูปแบบการรายงานทางอิเล็กทรอนิกส์** เลือก **นำเข้า** และจากนั้น เลือก **เรียกดู** เพื่อเลือกไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="0f04c-220">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="0f04c-221">![นำเข้ากล่องโต้ตอบการตั้งค่าเกณฑ์พื้นฐาน](media/GER-BaselineSample-ImportBaseline1.PNG "ภาพหน้าจอของกล่องโต้ตอบการตั้งค่านำเข้าเกณฑ์พื้นฐาน")</span><span class="sxs-lookup"><span data-stu-id="0f04c-221">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="0f04c-222">เมื่อต้องการนำเข้าการตั้งค่าพื้นฐานจากไฟล์ XML ที่จัดเก็บบน Microsoft SharePoint Server ตามการตั้งค่าการจัดการเอกสารปัจจุบัน และชนิดเอกสารที่เลือก บนหน้า **ข้อมูลพื้นฐานรูปแบบการรายงานทางอิเล็กทรอนิกส์** ให้เลือก **นำเข้าจากแหล่งที่มา**</span><span class="sxs-lookup"><span data-stu-id="0f04c-222">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="0f04c-223">จากนั้น เลือกชนิดเอกสารและไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="0f04c-223">Then select the document type and the XML file.</span></span> <span data-ttu-id="0f04c-224">ต้องมีการตั้งค่าคอนฟิกชนิดเอกสารที่จำเป็นต้องใช้ในการเข้าถึงโฟลเดอร์ SharePoint ไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="0f04c-224">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="0f04c-225">![นำเข้าจากกล่องโต้ตอบแหล่งที่มา](media/GER-BaselineSample-ImportBaseline2.PNG "ภาพหน้าจอของกล่องโต้ตอบนำเข้าจากแหล่งที่มา")</span><span class="sxs-lookup"><span data-stu-id="0f04c-225">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="0f04c-226">คุณสามารถใช้ตัวบันทึกงานเพื่อบันทึกขั้นตอนสำหรับการเลือกชนิดเอกสารที่จำเป็นและชื่อไฟล์ในกล่องโต้ตอบ **นำเข้าจากแหล่งที่มา**</span><span class="sxs-lookup"><span data-stu-id="0f04c-226">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="0f04c-227">ด้วยวิธีนี้ คุณสามารถรักษาการตั้งค่าพื้นฐานที่จำเป็นบน SharePoint Server แล้วนำเข้าโดยอัตโนมัติโดยการใช้การบันทึกงาน เมื่อคุณรันการทดสอบแบบอัตโนมัติโดยใช้ Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="0f04c-227">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f04c-228">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0f04c-228">Additional resources</span></span>

- [<span data-ttu-id="0f04c-229">ติดตามผลของรายงานที่จัดทำและเปรียบเทียบผลกับค่าพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="0f04c-229">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="0f04c-230">ทรัพยากรตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="0f04c-230">Task recorder resources</span></span>](../user-interface/task-recorder.md)
