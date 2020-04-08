---
title: คำนวณ BOM โดยใช้โครงสร้างหลายระดับ (กุมภาพันธ์ 2016)
description: กระบวนงานนี้แสดงวิธีการคำนวณต้นทุนของผลิตภัณฑ์สำเร็จรูปโดยใช้การกระจายหลายระดับจากในแผ่นงานการคิดต้นทุน
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c35d2b2d5c0fdd14c7e0a35316d482b2e3ffb49
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150495"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="4d6e2-103">คำนวณ BOM โดยใช้โครงสร้างหลายระดับ (กุมภาพันธ์ 2016)</span><span class="sxs-lookup"><span data-stu-id="4d6e2-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d6e2-104">กระบวนงานนี้แสดงวิธีการคำนวณต้นทุนของผลิตภัณฑ์สำเร็จรูปโดยใช้การกระจายหลายระดับจากในแผ่นงานการคิดต้นทุน</span><span class="sxs-lookup"><span data-stu-id="4d6e2-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="4d6e2-105">นี่คืองานที่เจ็ดในลำดับการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="4d6e2-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="4d6e2-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="4d6e2-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="4d6e2-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="4d6e2-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="4d6e2-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4d6e2-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4d6e2-109">เลือก ผลิตภัณฑ์ BOM_1</span><span class="sxs-lookup"><span data-stu-id="4d6e2-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="4d6e2-110">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="4d6e2-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="4d6e2-111">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="4d6e2-111">Click Item price.</span></span>
5. <span data-ttu-id="4d6e2-112">คลิก คำนวณต้นทุนสินค้า</span><span class="sxs-lookup"><span data-stu-id="4d6e2-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="4d6e2-113">คุณอาจต้องคลิกจุดไข่ปลา (...) เพื่อดูตัวเลือกนี้ในเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="4d6e2-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="4d6e2-114">ในฟิลด์เวอร์ชันการคิดต้นทุน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4d6e2-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="4d6e2-115">เลือกเวอร์ชันการคิดต้นทุน 20 เนื่องจากเป็นชนิดต้นทุนที่วางแผนไว้ และโหมดการกระจายเป็นหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="4d6e2-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="4d6e2-116">โหมดการกระจายหลายระดับมีไว้สำหรับการจำลองและต้นทุนที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="4d6e2-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="4d6e2-117">ไม่ได้ใช้สำหรับต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="4d6e2-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="4d6e2-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4d6e2-118">Click OK.</span></span>
8. <span data-ttu-id="4d6e2-119">คลิกดูรายละเอียดการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="4d6e2-119">Click View calculation details.</span></span>
    * <span data-ttu-id="4d6e2-120">คุณอาจต้องคลิกจุดไข่ปลา (...) เพื่อดูตัวเลือกนี้ในเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="4d6e2-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="4d6e2-121">ในกรณีนี้ ให้สังเกตว่า BOM_2 ถูกคำนวณโดยพิจารณาวัตถุดิบ กระบวนการ และโสหุ้ยที่มีผลรวมเป็น 29,40 แทนต้นทุนมาตรฐาน 10 ที่ถูกเรียกใช้ในคู่มืองานแรกเริ่มในชุดนี้</span><span class="sxs-lookup"><span data-stu-id="4d6e2-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="4d6e2-122">คลิกแท็บแผ่นงานการคิดต้นทุน</span><span class="sxs-lookup"><span data-stu-id="4d6e2-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="4d6e2-123">เมื่อย้ายไปยังแท็บแผ่นงานการคิดต้นทุน ผลรวมต่อกลุ่มต้นทุนจะแตกต่างกันโดยเปรียบเทียบกับการคำนวณในคู่มืองานก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="4d6e2-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="4d6e2-124">ในฟิลด์ระดับ ให้เลือก 'หลายระดับ'</span><span class="sxs-lookup"><span data-stu-id="4d6e2-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="4d6e2-125">เมื่อเลือกหลายระดับ ต้นทุนจะถูกจัดประเภทตามส่วนประกอบของ BOM_2 ซึ่ง 10 ได้รับมาจากกลุ่มต้นทุน M1 (ITEM_C) และ 15,60 ได้รับมาจากการผลิตที่มีกลุ่มต้นทุนเป็น L2</span><span class="sxs-lookup"><span data-stu-id="4d6e2-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="4d6e2-126">ต้นทุนทางอ้อมจะแตกต่างกันไป</span><span class="sxs-lookup"><span data-stu-id="4d6e2-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="4d6e2-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4d6e2-127">Close the page.</span></span>
12. <span data-ttu-id="4d6e2-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4d6e2-128">Close the page.</span></span>

