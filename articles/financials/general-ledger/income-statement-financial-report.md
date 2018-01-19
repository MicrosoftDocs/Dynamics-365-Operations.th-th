---
title: "รายงานงทางการเงินใบแจ้งยอดรายได้"
description: "บทความนี้อธิบายรายงานเริ่มต้นสำหรับงบดุล นอกจากนี้ยังอธิบายถึงบล็อคส่วนประกอบที่เกี่ยวข้องกับรายงานนี้"
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 7626928bdb8c44036a8f995ccf6d5fd5c684438d
ms.contentlocale: th-th
ms.lasthandoff: 01/19/2018

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="d2778-104">รายงานงทางการเงินใบแจ้งยอดรายได้</span><span class="sxs-lookup"><span data-stu-id="d2778-104">Income statement financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d2778-105">บทความนี้อธิบายรายงานเริ่มต้นสำหรับงบดุล</span><span class="sxs-lookup"><span data-stu-id="d2778-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="d2778-106">นอกจากนี้ยังอธิบายถึงบล็อคส่วนประกอบที่เกี่ยวข้องกับรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="d2778-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="d2778-107">รายงานใบแจ้งยอดรายได้เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d2778-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="d2778-108">รายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d2778-108">Default report</span></span>             | <span data-ttu-id="d2778-109">สิ่งที่ทำ</span><span class="sxs-lookup"><span data-stu-id="d2778-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2778-110">งบกำไรขาดทุน – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d2778-110">Income Statement – Default</span></span> | <span data-ttu-id="d2778-111">ให้ภาพรวมของผลกำไรขององค์กรสำหรับรอบระยะเวลาปัจจุบันและสำหรับตั้งแต่ต้นปีจนถึงปัจจุบันด้วย</span><span class="sxs-lookup"><span data-stu-id="d2778-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="d2778-112">ส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="d2778-112">Building blocks</span></span>
<span data-ttu-id="d2778-113">รายงานทางการเงินของใบแจ้งยอดรายได้ใช้ส่วนประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d2778-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="d2778-114">รายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d2778-114">Default report</span></span>             | <span data-ttu-id="d2778-115">คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="d2778-115">Row definition</span></span>                     | <span data-ttu-id="d2778-116">คำนิยามคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="d2778-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="d2778-117">ใบแจ้งยอดรายได้ – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d2778-117">Income Statement - Default</span></span> | <span data-ttu-id="d2778-118">สรุปใบแจ้งยอดรายได้ – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d2778-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="d2778-119">งานประจำงวด และ YTD - ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d2778-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="d2778-120">คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="d2778-120">Row definition</span></span>

<span data-ttu-id="d2778-121">คำนิยามของแถว สรุปใบแจ้งยอดรายได้ – ค่าเริ่มต้น ประกอบด้วยส่วนสำหรับแต่ละส่วนของใบแจ้งยอดรายได้ดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="d2778-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="d2778-122">มิติประเภทบัญชีหลักถูกใช้ในการสร้างคำนิยามของแถวนี้</span><span class="sxs-lookup"><span data-stu-id="d2778-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="d2778-123">ดังนั้น ใครก็ตามสามารถสร้างรายงาน โดยไม่ต้องทำการปรับเปลี่ยนใด ๆ</span><span class="sxs-lookup"><span data-stu-id="d2778-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="d2778-124">คำนิยามของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="d2778-124">Column Definition</span></span>

<span data-ttu-id="d2778-125">คำนิยามของคอลัมน์ประกอบด้วย ชนิดที่แตกต่างกันของคอลัมน์เพื่อให้ระดับที่แตกต่างกันของรายละเอียดและข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="d2778-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="d2778-126">**งานประจำงวดและ YTD – ชนิดของคอลัมน์เริ่มต้น:**</span><span class="sxs-lookup"><span data-stu-id="d2778-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="d2778-127">**DESC** – คำอธิบายจากคำนิยามของแถว</span><span class="sxs-lookup"><span data-stu-id="d2778-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d2778-128">**FD** – ข้อมูลทางการเงินสำหรับรอบระยะเวลาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d2778-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="d2778-129">**FD** – ข้อมูลทางการเงินสำหรับตั้งแต่ต้นปีจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d2778-129">**FD** – Financial data for the year to date</span></span>

 

<a name="see-also"></a><span data-ttu-id="d2778-130">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="d2778-130">See also</span></span>
--------

[<span data-ttu-id="d2778-131">การรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="d2778-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="d2778-132">ดูรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="d2778-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="d2778-133">บล็อกการรายงานทางการเงิน Dynamics</span><span class="sxs-lookup"><span data-stu-id="d2778-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




