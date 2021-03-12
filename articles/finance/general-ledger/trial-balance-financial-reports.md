---
title: รายงานทางการเงินของงบทดลอง
description: บทความนี้อธิบายรายงานเริ่มต้นสำหรับงบทดลอง นอกจากนี้ยังอธิบายถึงบล็อคส่วนประกอบที่เกี่ยวข้องกับรายงานเหล่านี้และวิธีที่คุณสามารถปรับเปลี่ยนรายงานให้พอดีกับความต้องการทางธุรกิจของคุณ
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25a90a137ea3f6dfa43f401354780d99b2fda8fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978497"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="37413-104">รายงานทางการเงินของงบทดลอง</span><span class="sxs-lookup"><span data-stu-id="37413-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37413-105">บทความนี้อธิบายรายงานเริ่มต้นสำหรับงบทดลอง</span><span class="sxs-lookup"><span data-stu-id="37413-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="37413-106">นอกจากนี้ยังอธิบายถึงบล็อคส่วนประกอบที่เกี่ยวข้องกับรายงานเหล่านี้และวิธีที่คุณสามารถปรับเปลี่ยนรายงานให้พอดีกับความต้องการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="37413-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="37413-107">รายงานงบทดลองเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="37413-108">รายงานงบทดลองสามฉบับจะพร้อมใช้งานในการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="37413-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="37413-109">รายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-109">Default report</span></span>                                 | <span data-ttu-id="37413-110">สิ่งที่ทำ</span><span class="sxs-lookup"><span data-stu-id="37413-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37413-111">งบทดลองโดยละเอียด – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="37413-112">ให้ข้อมูลยอดดุลสำหรับบัญชีทั้งหมด และรวมยอดดุลเดบิตและเครดิต และมูลค่าสุทธิของยอดดุลเหล่านี้ เข้ากับวันที่ทำธุรกรรม ใบสำคัญ และคำอธิบายเกี่ยวกับสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="37413-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="37413-113">สรุปงบทดลอง – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="37413-114">ให้ข้อมูลยอดดุลสำหรับบัญชีทั้งหมด และรวมยอดดุลยกมาและยอดดุลปิดบัญชี และยอดดุลเดบิตและเครดิต เข้ากับผลต่างสุทธิ</span><span class="sxs-lookup"><span data-stu-id="37413-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="37413-115">สรุปงบทดลองปีต่อปี – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="37413-116">ให้ข้อมูลยอดดุลสำหรับบัญชีทั้งหมด และรวมยอดดุลยกมาและยอดดุลปิดบัญชี และยอดดุลเดบิตและเครดิต เข้ากับผลต่างสุทธิสำหรับปีปัจจุบันและปีที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="37413-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="37413-117">ส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="37413-117">Building blocks</span></span>
<span data-ttu-id="37413-118">รายงานทางการเงินของงบทดลองใช้ส่วนประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="37413-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="37413-119">รายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-119">Default report</span></span>                                 | <span data-ttu-id="37413-120">คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="37413-120">Row definition</span></span>          | <span data-ttu-id="37413-121">คำนิยามคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="37413-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="37413-122">งบทดลองโดยละเอียด – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="37413-123">งบทดลอง - ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-123">Trial Balance - Default</span></span> | <span data-ttu-id="37413-124">งบทดลองโดยละเอียด – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="37413-125">สรุปงบทดลอง – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="37413-126">งบทดลอง - ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-126">Trial Balance - Default</span></span> | <span data-ttu-id="37413-127">สรุปงบทดลอง – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="37413-128">สรุปงบทดลองปีต่อปี – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="37413-129">งบทดลอง - ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-129">Trial Balance - Default</span></span> | <span data-ttu-id="37413-130">สรุปงบทดลองปีต่อปี – ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="37413-131">คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="37413-131">Row definition</span></span>

<span data-ttu-id="37413-132">คำนิยามของแถว งบทดลอง – ค่าเริ่มต้น ประกอบด้วย แถวหนึ่งแถวที่รวมบัญชีหลักทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="37413-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="37413-133">ดังนั้น ใครก็ตามสามารถสร้างรายงาน โดยไม่ต้องทำการปรับเปลี่ยนใด ๆ</span><span class="sxs-lookup"><span data-stu-id="37413-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="37413-134">เมื่อคุณดูรายงาน คุณเข้าถึงรายละเอียดแถวเดี่ยวเพื่อดูรายละเอียดเกี่ยวกับบัญชีแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="37413-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="37413-135">คุณสามารถปรับเปลี่ยนคำนิยามของแถวเพื่อให้รวมรายละเอียดมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="37413-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="37413-136">เพื่อแก้ไขงบทดลอง – คำนิยามของแถวเริ่มต้นเพื่อให้รวมแถวสำหรับบัญชีทั้งหมด ให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="37413-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="37413-137">คลิก **แก้ไข** และจากนั้นคลิก **แทรกแถวจากมิติ**</span><span class="sxs-lookup"><span data-stu-id="37413-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="37413-138">คำสั่ง **แทรกแถวจากมิติ** ช่วยให้คุณสามารถเลือกมิติที่คุณต้องการให้มีในคำนิยามของแถวของคุณ</span><span class="sxs-lookup"><span data-stu-id="37413-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="37413-139">สำหรับคำนิยามของแถวนี้ คุณจะใช้ **บัญชีหลัก**</span><span class="sxs-lookup"><span data-stu-id="37413-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="37413-140">ตรวจสอบให้แน่ใจว่าว่า **บัญชีหลัก** ประกอบด้วยเครื่องหมายและ (&) และจากนั้นคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="37413-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="37413-141">คำนิยามของแถวในขณะนี้ประกอบด้วยบัญชีหลักสำหรับนิติบุคคลเริ่มต้นของคุณทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="37413-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="37413-142">คำนิยามคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="37413-142">Column definition</span></span>

<span data-ttu-id="37413-143">รายงานงบทดลองแต่ละรายการใช้คำนิยามของคอลัมน์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="37413-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="37413-144">คำนิยามของคอลัมน์เหล่านี้ประกอบด้วย ชนิดที่แตกต่างกันของคอลัมน์เพื่อให้ระดับที่แตกต่างกันของรายละเอียดและข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="37413-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="37413-145">**งบทดลองโดยละเอียด – ชนิดของคอลัมน์เริ่มต้น:**</span><span class="sxs-lookup"><span data-stu-id="37413-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="37413-146">**DESC** – คำอธิบายจากคำนิยามของแถว</span><span class="sxs-lookup"><span data-stu-id="37413-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="37413-147">**ACCT** – รหัสบัญชี</span><span class="sxs-lookup"><span data-stu-id="37413-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="37413-148">**ATTR (3)** – แอททริบิวต์:</span><span class="sxs-lookup"><span data-stu-id="37413-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="37413-149">วันที่ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="37413-149">Transaction Date</span></span>
        -   <span data-ttu-id="37413-150">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="37413-150">Voucher</span></span>
        -   <span data-ttu-id="37413-151">คำอธิบายสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="37413-151">Journal Description</span></span>
    -   <span data-ttu-id="37413-152">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเดบิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="37413-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="37413-153">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเครดิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="37413-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="37413-154">**CALC** – ผลต่างสุทธิ</span><span class="sxs-lookup"><span data-stu-id="37413-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="37413-155">**สรุปงบทดลอง – ชนิดของคอลัมน์เริ่มต้น:**</span><span class="sxs-lookup"><span data-stu-id="37413-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="37413-156">**ACCT** – รหัสบัญชี</span><span class="sxs-lookup"><span data-stu-id="37413-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="37413-157">**DESC** – คำอธิบายจากคำนิยามของแถว</span><span class="sxs-lookup"><span data-stu-id="37413-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="37413-158">**ATTR** – แอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="37413-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="37413-159">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="37413-159">Voucher</span></span>
    -   <span data-ttu-id="37413-160">**FD** – ข้อมูลทางการเงินของยอดดุลเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="37413-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="37413-161">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเดบิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="37413-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="37413-162">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเครดิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="37413-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="37413-163">**CALC** – ผลต่างสุทธิ</span><span class="sxs-lookup"><span data-stu-id="37413-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="37413-164">**CALC** – ยอดดุลปิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="37413-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="37413-165">**สรุปงบทดลองปีต่อปี – ค่าเริ่มต้น:**</span><span class="sxs-lookup"><span data-stu-id="37413-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="37413-166">**ACCT** – รหัสบัญชี</span><span class="sxs-lookup"><span data-stu-id="37413-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="37413-167">**DESC** – คำอธิบายจากคำนิยามของแถว</span><span class="sxs-lookup"><span data-stu-id="37413-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="37413-168">**ATTR** – แอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="37413-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="37413-169">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="37413-169">Voucher</span></span>
    -   <span data-ttu-id="37413-170">**FD** – ข้อมูลทางการเงินของยอดดุลเริ่มต้นสำหรับปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="37413-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="37413-171">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเดบิตเท่านั้นสำหรับปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="37413-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="37413-172">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเครดิตเท่านั้นสำหรับปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="37413-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="37413-173">**CALC** – ผลต่างสุทธิ</span><span class="sxs-lookup"><span data-stu-id="37413-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="37413-174">**CALC** – ยอดดุลปิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="37413-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="37413-175">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเดบิตเท่านั้นสำหรับปีที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="37413-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="37413-176">**FD** – ข้อมูลทางการเงินที่ประกอบด้วยเครดิตเท่านั้นสำหรับปีที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="37413-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="37413-177">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="37413-177">Additional resources</span></span>
--------

[<span data-ttu-id="37413-178">ภาพรวมของการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="37413-178">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="37413-179">ดูรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="37413-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="37413-180">บล็อกการรายงานทางการเงิน Dynamics</span><span class="sxs-lookup"><span data-stu-id="37413-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



