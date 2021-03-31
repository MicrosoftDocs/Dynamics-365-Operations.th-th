---
title: สร้างผลิตภัณฑ์หลัก
description: 'สร้างผลิตภัณฑ์หลักสำหรับตัวแปรที่กำหนดไว้ล่วงหน้า '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d580d323409d84bab66dc03d39e084f5ee0cfc64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218500"
---
# <a name="create-a-product-master"></a><span data-ttu-id="26021-103">สร้างผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="26021-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="26021-104">สร้างผลิตภัณฑ์หลักสำหรับตัวแปรที่กำหนดไว้ล่วงหน้า </span><span class="sxs-lookup"><span data-stu-id="26021-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="26021-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="26021-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="26021-106">กระบวนงานนี้มีไว้สำหรับผู้ออกแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="26021-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="26021-107">สร้างผลิตภัณฑ์หลักใหม่</span><span class="sxs-lookup"><span data-stu-id="26021-107">Create a new product master</span></span>
1. <span data-ttu-id="26021-108">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="26021-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="26021-109">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="26021-109">Click **New**.</span></span>
3. <span data-ttu-id="26021-110">ในฟิลด์ **หมายเลขผลิตภัณฑ์** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="26021-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="26021-111">หมายเลขต้องไม่ซ้ำกัน </span><span class="sxs-lookup"><span data-stu-id="26021-111">The number must be unique.</span></span> <span data-ttu-id="26021-112">สามารถตั้งลำดับหมายเลขได้ในฟิลด์ **หมายเลขผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="26021-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="26021-113">ในกรณีนี้ผู้ใช้ไม่ต้องป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="26021-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="26021-114">ในฟิลด์ **ชื่อผลิตภัณฑ์** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="26021-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="26021-115">ป้อนชื่อที่เป็นคำอธิบายผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="26021-115">Enter a descriptive product name.</span></span> <span data-ttu-id="26021-116">ค่าเป็นค่าเริ่มต้นชื่อค้นหา แต่สามารถเปลี่ยนแปลงได้โดยผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="26021-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="26021-117">ในฟิลด์ **กลุ่มมิติของผลิตภัณฑ์** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="26021-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="26021-118">กลุ่มมิติของผลิตภัณฑ์ที่เป็น 4 มิติของผลิตภัณฑ์สามารถใช้เพื่อสร้างผลิตภัณฑ์ย่อย </span><span class="sxs-lookup"><span data-stu-id="26021-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="26021-119">ตัวอย่างนี้ใช้กับกลุ่มสีและขนาด</span><span class="sxs-lookup"><span data-stu-id="26021-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="26021-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="26021-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="26021-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="26021-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="26021-122">ค่าเริ่มต้นของ **เทคโนโลยีการตั้งค่าคอนฟิก** คือ 'ตัวแปรที่กำหนดไว้ล่วงหน้า'</span><span class="sxs-lookup"><span data-stu-id="26021-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="26021-123">ซึ่งจะใช้สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="26021-123">This will be used for this example.</span></span>
8. <span data-ttu-id="26021-124">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="26021-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="26021-125">เลือกกลุ่มมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="26021-125">Select product dimension groups</span></span>
1. <span data-ttu-id="26021-126">ในฟิลด์ **กลุ่มสี** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="26021-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="26021-127">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="26021-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="26021-128">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="26021-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="26021-129">ในฟิลด์ **กลุ่มขนาด** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="26021-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="26021-130">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="26021-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="26021-131">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="26021-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="26021-132">เพิ่มกลุ่มมิติ</span><span class="sxs-lookup"><span data-stu-id="26021-132">Add dimension groups</span></span>
1. <span data-ttu-id="26021-133">ใน **บานหน้าต่างการดำเนินการ** คลิก **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="26021-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="26021-134">ให้คลิก **กลุ่มมิติ** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="26021-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="26021-135">ในฟิลด์ **กลุ่มมิติการจัดเก็บ** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="26021-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="26021-136">มิติการจัดเก็บช่วยให้คุณสามารถควบคุมวิธีการจัดเก็บสินค้า และนำสินค้าออกจากคลัง </span><span class="sxs-lookup"><span data-stu-id="26021-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="26021-137">ตัวอย่างเช่น มิติการจัดเก็บสามารถรวมไซต์และคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="26021-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="26021-138">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="26021-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="26021-139">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="26021-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="26021-140">ในฟิลด์ **กลุ่มมิติการติดตาม** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="26021-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="26021-141">กลุ่มมิติการติดตามกำหนดว่ามิติการติดตามใดที่คุณสามารถเพิ่มลงในผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="26021-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="26021-142">ตัวอย่างเช่น หมายเลขชุดงานและหมายเลขประจำสินค้าสามารถใช้เพื่อติดตามสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="26021-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="26021-143">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="26021-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="26021-144">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="26021-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="26021-145">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="26021-145">Click **OK**.</span></span>
10. <span data-ttu-id="26021-146">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="26021-146">Click **Save**.</span></span>
11. <span data-ttu-id="26021-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="26021-147">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]