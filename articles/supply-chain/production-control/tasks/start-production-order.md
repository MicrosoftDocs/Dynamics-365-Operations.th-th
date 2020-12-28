---
title: เริ่มใบสั่งผลิต
description: 'กระบวนงานนี้แสดงวิธีการเริ่มใบสั่งผลิตลิในกระบวนการผลิต '
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47915a93151b1adc99ddb4e3facb29bf8db49dd6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438403"
---
# <a name="start-a-production-order"></a><span data-ttu-id="dcbcd-103">เริ่มใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="dcbcd-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dcbcd-104">กระบวนงานนี้แสดงวิธีการเริ่มใบสั่งผลิตลิในกระบวนการผลิต </span><span class="sxs-lookup"><span data-stu-id="dcbcd-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="dcbcd-105">เวลาและวัสดุที่ใช้ในการผลิตจะถูกรายงานในขั้นตอนนี้ </span><span class="sxs-lookup"><span data-stu-id="dcbcd-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="dcbcd-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="dcbcd-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="dcbcd-107">นี่เป็นขั้นตอนที่ห้าจากเจ็ดขั้นตอน ซึ่งอธิบายวงจรชีวิตของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="dcbcd-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="dcbcd-108">เริ่มใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="dcbcd-108">Start a production order</span></span>
1. <span data-ttu-id="dcbcd-109">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="dcbcd-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="dcbcd-110">เลือกใบสั่งผลิตที่มีสถานะเป็นนำออกใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="dcbcd-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="dcbcd-111">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="dcbcd-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="dcbcd-112">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dcbcd-112">Click Start.</span></span>
    * <span data-ttu-id="dcbcd-113">ในหน้านี้ คุณสามารถยืนยันจุดเริ่มต้นของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="dcbcd-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="dcbcd-114">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="dcbcd-114">Click the General tab.</span></span>
5. <span data-ttu-id="dcbcd-115">ในจากการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="dcbcd-115">In the From Oper.</span></span> <span data-ttu-id="dcbcd-116">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="dcbcd-116">No.</span></span> <span data-ttu-id="dcbcd-117">ฟิลด์ ป้อน '10'</span><span class="sxs-lookup"><span data-stu-id="dcbcd-117">field, enter '10'.</span></span>
6. <span data-ttu-id="dcbcd-118">ในฟิลด์ประเภทการทำงานของกระบวนการผลิตแบบอัตโนมัติ ให้เลือก 'เสมอ'</span><span class="sxs-lookup"><span data-stu-id="dcbcd-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="dcbcd-119">คลิกที่กล่องกาเครื่องหมายลงรายการบัญชีบัตรกระบวนการผลิตทันที</span><span class="sxs-lookup"><span data-stu-id="dcbcd-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="dcbcd-120">ในฟิลด์การใช้ BOM อัตโนมัติ ให้เลือก 'เสมอ'</span><span class="sxs-lookup"><span data-stu-id="dcbcd-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="dcbcd-121">คลิกที่กล่องกาเครื่องหมายลงรายการบัญชีรายการเบิกสินค้าทันที</span><span class="sxs-lookup"><span data-stu-id="dcbcd-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="dcbcd-122">คลิกที่กล่องกาเครื่องหมายการพิมพ์รายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="dcbcd-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="dcbcd-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="dcbcd-123">Click OK.</span></span>
    * <span data-ttu-id="dcbcd-124">นี่คือรายการเบิกสินค้าที่พิมพ์ออกมา ซึ่งใช้แสดงวัสดุที่ใช้สำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="dcbcd-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="dcbcd-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dcbcd-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="dcbcd-126">ตรวจสอบความถูกต้องของรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="dcbcd-126">Validate the picking list</span></span>
1. <span data-ttu-id="dcbcd-127">ในบานหน้าต่างการดำเนินการ ให้คลิก ดู</span><span class="sxs-lookup"><span data-stu-id="dcbcd-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="dcbcd-128">คลิกรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="dcbcd-128">Click Picking list.</span></span>
3. <span data-ttu-id="dcbcd-129">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="dcbcd-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="dcbcd-130">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="dcbcd-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="dcbcd-131">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="dcbcd-131">Click Edit.</span></span>
6. <span data-ttu-id="dcbcd-132">ในฟิลด์ปริมาณการใช้ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="dcbcd-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="dcbcd-133">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="dcbcd-133">Click Post.</span></span>
8. <span data-ttu-id="dcbcd-134">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="dcbcd-134">Click OK.</span></span>
    * <span data-ttu-id="dcbcd-135">ในสมุดรายวันการเบิกสินค้า วัตถุดิบที่ใช้โดยใบสั่งผลิตถูกนำลงรายการบัญชี </span><span class="sxs-lookup"><span data-stu-id="dcbcd-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="dcbcd-136">ก่อนจะลงรายการบัญชีสมุดรายวัน คุณสามารถทำการปรับปรุงได้ ถ้ามีความแตกต่างระหว่างปริมาณที่ประเมินไว้และปริมาณที่ใช้จริง</span><span class="sxs-lookup"><span data-stu-id="dcbcd-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="dcbcd-137">คลิกแท็บ GridPanel</span><span class="sxs-lookup"><span data-stu-id="dcbcd-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="dcbcd-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dcbcd-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="dcbcd-139">ตรวจสอบสมุดรายวันบัตรกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="dcbcd-139">Verify the route card journal</span></span>
1. <span data-ttu-id="dcbcd-140">ในบานหน้าต่างการดำเนินการ ให้คลิก ดู</span><span class="sxs-lookup"><span data-stu-id="dcbcd-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="dcbcd-141">คลิก บัตรกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="dcbcd-141">Click Route card.</span></span>
3. <span data-ttu-id="dcbcd-142">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="dcbcd-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="dcbcd-143">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="dcbcd-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="dcbcd-144">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="dcbcd-144">Click Edit.</span></span>
6. <span data-ttu-id="dcbcd-145">ในฟิลด์ชั่วโมง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="dcbcd-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="dcbcd-146">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="dcbcd-146">Click Post.</span></span>
8. <span data-ttu-id="dcbcd-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="dcbcd-147">Click OK.</span></span>
    * <span data-ttu-id="dcbcd-148">ในสมุดรายวันบัตรกระบวนการผลิต เวลาที่ใช้ในการดำเนินงานแต่ละตัวจะถูกบันทึกลงไป </span><span class="sxs-lookup"><span data-stu-id="dcbcd-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="dcbcd-149">นอกจากยังนี้สามารถรายงานปริมาณสินค้าที่ดีและข้อผิดพลาดได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="dcbcd-149">Good and error quantity can also be reported.</span></span>  
