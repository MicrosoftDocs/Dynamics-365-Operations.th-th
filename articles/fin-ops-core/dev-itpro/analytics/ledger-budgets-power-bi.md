---
title: เนื้อหา Power BI ข้อมูลจริงเทียบกับงบประมาณ
description: หัวข้อนี้อธิบายเนื้อหา Power BI ข้อมูลจริงเทียบกับงบประมาณ ซึ่งอธิบายวิธีการเข้าถึงรายงาน และแสดงข้อมูลเกี่ยวกับรูปแบบข้อมูล
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f3e2f62b666559ba9a356e4948c2033da9cc95d5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568584"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="93858-104">เนื้อหา Power BI ข้อมูลจริงเทียบกับงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="93858-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93858-105">หัวข้อนี้อธิบายเนื้อหา Microsoft Power BI **ข้อมูลจริงเทียบกับงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="93858-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="93858-106">และยังอธิบายถึงวิธีการเข้าถึงรายงาน Power BI และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างเนื้อหานี้</span><span class="sxs-lookup"><span data-stu-id="93858-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="93858-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="93858-107">Overview</span></span>

<span data-ttu-id="93858-108">เนื้อหา Power BI **ข้อมูลจริงเทียบกับงบประมาณ** ถูกสร้างสำหรับบุคคลที่รับผิดชอบการตรวจสอบประสิทธิภาพข้อมูลจริงเทียบกับงบประมาณในองค์กรของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="93858-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="93858-109">เนื้อหา Power BI ของ **ข้อมูลจริงเทียบกับงบประมาณ** ให้ความสามารถในการมองเห็นไปยังผลต่างของงบประมาณของคุณ</span><span class="sxs-lookup"><span data-stu-id="93858-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="93858-110">คุณสามารถวิเคราะห์งบประมาณสำหรับปีปัจจุบันโดยเรียงตามประเภทบัญชี รหัสงบประมาณ บัญชีหลัก คำอธิบายเกี่ยวกับบัญชีหลัก หรือรอบระยะเวลาทางบัญชีเพื่อที่จะทำความเข้าใจกับสาเหตุของผลต่างใด ๆ ได้ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="93858-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="93858-111">การเข้าถึงเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="93858-111">Accessing the Power BI content</span></span>
<span data-ttu-id="93858-112">รายงานจากเนื้อหา Power BI ของ **ข้อมูลจริงเทียบกับงบประมาณ** ถูกแสดงในพื้นที่ทำงาน **งบประมาณบัญชีแยกประเภทและการคาดการณ์** และ **CFO**</span><span class="sxs-lookup"><span data-stu-id="93858-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="93858-113">รายงานที่รวมอยู่ในเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="93858-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="93858-114">ตารางต่อไปนี้ให้รายละเอียดเกี่ยวกับการวัดที่ถูกพบในหน้ารายงานแต่ละหน้าในเนื้อหา Power BI ของ **ข้อมูลจริงเทียบกับงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="93858-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="93858-115">รายงาน</span><span class="sxs-lookup"><span data-stu-id="93858-115">Report</span></span>                      | <span data-ttu-id="93858-116">เมตริก</span><span class="sxs-lookup"><span data-stu-id="93858-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="93858-117">ค่าใช้จ่าย - เกิดขึ้นจริงเปรียบเทียบกับงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="93858-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="93858-118">ค่าใช้จ่ายรวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="93858-118">Total expenses this year</span></span></li><li><span data-ttu-id="93858-119">ค่าใช้จ่ายรวมของงบประมาณในปีนี้</span><span class="sxs-lookup"><span data-stu-id="93858-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="93858-120">รายได้ - ที่เกิดขึ้นจริงเทียบกับงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="93858-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="93858-121">รายได้รวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="93858-121">Total revenue this year</span></span></li><li><span data-ttu-id="93858-122">รายได้รวมของงบประมาณในปีนี้</span><span class="sxs-lookup"><span data-stu-id="93858-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="93858-123">ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="93858-123">Expense</span></span>                     | <ul><li><span data-ttu-id="93858-124">ค่าใช้จ่ายรวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="93858-124">Total expenses this year</span></span></li><li><span data-ttu-id="93858-125">เป้าหมายสำหรับค่าใช้จ่ายตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="93858-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="93858-126">รายได้</span><span class="sxs-lookup"><span data-stu-id="93858-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="93858-127">รายได้รวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="93858-127">Total revenue this year</span></span></li><li><span data-ttu-id="93858-128">เป้าหมายสำหรับรายได้ตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="93858-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="93858-129">กำไรสุทธิ</span><span class="sxs-lookup"><span data-stu-id="93858-129">Net income</span></span>                  | <ul><li><span data-ttu-id="93858-130">กำไรสุทธิปีนี้</span><span class="sxs-lookup"><span data-stu-id="93858-130">Net income this year</span></span></li><li><span data-ttu-id="93858-131">เป้าหมายสำหรับกำไรสุทธิตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="93858-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="93858-132">การทำความเข้าใจเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="93858-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="93858-133">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="93858-133">Entity</span></span>                    | <span data-ttu-id="93858-134">เนื้อหา</span><span class="sxs-lookup"><span data-stu-id="93858-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="93858-135">กิจกรรมของบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="93858-135">General Ledger Activities</span></span> | <span data-ttu-id="93858-136">ยอดเงินของธุรกรรมสำหรับบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="93858-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="93858-137">กิจกรรมของงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="93858-137">Budget Activities</span></span>         | <span data-ttu-id="93858-138">ยอดเงินธุรกรรมสำหรับทะเบียนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="93858-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="93858-139">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="93858-139">Main Accounts</span></span>             | <span data-ttu-id="93858-140">บัญชีหลักในการกรองข้อมูลรายงานโดย</span><span class="sxs-lookup"><span data-stu-id="93858-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="93858-141">ปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="93858-141">Fiscal Calendars</span></span>          | <span data-ttu-id="93858-142">ปฏิทินทางการเงินเพื่อกรองข้อมูลรายงานโดย</span><span class="sxs-lookup"><span data-stu-id="93858-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="93858-143">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="93858-143">Ledgers</span></span>                   | <span data-ttu-id="93858-144">บัญชีแยกประเภทที่สามารถนำมาใช้เพื่อกรองข้อมูลรายงานในบัญชีแยกประเภทปัจจุบันได้</span><span class="sxs-lookup"><span data-stu-id="93858-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="93858-145">รหัสงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="93858-145">Budget Codes</span></span>              | <span data-ttu-id="93858-146">รหัสงบประมาณเพื่อกรองข้อมูลรายงานโดย</span><span class="sxs-lookup"><span data-stu-id="93858-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="93858-147">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="93858-147">Legal Entities</span></span>            | <span data-ttu-id="93858-148">นิติบุคคลที่สามารถนำมาใช้เพื่อกรองข้อมูลรายงานในนิติบุคคลปัจจุบันได้</span><span class="sxs-lookup"><span data-stu-id="93858-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]