---
title: "ตัวเลือกธุรกรรมสินทรัพย์ถาวร"
description: "บทความนี้อธิบายวิธีการต่างๆ ที่พร้อมใช้งานเพื่อสร้างธุรกรรมสินทรัพย์ถาวร"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 18352ad921c2e2d110a7535f979272685105662f
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="04b74-103">ตัวเลือกธุรกรรมสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-103">Fixed asset transaction options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="04b74-104">บทความนี้อธิบายวิธีการต่างๆ ที่พร้อมใช้งานเพื่อสร้างธุรกรรมสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="04b74-105">คุณสามารถตั้งค่าสินทรัพย์ถาวรเพื่อรวมกับบัญชีเจ้าหนี้ ลูกหนี้ จัดซื้อ และการจัดหา และบัญชีแยกประเภททั่วไป </span><span class="sxs-lookup"><span data-stu-id="04b74-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="04b74-106">นอกจากนี้ คุณยังสามารถโอนย้ายสินค้าในการบริหารสินค้าคงคลังเป็นสินทรัพย์ถาวรถ้าคุณต้องการใช้สินค้าเป็นการภายใน</span><span class="sxs-lookup"><span data-stu-id="04b74-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="04b74-107">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="04b74-107">Accounts payable</span></span>
<span data-ttu-id="04b74-108">คุณสามารถป้อนธุรกรรมสินทรัพย์ถาวรในหน้าใบสำคัญสมุดรายวันได้</span><span class="sxs-lookup"><span data-stu-id="04b74-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="04b74-109">สามารถเปิดหน้านี้ได้จากหน้าสมุดรายวันใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="04b74-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="04b74-110">คุณยังสามารถเปิดหน้าใบสำคัญสมุดรายวันจากหน้าสมุดรายวันการอนุมัติใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="04b74-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="04b74-111">ในฟิลด์ชนิดบัญชี เลือกสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="04b74-112">จากนั้น ในฟิลด์หมายเลขบัญชีตรงข้าม เลือกหมายเลขสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="04b74-113">บนแท็บสินทรัพย์ถาวร ป้อนค่าฟิลด์ในชนิดของธุรกรรมและฟิลด์สมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="04b74-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="04b74-114">บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="04b74-114">Accounts receivable</span></span>
<span data-ttu-id="04b74-115">คุณสามารถป้อนธุรกรรมสินทรัพย์ถาวรในหน้าใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="04b74-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="04b74-116">ในหน้าใบแจ้งหนี้ข้อความอิสระ ในตารางบรรทัดใบแจ้งหนี้ เลือกสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="04b74-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="04b74-117">คลิกแท็บด่วนรายละเอียดรายการ</span><span class="sxs-lookup"><span data-stu-id="04b74-117">Click the Line details FastTab.</span></span> <span data-ttu-id="04b74-118">ป้อนหมายเลขสินทรัพย์ถาวรและสมุดบัญชีสำหรับธุรกรรมการตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="04b74-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="04b74-119">สำหรับใบแจ้งหนี้ข้อความอิสระ ชนิดธุรกรรมสินทรัพย์ถาวรจะเป็นการตัดจำหน่ายเสมอ - การขาย</span><span class="sxs-lookup"><span data-stu-id="04b74-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="04b74-120">การจัดซื้อและการจัดหา</span><span class="sxs-lookup"><span data-stu-id="04b74-120">Procurement and sourcing</span></span>
<span data-ttu-id="04b74-121">คุณสามารถป้อนธุรกรรมสินทรัพย์ถาวรในหน้าใบสั่งซื้อได้</span><span class="sxs-lookup"><span data-stu-id="04b74-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="04b74-122">ป้อนข้อมูลที่จำเป็นเพื่อสร้างใบสั่งซื้อ แล้วคลิกตกลง</span><span class="sxs-lookup"><span data-stu-id="04b74-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="04b74-123">ในหน้าใบสั่งซื้อ คลิกแท็บด่วนรายละเอียดรายการ</span><span class="sxs-lookup"><span data-stu-id="04b74-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="04b74-124">จากนั้น บนแท็บสินทรัพย์ถาวร ป้อนข้อมูลเกี่ยวกับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="04b74-125">เมื่อต้องการลงรายบัญชีธุรกรรมการซื้อสินทรัพย์สำหรับสินทรัพย์ถาวรที่มีอยู่ ระบุหมายเลขสินทรัพย์ถาวร สมุดบัญชี และชนิดของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="04b74-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="04b74-126">ไม่สามารถลงรายการสินทรัพย์ถาวรถ้าข้อมูลใดข้อมูลหนึ่งขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="04b74-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="04b74-127">เมื่อต้องการลงรายบัญชีธุรกรรมการซื้อสินทรัพย์สำหรับสินทรัพย์ถาวรใหม่ เลือกตัวเลือกสินทรัพย์ถาวรใหม่? และจากนั้น เลือกกลุ่มสินทรัพย์ถาวรเพื่อกำหนดสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="04b74-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="04b74-128">อย่างไรก็ตาม ฟิลด์สินทรัพย์ถาวรจะพร้อมใช้งานสำหรับรายการนั้น ถ้าสินค้าอยู่ในกลุ่มแบบจำลองสินค้าคงคลังที่ใช้แบบจำลองสินค้าคงคลังต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="04b74-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="04b74-129">นอกจากนี้ ตัวเลือกที่กำหนดไว้ในหน้าพารามิเตอร์สินทรัพย์ถาวรกำหนดว่า คุณสามารถลงรายบัญชีธุรกรรมการซื้อสินทรัพย์จากโมดูลการจัดซื้อได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="04b74-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="04b74-130">เมื่อใบสั่งซื้อหรือสมุดรายวันสินค้าคงคลังที่เก็บเป็นสินทรัพย์ถาวรถูกใช้เพื่อซื้อสินทรัพย์ถาวร มูลค่าสินค้าคงคลังจะได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="04b74-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="04b74-131">บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="04b74-131">General ledger</span></span>
<span data-ttu-id="04b74-132">คุณสามารถลงรายการบัญชีประเภทของธุรกรรมสินทรัพย์ถาวรใดๆ ในหน้าสมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="04b74-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="04b74-133">คุณยังสามารถใช้สมุดรายวันในสินทรัพย์ถาวรเพื่อลงรายบัญชีธุรกรรมสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="04b74-134">ตัวเลือกสำหรับการป้อนชนิดของธุรกรรมสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="04b74-135">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="04b74-135">Transaction type</span></span>                    | <span data-ttu-id="04b74-136">โมดูล</span><span class="sxs-lookup"><span data-stu-id="04b74-136">Module</span></span>                   | <span data-ttu-id="04b74-137">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="04b74-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="04b74-138">การซื้อสินทรัพย์ การปรับปรุงการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="04b74-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="04b74-139">สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-139">Fixed assets</span></span>             | <span data-ttu-id="04b74-140">สินทรัพย์ถาวร จากสินค้าคงคลังไปเป็นสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="04b74-141">บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="04b74-141">General ledger</span></span>           | <span data-ttu-id="04b74-142">สมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="04b74-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="04b74-143">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="04b74-143">Accounts payable</span></span>         | <span data-ttu-id="04b74-144">สมุดรายวันใบแจ้งหนี้ สมุดรายวันการอนุมัติใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="04b74-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="04b74-145">การจัดซื้อและการจัดหา</span><span class="sxs-lookup"><span data-stu-id="04b74-145">Procurement and sourcing</span></span> | <span data-ttu-id="04b74-146">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="04b74-146">Purchase order</span></span>                            |
| <span data-ttu-id="04b74-147">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="04b74-147">Depreciation</span></span>                        | <span data-ttu-id="04b74-148">สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-148">Fixed assets</span></span>             | <span data-ttu-id="04b74-149">สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="04b74-150">บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="04b74-150">General ledger</span></span>           | <span data-ttu-id="04b74-151">สมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="04b74-151">General journal</span></span>                           |
| <span data-ttu-id="04b74-152">การตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="04b74-152">Disposal</span></span>                            | <span data-ttu-id="04b74-153">สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-153">Fixed assets</span></span>             | <span data-ttu-id="04b74-154">สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="04b74-154">Fixed assets</span></span>                              |
| <span data-ttu-id="04b74-155">** **</span><span class="sxs-lookup"><span data-stu-id="04b74-155">** **</span></span>                               | <span data-ttu-id="04b74-156">บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="04b74-156">General ledger</span></span>           | <span data-ttu-id="04b74-157">สมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="04b74-157">General journal</span></span>                           |
| <span data-ttu-id="04b74-158">** **</span><span class="sxs-lookup"><span data-stu-id="04b74-158">** **</span></span>                               | <span data-ttu-id="04b74-159">บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="04b74-159">Accounts receivable</span></span>      | <span data-ttu-id="04b74-160">ใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="04b74-160">Free text invoice</span></span>                         |



<span data-ttu-id="04b74-161">สำหรับข้อมูลเพิ่มเติม ดู [การรวมสินทรัพย์ถาวร](fixed-asset-integration.md)</span><span class="sxs-lookup"><span data-stu-id="04b74-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




