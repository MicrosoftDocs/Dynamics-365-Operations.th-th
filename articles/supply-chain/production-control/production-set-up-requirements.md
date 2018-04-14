---
title: "ข้อกำหนดของการตั้งค่าการผลิต"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับข้อกำหนดการตั้งค่าก่อนที่คุณจะสามารถดำเนินการควบคุมการผลิต"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bcca20889fa0b79a289175ab901167509a908f3f
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="production-setup-requirements"></a><span data-ttu-id="24d21-103">ข้อกำหนดของการตั้งค่าการผลิต</span><span class="sxs-lookup"><span data-stu-id="24d21-103">Production setup requirements</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="24d21-104">บทความนี้แสดงข้อมูลเกี่ยวกับข้อกำหนดการตั้งค่าก่อนที่คุณจะสามารถดำเนินการควบคุมการผลิต</span><span class="sxs-lookup"><span data-stu-id="24d21-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="24d21-105">การควบคุมการผลิตถูกรวมเข้ากับลักษณะการทำงานในโมดูลอื่น</span><span class="sxs-lookup"><span data-stu-id="24d21-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="24d21-106">การเชื่อมโยงกันนี้ช่วยให้คุณสามารถเปลี่ยนใบสั่งผลิต และมั่นใจได้ว่ามีการอัพเดตใบสั่งผลิตโดยอัตโนมัติในกระบวนการและการคำนวณอื่นที่เกี่ยวข้องทั้งหมดในระบบ</span><span class="sxs-lookup"><span data-stu-id="24d21-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="24d21-107">ขั้นตอนการตั้งค่าต่อไปนี้จะแสดงรายการในใบสั่งที่คุณควรดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="24d21-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="24d21-108">การตั้งค่าพื้นฐานที่จำเป็นในโมดูลอื่น</span><span class="sxs-lookup"><span data-stu-id="24d21-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="24d21-109">ข้อมูลในโมดูลอื่นต้องมีการตั้งค่าก่อน คุณจึงจะสามารถทำงานกับการควบคุมการผลิตได้</span><span class="sxs-lookup"><span data-stu-id="24d21-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="24d21-110">การตั้งค่ารวมถึงงานดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="24d21-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="24d21-111">ตั้งค่าข้อมูลบริษัททั่วไป</span><span class="sxs-lookup"><span data-stu-id="24d21-111">Set up general company information.</span></span>
-   <span data-ttu-id="24d21-112">ตั้งค่าบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="24d21-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="24d21-113">กำหนดกลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="24d21-113">Define item groups.</span></span>
-   <span data-ttu-id="24d21-114">ตั้งค่าบัญชีแยกประเภทสำหรับกลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="24d21-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="24d21-115">ตั้งค่าตารางสินค้าคงคลังในการบริหารสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="24d21-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="24d21-116">สร้างสูตรการผลิต(BOMs) และ BOM เวอร์ชันในการบริหารสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="24d21-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="24d21-117">การตั้งค่าปฏิทินและการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="24d21-117">Required calendar and resource setup</span></span>
<span data-ttu-id="24d21-118">ก่อนที่คุณจะใช้การควบคุม ให้เปิดการจัดการองค์กร และสร้างและกำหนดปฏิทินและทรัพยากรการดำเนินงานในลำดับต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="24d21-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="24d21-119">**เท็มเพลตเวลาการทำงาน**– ตั้งค่าเท็มเพลตเวลาการทำงานเพื่อกำหนดเวลาที่พร้อมใช้งานสำหรับการจัดตารางการผลิต</span><span class="sxs-lookup"><span data-stu-id="24d21-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="24d21-120">**Calendars** – ตั้งค่าปฏิทินเวลาการทำงานเพื่อกำหนดจำนวนวันของปีที่พร้อมใช้งานสำหรับการจัดตารางการผลิต</span><span class="sxs-lookup"><span data-stu-id="24d21-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="24d21-121">**กลุ่มทรัพยากร**– ตั้งค่ากลุ่มทรัพยากรเพื่อจัดกลุ่มทรัพยากรการดำเนินงาน เพื่อให้คุณสามารถดูภาพรวมของกำลังการผลิตที่ว่างเมื่อคุณรันการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="24d21-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="24d21-122">คุณไม่จำเป็นต้องตั้งค่ากลุ่มทรัพยากรก่อนที่คุณตั้งค่าทรัพยากรการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="24d21-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="24d21-123">อย่างไรก็ตาม เราขอแนะนำให้คุณเข้าใจวิธีการจัดกลุ่มทรัพยากรเมื่อคุณตั้งค่าการควบคุมการผลิต</span><span class="sxs-lookup"><span data-stu-id="24d21-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="24d21-124">**ทรัพยากร** – ตั้งค่าทรัพยากรการดำเนินงานเพื่อกำหนดทรัพยากรต่างๆที่จะใช้เพื่อทำกระบวนการผลิตให้สมบูรณ์ และเพื่อวางแผนกำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="24d21-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="24d21-125">การตั้งค่าพารามิเตอร์การผลิตที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="24d21-125">Required production parameters setup</span></span>
<span data-ttu-id="24d21-126">**พารามิเตอร์การควบคุมการผลิต** – ตั้งค่าพารามิเตอร์การผลิตพื้นฐานเพื่อกำหนดวิธีจัดการกับระบบและกระบวนการใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="24d21-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="24d21-127">กำหนดวิธีการสร้าง ประเมิน จัดกำหนดการ และคำนวณปริมาณการใช้วัสดุของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="24d21-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="24d21-128">คุณยังสามารถเลือกชนิดของผลป้อนกลับที่คุณต้องการ และวิธีการลงบัญชีต้นทุนสินค้าได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="24d21-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="24d21-129">การระบุชื่อสมุดรายวันที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="24d21-129">Required journal name identification</span></span>
<span data-ttu-id="24d21-130">**ชื่อสมุดรายวันการผลิต**– ระบุชื่อสมุดรายวันการผลิตที่ใช้เพื่อบันทึกและลงรายการบัญชีธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="24d21-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="24d21-131">การตั้งค่าถ้าคุณใช้การดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="24d21-131">Setup if you use operations</span></span>
<span data-ttu-id="24d21-132">การดำเนินงานแสดงกิจกรรมเฉพาะที่เสร็จสมบูรณ์เพื่อผลิตผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="24d21-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="24d21-133">**หมายเหตุ:** คุณต้องทราบชนิดของกิจกรรมที่จำเป็นในการผลิตสินค้าของคุณ และใบสั่งและระดับความสำคัญของกิจกรรมเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="24d21-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="24d21-134">คุณต้องทราบว่าทรัพยากรใดที่เกี่ยวข้อง และจำนวนของทรัพยากรนั้น</span><span class="sxs-lookup"><span data-stu-id="24d21-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="24d21-135">**การดำเนินงาน** – ตั้งค่าการดำเนินงานเพื่อแสดงถึงงานที่ต้องทำให้เสร็จสมบูรณ์เพื่อผลิตสินค้าสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="24d21-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="24d21-136">**ความสัมพันธ์**– ตั้งค่าความสัมพันธ์ของการดำเนินงานเพื่อกำหนดคุณสมบัติโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="24d21-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="24d21-137">เมื่อต้องการกำหนดความสัมพันธ์ของการดำเนินงาน คลิก **ความสัมพันธ์** บนหน้า **การดำเนินงาน**</span><span class="sxs-lookup"><span data-stu-id="24d21-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="24d21-138">การตั้งค่าถ้าคุณใช้กระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="24d21-138">Setup if you use routes</span></span>
<span data-ttu-id="24d21-139">ถ้าคุณทำงานกับกระบวนการผลิตอยู่ คุณต้องกำหนดการดำเนินงานสำหรับกระบวนการผลิตแต่ละกระบวนการที่คุณตั้งค่าไว้</span><span class="sxs-lookup"><span data-stu-id="24d21-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="24d21-140">กระบวนการผลิตแสดงถึงเส้นทางที่สินค้าใช้จากการดำเนินงานหนึ่งไปยังอีกการดำเนินงานหนึ่ง จากจุดเริ่มต้นของกระบวนการผลิตไปจนกว่ากระบวนการจะสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="24d21-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="24d21-141">**ประเภทต้นทุน** – ตั้งค่าประเภทต้นทุนเพื่อกำหนดต้นทุนต่อชั่วโมงของเวลาที่ใช้ในกระบวนการและการตั้งค่าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="24d21-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="24d21-142">**กลุ่มต้นทุน** – ตั้งค่ากลุ่มต้นทุนเพื่อสร้างและรักษาการลงบัญชีต้นทุนชนิดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="24d21-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="24d21-143">**กลุ่มกระบวนการผลิต**– ตั้งค่ากลุ่มกระบวนการผลิตเพื่อกำหนดพารามิเตอร์ที่เกี่ยวข้องกับกลุ่มของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="24d21-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="24d21-144">ก่อนที่คุณจะตั้งค่ากระบวนการผลิต คุณต้องตั้งค่ากลุ่มกระบวนการผลิตก่อน</span><span class="sxs-lookup"><span data-stu-id="24d21-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="24d21-145">**กระบวนการผลิต** – ตั้งค่ากระบวนการผลิตและกำหนดการตั้งค่าเริ่มต้น เพื่อควบคุมการจัดกำหนดการ การลงบัญชีต้นทุน และการกำหนดราคาของกระบวนการผลิต และการรายงานความคืบหน้าการควบคุม</span><span class="sxs-lookup"><span data-stu-id="24d21-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="24d21-146">**กระบวนการผลิต** – ตั้งค่าเวอร์ชันกระบวนการผลิตเพื่อเปิดใช้งานการเปลี่ยนแปลงของสินค้าในการผลิต</span><span class="sxs-lookup"><span data-stu-id="24d21-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="24d21-147">กำหนดการตั้งค่าเสริมขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="24d21-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="24d21-148">**กลุ่มการผลิต** – ตั้งค่ากลุ่มการผลิตเพื่อสร้างความสัมพันธ์ระหว่างใบสั่งผลิตบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="24d21-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="24d21-149">บัญชีแยกประเภทจะถูกใช้ในการลงรายการบัญชีหรือการจัดกลุ่มใบสั่งสำหรับการรายงาน</span><span class="sxs-lookup"><span data-stu-id="24d21-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="24d21-150">**ประเภทการผลิต** - สร้างประเภทการผลิตเพื่อจัดกลุ่มใบสั่งผลิต เพื่อดำเนินการใบสั่งผลิตด่วน หรือเพื่อลบและการลงรายการบัญชีกลุ่มของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="24d21-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="24d21-151">**คุณสมบัติ**– กำหนดคุณสมบัติเพื่อสร้างแอททริบิวต์พิเศษซึ่งคุณสามารถมอบหมายให้กับทรัพยากรของคุณเพื่อควบคุมใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="24d21-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="24d21-152">แอททริบิวต์เหล่านี้มีความเกี่ยวข้องกับเท็มเพลตเวลาการทำงาน </span><span class="sxs-lookup"><span data-stu-id="24d21-152">These attributes are connected to the working time template.</span></span>





