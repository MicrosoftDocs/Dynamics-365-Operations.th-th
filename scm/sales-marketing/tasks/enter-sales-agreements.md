--- 
title: "ป้อนข้อตกลงการขาย"
description: "ขั้นตอนนี้แสดงวิธีการสร้างข้อตกลงการขายที่ยืนยันที่ลูกค้าของคุณให้ซื้อผลิตภัณฑ์เป็นจำนวนที่ตกลงกันตามช่วงเวลาการแลกเปลี่ยนสำหรับส่วนลดพิเศษ"
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 943ae430b148670d248716c9ece21850bf7d2dfd
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="766ca-103">ป้อนข้อตกลงการขาย</span><span class="sxs-lookup"><span data-stu-id="766ca-103">Enter sales agreements</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="766ca-104">ขั้นตอนนี้แสดงวิธีการสร้างข้อตกลงการขายที่ยืนยันที่ลูกค้าของคุณให้ซื้อผลิตภัณฑ์เป็น</span><span class="sxs-lookup"><span data-stu-id="766ca-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an</span></span>

<span data-ttu-id="766ca-105">จำนวนที่ตกลงกันตามช่วงเวลาการแลกเปลี่ยนสำหรับส่วนลดพิเศษ</span><span class="sxs-lookup"><span data-stu-id="766ca-105">agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="766ca-106">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="766ca-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="766ca-107">ตั้งค่าส่วนหัวข้อตกลงการขาย</span><span class="sxs-lookup"><span data-stu-id="766ca-107">Set up sales agreement header</span></span>
1. <span data-ttu-id="766ca-108">ไปที่ การขายและการตลาด > ข้อตกลงการขาย > ข้อตกลงการขาย</span><span class="sxs-lookup"><span data-stu-id="766ca-108">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="766ca-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="766ca-109">Click New.</span></span>
3. <span data-ttu-id="766ca-110">ในฟิลด์บัญชีลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="766ca-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="766ca-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="766ca-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="766ca-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="766ca-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="766ca-113">ในฟิลด์การจัดประเภทข้อตกลงการขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="766ca-113">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="766ca-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="766ca-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="766ca-115">ขยายส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="766ca-115">Expand the General section.</span></span>
9. <span data-ttu-id="766ca-116">ในฟิลด์ข้อผูกมัดเริ่มต้น เลือก 'ข้อผูกมัดมูลค่าผลิตภัณฑ์'</span><span class="sxs-lookup"><span data-stu-id="766ca-116">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="766ca-117">ประเภทข้อผูกมัดไม่บังคับใช้หลักเกณฑ์ที่คุณต้องมอบหมายไปยังข้อตกลงเพื่อกำหนดว่าจะครบถ้วนตามที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="766ca-117">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="766ca-118">สี่ประเภทที่กำหนดไว้ล่วงหน้าช่วยให้คุณตั้งค่าเป้าหมายข้อผูกมัดของลูกค้า แสดงเป็นปริมาณหรือค่า</span><span class="sxs-lookup"><span data-stu-id="766ca-118">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="766ca-119">ชนิดข้อผูกมัดของปริมาณสามารถใช้ได้เฉพาะกับผลิตภัณฑ์ที่ระบุ แต่ชนิดตามมูลค่าจะสามารถใช้ได้กับการขายของผลิตภัณฑ์ทั้งเฉพาะและไม่ใช่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="766ca-119">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="766ca-120">ในฟิลด์วันหมดอายุ ตั้งค่าวันที่เป็นวันที่ในอนาคตเมื่อคุณต้องการให้ข้อตกลงหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="766ca-120">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="766ca-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="766ca-121">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="766ca-122">ตั้งค่ารายการข้อผูกมัดเกี่ยวกับมูลค่าผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="766ca-122">Set up product value commitment lines</span></span>
1. <span data-ttu-id="766ca-123">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="766ca-123">Click Add line.</span></span>
2. <span data-ttu-id="766ca-124">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="766ca-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="766ca-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="766ca-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="766ca-126">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="766ca-126">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="766ca-127">ชนิดของข้อผูกมัดที่คุณเลือกสำหรับข้อตกลงมีผลต่อชนิดของข้อมูลที่คุณสามารถป้อนสำหรับรายการข้อตกลง </span><span class="sxs-lookup"><span data-stu-id="766ca-127">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="766ca-128">ตัวอย่างเช่น สำหรับข้อตกลงตามค่าที่คุณต้องระบุยอดรวมสุทธิ (ในสกุลเงินที่ตกลงกัน) สำหรับลูกค้าที่ตกลงจะซื้อสินค้าจากคุณ</span><span class="sxs-lookup"><span data-stu-id="766ca-128">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="766ca-129">ในตัวอย่างนี้ ฟิลด์ปริมาณและหน่วยในรายการไม่พร้อมใช้งานเนื่องจากคุณกำลังสร้างข้อตกลงสำหรับลูกค้าเพื่อจะซื้อผลิตภัณฑ์ตามค่าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="766ca-129">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="766ca-130">ในฟิลด์ยอดเงินสุทธิ ป้อนยอดเงินที่ลูกค้าได้ตกลงที่จะซื้อ</span><span class="sxs-lookup"><span data-stu-id="766ca-130">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="766ca-131">ในฟิลด์เปอร์เซ็นต์ส่วนลด ป้อนค่าเปอร์เซ็นต์ที่จะใช้กับรายการใบสั่งขายของลูกค้าที่เชื่อมโยงกับข้อตกลงนี้</span><span class="sxs-lookup"><span data-stu-id="766ca-131">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="766ca-132">ขยายส่วน รายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="766ca-132">Expand the Line details section.</span></span>
8. <span data-ttu-id="766ca-133">เลือกใช่ในฟิลด์ค่าสูงสุดที่ถูกบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="766ca-133">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="766ca-134">การเลือก Max จะถูกบังคับ แสดงว่าจำนวนรวมของรายการใบสั่งขายทั้งหมดที่ใช้ข้อผูกมัดราคาพิเศษ ส่วนลด และ/หรือเงื่อนไขการชำระเงินต้องไม่เกินจำนวนเงินที่ระบุในข้อผูกมัด</span><span class="sxs-lookup"><span data-stu-id="766ca-134">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="766ca-135">จำนวนเงินนำออกใช้ต่ำสุดและสูงสุดระบุช่วงของมูลค่าที่ต้องขายในใบสั่งขายแต่ละรายการที่ใช้ข้อตกลงที่เลือก</span><span class="sxs-lookup"><span data-stu-id="766ca-135">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="766ca-136">ขยายส่วนหัวของข้อตกลงการขาย</span><span class="sxs-lookup"><span data-stu-id="766ca-136">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="766ca-137">จนกว่าจะมีการตั้งค่าสถานะของข้อตกลงเป็นมีผลบังคับใช้ ใบสั่งขายจะไม่สามารถเชื่อมโยงกับข้อตกลง และดังนั้นมันไม่สามารถเป็นส่วนหนึ่งของส่วนเติมเต็มข้อตกลงนั้น </span><span class="sxs-lookup"><span data-stu-id="766ca-137">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="766ca-138">คุณสามารถเปลี่ยนสถานะด้วยตนเองในขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="766ca-138">You can change the status manually at this stage.</span></span> <span data-ttu-id="766ca-139">อย่างไรก็ตาม สถานะจะถูกเปลี่ยนตามปกติเมื่อคุณยืนยันข้อตกลงสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="766ca-139">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="766ca-140">ในบานหน้าต่างการดำเนินการ คลิกที่ข้อตกลงการขาย</span><span class="sxs-lookup"><span data-stu-id="766ca-140">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="766ca-141">คลิกการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="766ca-141">Click Confirmation.</span></span>
    * <span data-ttu-id="766ca-142">ทำให้มั่นใจว่าเครื่องหมายข้อตกลงมีผลบังคับใช้ตั้งค่าเป็นใช่</span><span class="sxs-lookup"><span data-stu-id="766ca-142">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="766ca-143">เลือก ใช่ ในฟิลด์การพิมพ์รายงาน</span><span class="sxs-lookup"><span data-stu-id="766ca-143">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="766ca-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="766ca-144">Click OK.</span></span>
14. <span data-ttu-id="766ca-145">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="766ca-145">Close the page.</span></span>
    * <span data-ttu-id="766ca-146">ข้อตกลงจะมีผลบังคับใช้ทันที และคุณสามารถเริ่มต้นการเชื่อมโยงใบสั่งของลูกค้ากับข้อตกลงเพื่อออฟเซ็ตกับเป้าหมายผูกมัด</span><span class="sxs-lookup"><span data-stu-id="766ca-146">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  


