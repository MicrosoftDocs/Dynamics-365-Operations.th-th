--- 
title: "สร้างเอกสารการโอนย้ายสำหรับการโอนย้ายสินค้าคงคลังภายใน"
description: "กระบวนงานนี้แสดงวิธีการสร้างเอกสารการโอนย้ายสำหรับการย้ายสินค้าภายในบริษัท "
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 30e5f6ad184720d0e119f86fb703ed7211b27fab
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a><span data-ttu-id="b1821-103">สร้างเอกสารการโอนย้ายสำหรับการโอนย้ายสินค้าคงคลังภายใน</span><span class="sxs-lookup"><span data-stu-id="b1821-103">Generate a transfer document for an internal inventory transfer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1821-104">กระบวนงานนี้แสดงวิธีการสร้างเอกสารการโอนย้ายสำหรับการย้ายสินค้าภายในบริษัท </span><span class="sxs-lookup"><span data-stu-id="b1821-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="b1821-105">กระบวนงานนี้จะพร้อมใช้งานสำหรับนิติบุคคลที่มีที่อยู่หลักในลิทัวเนียเท่านั้น </span><span class="sxs-lookup"><span data-stu-id="b1821-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="b1821-106">กระบวนงานจะถูกสร้างขึ้นโดยใช้ข้อมูลบริษัทสาธิต DEMF ที่มีที่อยู่หลักในลิทัวเนีย </span><span class="sxs-lookup"><span data-stu-id="b1821-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="b1821-107">ก่อนที่คุณจะสามารถทำกระบวนงานนี้ให้เสร็จสมบูรณ์ คุณจะต้องดำเนินกระบวนงาน "ตั้งค่าเอกสารการโอนย้ายสำหรับการย้ายสินค้าภายในบริษัท" ให้เสร็จสมบูรณ์ก่อน </span><span class="sxs-lookup"><span data-stu-id="b1821-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="b1821-108">กระบวนงานนี้มีไว้สำหรับผู้จัดทำบัญชีสินค้าคงคลัง </span><span class="sxs-lookup"><span data-stu-id="b1821-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="b1821-109">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="b1821-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="b1821-110">สร้างใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="b1821-110">Create a transfer order</span></span>
1. <span data-ttu-id="b1821-111">ไปที่ การบริหารสินค้าคงคลัง > ใบสั่งขาเข้า > ใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="b1821-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="b1821-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b1821-112">Click New.</span></span>
3. <span data-ttu-id="b1821-113">ในฟิลด์จากคลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b1821-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="b1821-114">ในฟิลด์ไปยังคลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b1821-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="b1821-115">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b1821-115">Click Add.</span></span>
6. <span data-ttu-id="b1821-116">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b1821-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="b1821-117">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b1821-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="b1821-118">ป้อนรายละเอียดการขนส่งสำหรับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="b1821-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="b1821-119">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b1821-119">Click Save.</span></span>
2. <span data-ttu-id="b1821-120">ในบานหน้าต่างการดำเนินการ คลิก จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b1821-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="b1821-121">คลิก รายละเอียดการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="b1821-121">Click Transportation details.</span></span>
4. <span data-ttu-id="b1821-122">เลือก ใช่ ในฟิลด์ พิมพ์รายละเอียดการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="b1821-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="b1821-123">ในฟิลด์สินค้าที่ออก ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b1821-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="b1821-124">ในฟิลด์บรรจุภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b1821-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="b1821-125">ในฟิลด์ระดับความเสี่ยงของจำนวนงานในศูนย์การผลิต ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b1821-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="b1821-126">ในฟิลด์ด์ผู้ขนส่ง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b1821-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="b1821-127">ในฟิลด์แบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b1821-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="b1821-128">ในฟิลด์หมายเลขการลงทะเบียน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b1821-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="b1821-129">ในฟิลด์หมายเลขทะเบียนปิดท้าย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b1821-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="b1821-130">ในฟิลด์พนักงานขนส่ง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b1821-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="b1821-131">ในฟิลด์ชื่อพนักงานขนส่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b1821-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="b1821-132">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b1821-132">Click Save.</span></span>
15. <span data-ttu-id="b1821-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b1821-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="b1821-134">ดูบันทึกการจัดส่งสำหรับใบสั่งโอนย้ายที่ไม่ได้ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="b1821-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="b1821-135">คลิกบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b1821-135">Click Packing slip.</span></span>
2. <span data-ttu-id="b1821-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b1821-136">Click OK.</span></span>
3. <span data-ttu-id="b1821-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b1821-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="b1821-138">ดูบันทึกการจัดส่งสำหรับใบสั่งโอนย้ายที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="b1821-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="b1821-139">ในบานหน้าต่างการดำเนินการ คลิก ใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="b1821-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="b1821-140">ในบานหน้าต่างการดำเนินการ คลิก จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b1821-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="b1821-141">คลิก ใบสั่งโอนย้ายการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b1821-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="b1821-142">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="b1821-142">Click the General tab.</span></span>
5. <span data-ttu-id="b1821-143">ในฟิลด์อัพเดต ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="b1821-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="b1821-144">คลิกแท็บ ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="b1821-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="b1821-145">ในฟิลด์ บันทึกการจัดส่ง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b1821-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="b1821-146">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b1821-146">Click OK.</span></span>
9. <span data-ttu-id="b1821-147">ในบานหน้าต่างการดำเนินการ คลิก จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b1821-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="b1821-148">คลิกบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b1821-148">Click Packing slip.</span></span>
11. <span data-ttu-id="b1821-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b1821-149">Click OK.</span></span>


