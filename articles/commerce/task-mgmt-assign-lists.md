---
title: กำหนดรายการงานให้กับร้านค้าหรือพนักงาน
description: หัวข้อนี้จะอธิบายถึงวิธีการกำหนดรายการงานให้กับร้านค้าหรือพนักงานใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 82cec9861b759037f40315fb2e6f36002a0ac059
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416195"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="b67d3-103">กำหนดรายการงานให้กับร้านค้าหรือพนักงาน</span><span class="sxs-lookup"><span data-stu-id="b67d3-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b67d3-104">หัวข้อนี้จะอธิบายถึงวิธีการกำหนดรายการงานให้กับร้านค้าหรือพนักงานใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b67d3-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b67d3-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="b67d3-105">Overview</span></span>

<span data-ttu-id="b67d3-106">การจัดการงานใน Dynamics 365 Commerce ช่วยให้คุณสามารถกำหนดรายการงานให้กับร้านค้าหรือพนักงานหลายแห่ง หรือสำหรับชุดของร้านค้าและพนักงาน</span><span class="sxs-lookup"><span data-stu-id="b67d3-106">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="b67d3-107">ตัวอย่างเช่น ผู้จัดการภูมิภาคสำหรับ 20 ร้านค้า อาจต้องการกำหนดรายการงาน **การจัดเตรียมเทศกาลวันหยุด** ให้กับร้านค้าทั้งหมด 20 ร้าน</span><span class="sxs-lookup"><span data-stu-id="b67d3-107">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="b67d3-108">เริ่มต้นกระบวนการกำหนดรายการงาน</span><span class="sxs-lookup"><span data-stu-id="b67d3-108">Start the task list assignment process</span></span>

<span data-ttu-id="b67d3-109">เมื่อต้องการเริ่มต้นกระบวนการกำหนดรายการงาน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b67d3-109">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="b67d3-110">ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> การจัดการดูแลการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="b67d3-110">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="b67d3-111">เลือกรายการงานที่จะกำหนด</span><span class="sxs-lookup"><span data-stu-id="b67d3-111">Select the task list to assign.</span></span>
1. <span data-ttu-id="b67d3-112">เลือก **เริ่มกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="b67d3-112">Select **Start process**.</span></span>
1. <span data-ttu-id="b67d3-113">ในกล่องโต้ตอบ **เริ่มต้นกระบวนการ** บนแท็บ **ทั่วไป** ในฟิลด์ **ชื่อกระบวนการ** ให้ป้อนชื่อ (ตัวอย่างเช่น **ร้านค้าภาคตะวันออก**)</span><span class="sxs-lookup"><span data-stu-id="b67d3-113">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="b67d3-114">ในฟิลด์ **วันที่เป้าหมาย** ให้ระบุวันที่</span><span class="sxs-lookup"><span data-stu-id="b67d3-114">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="b67d3-115">เมื่อต้องการกำหนดรายการงานให้กับร้านค้าบนแท็บ **ร้านค้า** ให้ใช้ตัวกรอง **ลำดับชั้นขององค์กร** ในการค้นหาและเลือกร้านค้า</span><span class="sxs-lookup"><span data-stu-id="b67d3-115">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="b67d3-116">เมื่อต้องการกำหนดรายการงานให้กับพนักงาน บนแท็บ **ผู้ปฏิบัติงาน** ให้ค้นหาและเลือกพนักงาน</span><span class="sxs-lookup"><span data-stu-id="b67d3-116">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="b67d3-117">เลือก **ตกลง** เพื่อเริ่มต้นกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="b67d3-117">Select **OK** to start the process.</span></span> <span data-ttu-id="b67d3-118">รายการงานมีการกำหนดให้กับร้านค้าหรือพนักงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b67d3-118">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="b67d3-119">ภาพประกอบต่อไปนี้แสดงตัวอย่างของวิธีการค้นหาและเลือกร้านค้าในกล่องโต้ตอบ **เริ่มต้นกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="b67d3-119">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![การค้นหาและการเลือกร้านค้าในกล่องโต้ตอบเริ่มต้นกระบวนการ](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="b67d3-121">กำหนดรายการงานบนฐานที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="b67d3-121">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="b67d3-122">บางครั้งผู้ค้าปลีกมีงานที่เกิดขึ้น เช่น "รายการตรวจสอบการปิดวันพฤหัสบดี" หรือ "รายการตรวจสอบวันแรกของเดือน"</span><span class="sxs-lookup"><span data-stu-id="b67d3-122">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="b67d3-123">ดังนั้นผู้ใช้งานอาจต้องการกำหนดรายการงานให้เป็นฐานที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="b67d3-123">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="b67d3-124">ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> การจัดการดูแลการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="b67d3-124">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="b67d3-125">เลือกรายการงานที่จะกำหนด</span><span class="sxs-lookup"><span data-stu-id="b67d3-125">Select the task list to assign.</span></span>
1. <span data-ttu-id="b67d3-126">เลือก **เริ่มกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="b67d3-126">Select **Start process**.</span></span>
1. <span data-ttu-id="b67d3-127">ในกล่องโต้ตอบ **เริ่มต้นกระบวนการ** บนแท็บ **ทั่วไป** ในฟิลด์ **ชื่อกระบวนการ** ให้ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="b67d3-127">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="b67d3-128">ตั้งค่าตัวเลือก **การเกิดซ้ำ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="b67d3-128">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="b67d3-129">ในฟิลด์ **วันที่เป้าหมายการเกิดซ้ำของออฟเซ็ตในหน่วยจำนวนวัน** ให้ป้อนจำนวนวัน</span><span class="sxs-lookup"><span data-stu-id="b67d3-129">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="b67d3-130">ตัวอย่างเช่น ถ้าคุณป้อน **4** วันที่เป้าหมายคือวันที่มีการเกิดซ้ำบวกสี่วัน</span><span class="sxs-lookup"><span data-stu-id="b67d3-130">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="b67d3-131">บนแท็บ **รันในพื้นหลัง** เลือก **การเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="b67d3-131">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="b67d3-132">ในกล่องโต้ตอบ **กำหนดการเกิดซ้ำ** ให้ป้อนเกณฑ์ความถี่ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b67d3-132">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="b67d3-133">ภาพประกอบต่อไปนี้แสดงตัวอย่างของวิธีการป้อนเกณฑ์ความถี่ในกล่องโต้ตอบ **กำหนดการเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="b67d3-133">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![การป้อนเกณฑ์ความถี่ในกล่องโต้ตอบกำหนดการเกิดซ้ำ](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="b67d3-135">ติดตามสถานะรายการงาน</span><span class="sxs-lookup"><span data-stu-id="b67d3-135">Track task list status</span></span>

<span data-ttu-id="b67d3-136">ถ้าคุณเป็นผู้จัดการระดับภูมิภาคหรือผู้จัดการร้านค้า คุณอาจต้องการติดตามสถานะของรายการงานที่กำหนดให้กับร้านค้าหลายแห่งหรือพนักงานหลายคน</span><span class="sxs-lookup"><span data-stu-id="b67d3-136">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="b67d3-137">คุณสามารถติดตามผลกับร้านค้าหรือผู้ปฏิบัติงานที่ไม่ได้ทำงานที่กำหนดไว้ให้เสร็จสมบูรณ์ทันเวลา</span><span class="sxs-lookup"><span data-stu-id="b67d3-137">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="b67d3-138">ฝ่ายสนับสนุนการค้าช่วยให้คุณสามารถดูสถานะของรายการงาน มอบหมายงาน หรือเปลี่ยนสถานะของงานได้</span><span class="sxs-lookup"><span data-stu-id="b67d3-138">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="b67d3-139">เมื่อต้องการติดตามสถานะรายการงานสำหรับงานทั้งหมด ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b67d3-139">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="b67d3-140">ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> กระบวนการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="b67d3-140">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="b67d3-141">เลือกแท็บ **รายการงานทั้งหมด** เพื่อดูสถานะของรายการงานทั้งหมดที่กำหนดให้กับร้านค้าต่างๆ</span><span class="sxs-lookup"><span data-stu-id="b67d3-141">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="b67d3-142">เมื่อต้องการติดตามสถานะรายการงานสำหรับงานทั้งหมดที่คุณได้รับมอบหมาย ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b67d3-142">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="b67d3-143">ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> กระบวนการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="b67d3-143">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="b67d3-144">เลือก **งานของฉัน** หรือแท็บ **งานทั้งหมด** เพื่อดูหรืออัปเดตสถานะของงานที่กำหนดให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="b67d3-144">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b67d3-145">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b67d3-145">Additional resources</span></span>

[<span data-ttu-id="b67d3-146">ภาพรวมของการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="b67d3-146">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="b67d3-147">ตั้งค่าคอนฟิกการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="b67d3-147">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="b67d3-148">สร้างรายการงานและเพิ่มงาน</span><span class="sxs-lookup"><span data-stu-id="b67d3-148">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="b67d3-149">การจัดการงานใน POS</span><span class="sxs-lookup"><span data-stu-id="b67d3-149">Task management in POS</span></span>](task-mgmt-POS.md)
