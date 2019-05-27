---
title: กำหนดนโยบายการตรวจสอบสำหรับเอกสารต้นทาง
description: 'กระบวนงานนี้แสดงวิธีตั้งค่าและดำเนินการกฎนโยบายการตรวจสอบ '
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a82c3e8e8787beb309b75b73cda36f4ca8031d6f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558894"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="4416f-103">กำหนดนโยบายการตรวจสอบสำหรับเอกสารต้นทาง</span><span class="sxs-lookup"><span data-stu-id="4416f-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4416f-104">กระบวนงานนี้แสดงวิธีตั้งค่าและดำเนินการกฎนโยบายการตรวจสอบ </span><span class="sxs-lookup"><span data-stu-id="4416f-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="4416f-105">ตัวอย่างได้ใช้รายงานค่าใช้จ่ายที่มีชนิดค่าใช้จ่ายโรงแรม </span><span class="sxs-lookup"><span data-stu-id="4416f-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="4416f-106">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="4416f-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="4416f-107">บทบาทผู้ตรวจสอบบัญชีประกอบด้วยสิทธิ์ที่ถูกต้องเพื่อการดำเนินการงานเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="4416f-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="4416f-108">ไปที่เวิร์กเบนช์การตรวจสอบ > การตั้งค่า > ประเภทกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="4416f-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="4416f-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4416f-109">Click New.</span></span>
3. <span data-ttu-id="4416f-110">ในฟิลด์ชื่อกฎ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4416f-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="4416f-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4416f-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4416f-112">ในฟิลด์ชื่อการสอบถาม ให้เลือกรายการรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4416f-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="4416f-113">ในฟิลด์ชนิดการสอบถาม ให้เลือกการรวม</span><span class="sxs-lookup"><span data-stu-id="4416f-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="4416f-114">ในฟิลด์นิติบุคคล ให้เลือกนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="4416f-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="4416f-115">ในฟิลด์การอ้างอิงวันที่เอกสาร ให้เลือกวันและเวลาที่แก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="4416f-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="4416f-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4416f-116">Click Save.</span></span>
10. <span data-ttu-id="4416f-117">ไปที่เวิร์กเบนช์การตรวจสอบ > การตั้งค่า > การตรวจสอบนโยบาย</span><span class="sxs-lookup"><span data-stu-id="4416f-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="4416f-118">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4416f-118">Click New.</span></span>
12. <span data-ttu-id="4416f-119">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="4416f-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="4416f-120">ขยายส่วนของนโยบายองค์กร</span><span class="sxs-lookup"><span data-stu-id="4416f-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="4416f-121">ในแผนภูมิ เลือก 'ระบบความบันเทิง Contoso USA'</span><span class="sxs-lookup"><span data-stu-id="4416f-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="4416f-122">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4416f-122">Click Add.</span></span>
16. <span data-ttu-id="4416f-123">ในแผนภูมิ เลือก 'การให้คำปรึกษา Contoso USA'</span><span class="sxs-lookup"><span data-stu-id="4416f-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="4416f-124">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4416f-124">Click Add.</span></span>
18. <span data-ttu-id="4416f-125">ในแผนภูมิ เลือก 'การขายปลีก Contoso USA'</span><span class="sxs-lookup"><span data-stu-id="4416f-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="4416f-126">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4416f-126">Click Add.</span></span>
20. <span data-ttu-id="4416f-127">ยุบส่วนของนโยบายองค์กร</span><span class="sxs-lookup"><span data-stu-id="4416f-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="4416f-128">ขยายส่วนของนโยบายองค์กร</span><span class="sxs-lookup"><span data-stu-id="4416f-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="4416f-129">ในรายการ ค้นหาและเลือกกฎนโยบายที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="4416f-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="4416f-130">คลิกสร้างกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="4416f-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="4416f-131">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="4416f-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="4416f-132">คลิกที่ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4416f-132">Click Filter.</span></span>
26. <span data-ttu-id="4416f-133">ในรายการ เลือกแถวสำหรับประเภทค่าใช้จ่ายและตั้งค่ารายละเอียดให้กับโรงแรม</span><span class="sxs-lookup"><span data-stu-id="4416f-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="4416f-134">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4416f-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="4416f-135">คลิกที่แท็บรวม</span><span class="sxs-lookup"><span data-stu-id="4416f-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="4416f-136">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4416f-136">Click Add.</span></span>
30. <span data-ttu-id="4416f-137">ในรายการ ให้เลือกค่าฟิลด์ของยอดเงินธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="4416f-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="4416f-138">ในฟิลด์ฟิลด์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4416f-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="4416f-139">ในฟิลด์ฟังก์ชันการรวม ให้เลือก 'ผลรวม'</span><span class="sxs-lookup"><span data-stu-id="4416f-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="4416f-140">คลิกที่แท็บจัดกลุ่มตาม</span><span class="sxs-lookup"><span data-stu-id="4416f-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="4416f-141">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4416f-141">Click Add.</span></span>
35. <span data-ttu-id="4416f-142">ในรายการ ให้เลือกค่าของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="4416f-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="4416f-143">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4416f-143">Click Add.</span></span>
37. <span data-ttu-id="4416f-144">ในรายการ ให้เลือกค่าของประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4416f-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="4416f-145">ในฟิลด์ฟิลด์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4416f-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="4416f-146">คลิกแท็บที่มี</span><span class="sxs-lookup"><span data-stu-id="4416f-146">Click the Having tab.</span></span>
40. <span data-ttu-id="4416f-147">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4416f-147">Click Add.</span></span>
41. <span data-ttu-id="4416f-148">เลือกยอดเงินธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="4416f-148">Select Transaction amount</span></span>
42. <span data-ttu-id="4416f-149">ในฟิลด์ฟิลด์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4416f-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="4416f-150">ในฟิลด์ฟังก์ชันการรวม ให้เลือก 'ผลรวม'</span><span class="sxs-lookup"><span data-stu-id="4416f-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="4416f-151">ในฟิลด์เงื่อนไข ให้พิมพ์ '>2000'</span><span class="sxs-lookup"><span data-stu-id="4416f-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="4416f-152">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4416f-152">Click OK.</span></span>
46. <span data-ttu-id="4416f-153">คลิก ทดสอบ </span><span class="sxs-lookup"><span data-stu-id="4416f-153">Click Test.</span></span>
47. <span data-ttu-id="4416f-154">ในฟิลด์วันที่เริ่มต้นของการเลือกเอกสาร ให้เลือกวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="4416f-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="4416f-155">ในฟิลด์วันที่สิ้นสุดของการเลือกเอกสาร ให้เลือกวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="4416f-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="4416f-156">คลิกที่ดำเนินการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="4416f-156">Click Run test.</span></span>
50. <span data-ttu-id="4416f-157">ในบานหน้าต่างการดำเนินการ คลิกนโยบายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="4416f-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="4416f-158">คลิกที่ตัวเลือกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4416f-158">Click Additional options.</span></span>
52. <span data-ttu-id="4416f-159">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="4416f-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="4416f-160">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="4416f-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="4416f-161">คลิกชุดงาน</span><span class="sxs-lookup"><span data-stu-id="4416f-161">Click Batch.</span></span>
55. <span data-ttu-id="4416f-162">ขยายการดำเนินงานในส่วนเบื้องหลัง</span><span class="sxs-lookup"><span data-stu-id="4416f-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="4416f-163">เลือกใช่ในฟิลด์กระบวนการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="4416f-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="4416f-164">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4416f-164">Click OK.</span></span>
58. <span data-ttu-id="4416f-165">ไปที่เวิร์กเบนช์การตรวจสอบ > กรณีการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="4416f-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="4416f-166">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4416f-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="4416f-167">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4416f-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="4416f-168">ขยายส่วนของความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="4416f-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="4416f-169">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4416f-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="4416f-170">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4416f-170">In the list, click the link in the selected row.</span></span>

