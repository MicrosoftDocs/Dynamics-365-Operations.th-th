---
title: ตรวจสอบใบแจ้งหนี้และข้อมูลสำคัญในระบบ AP
description: 'เมื่อคุณได้รับใบแจ้งหนี้จากผู้จัดจำหน่ายสำหรับสินค้าหรือบริการในใบสั่งซื้อ กระบวนการทางธุรกิจอาจต้องการได้รับสินค้าหรือบริการก่อนที่จะสามารถอนุมัติใบแจ้งหนี้สำหรับการชำระเงินได้ '
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e1af0dac107be6009eb3ca576c49ac5abbd9848
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139955"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="b2b50-103">ตรวจสอบใบแจ้งหนี้และข้อมูลสำคัญในระบบ AP</span><span class="sxs-lookup"><span data-stu-id="b2b50-103">Audit invoices and key data in AP system</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2b50-104">เมื่อคุณได้รับใบแจ้งหนี้จากผู้จัดจำหน่ายสำหรับสินค้าหรือบริการในใบสั่งซื้อ กระบวนการทางธุรกิจอาจต้องการได้รับสินค้าหรือบริการก่อนที่จะสามารถอนุมัติใบแจ้งหนี้สำหรับการชำระเงินได้ </span><span class="sxs-lookup"><span data-stu-id="b2b50-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="b2b50-105">ก่อนการเริ่มต้น ให้ตรวจสอบให้แน่ใจว่า มีเลือกคีย์การตั้งค่าคอนฟิกการจับคู่ใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="b2b50-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="b2b50-106">ในหน้าพารามิเตอร์บัญชีเจ้าหนี้ จะยืนยันว่ามีการเลือกตัวเลือกการเปิดใช้งานการตรวจสอบความถูกต้องของการจับคู่ใบแจ้งหนี้ มีการตั้งค่าการลงรายการบัญชีใบแจ้งหนี้ในฟิลด์ที่แตกต่างกัน และฟิลด์นโยบายการจับคู่รายการถูกตั้งค่าการจับคู่เป็น 3 วิธี </span><span class="sxs-lookup"><span data-stu-id="b2b50-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="b2b50-107">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="b2b50-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="b2b50-108">บทบาทของผู้จัดการฝ่ายบัญชีเจ้าหนี้หรือผู้จัดการฝ่ายบัญชีจะต้องดำเนินการขั้นตอนเหล่านี้ </span><span class="sxs-lookup"><span data-stu-id="b2b50-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="b2b50-109">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b2b50-109">Create a purchase order</span></span>
1. <span data-ttu-id="b2b50-110">ไปที่ **ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="b2b50-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="b2b50-111">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b2b50-111">Click **New**.</span></span>
3. <span data-ttu-id="b2b50-112">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b2b50-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="b2b50-113">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="b2b50-113">Click **OK**.</span></span>
5. <span data-ttu-id="b2b50-114">คลิก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="b2b50-114">Click **Add line**.</span></span>
6. <span data-ttu-id="b2b50-115">ในฟิลด์ **หมายเลขสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b2b50-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="b2b50-116">บนบานหน้าต่างการดำเนินการ คลิก **ซื้อ**</span><span class="sxs-lookup"><span data-stu-id="b2b50-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="b2b50-117">คลิก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="b2b50-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="b2b50-118">ลงรายการบัญชีใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b2b50-118">Post a product receipt</span></span>
1. <span data-ttu-id="b2b50-119">บนบานหน้าต่างการดำเนินการ คลิก **รับ**</span><span class="sxs-lookup"><span data-stu-id="b2b50-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="b2b50-120">คลิก **ใบรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="b2b50-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="b2b50-121">ในฟิลด์ **ใบรับสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b2b50-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="b2b50-122">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="b2b50-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="b2b50-123">บันทึกและจับคู่ใบแจ้งหนี้ของผู้จัดจำหน่ายกับใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b2b50-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="b2b50-124">บนบานหน้าต่างการดำเนินการ คลิก **ใบแจ้งหนี้ > ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="b2b50-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="b2b50-125">ในฟิลด์ **หมายเลข** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b2b50-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="b2b50-126">คลิก **ค่าเริ่มต้นจาก: ปริมาณที่สั่ง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b2b50-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="b2b50-127">ในฟิลด์ **ปริมาณเริ่มต้นสำหรับรายการ** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="b2b50-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="b2b50-128">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="b2b50-128">Click **OK**.</span></span>
6. <span data-ttu-id="b2b50-129">คลิก **ใช่** </span><span class="sxs-lookup"><span data-stu-id="b2b50-129">Click **Yes**.</span></span>
7. <span data-ttu-id="b2b50-130">คลิกที่ **จับคู่ใบรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="b2b50-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="b2b50-131">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="b2b50-131">Click **OK**.</span></span>
9. <span data-ttu-id="b2b50-132">บนบานหน้าต่างการดำเนินการ ให้คลิก **ทบทวน**</span><span class="sxs-lookup"><span data-stu-id="b2b50-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="b2b50-133">คลิก **รายละเอียดการจับคู่**</span><span class="sxs-lookup"><span data-stu-id="b2b50-133">Click **Matching details**.</span></span>

