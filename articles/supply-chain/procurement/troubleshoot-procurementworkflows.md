---
title: วิธีแก้ปัญหาลำดับงานการจัดซื้อและการจัดหา
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบในระหว่างที่คุณทำงานกับลำดับงานการจัดซื้อและการจัดหา
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cdedc45b8f057310801f134104156a732fb58d86
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018548"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="5d5d5-103">วิธีแก้ปัญหาลำดับงานการจัดซื้อและการจัดหา</span><span class="sxs-lookup"><span data-stu-id="5d5d5-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="5d5d5-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบในระหว่างที่คุณทำงานกับลำดับงานการจัดซื้อและการจัดหา</span><span class="sxs-lookup"><span data-stu-id="5d5d5-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="5d5d5-105">เกิดข้อผิดพลาดเมื่อส่งใบสั่งซื้อไปยังลำดับงานอีกครั้งหลังจากที่มีการเปลี่ยนแปลง: "การเปลี่ยนแปลงที่ใบสั่งซื้อ X สามารถใช้ได้เฉพาะในสถานะร่างเมื่อมีการเรียกใช้การจัดการการเปลี่ยนแปลง"</span><span class="sxs-lookup"><span data-stu-id="5d5d5-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="5d5d5-106">ปัญหานี้จะเกิดขึ้นเฉพาะเมื่อใบสั่งซื้ออยู่ในสถานะ *ยืนยัน* ก่อนที่คุณจะร้องขอการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="5d5d5-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="5d5d5-107">ถ้าคุณร้องขอการเปลี่ยนแปลงในขณะที่ใบสั่งซื้ออยู่ในสถานะ *อนุมัติแล้ว* คุณสามารถประมวลผลลำดับงานเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="5d5d5-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="5d5d5-108">คำอธิบายข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="5d5d5-108">Error description</span></span>

<span data-ttu-id="5d5d5-109">เกิดข้อผิดพลาดต่อไปนี้ในลำดับงานเมื่อส่งใบสั่งซื้ออีกครั้งหลังจากที่มีการเปลี่ยนแปลง:</span><span class="sxs-lookup"><span data-stu-id="5d5d5-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="5d5d5-110">หยุด (ข้อผิดพลาด): ข้อยกเว้น X++: การเปลี่ยนแปลงใบสั่งซื้อ PO0000569 เท่านั้นที่สามารถใช้ได้เฉพาะในแบบร่างสถานะที่มีการเรียกใช้การจัดการการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="5d5d5-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="5d5d5-111">SysWorkflowParticipantProvider-แก้ไข</span><span class="sxs-lookup"><span data-stu-id="5d5d5-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="5d5d5-112">SysWorkflowParticipantProvider-แก้ไขผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="5d5d5-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="5d5d5-113">SysWorkflowServiceProvider-แก้ไขผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="5d5d5-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="5d5d5-114">SysWorkflowQueue-ดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="5d5d5-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5d5d5-115">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="5d5d5-115">Issue resolution</span></span>

<span data-ttu-id="5d5d5-116">ปัญหานี้อาจเกิดขึ้นเนื่องจากความไม่สอดคล้องกันในการกระจายใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="5d5d5-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="5d5d5-117">เมื่อต้องการยกเลิกการบล็อกปัญหานี้และรีเซ็ตใบสั่งซื้อเป็นสถานะ *แบบร่าง* ให้ไปที่การ **จัดซื้อและการจัดหา \> งานประจำงวด \> ล้างข้อมูล \> รีเซ็ตการกระจายใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="5d5d5-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="5d5d5-118">สำหรับข้อมูลเพิ่มเติมให้ดูที่การลงรายการบัญชีบล็อกต่อไปนี้: [แก้ไขข้อผิดพลาดในการกระจาย PO ใน Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)</span><span class="sxs-lookup"><span data-stu-id="5d5d5-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="5d5d5-119">จะมีการแก้ไขปัญหานี้ผ่านทาง [บทความฐานความรู้ของ Microsoft (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138)</span><span class="sxs-lookup"><span data-stu-id="5d5d5-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="5d5d5-120">การกระจายการลงบัญชีหนึ่งรายการขึ้นไปมีการกระจายมากเกินไปหรือต่ำเกินไป</span><span class="sxs-lookup"><span data-stu-id="5d5d5-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="5d5d5-121">ปัญหานี้อาจเกิดขึ้นเนื่องจากความไม่สอดคล้องกันในการกระจายใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="5d5d5-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="5d5d5-122">เมื่อต้องการยกเลิกการบล็อกปัญหานี้และรีเซ็ตใบสั่งซื้อเป็นสถานะ *แบบร่าง* ให้ไปที่การ **จัดซื้อและการจัดหา \> งานประจำงวด \> ล้างข้อมูล \> รีเซ็ตการกระจายใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="5d5d5-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="5d5d5-123">สำหรับข้อมูลเพิ่มเติมให้ดูที่การลงรายการบัญชีบล็อกต่อไปนี้: [แก้ไขข้อผิดพลาดในการกระจาย PO ใน Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)</span><span class="sxs-lookup"><span data-stu-id="5d5d5-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="5d5d5-124">ถ้ายอดคงเหลือของการจัดส่งถูกยกเลิกในใบสั่งซื้อที่มีการเปิดใช้งานการจัดการการเปลี่ยนแปลง ใบสั่งซื้อจะเป็นสถานะเป็น ยืนยันแล้ว</span><span class="sxs-lookup"><span data-stu-id="5d5d5-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d5d5-125">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="5d5d5-125">Issue description</span></span>

<span data-ttu-id="5d5d5-126">สำหรับใบสั่งซื้อที่ขึ้นอยู่กับการจัดการการเปลี่ยนแปลง ถ้าการเปลี่ยนแปลงที่ร้องขอเท่านั้นที่มีการยกเลิกการจัดส่งสินค้าคงเหลือในบรรทัดหนึ่งบรรทัดขึ้นไป ใบสั่งซื้อจะเปลี่ยนเป็นสถานะ *ยืนยันแล้ว* โดยตรง เมื่ออนุมัติแล้วและจะไม่มีการสร้างสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5d5d5-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5d5d5-127">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="5d5d5-127">Issue resolution</span></span>

<span data-ttu-id="5d5d5-128">การยกเลิกส่วนที่เหลือของการจัดส่งไม่มีผลกระทบต่อเนื้อหาของสมุดรายวันใบยืนยัน</span><span class="sxs-lookup"><span data-stu-id="5d5d5-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="5d5d5-129">ฟังก์ชันนี้ควรใช้เมื่อมีการรับสินค้าเพียงบางส่วนและควรยกเลิกคุณภาพที่เหลือในขั้นตอนของกระบวนการหลังจากที่มีการยืนยันใบสั่งซื้อกับผู้จัดจำหน่ายแล้ว</span><span class="sxs-lookup"><span data-stu-id="5d5d5-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="5d5d5-130">ถ้าควรจะสะท้อนให้เห็นในการยืนยันใบสั่งซื้อ ปริมาณควรมีการปรับปรุงในบรรทัดใบสั่งซื้อเพื่อให้ต้องมีการใช้การยืนยัน</span><span class="sxs-lookup"><span data-stu-id="5d5d5-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="5d5d5-131">อีกทางหนึ่งคือถ้าไม่มีการรับสินค้าที่ได้รับในบรรทัด ปริมาณสามารถถูกลบออกได้</span><span class="sxs-lookup"><span data-stu-id="5d5d5-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="5d5d5-132">ในกรณีนี้จะต้องมีการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="5d5d5-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="5d5d5-133">ใบสั่งซื้อที่ถูกยกเลิกจะปรากฏในรายการแบบร่างในพื้นที่ทำงานการจัดเตรียมใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="5d5d5-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d5d5-134">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="5d5d5-134">Issue description</span></span>

<span data-ttu-id="5d5d5-135">หลังจากที่คุณยกเลิกใบสั่งซื้อที่อยู่ในสถานะ *ยืนยันแล้ว* ใบสั่งซื้อที่ถูกยกเลิกยังคงแสดงอยู่ในรายการของใบสั่งซื้อฉบับร่างในพื้นที่ทำงาน **การจัดเตรียมใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="5d5d5-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5d5d5-136">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="5d5d5-136">Issue resolution</span></span>

<span data-ttu-id="5d5d5-137">ปัญหานี้เกิดขึ้นเฉพาะสำหรับใบสั่งซื้อที่อาจมีการเปลี่ยนแปลงการจัดการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5d5d5-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="5d5d5-138">เกิดขึ้นเนื่องจากการยกเลิกจะถือว่ามีการเปลี่ยนแปลงที่ต้องได้รับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="5d5d5-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="5d5d5-139">โดยระบบจะดำเนินการอนุมัติโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="5d5d5-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="5d5d5-140">ดังนั้นกระบวนการคือการส่งใบสั่งซื้อที่ถูกยกเลิกไปที่ลำดับงานการอนุมัติเพื่อให้สามารถเปลี่ยนเป็นสถานะ *ที่อนุมัติแล้ว*</span><span class="sxs-lookup"><span data-stu-id="5d5d5-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="5d5d5-141">ในจุดนั้น ใบสั่งซื้อจะไม่ปรากฏในรายการใบสั่งซื้อฉบับร่างในพื้นที่ทำงาน **การจัดเตรียมใบสั่งซื้อ** อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="5d5d5-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

