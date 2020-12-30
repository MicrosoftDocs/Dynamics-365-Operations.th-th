---
title: การรายงานแบบคู่
description: หัวข้อนี้จะให้คำแนะนำเกี่ยวกับวิธีการที่คุณสามารถตอบสนองความต้องการสำหรับการรายงานมาตรฐาน Financial Reporting ระหว่างประเทศ (IFRS) และการรายงานตามกฎหมายในการเช่าสินทรัพย์
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96e1d4d460aef2f74422d5e4bd4fc68255466455
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4448597"
---
# <a name="dual-reporting"></a><span data-ttu-id="83103-103">การรายงานแบบคู่</span><span class="sxs-lookup"><span data-stu-id="83103-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83103-104">หัวข้อนี้จะให้คำแนะนำเกี่ยวกับวิธีการที่คุณสามารถตอบสนองความต้องการสำหรับการรายงานมาตรฐาน Financial Reporting ระหว่างประเทศ (IFRS) และการรายงานตามกฎหมายในการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="83103-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="83103-105">ความคุ้นเคยกับชั้นของการลงรายการบัญชีใน Microsoft Dynamics 365 Finance จำเป็นต้องใช้และจะทำให้เข้าใจง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="83103-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="83103-106">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="83103-106">Example</span></span>

<span data-ttu-id="83103-107">บัญชีตัวอย่างต่อไปนี้สำหรับการเช่าภายใต้การรายงานทางกฎหมายของอิตาลีโดยใช้ทั้งวิธีการเงินสดเป็นพื้นฐานและวิธีการรายงาน IFRS</span><span class="sxs-lookup"><span data-stu-id="83103-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="83103-108">บริษัทต้องสร้างสมุดบัญชีสามเล่มให้กับบัญชีสำหรับทั้งข้อกำหนดตามกฎหมายอิตาลีและข้อกำหนด IFRS 16</span><span class="sxs-lookup"><span data-stu-id="83103-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="83103-109">ต้องมีสมุดบัญชีหนึ่งเล่มสำหรับ IFRS 16 สมุดบัญชีหนึ่งเล่มจำเป็นสำหรับข้อกำหนดตามกฎหมาย และต้องมีสมุดบัญชีหนึ่งเล่มเพื่อย้อนกลับการลงรายการบัญชีตามกฎหมายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="83103-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="83103-110">จะมีการตั้งค่าสมุดบัญชีดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="83103-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="83103-111">**สมุดบัญชี IFRS 16**</span><span class="sxs-lookup"><span data-stu-id="83103-111">**IFRS 16 book**</span></span>

<span data-ttu-id="83103-112">มีการตั้งค่าสมุดบัญชี IFRS 16 ดังนั้นจึงสอดคล้องกับมาตรฐานการบัญชี IFRS 16</span><span class="sxs-lookup"><span data-stu-id="83103-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="83103-113">รายการทั้งหมดที่มีการลงรายการบัญชีในสมุดบัญชีนี้จะได้รับการลงรายการบัญชีในชั้นแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="83103-114">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="83103-114">Name</span></span>                                    | <span data-ttu-id="83103-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="83103-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="83103-116">ชนิดของสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-116">Book type</span></span>                               | <span data-ttu-id="83103-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="83103-117">IFRS 16</span></span>        |
| <span data-ttu-id="83103-118">คำอธิบายสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-118">Book description</span></span>                        | <span data-ttu-id="83103-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="83103-119">IFRS 16</span></span>        |
| <span data-ttu-id="83103-120">ชั้นของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-120">Posting Layer</span></span>                           | <span data-ttu-id="83103-121">ชั้นที่กำหนดเอง 1</span><span class="sxs-lookup"><span data-stu-id="83103-121">Custom layer 1</span></span> |
| <span data-ttu-id="83103-122">ชนิดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="83103-122">Lease Type</span></span>                              | <span data-ttu-id="83103-123">Finance</span><span class="sxs-lookup"><span data-stu-id="83103-123">Finance</span></span>        |
| <span data-ttu-id="83103-124">กรอบงานการบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-124">Accounting Framework</span></span>                    | <span data-ttu-id="83103-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="83103-125">IFRS 16</span></span>        |
| <span data-ttu-id="83103-126">การตั้งค่าระยะเวลาของสัญญาเช่า / อายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="83103-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="83103-127">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-127">0.00</span></span>           |
| <span data-ttu-id="83103-128">การตั้งค่ามูลค่าปัจจุบัน / มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="83103-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="83103-129">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-129">0.00</span></span>           |
| <span data-ttu-id="83103-130">ขีดจำกัดระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="83103-130">Short-term threshold</span></span>                    | <span data-ttu-id="83103-131">12</span><span class="sxs-lookup"><span data-stu-id="83103-131">12</span></span>             |
| <span data-ttu-id="83103-132">ขีดจำกัดมูลค่าต่ำ</span><span class="sxs-lookup"><span data-stu-id="83103-132">Low Value Threshold</span></span>                     | <span data-ttu-id="83103-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-133">5,000.00</span></span>       |
| <span data-ttu-id="83103-134">จ่ายให้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="83103-134">Pay to Vendor</span></span>                           | <span data-ttu-id="83103-135">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="83103-135">No</span></span>             |

<span data-ttu-id="83103-136">**สมุดบัญชีตามกฎหมาย**</span><span class="sxs-lookup"><span data-stu-id="83103-136">**Statutory book**</span></span>

<span data-ttu-id="83103-137">สมุดบัญชีตามกฎหมายเป็นสมุดบัญชีเงินสดซึ่งบริษัทจะเป็นผู้ชำระค่าใช้จ่ายในการเช่าโดยมียอดเงินสดที่ชำระให้แก่ลูกค้าแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="83103-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="83103-138">สมุดบัญชีเล่มนี้จะไม่ทำให้เกิดสิทธิ์การใช้สินทรัพย์หรือหนี้สินสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="83103-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="83103-139">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="83103-139">Name</span></span>                                    | <span data-ttu-id="83103-140">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="83103-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="83103-141">ชนิดของสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-141">Book type</span></span>                               | <span data-ttu-id="83103-142">ตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="83103-142">Statutory</span></span>   |
| <span data-ttu-id="83103-143">คำอธิบายสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-143">Book description</span></span>                        | <span data-ttu-id="83103-144">GAAP ท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="83103-144">Local GAAP</span></span>  |
| <span data-ttu-id="83103-145">ชั้นของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-145">Posting Layer</span></span>                           | <span data-ttu-id="83103-146">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-146">Current</span></span>     |
| <span data-ttu-id="83103-147">ชนิดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="83103-147">Lease Type</span></span>                              | <span data-ttu-id="83103-148">อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="83103-148">Automatic</span></span>   |
| <span data-ttu-id="83103-149">กรอบงานการบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-149">Accounting Framework</span></span>                    | <span data-ttu-id="83103-150">เกณฑ์เงินสด</span><span class="sxs-lookup"><span data-stu-id="83103-150">Cash basis</span></span>  |
| <span data-ttu-id="83103-151">การตั้งค่าระยะเวลาของสัญญาเช่า / อายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="83103-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="83103-152">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-152">0.00</span></span>        |
| <span data-ttu-id="83103-153">การตั้งค่ามูลค่าปัจจุบัน / มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="83103-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="83103-154">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-154">0.00</span></span>        |
| <span data-ttu-id="83103-155">ขีดจำกัดระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="83103-155">Short-term threshold</span></span>                    | <span data-ttu-id="83103-156">0</span><span class="sxs-lookup"><span data-stu-id="83103-156">0</span></span>           |
| <span data-ttu-id="83103-157">ขีดจำกัดมูลค่าต่ำ</span><span class="sxs-lookup"><span data-stu-id="83103-157">Low Value Threshold</span></span>                     | <span data-ttu-id="83103-158">0</span><span class="sxs-lookup"><span data-stu-id="83103-158">0</span></span>           |
| <span data-ttu-id="83103-159">จ่ายให้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="83103-159">Pay to Vendor</span></span>                           | <span data-ttu-id="83103-160">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="83103-160">No</span></span>          |

<span data-ttu-id="83103-161">**สมุดบัญชีการกลับรายการตามกฎหมาย**</span><span class="sxs-lookup"><span data-stu-id="83103-161">**Statutory reversal book**</span></span>

<span data-ttu-id="83103-162">สมุดบัญชีการกลับรายการตามกฎหมายถูกตั้งค่าในลักษณะเดียวกับสมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="83103-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="83103-163">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="83103-163">Name</span></span>                                    | <span data-ttu-id="83103-164">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="83103-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="83103-165">ชนิดของสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-165">Book type</span></span>                               | <span data-ttu-id="83103-166">ตามกฎหมาย – การกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="83103-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="83103-167">คำอธิบายสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-167">Book description</span></span>                        | <span data-ttu-id="83103-168">จองเพื่อกลับรายการสมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="83103-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="83103-169">ชั้นของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-169">Posting Layer</span></span>                           | <span data-ttu-id="83103-170">ชั้นที่กำหนดเอง 1</span><span class="sxs-lookup"><span data-stu-id="83103-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="83103-171">ชนิดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="83103-171">Lease Type</span></span>                              | <span data-ttu-id="83103-172">อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="83103-172">Automatic</span></span>                      |
| <span data-ttu-id="83103-173">กรอบงานการบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-173">Accounting Framework</span></span>                    | <span data-ttu-id="83103-174">เกณฑ์เงินสด</span><span class="sxs-lookup"><span data-stu-id="83103-174">Cash basis</span></span>                     |
| <span data-ttu-id="83103-175">การตั้งค่าระยะเวลาของสัญญาเช่า / อายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="83103-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="83103-176">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-176">0.00</span></span>                           |
| <span data-ttu-id="83103-177">การตั้งค่ามูลค่าปัจจุบัน / มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="83103-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="83103-178">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-178">0.00</span></span>                           |
| <span data-ttu-id="83103-179">ขีดจำกัดระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="83103-179">Short-term threshold</span></span>                    | <span data-ttu-id="83103-180">0</span><span class="sxs-lookup"><span data-stu-id="83103-180">0</span></span>                              |
| <span data-ttu-id="83103-181">ขีดจำกัดมูลค่าต่ำ</span><span class="sxs-lookup"><span data-stu-id="83103-181">Low Value Threshold</span></span>                     | <span data-ttu-id="83103-182">0</span><span class="sxs-lookup"><span data-stu-id="83103-182">0</span></span>                              |
| <span data-ttu-id="83103-183">จ่ายให้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="83103-183">Pay to Vendor</span></span>                           | <span data-ttu-id="83103-184">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="83103-184">No</span></span>                             |

<span data-ttu-id="83103-185">สำหรับตัวอย่างนี้ มีการสร้างการเช่าที่มีการตั้งค่าต่อไปนี้ในแท็บ **ทั่วไป** และ **รายการกำหนดการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="83103-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="83103-186">**แท็บทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="83103-186">**General tab**</span></span>

| <span data-ttu-id="83103-187">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="83103-187">Field</span></span>                      | <span data-ttu-id="83103-188">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="83103-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="83103-189">อัตราดอกเบี้ยเงินกู้ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="83103-189">Incremental borrowing rate</span></span> | <span data-ttu-id="83103-190">5%</span><span class="sxs-lookup"><span data-stu-id="83103-190">5%</span></span>               |
| <span data-ttu-id="83103-191">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="83103-191">Commencement date</span></span>          | <span data-ttu-id="83103-192">วันที่ 1/1/2020</span><span class="sxs-lookup"><span data-stu-id="83103-192">1/1/2020</span></span>         |
| <span data-ttu-id="83103-193">กลุ่มสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="83103-193">Lease group</span></span>                | <span data-ttu-id="83103-194">อาคาร</span><span class="sxs-lookup"><span data-stu-id="83103-194">Buildings</span></span>        |
| <span data-ttu-id="83103-195">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="83103-195">Vendor</span></span>                     | <span data-ttu-id="83103-196">1001</span><span class="sxs-lookup"><span data-stu-id="83103-196">1001</span></span>             |
| <span data-ttu-id="83103-197">มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="83103-197">Fair value of the asset</span></span>    | <span data-ttu-id="83103-198">245,000</span><span class="sxs-lookup"><span data-stu-id="83103-198">245,000</span></span>          |
| <span data-ttu-id="83103-199">อายุการใช้งานของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="83103-199">Asset useful life</span></span>          | <span data-ttu-id="83103-200">120</span><span class="sxs-lookup"><span data-stu-id="83103-200">120</span></span>              |
| <span data-ttu-id="83103-201">ชนิดเงินรายปี</span><span class="sxs-lookup"><span data-stu-id="83103-201">Annuity type</span></span>               | <span data-ttu-id="83103-202">เงินรายปีสามัญ</span><span class="sxs-lookup"><span data-stu-id="83103-202">Ordinary annuity</span></span> |
| <span data-ttu-id="83103-203">ช่วงเวลาการทบต้น</span><span class="sxs-lookup"><span data-stu-id="83103-203">Compounding interval</span></span>       | <span data-ttu-id="83103-204">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="83103-204">Monthly</span></span>          |

<span data-ttu-id="83103-205">**แท็บรายการกำหนดการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="83103-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="83103-206">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="83103-206">Field</span></span>             | <span data-ttu-id="83103-207">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="83103-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="83103-208">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="83103-208">Start date</span></span>        | <span data-ttu-id="83103-209">วันที่ 1/1/2020</span><span class="sxs-lookup"><span data-stu-id="83103-209">1/1/2020</span></span>   |
| <span data-ttu-id="83103-210">ช่วงรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="83103-210">Period interval</span></span>   | <span data-ttu-id="83103-211">เดือน</span><span class="sxs-lookup"><span data-stu-id="83103-211">Months</span></span>     |
| <span data-ttu-id="83103-212">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="83103-212">Periods</span></span>           | <span data-ttu-id="83103-213">24</span><span class="sxs-lookup"><span data-stu-id="83103-213">24</span></span>         |
| <span data-ttu-id="83103-214">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="83103-214">End date</span></span>          | <span data-ttu-id="83103-215">วันที่ 12/31/2020</span><span class="sxs-lookup"><span data-stu-id="83103-215">12/31/2020</span></span> |
| <span data-ttu-id="83103-216">ความถี่ในการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="83103-216">Payment frequency</span></span> | <span data-ttu-id="83103-217">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="83103-217">Monthly</span></span>    |
| <span data-ttu-id="83103-218">ยอดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="83103-218">Payment amount</span></span>    | <span data-ttu-id="83103-219">1,000</span><span class="sxs-lookup"><span data-stu-id="83103-219">1,000</span></span>      |

<span data-ttu-id="83103-220">ในการลงบัญชีสำหรับชั่การเช่านี้ภายใต้สองกรอบงาน คุณใช้ชั้นของการลงรายการบัญชีปัจจุบันและชั้นของการลงรายการบัญชีที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="83103-221">ตารางต่อไปนี้จะแสดงตัวอย่างของรายการสมุดรายวันทั้งหมดที่จำเป็นต้องแสดงถึงการเงินภายใต้มาตรฐานการรายงานแต่ละฉบับ</span><span class="sxs-lookup"><span data-stu-id="83103-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="83103-222">คำอธิบายโดยละเอียดของรายการสมุดรายวันแต่ละรายการสำหรับเดือนแรกของการเช่ามีให้หลังจากนี้</span><span class="sxs-lookup"><span data-stu-id="83103-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="83103-223">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="83103-224">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="83103-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="83103-225">สมุดบัญชีตามกฎหมาย (ชั้นปัจจุบัน)</span><span class="sxs-lookup"><span data-stu-id="83103-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="83103-226">ผลรวมชั้นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-226">Current layer total</span></span></th>
<th><span data-ttu-id="83103-227">สมุดบัญชีการกลับรายการ (ชั้นที่กำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="83103-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="83103-228">สมุดบัญชี IFRS 16 (ชั้นที่กำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="83103-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="83103-229">ชั้นปัจจุบัน + ยอดรวมชั้นแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="83103-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="83103-230">JE-100</span></span></th>
<th><span data-ttu-id="83103-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="83103-231">JE-110</span></span></th>
<th><span data-ttu-id="83103-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="83103-232">JE-120</span></span></th>
<th><span data-ttu-id="83103-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="83103-233">JE-130</span></span></th>
<th><span data-ttu-id="83103-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="83103-234">JE-140</span></span></th>
<th><span data-ttu-id="83103-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="83103-235">JE-150</span></span></th>
<th><span data-ttu-id="83103-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="83103-236">JE-160</span></span></th>
<th><span data-ttu-id="83103-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="83103-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="83103-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="83103-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="83103-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="83103-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="83103-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="83103-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="83103-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="83103-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="83103-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="83103-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="83103-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="83103-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="83103-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="83103-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="83103-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="83103-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="83103-246">1</span><span class="sxs-lookup"><span data-stu-id="83103-246">1</span></span></td>
<td><span data-ttu-id="83103-247">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="83103-247">Lease expense</span></span></td>
<td><span data-ttu-id="83103-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-249">1,000.00</span></span></td>
<td><span data-ttu-id="83103-250">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="83103-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-251">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-252">2</span><span class="sxs-lookup"><span data-stu-id="83103-252">2</span></span></td>
<td><span data-ttu-id="83103-253">ค่าธรรมเนียมของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="83103-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="83103-254">3.00</span><span class="sxs-lookup"><span data-stu-id="83103-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="83103-255">3.00</span><span class="sxs-lookup"><span data-stu-id="83103-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-256">3.00</span><span class="sxs-lookup"><span data-stu-id="83103-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-257">3</span><span class="sxs-lookup"><span data-stu-id="83103-257">3</span></span></td>
<td><span data-ttu-id="83103-258">ค่าใช้จ่าย VAT</span><span class="sxs-lookup"><span data-stu-id="83103-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="83103-259">5.00</span><span class="sxs-lookup"><span data-stu-id="83103-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="83103-260">5.00</span><span class="sxs-lookup"><span data-stu-id="83103-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-261">5.00</span><span class="sxs-lookup"><span data-stu-id="83103-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-262">4</span><span class="sxs-lookup"><span data-stu-id="83103-262">4</span></span></td>
<td><span data-ttu-id="83103-263">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="83103-263">Clearing account</span></span></td>
<td><span data-ttu-id="83103-264">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="83103-264">-1,000.00</span></span></td>
<td><span data-ttu-id="83103-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="83103-266">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-266">0.00</span></span></td>
<td><span data-ttu-id="83103-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="83103-268">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="83103-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-269">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-270">5</span><span class="sxs-lookup"><span data-stu-id="83103-270">5</span></span></td>
<td><span data-ttu-id="83103-271">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="83103-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="83103-272">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="83103-272">-1,008.00</span></span></td>
<td><span data-ttu-id="83103-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="83103-273">1,008.00</span></span></td>
<td><span data-ttu-id="83103-274">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-275">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-276">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="83103-276">6</span></span></td>
<td><span data-ttu-id="83103-277">สิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="83103-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-278">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="83103-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="83103-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="83103-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-281">7</span><span class="sxs-lookup"><span data-stu-id="83103-281">7</span></span></td>
<td><span data-ttu-id="83103-282">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="83103-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-283">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="83103-284">-22,794.00</span><span class="sxs-lookup"><span data-stu-id="83103-284">-22,794.00</span></span></td>
<td><span data-ttu-id="83103-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-285">1,000.00</span></span></td>
<td><span data-ttu-id="83103-286">-94.97</span><span class="sxs-lookup"><span data-stu-id="83103-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="83103-287">-21,888.87</span><span class="sxs-lookup"><span data-stu-id="83103-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-288">8</span><span class="sxs-lookup"><span data-stu-id="83103-288">8</span></span></td>
<td><span data-ttu-id="83103-289">ค่าใช้จ่ายดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="83103-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-290">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-291">94.97</span><span class="sxs-lookup"><span data-stu-id="83103-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="83103-292">94.97</span><span class="sxs-lookup"><span data-stu-id="83103-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-293">9</span><span class="sxs-lookup"><span data-stu-id="83103-293">9</span></span></td>
<td><span data-ttu-id="83103-294">เงินสด</span><span class="sxs-lookup"><span data-stu-id="83103-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-295">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="83103-295">-1,008.00</span></span></td>
<td><span data-ttu-id="83103-296">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="83103-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-297">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="83103-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-298">10</span><span class="sxs-lookup"><span data-stu-id="83103-298">10</span></span></td>
<td><span data-ttu-id="83103-299">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="83103-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-300">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-301">949.75</span><span class="sxs-lookup"><span data-stu-id="83103-301">949.75</span></span></td>
<td><span data-ttu-id="83103-302">949.75</span><span class="sxs-lookup"><span data-stu-id="83103-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-303">11</span><span class="sxs-lookup"><span data-stu-id="83103-303">11</span></span></td>
<td><span data-ttu-id="83103-304">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="83103-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-305">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-306">-949.75</span><span class="sxs-lookup"><span data-stu-id="83103-306">-949.75</span></span></td>
<td><span data-ttu-id="83103-307">-949.75</span><span class="sxs-lookup"><span data-stu-id="83103-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="83103-308">ตามตารางก่อนหน้านี้แสดงให้เห็น สมุดบัญชีสามเล่มต้องมีการรายงานที่มีการรายงานตามกฎหมายและการรายงาน IFRS</span><span class="sxs-lookup"><span data-stu-id="83103-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="83103-309">สมุดบัญชีตามกฎหมายจะบันทึกการชำระค่าเช่าตามกฎสำหรับการบัญชีเงินสดในชั้นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="83103-310">สมุดบัญชีการกลับรายการตามกฎหมายย้อนกลับรายการสมุดรายวันตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="83103-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="83103-311">สมุดบัญชี IFRS 16 สร้างรายการสมุดรายวันที่จำเป็นต้องใช้ภายใต้ IFRS 16</span><span class="sxs-lookup"><span data-stu-id="83103-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="83103-312">คุณต้องป้อนการเช่าเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="83103-312">You must enter a lease only one time.</span></span> <span data-ttu-id="83103-313">จากนั้นคุณสามารถเปิดหน้า **สมุดบัญชี** เพื่อดูสมุดบัญชีทั้งหมดที่เชื่อมโยงกับการเช่า</span><span class="sxs-lookup"><span data-stu-id="83103-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="83103-314">เมื่อคุณสร้างสมุดบัญชี สมุดบัญชีทั้งสามเล่มต้องเชื่อมโยงกับเรกคอร์ดการเช่าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="83103-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="83103-315">รายการสมุดรายวันแรกจะบันทึกค่าใช้จ่ายในการเช่าภายใต้สมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="83103-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="83103-316">คุณสามารถสร้างการชำระเงินอย่างใดอย่างหนึ่งในชุดงานหรือโดยการเลือกกำหนดการชำระเงินในสมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="83103-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="83103-317">สำหรับตัวอย่างนี้ รายการสมุดรายวันต่อไปนี้จะถูกสร้างขึ้นสำหรับสมุดบัญชีตามกฎหมายจากกำหนดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="83103-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="83103-318">การชำระค่าเช่า – 1/31/2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="83103-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="83103-319">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-319">Account type</span></span> | <span data-ttu-id="83103-320">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-320">Account number</span></span> | <span data-ttu-id="83103-321">ชั้น</span><span class="sxs-lookup"><span data-stu-id="83103-321">Layer</span></span>   | <span data-ttu-id="83103-322">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-322">Account description</span></span> | <span data-ttu-id="83103-323">เดบิต</span><span class="sxs-lookup"><span data-stu-id="83103-323">Debit</span></span>    | <span data-ttu-id="83103-324">เครดิต</span><span class="sxs-lookup"><span data-stu-id="83103-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="83103-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-325">Ledger</span></span>       | <span data-ttu-id="83103-326">1</span><span class="sxs-lookup"><span data-stu-id="83103-326">1</span></span>              | <span data-ttu-id="83103-327">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-327">Current</span></span> | <span data-ttu-id="83103-328">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="83103-328">Lease expense</span></span>       | <span data-ttu-id="83103-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-329">1,000.00</span></span> |          |
| <span data-ttu-id="83103-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-330">Ledger</span></span>       | <span data-ttu-id="83103-331">4</span><span class="sxs-lookup"><span data-stu-id="83103-331">4</span></span>              | <span data-ttu-id="83103-332">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-332">Current</span></span> | <span data-ttu-id="83103-333">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="83103-333">Clearing account</span></span>    |          | <span data-ttu-id="83103-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-334">1,000.00</span></span> |

<span data-ttu-id="83103-335">เสมียนบัญชีเจ้าหนี้ใช้ฟังก์ชัน Dynamics 365 มาตรฐานเพื่อสร้างใบแจ้งหนี้ที่จะชำระเงินสำหรับการเช่าสินทรัพย์ภายนอกสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="83103-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="83103-336">อย่างไรก็ตาม แทนที่จะเลือก **ค่าใช้จ่ายของสัญญาเช่า** เป็นบัญชีเดบิต เสมียนบัญชีเจ้าหนี้เลือกบัญชีเงินฝากเพื่อสร้างรายการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="83103-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="83103-337">กระบวนการ AP – 1/31/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="83103-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="83103-338">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-338">Account type</span></span> | <span data-ttu-id="83103-339">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-339">Account number</span></span> | <span data-ttu-id="83103-340">ชั้น</span><span class="sxs-lookup"><span data-stu-id="83103-340">Layer</span></span>   | <span data-ttu-id="83103-341">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-341">Account description</span></span> | <span data-ttu-id="83103-342">เดบิต</span><span class="sxs-lookup"><span data-stu-id="83103-342">Debit</span></span>    | <span data-ttu-id="83103-343">เครดิต</span><span class="sxs-lookup"><span data-stu-id="83103-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="83103-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-344">Ledger</span></span>       | <span data-ttu-id="83103-345">4</span><span class="sxs-lookup"><span data-stu-id="83103-345">4</span></span>              | <span data-ttu-id="83103-346">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-346">Current</span></span> | <span data-ttu-id="83103-347">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="83103-347">Clearing account</span></span>    | <span data-ttu-id="83103-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-348">1,000.00</span></span> |          |
| <span data-ttu-id="83103-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-349">Ledger</span></span>       | <span data-ttu-id="83103-350">2</span><span class="sxs-lookup"><span data-stu-id="83103-350">2</span></span>              | <span data-ttu-id="83103-351">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-351">Current</span></span> | <span data-ttu-id="83103-352">ค่าธรรมเนียมของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="83103-352">Bank fee</span></span>            | <span data-ttu-id="83103-353">3.00</span><span class="sxs-lookup"><span data-stu-id="83103-353">3.00</span></span>     |          |
| <span data-ttu-id="83103-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-354">Ledger</span></span>       | <span data-ttu-id="83103-355">3</span><span class="sxs-lookup"><span data-stu-id="83103-355">3</span></span>              | <span data-ttu-id="83103-356">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-356">Current</span></span> | <span data-ttu-id="83103-357">ค่าใช้จ่าย VAT</span><span class="sxs-lookup"><span data-stu-id="83103-357">VAT expense</span></span>         | <span data-ttu-id="83103-358">5.00</span><span class="sxs-lookup"><span data-stu-id="83103-358">5.00</span></span>     |          |
| <span data-ttu-id="83103-359">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="83103-359">Vendor</span></span>       | <span data-ttu-id="83103-360">5</span><span class="sxs-lookup"><span data-stu-id="83103-360">5</span></span>              | <span data-ttu-id="83103-361">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-361">Current</span></span> | <span data-ttu-id="83103-362">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="83103-362">Accounts payable</span></span>    |          | <span data-ttu-id="83103-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="83103-363">1,008.00</span></span> |

<span data-ttu-id="83103-364">เมื่อมีการออกคำสั่งให้กับผู้จัดจำหน่าย คุณทำตามขั้นตอนการชำระเงินทั่วไป</span><span class="sxs-lookup"><span data-stu-id="83103-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="83103-365">ในระหว่างกระบวนการนี้ จะมีการสร้างรายการสมุดรายวันต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="83103-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="83103-366">การชำระเงินสด– 1/31/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="83103-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="83103-367">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-367">Account type</span></span> | <span data-ttu-id="83103-368">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-368">Account number</span></span> | <span data-ttu-id="83103-369">ชั้น</span><span class="sxs-lookup"><span data-stu-id="83103-369">Layer</span></span>   | <span data-ttu-id="83103-370">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-370">Account description</span></span> | <span data-ttu-id="83103-371">เดบิต</span><span class="sxs-lookup"><span data-stu-id="83103-371">Debit</span></span>    | <span data-ttu-id="83103-372">เครดิต</span><span class="sxs-lookup"><span data-stu-id="83103-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="83103-373">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="83103-373">Vendor</span></span>       | <span data-ttu-id="83103-374">5</span><span class="sxs-lookup"><span data-stu-id="83103-374">5</span></span>              | <span data-ttu-id="83103-375">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-375">Current</span></span> | <span data-ttu-id="83103-376">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="83103-376">Accounts Payable</span></span>    | <span data-ttu-id="83103-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="83103-377">1,008.00</span></span> |          |
| <span data-ttu-id="83103-378">ธนาคาร</span><span class="sxs-lookup"><span data-stu-id="83103-378">Bank</span></span>         | <span data-ttu-id="83103-379">9</span><span class="sxs-lookup"><span data-stu-id="83103-379">9</span></span>              | <span data-ttu-id="83103-380">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-380">Current</span></span> | <span data-ttu-id="83103-381">เงินสด</span><span class="sxs-lookup"><span data-stu-id="83103-381">Cash</span></span>                |          | <span data-ttu-id="83103-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="83103-382">1,008.00</span></span> |

<span data-ttu-id="83103-383">ณ จุดนี้ คุณมีการลงบัญชีสำหรับการเช่านี้ทั้งหมดภายใต้ข้อกำหนดในการรายงานตามกฎหมายและสามารถสร้างงบทดลองโดยใช้ชั้นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="83103-384">ระบบส่งคืนงบทดลองที่มีตัวเลขต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="83103-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="83103-385">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="83103-386">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="83103-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="83103-387">สมุดบัญชีตามกฎหมาย (ชั้นปัจจุบัน)</span><span class="sxs-lookup"><span data-stu-id="83103-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="83103-388">ผลรวมชั้นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83103-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="83103-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="83103-389">JE-100</span></span></th>
<th><span data-ttu-id="83103-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="83103-390">JE-110</span></span></th>
<th><span data-ttu-id="83103-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="83103-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="83103-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="83103-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="83103-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="83103-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="83103-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="83103-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="83103-395">1</span><span class="sxs-lookup"><span data-stu-id="83103-395">1</span></span></td>
<td><span data-ttu-id="83103-396">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="83103-396">Lease expense</span></span></td>
<td><span data-ttu-id="83103-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-399">2</span><span class="sxs-lookup"><span data-stu-id="83103-399">2</span></span></td>
<td><span data-ttu-id="83103-400">ค่าธรรมเนียมของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="83103-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="83103-401">3.00</span><span class="sxs-lookup"><span data-stu-id="83103-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="83103-402">3.00</span><span class="sxs-lookup"><span data-stu-id="83103-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-403">3</span><span class="sxs-lookup"><span data-stu-id="83103-403">3</span></span></td>
<td><span data-ttu-id="83103-404">ค่าใช้จ่าย VAT</span><span class="sxs-lookup"><span data-stu-id="83103-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="83103-405">5.00</span><span class="sxs-lookup"><span data-stu-id="83103-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="83103-406">5.00</span><span class="sxs-lookup"><span data-stu-id="83103-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-407">4</span><span class="sxs-lookup"><span data-stu-id="83103-407">4</span></span></td>
<td><span data-ttu-id="83103-408">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="83103-408">Clearing account</span></span></td>
<td><span data-ttu-id="83103-409">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="83103-409">-1,000.00</span></span></td>
<td><span data-ttu-id="83103-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="83103-411">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-412">5</span><span class="sxs-lookup"><span data-stu-id="83103-412">5</span></span></td>
<td><span data-ttu-id="83103-413">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="83103-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="83103-414">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="83103-414">-1,008.00</span></span></td>
<td><span data-ttu-id="83103-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="83103-415">1,008.00</span></span></td>
<td><span data-ttu-id="83103-416">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-417">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="83103-417">6</span></span></td>
<td><span data-ttu-id="83103-418">สิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="83103-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-419">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-420">7</span><span class="sxs-lookup"><span data-stu-id="83103-420">7</span></span></td>
<td><span data-ttu-id="83103-421">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="83103-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-422">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-423">8</span><span class="sxs-lookup"><span data-stu-id="83103-423">8</span></span></td>
<td><span data-ttu-id="83103-424">ค่าใช้จ่ายดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="83103-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-425">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-426">9</span><span class="sxs-lookup"><span data-stu-id="83103-426">9</span></span></td>
<td><span data-ttu-id="83103-427">เงินสด</span><span class="sxs-lookup"><span data-stu-id="83103-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-428">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="83103-428">-1,008.00</span></span></td>
<td><span data-ttu-id="83103-429">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="83103-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-430">10</span><span class="sxs-lookup"><span data-stu-id="83103-430">10</span></span></td>
<td><span data-ttu-id="83103-431">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="83103-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-432">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83103-433">11</span><span class="sxs-lookup"><span data-stu-id="83103-433">11</span></span></td>
<td><span data-ttu-id="83103-434">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="83103-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="83103-435">0.00</span><span class="sxs-lookup"><span data-stu-id="83103-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="83103-436">ถ้าคุณต้องการใช้ตัวเลข IFRS 16 เพื่อรันงบทดลองเดียวกัน ต้องย้อนกลับรายการสมุดรายวันบัญชีตามกฎหมาย และต้องลงรายการบัญชีรายการสมุดรายวัน IFRS 16</span><span class="sxs-lookup"><span data-stu-id="83103-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="83103-437">เมื่อต้องการย้อนกลับรายการสมุดรายวันตามกฎหมาย ตัวอย่างนี้มีสมุดบัญชีการกลับรายการตามกฎหมายที่มีการตั้งค่าเดียวกันกับสมุดบัญชีตามกฎหมายแต่โปรไฟล์การลงรายการบัญชีตรงข้ามกัน</span><span class="sxs-lookup"><span data-stu-id="83103-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="83103-438">ตัวอย่างเช่น สมุดบัญชีที่ *มีการเดบิต* บัญชีค่าใช้จ่ายในการเช่า แต่สมุดบัญชีการกลับรายการจะ *เครดิต* บัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="83103-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="83103-439">ความสัมพันธ์เหล่านี้จะได้รับการกำหนดอย่างง่ายดายในบัญชีการลงรายการบัญชีการเช่าสินทรัพย์บนหน้า **พารามิเตอร์การเช่าสินทรัพย์** (**การเช่าสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การเช่าสินทรัพย์**)</span><span class="sxs-lookup"><span data-stu-id="83103-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="83103-440">เมื่อใช้กระบวนการเดียวกันกับที่ใช้สำหรับสมุดบัญชีที่ตามกฎหมายไว้สำหรับสมุดบัญชีการกลับ รายการสมุดรายวันต่อไปนี้จะถูกผลิต</span><span class="sxs-lookup"><span data-stu-id="83103-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="83103-441">ความแตกต่างของสมุดบัญชีการกลับรายการสมุดบัญชีการกลับรายการจากสมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="83103-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="83103-442">นอกจากนี้ยังมีการจัดทำรายการย้อนกลับไปยังชั้นที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="83103-443">เมื่อรันงบทดลองที่ชั้นปัจจุบัน จะไม่มีการรวมรายการสมุดรายวันการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="83103-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="83103-444">การชำระค่าเช่า – 1/31/2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="83103-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="83103-445">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-445">Account type</span></span> | <span data-ttu-id="83103-446">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-446">Account number</span></span> | <span data-ttu-id="83103-447">ชั้น</span><span class="sxs-lookup"><span data-stu-id="83103-447">Layer</span></span>  | <span data-ttu-id="83103-448">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-448">Account description</span></span> | <span data-ttu-id="83103-449">เดบิต</span><span class="sxs-lookup"><span data-stu-id="83103-449">Debit</span></span>    | <span data-ttu-id="83103-450">เครดิต</span><span class="sxs-lookup"><span data-stu-id="83103-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="83103-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-451">Ledger</span></span>       | <span data-ttu-id="83103-452">4</span><span class="sxs-lookup"><span data-stu-id="83103-452">4</span></span>              | <span data-ttu-id="83103-453">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-453">Custom</span></span> | <span data-ttu-id="83103-454">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="83103-454">Clearing account</span></span>    | <span data-ttu-id="83103-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-455">1,000.00</span></span> |          |
| <span data-ttu-id="83103-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-456">Ledger</span></span>       | <span data-ttu-id="83103-457">1</span><span class="sxs-lookup"><span data-stu-id="83103-457">1</span></span>              | <span data-ttu-id="83103-458">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-458">Custom</span></span> | <span data-ttu-id="83103-459">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="83103-459">Lease expense</span></span>       |          | <span data-ttu-id="83103-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-460">1,000.00</span></span> |

<span data-ttu-id="83103-461">หลังจากที่คุณได้ตัดรายการสมุดรายวันตามกฎหมายแล้ว คุณจะจองรายการสมุดรายวันทั้งหมดที่มี IFRS 16 ต้องมีอยู่ในสมุดบัญชี IFRS 16</span><span class="sxs-lookup"><span data-stu-id="83103-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="83103-462">รายการเหล่านี้รวมถึงการรับรู้เริ่มต้นของสิทธิ์การใช้สินทรัพย์และหนี้สิน และเรกคอร์ดของดอกเบี้ยและค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="83103-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="83103-463">การรับรู้เมื่อเริ่มแรก – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="83103-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="83103-464">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-464">Account type</span></span> | <span data-ttu-id="83103-465">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-465">Account number</span></span> | <span data-ttu-id="83103-466">ชั้น</span><span class="sxs-lookup"><span data-stu-id="83103-466">Layer</span></span>  | <span data-ttu-id="83103-467">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-467">Account description</span></span>      | <span data-ttu-id="83103-468">เดบิต</span><span class="sxs-lookup"><span data-stu-id="83103-468">Debit</span></span>     | <span data-ttu-id="83103-469">เครดิต</span><span class="sxs-lookup"><span data-stu-id="83103-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="83103-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-470">Ledger</span></span>       | <span data-ttu-id="83103-471">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="83103-471">6</span></span>              | <span data-ttu-id="83103-472">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-472">Custom</span></span> | <span data-ttu-id="83103-473">สิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="83103-473">ROU Asset</span></span>                | <span data-ttu-id="83103-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="83103-474">22,793.90</span></span> |           |
| <span data-ttu-id="83103-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-475">Ledger</span></span>       | <span data-ttu-id="83103-476">7</span><span class="sxs-lookup"><span data-stu-id="83103-476">7</span></span>              | <span data-ttu-id="83103-477">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-477">Custom</span></span> | <span data-ttu-id="83103-478">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="83103-478">Finance lease obligation</span></span> |           | <span data-ttu-id="83103-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="83103-479">22,793.90</span></span> |

<span data-ttu-id="83103-480">มีการลงรายการบัญชีการชำระค่าเช่า เช่น การชำระค่าเช่าอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="83103-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="83103-481">เหตุผลสำหรับการใช้บัญชีเงินฝากคือเพื่อให้แน่ใจว่าเงินสดจะถูกเครดิตเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="83103-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="83103-482">การชำระค่าเช่า – 1/31/2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="83103-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="83103-483">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-483">Account type</span></span> | <span data-ttu-id="83103-484">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-484">Account number</span></span> | <span data-ttu-id="83103-485">ชั้น</span><span class="sxs-lookup"><span data-stu-id="83103-485">Layer</span></span>  | <span data-ttu-id="83103-486">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-486">Account description</span></span>      | <span data-ttu-id="83103-487">เดบิต</span><span class="sxs-lookup"><span data-stu-id="83103-487">Debit</span></span>    | <span data-ttu-id="83103-488">เครดิต</span><span class="sxs-lookup"><span data-stu-id="83103-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="83103-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-489">Ledger</span></span>       | <span data-ttu-id="83103-490">7</span><span class="sxs-lookup"><span data-stu-id="83103-490">7</span></span>              | <span data-ttu-id="83103-491">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-491">Custom</span></span> | <span data-ttu-id="83103-492">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="83103-492">Finance lease obligation</span></span> | <span data-ttu-id="83103-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-493">1,000.00</span></span> |          |
| <span data-ttu-id="83103-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-494">Ledger</span></span>       | <span data-ttu-id="83103-495">4</span><span class="sxs-lookup"><span data-stu-id="83103-495">4</span></span>              | <span data-ttu-id="83103-496">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-496">Custom</span></span> | <span data-ttu-id="83103-497">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="83103-497">Clearing account</span></span>         |          | <span data-ttu-id="83103-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="83103-498">1,000.00</span></span> |

<span data-ttu-id="83103-499">รายการสมุดรายวันดอกเบี้ยจ่ายถูกสร้างขึ้นจากกำหนดการตัดบัญชีของหนี้สิน</span><span class="sxs-lookup"><span data-stu-id="83103-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="83103-500">ดอกเบี้ยจ่าย – 1/31/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="83103-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="83103-501">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-501">Account type</span></span> | <span data-ttu-id="83103-502">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-502">Account number</span></span> | <span data-ttu-id="83103-503">ชั้น</span><span class="sxs-lookup"><span data-stu-id="83103-503">Layer</span></span>  | <span data-ttu-id="83103-504">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-504">Account description</span></span>      | <span data-ttu-id="83103-505">เดบิต</span><span class="sxs-lookup"><span data-stu-id="83103-505">Debit</span></span> | <span data-ttu-id="83103-506">เครดิต</span><span class="sxs-lookup"><span data-stu-id="83103-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="83103-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-507">Ledger</span></span>       | <span data-ttu-id="83103-508">8</span><span class="sxs-lookup"><span data-stu-id="83103-508">8</span></span>              | <span data-ttu-id="83103-509">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-509">Custom</span></span> | <span data-ttu-id="83103-510">ค่าใช้จ่ายดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="83103-510">Interest expense</span></span>         | <span data-ttu-id="83103-511">94.97</span><span class="sxs-lookup"><span data-stu-id="83103-511">94.97</span></span> |        |
| <span data-ttu-id="83103-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-512">Ledger</span></span>       | <span data-ttu-id="83103-513">7</span><span class="sxs-lookup"><span data-stu-id="83103-513">7</span></span>              | <span data-ttu-id="83103-514">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-514">Custom</span></span> | <span data-ttu-id="83103-515">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="83103-515">Finance lease obligation</span></span> |       | <span data-ttu-id="83103-516">94.97</span><span class="sxs-lookup"><span data-stu-id="83103-516">94.97</span></span>  |

<span data-ttu-id="83103-517">รายการสมุดรายวันค่าเสื่อมราคาถูกสร้างขึ้นจากกำหนดการค่าเสื่อมราคาของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="83103-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="83103-518">ค่าเสื่อมราคา – 1/31/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="83103-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="83103-519">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-519">Account type</span></span> | <span data-ttu-id="83103-520">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-520">Account number</span></span> | <span data-ttu-id="83103-521">ชั้น</span><span class="sxs-lookup"><span data-stu-id="83103-521">Layer</span></span>  | <span data-ttu-id="83103-522">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-522">Account description</span></span>      | <span data-ttu-id="83103-523">เดบิต</span><span class="sxs-lookup"><span data-stu-id="83103-523">Debit</span></span>  | <span data-ttu-id="83103-524">เครดิต</span><span class="sxs-lookup"><span data-stu-id="83103-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="83103-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-525">Ledger</span></span>       | <span data-ttu-id="83103-526">10</span><span class="sxs-lookup"><span data-stu-id="83103-526">10</span></span>             | <span data-ttu-id="83103-527">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-527">Custom</span></span> | <span data-ttu-id="83103-528">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="83103-528">Depreciation expense</span></span>     | <span data-ttu-id="83103-529">949.75</span><span class="sxs-lookup"><span data-stu-id="83103-529">949.75</span></span> |        |
| <span data-ttu-id="83103-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="83103-530">Ledger</span></span>       | <span data-ttu-id="83103-531">11</span><span class="sxs-lookup"><span data-stu-id="83103-531">11</span></span>             | <span data-ttu-id="83103-532">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="83103-532">Custom</span></span> | <span data-ttu-id="83103-533">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="83103-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="83103-534">949.75</span><span class="sxs-lookup"><span data-stu-id="83103-534">949.75</span></span> |

<span data-ttu-id="83103-535">หลังจากที่มีการสร้างและลงรายการบัญชีสมุดรายวันทั้งหมดนี้แล้ว คุณจะเห็นค่า "ระดับชั้นที่กำหนดเอง 1" ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="83103-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="83103-536">โปรดทราบว่าคอลัมน์สุดท้ายรวมค่าธรรมเนียมของธนาคาร ค่าใช้จ่ายภาษีมูลค่าเพิ่ม (VAT) และการลดเงินสดจากชั้นก่อนหน้านี้ แต่ไม่รวมรายการสมุดรายวันการรายงานตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="83103-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="83103-537">ดังนั้น คุณจึงประสบความสำเร็จในการรายงานแบบคู่จริงได้</span><span class="sxs-lookup"><span data-stu-id="83103-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="83103-538">ณ จุดนี้ บริษัทเพียงแค่ต้องรันงบทดลอง และรวมชั้นปัจจุบันและชั้นแบบกำหนดเองเพื่อสร้างงบทดลองของ IFRS</span><span class="sxs-lookup"><span data-stu-id="83103-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="83103-539">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="83103-539">Account No</span></span> | <span data-ttu-id="83103-540">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="83103-540">Description</span></span>              | <span data-ttu-id="83103-541">สมุดบัญชีตามกฎหมาย\-ชั้นปัจจุบัน\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="83103-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="83103-542">สมุดบัญชีตามกฎหมาย\-ชั้นปัจจุบัน\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="83103-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="83103-543">สมุดบัญชีตามกฎหมาย\-ชั้นปัจจุบัน\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="83103-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="83103-544">ชั้นปัจจุบัน \- ผลรวม</span><span class="sxs-lookup"><span data-stu-id="83103-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="83103-545">สมุดบัญชีการกลับรายการ\-ชั้นแบบกำหนดเอง\-J\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="83103-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="83103-546">สมุดบัญชี IFRS 16\-ชั้นแบบกำหนดเอง\-J\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="83103-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="83103-547">สมุดบัญชี IFRS 16\-ชั้นแบบกำหนดเอง\-J\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="83103-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="83103-548">สมุดบัญชี IFRS 16\-ชั้นแบบกำหนดเอง\-J\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="83103-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="83103-549">สมุดบัญชี IFRS 16\-ชั้นแบบกำหนดเอง\-J\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="83103-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="83103-550">ชั้นแบบกำหนดเอง \+ ชั้นปัจจุบัน \- ผลรวม</span><span class="sxs-lookup"><span data-stu-id="83103-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="83103-551">1</span><span class="sxs-lookup"><span data-stu-id="83103-551">1</span></span>          | <span data-ttu-id="83103-552">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="83103-552">Lease expense</span></span>            | <span data-ttu-id="83103-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="83103-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="83103-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="83103-554">1,000\.00</span></span>               |   | <span data-ttu-id="83103-555">\-1,000.</span><span class="sxs-lookup"><span data-stu-id="83103-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="83103-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="83103-556">0\.00</span></span>                                   |
| <span data-ttu-id="83103-557">2</span><span class="sxs-lookup"><span data-stu-id="83103-557">2</span></span>          | <span data-ttu-id="83103-558">ค่าธรรมเนียมของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="83103-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="83103-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="83103-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="83103-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="83103-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="83103-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="83103-561">3\.00</span></span>                                   |
| <span data-ttu-id="83103-562">3</span><span class="sxs-lookup"><span data-stu-id="83103-562">3</span></span>          | <span data-ttu-id="83103-563">ค่าใช้จ่าย VAT</span><span class="sxs-lookup"><span data-stu-id="83103-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="83103-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="83103-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="83103-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="83103-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="83103-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="83103-566">5\.00</span></span>                                   |
| <span data-ttu-id="83103-567">4</span><span class="sxs-lookup"><span data-stu-id="83103-567">4</span></span>          | <span data-ttu-id="83103-568">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="83103-568">Clearing account</span></span>         | <span data-ttu-id="83103-569">\-1,000\.00</span><span class="sxs-lookup"><span data-stu-id="83103-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="83103-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="83103-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="83103-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="83103-571">0\.00</span></span>                   |   | <span data-ttu-id="83103-572">1,000</span><span class="sxs-lookup"><span data-stu-id="83103-572">1,000</span></span>                                           |                                                | <span data-ttu-id="83103-573">\-1,000.</span><span class="sxs-lookup"><span data-stu-id="83103-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="83103-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="83103-574">0\.00</span></span>                                   |
| <span data-ttu-id="83103-575">5</span><span class="sxs-lookup"><span data-stu-id="83103-575">5</span></span>          | <span data-ttu-id="83103-576">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="83103-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="83103-577">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="83103-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="83103-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="83103-578">1,008\.00</span></span>                                         | <span data-ttu-id="83103-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="83103-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="83103-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="83103-580">0\.00</span></span>                                   |
| <span data-ttu-id="83103-581">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="83103-581">6</span></span>          | <span data-ttu-id="83103-582">สิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="83103-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="83103-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="83103-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="83103-584">22,794</span><span class="sxs-lookup"><span data-stu-id="83103-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="83103-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="83103-585">22,793\.90</span></span>                              |
| <span data-ttu-id="83103-586">7</span><span class="sxs-lookup"><span data-stu-id="83103-586">7</span></span>          | <span data-ttu-id="83103-587">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="83103-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="83103-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="83103-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="83103-589">\-22,794.</span><span class="sxs-lookup"><span data-stu-id="83103-589">\-22,794</span></span>                                       | <span data-ttu-id="83103-590">1,000</span><span class="sxs-lookup"><span data-stu-id="83103-590">1,000</span></span>                                          | <span data-ttu-id="83103-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="83103-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="83103-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="83103-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="83103-593">8</span><span class="sxs-lookup"><span data-stu-id="83103-593">8</span></span>          | <span data-ttu-id="83103-594">ค่าใช้จ่ายดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="83103-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="83103-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="83103-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="83103-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="83103-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="83103-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="83103-597">94\.97</span></span>                                  |
| <span data-ttu-id="83103-598">9</span><span class="sxs-lookup"><span data-stu-id="83103-598">9</span></span>          | <span data-ttu-id="83103-599">เงินสด</span><span class="sxs-lookup"><span data-stu-id="83103-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="83103-600">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="83103-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="83103-601">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="83103-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="83103-602">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="83103-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="83103-603">10</span><span class="sxs-lookup"><span data-stu-id="83103-603">10</span></span>         | <span data-ttu-id="83103-604">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="83103-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="83103-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="83103-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="83103-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="83103-606">949\.75</span></span>                                        | <span data-ttu-id="83103-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="83103-607">949\.75</span></span>                                 |
| <span data-ttu-id="83103-608">11</span><span class="sxs-lookup"><span data-stu-id="83103-608">11</span></span>         | <span data-ttu-id="83103-609">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="83103-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="83103-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="83103-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="83103-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="83103-611">\-949\.75</span></span>                                      | <span data-ttu-id="83103-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="83103-612">\-949\.75</span></span>                               |


