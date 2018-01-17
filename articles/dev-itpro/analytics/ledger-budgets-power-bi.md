---
title: "เนื้อหา Power BI ของงบประมาณและที่เกิดขึ้นจริง"
description: "หัวข้อนี้อธิบายถึงเนื้อหางบประมาณและที่เกิดขึ้นจริงใน Power BI และยังอธิบายถึงวิธีการเข้าถึงรายงานที่รวมอยู่ในชุดเนื้อหานี้ และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้สร้างชุดเนื้อหานี้"
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: db79d594e67a0e163cabbd3a5f7b7b1452c2ae9e
ms.openlocfilehash: a395f29aa8a1ed58f4d8681c4d874ee8b8b0a860
ms.contentlocale: th-th
ms.lasthandoff: 01/09/2018

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="e791b-104">เนื้อหา Power BI ของงบประมาณและที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="e791b-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e791b-105">หัวข้อนี้อธิบายถึงเนื้อหา **ที่เกิดขึ้นจริงเปรียบเทียบกับงบประมาณ** ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="e791b-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="e791b-106">และยังอธิบายถึงวิธีการเข้าถึงรายงาน Power BI และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างเนื้อหานี้</span><span class="sxs-lookup"><span data-stu-id="e791b-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="e791b-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="e791b-107">Overview</span></span>

<span data-ttu-id="e791b-108">เนื้อหา Power BI **ที่เกิดขึ้นจริงเทียบกับงบประมาณ** ถูกสร้างขึ้นสำหรับบุคคลแต่ละบุคคลที่รับผิดชอบในการตรวจสอบที่เกิดขึ้นจริงเทียบกับประสิทธิภาพของงบประมาณในองค์กรของตน</span><span class="sxs-lookup"><span data-stu-id="e791b-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="e791b-109">เนื้อหา Power BI **ที่เกิดขึ้นจริงเทียบกับงบประมาณ** แสดงภาพของผลต่างงบประมาณของคุณ</span><span class="sxs-lookup"><span data-stu-id="e791b-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="e791b-110">คุณสามารถวิเคราะห์งบประมาณสำหรับปีปัจจุบันโดยเรียงตามประเภทบัญชี รหัสงบประมาณ บัญชีหลัก คำอธิบายเกี่ยวกับบัญชีหลัก หรือรอบระยะเวลาทางบัญชีเพื่อที่จะทำความเข้าใจกับสาเหตุของผลต่างใด ๆ ได้ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="e791b-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="e791b-111">การเข้าถึงเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="e791b-111">Accessing the Power BI content</span></span>
<span data-ttu-id="e791b-112">รายงานจากเนื้อหา Power BI **ที่เกิดขึ้นจริงเทียบกับงบประมาณ** จะแสดงในพื้นที่ทำงาน **งบประมาณบัญชีแยกประเภทและการคาดการณ์** และ **CFO**</span><span class="sxs-lookup"><span data-stu-id="e791b-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="e791b-113">รายงานที่รวมอยู่ในเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="e791b-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="e791b-114">ตารางต่อไปนี้ให้รายละเอียดเกี่ยวกับเมตริกที่พบในแต่ละหน้าของรายงานในเนื้อหา **ที่เกิดขึ้นจริงเทียบกับงบประมาณ** ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="e791b-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="e791b-115">รายงาน</span><span class="sxs-lookup"><span data-stu-id="e791b-115">Report</span></span>                      | <span data-ttu-id="e791b-116">เมตริก</span><span class="sxs-lookup"><span data-stu-id="e791b-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="e791b-117">ค่าใช้จ่าย - เกิดขึ้นจริงเปรียบเทียบกับงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="e791b-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="e791b-118">ค่าใช้จ่ายรวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="e791b-118">Total expenses this year</span></span></li><li><span data-ttu-id="e791b-119">ค่าใช้จ่ายรวมของงบประมาณในปีนี้</span><span class="sxs-lookup"><span data-stu-id="e791b-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="e791b-120">รายได้ - ที่เกิดขึ้นจริงเทียบกับงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="e791b-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="e791b-121">รายได้รวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="e791b-121">Total revenue this year</span></span></li><li><span data-ttu-id="e791b-122">รายได้รวมของงบประมาณในปีนี้</span><span class="sxs-lookup"><span data-stu-id="e791b-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="e791b-123">ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="e791b-123">Expense</span></span>                     | <ul><li><span data-ttu-id="e791b-124">ค่าใช้จ่ายรวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="e791b-124">Total expenses this year</span></span></li><li><span data-ttu-id="e791b-125">เป้าหมายสำหรับค่าใช้จ่ายตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="e791b-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="e791b-126">รายได้</span><span class="sxs-lookup"><span data-stu-id="e791b-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="e791b-127">รายได้รวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="e791b-127">Total revenue this year</span></span></li><li><span data-ttu-id="e791b-128">เป้าหมายสำหรับรายได้ตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="e791b-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="e791b-129">กำไรสุทธิ</span><span class="sxs-lookup"><span data-stu-id="e791b-129">Net income</span></span>                  | <ul><li><span data-ttu-id="e791b-130">กำไรสุทธิปีนี้</span><span class="sxs-lookup"><span data-stu-id="e791b-130">Net income this year</span></span></li><li><span data-ttu-id="e791b-131">เป้าหมายสำหรับกำไรสุทธิตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="e791b-131">Goal for net income based on budget</span></span> </li><ul> |


# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="e791b-132">การทำความเข้าใจเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="e791b-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="e791b-133">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="e791b-133">Entity</span></span>                    | <span data-ttu-id="e791b-134">เนื้อหา</span><span class="sxs-lookup"><span data-stu-id="e791b-134">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="e791b-135">กิจกรรมของบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="e791b-135">General Ledger Activities</span></span> | <span data-ttu-id="e791b-136">ยอดเงินของธุรกรรมสำหรับบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="e791b-136">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="e791b-137">กิจกรรมของงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="e791b-137">Budget Activities</span></span>         | <span data-ttu-id="e791b-138">ยอดเงินธุรกรรมสำหรับทะเบียนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="e791b-138">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="e791b-139">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="e791b-139">Main Accounts</span></span>             | <span data-ttu-id="e791b-140">บัญชีหลักในการกรองข้อมูลรายงานโดย</span><span class="sxs-lookup"><span data-stu-id="e791b-140">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="e791b-141">ปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e791b-141">Fiscal Calendars</span></span>          | <span data-ttu-id="e791b-142">ปฏิทินทางการเงินเพื่อกรองข้อมูลรายงานโดย</span><span class="sxs-lookup"><span data-stu-id="e791b-142">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="e791b-143">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="e791b-143">Ledgers</span></span>                   | <span data-ttu-id="e791b-144">บัญชีแยกประเภทที่สามารถนำมาใช้เพื่อกรองข้อมูลรายงานในบัญชีแยกประเภทปัจจุบันได้</span><span class="sxs-lookup"><span data-stu-id="e791b-144">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="e791b-145">รหัสงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="e791b-145">Budget Codes</span></span>              | <span data-ttu-id="e791b-146">รหัสงบประมาณเพื่อกรองข้อมูลรายงานโดย</span><span class="sxs-lookup"><span data-stu-id="e791b-146">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="e791b-147">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="e791b-147">Legal Entities</span></span>            | <span data-ttu-id="e791b-148">นิติบุคคลที่สามารถนำมาใช้เพื่อกรองข้อมูลรายงานในนิติบุคคลปัจจุบันได้</span><span class="sxs-lookup"><span data-stu-id="e791b-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |

