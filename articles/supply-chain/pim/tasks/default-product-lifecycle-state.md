---
title: สร้างสถานะรอบการขายของผลิตภัณฑ์ค่าเริ่มต้น
description: กระบวนงานนี้แสดงวิธีการสร้างสถานะวงจรชีวิตผลิตภัณฑ์เริ่มต้น รวมทั้งวิธีการเชื่อมโยงสถานะเริ่มต้นกับผลิตภัณฑ์ที่นำออกใช้ด้วย
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e7e637157ee06a3d07a1a9c5da71295eb75b424
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564189"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="bb890-103">สร้างสถานะรอบการขายของผลิตภัณฑ์ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bb890-103">Create a default product lifecycle state</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb890-104">กระบวนงานนี้แสดงวิธีการสร้างสถานะวงจรชีวิตผลิตภัณฑ์เริ่มต้น รวมทั้งวิธีการเชื่อมโยงสถานะเริ่มต้นกับผลิตภัณฑ์ที่นำออกใช้ด้วย</span><span class="sxs-lookup"><span data-stu-id="bb890-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="bb890-105">สร้างสถานะรอบการขายค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bb890-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="bb890-106">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การตั้งค่า > สถานะรอบการขายของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bb890-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="bb890-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="bb890-107">Click New.</span></span>
3. <span data-ttu-id="bb890-108">ในฟิลด์สถานะ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bb890-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="bb890-109">เลือก ใช่ ในค่าเริ่มต้น เมื่อนำออกใช้กับฟิลด์นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="bb890-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="bb890-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bb890-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="bb890-111">เลือก ไม่ ในฟิลด์ ใช้งานอยู่สำหรับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="bb890-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="bb890-112">ถ้าไม่ควรรวมผลิตภัณฑ์ที่นำออกใช้ใหม่ในการวางแผนหลัก เลือก ไม่</span><span class="sxs-lookup"><span data-stu-id="bb890-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="bb890-113">ถ้าควรรวมอยู่ในการวางแผนหลัก ปล่อยตัวควบคุมที่ค่าเริ่มต้น ใช่</span><span class="sxs-lookup"><span data-stu-id="bb890-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="bb890-114">สร้างผลิตภัณฑ์ที่นำออกใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="bb890-114">Create a new released product</span></span>
1. <span data-ttu-id="bb890-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bb890-115">Close the page.</span></span>
2. <span data-ttu-id="bb890-116">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="bb890-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="bb890-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="bb890-117">Click New.</span></span>
4. <span data-ttu-id="bb890-118">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bb890-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="bb890-119">ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bb890-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="bb890-120">ในฟิลด์ชื่อสำหรับค้นหา ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bb890-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="bb890-121">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="bb890-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="bb890-122">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bb890-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="bb890-123">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="bb890-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="bb890-124">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="bb890-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="bb890-125">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bb890-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="bb890-126">สถานะวงจรชีวิตของผลิตภัณฑ์เริ่มต้นคือ คำนิยามสากล</span><span class="sxs-lookup"><span data-stu-id="bb890-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="bb890-127">เปลี่ยนผลิตภัณฑ์เป็นสถานะที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="bb890-127">Change the product to an active state</span></span>
1. <span data-ttu-id="bb890-128">ในฟิลด์สถานะรอบการขายของผลิตภัณฑ์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="bb890-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="bb890-129">สมมติว่า คุณได้ตั้งค่าสถานะที่ใช้งานอยู่ ขณะนี้คุณสามารถเลือกสถานะที่ใช้งานอยู่เพื่ออนุญาตให้มีการใช้ผลิตภัณฑ์ในการคำนวณระดับ BOM และการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="bb890-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="bb890-130">เห็นได้ชัดว่า ควรใช้รายการนี้ก็ต่อเมื่อรายละเอียดผลิตภัณฑ์ทั้งหมดที่จำเป็นสำหรับการวางแผนถูกระบุเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="bb890-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  

