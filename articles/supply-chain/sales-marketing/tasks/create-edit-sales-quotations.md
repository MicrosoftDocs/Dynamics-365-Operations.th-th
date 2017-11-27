--- 
title: "สร้างและแก้ไขใบเสนอราคาขาย"
description: "กระบวนงานนี้อธิบายวิธีการสร้างและปรับปรุงใบเสนอราคาขาย "
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: 7ffa4fe8d87db5b3f8293ec9dbc042496d09d6e3
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="54615-103">สร้างและแก้ไขใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="54615-103">Create and edit sales quotations</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54615-104">กระบวนงานนี้อธิบายวิธีการสร้างและปรับปรุงใบเสนอราคาขาย </span><span class="sxs-lookup"><span data-stu-id="54615-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="54615-105">คุณสามารถทำตามขั้นตอนเหล่านี้กับข้อมูลของคุณ หรือกับบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="54615-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="54615-106">สร้างใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="54615-106">Create a sales quotation</span></span>
1. <span data-ttu-id="54615-107">ไปยัง การขายและการตลาด > ใบเสนอราคาขาย > ใบเสนอราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="54615-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="54615-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="54615-108">Click New.</span></span>
3. <span data-ttu-id="54615-109">ในฟิลด์ชนิดบัญชี ให้เลือก 'ผู้ที่มีแนวโน้มจะเป็นลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="54615-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="54615-110">ในฟิลด์ผู้ที่มีแนวโน้มจะเป็นลูกค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="54615-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="54615-111">ขยายส่วน ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="54615-111">Expand the General section.</span></span>
    * <span data-ttu-id="54615-112">เนื่องจากคุณเลือกที่จะสร้างใบเสนอราคาจากพื้นที่การขายและการตลาด ชนิดจะถูกกำหนดโดยอัตโนมัติไปยังใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="54615-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="54615-113">เมื่อต้องการสร้างใบเสนอราคาสำหรับโครงการ คุณต้องเข้าถึงได้จากการจัดการโครงการและโมดูลการบัญชี</span><span class="sxs-lookup"><span data-stu-id="54615-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="54615-114">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="54615-114">Click OK.</span></span>
    * <span data-ttu-id="54615-115">ฟิลด์และการดำเนินการต่างๆบนรายการใบเสนอราคาจะคล้ายกันมากกับในรายการใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="54615-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="54615-116">เช่นเดียวกับใบสั่งขาย ใบเสนอราคาสามารถสร้างขึ้นได้สำหรับสินค้าหนึ่งๆ หรือเมื่อไม่ทราบหมายเลขสินค้า หรือไม่ปรากฏอยู่ในเวลาการสร้างใบเสนอราคา ใบเสนอราคาจะสามารถสร้างขึ้นได้สำหรับประเภทการขาย</span><span class="sxs-lookup"><span data-stu-id="54615-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="54615-117">ในฟิลด์สินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="54615-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="54615-118">ในฟิลด์สินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="54615-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="54615-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54615-119">Close the page.</span></span>
10. <span data-ttu-id="54615-120">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="54615-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="54615-121">ถ้ามีข้อตกลงทางการค้าที่ถูกต้องสำหรับสินค้าที่เลือกไว้ในรายการ ราคาและส่วนลดที่เกี่ยวข้องจะถูกคัดลอกโดยอัตโนมัติไปยังรายการใบเสนอราคา </span><span class="sxs-lookup"><span data-stu-id="54615-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="54615-122">ตรวจสอบให้แน่ใจว่า ฟิลด์ราคาต่อหน่วยประกอบด้วยค่าและคุณยังสามารถป้อนมูลค่าส่วนลดได้ด้วยถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="54615-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="54615-123">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="54615-123">Click Save.</span></span>
12. <span data-ttu-id="54615-124">ในบานหน้าต่างการดำเนินการ คลิก ใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="54615-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="54615-125">คลิก ผลรวม</span><span class="sxs-lookup"><span data-stu-id="54615-125">Click Totals.</span></span>
14. <span data-ttu-id="54615-126">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="54615-126">Click OK.</span></span>
15. <span data-ttu-id="54615-127">คลิก รายการใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="54615-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="54615-128">คลิก ราคา</span><span class="sxs-lookup"><span data-stu-id="54615-128">Click Prices.</span></span>
    * <span data-ttu-id="54615-129">ในหน้าการดำเนินการจำลองราคา คุณสามารถลองใช้การปรับรายได้ที่คาดไว้หรือผลกำไรของใบเสนอราคาของคุณตามราคาต่อหน่วยที่ต้องการ ยอดส่วนลด เปอร์เซ็นต์ส่วนลด ยอดรวม กำไรเบื้องต้น หรืออัตราส่วนกำไรผันแปร </span><span class="sxs-lookup"><span data-stu-id="54615-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="54615-130">เมื่อคุณพอใจกับตัวเลขเป้าหมาย คุณนำคำแนะนำไปใช้กับรายการใบเสนอราคา และฟิลด์ที่เกี่ยวข้องกับราคานั้นจะถูกอัพเดตให้สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="54615-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="54615-131">คุณสามารถสร้างการจำลองราคาได้มากเท่าที่คุณต้องการ </span><span class="sxs-lookup"><span data-stu-id="54615-131">You can create as many price simulations as you wish.</span></span> <span data-ttu-id="54615-132">เมื่อคุณคลิกที่ ใหม่ เงื่อนไขราคาจากใบเสนอราคาปัจจุบันจะถูกคัดลอกไปที่หน้า </span><span class="sxs-lookup"><span data-stu-id="54615-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="54615-133">จากนั้นคุุณจะสามารถแก้ไขค่าในฟิลด์ใดๆของที่เกี่ยวข้องกับราคาเป็นราคาเป้าหมาย </span><span class="sxs-lookup"><span data-stu-id="54615-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="54615-134">การเปลี่ยนแปลงในฟิลด์ใดฟิลด์หนึ่งจะทริกเกอร์การคำนวณใหม่ในการคำนวณอื่นๆ ทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="54615-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="54615-135">เพื่อให้ระบบคำนวณกำไรการขายและอัตราส่วนกำไรผันแปร ต้นทุนต่อหน่วยของผลิตภัณฑ์ได้จะต้องถูกแจ้งให้ทราบ </span><span class="sxs-lookup"><span data-stu-id="54615-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="54615-136">ใช้แท็บการจำลองราคาสำหรับมุมมองโดยละเอียดของราคาเดิม การเปลี่ยนแปลงที่ถูกเสนอ และผลกระทบต่อผลรวมของใบเสนอราคา </span><span class="sxs-lookup"><span data-stu-id="54615-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="54615-137">ตามกฎทั่วไป เมื่อการจำลองที่กำหนดยอดเงินใหม่ได้นำมาใช้กับรายการใบเสนอราคา ระบบจะคำนวณใหม่อีกครั้งและป้อนค่าใหม่ในฟิลด์ราคาต่อหน่วย </span><span class="sxs-lookup"><span data-stu-id="54615-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="54615-138">เมื่อมีการจำลองตามกำไรเบื้องต้นใหม่หรืออัตราส่วนกำไรผันแปรใหม่ เฉพาะฟิลด์ยอดเงินสุทธิเท่านั้นที่จะได้รับการอัพเดต และราคาต่อหน่วยเป็นจะเป็นช่องว่าง </span><span class="sxs-lookup"><span data-stu-id="54615-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="54615-139">ในทั้งสองกรณี ส่วนลดใดๆที่เคยอยู่บนรายการใบเสนอราคาก่อนการจำลองจะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="54615-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="54615-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54615-140">Close the page.</span></span>
18. <span data-ttu-id="54615-141">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="54615-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="54615-142">คลิก ส่งใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="54615-142">Click Send quotation.</span></span>
20. <span data-ttu-id="54615-143">เลือก ใช่ ในฟิลด์พิมพ์ใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="54615-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="54615-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="54615-144">Click OK.</span></span>
    * <span data-ttu-id="54615-145">รายงานอาจใช้เวลาสักครู่เพื่อที่สร้าง </span><span class="sxs-lookup"><span data-stu-id="54615-145">The report may take a minute to generate.</span></span> <span data-ttu-id="54615-146">อย่าปิดหน้าจนกว่าจะเสร็จสิ้นการสร้าง</span><span class="sxs-lookup"><span data-stu-id="54615-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="54615-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54615-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="54615-148">อัพเดตใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="54615-148">Update a sales quotation</span></span>
1. <span data-ttu-id="54615-149">ในบานหน้าต่างการดำเนินการ ให้คลิก ติดตามผล</span><span class="sxs-lookup"><span data-stu-id="54615-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="54615-150">คลิกการแปลงเป็นลูกค้า</span><span class="sxs-lookup"><span data-stu-id="54615-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="54615-151">ในฟิลด์บัญชีลูกค้า ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="54615-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="54615-152">คลิกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="54615-152">Click Check.</span></span>
    * <span data-ttu-id="54615-153">ตรวจสอบให้แน่ใจว่า คุณเห็นข้อความที่ว่าหมายเลขบัญชีที่คุณพิมพ์สามารถใช้ได้โดยอิสระ</span><span class="sxs-lookup"><span data-stu-id="54615-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="54615-154">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="54615-154">Click OK.</span></span>
    * <span data-ttu-id="54615-155">ขณะนี้ระบบได้สร้างบัญชีลูกค้าใหม่สำหรับผู้ที่มีแนวโน้มจะเป็นลูกค้าบนใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="54615-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="54615-156">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54615-156">Close the page.</span></span>
7. <span data-ttu-id="54615-157">ในบานหน้าต่างการดำเนินการ ให้คลิก ติดตามผล</span><span class="sxs-lookup"><span data-stu-id="54615-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="54615-158">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="54615-158">Click Confirm.</span></span>
9. <span data-ttu-id="54615-159">ในฟิลด์เหตุผล ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="54615-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="54615-160">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="54615-160">Click OK.</span></span>
11. <span data-ttu-id="54615-161">ในบานหน้าต่างการดำเนินการ ให้คลิก ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="54615-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="54615-162">คลิก ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="54615-162">Click Sales orders.</span></span>
13. <span data-ttu-id="54615-163">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54615-163">Close the page.</span></span>


