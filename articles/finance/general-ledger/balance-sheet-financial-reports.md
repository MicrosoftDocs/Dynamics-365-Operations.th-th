---
title: รายงานทางการเงินของงบดุล
description: บทความนี้อธิบายรายงานเริ่มต้นสำหรับงบดุล นอกจากนี้ยังอธิบายถึงบล็อคส่วนประกอบที่เกี่ยวข้องกับรายงานเหล่านี้
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d249172c2bc4241a47502b57f2ac20b29111eeba
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985023"
---
# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="3d7b7-104">รายงานทางการเงินของงบดุล</span><span class="sxs-lookup"><span data-stu-id="3d7b7-104">Balance sheet financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d7b7-105">บทความนี้อธิบายรายงานเริ่มต้นสำหรับงบดุล</span><span class="sxs-lookup"><span data-stu-id="3d7b7-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="3d7b7-106">นอกจากนี้ยังอธิบายถึงบล็อคส่วนประกอบที่เกี่ยวข้องกับรายงานเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="3d7b7-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="3d7b7-107">รายงานงบดุลเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3d7b7-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="3d7b7-108">มีรายงานงบดุลเริ่มต้นสองฉบับ</span><span class="sxs-lookup"><span data-stu-id="3d7b7-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="3d7b7-109">ในรายงานหนึ่งฉบับ ส่วนต่างๆจะถูกซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="3d7b7-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="3d7b7-110">ในรายงานฉบับอื่น ส่วนจะอยู่เคียงข้างกัน</span><span class="sxs-lookup"><span data-stu-id="3d7b7-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="3d7b7-111">รายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3d7b7-111">Default report</span></span>                       | <span data-ttu-id="3d7b7-112">สิ่งที่ทำ</span><span class="sxs-lookup"><span data-stu-id="3d7b7-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7b7-113">งบดุล – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3d7b7-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="3d7b7-114">แสดงมุมมองของตำแหน่งทางการเงินขององค์กรต่อปี</span><span class="sxs-lookup"><span data-stu-id="3d7b7-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="3d7b7-115">งบดุลเคียงข้างกัน – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3d7b7-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="3d7b7-116">แสดงมุมมองของตำแหน่งทางการเงินขององค์กรต่อปี</span><span class="sxs-lookup"><span data-stu-id="3d7b7-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="3d7b7-117">สินทรัพย์และหนี้สินและส่วนของผู้ถือหุ้นเคียงข้างกัน</span><span class="sxs-lookup"><span data-stu-id="3d7b7-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="3d7b7-118">ส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="3d7b7-118">Building blocks</span></span>
<span data-ttu-id="3d7b7-119">รายงานทางการเงินของงบดุลใช้ส่วนประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3d7b7-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="3d7b7-120">รายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3d7b7-120">Default report</span></span>                       | <span data-ttu-id="3d7b7-121">คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="3d7b7-121">Row definition</span></span>                       | <span data-ttu-id="3d7b7-122">คำนิยามคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="3d7b7-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="3d7b7-123">งบดุล – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3d7b7-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="3d7b7-124">งบดุล – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3d7b7-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="3d7b7-125">YTD และผลต่าง - ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3d7b7-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="3d7b7-126">งบดุลเคียงข้างกัน – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3d7b7-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="3d7b7-127">งบดุลเคียงข้างกัน – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3d7b7-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="3d7b7-128">คอลัมน์ ตั้งแต่ต้นปีจนถึงปัจจุบัน - ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3d7b7-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="3d7b7-129">คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="3d7b7-129">Row definition</span></span>

<span data-ttu-id="3d7b7-130">คำนิยามของแถวสำหรับรายงานงบดุลทั้งสองฉบับประกอบด้วย ส่วนสำหรับส่วนของงบดุลแบบดั้งเดิมแต่ละส่วน</span><span class="sxs-lookup"><span data-stu-id="3d7b7-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="3d7b7-131">รายงานที่อยู่เคียงข้างกันรวมตัวแบ่งคอลัมน์ เพื่อให้หนี้สินและส่วนของผู้ถือหุ้นของเจ้าของปรากฏอยู่ติดกับสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="3d7b7-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="3d7b7-132">มิติประเภทบัญชีหลักถูกใช้ในการสร้างคำนิยามของแถวทั้งสองแถว</span><span class="sxs-lookup"><span data-stu-id="3d7b7-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="3d7b7-133">ดังนั้น ใครก็ตามสามารถสร้างรายงานได้โดยไม่ต้องทำการปรับเปลี่ยนใดๆ</span><span class="sxs-lookup"><span data-stu-id="3d7b7-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="3d7b7-134">คำนิยามคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="3d7b7-134">Column definition</span></span>

<span data-ttu-id="3d7b7-135">คำนิยามของคอลัมน์ประกอบด้วย ชนิดที่แตกต่างกันของคอลัมน์เพื่อให้ระดับที่แตกต่างกันของรายละเอียดและข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="3d7b7-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="3d7b7-136">**YTD และผลต่าง – ชนิดของคอลัมน์เริ่มต้น:**</span><span class="sxs-lookup"><span data-stu-id="3d7b7-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="3d7b7-137">**DESC** – คำอธิบายจากคำนิยามของแถว</span><span class="sxs-lookup"><span data-stu-id="3d7b7-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="3d7b7-138">**FD** – ข้อมูลทางการเงินตั้งแต่ต้นปีจนถึงปัจจุบันสำหรับปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3d7b7-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="3d7b7-139">**FD** – ข้อมูลทางการเงินตั้งแต่ต้นปีจนถึงปัจจุบันสำหรับปีที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="3d7b7-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="3d7b7-140">**CALC**– ผลต่างจากการลบปีที่ผ่านมาออกจากปีนี้</span><span class="sxs-lookup"><span data-stu-id="3d7b7-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="3d7b7-141">**คอลัมน์ตั้งแต่ต้นปีจนถึงปัจจุบัน - ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="3d7b7-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="3d7b7-142">**DESC** – คำอธิบายจากคำนิยามของแถว</span><span class="sxs-lookup"><span data-stu-id="3d7b7-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="3d7b7-143">**FD** – ข้อมูลทางการเงินตั้งแต่ต้นปีจนถึงปัจจุบันสำหรับปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3d7b7-143">**FD** – Year-to-date financial data for the current year</span></span>



<a name="additional-resources"></a><span data-ttu-id="3d7b7-144">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3d7b7-144">Additional resources</span></span>
--------

[<span data-ttu-id="3d7b7-145">ภาพรวมของการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="3d7b7-145">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="3d7b7-146">ดูรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="3d7b7-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="3d7b7-147">บล็อกการรายงานทางการเงิน Dynamics</span><span class="sxs-lookup"><span data-stu-id="3d7b7-147">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



