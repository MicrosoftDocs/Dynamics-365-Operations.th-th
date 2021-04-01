---
title: รายงานงทางการเงินใบแจ้งยอดรายได้
description: บทความนี้อธิบายรายงานเริ่มต้นสำหรับงบดุล นอกจากนี้ยังอธิบายถึงบล็อคส่วนประกอบที่เกี่ยวข้องกับรายงานนี้
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fab0e9d5e550b1848c3483b3172836e258353ebb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249082"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="7343a-104">รายงานงทางการเงินใบแจ้งยอดรายได้</span><span class="sxs-lookup"><span data-stu-id="7343a-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7343a-105">บทความนี้อธิบายรายงานเริ่มต้นสำหรับงบดุล</span><span class="sxs-lookup"><span data-stu-id="7343a-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="7343a-106">นอกจากนี้ยังอธิบายถึงบล็อคส่วนประกอบที่เกี่ยวข้องกับรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="7343a-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="7343a-107">รายงานใบแจ้งยอดรายได้เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7343a-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="7343a-108">รายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7343a-108">Default report</span></span>             | <span data-ttu-id="7343a-109">สิ่งที่ทำ</span><span class="sxs-lookup"><span data-stu-id="7343a-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7343a-110">งบกำไรขาดทุน – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7343a-110">Income Statement – Default</span></span> | <span data-ttu-id="7343a-111">ให้ภาพรวมของผลกำไรขององค์กรสำหรับรอบระยะเวลาปัจจุบันและสำหรับตั้งแต่ต้นปีจนถึงปัจจุบันด้วย</span><span class="sxs-lookup"><span data-stu-id="7343a-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="7343a-112">ส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="7343a-112">Building blocks</span></span>
<span data-ttu-id="7343a-113">รายงานทางการเงินของใบแจ้งยอดรายได้ใช้ส่วนประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7343a-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="7343a-114">รายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7343a-114">Default report</span></span>             | <span data-ttu-id="7343a-115">คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="7343a-115">Row definition</span></span>                     | <span data-ttu-id="7343a-116">คำนิยามคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="7343a-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="7343a-117">ใบแจ้งยอดรายได้ – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7343a-117">Income Statement - Default</span></span> | <span data-ttu-id="7343a-118">สรุปใบแจ้งยอดรายได้ – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7343a-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="7343a-119">งานประจำงวด และ YTD - ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7343a-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="7343a-120">คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="7343a-120">Row definition</span></span>

<span data-ttu-id="7343a-121">คำนิยามของแถว สรุปใบแจ้งยอดรายได้ – ค่าเริ่มต้น ประกอบด้วยส่วนสำหรับแต่ละส่วนของใบแจ้งยอดรายได้ดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="7343a-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="7343a-122">มิติประเภทบัญชีหลักถูกใช้ในการสร้างคำนิยามของแถวนี้</span><span class="sxs-lookup"><span data-stu-id="7343a-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="7343a-123">ดังนั้น ใครก็ตามสามารถสร้างรายงาน โดยไม่ต้องทำการปรับเปลี่ยนใด ๆ</span><span class="sxs-lookup"><span data-stu-id="7343a-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="7343a-124">คำนิยามของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="7343a-124">Column Definition</span></span>

<span data-ttu-id="7343a-125">คำนิยามของคอลัมน์ประกอบด้วย ชนิดที่แตกต่างกันของคอลัมน์เพื่อให้ระดับที่แตกต่างกันของรายละเอียดและข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="7343a-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="7343a-126">**งานประจำงวดและ YTD – ชนิดของคอลัมน์เริ่มต้น:**</span><span class="sxs-lookup"><span data-stu-id="7343a-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="7343a-127">**DESC** – คำอธิบายจากคำนิยามของแถว</span><span class="sxs-lookup"><span data-stu-id="7343a-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="7343a-128">**FD** – ข้อมูลทางการเงินสำหรับรอบระยะเวลาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="7343a-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="7343a-129">**FD** – ข้อมูลทางการเงินสำหรับตั้งแต่ต้นปีจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="7343a-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="7343a-130">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7343a-130">Additional resources</span></span>
--------

[<span data-ttu-id="7343a-131">ภาพรวมของการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="7343a-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="7343a-132">ดูรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="7343a-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="7343a-133">บล็อกการรายงานทางการเงิน Dynamics</span><span class="sxs-lookup"><span data-stu-id="7343a-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]