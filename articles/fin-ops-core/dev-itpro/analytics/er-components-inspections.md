---
title: ตรวจสอบส่วนประกอบ ER ที่ตั้งค่าคอนฟิกเพื่อป้องกันปัญหารันไทม์
description: หัวข้อนี้อธิบายถึงวิธีการตรวจสอบส่วนประกอบของการรายงานทางอิเล็กทรอนิกส์ (ER) ที่ตั้งค่าคอนฟิกไว้เพื่อป้องกันไม่ให้เกิดปัญหารันไทม์ซึ่งอาจเกิดขึ้นได้
author: NickSelin
manager: AnnBe
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 4ba696fb7a8d9083d11cc29953cf1340a581afcf
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797352"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a><span data-ttu-id="9d5b6-103">ตรวจสอบส่วนประกอบ ER ที่ตั้งค่าคอนฟิกเพื่อป้องกันปัญหารันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-103">Inspect the configured ER component to prevent runtime issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9d5b6-104">ทุก ๆ [รูปแบบ](general-electronic-reporting.md#FormatComponentOutbound) [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) และส่วนประกอบ [การแม็ปแบบจำลอง](general-electronic-reporting.md#data-model-and-model-mapping-components) สามารถ [ตรวจสอบความถูกต้อง](er-fillable-excel.md#validate-an-er-format) ในเวลาที่ออกแบบได้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-104">Every configured [Electronic reporting (ER)](general-electronic-reporting.md) [format](general-electronic-reporting.md#FormatComponentOutbound) and [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component can be [validated](er-fillable-excel.md#validate-an-er-format) at design time.</span></span> <span data-ttu-id="9d5b6-105">ในระหว่างการตรวจสอบความถูกต้องนี้ การตรวจสอบความสอดคล้องกันจะดำเนินการเพื่อช่วยป้องกันปัญหารันไทม์ซึ่งอาจเกิดขึ้น เช่น ข้อผิดพลาดในการดำเนินการและการลดประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-105">During this validation, a consistency check runs to help prevent runtime issues that might occur, such as execution errors and performance degradation.</span></span> <span data-ttu-id="9d5b6-106">สำหรับทุกปัญหาที่พบ การตรวจสอบจะระบุพาธของส่วนประกอบที่เป็นปัญหา</span><span class="sxs-lookup"><span data-stu-id="9d5b6-106">For every issue found, the check provides the path of a problematic element.</span></span> <span data-ttu-id="9d5b6-107">สำหรับปัญหาบางอย่าง การแก้ไขอัตโนมัติจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-107">For some issues, an automatic fix is available.</span></span>

<span data-ttu-id="9d5b6-108">โดยค่าเริ่มต้น การตรวจสอบความถูกต้องจะใช้โดยอัตโนมัติในกรณีต่อไปนี้สำหรับการตั้งค่าคอนฟิก ER ที่มีส่วนประกอบ ER ดังกล่าวก่อนหน้านี้:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-108">By default, the validation is automatically applied in the following cases for an ER configuration that contains the previously mentioned ER components:</span></span>

- <span data-ttu-id="9d5b6-109">คุณสามารถ [นำเข้า](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) [รุ่น](general-electronic-reporting.md#component-versioning) การตั้งค่าคอนฟิก ER ใหม่ไปยังอินสแตนซ์ของ Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9d5b6-109">You [import](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) a new [version](general-electronic-reporting.md#component-versioning) of an ER configuration into your instance of Microsoft Dynamics 365 Finance.</span></span>
- <span data-ttu-id="9d5b6-110">คุณเปลี่ยน [สถานะ](general-electronic-reporting.md#component-versioning) การตั้งค่าคอนฟิก ER ที่สามารถแก้ไขได้จาก **แบบร่าง** เป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-110">You change the [status](general-electronic-reporting.md#component-versioning) of the editable ER configuration from **Draft** to **Completed**.</span></span>
- <span data-ttu-id="9d5b6-111">คุณ [ปรับใช้](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) การตั้งค่าคอนฟิก ER ที่สามารถแก้ไขได้โดยใช้รุ่นพื้นฐานใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-111">You [rebase](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) an editable ER configuration by applying a new base version.</span></span>

<span data-ttu-id="9d5b6-112">คุณสามารถรันการตรวจสอบความถูกต้องนี้อย่างชัดแจ้ง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-112">You can explicitly run this validation.</span></span> <span data-ttu-id="9d5b6-113">เลือกตัวเลือกอย่างใดอย่างหนึ่งจากสามตัวเลือกต่อไปนี้และปฏิบัติตามขั้นตอนที่ระบุ:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-113">Select one of the following three options, and follow the steps that are provided:</span></span>

- <span data-ttu-id="9d5b6-114">ตัวเลือก 1:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-114">Option 1:</span></span>

    1. <span data-ttu-id="9d5b6-115">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-115">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="9d5b6-116">ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิก ER ที่ต้องการที่มีรูปแบบ ER หรือส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-116">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format or ER model mapping component.</span></span>
    3. <span data-ttu-id="9d5b6-117">บนแท็บด่วน **รุ่น** เลือกรุ่นที่ต้องการของการตั้งค่าคอนฟิก ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9d5b6-117">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="9d5b6-118">บนบานหน้าต่างการดำเนินการ เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-118">On the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="9d5b6-119">ตัวเลือก 2 สำหรับรูปแบบ ER:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-119">Option 2, for an ER format:</span></span>

    1. <span data-ttu-id="9d5b6-120">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-120">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="9d5b6-121">ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิก ER ที่ต้องการที่มีส่วนประกอบรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-121">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format component.</span></span>
    3. <span data-ttu-id="9d5b6-122">บนแท็บด่วน **รุ่น** เลือกรุ่นที่ต้องการของการตั้งค่าคอนฟิก ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9d5b6-122">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="9d5b6-123">บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-123">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="9d5b6-124">บนหน้า **ตัวออกแบบรูปแบบ** บนบานหน้าต่างการดำเนินการ ให้เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-124">On the **Format designer** page, on the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="9d5b6-125">ตัวเลือก 3 สำหรับการแม็ปแบบจำลอง ER:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-125">Option 3, for an ER model mapping:</span></span>

    1. <span data-ttu-id="9d5b6-126">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-126">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="9d5b6-127">ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิก ER ที่ต้องการที่มีส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-127">In the configurations tree in the left pane, select the desired ER configuration that contains the ER model mapping component.</span></span>
    3. <span data-ttu-id="9d5b6-128">บนแท็บด่วน **รุ่น** เลือกรุ่นที่ต้องการของการตั้งค่าคอนฟิก ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9d5b6-128">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="9d5b6-129">บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-129">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="9d5b6-130">บนหน้า **การแม็ปแบบจำลองกับแหล่งข้อมูล** บนแผงการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-130">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>
    6. <span data-ttu-id="9d5b6-131">บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** บนแผงการดำเนินการ เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-131">On the **Model mapping designer** page, on the Action Pane, select **Validate**.</span></span>

<span data-ttu-id="9d5b6-132">เมื่อต้องการข้ามการตรวจสอบความถูกต้องเมื่อมีการนำเข้าการตั้งค่าคอนฟิก ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-132">To skip the validation when the configuration is imported, follow these steps.</span></span>

1. <span data-ttu-id="9d5b6-133">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-133">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="9d5b6-134">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-134">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="9d5b6-135">ตั้งค่าตัวเลือก **ตรวจสอบความถูกต้องการตั้งค่าคอนฟิกหลังจากนำเข้า** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-135">Set the **Validate the configuration after importing** option to **No**.</span></span>

<span data-ttu-id="9d5b6-136">เมื่อต้องการข้ามการตรวจสอบความถูกต้องเมื่อคุณเปลี่ยนแปลงหรือปรับใช้สถานะของรุ่น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-136">To skip the validation when you change or rebase the version's status, follow these steps.</span></span>

1. <span data-ttu-id="9d5b6-137">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-137">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="9d5b6-138">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-138">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="9d5b6-139">ตั้งค่าตัวเลือก **ข้ามการตรวจสอบความถูกต้องเมื่อสถานะของการตั้งค่าคอนฟิกเปลี่ยนแปลงและปรับใช้** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-139">Set the **Skip validation at configuration's status change and rebase** option to **Yes**.</span></span>

<span data-ttu-id="9d5b6-140">ER ใช้ประเภทต่อไปนี้ในการตรวจสอบความสอดคล้องกันของกลุ่มการตรวจสอบ:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-140">ER uses the following categories to group consistency check inspections:</span></span>

- <span data-ttu-id="9d5b6-141">**ความสามารถในการปฏิบัติการ** – การตรวจสอบที่พบปัญหาที่สำคัญซึ่งอาจเกิดขึ้นเมื่อรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-141">**Executability** – Inspections that detect critical issues that might happen at runtime.</span></span> <span data-ttu-id="9d5b6-142">ปัญหาเหล่านี้ส่วนใหญ่จะอยู่ในระดับ **ข้อผิดพลาด**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-142">These issues are mostly at an **Error** level.</span></span> 
- <span data-ttu-id="9d5b6-143">**ประสิทธิภาพ** – การตรวจสอบที่ตรวจพบปัญหาที่อาจทำให้เกิดการดำเนินการที่ไม่มีประสิทธิภาพของส่วนประกอบ ER ที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="9d5b6-143">**Performance** – Inspections that detect issues that might cause inefficient execution of configured ER components.</span></span> <span data-ttu-id="9d5b6-144">ปัญหาเหล่านี้ส่วนใหญ่จะอยู่ในระดับ **คำเตือน**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-144">These issues are mostly at a **Warning** level.</span></span>
- <span data-ttu-id="9d5b6-145">**ความถูกต้องของข้อมูล** – การตรวจสอบที่ตรวจพบปัญหาที่อาจทำให้เกิดปัญหาการสูญเสียข้อมูลหรือรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-145">**Data integrity** – Inspections that detect issues that might cause data loss or runtime issues.</span></span> <span data-ttu-id="9d5b6-146">ปัญหาเหล่านี้ส่วนใหญ่จะอยู่ในระดับ **คำเตือน**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-146">These issues are mostly at a **Warning** level.</span></span>

## <a name="list-of-inspections"></a><span data-ttu-id="9d5b6-147">รายการของการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-147">List of inspections</span></span>

<span data-ttu-id="9d5b6-148">ตารางต่อไปนี้จะแสดงภาพรวมของการตรวจสอบที่ ER มีให้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-148">The following table provides an overview of the inspections that ER provides.</span></span> <span data-ttu-id="9d5b6-149">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตรวจสอบเหล่านี้ ให้ใช้การเชื่อมโยงในคอลัมน์แรกเพื่อไปที่ส่วนที่เกี่ยวข้องของหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-149">For more information about these inspections, use the links in the first column to go to the relevant sections of this topic.</span></span> <span data-ttu-id="9d5b6-150">ส่วนเหล่านี้จะอธิบายชนิดของส่วนประกอบที่ ER ให้การตรวจสอบและวิธีที่คุณสามารถตั้งค่าคอนฟิกส่วนประกอบ ER เพื่อช่วยป้องกันปัญหา</span><span class="sxs-lookup"><span data-stu-id="9d5b6-150">Those sections explain the types of components that ER provides inspections for and how you can reconfigure ER components to help prevent issues.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9d5b6-151">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-151">Name</span></span></th>
<th><span data-ttu-id="9d5b6-152">ประเภท</span><span class="sxs-lookup"><span data-stu-id="9d5b6-152">Category</span></span></th>
<th><span data-ttu-id="9d5b6-153">ระดับ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-153">Level</span></span></th>
<th><span data-ttu-id="9d5b6-154">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-154">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d5b6-155"><a href='#i1'>ชนิดการแปลง</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-155"><a href='#i1'>Type conversion</a></span></span></td>
<td><span data-ttu-id="9d5b6-156">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-156">Executability</span></span></td>
<td><span data-ttu-id="9d5b6-157">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-157">Error</span></span></td>
<td>
<p><span data-ttu-id="9d5b6-158">ไม่สามารถแปลงนิพจน์ชนิด &lt;ชนิด&gt; เป็นฟิลด์ชนิด &lt;ชนิด&gt;</span><span class="sxs-lookup"><span data-stu-id="9d5b6-158">Cannot convert expression of type &lt;type&gt; to field of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="9d5b6-159"><b>ข้อผิดพลาดรันไทม์:</b> ข้อยกเว้นสำหรับชนิด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-159"><b>Runtime error:</b> Exception for type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="9d5b6-160"><a href='#i2'>ความเข้ากันได้ของชนิด</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-160"><a href='#i2'>Type compatibility</a></span></span></td>
<td><span data-ttu-id="9d5b6-161">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-161">Executability</span></span></td>
<td><span data-ttu-id="9d5b6-162">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-162">Error</span></span></td>
<td>
<p><span data-ttu-id="9d5b6-163">นิพจน์ที่ตั้งค่าคอนฟิกไม่สามารถใช้ได้เนื่องจากมีการรวมกันขององค์ประกอบรูปแบบปัจจุบันไปยังแหล่งข้อมูลเป็นนิพจน์นี้ส่งคืนค่าชนิดของชนิดข้อมูล &lt;ชนิด&gt; ที่อยู่นอกขอบเขตของชนิดข้อมูลที่รองรับโดยองค์ประกอบรูปแบบปัจจุบันของชนิด &lt;ชนิด&gt;</span><span class="sxs-lookup"><span data-stu-id="9d5b6-163">The configured expression cannot be used as the binding of the current format element to a data source as this expression returns value of the data type &lt;type&gt; that is beyond the scope of data types that are supported by the current format element of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="9d5b6-164"><b>ข้อผิดพลาดรันไทม์:</b> ข้อยกเว้นของชนิด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-164"><b>Runtime error:</b> Exception of type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="9d5b6-165"><a href='#i3'>ขาดองค์ประกอบการตั้งค่าคอนฟิก</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-165"><a href='#i3'>Missing configuration element</a></span></span></td>
<td><span data-ttu-id="9d5b6-166">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-166">Executability</span></span></td>
<td><span data-ttu-id="9d5b6-167">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-167">Error</span></span></td>
<td>
<p><span data-ttu-id="9d5b6-168">ไม่พบพาธ &lt;พาธ&gt;</span><span class="sxs-lookup"><span data-stu-id="9d5b6-168">Path not found &lt;path&gt;.</span></span></p>
<p><span data-ttu-id="9d5b6-169"><b>ข้อผิดพลาดรันไทม์:</b> ไม่พบองค์ประกอบของพาธการตั้งค่าคอนฟิก &lt;พาธ&gt;</span><span class="sxs-lookup"><span data-stu-id="9d5b6-169"><b>Runtime error:</b> Element of the configuration &lt;path&gt; not found</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="9d5b6-170"><a href='#i4'>ความสามารถในการปฏิบัติการนิพจน์กับฟังก์ชันตัวกรอง</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-170"><a href='#i4'>Executability of an expression with FILTER function</a></span></span></td>
<td><span data-ttu-id="9d5b6-171">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-171">Executability</span></span></td>
<td><span data-ttu-id="9d5b6-172">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-172">Error</span></span></td>
<td>
<p><span data-ttu-id="9d5b6-173">นิพจน์รายการของฟังก์ชัน FILTER ไม่สามารถสอบถามได้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-173">The list expression of FILTER function is not queryable.</span></span></p>
<p><span data-ttu-id="9d5b6-174"><b>ข้อผิดพลาดรันไทม์:</b> ไม่สนับสนุนการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d5b6-174"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="9d5b6-175">ตรวจสอบความถูกต้องของการตั้งค่าคอนฟิกเพื่อดูรายละเอียดเพิ่มเติมเกี่ยวกับเรื่องนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-175">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="9d5b6-176"><a href='#i5'>ความสามารถในการปฏิบัติการของแหล่งข้อมูล GROUPBY</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-176"><a href='#i5'>Executability of a GROUPBY data source</a></span></span></td>
<td><span data-ttu-id="9d5b6-177">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-177">Executability</span></span></td>
<td><span data-ttu-id="9d5b6-178">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-178">Error</span></span></td>
<td><span data-ttu-id="9d5b6-179">พาธ &lt;พาธ&gt; ไม่รองรับการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-179">Path &lt;path&gt; does not support querying.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d5b6-180">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-180">Executability</span></span></td>
<td><span data-ttu-id="9d5b6-181">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-181">Error</span></span></td>
<td>
<p><span data-ttu-id="9d5b6-182">การจัดกลุ่มตามฟังก์ชันไม่สามารถดำเนินการโดยใช้การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-182">Group by function cannot be executed with query.</span></span></p>
<p><span data-ttu-id="9d5b6-183"><b>ข้อผิดพลาดรันไทม์:</b> การจัดกลุ่มตามฟังก์ชันไม่สามารถดำเนินการโดยใช้การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-183"><b>Runtime error:</b> Group by function can't be executed with query.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="9d5b6-184"><a href='#i6'>ความสามารถในการปฏิบัติการของแหล่งข้อมูล JOIN</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-184"><a href='#i6'>Executability of a JOIN data source</a></span></span></td>
<td><span data-ttu-id="9d5b6-185">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-185">Executability</span></span></td>
<td><span data-ttu-id="9d5b6-186">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-186">Error</span></span></td>
<td>
<p><span data-ttu-id="9d5b6-187">ไม่สามารถรวม &lt;พาธ&gt; ของรายการที่ไม่ใช่ตัวกรองข้อมูลในการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-187">Cannot join a list &lt;path&gt; that is not a filter in query.</span></span></p>
<p><span data-ttu-id="9d5b6-188"><b>ข้อผิดพลาดรันไทม์:</b> แหล่งข้อมูลที่รวมฟังก์ชันควรเป็นนิพจน์ของตัวกรอง ฟิลด์ที่คำนวณถูกเรียกอย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-188"><b>Runtime error:</b> Function Joined datasource should be a filter expression calculated field has been incorrectly called.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="9d5b6-189"><a href='#i7'>ความเป็นที่ต้องการมากกว่าของฟังก์ชัน FILTER เทียบกับฟังก์ชัน WHERE</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-189"><a href='#i7'>Preferability of FILTER vs WHERE function</a></span></span></td>
<td><span data-ttu-id="9d5b6-190">ประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-190">Performance</span></span></td>
<td><span data-ttu-id="9d5b6-191">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-191">Warning</span></span></td>
<td><span data-ttu-id="9d5b6-192">การใช้ฟังก์ชัน FILTER สำหรับนิพจน์นี้จะเป็นที่ต้องการมากกว่า WHERE จากมุมมองประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-192">Using FILTER function for the expression is preferable than WHERE from the performance perspective.</span></span> <span data-ttu-id="9d5b6-193">เลือก แก้ไข เพื่อแทนที่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-193">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d5b6-194"><a href='#i8'>ความเป็นที่ต้องการมากกว่าของฟังก์ชัน ALLITEMSQUERY เทียบกับฟังก์ชัน ALLITEMS</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-194"><a href='#i8'>Preferability of ALLITEMSQUERY vs ALLITEMS function</a></span></span></td>
<td><span data-ttu-id="9d5b6-195">ประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-195">Performance</span></span></td>
<td><span data-ttu-id="9d5b6-196">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-196">Warning</span></span></td>
<td><span data-ttu-id="9d5b6-197">การใช้ฟังก์ชัน ALLITEMSQUERY สำหรับนิพจน์นี้จะเป็นที่ต้องการมากกว่า ALLITEMS จากมุมมองประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-197">Using ALLITEMSQUERY function for the expression is preferable than ALLITEMS from the performance perspective.</span></span> <span data-ttu-id="9d5b6-198">เลือก แก้ไข เพื่อแทนที่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-198">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d5b6-199"><a href='#i9'>การพิจารณากรณีของรายการที่ว่างเปล่า</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-199"><a href='#i9'>Consideration of empty list cases</a></span></span></td>
<td><span data-ttu-id="9d5b6-200">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-200">Executability</span></span></td>
<td><span data-ttu-id="9d5b6-201">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-201">Warning</span></span></td>
<td>
<p><span data-ttu-id="9d5b6-202">รายการ &lt;พาธ&gt; ไม่มีการตรวจสอบสำหรับกรณีของรายการที่ว่างเปล่า อาจทำให้เกิดข้อผิดพลาดขณะดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-202">List &lt;path&gt; does not have any check for empty list case, it can result an error at run time.</span></span> <span data-ttu-id="9d5b6-203">เพิ่มการตรวจสอบสำหรับกรณีของรายการที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="9d5b6-203">Add a check for empty list case.</span></span></p>
<p><span data-ttu-id="9d5b6-204"><b>ข้อผิดพลาดรันไทม์:</b> รายการว่างเปล่าที่ &lt;พาธ&gt;</span><span class="sxs-lookup"><span data-stu-id="9d5b6-204"><b>Runtime error:</b> List is empty at &lt;path&gt;</span></span></p>
<p><span data-ttu-id="9d5b6-205"><b><a href='#i9a'>ปัญหาที่อาจเกิดขึ้น</a>:</b> มีการเติมข้อมูลรายการหนึ่งครั้งในขณะที่แหล่งข้อมูลมีการเติมข้อมูลจากหลายเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-205"><b><a href='#i9a'>Potential issue</a>:</b> Line is getting populated once while a data source it is populated from contains multiple records</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="9d5b6-206"><a href='#i10'>ความสามารถในการปฏิบัติการนิพจน์กับฟังก์ชันตัวกรอง (การแคช)</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-206"><a href='#i10'>Executability of an expression with FILTER function (caching)</a></span></span></td>
<td><span data-ttu-id="9d5b6-207">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-207">Executability</span></span></td>
<td><span data-ttu-id="9d5b6-208">ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-208">Error</span></span></td>
<td>
<p><span data-ttu-id="9d5b6-209">ฟังก์ชัน FILTER ไม่สามารถใช้กับชนิดแหล่งข้อมูลที่เลือกได้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-209">FILTER function cannot be applied to the selected type of data source.</span></span> <span data-ttu-id="9d5b6-210">แหล่งข้อมูลของชนิดเรกคอร์ดตารางใช้ได้เฉพาะเมื่อไม่มีการแคชไว้และไม่มีการเพิ่มแหล่งข้อมูลที่ซ้อนกันด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-210">A data source of the Table records type is applicable only when it is not cached and has no manually added nested data sources.</span></span></p>
<p><span data-ttu-id="9d5b6-211"><b>ข้อผิดพลาดรันไทม์:</b> ไม่สนับสนุนการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d5b6-211"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="9d5b6-212">ตรวจสอบความถูกต้องของการตั้งค่าคอนฟิกเพื่อดูรายละเอียดเพิ่มเติมเกี่ยวกับเรื่องนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-212">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="9d5b6-213"><a href='#i11'>ขาดการผูกข้อมูล</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-213"><a href='#i11'>Missing binding</a></span></span></td>
<td><span data-ttu-id="9d5b6-214">ความสามารถในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-214">Executability</span></span></td>
<td><span data-ttu-id="9d5b6-215">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-215">Warning</span></span></td>
<td>
<p><span data-ttu-id="9d5b6-216">พาธ &lt;พาธ&gt; ไม่มีการผูกกับแหล่งข้อมูลใด ๆ ในการใช้การแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-216">Path &lt;path&gt; has no binding to any datasource in using model's mapping.</span></span></p>
<p><span data-ttu-id="9d5b6-217"><b>ข้อผิดพลาดรันไทม์:</b> พาธ &lt;พาธ&gt; ไม่ถูกผูกไว้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-217"><b>Runtime error:</b> Path &lt;path&gt; is not bound</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="9d5b6-218"><a href='#i12'>แม่แบบไม่มีการเชื่อมโยง</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-218"><a href='#i12'>Not linked template</a></span></span></td>
<td><span data-ttu-id="9d5b6-219">ความสมบูรณ์ของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d5b6-219">Data integrity</span></span></td>
<td><span data-ttu-id="9d5b6-220">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-220">Warning</span></span></td>
<td><span data-ttu-id="9d5b6-221">ชื่อ &lt;ไฟล์&gt; ถูกลิงค์ไปยังไม่มีส่วนประกอบของไฟล์และจะถูกลบออกหลังจากเปลี่ยนสถานะของรุ่นการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="9d5b6-221">File &lt;name&gt; is linked to no file components and will be removed after changing status of configuration version.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d5b6-222"><a href='#i13'>รูปแบบที่ไม่ได้ซิงค์</a></span><span class="sxs-lookup"><span data-stu-id="9d5b6-222"><a href='#i13'>Not synced format</a></span></span></td>
<td><span data-ttu-id="9d5b6-223">ความสมบูรณ์ของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d5b6-223">Data integrity</span></span></td>
<td><span data-ttu-id="9d5b6-224">คำเตือน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-224">Warning</span></span></td>
<td><span data-ttu-id="9d5b6-225">ชื่อที่กำหนดของ &lt;ชื่อส่วนประกอบ&gt; ไม่มีอยู่ใน &lt;ชื่อแผ่นงาน&gt; แผ่นงาน Excel</span><span class="sxs-lookup"><span data-stu-id="9d5b6-225">Defined name &lt;component name&gt; does not exist in Excel sheet &lt;sheet name&gt;</span></span></td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a><span data-ttu-id="9d5b6-226">ชนิดการแปลง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-226">Type conversion</span></span>

<span data-ttu-id="9d5b6-227">ER จะตรวจสอบว่าชนิดข้อมูลของฟิลด์รูปแบบข้อมูลเข้ากันได้กับชนิดข้อมูลของนิพจน์ที่มีการตั้งค่าคอนฟิกเป็นการรวมของฟิลด์นั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-227">ER checks whether the data type of a data model field is compatible with the data type of an expression that is configured as the binding of that field.</span></span> <span data-ttu-id="9d5b6-228">หากชนิดข้อมูลเข้ากันไม่ได้ ข้อผิดพลาดในการตรวจสอบความถูกต้องเกิดขึ้นในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-228">If the data types are incompatible, a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="9d5b6-229">ข้อความที่คุณได้รับระบุว่า ER ไม่สามารถแปลงนิพจน์ชนิด A ไปยังฟิลด์ชนิด B</span><span class="sxs-lookup"><span data-stu-id="9d5b6-229">The message that you receive states that ER can't convert an expression of type A to a field of type B.</span></span>

<span data-ttu-id="9d5b6-230">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-230">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-231">เริ่มต้นการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER และส่วนประกอบการแม็ปแบบจำลอง ER พร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-231">Start to configure the ER data model and the ER model-mapping components simultaneously.</span></span>
2. <span data-ttu-id="9d5b6-232">ในแผนภูมิรูปแบบข้อมูล ให้เพิ่มฟิลด์ที่ชื่อ **X** และเลือก **จำนวนเต็ม** เป็นชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d5b6-232">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![ชนิดของฟิลด์ X และข้อมูลจำนวนเต็มที่เพิ่มลงในแผนภูมิโหมดข้อมูลบนหน้ารูปแบบข้อมูล](./media/er-components-inspections-01.png)

3. <span data-ttu-id="9d5b6-234">ในบานหน้าต่างแหล่งข้อมูลการแม็ปแบบจำลอง เพิ่มแหล่งข้อมูลของชนิด **ฟิลด์ที่มีการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-234">In the model-mapping data sources pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="9d5b6-235">ตั้งชื่อแหล่งข้อมูล **Y** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `INTVALUE(100)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-235">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="9d5b6-236">ผูก **X** กับ **Y**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-236">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="9d5b6-237">ในตัวออกแบบรูปแบบข้อมูล ให้เปลี่ยนชนิดข้อมูลของฟิลด์ **X** จาก **จำนวนเต็ม** เป็น **Int64**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-237">In the data model designer, change the data type of the **X** field from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="9d5b6-238">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-238">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![ตรวจสอบความถูกต้องส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-01.gif)

8. <span data-ttu-id="9d5b6-240">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองของการตั้งค่าคอนฟิก ER ที่เลือกบนหน้า **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-240">Select **Validate** to inspect the model-mapping component of the selected ER configuration on the **Configurations** page.</span></span>

    ![ตรวจสอบความถูกต้องเพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองบนหน้าการตั้งค่าคอนฟิก](./media/er-components-inspections-01a.png)

9. <span data-ttu-id="9d5b6-242">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-242">Notice that a validation error occurs.</span></span> <span data-ttu-id="9d5b6-243">ข้อความระบุว่าค่าของชนิด **จำนวนเต็ม** ที่นิพจน์ `INTVALUE(100)` ของการส่งคืนแหล่งข้อมูล **Y** ไม่สามารถจัดเก็บในฟิลด์รูปแบบข้อมูล **X** ของ ชนิด **Int64**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-243">The message states that the value of the **Integer** type that the `INTVALUE(100)` expression of the **Y** data source returns can't be stored in the **X** data model field of the **Int64** type.</span></span>

<span data-ttu-id="9d5b6-244">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้น ถ้าคุณละเว้นคำเตือนและเลือก **รัน** เพื่อรันรูปแบบที่มีการตั้งค่าคอนฟิกให้ใช้การแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-244">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model-mapping.</span></span>

![ข้อผิดพลาดรันไทม์บนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-246">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-246">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-247">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-247">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-248">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-248">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="9d5b6-249">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="9d5b6-249">Option 1</span></span>

<span data-ttu-id="9d5b6-250">อัปเดตโครงสร้างรูปแบบข้อมูลด้วยการเปลี่ยนชนิดข้อมูลของฟิลด์รูปแบบข้อมูลเพื่อให้ตรงกับชนิดข้อมูลของนิพจน์ที่มีการตั้งค่าคอนฟิกไว้สำหรับการผูกข้อมูลของฟิลด์นั้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-250">Update the data model structure by changing the data type of the data model field so that it matches the data type of the expression that is configured for the binding of that field.</span></span> <span data-ttu-id="9d5b6-251">สำหรับตัวอย่างก่อนหน้านี้ ชนิดข้อมูลของฟิลด์ **X** ต้องเปลี่ยนให้เป็น **จำนวนเต็ม**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-251">For the preceding example, the data type of the **X** field must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="9d5b6-252">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="9d5b6-252">Option 2</span></span>

<span data-ttu-id="9d5b6-253">อัปเดตการแม็ปแบบจำลองด้วยการเปลี่ยนนิพจน์ของแหล่งข้อมูลที่ผูกกับฟิลด์รูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d5b6-253">Update the model-mapping by changing the expression of the data source that is bound with the data model field.</span></span> <span data-ttu-id="9d5b6-254">สำหรับตัวอย่างก่อนหน้านี้ นิพจน์ของแหล่งข้อมูล **Y** ต้องเปลี่ยนเป็น `INT64VALUE(100)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-254">For the preceding example, the expression of the **Y** data source must be changed to `INT64VALUE(100)`.</span></span>

## <a name="type-compatibility"></a><a id="i2"></a><span data-ttu-id="9d5b6-255">ความเข้ากันได้ของชนิด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-255">Type compatibility</span></span>

<span data-ttu-id="9d5b6-256">ER จะตรวจสอบว่าชนิดข้อมูลขององค์ประกอบรูปแบบเข้ากันได้กับชนิดข้อมูลของนิพจน์ที่มีการตั้งค่าคอนฟิกเป็นการรวมขององค์ประกอบรูปแบบนั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-256">ER checks whether the data type of a format element is compatible with the data type of an expression that is configured as the binding of that format element.</span></span> <span data-ttu-id="9d5b6-257">หากชนิดข้อมูลเข้ากันไม่ได้ ข้อผิดพลาดในการตรวจสอบความถูกต้องเกิดขึ้นในโปรแกรมออกแบบการดำเนินงาน ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-257">If the data types are incompatible, a validation error occurs in the ER Operations designer.</span></span> <span data-ttu-id="9d5b6-258">ข้อความที่คุณได้รับระบุว่านิพจน์ที่ตั้งค่าคอนฟิกไม่สามารถใช้ได้เนื่องจากมีการรวมกันขององค์ประกอบรูปแบบปัจจุบันไปยังแหล่งข้อมูล เนื่องจากนิพจน์นี้ส่งคืนค่าชนิดของชนิดข้อมูล A ที่อยู่นอกขอบเขตของชนิดข้อมูลที่รองรับโดยองค์ประกอบรูปแบบปัจจุบันของชนิด B</span><span class="sxs-lookup"><span data-stu-id="9d5b6-258">The message that you receive states that the configured expression can't be used as the binding of the current format element to a data source, because the expression returns a value of data type A that is beyond the scope of the data types that are supported by the current format element of type B.</span></span>

<span data-ttu-id="9d5b6-259">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-259">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-260">เริ่มต้นการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER และส่วนประกอบการรูปแบบ ER พร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-260">Start to configure the ER data model and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="9d5b6-261">ในแผนภูมิรูปแบบข้อมูล ให้เพิ่มฟิลด์ที่ชื่อ **X** และเลือก **จำนวนเต็ม** เป็นชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d5b6-261">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>
3. <span data-ttu-id="9d5b6-262">ในแผนภูมิโครงสร้างรูปแบบ ให้เพิ่มองค์ประกอบรูปแบบของชนิด **ตัวเลข**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-262">In the format structure tree, add a format element of the **Numeric** type.</span></span>
4. <span data-ttu-id="9d5b6-263">ชื่อองค์ประกอบรูปแบบใหม่ **Y** ในฟิลด์ **ชนิดตัวเลข** ให้เลือก **จำนวนเต็ม** เป็นชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d5b6-263">Name the new format element **Y**. In the **Numeric type** field, select **Integer** as the data type.</span></span>
5. <span data-ttu-id="9d5b6-264">ผูก **X** กับ **Y**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-264">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="9d5b6-265">ในแผนภูมิโครงสร้างรูปแบบ ให้เปลี่ยนชนิดข้อมูลขององค์ประกอบรูปแบบ **Y** จาก **เลขจำนวนเต็ม** เป็น **Int64**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-265">In the format structure tree, change the data type of the **Y** format element from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="9d5b6-266">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของรูปแบบที่แก้ไขได้บนหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-266">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![กำลังตรวจสอบความเข้ากันได้ของชนิดบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-02.gif)

8. <span data-ttu-id="9d5b6-268">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-268">Notice that a validation error occurs.</span></span> <span data-ttu-id="9d5b6-269">ข้อความระบุว่านิพจน์ที่ตั้งค่าคอนฟิกสามารถยอมรับได้เฉพาะค่า **Int64**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-269">The message states that the configured expression can accept only **Int64** values.</span></span> <span data-ttu-id="9d5b6-270">ดังนั้น ค่าของฟิลด์รูปแบบข้อมูล **X** ของชนิด **จำนวนเต็ม** ไม่สามารถป้อนในองค์ประกอบรูปแบบ **Y**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-270">Therefore, the value of the **X** data model field of the **Integer** type can't be entered in the **Y** format element.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-271">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-271">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-272">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-272">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-273">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-273">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="9d5b6-274">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="9d5b6-274">Option 1</span></span>

<span data-ttu-id="9d5b6-275">อัปเดตโครงสร้างรูปแบบด้วยการเปลี่ยนชนิดข้อมูลขององค์ประกอบรูปแบบ **ตัวเลข** เพื่อให้ตรงกับชนิดข้อมูลของนิพจน์ ที่คุณตั้งค่าคอนฟิกไว้สำหรับการผูกข้อมูลขององค์ประกอบนั้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-275">Update the format structure by changing the data type of the **Numeric** format element so that it matches the data type of the expression that you configured for the binding of that element.</span></span> <span data-ttu-id="9d5b6-276">ในตัวอย่างก่อนหน้านี้ ค่า **ชนิดตัวเลข** ขององค์ประกอบรูปแบบ **X** ต้องเปลี่ยนให้เป็น **จำนวนเต็ม**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-276">In the preceding example, the **Numeric type** value of the **X** format element must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="9d5b6-277">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="9d5b6-277">Option 2</span></span>

<span data-ttu-id="9d5b6-278">อัปเดตการแม็ปรูปแบบขององค์ประกอบรูปแบบ **X** โดยการเปลี่ยนแปลงนิพจน์จาก `model.X` เป็น `INT64VALUE(model.X)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-278">Update the format mapping of the **X** format element by changing the expression from `model.X` to `INT64VALUE(model.X)`.</span></span>

## <a name="missing-configuration-element"></a><a id="i3"></a><span data-ttu-id="9d5b6-279">ขาดองค์ประกอบการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="9d5b6-279">Missing configuration element</span></span>

<span data-ttu-id="9d5b6-280">ER ตรวจสอบว่านิพจน์การผูกมีเฉพาะแหล่งข้อมูลที่มีการตั้งค่าคอนฟิกในส่วนประกอบ ER ที่แก้ไขได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-280">ER checks whether the binding expressions contain only data sources that are configured in the editable ER component.</span></span> <span data-ttu-id="9d5b6-281">สำหรับการผูกทั้งหมดที่มีแหล่งข้อมูลที่ขาดหายไปในส่วนประกอบ ER ที่แก้ไขได้ เกิดข้อผิดพลาดในการตรวจสอบความถูกต้องในตัวออกแบบการดำเนินงาน ER หรือตัวออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-281">For every binding that contains a data source that is missing in the editable ER component, a validation error occurs in the ER Operations designer or the ER model-mapping designer.</span></span>

<span data-ttu-id="9d5b6-282">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-282">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-283">เริ่มต้นการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER และส่วนประกอบการแม็ปแบบจำลอง ER พร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-283">Start to configure the ER data model and the ER model-mapping components simultaneously.</span></span>
2. <span data-ttu-id="9d5b6-284">ในแผนภูมิรูปแบบข้อมูล ให้เพิ่มฟิลด์ที่ชื่อ **X** และเลือก **จำนวนเต็ม** เป็นชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d5b6-284">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![แผนภูมิรูปแบบข้อมูลของฟิลด์ X และข้อมูลจำนวนเต็มบนหน้ารูปแบบข้อมูล](./media/er-components-inspections-01.png)

3. <span data-ttu-id="9d5b6-286">ในบานหน้าต่างแหล่งข้อมูลการแม็ปแบบจำลอง เพิ่มแหล่งข้อมูลของชนิด **ฟิลด์ที่มีการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-286">In the model-mapping data sources pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="9d5b6-287">ตั้งชื่อแหล่งข้อมูล **Y** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `INTVALUE(100)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-287">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="9d5b6-288">ผูก **X** กับ **Y**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-288">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="9d5b6-289">ในตัวออกแบบการแม็ปแบบจำลอง ในบานหน้าต่างแหล่งข้อมูล ให้ลบแหล่งข้อมูล **Y**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-289">In the model-mapping designer, in the data sources pane, delete the **Y** data source.</span></span>
7. <span data-ttu-id="9d5b6-290">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-290">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![ตรวจสอบส่วนประกอบของการแม็ปแบบจำลอง ER ที่แก้ไขได้บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-03.gif)

8. <span data-ttu-id="9d5b6-292">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-292">Notice that a validation error occurs.</span></span> <span data-ttu-id="9d5b6-293">ข้อความระบุว่าการผูกกันของฟิลด์รูปแบบข้อมูล **X** มีพาธที่อ้างอิงถึงแหล่งข้อมูล **Y** แต่ไม่พบแหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-293">The message states that the binding of the **X** data model field contains the path that refers to the **Y** data source, but this data source isn't found.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-294">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-294">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-295">เลือก **ยกเลิกการผูก** เพื่อแก้ไขปัญหานี้โดยอัตโนมัติโดยการลบการผูกข้อมูลแหล่งข้อมูลที่ขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="9d5b6-295">Select **Unbind** to automatically fix this issue by removing the missing data source binding.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-296">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-296">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="9d5b6-297">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="9d5b6-297">Option 1</span></span>

<span data-ttu-id="9d5b6-298">ยกเลิกการผูกฟิลด์รูปแบบข้อมูล **X** เพื่อหยุดการอ้างอิงถึงแหล่งข้อมูล **Y** ที่ไม่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-298">Unbind the **X** data model field to stop referring to the nonexistent **Y** data source.</span></span>

#### <a name="option-2"></a><span data-ttu-id="9d5b6-299">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="9d5b6-299">Option 2</span></span>

<span data-ttu-id="9d5b6-300">ในบานหน้าต่างแหล่งข้อมูลของตัวออกแบบการแม็ปแบบจำลอง ER ให้เพิ่มแหล่งข้อมูล **Y** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-300">In the data sources pane of the ER model-mapping designer, add the **Y** data source again.</span></span>

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a><span data-ttu-id="9d5b6-301">ความสามารถในการปฏิบัติการนิพจน์กับฟังก์ชันตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-301">Executability of an expression with FILTER function</span></span>

<span data-ttu-id="9d5b6-302">ฟังก์ชัน ER [FILTER](er-functions-list-filter.md) ที่มีอยู่แล้วภายในใช้เพื่อเข้าถึงตารางของโปรแกรมประยุกต์ มุมมอง หรือเอนทิตีข้อมูลโดยการวางการเรียก SQL เดียวเพื่อให้ได้ข้อมูลที่จำเป็นในฐานะรายการของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-302">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="9d5b6-303">แหล่งข้อมูลของชนิด **รายการเรกคอร์ด** ถูกใช้เป็นอาร์กิวเมนต์ของฟังก์ชันนี้และระบุแหล่งที่มาของโปรแกรมประยุกต์สำหรับการโทร</span><span class="sxs-lookup"><span data-stu-id="9d5b6-303">A data source of the **Record list** type is used as an argument of this function and specifies the application source for the call.</span></span> <span data-ttu-id="9d5b6-304">ER ตรวจสอบว่าสามารถสร้างการสอบถาม SQL โดยตรงกับแหล่งข้อมูลที่อ้างถึงในฟังก์ชัน `FILTER` หรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-304">ER checks whether a direct SQL query can be established to a data source that is referred to in the `FILTER` function.</span></span> <span data-ttu-id="9d5b6-305">ถ้าไม่สามารถสร้างการสอบถามโดยตรงได้ เกิดข้อผิดพลาดในการตรวจสอบความถูกต้องในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-305">If a direct query can't be established, a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="9d5b6-306">ข้อความที่คุณได้รับแจ้งว่านิพจน์ ER ที่มีฟังก์ชัน `FILTER` ไม่สามารถรันในขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-306">The message that you receive states that the ER expression that includes the `FILTER` function can't be run at runtime.</span></span> 

<span data-ttu-id="9d5b6-307">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-307">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-308">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-308">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="9d5b6-309">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-309">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="9d5b6-310">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-310">Name the new data source **Vendor**.</span></span> <span data-ttu-id="9d5b6-311">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="9d5b6-311">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="9d5b6-312">เพิ่มแหล่งข้อมูลของชนิด **ฟิลด์ที่มีการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-312">Add a data source of the **Calculated field** type.</span></span>
5. <span data-ttu-id="9d5b6-313">ตั้งชื่อแหล่งข้อมูล **FilteredVendor** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `FILTER(Vendor, Vendor.AccountNum="US-101")`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-313">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="9d5b6-314">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้ บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** และตรวจสอบว่านิพจน์ `FILTER(Vendor, Vendor.AccountNum="US-101")` ในแหล่งข้อมูล **ผู้จัดจำหน่าย** สามารถสอบถามได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-314">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>
7. <span data-ttu-id="9d5b6-315">ปรับเปลี่ยนแหล่งข้อมูล **ผู้จัดจำหน่าย** โดยการเพิ่มฟิลด์ที่ซ้อนกันของชนิด **ฟิลด์ที่คำนวณได้** เพื่อให้ได้หมายเลขบัญชีผู้จัดจำหน่ายที่ตัด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-315">Modify the **Vendor** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="9d5b6-316">ตั้งชื่อฟิลด์ที่ซ้อนกัน **$AccNumber** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `TRIM(Vendor.AccountNum)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-316">Name the new nested field **$AccNumber**, and configure it so that it contains the expression `TRIM(Vendor.AccountNum)`.</span></span>
9. <span data-ttu-id="9d5b6-317">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้ บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** และตรวจสอบว่านิพจน์ `FILTER(Vendor, Vendor.AccountNum="US-101")` ในแหล่งข้อมูล **ผู้จัดจำหน่าย** สามารถสอบถามได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-317">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>

    ![การตรวจสอบนิพจน์สามารถสอบถามบนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-04.gif)

10. <span data-ttu-id="9d5b6-319">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง เนื่องจากแหล่งข้อมูล **ผู้จัดจำหน่าย** ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิด **ฟิลด์ที่คำนวณได้** ที่ไม่อนุญาตให้มีการแปลนิพจน์ของแหล่งข้อมูล **FilteredVendor** ที่คำสั่ง SQL โดยตรง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-319">Notice that a validation error occurs, because the **Vendor** data source contains a nested field of the **Calculated field** type that doesn't allow the expression of the **FilteredVendor** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="9d5b6-320">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้น ถ้าคุณละเว้นคำเตือนและเลือก **รัน** เพื่อรันรูปแบบที่มีการตั้งค่าคอนฟิกให้ใช้การแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-320">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model-mapping.</span></span>

![ข้อผิดพลาดรันไทม์ที่เกิดขึ้นเมื่อคุณรันการจัดรูปแบบที่แก้ไขได้บนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-322">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-322">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-323">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-323">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-324">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-324">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="9d5b6-325">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="9d5b6-325">Option 1</span></span>

<span data-ttu-id="9d5b6-326">แทนที่จะเพิ่มฟิลด์ที่ซ้อนกันของชนิด **ฟิลด์ที่คำนวณได้** ให้กับแหล่งข้อมูล **ผู้จัดจำหน่าย** ให้เพิ่มฟิลด์ **$AccNumber** ที่ซ้อนกันลงในแหล่งข้อมูล **FilteredVendor** และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `TRIM(FilteredVendor.AccountNum)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-326">Instead of adding a nested field of the **Calculated field** type to the **Vendor** data source, add the **$AccNumber** nested field to the **FilteredVendor** data source, and configure it so that it contains the expression `TRIM(FilteredVendor.AccountNum)`.</span></span> <span data-ttu-id="9d5b6-327">ด้วยวิธีนี้ นิพจน์ `FILTER(Vendor, Vendor.AccountNum="US-101")` สามารถรันในระดับ SQL และคำนวณฟิลด์ **$AccNumbe** ที่ซ้อนกันได้ภายหลัง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-327">In this way, the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="9d5b6-328">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="9d5b6-328">Option 2</span></span>

<span data-ttu-id="9d5b6-329">เปลี่ยนนิพจน์ของแหล่งข้อมูล **FilteredVendor** จาก `FILTER(Vendor, Vendor.AccountNum="US-101")` เป็น `WHERE(Vendor, Vendor.AccountNum="US-101")`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-329">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="9d5b6-330">เราไม่แนะนำให้คุณเปลี่ยนนิพจน์สำหรับตารางที่มีจำนวนมากของข้อมูล (ตารางธุรกรรม) เนื่องจากเรกคอร์ดทั้งหมดจะถูกนำมาใช้และการเลือกเรกคอร์ดที่ต้องการจะดำเนินการในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-330">We don't recommend that you change the expression for a table that has a large volume of data (transactional table), because all records will be fetched, and selection of the required records will be done in memory.</span></span> <span data-ttu-id="9d5b6-331">วิธีการนี้อาจทำให้ประสิทธิภาพการทำงานดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-331">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="9d5b6-332">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ฟังก์ชัน WHERE ER](er-functions-list-where.md)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-332">For more information, see [WHERE ER function](er-functions-list-where.md).</span></span>

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a><span data-ttu-id="9d5b6-333">ความสามารถในการปฏิบัติการของแหล่งข้อมูล GROUPBY</span><span class="sxs-lookup"><span data-stu-id="9d5b6-333">Executability of a GROUPBY data source</span></span>

<span data-ttu-id="9d5b6-334">แหล่งข้อมูล **GROUPBY** แบ่งผลลัพธ์การสอบถามเป็นกลุ่มของเรกคอร์ด โดยทั่วไปจะใช้เพื่อวัตถุประสงค์ในการทำการรวมหนึ่งรายการขึ้นไปในแต่ละกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-334">The **GROUPBY** data source divides the query result into groups of records, usually for the purpose of doing one or more aggregations on each group.</span></span> <span data-ttu-id="9d5b6-335">ทุกแหล่งข้อมูล **GROUPBY** สามารถตั้งค่าคอนฟิกได้เพื่อให้รันในระดับฐานข้อมูลหรือในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-335">Every **GROUPBY** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="9d5b6-336">เมื่อตั้งค่าคอนฟิกแหล่งข้อมูล **GROUPBY** เพื่อให้รันในระดับฐานข้อมูล ER จะตรวจสอบว่าสามารถสร้างการสอบถาม SQL โดยตรงกับแหล่งข้อมูลที่อ้างถึงในแหล่งข้อมูลนั้นได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-336">When a **GROUPBY** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to a data source that is referred to in that data source.</span></span> <span data-ttu-id="9d5b6-337">ถ้าไม่สามารถสร้างการสอบถามโดยตรงได้ เกิดข้อผิดพลาดในการตรวจสอบความถูกต้องในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-337">If a direct query can't be established, a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="9d5b6-338">ข้อความที่คุณได้รับระบุว่าแหล่งข้อมูล **GROUPBY** ที่ตั้งค่าคอนฟิกไม่สามารถรันในขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-338">The message that you receive states that the configured **GROUPBY** data source can't be run at runtime.</span></span>

<span data-ttu-id="9d5b6-339">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-339">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-340">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-340">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="9d5b6-341">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-341">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="9d5b6-342">ตั้งชื่อแหล่งข้อมูลใหม่ **Trans** ในฟิลด์ **ตาราง** ให้เลือก **VendTrans** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTrans</span><span class="sxs-lookup"><span data-stu-id="9d5b6-342">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="9d5b6-343">เพิ่มแหล่งข้อมูลของชนิด **จัดกลุ่มตาม**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-343">Add a data source of the **Group by** type.</span></span>
5. <span data-ttu-id="9d5b6-344">ตั้งชื่อแหล่งข้อมูลใหม่ **GroupedTrans** และตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-344">Name the new data source **GroupedTrans**, and configure it in the following way:</span></span>

    - <span data-ttu-id="9d5b6-345">เลือกแหล่งข้อมูล **Trans** เป็นแหล่งที่มาของเรกคอร์ดที่ควรมีการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-345">Select the **Trans** data source as the source of records that should be grouped.</span></span>
    - <span data-ttu-id="9d5b6-346">ในฟิลด์ **สถานที่การดำเนินการ** ให้เลือก **การสอบถาม** เพื่อระบุว่าคุณต้องการรันแหล่งข้อมูลนี้ในระดับฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d5b6-346">In the **Execution location** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![กำลังตั้งค่าคอนฟิกแหล่งข้อมูลบนหน้าแก้ไขพารามิเตอร์ 'จัดกลุ่มตาม'](./media/er-components-inspections-05a.gif)

6. <span data-ttu-id="9d5b6-348">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้ บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** และตรวจสอบว่าแหล่งข้อมูล **GroupedTrans** ที่ตั้งค่าคอนฟิกสามารถสอบถามได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-348">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>
7. <span data-ttu-id="9d5b6-349">ปรับเปลี่ยนแหล่งข้อมูล **Trans** โดยการเพิ่มฟิลด์ที่ซ้อนกันของชนิด **ฟิลด์ที่คำนวณได้** เพื่อให้ได้หมายเลขบัญชีผู้จัดจำหน่ายที่ตัด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-349">Modify the **Trans** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="9d5b6-350">ตั้งชื่อแหล่งข้อมูล **$AccNumber** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `TRIM(Trans.AccountNum)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-350">Name the new data source **$AccNumber**, and configure it so that it contains the expression `TRIM(Trans.AccountNum)`.</span></span>

    ![ตั้งค่าคอนฟิกแหล่งข้อมูล Trans ในหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-05a.png)

9. <span data-ttu-id="9d5b6-352">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้ บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** และตรวจสอบว่าแหล่งข้อมูล **GroupedTrans** ที่ตั้งค่าคอนฟิกสามารถสอบถามได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-352">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>

    ![ตรวจสอบความถูกต้องส่วนประกอบการแม็ปแบบจำลอง ER และตรวจสอบว่าแหล่งข้อมูล GroupedTrans สามารถสอบถามบนหน้าตัวออกแบบการแม็ปแบบจำลองได้หรือไม่](./media/er-components-inspections-05b.png)

10. <span data-ttu-id="9d5b6-354">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง เนื่องจากแหล่งข้อมูล **Trans** ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิด **ฟิลด์ที่คำนวณได้** ที่ไม่อนุญาตให้มีการเรียกใช้งานแหล่งข้อมูล **GroupedTrans** ที่คำสั่ง SQL โดยตรง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-354">Notice that a validation error occurs, because the **Trans** data source contains a nested field of the **Calculated field** type that doesn't allow the call for the **GroupedTrans** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="9d5b6-355">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้น ถ้าคุณละเว้นคำเตือนและเลือก **รัน** เพื่อรันรูปแบบที่มีการตั้งค่าคอนฟิกให้ใช้การแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-355">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model-mapping.</span></span>

![ข้อผิดพลาดรันไทม์ที่เกิดขึ้นเมื่อคำเตือนถูกละเว้นบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-357">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-357">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-358">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-358">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-359">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-359">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="9d5b6-360">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="9d5b6-360">Option 1</span></span>

<span data-ttu-id="9d5b6-361">แทนที่จะเพิ่มฟิลด์ที่ซ้อนกันของชนิด **ฟิลด์ที่คำนวณได้** ให้กับแหล่งข้อมูล **Trans** ให้เพิ่มฟิลด์ **$AccNumber** ที่ซ้อนกันสำหรับรายการ **GroupedTrans.lines** ของแหล่งข้อมูล **GroupedTrans** และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `TRIM(GroupedTrans.lines.AccountNum)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-361">Instead of adding a nested field of the **Calculated field** type to the **Trans** data source, add the **$AccNumber** nested field for the **GroupedTrans.lines** item of the **GroupedTrans** data source, and configure it so that it contains the expression `TRIM(GroupedTrans.lines.AccountNum)`.</span></span> <span data-ttu-id="9d5b6-362">ด้วยวิธีนี้ แหล่งข้อมูล **GroupedTrans** สามารถรันในระดับ SQL และคำนวณฟิลด์ **$AccNumber** ที่ซ้อนกันได้ภายหลัง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-362">In this way, the **GroupedTrans** data source can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="9d5b6-363">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="9d5b6-363">Option 2</span></span>

<span data-ttu-id="9d5b6-364">เปลี่ยนค่าของฟิลด์ **สถานที่การดำเนินการ** สำหรับแหล่งข้อมูล **GroupedTrans** จาก **การสอบถาม** เป็น **ในหน่วยความจำ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-364">Change the value of the **Execution location** field for the **GroupedTrans** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="9d5b6-365">เราไม่แนะนำให้คุณเปลี่ยนค่าสำหรับตารางที่มีจำนวนมากของข้อมูล (ตารางธุรกรรม) เนื่องจากเรกคอร์ดทั้งหมดจะถูกนำมาใช้ และการจัดกลุ่มและการรวมจะดำเนินการในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-365">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and grouping and aggregation will be done in memory.</span></span> <span data-ttu-id="9d5b6-366">วิธีการนี้อาจทำให้ประสิทธิภาพการทำงานดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-366">Therefore, this approach can cause poor performance.</span></span>

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a><span data-ttu-id="9d5b6-367">ความสามารถในการปฏิบัติการของแหล่งข้อมูล JOIN</span><span class="sxs-lookup"><span data-stu-id="9d5b6-367">Executability of a JOIN data source</span></span>

<span data-ttu-id="9d5b6-368">แหล่งข้อมูล [JOIN](er-join-data-sources.md) จะรวมเรกคอร์ดจากตารางฐานข้อมูลสองตารางขึ้นไป โดยขึ้นอยู่กับฟิลด์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-368">The [JOIN](er-join-data-sources.md) data source combines records from two or more database tables, based on related fields.</span></span> <span data-ttu-id="9d5b6-369">ทุกแหล่งข้อมูล **JOIN** สามารถตั้งค่าคอนฟิกได้เพื่อให้รันในระดับฐานข้อมูลหรือในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-369">Every **JOIN** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="9d5b6-370">เมื่อตั้งค่าคอนฟิกแหล่งข้อมูล **JOIN** เพื่อให้รันในระดับฐานข้อมูล ER จะตรวจสอบว่าสามารถสร้างการสอบถาม SQL โดยตรงกับแหล่งข้อมูลที่อ้างถึงในแหล่งข้อมูลนั้นได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-370">When a **JOIN** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to data sources that are referred to in that data source.</span></span> <span data-ttu-id="9d5b6-371">ถ้าไม่สามารถสร้างการสอบถาม SQL โดยตรงได้ด้วยอย่างน้อยหนึ่งแหล่งข้อมูลอ้างอิง เกิดข้อผิดพลาดในการตรวจสอบความถูกต้องในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-371">If a direct SQL query can't be established with at least one referenced data source, a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="9d5b6-372">ข้อความที่คุณได้รับระบุว่าแหล่งข้อมูล **JOIN** ที่ตั้งค่าคอนฟิกไม่สามารถรันในขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-372">The message that you receive states that the configured **JOIN** data source can't be run at runtime.</span></span>

<span data-ttu-id="9d5b6-373">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-373">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-374">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-374">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="9d5b6-375">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-375">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="9d5b6-376">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-376">Name the new data source **Vendor**.</span></span> <span data-ttu-id="9d5b6-377">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="9d5b6-377">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="9d5b6-378">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-378">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
5. <span data-ttu-id="9d5b6-379">ตั้งชื่อแหล่งข้อมูลใหม่ **Trans** ในฟิลด์ **ตาราง** ให้เลือก **VendTrans** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTrans</span><span class="sxs-lookup"><span data-stu-id="9d5b6-379">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
6. <span data-ttu-id="9d5b6-380">เพิ่มแหล่งข้อมูลของชนิด **ฟิลด์ที่คำนวณได้** เป็นฟิลด์ซ้อนกันของแหล่งข้อมูล **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-380">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
7. <span data-ttu-id="9d5b6-381">ตั้งชื่อแหล่งข้อมูล **FilteredTrans** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-381">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
8. <span data-ttu-id="9d5b6-382">เพิ่มแหล่งข้อมูลของชนิด **Join**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-382">Add a data source of the **Join** type.</span></span>
9. <span data-ttu-id="9d5b6-383">ตั้งชื่อแหล่งข้อมูลใหม่ **JoinedList** และตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-383">Name the new data source **JoinedList**, and configure it in the following way:</span></span>

    1. <span data-ttu-id="9d5b6-384">เพิ่มแหล่งข้อมูล **ผู้จัดจำหน่าย** เป็นชุดของเรกคอร์ดแรกที่จะรวม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-384">Add the **Vendor** data source as the first set of records to join.</span></span>
    2. <span data-ttu-id="9d5b6-385">เพิ่มแหล่งข้อมูล **Vendor.FilteredTrans** เป็นชุดของเรกคอร์ดที่สองที่จะรวม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-385">Add the **Vendor.FilteredTrans** data source as the second set of records to join.</span></span> <span data-ttu-id="9d5b6-386">เลือก **ภายใน** เป็นชนิด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-386">Select **INNER** as the type.</span></span>
    3. <span data-ttu-id="9d5b6-387">ในฟิลด์ **ดำเนินการ** ให้เลือก **การสอบถาม** เพื่อระบุว่าคุณต้องการรันแหล่งข้อมูลนี้ในระดับฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d5b6-387">In the **Execute** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![ตั้งค่าคอนฟิกแหล่งข้อมูลในหน้าตัวออกแบบ Join](./media/er-components-inspections-06a.gif)

10. <span data-ttu-id="9d5b6-389">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้ บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** และตรวจสอบว่าแหล่งข้อมูล **JoinedList** ที่ตั้งค่าคอนฟิกสามารถสอบถามได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-389">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>
11. <span data-ttu-id="9d5b6-390">เปลี่ยนนิพจน์ของแหล่งข้อมูล **Vendor.FilteredTrans** จาก `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` เป็น `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-390">Change the expression of the **Vendor.FilteredTrans** data source from `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` to `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
12. <span data-ttu-id="9d5b6-391">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้ บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** และตรวจสอบว่าแหล่งข้อมูล **JoinedList** ที่ตั้งค่าคอนฟิกสามารถสอบถามได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-391">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>

    ![ตรวจสอบความถูกต้องส่วนประกอบการแม็ปแบบจำลองที่แก้ไขได้ และตรวจสอบว่าแหล่งข้อมูล JoinedList สามารถสอบถามได้บนหน้าตัวออกแบบการแม็ปแบบจำลองหรือไม่](./media/er-components-inspections-06b.png)

13. <span data-ttu-id="9d5b6-393">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง เนื่องจากนิพจน์ของแหล่งข้อมูล **Vendor.FilteredTrans** ไม่สามารถแปลเป็นการเรียก SQL โดยตรงได้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-393">Notice that a validation error occurs, because the expression of the **Vendor.FilteredTrans** data source can't be translated to the direct SQL call.</span></span> <span data-ttu-id="9d5b6-394">นอกจากนี้ การเรียก SQL โดยตรงไม่อนุญาตการเรียกสำหรับแหล่งข้อมูล **JoinedList** ที่จะแปลเป็นคำสั่ง SQL โดยตรง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-394">Additionally, the direct SQL call doesn't allow the call for the **JoinedList** data source to be translated to the direct SQL statement.</span></span>

    ![ข้อผิดพลาดรันไทม์จากการตรวจสอบความถูกต้องของแหล่งข้อมูล JoinedList บนหน้าตัวออกแบบการแม็ปแบบจำลองล้มเหลว](./media/er-components-inspections-06c.png)

<span data-ttu-id="9d5b6-396">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้น ถ้าคุณละเว้นคำเตือนและเลือก **รัน** เพื่อรันรูปแบบที่มีการตั้งค่าคอนฟิกให้ใช้การแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-396">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model-mapping.</span></span>

![การรันรูปแบบที่แก้ไขได้บนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-398">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-398">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-399">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-399">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-400">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-400">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="9d5b6-401">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="9d5b6-401">Option 1</span></span>

<span data-ttu-id="9d5b6-402">เปลี่ยนนิพจน์ของแหล่งข้อมูล **Vendor.FilteredTrans** จาก `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` กลับเป็น `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` ตามคำเตือนที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-402">Change the expression of the **Vendor.FilteredTrans** data source from `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` back to `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, as the warning advised.</span></span>

![นพจน์ที่อัปเดตของแหล่งข้อมูลในหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a><span data-ttu-id="9d5b6-404">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="9d5b6-404">Option 2</span></span>

<span data-ttu-id="9d5b6-405">เปลี่ยนค่าของฟิลด์ **ดำเนินการ** สำหรับแหล่งข้อมูล **JoinedList** จาก **การสอบถาม** เป็น **ในหน่วยความจำ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-405">Change the value of the **Execute** field for the **JoinedList** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="9d5b6-406">เราไม่แนะนำให้คุณเปลี่ยนค่าสำหรับตารางที่มีจำนวนมากของข้อมูล (ตารางธุรกรรม) เนื่องจากเรกคอร์ดทั้งหมดจะถูกนำมาใช้ และการรวมจะเกิดขึ้นในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-406">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and the join occurs in memory.</span></span> <span data-ttu-id="9d5b6-407">วิธีการนี้อาจทำให้ประสิทธิภาพการทำงานดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-407">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="9d5b6-408">คำเตือนการตรวจสอบความถูกต้องจะแสดงขึ้นเพื่อแจ้งให้คุณทราบเกี่ยวกับความเสี่ยงนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-408">A validation warning is shown to inform you about this risk.</span></span>

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a><span data-ttu-id="9d5b6-409">ความเป็นที่ต้องการมากกว่าของฟังก์ชัน FILTER เทียบกับฟังก์ชัน WHERE</span><span class="sxs-lookup"><span data-stu-id="9d5b6-409">Preferability of FILTER vs WHERE function</span></span>

<span data-ttu-id="9d5b6-410">ฟังก์ชัน ER [FILTER](er-functions-list-filter.md) ที่มีอยู่แล้วภายในใช้เพื่อเข้าถึงตารางของโปรแกรมประยุกต์ มุมมอง หรือเอนทิตีข้อมูลโดยการวางการเรียก SQL เดียวเพื่อให้ได้ข้อมูลที่จำเป็นในฐานะรายการของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-410">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="9d5b6-411">ฟังก์ชัน [WHERE](er-functions-list-where.md) ค้นหาเรกคอร์ดทั้งหมดจากต้นทางที่กำหนดและบันทึกการเลือกในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-411">The [WHERE](er-functions-list-where.md) function fetches all records from the given source and does record selection in memory.</span></span> <span data-ttu-id="9d5b6-412">แหล่งข้อมูลของชนิด **รายการเรกคอร์ด** ถูกใช้เป็นอาร์กิวเมนต์ของทั้งสองฟังก์ชันและระบุแหล่งที่มาสำหรับการรับเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-412">A data source of the **Record list** type is used as an argument of both functions and specifies a source for getting records.</span></span> <span data-ttu-id="9d5b6-413">ER ตรวจสอบว่าสามารถสร้างการเรียกใช้ SQL โดยตรงกับแหล่งข้อมูลที่อ้างถึงในฟังก์ชัน **WHERE** หรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-413">ER checks whether a direct SQL call can be established to a data source that is referred to in the **WHERE** function.</span></span> <span data-ttu-id="9d5b6-414">ถ้าไม่สามารถสร้างการเรียกใช้โดยตรงได้ เกิดคำเตือนในการตรวจสอบความถูกต้องในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-414">If a direct call can be established, a validation warning occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="9d5b6-415">ข้อความที่คุณได้รับแนะนำให้คุณใช้ฟังก์ชัน **FILTER** แทนที่จะใช้ฟังก์ชัน **WHERE** ที่จะช่วยปรับปรุงประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-415">The message that you receive recommends that you use the **FILTER** function instead of the **WHERE** function to help improve efficiency.</span></span>

<span data-ttu-id="9d5b6-416">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-416">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-417">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-417">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="9d5b6-418">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-418">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="9d5b6-419">ตั้งชื่อแหล่งข้อมูลใหม่ **Trans** ในฟิลด์ **ตาราง** ให้เลือก **VendTrans** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTrans</span><span class="sxs-lookup"><span data-stu-id="9d5b6-419">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="9d5b6-420">เพิ่มแหล่งข้อมูลของชนิด **ฟิลด์ที่คำนวณได้** เป็นฟิลด์ซ้อนกันของแหล่งข้อมูล **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-420">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
5. <span data-ttu-id="9d5b6-421">ตั้งชื่อแหล่งข้อมูล **FilteredTrans** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `WHERE(Trans, Trans.AccountNum="US-101")`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-421">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `WHERE(Trans, Trans.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="9d5b6-422">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-422">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="9d5b6-423">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-423">Name the new data source **Vendor**.</span></span> <span data-ttu-id="9d5b6-424">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="9d5b6-424">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="9d5b6-425">เพิ่มแหล่งข้อมูลของชนิด **ฟิลด์ที่มีการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-425">Add a data source of the **Calculated field** type.</span></span>
9. <span data-ttu-id="9d5b6-426">ตั้งชื่อแหล่งข้อมูล **FilteredVendor** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `WHERE(Vendor, Vendor.AccountNum="US-101")`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-426">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span>
10. <span data-ttu-id="9d5b6-427">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-427">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![ตรวจสอบความถูกต้องเพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-07a.png)

11. <span data-ttu-id="9d5b6-429">โปรดสังเกตว่าคำเตือนการตรวจสอบความถูกต้องขอแนะนำให้คุณใช้ฟังก์ชัน **FILTER** แทนที่จะใช้ฟังก์ชัน **WHERE** สำหรับแหล่งข้อมูล **FilteredVendor** และ **FilteredTrans**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-429">Notice that validation warnings recommend that you use the **FILTER** function instead of the **WHERE** function for the **FilteredVendor** and **FilteredTrans** data sources.</span></span>

    ![คำเตือนการตรวจสอบความถูกต้องแนะนำฟังก์ชัน FILTER แทนที่จะใช้ฟังก์ชัน WHERE บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-431">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-431">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-432">เลือก **แก้ไข** เพื่อแทนที่ฟังก์ชัน **WHERE** โดยอัตโนมัติโดยฟังก์ชัน **FILTER** ในนิพจน์ของแหล่งข้อมูลทั้งหมดที่จะปรากฏในกริดบนแท็บ **คำเตือน** สำหรับชนิดของการตรวจสอบนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-432">Select **Fix** to automatically replace the **WHERE** function with the **FILTER** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="9d5b6-433">อีกทางหนึ่งคือ คุณสามารถเลือกแถวสำหรับคำเตือนเดียวในกริดแล้วเลือก **แก้ไขที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-433">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="9d5b6-434">ในกรณีนี้ นิพจน์จะถูกเปลี่ยนโดยอัตโนมัติในแหล่งข้อมูลที่ระบุไว้ในคำเตือนที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-434">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![เลือกแก้ไขเพื่อแทนที่ฟังก์ชัน WHERE ด้วยฟังก์ชัน FILTER โดยอัตโนมัติบนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-436">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-436">Manual resolution</span></span>

<span data-ttu-id="9d5b6-437">คุณสามารถปรับนิพจน์ของแหล่งข้อมูลทั้งหมดในกริดการตรวจสอบความถูกต้องด้วยตนเองได้ โดยแทนฟังก์ชัน **WHERE** ด้วยฟังก์ชัน **FILTER**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-437">You can manually adjust the expressions of all the data sources in the validation grid by replacing the **WHERE** function with the **FILTER** function.</span></span>

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a><span data-ttu-id="9d5b6-438">ความเป็นที่ต้องการมากกว่าของฟังก์ชัน ALLITEMSQUERY เทียบกับฟังก์ชัน ALLITEMS</span><span class="sxs-lookup"><span data-stu-id="9d5b6-438">Preferability of ALLITEMSQUERY vs ALLITEMS function</span></span>

<span data-ttu-id="9d5b6-439">ฟังก์ชัน ER [ALLITEMS](er-functions-list-allitems.md) และ [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ส่งคืนค่า **รายการเรกคอร์ด** ที่ทำให้แบนใหม่ที่ประกอบด้วยรายการของเรกคอร์ดที่แสดงถึงรายการทั้งหมดที่ตรงกับพาธที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-439">The built-in [ALLITEMS](er-functions-list-allitems.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ER functions return a flattened **Record list** value that consists of a list of records that represent all items that match the specified path.</span></span> <span data-ttu-id="9d5b6-440">ER ตรวจสอบว่าสามารถสร้างการเรียกใช้ SQL โดยตรงกับแหล่งข้อมูลที่อ้างถึงในฟังก์ชัน **ALLITEMS** หรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-440">ER checks whether a direct SQL call can be established to a data source that is referred to in the **ALLITEMS** function.</span></span> <span data-ttu-id="9d5b6-441">ถ้าไม่สามารถสร้างการเรียกใช้โดยตรงได้ เกิดคำเตือนในการตรวจสอบความถูกต้องในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-441">If a direct call can be established, a validation warning occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="9d5b6-442">ข้อความที่คุณได้รับแนะนำให้คุณใช้ฟังก์ชัน **ALLITEMSQUERYR** แทนที่จะใช้ฟังก์ชัน **ALLITEMS** ที่จะช่วยปรับปรุงประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-442">The message that you receive recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function to help improve efficiency.</span></span>

<span data-ttu-id="9d5b6-443">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-443">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-444">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-444">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="9d5b6-445">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-445">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="9d5b6-446">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-446">Name the new data source **Vendor**.</span></span> <span data-ttu-id="9d5b6-447">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="9d5b6-447">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="9d5b6-448">เพิ่มแหล่งข้อมูลแบบพารามิเตอร์ชนิด **ฟิลด์ที่มีการคำนวณ** เพิ่มรับเรกคอร์ดจากผู้จัดจำหน่ายหลายราย:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-448">Add a data source of the **Calculated field** type to get records for several vendors.</span></span>
5. <span data-ttu-id="9d5b6-449">ตั้งชื่อแหล่งข้อมูล **FilteredVendor** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-449">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.</span></span>
6. <span data-ttu-id="9d5b6-450">เพิ่มแหล่งข้อมูลแบบพารามิเตอร์ชนิด **ฟิลด์ที่มีการคำนวณ** เพิ่มรับธุรกรรมของผู้จัดจำหน่ายที่กรองแล้วทั้งหมด:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-450">Add a data source of the **Calculated field** type to get transactions of all filtered vendors.</span></span>
7. <span data-ttu-id="9d5b6-451">ตั้งชื่อแหล่งข้อมูล **FilteredVendorTrans** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-451">Name the new data source **FilteredVendorTrans**, and configure it so that it contains the expression `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.</span></span>
8. <span data-ttu-id="9d5b6-452">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-452">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![หน้าตัวออกแบบการแม็ปแบบจำลอง ปุ่มตรวจสอบความถูกต้อง](./media/er-components-inspections-08a.png)

9. <span data-ttu-id="9d5b6-454">โปรดสังเกตว่าเกิดคำเตือนในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-454">Notice that a validation warning occurs.</span></span> <span data-ttu-id="9d5b6-455">ข้อความแนะนำว่าคุณควรใช้ฟังก์ชัน **ALLITEMSQUERY** แทนที่จะใช้ฟังก์ชัน **ALLITEMS** สำหรับแหล่งข้อมูล **FilteredVendorTrans**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-455">The message recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function for the **FilteredVendorTrans** data source.</span></span>

    ![คำเตือนการตรวจสอบความถูกต้องให้ใช้ฟังก์ชัน ALLITEMSQUERY แทนฟังก์ชัน ALLITEMS บนคอมโพเนนต์การแม็ปแบบจำลอง ER บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-457">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-457">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-458">เลือก **แก้ไข** เพื่อแทนที่ฟังก์ชัน **ALLITEMS** โดยอัตโนมัติโดยฟังก์ชัน **ALLITEMSQUERY** ในนิพจน์ของแหล่งข้อมูลทั้งหมดที่จะปรากฏในกริดบนแท็บ **คำเตือน** สำหรับชนิดของการตรวจสอบนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-458">Select **Fix** to automatically replace the **ALLITEMS** function with the **ALLITEMSQUERY** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="9d5b6-459">อีกทางหนึ่งคือ คุณสามารถเลือกแถวสำหรับคำเตือนเดียวในกริดแล้วเลือก **แก้ไขที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-459">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="9d5b6-460">ในกรณีนี้ นิพจน์จะถูกเปลี่ยนโดยอัตโนมัติในแหล่งข้อมูลที่ระบุไว้ในคำเตือนที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-460">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![หน้าตัวออกแบบการแม็ปแบบจำลอง เลือกแก้ไขที่เลือก](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-462">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-462">Manual resolution</span></span>

<span data-ttu-id="9d5b6-463">คุณสามารถปรับนิพจน์ของแหล่งข้อมูลทั้งหมดที่กล่าวถึงในกริดการตรวจสอบความถูกต้องด้วยตนเองได้โดยแทนฟังก์ชัน **ALLITEMS** ด้วยฟังก์ชัน **ALLITEMSQUERY**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-463">You can manually adjust the expressions of all the data sources that are mentioned in the validation grid by replacing the **ALLITEMS** function with the **ALLITEMSQUERY** function.</span></span>

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a><span data-ttu-id="9d5b6-464">การพิจารณากรณีของรายการที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="9d5b6-464">Consideration of empty list cases</span></span>

<span data-ttu-id="9d5b6-465">คุณสามารถตั้งค่าคอนฟิกรูปแบบ ER หรือส่วนประกอบการแม็ปรูปแบบเพื่อให้ได้ค่าฟิลด์ของแหล่งข้อมูลของชนิด **รายการเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-465">You can configure your ER format or model-mapping component to get the field value of a data source of the **Record list** type.</span></span> <span data-ttu-id="9d5b6-466">ตรวจสอบว่าการออกแบบของคุณพิจารณากรณีที่มีแหล่งข้อมูลที่เรียกว่าไม่มีเรกคอร์ด (นั่นคือ ฟิลด์นี้ว่างเปล่า) เพื่อป้องกันไม่ให้เกิดข้อผิดพลาดรันไทม์เมื่อมีการนำค่ามาใช้จากฟิลด์ของเรกคอร์ดที่ไม่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-466">ER checks whether your design considers the case where a data source that is called contains no records (that is, it's empty), to prevent runtime errors when a value is fetched from a field of a nonexistent record.</span></span>

<span data-ttu-id="9d5b6-467">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-467">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-468">เริ่มต้นการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER การแม็ปแบบจำลอง ER และส่วนประกอบรูปแบบ ER พร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-468">Start to configure the ER data model, the ER model-mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="9d5b6-469">ในแผนภูมิรูปแบบข้อมูล ให้เพิ่มรายการรากที่ชื่อ **Root3**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-469">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="9d5b6-470">ปรับเปลี่ยนรายการ **Root3** โดยการเพิ่มรายการที่ซ้อนกันของชนิด **รายการเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-470">Modify the **Root3** item by adding a nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="9d5b6-471">ตั้งชื่อ **ผู้จัดจำหน่าย** รายการที่ซ้อนกันใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-471">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="9d5b6-472">ปรับเปลี่ยนสินค้า **ผู้จัดจำหน่าย** ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-472">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="9d5b6-473">เพิ่มฟิลด์ที่ซ้อนกันของชนิด **สตริง** และตั้งชื่อเป็น **Name**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-473">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="9d5b6-474">เพิ่มฟิลด์ที่ซ้อนกันของชนิด **สตริง** และ **AccountNumber** นั้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-474">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![กำลังเพิ่มฟิลด์ที่ซ้อนกันบนหน้ารูปแบบข้อมูล](./media/er-components-inspections-09a.png)

6. <span data-ttu-id="9d5b6-476">ในบานหน้าต่างแหล่งข้อมูลการแม็ปแบบจำลอง เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-476">In the model-mapping data sources pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="9d5b6-477">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-477">Name the new data source **Vendor**.</span></span> <span data-ttu-id="9d5b6-478">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="9d5b6-478">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="9d5b6-479">เพิ่มแหล่งข้อมูลของชนิด **ทั่วไป \\ พารามิเตอร์ป้อนเข้าของผู้ใช้** ในการค้นหาบัญชีผู้จัดจำหน่ายในกล่องโต้ตอบรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-479">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
9. <span data-ttu-id="9d5b6-480">ตั้งชื่อแหล่งข้อมูล **RequestedAccountNum** ใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-480">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="9d5b6-481">ในฟิลด์ **ป้ายชื่อ** ให้ป้อน **หมายเลขบัญชีของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-481">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="9d5b6-482">ในฟิลด์ **ชื่อชนิดของข้อมูลการดำเนินงาน** ให้เว้นค่าเริ่มต้น **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-482">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="9d5b6-483">เพิ่มแหล่งข้อมูลแบบพารามิเตอร์ชนิด **ฟิลด์ที่มีการคำนวณ** เพิ่มกรองผู้จัดจำหน่ายที่จำเป็น:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-483">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="9d5b6-484">ตั้งชื่อแหล่งข้อมูล **FilteredVendor** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-484">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="9d5b6-485">ผูกรายการแบบจำลองข้อมูลเพื่อตั้งค่าคอนฟิกแหล่งข้อมูลในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-485">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="9d5b6-486">ผูก **FilteredVendor** กับ **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-486">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="9d5b6-487">ผูก **FilteredVendor.AccountNum** กับ **Vendor.AccountNumber**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-487">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>
    - <span data-ttu-id="9d5b6-488">ผูก **FilteredVendor.'name()'** กับ **Vendor.Name**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-488">Bind **FilteredVendor.'name()'** to **Vendor.Name**.</span></span>

    ![ผูกรายการแบบจำลองข้อมูลในหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-09b.png)

13. <span data-ttu-id="9d5b6-490">ในแผนภูมิรูปแบบโครงสร้าง เพิ่มรายการต่อไปนี้เพื่อสร้างเอกสารขาออกในรูปแบบ XML ที่มีรายละเอียดผู้จัดจำหน่าย:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-490">In the format structure tree, add the following items to generate an outbound document in XML format that contains the vendor details:</span></span>

    1. <span data-ttu-id="9d5b6-491">เพิ่มองค์ประกอบ XML ของราก **ใบแจ้งยอด**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-491">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="9d5b6-492">สำหรับองค์ประกอบ XML **ใบแจ้งยอด** เพิ่มองค์ประกอบ XML **ฝ่าย** ที่ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-492">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="9d5b6-493">สำหรับองค์ประกอบ XML **ฝ่าย** เพิ่มแอททริบิวต์ XML ที่ซ้อนกันต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-493">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="9d5b6-494">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-494">Name</span></span>
        - <span data-ttu-id="9d5b6-495">AccountNum</span><span class="sxs-lookup"><span data-stu-id="9d5b6-495">AccountNum</span></span>

14. <span data-ttu-id="9d5b6-496">ผูกองค์ประกอบรูปแบบไปยังแหล่งข้อมูลที่ให้ไว้ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-496">Bind format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="9d5b6-497">ผูกองค์ประกอบรูปแบบ **คำสั่ง\\ฝ่าย\\ชื่อ** เข้ากับกับฟิลด์แหล่งข้อมูล **แบบจำลอง.ผู้จัดจำหน่าย.ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-497">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="9d5b6-498">ผูกองค์ประกอบรูปแบบ **คำสั่ง\\ฝ่าย\\AccountNum** เข้ากับกับฟิลด์แหล่งข้อมูล **แบบจำลอง.ผู้จัดจำหน่าย.หมายเลขบัญชี'**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-498">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="9d5b6-499">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของรูปแบบที่แก้ไขได้บนหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-499">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![ตรวจสอบความถูกต้องขององค์ประกอบรูปแบบที่คุณผูกกับแหล่งข้อมูลบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-09c.png)

16. <span data-ttu-id="9d5b6-501">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-501">Notice that a validation error occurs.</span></span> <span data-ttu-id="9d5b6-502">ข้อความระบุว่าอาจเกิดข้อผิดพลาดสำหรับส่วนประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย\\ชื่อ** และ **ใบแจ้งยอด\\ฝ่าย\\หมายเลขบัญชี** ในขณะรันไทม์ถ้ารายการ `model.Vendor` ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="9d5b6-502">The message states that an error might be thrown for the configured **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format components at runtime if the `model.Vendor` list is empty.</span></span>

    ![ข้อผิดพลาดการตรวจสอบความถูกต้องที่แจ้งข้อผิดพลาดที่อาจเกิดขึ้นสำหรับส่วนประกอบรูปแบบที่กำหนดไว้](./media/er-components-inspections-09d.png)

<span data-ttu-id="9d5b6-504">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้นถ้าคุณละเว้นคำเตือน เลือก **รัน** เพื่อรันรูปแบบ และเลือกหมายเลขบัญชีของผู้จัดจำหน่ายที่ไม่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-504">The following illustration shows the runtime error that occurs if you ignore the warning, select **Run** to run the format, and select the account number of a nonexistent vendor.</span></span> <span data-ttu-id="9d5b6-505">เนื่องจากไม่มีผู้จัดจำหน่ายที่ร้องขออยู่ รายการ `model.Vendor` จะว่างเปล่า (นั่นคือ จะไม่มีเรกคอร์ด)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-505">Because the requested vendor doesn't exist, the `model.Vendor` list will be empty (that is, it will contain no records).</span></span>

![ข้อผิดพลาดรันไทม์เนื่องจากเกิดข้อผิดพลาดในระหว่างการรันการแม็ปรูปแบบ](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-507">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-507">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-508">สำหรับแถวที่เลือกในกริดบนแท็บ **คำเตือน** คุณสามารถเลือก **ยกเลิกการผูก**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-508">For the selected row in the grid on the **Warnings** tab, you can select **Unbind**.</span></span> <span data-ttu-id="9d5b6-509">การผูกที่ชี้ไปในคอลัมน์ **พาธ** จะถูกลบออกจากองค์ประกอบรูปแบบโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-509">The binding that is pointed to in the **Path** column is automatically removed from the format elements.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-510">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-510">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="9d5b6-511">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="9d5b6-511">Option 1</span></span>

<span data-ttu-id="9d5b6-512">คุณสามารถผูกองค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย\\ชื่่อ** เข้ากับกับรายการแหล่งข้อมูล `model.Vendor`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-512">You can bind the **Statement\\Party\\Name** format element to the `model.Vendor` data source item.</span></span> <span data-ttu-id="9d5b6-513">เมื่อรันไทม์ การผูกข้อมูลนี้เรียกแหล่งข้อมูล `model.Vendor` เป็นอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="9d5b6-513">At runtime, this binding calls the `model.Vendor` data source first.</span></span> <span data-ttu-id="9d5b6-514">เมื่อ `model.Vendor` ส่งคืนรายการเรกคอร์ดที่ว่างเปล่า จะไม่มีการรันองค์ประกอบรูปแบบซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-514">When `model.Vendor` returns an empty record list, the nested format elements aren't run.</span></span> <span data-ttu-id="9d5b6-515">ดังนั้น จึงไม่มีคำเตือนการตรวจสอบความถูกต้องสำหรับการตั้งค่าคอนฟิกรูปแบบนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-515">Therefore, no validation warnings occur for this format configuration.</span></span>

![ผูกองค์ประกอบรูปแบบกับรายการแหล่งข้อมูลบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a><span data-ttu-id="9d5b6-517">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="9d5b6-517">Option 2</span></span>

<span data-ttu-id="9d5b6-518">เปลี่ยนการผูกขององค์ประกอบรูปแบบ **คำสั่ง\\ฝ่าย\\ชื่อ** จาก `model.Vendor.Name` เป็น `FIRSTORNULL(model.Vendor).Name`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-518">Change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `FIRSTORNULL(model.Vendor).Name`.</span></span> <span data-ttu-id="9d5b6-519">เงื่อนไขการรวมที่มีการอัปเดตจะแปลงเรกคอร์ดแรกของแหล่งข้อมูล `model.Vendor` ของชนิด **รายการเรกคอร์ด** ไปยังแหล่งข้อมูลใหม่ของชนิด **เรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-519">The updated binding conditionally converts the first record of the `model.Vendor` data source of the **Record list** type to a new data source of the **Record** type.</span></span> <span data-ttu-id="9d5b6-520">แหล่งข้อมูลใหม่นี้ประกอบด้วยชุดของฟิลด์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-520">This new data source contains the same set of fields.</span></span>

- <span data-ttu-id="9d5b6-521">ถ้ามีเรกคอร์ดอย่างน้อยหนึ่งเรกคอร์ดในแหล่งข้อมูล `model.Vendor` ฟิลด์ของเรกคอร์ดดังกล่าวจะถูกเติมด้วยค่าของฟิลด์ของเรกคอร์ดแรกของแหล่งข้อมูล `model.Vendor`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-521">If at least one record is available in the `model.Vendor` data source, the fields of that record are filled with the values of the fields of the first record of the `model.Vendor` data source.</span></span> <span data-ttu-id="9d5b6-522">ในกรณีนี้ การผูกข้อมูลที่อัปเดตแล้วส่งคืนชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9d5b6-522">In this case, the updated binding returns the vendor name.</span></span>
- <span data-ttu-id="9d5b6-523">มิฉะนั้น ฟิลด์ทั้งหมดของเรกคอร์ดที่สร้างขึ้นจะถูกเติมด้วยค่าเริ่มต้นสำหรับชนิดข้อมูลของฟิลด์นั้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-523">Otherwise, every field of the record that is created is filled with the default value for the data type of that field.</span></span> <span data-ttu-id="9d5b6-524">ในกรณีนี้ มีการส่งคืนสตริงที่ว่างเปล่าเป็นค่าเริ่มต้นของชนิดข้อมูล **สตริง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-524">In this case, the blank string is returned as the default value of the **String** data type.</span></span>

<span data-ttu-id="9d5b6-525">ดังนั้น จึงไม่มีคำเตือนการตรวจสอบความถูกต้องสำหรับองค์ประกอบรูปแบบ **คำสั่ง\\ฝ่าย\\ชื่อ** เมื่อผูกกับนิพจน์ `FIRSTORNULL(model.Vendor).Name`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-525">Therefore, no validation warnings occur for the **Statement\\Party\\Name** format element when it's bound to the `FIRSTORNULL(model.Vendor).Name` expression.</span></span>

![การผูกที่เปลี่ยนแปลงแก้ไขคำเตือนการตรวจสอบความถูกต้องบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a><span data-ttu-id="9d5b6-527">ตัวเลือก 3</span><span class="sxs-lookup"><span data-stu-id="9d5b6-527">Option 3</span></span>

<span data-ttu-id="9d5b6-528">ถ้าคุณต้องการระบุข้อมูลที่ป้อนในเอกสารที่สร้างขึ้นอย่างชัดแจ้งเมื่อแหล่งข้อมูล `model.Vendor` ของชนิด **รายการเรกคอร์ด** ส่งคืนไม่มีเรกคอร์ด (ข้อความที่ **ไม่มีอยู่** ในตัวอย่างนี้) ให้เปลี่ยนการผูกขององค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย\\ชื่อ** จาก `model.Vendor.Name` เป็น `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-528">If you want to explicitly specify the data that is entered in a generated document when the `model.Vendor` data source of the **Record list** type returns no records (the text **Not available** in this example), change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`.</span></span> <span data-ttu-id="9d5b6-529">และคุณสามารถใช้นิพจน์ `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-529">You can also use the expression `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.</span></span>

### <a name="additional-consideration"></a><a id="i9a"></a><span data-ttu-id="9d5b6-530">การพิจารณาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-530">Additional consideration</span></span>

<span data-ttu-id="9d5b6-531">การตรวจสอบยังเตือนคุณเกี่ยวกับปัญหาที่อาจเกิดขึ้นอีกประการหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-531">The inspection also warns you about another potential issue.</span></span> <span data-ttu-id="9d5b6-532">ตามค่าเริ่มต้น ในขณะที่คุณผูกองค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย\\ชื่อ** และ **ใบแจ้งยอด\\ฝ่าย\\เลขที่บัญชี** ให้กับฟิลด์ที่เหมาะสมของแหล่งข้อมูล `model.Vendor` ของชนิด **รายการเรกคอร์ด** จะมีการรันการผูกเหล่านั้นและจะใช้ค่าของฟิลด์ที่เหมาะสมของเรกคอร์ดแรกของแหล่งข้อมูล `model.Vendor` ถ้ารายการดังกล่าวไม่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="9d5b6-532">By default, as you bind the **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format elements to the appropriate fields of the `model.Vendor` data source of the **Record list** type, those bindings will be run and will take the values of the appropriate fields of the first record of the `model.Vendor` data source, if that list isn't empty.</span></span>

<span data-ttu-id="9d5b6-533">เนื่องจากคุณไม่ได้ผูกองค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย** กับแหล่งข้อมูล `model.Vendor` องค์ประกอบ **ใบแจ้งยอด\\ฝ่าย** จะไม่มีการวนซ้ำสำหรับเรกคอร์ดทั้งหมดของแหล่งข้อมูล `model.Vendor` ในระหว่างการดำเนินการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-533">Because you haven't bound the **Statement\\Party** format element with the `model.Vendor` data source, the **Statement\\Party** element won't be iterated for every record of the `model.Vendor` data source during format execution.</span></span> <span data-ttu-id="9d5b6-534">เอกสารที่สร้างขึ้นจะถูกเติมด้วยข้อมูลจากเรกคอร์ดหนึ่งของรายการเรกคอร์ดเท่านั้น ถ้ารายการดังกล่าวประกอบด้วยเรกคอร์ดหลายเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-534">Instead, a generated document will be filled with information from only the first record of the record list, if that list contains multiple records.</span></span> <span data-ttu-id="9d5b6-535">การทำเช่นนี้อาจเป็นปัญหาถ้ารูปแบบนี้มีไว้เพื่อให้กรอกเอกสารที่สร้างขึ้นด้วยข้อมูลเกี่ยวกับผู้จัดจำหน่ายทั้งหมดจากแหล่งข้อมูล `model.Vendor`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-535">Therefore, there might be an issue if the format is intended to fill a generated document with information about all vendors from the `model.Vendor` data source.</span></span> <span data-ttu-id="9d5b6-536">เมื่อต้องการแก้ไขปัญหานี้ ให้ผูกองค์ประกอบ **ใบแจ้งยอด\\ฝ่าย** กับแหล่งข้อมูล `model.Vendor`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-536">To fix this issue, bind the **Statement\\Party** element with the `model.Vendor` data source.</span></span>

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a><span data-ttu-id="9d5b6-537">ความสามารถในการปฏิบัติการนิพจน์กับฟังก์ชันตัวกรอง (การแคช)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-537">Executability of an expression with FILTER function (caching)</span></span>

<span data-ttu-id="9d5b6-538">หลายฟังก์ชัน ER ภายใน รวมถึง [FILTER](er-functions-list-filter.md) และ [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ใช้เพื่อเข้าถึงตารางของโปรแกรมประยุกต์ มุมมอง หรือเอนทิตีข้อมูลโดยการวางการเรียก SQL เดียวเพื่อให้ได้ข้อมูลที่จำเป็นในฐานะรายการของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="9d5b6-538">Several built-in ER functions, including [FILTER](er-functions-list-filter.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md), are used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="9d5b6-539">แหล่งข้อมูลของชนิด **รายการเรกคอร์ด** ถูกใช้เป็นอาร์กิวเมนต์ของแต่ละฟังก์ชันเหล่านี้และระบุแหล่งที่มาของโปรแกรมประยุกต์สำหรับการโทร</span><span class="sxs-lookup"><span data-stu-id="9d5b6-539">A data source of the **Record list** type is used as an argument of each of these functions and specifies an application source for the call.</span></span> <span data-ttu-id="9d5b6-540">ER ตรวจสอบว่าสามารถสร้างการเรียกใช้ SQL โดยตรงกับแหล่งข้อมูลที่อ้างถึงในหนึ่งในฟังก์ชันเหล่านี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-540">ER checks whether a direct SQL call can be established to a data source that is referred to in one of these functions.</span></span> <span data-ttu-id="9d5b6-541">ถ้าไม่สามารถสร้างการเรียกใช้โดยตรงได้ เนื่องจากแหล่งข้อมูลอ้างอิงถูกทำเครื่องหมายเป็น [แคช](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace) เกิดข้อผิดพลาดในการตรวจสอบความถูกต้องในโปรแกรมออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-541">If a direct call can't be established because the data source was marked as [cached](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="9d5b6-542">ข้อความที่คุณได้รับแจ้งว่านิพจน์ ER ที่มีหนึ่งในฟังก์ชันเหล่านี้ไม่สามารถรันในขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-542">The message that you receive states that the ER expression that contains one of these functions can't be run at runtime.</span></span>

<span data-ttu-id="9d5b6-543">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-543">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-544">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-544">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="9d5b6-545">เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-545">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="9d5b6-546">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-546">Name the new data source **Vendor**.</span></span> <span data-ttu-id="9d5b6-547">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="9d5b6-547">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="9d5b6-548">เพิ่มแหล่งข้อมูลของชนิด **ทั่วไป \\ พารามิเตอร์ป้อนเข้าของผู้ใช้** ในการค้นหาบัญชีผู้จัดจำหน่ายในกล่องโต้ตอบรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-548">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
5. <span data-ttu-id="9d5b6-549">ตั้งชื่อแหล่งข้อมูล **RequestedAccountNum** ใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-549">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="9d5b6-550">ในฟิลด์ **ป้ายชื่อ** ให้ป้อน **หมายเลขบัญชีของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-550">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="9d5b6-551">ในฟิลด์ **ชื่อชนิดของข้อมูลการดำเนินงาน** ให้เว้นค่าเริ่มต้น **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-551">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
6. <span data-ttu-id="9d5b6-552">เพิ่มแหล่งข้อมูลแบบพารามิเตอร์ชนิด **ฟิลด์ที่มีการคำนวณ** เพิ่มกรองผู้จัดจำหน่ายที่จำเป็น:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-552">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
7. <span data-ttu-id="9d5b6-553">ตั้งชื่อแหล่งข้อมูล **FilteredVendor** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-553">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
8. <span data-ttu-id="9d5b6-554">ทำเครื่องหมายแหล่งข้อมูล **ผู้จัดจำหน่าย** ที่ตั้งค่าคอนฟิกเป็นแคช</span><span class="sxs-lookup"><span data-stu-id="9d5b6-554">Mark the configured **Vendor** data source as cached.</span></span>

    ![ตั้งค่าส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-10a.gif)

9. <span data-ttu-id="9d5b6-556">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของการแม็ปแบบจำลองที่แก้ไขได้บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-556">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![ตรวจสอบความถูกต้องของฟังก์ชันตัวกรองที่ใช้กับแหล่งข้อมูลของผู้จัดจำหน่ายแคชบนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-10a.png)

10. <span data-ttu-id="9d5b6-558">โปรดสังเกตว่าเกิดข้อผิดพลาดในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-558">Notice that a validation error occurs.</span></span> <span data-ttu-id="9d5b6-559">ข้อความแจ้งว่าฟังก์ชัน **FILTER** ไม่สามารถนำไปใช้แหล่งข้อมูล **ผู้จัดจำหน่าย** ที่ถูกเก็บไว้ในแคช</span><span class="sxs-lookup"><span data-stu-id="9d5b6-559">The message states that the **FILTER** function can't be applied to the cached **Vendor** data source.</span></span>

<span data-ttu-id="9d5b6-560">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้นถ้าคุณละเว้นคำเตือนและเลือก **รัน** เพื่อรันรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-560">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![ข้อผิดพลาดรันไทม์ที่เกิดขึ้นระหว่างการรันการแม็ปรูปแบบบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-562">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-562">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-563">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-563">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-564">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-564">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="9d5b6-565">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="9d5b6-565">Option 1</span></span>

<span data-ttu-id="9d5b6-566">ลบแฟล็ก **แคช** จากแหล่งข้อมูล **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-566">Remove the **Cache** flag from the **Vendor** data source.</span></span> <span data-ttu-id="9d5b6-567">แหล่งข้อมูล **FilteredVendor** จะกลายเป็นสามารถดำเนินการได้ แต่แหล่งข้อมูล **ผู้จัดจำหน่าย** ที่อ้างถึงในตาราง VendTable จะสามารถเข้าถึงได้ทุกครั้งที่มีการเรียกแหล่งข้อมูล **FilteredVendor**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-567">The **FilteredVendor** data source will then become executable, but the **Vendor** data source that is referred to in the VendTable table will be accessed every time that the **FilteredVendor** data source is called.</span></span>

#### <a name="option-2"></a><span data-ttu-id="9d5b6-568">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="9d5b6-568">Option 2</span></span>

<span data-ttu-id="9d5b6-569">เปลี่ยนนิพจน์ของแหล่งข้อมูล **FilteredVendor** จาก `FILTER(Vendor, Vendor.AccountNum="US-101")` เป็น `WHERE(Vendor, Vendor.AccountNum="US-101")`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-569">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="9d5b6-570">ในกรณีนี้ แหล่งข้อมูล **ผู้จัดจำหน่าย** ที่มีการอ้างอิงในตาราง VendTable จะมีการเข้าถึงในระหว่างการเรียกแรกของแหล่งข้อมูล **ผู้จัดจำหน่าย** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-570">In this case, the **Vendor** data source that is referred to in the VendTable table will be accessed only during the first call of the **Vendor** data source.</span></span> <span data-ttu-id="9d5b6-571">อย่างไรก็ตาม การเลือกเรกคอร์ดจะมีการดำเนินการในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-571">However, the selection of records will be done in memory.</span></span> <span data-ttu-id="9d5b6-572">วิธีการนี้อาจทำให้ประสิทธิภาพการทำงานดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-572">Therefore, this approach can cause poor performance.</span></span>

## <a name="missing-binding"></a><a id="i11"></a><span data-ttu-id="9d5b6-573">ขาดการผูกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d5b6-573">Missing binding</span></span>

<span data-ttu-id="9d5b6-574">เมื่อคุณตั้งค่าคอนฟิกส่วนประกอบรูปแบบ ER แบบจำลองข้อมูลพื้นฐาน ER จะถูกนำเสนอเป็นแหล่งข้อมูลเริ่มต้นสำหรับรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-574">When you configure an ER format component, the base ER data model is offered as a default data source for the ER format.</span></span> <span data-ttu-id="9d5b6-575">เมื่อรันรูปแบบ ER ที่ตั้งค่าคอนฟิก [การแม็ปแบบจำลองเริ่มต้น](er-country-dependent-model-mapping.md) สำหรับแบบจำลองพื้นฐานจะใช้ในการกรอกรูปแบบข้อมูลด้วยข้อมูลของโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-575">When the configured ER format is run, the [default model mapping](er-country-dependent-model-mapping.md) for the base model is used to fill the data model with application data.</span></span> <span data-ttu-id="9d5b6-576">ตัวออกแบบรูปแบบ ER แสดงคำเตือนถ้าคุณผูกองค์ประกอบรูปแบบไปยังรายการรูปแบบข้อมูลที่ไม่ได้ผูกกับแหล่งข้อมูลใด ๆ ในการแม็ปแบบจำลองที่เลือกไว้เป็นการแม็ปแบบจำลองเริ่มต้นสำหรับรูปแบบที่แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-576">The ER format designer shows a warning if you bind a format element to a data model item that isn't bound to any data source in the model-mapping that is currently selected as the default model-mapping for the editable format.</span></span> <span data-ttu-id="9d5b6-577">ไม่สามารถรันการผูกข้อมูลชนิดนี้เมื่อรันไทม์ได้ เนื่องจากรูปแบบที่รันไม่สามารถกรอกข้อมูลองค์ประกอบที่ผูกกับข้อมูลของโปรแกรมประยุกต์ได้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-577">This type of binding can't be run at runtime, because the format that runs can't fill a bound element with application data.</span></span> <span data-ttu-id="9d5b6-578">ข้อผิดพลาดเกิดขึ้นขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-578">Therefore, an error occurs at runtime.</span></span>

<span data-ttu-id="9d5b6-579">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-579">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-580">เริ่มต้นการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER การแม็ปแบบจำลอง ER และส่วนประกอบรูปแบบ ER พร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-580">Start to configure the ER data model, the ER model-mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="9d5b6-581">ในแผนภูมิรูปแบบข้อมูล ให้เพิ่มรายการรากที่ชื่อ **Root3**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-581">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="9d5b6-582">ปรับเปลี่ยนรายการ **Root3** โดยการเพิ่มรายการที่ซ้อนกันใหม่ของชนิด **รายการเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-582">Modify the **Root3** item by adding a new nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="9d5b6-583">ตั้งชื่อ **ผู้จัดจำหน่าย** รายการที่ซ้อนกันใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-583">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="9d5b6-584">ปรับเปลี่ยนสินค้า **ผู้จัดจำหน่าย** ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-584">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="9d5b6-585">เพิ่มฟิลด์ที่ซ้อนกันของชนิด **สตริง** และตั้งชื่อเป็น **Name**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-585">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="9d5b6-586">เพิ่มฟิลด์ที่ซ้อนกันของชนิด **สตริง** และ **AccountNumber** นั้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-586">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![เพิ่มฟิลด์ที่ซ้อนกันให้กับสินค้าของผู้จัดจำหน่ายบนหน้ารูปแบบข้อมูล](./media/er-components-inspections-11a.png)

6. <span data-ttu-id="9d5b6-588">ในบานหน้าต่างแหล่งข้อมูลการแม็ปแบบจำลอง เพิ่มแหล่งข้อมูลของชนิด **Dynamics 365 for Operations \\ เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-588">In the model-mapping data sources pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="9d5b6-589">ตั้งชื่อแหล่งข้อมูล **ผู้จัดจำหน่าย** ใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-589">Name the new data source **Vendor**.</span></span> <span data-ttu-id="9d5b6-590">ในฟิลด์ **ตาราง** ให้เลือก **VendTable** เพื่อระบุว่าแหล่งข้อมูลนี้จะร้องขอตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="9d5b6-590">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="9d5b6-591">เพิ่มแหล่งข้อมูลของชนิด **ทั่วไป \\ พารามิเตอร์ป้อนเข้าของผู้ใช้** ในการสอบถามบัญชีผู้จัดจำหน่ายในกล่องโต้ตอบรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-591">Add a data source of the **General \\ User input parameter** type to inquire about a vendor account in the runtime dialog box.</span></span>
<span data-ttu-id="9d5b6-592">9 ตั้งชื่อแหล่งข้อมูล **RequestedAccountNum** ใหม่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-592">9 Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="9d5b6-593">ในฟิลด์ **ป้ายชื่อ** ให้ป้อน **หมายเลขบัญชีของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-593">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="9d5b6-594">ในฟิลด์ **ชื่อชนิดของข้อมูลการดำเนินงาน** ให้เว้นค่าเริ่มต้น **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-594">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="9d5b6-595">เพิ่มแหล่งข้อมูลแบบพารามิเตอร์ชนิด **ฟิลด์ที่มีการคำนวณ** เพิ่มกรองผู้จัดจำหน่ายที่จำเป็น:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-595">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="9d5b6-596">ตั้งชื่อแหล่งข้อมูล **FilteredVendor** ใหม่และตั้งค่าคอนฟิกเพื่อให้มีนิพจน์ `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-596">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="9d5b6-597">ผูกรายการแบบจำลองข้อมูลเพื่อตั้งค่าคอนฟิกแหล่งข้อมูลในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-597">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="9d5b6-598">ผูก **FilteredVendor** กับ **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-598">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="9d5b6-599">ผูก **FilteredVendor.AccountNum** กับ **Vendor.AccountNumber**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-599">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9d5b6-600">ฟิลด์รูปแบบข้อมูล **ผู้จัดจำหน่าย.ชื่อ** ยังคงไม่ถูกผูกไว้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-600">The **Vendor.Name** data model field remains unbound.</span></span>

    ![รายการรูปแบบข้อมูลที่ผูกกับแหล่งข้อมูลที่ตั้งค่าคอนฟิกและรายการรูปแบบข้อมูลบนหน้าตัวออกแบบการแม็ปแบบจำลอง](./media/er-components-inspections-11b.png)

13. <span data-ttu-id="9d5b6-602">ในแผนภูมิรูปแบบโครงสร้าง เพิ่มรายการต่อไปนี้เพื่อสร้างเอกสารขาออกในรูปแบบ XML ที่มีรายละเอียดของผู้จัดจำหน่ายที่สอบถาม:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-602">In the format structure tree, add the following items to generate an outbound document in XML format that contains the details of the vendors that are inquired about:</span></span>

    1. <span data-ttu-id="9d5b6-603">เพิ่มองค์ประกอบ XML ของราก **ใบแจ้งยอด**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-603">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="9d5b6-604">สำหรับองค์ประกอบ XML **ใบแจ้งยอด** เพิ่มองค์ประกอบ XML **ฝ่าย** ที่ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-604">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="9d5b6-605">สำหรับองค์ประกอบ XML **ฝ่าย** เพิ่มแอททริบิวต์ XML ที่ซ้อนกันต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-605">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="9d5b6-606">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-606">Name</span></span>
        - <span data-ttu-id="9d5b6-607">AccountNum</span><span class="sxs-lookup"><span data-stu-id="9d5b6-607">AccountNum</span></span>

14. <span data-ttu-id="9d5b6-608">ผูกองค์ประกอบรูปแบบไปยังแหล่งข้อมูลที่ให้ไว้ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-608">Bind the format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="9d5b6-609">ผูกองค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย** เข้ากับกับรายการแหล่งข้อมูล `model.Vendor`</span><span class="sxs-lookup"><span data-stu-id="9d5b6-609">Bind the **Statement\\Party** format element to the `model.Vendor` data source item.</span></span>
    - <span data-ttu-id="9d5b6-610">ผูกองค์ประกอบรูปแบบ **คำสั่ง\\ฝ่าย\\ชื่อ** เข้ากับกับฟิลด์แหล่งข้อมูล **แบบจำลอง.ผู้จัดจำหน่าย.ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-610">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="9d5b6-611">ผูกองค์ประกอบรูปแบบ **คำสั่ง\\ฝ่าย\\AccountNum** เข้ากับกับฟิลด์แหล่งข้อมูล **แบบจำลอง.ผู้จัดจำหน่าย.หมายเลขบัญชี'**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-611">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="9d5b6-612">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของรูปแบบที่แก้ไขได้บนหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-612">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![การตรวจสอบความถูกต้องส่วนประกอบรูปแบบ ER บนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-11c.png)

16. <span data-ttu-id="9d5b6-614">โปรดสังเกตว่าเกิดคำเตือนในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-614">Notice that a validation warning occurs.</span></span> <span data-ttu-id="9d5b6-615">ข้อความระบุว่าฟิลด์แหล่งข้อมูล **แบบจำลอง.ผู้จัดจำหน่าย.ชื่อ** ไม่ได้ผูกกับแหล่งข้อมูลใด ๆ ในการแม็ปแบบจำลองที่มีการตั้งค่าคอนฟิกให้ใช้โดยรูปแบบนี้</span><span class="sxs-lookup"><span data-stu-id="9d5b6-615">The message states that the **model.Vendor.Name** data source field isn't bound to any data source in the model-mapping that is configured to be used by the format.</span></span> <span data-ttu-id="9d5b6-616">ดังนั้น องค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย\\ชื่อ** อาจไม่ได้รับการกรอกข้อมูลในขณะรันไทม์ และข้อยกเว้นรันไทม์อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-616">Therefore, the **Statement\\Party\\Name** format element might not be filled at runtime, and a runtime exception might occur.</span></span>

    ![การตรวจสอบความถูกต้องส่วนประกอบรูปแบบ ER บนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-11d.png)

<span data-ttu-id="9d5b6-618">ภาพประกอบต่อไปนี้แสดงข้อผิดพลาดรันไทม์ที่เกิดขึ้นถ้าคุณละเว้นคำเตือนและเลือก **รัน** เพื่อรันรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-618">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![รันรูปแบบที่แก้ไขได้บนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-620">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-620">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-621">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-621">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-622">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-622">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="9d5b6-623">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="9d5b6-623">Option 1</span></span>

<span data-ttu-id="9d5b6-624">ปรับเปลี่ยนการแม็ปแบบจำลองที่ตั้งค่าคอนฟิกโดยเพิ่มการรวมสำหรับฟิลด์แหล่งข้อมูล **model.Vendor.Name**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-624">Modify the configured model-mapping by adding a binding for the **model.Vendor.Name** data source field.</span></span>

#### <a name="option-2"></a><span data-ttu-id="9d5b6-625">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="9d5b6-625">Option 2</span></span>

<span data-ttu-id="9d5b6-626">ปรับเปลี่ยนรูปแบบที่ตั้งค่าคอนฟิกด้วยการลบการรวมสำหรับองค์ประกอบรูปแบบ **ใบแจ้งยอด\\ฝ่าย\\ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-626">Modify the configured format by removing a binding for the **Statement\\Party\\Name** format element.</span></span>

## <a name="not-linked-template"></a><a id="i12"></a><span data-ttu-id="9d5b6-627">แม่แบบไม่มีการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-627">Not linked template</span></span>

<span data-ttu-id="9d5b6-628">เมื่อคุณตั้งค่าคอนฟิกส่วนประกอบของรูปแบบ ER [ด้วยตนเอง](er-fillable-excel.md#manual-entry) เพื่อใช้แม่แบบเพื่อสร้างเอกสารขาออก คุณต้องเพิ่มองค์ประกอบ **Excel\\ไฟล์** ด้วยตนเอง เพิ่มแม่แบบที่จำเป็นต้องใช้เป็นสิ่งที่แนบมากับส่วนประกอบที่แก้ไขได้ และเลือกสิ่งที่แนบไว้ในองค์ประกอบ **Excel\\ไฟล์** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-628">When you [manually](er-fillable-excel.md#manual-entry) configure an ER format component to use a template to generate an outbound document, you must manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="9d5b6-629">ด้วยวิธีนี้ คุณบ่งชี้ว่าองค์ประกอบเพิ่มเติมจะเติมแม่แบบที่เลือกเมื่อรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-629">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="9d5b6-630">เมื่อคุณตั้งค่าคอนฟิกรุ่นของส่วนประกอบรูปแบบใน [สถานะ](general-electronic-reporting.md#component-versioning) **แบบร่าง** คุณอาจเพิ่มหลายแม่แบบไปยังส่วนประกอบที่แก้ไข แล้วเลือกแต่ละแม่แบบในองค์ประกอบ **Excel\\ไฟล์** เพื่อรันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-630">When you configure a format component version in **Draft** [status](general-electronic-reporting.md#component-versioning), you might add several templates to the editable component, and then select each template in the **Excel\\File** element to run the ER format.</span></span> <span data-ttu-id="9d5b6-631">ด้วยวิธีนี้ คุณสามารถดูวิธีการกรอกข้อมูลแม่แบบที่แตกต่างกันในขณะทำงาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-631">In this way, you can see how different templates are filled at runtime.</span></span> <span data-ttu-id="9d5b6-632">ถ้าคุณมีแม่แบบที่ไม่ได้เลือกไว้ในองค์ประกอบ **Excel\\ไฟล์** ใด ๆ ตัวออกแบบรูปแบบ ER จะแจ้งเตือนคุณว่าแม่แบบจะถูกลบออกจากรุ่นของส่วนประกอบรูปแบบ ER ที่สามารถแก้ไขได้เมื่อสถานะมีการเปลี่ยนแปลงจาก **แบบร่าง** เป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-632">If you have templates that aren't selected in any **Excel\\File** elements, the ER format designer warns you that those templates will be deleted from the editable ER format component version when its status is changed from **Draft** to **Completed**.</span></span>

<span data-ttu-id="9d5b6-633">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-633">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-634">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-634">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="9d5b6-635">ในแผนภูมิโครงสร้างรูปแบบ ให้เพิ่มองค์ประกอบ **Excel\\ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-635">In the format structure tree, add the **Excel\\File** element.</span></span>
3. <span data-ttu-id="9d5b6-636">สำหรับองค์ประกอบ **Excel\\ไฟล์** ที่คุณเพิ่งเพิ่ม ให้เพิ่มไฟล์สมุดงาน Excel **A.xlsx** เป็นไฟล์แนบ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-636">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="9d5b6-637">ใช้ชนิดเอกสารที่มีการตั้งค่าคอนฟิกใน [พารามิเตอร์ ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) เพื่อระบุการจัดเก็บแม่แบบรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-637">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>
4. <span data-ttu-id="9d5b6-638">สำหรับองค์ประกอบ **Excel\\ไฟล์** ให้เพิ่มไฟล์สมุดงาน Excel อื่น **B.xlsx** เป็นไฟล์แนบ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-638">For the **Excel\\File** element, add another Excel workbook file, **B.xlsx**, as an attachment.</span></span> <span data-ttu-id="9d5b6-639">ใช้ชนิดเอกสารเดียวกันกับที่ใช้สำหรับไฟล์สมุดงาน A</span><span class="sxs-lookup"><span data-stu-id="9d5b6-639">Use the same document type that is used for workbook file A.</span></span>
5. <span data-ttu-id="9d5b6-640">ในองค์ประกอบ **Excel\\ไฟล์** ให้เลือกไฟล์สมุดงาน A</span><span class="sxs-lookup"><span data-stu-id="9d5b6-640">In the **Excel\\File** element, select workbook file A.</span></span>
6. <span data-ttu-id="9d5b6-641">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของรูปแบบที่แก้ไขได้บนหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-641">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![การตรวจสอบความถูกต้องของส่วนประกอบของรูปแบบที่แก้ไขได้ของไฟล์สมุดงานในหน้าการจัดรูปแบบตัวออกแบบ](./media/er-components-inspections-12a.gif)

7. <span data-ttu-id="9d5b6-643">โปรดสังเกตว่าเกิดคำเตือนในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-643">Notice that a validation warning occurs.</span></span> <span data-ttu-id="9d5b6-644">ข้อความระบุว่าไฟล์สมุดงาน **B.xlsx** ไม่ได้เชื่อมโยงกับส่วนประกอบใด ๆ และจะถูกลบออกหลังจากสถานะของรุ่นการตั้งค่าคอนฟิกมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-644">The message states that workbook file **B.xlsx** isn't linked to any components, and that it will be removed after the status of the configuration version is changed.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-645">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-645">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-646">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-646">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-647">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-647">Manual resolution</span></span>

<span data-ttu-id="9d5b6-648">ปรับเปลี่ยนรูปแบบที่ตั้งค่าคอนฟิกด้วยการลบแม่แบบทั้งหมดที่ไม่ได้เชื่อมโยงกับองค์ประกอบ **Excel\\ไฟล์** ใดๆ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-648">Modify the configured format by removing all templates that aren't linked to any **Excel\\File** element.</span></span>

## <a name="not-synced-format"></a><a id="i13"></a><span data-ttu-id="9d5b6-649">รูปแบบที่ไม่ได้ซิงค์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-649">Not synced format</span></span>

<span data-ttu-id="9d5b6-650">เมื่อคุณ [ตั้งค่าคอนฟิก](er-fillable-excel.md) ส่วนประกอบของรูปแบบ ER เพื่อใช้แม่แบบ Excel เพื่อสร้างเอกสารขาออก คุณสามารถเพิ่มองค์ประกอบ **Excel\\ไฟล์** ด้วยตนเอง เพิ่มแม่แบบที่จำเป็นต้องใช้เป็นสิ่งที่แนบมากับส่วนประกอบที่แก้ไขได้ และเลือกสิ่งที่แนบไว้ในองค์ประกอบ **Excel\\ไฟล์** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-650">When you [configure](er-fillable-excel.md) an ER format component to use an Excel template to generate an outbound document, you can manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="9d5b6-651">ด้วยวิธีนี้ คุณบ่งชี้ว่าองค์ประกอบเพิ่มเติมจะเติมแม่แบบที่เลือกเมื่อรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9d5b6-651">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="9d5b6-652">เนื่องจากแม่แบบ Excel ที่เพิ่มมีการออกแบบภายนอก รูปแบบ ER ที่สามารถแก้ไขได้อาจประกอบด้วยชื่อ Excel ที่ขาดหายไปจากแม่แบบที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-652">Because the added Excel template has been externally designed, the editable ER format might contain Excel names that are missing from the added template.</span></span> <span data-ttu-id="9d5b6-653">ตัวออกแบบรูปแบบ ER เตือนคุณเกี่ยวกับความไม่สอดคล้องกันระหว่างคุณสมบัติต่าง ๆ ของรูปแบบ ER ซึ่งอ้างอิงถึงชื่อที่ไม่ได้รวมอยู่ในแม่แบบ Excel ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-653">The ER format designer warns you about any inconsistencies between the properties of the ER format elements that refer to names that aren't included in the added Excel template.</span></span>

<span data-ttu-id="9d5b6-654">ขั้นตอนต่อไปนี้แสดงวิธีการที่ปัญหานี้อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d5b6-654">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="9d5b6-655">เริ่มต้นการตั้งค่าคอนฟิกส่วนประกอบรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-655">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="9d5b6-656">ในแผนภูมิโครงสร้างรูปแบบ ให้เพิ่ม **รายงาน** องค์ประกอบ **Excel\\ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-656">In the format structure tree, add the **Excel\\File** element **Report**.</span></span>
3. <span data-ttu-id="9d5b6-657">สำหรับองค์ประกอบ **Excel\\ไฟล์** ที่คุณเพิ่งเพิ่ม ให้เพิ่มไฟล์สมุดงาน Excel **A.xlsx** เป็นไฟล์แนบ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-657">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="9d5b6-658">ใช้ชนิดเอกสารที่มีการตั้งค่าคอนฟิกใน [พารามิเตอร์ ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) เพื่อระบุการจัดเก็บแม่แบบรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-658">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="9d5b6-659">ตรวจสอบให้แน่ใจว่าสมุดงาน Excel ที่เพิ่มเข้ามาไม่มีชื่อ **ReportTitle**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-659">Make sure that the added Excel workbook doesn't contain the name **ReportTitle**.</span></span>

4. <span data-ttu-id="9d5b6-660">เพิ่ม **ชื่อ** องค์ประกอบ **Excel\\เซลล์** เป็นองค์ประกอบซ้อนกันขององค์ประกอบ **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-660">Add the following **Excel\\Cell** element **Title** as the nested element of the **Report** element.</span></span> <span data-ttu-id="9d5b6-661">ในฟิลด์ **ช่วงของ Excel** ให้ป้อน **ReportTitle**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-661">In the **Excel range** field, enter **ReportTitle**.</span></span>
5. <span data-ttu-id="9d5b6-662">เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบส่วนประกอบของรูปแบบที่แก้ไขได้บนหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-662">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![ตรวจสอบความถูกต้ององค์ประกอบและองค์ประกอบที่ซ้อนกันบนหน้าตัวออกแบบรูปแบบ](./media/er-components-inspections-13a.png)

6. <span data-ttu-id="9d5b6-664">โปรดสังเกตว่าเกิดคำเตือนในการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-664">Notice that a validation warning occurs.</span></span> <span data-ttu-id="9d5b6-665">ข้อความระบุว่าชื่อ **ReportTitle** ไม่มีอยู่บนแผ่นงาน **Sheet1** ของแม่แบบ Excel ที่คุณกำลังใช้อยู่</span><span class="sxs-lookup"><span data-stu-id="9d5b6-665">The message states that the name **ReportTitle** doesn't exist on sheet **Sheet1** of the Excel template that you're using.</span></span>

    ![คำเตือนการตรวจสอบความถูกต้องว่าชื่อ ReportTitle ไม่มีอยู่บน Sheet1 ของแม่แบบ Excel](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="9d5b6-667">การแก้ปัญหาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-667">Automatic resolution</span></span>

<span data-ttu-id="9d5b6-668">ไม่มีตัวเลือกในการแก้ไขปัญหานี้โดยอัตโนมัติพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9d5b6-668">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="9d5b6-669">การแก้ปัญหาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9d5b6-669">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="9d5b6-670">ตัวเลือก 1</span><span class="sxs-lookup"><span data-stu-id="9d5b6-670">Option 1</span></span>

<span data-ttu-id="9d5b6-671">ปรับเปลี่ยนรูปแบบที่ตั้งค่าคอนฟิกด้วยการลบองค์ประกอบทั้งหมดที่อ้างอิงถึงชื่อ Excel ที่ขาดหายไปจากแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-671">Modify the configured format by removing all elements that refer to Excel names that are missing from the template.</span></span>

#### <a name="option-2"></a><span data-ttu-id="9d5b6-672">ตัวเลือก 2</span><span class="sxs-lookup"><span data-stu-id="9d5b6-672">Option 2</span></span>

<span data-ttu-id="9d5b6-673">[อัพเดต](er-fillable-excel.md#template-import) รูปปแบบ ER ที่แก้ไขได้โดยการนำเข้าแม่แบบ Excel</span><span class="sxs-lookup"><span data-stu-id="9d5b6-673">[Update](er-fillable-excel.md#template-import) the editable ER format by importing an Excel template.</span></span> <span data-ttu-id="9d5b6-674">โครงสร้างของรูปแบบ ER ที่สามารถแก้ไขได้จะ [ถูกซิงค์](modify-electronic-reporting-format-reapply-excel-template.md) กับโครงสร้างของแม่แบบ Excel ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="9d5b6-674">The structure of the editable ER format will be [synced](modify-electronic-reporting-format-reapply-excel-template.md) with the structure of the imported Excel template.</span></span>

### <a name="additional-consideration"></a><span data-ttu-id="9d5b6-675">การพิจารณาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-675">Additional consideration</span></span>

<span data-ttu-id="9d5b6-676">เมื่อต้องการเรียนรู้วิธีการซิงค์โครงสร้างรูปแบบกับแม่แบบ ER ในโปรแกรมแก้ไขแม่แบบของ [การจัดการเอกสารทางธุรกิจ](er-business-document-management.md) ให้ดูที่ [ปรับปรุงโครงสร้างของแม่แบบเอกสารธุรกิจ](er-bdm-update-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-676">To learn how the format structure can be synced with an ER template in the template editor of [Business document management](er-business-document-management.md), see [Update the structure of a business document template](er-bdm-update-structure.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d5b6-677">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9d5b6-677">Additional resources</span></span>

[<span data-ttu-id="9d5b6-678">ฟังก์ชัน ALLITEMS ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-678">ALLITEMS ER function</span></span>](er-functions-list-allitems.md)

[<span data-ttu-id="9d5b6-679">ฟังก์ชัน ALLITEMSQUERY ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-679">ALLITEMSQUERY ER function</span></span>](er-functions-list-allitemsquery.md)

[<span data-ttu-id="9d5b6-680">ฟังก์ชัน INT64VALUE ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-680">INT64VALUE ER function</span></span>](er-functions-conversion-int64value.md)

[<span data-ttu-id="9d5b6-681">ฟังก์ชัน INTVALUE ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-681">INTVALUE ER function</span></span>](er-functions-conversion-intvalue.md)

[<span data-ttu-id="9d5b6-682">ฟังก์ชัน FILTER ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-682">FILTER ER function</span></span>](er-functions-list-filter.md)

[<span data-ttu-id="9d5b6-683">ฟังก์ชั่น WHERE ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-683">WHERE ER function</span></span>](er-functions-list-where.md)

[<span data-ttu-id="9d5b6-684">ใช้แหล่งข้อมูล JOIN เพื่อดึงข้อมูลจากหลายตารางโปรแกรมประยุกต์ในการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="9d5b6-684">Use JOIN data sources to get data from multiple application tables in ER model mappings</span></span>](er-join-data-sources.md)

[<span data-ttu-id="9d5b6-685">ติดตามการดำเนินการของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-685">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="9d5b6-686">ภาพรวมของการจัดการเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="9d5b6-686">Business document management overview</span></span>](er-business-document-management.md)
