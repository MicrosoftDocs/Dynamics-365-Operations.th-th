---
title: เนื้อหา Power BI ข้อมูลจริงเทียบกับงบประมาณ
description: หัวข้อนี้อธิบายเนื้อหา Power BI ข้อมูลจริงเทียบกับงบประมาณ และยังอธิบายถึงวิธีการเข้าถึงรายงานที่รวมอยู่ในชุดเนื้อหานี้ และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้สร้างชุดเนื้อหานี้
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c801544e9e37a528203f5a1730aa8cb526d63dbf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "343500"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="0dc6a-104">เนื้อหา Power BI ข้อมูลจริงเทียบกับงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="0dc6a-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0dc6a-105">หัวข้อนี้อธิบายเนื้อหา Microsoft Power BI **ข้อมูลจริงเทียบกับงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="0dc6a-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="0dc6a-106">และยังอธิบายถึงวิธีการเข้าถึงรายงาน Power BI และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างเนื้อหานี้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="0dc6a-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="0dc6a-107">Overview</span></span>

<span data-ttu-id="0dc6a-108">เนื้อหา Power BI **ข้อมูลจริงเทียบกับงบประมาณ** ถูกสร้างสำหรับบุคคลที่รับผิดชอบการตรวจสอบประสิทธิภาพข้อมูลจริงเทียบกับงบประมาณในองค์กรของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="0dc6a-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="0dc6a-109">เนื้อหา Power BI ของ **ข้อมูลจริงเทียบกับงบประมาณ** ให้ความสามารถในการมองเห็นไปยังผลต่างของงบประมาณของคุณ</span><span class="sxs-lookup"><span data-stu-id="0dc6a-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="0dc6a-110">คุณสามารถวิเคราะห์งบประมาณสำหรับปีปัจจุบันโดยเรียงตามประเภทบัญชี รหัสงบประมาณ บัญชีหลัก คำอธิบายเกี่ยวกับบัญชีหลัก หรือรอบระยะเวลาทางบัญชีเพื่อที่จะทำความเข้าใจกับสาเหตุของผลต่างใด ๆ ได้ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="0dc6a-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="0dc6a-111">การเข้าถึงเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="0dc6a-111">Accessing the Power BI content</span></span>
<span data-ttu-id="0dc6a-112">รายงานจากเนื้อหา Power BI ของ **ข้อมูลจริงเทียบกับงบประมาณ** ถูกแสดงในพื้นที่ทำงาน **งบประมาณบัญชีแยกประเภทและการคาดการณ์** และ **CFO**</span><span class="sxs-lookup"><span data-stu-id="0dc6a-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="0dc6a-113">รายงานที่รวมอยู่ในเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="0dc6a-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="0dc6a-114">ตารางต่อไปนี้ให้รายละเอียดเกี่ยวกับการวัดที่ถูกพบในหน้ารายงานแต่ละหน้าในเนื้อหา Power BI ของ **ข้อมูลจริงเทียบกับงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="0dc6a-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="0dc6a-115">รายงาน</span><span class="sxs-lookup"><span data-stu-id="0dc6a-115">Report</span></span>                      | <span data-ttu-id="0dc6a-116">เมตริก</span><span class="sxs-lookup"><span data-stu-id="0dc6a-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc6a-117">ค่าใช้จ่าย - เกิดขึ้นจริงเปรียบเทียบกับงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="0dc6a-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="0dc6a-118">ค่าใช้จ่ายรวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-118">Total expenses this year</span></span></li><li><span data-ttu-id="0dc6a-119">ค่าใช้จ่ายรวมของงบประมาณในปีนี้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="0dc6a-120">รายได้ - ที่เกิดขึ้นจริงเทียบกับงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="0dc6a-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="0dc6a-121">รายได้รวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-121">Total revenue this year</span></span></li><li><span data-ttu-id="0dc6a-122">รายได้รวมของงบประมาณในปีนี้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="0dc6a-123">ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0dc6a-123">Expense</span></span>                     | <ul><li><span data-ttu-id="0dc6a-124">ค่าใช้จ่ายรวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-124">Total expenses this year</span></span></li><li><span data-ttu-id="0dc6a-125">เป้าหมายสำหรับค่าใช้จ่ายตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="0dc6a-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="0dc6a-126">รายได้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="0dc6a-127">รายได้รวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-127">Total revenue this year</span></span></li><li><span data-ttu-id="0dc6a-128">เป้าหมายสำหรับรายได้ตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="0dc6a-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="0dc6a-129">กำไรสุทธิ</span><span class="sxs-lookup"><span data-stu-id="0dc6a-129">Net income</span></span>                  | <ul><li><span data-ttu-id="0dc6a-130">กำไรสุทธิปีนี้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-130">Net income this year</span></span></li><li><span data-ttu-id="0dc6a-131">เป้าหมายสำหรับกำไรสุทธิตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="0dc6a-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="0dc6a-132">การทำความเข้าใจเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="0dc6a-133">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-133">Entity</span></span>                    | <span data-ttu-id="0dc6a-134">เนื้อหา</span><span class="sxs-lookup"><span data-stu-id="0dc6a-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0dc6a-135">กิจกรรมของบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="0dc6a-135">General Ledger Activities</span></span> | <span data-ttu-id="0dc6a-136">ยอดเงินของธุรกรรมสำหรับบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="0dc6a-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="0dc6a-137">กิจกรรมของงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="0dc6a-137">Budget Activities</span></span>         | <span data-ttu-id="0dc6a-138">ยอดเงินธุรกรรมสำหรับทะเบียนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="0dc6a-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="0dc6a-139">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="0dc6a-139">Main Accounts</span></span>             | <span data-ttu-id="0dc6a-140">บัญชีหลักในการกรองข้อมูลรายงานโดย</span><span class="sxs-lookup"><span data-stu-id="0dc6a-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="0dc6a-141">ปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="0dc6a-141">Fiscal Calendars</span></span>          | <span data-ttu-id="0dc6a-142">ปฏิทินทางการเงินเพื่อกรองข้อมูลรายงานโดย</span><span class="sxs-lookup"><span data-stu-id="0dc6a-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="0dc6a-143">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="0dc6a-143">Ledgers</span></span>                   | <span data-ttu-id="0dc6a-144">บัญชีแยกประเภทที่สามารถนำมาใช้เพื่อกรองข้อมูลรายงานในบัญชีแยกประเภทปัจจุบันได้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="0dc6a-145">รหัสงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="0dc6a-145">Budget Codes</span></span>              | <span data-ttu-id="0dc6a-146">รหัสงบประมาณเพื่อกรองข้อมูลรายงานโดย</span><span class="sxs-lookup"><span data-stu-id="0dc6a-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="0dc6a-147">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="0dc6a-147">Legal Entities</span></span>            | <span data-ttu-id="0dc6a-148">นิติบุคคลที่สามารถนำมาใช้เพื่อกรองข้อมูลรายงานในนิติบุคคลปัจจุบันได้</span><span class="sxs-lookup"><span data-stu-id="0dc6a-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |
