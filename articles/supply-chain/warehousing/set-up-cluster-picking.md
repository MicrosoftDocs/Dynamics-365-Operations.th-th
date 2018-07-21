---
title: "ตั้งค่าการเลือกคลัสเตอร์"
description: "หัวข้อนี้อธิบายวิธีการตั้งค่าการเลือกคลัสเตอร์ และวิธีการใช้การยืนยันรายการที่มีการเลือกคลัสเตอร์"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 52750321588d69483439873861682636c13a4936
ms.contentlocale: th-th
ms.lasthandoff: 07/21/2018

---

[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a><span data-ttu-id="ab996-103">ตั้งค่าการเลือกคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="ab996-103">Set up cluster picking</span></span>

<span data-ttu-id="ab996-104">หัวข้อนี้อธิบายวิธีทำให้ผู้ปฏิบัติงานสามารถใช้อุปกรณ์เคลื่อนของตนเพื่อจัดกลุ่มงานที่เลือกไว้ในคลัสเตอร์ เพื่อให้พวกเขาสามารถเบิกสินค้าจากสถานที่เดียวสำหรับใบสั่งผลิตหลายใบพร้อมกัน </span><span class="sxs-lookup"><span data-stu-id="ab996-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="ab996-105">ซึ่งเรียกว่า *การเลือกคลัสเตอร์*</span><span class="sxs-lookup"><span data-stu-id="ab996-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="ab996-106">เกี่ยวกับการเลือกคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="ab996-106">About cluster picking</span></span>

<span data-ttu-id="ab996-107">หลังจากที่นำออกใช้ใบสั่งผลิตไปยังคลังสินค้า ผู้ปฏิบัติงานสามารถใช้อุปกรณ์เคลื่อนที่เพื่อกำหนดใบสั่งเข้าในคลัสเตอร์ </span><span class="sxs-lookup"><span data-stu-id="ab996-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="ab996-108">คลัสเตอร์จะจัดระเบียบงานการเบิกสินค้าสำหรับผู้ปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="ab996-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="ab996-109">เมื่อใบสั่งผลิตถูกกำหนดให้กับคลัสเตอร์ ผู้ปฏิบัติงานต้องใช้การเลือกคลัสเตอร์เพื่อดำเนินงานการเบิกสินค้าสำหรับใบสั่ง </span><span class="sxs-lookup"><span data-stu-id="ab996-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="ab996-110">ผู้ปฏิบัติงานไม่สามารถใช้วิธีการเบิกสินค้าอื่นๆ </span><span class="sxs-lookup"><span data-stu-id="ab996-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="ab996-111">ถ้าใบสั่งงานกำหนดให้กับคลัสเตอร์โดยไม่ได้ตั้งใจ  ผู้ปฏิบัติงานต้องแยกคลัสเตอร์ และจากนั้น สร้างขึ้นใหม่</span><span class="sxs-lookup"><span data-stu-id="ab996-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="ab996-112">ถ้าจำเป็น ผู้ปฏิบัติงานสามารถผ่านคลัสเตอร์ไปให้ผู้ปฏิบัติงานอื่น </span><span class="sxs-lookup"><span data-stu-id="ab996-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="ab996-113">ตัวเลือกนี้เปลี่ยนสถานะคลัสเตอร์เป็น ผ่าน </span><span class="sxs-lookup"><span data-stu-id="ab996-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="ab996-114">เมื่อผู้ปฏิบัติงานใช้อุปกรณ์เคลื่อนที่เพื่อบ่งชี้ว่างานสำรองและการเบิกสินค้าเสร็จสมบูรณ์แล้ว ต้องยืนยันการจัดส่งหรือโหลดในไคลเอนต์ Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab996-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the Dynamics 365 for Finance and Operations client.</span></span>

## <a name="set-up-cluster-picking"></a><span data-ttu-id="ab996-115">ตั้งค่าการเลือกคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="ab996-115">Set up cluster picking</span></span>

<span data-ttu-id="ab996-116">เมื่อต้องการเปิดใช้งานการเลือกคลัสเตอร์ คุณต้องตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ab996-116">To enable cluster picking, you must set up the following:</span></span>

-   <span data-ttu-id="ab996-117">**โพรไฟล์ของคลัสเตอร์** – ระบุว่าจะสร้างรหัสคลัสเตอร์ จำนวนตำแหน่งที่จะใช้ เวลาที่จะแบ่งคลัสเตอร์ และวิธีการจัดลำดับ และตรวจสอบงานการเบิกสินค้า โดยอัตโนมัติหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ab996-117">**Cluster profiles** – Specify whether to automatically generate cluster IDs, the number of positions to use, when to break clusters, and how to sequence and verify the picking work.</span></span>

-   <span data-ttu-id="ab996-118">**เท็มเพลตงาน** – กำหนดวิธีการสร้างงานการเบิกสินค้าสำหรับการเลือกคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="ab996-118">**Work templates** – Define how to create the picking work for cluster picking.</span></span>

-   <span data-ttu-id="ab996-119">**คำสั่งสถานที่** – ระบุสถานที่ที่จะเบิกสินค้า และตำแหน่งที่จะวางสินค้า</span><span class="sxs-lookup"><span data-stu-id="ab996-119">**Location directives** – Specify where to pick items from, and where to put them.</span></span>

-   <span data-ttu-id="ab996-120">**รายการเมนูของอุปกรณ์เคลื่อนที่** – ตั้งค่าคอนฟิกรายการเมนูของอุปกรณ์เคลื่อนที่เพื่อใช้งานที่มีอยู่ ที่กำกับโดยการเลือกคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="ab996-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="ab996-121">จากนั้นคุณต้องเพิ่มรายการเมนูไปยังเมนูอุปกรณ์เคลื่อนที่เพื่อให้แสดงบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="ab996-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

-   <span data-ttu-id="ab996-122">**พารามิเตอร์การจัดการคลังสินค้า** – ระบุลำดับหมายเลขที่จะใช้ ถ้าคุณต้องการสร้างตัวระบุสำหรับคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="ab996-122">**Warehouse management parameters** – Specify the number sequence to use if you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="ab996-123">การตั้งค่าโพรไฟล์คลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="ab996-123">Set up a cluster profile</span></span>

<span data-ttu-id="ab996-124">การตั้งค่าโพรไฟล์คลัสเตอร์ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ab996-124">To set up a cluster profile, follow these steps:</span></span>

1.  <span data-ttu-id="ab996-125">คลิก **การบริหารคลังสินค้า** \> **ตั้งค่า** \> **อุปกรณ์เคลื่อนที่** \> **โพรไฟล์ของคลัสเตอร์**</span><span class="sxs-lookup"><span data-stu-id="ab996-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \> **Cluster profiles**.</span></span>

2.  <span data-ttu-id="ab996-126">คลิก **สร้าง** เพื่อสร้างโพรไฟล์ใหม่</span><span class="sxs-lookup"><span data-stu-id="ab996-126">Click **New** to create a new profile.</span></span>

3.  <span data-ttu-id="ab996-127">คลิก **สร้างคลัสเตอร์** และ ภายใต้ **การเรียงคลัสเตอร์** คลิก **สร้าง** เพื่อตั้งค่าเงื่อนไขการเรียงลำดับสำหรับคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="ab996-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="ab996-128">เงื่อนไขการเรียงลำดับควบคุมลำดับผู้ปฏิบัติงานที่จะดำเนินงานการเบิกสินค้า </span><span class="sxs-lookup"><span data-stu-id="ab996-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="ab996-129">คุณสามารถเพิ่มเกณฑ์ได้มากตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ab996-129">You can add as many criteria as needed.</span></span>

4.  <span data-ttu-id="ab996-130">ในฟิลด์ **หมายเลขลำดับ** ป้อนหมายเลขเพื่อกำหนดลำดับที่ซึ่งจะประมวลผลเกณฑ์การเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="ab996-130">In the **Sequence number** field, enter a number to define the order in which the sorting criteria are processed.</span></span>

5.  <span data-ttu-id="ab996-131">ในฟิลด์ **ชื่อฟิลด์** เลือกฟิลด์ที่จะตรวจสอบการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="ab996-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="ab996-132">ตัวอย่างเช่น ถ้าคุณเลือกฟิลด์ **WMSLocationId** จะเรียงลำดับตามสถานที่ </span><span class="sxs-lookup"><span data-stu-id="ab996-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

6.  <span data-ttu-id="ab996-133">ในฟิลด์ **การเรียงลำดับ** ให้เลือกตัวเลือกใดตัวเลือกหนึ่งดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ab996-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="ab996-134">**ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="ab996-134">**Option**</span></span>     | <span data-ttu-id="ab996-135">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="ab996-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab996-136">**การเรียงจากน้อยไปมาก**</span><span class="sxs-lookup"><span data-stu-id="ab996-136">**Ascending**</span></span>  | <span data-ttu-id="ab996-137">งานการเบิกสินค้าจะถูกเรียงลำดับจากน้อยไปมาก ตามเกณฑ์การเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="ab996-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="ab996-138">ตัวอย่างเช่น ถ้าคุณใช้ฟิลด์ **WMSLocationId** เป็นเกณฑ์การเรียงลำดับ และรหัสสถานที่ของคุณคือ 1, 2, 3 และ 4 คุณจะเบิกสินค้าจากสถานที่เก็บ 4 แรก</span><span class="sxs-lookup"><span data-stu-id="ab996-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="ab996-139">**การเรียงจากมากไปน้อย**</span><span class="sxs-lookup"><span data-stu-id="ab996-139">**Descending**</span></span> | <span data-ttu-id="ab996-140">งานการเบิกสินค้าจะถูกเรียงลำดับจากมากไปน้อย ตามเกณฑ์การเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="ab996-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="ab996-141">ตัวอย่างเช่น ถ้าคุณใช้ฟิลด์ **WMSLocationId** เป็นเกณฑ์การเรียงลำดับ และรหัสสถานที่ของคุณคือ 1, 2, 3 และ 4 คุณจะเบิกสินค้าจากสถานที่เก็บ 1 แรก</span><span class="sxs-lookup"><span data-stu-id="ab996-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="ab996-142">การยืนยันสินค้า</span><span class="sxs-lookup"><span data-stu-id="ab996-142">Item confirmation</span></span>

<span data-ttu-id="ab996-143">เมื่อมีการนำการเบิกสินค้าคลัสเตอร์มาใช้ การยืนยันสินค้าเป็นสิ่งสำคัญยิ่งในการตรวจสอบสินค้าที่ถูกเพิ่มลงในคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="ab996-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="ab996-144">คุณสามารถตรวจสอบสินค้าในการเบิกสินค้าคลัสเตอร์ในระหว่างกระบวนการเบิกสินค้าคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="ab996-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="ab996-145">การตั้งค่าขึ้นอยู่กับการตั้งค่าบาร์โค้ดของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ab996-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="ab996-146">ตั้งค่าการตรวจสอบสินค้าที่มีการเบิกสินค้าคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="ab996-146">Set up item verification with cluster picking</span></span>

1.  <span data-ttu-id="ab996-147">บนรายการเมนูของอุปกรณ์เคลื่อนที่ เปิดแบบฟอร์มการตั้งค่าสำหรับการยืนยันงาน: **การบริหารคลังสินค้า** \> **การจัดการคลังสินค้า** \> **ตั้งค่า** \> **อุปกรณ์เคลื่อนที่** \> **รายการเมนูของอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="ab996-147">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** \> **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>

2.  <span data-ttu-id="ab996-148">จากรายการเมนูบนอุปกรณ์เคลื่อนที่ เปิด **การตั้งค่าการยืนยันงาน**</span><span class="sxs-lookup"><span data-stu-id="ab996-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="ab996-149">ตัวเลือก **การยืนยันผลิตภัณฑ์** ช่วยให้คุณสามารถตรวจสอบสินค้าคงคลังแต่ละรายการได้จากอุปกรณ์เคลื่อนที่ เมื่อมีการสแกน</span><span class="sxs-lookup"><span data-stu-id="ab996-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>

