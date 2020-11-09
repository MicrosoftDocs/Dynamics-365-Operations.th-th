---
title: สร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบ
description: หัวข้อนี้อธิบายวิธีการสร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบที่ซึ่งคุณสามารถติดตามการจัดส่งที่คาดไว้จากผู้จัดจำหน่ายไปยังสินค้าคงคลังที่มีการส่งมอบของคุณ
author: mkirknel
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e993190150e2d82088390d8db4b7c5ada2b0161
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018364"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="bcc05-103">สร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="bcc05-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bcc05-104">หัวข้อนี้อธิบายวิธีการสร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบที่ซึ่งคุณสามารถติดตามการจัดส่งที่คาดไว้จากผู้จัดจำหน่ายไปยังสินค้าคงคลังที่มีการส่งมอบของคุณ</span><span class="sxs-lookup"><span data-stu-id="bcc05-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="bcc05-105">นอกจากนี้ยังแสดงวิธีการบันทึกการรับผลิตภัณฑ์เพื่อลงทะเบียนสินค้าคงคลังที่มีการส่งมอบเป็นปริมาณคงคลังคงเหลือที่ผู้จัดจำหน่ายเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="bcc05-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="bcc05-106">โดยทั่วไป กระบวนงานนี้จะกระทำโดยผู้เชี่ยวชาญด้านการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="bcc05-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="bcc05-107">คุณสามารถใช้คำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="bcc05-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="bcc05-108">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="bcc05-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="bcc05-109">สร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="bcc05-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="bcc05-110">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > การส่งมอบ > ใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบ**</span><span class="sxs-lookup"><span data-stu-id="bcc05-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="bcc05-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="bcc05-111">Select **New**.</span></span>
3. <span data-ttu-id="bcc05-112">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** เลือกผู้จัดจำหน่าย **US-104** (คุณต้องเลือกผู้จัดจำหน่ายที่มีการลงทะเบียนเป็นเจ้าของในหน้า **เจ้าของสินค้าคงคลัง** )</span><span class="sxs-lookup"><span data-stu-id="bcc05-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="bcc05-113">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bcc05-113">Select **OK**.</span></span>
5. <span data-ttu-id="bcc05-114">เลือก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="bcc05-114">Select **Add line**.</span></span>
6. <span data-ttu-id="bcc05-115">ในฟิลด์ **หมายเลขสินค้า** ให้พิมพ์ `M9211CI` (คุณต้องเลือกสินค้าที่ตั้งค่าไว้สำหรับสินค้าคงคลังการส่งมอบ)</span><span class="sxs-lookup"><span data-stu-id="bcc05-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="bcc05-116">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="bcc05-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="bcc05-117">ในฟิลด์ **วันที่จัดส่งที่ร้องขอ** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="bcc05-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="bcc05-118">วันที่ร้องขอและวันที่ยืนยันจะถูกนำมาใช้โดยกลไกจัดการ MRP สำหรับการมาถึงที่คาดไว้ของสินค้า</span><span class="sxs-lookup"><span data-stu-id="bcc05-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="bcc05-119">ในฟิลด์ **วันที่จัดส่งที่ยืนยัน** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="bcc05-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="bcc05-120">ขยายส่วน **รายละเอียดรายการ**</span><span class="sxs-lookup"><span data-stu-id="bcc05-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="bcc05-121">เลือกแท็บ **มิติสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="bcc05-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="bcc05-122">เมื่อต้องการแสดงเจ้าของในฟิลด์ **เจ้าของมิติสินค้าคงคลัง** ให้รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="bcc05-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="bcc05-123">ขณะนี้มีการแสดงรายการ US-104 ของผู้จัดจำหน่ายเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="bcc05-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="bcc05-124">ตรวจสอบสถานะของรายการความเคลื่อนไหวของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="bcc05-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="bcc05-125">เลือก **สินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="bcc05-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="bcc05-126">เลือก **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="bcc05-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="bcc05-127">ในแถวที่ต้องการ โปรดทราบว่าฟิลด์ **ใบเสร็จ** ถูกตั้งค่าเป็น **สั่งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="bcc05-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="bcc05-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bcc05-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="bcc05-129">รับสินค้า</span><span class="sxs-lookup"><span data-stu-id="bcc05-129">Receive items</span></span>
1. <span data-ttu-id="bcc05-130">เลือก **ใบรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="bcc05-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="bcc05-131">ในฟิลด์ **ใบรับผลิตภัณฑ์ภายนอก** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bcc05-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="bcc05-132">ในฟิลด์ **ปริมาณ** ให้ป้อนหมายเลขที่ต่ำกว่าหมายเลขที่แสดงอยู่ที่นั่น</span><span class="sxs-lookup"><span data-stu-id="bcc05-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="bcc05-133">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bcc05-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="bcc05-134">ตรวจสอบปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="bcc05-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="bcc05-135">เลือก **สินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="bcc05-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="bcc05-136">เลือก **ปริมาณคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="bcc05-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="bcc05-137">เลือก **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="bcc05-137">Select **Overview**.</span></span> <span data-ttu-id="bcc05-138">สินค้าที่ได้รับเป็นสินค้าคงคลังที่มีการส่งมอบที่ผู้จัดจำหน่ายเป็นเจ้าของเป็นปริมาณคงคลังคงเหลือที่พร้อมใช้งาน </span><span class="sxs-lookup"><span data-stu-id="bcc05-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="bcc05-139">ปริมาณคงเหลือในใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบจะแสดงอยู่ในฟิลด์ **ผลรวมที่สั่ง**</span><span class="sxs-lookup"><span data-stu-id="bcc05-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="bcc05-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bcc05-140">Close the page.</span></span>

