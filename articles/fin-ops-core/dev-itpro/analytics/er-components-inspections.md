---
title: ตรวจสอบส่วนประกอบ ER ที่ตั้งค่าคอนฟิกเพื่อป้องกันปัญหารันไทม์
description: หัวข้อนี้อธิบายถึงวิธีการตรวจสอบส่วนประกอบของการรายงานทางอิเล็กทรอนิกส์ (ER) ที่ตั้งค่าคอนฟิกไว้เพื่อป้องกันไม่ให้เกิดปัญหารันไทม์ซึ่งอาจเกิดขึ้นได้
author: NickSelin
manager: AnnBe
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86db6dc27a8a76e90494e3dc7a7cc9c828f9ec37
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574136"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a><span data-ttu-id="a4e13-103">ตรวจสอบส่วนประกอบ ER ที่ตั้งค่าคอนฟิกเพื่อป้องกันปัญหารันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-103">Inspect the configured ER component to prevent runtime issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a4e13-104">ทุก ๆ [รูปแบบ](general-electronic-reporting.md#FormatComponentOutbound) [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) และส่วนประกอบ [การแม็ปแบบจำลอง](general-electronic-reporting.md#data-model-and-model-mapping-components) สามารถ [ตรวจสอบความถูกต้อง](er-fillable-excel.md#validate-an-er-format) ในเวลาที่ออกแบบได้</span><span class="sxs-lookup"><span data-stu-id="a4e13-104">Every configured [Electronic reporting (ER)](general-electronic-reporting.md) [format](general-electronic-reporting.md#FormatComponentOutbound) and [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component can be [validated](er-fillable-excel.md#validate-an-er-format) at design time.</span></span> <span data-ttu-id="a4e13-105">ในระหว่างการตรวจสอบความถูกต้องนี้ การตรวจสอบความสอดคล้องกันจะดำเนินการเพื่อช่วยป้องกันปัญหารันไทม์ซึ่งอาจเกิดขึ้น เช่น ข้อผิดพลาดในการดำเนินการและการลดประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-105">During this validation, a consistency check runs to help prevent runtime issues that might occur, such as execution errors and performance degradation.</span></span> <span data-ttu-id="a4e13-106">สำหรับทุกปัญหาที่พบ การตรวจสอบจะระบุเส้นทางของส่วนประกอบที่เป็นปัญหา</span><span class="sxs-lookup"><span data-stu-id="a4e13-106">For every issue that is found, the check provides the path of a problematic element.</span></span> <span data-ttu-id="a4e13-107">สำหรับปัญหาบางอย่าง การแก้ไขอัตโนมัติจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-107">For some issues, an automatic fix is available.</span></span>

<span data-ttu-id="a4e13-108">โดยค่าเริ่มต้น การตรวจสอบความถูกต้องจะใช้โดยอัตโนมัติในกรณีต่อไปนี้สำหรับการตั้งค่าคอนฟิก ER ที่มีส่วนประกอบ ER ดังกล่าวก่อนหน้านี้:</span><span class="sxs-lookup"><span data-stu-id="a4e13-108">By default, the validation is automatically applied in the following cases for an ER configuration that contains the previously mentioned ER components:</span></span>

- <span data-ttu-id="a4e13-109">คุณสามารถ [นำเข้า](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) [รุ่น](general-electronic-reporting.md#component-versioning) การตั้งค่าคอนฟิก ER ใหม่ไปยังอินสแตนซ์ของ Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="a4e13-109">You [import](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) a new [version](general-electronic-reporting.md#component-versioning) of an ER configuration into your instance of Microsoft Dynamics 365 Finance.</span></span>
- <span data-ttu-id="a4e13-110">คุณเปลี่ยน [สถานะ](general-electronic-reporting.md#component-versioning) การตั้งค่าคอนฟิก ER ที่สามารถแก้ไขได้จาก **แบบร่าง** เป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="a4e13-110">You change the [status](general-electronic-reporting.md#component-versioning) of the editable ER configuration from **Draft** to **Completed**.</span></span>
- <span data-ttu-id="a4e13-111">คุณ [ปรับใช้](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) การตั้งค่าคอนฟิก ER ที่สามารถแก้ไขได้โดยใช้รุ่นพื้นฐานใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-111">You [rebase](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) an editable ER configuration by applying a new base version.</span></span>

<span data-ttu-id="a4e13-112">คุณสามารถรันการตรวจสอบความถูกต้องนี้อย่างชัดแจ้ง</span><span class="sxs-lookup"><span data-stu-id="a4e13-112">You can explicitly run this validation.</span></span> <span data-ttu-id="a4e13-113">เลือกตัวเลือกอย่างใดอย่างหนึ่งจากสามตัวเลือกต่อไปนี้และปฏิบัติตามขั้นตอนที่ระบุ:</span><span class="sxs-lookup"><span data-stu-id="a4e13-113">Select one of the following three options, and follow the steps that are provided:</span></span>

- <span data-ttu-id="a4e13-114">ตัวเลือก 1:</span><span class="sxs-lookup"><span data-stu-id="a4e13-114">Option 1:</span></span>

    1. <span data-ttu-id="a4e13-115">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="a4e13-115">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="a4e13-116">ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิก ER ที่ต้องการที่มีรูปแบบ ER หรือส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-116">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format or ER model mapping component.</span></span>
    3. <span data-ttu-id="a4e13-117">บนแท็บด่วน **รุ่น** เลือกรุ่นที่ต้องการของการตั้งค่าคอนฟิก ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a4e13-117">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="a4e13-118">บนบานหน้าต่างการดำเนินการ เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-118">On the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="a4e13-119">ตัวเลือก 2 สำหรับรูปแบบ ER:</span><span class="sxs-lookup"><span data-stu-id="a4e13-119">Option 2, for an ER format:</span></span>

    1. <span data-ttu-id="a4e13-120">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="a4e13-120">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="a4e13-121">ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิก ER ที่ต้องการที่มีส่วนประกอบรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-121">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format component.</span></span>
    3. <span data-ttu-id="a4e13-122">บนแท็บด่วน **รุ่น** เลือกรุ่นที่ต้องการของการตั้งค่าคอนฟิก ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a4e13-122">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="a4e13-123">บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-123">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="a4e13-124">บนหน้า **ตัวออกแบบรูปแบบ** บนบานหน้าต่างการดำเนินการ ให้เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-124">On the **Format designer** page, on the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="a4e13-125">ตัวเลือก 3 สำหรับการแม็ปแบบจำลอง ER:</span><span class="sxs-lookup"><span data-stu-id="a4e13-125">Option 3, for an ER model mapping:</span></span>

    1. <span data-ttu-id="a4e13-126">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="a4e13-126">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="a4e13-127">ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิก ER ที่ต้องการที่มีส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-127">In the configurations tree in the left pane, select the desired ER configuration that contains the ER model mapping component.</span></span>
    3. <span data-ttu-id="a4e13-128">บนแท็บด่วน **รุ่น** เลือกรุ่นที่ต้องการของการตั้งค่าคอนฟิก ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a4e13-128">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="a4e13-129">บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-129">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="a4e13-130">บนหน้า **การแม็ปแบบจำลองกับแหล่งข้อมูล** บนแผงการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-130">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>
    6. <span data-ttu-id="a4e13-131">บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** บนแผงการดำเนินการ เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-131">On the **Model mapping designer** page, on the Action Pane, select **Validate**.</span></span>

<span data-ttu-id="a4e13-132">เมื่อต้องการข้ามการตรวจสอบความถูกต้องเมื่อมีการนำเข้าการตั้งค่าคอนฟิก ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-132">To skip the validation when the configuration is imported, follow these steps.</span></span>

1. <span data-ttu-id="a4e13-133">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="a4e13-133">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="a4e13-134">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="a4e13-134">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="a4e13-135">ตั้งค่าตัวเลือก **ตรวจสอบความถูกต้องการตั้งค่าคอนฟิกหลังจากนำเข้า** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="a4e13-135">Set the **Validate the configuration after importing** option to **No**.</span></span>

<span data-ttu-id="a4e13-136">เมื่อต้องการข้ามการตรวจสอบความถูกต้องเมื่อคุณเปลี่ยนแปลงหรือปรับใช้สถานะของรุ่น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-136">To skip the validation when you change or rebase the version's status, follow these steps.</span></span>

1. <span data-ttu-id="a4e13-137">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="a4e13-137">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="a4e13-138">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="a4e13-138">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="a4e13-139">ตั้งค่าตัวเลือก **ข้ามการตรวจสอบความถูกต้องเมื่อสถานะของการตั้งค่าคอนฟิกเปลี่ยนแปลงและปรับใช้** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="a4e13-139">Set the **Skip validation at configuration's status change and rebase** option to **Yes**.</span></span>

<span data-ttu-id="a4e13-140">ER ใช้ประเภทต่อไปนี้ในการตรวจสอบความสอดคล้องกันของกลุ่มการตรวจสอบ:</span><span class="sxs-lookup"><span data-stu-id="a4e13-140">ER uses the following categories to group consistency check inspections:</span></span>

- <span data-ttu-id="a4e13-141">**ความสามารถในการปฏิบัติการ** การตรวจสอบที่พบปัญหาที่สำคัญซึ่งอาจเกิดขึ้นเมื่อรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-141">**Executability** – Inspections that detect critical issues that might occur at runtime.</span></span> <span data-ttu-id="a4e13-142">ปัญหาเหล่านี้ส่วนใหญ่จะอยู่ในระดับ **ข้อผิดพลาด**</span><span class="sxs-lookup"><span data-stu-id="a4e13-142">These issues are mostly at an **Error** level.</span></span> 
- <span data-ttu-id="a4e13-143">**ประสิทธิภาพ** – การตรวจสอบที่ตรวจพบปัญหาที่อาจทำให้เกิดการดำเนินการที่ไม่มีประสิทธิภาพของส่วนประกอบ ER ที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="a4e13-143">**Performance** – Inspections that detect issues that might cause inefficient execution of configured ER components.</span></span> <span data-ttu-id="a4e13-144">ปัญหาเหล่านี้ส่วนใหญ่จะอยู่ในระดับ **คำเตือน**</span><span class="sxs-lookup"><span data-stu-id="a4e13-144">These issues are mostly at a **Warning** level.</span></span>
- <span data-ttu-id="a4e13-145">**ความถูกต้องของข้อมูล** – การตรวจสอบที่ตรวจพบปัญหาที่อาจทำให้เกิดปัญหาการสูญเสียข้อมูลหรือรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-145">**Data integrity** – Inspections that detect issues that might cause data loss or runtime issues.</span></span> <span data-ttu-id="a4e13-146">ปัญหาเหล่านี้ส่วนใหญ่จะอยู่ในระดับ **คำเตือน**</span><span class="sxs-lookup"><span data-stu-id="a4e13-146">These issues are mostly at a **Warning** level.</span></span>

## <a name="list-of-inspections"></a><span data-ttu-id="a4e13-147">รายการของการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a4e13-147">List of inspections</span></span>

<span data-ttu-id="a4e13-148">ตารางต่อไปนี้จะแสดงภาพรวมของการตรวจสอบที่ ER มีให้</span><span class="sxs-lookup"><span data-stu-id="a4e13-148">The following table provides an overview of the inspections that ER provides.</span></span> <span data-ttu-id="a4e13-149">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตรวจสอบเหล่านี้ ให้ใช้การเชื่อมโยงในคอลัมน์แรกเพื่อไปที่ส่วนที่เกี่ยวข้องของหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-149">For more information about these inspections, use the links in the first column to go to the relevant sections of this topic.</span></span> <span data-ttu-id="a4e13-150">ส่วนเหล่านี้จะอธิบายชนิดของส่วนประกอบที่ ER ให้การตรวจสอบและวิธีที่คุณสามารถตั้งค่าคอนฟิกส่วนประกอบ ER เพื่อช่วยป้องกันปัญหา</span><span class="sxs-lookup"><span data-stu-id="a4e13-150">Those sections explain the types of components that ER provides inspections for and how you can reconfigure ER components to help prevent issues.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a4e13-151">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="a4e13-151">Name</span></span></th>
<th><span data-ttu-id="a4e13-152">ประเภท</span><span class="sxs-lookup"><span data-stu-id="a4e13-152">Category</span></span></th>
<th><span data-ttu-id="a4e13-153">ระดับ</span><span class="sxs-lookup"><span data-stu-id="a4e13-153">Level</span></span></th>
<th><span data-ttu-id="a4e13-154">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="a4e13-154">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4e13-155"><a href='#i1'>ชนิดการแปลง</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-155"><a href='#i1'>Type conversion</a></span></span></td>
<td><span data-ttu-id="a4e13-156">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="a4e13-156">Executability</span></span></td>
<td><span data-ttu-id="a4e13-157">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a4e13-157">Error</span></span></td>
<td>
<p><span data-ttu-id="a4e13-158">ไม่สามารถแปลงนิพจน์ชนิด &lt;ชนิด&gt; เป็นฟิลด์ชนิด &lt;ชนิด&gt;</span><span class="sxs-lookup"><span data-stu-id="a4e13-158">Cannot convert expression of type &lt;type&gt; to field of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="a4e13-159"><b>ข้อผิดพลาดรันไทม์:</b> ข้อยกเว้นสำหรับชนิด</span><span class="sxs-lookup"><span data-stu-id="a4e13-159"><b>Runtime error:</b> Exception for type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-160"><a href='#i2'>ความเข้ากันได้ของชนิด</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-160"><a href='#i2'>Type compatibility</a></span></span></td>
<td><span data-ttu-id="a4e13-161">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="a4e13-161">Executability</span></span></td>
<td><span data-ttu-id="a4e13-162">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a4e13-162">Error</span></span></td>
<td>
<p><span data-ttu-id="a4e13-163">นิพจน์ที่ตั้งค่าคอนฟิกไม่สามารถใช้ได้เนื่องจากมีการรวมกันขององค์ประกอบรูปแบบปัจจุบันไปยังแหล่งข้อมูลเป็นนิพจน์นี้ส่งคืนค่าชนิดของชนิดข้อมูล &lt;ชนิด&gt; ที่อยู่นอกขอบเขตของชนิดข้อมูลที่รองรับโดยองค์ประกอบรูปแบบปัจจุบันของชนิด &lt;ชนิด&gt;</span><span class="sxs-lookup"><span data-stu-id="a4e13-163">The configured expression cannot be used as the binding of the current format element to a data source as this expression returns value of the data type &lt;type&gt; that is beyond the scope of data types that are supported by the current format element of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="a4e13-164"><b>ข้อผิดพลาดรันไทม์:</b> ข้อยกเว้นของชนิด</span><span class="sxs-lookup"><span data-stu-id="a4e13-164"><b>Runtime error:</b> Exception of type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-165"><a href='#i3'>ขาดองค์ประกอบการตั้งค่าคอนฟิก</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-165"><a href='#i3'>Missing configuration element</a></span></span></td>
<td><span data-ttu-id="a4e13-166">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="a4e13-166">Executability</span></span></td>
<td><span data-ttu-id="a4e13-167">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a4e13-167">Error</span></span></td>
<td>
<p><span data-ttu-id="a4e13-168">ไม่พบพาธ &lt;พาธ&gt;</span><span class="sxs-lookup"><span data-stu-id="a4e13-168">Path not found &lt;path&gt;.</span></span></p>
<p><span data-ttu-id="a4e13-169"><b>ข้อผิดพลาดรันไทม์:</b> ไม่พบองค์ประกอบของพาธการตั้งค่าคอนฟิก &lt;พาธ&gt;</span><span class="sxs-lookup"><span data-stu-id="a4e13-169"><b>Runtime error:</b> Element of the configuration &lt;path&gt; not found</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-170"><a href='#i4'>ความสามารถในการปฏิบัติการนิพจน์กับฟังก์ชันตัวกรอง</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-170"><a href='#i4'>Executability of an expression with FILTER function</a></span></span></td>
<td><span data-ttu-id="a4e13-171">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="a4e13-171">Executability</span></span></td>
<td><span data-ttu-id="a4e13-172">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a4e13-172">Error</span></span></td>
<td>
<p><span data-ttu-id="a4e13-173">นิพจน์รายการของฟังก์ชัน FILTER ไม่สามารถสอบถามได้</span><span class="sxs-lookup"><span data-stu-id="a4e13-173">The list expression of FILTER function is not queryable.</span></span></p>
<p><span data-ttu-id="a4e13-174"><b>ข้อผิดพลาดรันไทม์:</b> ไม่สนับสนุนการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-174"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="a4e13-175">ตรวจสอบความถูกต้องของการตั้งค่าคอนฟิกเพื่อดูรายละเอียดเพิ่มเติมเกี่ยวกับเรื่องนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-175">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="a4e13-176"><a href='#i5'>ความสามารถในการปฏิบัติการของแหล่งข้อมูล GROUPBY</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-176"><a href='#i5'>Executability of a GROUPBY data source</a></span></span></td>
<td><span data-ttu-id="a4e13-177">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="a4e13-177">Executability</span></span></td>
<td><span data-ttu-id="a4e13-178">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a4e13-178">Error</span></span></td>
<td><span data-ttu-id="a4e13-179">พาธ &lt;พาธ&gt; ไม่รองรับการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="a4e13-179">Path &lt;path&gt; does not support querying.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-180">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="a4e13-180">Executability</span></span></td>
<td><span data-ttu-id="a4e13-181">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a4e13-181">Error</span></span></td>
<td>
<p><span data-ttu-id="a4e13-182">การจัดกลุ่มตามฟังก์ชันไม่สามารถดำเนินการโดยใช้การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="a4e13-182">Group by function cannot be executed with query.</span></span></p>
<p><span data-ttu-id="a4e13-183"><b>ข้อผิดพลาดรันไทม์:</b> การจัดกลุ่มตามฟังก์ชันไม่สามารถดำเนินการโดยใช้การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="a4e13-183"><b>Runtime error:</b> Group by function can't be executed with query.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-184"><a href='#i6'>ความสามารถในการปฏิบัติการของแหล่งข้อมูล JOIN</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-184"><a href='#i6'>Executability of a JOIN data source</a></span></span></td>
<td><span data-ttu-id="a4e13-185">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="a4e13-185">Executability</span></span></td>
<td><span data-ttu-id="a4e13-186">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a4e13-186">Error</span></span></td>
<td>
<p><span data-ttu-id="a4e13-187">ไม่สามารถรวม &lt;พาธ&gt; ของรายการที่ไม่ใช่ตัวกรองข้อมูลในการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="a4e13-187">Cannot join a list &lt;path&gt; that is not a filter in query.</span></span></p>
<p><span data-ttu-id="a4e13-188"><b>ข้อผิดพลาดรันไทม์:</b> แหล่งข้อมูลที่รวมฟังก์ชันควรเป็นนิพจน์ของตัวกรอง ฟิลด์ที่คำนวณถูกเรียกอย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-188"><b>Runtime error:</b> Function Joined datasource should be a filter expression calculated field has been incorrectly called.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-189"><a href='#i7'>ความเป็นที่ต้องการมากกว่าของฟังก์ชัน FILTER เทียบกับฟังก์ชัน WHERE</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-189"><a href='#i7'>Preferability of FILTER vs WHERE function</a></span></span></td>
<td><span data-ttu-id="a4e13-190">ประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a4e13-190">Performance</span></span></td>
<td><span data-ttu-id="a4e13-191">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="a4e13-191">Warning</span></span></td>
<td><span data-ttu-id="a4e13-192">การใช้ฟังก์ชัน FILTER สำหรับนิพจน์นี้จะเป็นที่ต้องการมากกว่า WHERE จากมุมมองประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-192">Using FILTER function for the expression is preferable than WHERE from the performance perspective.</span></span> <span data-ttu-id="a4e13-193">เลือก แก้ไข เพื่อแทนที่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-193">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-194"><a href='#i8'>ความเป็นที่ต้องการมากกว่าของฟังก์ชัน ALLITEMSQUERY เทียบกับฟังก์ชัน ALLITEMS</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-194"><a href='#i8'>Preferability of ALLITEMSQUERY vs ALLITEMS function</a></span></span></td>
<td><span data-ttu-id="a4e13-195">ประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a4e13-195">Performance</span></span></td>
<td><span data-ttu-id="a4e13-196">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="a4e13-196">Warning</span></span></td>
<td><span data-ttu-id="a4e13-197">การใช้ฟังก์ชัน ALLITEMSQUERY สำหรับนิพจน์นี้จะเป็นที่ต้องการมากกว่า ALLITEMS จากมุมมองประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-197">Using ALLITEMSQUERY function for the expression is preferable than ALLITEMS from the performance perspective.</span></span> <span data-ttu-id="a4e13-198">เลือก แก้ไข เพื่อแทนที่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-198">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-199"><a href='#i9'>การพิจารณากรณีของรายการที่ว่างเปล่า</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-199"><a href='#i9'>Consideration of empty list cases</a></span></span></td>
<td><span data-ttu-id="a4e13-200">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="a4e13-200">Executability</span></span></td>
<td><span data-ttu-id="a4e13-201">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="a4e13-201">Warning</span></span></td>
<td>
<p><span data-ttu-id="a4e13-202">รายการ &lt;พาธ&gt; ไม่มีการตรวจสอบสำหรับกรณีของรายการที่ว่างเปล่า อาจทำให้เกิดข้อผิดพลาดขณะดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a4e13-202">List &lt;path&gt; does not have any check for empty list case, it can result an error at run time.</span></span> <span data-ttu-id="a4e13-203">เพิ่มการตรวจสอบสำหรับกรณีของรายการที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="a4e13-203">Add a check for empty list case.</span></span></p>
<p><span data-ttu-id="a4e13-204"><b>ข้อผิดพลาดรันไทม์:</b> รายการว่างเปล่าที่ &lt;พาธ&gt;</span><span class="sxs-lookup"><span data-stu-id="a4e13-204"><b>Runtime error:</b> List is empty at &lt;path&gt;</span></span></p>
<p><span data-ttu-id="a4e13-205"><b><a href='#i9a'>ปัญหาที่อาจเกิดขึ้น</a>:</b> มีการเติมข้อมูลรายการหนึ่งครั้งในขณะที่แหล่งข้อมูลมีการเติมข้อมูลจากหลายเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="a4e13-205"><b><a href='#i9a'>Potential issue</a>:</b> Line is getting populated once while a data source it is populated from contains multiple records</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-206"><a href='#i10'>ความสามารถในการปฏิบัติการนิพจน์กับฟังก์ชันตัวกรอง (การแคช)</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-206"><a href='#i10'>Executability of an expression with FILTER function (caching)</a></span></span></td>
<td><span data-ttu-id="a4e13-207">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="a4e13-207">Executability</span></span></td>
<td><span data-ttu-id="a4e13-208">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a4e13-208">Error</span></span></td>
<td>
<p><span data-ttu-id="a4e13-209">ฟังก์ชัน FILTER ไม่สามารถใช้กับชนิดแหล่งข้อมูลที่เลือกได้</span><span class="sxs-lookup"><span data-stu-id="a4e13-209">FILTER function cannot be applied to the selected type of data source.</span></span> <span data-ttu-id="a4e13-210">แหล่งข้อมูลของชนิดเรกคอร์ดตารางใช้ได้เฉพาะเมื่อไม่มีการแคชไว้และไม่มีการเพิ่มแหล่งข้อมูลที่ซ้อนกันด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-210">A data source of the Table records type is applicable only when it is not cached and has no manually added nested data sources.</span></span></p>
<p><span data-ttu-id="a4e13-211"><b>ข้อผิดพลาดรันไทม์:</b> ไม่สนับสนุนการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-211"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="a4e13-212">ตรวจสอบความถูกต้องของการตั้งค่าคอนฟิกเพื่อดูรายละเอียดเพิ่มเติมเกี่ยวกับเรื่องนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-212">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-213"><a href='#i11'>ขาดการผูกข้อมูล</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-213"><a href='#i11'>Missing binding</a></span></span></td>
<td><span data-ttu-id="a4e13-214">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="a4e13-214">Executability</span></span></td>
<td><span data-ttu-id="a4e13-215">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="a4e13-215">Warning</span></span></td>
<td>
<p><span data-ttu-id="a4e13-216">พาธ &lt;พาธ&gt; ไม่มีการผูกกับแหล่งข้อมูลใด ๆ ในการใช้การแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-216">Path &lt;path&gt; has no binding to any datasource in using model's mapping.</span></span></p>
<p><span data-ttu-id="a4e13-217"><b>ข้อผิดพลาดรันไทม์:</b> พาธ &lt;พาธ&gt; ไม่ถูกผูกไว้</span><span class="sxs-lookup"><span data-stu-id="a4e13-217"><b>Runtime error:</b> Path &lt;path&gt; is not bound</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-218"><a href='#i12'>แม่แบบไม่มีการเชื่อมโยง</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-218"><a href='#i12'>Not linked template</a></span></span></td>
<td><span data-ttu-id="a4e13-219">ความสมบูรณ์ของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-219">Data integrity</span></span></td>
<td><span data-ttu-id="a4e13-220">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="a4e13-220">Warning</span></span></td>
<td><span data-ttu-id="a4e13-221">ชื่อ &lt;ไฟล์&gt; ถูกลิงค์ไปยังไม่มีส่วนประกอบของไฟล์และจะถูกลบออกหลังจากเปลี่ยนสถานะของรุ่นการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="a4e13-221">File &lt;name&gt; is linked to no file components and will be removed after changing status of configuration version.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-222"><a href='#i13'>รูปแบบที่ไม่ได้ซิงค์</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-222"><a href='#i13'>Not synced format</a></span></span></td>
<td><span data-ttu-id="a4e13-223">ความสมบูรณ์ของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-223">Data integrity</span></span></td>
<td><span data-ttu-id="a4e13-224">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="a4e13-224">Warning</span></span></td>
<td><span data-ttu-id="a4e13-225">ชื่อที่กำหนดของ &lt;ชื่อส่วนประกอบ&gt; ไม่มีอยู่ใน &lt;ชื่อแผ่นงาน&gt; แผ่นงาน Excel</span><span class="sxs-lookup"><span data-stu-id="a4e13-225">Defined name &lt;component name&gt; does not exist in Excel sheet &lt;sheet name&gt;</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-226"><a href='#i14'>รูปแบบที่ไม่ได้ซิงค์</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-226"><a href='#i14'>Not synced format</a></span></span></td>
<td><span data-ttu-id="a4e13-227">ความสมบูรณ์ของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-227">Data integrity</span></span></td>
<td><span data-ttu-id="a4e13-228">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="a4e13-228">Warning</span></span></td>
<td>
<p><span data-ttu-id="a4e13-229">&lt;แท็กการควบคุมเนื้อหา Word&gt; ไม่มีแท็กอยู่ในไฟล์เทมเพลต Word</span><span class="sxs-lookup"><span data-stu-id="a4e13-229">&lt;Tagged Word content control&gt; tag does not exist in Word template file</span></span></p>
<p><span data-ttu-id="a4e13-230"><b>การทำงานผิดพลาด:</b> &lt;แท็กการควบคุมเนื้อหา Word&gt; ไม่มีแท็กอยู่ในไฟล์เทมเพลต Word</span><span class="sxs-lookup"><span data-stu-id="a4e13-230"><b>Runtime error:</b> &lt;Tagged Word content control&gt; tag does not exist in Word template file.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-231"><a href='#i15'>ไม่มีการแม็ปเริ่มต้น</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-231"><a href='#i15'>No default mapping</a></span></span></td>
<td><span data-ttu-id="a4e13-232">ความสมบูรณ์ของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-232">Data integrity</span></span></td>
<td><span data-ttu-id="a4e13-233">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a4e13-233">Error</span></span></td>
<td>
<p><span data-ttu-id="a4e13-234">มีการแม็ปแบบแผนที่มากกว่าหนึ่งแบบเกิดขึ้นสำหรับการกำหนดค่าคอนฟิก &lt;ชื่อแบบจำลอง (ตัวบอกราก)&gt; แบบจำลองข้อมูลในการกำหนดค่าคอนฟิก &lt;ที่เรียกแยกกันโดยมีเครื่องหมายจุลภาคคั่น&gt;</span><span class="sxs-lookup"><span data-stu-id="a4e13-234">More than one model mapping exists for the &lt;model name (root descriptor)&gt; data model in the configurations &lt;configuration names separated by comma&gt;.</span></span> <span data-ttu-id="a4e13-235">ตั้งค่าการกําหนดค่าคอนฟิกค่าใดค่าหนึ่งเป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-235">Set one of the configurations as default</span></span></p>
<p><span data-ttu-id="a4e13-236"><b>การทำงานผิดพลาด:</b> มีการแมปแบบจำลองมากกว่าหนึ่งรายการสำหรับการกำหนดค่าคอนฟิก &lt;ชื่อแบบจำลอง (ตัวบอกราก)&gt; แบบจำลองข้อมูลในการกำหนดค่าคอนฟิก &lt;ที่เรียกแยกกันโดยมีเครื่องหมายจุลภาคคั่น&gt;</span><span class="sxs-lookup"><span data-stu-id="a4e13-236"><b>Runtime error:</b> More than one model mapping exists for the &lt;model name (root descriptor)&gt; data model in the configurations &lt;configuration names separated by comma&gt;.</span></span> <span data-ttu-id="a4e13-237">กําหนดการตั้งค่าคอนฟิกตัวใดค่าหนึ่งเป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-237">Set one of the configurations as default.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a4e13-238"><a href='#i16'>การตั้งค่าส่วนประกอบส่วนหัวหรือส่วนท้ายไม่สอดคล้องกัน</a></span><span class="sxs-lookup"><span data-stu-id="a4e13-238"><a href='#i16'>Inconsistent setting of Header or Footer components</a></span></span></td>
<td><span data-ttu-id="a4e13-239">ความสมบูรณ์ของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-239">Data integrity</span></span></td>
<td><span data-ttu-id="a4e13-240">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a4e13-240">Error</span></span></td>
<td>
<p><span data-ttu-id="a4e13-241">ส่วนหัว/ส่วนท้าย (&lt;ชนิดของส่วนประกอบ: ส่วนหัวหรือส่วนท้าย&gt;) ไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-241">Headers/footers (&lt;component type: Header or Footer&gt;) are inconsistent</span></span></p>
<p><span data-ttu-id="a4e13-242"><b>รันไทม์:</b> จะใช้ส่วนประกอบที่กำหนดค่าคอนฟิกล่าสุดในช่วงรันไทม์ ถ้ามีการเรียกใช้เวอร์ชันแบบร่างของรูปแบบ ER ที่กำหนดค่าคอนฟิกไว้</span><span class="sxs-lookup"><span data-stu-id="a4e13-242"><b>Runtime:</b> The last configured component is used at runtime if the draft version of the configured ER format is executed.</span></span></p>
</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a><span data-ttu-id="a4e13-243">ชนิดการแปลง</span><span class="sxs-lookup"><span data-stu-id="a4e13-243">Type conversion</span></span>

<span data-ttu-id="a4e13-244">ER จะตรวจสอบว่าชนิดข้อมูลของฟิลด์รูปแบบข้อมูลเข้ากันได้กับชนิดข้อมูลของนิพจน์ที่มีการตั้งค่าคอนฟิกเป็นการรวมของฟิลด์นั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-244">ER checks whether the data type of a data model field is compatible with the data type of an expression that is configured as the binding of that field.</span></span> <span data-ttu-id="a4e13-245">หากชนิดข้อมูลเข้ากันไม่ได้ ข้อผิดพลาดในการตรวจสอบความถูกต้องเกิดขึ้นในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-245">If the data types are incompatible, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a4e13-246">ข้อความที่คุณได้รับระบุว่า ER ไม่สามารถแปลงนิพจน์ชนิด A ไปยังฟิลด์ชนิด B</span><span class="sxs-lookup"><span data-stu-id="a4e13-246">The message that you receive states that ER can't convert an expression of type A to a field of type B.</span></span>

<span data-ttu-id="a4e13-247">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-247">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-248">เริ่มต้นการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER และส่วนประกอบการแม็ปแบบจำลอง ER พร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-248">Start to configure the ER data model and the ER model mapping components simultaneously.</span></span>
2. <span data-ttu-id="a4e13-249">ในแผนภูมิรูปแบบข้อมูล ให้เพิ่มฟิลด์ที่ชื่อ **X** และเลือก **จำนวนเต็ม** เป็นชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-249">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![ชนิดของฟิลด์ X และข้อมูลจำนวนเต็มที่เพิ่มลงในแผนภูมิโหมดข้อมูลบนหน้ารูปแบบข้อมูล](./media/er-components-inspections-01.png)

3. <span data-ttu-id="a4e13-251">ในตัวออกแบบการแม็ปแบบจำลอง ในบานหน้าต่าง **ที่มาของข้อมูล** ให้เพิ่มที่มาของข้อมูลของชนิด **ฟิลด์จากการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-251">In the model mapping designer, in the **Data sources** pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="a4e13-252">ตั้งชื่อแหล่งข้อมูล **Y** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `INTVALUE(100)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-252">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="a4e13-253">ผูก **X** กับ **Y**</span><span class="sxs-lookup"><span data-stu-id="a4e13-253">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="a4e13-254">ในตัวออกแบบรูปแบบข้อมูล ให้เปลี่ยนชนิดข้อมูลของฟิลด์ **X** จาก **จำนวนเต็ม** เป็น **Int64**</span><span class="sxs-lookup"><span data-stu-id="a4e13-254">In the data model designer, change the data type of the **X** field from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="a4e13-255">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-255">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![ตรวจสอบความถูกต้องส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-01.gif)

8. <span data-ttu-id="a4e13-257">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองของการตั้งค่าคอนฟิก ER ที่เลือกบนหน้า **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="a4e13-257">Select **Validate** to inspect the model mapping component of the selected ER configuration on the **Configurations** page.</span></span>

    ![การตรวจสอบส่วนประกอบของการแม็ปแบบจำลองในหน้าการกำหนดค่าคอนฟิก](./media/er-components-inspections-01a.png)

9. <span data-ttu-id="a4e13-259">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-259">Notice that a validation error occurs.</span></span> <span data-ttu-id="a4e13-260">ข้อความระบุว่าค่าของชนิด **จำนวนเต็ม** ที่นิพจน์ `INTVALUE(100)` ของการส่งคืนแหล่งข้อมูล **Y** ไม่สามารถจัดเก็บในฟิลด์รูปแบบข้อมูล **X** ของ ชนิด **Int64**</span><span class="sxs-lookup"><span data-stu-id="a4e13-260">The message states that the value of the **Integer** type that the `INTVALUE(100)` expression of the **Y** data source returns can't be stored in the **X** data model field of the **Int64** type.</span></span>

<span data-ttu-id="a4e13-261">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้นถ้าคุณละเว้นคำเตือนและเลือก **รัน** เพื่อรันรูปแบบที่มีการตั้งค่าคอนฟิกให้ใช้การแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-261">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![ข้อผิดพลาดรันไทม์บนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-263">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-263">Automatic resolution</span></span>

<span data-ttu-id="a4e13-264">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-264">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-265">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-265">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a4e13-266">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="a4e13-266">Option 1</span></span>

<span data-ttu-id="a4e13-267">อัปเดตโครงสร้างรูปแบบข้อมูลด้วยการเปลี่ยนชนิดข้อมูลของฟิลด์รูปแบบข้อมูลเพื่อให้ตรงกับชนิดข้อมูลของนิพจน์ที่มีการตั้งค่าคอนฟิกไว้สำหรับการผูกข้อมูลของฟิลด์นั้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-267">Update the data model structure by changing the data type of the data model field so that it matches the data type of the expression that is configured for the binding of that field.</span></span> <span data-ttu-id="a4e13-268">สำหรับตัวอย่างก่อนหน้านี้ ชนิดข้อมูลของฟิลด์ **X** ต้องเปลี่ยนให้เป็น **จำนวนเต็ม**</span><span class="sxs-lookup"><span data-stu-id="a4e13-268">For the preceding example, the data type of the **X** field must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a4e13-269">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="a4e13-269">Option 2</span></span>

<span data-ttu-id="a4e13-270">อัปเดตการแม็ปแบบจำลองด้วยการเปลี่ยนนิพจน์ของแหล่งข้อมูลที่ผูกกับฟิลด์รูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-270">Update the model mapping by changing the expression of the data source that is bound with the data model field.</span></span> <span data-ttu-id="a4e13-271">สำหรับตัวอย่างก่อนหน้านี้ นิพจน์ของแหล่งข้อมูล **Y** ต้องเปลี่ยนเป็น `INT64VALUE(100)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-271">For the preceding example, the expression of the **Y** data source must be changed to `INT64VALUE(100)`.</span></span>

## <a name="type-compatibility"></a><a id="i2"></a><span data-ttu-id="a4e13-272">ความเข้ากันได้ของชนิด</span><span class="sxs-lookup"><span data-stu-id="a4e13-272">Type compatibility</span></span>

<span data-ttu-id="a4e13-273">ER จะตรวจสอบว่าชนิดข้อมูลขององค์ประกอบรูปแบบเข้ากันได้กับชนิดข้อมูลของนิพจน์ที่มีการตั้งค่าคอนฟิกเป็นการรวมขององค์ประกอบรูปแบบนั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-273">ER checks whether the data type of a format element is compatible with the data type of an expression that is configured as the binding of that format element.</span></span> <span data-ttu-id="a4e13-274">หากชนิดข้อมูลเข้ากันไม่ได้ ข้อผิดพลาดในการตรวจสอบความถูกต้องเกิดขึ้นในโปรแกรมออกแบบการดำเนินงาน ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-274">If the data types are incompatible, a validation error occurs in the ER Operations designer.</span></span> <span data-ttu-id="a4e13-275">ข้อความที่คุณได้รับระบุว่านิพจน์ที่ตั้งค่าคอนฟิกไม่สามารถใช้ได้เนื่องจากมีการรวมกันขององค์ประกอบรูปแบบปัจจุบันไปยังแหล่งข้อมูล เนื่องจากนิพจน์นี้ส่งคืนค่าชนิดของชนิดข้อมูล A ที่อยู่นอกขอบเขตของชนิดข้อมูลที่รองรับโดยองค์ประกอบรูปแบบปัจจุบันของชนิด B</span><span class="sxs-lookup"><span data-stu-id="a4e13-275">The message that you receive states that the configured expression can't be used as the binding of the current format element to a data source, because the expression returns a value of data type A that is beyond the scope of the data types that are supported by the current format element of type B.</span></span>

<span data-ttu-id="a4e13-276">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-276">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-277">เริ่มต้นการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER และส่วนประกอบการรูปแบบ ER พร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-277">Start to configure the ER data model and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="a4e13-278">ในแผนภูมิรูปแบบข้อมูล ให้เพิ่มฟิลด์ที่ชื่อ **X** และเลือก **จำนวนเต็ม** เป็นชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-278">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>
3. <span data-ttu-id="a4e13-279">ในแผนภูมิโครงสร้างรูปแบบ ให้เพิ่มองค์ประกอบรูปแบบของชนิด **ตัวเลข**</span><span class="sxs-lookup"><span data-stu-id="a4e13-279">In the format structure tree, add a format element of the **Numeric** type.</span></span>
4. <span data-ttu-id="a4e13-280">ชื่อองค์ประกอบรูปแบบใหม่ **Y** ในฟิลด์ **ชนิดตัวเลข** ให้เลือก **จำนวนเต็ม** เป็นชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-280">Name the new format element **Y**. In the **Numeric type** field, select **Integer** as the data type.</span></span>
5. <span data-ttu-id="a4e13-281">ผูก **X** กับ **Y**</span><span class="sxs-lookup"><span data-stu-id="a4e13-281">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="a4e13-282">ในแผนภูมิโครงสร้างรูปแบบ ให้เปลี่ยนชนิดข้อมูลขององค์ประกอบรูปแบบ **Y** จาก **เลขจำนวนเต็ม** เป็น **Int64**</span><span class="sxs-lookup"><span data-stu-id="a4e13-282">In the format structure tree, change the data type of the **Y** format element from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="a4e13-283">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของรูปแบบที่แก้ไขได้บนหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-283">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![กำลังตรวจสอบความเข้ากันได้ของชนิดบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-02.gif)

8. <span data-ttu-id="a4e13-285">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-285">Notice that a validation error occurs.</span></span> <span data-ttu-id="a4e13-286">ข้อความระบุว่านิพจน์ที่ตั้งค่าคอนฟิกสามารถยอมรับได้เฉพาะค่า **Int64**</span><span class="sxs-lookup"><span data-stu-id="a4e13-286">The message states that the configured expression can accept only **Int64** values.</span></span> <span data-ttu-id="a4e13-287">ดังนั้น ค่าของฟิลด์รูปแบบข้อมูล **X** ของชนิด **จำนวนเต็ม** ไม่สามารถป้อนในองค์ประกอบรูปแบบ **Y**</span><span class="sxs-lookup"><span data-stu-id="a4e13-287">Therefore, the value of the **X** data model field of the **Integer** type can't be entered in the **Y** format element.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-288">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-288">Automatic resolution</span></span>

<span data-ttu-id="a4e13-289">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-289">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-290">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-290">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a4e13-291">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="a4e13-291">Option 1</span></span>

<span data-ttu-id="a4e13-292">อัปเดตโครงสร้างรูปแบบด้วยการเปลี่ยนชนิดข้อมูลขององค์ประกอบรูปแบบ **ตัวเลข** เพื่อให้ตรงกับชนิดข้อมูลของนิพจน์ ที่คุณตั้งค่าคอนฟิกไว้สำหรับการผูกข้อมูลขององค์ประกอบนั้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-292">Update the format structure by changing the data type of the **Numeric** format element so that it matches the data type of the expression that you configured for the binding of that element.</span></span> <span data-ttu-id="a4e13-293">ในตัวอย่างก่อนหน้านี้ ค่า **ชนิดตัวเลข** ขององค์ประกอบรูปแบบ **X** ต้องเปลี่ยนให้เป็น **จำนวนเต็ม**</span><span class="sxs-lookup"><span data-stu-id="a4e13-293">In the preceding example, the **Numeric type** value of the **X** format element must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a4e13-294">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="a4e13-294">Option 2</span></span>

<span data-ttu-id="a4e13-295">อัปเดตการแม็ปรูปแบบขององค์ประกอบรูปแบบ **X** โดยการเปลี่ยนแปลงนิพจน์จาก `model.X` เป็น `INT64VALUE(model.X)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-295">Update the format mapping of the **X** format element by changing the expression from `model.X` to `INT64VALUE(model.X)`.</span></span>

## <a name="missing-configuration-element"></a><a id="i3"></a><span data-ttu-id="a4e13-296">ขาดองค์ประกอบการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="a4e13-296">Missing configuration element</span></span>

<span data-ttu-id="a4e13-297">ER ตรวจสอบว่านิพจน์การผูกมีเฉพาะแหล่งข้อมูลที่มีการตั้งค่าคอนฟิกในส่วนประกอบ ER ที่แก้ไขได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-297">ER checks whether the binding expressions contain only data sources that are configured in the editable ER component.</span></span> <span data-ttu-id="a4e13-298">สำหรับการผูกทั้งหมดที่มีแหล่งข้อมูลที่ขาดหายไปในส่วนประกอบ ER ที่แก้ไขได้ เกิดข้อผิดพลาดในการตรวจสอบความถูกต้องในตัวออกแบบการดำเนินงาน ER หรือตัวออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-298">For every binding that contains a data source that is missing in the editable ER component, a validation error occurs in the ER Operations designer or the ER model mapping designer.</span></span>

<span data-ttu-id="a4e13-299">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-299">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-300">เริ่มต้นการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER และส่วนประกอบการแม็ปแบบจำลอง ER พร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-300">Start to configure the ER data model and the ER model mapping components simultaneously.</span></span>
2. <span data-ttu-id="a4e13-301">ในแผนภูมิรูปแบบข้อมูล ให้เพิ่มฟิลด์ที่ชื่อ **X** และเลือก **จำนวนเต็ม** เป็นชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-301">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![แผนภูมิรูปแบบข้อมูลของฟิลด์ X และข้อมูลจำนวนเต็มบนหน้ารูปแบบข้อมูล](./media/er-components-inspections-01.png)

3. <span data-ttu-id="a4e13-303">ในตัวออกแบบการแม็ปแบบจำลอง ในบานหน้าต่าง **ที่มาของข้อมูล** ให้เพิ่มที่มาของข้อมูลของชนิด **ฟิลด์จากการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-303">In the model mapping designer, in the **Data sources** pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="a4e13-304">ตั้งชื่อแหล่งข้อมูล **Y** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `INTVALUE(100)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-304">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="a4e13-305">ผูก **X** กับ **Y**</span><span class="sxs-lookup"><span data-stu-id="a4e13-305">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="a4e13-306">ในตัวออกแบบการแม็ปแบบจำลอง ในบานหน้าต่าง **แหล่งข้อมูล** ให้ลบแหล่งข้อมูล **Y**</span><span class="sxs-lookup"><span data-stu-id="a4e13-306">In the model mapping designer, in the **Data sources** pane, delete the **Y** data source.</span></span>
7. <span data-ttu-id="a4e13-307">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-307">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![การตรวจสอบส่วนประกอบของการแม็ปแบบจำลอง ER ที่แก้ไขได้บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-03.gif)

8. <span data-ttu-id="a4e13-309">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-309">Notice that a validation error occurs.</span></span> <span data-ttu-id="a4e13-310">ข้อความระบุว่าการผูกกันของฟิลด์รูปแบบข้อมูล **X** มีพาธที่อ้างอิงถึงแหล่งข้อมูล **Y** แต่ไม่พบแหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-310">The message states that the binding of the **X** data model field contains the path that refers to the **Y** data source, but this data source isn't found.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-311">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-311">Automatic resolution</span></span>

<span data-ttu-id="a4e13-312">เลือก **ยกเลิกการผูก** เพื่อแก้ไขปัญหานี้โดยอัตโนมัติโดยการลบการผูกข้อมูลแหล่งข้อมูลที่ขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="a4e13-312">Select **Unbind** to automatically fix this issue by removing the missing data source binding.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-313">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-313">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a4e13-314">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="a4e13-314">Option 1</span></span>

<span data-ttu-id="a4e13-315">ยกเลิกการผูกฟิลด์รูปแบบข้อมูล **X** เพื่อหยุดการอ้างอิงถึงแหล่งข้อมูล **Y** ที่ไม่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a4e13-315">Unbind the **X** data model field to stop referring to the nonexistent **Y** data source.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a4e13-316">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="a4e13-316">Option 2</span></span>

<span data-ttu-id="a4e13-317">ในตัวออกแบบการแม็ปแบบจำลอง ในบานหน้าต่าง **แหล่งข้อมูล** ให้เพิ่มแหล่งข้อมูล **Y** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a4e13-317">In the model mapping designer, in the **Data sources** pane, add the **Y** data source again.</span></span>

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a><span data-ttu-id="a4e13-318">ความสามารถในการปฏิบัติการนิพจน์กับฟังก์ชันตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-318">Executability of an expression with FILTER function</span></span>

<span data-ttu-id="a4e13-319">ฟังก์ชัน ER [FILTER](er-functions-list-filter.md) ที่มีอยู่แล้วภายในใช้เพื่อเข้าถึงตารางของโปรแกรมประยุกต์ มุมมอง หรือเอนทิตีข้อมูลโดยการวางการเรียก SQL เดียวเพื่อให้ได้ข้อมูลที่จำเป็นในฐานะรายการของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="a4e13-319">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="a4e13-320">แหล่งข้อมูลของชนิด **รายการเรกคอร์ด** ถูกใช้เป็นอาร์กิวเมนต์ของฟังก์ชันนี้และระบุแหล่งที่มาของโปรแกรมประยุกต์สำหรับการโทร</span><span class="sxs-lookup"><span data-stu-id="a4e13-320">A data source of the **Record list** type is used as an argument of this function and specifies the application source for the call.</span></span> <span data-ttu-id="a4e13-321">ER ตรวจสอบว่าสามารถสร้างการสอบถาม SQL โดยตรงกับแหล่งข้อมูลที่อ้างถึงในฟังก์ชัน `FILTER` หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-321">ER checks whether a direct SQL query can be established to a data source that is referred to in the `FILTER` function.</span></span> <span data-ttu-id="a4e13-322">ถ้าไม่สามารถสร้างการสอบถามโดยตรงได้ เกิดข้อผิดพลาดในการตรวจสอบความถูกต้องในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-322">If a direct query can't be established, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a4e13-323">ข้อความที่คุณได้รับแจ้งว่านิพจน์ ER ที่มีฟังก์ชัน `FILTER` ไม่สามารถรันในขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-323">The message that you receive states that the ER expression that includes the `FILTER` function can't be run at runtime.</span></span>

<span data-ttu-id="a4e13-324">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-324">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-325">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-325">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a4e13-326">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-326">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a4e13-327">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-327">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a4e13-328">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="a4e13-328">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="a4e13-329">เพิ่มแหล่งข้อมูลของชนิด **ฟิลด์ที่มีการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-329">Add a data source of the **Calculated field** type.</span></span>
5. <span data-ttu-id="a4e13-330">ตั้งชื่อแหล่งข้อมูล **FilteredVendor** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `FILTER(Vendor, Vendor.AccountNum="US-101")`</span><span class="sxs-lookup"><span data-stu-id="a4e13-330">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="a4e13-331">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** และตรวจสอบว่านิพจน์ `FILTER(Vendor, Vendor.AccountNum="US-101")` ในแหล่งข้อมูล **ผู้จัดจำหน่าย** สามารถสอบถามได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-331">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>
7. <span data-ttu-id="a4e13-332">ปรับเปลี่ยนแหล่งข้อมูล **ผู้จัดจำหน่าย** โดยการเพิ่มฟิลด์ที่ซ้อนกันของชนิด **ฟิลด์ที่คำนวณได้** เพื่อให้ได้หมายเลขบัญชีผู้จัดจำหน่ายที่ตัด</span><span class="sxs-lookup"><span data-stu-id="a4e13-332">Modify the **Vendor** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="a4e13-333">ตั้งชื่อฟิลด์ที่ซ้อนกัน **$AccNumber** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `TRIM(Vendor.AccountNum)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-333">Name the new nested field **$AccNumber**, and configure it so that it contains the expression `TRIM(Vendor.AccountNum)`.</span></span>
9. <span data-ttu-id="a4e13-334">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** และตรวจสอบว่านิพจน์ `FILTER(Vendor, Vendor.AccountNum="US-101")` ในแหล่งข้อมูล **ผู้จัดจำหน่าย** สามารถสอบถามได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-334">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>

    ![การตรวจสอบว่าการดำเนินงานสามารถสอบถามบนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-04.gif)

10. <span data-ttu-id="a4e13-336">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง เนื่องจากแหล่งข้อมูล **ผู้จัดจำหน่าย** ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิด **ฟิลด์ที่คำนวณได้** ที่ไม่อนุญาตให้มีการแปลนิพจน์ของแหล่งข้อมูล **FilteredVendor** ที่คำสั่ง SQL โดยตรง</span><span class="sxs-lookup"><span data-stu-id="a4e13-336">Notice that a validation error occurs, because the **Vendor** data source contains a nested field of the **Calculated field** type that doesn't allow the expression of the **FilteredVendor** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="a4e13-337">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้นถ้าคุณละเว้นคำเตือนและเลือก **รัน** เพื่อรันรูปแบบที่มีการตั้งค่าคอนฟิกให้ใช้การแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-337">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![ข้อผิดพลาดรันไทม์ที่เกิดขึ้นเมื่อคุณรันการจัดรูปแบบที่แก้ไขได้บนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-339">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-339">Automatic resolution</span></span>

<span data-ttu-id="a4e13-340">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-340">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-341">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-341">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a4e13-342">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="a4e13-342">Option 1</span></span>

<span data-ttu-id="a4e13-343">แทนที่จะเพิ่มฟิลด์ที่ซ้อนกันของชนิด **ฟิลด์ที่คำนวณได้** ให้กับแหล่งข้อมูล **ผู้จัดจำหน่าย** ให้เพิ่มฟิลด์ **$AccNumber** ที่ซ้อนกันลงในแหล่งข้อมูล **FilteredVendor** และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `TRIM(FilteredVendor.AccountNum)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-343">Instead of adding a nested field of the **Calculated field** type to the **Vendor** data source, add the **$AccNumber** nested field to the **FilteredVendor** data source, and configure it so that it contains the expression `TRIM(FilteredVendor.AccountNum)`.</span></span> <span data-ttu-id="a4e13-344">ด้วยวิธีนี้ นิพจน์ `FILTER(Vendor, Vendor.AccountNum="US-101")` สามารถรันในระดับ SQL และคำนวณฟิลด์ **$AccNumbe** ที่ซ้อนกันได้ภายหลัง</span><span class="sxs-lookup"><span data-stu-id="a4e13-344">In this way, the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a4e13-345">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="a4e13-345">Option 2</span></span>

<span data-ttu-id="a4e13-346">เปลี่ยนนิพจน์ของแหล่งข้อมูล **FilteredVendor** จาก `FILTER(Vendor, Vendor.AccountNum="US-101")` เป็น `WHERE(Vendor, Vendor.AccountNum="US-101")`</span><span class="sxs-lookup"><span data-stu-id="a4e13-346">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="a4e13-347">เราไม่แนะนำให้คุณเปลี่ยนนิพจน์สำหรับตารางที่มีจำนวนมากของข้อมูล (ตารางธุรกรรม) เนื่องจากเรกคอร์ดทั้งหมดจะถูกนำมาใช้และการเลือกเรกคอร์ดที่ต้องการจะดำเนินการในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="a4e13-347">We don't recommend that you change the expression for a table that has a large volume of data (transactional table), because all records will be fetched, and selection of the required records will be done in memory.</span></span> <span data-ttu-id="a4e13-348">วิธีการนี้อาจทำให้ประสิทธิภาพการทำงานดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-348">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="a4e13-349">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ฟังก์ชัน WHERE ER](er-functions-list-where.md)</span><span class="sxs-lookup"><span data-stu-id="a4e13-349">For more information, see [WHERE ER function](er-functions-list-where.md).</span></span>

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a><span data-ttu-id="a4e13-350">ความสามารถในการปฏิบัติการของแหล่งข้อมูล GROUPBY</span><span class="sxs-lookup"><span data-stu-id="a4e13-350">Executability of a GROUPBY data source</span></span>

<span data-ttu-id="a4e13-351">แหล่งข้อมูล **GROUPBY** แบ่งผลลัพธ์การสอบถามเป็นกลุ่มของเรกคอร์ด โดยทั่วไปจะใช้เพื่อวัตถุประสงค์ในการทำการรวมหนึ่งรายการขึ้นไปในแต่ละกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="a4e13-351">The **GROUPBY** data source divides the query result into groups of records, usually for the purpose of doing one or more aggregations on each group.</span></span> <span data-ttu-id="a4e13-352">ทุกแหล่งข้อมูล **GROUPBY** สามารถตั้งค่าคอนฟิกได้เพื่อให้รันในระดับฐานข้อมูลหรือในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="a4e13-352">Every **GROUPBY** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="a4e13-353">เมื่อตั้งค่าคอนฟิกแหล่งข้อมูล **GROUPBY** เพื่อให้รันในระดับฐานข้อมูล ER จะตรวจสอบว่าสามารถสร้างการสอบถาม SQL โดยตรงกับแหล่งข้อมูลที่อ้างถึงในแหล่งข้อมูลนั้นได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-353">When a **GROUPBY** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to a data source that is referred to in that data source.</span></span> <span data-ttu-id="a4e13-354">ถ้าไม่สามารถสร้างการสอบถามโดยตรงได้ เกิดข้อผิดพลาดในการตรวจสอบความถูกต้องในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-354">If a direct query can't be established, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a4e13-355">ข้อความที่คุณได้รับระบุว่าแหล่งข้อมูล **GROUPBY** ที่ตั้งค่าคอนฟิกไม่สามารถรันในขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-355">The message that you receive states that the configured **GROUPBY** data source can't be run at runtime.</span></span>

<span data-ttu-id="a4e13-356">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-356">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-357">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-357">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a4e13-358">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-358">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a4e13-359">ตั้งชื่อแหล่งข้อมูลใหม่ **Trans** ในฟิลด์ **ตาราง** ให้เลือก **VendTrans** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTrans</span><span class="sxs-lookup"><span data-stu-id="a4e13-359">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="a4e13-360">เพิ่มแหล่งข้อมูลของชนิด **จัดกลุ่มตาม**</span><span class="sxs-lookup"><span data-stu-id="a4e13-360">Add a data source of the **Group by** type.</span></span>
5. <span data-ttu-id="a4e13-361">ตั้งชื่อแหล่งข้อมูลใหม่ **GroupedTrans** และตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a4e13-361">Name the new data source **GroupedTrans**, and configure it in the following way:</span></span>

    - <span data-ttu-id="a4e13-362">เลือกแหล่งข้อมูล **Trans** เป็นแหล่งที่มาของเรกคอร์ดที่ควรมีการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="a4e13-362">Select the **Trans** data source as the source of records that should be grouped.</span></span>
    - <span data-ttu-id="a4e13-363">ในฟิลด์ **สถานที่การดำเนินการ** ให้เลือก **การสอบถาม** เพื่อระบุว่าคุณต้องการรันแหล่งข้อมูลนี้ในระดับฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-363">In the **Execution location** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![กำลังตั้งค่าคอนฟิกแหล่งข้อมูลบนหน้าแก้ไขพารามิเตอร์ 'จัดกลุ่มตาม'](./media/er-components-inspections-05a.gif)

6. <span data-ttu-id="a4e13-365">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** และตรวจสอบว่าแหล่งข้อมูล **GroupedTrans** ที่ตั้งค่าคอนฟิกสามารถสอบถามได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-365">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>
7. <span data-ttu-id="a4e13-366">ปรับเปลี่ยนแหล่งข้อมูล **Trans** โดยการเพิ่มฟิลด์ที่ซ้อนกันของชนิด **ฟิลด์ที่คำนวณได้** เพื่อให้ได้หมายเลขบัญชีผู้จัดจำหน่ายที่ตัด</span><span class="sxs-lookup"><span data-stu-id="a4e13-366">Modify the **Trans** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="a4e13-367">ตั้งชื่อแหล่งข้อมูล **$AccNumber** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `TRIM(Trans.AccountNum)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-367">Name the new data source **$AccNumber**, and configure it so that it contains the expression `TRIM(Trans.AccountNum)`.</span></span>

    ![ตั้งค่าคอนฟิกแหล่งข้อมูล Trans ในหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-05a.png)

9. <span data-ttu-id="a4e13-369">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** และตรวจสอบว่าแหล่งข้อมูล **GroupedTrans** ที่ตั้งค่าคอนฟิกสามารถสอบถามได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-369">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>

    ![ตรวจสอบความถูกต้องของส่วนประกอบการแม็ปแบบจำลอง ER และการตรวจสอบว่าสามารถสอบถามแหล่งข้อมูล GroupedTrans ได้บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-05b.png)

10. <span data-ttu-id="a4e13-371">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง เนื่องจากแหล่งข้อมูล **Trans** ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิด **ฟิลด์ที่คำนวณได้** ที่ไม่อนุญาตให้มีการเรียกใช้งานแหล่งข้อมูล **GroupedTrans** ที่คำสั่ง SQL โดยตรง</span><span class="sxs-lookup"><span data-stu-id="a4e13-371">Notice that a validation error occurs, because the **Trans** data source contains a nested field of the **Calculated field** type that doesn't allow the call for the **GroupedTrans** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="a4e13-372">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้นถ้าคุณละเว้นคำเตือนและเลือก **รัน** เพื่อรันรูปแบบที่มีการตั้งค่าคอนฟิกให้ใช้การแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-372">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![ข้อผิดพลาดรันไทม์ที่เกิดขึ้นเมื่อคำเตือนถูกละเว้นบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-374">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-374">Automatic resolution</span></span>

<span data-ttu-id="a4e13-375">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-375">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-376">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-376">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a4e13-377">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="a4e13-377">Option 1</span></span>

<span data-ttu-id="a4e13-378">แทนที่จะเพิ่มฟิลด์ที่ซ้อนกันของชนิด **ฟิลด์ที่คำนวณได้** ให้กับแหล่งข้อมูล **Trans** ให้เพิ่มฟิลด์ **$AccNumber** ที่ซ้อนกันสำหรับรายการ **GroupedTrans.lines** ของแหล่งข้อมูล **GroupedTrans** และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `TRIM(GroupedTrans.lines.AccountNum)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-378">Instead of adding a nested field of the **Calculated field** type to the **Trans** data source, add the **$AccNumber** nested field for the **GroupedTrans.lines** item of the **GroupedTrans** data source, and configure it so that it contains the expression `TRIM(GroupedTrans.lines.AccountNum)`.</span></span> <span data-ttu-id="a4e13-379">ด้วยวิธีนี้ แหล่งข้อมูล **GroupedTrans** สามารถรันในระดับ SQL และคำนวณฟิลด์ **$AccNumber** ที่ซ้อนกันได้ภายหลัง</span><span class="sxs-lookup"><span data-stu-id="a4e13-379">In this way, the **GroupedTrans** data source can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a4e13-380">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="a4e13-380">Option 2</span></span>

<span data-ttu-id="a4e13-381">เปลี่ยนค่าของฟิลด์ **สถานที่การดำเนินการ** สำหรับแหล่งข้อมูล **GroupedTrans** จาก **การสอบถาม** เป็น **ในหน่วยความจำ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-381">Change the value of the **Execution location** field for the **GroupedTrans** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="a4e13-382">เราไม่แนะนำให้คุณเปลี่ยนค่าสำหรับตารางที่มีจำนวนมากของข้อมูล (ตารางธุรกรรม) เนื่องจากเรกคอร์ดทั้งหมดจะถูกนำมาใช้ และการจัดกลุ่มและการรวมจะดำเนินการในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="a4e13-382">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and grouping and aggregation will be done in memory.</span></span> <span data-ttu-id="a4e13-383">วิธีการนี้อาจทำให้ประสิทธิภาพการทำงานดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-383">Therefore, this approach can cause poor performance.</span></span>

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a><span data-ttu-id="a4e13-384">ความสามารถในการปฏิบัติการของแหล่งข้อมูล JOIN</span><span class="sxs-lookup"><span data-stu-id="a4e13-384">Executability of a JOIN data source</span></span>

<span data-ttu-id="a4e13-385">แหล่งข้อมูล [JOIN](er-join-data-sources.md) จะรวมเรกคอร์ดจากตารางฐานข้อมูลสองตารางขึ้นไป โดยขึ้นอยู่กับฟิลด์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-385">The [JOIN](er-join-data-sources.md) data source combines records from two or more database tables, based on related fields.</span></span> <span data-ttu-id="a4e13-386">ทุกแหล่งข้อมูล **JOIN** สามารถตั้งค่าคอนฟิกได้เพื่อให้รันในระดับฐานข้อมูลหรือในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="a4e13-386">Every **JOIN** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="a4e13-387">เมื่อตั้งค่าคอนฟิกแหล่งข้อมูล **JOIN** เพื่อให้รันในระดับฐานข้อมูล ER จะตรวจสอบว่าสามารถสร้างการสอบถาม SQL โดยตรงกับแหล่งข้อมูลที่อ้างถึงในแหล่งข้อมูลนั้นได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-387">When a **JOIN** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to data sources that are referred to in that data source.</span></span> <span data-ttu-id="a4e13-388">ถ้าไม่สามารถสร้างการสอบถาม SQL โดยตรงได้ด้วยอย่างน้อยหนึ่งแหล่งข้อมูลอ้างอิง เกิดข้อผิดพลาดในการตรวจสอบความถูกต้องในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-388">If a direct SQL query can't be established with at least one referenced data source, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a4e13-389">ข้อความที่คุณได้รับระบุว่าแหล่งข้อมูล **JOIN** ที่ตั้งค่าคอนฟิกไม่สามารถรันในขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-389">The message that you receive states that the configured **JOIN** data source can't be run at runtime.</span></span>

<span data-ttu-id="a4e13-390">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-390">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-391">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-391">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a4e13-392">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-392">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a4e13-393">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-393">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a4e13-394">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="a4e13-394">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="a4e13-395">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-395">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
5. <span data-ttu-id="a4e13-396">ตั้งชื่อแหล่งข้อมูลใหม่ **Trans** ในฟิลด์ **ตาราง** ให้เลือก **VendTrans** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTrans</span><span class="sxs-lookup"><span data-stu-id="a4e13-396">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
6. <span data-ttu-id="a4e13-397">เพิ่มแหล่งข้อมูลของชนิด **ฟิลด์ที่คำนวณได้** เป็นฟิลด์ซ้อนกันของแหล่งข้อมูล **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="a4e13-397">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
7. <span data-ttu-id="a4e13-398">ตั้งชื่อแหล่งข้อมูล **FilteredTrans** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-398">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
8. <span data-ttu-id="a4e13-399">เพิ่มแหล่งข้อมูลของชนิด **Join**</span><span class="sxs-lookup"><span data-stu-id="a4e13-399">Add a data source of the **Join** type.</span></span>
9. <span data-ttu-id="a4e13-400">ตั้งชื่อแหล่งข้อมูลใหม่ **JoinedList** และตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a4e13-400">Name the new data source **JoinedList**, and configure it in the following way:</span></span>

    1. <span data-ttu-id="a4e13-401">เพิ่มแหล่งข้อมูล **ผู้จัดจำหน่าย** เป็นชุดของเรกคอร์ดแรกที่จะรวม</span><span class="sxs-lookup"><span data-stu-id="a4e13-401">Add the **Vendor** data source as the first set of records to join.</span></span>
    2. <span data-ttu-id="a4e13-402">เพิ่มแหล่งข้อมูล **Vendor.FilteredTrans** เป็นชุดของเรกคอร์ดที่สองที่จะรวม</span><span class="sxs-lookup"><span data-stu-id="a4e13-402">Add the **Vendor.FilteredTrans** data source as the second set of records to join.</span></span> <span data-ttu-id="a4e13-403">เลือก **ภายใน** เป็นชนิด</span><span class="sxs-lookup"><span data-stu-id="a4e13-403">Select **INNER** as the type.</span></span>
    3. <span data-ttu-id="a4e13-404">ในฟิลด์ **ดำเนินการ** ให้เลือก **การสอบถาม** เพื่อระบุว่าคุณต้องการรันแหล่งข้อมูลนี้ในระดับฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-404">In the **Execute** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![ตั้งค่าคอนฟิกแหล่งข้อมูลในหน้าตัวออกแบบ Join](./media/er-components-inspections-06a.gif)

10. <span data-ttu-id="a4e13-406">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** และตรวจสอบว่าแหล่งข้อมูล **JoinedList** ที่ตั้งค่าคอนฟิกสามารถสอบถามได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-406">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>
11. <span data-ttu-id="a4e13-407">เปลี่ยนนิพจน์ของแหล่งข้อมูล **Vendor.FilteredTrans** จาก `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` เป็น `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-407">Change the expression of the **Vendor.FilteredTrans** data source from `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` to `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
12. <span data-ttu-id="a4e13-408">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** และตรวจสอบว่าแหล่งข้อมูล **JoinedList** ที่ตั้งค่าคอนฟิกสามารถสอบถามได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-408">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>

    ![ตรวจสอบความถูกต้องของส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้ และการตรวจสอบว่าสามารถสอบถามแหล่งข้อมูล JoinedList ได้บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-06b.png)

13. <span data-ttu-id="a4e13-410">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง เนื่องจากนิพจน์ของแหล่งข้อมูล **Vendor.FilteredTrans** ไม่สามารถแปลเป็นการเรียก SQL โดยตรงได้</span><span class="sxs-lookup"><span data-stu-id="a4e13-410">Notice that a validation error occurs, because the expression of the **Vendor.FilteredTrans** data source can't be translated to the direct SQL call.</span></span> <span data-ttu-id="a4e13-411">นอกจากนี้ การเรียก SQL โดยตรงไม่อนุญาตการเรียกสำหรับแหล่งข้อมูล **JoinedList** ที่จะแปลเป็นคำสั่ง SQL โดยตรง</span><span class="sxs-lookup"><span data-stu-id="a4e13-411">Additionally, the direct SQL call doesn't allow the call for the **JoinedList** data source to be translated to the direct SQL statement.</span></span>

    ![ข้อผิดพลาดรันไทม์จากการตรวจสอบความถูกต้องของแหล่งข้อมูล JoinedList บนหน้าตัวออกแบบการแม็ปแบบจำลองล้มเหลว](./media/er-components-inspections-06c.png)

<span data-ttu-id="a4e13-413">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้นถ้าคุณละเว้นคำเตือนและเลือก **รัน** เพื่อรันรูปแบบที่มีการตั้งค่าคอนฟิกให้ใช้การแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-413">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![รันรูปแบบที่แก้ไขได้บนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-415">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-415">Automatic resolution</span></span>

<span data-ttu-id="a4e13-416">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-416">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-417">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-417">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a4e13-418">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="a4e13-418">Option 1</span></span>

<span data-ttu-id="a4e13-419">เปลี่ยนนิพจน์ของแหล่งข้อมูล **Vendor.FilteredTrans** จาก `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` กลับเป็น `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` ตามคำเตือนที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="a4e13-419">Change the expression of the **Vendor.FilteredTrans** data source from `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` back to `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, as the warning advised.</span></span>

![นพจน์ที่อัปเดตของแหล่งข้อมูลในหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a><span data-ttu-id="a4e13-421">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="a4e13-421">Option 2</span></span>

<span data-ttu-id="a4e13-422">เปลี่ยนค่าของฟิลด์ **ดำเนินการ** สำหรับแหล่งข้อมูล **JoinedList** จาก **การสอบถาม** เป็น **ในหน่วยความจำ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-422">Change the value of the **Execute** field for the **JoinedList** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="a4e13-423">เราไม่แนะนำให้คุณเปลี่ยนค่าสำหรับตารางที่มีจำนวนมากของข้อมูล (ตารางธุรกรรม) เนื่องจากเรกคอร์ดทั้งหมดจะถูกนำมาใช้ และการรวมจะเกิดขึ้นในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="a4e13-423">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and the join occurs in memory.</span></span> <span data-ttu-id="a4e13-424">วิธีการนี้อาจทำให้ประสิทธิภาพการทำงานดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-424">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="a4e13-425">คำเตือนการตรวจสอบความถูกต้องจะแสดงขึ้นเพื่อแจ้งให้คุณทราบเกี่ยวกับความเสี่ยงนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-425">A validation warning is shown to inform you about this risk.</span></span>

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a><span data-ttu-id="a4e13-426">ความเป็นที่ต้องการมากกว่าของฟังก์ชัน FILTER เทียบกับฟังก์ชัน WHERE</span><span class="sxs-lookup"><span data-stu-id="a4e13-426">Preferability of FILTER vs WHERE function</span></span>

<span data-ttu-id="a4e13-427">ฟังก์ชัน ER [FILTER](er-functions-list-filter.md) ที่มีอยู่แล้วภายในใช้เพื่อเข้าถึงตารางของโปรแกรมประยุกต์ มุมมอง หรือเอนทิตีข้อมูลโดยการวางการเรียก SQL เดียวเพื่อให้ได้ข้อมูลที่จำเป็นในฐานะรายการของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="a4e13-427">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="a4e13-428">ฟังก์ชัน [WHERE](er-functions-list-where.md) ค้นหาเรกคอร์ดทั้งหมดจากต้นทางที่กำหนดและบันทึกการเลือกในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="a4e13-428">The [WHERE](er-functions-list-where.md) function fetches all records from the given source and does record selection in memory.</span></span> <span data-ttu-id="a4e13-429">แหล่งข้อมูลของชนิด **รายการเรกคอร์ด** ถูกใช้เป็นอาร์กิวเมนต์ของทั้งสองฟังก์ชันและระบุแหล่งที่มาสำหรับการรับเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="a4e13-429">A data source of the **Record list** type is used as an argument of both functions and specifies a source for getting records.</span></span> <span data-ttu-id="a4e13-430">ER ตรวจสอบว่าสามารถสร้างการเรียกใช้ SQL โดยตรงกับแหล่งข้อมูลที่อ้างถึงในฟังก์ชัน **WHERE** หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-430">ER checks whether a direct SQL call can be established to a data source that is referred to in the **WHERE** function.</span></span> <span data-ttu-id="a4e13-431">ถ้าไม่สามารถสร้างการเรียกใช้โดยตรงได้ เกิดคำเตือนในการตรวจสอบความถูกต้องในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-431">If a direct call can be established, a validation warning occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a4e13-432">ข้อความที่คุณได้รับแนะนำให้คุณใช้ฟังก์ชัน **FILTER** แทนที่จะใช้ฟังก์ชัน **WHERE** ที่จะช่วยปรับปรุงประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a4e13-432">The message that you receive recommends that you use the **FILTER** function instead of the **WHERE** function to help improve efficiency.</span></span>

<span data-ttu-id="a4e13-433">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-433">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-434">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-434">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a4e13-435">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-435">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a4e13-436">ตั้งชื่อแหล่งข้อมูลใหม่ **Trans** ในฟิลด์ **ตาราง** ให้เลือก **VendTrans** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTrans</span><span class="sxs-lookup"><span data-stu-id="a4e13-436">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="a4e13-437">เพิ่มแหล่งข้อมูลของชนิด **ฟิลด์ที่คำนวณได้** เป็นฟิลด์ซ้อนกันของแหล่งข้อมูล **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="a4e13-437">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
5. <span data-ttu-id="a4e13-438">ตั้งชื่อแหล่งข้อมูล **FilteredTrans** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `WHERE(Trans, Trans.AccountNum="US-101")`</span><span class="sxs-lookup"><span data-stu-id="a4e13-438">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `WHERE(Trans, Trans.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="a4e13-439">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-439">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="a4e13-440">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-440">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a4e13-441">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="a4e13-441">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="a4e13-442">เพิ่มแหล่งข้อมูลของชนิด **ฟิลด์ที่มีการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-442">Add a data source of the **Calculated field** type.</span></span>
9. <span data-ttu-id="a4e13-443">ตั้งชื่อแหล่งข้อมูล **FilteredVendor** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `WHERE(Vendor, Vendor.AccountNum="US-101")`</span><span class="sxs-lookup"><span data-stu-id="a4e13-443">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span>
10. <span data-ttu-id="a4e13-444">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-444">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![ตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-07a.png)

11. <span data-ttu-id="a4e13-446">โปรดสังเกตว่าคำเตือนการตรวจสอบความถูกต้องขอแนะนำให้คุณใช้ฟังก์ชัน **FILTER** แทนที่จะใช้ฟังก์ชัน **WHERE** สำหรับแหล่งข้อมูล **FilteredVendor** และ **FilteredTrans**</span><span class="sxs-lookup"><span data-stu-id="a4e13-446">Notice that validation warnings recommend that you use the **FILTER** function instead of the **WHERE** function for the **FilteredVendor** and **FilteredTrans** data sources.</span></span>

    ![คำแนะนำให้ใช้ฟังก์ชัน FILTER แทนที่จะใช้ฟังก์ชัน WHERE บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-448">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-448">Automatic resolution</span></span>

<span data-ttu-id="a4e13-449">เลือก **แก้ไข** เพื่อแทนที่ฟังก์ชัน **WHERE** โดยอัตโนมัติโดยฟังก์ชัน **FILTER** ในนิพจน์ของแหล่งข้อมูลทั้งหมดที่จะปรากฏในกริดบนแท็บ **คำเตือน** สำหรับชนิดของการตรวจสอบนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-449">Select **Fix** to automatically replace the **WHERE** function with the **FILTER** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="a4e13-450">อีกทางหนึ่งคือ คุณสามารถเลือกแถวสำหรับคำเตือนเดียวในกริดแล้วเลือก **แก้ไขที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="a4e13-450">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="a4e13-451">ในกรณีนี้ นิพจน์จะถูกเปลี่ยนโดยอัตโนมัติในแหล่งข้อมูลที่ระบุไว้ในคำเตือนที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-451">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![การเลือก Fix เพื่อแทนที่ฟังก์ชัน WHERE ด้วยฟังก์ชัน FILTER บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-453">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-453">Manual resolution</span></span>

<span data-ttu-id="a4e13-454">คุณสามารถปรับนิพจน์ของแหล่งข้อมูลทั้งหมดในกริดการตรวจสอบความถูกต้องด้วยตนเองได้ โดยแทนฟังก์ชัน **WHERE** ด้วยฟังก์ชัน **FILTER**</span><span class="sxs-lookup"><span data-stu-id="a4e13-454">You can manually adjust the expressions of all the data sources in the validation grid by replacing the **WHERE** function with the **FILTER** function.</span></span>

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a><span data-ttu-id="a4e13-455">ความเป็นที่ต้องการมากกว่าของฟังก์ชัน ALLITEMSQUERY เทียบกับฟังก์ชัน ALLITEMS</span><span class="sxs-lookup"><span data-stu-id="a4e13-455">Preferability of ALLITEMSQUERY vs ALLITEMS function</span></span>

<span data-ttu-id="a4e13-456">ฟังก์ชัน ER [ALLITEMS](er-functions-list-allitems.md) และ [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ส่งคืนค่า **รายการเรกคอร์ด** ที่ทำให้แบนใหม่ที่ประกอบด้วยรายการของเรกคอร์ดที่แสดงถึงรายการทั้งหมดที่ตรงกับพาธที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a4e13-456">The built-in [ALLITEMS](er-functions-list-allitems.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ER functions return a flattened **Record list** value that consists of a list of records that represent all items that match the specified path.</span></span> <span data-ttu-id="a4e13-457">ER ตรวจสอบว่าสามารถสร้างการเรียกใช้ SQL โดยตรงกับแหล่งข้อมูลที่อ้างถึงในฟังก์ชัน **ALLITEMS** หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-457">ER checks whether a direct SQL call can be established to a data source that is referred to in the **ALLITEMS** function.</span></span> <span data-ttu-id="a4e13-458">ถ้าไม่สามารถสร้างการเรียกใช้โดยตรงได้ เกิดคำเตือนในการตรวจสอบความถูกต้องในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-458">If a direct call can be established, a validation warning occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a4e13-459">ข้อความที่คุณได้รับแนะนำให้คุณใช้ฟังก์ชัน **ALLITEMSQUERYR** แทนที่จะใช้ฟังก์ชัน **ALLITEMS** ที่จะช่วยปรับปรุงประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a4e13-459">The message that you receive recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function to help improve efficiency.</span></span>

<span data-ttu-id="a4e13-460">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-460">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-461">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-461">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a4e13-462">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-462">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a4e13-463">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-463">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a4e13-464">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="a4e13-464">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="a4e13-465">เพิ่มแหล่งข้อมูลแบบพารามิเตอร์ชนิด **ฟิลด์ที่มีการคำนวณ** เพิ่มรับเรกคอร์ดจากผู้จัดจำหน่ายหลายราย:</span><span class="sxs-lookup"><span data-stu-id="a4e13-465">Add a data source of the **Calculated field** type to get records for several vendors.</span></span>
5. <span data-ttu-id="a4e13-466">ตั้งชื่อแหล่งข้อมูล **FilteredVendor** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`</span><span class="sxs-lookup"><span data-stu-id="a4e13-466">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.</span></span>
6. <span data-ttu-id="a4e13-467">เพิ่มแหล่งข้อมูลชองชนิด **ฟิลด์ที่มีการคำนวณ** เพิ่มรับธุรกรรมของผู้จัดจำหน่ายที่กรองแล้วทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a4e13-467">Add a data source of the **Calculated field** type to get the transactions of all filtered vendors.</span></span>
7. <span data-ttu-id="a4e13-468">ตั้งชื่อแหล่งข้อมูล **FilteredVendorTrans** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`</span><span class="sxs-lookup"><span data-stu-id="a4e13-468">Name the new data source **FilteredVendorTrans**, and configure it so that it contains the expression `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.</span></span>
8. <span data-ttu-id="a4e13-469">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-469">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![การตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-08a.png)

9. <span data-ttu-id="a4e13-471">โปรดสังเกตว่าเกิดคำเตือนในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-471">Notice that a validation warning occurs.</span></span> <span data-ttu-id="a4e13-472">ข้อความแนะนำว่าคุณควรใช้ฟังก์ชัน **ALLITEMSQUERY** แทนที่จะใช้ฟังก์ชัน **ALLITEMS** สำหรับแหล่งข้อมูล **FilteredVendorTrans**</span><span class="sxs-lookup"><span data-stu-id="a4e13-472">The message recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function for the **FilteredVendorTrans** data source.</span></span>

    ![คำแนะนำให้ใช้ฟังก์ชัน ALLITEMSQUERY แทนที่จะใช้ฟังก์ชัน ALLITEMS บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-474">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-474">Automatic resolution</span></span>

<span data-ttu-id="a4e13-475">เลือก **แก้ไข** เพื่อแทนที่ฟังก์ชัน **ALLITEMS** โดยอัตโนมัติโดยฟังก์ชัน **ALLITEMSQUERY** ในนิพจน์ของแหล่งข้อมูลทั้งหมดที่จะปรากฏในกริดบนแท็บ **คำเตือน** สำหรับชนิดของการตรวจสอบนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-475">Select **Fix** to automatically replace the **ALLITEMS** function with the **ALLITEMSQUERY** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="a4e13-476">อีกทางหนึ่งคือ คุณสามารถเลือกแถวสำหรับคำเตือนเดียวในกริดแล้วเลือก **แก้ไขที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="a4e13-476">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="a4e13-477">ในกรณีนี้ นิพจน์จะถูกเปลี่ยนโดยอัตโนมัติในแหล่งข้อมูลที่ระบุไว้ในคำเตือนที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-477">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![การเลือก Fix ที่เลือกไว้ยนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-479">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-479">Manual resolution</span></span>

<span data-ttu-id="a4e13-480">คุณสามารถปรับนิพจน์ของแหล่งข้อมูลทั้งหมดที่กล่าวถึงในกริดการตรวจสอบความถูกต้องด้วยตนเองได้โดยแทนฟังก์ชัน **ALLITEMS** ด้วยฟังก์ชัน **ALLITEMSQUERY**</span><span class="sxs-lookup"><span data-stu-id="a4e13-480">You can manually adjust the expressions of all the data sources that are mentioned in the validation grid by replacing the **ALLITEMS** function with the **ALLITEMSQUERY** function.</span></span>

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a><span data-ttu-id="a4e13-481">การพิจารณากรณีของรายการที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="a4e13-481">Consideration of empty list cases</span></span>

<span data-ttu-id="a4e13-482">คุณสามารถตั้งค่าคอนฟิกรูปแบบ ER หรือส่วนประกอบการแม็ปรูปแบบเพื่อให้ได้ค่าฟิลด์ของแหล่งข้อมูลของชนิด **รายการเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="a4e13-482">You can configure your ER format or model mapping component to get the field value of a data source of the **Record list** type.</span></span> <span data-ttu-id="a4e13-483">ตรวจสอบว่าการออกแบบของคุณพิจารณากรณีที่มีแหล่งข้อมูลที่เรียกว่าไม่มีเรกคอร์ด (นั่นคือ ฟิลด์นี้ว่างเปล่า) เพื่อป้องกันไม่ให้เกิดข้อผิดพลาดรันไทม์เมื่อมีการนำค่ามาใช้จากฟิลด์ของเรกคอร์ดที่ไม่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a4e13-483">ER checks whether your design considers the case where a data source that is called contains no records (that is, it's empty), to prevent runtime errors when a value is fetched from a field of a nonexistent record.</span></span>

<span data-ttu-id="a4e13-484">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-484">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-485">เริ่มต้นการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER การแม็ปแบบจำลอง ER และส่วนประกอบรูปแบบ ER พร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-485">Start to configure the ER data model, the ER model mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="a4e13-486">ในแผนภูมิรูปแบบข้อมูล ให้เพิ่มรายการรากที่ชื่อ **Root3**</span><span class="sxs-lookup"><span data-stu-id="a4e13-486">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="a4e13-487">ปรับเปลี่ยนรายการ **Root3** โดยการเพิ่มรายการที่ซ้อนกันของชนิด **รายการเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="a4e13-487">Modify the **Root3** item by adding a nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="a4e13-488">ตั้งชื่อ **ผู้จัดจำหน่าย** รายการที่ซ้อนกันใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-488">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="a4e13-489">ปรับเปลี่ยนสินค้า **ผู้จัดจำหน่าย** ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a4e13-489">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="a4e13-490">เพิ่มฟิลด์ที่ซ้อนกันของชนิด **สตริง** และตั้งชื่อเป็น **Name**</span><span class="sxs-lookup"><span data-stu-id="a4e13-490">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="a4e13-491">เพิ่มฟิลด์ที่ซ้อนกันของชนิด **สตริง** และ **AccountNumber** นั้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-491">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![กำลังเพิ่มฟิลด์ที่ซ้อนกันบนหน้ารูปแบบข้อมูล](./media/er-components-inspections-09a.png)

6. <span data-ttu-id="a4e13-493">ในตัวออกแบบการแม็ปแบบจำลอง ในบานหน้าต่าง **แหล่งข้อมูล** ให้เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ ตารางบันทึก**</span><span class="sxs-lookup"><span data-stu-id="a4e13-493">In the model mapping designer, in the **Data sources** pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="a4e13-494">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-494">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a4e13-495">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="a4e13-495">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="a4e13-496">เพิ่มแหล่งข้อมูลของชนิด **ทั่วไป \\ พารามิเตอร์ป้อนเข้าของผู้ใช้** ในการค้นหาบัญชีผู้จัดจำหน่ายในกล่องโต้ตอบรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-496">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
9. <span data-ttu-id="a4e13-497">ตั้งชื่อแหล่งข้อมูล **RequestedAccountNum** ใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-497">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="a4e13-498">ในฟิลด์ **ป้ายชื่อ** ให้ป้อน **หมายเลขบัญชีของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="a4e13-498">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="a4e13-499">ในฟิลด์ **ชื่อชนิดของข้อมูลการดำเนินงาน** ให้เว้นค่าเริ่มต้น **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="a4e13-499">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="a4e13-500">เพิ่มแหล่งข้อมูลแบบพารามิเตอร์ชนิด **ฟิลด์ที่มีการคำนวณ** เพิ่มกรองผู้จัดจำหน่ายที่จำเป็น:</span><span class="sxs-lookup"><span data-stu-id="a4e13-500">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="a4e13-501">ตั้งชื่อแหล่งข้อมูล **FilteredVendor** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-501">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="a4e13-502">ผูกรายการแบบจำลองข้อมูลเพื่อตั้งค่าคอนฟิกแหล่งข้อมูลในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a4e13-502">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="a4e13-503">ผูก **FilteredVendor** กับ **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="a4e13-503">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="a4e13-504">ผูก **FilteredVendor.AccountNum** กับ **Vendor.AccountNumber**</span><span class="sxs-lookup"><span data-stu-id="a4e13-504">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>
    - <span data-ttu-id="a4e13-505">ผูก **FilteredVendor.'name()'** กับ **Vendor.Name**</span><span class="sxs-lookup"><span data-stu-id="a4e13-505">Bind **FilteredVendor.'name()'** to **Vendor.Name**.</span></span>

    ![ผูกรายการแบบจำลองข้อมูลในหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-09b.png)

13. <span data-ttu-id="a4e13-507">ในแผนภูมิรูปแบบโครงสร้าง เพิ่มรายการต่อไปนี้เพื่อสร้างเอกสารขาออกในรูปแบบ XML ที่มีรายละเอียดผู้จัดจำหน่าย:</span><span class="sxs-lookup"><span data-stu-id="a4e13-507">In the format structure tree, add the following items to generate an outbound document in XML format that contains the vendor details:</span></span>

    1. <span data-ttu-id="a4e13-508">เพิ่มองค์ประกอบ XML ของราก **ใบแจ้งยอด**</span><span class="sxs-lookup"><span data-stu-id="a4e13-508">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="a4e13-509">สำหรับองค์ประกอบ XML **ใบแจ้งยอด** เพิ่มองค์ประกอบ XML **ฝ่าย** ที่ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-509">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="a4e13-510">สำหรับองค์ประกอบ XML **ฝ่าย** เพิ่มแอททริบิวต์ XML ที่ซ้อนกันต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-510">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="a4e13-511">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="a4e13-511">Name</span></span>
        - <span data-ttu-id="a4e13-512">AccountNum</span><span class="sxs-lookup"><span data-stu-id="a4e13-512">AccountNum</span></span>

14. <span data-ttu-id="a4e13-513">ผูกองค์ประกอบรูปแบบไปยังแหล่งข้อมูลที่ให้ไว้ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a4e13-513">Bind format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="a4e13-514">ผูกองค์ประกอบรูปแบบ **คำสั่ง\\ฝ่าย\\ชื่อ** เข้ากับกับฟิลด์แหล่งข้อมูล **แบบจำลอง.ผู้จัดจำหน่าย.ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-514">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="a4e13-515">ผูกองค์ประกอบรูปแบบ **คำสั่ง\\ฝ่าย\\AccountNum** เข้ากับกับฟิลด์แหล่งข้อมูล **แบบจำลอง.ผู้จัดจำหน่าย.หมายเลขบัญชี'**</span><span class="sxs-lookup"><span data-stu-id="a4e13-515">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="a4e13-516">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของรูปแบบที่แก้ไขได้บนหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-516">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![ตรวจสอบความถูกต้องขององค์ประกอบรูปแบบที่คุณผูกกับแหล่งข้อมูลบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-09c.png)

16. <span data-ttu-id="a4e13-518">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-518">Notice that a validation error occurs.</span></span> <span data-ttu-id="a4e13-519">ข้อความระบุว่าอาจเกิดข้อผิดพลาดสำหรับส่วนประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย\\ชื่อ** และ **ใบแจ้งยอด\\ฝ่าย\\หมายเลขบัญชี** ในขณะรันไทม์ถ้ารายการ `model.Vendor` ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="a4e13-519">The message states that an error might be thrown for the configured **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format components at runtime if the `model.Vendor` list is empty.</span></span>

    ![ข้อผิดพลาดการตรวจสอบความถูกต้องเกี่ยวกับข้อผิดพลาดที่อาจเกิดขึ้นสำหรับส่วนประกอบรูปแบบที่กำหนดไว้](./media/er-components-inspections-09d.png)

<span data-ttu-id="a4e13-521">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้นถ้าคุณละเว้นคำเตือน เลือก **รัน** เพื่อรันรูปแบบ และเลือกหมายเลขบัญชีของผู้จัดจำหน่ายที่ไม่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a4e13-521">The following illustration shows the runtime error that occurs if you ignore the warning, select **Run** to run the format, and select the account number of a nonexistent vendor.</span></span> <span data-ttu-id="a4e13-522">เนื่องจากไม่มีผู้จัดจำหน่ายที่ร้องขออยู่ รายการ `model.Vendor` จะว่างเปล่า (นั่นคือ จะไม่มีเรกคอร์ด)</span><span class="sxs-lookup"><span data-stu-id="a4e13-522">Because the requested vendor doesn't exist, the `model.Vendor` list will be empty (that is, it will contain no records).</span></span>

![ข้อผิดพลาดรันไทม์ที่เกิดขึ้นระหว่างการรันการแม็ปรูปแบบ](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-524">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-524">Automatic resolution</span></span>

<span data-ttu-id="a4e13-525">สำหรับแถวที่เลือกในกริดบนแท็บ **คำเตือน** คุณสามารถเลือก **ยกเลิกการผูก**</span><span class="sxs-lookup"><span data-stu-id="a4e13-525">For the selected row in the grid on the **Warnings** tab, you can select **Unbind**.</span></span> <span data-ttu-id="a4e13-526">การผูกที่ชี้ไปในคอลัมน์ **พาธ** จะถูกลบออกจากองค์ประกอบรูปแบบโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-526">The binding that is pointed to in the **Path** column is automatically removed from the format elements.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-527">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-527">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a4e13-528">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="a4e13-528">Option 1</span></span>

<span data-ttu-id="a4e13-529">คุณสามารถผูกองค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย\\ชื่่อ** เข้ากับกับรายการแหล่งข้อมูล `model.Vendor`</span><span class="sxs-lookup"><span data-stu-id="a4e13-529">You can bind the **Statement\\Party\\Name** format element to the `model.Vendor` data source item.</span></span> <span data-ttu-id="a4e13-530">เมื่อรันไทม์ การผูกข้อมูลนี้เรียกแหล่งข้อมูล `model.Vendor` เป็นอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="a4e13-530">At runtime, this binding calls the `model.Vendor` data source first.</span></span> <span data-ttu-id="a4e13-531">เมื่อ `model.Vendor` ส่งคืนรายการเรกคอร์ดที่ว่างเปล่า จะไม่มีการรันองค์ประกอบรูปแบบซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-531">When `model.Vendor` returns an empty record list, the nested format elements aren't run.</span></span> <span data-ttu-id="a4e13-532">ดังนั้น จึงไม่มีคำเตือนการตรวจสอบความถูกต้องสำหรับการตั้งค่าคอนฟิกรูปแบบนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-532">Therefore, no validation warnings occur for this format configuration.</span></span>

![การผูกองค์ประกอบรูปแบบกับรายการแหล่งข้อมูลบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a><span data-ttu-id="a4e13-534">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="a4e13-534">Option 2</span></span>

<span data-ttu-id="a4e13-535">เปลี่ยนการผูกขององค์ประกอบรูปแบบ **คำสั่ง\\ฝ่าย\\ชื่อ** จาก `model.Vendor.Name` เป็น `FIRSTORNULL(model.Vendor).Name`</span><span class="sxs-lookup"><span data-stu-id="a4e13-535">Change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `FIRSTORNULL(model.Vendor).Name`.</span></span> <span data-ttu-id="a4e13-536">เงื่อนไขการรวมที่มีการอัปเดตจะแปลงเรกคอร์ดแรกของแหล่งข้อมูล `model.Vendor` ของชนิด **รายการเรกคอร์ด** ไปยังแหล่งข้อมูลใหม่ของชนิด **เรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="a4e13-536">The updated binding conditionally converts the first record of the `model.Vendor` data source of the **Record list** type to a new data source of the **Record** type.</span></span> <span data-ttu-id="a4e13-537">แหล่งข้อมูลใหม่นี้ประกอบด้วยชุดของฟิลด์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-537">This new data source contains the same set of fields.</span></span>

- <span data-ttu-id="a4e13-538">ถ้ามีเรกคอร์ดอย่างน้อยหนึ่งเรกคอร์ดในแหล่งข้อมูล `model.Vendor` ฟิลด์ของเรกคอร์ดดังกล่าวจะถูกเติมด้วยค่าของฟิลด์ของเรกคอร์ดแรกของแหล่งข้อมูล `model.Vendor`</span><span class="sxs-lookup"><span data-stu-id="a4e13-538">If at least one record is available in the `model.Vendor` data source, the fields of that record are filled with the values of the fields of the first record of the `model.Vendor` data source.</span></span> <span data-ttu-id="a4e13-539">ในกรณีนี้ การผูกข้อมูลที่อัปเดตแล้วส่งคืนชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a4e13-539">In this case, the updated binding returns the vendor name.</span></span>
- <span data-ttu-id="a4e13-540">มิฉะนั้น ฟิลด์ทั้งหมดของเรกคอร์ดที่สร้างขึ้นจะถูกเติมด้วยค่าเริ่มต้นสำหรับชนิดข้อมูลของฟิลด์นั้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-540">Otherwise, every field of the record that is created is filled with the default value for the data type of that field.</span></span> <span data-ttu-id="a4e13-541">ในกรณีนี้ มีการส่งคืนสตริงที่ว่างเปล่าเป็นค่าเริ่มต้นของชนิดข้อมูล **สตริง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-541">In this case, the blank string is returned as the default value of the **String** data type.</span></span>

<span data-ttu-id="a4e13-542">ดังนั้น จึงไม่มีคำเตือนการตรวจสอบความถูกต้องสำหรับองค์ประกอบรูปแบบ **คำสั่ง\\ฝ่าย\\ชื่อ** เมื่อผูกกับนิพจน์ `FIRSTORNULL(model.Vendor).Name`</span><span class="sxs-lookup"><span data-stu-id="a4e13-542">Therefore, no validation warnings occur for the **Statement\\Party\\Name** format element when it's bound to the `FIRSTORNULL(model.Vendor).Name` expression.</span></span>

![การผูกที่เปลี่ยนแปลงแก้ไขคำเตือนการตรวจสอบความถูกต้องบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a><span data-ttu-id="a4e13-544">ตัวเลือก 3</span><span class="sxs-lookup"><span data-stu-id="a4e13-544">Option 3</span></span>

<span data-ttu-id="a4e13-545">ถ้าคุณต้องการระบุข้อมูลที่ป้อนในเอกสารที่สร้างขึ้นอย่างชัดแจ้งเมื่อแหล่งข้อมูล `model.Vendor` ของชนิด **รายการเรกคอร์ด** ส่งคืนไม่มีเรกคอร์ด (ข้อความที่ **ไม่มีอยู่** ในตัวอย่างนี้) ให้เปลี่ยนการผูกขององค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย\\ชื่อ** จาก `model.Vendor.Name` เป็น `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`</span><span class="sxs-lookup"><span data-stu-id="a4e13-545">If you want to explicitly specify the data that is entered in a generated document when the `model.Vendor` data source of the **Record list** type returns no records (the text **Not available** in this example), change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`.</span></span> <span data-ttu-id="a4e13-546">และคุณสามารถใช้นิพจน์ `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`</span><span class="sxs-lookup"><span data-stu-id="a4e13-546">You can also use the expression `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.</span></span>

### <a name="additional-consideration"></a><a id="i9a"></a><span data-ttu-id="a4e13-547">การพิจารณาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a4e13-547">Additional consideration</span></span>

<span data-ttu-id="a4e13-548">การตรวจสอบยังเตือนคุณเกี่ยวกับปัญหาที่อาจเกิดขึ้นอีกประการหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a4e13-548">The inspection also warns you about another potential issue.</span></span> <span data-ttu-id="a4e13-549">ตามค่าเริ่มต้น ในขณะที่คุณผูกองค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย\\ชื่อ** และ **ใบแจ้งยอด\\ฝ่าย\\เลขที่บัญชี** ให้กับฟิลด์ที่เหมาะสมของแหล่งข้อมูล `model.Vendor` ของชนิด **รายการเรกคอร์ด** จะมีการรันการผูกเหล่านั้นและจะใช้ค่าของฟิลด์ที่เหมาะสมของเรกคอร์ดแรกของแหล่งข้อมูล `model.Vendor` ถ้ารายการดังกล่าวไม่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="a4e13-549">By default, as you bind the **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format elements to the appropriate fields of the `model.Vendor` data source of the **Record list** type, those bindings will be run and will take the values of the appropriate fields of the first record of the `model.Vendor` data source, if that list isn't empty.</span></span>

<span data-ttu-id="a4e13-550">เนื่องจากคุณไม่ได้ผูกองค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย** กับแหล่งข้อมูล `model.Vendor` องค์ประกอบ **ใบแจ้งยอด\\ฝ่าย** จะไม่มีการวนซ้ำสำหรับเรกคอร์ดทั้งหมดของแหล่งข้อมูล `model.Vendor` ในระหว่างการดำเนินการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="a4e13-550">Because you haven't bound the **Statement\\Party** format element with the `model.Vendor` data source, the **Statement\\Party** element won't be iterated for every record of the `model.Vendor` data source during format execution.</span></span> <span data-ttu-id="a4e13-551">เอกสารที่สร้างขึ้นจะถูกเติมด้วยข้อมูลจากเรกคอร์ดหนึ่งของรายการเรกคอร์ดเท่านั้น ถ้ารายการดังกล่าวประกอบด้วยเรกคอร์ดหลายเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="a4e13-551">Instead, a generated document will be filled with information from only the first record of the record list, if that list contains multiple records.</span></span> <span data-ttu-id="a4e13-552">การทำเช่นนี้อาจเป็นปัญหาถ้ารูปแบบนี้มีไว้เพื่อให้กรอกเอกสารที่สร้างขึ้นด้วยข้อมูลเกี่ยวกับผู้จัดจำหน่ายทั้งหมดจากแหล่งข้อมูล `model.Vendor`</span><span class="sxs-lookup"><span data-stu-id="a4e13-552">Therefore, there might be an issue if the format is intended to fill a generated document with information about all vendors from the `model.Vendor` data source.</span></span> <span data-ttu-id="a4e13-553">เมื่อต้องการแก้ไขปัญหานี้ ให้ผูกองค์ประกอบ **ใบแจ้งยอด\\ฝ่าย** กับแหล่งข้อมูล `model.Vendor`</span><span class="sxs-lookup"><span data-stu-id="a4e13-553">To fix this issue, bind the **Statement\\Party** element with the `model.Vendor` data source.</span></span>

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a><span data-ttu-id="a4e13-554">ความสามารถในการปฏิบัติการนิพจน์กับฟังก์ชันตัวกรอง (การแคช)</span><span class="sxs-lookup"><span data-stu-id="a4e13-554">Executability of an expression with FILTER function (caching)</span></span>

<span data-ttu-id="a4e13-555">หลายฟังก์ชัน ER ภายใน รวมถึง [FILTER](er-functions-list-filter.md) และ [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ใช้เพื่อเข้าถึงตารางของโปรแกรมประยุกต์ มุมมอง หรือเอนทิตีข้อมูลโดยการวางการเรียก SQL เดียวเพื่อให้ได้ข้อมูลที่จำเป็นในฐานะรายการของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="a4e13-555">Several built-in ER functions, including [FILTER](er-functions-list-filter.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md), are used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="a4e13-556">แหล่งข้อมูลของชนิด **รายการเรกคอร์ด** ถูกใช้เป็นอาร์กิวเมนต์ของแต่ละฟังก์ชันเหล่านี้และระบุแหล่งที่มาของโปรแกรมประยุกต์สำหรับการโทร</span><span class="sxs-lookup"><span data-stu-id="a4e13-556">A data source of the **Record list** type is used as an argument of each of these functions and specifies an application source for the call.</span></span> <span data-ttu-id="a4e13-557">ER ตรวจสอบว่าสามารถสร้างการเรียกใช้ SQL โดยตรงกับแหล่งข้อมูลที่อ้างถึงในหนึ่งในฟังก์ชันเหล่านี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-557">ER checks whether a direct SQL call can be established to a data source that is referred to in one of these functions.</span></span> <span data-ttu-id="a4e13-558">ถ้าไม่สามารถสร้างการเรียกใช้โดยตรงได้ เนื่องจากแหล่งข้อมูลอ้างอิงถูกทำเครื่องหมายเป็น [แคช](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace) เกิดข้อผิดพลาดในการตรวจสอบความถูกต้องในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-558">If a direct call can't be established because the data source was marked as [cached](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a4e13-559">ข้อความที่คุณได้รับแจ้งว่านิพจน์ ER ที่มีหนึ่งในฟังก์ชันเหล่านี้ไม่สามารถรันในขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-559">The message that you receive states that the ER expression that contains one of these functions can't be run at runtime.</span></span>

<span data-ttu-id="a4e13-560">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-560">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-561">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-561">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a4e13-562">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-562">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a4e13-563">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-563">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a4e13-564">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="a4e13-564">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="a4e13-565">เพิ่มแหล่งข้อมูลของชนิด **ทั่วไป \\ พารามิเตอร์ป้อนเข้าของผู้ใช้** ในการค้นหาบัญชีผู้จัดจำหน่ายในกล่องโต้ตอบรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-565">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
5. <span data-ttu-id="a4e13-566">ตั้งชื่อแหล่งข้อมูล **RequestedAccountNum** ใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-566">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="a4e13-567">ในฟิลด์ **ป้ายชื่อ** ให้ป้อน **หมายเลขบัญชีของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="a4e13-567">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="a4e13-568">ในฟิลด์ **ชื่อชนิดของข้อมูลการดำเนินงาน** ให้เว้นค่าเริ่มต้น **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="a4e13-568">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
6. <span data-ttu-id="a4e13-569">เพิ่มแหล่งข้อมูลแบบพารามิเตอร์ชนิด **ฟิลด์ที่มีการคำนวณ** เพิ่มกรองผู้จัดจำหน่ายที่จำเป็น:</span><span class="sxs-lookup"><span data-stu-id="a4e13-569">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
7. <span data-ttu-id="a4e13-570">ตั้งชื่อแหล่งข้อมูล **FilteredVendor** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-570">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
8. <span data-ttu-id="a4e13-571">ทำเครื่องหมายแหล่งข้อมูล **ผู้จัดจำหน่าย** ที่ตั้งค่าคอนฟิกเป็นแคช</span><span class="sxs-lookup"><span data-stu-id="a4e13-571">Mark the configured **Vendor** data source as cached.</span></span>

    ![การกำหนดค่าส่วนประกอบของการแม็ปแบบจำลองบนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-10a.gif)

9. <span data-ttu-id="a4e13-573">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="a4e13-573">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![การตรวจสอบฟังก์ชัน FILTER ที่นำไปใช้กับแหล่งข้อมูลผู้จัดจำหน่ายที่แคชไว้บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-10a.png)

10. <span data-ttu-id="a4e13-575">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-575">Notice that a validation error occurs.</span></span> <span data-ttu-id="a4e13-576">ข้อความแจ้งว่าฟังก์ชัน **FILTER** ไม่สามารถนำไปใช้แหล่งข้อมูล **ผู้จัดจำหน่าย** ที่ถูกเก็บไว้ในแคช</span><span class="sxs-lookup"><span data-stu-id="a4e13-576">The message states that the **FILTER** function can't be applied to the cached **Vendor** data source.</span></span>

<span data-ttu-id="a4e13-577">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้นถ้าคุณละเว้นคำเตือนและเลือก **รัน** เพื่อรันรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="a4e13-577">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![ข้อผิดพลาดรันไทม์ที่เกิดขึ้นระหว่างการรันการแม็ปรูปแบบบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-579">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-579">Automatic resolution</span></span>

<span data-ttu-id="a4e13-580">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-580">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-581">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-581">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a4e13-582">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="a4e13-582">Option 1</span></span>

<span data-ttu-id="a4e13-583">ลบแฟล็ก **แคช** จากแหล่งข้อมูล **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="a4e13-583">Remove the **Cache** flag from the **Vendor** data source.</span></span> <span data-ttu-id="a4e13-584">แหล่งข้อมูล **FilteredVendor** จะกลายเป็นสามารถดำเนินการได้ แต่แหล่งข้อมูล **ผู้จัดจำหน่าย** ที่อ้างถึงในตาราง VendTable จะสามารถเข้าถึงได้ทุกครั้งที่มีการเรียกแหล่งข้อมูล **FilteredVendor**</span><span class="sxs-lookup"><span data-stu-id="a4e13-584">The **FilteredVendor** data source will then become executable, but the **Vendor** data source that is referred to in the VendTable table will be accessed every time that the **FilteredVendor** data source is called.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a4e13-585">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="a4e13-585">Option 2</span></span>

<span data-ttu-id="a4e13-586">เปลี่ยนนิพจน์ของแหล่งข้อมูล **FilteredVendor** จาก `FILTER(Vendor, Vendor.AccountNum="US-101")` เป็น `WHERE(Vendor, Vendor.AccountNum="US-101")`</span><span class="sxs-lookup"><span data-stu-id="a4e13-586">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="a4e13-587">ในกรณีนี้ แหล่งข้อมูล **ผู้จัดจำหน่าย** ที่มีการอ้างอิงในตาราง VendTable จะมีการเข้าถึงในระหว่างการเรียกแรกของแหล่งข้อมูล **ผู้จัดจำหน่าย** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-587">In this case, the **Vendor** data source that is referred to in the VendTable table will be accessed only during the first call of the **Vendor** data source.</span></span> <span data-ttu-id="a4e13-588">อย่างไรก็ตาม การเลือกเรกคอร์ดจะมีการดำเนินการในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="a4e13-588">However, the selection of records will be done in memory.</span></span> <span data-ttu-id="a4e13-589">วิธีการนี้อาจทำให้ประสิทธิภาพการทำงานดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-589">Therefore, this approach can cause poor performance.</span></span>

## <a name="missing-binding"></a><a id="i11"></a><span data-ttu-id="a4e13-590">ขาดการผูกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a4e13-590">Missing binding</span></span>

<span data-ttu-id="a4e13-591">เมื่อคุณตั้งค่าคอนฟิกส่วนประกอบรูปแบบ ER แบบจำลองข้อมูลพื้นฐาน ER จะถูกนำเสนอเป็นแหล่งข้อมูลเริ่มต้นสำหรับรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-591">When you configure an ER format component, the base ER data model is offered as a default data source for the ER format.</span></span> <span data-ttu-id="a4e13-592">เมื่อรันรูปแบบ ER ที่ตั้งค่าคอนฟิก [การแม็ปแบบจำลองเริ่มต้น](er-country-dependent-model-mapping.md) สำหรับแบบจำลองพื้นฐานจะใช้ในการกรอกรูปแบบข้อมูลด้วยข้อมูลของโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="a4e13-592">When the configured ER format is run, the [default model mapping](er-country-dependent-model-mapping.md) for the base model is used to fill the data model with application data.</span></span> <span data-ttu-id="a4e13-593">ตัวออกแบบรูปแบบ ER แสดงคำเตือนถ้าคุณผูกองค์ประกอบรูปแบบไปยังรายการรูปแบบข้อมูลที่ไม่ได้ผูกกับแหล่งข้อมูลใด ๆ ในการแม็ปแบบจำลองที่เลือกไว้เป็นการแม็ปแบบจำลองเริ่มต้นสำหรับรูปแบบที่แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="a4e13-593">The ER format designer shows a warning if you bind a format element to a data model item that isn't bound to any data source in the model mapping that is currently selected as the default model mapping for the editable format.</span></span> <span data-ttu-id="a4e13-594">ไม่สามารถรันการผูกข้อมูลชนิดนี้เมื่อรันไทม์ได้ เนื่องจากรูปแบบที่รันไม่สามารถกรอกข้อมูลองค์ประกอบที่ผูกกับข้อมูลของโปรแกรมประยุกต์ได้</span><span class="sxs-lookup"><span data-stu-id="a4e13-594">This type of binding can't be run at runtime, because the format that runs can't fill a bound element with application data.</span></span> <span data-ttu-id="a4e13-595">ข้อผิดพลาดเกิดขึ้นขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-595">Therefore, an error occurs at runtime.</span></span>

<span data-ttu-id="a4e13-596">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-596">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-597">เริ่มต้นการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER การแม็ปแบบจำลอง ER และส่วนประกอบรูปแบบ ER พร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-597">Start to configure the ER data model, the ER model mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="a4e13-598">ในแผนภูมิรูปแบบข้อมูล ให้เพิ่มรายการรากที่ชื่อ **Root3**</span><span class="sxs-lookup"><span data-stu-id="a4e13-598">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="a4e13-599">ปรับเปลี่ยนรายการ **Root3** โดยการเพิ่มรายการที่ซ้อนกันใหม่ของชนิด **รายการเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="a4e13-599">Modify the **Root3** item by adding a new nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="a4e13-600">ตั้งชื่อ **ผู้จัดจำหน่าย** รายการที่ซ้อนกันใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-600">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="a4e13-601">ปรับเปลี่ยนสินค้า **ผู้จัดจำหน่าย** ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a4e13-601">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="a4e13-602">เพิ่มฟิลด์ที่ซ้อนกันของชนิด **สตริง** และตั้งชื่อเป็น **Name**</span><span class="sxs-lookup"><span data-stu-id="a4e13-602">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="a4e13-603">เพิ่มฟิลด์ที่ซ้อนกันของชนิด **สตริง** และ **AccountNumber** นั้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-603">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![การเพิ่มฟิลด์ที่ซ้อนกันให้กับรายการของผู้จัดจำหน่ายบนหน้ารูปแบบข้อมูล](./media/er-components-inspections-11a.png)

6. <span data-ttu-id="a4e13-605">ในตัวออกแบบการแม็ปแบบจำลอง ในบานหน้าต่าง **แหล่งข้อมูล** ให้เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ ตารางบันทึก**</span><span class="sxs-lookup"><span data-stu-id="a4e13-605">In the model mapping designer, in the **Data sources** pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="a4e13-606">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-606">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a4e13-607">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="a4e13-607">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="a4e13-608">เพิ่มแหล่งข้อมูลของชนิด **ทั่วไป \\ พารามิเตอร์ป้อนเข้าของผู้ใช้** ในการสอบถามบัญชีผู้จัดจำหน่ายในกล่องโต้ตอบรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-608">Add a data source of the **General \\ User input parameter** type to inquire about a vendor account in the runtime dialog box.</span></span>
9. <span data-ttu-id="a4e13-609">ตั้งชื่อแหล่งข้อมูล **RequestedAccountNum** ใหม่</span><span class="sxs-lookup"><span data-stu-id="a4e13-609">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="a4e13-610">ในฟิลด์ **ป้ายชื่อ** ให้ป้อน **หมายเลขบัญชีของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="a4e13-610">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="a4e13-611">ในฟิลด์ **ชื่อชนิดของข้อมูลการดำเนินงาน** ให้เว้นค่าเริ่มต้น **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="a4e13-611">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="a4e13-612">เพิ่มแหล่งข้อมูลแบบพารามิเตอร์ชนิด **ฟิลด์ที่มีการคำนวณ** เพิ่มกรองผู้จัดจำหน่ายที่จำเป็น:</span><span class="sxs-lookup"><span data-stu-id="a4e13-612">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="a4e13-613">ตั้งชื่อแหล่งข้อมูล **FilteredVendor** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`</span><span class="sxs-lookup"><span data-stu-id="a4e13-613">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="a4e13-614">ผูกรายการแบบจำลองข้อมูลเพื่อตั้งค่าคอนฟิกแหล่งข้อมูลในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a4e13-614">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="a4e13-615">ผูก **FilteredVendor** กับ **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="a4e13-615">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="a4e13-616">ผูก **FilteredVendor.AccountNum** กับ **Vendor.AccountNumber**</span><span class="sxs-lookup"><span data-stu-id="a4e13-616">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4e13-617">ฟิลด์รูปแบบข้อมูล **ผู้จัดจำหน่าย.ชื่อ** ยังคงไม่ถูกผูกไว้</span><span class="sxs-lookup"><span data-stu-id="a4e13-617">The **Vendor.Name** data model field remains unbound.</span></span>

    ![รายการรูปแบบข้อมูลที่ผูกกับแหล่งข้อมูลที่ถูกกำหนดค่าคอนฟิกและรายการรูปแบบข้อมูลบนที่ยังไม่ได้ผูกไว้บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-11b.png)

13. <span data-ttu-id="a4e13-619">ในแผนภูมิรูปแบบโครงสร้าง เพิ่มรายการต่อไปนี้เพื่อสร้างเอกสารขาออกในรูปแบบ XML ที่มีรายละเอียดของผู้จัดจำหน่ายที่สอบถาม:</span><span class="sxs-lookup"><span data-stu-id="a4e13-619">In the format structure tree, add the following items to generate an outbound document in XML format that contains the details of the vendors that are inquired about:</span></span>

    1. <span data-ttu-id="a4e13-620">เพิ่มองค์ประกอบ XML ของราก **ใบแจ้งยอด**</span><span class="sxs-lookup"><span data-stu-id="a4e13-620">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="a4e13-621">สำหรับองค์ประกอบ XML **ใบแจ้งยอด** เพิ่มองค์ประกอบ XML **ฝ่าย** ที่ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-621">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="a4e13-622">สำหรับองค์ประกอบ XML **ฝ่าย** เพิ่มแอททริบิวต์ XML ที่ซ้อนกันต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-622">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="a4e13-623">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="a4e13-623">Name</span></span>
        - <span data-ttu-id="a4e13-624">AccountNum</span><span class="sxs-lookup"><span data-stu-id="a4e13-624">AccountNum</span></span>

14. <span data-ttu-id="a4e13-625">ผูกองค์ประกอบรูปแบบไปยังแหล่งข้อมูลที่ให้ไว้ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a4e13-625">Bind the format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="a4e13-626">ผูกองค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย** เข้ากับกับรายการแหล่งข้อมูล `model.Vendor`</span><span class="sxs-lookup"><span data-stu-id="a4e13-626">Bind the **Statement\\Party** format element to the `model.Vendor` data source item.</span></span>
    - <span data-ttu-id="a4e13-627">ผูกองค์ประกอบรูปแบบ **คำสั่ง\\ฝ่าย\\ชื่อ** เข้ากับกับฟิลด์แหล่งข้อมูล **แบบจำลอง.ผู้จัดจำหน่าย.ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-627">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="a4e13-628">ผูกองค์ประกอบรูปแบบ **คำสั่ง\\ฝ่าย\\AccountNum** เข้ากับกับฟิลด์แหล่งข้อมูล **แบบจำลอง.ผู้จัดจำหน่าย.หมายเลขบัญชี'**</span><span class="sxs-lookup"><span data-stu-id="a4e13-628">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="a4e13-629">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของรูปแบบที่แก้ไขได้บนหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-629">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![การตรวจสอบความถูกต้องส่วนประกอบรูปแบบ ER บนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-11c.png)

16. <span data-ttu-id="a4e13-631">โปรดสังเกตว่าเกิดคำเตือนในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-631">Notice that a validation warning occurs.</span></span> <span data-ttu-id="a4e13-632">ข้อความระบุว่าฟิลด์แหล่งข้อมูล **แบบจำลอง.ผู้จัดจำหน่าย.ชื่อ** ไม่ได้ผูกกับแหล่งข้อมูลใด ๆ ในการแม็ปแบบจำลองที่มีการตั้งค่าคอนฟิกให้ใช้โดยรูปแบบนี้</span><span class="sxs-lookup"><span data-stu-id="a4e13-632">The message states that the **model.Vendor.Name** data source field isn't bound to any data source in the model mapping that is configured to be used by the format.</span></span> <span data-ttu-id="a4e13-633">ดังนั้น องค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย\\ชื่อ** อาจไม่ได้รับการกรอกข้อมูลในขณะรันไทม์ และข้อยกเว้นรันไทม์อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-633">Therefore, the **Statement\\Party\\Name** format element might not be filled at runtime, and a runtime exception might occur.</span></span>

    ![การตรวจสอบความถูกต้องส่วนประกอบรูปแบบ ER บนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-11d.png)

<span data-ttu-id="a4e13-635">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้นถ้าคุณละเว้นคำเตือนและเลือก **รัน** เพื่อรันรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="a4e13-635">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![การรันรูปแบบที่แก้ไขได้บนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-637">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-637">Automatic resolution</span></span>

<span data-ttu-id="a4e13-638">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-638">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-639">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-639">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a4e13-640">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="a4e13-640">Option 1</span></span>

<span data-ttu-id="a4e13-641">ปรับเปลี่ยนการแม็ปแบบจำลองที่ตั้งค่าคอนฟิกโดยเพิ่มการรวมสำหรับฟิลด์แหล่งข้อมูล **แบบจำลอง.ผู้จัดจำหน่าย.ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-641">Modify the configured model mapping by adding a binding for the **model.Vendor.Name** data source field.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a4e13-642">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="a4e13-642">Option 2</span></span>

<span data-ttu-id="a4e13-643">ปรับเปลี่ยนรูปแบบที่กำหนดค่าคอนฟิกด้วยการลบการผูกสำหรับองค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย\\ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-643">Modify the configured format by removing the binding for the **Statement\\Party\\Name** format element.</span></span>

## <a name="not-linked-template"></a><a id="i12"></a><span data-ttu-id="a4e13-644">แม่แบบไม่มีการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="a4e13-644">Not linked template</span></span>

<span data-ttu-id="a4e13-645">เมื่อคุณตั้งค่าคอนฟิกส่วนประกอบของรูปแบบ ER [ด้วยตนเอง](er-fillable-excel.md#manual-entry) เพื่อใช้แม่แบบเพื่อสร้างเอกสารขาออก คุณต้องเพิ่มองค์ประกอบ **Excel\\ไฟล์** ด้วยตนเอง เพิ่มแม่แบบที่จำเป็นต้องใช้เป็นสิ่งที่แนบมากับส่วนประกอบที่แก้ไขได้ และเลือกสิ่งที่แนบไว้ในองค์ประกอบ **Excel\\ไฟล์** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a4e13-645">When you [manually](er-fillable-excel.md#manual-entry) configure an ER format component to use a template to generate an outbound document, you must manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="a4e13-646">ด้วยวิธีนี้ คุณบ่งชี้ว่าองค์ประกอบเพิ่มเติมจะเติมแม่แบบที่เลือกเมื่อรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-646">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="a4e13-647">เมื่อคุณกำหนดค่าคอนฟิกรุ่นของส่วนประกอบรูปแบบใน **แบบร่าง** [สถานะ](general-electronic-reporting.md#component-versioning) คุณอาจเพิ่มหลายแม่แบบไปยังส่วนประกอบที่แก้ไขได้แล้วเลือกแต่ละแม่แบบในองค์ประกอบ **Excel\\ไฟล์** เพื่อรันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-647">When you configure a format component version in **Draft** [status](general-electronic-reporting.md#component-versioning), you might add several templates to the editable component and then select each template in the **Excel\\File** element to run the ER format.</span></span> <span data-ttu-id="a4e13-648">ด้วยวิธีนี้ คุณสามารถดูวิธีการกรอกข้อมูลแม่แบบที่แตกต่างกันในขณะทำงาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-648">In this way, you can see how different templates are filled at runtime.</span></span> <span data-ttu-id="a4e13-649">ถ้าคุณมีแม่แบบที่ไม่ได้เลือกไว้ในองค์ประกอบ **Excel\\ไฟล์** ใด ๆ ตัวออกแบบรูปแบบ ER จะแจ้งเตือนคุณว่าแม่แบบจะถูกลบออกจากรุ่นของส่วนประกอบรูปแบบ ER ที่สามารถแก้ไขได้เมื่อสถานะมีการเปลี่ยนแปลงจาก **แบบร่าง** เป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="a4e13-649">If you have templates that aren't selected in any **Excel\\File** elements, the ER format designer warns you that those templates will be deleted from the editable ER format component version when its status is changed from **Draft** to **Completed**.</span></span>

<span data-ttu-id="a4e13-650">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-650">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-651">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-651">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="a4e13-652">ในแผนภูมิโครงสร้างรูปแบบ ให้เพิ่มองค์ประกอบ **Excel\\ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="a4e13-652">In the format structure tree, add the **Excel\\File** element.</span></span>
3. <span data-ttu-id="a4e13-653">สำหรับองค์ประกอบ **Excel\\ไฟล์** ที่คุณเพิ่งเพิ่ม ให้เพิ่มไฟล์สมุดงาน Excel **A.xlsx** เป็นไฟล์แนบ</span><span class="sxs-lookup"><span data-stu-id="a4e13-653">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="a4e13-654">ใช้ชนิดเอกสารที่มีการตั้งค่าคอนฟิกใน [พารามิเตอร์ ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) เพื่อระบุการจัดเก็บแม่แบบรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-654">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>
4. <span data-ttu-id="a4e13-655">สำหรับองค์ประกอบ **Excel\\ไฟล์** ให้เพิ่มไฟล์สมุดงาน Excel อื่น **B.xlsx** เป็นไฟล์แนบ</span><span class="sxs-lookup"><span data-stu-id="a4e13-655">For the **Excel\\File** element, add another Excel workbook file, **B.xlsx**, as an attachment.</span></span> <span data-ttu-id="a4e13-656">ใช้ชนิดเอกสารเดียวกันกับที่ใช้สำหรับไฟล์สมุดงาน A</span><span class="sxs-lookup"><span data-stu-id="a4e13-656">Use the same document type that is used for workbook file A.</span></span>
5. <span data-ttu-id="a4e13-657">ในองค์ประกอบ **Excel\\ไฟล์** ให้เลือกไฟล์สมุดงาน A</span><span class="sxs-lookup"><span data-stu-id="a4e13-657">In the **Excel\\File** element, select workbook file A.</span></span>
6. <span data-ttu-id="a4e13-658">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของรูปแบบที่แก้ไขได้บนหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-658">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![การตรวจสอบความถูกต้องของส่วนประกอบของรูปแบบที่แก้ไขได้ของไฟล์สมุดงานในหน้าการจัดรูปแบบตัวออกแบบ](./media/er-components-inspections-12a.gif)

7. <span data-ttu-id="a4e13-660">โปรดสังเกตว่าเกิดคำเตือนในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-660">Notice that a validation warning occurs.</span></span> <span data-ttu-id="a4e13-661">ข้อความระบุว่าไฟล์สมุดงาน B.xlsx ไม่ได้เชื่อมโยงกับส่วนประกอบใด ๆ และจะถูกลบออกหลังจากสถานะของรุ่นการตั้งค่าคอนฟิกมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="a4e13-661">The message states that workbook file B.xlsx isn't linked to any components, and that it will be removed after the status of the configuration version is changed.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-662">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-662">Automatic resolution</span></span>

<span data-ttu-id="a4e13-663">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-663">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-664">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-664">Manual resolution</span></span>

<span data-ttu-id="a4e13-665">ปรับเปลี่ยนรูปแบบที่ตั้งค่าคอนฟิกด้วยการลบแม่แบบทั้งหมดที่ไม่ได้เชื่อมโยงกับองค์ประกอบ **Excel\\ไฟล์** ใดๆ</span><span class="sxs-lookup"><span data-stu-id="a4e13-665">Modify the configured format by removing all templates that aren't linked to any **Excel\\File** element.</span></span>

## <a name="not-synced-format"></a><a id="i13"></a><span data-ttu-id="a4e13-666">รูปแบบที่ไม่ได้ซิงค์</span><span class="sxs-lookup"><span data-stu-id="a4e13-666">Not synced format</span></span>

<span data-ttu-id="a4e13-667">เมื่อคุณ [ตั้งค่าคอนฟิก](er-fillable-excel.md) ส่วนประกอบของรูปแบบ ER เพื่อใช้แม่แบบ Excel เพื่อสร้างเอกสารขาออก คุณสามารถเพิ่มองค์ประกอบ **Excel\\ไฟล์** ด้วยตนเอง เพิ่มแม่แบบที่จำเป็นต้องใช้เป็นสิ่งที่แนบมากับส่วนประกอบที่แก้ไขได้ และเลือกสิ่งที่แนบไว้ในองค์ประกอบ **Excel\\ไฟล์** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a4e13-667">When you [configure](er-fillable-excel.md) an ER format component to use an Excel template to generate an outbound document, you can manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="a4e13-668">ด้วยวิธีนี้ คุณบ่งชี้ว่าองค์ประกอบเพิ่มเติมจะเติมแม่แบบที่เลือกเมื่อรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-668">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="a4e13-669">เนื่องจากแม่แบบ Excel ที่เพิ่มมีการออกแบบภายนอก รูปแบบ ER ที่สามารถแก้ไขได้อาจประกอบด้วยชื่อ Excel ที่ขาดหายไปจากแม่แบบที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a4e13-669">Because the added Excel template has been externally designed, the editable ER format might contain Excel names that are missing from the added template.</span></span> <span data-ttu-id="a4e13-670">ตัวออกแบบรูปแบบ ER เตือนคุณเกี่ยวกับความไม่สอดคล้องกันระหว่างคุณสมบัติต่าง ๆ ของรูปแบบ ER ซึ่งอ้างอิงถึงชื่อที่ไม่ได้รวมอยู่ในแม่แบบ Excel ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a4e13-670">The ER format designer warns you about any inconsistencies between the properties of the ER format elements that refer to names that aren't included in the added Excel template.</span></span>

<span data-ttu-id="a4e13-671">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-671">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a4e13-672">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-672">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="a4e13-673">ในแผนภูมิโครงสร้างรูปแบบ ให้เพิ่ม **รายงาน** องค์ประกอบ **Excel\\ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="a4e13-673">In the format structure tree, add the **Excel\\File** element **Report**.</span></span>
3. <span data-ttu-id="a4e13-674">สำหรับองค์ประกอบ **Excel\\ไฟล์** ที่คุณเพิ่งเพิ่ม ให้เพิ่มไฟล์สมุดงาน Excel **A.xlsx** เป็นไฟล์แนบ</span><span class="sxs-lookup"><span data-stu-id="a4e13-674">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="a4e13-675">ใช้ชนิดเอกสารที่มีการตั้งค่าคอนฟิกใน [พารามิเตอร์ ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) เพื่อระบุการจัดเก็บแม่แบบรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-675">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a4e13-676">ตรวจสอบให้แน่ใจว่าสมุดงาน Excel ที่เพิ่มเข้ามาไม่มีชื่อ **ReportTitle**</span><span class="sxs-lookup"><span data-stu-id="a4e13-676">Make sure that the added Excel workbook doesn't contain the name **ReportTitle**.</span></span>

4. <span data-ttu-id="a4e13-677">เพิ่มองค์ประกอบ **Excel\\เซลล์** องค์ประกอบ **ชื่อเรื่อง** เป็นองค์ประกอบที่ซ้อนกันขององค์ประกอบ **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="a4e13-677">Add the **Excel\\Cell** element **Title** as a nested element of the **Report** element.</span></span> <span data-ttu-id="a4e13-678">ในฟิลด์ **ช่วงของ Excel** ให้ป้อน **ReportTitle**</span><span class="sxs-lookup"><span data-stu-id="a4e13-678">In the **Excel range** field, enter **ReportTitle**.</span></span>
5. <span data-ttu-id="a4e13-679">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของรูปแบบที่แก้ไขได้บนหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="a4e13-679">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![การตรวจสอบความถูกต้องขององค์ประกอบที่ซ้อนกันและเขตข้อมูลบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-13a.png)

6. <span data-ttu-id="a4e13-681">โปรดสังเกตว่าเกิดคำเตือนในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-681">Notice that a validation warning occurs.</span></span> <span data-ttu-id="a4e13-682">ข้อความระบุว่าชื่อ **ReportTitle** ไม่มีอยู่บนแผ่นงาน **Sheet1** ของแม่แบบ Excel ที่คุณกำลังใช้อยู่</span><span class="sxs-lookup"><span data-stu-id="a4e13-682">The message states that the name **ReportTitle** doesn't exist on sheet **Sheet1** of the Excel template that you're using.</span></span>

    ![คำเตือนการตรวจสอบความถูกต้องว่าชื่อ ReportTitle ไม่มีอยู่บน Sheet1 ของแม่แบบ Excel](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-684">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-684">Automatic resolution</span></span>

<span data-ttu-id="a4e13-685">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-685">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-686">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-686">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a4e13-687">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="a4e13-687">Option 1</span></span>

<span data-ttu-id="a4e13-688">ปรับเปลี่ยนรูปแบบที่ตั้งค่าคอนฟิกด้วยการลบองค์ประกอบทั้งหมดที่อ้างอิงถึงชื่อ Excel ที่ขาดหายไปจากแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="a4e13-688">Modify the configured format by removing all elements that refer to Excel names that are missing from the template.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a4e13-689">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="a4e13-689">Option 2</span></span>

<span data-ttu-id="a4e13-690">[อัพเดต](er-fillable-excel.md#template-import) รูปปแบบ ER ที่แก้ไขได้โดยการนำเข้าแม่แบบ Excel</span><span class="sxs-lookup"><span data-stu-id="a4e13-690">[Update](er-fillable-excel.md#template-import) the editable ER format by importing an Excel template.</span></span> <span data-ttu-id="a4e13-691">โครงสร้างของรูปแบบ ER ที่สามารถแก้ไขได้จะ [ถูกซิงค์](modify-electronic-reporting-format-reapply-excel-template.md) กับโครงสร้างของแม่แบบ Excel ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="a4e13-691">The structure of the editable ER format will be [synced](modify-electronic-reporting-format-reapply-excel-template.md) with the structure of the imported Excel template.</span></span>

### <a name="additional-consideration"></a><span data-ttu-id="a4e13-692">การพิจารณาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a4e13-692">Additional consideration</span></span>

<span data-ttu-id="a4e13-693">เมื่อต้องการเรียนรู้วิธีการซิงค์โครงสร้างรูปแบบกับแม่แบบ ER ในโปรแกรมแก้ไขแม่แบบของ [การจัดการเอกสารทางธุรกิจ](er-business-document-management.md) ให้ดูที่ [ปรับปรุงโครงสร้างของแม่แบบเอกสารธุรกิจ](er-bdm-update-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a4e13-693">To learn how the format structure can be synced with an ER template in the template editor of [Business document management](er-business-document-management.md), see [Update the structure of a business document template](er-bdm-update-structure.md).</span></span>

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a><span data-ttu-id="a4e13-694">ไม่ได้ซิงค์กับรูปแบบเท็มเพลต Word</span><span class="sxs-lookup"><span data-stu-id="a4e13-694">Not synced with a Word template format</span></span>

<span data-ttu-id="a4e13-695">เมื่อคุณ [กำหนดค่าคอนฟิก](er-fillable-excel.md) ส่วนประกอบของรูปแบบ ER เพื่อใช้เทมเพลต Word เพื่อสร้างเอกสารขาออก คุณจะสามารถเพิ่มองค์ประกอบ **Excel\\ไฟล์** ด้วยตนเองได้ เพิ่มเทมเพลต Word ที่จำเป็นต้องใช้เป็นสิ่งที่แนบมากับส่วนประกอบที่แก้ไขได้ และเลือกสิ่งที่แนบไว้ในองค์ประกอบ **Excel\\ไฟล์** ที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-695">When you [configure](er-fillable-excel.md) an ER format component to use a Word template to generate an outbound document, you can manually add the **Excel\\File** element, add the required Word template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span>

> [!NOTE]
> <span data-ttu-id="a4e13-696">เมื่อแนบเอกสาร Word โปรแกรมออกแบบรูปแบบ ER จะแสดงองค์ประกอบที่แก้ไขได้เป็น **Word\\ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="a4e13-696">When the Word document is attached, the ER format designer presents the editable element as **Word\\File**.</span></span>

<span data-ttu-id="a4e13-697">ด้วยวิธีนี้ คุณบ่งชี้ว่าองค์ประกอบเพิ่มเติมจะเติมแม่แบบที่เลือกเมื่อรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a4e13-697">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="a4e13-698">เนื่องจากเทมเพลต Word ที่เพิ่มขึ้นมีการออกแบบภายนอก รูปแบบ ER ที่สามารถแก้ไขได้อาจมีการอ้างอิงถึงตัวควบคุมเนื้อหา Word ที่ขาดหายไปจากเทมเพลตที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-698">Because the added Word template has been externally designed, the editable ER format might contain references to Word content controls that are missing from the added template.</span></span> <span data-ttu-id="a4e13-699">ตัวออกแบบรูปแบบ ER จะเตือนคุณเกี่ยวกับความไม่สอดคล้องกันระหว่างคุณสมบัติของส่วนประกอบรูปแบบ ER ซึ่งอ้างอิงถึงตัวควบคุมเนื้อหาที่ไม่ได้รวมอยู่ในแม่แบบ Word ที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-699">The ER format designer warns you about any inconsistencies between the properties of the ER format elements that refer to content controls that aren't included in the added Word template.</span></span>

<span data-ttu-id="a4e13-700">ตัวอย่างที่แสดงว่าปัญหานี้อาจเกิดขึ้น ดูได้ที่ [กำหนดค่าคอนฟิกรูปแบบที่แก้ไขได้เพื่อระงับส่วนสรุป](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control)</span><span class="sxs-lookup"><span data-stu-id="a4e13-700">For an example that shows how this issue might occur, see [Configure the editable format to suppress the summary section](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control).</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-701">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-701">Automatic resolution</span></span>

<span data-ttu-id="a4e13-702">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-702">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-703">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-703">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a4e13-704">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="a4e13-704">Option 1</span></span>

<span data-ttu-id="a4e13-705">แก้ไขรูปแบบที่กำหนดค่าคอนฟิกด้วยการลบสูตร **เอาออก** จากองค์ประกอบรูปแบบที่กล่าวถึงในคําเตือนการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-705">Modify the configured format by deleting the **Removed** formula from the format element that is mentioned in the validation warning.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a4e13-706">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="a4e13-706">Option 2</span></span>

<span data-ttu-id="a4e13-707">แก้ไขการใช้เท็มเพลต Word ด้วย [การเพิ่ม](er-design-configuration-word-suppress-controls.md#tag-control) แท็กที่ต้องใช้ในการควบคุมเนื้อหา Word ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-707">Modify the using Word template by [adding](er-design-configuration-word-suppress-controls.md#tag-control) the required tag to the relevant Word content control.</span></span>

## <a name="no-default-mapping"></a><a id="i15"></a><span data-ttu-id="a4e13-708">ไม่มีการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-708">No default mapping</span></span>

<span data-ttu-id="a4e13-709">เมื่อได้ดำเนินการตรวจสอบ [การผูกข้อมูลที่ขาดหายไป](#i11) แล้ว การผูกข้อมูลรูปแบบที่ตรวจสอบจะประเมินเทียบกับการผูกมัดของส่วนประกอบการแม็ปแบบโมเดลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="a4e13-709">When the [Missing binding](#i11) inspection is done, the inspected format bindings are evaluated against the bindings of the relevant model mapping component.</span></span> <span data-ttu-id="a4e13-710">เนื่องจากคุณสามารถนำเข้าการกำหนดค่าการแม็ปโมเดล ER [จำนวนมาก](./tasks/er-manage-model-mapping-configurations-july-2017.md) ไปยังอินสแตนซ์ Finance ของคุณได้ และค่าคอนฟิกแต่ละค่าอาจมีส่วนประกอบการแม็พโมเดลที่เกี่ยวข้อง ค่าคอนฟิกหนึ่งจะต้องถูกเลือกเป็นค่าคอนฟิกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-710">Because you can import [several](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER model mapping configurations to your Finance instance, and each configuration might contain the applicable model mapping component, one configuration must be selected as the default configuration.</span></span> <span data-ttu-id="a4e13-711">มิฉะนั้น เมื่อคุณพยายามรัน แก้ไข หรือตรวจสอบความถูกต้องของรูปแบบ ER ที่ตรวจสอบแล้ว จะเกิดข้อยกเว้นขึ้น และคุณจะได้รับข้อความต่อไปนี้ "มีการแม็ปแบบลองมากกว่าหนึ่งรายการสำหรับ \<model name (root descriptor)\> แบบจำลองข้อมูลในค่าคอนฟิก \<configuration names separated by comma\></span><span class="sxs-lookup"><span data-stu-id="a4e13-711">Otherwise, when you try to run, edit, or validate the inspected ER format, an exception will occur, and you will receive the following message: "More than one model mapping exists for the \<model name (root descriptor)\> data model in the configurations \<configuration names separated by comma\>.</span></span> <span data-ttu-id="a4e13-712">ตั้งค่าการกําหนดค่าคอนฟิกค่าใดค่าหนึ่งเป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-712">Set one of the configurations as default."</span></span>

<span data-ttu-id="a4e13-713">ตัวอย่างที่แสดงว่าปัญหานี้จะเกิดขึ้นและจะสามารถแก้ไขได้อย่างไร ดูได้ที่ [จัดการการแม็พที่ได้รับหลายรายการสำหรับรูทแบบจำลองเดียว](er-multiple-model-mappings.md)</span><span class="sxs-lookup"><span data-stu-id="a4e13-713">For an example that shows how this issue might occur and how it can be fixed, see [Manage several derived mappings for a single model root](er-multiple-model-mappings.md).</span></span>

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a><span data-ttu-id="a4e13-714">การตั้งค่าส่วนประกอบส่วนหัวหรือส่วนท้ายไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-714">Inconsistent setting of Header or Footer components</span></span>

<span data-ttu-id="a4e13-715">เมื่อคุณ [กำหนดค่าคอนฟิก](er-fillable-excel.md) ส่วนประกอบรูปแบบ ER เพื่อใช้เทมเพลต Excel เพื่อสร้างเอกสารขาออก คุณจะสามารถเพิ่มส่วนประกอบ **Excel\\ส่วนหัว** เพื่อเติมในส่วนหัวที่ด้านบนของแผ่นงานในสมุดงาน Excel ได้</span><span class="sxs-lookup"><span data-stu-id="a4e13-715">When you [configure](er-fillable-excel.md) an ER format component to use an Excel template to generate an outbound document, you can add the **Excel\\Header** component to fill in headers at the top of a worksheet in an Excel workbook.</span></span> <span data-ttu-id="a4e13-716">คุณยังสามารถเพิ่มส่วนประกอบ **Excel\\ส่วนท้าย** เพื่อเติมส่วนท้ายที่ด้านล่างของแผ่นงานได้</span><span class="sxs-lookup"><span data-stu-id="a4e13-716">You can also add the **Excel\\Footer** component to fill in footers at the bottom of a worksheet.</span></span> <span data-ttu-id="a4e13-717">สำหรับส่วนประกอบ **Excel\\ส่วนหัว** หรือ **Excel\\ส่วนท้าย** ทุกตัวที่คุณเพิ่ม คุณต้องตั้งค่าคุณสมบัติ **ลักษณะที่ปรากฏของส่วนหัว/ส่วนท้าย** เพื่อระบุหน้าที่รันส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="a4e13-717">For every **Excel\\Header** or **Excel\\Footer** component that you add, you must set the **Header/footer appearance** property to specify the pages that the component is run for.</span></span> <span data-ttu-id="a4e13-718">เนื่องจากคุณสามารถกำหนดค่าคอนฟิกส่วนประกอบ **Excel\\ส่วนหัว** หรือ **Excel\\ส่วนท้าย** หลายส่วน สำหรับส่วนประกอบ **แผ่นงาน** เดี่ยวได้ และคุณสามารถสร้างส่วนหัวหรือส่วนท้ายที่ต่างกันของหน้าชนิดต่างๆ ในแผ่นงาน Excel ได้ คุณต้องกำหนดค่าคอนฟิกของส่วนประกอบ **Excel\\ส่วนหัว** หรือ **Excel\\ส่วนท้าย** เดียวเพื่อกำหนดค่าเฉพาะของคุณสมบัติ **ลักษณะที่ปรากฏของส่วนหัว/ส่วนท้าย**</span><span class="sxs-lookup"><span data-stu-id="a4e13-718">Because you can configure several **Excel\\Header** or **Excel\\Footer** components for a single **Sheet** component, and you can generate different headers or footers for different type of pages in an Excel worksheet, you must configure a single **Excel\\Header** or **Excel\\Footer** component for a specific value of the **Header/footer appearance** property.</span></span> <span data-ttu-id="a4e13-719">ถ้ามีการกำหนดค่าคอนฟิกส่วนประกอบ **Excel\\ส่วนหัว** หรือ **Excel\\ส่วนท้าย** มากกว่าหนึ่งรายการไว้เป็นค่าเฉพาะของคุณสมบัติ **ลักษณะที่ปรากฏของส่วนหัว/ส่วนท้าย** ข้อผิดพลาดการตรวจสอบความถูกต้องจะเกิดขึ้น และคุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ "ส่วนหัว/ส่วนท้าย (&lt;ชนิดส่วนประกอบ: ส่วนหัวหรือส่วนท้าย&gt;) ไม่สอดคล้องกัน"</span><span class="sxs-lookup"><span data-stu-id="a4e13-719">If more than one **Excel\\Header** or **Excel\\Footer** component is configured for a specific value of the **Header/footer appearance** property, a validation error occurs, and you receive the following error message: "Headers/footers (&lt;component type: Header or Footer&gt;) are inconsistent."</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a4e13-720">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a4e13-720">Automatic resolution</span></span>

<span data-ttu-id="a4e13-721">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4e13-721">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a4e13-722">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a4e13-722">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a4e13-723">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="a4e13-723">Option 1</span></span>

<span data-ttu-id="a4e13-724">แก้ไขรูปแบบที่ถูกกำหนดค่าคอนฟิกด้วยการลบส่วนประกอบ **Excel\\ส่วนหัว** หรือ **Excel\\ส่วนท้าย** อย่างใดอย่างหนึ่งที่ไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-724">Modify the configured format by deleting one of the inconsistent **Excel\\Header** or **Excel\\Footer** components.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a4e13-725">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="a4e13-725">Option 2</span></span>

<span data-ttu-id="a4e13-726">แก้ไขค่าของคุณสมบัติ **ลักษณะที่ปรากฏของส่วนหัว/ส่วนท้าย** สำหรับส่วนประกอบ **Excel\\ส่วนหัว** หรือ **Excel\\ส่วนท้าย** ที่ไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="a4e13-726">Modify the value of the **Header/footer appearance** property for one of the inconsistent **Excel\\Header** or **Excel\\Footer** components.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4e13-727">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a4e13-727">Additional resources</span></span>

[<span data-ttu-id="a4e13-728">ฟังก์ชัน ALLITEMS ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-728">ALLITEMS ER function</span></span>](er-functions-list-allitems.md)

[<span data-ttu-id="a4e13-729">ฟังก์ชัน ALLITEMSQUERY ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-729">ALLITEMSQUERY ER function</span></span>](er-functions-list-allitemsquery.md)

[<span data-ttu-id="a4e13-730">ฟังก์ชัน INT64VALUE ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-730">INT64VALUE ER function</span></span>](er-functions-conversion-int64value.md)

[<span data-ttu-id="a4e13-731">ฟังก์ชัน INTVALUE ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-731">INTVALUE ER function</span></span>](er-functions-conversion-intvalue.md)

[<span data-ttu-id="a4e13-732">ฟังก์ชัน FILTER ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-732">FILTER ER function</span></span>](er-functions-list-filter.md)

[<span data-ttu-id="a4e13-733">ฟังก์ชั่น WHERE ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-733">WHERE ER function</span></span>](er-functions-list-where.md)

[<span data-ttu-id="a4e13-734">ใช้แหล่งข้อมูล JOIN เพื่อดึงข้อมูลจากหลายตารางโปรแกรมประยุกต์ในการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="a4e13-734">Use JOIN data sources to get data from multiple application tables in ER model mappings</span></span>](er-join-data-sources.md)

[<span data-ttu-id="a4e13-735">ติดตามการดำเนินการของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a4e13-735">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="a4e13-736">ภาพรวมของการจัดการเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="a4e13-736">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="a4e13-737">ระงับการควบคุมเนื้อหา Word ในรายงานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e13-737">Suppress Word content controls in generated reports</span></span>](er-design-configuration-word-suppress-controls.md)

[<span data-ttu-id="a4e13-738">จัดการการแม็ปที่ได้รับมาหลายรายการสำหรับรากของแบบจำลองเดียว</span><span class="sxs-lookup"><span data-stu-id="a4e13-738">Manage several derived mappings for a single model root</span></span>](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
