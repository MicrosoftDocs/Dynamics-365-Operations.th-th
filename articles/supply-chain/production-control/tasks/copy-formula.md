--- 
title: "คัดลอกสูตร"
description: "ขั้นตอนนี้มุ่งเน้นการสร้างสูตรที่รวมส่วนผสมเดียวกับสูตรที่มีอยู่ แต่ มีความแตกต่างเล็กน้อย "
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 036bd9f592ca584afad9d4b9b7a49a9787076056
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="copy-a-formula"></a><span data-ttu-id="f7336-103">คัดลอกสูตร</span><span class="sxs-lookup"><span data-stu-id="f7336-103">Copy a formula</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7336-104">ขั้นตอนนี้มุ่งเน้นการสร้างสูตรที่รวมส่วนผสมเดียวกับสูตรที่มีอยู่ แต่ มีความแตกต่างเล็กน้อย </span><span class="sxs-lookup"><span data-stu-id="f7336-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="f7336-105">เมื่อต้องการสร้างบรรทัดสูตร คุณสามารถใช้ฟังก์ชั่นคัดลอกเพื่อคัดลอกสูตรที่มีอยู่แล้วซึ่งส่วนใหญ่จะเป็นส่วนผสมที่คุณต้องการ </span><span class="sxs-lookup"><span data-stu-id="f7336-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="f7336-106">จากนั้นคุณสามารถเปลี่ยนแปลงใดๆก็ได้กับแต่ละบรรทัดในเวอร์ชันใหม่ </span><span class="sxs-lookup"><span data-stu-id="f7336-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="f7336-107">โดยการใช้ฟังก์ชั่นคัดลอก คุณไม่ต้องสร้างหลายสูตรที่ค่อนข้างจะเหมือนกัน </span><span class="sxs-lookup"><span data-stu-id="f7336-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="f7336-108">บริษัทข้อมูลสาธิตที่เคยสร้างงานนี้คือ USP2</span><span class="sxs-lookup"><span data-stu-id="f7336-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="f7336-109">สร้างสูตร</span><span class="sxs-lookup"><span data-stu-id="f7336-109">Create a formula</span></span>
1. <span data-ttu-id="f7336-110">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > สูตรการผลิตและสูตร > สูตร</span><span class="sxs-lookup"><span data-stu-id="f7336-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="f7336-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f7336-111">Click New.</span></span>
3. <span data-ttu-id="f7336-112">ในฟิลด์สูตร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f7336-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="f7336-113">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="f7336-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f7336-114">พิมพ์ชื่อที่มีความหมายสำหรับสูตร</span><span class="sxs-lookup"><span data-stu-id="f7336-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="f7336-115">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f7336-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f7336-116">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7336-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f7336-117">ในฟิลด์กลุ่มสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f7336-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f7336-118">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f7336-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f7336-119">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7336-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="f7336-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f7336-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="f7336-121">คัดลอกบรรทัดสูตร</span><span class="sxs-lookup"><span data-stu-id="f7336-121">Copy formula lines</span></span>
1. <span data-ttu-id="f7336-122">ในบานหน้าต่างการดำเนินการ คลิกสูตร</span><span class="sxs-lookup"><span data-stu-id="f7336-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="f7336-123">คลิก คัดลอก</span><span class="sxs-lookup"><span data-stu-id="f7336-123">Click Copy.</span></span>
3. <span data-ttu-id="f7336-124">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f7336-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f7336-125">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7336-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f7336-126">ในฟิลด์เวอร์ชั่นสูตตร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f7336-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f7336-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7336-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f7336-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f7336-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="f7336-129">ปรับปรุงบรรทัดสูตรที่คัดลอก</span><span class="sxs-lookup"><span data-stu-id="f7336-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="f7336-130">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7336-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="f7336-131">คลิก ลบ</span><span class="sxs-lookup"><span data-stu-id="f7336-131">Click Delete.</span></span>
3. <span data-ttu-id="f7336-132">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="f7336-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="f7336-133">อนุมัติสูตร</span><span class="sxs-lookup"><span data-stu-id="f7336-133">Approve formula</span></span>
1. <span data-ttu-id="f7336-134">ในบานหน้าต่างการดำเนินการ คลิกสูตร</span><span class="sxs-lookup"><span data-stu-id="f7336-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="f7336-135">คลิกอนุมัติสูตร</span><span class="sxs-lookup"><span data-stu-id="f7336-135">Click Approve formula.</span></span>
3. <span data-ttu-id="f7336-136">ในฟิลด์อนุมัติโดย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="f7336-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f7336-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7336-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f7336-138">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="f7336-138">Click Select.</span></span>
6. <span data-ttu-id="f7336-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f7336-139">Click OK.</span></span>


