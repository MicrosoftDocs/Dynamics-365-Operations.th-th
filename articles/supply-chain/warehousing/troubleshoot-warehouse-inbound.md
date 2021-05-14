---
title: แก้ไขปัญหาการดำเนินงานคลังสินค้าขาเข้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการดำเนินงานคลังสินค้าขาเข้าใน Microsoft Dynamics 365 Supply Chain Management
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920998"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="98e49-103">แก้ไขปัญหาการดำเนินงานคลังสินค้าขาเข้า</span><span class="sxs-lookup"><span data-stu-id="98e49-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98e49-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการดำเนินงานคลังสินค้าขาเข้าใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="98e49-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="98e49-105">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "สร้างใบสั่งตรวจสอบคุณภาพแล้ว %1</span><span class="sxs-lookup"><span data-stu-id="98e49-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="98e49-106">ไม่พบโพรไฟล์ของคลัสเตอร์ โปรดตรวจสอบการตั้งค่าคอนฟิกของคุณ"</span><span class="sxs-lookup"><span data-stu-id="98e49-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="98e49-107">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="98e49-107">Issue description</span></span>

<span data-ttu-id="98e49-108">ข้อความแสดงข้อผิดพลาดนี้เกี่ยวข้องกับกระบวนการรับที่มีการเปิดใช้งานการจัดการคุณภาพ (QMS)</span><span class="sxs-lookup"><span data-stu-id="98e49-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="98e49-109">ขึ้นอยู่กับการตั้งค่าคอนฟิกในสภาพแวดล้อมของคุณ รายละเอียดเพิ่มเติมเกี่ยวกับธุรกรรมที่สร้างข้อความแสดงข้อผิดพลาดอาจช่วยแก้ไขปัญหานี้ได้</span><span class="sxs-lookup"><span data-stu-id="98e49-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="98e49-110">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="98e49-110">Issue resolution</span></span>

<span data-ttu-id="98e49-111">อันดับแรก ให้ตรวจสอบการตั้งค่า [การเบิกสินค้าคลัสเตอร์](set-up-cluster-picking.md) และตรวจสอบให้แน่ใจว่ามีการตั้งค่าโปรไฟล์ของคลัสเตอร์ของคุณอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="98e49-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="98e49-112">คุณไม่สามารถใช้รายการเมนูของอุปกรณ์เคลื่อนที่สำหรับการเบิกสินค้าคลัสเตอร์เว้นแต่จะมีการตั้งค่าโปรไฟล์ของคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="98e49-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="98e49-113">ขึ้นอยู่กับสภาพแวดล้อมของคุณ คุณอาจต้องตรวจทานการตั้งค่าคอนฟิกที่เกี่ยวข้องอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="98e49-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="98e49-114">การรับป้ายทะเบียนแบบผสมไม่ทำงานสำหรับรหัสการโอนการครอบครองใด ๆ ยกเว้นเครดิต</span><span class="sxs-lookup"><span data-stu-id="98e49-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="98e49-115">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="98e49-115">Issue description</span></span>

<span data-ttu-id="98e49-116">เมื่อฟิลด์ **การดำเนินการ** สำหรับรหัสการโอนการครอบครองถูกตั้งค่าเป็น *เครดิต* หรือ *เสีย* คุณสามารถใช้ได้เฉพาะ [รายการเมนูการรับป้ายทะเบียนแบบผสม](mixed-license-plate-receiving.md) เพื่อประมวลผลสินค้าที่ส่งคืนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="98e49-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="98e49-117">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="98e49-117">Issue resolution</span></span>

<span data-ttu-id="98e49-118">Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="98e49-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="98e49-119">ปัจจุบัน เฉพาะ [รหัสการโอนการครอบครอง](../service-management/set-up-disposition-codes.md) ที่มีฟิลด์ **การดำเนินการ** ตั้งค่าเป็น *เครดิต* หรือ *เสีย* ได้รับการสนับสนุนสำหรับการรับป้ายทะเบียนแบบผสม</span><span class="sxs-lookup"><span data-stu-id="98e49-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="98e49-120">เมื่อฉันเรียกใช้งานประจำงวดอัปเดตใบรับสินค้า ใบสั่งซื้อที่ยังไม่ได้ยืนยันจะได้รับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="98e49-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="98e49-121">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="98e49-121">Issue description</span></span>

<span data-ttu-id="98e49-122">หลังจากที่คุณเรียกใช้งานประจำงวด *อัปเดตใบรับสินค้า* ระบบจะยืนยันใบสั่งซื้อที่ยังไม่ได้ยืนยันที่มีสถานะธุรกรรมสินค้าคงคลังที่ *ลงทะเบียน* ไว้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="98e49-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="98e49-123">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="98e49-123">Issue resolution</span></span>

<span data-ttu-id="98e49-124">ลักษณะการทำงานในการจัดการโหลดขาเข้าใหม่ *ผ่านการรับสินค้าในปริมาณการโหลด* ให้แก้ไขปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="98e49-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="98e49-125">เมื่อต้องการเปิดคุณลักษณะนี้ ไปที่พื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) และเปิดใช้งานคุณลักษณะต่อไปนี้ (ในใบสั่งที่แสดงในรายการ):</span><span class="sxs-lookup"><span data-stu-id="98e49-125">To turn on this feature, go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="98e49-126">เชื่อมโยงธุรกรรมสินค้าคงคลังของใบสั่งซื้อกับการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="98e49-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="98e49-127">การรับเกินปริมาณของการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="98e49-127">Over receipt of load quantities</span></span>

<span data-ttu-id="98e49-128">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ลงรายการบัญชีปริมาณผลิตภัณฑ์ที่ลงทะเบียนสำหรับใบสั่งซื้อ](inbound-load-handling.md#post-registered-quantities)</span><span class="sxs-lookup"><span data-stu-id="98e49-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="98e49-129">เมื่อฉันลงทะเบียนใบสั่งขาเข้า ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ปริมาณไม่ถูกต้อง"</span><span class="sxs-lookup"><span data-stu-id="98e49-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="98e49-130">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="98e49-130">Issue description</span></span>

<span data-ttu-id="98e49-131">ถ้าฟิลด์ **นโยบายการจัดกลุ่มป้ายทะเบียน** ถูกกําหนดเป็น *ผู้ใช้กําหนดไว้* เพื่อรายการเมนูของอุปกรณ์เคลื่อนที่ที่ใช้เพื่อลงทะเบียนใบสั่งขาเข้า คุณจะได้รับข้อความแสดงข้อผิดพลาด ("ปริมาณไม่ถูกต้อง") และคุณไม่สามารถลงทะเบียนให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="98e49-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="98e49-132">สาเหตุปัญหา</span><span class="sxs-lookup"><span data-stu-id="98e49-132">Issue cause</span></span>

<span data-ttu-id="98e49-133">เมื่อ *ผู้ใช้กําหนดไว้* ใช้เป็นนโยบายการจัดกลุ่มป้ายทะเบียน ระบบจะแบ่งสินค้าคงคลังขาเข้าออกเป็นป้ายทะเบียนแยกต่างหาก ตามที่ระบุโดยกลุ่มลดับหน่วย</span><span class="sxs-lookup"><span data-stu-id="98e49-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="98e49-134">ถ้ามีการใช้หมายเลขชุดงานหรือหมายเลขลำดับประจำสินค้าเพื่อติดตามสินค้าที่รับ จะต้องระบุปริมาณของชุดงานหรือหมายเลขลำดับประจำสินค้าชนิดต่อป้ายทะเบียนที่มีการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="98e49-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="98e49-135">หากปริมาณที่ระบุเป็นป้ายทะเบียนเกินปริมาณที่ต้องได้รับสำหรับมิติปัจจุบัน คุณจะได้รับข้อความแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="98e49-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="98e49-136">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="98e49-136">Issue resolution</span></span>

<span data-ttu-id="98e49-137">เมื่อคุณลงทะเบียนสินค้าโดยใช้รายการเมนูของอุปกรณ์เคลื่อนที่ที่มีการตั้งค่าฟิลด์ **นโยบายการจัดกลุ่มป้ายทะเบียน** เป็น *กําหนดโดยผู้ใช้* ระบบอาจกําหนดให้คุณต้องยืนยันหรือป้อนหมายเลขป้ายทะเบียน หมายเลขชุดงาน หรือหหมายเลขลำดับประจำสินค้า</span><span class="sxs-lookup"><span data-stu-id="98e49-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="98e49-138">บนหน้าการยืนยันป้ายทะเบียน ระบบจะแสดงปริมาณที่ถูกปันส่วนให้กับป้ายทะเบียนปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="98e49-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="98e49-139">ในหน้าการยืนยันชุดงานหรือชุด ระบบจะแสดงปริมาณที่ยังคงได้รับบนป้ายทะเบียนปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="98e49-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="98e49-140">และยังจะรวมฟิลด์ที่คุณสามารถป้อนปริมาณที่จะลงทะเบียนให้กับชุดป้ายทะเบียนและหมายเลขชุดงานหรือหมายเลขลำดับประจำสินค้าด้วย</span><span class="sxs-lookup"><span data-stu-id="98e49-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="98e49-141">ในกรณีนี้ ตรวจสอบให้แน่ใจว่าปริมาณที่ลงทะเบียนไว้ของป้ายทะเบียนไม่เกินปริมาณที่ยังคงได้รับ</span><span class="sxs-lookup"><span data-stu-id="98e49-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="98e49-142">หรือถ้ามีการสร้างป้ายทะเบียนมากเกินไปในการลงทะเบียนใบสั่งขาเข้า ค่าของฟิลด์น **โยบายการจัดกลุ่มป้ายทะเบียน** สามารถเปลี่ยนเป็น *การจัดกลุ่มป้ายทะเบียน* ได้ คุณสามารถมอบหมายกลุ่มลำดับหน่วยใหม่ให้กับสินค้า หรือตัวเลือก **การจัดกลุ่มป้ายทะเบียน** สำหรับกลุ่มลำดับที่สามารถยกเลิกการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="98e49-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
