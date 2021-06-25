---
title: การสนับสนุนบอร์ดการโอนย้ายคัมบังสำหรับเครื่องสแกนบาร์โค้ด
description: บอร์ดการโอนย้ายคัมบังสนับสนุนสแกนเนอร์อินพุตจากเครื่องสแกนบาร์โค้ดราคาให้เป็น การเลือก เริ่มต้น เสร็จสมบูรณ์ และลบงานคัมบัง
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c48c4737c260004ea44109cfb2a0478a3e8653cc
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190075"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="00f9e-103">การสนับสนุนบอร์ดการโอนย้ายคัมบังสำหรับเครื่องสแกนบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="00f9e-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00f9e-104">บอร์ดการโอนย้ายคัมบังสนับสนุนสแกนเนอร์อินพุตจากเครื่องสแกนบาร์โค้ดราคาให้เป็น การเลือก เริ่มต้น เสร็จสมบูรณ์ และลบงานคัมบัง</span><span class="sxs-lookup"><span data-stu-id="00f9e-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

## <a name="registration-modes"></a><span data-ttu-id="00f9e-105">โหมดการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="00f9e-105">Registration modes</span></span>

<span data-ttu-id="00f9e-106">ในแท็บด่วน **การลงทะเบียนสแกนเนอร์** คุณสามารถเลือกโหมดการลงทะเบียน ซึ่งควบคุมการดำเนินการเมื่อคุณสแกนหมายเลขบัตรคัมบัง หรือพิมพ์หมายเลขในฟิลด์หมายเลขบัตรคัมบังด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="00f9e-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="00f9e-107">ตั้งค่าโหมดการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="00f9e-107">Set registration mode</span></span> | <span data-ttu-id="00f9e-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="00f9e-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00f9e-109">เริ่ม</span><span class="sxs-lookup"><span data-stu-id="00f9e-109">Start</span></span>                 | <span data-ttu-id="00f9e-110">ลงทะเบียนงานการโอนย้ายคัมบังอยู่ในระหว่างดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="00f9e-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="00f9e-111">เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="00f9e-111">Complete</span></span>              | <span data-ttu-id="00f9e-112">ลงทะเบียนงานการโอนย้ายคัมบังเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="00f9e-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="00f9e-113">ว่าง</span><span class="sxs-lookup"><span data-stu-id="00f9e-113">Empty</span></span>                 | <span data-ttu-id="00f9e-114">ลงทะเบียนหน่วยจัดการวัสดุที่อ้างอิงโดยบัตรคัมบังเป็นว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="00f9e-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="00f9e-115">เลือก</span><span class="sxs-lookup"><span data-stu-id="00f9e-115">Select</span></span>                | <span data-ttu-id="00f9e-116">ลงทะเบียนหมายเลขบัตรคัมบังและเลือกงานที่อ้างอิงในรายการคัมบังโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="00f9e-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
## <a name="registration-mode-select"></a><span data-ttu-id="00f9e-117">โหมดการลงทะเบียน เลือก</span><span class="sxs-lookup"><span data-stu-id="00f9e-117">Registration mode Select</span></span>

<span data-ttu-id="00f9e-118">เมื่อคุณใช้ตัวอ่านบาร์โค้ดเพื่อเลือกงาน โหมดการแสดงผลของการเปลี่ยนแปลงบอร์ดคัมบัง</span><span class="sxs-lookup"><span data-stu-id="00f9e-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="00f9e-119">ในโหมดนี้ เงื่อนไขต่อไปนี้นำไปใช้:</span><span class="sxs-lookup"><span data-stu-id="00f9e-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="00f9e-120">เฉพาะงานคัมบังที่สแกนจะถูกแสดง</span><span class="sxs-lookup"><span data-stu-id="00f9e-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="00f9e-121">รายละเอียดเกี่ยวกับงานที่เลือกจะแสดงในแท็บด่วน **รายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="00f9e-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="00f9e-122">แท็บด่วน **ข้อความ** แสดงข้อความสำหรับงานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="00f9e-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="00f9e-123">คุณสามารถเปลี่ยนสถานะของงาน โดยใช้ฟังก์ชันที่พร้อมใช้งานบน บานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="00f9e-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="00f9e-124">บอร์ดการโอนย้ายคัมบังดำเนินต่อไปเพื่อแสดงเฉพาะงานเดียวระหว่างช่วงเวลานี้</span><span class="sxs-lookup"><span data-stu-id="00f9e-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="00f9e-125">คุณสามารถอัพเดทข้อมูลในรายการงานด้วยตนเอง โดยการคลิก  **รีเฟรช** (Shift + F5) บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="00f9e-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="00f9e-126">หลังจากที่คุณรีเฟรชข้อมูล ผลลัพธ์แบบเต็มสำหรับตัวกรองงานถูกแสดงผลอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="00f9e-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="00f9e-127">สถานะงานและการดำเนินการที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="00f9e-127">Job status and possible actions</span></span>
<span data-ttu-id="00f9e-128">สถานะของงานที่เลือกและสถานะของงานโยงใด ๆ สำหรับคัมบังเหตุการณ์ กำหนดว่าคุณสามารถดำเนินงานต่อไปได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="00f9e-129">ตารางต่อไปนี้แสดงข้อมูลเกี่ยวกับสถานะและงานเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="00f9e-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="00f9e-130">สถานะซึ่งพร้อมใช้งานสำหรับงาน หรือสำหรับหน่วยจัดการวัสดุที่ถูกอ้างอิงโดยงาน</span><span class="sxs-lookup"><span data-stu-id="00f9e-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="00f9e-131">งานแต่ละงานที่คุณสามารถดำเนินการสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="00f9e-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00f9e-132">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="00f9e-132">Job type</span></span></th>
<th><span data-ttu-id="00f9e-133">สถานะงานหรือสถานะหน่วยจัดการวัสดุ</span><span class="sxs-lookup"><span data-stu-id="00f9e-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="00f9e-134">อัพเดตรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="00f9e-134">Update picking list</span></span></th>
<th><span data-ttu-id="00f9e-135">เริ่ม</span><span class="sxs-lookup"><span data-stu-id="00f9e-135">Start</span></span></th>
<th><span data-ttu-id="00f9e-136">อัพเดตการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="00f9e-136">Update registration</span></span></th>
<th><span data-ttu-id="00f9e-137">เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="00f9e-137">Complete</span></span></th>
<th><span data-ttu-id="00f9e-138">ว่าง</span><span class="sxs-lookup"><span data-stu-id="00f9e-138">Empty</span></span></th>
<th><span data-ttu-id="00f9e-139">สร้างคัมบังเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="00f9e-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00f9e-140">การโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="00f9e-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="00f9e-141">ไม่ได้วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="00f9e-141">Not planned</span></span></li>
<li><span data-ttu-id="00f9e-142">ไม่มีงานโยง หรืองานโยงที่เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="00f9e-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="00f9e-143">ใช่</span><span class="sxs-lookup"><span data-stu-id="00f9e-143">Yes</span></span></td>
<td><span data-ttu-id="00f9e-144">ใช่</span><span class="sxs-lookup"><span data-stu-id="00f9e-144">Yes</span></span></td>
<td><span data-ttu-id="00f9e-145">ใช่</span><span class="sxs-lookup"><span data-stu-id="00f9e-145">Yes</span></span></td>
<td><span data-ttu-id="00f9e-146">ใช่</span><span class="sxs-lookup"><span data-stu-id="00f9e-146">Yes</span></span></td>
<td><span data-ttu-id="00f9e-147">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-147">No</span></span></td>
<td><span data-ttu-id="00f9e-148">ใช่</span><span class="sxs-lookup"><span data-stu-id="00f9e-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00f9e-149">การโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="00f9e-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="00f9e-150">ไม่ได้วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="00f9e-150">Not planned</span></span></li>
<li><span data-ttu-id="00f9e-151">งานโยงยังไม่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="00f9e-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="00f9e-152">ใช่</span><span class="sxs-lookup"><span data-stu-id="00f9e-152">Yes</span></span></td>
<td><span data-ttu-id="00f9e-153">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-153">No</span></span></td>
<td><span data-ttu-id="00f9e-154">ใช่</span><span class="sxs-lookup"><span data-stu-id="00f9e-154">Yes</span></span></td>
<td><span data-ttu-id="00f9e-155">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-155">No</span></span></td>
<td><span data-ttu-id="00f9e-156">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-156">No</span></span></td>
<td><span data-ttu-id="00f9e-157">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00f9e-158">การโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="00f9e-158">Transfer</span></span></td>
<td><span data-ttu-id="00f9e-159">อยู่ระหว่างดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="00f9e-159">In progress</span></span></td>
<td><span data-ttu-id="00f9e-160">ใช่</span><span class="sxs-lookup"><span data-stu-id="00f9e-160">Yes</span></span></td>
<td><span data-ttu-id="00f9e-161">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-161">No</span></span></td>
<td><span data-ttu-id="00f9e-162">ใช่</span><span class="sxs-lookup"><span data-stu-id="00f9e-162">Yes</span></span></td>
<td><span data-ttu-id="00f9e-163">ใช่</span><span class="sxs-lookup"><span data-stu-id="00f9e-163">Yes</span></span></td>
<td><span data-ttu-id="00f9e-164">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-164">No</span></span></td>
<td><span data-ttu-id="00f9e-165">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00f9e-166">การโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="00f9e-166">Transfer</span></span></td>
<td><span data-ttu-id="00f9e-167">เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="00f9e-167">Completed</span></span></td>
<td><span data-ttu-id="00f9e-168">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-168">No</span></span></td>
<td><span data-ttu-id="00f9e-169">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-169">No</span></span></td>
<td><span data-ttu-id="00f9e-170">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-170">No</span></span></td>
<td><span data-ttu-id="00f9e-171">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-171">No</span></span></td>
<td><span data-ttu-id="00f9e-172">ใช่</span><span class="sxs-lookup"><span data-stu-id="00f9e-172">Yes</span></span></td>
<td><span data-ttu-id="00f9e-173">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00f9e-174">การโอนย้ายหรือกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="00f9e-174">Transfer or process</span></span></td>
<td><span data-ttu-id="00f9e-175">ว่าง</span><span class="sxs-lookup"><span data-stu-id="00f9e-175">Empty</span></span></td>
<td><span data-ttu-id="00f9e-176">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-176">No</span></span></td>
<td><span data-ttu-id="00f9e-177">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-177">No</span></span></td>
<td><span data-ttu-id="00f9e-178">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-178">No</span></span></td>
<td><span data-ttu-id="00f9e-179">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-179">No</span></span></td>
<td><span data-ttu-id="00f9e-180">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-180">No</span></span></td>
<td><span data-ttu-id="00f9e-181">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00f9e-182">การโอนย้ายหรือกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="00f9e-182">Transfer or process</span></span></td>
<td><span data-ttu-id="00f9e-183">บัตรคัมบังไม่ถูกพบ</span><span class="sxs-lookup"><span data-stu-id="00f9e-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="00f9e-184">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-184">No</span></span></td>
<td><span data-ttu-id="00f9e-185">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-185">No</span></span></td>
<td><span data-ttu-id="00f9e-186">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-186">No</span></span></td>
<td><span data-ttu-id="00f9e-187">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-187">No</span></span></td>
<td><span data-ttu-id="00f9e-188">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-188">No</span></span></td>
<td><span data-ttu-id="00f9e-189">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00f9e-190">การโอนย้ายหรือกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="00f9e-190">Transfer or process</span></span></td>
<td><span data-ttu-id="00f9e-191">บัตรคัมบังถูกพบ แต่บัตรคัมบังไม่ถูกกำหนดให้กับคัมบัง</span><span class="sxs-lookup"><span data-stu-id="00f9e-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="00f9e-192">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-192">No</span></span></td>
<td><span data-ttu-id="00f9e-193">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-193">No</span></span></td>
<td><span data-ttu-id="00f9e-194">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-194">No</span></span></td>
<td><span data-ttu-id="00f9e-195">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-195">No</span></span></td>
<td><span data-ttu-id="00f9e-196">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-196">No</span></span></td>
<td><span data-ttu-id="00f9e-197">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00f9e-198">ดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="00f9e-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="00f9e-199">ไม่ได้วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="00f9e-199">Not planned</span></span></li>
<li><span data-ttu-id="00f9e-200">จัดเตรียมไว้</span><span class="sxs-lookup"><span data-stu-id="00f9e-200">Prepared</span></span></li>
<li><span data-ttu-id="00f9e-201">อยู่ระหว่างดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="00f9e-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="00f9e-202">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-202">No</span></span></td>
<td><span data-ttu-id="00f9e-203">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-203">No</span></span></td>
<td><span data-ttu-id="00f9e-204">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-204">No</span></span></td>
<td><span data-ttu-id="00f9e-205">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-205">No</span></span></td>
<td><span data-ttu-id="00f9e-206">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-206">No</span></span></td>
<td><span data-ttu-id="00f9e-207">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00f9e-208">ดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="00f9e-208">Process</span></span></td>
<td><span data-ttu-id="00f9e-209">เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="00f9e-209">Completed</span></span></td>
<td><span data-ttu-id="00f9e-210">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-210">No</span></span></td>
<td><span data-ttu-id="00f9e-211">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-211">No</span></span></td>
<td><span data-ttu-id="00f9e-212">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-212">No</span></span></td>
<td><span data-ttu-id="00f9e-213">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-213">No</span></span></td>
<td><span data-ttu-id="00f9e-214">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-214">No</span></span></td>
<td><span data-ttu-id="00f9e-215">ไม่</span><span class="sxs-lookup"><span data-stu-id="00f9e-215">No</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]