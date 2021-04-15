---
title: กำหนดรายการงานให้กับร้านค้าหรือพนักงาน
description: หัวข้อนี้จะอธิบายถึงวิธีการกำหนดรายการงานให้กับร้านค้าหรือพนักงานใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0c4f028367c894c54392963ffc4f6a0f0c04c03a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795272"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="e7a47-103">กำหนดรายการงานให้กับร้านค้าหรือพนักงาน</span><span class="sxs-lookup"><span data-stu-id="e7a47-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7a47-104">หัวข้อนี้จะอธิบายถึงวิธีการกำหนดรายการงานให้กับร้านค้าหรือพนักงานใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e7a47-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e7a47-105">การจัดการงานใน Dynamics 365 Commerce ช่วยให้คุณสามารถกำหนดรายการงานให้กับร้านค้าหรือพนักงานหลายแห่ง หรือสำหรับชุดของร้านค้าและพนักงาน</span><span class="sxs-lookup"><span data-stu-id="e7a47-105">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="e7a47-106">ตัวอย่างเช่น ผู้จัดการภูมิภาคสำหรับ 20 ร้านค้า อาจต้องการกำหนดรายการงาน **การจัดเตรียมเทศกาลวันหยุด** ให้กับร้านค้าทั้งหมด 20 ร้าน</span><span class="sxs-lookup"><span data-stu-id="e7a47-106">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="e7a47-107">เริ่มต้นกระบวนการกำหนดรายการงาน</span><span class="sxs-lookup"><span data-stu-id="e7a47-107">Start the task list assignment process</span></span>

<span data-ttu-id="e7a47-108">เมื่อต้องการเริ่มต้นกระบวนการกำหนดรายการงาน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e7a47-108">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="e7a47-109">ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> การจัดการดูแลการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="e7a47-109">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="e7a47-110">เลือกรายการงานที่จะกำหนด</span><span class="sxs-lookup"><span data-stu-id="e7a47-110">Select the task list to assign.</span></span>
1. <span data-ttu-id="e7a47-111">เลือก **เริ่มกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="e7a47-111">Select **Start process**.</span></span>
1. <span data-ttu-id="e7a47-112">ในกล่องโต้ตอบ **เริ่มต้นกระบวนการ** บนแท็บ **ทั่วไป** ในฟิลด์ **ชื่อกระบวนการ** ให้ป้อนชื่อ (ตัวอย่างเช่น **ร้านค้าภาคตะวันออก**)</span><span class="sxs-lookup"><span data-stu-id="e7a47-112">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="e7a47-113">ในฟิลด์ **วันที่เป้าหมาย** ให้ระบุวันที่</span><span class="sxs-lookup"><span data-stu-id="e7a47-113">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="e7a47-114">เมื่อต้องการกำหนดรายการงานให้กับร้านค้าบนแท็บ **ร้านค้า** ให้ใช้ตัวกรอง **ลำดับชั้นขององค์กร** ในการค้นหาและเลือกร้านค้า</span><span class="sxs-lookup"><span data-stu-id="e7a47-114">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="e7a47-115">เมื่อต้องการกำหนดรายการงานให้กับพนักงาน บนแท็บ **ผู้ปฏิบัติงาน** ให้ค้นหาและเลือกพนักงาน</span><span class="sxs-lookup"><span data-stu-id="e7a47-115">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="e7a47-116">เลือก **ตกลง** เพื่อเริ่มต้นกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="e7a47-116">Select **OK** to start the process.</span></span> <span data-ttu-id="e7a47-117">รายการงานมีการกำหนดให้กับร้านค้าหรือพนักงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e7a47-117">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="e7a47-118">ภาพประกอบต่อไปนี้แสดงตัวอย่างของวิธีการค้นหาและเลือกร้านค้าในกล่องโต้ตอบ **เริ่มต้นกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="e7a47-118">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![การค้นหาและการเลือกร้านค้าในกล่องโต้ตอบเริ่มต้นกระบวนการ](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="e7a47-120">กำหนดรายการงานบนฐานที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="e7a47-120">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="e7a47-121">บางครั้งผู้ค้าปลีกมีงานที่เกิดขึ้น เช่น "รายการตรวจสอบการปิดวันพฤหัสบดี" หรือ "รายการตรวจสอบวันแรกของเดือน"</span><span class="sxs-lookup"><span data-stu-id="e7a47-121">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="e7a47-122">ดังนั้นผู้ใช้งานอาจต้องการกำหนดรายการงานให้เป็นฐานที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="e7a47-122">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="e7a47-123">ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> การจัดการดูแลการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="e7a47-123">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="e7a47-124">เลือกรายการงานที่จะกำหนด</span><span class="sxs-lookup"><span data-stu-id="e7a47-124">Select the task list to assign.</span></span>
1. <span data-ttu-id="e7a47-125">เลือก **เริ่มกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="e7a47-125">Select **Start process**.</span></span>
1. <span data-ttu-id="e7a47-126">ในกล่องโต้ตอบ **เริ่มต้นกระบวนการ** บนแท็บ **ทั่วไป** ในฟิลด์ **ชื่อกระบวนการ** ให้ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="e7a47-126">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="e7a47-127">ตั้งค่าตัวเลือก **การเกิดซ้ำ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="e7a47-127">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="e7a47-128">ในฟิลด์ **วันที่เป้าหมายการเกิดซ้ำของออฟเซ็ตในหน่วยจำนวนวัน** ให้ป้อนจำนวนวัน</span><span class="sxs-lookup"><span data-stu-id="e7a47-128">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="e7a47-129">ตัวอย่างเช่น ถ้าคุณป้อน **4** วันที่เป้าหมายคือวันที่มีการเกิดซ้ำบวกสี่วัน</span><span class="sxs-lookup"><span data-stu-id="e7a47-129">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="e7a47-130">บนแท็บ **รันในพื้นหลัง** เลือก **การเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="e7a47-130">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="e7a47-131">ในกล่องโต้ตอบ **กำหนดการเกิดซ้ำ** ให้ป้อนเกณฑ์ความถี่ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e7a47-131">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="e7a47-132">ภาพประกอบต่อไปนี้แสดงตัวอย่างของวิธีการป้อนเกณฑ์ความถี่ในกล่องโต้ตอบ **กำหนดการเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="e7a47-132">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![การป้อนเกณฑ์ความถี่ในกล่องโต้ตอบกำหนดการเกิดซ้ำ](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="e7a47-134">ติดตามสถานะรายการงาน</span><span class="sxs-lookup"><span data-stu-id="e7a47-134">Track task list status</span></span>

<span data-ttu-id="e7a47-135">ถ้าคุณเป็นผู้จัดการระดับภูมิภาคหรือผู้จัดการร้านค้า คุณอาจต้องการติดตามสถานะของรายการงานที่กำหนดให้กับร้านค้าหลายแห่งหรือพนักงานหลายคน</span><span class="sxs-lookup"><span data-stu-id="e7a47-135">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="e7a47-136">คุณสามารถติดตามผลกับร้านค้าหรือผู้ปฏิบัติงานที่ไม่ได้ทำงานที่กำหนดไว้ให้เสร็จสมบูรณ์ทันเวลา</span><span class="sxs-lookup"><span data-stu-id="e7a47-136">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="e7a47-137">ฝ่ายสนับสนุนการค้าช่วยให้คุณสามารถดูสถานะของรายการงาน มอบหมายงาน หรือเปลี่ยนสถานะของงานได้</span><span class="sxs-lookup"><span data-stu-id="e7a47-137">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="e7a47-138">เมื่อต้องการติดตามสถานะรายการงานสำหรับงานทั้งหมด ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e7a47-138">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="e7a47-139">ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> กระบวนการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="e7a47-139">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="e7a47-140">เลือกแท็บ **รายการงานทั้งหมด** เพื่อดูสถานะของรายการงานทั้งหมดที่กำหนดให้กับร้านค้าต่างๆ</span><span class="sxs-lookup"><span data-stu-id="e7a47-140">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="e7a47-141">เมื่อต้องการติดตามสถานะรายการงานสำหรับงานทั้งหมดที่คุณได้รับมอบหมาย ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e7a47-141">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="e7a47-142">ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> กระบวนการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="e7a47-142">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="e7a47-143">เลือก **งานของฉัน** หรือแท็บ **งานทั้งหมด** เพื่อดูหรืออัปเดตสถานะของงานที่กำหนดให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="e7a47-143">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7a47-144">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e7a47-144">Additional resources</span></span>

[<span data-ttu-id="e7a47-145">ภาพรวมของการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="e7a47-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="e7a47-146">ตั้งค่าคอนฟิกการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="e7a47-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="e7a47-147">สร้างรายการงานและเพิ่มงาน</span><span class="sxs-lookup"><span data-stu-id="e7a47-147">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="e7a47-148">การจัดการงานใน POS</span><span class="sxs-lookup"><span data-stu-id="e7a47-148">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
