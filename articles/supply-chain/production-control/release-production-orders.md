---
title: "นำใบสั่งผลิตออกใช้"
description: "ใบสั่งผลิตที่นำออกใช้คือใบสั่งที่ได้รับอนุมัติสำหรับการผลิต เงื่อนไขการออกถูกใช้เพื่ออธิบายสถานะในวงจรอายุการใช้งานใบสั่งผลิต ซึ่งใบสั่งผลิตจะพร้อมใช้งานสำหรับการดำเนินการในการผลิตและกระบวนการคลังสินค้า"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 400c2786d80681827829286e6e9667b4d51612c4
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="release-production-orders"></a><span data-ttu-id="6cefd-104">นำใบสั่งผลิตออกใช้</span><span class="sxs-lookup"><span data-stu-id="6cefd-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cefd-105">ใบสั่งผลิตที่นำออกใช้คือใบสั่งที่ได้รับอนุมัติสำหรับการผลิต</span><span class="sxs-lookup"><span data-stu-id="6cefd-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="6cefd-106">เงื่อนไขการออกถูกใช้เพื่ออธิบายสถานะในวงจรอายุการใช้งานใบสั่งผลิต ซึ่งใบสั่งผลิตจะพร้อมใช้งานสำหรับการดำเนินการในการผลิตและกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6cefd-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="6cefd-107">ลักษณะของสถานะที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="6cefd-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="6cefd-108">สถานะ **นำออกใช้แล้ว** เป็นสถานะหนึ่งในวงจรชีวิตของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="6cefd-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="6cefd-109">ใบสั่งผลิตที่อยู่ในสถานะ **นำออกใช้แล้ว** พร้อมใช้งานสำหรับการดำเนินการในการผลิตและสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6cefd-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="6cefd-110">สถานะ **นำออกใช้แล้ว** มีลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6cefd-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="6cefd-111">ใบสั่งผลิตสามารถเปลี่ยนเป็นสถานะ **นำออกใช้แล้ว** จากใบสั่งผลิตหรือโดยการใช้กระบวนการชุดงานได้</span><span class="sxs-lookup"><span data-stu-id="6cefd-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="6cefd-112">ใบสั่งผลิตยังสามารถถูกอัพเดตโดยอัตโนมัติจากใบสั่งผลิตที่วางแผนไว้ซึ่งมีการยืนยันโดยใช้ฟิลด์ **กรอบเวลาการยืนยันยอด** ในหน้า **แผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="6cefd-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="6cefd-113">สถานะ **นำออกใช้แล้ว** คือ สัญญาณสำหรับตัวดำเนินการผลิต (ตัวดำเนินการ) เพื่อเริ่มต้นการดำเนินงานการผลิตในการผลิต</span><span class="sxs-lookup"><span data-stu-id="6cefd-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="6cefd-114">เอกสารการผลิต เช่น บัตรกระบวนการผลิต งานในกระบวนการผลิต และบัตรงานให้ข้อมูลเกี่ยวกับงานการผลิตและสามารถนำออกไปใช้ได้</span><span class="sxs-lookup"><span data-stu-id="6cefd-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="6cefd-115">สำหรับวัสดุที่มีจองทางกายภาพ งานคลังสินค้าจะถูกสร้างขึ้นเพื่อเบิกวัสดุและส่วนประกอบสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="6cefd-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="6cefd-116">การปล่อยงานให้การผลิต</span><span class="sxs-lookup"><span data-stu-id="6cefd-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="6cefd-117">หลังจากที่นำใบสั่งผลิตออกใช้ งานการผลิตที่เกี่ยวข้องกับใบสั่งจะสามารถมองเห็นได้ และพร้อมสำหรับการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="6cefd-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="6cefd-118">ตัวดำเนินการสามารถทำการลงทะเบียนงาน เช่น การเริ่มต้น การหยุด การเสร็จสมบูรณ์ ในหน้า **เทอร์มินัลบัตรงาน** หรือหน้า **อุปกรณ์สำหรับบัตรงาน**</span><span class="sxs-lookup"><span data-stu-id="6cefd-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="6cefd-119">เวลาและปริมาณที่ลงทะเบียนถูกโอนย้ายจากหน้าการลงทะเบียนไปยังสมุดรายวันการผลิตเพื่อติดตามเวลาและปริมาณที่ใช้</span><span class="sxs-lookup"><span data-stu-id="6cefd-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="6cefd-120">บัตรกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="6cefd-120">Route cards</span></span>
<span data-ttu-id="6cefd-121">บัตรกระบวนการผลิตจะแสดงภาพรวมข้อมูลที่มาจากการตั้งค่ากระบวนการผลิตและการดำเนินงาน และมาจากวิธีการดำเนินงานและการจัดตารางงาน</span><span class="sxs-lookup"><span data-stu-id="6cefd-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="6cefd-122">งานในกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="6cefd-122">Route jobs</span></span>
<span data-ttu-id="6cefd-123">รายงานงานในกระบวนการผลิตแสดงรายการแต่ละงานของการดำเนินงานโดยละเอียด และรวมถึงการตั้งค่า กระบวนการ คิว และเวลาการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="6cefd-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="6cefd-124">ตัวอย่างเช่น การดำเนินการ เช่น การทาสีอาจต้องการแต่ละงาน เช่น เวลาตั้งค่า เวลาการดำเนินงานสำหรับกระบวนการทาสี และเวลาในการรอให้แห้ง</span><span class="sxs-lookup"><span data-stu-id="6cefd-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="6cefd-125">บัตรงาน</span><span class="sxs-lookup"><span data-stu-id="6cefd-125">Job cards</span></span>
<span data-ttu-id="6cefd-126">บัตรงานแสดงรายการแต่ละหมายเลขงานของการดำเนินงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="6cefd-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="6cefd-127">งานหนึ่งงานปรากฏขึ้นบนแต่ละหน้า</span><span class="sxs-lookup"><span data-stu-id="6cefd-127">One job appears on each page.</span></span> <span data-ttu-id="6cefd-128">งานที่รวมอยู่ในบัตรงานและเวลาโดยประมาณ มาจากข้อมูลการตั้งค่ากระบวนการผลิตและการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="6cefd-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="6cefd-129">จากบัตรงาน คุณสามารถเปิดหน้า **รายการสมุดรายวันการผลิต** **บัตรงาน**ได้</span><span class="sxs-lookup"><span data-stu-id="6cefd-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="6cefd-130">บุคคลที่ดำเนินการทรัพยากรการดำเนินงานสามารถให้ผลป้อนกลับเกี่ยวกับกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="6cefd-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="6cefd-131">มีฟิลด์ที่คุณสามารถป้อนสถิติปริมาณการใช้และข้อมูล เช่น ปริมาณสินค้าที่บกพร่อง</span><span class="sxs-lookup"><span data-stu-id="6cefd-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="6cefd-132">งานคลังสินค้าสำหรับการเบิกวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="6cefd-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="6cefd-133">มีการสร้างงานสำหรับการเบิกวัตถุดิบในระหว่างการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="6cefd-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="6cefd-134">มีการสร้างงานสำหรับเฉพาะปริมาณของวัสดุที่มีการจองทางกายภาพสำหรับใบสั่งผลิตก่อนนำใบสั่งออกใช้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6cefd-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="6cefd-135">การตั้งค่าต่อไปนี้จำเป็นต้องใช้ในการสร้างงานที่คลังสินค้าสำหรับการเบิกวัตถุดิบ:</span><span class="sxs-lookup"><span data-stu-id="6cefd-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="6cefd-136">คำสั่งสถานที่สำหรับการเบิกวัตถุดิบที่กำหนดว่าที่ตั้งคลังสินค้าใดที่จะเบิกวัสดุ</span><span class="sxs-lookup"><span data-stu-id="6cefd-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="6cefd-137">เท็มเพลตเวฟสำหรับวัตถุดิบ ที่มีการตั้งค่าคอนฟิกนโยบายสำหรับการดำเนินงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6cefd-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="6cefd-138">ที่ตั้งอินพุทการผลิตที่กำหนดที่วางวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="6cefd-138">A production input location that determines where materials are put</span></span>





