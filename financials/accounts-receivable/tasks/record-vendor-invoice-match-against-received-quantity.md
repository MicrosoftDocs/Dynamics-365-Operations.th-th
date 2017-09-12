--- 
title: "บันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายและจับคู่กับปริมาณที่ได้รับ"
description: "เมื่อคุณได้รับใบแจ้งหนี้จากผู้จัดจำหน่ายสำหรับสินค้าหรือบริการในใบสั่งซื้อ กระบวนการทางธุรกิจอาจต้องการได้รับสินค้าหรือบริการก่อนที่จะสามารถอนุมัติใบแจ้งหนี้สำหรับการชำระเงินได้ "
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2247edfd803ce238b3b7ca57d9d47dda9c3b0cae
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="0148b-103">บันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายและจับคู่กับปริมาณที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="0148b-103">Record vendor invoice and match against received quantity</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0148b-104">เมื่อคุณได้รับใบแจ้งหนี้จากผู้จัดจำหน่ายสำหรับสินค้าหรือบริการในใบสั่งซื้อ กระบวนการทางธุรกิจอาจต้องการได้รับสินค้าหรือบริการก่อนที่จะสามารถอนุมัติใบแจ้งหนี้สำหรับการชำระเงินได้ </span><span class="sxs-lookup"><span data-stu-id="0148b-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="0148b-105">ก่อนการเริ่มต้น ให้ตรวจสอบให้แน่ใจว่า มีเลือกคีย์การตั้งค่าคอนฟิกการจับคู่ใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="0148b-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="0148b-106">ในหน้าพารามิเตอร์บัญชีเจ้าหนี้ จะยืนยันว่ามีการเลือกตัวเลือกการเปิดใช้งานการตรวจสอบความถูกต้องของการจับคู่ใบแจ้งหนี้ มีการตั้งค่าการลงรายการบัญชีใบแจ้งหนี้ในฟิลด์ที่แตกต่างกัน และฟิลด์นโยบายการจับคู่รายการถูกตั้งค่าการจับคู่เป็น 3 วิธี </span><span class="sxs-lookup"><span data-stu-id="0148b-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="0148b-107">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="0148b-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="0148b-108">บทบาทของผู้จัดการฝ่ายบัญชีเจ้าหนี้หรือผู้จัดการฝ่ายบัญชีจะต้องดำเนินการขั้นตอนเหล่านี้ </span><span class="sxs-lookup"><span data-stu-id="0148b-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="0148b-109">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="0148b-109">Create a purchase order</span></span>
1. <span data-ttu-id="0148b-110">ไปที่ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0148b-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="0148b-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0148b-111">Click New.</span></span>
3. <span data-ttu-id="0148b-112">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0148b-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0148b-113">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0148b-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="0148b-114">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0148b-114">Click OK.</span></span>
6. <span data-ttu-id="0148b-115">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="0148b-115">Click Add line.</span></span>
7. <span data-ttu-id="0148b-116">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0148b-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="0148b-117">ในบานหน้าต่างการดำเนินการ ให้คลิก ซื้อ</span><span class="sxs-lookup"><span data-stu-id="0148b-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="0148b-118">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="0148b-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="0148b-119">ลงรายการบัญชีใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="0148b-119">Post a product receipt</span></span>
1. <span data-ttu-id="0148b-120">ในบานหน้าต่างการดำเนินการ ให้คลิก รับ</span><span class="sxs-lookup"><span data-stu-id="0148b-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="0148b-121">คลิก ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="0148b-121">Click Product receipt.</span></span>
3. <span data-ttu-id="0148b-122">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0148b-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0148b-123">ในฟิลด์ใบรับสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0148b-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="0148b-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0148b-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="0148b-125">บันทึกและจับคู่ใบแจ้งหนี้ของผู้จัดจำหน่ายกับใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="0148b-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="0148b-126">ในบานหน้าต่างการดำเนินการ คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0148b-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="0148b-127">คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0148b-127">Click Invoice.</span></span>
3. <span data-ttu-id="0148b-128">ในฟิลด์หมายเลข ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0148b-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="0148b-129">คลิกที่ค่าเริ่มต้น จากปริมาณที่สั่งไปยังเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="0148b-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="0148b-130">ในฟิลด์ปริมาณเริ่มต้นสำหรับรายการ ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="0148b-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="0148b-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0148b-131">Click OK.</span></span>
7. <span data-ttu-id="0148b-132">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="0148b-132">Click Yes.</span></span>
8. <span data-ttu-id="0148b-133">คลิกที่จับคู่ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="0148b-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="0148b-134">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0148b-134">Click OK.</span></span>
10. <span data-ttu-id="0148b-135">ในบานหน้าต่างการดำเนินการ ให้คลิก ทบทวน</span><span class="sxs-lookup"><span data-stu-id="0148b-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="0148b-136">คลิก รายละเอียดการจับคู่</span><span class="sxs-lookup"><span data-stu-id="0148b-136">Click Matching details.</span></span>


