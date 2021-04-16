---
title: การหยุดทำงานของการบำรุงรักษาสำหรับใบสั่งงาน
description: หัวข้อนี้อธิบายวิธีการสร้างการลงทะเบียนการหยุดทำงานของการบำรุงรักษาบนสินทรัพย์ที่มีการเลือกบนใบสั่งงาน
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5c0c584ed53dc4ec8a761065838127dc67cbc41e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813736"
---
# <a name="maintenance-downtime-for-work-orders"></a><span data-ttu-id="96e20-103">การหยุดทำงานของการบำรุงรักษาสำหรับใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="96e20-103">Maintenance downtime for work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="96e20-104">คุณสามารถสร้างการลงทะเบียนการหยุดทำงานของการบำรุงรักษาบนสินทรัพย์ที่มีการเลือกบนใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="96e20-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="96e20-105">ความสามารถนี้มีประโยชน์หากคุณต้องการลงทะเบียนการหยุดทำงานของการบำรุงรักษาบนเครื่องจักรหนึ่งเครื่องหรือหลายเครื่องขึ้นไปในพื้นที่การผลิต</span><span class="sxs-lookup"><span data-stu-id="96e20-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="96e20-106">ให้คุณสร้างรหัสเหตุผลของการหยุดการทำงานของการบำรุงรักษาที่คุณต้องการใช้ก่อน เช่น **การแบ่งงาน** และ **การหยุดที่วางแผนไว้**</span><span class="sxs-lookup"><span data-stu-id="96e20-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="96e20-107">ขั้นตอนนี้จะดำเนินการบนเพจ **รหัสเหตุผลการหยุดการทำงานของการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="96e20-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="96e20-108">คุณสามารถสร้างการลงทะเบียนการหยุดทำงานของการบำรุงรักษาต่อไปบนเพจ **การหยุดการทำงานของการบำรุงรักษา** เเละเพิ่มรหัสเหตุผลการหยุดทำงานของการบำรุงรักษาที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="96e20-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="96e20-109">สร้างรหัสเหตุผลการหยุดทำงานของการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="96e20-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="96e20-110">เลือก **การจัดการสินทรัพย์** > **การตั้งค่า** > **ใบสั่งงาน** > **รหัสเหตุผลการหยุดการทำงานของการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="96e20-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="96e20-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="96e20-111">Select **New**.</span></span>

3. <span data-ttu-id="96e20-112">ในฟิลด์ **รหัสเหตุผลการหยุดทำงานของการบำรุงรักษา** ให้ป้อนรหัสสำหรับเหตุผลการหยุดทำงานของการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="96e20-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="96e20-113">ในฟิลด์ **ชื่อ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="96e20-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="96e20-114">เลือกกล่องกาเครื่องหมาย **รวม KPI** หากรหัสเหตุผลควรมีการรวมในการคำนวณของตัวบ่งชี้ประสิทธิภาพการทำงานหลัก (KPI) สำหรับสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="96e20-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="96e20-115">โดยทั่วไป การหยุดเเผนการผลิตไม่ควรรวมอยู่ในการคำนวณ KPI เนื่องจากไม่มีผลกระทบต่อประสิทธิภาพการทำงานที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="96e20-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="96e20-116">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="96e20-116">Select **Save**.</span></span>

<span data-ttu-id="96e20-117">ภาพประกอบต่อไปนี้แสดงตัวอย่างของเพจ **รหัสเหตุผลการหยุดทำงานของการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="96e20-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![รูปที่ 1](media/15-work-orders.png)

<span data-ttu-id="96e20-119">หลังจากที่คุณได้สร้างรหัสเหตุผลการหยุดทำงานของการบำรุงรักษาที่คุณต้องการใช้แล้ว คุณสามารถสร้างการลงทะเบียนการหยุดทำงานของการบำรุงรักษาสำหรับใบสั่งงาน เเละสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="96e20-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="96e20-120">สร้างการลงทะเบียนการหยุดทำงานของการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="96e20-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="96e20-121">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="96e20-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="96e20-122">เลือกใบสั่งงาน จากนั้น บนแท็บ **ใบสั่งงาน** ในกลุ่ม **สินทรัพย์** ให้เลือก **การหยุดทำงานของการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="96e20-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="96e20-123">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="96e20-123">Select **New**.</span></span>

4. <span data-ttu-id="96e20-124">ในฟิลด์ **เริ่มต้น** เเละ **สิ้นสุด** กำหนดช่วงวันที่และเวลาสำหรับการลงทะเบียนการหยุดทำงานของการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="96e20-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="96e20-125">เมื่อคุณออกจากฟิลด์ **สิ้นสุด** ระยะเวลาในชั่วโมงจะถูกแทรกโดยอัตโนมัติในฟิลด์ **ระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="96e20-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="96e20-126">ในฟิลด์ **รหัสเหตุผลการหยุดการทำงานของการบำรุงรักษา** ให้เลือกรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="96e20-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="96e20-127">ทำซ้ำขั้นตอนที่ 3 ถึง 5 หากต้องการเพิ่มการลงทะเบียนอีก</span><span class="sxs-lookup"><span data-stu-id="96e20-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="96e20-128">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="96e20-128">Select **Save**.</span></span>

<span data-ttu-id="96e20-129">แผนภาพด้านล่างแสดงตัวอย่างของการลงทะเบียนการหยุดทำงานของการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="96e20-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![รูปที่ 2](media/16-work-orders.png)

<span data-ttu-id="96e20-131">ปฏิทินที่ใช้ในการคำนวณการลงทะเบียนการหยุดทำงานของการบำรุงรักษาจะขึ้นอยู่กับการเลือกของคุณในการตั้งค่าสินทรัพย์และพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="96e20-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="96e20-132">หากมีการเลือกทรัพยากรไว้บนสินทรัพย์ในฟิลด์ **ทรัพยากร** บนแท็บด่วน **สินทรัพย์ถาวร** ของเพจ **สินทรัพย์ทั้งหมด** ปฏิทินที่มีการตั้งค่าสำหรับกลุ่มทรัพยากรเชื่อมโยงที่ใช้ ตามที่เเสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="96e20-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![รูปที่ 3](media/17-work-orders.png)

<span data-ttu-id="96e20-134">ถ้าไม่มีทรัพยากรถูกเลือกบนสินทรัพย์ ปฏิทินมาตรฐานจะมีการเลือกบนเพจ **พารามิเตอร์การจัดการสินทรัพย์** ที่ใช้ ตามที่เเสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="96e20-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![รูปที่ 4](media/18-work-orders.png)

<span data-ttu-id="96e20-136">ในการดูภาพรวมของการลงทะเบียนการหยุดทำงานของการบำรุงรักษา ให้คลิก **การจัดการสินทรัพย์องค์กร** > **การสอบถาม** > **การหยุดทำงานของการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="96e20-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="96e20-137">ปฏิทินทั้งหมดที่มีการใช้ในโมดูล **การจัดการสินทรัพย์** ถูกตั้งค่าใน **การจัดการองค์กร** > **การตั้งค่า** > **ปฏิทิน** > **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="96e20-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]