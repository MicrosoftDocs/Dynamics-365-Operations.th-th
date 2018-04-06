---
title: "จัดการผู้ปฏิบัติงานสำหรับคลังสินค้า"
description: "บทความนี้อธิบายถึงวิธีการที่คุณสามารถใช้ Dynamics 365 for Finance and Operations เพื่อช่วยควบคุมและตรวจสอบงานที่มีการดำเนินการโดยพนักงานในคลังสินค้าของคุณ"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 211ced007e7729265621a05c2162a228eb0023c2
ms.contentlocale: th-th
ms.lasthandoff: 03/26/2018

---

# <a name="manage-warehouse-workers"></a><span data-ttu-id="6c66e-103">จัดการผู้ปฏิบัติงานสำหรับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c66e-103">Manage warehouse workers</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6c66e-104">บทความนี้อธิบายถึงวิธีการที่คุณสามารถใช้ Microsoft Dynamics 365 for Finance and Operations เพื่อช่วยควบคุมและตรวจสอบงานที่มีการดำเนินการโดยพนักงานในคลังสินค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="6c66e-104">This article describes how you can use Microsoft Dynamics 365 for Finance and Operations to help control and monitor the work that's carried out by employees in your warehouses.</span></span>

<span data-ttu-id="6c66e-105">ถ้าคุณกำลังใช้ฟังก์ชันในการจัดการคลังสินค้า การดำเนินงานของผู้ปฏิบัติงานคลังสินค้าทั้งหมดจะถูกอ้างอิงเป็น *งาน*</span><span class="sxs-lookup"><span data-stu-id="6c66e-105">If you're using the functionality in Warehouse management, all warehouse worker operations are referred to as *work*.</span></span> <span data-ttu-id="6c66e-106">งานเช่น การเบิกสินค้า การย้าย และการตรวจนับปริมาณคงคลังคงเหลือจะถูกบันทึกโดยใช้อุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="6c66e-106">Work such as picking, moving, and counting on-hand inventory is recorded by using mobile devices.</span></span> <span data-ttu-id="6c66e-107">ก่อนที่ผู้ปฏิบัติงานคลังสินค้าจะสามารถทำงานได้ เขาหรือเธอต้องมีการเชื่อมโยงกับผู้ปฏิบัติงานในฝ่ายทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c66e-107">Before a warehouse worker can perform work, he or she must be associated with a worker in Human resources.</span></span> <span data-ttu-id="6c66e-108">บัญชี **ผู้ปฏิบัติงาน** แต่ละรายการสามารถมีผู้ใช้งานคลังสินค้าหลายรายที่เกี่ยวข้องได้</span><span class="sxs-lookup"><span data-stu-id="6c66e-108">Each **Worker** account can have multiple warehouse work users associated with it.</span></span> <span data-ttu-id="6c66e-109">ผู้ใช้งานเหล่านั้นสามารถทำงานในคลังสินค้าที่แตกต่างกัน และสามารถมีการเข้าถึงเมนูอุปกรณ์เคลื่อนต่างๆในระดับที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="6c66e-109">Those work users can work in different warehouses and can have different levels of access to the various mobile device menus.</span></span> <span data-ttu-id="6c66e-110">คุณสามารถพิจารณาผู้ใช้งานที่คลังสินค้าให้เป็นการล็อกออนหลายเครื่องสำหรับผู้ปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6c66e-110">You can think of the warehouse work users as multiple logons for the selected worker.</span></span> <span data-ttu-id="6c66e-111">ผู้ใช้งานแต่ละรายมีคลังสินค้าเริ่มต้น และลำดับงานเฉพาะถูกแสดงโดยรายการเมนูที่มีอยู่ให้กับผู้ใช้งานนั้น</span><span class="sxs-lookup"><span data-stu-id="6c66e-111">Each work user has a default warehouse, and specific workflows are exposed by the menus items that are available to that work user.</span></span> 

<span data-ttu-id="6c66e-112">เพื่อสร้างงานผู้ใช้งานใหม่ ในหน้า **ผู้ปฏิบัติงาน** บนแท็บ **ทั่วไป** ในส่วน **คลังสินค้า** ให้คลิก **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="6c66e-112">To create a new work user, on the **Workers** page, on the **General** tab, in the **Warehouses** section, click **Worker**.</span></span> <span data-ttu-id="6c66e-113">คุณต้องระบุรหัสผู้ใช้ ชื่อผู้ใช้ คลังสินค้าเริ่มต้น และชื่อเมนู</span><span class="sxs-lookup"><span data-stu-id="6c66e-113">You must specify a user ID, a user name, a default warehouse, and a menu name.</span></span> <span data-ttu-id="6c66e-114">เมนูนี้จะถูกโหลดเมื่อผู้ใช้ลงทะเบียนไปยังพอร์ทัลอุปกรณ์เคลื่อนของคลังสินค้า และช่วยให้คุณกำหนดว่ารายการเมนูใดที่ผู้ใช้มีสิทธิ์เข้าถึง</span><span class="sxs-lookup"><span data-stu-id="6c66e-114">This menu is loaded when the user signs in to the Warehouse Mobile Device Portal, and lets you define which menu items the user has access to.</span></span> 

<span data-ttu-id="6c66e-115">เนื่องจากเป็นส่วนหนึ่งของการตั้งค่าสำหรับผู้ใช้งานแต่ละราย คุณยังสามารถกำหนดลำดับงานของกระบวนการเฉพาะได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="6c66e-115">As part of the setup for each work user, you can also define specific process workflows.</span></span> <span data-ttu-id="6c66e-116">ตัวอย่างเช่น คุณสามารถใช้ฟิลด์ **เป็นหัวหน้างานการตรวจสอบวงจรหรือไม่** เพื่อระบุว่า ผู้ใช้สามารถประมวลผลการปรับปรุงส่วนต่างการตรวจนับตามรอบในระหว่างการดำเนินการตรวจนับ หรือว่าการปรับปรุงเหล่านี้ต้องถูกตรวจทานก่อนโดยพนักงานคนอื่น</span><span class="sxs-lookup"><span data-stu-id="6c66e-116">For example, you can use the **Is a cycle count supervisor** field to specify whether the user can process adjustments to cycle counting discrepancies during a counting operation, or whether these adjustments must first be reviewed by another person.</span></span>

## <a name="defining-labor-standards"></a><span data-ttu-id="6c66e-117">การกำหนดมาตรฐานแรงงาน</span><span class="sxs-lookup"><span data-stu-id="6c66e-117">Defining labor standards</span></span>
<span data-ttu-id="6c66e-118">หน้า **มาตรฐานแรงงาน** ช่วยให้คุณสามารถกำหนดวิธีการคำนวณที่ระบบใช้ เพื่อคำนวณเวลาโดยประมาณที่ชนิดงานที่เฉพาะเจาะจงต้องการ</span><span class="sxs-lookup"><span data-stu-id="6c66e-118">The **Labor standards** page lets you define the calculation methods that the system uses to calculate the estimated time that a particular type of work should require.</span></span> <span data-ttu-id="6c66e-119">สามารถตั้งค่าข้อกำหนดนี้ในระดับทั่วไปหรือในระดับเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="6c66e-119">This definition can be set on a generic level or on a specific level.</span></span> <span data-ttu-id="6c66e-120">ตัวอย่างเช่น คุณสามารถกำหนดระยะเวลาที่ควรใช้สำหรับการประมวลผลการเบิกสินค้าของใบสั่งขายต่อน้ำหนัก สำหรับข้อกำหนดของหน่วยเฉพาะเมื่อมีใช้กระบวนการเบิกสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="6c66e-120">For example, you can define the time that should be required in order to process a sales order pick per weight for a specific unit definition when a specific picking process is used.</span></span> <span data-ttu-id="6c66e-121">ในเวลาเดียวกัน คุณสามารถบันทึกเวลา ที่ขึ้นอยู่กับวิธีการคำนวณอีกวิธีหนึ่ง สำหรับการดำเนินการส่งสินค้าของสินค้าคงคลังคงเหลือที่จะมีการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c66e-121">At the same time, you can record the time, based on another calculation method, for the put operation of the on-hand inventory that is picked.</span></span> 

<span data-ttu-id="6c66e-122">เมื่อต้องการเปิดใช้งานมาตรฐานแรงงานที่คุณได้กำหนดไว้ คุณต้องเลือกตัวเลือก **อนุญาตมาตรฐานแรงงาน** สำหรับคลังสินค้าแต่ละแห่งที่ที่จะใช้มาตรฐานแรงงาน</span><span class="sxs-lookup"><span data-stu-id="6c66e-122">To enable the labor standards that you've defined, you must select the **Allow labor standards** option for each warehouse where labor standards will be used.</span></span>

## <a name="monitoring-and-controlling-warehouse-work"></a><span data-ttu-id="6c66e-123">การติดตามและการควบคุมงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c66e-123">Monitoring and controlling warehouse work</span></span>
<span data-ttu-id="6c66e-124">หน้า **งานทั้งหมด** ช่วยให้คุณสามารถตรวจสอบและรักษางานทั้งหมดที่มีการวางแผน ในระหว่างดำเนินการ และที่เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="6c66e-124">The **All work** page lets you monitor and maintain all work that is planned, in progress, and completed.</span></span> <span data-ttu-id="6c66e-125">จากหน้านี้ คุณสามารถอัพเดตกระบวนการต่างๆเช่น การมอบหมายผู้ใช้งานที่คลังสินค้า และระดับความสำคัญของงาน</span><span class="sxs-lookup"><span data-stu-id="6c66e-125">From this page, you can update various processes, such as warehouse work user assignments and work priority.</span></span> <span data-ttu-id="6c66e-126">คุณยัสามารถลงลึกในรายละเอียดที่เกี่ยวข้องกับหัวข้องานและรายการงาน เพื่อให้มีความเข้าใจกระบวนการทำงานที่คาดไว้หรือที่เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="6c66e-126">You can also drill down into the details that are related to the work header and work lines to gain an understanding of the expected or completed work processes.</span></span> 

<span data-ttu-id="6c66e-127">ถ้าคุณเปิดใช้งานตัวเลือก **มาตรฐานแรงงาน** คุณสามารถดูเวลาโดยประมาณที่คำนวณได้สำหรับการทำงาน</span><span class="sxs-lookup"><span data-stu-id="6c66e-127">If you enable the **Labor standards** option, you can see the calculated estimated time for the work.</span></span> <span data-ttu-id="6c66e-128">จากนั้น เมื่อมีการดำเนินงาน เวลาที่แท้จริงจะยังถูกแสดงสำหรับการดำเนินงานแต่ละครั้งด้วย</span><span class="sxs-lookup"><span data-stu-id="6c66e-128">Then, when the work is processed, the actual time will also be shown for each work operation.</span></span> <span data-ttu-id="6c66e-129">ด้วยวิธีนี้ คุณสามารถเปรียบเทียบการคำนวณเวลาโดยประมาณจนถึงเวลาเกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="6c66e-129">In this way, you can compare the estimated time calculations to the actual time.</span></span> 

<span data-ttu-id="6c66e-130">นอกจากนี้ คุณยังสามารถใช้เวลาโดยประมาณในกฎสำหรับการแบ่งงานระหว่างการสร้างงานโดยอัตโนมัติได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="6c66e-130">Additionally, you can use the estimated time in the rules for automatically splitting work during work creation.</span></span> <span data-ttu-id="6c66e-131">ด้วยวิธีนี้ คุณสามารถโหลดงานยอดดุล ตามเวลาที่คาดไว้เพื่อดำเนินงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6c66e-131">In this way, you can load balance work, based on the expected time to complete the tasks.</span></span> 

<span data-ttu-id="6c66e-132">การวิเคราะห์ของเวลาที่ใช้ในการประมวลผลรายการงานสามารถช่วยการปรับปรุงไดรฟ์ในด้านประสิทธิภาพของผู้ปฏิบัติงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c66e-132">Analysis of the time that is used to process work items can help drive improvements in the warehouse workers’ efficiency.</span></span> <span data-ttu-id="6c66e-133">รายงานต่อไปนี้พร้อมใช้งานเพื่อช่วยในการวิเคราะห์นี้:</span><span class="sxs-lookup"><span data-stu-id="6c66e-133">The following reports are available to help with this analysis:</span></span>

-   <span data-ttu-id="6c66e-134">**แรงงานโดยผู้ใช้**– รายงานนี้แสดงประสิทธิภาพการทำงานของผู้ปฏิบัติงาน ตามระยะเวลาที่เกิดขึ้นจริงเทียบกับเวลาที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="6c66e-134">**Labor by user** – This report shows worker productivity, based on actual times against expected times.</span></span>
-   <span data-ttu-id="6c66e-135">**แรงงานตามชนิดธุรกรรมงาน**– คุณสามารถใช้รายงานนี้เพื่อตรวจสอบความไม่มีประสิทธิภาพในกระบวนการคลังสินค้าเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="6c66e-135">**Labor by work transaction type** – You can use this report to investigate inefficiencies in specific warehouse processes.</span></span> <span data-ttu-id="6c66e-136">ตัวอย่างเช่น คุณสังเกตเห็นว่า การเบิกสินค้าสำหรับใบสั่งโอนย้ายกำลังดำเนินงานในสัปดาห์นี้นานกว่าสัปดาห์ก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="6c66e-136">For example, you notice that picks for transfer orders are taking longer this week than in previous weeks.</span></span> <span data-ttu-id="6c66e-137">จากนั้นคุณสามารถใช้ข้อมูลนี้สำหรับการตรวจสอบเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="6c66e-137">You can then use this information for further investigation.</span></span>





