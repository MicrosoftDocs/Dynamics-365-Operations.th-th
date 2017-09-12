--- 
title: "สร้างการจัดโครงแบบตามมิติ"
description: "กระบวนงานนี้แสดงวิธีการกำหนดการปรับเปลี่ยนสำหรับผลิตภัณฑ์ตามมิติ "
author: BibiSp
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 97c3f879ecae979803e22c7f4eb515f35f95c182
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="b32b3-103">สร้างการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="b32b3-103">Create dimension-based configurations</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b32b3-104">กระบวนงานนี้แสดงวิธีการกำหนดการปรับเปลี่ยนสำหรับผลิตภัณฑ์ตามมิติ </span><span class="sxs-lookup"><span data-stu-id="b32b3-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="b32b3-105">นี่คือกระบวนงานสุดท้ายในชุดที่อธิบายถึงวิธีการสร้างชุดงานสำหรับการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="b32b3-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="b32b3-106">การดำเนินการกระบวนงานนี้จะขึ้นอยู่กับข้อมูลที่สร้างขึ้นในการบันทึกเจ็ดรายการก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="b32b3-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="b32b3-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="b32b3-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="b32b3-108">หาผลิตภัณฑ์หลักตามมิติ</span><span class="sxs-lookup"><span data-stu-id="b32b3-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="b32b3-109">คลิก การบำรุงรักษาผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="b32b3-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="b32b3-110">คลิกผลิตภัณฑ์ต่างๆที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="b32b3-110">Click Released products.</span></span>
3. <span data-ttu-id="b32b3-111">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b32b3-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b32b3-112">เลือกผลิตภัณฑ์หลักตามมิติ ที่คุณสร้างขึ้นในการบันทึกแรกในลำดับงานของการบันทึก 8 รายการนี้</span><span class="sxs-lookup"><span data-stu-id="b32b3-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="b32b3-113">สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="b32b3-113">Create configurations</span></span>
1. <span data-ttu-id="b32b3-114">ในหน้าต่างการดำเนินการด้านวิศวกรรม คลิกรักษาโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="b32b3-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="b32b3-115">คลิกตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="b32b3-115">Click Configure.</span></span>
3. <span data-ttu-id="b32b3-116">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b32b3-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b32b3-117">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b32b3-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="b32b3-118">เลือกสินค้าใดๆของกลุ่มการปรับเปลี่ยนแรก</span><span class="sxs-lookup"><span data-stu-id="b32b3-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="b32b3-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b32b3-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="b32b3-120">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b32b3-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="b32b3-121">เลือกสินค้าใดๆจากกลุ่มการปรับเปลี่ยนที่สอง</span><span class="sxs-lookup"><span data-stu-id="b32b3-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="b32b3-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b32b3-122">Click OK.</span></span>
8. <span data-ttu-id="b32b3-123">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b32b3-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b32b3-124">ในฟิลด์การตั้งค่าคอนฟิก ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b32b3-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="b32b3-125">ป้อนชื่อของกลุ่มการปรับเปลี่ยนที่จะทำให้ง่ายต่อการระบุการปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="b32b3-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="b32b3-126">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b32b3-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b32b3-127">ป้อนคำอธิบายของการปรับเปลี่ยนเพื่ออธิบายส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="b32b3-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="b32b3-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b32b3-128">Click OK.</span></span>


