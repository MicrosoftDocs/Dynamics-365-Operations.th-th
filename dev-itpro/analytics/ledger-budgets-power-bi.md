---
title: "เนื้อหา Power BI ของงบประมาณและที่เกิดขึ้นจริง"
description: "หัวข้อนี้อธิบายถึงเนื้อหางบประมาณและที่เกิดขึ้นจริงใน Power BI และยังอธิบายถึงวิธีการเข้าถึงรายงานที่รวมอยู่ในชุดเนื้อหานี้ และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้สร้างชุดเนื้อหานี้"
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 6e675ccd610561668dec4f5c7410530edaa122b8
ms.contentlocale: th-th
ms.lasthandoff: 07/18/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="9772c-104">เนื้อหา Power BI ของงบประมาณและที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="9772c-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9772c-105">หัวข้อนี้อธิบายถึงเนื้อหา **ที่เกิดขึ้นจริงเปรียบเทียบกับงบประมาณ** ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="9772c-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="9772c-106">และยังอธิบายถึงวิธีการเข้าถึงรายงาน Power BI และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างเนื้อหานี้</span><span class="sxs-lookup"><span data-stu-id="9772c-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="9772c-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="9772c-107">Overview</span></span>

<span data-ttu-id="9772c-108">เนื้อหา Power BI **ที่เกิดขึ้นจริงเทียบกับงบประมาณ** ถูกสร้างขึ้นสำหรับบุคคลแต่ละบุคคลที่รับผิดชอบในการตรวจสอบที่เกิดขึ้นจริงเทียบกับประสิทธิภาพของงบประมาณในองค์กรของตน</span><span class="sxs-lookup"><span data-stu-id="9772c-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="9772c-109">เนื้อหา Power BI **ที่เกิดขึ้นจริงเทียบกับงบประมาณ** แสดงภาพของผลต่างงบประมาณของคุณ</span><span class="sxs-lookup"><span data-stu-id="9772c-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="9772c-110">คุณสามารถวิเคราะห์งบประมาณสำหรับปีปัจจุบันโดยเรียงตามประเภทบัญชี รหัสงบประมาณ บัญชีหลัก คำอธิบายเกี่ยวกับบัญชีหลัก หรือรอบระยะเวลาทางบัญชีเพื่อที่จะทำความเข้าใจกับสาเหตุของผลต่างใด ๆ ได้ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="9772c-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="9772c-111">การเข้าถึงเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="9772c-111">Accessing the Power BI content</span></span>
<span data-ttu-id="9772c-112">ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition การอัพเดตของเดือนกรกฎาคม 2017 รายงานจากเนื้อหา Power BI **ที่เกิดขึ้นจริงเทียบกับงบประมาณ** จะแสดงอยู่ในพื้นที่ทำงาน **งบประมาณบัญชีแยกประเภทและการคาดการณ์** และ **CFO**</span><span class="sxs-lookup"><span data-stu-id="9772c-112">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="9772c-113">รายงานที่รวมอยู่ในเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="9772c-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="9772c-114">ตารางต่อไปนี้ให้รายละเอียดเกี่ยวกับเมตริกที่พบในแต่ละหน้าของรายงานในเนื้อหา **ที่เกิดขึ้นจริงเทียบกับงบประมาณ** ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="9772c-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="9772c-115">รายงาน</span><span class="sxs-lookup"><span data-stu-id="9772c-115">Report</span></span>                      | <span data-ttu-id="9772c-116">เมตริก</span><span class="sxs-lookup"><span data-stu-id="9772c-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="9772c-117">ค่าใช้จ่าย - เกิดขึ้นจริงเปรียบเทียบกับงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9772c-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="9772c-118">ค่าใช้จ่ายรวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="9772c-118">Total expenses this year</span></span></li><li><span data-ttu-id="9772c-119">ค่าใช้จ่ายรวมของงบประมาณในปีนี้</span><span class="sxs-lookup"><span data-stu-id="9772c-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="9772c-120">รายได้ - ที่เกิดขึ้นจริงเทียบกับงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9772c-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="9772c-121">รายได้รวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="9772c-121">Total revenue this year</span></span></li><li><span data-ttu-id="9772c-122">รายได้รวมของงบประมาณในปีนี้</span><span class="sxs-lookup"><span data-stu-id="9772c-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="9772c-123">ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="9772c-123">Expense</span></span>                     | <ul><li><span data-ttu-id="9772c-124">ค่าใช้จ่ายรวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="9772c-124">Total expenses this year</span></span></li><li><span data-ttu-id="9772c-125">เป้าหมายสำหรับค่าใช้จ่ายตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9772c-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="9772c-126">รายได้</span><span class="sxs-lookup"><span data-stu-id="9772c-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="9772c-127">รายได้รวมปีนี้</span><span class="sxs-lookup"><span data-stu-id="9772c-127">Total revenue this year</span></span></li><li><span data-ttu-id="9772c-128">เป้าหมายสำหรับรายได้ตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9772c-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="9772c-129">กำไรสุทธิ</span><span class="sxs-lookup"><span data-stu-id="9772c-129">Net income</span></span>                  | <ul><li><span data-ttu-id="9772c-130">กำไรสุทธิปีนี้</span><span class="sxs-lookup"><span data-stu-id="9772c-130">Net income this year</span></span></li><li><span data-ttu-id="9772c-131">เป้าหมายสำหรับกำไรสุทธิตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9772c-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="9772c-132">การขยายเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="9772c-132">Extending the Power BI content</span></span>
<span data-ttu-id="9772c-133">โดยการใช้ชุดเนื้อหาที่พร้อมใช้งานใน Microsoft Dynamics Lifecycle Services (LCS) คุณสามารถให้ข้อมูลการวิเคราะห์ที่ยอดเยี่ยมแก่ผู้ที่ไม่ได้ลงชื่อเข้าใช้ Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9772c-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="9772c-134">คุณสามารถแก้ไขชุดเนื้อหาเหล่านี้ เพื่อรวมกับการรายงานหรือสิ่งที่มองเห็นได้อื่น ๆ และจากนั้นเผยแพร่ชุดเนื้อหานี้ไปยังผู้เช่า Power BI.com ของคุณสำหรับการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="9772c-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="9772c-135">คุณสามารถค้นหาเนื้อหา Power BI **ที่เกิดขึ้นจริงเทียบกับงบประมาณ** ได้ในไลบรารีสินทรัพย์ที่ใช้ร่วมกันใน LCS</span><span class="sxs-lookup"><span data-stu-id="9772c-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="9772c-136">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการดาวน์โหลดเนื้อหา Power BI และนำไปใช้ในองค์กรของคุณ ให้ดูที่ [เนื้อหา Power BI ใน LCS จาก Microsoft และคู่ค้าของคุณ](power-bi-content-microsoft-partners.md)</span><span class="sxs-lookup"><span data-stu-id="9772c-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="9772c-137">เมื่อต้องการดูการสาธิตที่แสดงวิธีใช้เนื้อหา Power BI ให้ดูที่ Office Mix [เนื้อหา Power BI จาก Microsoft และคู่ค้าของคุณใน Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w)</span><span class="sxs-lookup"><span data-stu-id="9772c-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="9772c-138">การทำความเข้าใจเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="9772c-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="9772c-139">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="9772c-139">Entity</span></span>                    | <span data-ttu-id="9772c-140">เนื้อหา</span><span class="sxs-lookup"><span data-stu-id="9772c-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="9772c-141">กิจกรรมของบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="9772c-141">General Ledger Activities</span></span> | <span data-ttu-id="9772c-142">ยอดเงินของธุรกรรมสำหรับบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="9772c-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="9772c-143">กิจกรรมของงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9772c-143">Budget Activities</span></span>         | <span data-ttu-id="9772c-144">ยอดเงินธุรกรรมสำหรับทะเบียนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9772c-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="9772c-145">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="9772c-145">Main Accounts</span></span>             | <span data-ttu-id="9772c-146">บัญชีหลักในการกรองข้อมูลรายงานโดย</span><span class="sxs-lookup"><span data-stu-id="9772c-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="9772c-147">ปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="9772c-147">Fiscal Calendars</span></span>          | <span data-ttu-id="9772c-148">ปฏิทินทางการเงินเพื่อกรองข้อมูลรายงานโดย</span><span class="sxs-lookup"><span data-stu-id="9772c-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="9772c-149">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="9772c-149">Ledgers</span></span>                   | <span data-ttu-id="9772c-150">บัญชีแยกประเภทที่สามารถนำมาใช้เพื่อกรองข้อมูลรายงานในบัญชีแยกประเภทปัจจุบันได้</span><span class="sxs-lookup"><span data-stu-id="9772c-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="9772c-151">รหัสงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9772c-151">Budget Codes</span></span>              | <span data-ttu-id="9772c-152">รหัสงบประมาณเพื่อกรองข้อมูลรายงานโดย</span><span class="sxs-lookup"><span data-stu-id="9772c-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="9772c-153">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="9772c-153">Legal Entities</span></span>            | <span data-ttu-id="9772c-154">นิติบุคคลที่สามารถนำมาใช้เพื่อกรองข้อมูลรายงานในนิติบุคคลปัจจุบันได้</span><span class="sxs-lookup"><span data-stu-id="9772c-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

