---
title: กำหนดนโยบายการตรวจสอบสำหรับเอกสารต้นทาง
description: หัวข้อนี้อธิบายวิธีตั้งค่าและดำเนินการกฎนโยบายการตรวจสอบ
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62ebe3d6ba1208bd5f9a2082969b1960c413c152
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836972"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="a6c37-103">กำหนดนโยบายการตรวจสอบสำหรับเอกสารต้นทาง</span><span class="sxs-lookup"><span data-stu-id="a6c37-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6c37-104">หัวข้อนี้อธิบายวิธีตั้งค่าและดำเนินการกฎนโยบายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a6c37-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="a6c37-105">ตัวอย่างได้ใช้รายงานค่าใช้จ่ายที่มีชนิดค่าใช้จ่ายโรงแรม </span><span class="sxs-lookup"><span data-stu-id="a6c37-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="a6c37-106">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="a6c37-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="a6c37-107">บทบาทผู้ตรวจสอบบัญชีประกอบด้วยสิทธิ์ที่ถูกต้องเพื่อการดำเนินการงานเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a6c37-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="a6c37-108">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > เวิร์กเบนช์การตรวจสอบ > การตั้งค่า > ชนิดกฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="a6c37-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="a6c37-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="a6c37-109">Select **New**.</span></span>
3. <span data-ttu-id="a6c37-110">ในฟิลด์ **ชื่อกฎ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a6c37-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="a6c37-111">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a6c37-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="a6c37-112">ในฟิลด์ **ชื่อการสอบถาม** เลือก **รายการรายงานค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="a6c37-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="a6c37-113">ในฟิลด์ **ประเภทการสอบถาม** เลือก **รวม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="a6c37-114">ในฟิลด์ **นิติบุคคล** เลือก **นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="a6c37-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="a6c37-115">ในฟิลด์ **การอ้างอิงวันที่เอกสาร** เลือก **วันที่และเวลาที่แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="a6c37-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="a6c37-116">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a6c37-116">Select **Save**.</span></span>
10. <span data-ttu-id="a6c37-117">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > เวิร์กเบนช์การตรวจสอบ > การตั้งค่า > นโยบายการตรวจสอบบัญชี**</span><span class="sxs-lookup"><span data-stu-id="a6c37-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="a6c37-118">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="a6c37-118">Select **New**.</span></span>
12. <span data-ttu-id="a6c37-119">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a6c37-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="a6c37-120">ขยายส่วน **องค์กรนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="a6c37-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="a6c37-121">ในแผนภูมิ เลือก **Contoso Entertainment System USA** จากนั้น เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="a6c37-122">ในแผนภูมิ เลือก **Contoso Consulting USA** จากนั้น เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="a6c37-123">ในแผนภูมิ เลือก **Contoso Retail USA** จากนั้น เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="a6c37-124">ยุบส่วน **องค์กรนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="a6c37-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="a6c37-125">ขยายส่วน **กฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="a6c37-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="a6c37-126">ในรายการ ค้นหาและเลือกกฎนโยบายที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="a6c37-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="a6c37-127">เลือก **สร้างกฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="a6c37-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="a6c37-128">ในฟิลด์ **วันที่มีผลบังคับใช้** ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="a6c37-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="a6c37-129">เลือก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="a6c37-129">Select **Filter**.</span></span>
23. <span data-ttu-id="a6c37-130">ในรายการ เลือกแถวสำหรับ **ประเภทค่าใช้จ่าย** และตั้งค่ารายละเอียดเป็น **โรงแรม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="a6c37-131">ในฟิลด์ **เกณฑ์** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="a6c37-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="a6c37-132">เลือกแท็บ **รวม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="a6c37-133">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-133">Select **Add**.</span></span>
27. <span data-ttu-id="a6c37-134">ในรายการ ให้เลือกค่าฟิลด์ของ **ยอดเงินธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="a6c37-135">ในฟิลด์ **Field** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a6c37-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="a6c37-136">ในฟิลด์ **AggregateFunction** เลือก **ผลรวม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="a6c37-137">เลือกแท็บ **จัดกลุ่มตาม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="a6c37-138">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-138">Select **Add**.</span></span>
32. <span data-ttu-id="a6c37-139">ในรายการ ให้เลือกค่าของ **พนักงาน**</span><span class="sxs-lookup"><span data-stu-id="a6c37-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="a6c37-140">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-140">Select **Add**.</span></span>
34. <span data-ttu-id="a6c37-141">ในรายการ ให้เลือกค่าของ **ประเภทค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="a6c37-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="a6c37-142">ในฟิลด์ **Field** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a6c37-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="a6c37-143">เลือกแท็บ **Having**</span><span class="sxs-lookup"><span data-stu-id="a6c37-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="a6c37-144">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-144">Select **Add**.</span></span>
38. <span data-ttu-id="a6c37-145">เลือก **ยอดเงินธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="a6c37-146">ในฟิลด์ **Field** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a6c37-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="a6c37-147">ในฟิลด์ **AggregateFunction** เลือก **ผลรวม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="a6c37-148">ในฟิลด์ **เกณฑ์** ให้พิมพ์ `>2000`</span><span class="sxs-lookup"><span data-stu-id="a6c37-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="a6c37-149">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a6c37-149">Select **OK**.</span></span>
43. <span data-ttu-id="a6c37-150">เลือก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="a6c37-150">Select **Test**.</span></span>
44. <span data-ttu-id="a6c37-151">ในฟิลด์ **วันที่เริ่มต้นของการเลือกเอกสาร** ให้เลือกวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="a6c37-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="a6c37-152">ในฟิลด์ **วันที่สิ้นสุดของการเลือกเอกสาร** ให้เลือกวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="a6c37-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="a6c37-153">เลือก **รันการทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="a6c37-153">Select **Run test**.</span></span>
47. <span data-ttu-id="a6c37-154">บนบานหน้าต่างการดำเนินการ เลือก **นโยบายการตรวจสอบ**</span><span class="sxs-lookup"><span data-stu-id="a6c37-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="a6c37-155">เลือก **ตัวเลือกเพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="a6c37-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="a6c37-156">ในฟิลด์ **วันที่เริ่มต้น** ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="a6c37-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="a6c37-157">ในฟิลด์ **วันที่สิ้นสุด** ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="a6c37-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="a6c37-158">เลือก **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="a6c37-158">Select **Batch**.</span></span>
52. <span data-ttu-id="a6c37-159">ขยายส่วน **รันในพื้นหลัง**</span><span class="sxs-lookup"><span data-stu-id="a6c37-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="a6c37-160">เลือก **ใช่** ในฟิลด์ **การประมวลชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="a6c37-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="a6c37-161">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a6c37-161">Select **OK**.</span></span>
55. <span data-ttu-id="a6c37-162">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > เวิร์กเบนช์การตรวจสอบ > กรณีการตรวจสอบ**</span><span class="sxs-lookup"><span data-stu-id="a6c37-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="a6c37-163">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a6c37-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="a6c37-164">ขยายส่วน **การเชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="a6c37-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="a6c37-165">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a6c37-165">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]