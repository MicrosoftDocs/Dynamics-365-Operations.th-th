---
title: บันทึกการรับสินค้าในใบสั่งซื้อ
description: หัวข้อนี้แสดงวิธีการบันทึกการรับสินค้าโดยตรงในใบสั่งซื้อ
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1aa4043aca2e53eae32256a98d556c25b4ec1957
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454798"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="4ecf6-103">บันทึกการรับสินค้าในใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="4ecf6-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4ecf6-104">หัวข้อนี้แสดงวิธีการบันทึกการรับสินค้าโดยตรงในใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="4ecf6-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="4ecf6-105">นอกจากนี้ ยังสามารถลงทะเบียนใบรับสินค้าในคลังสินค้า และจากนั้น บันทึกบนใบสั่งซื้อในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="4ecf6-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="4ecf6-106">โดยทั่วไปจะมีการทำงานนี้โดยเจ้าหน้าที่จัดซื้อหรือผู้ประสานงานเจ้าหนี้บัญชี</span><span class="sxs-lookup"><span data-stu-id="4ecf6-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="4ecf6-107">ตัวอย่างที่แสดงในคำแนะนำนี้สามารถใช้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="4ecf6-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="4ecf6-108">ตัวอย่างประกอบด้วยขั้นตอนในการสร้างใบสั่งซื้อแบบง่ายเพื่อให้คุณสามารถใช้กระบวนงานเป็นคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="4ecf6-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="4ecf6-109">ถ้าคุณเคยใช้กระบวนงานในข้อมูลของคุณเอง คุณจะเริ่มต้นที่งานย่อย **บันทึกการรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="4ecf6-110">เตรียมใบสั่งซื้อใหม่สำหรับการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ecf6-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="4ecf6-111">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดซื้อและการจัดหา > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="4ecf6-112">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-112">Select **New**.</span></span>
3. <span data-ttu-id="4ecf6-113">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ป้อน `US-101`</span><span class="sxs-lookup"><span data-stu-id="4ecf6-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="4ecf6-114">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-114">Select **OK**.</span></span>
5. <span data-ttu-id="4ecf6-115">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อน `M0001`</span><span class="sxs-lookup"><span data-stu-id="4ecf6-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="4ecf6-116">ในฟิลด์ **ปริมาณ** ให้ป้อน `5`</span><span class="sxs-lookup"><span data-stu-id="4ecf6-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="4ecf6-117">บนบานหน้าต่างการดำเนินการ เลือก **ซื้อ**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="4ecf6-118">เลือก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="4ecf6-119">บันทึกการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ecf6-119">Record receipt of goods</span></span>
1. <span data-ttu-id="4ecf6-120">ในบานหน้าต่างการดำเนินการ เลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="4ecf6-121">เลือก **ใบรับผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-121">Select **Product receipt**.</span></span> <span data-ttu-id="4ecf6-122">ฟิลด์ **ปริมาณ** ช่วยให้คุณสามารถเลือกตัวเลือกต่างๆ สำหรับปริมาณที่คุณต้องการได้รับ</span><span class="sxs-lookup"><span data-stu-id="4ecf6-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="4ecf6-123">ตัวอย่างเช่น ถ้ามีการลงทะเบียนปริมาณไว้ก่อนหน้านี้ในคลังสินค้า คุณสามารถเลือก **ปริมาณที่ลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="4ecf6-124">สำหรับตัวอย่างนี้ จะใช้ค่า **ปริมาณที่สั่ง**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="4ecf6-125">ขยายส่วน **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="4ecf6-126">ในฟิลด์ **ใบรับสินค้า** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4ecf6-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="4ecf6-127">ฟิลด์นี้จะใช้ในการป้อนข้อมูลอ้างอิงที่จะใช้เป็นใบสำคัญสำหรับมุดรายวันใบรับสินค้าจากใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="4ecf6-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="4ecf6-128">ขยายส่วน **รายการ**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="4ecf6-129">กำหนด **ปริมาณเป็น** '4'</span><span class="sxs-lookup"><span data-stu-id="4ecf6-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="4ecf6-130">ที่นี่คุณจะสามารถระบุปริมาณที่จะได้รับสำหรับแต่ละบรรทัดในใบสั่งด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="4ecf6-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="4ecf6-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4ecf6-131">Select **OK**.</span></span> <span data-ttu-id="4ecf6-132">ขณะนี้สินค้ามีการบันทึกเป็นได้รับตามใบสั่งส่งคืนสินค้าที่ซื้อ และมีการสร้างมุดรายวันใบรับสินค้าเป็นเอกสารเพื่อแสดงขั้นตอนนี้ </span><span class="sxs-lookup"><span data-stu-id="4ecf6-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="4ecf6-133">คุณสามารถใช้การดำเนินการรับสินค้าเพื่อตรวจสอบสมุดรายวันที่สร้างด้วยใบสั่งซื้อ และดูรายการที่ได้รับและเวลาที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="4ecf6-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

