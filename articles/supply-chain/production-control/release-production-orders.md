---
title: นำใบสั่งผลิตออกใช้
description: ใบสั่งผลิตที่นำออกใช้คือใบสั่งที่ได้รับอนุมัติสำหรับการผลิต เงื่อนไขการออกถูกใช้เพื่ออธิบายสถานะในวงจรอายุการใช้งานใบสั่งผลิต ซึ่งใบสั่งผลิตจะพร้อมใช้งานสำหรับการดำเนินการในการผลิตและกระบวนการคลังสินค้า
author: johanhoffmann
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 118b0d6300647135b22e42cc84a79f07e48d7ef4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811713"
---
# <a name="release-production-orders"></a><span data-ttu-id="382b4-104">นำใบสั่งผลิตออกใช้</span><span class="sxs-lookup"><span data-stu-id="382b4-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="382b4-105">ใบสั่งผลิตที่นำออกใช้คือใบสั่งที่ได้รับอนุมัติสำหรับการผลิต</span><span class="sxs-lookup"><span data-stu-id="382b4-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="382b4-106">เงื่อนไขการออกถูกใช้เพื่ออธิบายสถานะในวงจรอายุการใช้งานใบสั่งผลิต ซึ่งใบสั่งผลิตจะพร้อมใช้งานสำหรับการดำเนินการในการผลิตและกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="382b4-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span>

## <a name="characteristics-of-the-released-state"></a><span data-ttu-id="382b4-107">ลักษณะของสถานะที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="382b4-107">Characteristics of the Released state</span></span>

<span data-ttu-id="382b4-108">สถานะ **นำออกใช้แล้ว** เป็นสถานะหนึ่งในวงจรชีวิตของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="382b4-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="382b4-109">ใบสั่งผลิตที่อยู่ในสถานะ **นำออกใช้แล้ว** พร้อมใช้งานสำหรับการดำเนินการในการผลิตและสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="382b4-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="382b4-110">สถานะ **นำออกใช้แล้ว** มีลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="382b4-110">The **Released** state has the following characteristics:</span></span>

- <span data-ttu-id="382b4-111">ใบสั่งผลิตสามารถเปลี่ยนเป็นสถานะ **นำออกใช้แล้ว** จากใบสั่งผลิตหรือโดยการใช้กระบวนการชุดงานได้</span><span class="sxs-lookup"><span data-stu-id="382b4-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="382b4-112">ใบสั่งผลิตยังสามารถถูกอัพเดตโดยอัตโนมัติจากใบสั่งผลิตที่วางแผนไว้ซึ่งมีการยืนยันโดยใช้ฟิลด์ **กรอบเวลาการยืนยันยอด** ในหน้า **แผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="382b4-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
- <span data-ttu-id="382b4-113">สถานะ **นำออกใช้แล้ว** คือ สัญญาณสำหรับตัวดำเนินการผลิต (ตัวดำเนินการ) เพื่อเริ่มต้นการดำเนินงานการผลิตในการผลิต</span><span class="sxs-lookup"><span data-stu-id="382b4-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
- <span data-ttu-id="382b4-114">เอกสารการผลิต เช่น บัตรกระบวนการผลิต งานในกระบวนการผลิต และบัตรงานให้ข้อมูลเกี่ยวกับงานการผลิตและสามารถนำออกไปใช้ได้</span><span class="sxs-lookup"><span data-stu-id="382b4-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
- <span data-ttu-id="382b4-115">สำหรับวัสดุที่มีจองทางกายภาพ งานคลังสินค้าจะถูกสร้างขึ้นเพื่อเบิกวัสดุและส่วนประกอบสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="382b4-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="382b4-116">การปล่อยงานให้การผลิต</span><span class="sxs-lookup"><span data-stu-id="382b4-116">Releasing jobs to the shop floor</span></span>

<span data-ttu-id="382b4-117">หลังจากที่นำใบสั่งผลิตออกใช้ งานการผลิตที่เกี่ยวข้องกับใบสั่งจะสามารถมองเห็นได้ และพร้อมสำหรับการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="382b4-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="382b4-118">ตัวดำเนินการสามารถทำการลงทะเบียนงาน เช่น การเริ่มต้น การหยุด การเสร็จสมบูรณ์ ในหน้า **เทอร์มินัลบัตรงาน** หรือหน้า **อุปกรณ์สำหรับบัตรงาน**</span><span class="sxs-lookup"><span data-stu-id="382b4-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="382b4-119">เวลาและปริมาณที่ลงทะเบียนถูกโอนย้ายจากหน้าการลงทะเบียนไปยังสมุดรายวันการผลิตเพื่อติดตามเวลาและปริมาณที่ใช้</span><span class="sxs-lookup"><span data-stu-id="382b4-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="382b4-120">บัตรกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="382b4-120">Route cards</span></span>

<span data-ttu-id="382b4-121">บัตรกระบวนการผลิตจะแสดงภาพรวมข้อมูลที่มาจากการตั้งค่ากระบวนการผลิตและการดำเนินงาน และมาจากวิธีการดำเนินงานและการจัดตารางงาน</span><span class="sxs-lookup"><span data-stu-id="382b4-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="382b4-122">งานในกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="382b4-122">Route jobs</span></span>

<span data-ttu-id="382b4-123">รายงานงานในกระบวนการผลิตแสดงรายการแต่ละงานของการดำเนินงานโดยละเอียด และรวมถึงการตั้งค่า กระบวนการ คิว และเวลาการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="382b4-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="382b4-124">ตัวอย่างเช่น การดำเนินการ เช่น การทาสีอาจต้องการแต่ละงาน เช่น เวลาตั้งค่า เวลาการดำเนินงานสำหรับกระบวนการทาสี และเวลาในการรอให้แห้ง</span><span class="sxs-lookup"><span data-stu-id="382b4-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="382b4-125">บัตรงาน</span><span class="sxs-lookup"><span data-stu-id="382b4-125">Job cards</span></span>

<span data-ttu-id="382b4-126">บัตรงานแสดงรายการแต่ละหมายเลขงานของการดำเนินงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="382b4-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="382b4-127">งานหนึ่งงานปรากฏขึ้นบนแต่ละหน้า</span><span class="sxs-lookup"><span data-stu-id="382b4-127">One job appears on each page.</span></span> <span data-ttu-id="382b4-128">งานที่รวมอยู่ในบัตรงานและเวลาโดยประมาณ มาจากข้อมูลการตั้งค่ากระบวนการผลิตและการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="382b4-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="382b4-129">จากบัตรงาน คุณสามารถเปิดหน้า **รายการสมุดรายวันการผลิต** **บัตรงาน** ได้</span><span class="sxs-lookup"><span data-stu-id="382b4-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="382b4-130">บุคคลที่ดำเนินการทรัพยากรการดำเนินงานสามารถให้ผลป้อนกลับเกี่ยวกับกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="382b4-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="382b4-131">มีฟิลด์ที่คุณสามารถป้อนสถิติปริมาณการใช้และข้อมูล เช่น ปริมาณสินค้าที่บกพร่อง</span><span class="sxs-lookup"><span data-stu-id="382b4-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="382b4-132">งานคลังสินค้าสำหรับการเบิกวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="382b4-132">Warehouse work for raw material picking</span></span>

<span data-ttu-id="382b4-133">มีการสร้างงานสำหรับการเบิกวัตถุดิบในระหว่างการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="382b4-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="382b4-134">มีการสร้างงานสำหรับเฉพาะปริมาณของวัสดุที่มีการจองทางกายภาพสำหรับใบสั่งผลิตก่อนนำใบสั่งออกใช้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="382b4-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="382b4-135">การตั้งค่าต่อไปนี้จำเป็นต้องใช้ในการสร้างงานที่คลังสินค้าสำหรับการเบิกวัตถุดิบ:</span><span class="sxs-lookup"><span data-stu-id="382b4-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

- <span data-ttu-id="382b4-136">คำสั่งสถานที่สำหรับการเบิกวัตถุดิบที่กำหนดว่าที่ตั้งคลังสินค้าใดที่จะเบิกวัสดุ</span><span class="sxs-lookup"><span data-stu-id="382b4-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
- <span data-ttu-id="382b4-137">เท็มเพลตเวฟสำหรับวัตถุดิบ ที่มีการตั้งค่าคอนฟิกนโยบายสำหรับการดำเนินงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="382b4-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
- <span data-ttu-id="382b4-138">ที่ตั้งอินพุทการผลิตที่กำหนดที่วางวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="382b4-138">A production input location that determines where materials are put</span></span>

<span data-ttu-id="382b4-139">เมื่อใช้สถานที่ควบคุมป้ายทะเบียน คุณสามารถเลือกว่าปริมาณที่สั่งหรือปริมาณทั้งหมดที่มีอยู่ของสินค้าควรมีการเบิกสินค้าขณะประมวลผลงานการเบิกวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="382b4-139">When using license plate controlled locations, you can choose whether the ordered quantity or the full quantity available for the item should be picked while processing the raw material picking work.</span></span> <span data-ttu-id="382b4-140">เพื่อตั้งค่าตัวเลือกนี้:</span><span class="sxs-lookup"><span data-stu-id="382b4-140">To set this option:</span></span>

1. <span data-ttu-id="382b4-141">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้** แล้วเปิดสินค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="382b4-141">Go to **Product information management \> Products \> Released products** and open the relevant item.</span></span>
1. <span data-ttu-id="382b4-142">ขยายแท็บด่วน **คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="382b4-142">Expand the **Warehouse** FastTab.</span></span>
1. <span data-ttu-id="382b4-143">เลือกหนึ่งในตัวเลือกต่อไปนี้สำหรับฟิลด์ **การเบิกวัสดุในสถานที่ป้ายทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="382b4-143">Select one of the following options for the  **Material picking in license plate locations** field:</span></span>
    - <span data-ttu-id="382b4-144">*การเบิกสินค้าตามใบสั่ง*: ควรเบิกสินค้าเฉพาะปริมาณที่สั่งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="382b4-144">*Order picking*: Only the ordered quantity should be picked.</span></span>
    - <span data-ttu-id="382b4-145">*การจัดเตรียม*: เมื่อใดก็ตามที่เป็นไปได้ ปริมาณทั้งหมดที่พร้อมใช้งานที่ป้ายทะเบียนควรถูกเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="382b4-145">*Staging*: Whenever possible, the full quantity available at the license plate should be picked.</span></span> <span data-ttu-id="382b4-146">เพื่อให้ผู้ปฏิบัติงานสามารถเบิกปริมาณป้ายทะเบียนแบบเต็มได้ ป้ายทะเบียนต้องไม่มีสินค้าผสมและต้องไม่มีมิติผสม</span><span class="sxs-lookup"><span data-stu-id="382b4-146">For a worker to be able to pick the full license plate quantity, the license plate must not contain mixed items and must not have mixed dimensions.</span></span> <span data-ttu-id="382b4-147">หากป้ายทะเบียนมีมิติหรือสินค้าผสม การเบิกสินค้าจะดําเนินการต่อไปเหมือนกับถูกตั้งค่าเป็น *การเบิกสินค้าตามใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="382b4-147">If the license plate contains mixed dimensions or items, the pick will proceed as if it were set to *Order picking*.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]