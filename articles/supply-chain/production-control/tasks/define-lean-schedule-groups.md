---
title: กำหนดกลุ่มกำหนดการแบบลีน
description: 'กลุ่มกำหนดการแบบ lean ถูกกำหนดเป็นกลุ่ม และแยกแยะผลิตภัณฑ์ในการจัดกำหนดการคัมบัง '
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0cb17c68abbc4979a65e33c50450be575df3d93
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836275"
---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="8b1f1-103">กำหนดกลุ่มกำหนดการแบบลีน</span><span class="sxs-lookup"><span data-stu-id="8b1f1-103">Define lean schedule groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b1f1-104">กลุ่มกำหนดการแบบ lean ถูกกำหนดเป็นกลุ่ม และแยกแยะผลิตภัณฑ์ในการจัดกำหนดการคัมบัง </span><span class="sxs-lookup"><span data-stu-id="8b1f1-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="8b1f1-105">การจัดกลุ่มสามารถทำให้เสร็จเป็นความสัมพันธ์ทั่วไปสำหรับแต่ละบริษัท หรือเฉพาะสำหรับเซลล์ทำงาน </span><span class="sxs-lookup"><span data-stu-id="8b1f1-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="8b1f1-106">แต่ละกลุ่มมีรหัสสีกำหนดให้สำหรับภาพที่บ่งชี้ในหน้ารายการการจัดกำหนดการคัมบัง </span><span class="sxs-lookup"><span data-stu-id="8b1f1-106">Each group has a color code assigned for visual indication in the kanban scheduling listpage.</span></span> <span data-ttu-id="8b1f1-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="8b1f1-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="8b1f1-108">กำหนดกลุ่มที่กำหนดการจัดการแบบ Lean</span><span class="sxs-lookup"><span data-stu-id="8b1f1-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="8b1f1-109">ไปที่ การจัดการข้อมูลผลิตภัณฑ์ > Lean Manufacturing > กลุ่มกำหนดการแบบ Lean</span><span class="sxs-lookup"><span data-stu-id="8b1f1-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="8b1f1-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="8b1f1-110">Click New.</span></span>
3. <span data-ttu-id="8b1f1-111">ในฟิลด์กลุ่มกำหนดการ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8b1f1-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="8b1f1-112">กลุ่มกำหนดการอาจกำหนดเป็นกลุ่มสากลหรือเฉพาะสำหรับเซลล์ทำงาน </span><span class="sxs-lookup"><span data-stu-id="8b1f1-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="8b1f1-113">ในตัวอย่างง่ายๆ นี้ เรากำหนดเป็นกลุ่มสากล และเซลล์ทำงานจะถูกรักษาไว้เป็นว่างเปล่า </span><span class="sxs-lookup"><span data-stu-id="8b1f1-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="8b1f1-114">การตั้งค่าของกลุ่มนี้นำไปใช้กับเซลล์ทำงานที่ไม่มีกลุ่มกำหนดการเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8b1f1-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="8b1f1-115">เลือกสีจากตัวเลือกสี</span><span class="sxs-lookup"><span data-stu-id="8b1f1-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="8b1f1-116">สีจะใช้เพื่อเน้นงานบนหน้ารายการกำหนดการคัมบังหรือบอร์ดกำหนดการคัมบัง</span><span class="sxs-lookup"><span data-stu-id="8b1f1-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="8b1f1-117">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8b1f1-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="8b1f1-118">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8b1f1-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="8b1f1-119">เชื่อมโยงผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8b1f1-119">Associate product</span></span>
1. <span data-ttu-id="8b1f1-120">เชื่อมโยงผลิตภัณฑ์เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8b1f1-120">Associate a specific product</span></span>
    * <span data-ttu-id="8b1f1-121">มีสองวิธีในการเชื่อมโยงผลิตภัณฑ์ไปยังกลุ่มกำหนดการแบบ lean เป็นผลิตภัณฑ์เฉพาะ (ชนิดความสัมพันธ์ของสินค้า =สินค้า) หรือ เป็นส่วนหนึ่งของคีย์การปันส่วนสินค้า (ชนิดความสัมพันธ์ของสินค้า =กลุ่ม)</span><span class="sxs-lookup"><span data-stu-id="8b1f1-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="8b1f1-122">ในฟิลด์ความสัมพันธ์สินค้า ให้เลือก สินค้า</span><span class="sxs-lookup"><span data-stu-id="8b1f1-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="8b1f1-123">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8b1f1-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="8b1f1-124">ในฟิลด์อัตราปริมาณที่สามารถประมวลผลได้ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="8b1f1-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="8b1f1-125">อัตราส่วนปริมาณที่สามารถประมวลผลได้เริ่มต้นคือ 1 ซึ่งหมายความว่าผลิตภัณฑ์ที่เกี่ยวข้องใช้กำลังการผลิตที่ระบุไว้เท่านั้นในกิจกรรมกระบวนการของขั้นตอนการผลิต </span><span class="sxs-lookup"><span data-stu-id="8b1f1-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activites of the production flows.</span></span> <span data-ttu-id="8b1f1-126">อัตราส่วนปริมาณที่สามารถประมวลผลได้ > 1 กำหนดปริมาณการใช้ทรัพยากรที่สูงกว่า อัตราปริมาณที่สามารถประมวลผลได้ < 1 กำหนดปริมาณการใช้ทรัพยากรที่ต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="8b1f1-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="8b1f1-127">อัตราส่วนจะใช้ในการคำนวณต้นทุนและในการคำนวณปริมาณการใช้วัสดุในงานคัมบัง</span><span class="sxs-lookup"><span data-stu-id="8b1f1-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="8b1f1-128">เชื่อมโยงคีย์การปันส่วนสินค้า</span><span class="sxs-lookup"><span data-stu-id="8b1f1-128">Associate item allocation key</span></span>
1. <span data-ttu-id="8b1f1-129">เชื่อมโยงคีย์การปันส่วนสินค้า</span><span class="sxs-lookup"><span data-stu-id="8b1f1-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="8b1f1-130">เพิ่มการเชื่อมโยงไปยังคีย์การปันส่วนสินค้าโดยใช้กลุ่มชนิดความสัมพันธ์ของสินค้า </span><span class="sxs-lookup"><span data-stu-id="8b1f1-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="8b1f1-131">โปรดทราบว่ากระบวนการนี้ คุณจำเป็นต้องใช้คีย์การปันส่วนของการคาดการณ์สินค้าที่กำหนดในข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="8b1f1-131">Note that for this process, you need a forecast item alllocation key defined in your data.</span></span>  
2. <span data-ttu-id="8b1f1-132">ในฟิลด์ความสัมพัทธ์สินค้า ให้เลือก กลุ่ม</span><span class="sxs-lookup"><span data-stu-id="8b1f1-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="8b1f1-133">ในฟิลด์คีย์การปันส่วนสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8b1f1-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8b1f1-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8b1f1-134">In the list, click the link in the selected row.</span></span>

