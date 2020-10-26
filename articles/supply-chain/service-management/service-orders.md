---
title: ใบสั่งบริการ
description: ใบสั่งบริการแสดงถึงการไปเยี่ยมที่ช่างเทคนิคบริการทำต่อไซต์ของลูกค้าในวันที่เฉพาะ
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b049b166edf2b5a318a4b1af85e7f74cfe433f2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975475"
---
# <a name="service-orders"></a><span data-ttu-id="169ae-103">ใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="169ae-104">ใบสั่งบริการแสดงถึงการไปเยี่ยมที่ช่างเทคนิคบริการทำต่อไซต์ของลูกค้าในวันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="169ae-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="169ae-105">ใบสั่งบริการแต่ละใบประกอบด้วยบรรทัดใบสั่งบริการหนึ่งบรรทัดขึ้นไป </span><span class="sxs-lookup"><span data-stu-id="169ae-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="169ae-106">รายการใบสั่งบริการแสดงชั่วโมงการทำงานที่ต้องดำเนินการโดยช่างเทคนิคที่ให้บริการ และสินค้าที่เกี่ยวข้อง ค่าใช้จ่าย และค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="169ae-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="169ae-107">คุณสามารถแนบภารกิจและวัตถุกับรายการใบสั่งบริการได้</span><span class="sxs-lookup"><span data-stu-id="169ae-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="169ae-108">จากนั้น คุณสามารถจัดกลุ่มรายการใบสั่งบริการได้ตามภารกิจ หรือตามวัตถุ</span><span class="sxs-lookup"><span data-stu-id="169ae-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="169ae-109">คุณยังสามารถแนบสินค้าที่แสดงรายการในสินค้าคงคลังกับรายการใบสั่งบริการได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="169ae-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="169ae-110">สร้างใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-110">Create service orders</span></span>

<span data-ttu-id="169ae-111">คุณสามารถสร้างใบสั่งบริการที่เป็นไปตามข้อตกลงการให้บริการ และรายการที่อยู่ในข้อตกลงนั้น</span><span class="sxs-lookup"><span data-stu-id="169ae-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="169ae-112">อย่างไรก็ตาม คุณสามารถสร้างใบสั่งบริการที่เชื่อมโยงกับข้อตกลงการให้บริการในรอบระยะเวลาที่ระบุไว้ในข้อตกลงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="169ae-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="169ae-113">ตัวอย่างเช่น ถ้าข้อตกลงการให้บริการมีผลบังคับใช้สำหรับปีปฏิทิน 2011 คุณสามารถสร้างใบสั่งบริการสำหรับข้อตกลงตั้งแต่ 1 มกราคม 2011 และ 31 ธันวาคม 2011 ได้</span><span class="sxs-lookup"><span data-stu-id="169ae-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="169ae-114">คุณยังสามารถสร้างใบสั่งบริการได้โดยแยกกัน โดยไม่ต้องเชื่อมโยงใบสั่งบริการนั้นกับข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="169ae-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="169ae-115">ใบสั่งบริการเหล่านี้สามารถใช้เพื่อจัดการกับการไปเยี่ยมเพื่อให้บริการขาจร หรือไม่ได้จัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="169ae-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="169ae-116">ตัวอย่างเช่น ในเดือนมีนาคม ลูกค้าของคุณต้องการให้ดำเนินการบริการในเครื่องจักรสองเครื่อง เพิ่มเติมจากเครื่องจักรที่ระบุไว้ในข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="169ae-117">สำหรับภารกิจนี้ คุณสร้างใบสั่งบริการ แต่ต้องไม่ต้องเชื่อมโยงกับข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="169ae-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="169ae-118">เมื่อต้องการสร้างใบสั่งบริการที่ไม่เกี่ยวข้องกับข้อตกลงการให้บริการ คุณต้องเลือกกล่องกาเครื่องหมาย <STRONG>อนุญาตโดยไม่มีข้อตกลงการให้บริการ</STRONG> ในแบบฟอร์ม <STRONG>พารามิเตอร์การจัดการบริการ</STRONG></span><span class="sxs-lookup"><span data-stu-id="169ae-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="169ae-119">**สถานการณ์จำลอง**</span><span class="sxs-lookup"><span data-stu-id="169ae-119">**Scenario**</span></span>

<span data-ttu-id="169ae-120">สถานการณ์จำลองต่อไปนี้อธิบายถึง สถานการณ์อื่นซึ่งมีประโยชน์ในการสร้างใบสั่งบริการที่ไม่เกี่ยวข้องกับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="169ae-121">ผู้จัดส่งของบริษัทได้รับโทรศัพท์ร้องขอการบริการฉุกเฉินสำหรับลิฟต์ </span><span class="sxs-lookup"><span data-stu-id="169ae-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="169ae-122">ไม่มีเวลาในการตั้งค่าข้อตกลงการให้บริการและโครงการสำหรับการบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="169ae-123">ดังนั้น ผู้จัดส่งจะสร้างใบสั่งบริการได้โดยตรงในแบบฟอร์ม **ใบสั่งบริการ** จะแนบใบสั่งบริการกับโครงการที่มีอยู่ และสร้างรายการใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="169ae-124">ผู้จัดส่งยังสร้างความสัมพันธ์ของภารกิจหรือวัตถุสำหรับใบสั่งบริการที่มีอยู่ด้วย เพื่อบันทึกงานที่ไม่เกี่ยวข้องกับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="169ae-125">สำหรับข้อมูลเพิ่มเติม ดู [สร้างใบสั่งบริการด้วยตนเอง](create-service-orders-manually.md) และ [สร้างความสัมพันธ์ของภารกิจการให้บริการ](create-service-task-relations.md)</span><span class="sxs-lookup"><span data-stu-id="169ae-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="169ae-126">ตรวจสอบความคืบหน้าของใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="169ae-127">เพื่อตรวจสอบความคืบหน้าของใบสั่งขายผ่านทางทีมงานและกระบวนงานที่แตกต่างกัน คุณสามารถตั้งค่าระบบของขั้นตอนและรหัสเหตุผลสำหรับใบสั่งบริการได้</span><span class="sxs-lookup"><span data-stu-id="169ae-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="169ae-128">สำหรับแต่ละขั้นตอน คุณสามารถระบุการดำเนินการที่ได้รับอนุญาตได้</span><span class="sxs-lookup"><span data-stu-id="169ae-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="169ae-129">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างรหัสเหตุผล](create-reason-codes.md)</span><span class="sxs-lookup"><span data-stu-id="169ae-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="169ae-130">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="169ae-130">**Example**</span></span>

<span data-ttu-id="169ae-131">ใบสั่งบริการได้รับการอนุมัติโดยผู้จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="169ae-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="169ae-132">ผู้จัดส่งอัพเดตขั้นตอนของใบสั่งบริการ และระบุรหัสเหตุผลที่บ่งชี้ว่า ใบสั่งบริการได้ถูกนำออกใช้ให้แก่ช่างเทคนิคการบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="169ae-133">ช่างเทคนิคไปที่ไซต์ของลูกค้าและดำเนินการบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="169ae-134">ระบุความต้องการสินค้าสำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="169ae-135">คุณสามารถระบุสินค้าคงคลังที่จำเป็นสำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="169ae-136">อย่างไรก็ตาม ใบสั่งบริการต้องเชื่อมโยงกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="169ae-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="169ae-137">ข้อกำหนดรายการสำหรับใบสั่งรายการมีการประมวลผลผ่านโครงการ </span><span class="sxs-lookup"><span data-stu-id="169ae-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="169ae-138">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="169ae-138">**Example**</span></span>

<span data-ttu-id="169ae-139">ใบสั่งบริการที่ถูกสร้างขึ้นจากข้อตกลงการให้บริการจะถูกประมวลผลโดยผู้จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="169ae-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="169ae-140">สำหรับใบสั่งบริการแรก ผู้จัดส่งพบว่าช่างเทคนิคบริการต้องการอะไหล่สำรองที่สำคัญที่ไม่มีในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="169ae-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="169ae-141">ดังนั้น ผู้จัดส่งจะสร้างความต้องการสินค้าสำหรับอะไหล่สำรองนั้นจากใบสั่งบริการโดยตรง</span><span class="sxs-lookup"><span data-stu-id="169ae-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="169ae-142">การย้ายและลงรายการบัญชีบรรทัด</span><span class="sxs-lookup"><span data-stu-id="169ae-142">Move and post lines</span></span>

<span data-ttu-id="169ae-143">ช่างเทคนิคการบริการกลับจากการให้บริการ และจากนั้นจะปรับปรุงและอัพเดตรายการใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="169ae-144">ในขณะที่ให้บริการ ช่างเทคนิคทำงานการบริการที่ถูกจัดกำหนดการไว้สำหรับการให้บริการครั้งถัดไป</span><span class="sxs-lookup"><span data-stu-id="169ae-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="169ae-145">ดังนั้น ช่างเทคนิคจึงย้ายรายการจากการให้บริการครั้งถัดไป มาที่การให้บริการปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="169ae-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="169ae-146">จากนั้น ช่างเทคนิคจะลงรายการบัญชีใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-146">The technician then posts the service order.</span></span> <span data-ttu-id="169ae-147">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ย้ายรายการใบสั่งบริการ](move-service-order-lines.md)</span><span class="sxs-lookup"><span data-stu-id="169ae-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="169ae-148">ยกเลิกใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-148">Cancel service orders</span></span>

<span data-ttu-id="169ae-149">หนึ่งในใบสั่งบริการอื่นที่สร้างขึ้นสำหรับเดือนมกราคมกลายเป็นใบสั่งบริการที่ล้าสมัย เนื่องจากงานถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="169ae-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="169ae-150">ดังนั้น ผู้จัดส่งการบริการจะยกเลิกใบสั่งบริการนั้น</span><span class="sxs-lookup"><span data-stu-id="169ae-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="169ae-151">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยกเลิกใบสั่งบริการ](cancel-service-orders.md)</span><span class="sxs-lookup"><span data-stu-id="169ae-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="169ae-152">ลงรายการบัญชีจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="169ae-152">Post from projects</span></span>

<span data-ttu-id="169ae-153">เมื่อสิ้นสุดแต่ละสัปดาห์ ผู้จัดส่งต้องการลงรายการบัญชีใบสั่งบริการทั้งหมดที่ถูกแนบอยู่กับโครงการเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="169ae-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="169ae-154">ดังนั้น ผู้จัดส่งจะค้นหาโครงการที่เกี่ยวข้องในแบบฟอร์ม **โครงการ** และลงรายการบัญชีใบสั่งบริการที่เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="169ae-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="169ae-155">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ลงรายการบัญชีใบสั่งบริการ (แบบฟอร์มคลาส)](https://technet.microsoft.com/library/aa574685\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="169ae-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="169ae-156">ลบใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="169ae-156">Delete service orders</span></span>

<span data-ttu-id="169ae-157">ในระหว่างครึ่งปีหลัง ลูกค้าของคุณตัดสินใจว่า การไปเยี่ยมเพื่อให้บริการมีความถี่มากเกินไป</span><span class="sxs-lookup"><span data-stu-id="169ae-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="169ae-158">คุณต้องสร้างชุดของการไปเยี่ยมเพื่อให้บริการใหม่ที่มีความถี่น้อยลงสำหรับเวลาที่เหลืออยู่ในข้อตกลงการให้บริการ </span><span class="sxs-lookup"><span data-stu-id="169ae-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="169ae-159">ดังนั้น คุณต้องลบใบสั่งบริการที่มีอยู่ และสร้างใบสั่งบริการใหม่</span><span class="sxs-lookup"><span data-stu-id="169ae-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="169ae-160">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ลบใบสั่งบริการ](delete-service-orders.md)</span><span class="sxs-lookup"><span data-stu-id="169ae-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="169ae-161">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="169ae-161">See also</span></span>

<span data-ttu-id="169ae-162">[ใบสั่งบริการ (แบบฟอร์ม)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="169ae-162">[Service orders (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span></span>

  


