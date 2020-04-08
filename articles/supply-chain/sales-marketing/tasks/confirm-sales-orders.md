---
title: ยืนยันใบสั่งขาย
description: 'ขั้นตอนนี้อธิบายวิธีการยืนยันใบสั่งขาย '
author: omulvad
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6383576302789d268d64edcbbe05305b03e956d0
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148726"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="e3cfc-103">ยืนยันใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="e3cfc-103">Confirm sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3cfc-104">ขั้นตอนนี้อธิบายวิธีการยืนยันใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="e3cfc-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="e3cfc-105">คุณจะได้เห็นวิธีการยืนยันใบสั่งเดียว และวิธีการยืนยันใบสั่งหลายใบพร้อมกันในครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="e3cfc-105">You'll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="e3cfc-106">งานเหล่านี้อาจจะสามารถกระทำโดยผู้ประมวลผลใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="e3cfc-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="e3cfc-107">คุณสามารถใช้ขั้นตอนนี้ในข้อมูลสาธิตบริษัท USMF หรือข้อมูลของคุณเอง </span><span class="sxs-lookup"><span data-stu-id="e3cfc-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="e3cfc-108">ก่อนที่คุณเริ่ม ตรวจสอบว่ามีใบสั่งขายหลายใบสำหรับลูกค้ารายเดียวกันเปิดอยู่ </span><span class="sxs-lookup"><span data-stu-id="e3cfc-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="e3cfc-109">ถ้าคุณกำลังใช้ USMF คุณสามารถใช้ลูกค้า US-027</span><span class="sxs-lookup"><span data-stu-id="e3cfc-109">If you're using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="e3cfc-110">ยืนยันใบสั่งขายใบเดียว</span><span class="sxs-lookup"><span data-stu-id="e3cfc-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="e3cfc-111">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-111">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="e3cfc-112">ในรายการ ค้นหาและเลือกใบสั่งที่คุณต้องการจะยืนยัน</span><span class="sxs-lookup"><span data-stu-id="e3cfc-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="e3cfc-113">คลิกลิงค์หมายเลขใบสั่งขายเพื่อเปิดใบสั่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e3cfc-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="e3cfc-114">ใน **บานหน้าต่างการดำเนินการ** คลิก **ขาย**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-114">On the **Action Pane**, click **Sell**.</span></span>
5. <span data-ttu-id="e3cfc-115">คลิก **ยืนยันใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-115">Click **Confirm sales order**.</span></span>
6. <span data-ttu-id="e3cfc-116">ขยายส่วน **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-116">Expand the **Parameters** section.</span></span> <span data-ttu-id="e3cfc-117">ตรวจสอบให้แน่ใจว่าตัวเลือก **การลงรายการบัญชี** ได้ถูกตั้งค่าเป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="e3cfc-117">Make sure that the **Posting** option is set to 'Yes'.</span></span>  
7. <span data-ttu-id="e3cfc-118">ตั้งค่า **ตัวเลือกการพิมพ์ใบยืนยันการขาย** เป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="e3cfc-118">Set the **Print confirmation option** to 'Yes'.</span></span> <span data-ttu-id="e3cfc-119">ฟิลด์ **เช็ควงเงินสินเชื่อ** เป็นการระบุวิธีการที่ใช้ในการคำนวณสินเชื่อคงเหลือของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e3cfc-119">The **Check credit limit** field specifies the method that's used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="e3cfc-120">โดยค่าเริ่มต้น จะมีการคัดลอกมาจากหน้าพารามิเตอร์บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="e3cfc-120">By default, it's copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="e3cfc-121">ถ้าคุณต้องการข้ามการตรวจสอบวงเงินสินเชื่อเมื่อมีการยืนยันใบสั่งขาย ให้ตั้งค่า **ตรวจสอบวงเงินสินเชื่อ** เป็น 'ไม่มี'</span><span class="sxs-lookup"><span data-stu-id="e3cfc-121">If you want to skip the credit limit check when confirming a specific sales order, set the **Check credit limit** to 'None'.</span></span> <span data-ttu-id="e3cfc-122">อย่างไรก็ตาม คุณควรทราบว่าแม้ว่าถ้าฟิลด์นี้ถูกกำหนดเป็น 'ไม่มี' การตรวจสอบวงเงินสินเชื่อจะยังคงต้องทำถ้าเลือกตัวเลือก **บังคับสำหรับวงเงินสินเชื่อ** ในข้อมูลหลักของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e3cfc-122">However, you should be aware that even with if this field is set to 'None', the credit limit check will still be performed if the **Mandatory credit limit** option is selected on the customer master data.</span></span> 
8. <span data-ttu-id="e3cfc-123">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-123">Click **OK**.</span></span>
9. <span data-ttu-id="e3cfc-124">คลิก **ใช่** </span><span class="sxs-lookup"><span data-stu-id="e3cfc-124">Click **Yes**.</span></span>
10. <span data-ttu-id="e3cfc-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e3cfc-125">Close the page.</span></span>
11. <span data-ttu-id="e3cfc-126">ใน **หน้าต่างการดำเนินการ** คลิก **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-126">On the **Action Pane**, click **Options**.</span></span>
12. <span data-ttu-id="e3cfc-127">คลิก **เปลี่ยนมุมมอง**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-127">Click **Change view**.</span></span>
13. <span data-ttu-id="e3cfc-128">คลิก **มุมมองหัวข้อ**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-128">Click **Header view**.</span></span> <span data-ttu-id="e3cfc-129">เมื่อมีการยืนยันใบสั่ง **สถานะของเอกสาร** จะตั้งค่าเป็น 'การยืนยัน'</span><span class="sxs-lookup"><span data-stu-id="e3cfc-129">When an order is confirmed, the **Document status** is set to 'Confirmation'.</span></span> 
14. <span data-ttu-id="e3cfc-130">ใน **บานหน้าต่างการดำเนินการ** คลิก **ขาย**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-130">On the **Action Pane**, click **Sell**.</span></span>
15. <span data-ttu-id="e3cfc-131">คลิก **การยืนยันใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-131">Click **Sales order confirmation**.</span></span>
16. <span data-ttu-id="e3cfc-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e3cfc-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="e3cfc-133">ยืนยันใบสั่งขายหลายใบพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="e3cfc-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="e3cfc-134">ไปที่ **การขายและการตลาด > ใบสั่งขาย > การยืนยันใบสั่ง > ยืนยันใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-134">Go to **Sales and marketing > Sales orders > Order confirmation > Confirm sales order**.</span></span>
2. <span data-ttu-id="e3cfc-135">คลิก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-135">Click **Select**.</span></span>
3. <span data-ttu-id="e3cfc-136">ในรายการบนแท็บ **การกำหนดช่วง** หาและเลือกเรกคอร์ดที่อ้างอิงฟิลด์ **บัญชีลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-136">In the list on the **Range** tab, find and select the record that references the **Customer account** field.</span></span>
4. <span data-ttu-id="e3cfc-137">ในฟิลด์ **เงื่อนไข** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="e3cfc-137">In the **Criteria** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e3cfc-138">ในรายการ ค้นหาและเลือกบัญชีลูกค้าที่มีใบสั่งหลายใบซึ่งคุณต้องการยืนยันโดยรวม</span><span class="sxs-lookup"><span data-stu-id="e3cfc-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span> <span data-ttu-id="e3cfc-139">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือกบัญชี US-027</span><span class="sxs-lookup"><span data-stu-id="e3cfc-139">If you're using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="e3cfc-140">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-140">Click **OK**.</span></span>
    - <span data-ttu-id="e3cfc-141">แท็บ **ภาพรวม** จะแสดงรายการของใบสั่งที่ตรงกับเกณฑ์การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="e3cfc-141">The **Overview** tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="e3cfc-142">รายการต่อไปนี้จะถูกรวมในรายการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="e3cfc-142">These will be included in the confirmation.</span></span>  
    - <span data-ttu-id="e3cfc-143">ฟิลด์ **การอัพเดตสรุป** สำหรับที่ระบุในส่วน **พารามิเตอร์** โดยใบสั่งหลายใบจะสรุปเข้าในเอกสารใบยืนยันหนึ่งฉบับ</span><span class="sxs-lookup"><span data-stu-id="e3cfc-143">The **Summary update for** field in the **Parameters** section specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="e3cfc-144">โดยค่าเริ่มต้น ตัวเลือกจะถูกคัดลอกจาก **ค่าเริ่มต้นสำหรับการตั้งค่าอัพเดตสรุป** ในเพจ **พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-144">By default, the option is copied from the D**efault values for summary update setting** on the **Accounts receivable parameters** page.</span></span>  
7. <span data-ttu-id="e3cfc-145">ในฟิลด์ **อัพเดตสรุป** เลือก 'ใบสั่ง'</span><span class="sxs-lookup"><span data-stu-id="e3cfc-145">In the **Summary update for** field, select 'Order'.</span></span> <span data-ttu-id="e3cfc-146">พารามิเตอร์ขั้นต่ำที่จำเป็นเพื่อการสร้างอัพเดตสรุปคือ **บัญชีใบแจ้งหนี้** และ **สกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-146">The minimum parameters that are required to create summary updates are **Invoice account** and **Currency**.</span></span> <span data-ttu-id="e3cfc-147">ซึ่งหมายความว่า การอัพเดตสรุปที่มีบัญชีใบแจ้งหนี้ที่แตกต่างกันและสกุลเงินที่แตกต่างกันนั้นไม่ได้รับอนุญาต </span><span class="sxs-lookup"><span data-stu-id="e3cfc-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="e3cfc-148">สามารถตั้งค่าพารามิเตอร์เพิ่มเติมได้ในเพจ **พารามิเตอร์การอัพเดตบทสรุป** ซึ่งสามารถเข้าถึงได้จากเพจ **พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-148">Additional parameters can be set up in the **Summary update parameters** page which is accessible from the **Accounts receivable parameters** page.</span></span> 
8. <span data-ttu-id="e3cfc-149">ในฟิลด์ **ใบสั่งขาย** คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="e3cfc-149">In the **Sales order** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e3cfc-150">ในรายการ ให้เลือกหมายเลขใบสั่งซื้อที่คุณต้องการใบสั่งสรุป</span><span class="sxs-lookup"><span data-stu-id="e3cfc-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="e3cfc-151">คลิก **จัดเรียง**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-151">Click **Arrange**.</span></span>
11. <span data-ttu-id="e3cfc-152">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-152">Click **OK**.</span></span>
12. <span data-ttu-id="e3cfc-153">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e3cfc-153">Click **OK**.</span></span>

