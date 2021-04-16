---
title: การจัดการเวลาและการเข้างานใน Retail
description: หัวข้อนี้อธิบายสถานการณ์จำลองที่ได้รับการสนับสนุนสำหรับการจัดการเวลาและการเข้าร่วมใน Dynamics 365 Commerce
author: aamirallaqaband
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9bec213cd4954f69605387ae2801d8af98a8111c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791906"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="beb34-103">การจัดการเวลาและการเข้างานใน Retail</span><span class="sxs-lookup"><span data-stu-id="beb34-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="beb34-104">หัวข้อนี้อธิบายสถานการณ์จำลองที่ได้รับการสนับสนุนสำหรับการจัดการเวลาและการเข้าร่วมใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="beb34-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="beb34-105">จัดการการตั้งค่าผู้ปฏิบัติงานและการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="beb34-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="beb34-106">การตั้งค่าคอนฟิกเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="beb34-106">Initial configuration</span></span>

- <span data-ttu-id="beb34-107">ดำเนินการวิซาร์ดการตั้งค่าคอนฟิกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="beb34-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="beb34-108">ลงทะเบียนผู้ปฏิบัติงานเป็นผู้ปฏิบัติงานลงทะเบียนเวลา</span><span class="sxs-lookup"><span data-stu-id="beb34-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="beb34-109">วางแผนกำหนดการของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="beb34-109">Plan worker schedules</span></span>

- <span data-ttu-id="beb34-110">การนำโพรไฟล์มาใช้โดยการใช้โปรแกรมวางแผนงาน</span><span class="sxs-lookup"><span data-stu-id="beb34-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="beb34-111">สำหรับข้อมูลเพิ่มเติม ดู [นำโพรไฟล์ไปใช้โดยใช้โปรแกรมการวางแผนงาน](https://technet.microsoft.com/library/aa551234.aspx)</span><span class="sxs-lookup"><span data-stu-id="beb34-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="beb34-112">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าตอนฟิกขั้นตอน โปรดดู [ตั้งค่าเวลาและการเข้างาน](https://technet.microsoft.com/library/aa496971.aspx)</span><span class="sxs-lookup"><span data-stu-id="beb34-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="beb34-113">การตั้งค่าคอนฟิกเฉพาะทางการค้า</span><span class="sxs-lookup"><span data-stu-id="beb34-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="beb34-114">เปิดใช้งานโพรไฟล์ฟังก์ชันสำหรับนาฬิกาตอกบัตร สำหรับผู้ปฏิบัติงานที่คุณต้องการเปิดใช้งานสำหรับการลงทะเบียนเวลา</span><span class="sxs-lookup"><span data-stu-id="beb34-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="beb34-115">คลิก **โพรไฟล์ฟังก์ชัน POS** &gt; **ฟังก์ชัน** &gt; **การลงทะเบียนเวลา POS** &gt; **เปิดใช้งานการลงทะเบียนเวลา**</span><span class="sxs-lookup"><span data-stu-id="beb34-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="beb34-116">ตั้งค่าคอนฟิกกลุ่มสิทธิ์การขายหน้าร้าน (POS) เพื่อเปิดใช้งานสิทธิ์การดูรายการของนาฬิกาตอกบัตร</span><span class="sxs-lookup"><span data-stu-id="beb34-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="beb34-117">สิทธิ์นี้ช่วยให้ผู้ใช้สามารถดูการลงทะเบียนนาฬิกาตอกบัตรของผู้ปฏิบัติงานอื่นๆในร้านค้า (และจากร้านค้าอื่นๆที่เกี่ยวข้องกับผู้ใช้ผ่านทางสมุดที่อยู่)</span><span class="sxs-lookup"><span data-stu-id="beb34-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="beb34-118">คุณอาจต้องการเปิดใช้งานสิทธิ์นี้สำหรับบทบาทผู้จัดการ แต่ไม่ใช่สำหรับบทบาทพนักงานเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="beb34-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="beb34-119">คลิก **กลุ่มสิทธิ์ของ POS** &gt; **ดูรายการของนาฬิกาตอกบัตร**</span><span class="sxs-lookup"><span data-stu-id="beb34-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="beb34-120">ลงทะเบียนเวลา</span><span class="sxs-lookup"><span data-stu-id="beb34-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="beb34-121">การลงทะเบียนเวลาพนักงานเก็บเงินและไม่ใช่พนักงานเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="beb34-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="beb34-122">ใน POS:</span><span class="sxs-lookup"><span data-stu-id="beb34-122">On POS:</span></span>

    - <span data-ttu-id="beb34-123">การดำเนินการตอกบัตรเข้า:</span><span class="sxs-lookup"><span data-stu-id="beb34-123">Clock-in operations:</span></span>

        - <span data-ttu-id="beb34-124">เข้าสู่ระบบด้วยการดำเนินงานไม่มีลิ้นชักหรือกะใหม่</span><span class="sxs-lookup"><span data-stu-id="beb34-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="beb34-125">เลือกการดำเนินงานของนาฬิกาตอกบัตร</span><span class="sxs-lookup"><span data-stu-id="beb34-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="beb34-126">เลือกการดำเนินงานที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="beb34-126">Select a desired operation:</span></span>

            - <span data-ttu-id="beb34-127">การตอกบัตรเข้า</span><span class="sxs-lookup"><span data-stu-id="beb34-127">Clock-in</span></span>
            - <span data-ttu-id="beb34-128">หยุดพักจากงาน</span><span class="sxs-lookup"><span data-stu-id="beb34-128">Break for Work</span></span>
            - <span data-ttu-id="beb34-129">หยุดพักกลางวัน</span><span class="sxs-lookup"><span data-stu-id="beb34-129">Break for Lunch</span></span>
            - <span data-ttu-id="beb34-130">การตอกบัตรออก</span><span class="sxs-lookup"><span data-stu-id="beb34-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="beb34-131">สถานะปัจจุบัน:</span><span class="sxs-lookup"><span data-stu-id="beb34-131">Current state</span></span></th>
        <th><span data-ttu-id="beb34-132">การดำเนินงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="beb34-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="beb34-133">การตอกบัตรเข้า</span><span class="sxs-lookup"><span data-stu-id="beb34-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="beb34-134">หยุดพักจากงาน</span><span class="sxs-lookup"><span data-stu-id="beb34-134">Break for Work</span></span></li>
        <li><span data-ttu-id="beb34-135">หยุดพักกลางวัน</span><span class="sxs-lookup"><span data-stu-id="beb34-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="beb34-136">การตอกบัตรออก</span><span class="sxs-lookup"><span data-stu-id="beb34-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="beb34-137">หยุดพักจากงาน</span><span class="sxs-lookup"><span data-stu-id="beb34-137">Break for Work</span></span></td>
        <td><span data-ttu-id="beb34-138">การตอกบัตรเข้า</span><span class="sxs-lookup"><span data-stu-id="beb34-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="beb34-139">หยุดพักกลางวัน</span><span class="sxs-lookup"><span data-stu-id="beb34-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="beb34-140">การตอกบัตรเข้า</span><span class="sxs-lookup"><span data-stu-id="beb34-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="beb34-141">การตอกบัตรออก</span><span class="sxs-lookup"><span data-stu-id="beb34-141">Clock-out</span></span></td>
        <td><span data-ttu-id="beb34-142">การตอกบัตรเข้า</span><span class="sxs-lookup"><span data-stu-id="beb34-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="beb34-143">[![สถานะของนาฬิกาตอกบัตร](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="beb34-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="beb34-144">ดูข้อความยืนยัน และตรวจสอบว่าเวลาของกิจกรรมปัจจุบันถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="beb34-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="beb34-145">ล็อกบุ๊ค:</span><span class="sxs-lookup"><span data-stu-id="beb34-145">Logbook:</span></span>

    - <span data-ttu-id="beb34-146">คลิก **ล็อกบุ๊ค** เพื่อดูกิจกรรมของนาฬิกาตอกบัตร</span><span class="sxs-lookup"><span data-stu-id="beb34-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="beb34-147">ใช้ตัวกรองเวลาเพื่อเลือกหน้าต่างเวลาที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="beb34-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="beb34-148">ถ้าคุณทำงานในตำแหน่งที่ตั้งของร้านค้าหลายแห่ง คุณจะเห็นการลงทะเบียนเวลาของคุณจากร้านค้าทั้งหมดที่คุณทำการบันทึกเวลา</span><span class="sxs-lookup"><span data-stu-id="beb34-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="beb34-149">คุณสามารถใช้ตัวกรองข้อมูลร้านค้าเพื่อดูการลงทะเบียนเวลาจากร้านค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="beb34-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="beb34-150">โซนเวลาที่แตกต่างกัน:</span><span class="sxs-lookup"><span data-stu-id="beb34-150">Different time zones:</span></span>

    - <span data-ttu-id="beb34-151">ถ้าคุณดูเวลาจากตำแหน่งที่ตั้งที่แตกต่างกัน (สำหรับล็อกบุ๊คพนักงานเก็บเงิน หรือโดยการใช้ **ดูรายการของนาฬิกาตอกบัตร** สำหรับสถานการณ์จำลองของผู้จัดการฝ่าย) และตำแหน่งที่ตั้งนั้นอยู่ในโซนเวลาที่แตกต่างกัน เรกคอร์ดเวลาที่คุณเห็นจะถูกแปลงเป็นโซนเวลาท้องถิ่นของคุณ</span><span class="sxs-lookup"><span data-stu-id="beb34-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="beb34-152">ตัวอย่างเช่น คุณเป็นผู้จัดการสำหรับร้านค้าสองร้าน ร้านหนึ่งในแอริโซนา และอีกร้านหนึ่งในเนวาดา</span><span class="sxs-lookup"><span data-stu-id="beb34-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="beb34-153">พนักงานเก็บเงินลงทะเบียนการตอกเวลาที่เวลา 9:00 น.</span><span class="sxs-lookup"><span data-stu-id="beb34-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="beb34-154">ในแอริโซนา</span><span class="sxs-lookup"><span data-stu-id="beb34-154">in Arizona.</span></span> <span data-ttu-id="beb34-155">ในขณะนั้น เวลาในเนวาดาเป็น 8:00 น.</span><span class="sxs-lookup"><span data-stu-id="beb34-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="beb34-156">ดังนั้น ถ้าคุณอยู่ในร้านที่เนวาดาและดูเรกคอร์ดการลงทะเบียนเวลา การลงทะเบียนเวลาจะถูกทำเครื่องหมายเป็น 8:00 น.</span><span class="sxs-lookup"><span data-stu-id="beb34-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="beb34-157">ดูการลงทะเบียนเวลาของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="beb34-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="beb34-158">ดูการลงทะเบียนเวลาของผู้ปฏิบัติงาน และกรองข้อมูลตามชนิดของร้านค้าหรือกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="beb34-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="beb34-159">ใน POS:</span><span class="sxs-lookup"><span data-stu-id="beb34-159">On POS:</span></span>

- <span data-ttu-id="beb34-160">เลือก **ดูรายการของนาฬิกาตอกบัตร**</span><span class="sxs-lookup"><span data-stu-id="beb34-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="beb34-161">คุณดูกิจกรรมการลงทะเบียนนาฬิกาตอกบัตรจากพนักงานทั้งหมดที่ถูกกำหนดให้กับร้านค้าเดียวกันกับที่คุณได้รับมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="beb34-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="beb34-162">คุณสามารถใช้ชนิดของกิจกรรม และเก็บตัวกรองเพื่อกรองข้อมูลสำหรับการลงทะเบียนเวลา</span><span class="sxs-lookup"><span data-stu-id="beb34-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="beb34-163">ประมวลผลและจัดการการลงทะเบียนเวลา</span><span class="sxs-lookup"><span data-stu-id="beb34-163">Process and manage time registrations</span></span>

<span data-ttu-id="beb34-164">ผู้ใช้การค้าติดตามลำดับงานเพื่อคำนวณ อนุมัติ และโอนย้ายการลงทะเบียนเวลาไปยังระบบค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="beb34-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="beb34-165">การดำเนินงานหลัก</span><span class="sxs-lookup"><span data-stu-id="beb34-165">Primary operations</span></span>

- <span data-ttu-id="beb34-166">คำนวณ</span><span class="sxs-lookup"><span data-stu-id="beb34-166">Calculate</span></span>
- <span data-ttu-id="beb34-167">อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="beb34-167">Approve</span></span>
- <span data-ttu-id="beb34-168">ส่งไปที่ค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="beb34-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="beb34-169">การดำเนินงานทั่วไปอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="beb34-169">Other common operations</span></span>

- <span data-ttu-id="beb34-170">การตอกบัตรออกจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="beb34-170">Bulk Clock-out</span></span>
- <span data-ttu-id="beb34-171">ลงทะเบียนการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="beb34-171">Register Absence</span></span>

<span data-ttu-id="beb34-172">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการลงทะเบียนเวลาและการเข้างานของกระบวนการ ดู [ประมวลผลการลงทะเบียนเวลาและการเข้างาน](https://technet.microsoft.com/library/aa573180.aspx)</span><span class="sxs-lookup"><span data-stu-id="beb34-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]