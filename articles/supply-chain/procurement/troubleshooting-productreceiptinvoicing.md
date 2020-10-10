---
title: วิธีแก้ปัญหาใบรับสินค้าและการออกใบแจ้งหนี้
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบในระหว่างที่คุณทำงานกับใบรับสินค้าและการออกใบแจ้งหนี้
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d86fa3df1de13cc0e0fb94449207a326069da25b
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834436"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="bf788-103">วิธีแก้ปัญหาใบรับสินค้าและการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="bf788-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="bf788-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบในระหว่างที่คุณทำงานกับใบรับสินค้าและการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="bf788-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="bf788-105">ฉันไม่สามารถลงรายการบัญชีใบแจ้งหนี้มากกว่าหนึ่งรายการสำหรับบรรทัดใบสั่งซื้อที่มีสินค้าตามประเภท</span><span class="sxs-lookup"><span data-stu-id="bf788-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="bf788-106">ปริมาณเป็นฟิลด์บังคับถ้าคุณต้องการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="bf788-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="bf788-107">ถ้าปริมาณทั้งหมดของบรรทัดมีการออกใบแจ้งหนี้สำหรับเฉพาะยอดเงินเพียงบางส่วน คุณจะไม่สามารถออกใบแจ้งหนี้ยอดเงินคงเหลือในใบแจ้งหนี้อื่นได้</span><span class="sxs-lookup"><span data-stu-id="bf788-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="bf788-108">ฉันได้รับข้อผิดพลาด "ไม่มีการตั้งค่าการอ้างอิงอ็อบเจกต์" ในระหว่างการยืนยันใบสั่งซื้อหรือมีข้อยกเว้น "เกิดข้อยกเว้นตามเป้าหมายของการเรียก" เกิดขึ้นระหว่างการลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="bf788-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="bf788-109">ปัญหานี้อาจเกิดขึ้นเนื่องจากความไม่สอดคล้องกันในการกระจายใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="bf788-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="bf788-110">เมื่อต้องการยกเลิกการบล็อกปัญหานี้และรีเซ็ตใบสั่งซื้อเป็นสถานะ *แบบร่าง* ให้ไปที่การ **จัดซื้อและการจัดหา \> งานประจำงวด \> ล้างข้อมูล \> รีเซ็ตการกระจายใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="bf788-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="bf788-111">สำหรับข้อมูลเพิ่มเติมให้ดูที่การลงรายการบัญชีบล็อกต่อไปนี้: [แก้ไขข้อผิดพลาดในการกระจาย PO ใน Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)</span><span class="sxs-lookup"><span data-stu-id="bf788-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="bf788-112">ฉันไม่สามารถรวมใบรับสินค้าหลายใบเข้ากับใบสั่งซื้อใบเดียวได้</span><span class="sxs-lookup"><span data-stu-id="bf788-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="bf788-113">คุณไม่สามารถรวมใบรับสินค้าหลายใบเข้ากับใบสั่งซื้อใบเดียวได้ถ้าบรรทัดใบรับสินค้าที่แตกต่างกันมีวันที่ลงบัญชีที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="bf788-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="bf788-114">ใน Microsoft เวอร์ชันก่อนหน้านี้การรวมบัญชี Microsoft Dynamics 365 Supply Chain Management ได้รับอนุญาตในสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="bf788-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="bf788-115">อย่างไรก็ตามการปฏิบัติมีแนวโน้มที่จะเกิดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="bf788-115">However, the practice is prone to error.</span></span> <span data-ttu-id="bf788-116">วันที่ลงบัญชีของบรรทัดใบสั่งซื้อที่สร้างขึ้นไม่ควรแตกต่างจากวันที่ลงบัญชีในรายการใบรับสินค้าที่มีการสร้างบรรทัดใบสั่งซื้อเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="bf788-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="bf788-117">(วันที่ลงบัญชีของบรรทัดใบสั่งซื้อตรงกับวันที่ลงบัญชีบนส่วนหน้าของใบสั่งซื้อ) ดังนั้นการรวมใบรับสินค้าหลายใบเป็นใบสั่งซื้อแต่ละใบจะไม่สามารถใช้ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="bf788-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="bf788-118">มีการใช้วันที่ลงบัญชี ตัวอย่างเช่น สำหรับการจองงบประมาณและภาระผูกพัน</span><span class="sxs-lookup"><span data-stu-id="bf788-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="bf788-119">ดังนั้นจึงควรเก็บรักษาไว้ในระหว่างการเปลี่ยนจากใบรับสินค้าไปยังใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="bf788-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="bf788-120">เมื่อยกเลิกใบรับสินค้าแล้ว คุณสามารถลงรายการบัญชีธุรกรรมไปยังบัญชีแยกประเภทที่ระงับได้</span><span class="sxs-lookup"><span data-stu-id="bf788-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="bf788-121">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="bf788-121">Issue description</span></span>

<span data-ttu-id="bf788-122">ถ้ามีการยกเลิกใบรับสินค้า ระบบจะอนุญาตให้ลงรายการบัญชีธุรกรรมไปยังบัญชีแยกประเภทที่ระงับได้ แม้ว่าบัญชีหลักจะถูกระงับ</span><span class="sxs-lookup"><span data-stu-id="bf788-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="bf788-123">สร้างปัญหาอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="bf788-123">Reproduce the issue</span></span>

<span data-ttu-id="bf788-124">กระบวนการต่อไปนี้แสดงวิธีหนึ่งที่จะสร้างปัญหาอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="bf788-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="bf788-125">บนหน้า **พารามิเตอร์บัญชีเจ้าหนี้** บนแท็บ **ทั่วไป** โปรดตรวจสอบให้แน่ใจว่าได้ตั้งค่าตัวเลือก **ลงรายการบัญชีใบรับสินค้าในบัญชีแยกประเภท** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="bf788-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="bf788-126">สร้างใบสั่งซื้อและเพิ่มบรรทัดใบสั่งที่มีปริมาณ *1,000* สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bf788-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="bf788-127">ยืนยันใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="bf788-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="bf788-128">ลงรายการบัญชีใบรับสินค้าและตรวจสอบใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="bf788-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="bf788-129">ระงับบัญชีหลักที่เกี่ยวข้อง *200140* และ *140200*</span><span class="sxs-lookup"><span data-stu-id="bf788-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="bf788-130">ยกเลิกใบรับสินค้าที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="bf788-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="bf788-131">โปรดสังเกตว่าธุรกรรมสามารถลงรายการบัญชีไปยังบัญชีแยกประเภทที่ระงับได้</span><span class="sxs-lookup"><span data-stu-id="bf788-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bf788-132">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="bf788-132">Issue resolution</span></span>

<span data-ttu-id="bf788-133">คุณสามารถลงรายการบัญชีธุรกรรมไปยังบัญชีแยกประเภทที่ถูกระงับเมื่อยกเลิกใบรับสินค้า เนื่องจากลักษณะการทำงานนี้ช่วยให้สามารถลงรายการบัญชีได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="bf788-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="bf788-134">มีการใช้หมายเลขใบสำคัญของใบรับสินค้าถึงแม้ว่าจะไม่มีการสร้างใบสำคัญทางการเงินในระหว่างการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="bf788-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="bf788-135">ถ้ามีการตั้งค่าตัวเลือก **บันทึกหนี้สินค้างจ่ายของใบรับสินค้า** เป็น *ไม่มี* สำหรับกลุ่มแบบจำลองสินค้า จะไม่มีการลงรายการบัญชีในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="bf788-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="bf788-136">อย่างไรก็ตามจะมีการบันทึกเหตุการณ์ทางกายภาพสำหรับวัตถุประสงค์ของการบัญชีในบัญชีแยกประเภทย่อย และเหตุการณ์นั้นต้องใช้หมายเลขใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="bf788-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="bf788-137">หมายเลขใบสำคัญนี้คือหมายเลขใบสำคัญที่มีการอ้างอิงในรายการธุรกรรมของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="bf788-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="bf788-138">เราขอแนะนำให้คุณตั้งค่าตัวเลือก **บันทึกหนี้สินค้างจ่ายของใบรับสินค้า** เป็น *ใช่* ดังที่อธิบายไว้ในการลงรายการบัญชีบล็อกต่อไปนี้: [ลงรายการบัญชีค่าธรรมเนียมเบ็ดเตล็ดในเวลาของใบรับสินค้า](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)</span><span class="sxs-lookup"><span data-stu-id="bf788-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="bf788-139">ไม่ได้เปิดใช้งานการลงรายการบัญชีไปยังบัญชีแยกประเภทในการตั้งค่าบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="bf788-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="bf788-140">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="bf788-140">Issue description</span></span>

<span data-ttu-id="bf788-141">ปัญหานี้เกิดขึ้นเมื่อใบสั่งซื้อมีการออกใบแจ้งหนี้แล้วถ้ามีการตั้งค่าตัวเลือก **ลงรายการบัญชีในบัญชีแยกประเภท** เป็น *ใช่* บนแท็บ **ใบแจ้งหนี้** ของหน้า **พารามิเตอร์บัญชีเจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="bf788-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="bf788-142">สร้างปัญหาอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="bf788-142">Reproduce the issue</span></span>

<span data-ttu-id="bf788-143">กระบวนการต่อไปนี้แสดงวิธีหนึ่งที่จะสร้างปัญหาอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="bf788-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="bf788-144">ไปที่ **บัญชีเจ้าหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีเจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="bf788-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="bf788-145">บนแท็บ **ใบแจ้งหนี้** ให้ตั้งค่าตัวเลือก **ลงรายการบัญชีค่าธรรมเนียมบัญชีในบัญชีแยกประเภท** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="bf788-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="bf788-146">ไปที่ **การจัดการสินค้างคงคลัง \> ตั้งค่า \> การลงรายการบัญชี \> การลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="bf788-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="bf788-147">บนแท็บ **ใบสั่งซื้อ** ตรวจสอบให้แน่ใจว่าคุณได้ลบบรรทัดทั้งหมดในรายจ่ายการซื้อสำหรับผลิตภัณฑ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="bf788-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="bf788-148">ไปที่ **บัญชีเจ้าหนี้ \> ใบสั่งซื้อ \> ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="bf788-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="bf788-149">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="bf788-149">Create a purchase order.</span></span> <span data-ttu-id="bf788-150">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้เลือก *วัสดุสำนักงาน 1001 Acme*</span><span class="sxs-lookup"><span data-stu-id="bf788-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="bf788-151">เพิ่มบรรทัดใบสั่งซื้อที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bf788-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="bf788-152">**หมายเลขสินค้า:** *เครื่องฉายเลเซอร์ D0011*</span><span class="sxs-lookup"><span data-stu-id="bf788-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="bf788-153">**ไซต์:** *1*</span><span class="sxs-lookup"><span data-stu-id="bf788-153">**Site:** *1*</span></span>
    - <span data-ttu-id="bf788-154">**คลังสินค้า:** *11*</span><span class="sxs-lookup"><span data-stu-id="bf788-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="bf788-155">**ปริมาณ:** *4*</span><span class="sxs-lookup"><span data-stu-id="bf788-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="bf788-156">ในบานหน้าต่างการดำเนินการ บนแท็บ **การซื้อ** ในกลุ่ม **การดำเนินการ** ให้เลือก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="bf788-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="bf788-157">บนบานหน้าต่างการดำเนินการ บนแท็บ **การรับสินค้า** ในกลุ่ม **ทั่วไป** ให้เลือก **ใบรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="bf788-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="bf788-158">ในกล่องโต้ตอบ **การลงรายการบัญชีใบรับสินค้า** ในฟิลด์ **ใบรับสินค้า** ให้ป้อนหมายเลขตามต้องการ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bf788-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="bf788-159">ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบแจ้งหนี้** ในกลุ่ม **สร้าง** ให้เลือก **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="bf788-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="bf788-160">ในฟิลด์ **หมายเลข** ให้ป้อนหมายเลขอำเภอใจเป็นหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="bf788-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="bf788-161">อัปเดตสถานะการจับคู่และการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="bf788-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="bf788-162">โปรดสังเกตว่าขณะนี้คุณได้รับข้อผิดพลาดต่อไปนี้เมื่อคุณสร้างใบแจ้งหนี้จากใบสั่งซื้อ: "หมายเลขบัญชีสำหรับชนิดธุรกรรมรายจ่ายการซื้อสำหรับผลิตภัณฑ์ไม่มีอยู่"</span><span class="sxs-lookup"><span data-stu-id="bf788-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bf788-163">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="bf788-163">Issue resolution</span></span>

<span data-ttu-id="bf788-164">ทั้งนี้ขึ้นอยู่กับการตั้งค่าพารามิเตอร์สำหรับใบแจ้งหนี้และกลุ่มใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="bf788-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="bf788-165">สำหรับข้อมูลเพิ่มเติม ให้ดูที่การลงรายการบัญชีบล็อกต่อไปนี้: [การลงบัญชีสำหรับค่าธรรมเนียมการซื้อและการเปลี่ยนแปลงสินค้าคงคลัง](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/)</span><span class="sxs-lookup"><span data-stu-id="bf788-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
