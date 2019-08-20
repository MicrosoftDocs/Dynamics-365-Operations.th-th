---
title: สร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบ
description: 'กระบวนงานนี้แสดงวิธีการสร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบซึ่งคุณสามารถติดตามการจัดส่งที่คาดไว้จากผู้จัดจำหน่ายไปยังสินค้าคงคลังที่มีการส่งมอบของคุณ '
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cf2e8f742fee2dedaac72902d207af0081700ca
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845557"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="14772-103">สร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="14772-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14772-104">กระบวนงานนี้แสดงวิธีการสร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบซึ่งคุณสามารถติดตามการจัดส่งที่คาดไว้จากผู้จัดจำหน่ายไปยังสินค้าคงคลังที่มีการส่งมอบของคุณ </span><span class="sxs-lookup"><span data-stu-id="14772-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="14772-105">นอกจากนี้ยังแสดงวิธีการบันทึกการรับผลิตภัณฑ์เพื่อลงทะเบียนสินค้าคงคลังที่มีการส่งมอบเป็นปริมาณคงคลังคงเหลือที่ผู้จัดจำหน่ายเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="14772-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="14772-106">โดยทั่วไป กระบวนงานนี้จะกระทำโดยผู้เชี่ยวชาญด้านการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="14772-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="14772-107">คุณสามารถใช้คำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="14772-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="14772-108">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="14772-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="14772-109">สร้างใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="14772-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="14772-110">ไปที่ การจัดซื้อและการจัดหา > การส่งมอบ > ใบสั่งการเพิ่มเติมสำหรับสินค้าที่มีการส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="14772-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="14772-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="14772-111">Click New.</span></span>
3. <span data-ttu-id="14772-112">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้เลือกผู้จัดจำหน่าย US-104</span><span class="sxs-lookup"><span data-stu-id="14772-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="14772-113">คุณต้องเลือกผู้จัดจำหน่ายที่ลงทะเบียนเป็นเจ้าของในหน้าเจ้าของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="14772-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="14772-114">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="14772-114">Click OK.</span></span>
5. <span data-ttu-id="14772-115">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="14772-115">Click Add line.</span></span>
6. <span data-ttu-id="14772-116">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ M9211CI</span><span class="sxs-lookup"><span data-stu-id="14772-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="14772-117">คุณต้องเลือกสินค้าที่ตั้งค่าสำหรับสินค้าคงคลังที่มีการส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="14772-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="14772-118">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="14772-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="14772-119">ในฟิลด์วันที่จัดส่งที่ร้องขอ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="14772-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="14772-120">วันที่ร้องขอและวันที่ยืนยันจะถูกนำมาใช้โดยกลไกจัดการ MRP สำหรับการมาถึงที่คาดไว้ของสินค้า</span><span class="sxs-lookup"><span data-stu-id="14772-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="14772-121">ในฟิลด์วันที่จัดส่งที่ยืนยัน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="14772-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="14772-122">ขยายส่วน รายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="14772-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="14772-123">คลิก แท็บมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="14772-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="14772-124">เมื่อต้องการแสดงเจ้าของในฟิลด์เจ้าของมิติสินค้าคงคลัง ให้รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="14772-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="14772-125">ขณะนี้มีการแสดงรายการ US-104 ของผู้จัดจำหน่ายเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="14772-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="14772-126">ตรวจสอบสถานะของรายการความเคลื่อนไหวของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="14772-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="14772-127">คลิกสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="14772-127">Click Inventory.</span></span>
2. <span data-ttu-id="14772-128">คลิกธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="14772-128">Click Transactions.</span></span>
3. <span data-ttu-id="14772-129">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="14772-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="14772-130">โปรดทราบว่าฟิลด์ใบเสร็จถูกตั้งค่าเป็นสั่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="14772-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="14772-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="14772-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="14772-132">รับสินค้า</span><span class="sxs-lookup"><span data-stu-id="14772-132">Receive items</span></span>
1. <span data-ttu-id="14772-133">คลิก ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="14772-133">Click Product receipt.</span></span>
2. <span data-ttu-id="14772-134">ในฟิลด์ใบรับสินค้าภายนอก ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="14772-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="14772-135">ในฟิลด์ปริมาณ ให้ป้อนหมายเลขที่ต่ำกว่าหมายเลขที่แสดงอยู่</span><span class="sxs-lookup"><span data-stu-id="14772-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span> 
4. <span data-ttu-id="14772-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="14772-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="14772-137">ตรวจสอบปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="14772-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="14772-138">คลิกสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="14772-138">Click Inventory.</span></span>
2. <span data-ttu-id="14772-139">คลิก ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="14772-139">Click On-hand.</span></span>
3. <span data-ttu-id="14772-140">คลิก ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="14772-140">Click Overview.</span></span>
    * <span data-ttu-id="14772-141">สินค้าที่ได้รับเป็นสินค้าคงคลังที่มีการส่งมอบที่ผู้จัดจำหน่ายเป็นเจ้าของเป็นปริมาณคงคลังคงเหลือที่พร้อมใช้งาน </span><span class="sxs-lookup"><span data-stu-id="14772-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="14772-142">ปริมาณคงเหลือในใบสั่งการเพิ่มเติมสินค้าที่มีการส่งมอบจะแสดงอยู่ในฟิลด์ผลรวมที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="14772-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="14772-143">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="14772-143">Close the page.</span></span>
5. <span data-ttu-id="14772-144">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="14772-144">Click Close.</span></span>

