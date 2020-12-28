---
title: สร้างปฏิทินเวลาทำงาน
description: กำหนดปฏิทินเวลาทำงาน วันหยุด และเวลาที่ไม่ได้ทำงานใน Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2bedbe65f146c4159c2a809de8f683815fd4a01f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420744"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="2a10c-103">สร้างปฏิทินเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="2a10c-103">Create a working time calendar</span></span>

<span data-ttu-id="2a10c-104">ปฏิทินเวลาทำงานใน Dynamics 365 Human Resources แสดงวันและชั่วโมงที่พนักงานทำงานในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a10c-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="2a10c-105">เมื่อพนักงานส่งคำขอการเวลาหยุดพัก พนักงานไม่ต้องกังวลเกี่ยวกับวันหยุดและการปิดทำการ</span><span class="sxs-lookup"><span data-stu-id="2a10c-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="2a10c-106">เมื่อต้องการปรับปรุงการร้องขอเวลาหยุดพักให้ตั้งค่าคอนฟิกรายการเหล่านี้สำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a10c-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="2a10c-107">ปฏิทินเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="2a10c-107">Working time calendar</span></span>
- <span data-ttu-id="2a10c-108">วันหยุดและการปิดทำการ</span><span class="sxs-lookup"><span data-stu-id="2a10c-108">Holidays and closures</span></span>
- <span data-ttu-id="2a10c-109">เวลาที่ไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="2a10c-109">Non-work time</span></span>

<span data-ttu-id="2a10c-110">คุณสามารถเพิ่มรายการสองรายการในขณะที่คุณกำลังตั้งค่าปฏิทินเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="2a10c-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="2a10c-111">นอกจากนี้คุณยังสามารถตั้งค่าคอนฟิกหรืออัพเดตได้โดยแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="2a10c-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="2a10c-112">ตั้งค่าปฏิทินเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="2a10c-112">Set up a working time calendar</span></span>

<span data-ttu-id="2a10c-113">ตั้งค่าปฏิทินเวลาทำงานอย่างน้อยหนึ่งปฏิทินที่แสดงวันและชั่วโมงของการดำเนินงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a10c-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="2a10c-114">ถ้าคุณมีสถานที่ในหลายประเทศและภูมิภาคคุณอาจต้องการที่จะตั้งค่าปฏิทินเวลาการทำงานสำหรับแต่ละพื้นที่</span><span class="sxs-lookup"><span data-stu-id="2a10c-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="2a10c-115">ในหน้า **การจัดการองค์กร** เลือก **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="2a10c-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="2a10c-116">เลือก **ใหม่** และป้อนชื่อและคำอธิบายสำหรับปฏิทินของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a10c-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="2a10c-117">ภายใต้ **ตัวเลือกการสร้าง** ให้เลือกวันทำงานสำหรับองค์กรของคุณและป้อนเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="2a10c-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="2a10c-118">เมื่อต้องการเพิ่มวันหยุดหรือปิดทำการให้เลือกปุ่ม **เพิ่ม** ที่อยู่ถัดจาก **วันหยุดและการปิดทำการ**</span><span class="sxs-lookup"><span data-stu-id="2a10c-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="2a10c-119">เมื่อต้องการเพิ่มเวลาที่ไม่ทำงานเช่นพักกลางวันหรือพักทานของว่าง ให้เลือก **เพิ่ม** ภายใต้ **เวลาที่ไม่ทำงาน** แล้วป้อนชื่อและช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="2a10c-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="2a10c-120">ภายใต้ **วัน** เลือก **สร้าง** เพื่อสร้างวันในปฏิทินของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a10c-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="2a10c-121">ป้อนช่วงวันที่สำหรับปฏิทินของคุณแล้วเลือก **สร้างวัน**</span><span class="sxs-lookup"><span data-stu-id="2a10c-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="2a10c-122">ถ้าต้องการเพิ่มกำหนดการทำงานภายใต้ **กำหนดการทำงาน** ให้เลือก **เพิ่ม** แล้วป้อนเวลาสำหรับแต่ละกำหนดการทำงาน</span><span class="sxs-lookup"><span data-stu-id="2a10c-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="2a10c-123">ตั้งค่าคอนฟิกวันหยุดและการปิดทำการ</span><span class="sxs-lookup"><span data-stu-id="2a10c-123">Configure holidays and closures</span></span>

<span data-ttu-id="2a10c-124">คุณสามารถเพิ่มหรือเปลี่ยนแปลงวันหยุดและการปิดทำการแยกต่างหากจากปฏิทินเวลาทำงานได้</span><span class="sxs-lookup"><span data-stu-id="2a10c-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="2a10c-125">ในหน้า **การจัดการองค์กร** เลือก **วันหยุดและปิดทำการ**</span><span class="sxs-lookup"><span data-stu-id="2a10c-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="2a10c-126">เลือก **ใหม่** และป้อนชื่อและวันที่คำอธิบายสำหรับวันหยุดและปิดทำการ</span><span class="sxs-lookup"><span data-stu-id="2a10c-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="2a10c-127">ตั้งค่าคอนฟิกเวลาที่ไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="2a10c-127">Configure non-work time</span></span>

<span data-ttu-id="2a10c-128">คุณสามารถเพิ่มหรือเปลี่ยนแปลงวันที่ไม่ทำงานแยกต่างหากจากปฏิทินเวลาทำงานได้</span><span class="sxs-lookup"><span data-stu-id="2a10c-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="2a10c-129">ในหน้า **การจัดการองค์กร** เลือก **เวลาที่ไม่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="2a10c-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="2a10c-130">เลือก **ใหม่** และป้อนชื่อและช่วงเวลาสำหรับเวลาที่ไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="2a10c-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="2a10c-131">ถ้าคุณได้เปิดใช้งานคุณลักษณะตัวอย่างการแก้ไขวันหยุดของธนาคารการลางานและการขาดงาน ทรัพยากรบุคคลจะใช้วันหยุดและเวลาปิดทำการเพื่อกำหนดจำนวนวันที่จะปรับปรุงสำหรับพนักงานที่ลงทะเบียนในปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="2a10c-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a10c-132">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="2a10c-132">See also</span></span>

- [<span data-ttu-id="2a10c-133">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="2a10c-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="2a10c-134">ตั้งค่าคอนฟิกชนิดการลางานและการหยุดงาน</span><span class="sxs-lookup"><span data-stu-id="2a10c-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
