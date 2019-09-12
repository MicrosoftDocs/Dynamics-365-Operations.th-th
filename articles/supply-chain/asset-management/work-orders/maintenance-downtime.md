---
title: การหยุดทำงานของการบำรุงรักษา
description: หัวข้อนี้อธิบายถึงการหยุดทำงานของการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918255"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="f35fd-103">การหยุดทำงานของการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="f35fd-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="f35fd-104">คุณสามารถสร้างการลงทะเบียนการหยุดทำงานของการบำรุงรักษาบนสินทรัพย์ที่ถูกเลือกบนใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="f35fd-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="f35fd-105">การทำเช่นนี้มีประโยชน์ถ้าคุณต้องการลงทะเบียนการหยุดทำงานการบำรุงรักษาบนเครื่องจักรหนึ่งเครื่องหรือหลายเครื่องขึ้นไปในพื้นที่การผลิต</span><span class="sxs-lookup"><span data-stu-id="f35fd-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="f35fd-106">ขั้นแรก คุณสร้างรหัสเหตุผลของการหยุดการทำงานของการบำรุงรักษาที่คุณต้องการใช้ ตัวอย่างเช่น การแบ่งงาน และการหยุดวางแผน</span><span class="sxs-lookup"><span data-stu-id="f35fd-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="f35fd-107">ซึ่งจะกระทำภายใน **รหัสเหตุผลการหยุดการทำงานของการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="f35fd-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="f35fd-108">ขั้นตอนถัดไป คุณสามารถสร้างการลงทะเบียนการหยุดทำงานของการบำรุงรักษาใน **การหยุดการทำงานของการบำรุงรักษา** เเละเพิ่มรหัสเหตุผลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f35fd-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="f35fd-109">สร้างรหัสเหตุผลการหยุดทำงานของการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="f35fd-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="f35fd-110">คลิก **การจัดการสินทรัพย์** > **การตั้งค่า** > **ใบสั่งงาน** > **รหัสเหตุผลการหยุดการทำงานของการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="f35fd-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="f35fd-111">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f35fd-111">Click **New**.</span></span>

3. <span data-ttu-id="f35fd-112">แทรกรหัสในฟิลด์ **รหัสเหตุผลการหยุดการทำงานของการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="f35fd-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="f35fd-113">เเทรกชื่อสำหรับรหัสเหตุผลในฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="f35fd-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="f35fd-114">เลือกกล่องกาเครื่องหมาย **รวม KPI** ถ้าควรรวมรหัสเหตุผลในการคำนวณ KPI ของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="f35fd-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="f35fd-115">โดยทั่วไปแล้ว การหยุดเเผนการผลิตไม่ควรรวมอยู่ในการคำนวณ KPI เนื่องจากไม่มีผลกระทบต่อประสิทธิภาพการทำงานที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="f35fd-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="f35fd-116">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f35fd-116">Click **Save**.</span></span>

![รูปที่ 1](media/15-work-orders.png)


<span data-ttu-id="f35fd-118">เมื่อคุณได้สร้างรหัสเหตุผลการหยุดทำงานของการบำรุงรักษาที่คุณต้องการใช้แล้ว คุณสามารถสร้างการลงทะเบียนการหยุดทำงานของการบำรุงรักษาสำหรับใบสั่งงาน เเละสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="f35fd-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="f35fd-119">สร้างการลงทะเบียนการหยุดทำงานของการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="f35fd-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="f35fd-120">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="f35fd-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f35fd-121">เลือกใบสั่งงาน และคลิก **การหยุดการทำงานของการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="f35fd-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="f35fd-122">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f35fd-122">Click **New**.</span></span>

4. <span data-ttu-id="f35fd-123">แทรกช่วงวันที่ เเละเวลาสำหรับการลงทะเบียนการหยุดทำงานของการบำรุงรักษาในฟิลด์ **เริ่มต้น** เเละ **สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="f35fd-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="f35fd-124">เมื่อคุณออกจากฟิลด์ **สิ้นสุด** ระยะเวลาในชั่วโมงจะถูกแทรกโดยอัตโนมัติในฟิลด์ **ระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="f35fd-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="f35fd-125">เลือกรหัสเหตุผลในฟิลด์ **รหัสเหตุผลการหยุดการทำงานของการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="f35fd-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="f35fd-126">ทำซ้ำขั้นตอนที่ 3-6 ถ้าคุณต้องการการลงทะเบียนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f35fd-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="f35fd-127">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f35fd-127">Click **Save**.</span></span>


![รูปที่ 2](media/16-work-orders.png)


<span data-ttu-id="f35fd-129">ปฏิทินที่ใช้ในการคำนวณการลงทะเบียนการหยุดทำงานของการบำรุงรักษาจะขึ้นอยู่กับการเลือกของคุณในการตั้งค่าสินทรัพย์ และพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="f35fd-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="f35fd-130">ถ้ามีการเลือกทรัพยากรไว้บนสินทรัพย์ใน **สินทรัพย์ทั้งหมด** > **สินทรัพย์ถาวร** เเท็บด่วน > **ทรัพยากร** ฟิลด์ การตั้งค่าปฏิทินสำหรับกลุ่มทรัพยากรเชื่อมโยงที่ใช้ ดังที่เเสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f35fd-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![รูปที่ 3](media/17-work-orders.png)


<span data-ttu-id="f35fd-132">ถ้าไม่มีทรัพยากรถูกเลือกบนสินทรัพย์ ปฏิทินมาตราฐานจะถูกเลือกใน **พารามิเตอร์การจัดการสินทรัพย์** ที่ใช้ ดังที่เเสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f35fd-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![รูปที่ 4](media/18-work-orders.png)


<span data-ttu-id="f35fd-134">คลิก **การจัดการสินทรัพย์องค์กร** > **การสอบถาม** > **การหยุดทำงานของการบำรุงรักษา** เพื่อดูภาพรวมของการลงทะเบียนการหยุดทำงานของการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="f35fd-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="f35fd-135">ปฏิทินทั้งหมดที่ใช้ในโมดูล **การจัดการสินทรัพย์** ถูกตั้งค่าใน **การจัดการองค์กร** > **การตั้งค่า** > **ปฏิทิน** > **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="f35fd-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

