---
title: "รายงานทางการเงินของงบทดลอง"
description: "บทความนี้อธิบายรายงานเริ่มต้นสำหรับงบทดลอง นอกจากนี้ยังอธิบายถึงบล็อคส่วนประกอบที่เกี่ยวข้องกับรายงานเหล่านี้และวิธีที่คุณสามารถปรับเปลี่ยนรายงานให้พอดีกับความต้องการทางธุรกิจของคุณ"
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
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6405599186c8d07ac5ade19d3b7d27ae83b036ff
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="trial-balance-financial-reports"></a><span data-ttu-id="69952-104">รายงานทางการเงินของงบทดลอง</span><span class="sxs-lookup"><span data-stu-id="69952-104">Trial balance financial reports</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="69952-105">บทความนี้อธิบายรายงานเริ่มต้นสำหรับงบทดลอง</span><span class="sxs-lookup"><span data-stu-id="69952-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="69952-106">นอกจากนี้ยังอธิบายถึงบล็อคส่วนประกอบที่เกี่ยวข้องกับรายงานเหล่านี้และวิธีที่คุณสามารถปรับเปลี่ยนรายงานให้พอดีกับความต้องการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="69952-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="69952-107">รายงานงบทดลองเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="69952-108">รายงานงบทดลองสามรายงานจะพร้อมใช้งานในการรายงานทางการเงินใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="69952-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

| <span data-ttu-id="69952-109">รายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-109">Default report</span></span>                                 | <span data-ttu-id="69952-110">สิ่งที่ทำ</span><span class="sxs-lookup"><span data-stu-id="69952-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69952-111">งบทดลองโดยละเอียด – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="69952-112">ให้ข้อมูลยอดดุลสำหรับบัญชีทั้งหมด และรวมยอดดุลเดบิตและเครดิต และมูลค่าสุทธิของยอดดุลเหล่านี้ เข้ากับวันที่ทำธุรกรรม ใบสำคัญ และคำอธิบายเกี่ยวกับสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69952-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="69952-113">สรุปงบทดลอง – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="69952-114">ให้ข้อมูลยอดดุลสำหรับบัญชีทั้งหมด และรวมยอดดุลยกมาและยอดดุลปิดบัญชี และยอดดุลเดบิตและเครดิต เข้ากับผลต่างสุทธิ</span><span class="sxs-lookup"><span data-stu-id="69952-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="69952-115">สรุปงบทดลองปีต่อปี – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="69952-116">ให้ข้อมูลยอดดุลสำหรับบัญชีทั้งหมด และรวมยอดดุลยกมาและยอดดุลปิดบัญชี และยอดดุลเดบิตและเครดิต เข้ากับผลต่างสุทธิสำหรับปีปัจจุบันและปีที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="69952-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="69952-117">ส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69952-117">Building blocks</span></span>
<span data-ttu-id="69952-118">รายงานทางการเงินของงบทดลองใช้ส่วนประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="69952-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="69952-119">รายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-119">Default report</span></span>                                 | <span data-ttu-id="69952-120">คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="69952-120">Row definition</span></span>          | <span data-ttu-id="69952-121">คำนิยามคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="69952-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="69952-122">งบทดลองโดยละเอียด – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="69952-123">งบทดลอง - ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-123">Trial Balance - Default</span></span> | <span data-ttu-id="69952-124">งบทดลองโดยละเอียด – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="69952-125">สรุปงบทดลอง – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="69952-126">งบทดลอง - ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-126">Trial Balance - Default</span></span> | <span data-ttu-id="69952-127">สรุปงบทดลอง – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="69952-128">สรุปงบทดลองปีต่อปี – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="69952-129">งบทดลอง - ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-129">Trial Balance - Default</span></span> | <span data-ttu-id="69952-130">สรุปงบทดลองปีต่อปี – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="69952-131">คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="69952-131">Row definition</span></span>

<span data-ttu-id="69952-132">คำนิยามของแถว งบทดลอง – ค่าเริ่มต้น ประกอบด้วย แถวหนึ่งแถวที่รวมบัญชีหลักทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="69952-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="69952-133">ดังนั้น ใครก็ตามสามารถสร้างรายงาน โดยไม่ต้องทำการปรับเปลี่ยนใด ๆ</span><span class="sxs-lookup"><span data-stu-id="69952-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="69952-134">เมื่อคุณดูรายงาน คุณเข้าถึงรายละเอียดแถวเดี่ยวเพื่อดูรายละเอียดเกี่ยวกับบัญชีแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="69952-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="69952-135">คุณสามารถปรับเปลี่ยนคำนิยามของแถวเพื่อให้รวมรายละเอียดมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="69952-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="69952-136">เพื่อแก้ไขงบทดลอง – คำนิยามของแถวเริ่มต้นเพื่อให้รวมแถวสำหรับบัญชีทั้งหมด ให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="69952-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="69952-137">คลิก **แก้ไข** และจากนั้นคลิก **แทรกแถวจากมิติ**</span><span class="sxs-lookup"><span data-stu-id="69952-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="69952-138">คำสั่ง **แทรกแถวจากมิติ** ช่วยให้คุณสามารถเลือกมิติที่คุณต้องการให้มีในคำนิยามของแถวของคุณ</span><span class="sxs-lookup"><span data-stu-id="69952-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="69952-139">สำหรับคำนิยามของแถวนี้ คุณจะใช้ **บัญชีหลัก**</span><span class="sxs-lookup"><span data-stu-id="69952-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="69952-140">ตรวจสอบให้แน่ใจว่าว่า **บัญชีหลัก** ประกอบด้วยเครื่องหมายและ (&) และจากนั้นคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="69952-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="69952-141">คำนิยามของแถวในขณะนี้ประกอบด้วยบัญชีหลักสำหรับนิติบุคคลเริ่มต้นของคุณทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="69952-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="69952-142">คำนิยามคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="69952-142">Column definition</span></span>

<span data-ttu-id="69952-143">รายงานงบทดลองแต่ละรายการใช้คำนิยามของคอลัมน์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="69952-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="69952-144">คำนิยามของคอลัมน์เหล่านี้ประกอบด้วย ชนิดที่แตกต่างกันของคอลัมน์เพื่อให้ระดับที่แตกต่างกันของรายละเอียดและข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="69952-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="69952-145">**งบทดลองโดยละเอียด – ชนิดของคอลัมน์เริ่มต้น:**</span><span class="sxs-lookup"><span data-stu-id="69952-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="69952-146">**DESC** – คำอธิบายจากคำนิยามของแถว</span><span class="sxs-lookup"><span data-stu-id="69952-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="69952-147">**ACCT** – รหัสบัญชี</span><span class="sxs-lookup"><span data-stu-id="69952-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="69952-148">**ATTR (3)** – แอททริบิวต์:</span><span class="sxs-lookup"><span data-stu-id="69952-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="69952-149">วันที่ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="69952-149">Transaction Date</span></span>
        -   <span data-ttu-id="69952-150">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="69952-150">Voucher</span></span>
        -   <span data-ttu-id="69952-151">คำอธิบายสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69952-151">Journal Description</span></span>
    -   <span data-ttu-id="69952-152">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเดบิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="69952-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="69952-153">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเครดิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="69952-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="69952-154">**CALC** – ผลต่างสุทธิ</span><span class="sxs-lookup"><span data-stu-id="69952-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="69952-155">**สรุปงบทดลอง – ชนิดของคอลัมน์เริ่มต้น:**</span><span class="sxs-lookup"><span data-stu-id="69952-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="69952-156">**ACCT** – รหัสบัญชี</span><span class="sxs-lookup"><span data-stu-id="69952-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="69952-157">**DESC** – คำอธิบายจากคำนิยามของแถว</span><span class="sxs-lookup"><span data-stu-id="69952-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="69952-158">**ATTR** – แอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="69952-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="69952-159">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="69952-159">Voucher</span></span>
    -   <span data-ttu-id="69952-160">**FD** – ข้อมูลทางการเงินของยอดดุลเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69952-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="69952-161">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเดบิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="69952-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="69952-162">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเครดิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="69952-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="69952-163">**CALC** – ผลต่างสุทธิ</span><span class="sxs-lookup"><span data-stu-id="69952-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="69952-164">**CALC** – ยอดดุลปิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="69952-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="69952-165">**สรุปงบทดลองปีต่อปี – ค่าเริ่มต้น:**</span><span class="sxs-lookup"><span data-stu-id="69952-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="69952-166">**ACCT** – รหัสบัญชี</span><span class="sxs-lookup"><span data-stu-id="69952-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="69952-167">**DESC** – คำอธิบายจากคำนิยามของแถว</span><span class="sxs-lookup"><span data-stu-id="69952-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="69952-168">**ATTR** – แอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="69952-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="69952-169">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="69952-169">Voucher</span></span>
    -   <span data-ttu-id="69952-170">**FD** – ข้อมูลทางการเงินของยอดดุลเริ่มต้นสำหรับปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="69952-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="69952-171">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเดบิตเท่านั้นสำหรับปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="69952-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="69952-172">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเครดิตเท่านั้นสำหรับปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="69952-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="69952-173">**CALC** – ผลต่างสุทธิ</span><span class="sxs-lookup"><span data-stu-id="69952-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="69952-174">**CALC** – ยอดดุลปิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="69952-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="69952-175">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเดบิตเท่านั้นสำหรับปีที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="69952-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="69952-176">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเครดิตเท่านั้นสำหรับปีที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="69952-176">**FD** – Financial data that contains only credits for the last year</span></span>

 

<a name="see-also"></a><span data-ttu-id="69952-177">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="69952-177">See also</span></span>
--------

[<span data-ttu-id="69952-178">การรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="69952-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="69952-179">ดูรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="69952-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="69952-180">บล็อกการรายงานทางการเงิน Dynamics</span><span class="sxs-lookup"><span data-stu-id="69952-180">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




