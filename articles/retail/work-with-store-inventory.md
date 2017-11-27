---
title: "จัดการสินค้าคงคลังของร้านค้า"
description: "บทความนี้อธิบายถึงชนิดของเอกสารที่คุณสามารถใช้เพื่อจัดการสินค้าคงคลังได้"
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6245d37ace9f46ecce83a0cf80a014d5de898bbc
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="manage-store-inventory"></a><span data-ttu-id="595a7-103">จัดการสินค้าคงคลังของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="595a7-103">Manage store inventory</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="595a7-104">บทความนี้อธิบายถึงชนิดของเอกสารที่คุณสามารถใช้เพื่อจัดการสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="595a7-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="595a7-105">คุณสามารถใช้ชนิดเอกสารต่อไปนี้ในการจัดการสินค้าคงคลังขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="595a7-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="595a7-106">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="595a7-106">Purchase orders</span></span>
<span data-ttu-id="595a7-107">ใบสั่งซื้อถูกสร้างที่สำนักงานใหญ่</span><span class="sxs-lookup"><span data-stu-id="595a7-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="595a7-108">ถ้าคลังสินค้าขายปลีกถูกรวมในหัวข้อของใบสั่งซื้อ ใบสั่งจะได้รับที่ร้านค้าโดยใช้ Modern POS (MPOS) หรือระบบคลาวด์ POS ใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="595a7-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="595a7-109">หลังจากที่ป้อนปริมาณที่ได้รับที่ร้านค้าถูกป้อน สามารถบันทึกเฉพาะสำหรับการแก้ไขเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="595a7-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="595a7-110">หรือปริมาณจะถูกกำหนด และส่งไปยังสำนักงานใหญ่</span><span class="sxs-lookup"><span data-stu-id="595a7-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="595a7-111">ที่สำนักงานใหญ่ ปริมาณที่ได้รับที่ร้านค้าจะแสดงอยู่ใน Dynamics 365 for Retail ในฟิลด์ **รับทันที** บนใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="595a7-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="595a7-112">ใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="595a7-112">Transfer orders</span></span>
<span data-ttu-id="595a7-113">ใบสั่งโอนย้ายสามารถระบุว่า ร้านค้าเฉพาะใดเป็นสถานที่สินค้าถูกจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="595a7-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="595a7-114">ในกรณีนี้ ใบสั่งโอนย้ายปรากฏที่ร้านค้าเป็นคำขอเบิกสินค้าใน Modern POS หรือระบบคลาวด์ POS</span><span class="sxs-lookup"><span data-stu-id="595a7-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="595a7-115">หลังจากที่ปริมาณที่ร้องขอถูกเบิก พวกเขาจะถูกยอมรับ และส่งไปยังสำนักงานใหญ่</span><span class="sxs-lookup"><span data-stu-id="595a7-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="595a7-116">ที่สำนักงานใหญ่ ปริมาณที่ถูกเบิกที่ร้านค้าจะแสดงอยู่ใน Dynamics 365 for Retail ในฟิลด์ **จัดส่งทันที** บนใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="595a7-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="595a7-117">ใบสั่งโอนย้ายอาจระบุว่าร้านค้าเฉพาะใดเป็นสถานที่สินค้าถูกส่งไป</span><span class="sxs-lookup"><span data-stu-id="595a7-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="595a7-118">ในกรณีนี้ ใบสั่งโอนย้ายปรากฏที่ร้านค้าเป็นคำขอรับใน Modern POS หรือระบบคลาวด์ POS</span><span class="sxs-lookup"><span data-stu-id="595a7-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="595a7-119">หลังจากที่ป้อนปริมาณที่ได้รับที่ร้านค้าถูกป้อน สามารถบันทึกเฉพาะสำหรับการแก้ไขเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="595a7-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="595a7-120">หรือปริมาณจะถูกกำหนด และส่งไปยังสำนักงานใหญ่</span><span class="sxs-lookup"><span data-stu-id="595a7-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="595a7-121">ที่สำนักงานใหญ่ ปริมาณที่ได้รับที่ร้านค้าจะแสดงอยู่ใน Dynamics 365 for Retail ในฟิลด์ **รับทันที** บนใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="595a7-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="595a7-122">การตรวจนับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="595a7-122">Stock counts</span></span>
<span data-ttu-id="595a7-123">การตรวจนับสินค้าคงคลังสามารถตามกำหนดการ หรือไม่ได้ตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="595a7-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="595a7-124">การตรวจนับสินค้าคงคลังตามกำหนดการเริ่มต้นที่สำนักงานใหญ่ ซึ่งระบุสินค้าที่ต้องถูกตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="595a7-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="595a7-125">สำนักงานใหญ่สร้างเอกสารการตรวจนับที่จะได้รับที่ร้านค้า ซึ่งมีปริมาณของสินค้าคงคลังคงเหลือจริงใน MPOS หรือระบบคลาวด์ POS</span><span class="sxs-lookup"><span data-stu-id="595a7-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="595a7-126">การตรวจนับสินค้าคงคลังที่ไม่ได้ตามกำหนดการเริ่มต้นที่ร้านค้า และปริมาณของสินค้าคงคลังคงเหลือจริงถูกอัพเดตทั้งใน MPOS หรือระบบคลาวด์ POS</span><span class="sxs-lookup"><span data-stu-id="595a7-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="595a7-127">ไม่เหมือนกับการตรวจนับสินค้าคงคลังตามกำหนดการ การตรวจนับสินค้าคงคลังที่ไม่ได้ตามกำหนดการจะไม่มีรายการที่กำหนดไว้ล่วงหน้าของสินค้า</span><span class="sxs-lookup"><span data-stu-id="595a7-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="595a7-128">เมื่อเสร็จสิ้นการตรวจนับสินค้าคงคลังชนิดใดชนิดหนึ่ง จะถูกกำหนด และส่งไปยังสำนักงานใหญ่</span><span class="sxs-lookup"><span data-stu-id="595a7-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="595a7-129">ที่สำนักงานใหญ่ การตรวจนับจะถูกตรวจสอบ และลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="595a7-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="595a7-130">การค้นหาสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="595a7-130">Inventory lookup</span></span>
<span data-ttu-id="595a7-131">สามารถดูปริมาณสินค้าคงเหลือปัจจุบันสำหรับร้านค้าและคลังสินค้าต่างๆ ได้บนหน้าการค้นหาสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="595a7-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="595a7-132">นอกเหนือจากปริมาณคงคลังคงเหลือปัจจุบัน ยังสามารถดูปริมาณที่ให้สัญญาได้ (ATP) สำหรับแต่ละร้านค้าได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="595a7-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="595a7-133">เมื่อต้องการทำเช่นนั้น เลือกร้านค้าที่คุณต้องการดู ATP แล้วคลิก **แสดงความพร้อมใช้งานของร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="595a7-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





