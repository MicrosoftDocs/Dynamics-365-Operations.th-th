---
title: รอบการบำรุงรักษา
description: หัวข้อนี้ อธิบายถึงรอบการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.openlocfilehash: eca732f245650c8e1f3dc976454536a0ab1ee117
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922033"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="d3136-103">รอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="d3136-104">ใน **การจัดการสินทรัพย์** คุณสามารถสร้างรอบการบำรุงรักษาสำหรับสินทรัพย์ต่างๆ ซึ่งคุณจำเป็นต้องดำเนินงานที่คล้ายกันในช่วงเวลาปกติ</span><span class="sxs-lookup"><span data-stu-id="d3136-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="d3136-105">ตัวอย่าง เช่น งานหล่อลื่นหรืองานการตรวจสอบความปลอดภัย ที่จำเป็นต้องดำเนินการกับเครื่องจักรจำนวนมากภายในช่วงเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d3136-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="d3136-106">ขั้นตอนแรก คือสร้างรอบการบำรุงรักษา รวมถึงสินทรัพย์ที่จำเป็นต้องใช้ฟอร์มเดียวกันของงานการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="d3136-107">ถัดไป คุณจัดกำหนดการรอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="d3136-108">เมื่อคุณจัดกำหนดการรอบการบำรุงรักษาเสร็จเรียบร้อยแล้ว คุณสามารถดูเรกคอร์ดงานทั้งหมดที่เกี่ยวข้องกับรอบ ใน **กำหนดการบำรุงรักษาทั้งหมด** และ **รายการกำหนดการบำรุงรักษาแบบเปิด**</span><span class="sxs-lookup"><span data-stu-id="d3136-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="d3136-109">รอบการบำรุงรักษายังสามารถตั้งค่าบนตำแหน่งที่ทำงานที่จะดำเนินการให้เสร็จสมบูรณ์ในสินทรัพย์ที่ติดตั้งบนตำแหน่งที่ทำงาน ในขณะที่มีการสร้างใบสั่งงานตามรอบ</span><span class="sxs-lookup"><span data-stu-id="d3136-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="d3136-110">อ้างถึง [การสร้างตำแหน่งที่ทำงาน](../functional-locations/create-functional-locations.md) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่ารอบการบำรุงรักษาบนตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="d3136-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="d3136-111">การตั้งค่ารอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="d3136-112">คลิก **การจัดการสินทรัพย์** > **ตั้งค่า** > **การบำรุงรักษาเชิงป้องกัน** > **รอบการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="d3136-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="d3136-113">คลิก **ใหม่** เพื่อสร้างรอบการบำรุงรักษาใหม่</span><span class="sxs-lookup"><span data-stu-id="d3136-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="d3136-114">ใส่รหัสในฟิลด์ **รอบการบำรุงรักษา** และชื่อสำหรับรอบการบำรุงรักษาในฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="d3136-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="d3136-115">เลือกวันที่เริ่มต้นสำหรับรอบ ในฟิลด์ **วันเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="d3136-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="d3136-116">ในฟิลด์ **เสร็จสิ้นภายในวัน** และฟิลด์ **เสร็จสิ้นภายในชั่วโมง** คุณสามารถแทรกวันที่สิ้นสุดที่คาดไว้เป็นวันหรือชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="d3136-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="d3136-117">วันที่สิ้นสุดที่คาดไว้จะถูกคำนวณให้สอดคล้องกับวันที่เริ่มต้น ซึ่งจะคำนวณเมื่อมีการสร้างรายการกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="d3136-118">ตัวอย่าง เช่น คุณสามารถใส่ "7" ในฟิลด์ **"เสร็จสิ้นภายในจำนวนวัน** เพื่อบ่งชี้ว่างานที่เกี่ยวข้องควรมีการดำเนินการให้เสร็จสมบูรณ์ภายในหนึ่งสัปดาห์นับจากวันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d3136-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="d3136-119">เลือก "ใช่" บนปุ่มสลับ **สร้างอัตโนมัติ** หากใบสั่งงานควรมีการสร้างขึ้นโดยอัตโนมัติ จากรายการกำหนดการบำรุงรักษาที่สร้างจากรอบการบำรุงรักษานี้</span><span class="sxs-lookup"><span data-stu-id="d3136-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="d3136-120">ในฟิลด์ **ชนิดของใบสั่งงาน** เลือกชนิดของใบสั่งงานที่จะใช้ในใบสั่งงานที่สร้างขึ้นจากรอบการบำรุงรักษานี้</span><span class="sxs-lookup"><span data-stu-id="d3136-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="d3136-121">ในฟิลด์ **ระดับการบริการ** เลือกระดับการบริการของใบสั่งงานที่จะใช้ในใบสั่งงานที่สร้างขึ้นจากรอบการบำรุงรักษานี้</span><span class="sxs-lookup"><span data-stu-id="d3136-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="d3136-122">บนแท็บด่วน **รายการสินทรัพย์** คลิก **เพิ่ม** เพื่อเพิ่มสินทรัพย์ให้กับรอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="d3136-123">หมายเลขรายการที่ใส่เข้ามาโดยอัตโนมัติ ในฟิลด์ **หมายเลขรายการ** เพื่อระบุลำดับของสินทรัพย์ในรอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="d3136-124">เลือกสินทรัพย์ ในฟิลด์ **สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="d3136-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="d3136-125">เลือก ชนิดงานบำรุงรักษาสำหรับสินทรัพย์ ในฟิลด์ **ชนิดงานบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="d3136-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="d3136-126">หากจำเป็น เลือก **ตัวแปรชนิดของงานบำรุงรักษา** และ **ความเชี่ยวชาญ** ที่เกี่ยวข้องกับชนิดงานการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="d3136-127">เลือกการเกิดซ้ำ (วัน สัปดาห์ ฯลฯ) ในฟิลด์ **ชนิดของรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="d3136-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="d3136-128">ในฟิลด์ **ความถี่ของรอบระยะเวลา** ให้ใส่จำนวนของการเกิดซ้ำสำหรับรอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="d3136-129">ตัวอย่าง: หากคุณได้เลือก "วัน" ในฟิลดื **ชนิดของรอบระยะเวลา** และคุณใส่หมายเลข "7" ในฟิลด์นี้ จะมีการสร้างรายการรอบการบำรุงรักษาใหม่ ระหว่างการจัดกำหนดการบำรุงรักษาเชิงป้องกันสัปดาห์ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="d3136-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="d3136-130">เลือกวันที่เริ่มต้นสำหรับสินทรัพย์ที่จะรวมไว้ในรอบการบำรุงรักษา ในฟิลด์ **วันที่เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="d3136-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="d3136-131">วันที่นี้อาจแตกต่างจากวันที่เริ่มต้นที่ตั้งค่าไว้ในรอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="d3136-132">ทำซ้ำขั้นตอนที่ 9 ถึง 16 เพื่อเพิ่มสินทรัพย์ให้กับรอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="d3136-133">บนแท็บด่วน **รายการสถานที่ทำงาน** คลิก **เพิ่ม** เพื่อเพิ่มสถานที่ทำงานไปยังรอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="d3136-134">อ้างถึงคำอธิบายของฟิลด์ที่เกี่ยวข้องด้านบน</span><span class="sxs-lookup"><span data-stu-id="d3136-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="d3136-135">ฟิลด์เดียวกันมีพร้อมใช้งานสำหรับการสร้างรายการสินทรัพย์ แต่คุณยังสามารถเลือก **ผู้ผลิต** และ **แบบจำลอง** สำหรับสถานที่ทำงานได้หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d3136-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="d3136-136">หากคุณเลือกสถานที่ทำงานบนรายการ แต่ไม่มีการเลือกใน **ชนิดสินทรัพย์** **ผู้ผลิต** **แบบจำลอง** **ชนิดของงานการบำรุงรักษษ** **ตัวแปรของชนิดของงานการบำรุงรักษา** และ **ความเชี่ยวชาญ** สินทรัพย์ทั้งหมดที่เกี่ยวข้องกับสถานที่ทำงาน ณ เวลาของการจัดกำหนดการบำรุงรักษา จะถูกรวมอยู่ในรอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="d3136-137">บนแท็บด่วน **กลุ่ม** คลิก **เพิ่ม** เพื่อเลือกกลุ่มใบสั่งงานที่จะรวมไว้ในรอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="d3136-138">กลุ่มใบสั่งงานหลายแห่งสามารถเชื่อมโยงกับรอบการบำรุงรักษาเดียว</span><span class="sxs-lookup"><span data-stu-id="d3136-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="d3136-139">บันทึกการตั้งค่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="d3136-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="d3136-140">ฟิลด์ **สินทรัพย์** และ **รายการ** ที่อยู่ในกลุ่ม **รายละเอียด** บนแท็บด่วน **หัวข้อ** จะแสดงจำนวนรวมของสินทรัพย์และรายการที่เกี่ยวข้องกับรอบการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d3136-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="d3136-141">ภาพด้านล่างแสดงและเป็นตัวอย่างของรอบการบำรุงรักษาที่มีสินทรัพย์สามรายการ</span><span class="sxs-lookup"><span data-stu-id="d3136-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![รูปที่ 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="d3136-143">จัดกำหนดการรอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="d3136-144">เมื่อคุณตั้งค่ารอบการบำรุงรักษาแล้ว คุณดำเนินการกำหนดงานเพื่อกำหนดงานทั้งหมดที่เกี่ยวข้องกับรอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="d3136-145">คลิก **การจัดการสินทรัพย์** > **ประจำงวด** > **การบำรุงรักษาเชิงป้องกัน** > **กำหนดรอบการบำรุงรักษา** หรือ **การจัดการสินทรัพย์** > **ทั่วไป** > **กำหนดการบำรุงรักษา** > **กำหนดการบำรุงรักษาทั้งหมด** หรือ **เปิดรายการกำหนดการบำรุงรักษา** หรือ **เปิดกลุ่มกำหนดการบำรุงรักษส** > เลือกรายการกำหนดการบำรุงรักษา ในรายการ > ปุ่ม **รอบการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="d3136-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="d3136-146">ในฟิลด์ **กลุ่ม** เลือกชนิดของรอบระยะเวลาที่จะใช้สำหรับงานการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="d3136-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="d3136-147">ในฟิลด์ **ความถี่ของรอบระยะเวลา** ใส่จำนวนของรอบระยะเวลาที่จะรวมไว้ในงานการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="d3136-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="d3136-148">วันที่เริ่มต้นกำหนดการคือวันที่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d3136-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="d3136-149">เลือก "ใช่" บนปุ่มสลับ **สร้างอัตโนมัติ** หากใบสั่งงานควรมีการสร้างขึ้นโดยอัตโนมัติโดยใช้รอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="d3136-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="d3136-150">หากปุ่มสลับนี้ถูกตั้งค่าเป็น "ใช่" และปุ่มสลับ **สร้างอัตโนมัติ** ถูกตั้งค่าเป็น "ใช่" บนรอบการบำรุงรักษา ในฟอร์ม **รอบการบำรุงรักษา** ใบสั่งงานจะถูกสร้างขึ้นตามรายการรอบการบำรุงรักษา และรายการกำหนดการบำรุงรักษาที่มีสถานะเป็น "ใบสั่งงานที่สร้าง" ก็จะถูกสร้างด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="d3136-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="d3136-151">หากมีการตั้งค่าปุ่มสลับ **สร้างอัตโนมัติ** เพียงหนึ่งปุ่มเป็น "ใช่" ในรายการแบบหล่นลงนี้ หรือใน **รอบการบำรุงรักษา** เฉพาะรายการกำหนดการบำรุงรักษาเท่านั้นที่มีการสร้างขึ้นโดยมีสถานะเป็น "สร้างแล้ว"</span><span class="sxs-lookup"><span data-stu-id="d3136-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="d3136-152">ในกรณีดังกล่าว จะไม่มีการสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="d3136-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="d3136-153">หากจำเป็น คุณสามารถเลือกรอบที่ระบุหรือวันที่เริ่มต้นอื่นสำหรับงานกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="d3136-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="d3136-154">คลิก **ตัวกรอง** และเพิ่มรอบที่จะรวม</span><span class="sxs-lookup"><span data-stu-id="d3136-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="d3136-155">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d3136-155">Click **OK**.</span></span>

7. <span data-ttu-id="d3136-156">ขณะนี้คุณสามารถดูงานรอบการบำรุงรักษา ใน **การจัดการสินทรัพย์** > **ทั่วไป** > **กำหนดการบำรุงรักษา** > **กำหนดการบำรุงรักษาทั้งหมด** หรือ **รายการกำหนดการบำรุงรักษาแบบเปิด**</span><span class="sxs-lookup"><span data-stu-id="d3136-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="d3136-157">หากรอบกำหนดการบำรุงรักษาเชื่อมโยงกับกลุ่มใบสั่งงาน คุณยังสามารถดูรายการกำหนดการบำรุงรักษา ใน **กลุ่มกำหนดการบำรุงรักษาแบบเปิด**</span><span class="sxs-lookup"><span data-stu-id="d3136-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="d3136-158">รายการกำหนดการบำรุงรักษาที่สร้างจากรอบมีชนิดการอ้างอิง "รอบการบำรุงรักษา"</span><span class="sxs-lookup"><span data-stu-id="d3136-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="d3136-159">ภาพประกอบทั้งสองด้านล่างแสดงการกำหนดงานในกล่องโต้ตอบ **จัดกำหนดการรอบการบำรุงรักษา** และบรรทัดกำหนดการบำรุงรักษาที่สร้างขึ้นใน **กำหนดการบำรุงรักษาทั้งหมด** โดยยึดตามการกำหนดงานนั้น</span><span class="sxs-lookup"><span data-stu-id="d3136-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![รูปที่ 2](media/14-preventive-maintenance.png)

![รูปที่ 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="d3136-162">เมื่อมีการสร้างใบสั่งงานด้วยตนเองในสินทรัพย์ที่ครอบคลุมโดยการรับประกันของผู้จัดจำหน่าย กล่องโต้ตอบจะแสดงขึ้นเพื่อให้ผู้ใช้ทราบถึงการรับประกัน</span><span class="sxs-lookup"><span data-stu-id="d3136-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="d3136-163">จากนั้น การสร้างของใบสั่งงานสามารถถูกยกเลิกได้</span><span class="sxs-lookup"><span data-stu-id="d3136-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="d3136-164">มีการละเว้นการตรวจสอบความสัมพันธ์ของการรับประกันสำหรับใบสั่งงานที่สร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d3136-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="d3136-165">คุณสามารถตั้งค่าชุดงาน บนแท็บด่วน **รันในแบบเบื้องหลัง** เพื่อจัดกำหนดการรอบอย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="d3136-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="d3136-166">หากรอบถูกรวมอยู่ในกลุ่มใบสั่งงานหลายแห่ง (อ้างถึง [กลุ่มใบสั่งงาน](../work-orders/work-order-pools.md)) แต่ละกลุ่มจะแสดงหนึ่งเรกคอร์ด ใน **กลุ่มกำหนดการบำรุงรักษาแบบเปิด**</span><span class="sxs-lookup"><span data-stu-id="d3136-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="d3136-167">การดำเนินการนี้จะทำให้ตัวเลือกการกรองข้อมูลสำหรับกลุ่มใบสั่งงานมีประสิทธิภาพมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="d3136-167">This is done to optimize the filtering options for work order pools.</span></span>

