---
title: ตรวจสอบใบแจ้งหนี้และข้อมูลสำคัญในบัญชีเจ้าหนี้
description: หัวข้อนี้แสดงวิธีการตรวจสอบใบแจ้งหนี้และข้อมูลสำคัญในบัญชีเจ้าหนี้
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6ac1e9d8c5255b8347c9563ce9ea846933c0c9dd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815247"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="3e0aa-103">ตรวจสอบใบแจ้งหนี้และข้อมูลสำคัญในบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="3e0aa-103">Audit invoices and key data in accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e0aa-104">เมื่อคุณได้รับใบแจ้งหนี้จากผู้จัดจำหน่ายสำหรับสินค้าหรือบริการในใบสั่งซื้อ กระบวนการทางธุรกิจอาจต้องการได้รับสินค้าหรือบริการก่อนที่จะสามารถอนุมัติใบแจ้งหนี้สำหรับการชำระเงินได้ </span><span class="sxs-lookup"><span data-stu-id="3e0aa-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="3e0aa-105">ก่อนการเริ่มต้น ให้ตรวจสอบให้แน่ใจว่า มีเลือกคีย์การตั้งค่าคอนฟิกการจับคู่ใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="3e0aa-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="3e0aa-106">ในหน้าพารามิเตอร์ **บัญชีเจ้าหนี้** ยืนยันว่ามีการเลือกตัวเลือกการเปิดใช้งานการตรวจสอบความถูกต้องของการจับคู่ใบแจ้งหนี้ ตั้งค่าฟิลด์ **ลงรายการบัญชีใบแจ้งหนี้ที่มีส่วนต่าง** เป็น **ต้องมีการอนุมัติ** และฟิลด์ **นโยบายการจับคู่รายการ** เป็น **นโยบายการจับคู่สามทาง**</span><span class="sxs-lookup"><span data-stu-id="3e0aa-106">In the **Accounts payable parameters** page, ensure that the Enable invoice matching validation option is selected, the **Post invoice with discrepancies** field is set to **Require approval**, and the **Line matching policy** field is set to **Three-way matching**.</span></span>

<span data-ttu-id="3e0aa-107">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="3e0aa-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="3e0aa-108">บทบาทของผู้จัดการฝ่ายบัญชีเจ้าหนี้หรือผู้จัดการฝ่ายบัญชีจะต้องดำเนินการขั้นตอนเหล่านี้ </span><span class="sxs-lookup"><span data-stu-id="3e0aa-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="3e0aa-109">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="3e0aa-109">Create a purchase order</span></span>
1. <span data-ttu-id="3e0aa-110">ไปที่ **ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="3e0aa-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="3e0aa-111">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="3e0aa-111">Click **New**.</span></span>
3. <span data-ttu-id="3e0aa-112">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3e0aa-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="3e0aa-113">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="3e0aa-113">Click **OK**.</span></span>
5. <span data-ttu-id="3e0aa-114">คลิก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="3e0aa-114">Click **Add line**.</span></span>
6. <span data-ttu-id="3e0aa-115">ในฟิลด์ **หมายเลขสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3e0aa-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="3e0aa-116">บนบานหน้าต่างการดำเนินการ คลิก **ซื้อ**</span><span class="sxs-lookup"><span data-stu-id="3e0aa-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="3e0aa-117">คลิก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="3e0aa-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="3e0aa-118">ลงรายการบัญชีใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="3e0aa-118">Post a product receipt</span></span>
1. <span data-ttu-id="3e0aa-119">บนบานหน้าต่างการดำเนินการ คลิก **รับ**</span><span class="sxs-lookup"><span data-stu-id="3e0aa-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="3e0aa-120">คลิก **ใบรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="3e0aa-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="3e0aa-121">ในฟิลด์ **ใบรับสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3e0aa-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="3e0aa-122">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="3e0aa-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="3e0aa-123">บันทึกและจับคู่ใบแจ้งหนี้ของผู้จัดจำหน่ายกับใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="3e0aa-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="3e0aa-124">บนบานหน้าต่างการดำเนินการ คลิก **ใบแจ้งหนี้ > ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="3e0aa-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="3e0aa-125">ในฟิลด์ **หมายเลข** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3e0aa-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="3e0aa-126">คลิก **ค่าเริ่มต้นจาก: ปริมาณที่สั่ง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="3e0aa-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="3e0aa-127">ในฟิลด์ **ปริมาณเริ่มต้นสำหรับรายการ** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="3e0aa-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="3e0aa-128">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="3e0aa-128">Click **OK**.</span></span>
6. <span data-ttu-id="3e0aa-129">คลิก **ใช่** </span><span class="sxs-lookup"><span data-stu-id="3e0aa-129">Click **Yes**.</span></span>
7. <span data-ttu-id="3e0aa-130">คลิกที่ **จับคู่ใบรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="3e0aa-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="3e0aa-131">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="3e0aa-131">Click **OK**.</span></span>
9. <span data-ttu-id="3e0aa-132">บนบานหน้าต่างการดำเนินการ ให้คลิก **ทบทวน**</span><span class="sxs-lookup"><span data-stu-id="3e0aa-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="3e0aa-133">คลิก **รายละเอียดการจับคู่**</span><span class="sxs-lookup"><span data-stu-id="3e0aa-133">Click **Matching details**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]