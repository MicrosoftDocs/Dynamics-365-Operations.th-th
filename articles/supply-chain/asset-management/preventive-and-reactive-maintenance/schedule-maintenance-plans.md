---
title: จัดกำหนดการแผนการบำรุงรักษา
description: หัวข้อนี้อธิบายถึงการจัดกำหนดแผนการบำรุงรักษาในการจัดการสินทรัพย์
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
ms.openlocfilehash: 698888533bf503838f455585f61cc7afc7239b05
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922056"
---
# <a name="schedule-maintenance-plans"></a><span data-ttu-id="eeb05-103">จัดกำหนดการแผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="eeb05-103">Schedule maintenance plans</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="eeb05-104">การจัดกำหนดการบำรุงรักษาเชิงป้องกันสร้างรายการปฏิทินบนสินทรัพย์ตามแผนการบำรุงรักษาที่ตั้งค่าไว้ในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="eeb05-104">Preventive maintenance scheduling generates calendar entries on assets, based on the maintenance plans set up on the assets.</span></span> <span data-ttu-id="eeb05-105">คุณสามารถจัดกำหนดการรายการปฏิทินตามแผนการบำรุงรักษา ชนิดสินทรัพย์ และสินทรัพย์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="eeb05-105">You can schedule calendar entries based on selected maintenance plans, asset types, and assets.</span></span>

1. <span data-ttu-id="eeb05-106">คลิก **การจัดการสินทรัพย์** > **ประจำงวด** > **การบำรุงรักษาเชิงป้องกัน** > **กำหนดการแผนการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="eeb05-106">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance plans**.</span></span>

2. <span data-ttu-id="eeb05-107">คุณสามารถเลือกช่วงเวลาได้ในฟิลด์ **รอบระยะเวลา** และ **ความถี่ของรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="eeb05-107">You can select a time interval in the **Period** and **Period frequency** fields.</span></span>

>[!NOTE]
><span data-ttu-id="eeb05-108">ฟิลด์ **รอบระยะเวลา** และ **ความถี่รอบระยะเวลา** บ่งชี้ถึงระยะเวลาล่วงหน้าที่คุณต้องการให้มีการสร้างรายการกำหนดการบำรุงรักษา ตามแผนการบำรุงรักษาที่คุณสร้างขึ้น (ตามเวลาหรือตามตัวนับ)</span><span class="sxs-lookup"><span data-stu-id="eeb05-108">The **Period** and **Period frequencey** fields indicate how far ahead in time you want maintenance schedule lines to be created, based on the maintenance plans you have created (time-based or counter-based).</span></span> <span data-ttu-id="eeb05-109">ในรูปด้านล่าง รายการกำหนดการบำรุงรักษา (= ข้อเสนอของใบสั่งงาน) จะถูกสร้างขึ้นจากวันที่ปัจจุบันและสามเดือนต่อจากนี้</span><span class="sxs-lookup"><span data-stu-id="eeb05-109">In the figure below, maintenance schedule lines (= work order proposals) are created from the current date and three months onwards.</span></span>

3. <span data-ttu-id="eeb05-110">เลือก "ใช่" บนปุ่มสลับ **สร้างอัตโนมัติถ้ามีการระบุไว้ในรายการ** ถ้าใบสั่งงานควรมีการสร้างขึ้นโดยอัตโนมัติตามรายการแผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="eeb05-110">Select "Yes" on the **Auto create if specified in the line** toggle button if work orders should automatically be created according to the maintenance plan line.</span></span>

>[!NOTE]
><span data-ttu-id="eeb05-111">หากปุ่มสลับนี้ถูกตั้งค่าเป็น "ใช่" *และ* กล่องกาเครื่องหมาย **สร้างอัตโนมัติ** ถูกเลือกบนรายการ **แผนการบำรุงรักษา**  ใบสั่งงานจะถูกสร้างขึ้นตามรายการแผนการบำรุงรักษา และรายการกำหนดการแผนบำรุงรักษาที่มีสถานะเป็น "ใบสั่งงานที่สร้าง" ก็จะถูกสร้างด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="eeb05-111">If this toggle button is set to "Yes", *and* the **Auto create** check box is also selected on maintenance plan lines in **Maintenance plans**, work orders are created based on the maintenance plan lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="eeb05-112">ถ้ามีการเลือกเพียงตัวเลือกเดียว ปุ่มสลับในกล่องตอบโต้ (**สร้างอัตโนมัติถ้ามีการระบุไว้ในรายการ** หรือกล่องกาเครื่องหมาย **สร้างโดยอัตโนมัติ** ในฟอร์ม **แผนการบำรุงรักษา**) จะมีการสร้างเฉพาะรายการกำหนดการบำรุงรักษาด้วยสถานะ "สร้างแล้ว"</span><span class="sxs-lookup"><span data-stu-id="eeb05-112">If only one option is selected (**Auto create if specified in the line** toggle button in this dialog or **Auto create** check box in **Maintenance plans** form), only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="eeb05-113">ในกรณีดังกล่าว จะไม่มีการสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="eeb05-113">In that case, no work orders are created.</span></span>

4. <span data-ttu-id="eeb05-114">คุณสามารถสร้างรายการปฏิทินตามแผนการบำรุงรักษา (เวลาหรือตัวนับ) สินทรัพย์ ชนิดสินทรัพย์ ตำแหน่งที่ทำงาน และชนิดของตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="eeb05-114">It is possible to generate calendar entries based on maintenance plans (time or counter), assets, asset types, functional locations, and functional location types.</span></span> <span data-ttu-id="eeb05-115">คลิกปุ่ม **ตัวกรอง** และทำการเลือกของคุณ ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="eeb05-115">Click the **Filter** button and make your selections, if required.</span></span>

- <span data-ttu-id="eeb05-116">ตามการจัดการแผนการบำรุงรักษาเกี่ยวกับตำแหน่งที่ทำงาน ถ้าคุณอัพเดตการตั้งค่าของชนิดสินทรัพย์ ผู้ผลิต และแบบจำลองแผนการบำรุงรักษาใน **ตำแหน่งที่ทำงานทั้งหมด**  แท็บด่วน > **แผนการบำรุงรักษา** หลังจากที่คุณได้จัดกำหนดการแผนการบำรุงรักษา รายการกำหนดการบำรุงรักษาที่มีอยู่ที่เกี่ยวข้องกับตำแหน่งที่ทำงานนั้นจะถูกลบโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="eeb05-116">Regarding scheduling of maintenance plans on functional locations: If you update the setup of asset types, manufacturers, and models on maintenance plans in **All functional locations** > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="eeb05-117">ในการสร้างรายการปฏิทินใหม่ ซึ่งสอดคล้องกับการตั้งค่าแผนการบำรุงรักษาที่อัพเดตแล้วในตำแหน่งที่ทำงาน คุณต้องรันกำหนดการแผนการบำรุงรักษาสำหรับตำแหน่งที่ทำงานนั้นใหม่</span><span class="sxs-lookup"><span data-stu-id="eeb05-117">In order to create new calendar entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> <span data-ttu-id="eeb05-118">อ่านข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าชนิดสินทรัพย์ ผู้ผลิต และแบบจำลองในตำแหน่งที่ทำงานใน [สร้างตำแหน่งที่ทำงาน](../functional-locations/create-functional-locations.md)</span><span class="sxs-lookup"><span data-stu-id="eeb05-118">Read more about the setup of asset types, manufacturers, and models on functional locations in [Create functional locations](../functional-locations/create-functional-locations.md).</span></span>

><span data-ttu-id="eeb05-119">*ตัวอย่าง* คุณต้องการสร้างแผนการบำรุงรักษาสำหรับตำแหน่งที่ทำงานหนึ่งๆ ซึ่งหมายความว่าสินทรัพย์ทั้งหมดที่ตั้งค่าไว้ในตำแหน่งที่ทำงานนั้นจะรวมอยู่ในเวลาที่กำหนดไว้เมื่อคุณจัดกำหนดการแผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="eeb05-119">*Example:* You want to create a maintenance plan for a specific functional location, meaning all assets set up on that functional location at any given time will be included when you schedule the maintenance plan.</span></span> <span data-ttu-id="eeb05-120">ในกรณีดังกล่าว คุณสร้างแผนการบำรุงรักษาและเลือกตำแหน่งที่ทำงานที่ระบุ แต่คุณไม่ต้องเพิ่มสินทรัพย์ใดๆ ในแผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="eeb05-120">In that case, you create a maintenance plan and select the specific functional location, but you do NOT add any assets in the maintenance plan.</span></span> <span data-ttu-id="eeb05-121">ผลลัพธ์คือเมื่อคุณจัดกำหนดการแผนการบำรุงรักษา รายการกำหนดการบำรุงรักษาจะถูกสร้างขึ้นสำหรับสินทรัพย์ทั้งหมดที่เกี่ยวข้องกับสถานที่ทำงานในขณะนั้น</span><span class="sxs-lookup"><span data-stu-id="eeb05-121">The result is that when you schedule that maintenance plan, maintenance schedule lines will be created for all the assets related to the functional location at that time.</span></span>

- <span data-ttu-id="eeb05-122">ถ้าคุณทำการเปลี่ยนแปลงชนิดสินทรัพย์ ผู้ผลิต และแบบจำลองใน **ชนิดสินทรัพย์** การเปลี่ยนแปลงดังกล่าวจะมีผลกระทบต่อสินทรัพย์ใหม่ที่ใช้ชนิดสินทรัพย์ที่อัพเดตแล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="eeb05-122">If you make changes to asset types, manufacturers and models in **Asset types**, those changes only affect new assets that use the updated asset type.</span></span> <span data-ttu-id="eeb05-123">อ่านเพิ่มเติมเกี่ยวกับการตั้งค่าชนิดสินทรัพย์ใน [ชนิดสินทรัพย์](../setup-for-objects/object-types.md)</span><span class="sxs-lookup"><span data-stu-id="eeb05-123">Read more about asset type setup in [Asset types](../setup-for-objects/object-types.md).</span></span>  

5. <span data-ttu-id="eeb05-124">คลิก **ตกลง** เพื่อเริ่มต้นการสร้างรายการกำหนดการบำรุงรักษาในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="eeb05-124">Click **OK** to start the generation of maintenance schedule entries on assets.</span></span> <span data-ttu-id="eeb05-125">รายการที่สร้างขึ้นจะแสดงในหน้ารายการ **กำหนดการบำรุงรักษาทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="eeb05-125">The generated entries will be shown in the **All maintenance schedule** list page.</span></span> <span data-ttu-id="eeb05-126">ภาพประกอบต่อไปนี้แสดงตัวอย่างของกล่องโต้ตอบ **จัดกำหนดการแผนการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="eeb05-126">The following illustration shows an example of the **Schedule maintenance plans** dialog.</span></span>

![รูปที่ 1](media/09-preventive-maintenance.png)

- <span data-ttu-id="eeb05-128">ในกล่องโต้ตอบ **กำหนดการแผนการบำรุงรักษา** คุณสามารถตั้งค่าชุดงานสำหรับบนแท็บด่วน **รันบนพื้นหลัง** เพื่อสร้างรายการปฏิทินโดยอัตโนมัติในช่วงเวลาปกติ</span><span class="sxs-lookup"><span data-stu-id="eeb05-128">In the **Schedule maintenance plans** dialog, you can set up batch jobs on the **Run in the background** FastTab to automatically generate calendar entries at regular intervals.</span></span>  
- <span data-ttu-id="eeb05-129">เมื่อคุณจัดกำหนดการบำรุงรักษาเชิงป้องกัน รายการกำหนดการบำรุงรักษาที่มีวันที่และเวลาเริ่มต้นที่คาดไว้ก่อนวันที่และเวลาของระบบจะไม่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="eeb05-129">When you schedule preventive maintenance, maintenance schedule lines with expected start date and time earlier than the system date and time will not be created.</span></span>  

<span data-ttu-id="eeb05-130">ตัวเลขด้านล่างนี้แสดงภาพที่แสดงเป็นรูปภาพของการคำนวณแผนการบำรุงรักษาตามเวลา</span><span class="sxs-lookup"><span data-stu-id="eeb05-130">The figure below provides a graphic illustration of a time-based maintenance plan calculation.</span></span>  

![รูปที่ 2](media/10-preventive-maintenance.jpg)

<span data-ttu-id="eeb05-132">ตามแผนการบำรุงรักษาตามตัวนับ: ในตัวเลขด้านล่างนี้ การลงทะเบียนตัวนับสองรอบที่แตกต่างกันจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="eeb05-132">Regarding counter-based maintenance plans: In the figures below, two different counter registration cycles are shown.</span></span> <span data-ttu-id="eeb05-133">โดยจะขึ้นอยู่กับแผนการบำรุงรักษาที่ตั้งค่าไว้สำหรับสินทรัพย์ "V0001" คาดหวังสินทรัพย์ (รถยนต์) เพื่อรันประมาณ 2,000 กม. ทุกเดือน</span><span class="sxs-lookup"><span data-stu-id="eeb05-133">They are based on a maintenance plan set up for asset "V0001", expecting the asset (a car) to run approx. 2,000 km every month.</span></span>

<span data-ttu-id="eeb05-134">ในตัวอย่างแรก ที่คาดไว้ 2,000 กม. ไม่ถึงเป้าทุกเดือน</span><span class="sxs-lookup"><span data-stu-id="eeb05-134">In the first example, the expected 2,000 km are not reached every month.</span></span> <span data-ttu-id="eeb05-135">ตามแผนการบำรุงรักษาตามตัวนับ ขีดจำกัดคือ 2,000 กม. ซึ่งหมายความว่าเมื่อคุณรันการจัดกำหนดการแผนการบำรุงรักษา รายการกำหนดการบำรุงรักษาควรจะถูกสร้างให้ถึงขีดจำกัดของ 2,000 กิโลเมตรทุกครั้ง</span><span class="sxs-lookup"><span data-stu-id="eeb05-135">According to the counter-based maintenance plan, the threshold is 2,000 km, meaning when you run a maintenance plan scheduling, a maintenance schedule line should be created each time the 2,000-kilometer threshold is reached.</span></span> <span data-ttu-id="eeb05-136">ในตัวอย่างที่ 1 มีรายการลงทะเบียน 4 รายการ แต่มีการเข้าถึงขีดจำกัดที่ 2,000 กิโลเมตรเพียงครั้งเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="eeb05-136">In example 1, there are 4 registration lines, but the 2,000-kilometer threshold is only reached once.</span></span> <span data-ttu-id="eeb05-137">ซึ่งหมายความว่าเมื่อคุณรันแผนการบำรุงรักษาจัดกำหนดการสินทรัพย์นี้ตัวอย่างเช่นสำหรับรอบระยะเวลา3เดือนจะมีการสร้างรายการกำหนดการบำรุงรักษาเพียงรายการเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="eeb05-137">This means that when you run schedule maintenance plans this asset, for example for a 3-month period, only one maintenance schedule line will be created.</span></span>

<span data-ttu-id="eeb05-138">ในรูปถัดไป 2,000 กม. ขึ้นไป จะมีการลงทะเบียนทุกเดือน</span><span class="sxs-lookup"><span data-stu-id="eeb05-138">In the next figure, 2,000 km or more are registered every month.</span></span> <span data-ttu-id="eeb05-139">ดังนั้นจึงมีการสร้างรายการบำรุงรักษาสามรายการ ถ้าคุณจัดกำหนดการแผนบำรุงรักษาสำหรับสินทรัพย์นี้สำหรับรอบระยะเวลา 3 เดือน</span><span class="sxs-lookup"><span data-stu-id="eeb05-139">Therefore, three maintenance lines would be created if you schedule maintenance plans for this asset for a 3-month period.</span></span> 

<span data-ttu-id="eeb05-140">ตัวอย่างที่อธิบายไว้ที่นี่แสดงให้เห็นว่าการลงทะเบียนตัวนับทั้งหมดที่ทำในสินทรัพย์แสดงแนวโน้มที่อธิบายถึงการสึกหรอและการฉีกขาดของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="eeb05-140">The examples described here show that all counter registrations made on an asset show a trend describing wear and tear on the asset.</span></span> <span data-ttu-id="eeb05-141">แนวโน้มดังกล่าวจะใช้เป็นข้อมูลพื้นฐานของการคำนวณเมื่อจัดตารางรของแผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="eeb05-141">That trend is used as calculation basis at the time of maintenance plan scheduling.</span></span>

![รูปที่ 3](media/11-preventive-maintenance.png)

![รูปที่ 4](media/12-preventive-maintenance.png)

