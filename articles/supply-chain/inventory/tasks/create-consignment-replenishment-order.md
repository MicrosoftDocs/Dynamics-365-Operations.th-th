---
title: สร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบ
description: หัวข้อนี้อธิบายวิธีการสร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบที่ซึ่งคุณสามารถติดตามการจัดส่งที่คาดไว้จากผู้จัดจำหน่ายไปยังสินค้าคงคลังที่มีการส่งมอบของคุณ
author: sherry-zheng
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0d2030277e0810bebef9356136b0e11effc6d5b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834036"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="27307-103">สร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="27307-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27307-104">หัวข้อนี้อธิบายวิธีการสร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบที่ซึ่งคุณสามารถติดตามการจัดส่งที่คาดไว้จากผู้จัดจำหน่ายไปยังสินค้าคงคลังที่มีการส่งมอบของคุณ</span><span class="sxs-lookup"><span data-stu-id="27307-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="27307-105">นอกจากนี้ยังแสดงวิธีการบันทึกการรับผลิตภัณฑ์เพื่อลงทะเบียนสินค้าคงคลังที่มีการส่งมอบเป็นปริมาณคงคลังคงเหลือที่ผู้จัดจำหน่ายเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="27307-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="27307-106">โดยทั่วไป กระบวนงานนี้จะกระทำโดยผู้เชี่ยวชาญด้านการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="27307-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="27307-107">คุณสามารถใช้คำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="27307-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="27307-108">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="27307-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="27307-109">สร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="27307-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="27307-110">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > การส่งมอบ > ใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบ**</span><span class="sxs-lookup"><span data-stu-id="27307-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="27307-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="27307-111">Select **New**.</span></span>
3. <span data-ttu-id="27307-112">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** เลือกผู้จัดจำหน่าย **US-104** (คุณต้องเลือกผู้จัดจำหน่ายที่มีการลงทะเบียนเป็นเจ้าของในหน้า **เจ้าของสินค้าคงคลัง**)</span><span class="sxs-lookup"><span data-stu-id="27307-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="27307-113">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="27307-113">Select **OK**.</span></span>
5. <span data-ttu-id="27307-114">เลือก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="27307-114">Select **Add line**.</span></span>
6. <span data-ttu-id="27307-115">ในฟิลด์ **หมายเลขสินค้า** ให้พิมพ์ `M9211CI` (คุณต้องเลือกสินค้าที่ตั้งค่าไว้สำหรับสินค้าคงคลังการส่งมอบ)</span><span class="sxs-lookup"><span data-stu-id="27307-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="27307-116">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="27307-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="27307-117">ในฟิลด์ **วันที่จัดส่งที่ร้องขอ** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="27307-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="27307-118">วันที่ร้องขอและวันที่ยืนยันจะถูกนำมาใช้โดยกลไกจัดการ MRP สำหรับการมาถึงที่คาดไว้ของสินค้า</span><span class="sxs-lookup"><span data-stu-id="27307-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="27307-119">ในฟิลด์ **วันที่จัดส่งที่ยืนยัน** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="27307-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="27307-120">ขยายส่วน **รายละเอียดรายการ**</span><span class="sxs-lookup"><span data-stu-id="27307-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="27307-121">เลือกแท็บ **มิติสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="27307-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="27307-122">เมื่อต้องการแสดงเจ้าของในฟิลด์ **เจ้าของมิติสินค้าคงคลัง** ให้รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="27307-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="27307-123">ขณะนี้มีการแสดงรายการ US-104 ของผู้จัดจำหน่ายเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="27307-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="27307-124">ตรวจสอบสถานะของรายการความเคลื่อนไหวของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="27307-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="27307-125">เลือก **สินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="27307-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="27307-126">เลือก **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="27307-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="27307-127">ในแถวที่ต้องการ โปรดทราบว่าฟิลด์ **ใบเสร็จ** ถูกตั้งค่าเป็น **สั่งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="27307-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="27307-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="27307-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="27307-129">รับสินค้า</span><span class="sxs-lookup"><span data-stu-id="27307-129">Receive items</span></span>
1. <span data-ttu-id="27307-130">เลือก **ใบรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="27307-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="27307-131">ในฟิลด์ **ใบรับผลิตภัณฑ์ภายนอก** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="27307-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="27307-132">ในฟิลด์ **ปริมาณ** ให้ป้อนหมายเลขที่ต่ำกว่าหมายเลขที่แสดงอยู่ที่นั่น</span><span class="sxs-lookup"><span data-stu-id="27307-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="27307-133">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="27307-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="27307-134">ตรวจสอบปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="27307-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="27307-135">เลือก **สินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="27307-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="27307-136">เลือก **ปริมาณคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="27307-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="27307-137">เลือก **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="27307-137">Select **Overview**.</span></span> <span data-ttu-id="27307-138">สินค้าที่ได้รับเป็นสินค้าคงคลังที่มีการส่งมอบที่ผู้จัดจำหน่ายเป็นเจ้าของเป็นปริมาณคงคลังคงเหลือที่พร้อมใช้งาน </span><span class="sxs-lookup"><span data-stu-id="27307-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="27307-139">ปริมาณคงเหลือในใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบจะแสดงอยู่ในฟิลด์ **ผลรวมที่สั่ง**</span><span class="sxs-lookup"><span data-stu-id="27307-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="27307-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="27307-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]