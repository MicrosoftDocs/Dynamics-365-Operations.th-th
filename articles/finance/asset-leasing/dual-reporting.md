---
title: การรายงานแบบคู่
description: หัวข้อนี้จะให้คำแนะนำเกี่ยวกับวิธีการที่คุณสามารถตอบสนองความต้องการสำหรับการรายงานมาตรฐาน Financial Reporting ระหว่างประเทศ (IFRS) และการรายงานตามกฎหมายในการเช่าสินทรัพย์
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c9f2bae330e688e1e941277d46ddcbd38916f8c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815991"
---
# <a name="dual-reporting"></a><span data-ttu-id="4234e-103">การรายงานแบบคู่</span><span class="sxs-lookup"><span data-stu-id="4234e-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4234e-104">หัวข้อนี้จะให้คำแนะนำเกี่ยวกับวิธีการที่คุณสามารถตอบสนองความต้องการสำหรับการรายงานมาตรฐาน Financial Reporting ระหว่างประเทศ (IFRS) และการรายงานตามกฎหมายในการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4234e-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="4234e-105">ความคุ้นเคยกับชั้นของการลงรายการบัญชีใน Microsoft Dynamics 365 Finance จำเป็นต้องใช้และจะทำให้เข้าใจง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="4234e-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="4234e-106">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="4234e-106">Example</span></span>

<span data-ttu-id="4234e-107">บัญชีตัวอย่างต่อไปนี้สำหรับการเช่าภายใต้การรายงานทางกฎหมายของอิตาลีโดยใช้ทั้งวิธีการเงินสดเป็นพื้นฐานและวิธีการรายงาน IFRS</span><span class="sxs-lookup"><span data-stu-id="4234e-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="4234e-108">บริษัทต้องสร้างสมุดบัญชีสามเล่มให้กับบัญชีสำหรับทั้งข้อกำหนดตามกฎหมายอิตาลีและข้อกำหนด IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4234e-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="4234e-109">ต้องมีสมุดบัญชีหนึ่งเล่มสำหรับ IFRS 16 สมุดบัญชีหนึ่งเล่มจำเป็นสำหรับข้อกำหนดตามกฎหมาย และต้องมีสมุดบัญชีหนึ่งเล่มเพื่อย้อนกลับการลงรายการบัญชีตามกฎหมายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4234e-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="4234e-110">จะมีการตั้งค่าสมุดบัญชีดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4234e-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="4234e-111">**สมุดบัญชี IFRS 16**</span><span class="sxs-lookup"><span data-stu-id="4234e-111">**IFRS 16 book**</span></span>

<span data-ttu-id="4234e-112">มีการตั้งค่าสมุดบัญชี IFRS 16 ดังนั้นจึงสอดคล้องกับมาตรฐานการบัญชี IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4234e-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="4234e-113">รายการทั้งหมดที่มีการลงรายการบัญชีในสมุดบัญชีนี้จะได้รับการลงรายการบัญชีในชั้นแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="4234e-114">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4234e-114">Name</span></span>                                    | <span data-ttu-id="4234e-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4234e-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="4234e-116">ชนิดของสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-116">Book type</span></span>                               | <span data-ttu-id="4234e-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4234e-117">IFRS 16</span></span>        |
| <span data-ttu-id="4234e-118">คำอธิบายสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-118">Book description</span></span>                        | <span data-ttu-id="4234e-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4234e-119">IFRS 16</span></span>        |
| <span data-ttu-id="4234e-120">ชั้นของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-120">Posting Layer</span></span>                           | <span data-ttu-id="4234e-121">ชั้นที่กำหนดเอง 1</span><span class="sxs-lookup"><span data-stu-id="4234e-121">Custom layer 1</span></span> |
| <span data-ttu-id="4234e-122">ชนิดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="4234e-122">Lease Type</span></span>                              | <span data-ttu-id="4234e-123">Finance</span><span class="sxs-lookup"><span data-stu-id="4234e-123">Finance</span></span>        |
| <span data-ttu-id="4234e-124">กรอบงานการบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-124">Accounting Framework</span></span>                    | <span data-ttu-id="4234e-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4234e-125">IFRS 16</span></span>        |
| <span data-ttu-id="4234e-126">การตั้งค่าระยะเวลาของสัญญาเช่า / อายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4234e-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="4234e-127">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-127">0.00</span></span>           |
| <span data-ttu-id="4234e-128">การตั้งค่ามูลค่าปัจจุบัน / มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4234e-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="4234e-129">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-129">0.00</span></span>           |
| <span data-ttu-id="4234e-130">ขีดจำกัดระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="4234e-130">Short-term threshold</span></span>                    | <span data-ttu-id="4234e-131">12</span><span class="sxs-lookup"><span data-stu-id="4234e-131">12</span></span>             |
| <span data-ttu-id="4234e-132">ขีดจำกัดมูลค่าต่ำ</span><span class="sxs-lookup"><span data-stu-id="4234e-132">Low Value Threshold</span></span>                     | <span data-ttu-id="4234e-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-133">5,000.00</span></span>       |
| <span data-ttu-id="4234e-134">จ่ายให้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="4234e-134">Pay to Vendor</span></span>                           | <span data-ttu-id="4234e-135">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="4234e-135">No</span></span>             |

<span data-ttu-id="4234e-136">**สมุดบัญชีตามกฎหมาย**</span><span class="sxs-lookup"><span data-stu-id="4234e-136">**Statutory book**</span></span>

<span data-ttu-id="4234e-137">สมุดบัญชีตามกฎหมายเป็นสมุดบัญชีเงินสดซึ่งบริษัทจะเป็นผู้ชำระค่าใช้จ่ายในการเช่าโดยมียอดเงินสดที่ชำระให้แก่ลูกค้าแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="4234e-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="4234e-138">สมุดบัญชีเล่มนี้จะไม่ทำให้เกิดสิทธิ์การใช้สินทรัพย์หรือหนี้สินสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="4234e-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="4234e-139">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4234e-139">Name</span></span>                                    | <span data-ttu-id="4234e-140">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4234e-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="4234e-141">ชนิดของสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-141">Book type</span></span>                               | <span data-ttu-id="4234e-142">ตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="4234e-142">Statutory</span></span>   |
| <span data-ttu-id="4234e-143">คำอธิบายสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-143">Book description</span></span>                        | <span data-ttu-id="4234e-144">GAAP ท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="4234e-144">Local GAAP</span></span>  |
| <span data-ttu-id="4234e-145">ชั้นของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-145">Posting Layer</span></span>                           | <span data-ttu-id="4234e-146">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-146">Current</span></span>     |
| <span data-ttu-id="4234e-147">ชนิดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="4234e-147">Lease Type</span></span>                              | <span data-ttu-id="4234e-148">อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4234e-148">Automatic</span></span>   |
| <span data-ttu-id="4234e-149">กรอบงานการบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-149">Accounting Framework</span></span>                    | <span data-ttu-id="4234e-150">เกณฑ์เงินสด</span><span class="sxs-lookup"><span data-stu-id="4234e-150">Cash basis</span></span>  |
| <span data-ttu-id="4234e-151">การตั้งค่าระยะเวลาของสัญญาเช่า / อายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4234e-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="4234e-152">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-152">0.00</span></span>        |
| <span data-ttu-id="4234e-153">การตั้งค่ามูลค่าปัจจุบัน / มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4234e-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="4234e-154">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-154">0.00</span></span>        |
| <span data-ttu-id="4234e-155">ขีดจำกัดระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="4234e-155">Short-term threshold</span></span>                    | <span data-ttu-id="4234e-156">0</span><span class="sxs-lookup"><span data-stu-id="4234e-156">0</span></span>           |
| <span data-ttu-id="4234e-157">ขีดจำกัดมูลค่าต่ำ</span><span class="sxs-lookup"><span data-stu-id="4234e-157">Low Value Threshold</span></span>                     | <span data-ttu-id="4234e-158">0</span><span class="sxs-lookup"><span data-stu-id="4234e-158">0</span></span>           |
| <span data-ttu-id="4234e-159">จ่ายให้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="4234e-159">Pay to Vendor</span></span>                           | <span data-ttu-id="4234e-160">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="4234e-160">No</span></span>          |

<span data-ttu-id="4234e-161">**สมุดบัญชีการกลับรายการตามกฎหมาย**</span><span class="sxs-lookup"><span data-stu-id="4234e-161">**Statutory reversal book**</span></span>

<span data-ttu-id="4234e-162">สมุดบัญชีการกลับรายการตามกฎหมายถูกตั้งค่าในลักษณะเดียวกับสมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="4234e-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="4234e-163">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4234e-163">Name</span></span>                                    | <span data-ttu-id="4234e-164">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4234e-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="4234e-165">ชนิดของสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-165">Book type</span></span>                               | <span data-ttu-id="4234e-166">ตามกฎหมาย – การกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="4234e-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="4234e-167">คำอธิบายสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-167">Book description</span></span>                        | <span data-ttu-id="4234e-168">จองเพื่อกลับรายการสมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="4234e-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="4234e-169">ชั้นของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-169">Posting Layer</span></span>                           | <span data-ttu-id="4234e-170">ชั้นที่กำหนดเอง 1</span><span class="sxs-lookup"><span data-stu-id="4234e-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="4234e-171">ชนิดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="4234e-171">Lease Type</span></span>                              | <span data-ttu-id="4234e-172">อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4234e-172">Automatic</span></span>                      |
| <span data-ttu-id="4234e-173">กรอบงานการบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-173">Accounting Framework</span></span>                    | <span data-ttu-id="4234e-174">เกณฑ์เงินสด</span><span class="sxs-lookup"><span data-stu-id="4234e-174">Cash basis</span></span>                     |
| <span data-ttu-id="4234e-175">การตั้งค่าระยะเวลาของสัญญาเช่า / อายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4234e-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="4234e-176">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-176">0.00</span></span>                           |
| <span data-ttu-id="4234e-177">การตั้งค่ามูลค่าปัจจุบัน / มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4234e-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="4234e-178">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-178">0.00</span></span>                           |
| <span data-ttu-id="4234e-179">ขีดจำกัดระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="4234e-179">Short-term threshold</span></span>                    | <span data-ttu-id="4234e-180">0</span><span class="sxs-lookup"><span data-stu-id="4234e-180">0</span></span>                              |
| <span data-ttu-id="4234e-181">ขีดจำกัดมูลค่าต่ำ</span><span class="sxs-lookup"><span data-stu-id="4234e-181">Low Value Threshold</span></span>                     | <span data-ttu-id="4234e-182">0</span><span class="sxs-lookup"><span data-stu-id="4234e-182">0</span></span>                              |
| <span data-ttu-id="4234e-183">จ่ายให้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="4234e-183">Pay to Vendor</span></span>                           | <span data-ttu-id="4234e-184">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="4234e-184">No</span></span>                             |

<span data-ttu-id="4234e-185">สำหรับตัวอย่างนี้ มีการสร้างการเช่าที่มีการตั้งค่าต่อไปนี้ในแท็บ **ทั่วไป** และ **รายการกำหนดการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="4234e-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="4234e-186">**แท็บทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="4234e-186">**General tab**</span></span>

| <span data-ttu-id="4234e-187">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="4234e-187">Field</span></span>                      | <span data-ttu-id="4234e-188">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="4234e-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="4234e-189">อัตราดอกเบี้ยเงินกู้ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4234e-189">Incremental borrowing rate</span></span> | <span data-ttu-id="4234e-190">5%</span><span class="sxs-lookup"><span data-stu-id="4234e-190">5%</span></span>               |
| <span data-ttu-id="4234e-191">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4234e-191">Commencement date</span></span>          | <span data-ttu-id="4234e-192">วันที่ 1/1/2020</span><span class="sxs-lookup"><span data-stu-id="4234e-192">1/1/2020</span></span>         |
| <span data-ttu-id="4234e-193">กลุ่มสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="4234e-193">Lease group</span></span>                | <span data-ttu-id="4234e-194">อาคาร</span><span class="sxs-lookup"><span data-stu-id="4234e-194">Buildings</span></span>        |
| <span data-ttu-id="4234e-195">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="4234e-195">Vendor</span></span>                     | <span data-ttu-id="4234e-196">1001</span><span class="sxs-lookup"><span data-stu-id="4234e-196">1001</span></span>             |
| <span data-ttu-id="4234e-197">มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4234e-197">Fair value of the asset</span></span>    | <span data-ttu-id="4234e-198">245,000</span><span class="sxs-lookup"><span data-stu-id="4234e-198">245,000</span></span>          |
| <span data-ttu-id="4234e-199">อายุการใช้งานของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4234e-199">Asset useful life</span></span>          | <span data-ttu-id="4234e-200">120</span><span class="sxs-lookup"><span data-stu-id="4234e-200">120</span></span>              |
| <span data-ttu-id="4234e-201">ชนิดเงินรายปี</span><span class="sxs-lookup"><span data-stu-id="4234e-201">Annuity type</span></span>               | <span data-ttu-id="4234e-202">เงินรายปีสามัญ</span><span class="sxs-lookup"><span data-stu-id="4234e-202">Ordinary annuity</span></span> |
| <span data-ttu-id="4234e-203">ช่วงเวลาการทบต้น</span><span class="sxs-lookup"><span data-stu-id="4234e-203">Compounding interval</span></span>       | <span data-ttu-id="4234e-204">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="4234e-204">Monthly</span></span>          |

<span data-ttu-id="4234e-205">**แท็บรายการกำหนดการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="4234e-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="4234e-206">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="4234e-206">Field</span></span>             | <span data-ttu-id="4234e-207">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="4234e-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="4234e-208">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4234e-208">Start date</span></span>        | <span data-ttu-id="4234e-209">วันที่ 1/1/2020</span><span class="sxs-lookup"><span data-stu-id="4234e-209">1/1/2020</span></span>   |
| <span data-ttu-id="4234e-210">ช่วงรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="4234e-210">Period interval</span></span>   | <span data-ttu-id="4234e-211">เดือน</span><span class="sxs-lookup"><span data-stu-id="4234e-211">Months</span></span>     |
| <span data-ttu-id="4234e-212">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="4234e-212">Periods</span></span>           | <span data-ttu-id="4234e-213">24</span><span class="sxs-lookup"><span data-stu-id="4234e-213">24</span></span>         |
| <span data-ttu-id="4234e-214">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="4234e-214">End date</span></span>          | <span data-ttu-id="4234e-215">วันที่ 12/31/2020</span><span class="sxs-lookup"><span data-stu-id="4234e-215">12/31/2020</span></span> |
| <span data-ttu-id="4234e-216">ความถี่ในการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4234e-216">Payment frequency</span></span> | <span data-ttu-id="4234e-217">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="4234e-217">Monthly</span></span>    |
| <span data-ttu-id="4234e-218">ยอดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4234e-218">Payment amount</span></span>    | <span data-ttu-id="4234e-219">1,000</span><span class="sxs-lookup"><span data-stu-id="4234e-219">1,000</span></span>      |

<span data-ttu-id="4234e-220">ในการลงบัญชีสำหรับชั่การเช่านี้ภายใต้สองกรอบงาน คุณใช้ชั้นของการลงรายการบัญชีปัจจุบันและชั้นของการลงรายการบัญชีที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="4234e-221">ตารางต่อไปนี้จะแสดงตัวอย่างของรายการสมุดรายวันทั้งหมดที่จำเป็นต้องแสดงถึงการเงินภายใต้มาตรฐานการรายงานแต่ละฉบับ</span><span class="sxs-lookup"><span data-stu-id="4234e-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="4234e-222">คำอธิบายโดยละเอียดของรายการสมุดรายวันแต่ละรายการสำหรับเดือนแรกของการเช่ามีให้หลังจากนี้</span><span class="sxs-lookup"><span data-stu-id="4234e-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="4234e-223">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="4234e-224">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4234e-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="4234e-225">สมุดบัญชีตามกฎหมาย (ชั้นปัจจุบัน)</span><span class="sxs-lookup"><span data-stu-id="4234e-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="4234e-226">ผลรวมชั้นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-226">Current layer total</span></span></th>
<th><span data-ttu-id="4234e-227">สมุดบัญชีการกลับรายการ (ชั้นที่กำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="4234e-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="4234e-228">สมุดบัญชี IFRS 16 (ชั้นที่กำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="4234e-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="4234e-229">ชั้นปัจจุบัน + ยอดรวมชั้นแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4234e-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="4234e-230">JE-100</span></span></th>
<th><span data-ttu-id="4234e-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="4234e-231">JE-110</span></span></th>
<th><span data-ttu-id="4234e-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="4234e-232">JE-120</span></span></th>
<th><span data-ttu-id="4234e-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="4234e-233">JE-130</span></span></th>
<th><span data-ttu-id="4234e-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="4234e-234">JE-140</span></span></th>
<th><span data-ttu-id="4234e-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="4234e-235">JE-150</span></span></th>
<th><span data-ttu-id="4234e-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="4234e-236">JE-160</span></span></th>
<th><span data-ttu-id="4234e-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="4234e-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4234e-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4234e-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4234e-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4234e-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4234e-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4234e-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4234e-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4234e-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4234e-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4234e-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4234e-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4234e-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4234e-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4234e-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4234e-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4234e-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4234e-246">1</span><span class="sxs-lookup"><span data-stu-id="4234e-246">1</span></span></td>
<td><span data-ttu-id="4234e-247">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="4234e-247">Lease expense</span></span></td>
<td><span data-ttu-id="4234e-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-249">1,000.00</span></span></td>
<td><span data-ttu-id="4234e-250">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="4234e-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-251">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-252">2</span><span class="sxs-lookup"><span data-stu-id="4234e-252">2</span></span></td>
<td><span data-ttu-id="4234e-253">ค่าธรรมเนียมของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4234e-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-254">3.00</span><span class="sxs-lookup"><span data-stu-id="4234e-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-255">3.00</span><span class="sxs-lookup"><span data-stu-id="4234e-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-256">3.00</span><span class="sxs-lookup"><span data-stu-id="4234e-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-257">3</span><span class="sxs-lookup"><span data-stu-id="4234e-257">3</span></span></td>
<td><span data-ttu-id="4234e-258">ค่าใช้จ่าย VAT</span><span class="sxs-lookup"><span data-stu-id="4234e-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-259">5.00</span><span class="sxs-lookup"><span data-stu-id="4234e-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-260">5.00</span><span class="sxs-lookup"><span data-stu-id="4234e-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-261">5.00</span><span class="sxs-lookup"><span data-stu-id="4234e-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-262">4</span><span class="sxs-lookup"><span data-stu-id="4234e-262">4</span></span></td>
<td><span data-ttu-id="4234e-263">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="4234e-263">Clearing account</span></span></td>
<td><span data-ttu-id="4234e-264">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="4234e-264">-1,000.00</span></span></td>
<td><span data-ttu-id="4234e-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-266">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-266">0.00</span></span></td>
<td><span data-ttu-id="4234e-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-268">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="4234e-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-269">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-270">5</span><span class="sxs-lookup"><span data-stu-id="4234e-270">5</span></span></td>
<td><span data-ttu-id="4234e-271">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="4234e-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-272">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="4234e-272">-1,008.00</span></span></td>
<td><span data-ttu-id="4234e-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4234e-273">1,008.00</span></span></td>
<td><span data-ttu-id="4234e-274">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-275">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-276">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4234e-276">6</span></span></td>
<td><span data-ttu-id="4234e-277">สิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4234e-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-278">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="4234e-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="4234e-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-281">7</span><span class="sxs-lookup"><span data-stu-id="4234e-281">7</span></span></td>
<td><span data-ttu-id="4234e-282">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="4234e-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-283">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-284">-22,794.00</span><span class="sxs-lookup"><span data-stu-id="4234e-284">-22,794.00</span></span></td>
<td><span data-ttu-id="4234e-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-285">1,000.00</span></span></td>
<td><span data-ttu-id="4234e-286">-94.97</span><span class="sxs-lookup"><span data-stu-id="4234e-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-287">-21,888.87</span><span class="sxs-lookup"><span data-stu-id="4234e-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-288">8</span><span class="sxs-lookup"><span data-stu-id="4234e-288">8</span></span></td>
<td><span data-ttu-id="4234e-289">ค่าใช้จ่ายดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="4234e-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-290">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-291">94.97</span><span class="sxs-lookup"><span data-stu-id="4234e-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-292">94.97</span><span class="sxs-lookup"><span data-stu-id="4234e-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-293">9</span><span class="sxs-lookup"><span data-stu-id="4234e-293">9</span></span></td>
<td><span data-ttu-id="4234e-294">เงินสด</span><span class="sxs-lookup"><span data-stu-id="4234e-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-295">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="4234e-295">-1,008.00</span></span></td>
<td><span data-ttu-id="4234e-296">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="4234e-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-297">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="4234e-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-298">10</span><span class="sxs-lookup"><span data-stu-id="4234e-298">10</span></span></td>
<td><span data-ttu-id="4234e-299">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="4234e-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-300">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-301">949.75</span><span class="sxs-lookup"><span data-stu-id="4234e-301">949.75</span></span></td>
<td><span data-ttu-id="4234e-302">949.75</span><span class="sxs-lookup"><span data-stu-id="4234e-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-303">11</span><span class="sxs-lookup"><span data-stu-id="4234e-303">11</span></span></td>
<td><span data-ttu-id="4234e-304">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="4234e-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-305">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-306">-949.75</span><span class="sxs-lookup"><span data-stu-id="4234e-306">-949.75</span></span></td>
<td><span data-ttu-id="4234e-307">-949.75</span><span class="sxs-lookup"><span data-stu-id="4234e-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4234e-308">ตามตารางก่อนหน้านี้แสดงให้เห็น สมุดบัญชีสามเล่มต้องมีการรายงานที่มีการรายงานตามกฎหมายและการรายงาน IFRS</span><span class="sxs-lookup"><span data-stu-id="4234e-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="4234e-309">สมุดบัญชีตามกฎหมายจะบันทึกการชำระค่าเช่าตามกฎสำหรับการบัญชีเงินสดในชั้นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="4234e-310">สมุดบัญชีการกลับรายการตามกฎหมายย้อนกลับรายการสมุดรายวันตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="4234e-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="4234e-311">สมุดบัญชี IFRS 16 สร้างรายการสมุดรายวันที่จำเป็นต้องใช้ภายใต้ IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4234e-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="4234e-312">คุณต้องป้อนการเช่าเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="4234e-312">You must enter a lease only one time.</span></span> <span data-ttu-id="4234e-313">จากนั้นคุณสามารถเปิดหน้า **สมุดบัญชี** เพื่อดูสมุดบัญชีทั้งหมดที่เชื่อมโยงกับการเช่า</span><span class="sxs-lookup"><span data-stu-id="4234e-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="4234e-314">เมื่อคุณสร้างสมุดบัญชี สมุดบัญชีทั้งสามเล่มต้องเชื่อมโยงกับเรกคอร์ดการเช่าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="4234e-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="4234e-315">รายการสมุดรายวันแรกจะบันทึกค่าใช้จ่ายในการเช่าภายใต้สมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="4234e-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="4234e-316">คุณสามารถสร้างการชำระเงินอย่างใดอย่างหนึ่งในชุดงานหรือโดยการเลือกกำหนดการชำระเงินในสมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="4234e-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="4234e-317">สำหรับตัวอย่างนี้ รายการสมุดรายวันต่อไปนี้จะถูกสร้างขึ้นสำหรับสมุดบัญชีตามกฎหมายจากกำหนดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4234e-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="4234e-318">การชำระค่าเช่า – 1/31/2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="4234e-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="4234e-319">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-319">Account type</span></span> | <span data-ttu-id="4234e-320">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-320">Account number</span></span> | <span data-ttu-id="4234e-321">ชั้น</span><span class="sxs-lookup"><span data-stu-id="4234e-321">Layer</span></span>   | <span data-ttu-id="4234e-322">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-322">Account description</span></span> | <span data-ttu-id="4234e-323">เดบิต</span><span class="sxs-lookup"><span data-stu-id="4234e-323">Debit</span></span>    | <span data-ttu-id="4234e-324">เครดิต</span><span class="sxs-lookup"><span data-stu-id="4234e-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="4234e-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-325">Ledger</span></span>       | <span data-ttu-id="4234e-326">1</span><span class="sxs-lookup"><span data-stu-id="4234e-326">1</span></span>              | <span data-ttu-id="4234e-327">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-327">Current</span></span> | <span data-ttu-id="4234e-328">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="4234e-328">Lease expense</span></span>       | <span data-ttu-id="4234e-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-329">1,000.00</span></span> |          |
| <span data-ttu-id="4234e-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-330">Ledger</span></span>       | <span data-ttu-id="4234e-331">4</span><span class="sxs-lookup"><span data-stu-id="4234e-331">4</span></span>              | <span data-ttu-id="4234e-332">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-332">Current</span></span> | <span data-ttu-id="4234e-333">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="4234e-333">Clearing account</span></span>    |          | <span data-ttu-id="4234e-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-334">1,000.00</span></span> |

<span data-ttu-id="4234e-335">เสมียนบัญชีเจ้าหนี้ใช้ฟังก์ชัน Dynamics 365 มาตรฐานเพื่อสร้างใบแจ้งหนี้ที่จะชำระเงินสำหรับการเช่าสินทรัพย์ภายนอกสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="4234e-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="4234e-336">อย่างไรก็ตาม แทนที่จะเลือก **ค่าใช้จ่ายของสัญญาเช่า** เป็นบัญชีเดบิต เสมียนบัญชีเจ้าหนี้เลือกบัญชีเงินฝากเพื่อสร้างรายการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4234e-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="4234e-337">กระบวนการ AP – 1/31/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="4234e-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="4234e-338">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-338">Account type</span></span> | <span data-ttu-id="4234e-339">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-339">Account number</span></span> | <span data-ttu-id="4234e-340">ชั้น</span><span class="sxs-lookup"><span data-stu-id="4234e-340">Layer</span></span>   | <span data-ttu-id="4234e-341">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-341">Account description</span></span> | <span data-ttu-id="4234e-342">เดบิต</span><span class="sxs-lookup"><span data-stu-id="4234e-342">Debit</span></span>    | <span data-ttu-id="4234e-343">เครดิต</span><span class="sxs-lookup"><span data-stu-id="4234e-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="4234e-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-344">Ledger</span></span>       | <span data-ttu-id="4234e-345">4</span><span class="sxs-lookup"><span data-stu-id="4234e-345">4</span></span>              | <span data-ttu-id="4234e-346">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-346">Current</span></span> | <span data-ttu-id="4234e-347">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="4234e-347">Clearing account</span></span>    | <span data-ttu-id="4234e-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-348">1,000.00</span></span> |          |
| <span data-ttu-id="4234e-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-349">Ledger</span></span>       | <span data-ttu-id="4234e-350">2</span><span class="sxs-lookup"><span data-stu-id="4234e-350">2</span></span>              | <span data-ttu-id="4234e-351">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-351">Current</span></span> | <span data-ttu-id="4234e-352">ค่าธรรมเนียมของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4234e-352">Bank fee</span></span>            | <span data-ttu-id="4234e-353">3.00</span><span class="sxs-lookup"><span data-stu-id="4234e-353">3.00</span></span>     |          |
| <span data-ttu-id="4234e-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-354">Ledger</span></span>       | <span data-ttu-id="4234e-355">3</span><span class="sxs-lookup"><span data-stu-id="4234e-355">3</span></span>              | <span data-ttu-id="4234e-356">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-356">Current</span></span> | <span data-ttu-id="4234e-357">ค่าใช้จ่าย VAT</span><span class="sxs-lookup"><span data-stu-id="4234e-357">VAT expense</span></span>         | <span data-ttu-id="4234e-358">5.00</span><span class="sxs-lookup"><span data-stu-id="4234e-358">5.00</span></span>     |          |
| <span data-ttu-id="4234e-359">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="4234e-359">Vendor</span></span>       | <span data-ttu-id="4234e-360">5</span><span class="sxs-lookup"><span data-stu-id="4234e-360">5</span></span>              | <span data-ttu-id="4234e-361">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-361">Current</span></span> | <span data-ttu-id="4234e-362">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="4234e-362">Accounts payable</span></span>    |          | <span data-ttu-id="4234e-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4234e-363">1,008.00</span></span> |

<span data-ttu-id="4234e-364">เมื่อมีการออกคำสั่งให้กับผู้จัดจำหน่าย คุณทำตามขั้นตอนการชำระเงินทั่วไป</span><span class="sxs-lookup"><span data-stu-id="4234e-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="4234e-365">ในระหว่างกระบวนการนี้ จะมีการสร้างรายการสมุดรายวันต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4234e-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="4234e-366">การชำระเงินสด– 1/31/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="4234e-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="4234e-367">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-367">Account type</span></span> | <span data-ttu-id="4234e-368">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-368">Account number</span></span> | <span data-ttu-id="4234e-369">ชั้น</span><span class="sxs-lookup"><span data-stu-id="4234e-369">Layer</span></span>   | <span data-ttu-id="4234e-370">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-370">Account description</span></span> | <span data-ttu-id="4234e-371">เดบิต</span><span class="sxs-lookup"><span data-stu-id="4234e-371">Debit</span></span>    | <span data-ttu-id="4234e-372">เครดิต</span><span class="sxs-lookup"><span data-stu-id="4234e-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="4234e-373">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="4234e-373">Vendor</span></span>       | <span data-ttu-id="4234e-374">5</span><span class="sxs-lookup"><span data-stu-id="4234e-374">5</span></span>              | <span data-ttu-id="4234e-375">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-375">Current</span></span> | <span data-ttu-id="4234e-376">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="4234e-376">Accounts Payable</span></span>    | <span data-ttu-id="4234e-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4234e-377">1,008.00</span></span> |          |
| <span data-ttu-id="4234e-378">ธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4234e-378">Bank</span></span>         | <span data-ttu-id="4234e-379">9</span><span class="sxs-lookup"><span data-stu-id="4234e-379">9</span></span>              | <span data-ttu-id="4234e-380">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-380">Current</span></span> | <span data-ttu-id="4234e-381">เงินสด</span><span class="sxs-lookup"><span data-stu-id="4234e-381">Cash</span></span>                |          | <span data-ttu-id="4234e-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4234e-382">1,008.00</span></span> |

<span data-ttu-id="4234e-383">ณ จุดนี้ คุณมีการลงบัญชีสำหรับการเช่านี้ทั้งหมดภายใต้ข้อกำหนดในการรายงานตามกฎหมายและสามารถสร้างงบทดลองโดยใช้ชั้นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="4234e-384">ระบบส่งคืนงบทดลองที่มีตัวเลขต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4234e-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="4234e-385">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="4234e-386">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4234e-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="4234e-387">สมุดบัญชีตามกฎหมาย (ชั้นปัจจุบัน)</span><span class="sxs-lookup"><span data-stu-id="4234e-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="4234e-388">ผลรวมชั้นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4234e-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4234e-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="4234e-389">JE-100</span></span></th>
<th><span data-ttu-id="4234e-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="4234e-390">JE-110</span></span></th>
<th><span data-ttu-id="4234e-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="4234e-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4234e-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4234e-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4234e-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4234e-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4234e-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4234e-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4234e-395">1</span><span class="sxs-lookup"><span data-stu-id="4234e-395">1</span></span></td>
<td><span data-ttu-id="4234e-396">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="4234e-396">Lease expense</span></span></td>
<td><span data-ttu-id="4234e-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-399">2</span><span class="sxs-lookup"><span data-stu-id="4234e-399">2</span></span></td>
<td><span data-ttu-id="4234e-400">ค่าธรรมเนียมของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4234e-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-401">3.00</span><span class="sxs-lookup"><span data-stu-id="4234e-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-402">3.00</span><span class="sxs-lookup"><span data-stu-id="4234e-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-403">3</span><span class="sxs-lookup"><span data-stu-id="4234e-403">3</span></span></td>
<td><span data-ttu-id="4234e-404">ค่าใช้จ่าย VAT</span><span class="sxs-lookup"><span data-stu-id="4234e-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-405">5.00</span><span class="sxs-lookup"><span data-stu-id="4234e-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-406">5.00</span><span class="sxs-lookup"><span data-stu-id="4234e-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-407">4</span><span class="sxs-lookup"><span data-stu-id="4234e-407">4</span></span></td>
<td><span data-ttu-id="4234e-408">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="4234e-408">Clearing account</span></span></td>
<td><span data-ttu-id="4234e-409">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="4234e-409">-1,000.00</span></span></td>
<td><span data-ttu-id="4234e-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-411">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-412">5</span><span class="sxs-lookup"><span data-stu-id="4234e-412">5</span></span></td>
<td><span data-ttu-id="4234e-413">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="4234e-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="4234e-414">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="4234e-414">-1,008.00</span></span></td>
<td><span data-ttu-id="4234e-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4234e-415">1,008.00</span></span></td>
<td><span data-ttu-id="4234e-416">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-417">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4234e-417">6</span></span></td>
<td><span data-ttu-id="4234e-418">สิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4234e-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-419">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-420">7</span><span class="sxs-lookup"><span data-stu-id="4234e-420">7</span></span></td>
<td><span data-ttu-id="4234e-421">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="4234e-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-422">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-423">8</span><span class="sxs-lookup"><span data-stu-id="4234e-423">8</span></span></td>
<td><span data-ttu-id="4234e-424">ค่าใช้จ่ายดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="4234e-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-425">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-426">9</span><span class="sxs-lookup"><span data-stu-id="4234e-426">9</span></span></td>
<td><span data-ttu-id="4234e-427">เงินสด</span><span class="sxs-lookup"><span data-stu-id="4234e-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-428">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="4234e-428">-1,008.00</span></span></td>
<td><span data-ttu-id="4234e-429">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="4234e-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-430">10</span><span class="sxs-lookup"><span data-stu-id="4234e-430">10</span></span></td>
<td><span data-ttu-id="4234e-431">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="4234e-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-432">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4234e-433">11</span><span class="sxs-lookup"><span data-stu-id="4234e-433">11</span></span></td>
<td><span data-ttu-id="4234e-434">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="4234e-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4234e-435">0.00</span><span class="sxs-lookup"><span data-stu-id="4234e-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4234e-436">ถ้าคุณต้องการใช้ตัวเลข IFRS 16 เพื่อรันงบทดลองเดียวกัน ต้องย้อนกลับรายการสมุดรายวันบัญชีตามกฎหมาย และต้องลงรายการบัญชีรายการสมุดรายวัน IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4234e-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="4234e-437">เมื่อต้องการย้อนกลับรายการสมุดรายวันตามกฎหมาย ตัวอย่างนี้มีสมุดบัญชีการกลับรายการตามกฎหมายที่มีการตั้งค่าเดียวกันกับสมุดบัญชีตามกฎหมายแต่โปรไฟล์การลงรายการบัญชีตรงข้ามกัน</span><span class="sxs-lookup"><span data-stu-id="4234e-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="4234e-438">ตัวอย่างเช่น สมุดบัญชีที่ *มีการเดบิต* บัญชีค่าใช้จ่ายในการเช่า แต่สมุดบัญชีการกลับรายการจะ *เครดิต* บัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="4234e-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="4234e-439">ความสัมพันธ์เหล่านี้จะได้รับการกำหนดอย่างง่ายดายในบัญชีการลงรายการบัญชีการเช่าสินทรัพย์บนหน้า **พารามิเตอร์การเช่าสินทรัพย์** (**การเช่าสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การเช่าสินทรัพย์**)</span><span class="sxs-lookup"><span data-stu-id="4234e-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="4234e-440">เมื่อใช้กระบวนการเดียวกันกับที่ใช้สำหรับสมุดบัญชีที่ตามกฎหมายไว้สำหรับสมุดบัญชีการกลับ รายการสมุดรายวันต่อไปนี้จะถูกผลิต</span><span class="sxs-lookup"><span data-stu-id="4234e-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="4234e-441">ความแตกต่างของสมุดบัญชีการกลับรายการสมุดบัญชีการกลับรายการจากสมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="4234e-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="4234e-442">นอกจากนี้ยังมีการจัดทำรายการย้อนกลับไปยังชั้นที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="4234e-443">เมื่อรันงบทดลองที่ชั้นปัจจุบัน จะไม่มีการรวมรายการสมุดรายวันการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="4234e-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="4234e-444">การชำระค่าเช่า – 1/31/2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="4234e-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="4234e-445">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-445">Account type</span></span> | <span data-ttu-id="4234e-446">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-446">Account number</span></span> | <span data-ttu-id="4234e-447">ชั้น</span><span class="sxs-lookup"><span data-stu-id="4234e-447">Layer</span></span>  | <span data-ttu-id="4234e-448">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-448">Account description</span></span> | <span data-ttu-id="4234e-449">เดบิต</span><span class="sxs-lookup"><span data-stu-id="4234e-449">Debit</span></span>    | <span data-ttu-id="4234e-450">เครดิต</span><span class="sxs-lookup"><span data-stu-id="4234e-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="4234e-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-451">Ledger</span></span>       | <span data-ttu-id="4234e-452">4</span><span class="sxs-lookup"><span data-stu-id="4234e-452">4</span></span>              | <span data-ttu-id="4234e-453">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-453">Custom</span></span> | <span data-ttu-id="4234e-454">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="4234e-454">Clearing account</span></span>    | <span data-ttu-id="4234e-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-455">1,000.00</span></span> |          |
| <span data-ttu-id="4234e-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-456">Ledger</span></span>       | <span data-ttu-id="4234e-457">1</span><span class="sxs-lookup"><span data-stu-id="4234e-457">1</span></span>              | <span data-ttu-id="4234e-458">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-458">Custom</span></span> | <span data-ttu-id="4234e-459">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="4234e-459">Lease expense</span></span>       |          | <span data-ttu-id="4234e-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-460">1,000.00</span></span> |

<span data-ttu-id="4234e-461">หลังจากที่คุณได้ตัดรายการสมุดรายวันตามกฎหมายแล้ว คุณจะจองรายการสมุดรายวันทั้งหมดที่มี IFRS 16 ต้องมีอยู่ในสมุดบัญชี IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4234e-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="4234e-462">รายการเหล่านี้รวมถึงการรับรู้เริ่มต้นของสิทธิ์การใช้สินทรัพย์และหนี้สิน และเรกคอร์ดของดอกเบี้ยและค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="4234e-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="4234e-463">การรับรู้เมื่อเริ่มแรก – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="4234e-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="4234e-464">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-464">Account type</span></span> | <span data-ttu-id="4234e-465">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-465">Account number</span></span> | <span data-ttu-id="4234e-466">ชั้น</span><span class="sxs-lookup"><span data-stu-id="4234e-466">Layer</span></span>  | <span data-ttu-id="4234e-467">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-467">Account description</span></span>      | <span data-ttu-id="4234e-468">เดบิต</span><span class="sxs-lookup"><span data-stu-id="4234e-468">Debit</span></span>     | <span data-ttu-id="4234e-469">เครดิต</span><span class="sxs-lookup"><span data-stu-id="4234e-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="4234e-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-470">Ledger</span></span>       | <span data-ttu-id="4234e-471">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4234e-471">6</span></span>              | <span data-ttu-id="4234e-472">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-472">Custom</span></span> | <span data-ttu-id="4234e-473">สิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4234e-473">ROU Asset</span></span>                | <span data-ttu-id="4234e-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="4234e-474">22,793.90</span></span> |           |
| <span data-ttu-id="4234e-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-475">Ledger</span></span>       | <span data-ttu-id="4234e-476">7</span><span class="sxs-lookup"><span data-stu-id="4234e-476">7</span></span>              | <span data-ttu-id="4234e-477">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-477">Custom</span></span> | <span data-ttu-id="4234e-478">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="4234e-478">Finance lease obligation</span></span> |           | <span data-ttu-id="4234e-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="4234e-479">22,793.90</span></span> |

<span data-ttu-id="4234e-480">มีการลงรายการบัญชีการชำระค่าเช่า เช่น การชำระค่าเช่าอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="4234e-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="4234e-481">เหตุผลสำหรับการใช้บัญชีเงินฝากคือเพื่อให้แน่ใจว่าเงินสดจะถูกเครดิตเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="4234e-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="4234e-482">การชำระค่าเช่า – 1/31/2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="4234e-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="4234e-483">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-483">Account type</span></span> | <span data-ttu-id="4234e-484">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-484">Account number</span></span> | <span data-ttu-id="4234e-485">ชั้น</span><span class="sxs-lookup"><span data-stu-id="4234e-485">Layer</span></span>  | <span data-ttu-id="4234e-486">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-486">Account description</span></span>      | <span data-ttu-id="4234e-487">เดบิต</span><span class="sxs-lookup"><span data-stu-id="4234e-487">Debit</span></span>    | <span data-ttu-id="4234e-488">เครดิต</span><span class="sxs-lookup"><span data-stu-id="4234e-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="4234e-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-489">Ledger</span></span>       | <span data-ttu-id="4234e-490">7</span><span class="sxs-lookup"><span data-stu-id="4234e-490">7</span></span>              | <span data-ttu-id="4234e-491">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-491">Custom</span></span> | <span data-ttu-id="4234e-492">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="4234e-492">Finance lease obligation</span></span> | <span data-ttu-id="4234e-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-493">1,000.00</span></span> |          |
| <span data-ttu-id="4234e-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-494">Ledger</span></span>       | <span data-ttu-id="4234e-495">4</span><span class="sxs-lookup"><span data-stu-id="4234e-495">4</span></span>              | <span data-ttu-id="4234e-496">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-496">Custom</span></span> | <span data-ttu-id="4234e-497">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="4234e-497">Clearing account</span></span>         |          | <span data-ttu-id="4234e-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4234e-498">1,000.00</span></span> |

<span data-ttu-id="4234e-499">รายการสมุดรายวันดอกเบี้ยจ่ายถูกสร้างขึ้นจากกำหนดการตัดบัญชีของหนี้สิน</span><span class="sxs-lookup"><span data-stu-id="4234e-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="4234e-500">ดอกเบี้ยจ่าย – 1/31/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="4234e-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="4234e-501">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-501">Account type</span></span> | <span data-ttu-id="4234e-502">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-502">Account number</span></span> | <span data-ttu-id="4234e-503">ชั้น</span><span class="sxs-lookup"><span data-stu-id="4234e-503">Layer</span></span>  | <span data-ttu-id="4234e-504">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-504">Account description</span></span>      | <span data-ttu-id="4234e-505">เดบิต</span><span class="sxs-lookup"><span data-stu-id="4234e-505">Debit</span></span> | <span data-ttu-id="4234e-506">เครดิต</span><span class="sxs-lookup"><span data-stu-id="4234e-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="4234e-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-507">Ledger</span></span>       | <span data-ttu-id="4234e-508">8</span><span class="sxs-lookup"><span data-stu-id="4234e-508">8</span></span>              | <span data-ttu-id="4234e-509">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-509">Custom</span></span> | <span data-ttu-id="4234e-510">ค่าใช้จ่ายดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="4234e-510">Interest expense</span></span>         | <span data-ttu-id="4234e-511">94.97</span><span class="sxs-lookup"><span data-stu-id="4234e-511">94.97</span></span> |        |
| <span data-ttu-id="4234e-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-512">Ledger</span></span>       | <span data-ttu-id="4234e-513">7</span><span class="sxs-lookup"><span data-stu-id="4234e-513">7</span></span>              | <span data-ttu-id="4234e-514">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-514">Custom</span></span> | <span data-ttu-id="4234e-515">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="4234e-515">Finance lease obligation</span></span> |       | <span data-ttu-id="4234e-516">94.97</span><span class="sxs-lookup"><span data-stu-id="4234e-516">94.97</span></span>  |

<span data-ttu-id="4234e-517">รายการสมุดรายวันค่าเสื่อมราคาถูกสร้างขึ้นจากกำหนดการค่าเสื่อมราคาของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4234e-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="4234e-518">ค่าเสื่อมราคา – 1/31/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="4234e-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="4234e-519">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-519">Account type</span></span> | <span data-ttu-id="4234e-520">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-520">Account number</span></span> | <span data-ttu-id="4234e-521">ชั้น</span><span class="sxs-lookup"><span data-stu-id="4234e-521">Layer</span></span>  | <span data-ttu-id="4234e-522">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-522">Account description</span></span>      | <span data-ttu-id="4234e-523">เดบิต</span><span class="sxs-lookup"><span data-stu-id="4234e-523">Debit</span></span>  | <span data-ttu-id="4234e-524">เครดิต</span><span class="sxs-lookup"><span data-stu-id="4234e-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="4234e-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-525">Ledger</span></span>       | <span data-ttu-id="4234e-526">10</span><span class="sxs-lookup"><span data-stu-id="4234e-526">10</span></span>             | <span data-ttu-id="4234e-527">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-527">Custom</span></span> | <span data-ttu-id="4234e-528">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="4234e-528">Depreciation expense</span></span>     | <span data-ttu-id="4234e-529">949.75</span><span class="sxs-lookup"><span data-stu-id="4234e-529">949.75</span></span> |        |
| <span data-ttu-id="4234e-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="4234e-530">Ledger</span></span>       | <span data-ttu-id="4234e-531">11</span><span class="sxs-lookup"><span data-stu-id="4234e-531">11</span></span>             | <span data-ttu-id="4234e-532">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4234e-532">Custom</span></span> | <span data-ttu-id="4234e-533">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="4234e-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="4234e-534">949.75</span><span class="sxs-lookup"><span data-stu-id="4234e-534">949.75</span></span> |

<span data-ttu-id="4234e-535">หลังจากที่มีการสร้างและลงรายการบัญชีสมุดรายวันทั้งหมดนี้แล้ว คุณจะเห็นค่า "ระดับชั้นที่กำหนดเอง 1" ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4234e-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="4234e-536">โปรดทราบว่าคอลัมน์สุดท้ายรวมค่าธรรมเนียมของธนาคาร ค่าใช้จ่ายภาษีมูลค่าเพิ่ม (VAT) และการลดเงินสดจากชั้นก่อนหน้านี้ แต่ไม่รวมรายการสมุดรายวันการรายงานตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="4234e-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="4234e-537">ดังนั้น คุณจึงประสบความสำเร็จในการรายงานแบบคู่จริงได้</span><span class="sxs-lookup"><span data-stu-id="4234e-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="4234e-538">ณ จุดนี้ บริษัทเพียงแค่ต้องรันงบทดลอง และรวมชั้นปัจจุบันและชั้นแบบกำหนดเองเพื่อสร้างงบทดลองของ IFRS</span><span class="sxs-lookup"><span data-stu-id="4234e-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="4234e-539">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="4234e-539">Account No</span></span> | <span data-ttu-id="4234e-540">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4234e-540">Description</span></span>              | <span data-ttu-id="4234e-541">สมุดบัญชีตามกฎหมาย\-ชั้นปัจจุบัน\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4234e-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="4234e-542">สมุดบัญชีตามกฎหมาย\-ชั้นปัจจุบัน\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4234e-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="4234e-543">สมุดบัญชีตามกฎหมาย\-ชั้นปัจจุบัน\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4234e-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="4234e-544">ชั้นปัจจุบัน \- ผลรวม</span><span class="sxs-lookup"><span data-stu-id="4234e-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="4234e-545">สมุดบัญชีการกลับรายการ\-ชั้นแบบกำหนดเอง\-J\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4234e-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="4234e-546">สมุดบัญชี IFRS 16\-ชั้นแบบกำหนดเอง\-J\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4234e-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="4234e-547">สมุดบัญชี IFRS 16\-ชั้นแบบกำหนดเอง\-J\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4234e-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="4234e-548">สมุดบัญชี IFRS 16\-ชั้นแบบกำหนดเอง\-J\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4234e-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="4234e-549">สมุดบัญชี IFRS 16\-ชั้นแบบกำหนดเอง\-J\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4234e-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="4234e-550">ชั้นแบบกำหนดเอง \+ ชั้นปัจจุบัน \- ผลรวม</span><span class="sxs-lookup"><span data-stu-id="4234e-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="4234e-551">1</span><span class="sxs-lookup"><span data-stu-id="4234e-551">1</span></span>          | <span data-ttu-id="4234e-552">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="4234e-552">Lease expense</span></span>            | <span data-ttu-id="4234e-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="4234e-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-554">1,000\.00</span></span>               |   | <span data-ttu-id="4234e-555">\-1,000.</span><span class="sxs-lookup"><span data-stu-id="4234e-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="4234e-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-556">0\.00</span></span>                                   |
| <span data-ttu-id="4234e-557">2</span><span class="sxs-lookup"><span data-stu-id="4234e-557">2</span></span>          | <span data-ttu-id="4234e-558">ค่าธรรมเนียมของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4234e-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="4234e-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="4234e-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="4234e-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-561">3\.00</span></span>                                   |
| <span data-ttu-id="4234e-562">3</span><span class="sxs-lookup"><span data-stu-id="4234e-562">3</span></span>          | <span data-ttu-id="4234e-563">ค่าใช้จ่าย VAT</span><span class="sxs-lookup"><span data-stu-id="4234e-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="4234e-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="4234e-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="4234e-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-566">5\.00</span></span>                                   |
| <span data-ttu-id="4234e-567">4</span><span class="sxs-lookup"><span data-stu-id="4234e-567">4</span></span>          | <span data-ttu-id="4234e-568">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="4234e-568">Clearing account</span></span>         | <span data-ttu-id="4234e-569">\-1,000\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="4234e-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="4234e-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-571">0\.00</span></span>                   |   | <span data-ttu-id="4234e-572">1,000</span><span class="sxs-lookup"><span data-stu-id="4234e-572">1,000</span></span>                                           |                                                | <span data-ttu-id="4234e-573">\-1,000.</span><span class="sxs-lookup"><span data-stu-id="4234e-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="4234e-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-574">0\.00</span></span>                                   |
| <span data-ttu-id="4234e-575">5</span><span class="sxs-lookup"><span data-stu-id="4234e-575">5</span></span>          | <span data-ttu-id="4234e-576">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="4234e-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="4234e-577">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="4234e-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-578">1,008\.00</span></span>                                         | <span data-ttu-id="4234e-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="4234e-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-580">0\.00</span></span>                                   |
| <span data-ttu-id="4234e-581">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4234e-581">6</span></span>          | <span data-ttu-id="4234e-582">สิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4234e-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="4234e-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="4234e-584">22,794</span><span class="sxs-lookup"><span data-stu-id="4234e-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="4234e-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="4234e-585">22,793\.90</span></span>                              |
| <span data-ttu-id="4234e-586">7</span><span class="sxs-lookup"><span data-stu-id="4234e-586">7</span></span>          | <span data-ttu-id="4234e-587">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="4234e-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="4234e-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="4234e-589">\-22,794.</span><span class="sxs-lookup"><span data-stu-id="4234e-589">\-22,794</span></span>                                       | <span data-ttu-id="4234e-590">1,000</span><span class="sxs-lookup"><span data-stu-id="4234e-590">1,000</span></span>                                          | <span data-ttu-id="4234e-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="4234e-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="4234e-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="4234e-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="4234e-593">8</span><span class="sxs-lookup"><span data-stu-id="4234e-593">8</span></span>          | <span data-ttu-id="4234e-594">ค่าใช้จ่ายดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="4234e-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="4234e-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="4234e-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="4234e-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="4234e-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="4234e-597">94\.97</span></span>                                  |
| <span data-ttu-id="4234e-598">9</span><span class="sxs-lookup"><span data-stu-id="4234e-598">9</span></span>          | <span data-ttu-id="4234e-599">เงินสด</span><span class="sxs-lookup"><span data-stu-id="4234e-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="4234e-600">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="4234e-601">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="4234e-602">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="4234e-603">10</span><span class="sxs-lookup"><span data-stu-id="4234e-603">10</span></span>         | <span data-ttu-id="4234e-604">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="4234e-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="4234e-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="4234e-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="4234e-606">949\.75</span></span>                                        | <span data-ttu-id="4234e-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="4234e-607">949\.75</span></span>                                 |
| <span data-ttu-id="4234e-608">11</span><span class="sxs-lookup"><span data-stu-id="4234e-608">11</span></span>         | <span data-ttu-id="4234e-609">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="4234e-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="4234e-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="4234e-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="4234e-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="4234e-611">\-949\.75</span></span>                                      | <span data-ttu-id="4234e-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="4234e-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]