---
title: สร้างผลิตภัณฑ์หลัก
description: 'สร้างผลิตภัณฑ์หลักสำหรับตัวแปรที่กำหนดไว้ล่วงหน้า '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e34f7c630e872468d888938e0f1aa57f3f0d4c4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570017"
---
# <a name="create-a-product-master"></a><span data-ttu-id="343f6-103">สร้างผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="343f6-103">Create a product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="343f6-104">สร้างผลิตภัณฑ์หลักสำหรับตัวแปรที่กำหนดไว้ล่วงหน้า </span><span class="sxs-lookup"><span data-stu-id="343f6-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="343f6-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="343f6-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="343f6-106">กระบวนงานนี้มีไว้สำหรับผู้ออกแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="343f6-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="343f6-107">สร้างผลิตภัณฑ์หลักใหม่</span><span class="sxs-lookup"><span data-stu-id="343f6-107">Create a new product master</span></span>
1. <span data-ttu-id="343f6-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์หลัก </span><span class="sxs-lookup"><span data-stu-id="343f6-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="343f6-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="343f6-109">Click New.</span></span>
3. <span data-ttu-id="343f6-110">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="343f6-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="343f6-111">หมายเลขต้องไม่ซ้ำกัน </span><span class="sxs-lookup"><span data-stu-id="343f6-111">The number must be unique.</span></span> <span data-ttu-id="343f6-112">สามารถตั้งลำดับหมายเลขสำหรับฟิลด์หมายเลขผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="343f6-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="343f6-113">ในกรณีนี้ผู้ใช้ไม่ต้องป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="343f6-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="343f6-114">ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="343f6-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="343f6-115">ป้อนชื่อที่เป็นคำอธิบายผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="343f6-115">Enter a descriptive product name.</span></span> <span data-ttu-id="343f6-116">ค่าเป็นค่าเริ่มต้นชื่อค้นหา แต่สามารถเปลี่ยนแปลงได้โดยผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="343f6-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="343f6-117">ในฟิลด์กลุ่มมิติของผลิตภัณฑ์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="343f6-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="343f6-118">กลุ่มมิติของผลิตภัณฑ์ที่เป็น 4 มิติของผลิตภัณฑ์สามารถใช้เพื่อสร้างผลิตภัณฑ์ย่อย </span><span class="sxs-lookup"><span data-stu-id="343f6-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="343f6-119">ตัวอย่างนี้ใช้กับกลุ่มสีและขนาด</span><span class="sxs-lookup"><span data-stu-id="343f6-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="343f6-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="343f6-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="343f6-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="343f6-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="343f6-122">เทคโนโลยีการตั้งค่าคอนฟิกเริ่มต้นเป็นตัวแปรย่อยที่กำหนดไว้ล่วงหน้า </span><span class="sxs-lookup"><span data-stu-id="343f6-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="343f6-123">ซึ่งจะใช้สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="343f6-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="343f6-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="343f6-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="343f6-125">เลือกกลุ่มมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="343f6-125">Select product dimension groups</span></span>
1. <span data-ttu-id="343f6-126">ในฟิลด์กลุ่มสี ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="343f6-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="343f6-127">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="343f6-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="343f6-128">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="343f6-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="343f6-129">ในฟิลด์กลุ่มขนาด ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="343f6-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="343f6-130">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="343f6-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="343f6-131">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="343f6-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="343f6-132">เพิ่มกลุ่มมิติ</span><span class="sxs-lookup"><span data-stu-id="343f6-132">Add dimension groups</span></span>
1. <span data-ttu-id="343f6-133">ในบานหน้าต่างการดำเนินการ คลิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="343f6-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="343f6-134">คลิกกลุ่มมิติเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="343f6-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="343f6-135">ในฟิลด์กลุ่มมิติการจัดเก็บ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="343f6-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="343f6-136">มิติการจัดเก็บช่วยให้คุณสามารถควบคุมวิธีการจัดเก็บสินค้า และนำสินค้าออกจากคลัง </span><span class="sxs-lookup"><span data-stu-id="343f6-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="343f6-137">ตัวอย่างเช่น มิติการจัดเก็บสามารถรวมไซต์และคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="343f6-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="343f6-138">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="343f6-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="343f6-139">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="343f6-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="343f6-140">ในฟิลก์กลุ่มมิติการติดตาม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="343f6-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="343f6-141">กลุ่มมิติการติดตามกำหนดว่ามิติการติดตามใดที่คุณสามารถเพิ่มลงในผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="343f6-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="343f6-142">ตัวอย่างเช่น หมายเลขชุดงานและหมายเลขประจำสินค้าสามารถใช้เพื่อติดตามสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="343f6-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="343f6-143">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="343f6-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="343f6-144">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="343f6-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="343f6-145">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="343f6-145">Click OK.</span></span>
10. <span data-ttu-id="343f6-146">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="343f6-146">Click Save.</span></span>
11. <span data-ttu-id="343f6-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="343f6-147">Close the page.</span></span>

