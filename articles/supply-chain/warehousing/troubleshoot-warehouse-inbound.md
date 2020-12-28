---
title: แก้ไขปัญหาการดำเนินงานคลังสินค้าขาเข้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการดำเนินงานคลังสินค้าขาเข้าใน Microsoft Dynamics 365 Supply Chain Management
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 60b6e37ec9d716f635c2d25374ac25a82286660e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645983"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="a9dc1-103">แก้ไขปัญหาการดำเนินงานคลังสินค้าขาเข้า</span><span class="sxs-lookup"><span data-stu-id="a9dc1-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9dc1-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการดำเนินงานคลังสินค้าขาเข้าใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a9dc1-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="a9dc1-105">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "สร้างใบสั่งตรวจสอบคุณภาพแล้ว %1</span><span class="sxs-lookup"><span data-stu-id="a9dc1-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="a9dc1-106">ไม่พบโพรไฟล์ของคลัสเตอร์ โปรดตรวจสอบการตั้งค่าคอนฟิกของคุณ"</span><span class="sxs-lookup"><span data-stu-id="a9dc1-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a9dc1-107">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="a9dc1-107">Issue description</span></span>

<span data-ttu-id="a9dc1-108">ข้อความแสดงข้อผิดพลาดนี้เกี่ยวข้องกับกระบวนการรับที่มีการเปิดใช้งานการจัดการคุณภาพ (QMS)</span><span class="sxs-lookup"><span data-stu-id="a9dc1-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="a9dc1-109">ขึ้นอยู่กับการตั้งค่าคอนฟิกในสภาพแวดล้อมของคุณ รายละเอียดเพิ่มเติมเกี่ยวกับธุรกรรมที่สร้างข้อความแสดงข้อผิดพลาดอาจช่วยแก้ไขปัญหานี้ได้</span><span class="sxs-lookup"><span data-stu-id="a9dc1-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a9dc1-110">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="a9dc1-110">Issue resolution</span></span>

<span data-ttu-id="a9dc1-111">อันดับแรก ให้ตรวจสอบการตั้งค่า [การเบิกสินค้าคลัสเตอร์](set-up-cluster-picking.md) และตรวจสอบให้แน่ใจว่ามีการตั้งค่าโปรไฟล์ของคลัสเตอร์ของคุณอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a9dc1-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="a9dc1-112">คุณไม่สามารถใช้รายการเมนูของอุปกรณ์เคลื่อนที่สำหรับการเบิกสินค้าคลัสเตอร์เว้นแต่จะมีการตั้งค่าโปรไฟล์ของคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="a9dc1-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="a9dc1-113">ขึ้นอยู่กับสภาพแวดล้อมของคุณ คุณอาจต้องตรวจทานการตั้งค่าคอนฟิกที่เกี่ยวข้องอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="a9dc1-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="a9dc1-114">การรับป้ายทะเบียนแบบผสมไม่ทำงานสำหรับรหัสการโอนการครอบครองใด ๆ ยกเว้นเครดิต</span><span class="sxs-lookup"><span data-stu-id="a9dc1-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a9dc1-115">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="a9dc1-115">Issue description</span></span>

<span data-ttu-id="a9dc1-116">เมื่อฟิลด์ **การดำเนินการ** สำหรับรหัสการโอนการครอบครองถูกตั้งค่าเป็น *เครดิต* หรือ *เสีย* คุณสามารถใช้ได้เฉพาะ [รายการเมนูการรับป้ายทะเบียนแบบผสม](mixed-license-plate-receiving.md) เพื่อประมวลผลสินค้าที่ส่งคืนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a9dc1-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a9dc1-117">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="a9dc1-117">Issue resolution</span></span>

<span data-ttu-id="a9dc1-118">Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="a9dc1-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="a9dc1-119">ปัจจุบัน เฉพาะ [รหัสการโอนการครอบครอง](../service-management/set-up-disposition-codes.md) ที่มีฟิลด์ **การดำเนินการ** ตั้งค่าเป็น *เครดิต* หรือ *เสีย* ได้รับการสนับสนุนสำหรับการรับป้ายทะเบียนแบบผสม</span><span class="sxs-lookup"><span data-stu-id="a9dc1-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="a9dc1-120">เมื่อฉันเรียกใช้งานประจำงวดอัปเดตใบรับสินค้า ใบสั่งซื้อที่ยังไม่ได้ยืนยันจะได้รับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="a9dc1-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a9dc1-121">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="a9dc1-121">Issue description</span></span>

<span data-ttu-id="a9dc1-122">หลังจากที่คุณเรียกใช้งานประจำงวด *อัปเดตใบรับสินค้า* ระบบจะยืนยันใบสั่งซื้อที่ยังไม่ได้ยืนยันที่มีสถานะธุรกรรมสินค้าคงคลังที่ *ลงทะเบียน* ไว้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a9dc1-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a9dc1-123">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="a9dc1-123">Issue resolution</span></span>

<span data-ttu-id="a9dc1-124">ลักษณะการทำงานในการจัดการโหลดขาเข้าใหม่ *ผ่านการรับสินค้าในปริมาณการโหลด* ให้แก้ไขปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="a9dc1-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="a9dc1-125">เมื่อต้องการเปิดคุณลักษณะนี้ ไปที่ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) และเปิดใช้งานคุณลักษณะต่อไปนี้ (ในใบสั่งที่แสดงในรายการ):</span><span class="sxs-lookup"><span data-stu-id="a9dc1-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="a9dc1-126">เชื่อมโยงธุรกรรมสินค้าคงคลังของใบสั่งซื้อกับการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="a9dc1-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="a9dc1-127">การรับเกินปริมาณของการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="a9dc1-127">Over receipt of load quantities</span></span>

<span data-ttu-id="a9dc1-128">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ลงรายการบัญชีปริมาณผลิตภัณฑ์ที่ลงทะเบียนสำหรับใบสั่งซื้อ](inbound-load-handling.md#post-registered-quantities)</span><span class="sxs-lookup"><span data-stu-id="a9dc1-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>
