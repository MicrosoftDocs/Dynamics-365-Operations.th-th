--- 
title: "รักษา BOM สำหรับแบบจำลองการจัดโครงแบบผลิตภัณฑ์"
description: "การดำเนินขั้นตอนนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่ "
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c017d7719ac6af43b0c8a162080bb753587df030
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="511c8-103">รักษา BOM สำหรับแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="511c8-103">Maintain BOM for a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="511c8-104">การดำเนินขั้นตอนนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="511c8-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="511c8-105">แบบจำลองลำโพงขีดขั้นสูงในบริษัทสาธิต USMF จะใช้เพื่อสร้างกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="511c8-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="511c8-106">เพิมรายการ BOM</span><span class="sxs-lookup"><span data-stu-id="511c8-106">Add a BOM line</span></span>
1. <span data-ttu-id="511c8-107">คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="511c8-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="511c8-108">คลิก แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="511c8-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="511c8-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="511c8-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="511c8-110">เลือกลำโพงขั้นสูงสำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="511c8-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="511c8-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="511c8-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="511c8-112">ขยายส่วนรายการ BOM</span><span class="sxs-lookup"><span data-stu-id="511c8-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="511c8-113">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="511c8-113">Click Add.</span></span>
7. <span data-ttu-id="511c8-114">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="511c8-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="511c8-115">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="511c8-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="511c8-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="511c8-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="511c8-117">เพิ่มรายละเอียดรายการ BOM</span><span class="sxs-lookup"><span data-stu-id="511c8-117">Add BOM line details</span></span>
1. <span data-ttu-id="511c8-118">คลิกรายละเอียดรายการ BOM</span><span class="sxs-lookup"><span data-stu-id="511c8-118">Click BOM line details.</span></span>
2. <span data-ttu-id="511c8-119">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="511c8-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="511c8-120">ตัวอย่างเช่น คุณสามารถเลือกสินค้า M0055</span><span class="sxs-lookup"><span data-stu-id="511c8-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="511c8-121">สำหรับแต่ละคุณสมบัติของรายการ BOM คุณสามารถเลือกได้ว่าจะเป็นค่าคงที่หรือมีการแม็ปไปที่คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="511c8-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="511c8-122">เลือกการตั้งค่ากล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="511c8-122">Select the Set check box.</span></span>
4. <span data-ttu-id="511c8-123">เลือก ใช่ ในฟิลด์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="511c8-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="511c8-124">การตั้งค่าคุณสมบัติการคำนวณเป็น ใช่ ช่วยให้มั่นใจว่ารายการ BOM จะถูกรวมอยู่ในการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="511c8-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="511c8-125">คลิกแท็บ การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="511c8-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="511c8-126">เลือกการตั้งค่ากล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="511c8-126">Select the Set check box.</span></span>
7. <span data-ttu-id="511c8-127">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="511c8-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="511c8-128">ฟิลด์ปริมาณกำหนดจำนวนของสินค้าที่จะรวมอยู่ใน BOM </span><span class="sxs-lookup"><span data-stu-id="511c8-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="511c8-129">นี่อาจเป็นตัวเลือกที่ชัดเจนสำหรับการแม็ปคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="511c8-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="511c8-130">คลิกแท็บมิติ</span><span class="sxs-lookup"><span data-stu-id="511c8-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="511c8-131">ตรวจสอบถ้ามีมิติของผลิตภัณฑ์ใดๆมีการใช้งานอยู่ และดังนั้น ต้องมีค่าหรือคุณลักษณะที่กำหนดให้</span><span class="sxs-lookup"><span data-stu-id="511c8-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="511c8-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="511c8-132">Click OK.</span></span>


