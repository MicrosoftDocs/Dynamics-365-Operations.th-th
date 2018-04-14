--- 
title: "บันทึกการรับสินค้าในใบสั่งซื้อ"
description: "ขั้นตอนนี้แสดงวิธีการบันทึกการรับสินค้าโดยตรงในใบสั่งซื้อ "
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d8a47dac61705831b330f7b4939a18c865a8ace7
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="380b4-103">บันทึกการรับสินค้าในใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="380b4-103">Record the receipt of goods on the purchase order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="380b4-104">ขั้นตอนนี้แสดงวิธีการบันทึกการรับสินค้าโดยตรงในใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="380b4-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="380b4-105">และยังสามารถลงทะเบียนการรับสินค้าในคลังสินค้า และจากนั้น บันทึกบนใบสั่งซื้อในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="380b4-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="380b4-106">โดยทั่วไปจะมีการทำงานนี้โดยเจ้าหน้าที่จัดซื้อหรือผู้ประสานงานเจ้าหนี้บัญชี</span><span class="sxs-lookup"><span data-stu-id="380b4-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="380b4-107">ตัวอย่างที่แสดงในคำแนะนำนี้สามารถใช้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="380b4-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="380b4-108">ตัวอย่างประกอบด้วยขั้นตอนในการสร้างใบสั่งซื้อแบบง่ายเพื่อให้คุณสามารถใช้กระบวนงานเป็นคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="380b4-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="380b4-109">ถ้าคุณเคยใช้กระบวนงานในข้อมูลของคุณเอง ให้เริ่มต้นที่งานย่อย บันทึกการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="380b4-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="380b4-110">เตรียมใบสั่งซื้อใหม่สำหรับการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="380b4-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="380b4-111">ไปที่การจัดซื้อและการจัดหา > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="380b4-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="380b4-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="380b4-112">Click New.</span></span>
3. <span data-ttu-id="380b4-113">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อน US-101'</span><span class="sxs-lookup"><span data-stu-id="380b4-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="380b4-114">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="380b4-114">Click OK.</span></span>
5. <span data-ttu-id="380b4-115">ในฟิลด์หมายเลขสินค้า ให้ป้อน M0001</span><span class="sxs-lookup"><span data-stu-id="380b4-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="380b4-116">ในฟิลด์ปริมาณ ให้ป้อน 5</span><span class="sxs-lookup"><span data-stu-id="380b4-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="380b4-117">ในบานหน้าต่างการดำเนินการ ให้คลิก ซื้อ</span><span class="sxs-lookup"><span data-stu-id="380b4-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="380b4-118">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="380b4-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="380b4-119">บันทึกการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="380b4-119">Record receipt of goods</span></span>
1. <span data-ttu-id="380b4-120">ในบานหน้าต่างการดำเนินการ ให้คลิก รับ</span><span class="sxs-lookup"><span data-stu-id="380b4-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="380b4-121">คลิก ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="380b4-121">Click Product receipt.</span></span>
    * <span data-ttu-id="380b4-122">ฟิลด์ปริมาณช่วยให้คุณสามารถเลือกตัวเลือกต่าง ๆ สำหรับปริมาณที่คุณต้องการได้รับ </span><span class="sxs-lookup"><span data-stu-id="380b4-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="380b4-123">ตัวอย่างเช่น ถ้ามีการลงทะเบียนปริมาณไว้ก่อนหน้านี้ในคลังสินค้า คุณสามารถเลือกปริมาณที่ลงทะเบียน </span><span class="sxs-lookup"><span data-stu-id="380b4-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="380b4-124">สำหรับตัวอย่างนี้ จะใช้ค่า ปริมาณที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="380b4-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="380b4-125">ในฟิลด์ใบรับสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="380b4-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="380b4-126">ฟิลด์นี้จะใช้ในการป้อนข้อมูลอ้างอิงที่จะใช้เป็นใบสำคัญสำหรับมุดรายวันใบรับสินค้าจากใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="380b4-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="380b4-127">ขยายส่วนรายการ</span><span class="sxs-lookup"><span data-stu-id="380b4-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="380b4-128">กำหนดปริมาณเป็น '4'</span><span class="sxs-lookup"><span data-stu-id="380b4-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="380b4-129">ที่นี่คุณจะสามารถระบุปริมาณที่จะได้รับสำหรับแต่ละบรรทัดในใบสั่งด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="380b4-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="380b4-130">ยุบส่วนรายการ</span><span class="sxs-lookup"><span data-stu-id="380b4-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="380b4-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="380b4-131">Click OK.</span></span>
    * <span data-ttu-id="380b4-132">ขณะนี้สินค้ามีการบันทึกเป็นได้รับตามใบสั่งส่งคืนสินค้าที่ซื้อ และมีการสร้างมุดรายวันใบรับสินค้าเป็นเอกสารเพื่อแสดงขั้นตอนนี้ </span><span class="sxs-lookup"><span data-stu-id="380b4-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="380b4-133">คุณสามารถใช้การดำเนินการรับสินค้าเพื่อตรวจสอบสมุดรายวันที่สร้างด้วยใบสั่งซื้อ และดูรายการที่ได้รับและเวลาที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="380b4-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


