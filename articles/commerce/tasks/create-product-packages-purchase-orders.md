---
title: " สร้างบรรจุภัณฑ์ของผลิตภัณฑ์สำหรับใบสั่งซื้อ"
description: 'กระบวนการนี้นำไปสู่การสร้างบรรจุภรรฑ์ของผลิตภัณฑ์ และการใช้บนใบสั่งซื้อ '
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b0084c6b4acbf14e3afec552575d5be26114237
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416177"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="b77ee-103"> สร้างบรรจุภัณฑ์ของผลิตภัณฑ์สำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b77ee-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b77ee-104">กระบวนการนี้นำไปสู่การสร้างบรรจุภรรฑ์ของผลิตภัณฑ์ และการใช้บนใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="b77ee-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="b77ee-105">ใบสั่งซื้อจะถูกใช้เพื่อสร้างใบสั่งสำหรับผลิตภัณฑ์ชุดที่กำหนดไว้ล่วงหน้า </span><span class="sxs-lookup"><span data-stu-id="b77ee-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="b77ee-106">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="b77ee-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="b77ee-107">สร้างบรรจุภัณฑ์ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b77ee-107">Create a product package</span></span>
1. <span data-ttu-id="b77ee-108">ไปยัง การขายปลีกและการค้า > การบริหารสินค้าคงคลัง > การเติมเต็มสินค้า > แพคเกจสินค้า</span><span class="sxs-lookup"><span data-stu-id="b77ee-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="b77ee-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b77ee-109">Click New.</span></span>
3. <span data-ttu-id="b77ee-110">ในฟิลด์หมายเลขบรรจุภรรฑ์ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b77ee-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="b77ee-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b77ee-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b77ee-112">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b77ee-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b77ee-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b77ee-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b77ee-114">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b77ee-114">Click Add.</span></span>
8. <span data-ttu-id="b77ee-115">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ '0160'</span><span class="sxs-lookup"><span data-stu-id="b77ee-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="b77ee-116">ในฟิลด์ขนาด ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b77ee-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="b77ee-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b77ee-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="b77ee-118">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b77ee-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="b77ee-119">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b77ee-119">Click Add.</span></span>
13. <span data-ttu-id="b77ee-120">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ '0160'</span><span class="sxs-lookup"><span data-stu-id="b77ee-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="b77ee-121">ในฟิลด์หมายเลขตัวแปร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b77ee-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="b77ee-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b77ee-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="b77ee-123">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b77ee-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="b77ee-124">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b77ee-124">Click Add.</span></span>
18. <span data-ttu-id="b77ee-125">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ '0175'</span><span class="sxs-lookup"><span data-stu-id="b77ee-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="b77ee-126">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b77ee-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="b77ee-127">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b77ee-127">Click Save.</span></span>
21. <span data-ttu-id="b77ee-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b77ee-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="b77ee-129">เพิ่มแพคเกจในใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b77ee-129">Add package to purchase order</span></span>
1. <span data-ttu-id="b77ee-130">ไปที่บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b77ee-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="b77ee-131">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b77ee-131">Click New.</span></span>
3. <span data-ttu-id="b77ee-132">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b77ee-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b77ee-133">ในรายการ ให้เลือกผู้จัดจำหน่ายเดียวกันกับที่บรรจุภัณฑ์ของผลิตภัณฑ์ถูกสร้างไว้ให้ก่อนหน้านี้ ถ้าผู้จัดจำหน่ายถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="b77ee-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="b77ee-134">เปิดปิดการขยายของส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="b77ee-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="b77ee-135">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b77ee-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b77ee-136">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b77ee-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b77ee-137">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b77ee-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="b77ee-138">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b77ee-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="b77ee-139">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b77ee-139">Click OK.</span></span>
11. <span data-ttu-id="b77ee-140">สลับการขยายของส่วนรายละเอียดรายการ</span><span class="sxs-lookup"><span data-stu-id="b77ee-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="b77ee-141">คลิกที่แท็บบรรจุภัณฑ์ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b77ee-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="b77ee-142">คลิก บรรทัดรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b77ee-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="b77ee-143">คลิก สร้างบรรทัดรายการจากบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b77ee-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="b77ee-144">ในรายการ ค้นหาและเลือกบรรจุภรรฑ์ของผลิตภัณฑ์ที่สร้างขึ้นในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="b77ee-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="b77ee-145">ในฟิลด์ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b77ee-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="b77ee-146">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b77ee-146">Click Create.</span></span>
18. <span data-ttu-id="b77ee-147">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b77ee-147">Click Save.</span></span>

