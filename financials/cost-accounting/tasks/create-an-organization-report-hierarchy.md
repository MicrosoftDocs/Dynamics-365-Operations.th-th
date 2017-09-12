--- 
title: "สร้างลำดับชั้นรายงานขององค์กร"
description: "ใช้กระบวนงานนี้เพื่อสร้างลำดับชั้นรายงานสำหรับการรายงานขององค์กร"
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f593c59660abcf5b0d5771ddd9daced6ec5fbfb4
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="6c9df-103">สร้างลำดับชั้นรายงานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="6c9df-103">Create an organization report hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c9df-104">ใช้กระบวนงานนี้เพื่อสร้างลำดับชั้นรายงานสำหรับการรายงานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="6c9df-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="6c9df-105">วัตถุประสงค์ของการบันทึกนี้คือเพื่อแนะนำคุณเกี่ยวกับลำดับชั้นมิติเพื่อให้คุณสามารถดำเนินการต่อไปจนกว่าจะมีการสร้างโครงสร้างการรายงานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="6c9df-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="6c9df-106">การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USP2</span><span class="sxs-lookup"><span data-stu-id="6c9df-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="6c9df-107">ไปที่ การบัญชีต้นทุน > มิติ > ลำดับชั้นของมิติ</span><span class="sxs-lookup"><span data-stu-id="6c9df-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="6c9df-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-108">Click New.</span></span>
3. <span data-ttu-id="6c9df-109">ในฟิลด์ HierarchyTypeComboBox เลือก 'ลำดับชั้นการจัดประเภทมิติ'</span><span class="sxs-lookup"><span data-stu-id="6c9df-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="6c9df-110">เลือกลำดับชั้นการจัดประเภทมิติ</span><span class="sxs-lookup"><span data-stu-id="6c9df-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="6c9df-111">ชนิด ลำดับชั้นของการจัดประเภทของมิติ ถูกใช้ในการกำหนดกฎและสำหรับวัตถุประสงค์ในการรายงาน</span><span class="sxs-lookup"><span data-stu-id="6c9df-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="6c9df-112">ซึ่งสนับสนุนมิติทั้งหมด เช่น วัตถุต้นทุน องค์ประกอบต้นทุน และมิติทางสถิติ</span><span class="sxs-lookup"><span data-stu-id="6c9df-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="6c9df-113">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-113">Click Create.</span></span>
5. <span data-ttu-id="6c9df-114">ในฟิลด์ชื่อลำดับชั้นมิติ ให้พิมพ์ 'องค์กร USP2'</span><span class="sxs-lookup"><span data-stu-id="6c9df-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="6c9df-115">ในฟิลด์มิติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6c9df-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="6c9df-116">เลือกศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c9df-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="6c9df-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-117">Click Save.</span></span>
8. <span data-ttu-id="6c9df-118">คลิกดูลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="6c9df-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="6c9df-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-119">Click New.</span></span>
10. <span data-ttu-id="6c9df-120">ในฟิลด์ชื่อโหนด ให้พิมพ์ 'CEO'</span><span class="sxs-lookup"><span data-stu-id="6c9df-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="6c9df-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-121">Click Save.</span></span>
12. <span data-ttu-id="6c9df-122">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-122">Click New.</span></span>
13. <span data-ttu-id="6c9df-123">ในฟิลด์ชื่อโหนด ให้พิมพ์ 'CEO'</span><span class="sxs-lookup"><span data-stu-id="6c9df-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="6c9df-124">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-124">Click Save.</span></span>
15. <span data-ttu-id="6c9df-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-125">Click New.</span></span>
16. <span data-ttu-id="6c9df-126">ในฟิลด์ชื่อโหนด ให้พิมพ์ 'ภูมิภาคตะวันออก'</span><span class="sxs-lookup"><span data-stu-id="6c9df-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="6c9df-127">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-127">Click Save.</span></span>
18. <span data-ttu-id="6c9df-128">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-128">Click New.</span></span>
19. <span data-ttu-id="6c9df-129">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6c9df-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="6c9df-130">ในฟิลด์สมาชิกมิติเริ่มต้น ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6c9df-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6c9df-131">เลือกสมาชิกมิติที่สอดคล้องกับโหนด</span><span class="sxs-lookup"><span data-stu-id="6c9df-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="6c9df-132">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-132">Click Save.</span></span>
22. <span data-ttu-id="6c9df-133">ในแผนภูมิ เลือก 'ศูนย์ต้นทุนขององค์กร USP2\CEO\CEO'</span><span class="sxs-lookup"><span data-stu-id="6c9df-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="6c9df-134">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-134">Click New.</span></span>
24. <span data-ttu-id="6c9df-135">ในฟิลด์ชื่อโหนด ให้พิมพ์ 'ภูมิภาคตะวันตก'</span><span class="sxs-lookup"><span data-stu-id="6c9df-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="6c9df-136">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-136">Click Save.</span></span>
26. <span data-ttu-id="6c9df-137">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-137">Click New.</span></span>
27. <span data-ttu-id="6c9df-138">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6c9df-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="6c9df-139">ในฟิลด์สมาชิกมิติเริ่มต้น ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6c9df-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6c9df-140">เลือกสมาชิกมิติที่สอดคล้องกับโหนด</span><span class="sxs-lookup"><span data-stu-id="6c9df-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="6c9df-141">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-141">Click Save.</span></span>
30. <span data-ttu-id="6c9df-142">ในแผนภูมิ ให้เลือก 'องค์กร USP2\CEO'</span><span class="sxs-lookup"><span data-stu-id="6c9df-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="6c9df-143">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-143">Click New.</span></span>
32. <span data-ttu-id="6c9df-144">ในฟิลด์ชื่อโหนด ให้พิมพ์ 'CFO'</span><span class="sxs-lookup"><span data-stu-id="6c9df-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="6c9df-145">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-145">Click Save.</span></span>
34. <span data-ttu-id="6c9df-146">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-146">Click New.</span></span>
35. <span data-ttu-id="6c9df-147">ในฟิลด์ชื่อโหนด ให้พิมพ์ 'การส่งเสริมการขาย'</span><span class="sxs-lookup"><span data-stu-id="6c9df-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="6c9df-148">ในฟิลด์ชื่อโหนด ให้พิมพ์ 'การส่งเสริมการขาย'</span><span class="sxs-lookup"><span data-stu-id="6c9df-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="6c9df-149">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-149">Click Save.</span></span>
38. <span data-ttu-id="6c9df-150">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-150">Click New.</span></span>
39. <span data-ttu-id="6c9df-151">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6c9df-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="6c9df-152">ในฟิลด์สมาชิกมิติเริ่มต้น ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6c9df-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6c9df-153">เลือกสมาชิกมิติที่สอดคล้องกับโหนด</span><span class="sxs-lookup"><span data-stu-id="6c9df-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="6c9df-154">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-154">Click Save.</span></span>
42. <span data-ttu-id="6c9df-155">ในแผนภูมิ เลือก 'ศูนย์ต้นทุนขององค์กร USP2\CEO\CFO'</span><span class="sxs-lookup"><span data-stu-id="6c9df-155">In the tree, select 'Oganization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="6c9df-156">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-156">Click New.</span></span>
44. <span data-ttu-id="6c9df-157">ในฟิลด์ชื่อโหนด ให้พิมพ์ 'แสดงการค้า'</span><span class="sxs-lookup"><span data-stu-id="6c9df-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="6c9df-158">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-158">Click Save.</span></span>
46. <span data-ttu-id="6c9df-159">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-159">Click New.</span></span>
47. <span data-ttu-id="6c9df-160">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6c9df-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="6c9df-161">ในฟิลด์สมาชิกมิติเริ่มต้น ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6c9df-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6c9df-162">เลือกสมาชิกมิติที่สอดคล้องกับโหนด</span><span class="sxs-lookup"><span data-stu-id="6c9df-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="6c9df-163">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-163">Click Save.</span></span>
50. <span data-ttu-id="6c9df-164">ในแผนภูมิ ให้เลือก 'องค์กร USP2\CEO'</span><span class="sxs-lookup"><span data-stu-id="6c9df-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="6c9df-165">ในฟิลด์ชื่อโหนด ให้พิมพ์ 'CIO'</span><span class="sxs-lookup"><span data-stu-id="6c9df-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="6c9df-166">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-166">Click Save.</span></span>
53. <span data-ttu-id="6c9df-167">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-167">Click New.</span></span>
54. <span data-ttu-id="6c9df-168">ในฟิลด์ชื่อโหนด ให้พิมพ์ 'ศูนย์บริการ'</span><span class="sxs-lookup"><span data-stu-id="6c9df-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="6c9df-169">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-169">Click Save.</span></span>
56. <span data-ttu-id="6c9df-170">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6c9df-170">Click New.</span></span>
57. <span data-ttu-id="6c9df-171">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6c9df-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="6c9df-172">ในฟิลด์สมาชิกมิติเริ่มต้น ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6c9df-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6c9df-173">เลือกสมาชิกมิติที่สอดคล้องกับโหนด</span><span class="sxs-lookup"><span data-stu-id="6c9df-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="6c9df-174">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6c9df-174">Click Save.</span></span>


