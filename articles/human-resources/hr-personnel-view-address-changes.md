---
title: ดูและจัดการการเปลี่ยนแปลงที่อยู่
description: หัวข้อนี้จะอธิบายถึงวิธีการที่คุณสามารถดูและจัดการการเปลี่ยนแปลงที่อยู่ใน Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a69d723b45e834b022491c8eaf2a7fb580e54f1d
ms.sourcegitcommit: 288df4fe766536e51ca9b5306c5bb948b7772ac5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2020
ms.locfileid: "3688332"
---
# <a name="view-and-manage-address-changes"></a><span data-ttu-id="d5fe6-103">ดูและจัดการการเปลี่ยนแปลงที่อยู่</span><span class="sxs-lookup"><span data-stu-id="d5fe6-103">View and manage address changes</span></span>

<span data-ttu-id="d5fe6-104">หัวข้อนี้จะอธิบายวิธีการที่คุณสามารถดูและจัดการการเปลี่ยนแปลงที่อยู่ในหน้า **แก้ไขรายละเอียดส่วนบุคคล** ของระบบบริการตนเองของพนักงาน หรือหน้ารายละเอียดของ **ผู้ปฏิบัติงาน** ใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="d5fe6-104">This topic explains how you can view and manage address changes in the Employee self-service **Edit personal details** page or the **Worker** details page in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d5fe6-105">องค์กรหลายแห่งต้องการให้พนักงานจัดการรายละเอียดส่วนตัวของตนเองผ่านการใช้ระบบบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="d5fe6-105">Many organizations want employees to manage their own personal details through a self-service experience.</span></span> <span data-ttu-id="d5fe6-106">คุณสามารถอนุญาตให้ผู้ใช้อัปเดตที่อยู่ของตนในพื้นที่ทำงาน **ระบบบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-106">You can allow users to update their address in the **Employee self service** workspace.</span></span> <span data-ttu-id="d5fe6-107">คุณสามารถตรวจสอบการเปลี่ยนแปลงเหล่านี้ได้ในพื้นที่ทำงาน **การจัดการบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-107">You can then monitor these changes in the **Personnel management** workspace.</span></span> <span data-ttu-id="d5fe6-108">เมื่อต้องการใช้คุณลักษณะนี้ คุณต้องระบุจำนวนวันที่คุณต้องการดูการเปลี่ยนแปลงในหน้า **พารามิเตอร์ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-108">To use this feature, you must specify the number of days that you want to view changes in the **Human resources parameters** page.</span></span>

## <a name="configure-address-change-parameters"></a><span data-ttu-id="d5fe6-109">ตั้งค่าคอนฟิกพารามิเตอร์การเปลี่ยนแปลงที่อยู่</span><span class="sxs-lookup"><span data-stu-id="d5fe6-109">Configure address change parameters</span></span>

<span data-ttu-id="d5fe6-110">เมื่อต้องการตั้งค่าคอนฟิกจำนวนวันที่คุณต้องการให้การเปลี่ยนแปลงที่อยู่แสดงในพื้นที่ทำงาน **การจัดการบุคลากร** ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d5fe6-110">To configure the number of days that you want address changes to appear in the **Personnel management** workspace, follow these steps:</span></span>

1. <span data-ttu-id="d5fe6-111">ในบานหน้าต่างนำทาง ให้เลือก **การจัดการบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-111">On the navigation pane, select **Personnel management**.</span></span>

2. <span data-ttu-id="d5fe6-112">เลือก **ลิงก์**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-112">Select **Links**.</span></span>

3. <span data-ttu-id="d5fe6-113">เลือก **พารามิเตอร์ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-113">Select **Human resources parameters**.</span></span>

4. <span data-ttu-id="d5fe6-114">ในฟิลด์ **จำนวนวัน** ที่อยู่ภายใต้ **การเปลี่ยนแปลงที่อยู่** ให้ป้อนจำนวนวันที่คุณต้องการให้การเปลี่ยนแปลงที่อยู่ปรากฏในพื้นที่ทำงาน **การจัดการบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-114">In the **Number of days** field under **Address change**, enter the number of days that you want address changes to appear in the **Personnel management** workspace.</span></span>

5. <span data-ttu-id="d5fe6-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d5fe6-115">Close the page.</span></span>

## <a name="create-or-change-an-employee-address"></a><span data-ttu-id="d5fe6-116">การสร้างหรือเปลี่ยนที่อยู่ของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="d5fe6-116">Create or change an employee address</span></span>

<span data-ttu-id="d5fe6-117">พนักงานสามารถอัพเดตที่อยู่ของตนในพื้นที่ทำงาน **ระบบบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-117">Employees can update their own address in the **Employee self service** workspace.</span></span> <span data-ttu-id="d5fe6-118">ทำตามขั้นตอนเหล่านี้เพื่อสร้างหรือเปลี่ยนที่อยู่</span><span class="sxs-lookup"><span data-stu-id="d5fe6-118">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="d5fe6-119">เลือกไทล์ **ระบบบริการตนเองของพนักงาน** บนโฮมเพจของคุณ</span><span class="sxs-lookup"><span data-stu-id="d5fe6-119">Select the **Employee self-service** tile on your home page.</span></span>

2. <span data-ttu-id="d5fe6-120">เลือก **แก้ไขรายละเอียดส่วนตัว**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-120">Select **Edit personal details**.</span></span>

3. <span data-ttu-id="d5fe6-121">หากต้องการเพิ่มที่อยู่ ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-121">To add an address, select **Add**.</span></span> <span data-ttu-id="d5fe6-122">ถ้าต้องการอัพเดตที่อยู่ที่มีอยู่ ให้เลือกที่อยู่จากรายการ และจากนั้นเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-122">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="d5fe6-123">ป้อน **ชื่อหรือคำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-123">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="d5fe6-124">เลือกกล่องแบบหล่นลงของ **วัตถุประสงค์** แล้วเลือกชนิดของที่อยู่</span><span class="sxs-lookup"><span data-stu-id="d5fe6-124">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="d5fe6-125">ป้อน **ประเทศ/ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-125">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="d5fe6-126">ป้อน **รหัสไปรษณีย์**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-126">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="d5fe6-127">ป้อน **ถนน**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-127">Enter the **Street**.</span></span>

9. <span data-ttu-id="d5fe6-128">ป้อน **เมือง**, **รัฐ** และ **เขต**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-128">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="d5fe6-129">โดยทั่วไปแล้วจะมีการตั้งค่าฟิลด์เหล่านี้โดยอัตโนมัติตามฟิลด์ **รหัสไปรษณีย์**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-129">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="d5fe6-130">อีกทางหนึ่งคือเลือกฟิลด์ **หลัก** เพื่อระบุที่อยู่หลัก</span><span class="sxs-lookup"><span data-stu-id="d5fe6-130">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="d5fe6-131">คุณสามารถทำเครื่องหมายที่อยู่ได้เพียงรายการเดียวเป็นที่อยู่หลัก</span><span class="sxs-lookup"><span data-stu-id="d5fe6-131">Only one address can be marked as the primary.</span></span> <span data-ttu-id="d5fe6-132">ถ้ามีการทำเครื่องหมายที่อยู่อื่นเป็นที่อยู่หลักอยู่แล้ว คุณต้องยืนยันว่าคุณต้องการใช้ที่อยู่นี้เป็นที่อยู่หลัก</span><span class="sxs-lookup"><span data-stu-id="d5fe6-132">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="d5fe6-133">อีกทางหนึ่งคือเลือกฟิลด์ **ส่วนตัว** เพื่อระบุที่อยู่เป็นแบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="d5fe6-133">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="d5fe6-134">เฉพาะผู้ใช้ที่มีสิทธิอย่างชัดแจ้งในการดูข้อมูลที่อยู่ส่วนตัวเท่านั้นที่สามารถดูที่อยู่นี้ได้</span><span class="sxs-lookup"><span data-stu-id="d5fe6-134">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="d5fe6-135">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-135">Select **OK**.</span></span>

## <a name="create-or-change-a-worker-address"></a><span data-ttu-id="d5fe6-136">สร้างหรือเปลี่ยนที่อยู่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="d5fe6-136">Create or change a worker address</span></span>

<span data-ttu-id="d5fe6-137">คุณสามารถอัปเดตที่อยู่ในพื้นที่ทำงาน **การจัดการบุคลากร** ได้</span><span class="sxs-lookup"><span data-stu-id="d5fe6-137">You can update an address in the **Personnel management** workspace.</span></span> <span data-ttu-id="d5fe6-138">ทำตามขั้นตอนเหล่านี้เพื่อสร้างหรือเปลี่ยนที่อยู่</span><span class="sxs-lookup"><span data-stu-id="d5fe6-138">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="d5fe6-139">ในพื้นที่ทำงาน **การจัดการบุคลากร** ให้เลือก **ลิงก์** แล้วเลือก **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-139">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>

3. <span data-ttu-id="d5fe6-140">เลือกผู้ปฏิบัติงาน แล้วเลือก **ที่อยู่**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-140">Select the worker, and then select **Addresses**.</span></span>

3. <span data-ttu-id="d5fe6-141">หากต้องการเพิ่มที่อยู่ ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-141">To add an address, select **Add**.</span></span> <span data-ttu-id="d5fe6-142">ถ้าต้องการอัพเดตที่อยู่ที่มีอยู่ ให้เลือกที่อยู่จากรายการ และจากนั้นเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-142">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="d5fe6-143">ป้อน **ชื่อหรือคำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-143">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="d5fe6-144">เลือกกล่องแบบหล่นลงของ **วัตถุประสงค์** แล้วเลือกชนิดของที่อยู่</span><span class="sxs-lookup"><span data-stu-id="d5fe6-144">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="d5fe6-145">ป้อน **ประเทศ/ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-145">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="d5fe6-146">ป้อน **รหัสไปรษณีย์**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-146">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="d5fe6-147">ป้อน **ถนน**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-147">Enter the **Street**.</span></span>

9. <span data-ttu-id="d5fe6-148">ป้อน **เมือง**, **รัฐ** และ **เขต**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-148">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="d5fe6-149">โดยทั่วไปแล้วจะมีการตั้งค่าฟิลด์เหล่านี้โดยอัตโนมัติตามฟิลด์ **รหัสไปรษณีย์**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-149">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="d5fe6-150">อีกทางหนึ่งคือเลือกฟิลด์ **หลัก** เพื่อระบุที่อยู่หลัก</span><span class="sxs-lookup"><span data-stu-id="d5fe6-150">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="d5fe6-151">คุณสามารถทำเครื่องหมายที่อยู่ได้เพียงรายการเดียวเป็นที่อยู่หลัก</span><span class="sxs-lookup"><span data-stu-id="d5fe6-151">Only one address can be marked as the primary.</span></span> <span data-ttu-id="d5fe6-152">ถ้ามีการทำเครื่องหมายที่อยู่อื่นเป็นที่อยู่หลักอยู่แล้ว คุณต้องยืนยันว่าคุณต้องการใช้ที่อยู่นี้เป็นที่อยู่หลัก</span><span class="sxs-lookup"><span data-stu-id="d5fe6-152">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="d5fe6-153">อีกทางหนึ่งคือเลือกฟิลด์ **ส่วนตัว** เพื่อระบุที่อยู่เป็นแบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="d5fe6-153">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="d5fe6-154">เฉพาะผู้ใช้ที่มีสิทธิอย่างชัดแจ้งในการดูข้อมูลที่อยู่ส่วนตัวเท่านั้นที่สามารถดูที่อยู่นี้ได้</span><span class="sxs-lookup"><span data-stu-id="d5fe6-154">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="d5fe6-155">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-155">Select **OK**.</span></span>
 
## <a name="create-a-future-change-for-an-address"></a><span data-ttu-id="d5fe6-156">สร้างการเปลี่ยนแปลงในอนาคตสำหรับที่อยู่</span><span class="sxs-lookup"><span data-stu-id="d5fe6-156">Create a future change for an address</span></span>

<span data-ttu-id="d5fe6-157">ในบางกรณี คุณอาจต้องการอัพเดตที่อยู่ที่จะเปลี่ยนในอนาคต</span><span class="sxs-lookup"><span data-stu-id="d5fe6-157">In some cases, you might want to update an address to change in the future.</span></span> <span data-ttu-id="d5fe6-158">ตัวอย่างเช่น การตั้งค่านี้จะเป็นประโยชน์ถ้าพนักงานย้ายในวันที่ 15 ของเดือนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d5fe6-158">For example, this would be useful if an employee is moving on the 15th of the following month.</span></span>

1. <span data-ttu-id="d5fe6-159">เปิดหน้า **จัดการที่อยู่** โดยการเลือก **ตัวเลือกเพิ่มเติม > ขั้นสูง** จากตารางที่อยู่</span><span class="sxs-lookup"><span data-stu-id="d5fe6-159">Open the **Manage addresses** page by selecting **More options > Advanced** from any address grid.</span></span>

2. <span data-ttu-id="d5fe6-160">เลือก **สร้าง** เพื่อสร้างที่อยู่ใหม่</span><span class="sxs-lookup"><span data-stu-id="d5fe6-160">Select **New** to create a new address.</span></span>

3. <span data-ttu-id="d5fe6-161">ป้อนรายละเอียดของที่อยู่</span><span class="sxs-lookup"><span data-stu-id="d5fe6-161">Enter the details of the address.</span></span>

4. <span data-ttu-id="d5fe6-162">เลือกแท็บด่วน **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-162">Select the **General** FastTab.</span></span>

5. <span data-ttu-id="d5fe6-163">ในฟิลด์ **วันที่มีผลบังคับใช้** ให้เลือกวันที่ที่อยู่ใหม่จะมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="d5fe6-163">In the **Effective date** field, select the date the new address will be effective.</span></span>

6. <span data-ttu-id="d5fe6-164">ในฟิลด์ **วันหมดอายุ** เลือกเวลาที่ที่อยู่จะไม่มีผลบังคับใช้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="d5fe6-164">In the **Expiration date** field, optionally select when the address will no longer be effective.</span></span>

7. <span data-ttu-id="d5fe6-165">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d5fe6-165">Close the pages.</span></span>

## <a name="view-and-monitor-address-changes"></a><span data-ttu-id="d5fe6-166">ดูและตรวจสอบการเปลี่ยนแปลงที่อยู่</span><span class="sxs-lookup"><span data-stu-id="d5fe6-166">View and monitor address changes</span></span>

<span data-ttu-id="d5fe6-167">บุคลากรฝ่ายบุคคลสามารถดูและตรวจสอบการเปลี่ยนแปลงที่อยู่จากพื้นที่ทำงาน **การจัดการบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-167">HR personnel can view and monitor address changes from the **Personnel management** workspace.</span></span> <span data-ttu-id="d5fe6-168">เมื่อต้องการดูการเปลี่ยนแปลงที่อยู่ ให้เปิดไทล์ **การจัดการบุคลากร** จาก **หน้าแรก**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-168">To view the address changes, open the **Personnel management** tile from the **Home** page.</span></span> <span data-ttu-id="d5fe6-169">ที่อยู่ที่เปลี่ยนแปลงแสดงอยู่บนไทล์ในมุมบนขวา</span><span class="sxs-lookup"><span data-stu-id="d5fe6-169">The address changes display on a tile in the upper-right corner.</span></span> <span data-ttu-id="d5fe6-170">จำนวนของ **การเปลี่ยนแปลงที่อยู่** ด้านบนแสดงการเปลี่ยนแปลงที่อยู่ที่เกิดขึ้นในจำนวนวันที่ระบุในหน้า **พารามิเตอร์ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="d5fe6-170">The number above **Address changes** shows how many address changes occurred in the number of days specified in the **Human resources parameters** page.</span></span> 

<span data-ttu-id="d5fe6-171">เมื่อคุณเลือกไทล์ **การเปลี่ยนแปลงที่อยู่** หน้าใหม่จะแสดงรายละเอียดของการเปลี่ยนแปลงที่อยู่ใดๆ</span><span class="sxs-lookup"><span data-stu-id="d5fe6-171">When you select the **Address changes** tile, a new page displays the details of any address changes.</span></span> <span data-ttu-id="d5fe6-172">คุณสามารถเลือก **รวมการเปลี่ยนแปลงที่อยู่ในอนาคต** ในมุมด้านขวาบนเพื่อแสดงการเปลี่ยนแปลงที่อยู่ด้วยวันที่ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="d5fe6-172">You can optionally select **Include future address changes** in the upper-right corner to display address changes with a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="d5fe6-173">ถ้าคุณต้องการรับข้อความแจ้งเตือนหรืออีเมลเกี่ยวกับการเปลี่ยนแปลงที่อยู่เหล่านี้ คุณสามารถสร้างกฎการแจ้งเตือนใหม่บนแท็บ **ตัวเลือก** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="d5fe6-173">If you want to receive an alert or email about these address changes, you can create a new alert rule on the **Options** tab in the Action Pane.</span></span> <span data-ttu-id="d5fe6-174">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกฎการแจ้งเตือน ให้ดูที่ [สร้างกฎการแจ้งเตือน](/fin-ops-core/fin-ops/get-started/create-alert-rules.md)</span><span class="sxs-lookup"><span data-stu-id="d5fe6-174">For more information about alert rules, see [Create alert rules](/fin-ops-core/fin-ops/get-started/create-alert-rules.md).</span></span><br><br>

> <span data-ttu-id="d5fe6-175">ถ้าคุณต้องการตั้งค่าคอนฟิกลำดับงานสำหรับการเปลี่ยนแปลงที่อยู่ คุณสามารถเลือกตัวเลือก **ส่งจากภายนอก** ในกฎการแจ้งเตือนของคุณ แล้วใช้ Power Automate เพื่อทริกเกอร์เหตุการณ์ทางธุรกิจและตั้งค่าคอนฟิกลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="d5fe6-175">If you want to configure a workflow for the address changes, you can select the **Send externally** option on your alert rule, and then use Power Automate to trigger the business event and configure a workflow.</span></span> <span data-ttu-id="d5fe6-176">สำหรับข้อมูลเพิ่มเติม ให้ดู [การแจ้งเตือนเป็นเหตุการณ์ทางธุรกิจ](/fin-ops-core/dev-itpro/business-events/alerts-business-events.md)</span><span class="sxs-lookup"><span data-stu-id="d5fe6-176">For more information, see [Alerts as business events](/fin-ops-core/dev-itpro/business-events/alerts-business-events.md).</span></span>
