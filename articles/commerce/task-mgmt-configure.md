---
title: ตั้งค่าคอนฟิกการจัดการงาน
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าคอนฟิกคุณลักษณะการจัดการงานใน Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416194"
---
# <a name="configure-task-management"></a><span data-ttu-id="ec285-103">ตั้งค่าคอนฟิกการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="ec285-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ec285-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่าคอนฟิกคุณลักษณะการจัดการงานใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ec285-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ec285-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="ec285-105">Overview</span></span>

<span data-ttu-id="ec285-106">ก่อนที่ผู้จัดการและพนักงาน Dynamics 365 Commerce จะสามารถใช้คุณลักษณะการจัดการงานใน Commerce ได้ ต้องมีการตั้งค่าคอนฟิกการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="ec285-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="ec285-107">ขั้นตอนการตั้งค่าคอนฟิกรวมถึงการให้สิทธิ์กับผู้จัดการและพนักงาน การกระจายสิทธิ์ไปยังไคลเอนต์ของการขายหน้าร้าน (POS) การตั้งค่าการแจ้งเตือน POS และการตั้งค่าไทล์ **งาน** บนโฮมเพจของแอปพลิเคชัน POS</span><span class="sxs-lookup"><span data-stu-id="ec285-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="ec285-108">ตั้งค่าคอนฟิกสิทธิ์สำหรับผู้จัดการร้านค้า</span><span class="sxs-lookup"><span data-stu-id="ec285-108">Configure permissions for store managers</span></span>

<span data-ttu-id="ec285-109">ผู้ปฏิบัติงานทุกคนในร้านค้าที่กำหนดสามารถดูงานทั้งหมดที่กำหนดให้กับร้านค้าดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="ec285-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="ec285-110">นอกจากนี้ คุณยังสามารถอัปเดตสถานะของงานที่กำหนดให้กับผู้ใช้เหล่านั้นได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="ec285-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="ec285-111">อย่างไรก็ตาม บทบาท เช่น ผู้จัดการร้านค้า ต้องมีสิทธ์ในการจัดการงานที่ได้รับมอบหมายให้กับร้านค้าและเพื่อสร้างงานวัตถุประสงค์เดียว</span><span class="sxs-lookup"><span data-stu-id="ec285-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="ec285-112">เมื่อต้องการตั้งค่าคอนฟิกสิทธิ์การจัดการงานสำหรับผู้จัดการร้านค้า ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ec285-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="ec285-113">ไปที่ **การขายปลีกและการค้า \> พนักงาน \> กลุ่มสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="ec285-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="ec285-114">เลือกกลุ่มสิทธิ์เฉพาะ (ตัวอย่างเช่น **ผู้จัดการ**) แล้วเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="ec285-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="ec285-115">บนแท็บด่วน **สิทธิ์** ให้ตั้งค่าตัวเลือก **อนุญาตการจัดการงาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ec285-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="ec285-116">บนแท็บด่วน **การแจ้งเตือน** ให้เพิ่มการดำเนินงาน **การจัดการงาน** และป้อนค่าในฟิลด์ **ลำดับการแสดงผล**</span><span class="sxs-lookup"><span data-stu-id="ec285-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="ec285-117">ตัวอย่างเช่น ป้อน **2** ถ้าการดำเนินงาน **การเติมสินค้าของใบสั่ง** มีค่า **ลำดับการแสดงผล** เป็น **1** อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="ec285-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ec285-118">ถ้าบทบาทที่ไม่ใช่ผู้จัดการต้องมีสิทธิ์ในการจัดการงานใน POS คุณสามารถให้สิทธิ์สำหรับแต่ละบุคคล</span><span class="sxs-lookup"><span data-stu-id="ec285-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="ec285-119">อีกทางหนึ่งคือ คุณสามารถสร้างกลุ่มสิทธิ์ใหม่สำหรับผู้ที่ไม่ใช่ผู้จัดการและตั้งค่าตัวเลือก **อนุญาตการจัดการงาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ec285-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="ec285-120">แผนภาพต่อไปนี้แสดงวิธีตั้งค่าคอนฟิกสิทธิ์การจัดการงานสำหรับผู้จัดการร้านค้า</span><span class="sxs-lookup"><span data-stu-id="ec285-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![การตั้งค่าคอนฟิกสิทธิ์การจัดการงานสำหรับผู้จัดการร้านค้า](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="ec285-122">ตั้งค่าคอนฟิกสิทธิ์สำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="ec285-122">Configure permissions for employees</span></span>

<span data-ttu-id="ec285-123">พนักงานต้องมีสิทธิ์ในการสร้างรายการงาน จัดการเงื่อนไขการกำหนด และตั้งค่าคอนฟิกการเกิดซ้ำของรายการงานใดๆ</span><span class="sxs-lookup"><span data-stu-id="ec285-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="ec285-124">เมื่อต้องการตั้งค่าคอนฟิกสิทธิ์เหล่านี้ คุณสามารถกำหนดพนักงานให้กับบทบาท **จัดการงานขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="ec285-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="ec285-125">ในการตั้งค่าคอนฟิกสิทธิ์สำหรับพนักงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ec285-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="ec285-126">ไปยัง **การขายปลีกและการค้า \> พนักงาน \> ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="ec285-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="ec285-127">เลือกพนักงาน</span><span class="sxs-lookup"><span data-stu-id="ec285-127">Select an employee.</span></span>
1. <span data-ttu-id="ec285-128">บนแท็บด่วน **บทบาทของผู้ใช้** ให้เลือก **กำหนดบทบาท**</span><span class="sxs-lookup"><span data-stu-id="ec285-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="ec285-129">ในกล่องโต้ตอบ **กำหนดบทบาทให้กับผู้ใช้** ให้เลือกบทบาทของ **ผู้จัดการงานขายปลีก** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ec285-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="ec285-130">กระจายสิทธิ์ไปยังไคลเอนต์ POS</span><span class="sxs-lookup"><span data-stu-id="ec285-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="ec285-131">ก่อนที่พนักงานสามารถใช้ไคลเอนต์ POS ต้องมีการกระจายสิทธิ์และซิงค์กับไคลเอนต์เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="ec285-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="ec285-132">เมื่อต้องการกระจายสิทธิ์ไปยังไคลเอนต์ POS ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ec285-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="ec285-133">ไปยัง **การขายปลีกและการค้า \> การขายปลีกและไอทีเชิงพาณิชย์ \> กำหนดการการจัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="ec285-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="ec285-134">เลือกตารางการหระจาย **1060** (**พนักงาน**) แล้วเลือก **เรียกใช้เดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="ec285-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="ec285-135">เลือกตารางการกระจาย **1070** (**การตั้งค่าคอนฟิกช่องทาง**) แล้วเลือก **เรียกใช้เดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="ec285-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="ec285-136">ตั้งค่าคอนฟิกการแจ้งเตือน POS สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="ec285-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="ec285-137">ต้องมีการตั้งค่าคอนฟิกการจัดการงานเพื่อให้การแจ้งเตือนพร้อมใช้งานในแอปพลิเคชัน POS</span><span class="sxs-lookup"><span data-stu-id="ec285-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="ec285-138">ในการตั้งค่าคอนฟิกการแจ้งเตือน POS สำหรับงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ec285-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="ec285-139">ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> POS \> การดำเนินการ POS**</span><span class="sxs-lookup"><span data-stu-id="ec285-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="ec285-140">ค้นหาการดำเนินงาน **1400** (**การจัดการงาน**) และเลือกกล่องกาเครื่องหมาย **เปิดใช้งานการแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="ec285-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="ec285-141">ภาพประกอบต่อไปนี้จะแสดงการดำเนินงานของ **การจัดการงาน** ในหน้า **การดำเนินงาน POS**</span><span class="sxs-lookup"><span data-stu-id="ec285-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![การดำเนินงานการจัดการงานในหน้าการดำเนินงาน POS](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="ec285-143">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกการแจ้งเตือน POS ให้ดูที่ [แสดงการแจ้งเตือนใบสั่งในการขายหน้าร้าน (POS)](notifications-pos.md)</span><span class="sxs-lookup"><span data-stu-id="ec285-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="ec285-144">ตั้งค่าคอนฟิกไทล์งานบนโฮมเพจของแอปพลิเคชัน POS</span><span class="sxs-lookup"><span data-stu-id="ec285-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="ec285-145">ก่อนที่คุณจะตั้งค่าคอนฟิกไทล์ **งาน** บนโฮมเพจของแอปพลิเคชัน POS ให้ดูที่ [โครงร่างหน้าจอสำหรับการขายหน้าร้าน (POS)](pos-screen-layouts.md) สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกและเพิ่มปุ่มใหม่ลงในโครงร่างหน้าจอ POS</span><span class="sxs-lookup"><span data-stu-id="ec285-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="ec285-146">หากต้องการตั้งค่าคอนฟิกไทล์ **งาน** บนโฮมเพจของแอปพลิเคชัน POS ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ec285-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="ec285-147">ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า \> POS \> โครงร่างหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="ec285-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="ec285-148">เลือกโครงร่างหน้าจอ เลือกขนาดโครงร่าง และเลือกกริดปุ่ม</span><span class="sxs-lookup"><span data-stu-id="ec285-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="ec285-149">บนแท็บด่วน **กริดปุ่ม** ให้เลือก **ผู้ออกแบบ** เพื่อแก้ไขกริดปุ่มที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ec285-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="ec285-150">เพิ่มไทล์ **งาน** ไปยังส่วนที่เหมาะสมของโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="ec285-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="ec285-151">ภาพประกอบต่อไปนี้แสดงตัวอย่างของไทล์ **งาน** บนโฮมเพจ POS</span><span class="sxs-lookup"><span data-stu-id="ec285-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![ไทล์งานบนโฮมเพจของ POS](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="ec285-153">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ec285-153">Additional resources</span></span>

[<span data-ttu-id="ec285-154">ภาพรวมของการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="ec285-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="ec285-155">สร้างรายการงานและเพิ่มงาน</span><span class="sxs-lookup"><span data-stu-id="ec285-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="ec285-156">กำหนดรายการงานให้กับร้านค้าหรือพนักงาน</span><span class="sxs-lookup"><span data-stu-id="ec285-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="ec285-157">การจัดการงานใน POS</span><span class="sxs-lookup"><span data-stu-id="ec285-157">Task management in POS</span></span>](task-mgmt-POS.md)
