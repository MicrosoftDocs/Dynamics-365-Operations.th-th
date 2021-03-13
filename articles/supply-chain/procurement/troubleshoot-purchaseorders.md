---
title: แก้ไขปัญหาใบสั่งซื้อ
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบสั่งซื้อ
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 7b65c23fc7ac04fc30c0001bee9541a475026018
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007502"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="2b72d-103">แก้ไขปัญหาใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b72d-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="2b72d-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b72d-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="2b72d-105">การดำเนินการสามารถดำเนินการให้เสร็จสมบูรณ์ได้หลังจากกระจายหมายเลขรายการเต็มจำนวนแล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2b72d-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="2b72d-106">ปัญหานี้อาจเกิดขึ้นเนื่องจากความไม่สอดคล้องกันในการกระจายใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b72d-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="2b72d-107">เมื่อต้องการยกเลิกการบล็อกปัญหานี้และรีเซ็ตใบสั่งซื้อเป็นสถานะ *แบบร่าง* ให้ไปที่การ **จัดซื้อและการจัดหา \> งานประจำงวด \> ล้างข้อมูล \> รีเซ็ตการกระจายใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="2b72d-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="2b72d-108">สำหรับข้อมูลเพิ่มเติมให้ดูที่การลงรายการบัญชีบล็อกต่อไปนี้: [แก้ไขข้อผิดพลาดในการกระจาย PO ใน Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)</span><span class="sxs-lookup"><span data-stu-id="2b72d-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="2b72d-109">เมื่อมีการนำเข้าใบสั่งซื้อโดยใช้การจัดการข้อมูล หมายเลขบรรทัดใบสั่งซื้อไม่ได้เป็นไปตามการเพิ่มที่กำหนดไว้ในพารามิเตอร์ระบบ</span><span class="sxs-lookup"><span data-stu-id="2b72d-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2b72d-110">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="2b72d-110">Issue description</span></span>

<span data-ttu-id="2b72d-111">ตามค่าเริ่มต้นจะมีการสร้างหมายเลขรายการโดยอัตโนมัติสำหรับบรรทัดใบสั่งซื้อที่นำเข้าโดยหน่วยงานข้อมูลของ *บรรทัดใบสั่งซื้อ V2* ไม่ใช้การเพิ่มขึ้นของหมายเลขบรรทัดของระบบที่ระบุไว้ในพารามิเตอร์ระบบ</span><span class="sxs-lookup"><span data-stu-id="2b72d-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="2b72d-112">ถ้าคุณสร้างใบสั่งซื้อด้วยตนเองและเพิ่มบรรทัดผ่านอินเทอร์เฟสผู้ใช้ (UI) หมายเลขบรรทัดจะเพิ่มอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2b72d-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="2b72d-113">อย่างไรก็ตามถ้าคุณใช้กรอบงานการจัดการข้อมูล (DMF) จะไม่มีการเพิ่มขึ้นอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2b72d-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="2b72d-114">ปัญหานี้เกิดขึ้นเนื่องจากเมื่อคุณนำเข้าบรรทัดผ่าน DMF ถ้าหมายเลขบรรทัดยังไม่ได้รับการกำหนดในเอนทิตีที่นำเข้า ระบบจะใช้วิธีการของ DMF สำหรับการกำหนดผู้ใช้เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="2b72d-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="2b72d-115">วิธีการนี้จะเพิ่มหมายเลขบรรทัดเสมอ</span><span class="sxs-lookup"><span data-stu-id="2b72d-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="2b72d-116">วิธีการแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="2b72d-116">Issue workaround</span></span>

<span data-ttu-id="2b72d-117">ตรวจสอบให้แน่ใจว่ามีการกำหนดหมายเลขบรรทัดที่ต้องการในฟิลด์หมายเลขบรรทัดเอนทิตีข้อมูลแล้ว เมื่อคุณนำเข้าบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b72d-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="2b72d-118">ในกรณีนี้ DMF จะไม่เขียนทับหมายเลขบรรทัด</span><span class="sxs-lookup"><span data-stu-id="2b72d-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="2b72d-119">กลุ่มภาษีเริ่มต้นและส่วนลดเงินสดเริ่มต้นไม่ได้รับการเติมข้อมูลจากบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2b72d-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="2b72d-120">ถ้าคุณกำลังใช้บัญชีใบแจ้งหนี้ที่แตกต่างจากบัญชีลูกค้า กลุ่มภาษีเริ่มต้นและส่วนลดเงินสดเริ่มต้นจะไม่มีการเติมข้อมูลจากบัญชีใบแจ้งหนี้เมื่อสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b72d-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="2b72d-121">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="2b72d-121">This behavior is by design.</span></span> <span data-ttu-id="2b72d-122">ค่าเริ่มต้นสำหรับกลุ่มภาษี ส่วนลด เงินสด และข้อมูลราคาอื่นๆ จะขึ้นอยู่กับบัญชีลูกค้าไม่ใช่บัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2b72d-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="2b72d-123">ฉันได้รับข้อผิดพลาด "ไม่มีการตั้งค่าการอ้างอิงอ็อบเจกต์" ในระหว่างการยืนยันใบสั่งซื้อหรือมีข้อยกเว้น "เกิดข้อยกเว้นตามเป้าหมายของการเรียก" เกิดขึ้นระหว่างการลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2b72d-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="2b72d-124">ปัญหานี้อาจเกิดขึ้นเนื่องจากความไม่สอดคล้องกันในการกระจายใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b72d-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="2b72d-125">เมื่อต้องการยกเลิกการบล็อกปัญหานี้และรีเซ็ตใบสั่งซื้อเป็นสถานะ *แบบร่าง* ให้ไปที่การ **จัดซื้อและการจัดหา \> งานประจำงวด \> ล้างข้อมูล \> รีเซ็ตการกระจายใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="2b72d-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="2b72d-126">สำหรับข้อมูลเพิ่มเติมให้ดูที่การลงรายการบัญชีบล็อกต่อไปนี้: [แก้ไขข้อผิดพลาดในการกระจาย PO ใน Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)</span><span class="sxs-lookup"><span data-stu-id="2b72d-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="2b72d-127">การกระจายการลงบัญชีหนึ่งรายการขึ้นไปมีการกระจายมากเกินไปหรือต่ำเกินไป</span><span class="sxs-lookup"><span data-stu-id="2b72d-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2b72d-128">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="2b72d-128">Issue description</span></span>

<span data-ttu-id="2b72d-129">คุณจะได้รับข้อผิดพลาดต่อไปนี้: "การกระจายการลงบัญชีหนึ่งรายการขึ้นไปมีการกระจายมากเกินไปหรือต่ำกว่าแจกจ่าย"</span><span class="sxs-lookup"><span data-stu-id="2b72d-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2b72d-130">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="2b72d-130">Issue resolution</span></span>

<span data-ttu-id="2b72d-131">ปัญหานี้อาจเกิดขึ้นเนื่องจากความไม่สอดคล้องกันในการกระจายใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b72d-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="2b72d-132">เมื่อต้องการยกเลิกการบล็อกปัญหานี้และรีเซ็ตใบสั่งซื้อเป็นสถานะ *แบบร่าง* ให้ไปที่การ **จัดซื้อและการจัดหา \> งานประจำงวด \> ล้างข้อมูล \> รีเซ็ตการกระจายใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="2b72d-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="2b72d-133">สำหรับข้อมูลเพิ่มเติมให้ดูที่การลงรายการบัญชีบล็อกต่อไปนี้: [แก้ไขข้อผิดพลาดในการกระจาย PO ใน Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)</span><span class="sxs-lookup"><span data-stu-id="2b72d-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="2b72d-134">ฉันจะแสดงเฉพาะใบสั่งซื้อที่ฉันสร้างขึ้นได้เท่านั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2b72d-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="2b72d-135">ฟังก์ชันนี้ไม่พร้อมใช้งานในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2b72d-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="2b72d-136">ฉันสามารถจองสินค้าคงคลังและสร้างธุรกรรมสำหรับสินค้าคงคลังที่ลงทะเบียนไว้ในใบสั่งซื้อได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="2b72d-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="2b72d-137">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="2b72d-137">Issue description</span></span>

<span data-ttu-id="2b72d-138">แม้ว่าสินค้าจะอยู่ในสถานะ *ลงทะเบียนแล้ว* ในใบสั่งซื้อ คุณก็ยังสามารถจองสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="2b72d-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="2b72d-139">นั่นคือคุณสามารถสร้างธุรกรรมที่มีการลงทะเบียนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2b72d-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="2b72d-140">สร้างปัญหาอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="2b72d-140">Reproduce the issue</span></span>

<span data-ttu-id="2b72d-141">กระบวนการต่อไปนี้แสดงวิธีหนึ่งที่จะสร้างปัญหาอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="2b72d-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="2b72d-142">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b72d-142">Create a purchase order.</span></span>
2. <span data-ttu-id="2b72d-143">ลงทะเบียนบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b72d-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="2b72d-144">โปรดสังเกตว่าคุณสามารถสร้างการจองสินค้าหรือธุรกรรมที่มีการลงทะเบียนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2b72d-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2b72d-145">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="2b72d-145">Issue resolution</span></span>

<span data-ttu-id="2b72d-146">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="2b72d-146">This behavior is by design.</span></span> <span data-ttu-id="2b72d-147">ความคาดหวังคือสินค้าที่ลงทะเบียนไว้มีจริงในคลังสินค้าหรือสินค้าคงคลังและมีสำหรับการจอง</span><span class="sxs-lookup"><span data-stu-id="2b72d-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="2b72d-148">ใบสั่งซื้อไม่ได้สะท้อนถึงการตั้งค่าภาษาของนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="2b72d-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2b72d-149">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="2b72d-149">Issue description</span></span>

<span data-ttu-id="2b72d-150">ชื่อผลิตภัณฑ์ในใบสั่งซื้อจะแสดงอยู่ในภาษาของระบบแทนที่จะเป็นภาษาที่ตั้งค่าไว้สำหรับนิติบุคคลที่มีการสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b72d-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="2b72d-151">สร้างปัญหาอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="2b72d-151">Reproduce the issue</span></span>

<span data-ttu-id="2b72d-152">กระบวนการต่อไปนี้แสดงวิธีหนึ่งที่จะสร้างปัญหาอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="2b72d-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="2b72d-153">ตั้งค่าภาษาของระบบเป็น *EN-US* (ภาษาอังกฤษอเมริกัน)</span><span class="sxs-lookup"><span data-stu-id="2b72d-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="2b72d-154">ตรวจสอบให้แน่ใจว่ามีผลิตภัณฑ์ที่ภาษา *EN-US* และ *DE* (เยอรมัน) ถูกรักษาไว้สำหรับการแปลชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2b72d-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="2b72d-155">เปลี่ยนภาษาของนิติบุคคลที่จะเป็น *DE*</span><span class="sxs-lookup"><span data-stu-id="2b72d-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="2b72d-156">ในนิติบุคคลที่มีการตั้งค่าเป็นภาษา *DE* ให้สร้างใบสั่งซื้อที่มีผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2b72d-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="2b72d-157">โปรดสังเกตว่าชื่อผลิตภัณฑ์ยังคงแสดงอยู่ในภาษาอังกฤษแบบอเมริกัน (ภาษาของระบบ)</span><span class="sxs-lookup"><span data-stu-id="2b72d-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2b72d-158">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="2b72d-158">Issue resolution</span></span>

<span data-ttu-id="2b72d-159">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="2b72d-159">This behavior is by design.</span></span> <span data-ttu-id="2b72d-160">ในใบสั่งซื้อ ผลิตภัณฑ์จะแสดงอยู่ในภาษาของระบบเสมอ</span><span class="sxs-lookup"><span data-stu-id="2b72d-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="2b72d-161">ใช้ภาษาของใบสั่งซื้อเมื่อสร้างสมุดรายวันการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="2b72d-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="2b72d-162">รายชื่อผู้จัดจำหน่ายที่ได้รับอนุมัติตามเอนทิตีผลิตภัณฑ์ไม่อนุญาตให้มีการเปลี่ยนแปลงวันที่มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="2b72d-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2b72d-163">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="2b72d-163">Issue description</span></span>

<span data-ttu-id="2b72d-164">ผลิตภัณฑ์มีผู้จัดจำหน่ายที่ได้รับอนุมัติซึ่งมี ตัวอย่างเช่น วันที่มีผลบังคับใช้ตั้งแต่วันที่ 11 มกราคม 2018 (*01/11/2018*) และวันที่สิ้นสุด *ไม่มี*</span><span class="sxs-lookup"><span data-stu-id="2b72d-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="2b72d-165">ถ้าคุณพยายามเปลี่ยนแปลงวันที่มีผลบังคับใช้เป็นวันที่ 10 มกราคม 2018 (*01/10/2018*) หรือ 12 มกราคม 2018 (*01/12/2018*) คุณจะได้รับข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2b72d-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="2b72d-166">สามารถสร้างเรกคอร์ดในรายชื่อผู้จัดจำหน่ายที่ได้รับอนุมัติแล้ว (PdsApproveVendorList)</span><span class="sxs-lookup"><span data-stu-id="2b72d-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="2b72d-167">ค่า 'หมดอายุ' ต้องมากกว่าหรือเท่ากับค่า 'มีผลบังคับใช้'</span><span class="sxs-lookup"><span data-stu-id="2b72d-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2b72d-168">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="2b72d-168">Issue resolution</span></span>

<span data-ttu-id="2b72d-169">คุณสามารถขยายรอบระยะเวลาที่ผู้จัดจำหน่ายได้รับการอนุมัติแล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2b72d-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="2b72d-170">กฎต่อไปนี้จะมีผลบังคับ</span><span class="sxs-lookup"><span data-stu-id="2b72d-170">The following rules apply:</span></span>

- <span data-ttu-id="2b72d-171">เมื่อต้องการเปลี่ยนแปลงวันที่มีผลบังคับใช้เพื่อให้อยู่ก่อนหน้าเรกคอร์ดที่มีอยู่ (รอบระยะเวลา) ใดๆ สำหรับผู้จัดจำหน่ายสินค้า วันหมดอายุของรอบระยะเวลาใหม่ต้องเป็นวันก่อนหน้าวันหมดอายุทั้งหมดในเรกคอร์ดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="2b72d-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="2b72d-172">เมื่อต้องการเปลี่ยนแปลงวันหมดอายุเพื่อให้เป็นวันหลังจากรอบระยะเวลาใดๆ ที่มีอยู่ วันที่มีผลบังคับใช้ต้องเป็นวันหลังจากวันหมดอายุล่าสุดในเรกคอร์ดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="2b72d-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="2b72d-173">เมื่อต้องการลดรอบระยะเวลาทั้งหมดที่ผู้จัดจำหน่ายได้รับการอนุมัติแล้ว คุณต้องลบหรือปรับเปลี่ยนเรกคอร์ดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="2b72d-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="2b72d-174">อีกทางหนึ่งคือคุณสามารถใช้สวิตช์ **ตัด** ในระหว่างการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="2b72d-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="2b72d-175">สวิตช์นี้จะลบเรกคอร์ดที่มีอยู่ทั้งหมดในตารางสำหรับผู้จัดจำหน่ายที่ได้รับอนุมัติโดยเรียงตามสินค้า</span><span class="sxs-lookup"><span data-stu-id="2b72d-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="2b72d-176">สำหรับสถานการณ์จำลองตัวอย่างที่อธิบายไว้ในคำอธิบายปัญหา ซึ่งเรกคอร์ดมีวันที่มีผลบังคับใช้ *01/11/2018* และวันหมดอายุ *ไม่เคย* คุณสามารถนำเข้าเรกคอร์ดใหม่ที่มีวันที่มีผลบังคับใช้ของ *01/10/2018* และวันที่หมดอายุ *ไม่มี*</span><span class="sxs-lookup"><span data-stu-id="2b72d-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="2b72d-177">อย่างไรก็ตามคุณไม่สามารถลดรอบระยะเวลาเพื่อให้วันที่มีผลบังคับใช้มีการอัปเดตเป็น *01/12/2018* ผ่านทางการจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2b72d-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="2b72d-178">คุณต้องทำการเปลี่ยนแปลงนี้ผ่าน UI</span><span class="sxs-lookup"><span data-stu-id="2b72d-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a><span data-ttu-id="2b72d-179">หลังจากที่เปลี่ยนที่อยู่ที่จัดส่งในส่วนหัวของใบสั่งซื้อ จะไม่มีการซิงค์ชื่อการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="2b72d-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2b72d-180">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="2b72d-180">Issue description</span></span>

<span data-ttu-id="2b72d-181">ที่อยู่ในส่วนหัวของใบสั่งซื้อจะถูกอัปเดตไปยังที่อยู่ที่ ไม่ใช่ที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="2b72d-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="2b72d-182">ถึงแม้ว่ามีการอัปเดตที่อยู่บนใบสั่งซื้อ ก็จะไม่มีการอัปเดตชื่อการจัดส่งตามที่อยู่ที่อัปเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="2b72d-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2b72d-183">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="2b72d-183">Issue resolution</span></span>

<span data-ttu-id="2b72d-184">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="2b72d-184">This behavior is by design.</span></span> <span data-ttu-id="2b72d-185">ต้องจัดประเภทที่อยู่ที่เลือกเป็นที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="2b72d-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="2b72d-186">มิฉะนั้นจะไม่มีการอัปเดตชื่อการจัดส่งตามที่อยู่ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2b72d-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="2b72d-187">ฉันสามารถหาผู้ใช้ที่ยกเลิกใบสั่งซื้อได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="2b72d-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="2b72d-188">ข้อมูลนี้จะถูกติดตามเฉพาะเมื่อใบสั่งซื้ออาจมีการจัดการการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="2b72d-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="2b72d-189">ถ้าคุณใช้การจัดการการเปลี่ยนแปลง คุณสามารถดูว่าใครเป็นผู้ส่งการเปลี่ยนแปลง (การยกเลิก) และใครเป็นผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="2b72d-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>
