---
title: "รายงานทางการเงินของงบดุล"
description: "บทความนี้อธิบายรายงานเริ่มต้นสำหรับงบดุล นอกจากนี้ยังอธิบายถึงบล็อคส่วนประกอบที่เกี่ยวข้องกับรายงานเหล่านี้"
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6323a2bf40a853edff4b3cef31eea7e95542a92e
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---

# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="ceab1-104">รายงานทางการเงินของงบดุล</span><span class="sxs-lookup"><span data-stu-id="ceab1-104">Balance sheet financial reports</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ceab1-105">บทความนี้อธิบายรายงานเริ่มต้นสำหรับงบดุล</span><span class="sxs-lookup"><span data-stu-id="ceab1-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="ceab1-106">นอกจากนี้ยังอธิบายถึงบล็อคส่วนประกอบที่เกี่ยวข้องกับรายงานเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ceab1-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="ceab1-107">รายงานงบดุลเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ceab1-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="ceab1-108">มีรายงานงบดุลเริ่มต้นสองฉบับ</span><span class="sxs-lookup"><span data-stu-id="ceab1-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="ceab1-109">ในรายงานหนึ่งฉบับ ส่วนต่างๆจะถูกซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="ceab1-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="ceab1-110">ในรายงานฉบับอื่น ส่วนจะอยู่เคียงข้างกัน</span><span class="sxs-lookup"><span data-stu-id="ceab1-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="ceab1-111">รายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ceab1-111">Default report</span></span>                       | <span data-ttu-id="ceab1-112">สิ่งที่ทำ</span><span class="sxs-lookup"><span data-stu-id="ceab1-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceab1-113">งบดุล – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ceab1-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="ceab1-114">แสดงมุมมองของตำแหน่งทางการเงินขององค์กรต่อปี</span><span class="sxs-lookup"><span data-stu-id="ceab1-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="ceab1-115">งบดุลเคียงข้างกัน – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ceab1-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="ceab1-116">แสดงมุมมองของตำแหน่งทางการเงินขององค์กรต่อปี</span><span class="sxs-lookup"><span data-stu-id="ceab1-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="ceab1-117">สินทรัพย์และหนี้สินและส่วนของผู้ถือหุ้นเคียงข้างกัน</span><span class="sxs-lookup"><span data-stu-id="ceab1-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="ceab1-118">ส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="ceab1-118">Building blocks</span></span>
<span data-ttu-id="ceab1-119">รายงานทางการเงินของงบดุลใช้ส่วนประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ceab1-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="ceab1-120">รายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ceab1-120">Default report</span></span>                       | <span data-ttu-id="ceab1-121">คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="ceab1-121">Row definition</span></span>                       | <span data-ttu-id="ceab1-122">คำนิยามคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="ceab1-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="ceab1-123">งบดุล – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ceab1-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="ceab1-124">งบดุล – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ceab1-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="ceab1-125">YTD และผลต่าง - ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ceab1-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="ceab1-126">งบดุลเคียงข้างกัน – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ceab1-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="ceab1-127">งบดุลเคียงข้างกัน – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ceab1-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="ceab1-128">คอลัมน์ ตั้งแต่ต้นปีจนถึงปัจจุบัน - ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ceab1-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="ceab1-129">คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="ceab1-129">Row definition</span></span>

<span data-ttu-id="ceab1-130">คำนิยามของแถวสำหรับรายงานงบดุลทั้งสองฉบับประกอบด้วย ส่วนสำหรับส่วนของงบดุลแบบดั้งเดิมแต่ละส่วน</span><span class="sxs-lookup"><span data-stu-id="ceab1-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="ceab1-131">รายงานที่อยู่เคียงข้างกันรวมตัวแบ่งคอลัมน์ เพื่อให้หนี้สินและส่วนของผู้ถือหุ้นของเจ้าของปรากฏอยู่ติดกับสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ceab1-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="ceab1-132">มิติประเภทบัญชีหลักถูกใช้ในการสร้างคำนิยามของแถวทั้งสองแถว</span><span class="sxs-lookup"><span data-stu-id="ceab1-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="ceab1-133">ดังนั้น ใครก็ตามสามารถสร้างรายงานได้โดยไม่ต้องทำการปรับเปลี่ยนใดๆ</span><span class="sxs-lookup"><span data-stu-id="ceab1-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="ceab1-134">คำนิยามคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="ceab1-134">Column definition</span></span>

<span data-ttu-id="ceab1-135">คำนิยามของคอลัมน์ประกอบด้วย ชนิดที่แตกต่างกันของคอลัมน์เพื่อให้ระดับที่แตกต่างกันของรายละเอียดและข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ceab1-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="ceab1-136">**YTD และผลต่าง – ชนิดของคอลัมน์เริ่มต้น:**</span><span class="sxs-lookup"><span data-stu-id="ceab1-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="ceab1-137">**DESC** – คำอธิบายจากคำนิยามของแถว</span><span class="sxs-lookup"><span data-stu-id="ceab1-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="ceab1-138">**FD** – ข้อมูลทางการเงินตั้งแต่ต้นปีจนถึงปัจจุบันสำหรับปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ceab1-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="ceab1-139">**FD** – ข้อมูลทางการเงินตั้งแต่ต้นปีจนถึงปัจจุบันสำหรับปีที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="ceab1-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="ceab1-140">**CALC**– ผลต่างจากการลบปีที่ผ่านมาออกจากปีนี้</span><span class="sxs-lookup"><span data-stu-id="ceab1-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="ceab1-141">**คอลัมน์ตั้งแต่ต้นปีจนถึงปัจจุบัน - ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="ceab1-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="ceab1-142">**DESC** – คำอธิบายจากคำนิยามของแถว</span><span class="sxs-lookup"><span data-stu-id="ceab1-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="ceab1-143">**FD** – ข้อมูลทางการเงินตั้งแต่ต้นปีจนถึงปัจจุบันสำหรับปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ceab1-143">**FD** – Year-to-date financial data for the current year</span></span>

 

<a name="see-also"></a><span data-ttu-id="ceab1-144">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="ceab1-144">See also</span></span>
--------

[<span data-ttu-id="ceab1-145">การรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ceab1-145">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="ceab1-146">ดูรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ceab1-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="ceab1-147">บล็อกการรายงานทางการเงิน Dynamics</span><span class="sxs-lookup"><span data-stu-id="ceab1-147">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




