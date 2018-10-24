--- 
title: "สร้างผลิตภัณฑ์สำเร็จรูป (กุมภาพันธ์ 2016)"
description: "งานนี้มุ่งเน้นการสร้างผลิตภัณฑ์สำเร็จรูป"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 44b3bf17c69f37e7a96c75345a3e4f27ba9eab50
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-finished-product-february-2016"></a><span data-ttu-id="e40e1-103">สร้างผลิตภัณฑ์สำเร็จรูป (กุมภาพันธ์ 2016)</span><span class="sxs-lookup"><span data-stu-id="e40e1-103">Create a finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e40e1-104">งานนี้มุ่งเน้นการสร้างผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="e40e1-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="e40e1-105">นี่คืองานแรกในลำดับการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="e40e1-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="e40e1-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="e40e1-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="e40e1-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="e40e1-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="e40e1-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e40e1-108">Click New.</span></span>
3. <span data-ttu-id="e40e1-109">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e40e1-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e40e1-110">สำหรับการสาธิต ให้พิมพ์ BOM_1</span><span class="sxs-lookup"><span data-stu-id="e40e1-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="e40e1-111">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e40e1-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e40e1-112">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="e40e1-112">Select STD.</span></span> <span data-ttu-id="e40e1-113">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e40e1-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="e40e1-114">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e40e1-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e40e1-115">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="e40e1-115">For example, select Audio.</span></span> <span data-ttu-id="e40e1-116">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e40e1-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="e40e1-117">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e40e1-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e40e1-118">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="e40e1-118">Select SiteWH.</span></span> <span data-ttu-id="e40e1-119">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับการสาธิต</span><span class="sxs-lookup"><span data-stu-id="e40e1-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="e40e1-120">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e40e1-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e40e1-121">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้ เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="e40e1-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="e40e1-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e40e1-122">Click OK.</span></span>
9. <span data-ttu-id="e40e1-123">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e40e1-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="e40e1-124">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e40e1-124">Click Default order settings.</span></span>
11. <span data-ttu-id="e40e1-125">ในฟิลด์ชนิดใบสั่งเริ่มต้น ให้เลือก 'การผลิต'</span><span class="sxs-lookup"><span data-stu-id="e40e1-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="e40e1-126">เนื่องจากเป็นผลิตภัณฑ์สำเร็จรูปที่จะผลิต เลือก การผลิต</span><span class="sxs-lookup"><span data-stu-id="e40e1-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="e40e1-127">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e40e1-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e40e1-128">สำหรับการสาธิต เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="e40e1-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="e40e1-129">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e40e1-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e40e1-130">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="e40e1-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="e40e1-131">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e40e1-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e40e1-132">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="e40e1-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="e40e1-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e40e1-133">Close the page.</span></span>


