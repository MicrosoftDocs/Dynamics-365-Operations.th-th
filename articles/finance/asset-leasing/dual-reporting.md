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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a7d9b3ea3d4f1d48b8a7326bd5a01d3119310c62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003192"
---
# <a name="dual-reporting"></a><span data-ttu-id="2a7b2-103">การรายงานแบบคู่</span><span class="sxs-lookup"><span data-stu-id="2a7b2-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a7b2-104">หัวข้อนี้จะให้คำแนะนำเกี่ยวกับวิธีการที่คุณสามารถตอบสนองความต้องการสำหรับการรายงานมาตรฐาน Financial Reporting ระหว่างประเทศ (IFRS) และการรายงานตามกฎหมายในการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="2a7b2-105">ความคุ้นเคยกับชั้นของการลงรายการบัญชีใน Microsoft Dynamics 365 Finance จำเป็นต้องใช้และจะทำให้เข้าใจง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="2a7b2-106">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-106">Example</span></span>

<span data-ttu-id="2a7b2-107">บัญชีตัวอย่างต่อไปนี้สำหรับการเช่าภายใต้การรายงานทางกฎหมายของอิตาลีโดยใช้ทั้งวิธีการเงินสดเป็นพื้นฐานและวิธีการรายงาน IFRS</span><span class="sxs-lookup"><span data-stu-id="2a7b2-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="2a7b2-108">บริษัทต้องสร้างสมุดบัญชีสามเล่มให้กับบัญชีสำหรับทั้งข้อกำหนดตามกฎหมายอิตาลีและข้อกำหนด IFRS 16</span><span class="sxs-lookup"><span data-stu-id="2a7b2-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="2a7b2-109">ต้องมีสมุดบัญชีหนึ่งเล่มสำหรับ IFRS 16 สมุดบัญชีหนึ่งเล่มจำเป็นสำหรับข้อกำหนดตามกฎหมาย และต้องมีสมุดบัญชีหนึ่งเล่มเพื่อย้อนกลับการลงรายการบัญชีตามกฎหมายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="2a7b2-110">จะมีการตั้งค่าสมุดบัญชีดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="2a7b2-111">**สมุดบัญชี IFRS 16**</span><span class="sxs-lookup"><span data-stu-id="2a7b2-111">**IFRS 16 book**</span></span>

<span data-ttu-id="2a7b2-112">มีการตั้งค่าสมุดบัญชี IFRS 16 ดังนั้นจึงสอดคล้องกับมาตรฐานการบัญชี IFRS 16</span><span class="sxs-lookup"><span data-stu-id="2a7b2-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="2a7b2-113">รายการทั้งหมดที่มีการลงรายการบัญชีในสมุดบัญชีนี้จะได้รับการลงรายการบัญชีในชั้นแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="2a7b2-114">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-114">Name</span></span>                                    | <span data-ttu-id="2a7b2-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="2a7b2-116">ชนิดของสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-116">Book type</span></span>                               | <span data-ttu-id="2a7b2-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="2a7b2-117">IFRS 16</span></span>        |
| <span data-ttu-id="2a7b2-118">คำอธิบายสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-118">Book description</span></span>                        | <span data-ttu-id="2a7b2-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="2a7b2-119">IFRS 16</span></span>        |
| <span data-ttu-id="2a7b2-120">ชั้นของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-120">Posting Layer</span></span>                           | <span data-ttu-id="2a7b2-121">ชั้นที่กำหนดเอง 1</span><span class="sxs-lookup"><span data-stu-id="2a7b2-121">Custom layer 1</span></span> |
| <span data-ttu-id="2a7b2-122">ชนิดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-122">Lease Type</span></span>                              | <span data-ttu-id="2a7b2-123">Finance</span><span class="sxs-lookup"><span data-stu-id="2a7b2-123">Finance</span></span>        |
| <span data-ttu-id="2a7b2-124">กรอบงานการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-124">Accounting Framework</span></span>                    | <span data-ttu-id="2a7b2-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="2a7b2-125">IFRS 16</span></span>        |
| <span data-ttu-id="2a7b2-126">การตั้งค่าระยะเวลาของสัญญาเช่า / อายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="2a7b2-127">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-127">0.00</span></span>           |
| <span data-ttu-id="2a7b2-128">การตั้งค่ามูลค่าปัจจุบัน / มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="2a7b2-129">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-129">0.00</span></span>           |
| <span data-ttu-id="2a7b2-130">ขีดจำกัดระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-130">Short-term threshold</span></span>                    | <span data-ttu-id="2a7b2-131">12</span><span class="sxs-lookup"><span data-stu-id="2a7b2-131">12</span></span>             |
| <span data-ttu-id="2a7b2-132">ขีดจำกัดมูลค่าต่ำ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-132">Low Value Threshold</span></span>                     | <span data-ttu-id="2a7b2-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-133">5,000.00</span></span>       |
| <span data-ttu-id="2a7b2-134">จ่ายให้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-134">Pay to Vendor</span></span>                           | <span data-ttu-id="2a7b2-135">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="2a7b2-135">No</span></span>             |

<span data-ttu-id="2a7b2-136">**สมุดบัญชีตามกฎหมาย**</span><span class="sxs-lookup"><span data-stu-id="2a7b2-136">**Statutory book**</span></span>

<span data-ttu-id="2a7b2-137">สมุดบัญชีตามกฎหมายเป็นสมุดบัญชีเงินสดซึ่งบริษัทจะเป็นผู้ชำระค่าใช้จ่ายในการเช่าโดยมียอดเงินสดที่ชำระให้แก่ลูกค้าแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="2a7b2-138">สมุดบัญชีเล่มนี้จะไม่ทำให้เกิดสิทธิ์การใช้สินทรัพย์หรือหนี้สินสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="2a7b2-139">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-139">Name</span></span>                                    | <span data-ttu-id="2a7b2-140">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="2a7b2-141">ชนิดของสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-141">Book type</span></span>                               | <span data-ttu-id="2a7b2-142">ตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-142">Statutory</span></span>   |
| <span data-ttu-id="2a7b2-143">คำอธิบายสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-143">Book description</span></span>                        | <span data-ttu-id="2a7b2-144">GAAP ท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-144">Local GAAP</span></span>  |
| <span data-ttu-id="2a7b2-145">ชั้นของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-145">Posting Layer</span></span>                           | <span data-ttu-id="2a7b2-146">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-146">Current</span></span>     |
| <span data-ttu-id="2a7b2-147">ชนิดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-147">Lease Type</span></span>                              | <span data-ttu-id="2a7b2-148">อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-148">Automatic</span></span>   |
| <span data-ttu-id="2a7b2-149">กรอบงานการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-149">Accounting Framework</span></span>                    | <span data-ttu-id="2a7b2-150">เกณฑ์เงินสด</span><span class="sxs-lookup"><span data-stu-id="2a7b2-150">Cash basis</span></span>  |
| <span data-ttu-id="2a7b2-151">การตั้งค่าระยะเวลาของสัญญาเช่า / อายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="2a7b2-152">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-152">0.00</span></span>        |
| <span data-ttu-id="2a7b2-153">การตั้งค่ามูลค่าปัจจุบัน / มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="2a7b2-154">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-154">0.00</span></span>        |
| <span data-ttu-id="2a7b2-155">ขีดจำกัดระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-155">Short-term threshold</span></span>                    | <span data-ttu-id="2a7b2-156">0</span><span class="sxs-lookup"><span data-stu-id="2a7b2-156">0</span></span>           |
| <span data-ttu-id="2a7b2-157">ขีดจำกัดมูลค่าต่ำ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-157">Low Value Threshold</span></span>                     | <span data-ttu-id="2a7b2-158">0</span><span class="sxs-lookup"><span data-stu-id="2a7b2-158">0</span></span>           |
| <span data-ttu-id="2a7b2-159">จ่ายให้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-159">Pay to Vendor</span></span>                           | <span data-ttu-id="2a7b2-160">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="2a7b2-160">No</span></span>          |

<span data-ttu-id="2a7b2-161">**สมุดบัญชีการกลับรายการตามกฎหมาย**</span><span class="sxs-lookup"><span data-stu-id="2a7b2-161">**Statutory reversal book**</span></span>

<span data-ttu-id="2a7b2-162">สมุดบัญชีการกลับรายการตามกฎหมายถูกตั้งค่าในลักษณะเดียวกับสมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="2a7b2-163">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-163">Name</span></span>                                    | <span data-ttu-id="2a7b2-164">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="2a7b2-165">ชนิดของสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-165">Book type</span></span>                               | <span data-ttu-id="2a7b2-166">ตามกฎหมาย – การกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="2a7b2-167">คำอธิบายสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-167">Book description</span></span>                        | <span data-ttu-id="2a7b2-168">จองเพื่อกลับรายการสมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="2a7b2-169">ชั้นของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-169">Posting Layer</span></span>                           | <span data-ttu-id="2a7b2-170">ชั้นที่กำหนดเอง 1</span><span class="sxs-lookup"><span data-stu-id="2a7b2-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="2a7b2-171">ชนิดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-171">Lease Type</span></span>                              | <span data-ttu-id="2a7b2-172">อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-172">Automatic</span></span>                      |
| <span data-ttu-id="2a7b2-173">กรอบงานการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-173">Accounting Framework</span></span>                    | <span data-ttu-id="2a7b2-174">เกณฑ์เงินสด</span><span class="sxs-lookup"><span data-stu-id="2a7b2-174">Cash basis</span></span>                     |
| <span data-ttu-id="2a7b2-175">การตั้งค่าระยะเวลาของสัญญาเช่า / อายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="2a7b2-176">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-176">0.00</span></span>                           |
| <span data-ttu-id="2a7b2-177">การตั้งค่ามูลค่าปัจจุบัน / มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="2a7b2-178">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-178">0.00</span></span>                           |
| <span data-ttu-id="2a7b2-179">ขีดจำกัดระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-179">Short-term threshold</span></span>                    | <span data-ttu-id="2a7b2-180">0</span><span class="sxs-lookup"><span data-stu-id="2a7b2-180">0</span></span>                              |
| <span data-ttu-id="2a7b2-181">ขีดจำกัดมูลค่าต่ำ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-181">Low Value Threshold</span></span>                     | <span data-ttu-id="2a7b2-182">0</span><span class="sxs-lookup"><span data-stu-id="2a7b2-182">0</span></span>                              |
| <span data-ttu-id="2a7b2-183">จ่ายให้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-183">Pay to Vendor</span></span>                           | <span data-ttu-id="2a7b2-184">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="2a7b2-184">No</span></span>                             |

<span data-ttu-id="2a7b2-185">สำหรับตัวอย่างนี้ มีการสร้างการเช่าที่มีการตั้งค่าต่อไปนี้ในแท็บ **ทั่วไป** และ **รายการกำหนดการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="2a7b2-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="2a7b2-186">**แท็บทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="2a7b2-186">**General tab**</span></span>

| <span data-ttu-id="2a7b2-187">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-187">Field</span></span>                      | <span data-ttu-id="2a7b2-188">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="2a7b2-189">อัตราดอกเบี้ยเงินกู้ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="2a7b2-189">Incremental borrowing rate</span></span> | <span data-ttu-id="2a7b2-190">5%</span><span class="sxs-lookup"><span data-stu-id="2a7b2-190">5%</span></span>               |
| <span data-ttu-id="2a7b2-191">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-191">Commencement date</span></span>          | <span data-ttu-id="2a7b2-192">วันที่ 1/1/2020</span><span class="sxs-lookup"><span data-stu-id="2a7b2-192">1/1/2020</span></span>         |
| <span data-ttu-id="2a7b2-193">กลุ่มสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-193">Lease group</span></span>                | <span data-ttu-id="2a7b2-194">อาคาร</span><span class="sxs-lookup"><span data-stu-id="2a7b2-194">Buildings</span></span>        |
| <span data-ttu-id="2a7b2-195">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-195">Vendor</span></span>                     | <span data-ttu-id="2a7b2-196">1001</span><span class="sxs-lookup"><span data-stu-id="2a7b2-196">1001</span></span>             |
| <span data-ttu-id="2a7b2-197">มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-197">Fair value of the asset</span></span>    | <span data-ttu-id="2a7b2-198">245,000</span><span class="sxs-lookup"><span data-stu-id="2a7b2-198">245,000</span></span>          |
| <span data-ttu-id="2a7b2-199">อายุการใช้งานของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-199">Asset useful life</span></span>          | <span data-ttu-id="2a7b2-200">120</span><span class="sxs-lookup"><span data-stu-id="2a7b2-200">120</span></span>              |
| <span data-ttu-id="2a7b2-201">ชนิดเงินรายปี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-201">Annuity type</span></span>               | <span data-ttu-id="2a7b2-202">เงินรายปีสามัญ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-202">Ordinary annuity</span></span> |
| <span data-ttu-id="2a7b2-203">ช่วงเวลาการทบต้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-203">Compounding interval</span></span>       | <span data-ttu-id="2a7b2-204">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-204">Monthly</span></span>          |

<span data-ttu-id="2a7b2-205">**แท็บรายการกำหนดการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="2a7b2-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="2a7b2-206">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-206">Field</span></span>             | <span data-ttu-id="2a7b2-207">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="2a7b2-208">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-208">Start date</span></span>        | <span data-ttu-id="2a7b2-209">วันที่ 1/1/2020</span><span class="sxs-lookup"><span data-stu-id="2a7b2-209">1/1/2020</span></span>   |
| <span data-ttu-id="2a7b2-210">ช่วงรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="2a7b2-210">Period interval</span></span>   | <span data-ttu-id="2a7b2-211">เดือน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-211">Months</span></span>     |
| <span data-ttu-id="2a7b2-212">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="2a7b2-212">Periods</span></span>           | <span data-ttu-id="2a7b2-213">24</span><span class="sxs-lookup"><span data-stu-id="2a7b2-213">24</span></span>         |
| <span data-ttu-id="2a7b2-214">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="2a7b2-214">End date</span></span>          | <span data-ttu-id="2a7b2-215">วันที่ 12/31/2020</span><span class="sxs-lookup"><span data-stu-id="2a7b2-215">12/31/2020</span></span> |
| <span data-ttu-id="2a7b2-216">ความถี่ในการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-216">Payment frequency</span></span> | <span data-ttu-id="2a7b2-217">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-217">Monthly</span></span>    |
| <span data-ttu-id="2a7b2-218">ยอดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-218">Payment amount</span></span>    | <span data-ttu-id="2a7b2-219">1,000</span><span class="sxs-lookup"><span data-stu-id="2a7b2-219">1,000</span></span>      |

<span data-ttu-id="2a7b2-220">ในการลงบัญชีสำหรับชั่การเช่านี้ภายใต้สองกรอบงาน คุณใช้ชั้นของการลงรายการบัญชีปัจจุบันและชั้นของการลงรายการบัญชีที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="2a7b2-221">ตารางต่อไปนี้จะแสดงตัวอย่างของรายการสมุดรายวันทั้งหมดที่จำเป็นต้องแสดงถึงการเงินภายใต้มาตรฐานการรายงานแต่ละฉบับ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="2a7b2-222">คำอธิบายโดยละเอียดของรายการสมุดรายวันแต่ละรายการสำหรับเดือนแรกของการเช่ามีให้หลังจากนี้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="2a7b2-223">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="2a7b2-224">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="2a7b2-225">สมุดบัญชีตามกฎหมาย (ชั้นปัจจุบัน)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="2a7b2-226">ผลรวมชั้นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-226">Current layer total</span></span></th>
<th><span data-ttu-id="2a7b2-227">สมุดบัญชีการกลับรายการ (ชั้นที่กำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="2a7b2-228">สมุดบัญชี IFRS 16 (ชั้นที่กำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="2a7b2-229">ชั้นปัจจุบัน + ยอดรวมชั้นแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2a7b2-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="2a7b2-230">JE-100</span></span></th>
<th><span data-ttu-id="2a7b2-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="2a7b2-231">JE-110</span></span></th>
<th><span data-ttu-id="2a7b2-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="2a7b2-232">JE-120</span></span></th>
<th><span data-ttu-id="2a7b2-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="2a7b2-233">JE-130</span></span></th>
<th><span data-ttu-id="2a7b2-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="2a7b2-234">JE-140</span></span></th>
<th><span data-ttu-id="2a7b2-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="2a7b2-235">JE-150</span></span></th>
<th><span data-ttu-id="2a7b2-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="2a7b2-236">JE-160</span></span></th>
<th><span data-ttu-id="2a7b2-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="2a7b2-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2a7b2-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="2a7b2-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="2a7b2-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="2a7b2-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="2a7b2-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="2a7b2-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="2a7b2-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="2a7b2-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2a7b2-246">1</span><span class="sxs-lookup"><span data-stu-id="2a7b2-246">1</span></span></td>
<td><span data-ttu-id="2a7b2-247">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-247">Lease expense</span></span></td>
<td><span data-ttu-id="2a7b2-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-249">1,000.00</span></span></td>
<td><span data-ttu-id="2a7b2-250">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="2a7b2-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-251">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-252">2</span><span class="sxs-lookup"><span data-stu-id="2a7b2-252">2</span></span></td>
<td><span data-ttu-id="2a7b2-253">ค่าธรรมเนียมของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="2a7b2-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-254">3.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-255">3.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-256">3.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-257">3</span><span class="sxs-lookup"><span data-stu-id="2a7b2-257">3</span></span></td>
<td><span data-ttu-id="2a7b2-258">ค่าใช้จ่าย VAT</span><span class="sxs-lookup"><span data-stu-id="2a7b2-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-259">5.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-260">5.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-261">5.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-262">4</span><span class="sxs-lookup"><span data-stu-id="2a7b2-262">4</span></span></td>
<td><span data-ttu-id="2a7b2-263">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-263">Clearing account</span></span></td>
<td><span data-ttu-id="2a7b2-264">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="2a7b2-264">-1,000.00</span></span></td>
<td><span data-ttu-id="2a7b2-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-266">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-266">0.00</span></span></td>
<td><span data-ttu-id="2a7b2-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-268">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="2a7b2-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-269">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-270">5</span><span class="sxs-lookup"><span data-stu-id="2a7b2-270">5</span></span></td>
<td><span data-ttu-id="2a7b2-271">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-272">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-272">-1,008.00</span></span></td>
<td><span data-ttu-id="2a7b2-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-273">1,008.00</span></span></td>
<td><span data-ttu-id="2a7b2-274">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-275">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-276">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-276">6</span></span></td>
<td><span data-ttu-id="2a7b2-277">สิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-278">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="2a7b2-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-281">7</span><span class="sxs-lookup"><span data-stu-id="2a7b2-281">7</span></span></td>
<td><span data-ttu-id="2a7b2-282">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-283">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-284">-22,794.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-284">-22,794.00</span></span></td>
<td><span data-ttu-id="2a7b2-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-285">1,000.00</span></span></td>
<td><span data-ttu-id="2a7b2-286">-94.97</span><span class="sxs-lookup"><span data-stu-id="2a7b2-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-287">-21,888.87</span><span class="sxs-lookup"><span data-stu-id="2a7b2-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-288">8</span><span class="sxs-lookup"><span data-stu-id="2a7b2-288">8</span></span></td>
<td><span data-ttu-id="2a7b2-289">ค่าใช้จ่ายดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-290">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-291">94.97</span><span class="sxs-lookup"><span data-stu-id="2a7b2-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-292">94.97</span><span class="sxs-lookup"><span data-stu-id="2a7b2-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-293">9</span><span class="sxs-lookup"><span data-stu-id="2a7b2-293">9</span></span></td>
<td><span data-ttu-id="2a7b2-294">เงินสด</span><span class="sxs-lookup"><span data-stu-id="2a7b2-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-295">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-295">-1,008.00</span></span></td>
<td><span data-ttu-id="2a7b2-296">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-297">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-298">10</span><span class="sxs-lookup"><span data-stu-id="2a7b2-298">10</span></span></td>
<td><span data-ttu-id="2a7b2-299">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="2a7b2-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-300">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-301">949.75</span><span class="sxs-lookup"><span data-stu-id="2a7b2-301">949.75</span></span></td>
<td><span data-ttu-id="2a7b2-302">949.75</span><span class="sxs-lookup"><span data-stu-id="2a7b2-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-303">11</span><span class="sxs-lookup"><span data-stu-id="2a7b2-303">11</span></span></td>
<td><span data-ttu-id="2a7b2-304">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="2a7b2-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-305">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-306">-949.75</span><span class="sxs-lookup"><span data-stu-id="2a7b2-306">-949.75</span></span></td>
<td><span data-ttu-id="2a7b2-307">-949.75</span><span class="sxs-lookup"><span data-stu-id="2a7b2-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2a7b2-308">ตามตารางก่อนหน้านี้แสดงให้เห็น สมุดบัญชีสามเล่มต้องมีการรายงานที่มีการรายงานตามกฎหมายและการรายงาน IFRS</span><span class="sxs-lookup"><span data-stu-id="2a7b2-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="2a7b2-309">สมุดบัญชีตามกฎหมายจะบันทึกการชำระค่าเช่าตามกฎสำหรับการบัญชีเงินสดในชั้นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="2a7b2-310">สมุดบัญชีการกลับรายการตามกฎหมายย้อนกลับรายการสมุดรายวันตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="2a7b2-311">สมุดบัญชี IFRS 16 สร้างรายการสมุดรายวันที่จำเป็นต้องใช้ภายใต้ IFRS 16</span><span class="sxs-lookup"><span data-stu-id="2a7b2-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="2a7b2-312">คุณต้องป้อนการเช่าเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="2a7b2-312">You must enter a lease only one time.</span></span> <span data-ttu-id="2a7b2-313">จากนั้นคุณสามารถเปิดหน้า **สมุดบัญชี** เพื่อดูสมุดบัญชีทั้งหมดที่เชื่อมโยงกับการเช่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="2a7b2-314">เมื่อคุณสร้างสมุดบัญชี สมุดบัญชีทั้งสามเล่มต้องเชื่อมโยงกับเรกคอร์ดการเช่าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="2a7b2-315">รายการสมุดรายวันแรกจะบันทึกค่าใช้จ่ายในการเช่าภายใต้สมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="2a7b2-316">คุณสามารถสร้างการชำระเงินอย่างใดอย่างหนึ่งในชุดงานหรือโดยการเลือกกำหนดการชำระเงินในสมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="2a7b2-317">สำหรับตัวอย่างนี้ รายการสมุดรายวันต่อไปนี้จะถูกสร้างขึ้นสำหรับสมุดบัญชีตามกฎหมายจากกำหนดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="2a7b2-318">การชำระค่าเช่า – 1/31/2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="2a7b2-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="2a7b2-319">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-319">Account type</span></span> | <span data-ttu-id="2a7b2-320">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-320">Account number</span></span> | <span data-ttu-id="2a7b2-321">ชั้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-321">Layer</span></span>   | <span data-ttu-id="2a7b2-322">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-322">Account description</span></span> | <span data-ttu-id="2a7b2-323">เดบิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-323">Debit</span></span>    | <span data-ttu-id="2a7b2-324">เครดิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="2a7b2-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-325">Ledger</span></span>       | <span data-ttu-id="2a7b2-326">1</span><span class="sxs-lookup"><span data-stu-id="2a7b2-326">1</span></span>              | <span data-ttu-id="2a7b2-327">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-327">Current</span></span> | <span data-ttu-id="2a7b2-328">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-328">Lease expense</span></span>       | <span data-ttu-id="2a7b2-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-329">1,000.00</span></span> |          |
| <span data-ttu-id="2a7b2-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-330">Ledger</span></span>       | <span data-ttu-id="2a7b2-331">4</span><span class="sxs-lookup"><span data-stu-id="2a7b2-331">4</span></span>              | <span data-ttu-id="2a7b2-332">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-332">Current</span></span> | <span data-ttu-id="2a7b2-333">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-333">Clearing account</span></span>    |          | <span data-ttu-id="2a7b2-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-334">1,000.00</span></span> |

<span data-ttu-id="2a7b2-335">เสมียนบัญชีเจ้าหนี้ใช้ฟังก์ชัน Dynamics 365 มาตรฐานเพื่อสร้างใบแจ้งหนี้ที่จะชำระเงินสำหรับการเช่าสินทรัพย์ภายนอกสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="2a7b2-336">อย่างไรก็ตาม แทนที่จะเลือก **ค่าใช้จ่ายของสัญญาเช่า** เป็นบัญชีเดบิต เสมียนบัญชีเจ้าหนี้เลือกบัญชีเงินฝากเพื่อสร้างรายการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="2a7b2-337">กระบวนการ AP – 1/31/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="2a7b2-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="2a7b2-338">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-338">Account type</span></span> | <span data-ttu-id="2a7b2-339">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-339">Account number</span></span> | <span data-ttu-id="2a7b2-340">ชั้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-340">Layer</span></span>   | <span data-ttu-id="2a7b2-341">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-341">Account description</span></span> | <span data-ttu-id="2a7b2-342">เดบิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-342">Debit</span></span>    | <span data-ttu-id="2a7b2-343">เครดิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="2a7b2-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-344">Ledger</span></span>       | <span data-ttu-id="2a7b2-345">4</span><span class="sxs-lookup"><span data-stu-id="2a7b2-345">4</span></span>              | <span data-ttu-id="2a7b2-346">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-346">Current</span></span> | <span data-ttu-id="2a7b2-347">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-347">Clearing account</span></span>    | <span data-ttu-id="2a7b2-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-348">1,000.00</span></span> |          |
| <span data-ttu-id="2a7b2-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-349">Ledger</span></span>       | <span data-ttu-id="2a7b2-350">2</span><span class="sxs-lookup"><span data-stu-id="2a7b2-350">2</span></span>              | <span data-ttu-id="2a7b2-351">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-351">Current</span></span> | <span data-ttu-id="2a7b2-352">ค่าธรรมเนียมของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="2a7b2-352">Bank fee</span></span>            | <span data-ttu-id="2a7b2-353">3.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-353">3.00</span></span>     |          |
| <span data-ttu-id="2a7b2-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-354">Ledger</span></span>       | <span data-ttu-id="2a7b2-355">3</span><span class="sxs-lookup"><span data-stu-id="2a7b2-355">3</span></span>              | <span data-ttu-id="2a7b2-356">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-356">Current</span></span> | <span data-ttu-id="2a7b2-357">ค่าใช้จ่าย VAT</span><span class="sxs-lookup"><span data-stu-id="2a7b2-357">VAT expense</span></span>         | <span data-ttu-id="2a7b2-358">5.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-358">5.00</span></span>     |          |
| <span data-ttu-id="2a7b2-359">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-359">Vendor</span></span>       | <span data-ttu-id="2a7b2-360">5</span><span class="sxs-lookup"><span data-stu-id="2a7b2-360">5</span></span>              | <span data-ttu-id="2a7b2-361">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-361">Current</span></span> | <span data-ttu-id="2a7b2-362">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-362">Accounts payable</span></span>    |          | <span data-ttu-id="2a7b2-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-363">1,008.00</span></span> |

<span data-ttu-id="2a7b2-364">เมื่อมีการออกคำสั่งให้กับผู้จัดจำหน่าย คุณทำตามขั้นตอนการชำระเงินทั่วไป</span><span class="sxs-lookup"><span data-stu-id="2a7b2-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="2a7b2-365">ในระหว่างกระบวนการนี้ จะมีการสร้างรายการสมุดรายวันต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="2a7b2-366">การชำระเงินสด– 1/31/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="2a7b2-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="2a7b2-367">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-367">Account type</span></span> | <span data-ttu-id="2a7b2-368">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-368">Account number</span></span> | <span data-ttu-id="2a7b2-369">ชั้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-369">Layer</span></span>   | <span data-ttu-id="2a7b2-370">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-370">Account description</span></span> | <span data-ttu-id="2a7b2-371">เดบิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-371">Debit</span></span>    | <span data-ttu-id="2a7b2-372">เครดิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="2a7b2-373">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-373">Vendor</span></span>       | <span data-ttu-id="2a7b2-374">5</span><span class="sxs-lookup"><span data-stu-id="2a7b2-374">5</span></span>              | <span data-ttu-id="2a7b2-375">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-375">Current</span></span> | <span data-ttu-id="2a7b2-376">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-376">Accounts Payable</span></span>    | <span data-ttu-id="2a7b2-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-377">1,008.00</span></span> |          |
| <span data-ttu-id="2a7b2-378">ธนาคาร</span><span class="sxs-lookup"><span data-stu-id="2a7b2-378">Bank</span></span>         | <span data-ttu-id="2a7b2-379">9</span><span class="sxs-lookup"><span data-stu-id="2a7b2-379">9</span></span>              | <span data-ttu-id="2a7b2-380">ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-380">Current</span></span> | <span data-ttu-id="2a7b2-381">เงินสด</span><span class="sxs-lookup"><span data-stu-id="2a7b2-381">Cash</span></span>                |          | <span data-ttu-id="2a7b2-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-382">1,008.00</span></span> |

<span data-ttu-id="2a7b2-383">ณ จุดนี้ คุณมีการลงบัญชีสำหรับการเช่านี้ทั้งหมดภายใต้ข้อกำหนดในการรายงานตามกฎหมายและสามารถสร้างงบทดลองโดยใช้ชั้นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="2a7b2-384">ระบบส่งคืนงบทดลองที่มีตัวเลขต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="2a7b2-385">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="2a7b2-386">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="2a7b2-387">สมุดบัญชีตามกฎหมาย (ชั้นปัจจุบัน)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="2a7b2-388">ผลรวมชั้นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2a7b2-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="2a7b2-389">JE-100</span></span></th>
<th><span data-ttu-id="2a7b2-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="2a7b2-390">JE-110</span></span></th>
<th><span data-ttu-id="2a7b2-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="2a7b2-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2a7b2-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="2a7b2-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="2a7b2-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2a7b2-395">1</span><span class="sxs-lookup"><span data-stu-id="2a7b2-395">1</span></span></td>
<td><span data-ttu-id="2a7b2-396">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-396">Lease expense</span></span></td>
<td><span data-ttu-id="2a7b2-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-399">2</span><span class="sxs-lookup"><span data-stu-id="2a7b2-399">2</span></span></td>
<td><span data-ttu-id="2a7b2-400">ค่าธรรมเนียมของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="2a7b2-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-401">3.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-402">3.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-403">3</span><span class="sxs-lookup"><span data-stu-id="2a7b2-403">3</span></span></td>
<td><span data-ttu-id="2a7b2-404">ค่าใช้จ่าย VAT</span><span class="sxs-lookup"><span data-stu-id="2a7b2-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-405">5.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-406">5.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-407">4</span><span class="sxs-lookup"><span data-stu-id="2a7b2-407">4</span></span></td>
<td><span data-ttu-id="2a7b2-408">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-408">Clearing account</span></span></td>
<td><span data-ttu-id="2a7b2-409">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="2a7b2-409">-1,000.00</span></span></td>
<td><span data-ttu-id="2a7b2-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-411">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-412">5</span><span class="sxs-lookup"><span data-stu-id="2a7b2-412">5</span></span></td>
<td><span data-ttu-id="2a7b2-413">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="2a7b2-414">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-414">-1,008.00</span></span></td>
<td><span data-ttu-id="2a7b2-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-415">1,008.00</span></span></td>
<td><span data-ttu-id="2a7b2-416">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-417">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-417">6</span></span></td>
<td><span data-ttu-id="2a7b2-418">สิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-419">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-420">7</span><span class="sxs-lookup"><span data-stu-id="2a7b2-420">7</span></span></td>
<td><span data-ttu-id="2a7b2-421">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-422">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-423">8</span><span class="sxs-lookup"><span data-stu-id="2a7b2-423">8</span></span></td>
<td><span data-ttu-id="2a7b2-424">ค่าใช้จ่ายดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-425">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-426">9</span><span class="sxs-lookup"><span data-stu-id="2a7b2-426">9</span></span></td>
<td><span data-ttu-id="2a7b2-427">เงินสด</span><span class="sxs-lookup"><span data-stu-id="2a7b2-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-428">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-428">-1,008.00</span></span></td>
<td><span data-ttu-id="2a7b2-429">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-430">10</span><span class="sxs-lookup"><span data-stu-id="2a7b2-430">10</span></span></td>
<td><span data-ttu-id="2a7b2-431">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="2a7b2-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-432">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a7b2-433">11</span><span class="sxs-lookup"><span data-stu-id="2a7b2-433">11</span></span></td>
<td><span data-ttu-id="2a7b2-434">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="2a7b2-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="2a7b2-435">0.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2a7b2-436">ถ้าคุณต้องการใช้ตัวเลข IFRS 16 เพื่อรันงบทดลองเดียวกัน ต้องย้อนกลับรายการสมุดรายวันบัญชีตามกฎหมาย และต้องลงรายการบัญชีรายการสมุดรายวัน IFRS 16</span><span class="sxs-lookup"><span data-stu-id="2a7b2-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="2a7b2-437">เมื่อต้องการย้อนกลับรายการสมุดรายวันตามกฎหมาย ตัวอย่างนี้มีสมุดบัญชีการกลับรายการตามกฎหมายที่มีการตั้งค่าเดียวกันกับสมุดบัญชีตามกฎหมายแต่โปรไฟล์การลงรายการบัญชีตรงข้ามกัน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="2a7b2-438">ตัวอย่างเช่น สมุดบัญชีที่ *มีการเดบิต* บัญชีค่าใช้จ่ายในการเช่า แต่สมุดบัญชีการกลับรายการจะ *เครดิต* บัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="2a7b2-439">ความสัมพันธ์เหล่านี้จะได้รับการกำหนดอย่างง่ายดายในบัญชีการลงรายการบัญชีการเช่าสินทรัพย์บนหน้า **พารามิเตอร์การเช่าสินทรัพย์** (**การเช่าสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การเช่าสินทรัพย์**)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="2a7b2-440">เมื่อใช้กระบวนการเดียวกันกับที่ใช้สำหรับสมุดบัญชีที่ตามกฎหมายไว้สำหรับสมุดบัญชีการกลับ รายการสมุดรายวันต่อไปนี้จะถูกผลิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="2a7b2-441">ความแตกต่างของสมุดบัญชีการกลับรายการสมุดบัญชีการกลับรายการจากสมุดบัญชีตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="2a7b2-442">นอกจากนี้ยังมีการจัดทำรายการย้อนกลับไปยังชั้นที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="2a7b2-443">เมื่อรันงบทดลองที่ชั้นปัจจุบัน จะไม่มีการรวมรายการสมุดรายวันการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="2a7b2-444">การชำระค่าเช่า – 1/31/2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="2a7b2-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="2a7b2-445">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-445">Account type</span></span> | <span data-ttu-id="2a7b2-446">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-446">Account number</span></span> | <span data-ttu-id="2a7b2-447">ชั้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-447">Layer</span></span>  | <span data-ttu-id="2a7b2-448">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-448">Account description</span></span> | <span data-ttu-id="2a7b2-449">เดบิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-449">Debit</span></span>    | <span data-ttu-id="2a7b2-450">เครดิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="2a7b2-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-451">Ledger</span></span>       | <span data-ttu-id="2a7b2-452">4</span><span class="sxs-lookup"><span data-stu-id="2a7b2-452">4</span></span>              | <span data-ttu-id="2a7b2-453">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-453">Custom</span></span> | <span data-ttu-id="2a7b2-454">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-454">Clearing account</span></span>    | <span data-ttu-id="2a7b2-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-455">1,000.00</span></span> |          |
| <span data-ttu-id="2a7b2-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-456">Ledger</span></span>       | <span data-ttu-id="2a7b2-457">1</span><span class="sxs-lookup"><span data-stu-id="2a7b2-457">1</span></span>              | <span data-ttu-id="2a7b2-458">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-458">Custom</span></span> | <span data-ttu-id="2a7b2-459">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-459">Lease expense</span></span>       |          | <span data-ttu-id="2a7b2-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-460">1,000.00</span></span> |

<span data-ttu-id="2a7b2-461">หลังจากที่คุณได้ตัดรายการสมุดรายวันตามกฎหมายแล้ว คุณจะจองรายการสมุดรายวันทั้งหมดที่มี IFRS 16 ต้องมีอยู่ในสมุดบัญชี IFRS 16</span><span class="sxs-lookup"><span data-stu-id="2a7b2-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="2a7b2-462">รายการเหล่านี้รวมถึงการรับรู้เริ่มต้นของสิทธิ์การใช้สินทรัพย์และหนี้สิน และเรกคอร์ดของดอกเบี้ยและค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="2a7b2-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="2a7b2-463">การรับรู้เมื่อเริ่มแรก – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="2a7b2-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="2a7b2-464">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-464">Account type</span></span> | <span data-ttu-id="2a7b2-465">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-465">Account number</span></span> | <span data-ttu-id="2a7b2-466">ชั้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-466">Layer</span></span>  | <span data-ttu-id="2a7b2-467">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-467">Account description</span></span>      | <span data-ttu-id="2a7b2-468">เดบิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-468">Debit</span></span>     | <span data-ttu-id="2a7b2-469">เครดิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="2a7b2-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-470">Ledger</span></span>       | <span data-ttu-id="2a7b2-471">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-471">6</span></span>              | <span data-ttu-id="2a7b2-472">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-472">Custom</span></span> | <span data-ttu-id="2a7b2-473">สิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-473">ROU Asset</span></span>                | <span data-ttu-id="2a7b2-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="2a7b2-474">22,793.90</span></span> |           |
| <span data-ttu-id="2a7b2-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-475">Ledger</span></span>       | <span data-ttu-id="2a7b2-476">7</span><span class="sxs-lookup"><span data-stu-id="2a7b2-476">7</span></span>              | <span data-ttu-id="2a7b2-477">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-477">Custom</span></span> | <span data-ttu-id="2a7b2-478">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-478">Finance lease obligation</span></span> |           | <span data-ttu-id="2a7b2-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="2a7b2-479">22,793.90</span></span> |

<span data-ttu-id="2a7b2-480">มีการลงรายการบัญชีการชำระค่าเช่า เช่น การชำระค่าเช่าอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="2a7b2-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="2a7b2-481">เหตุผลสำหรับการใช้บัญชีเงินฝากคือเพื่อให้แน่ใจว่าเงินสดจะถูกเครดิตเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="2a7b2-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="2a7b2-482">การชำระค่าเช่า – 1/31/2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="2a7b2-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="2a7b2-483">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-483">Account type</span></span> | <span data-ttu-id="2a7b2-484">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-484">Account number</span></span> | <span data-ttu-id="2a7b2-485">ชั้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-485">Layer</span></span>  | <span data-ttu-id="2a7b2-486">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-486">Account description</span></span>      | <span data-ttu-id="2a7b2-487">เดบิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-487">Debit</span></span>    | <span data-ttu-id="2a7b2-488">เครดิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="2a7b2-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-489">Ledger</span></span>       | <span data-ttu-id="2a7b2-490">7</span><span class="sxs-lookup"><span data-stu-id="2a7b2-490">7</span></span>              | <span data-ttu-id="2a7b2-491">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-491">Custom</span></span> | <span data-ttu-id="2a7b2-492">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-492">Finance lease obligation</span></span> | <span data-ttu-id="2a7b2-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-493">1,000.00</span></span> |          |
| <span data-ttu-id="2a7b2-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-494">Ledger</span></span>       | <span data-ttu-id="2a7b2-495">4</span><span class="sxs-lookup"><span data-stu-id="2a7b2-495">4</span></span>              | <span data-ttu-id="2a7b2-496">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-496">Custom</span></span> | <span data-ttu-id="2a7b2-497">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-497">Clearing account</span></span>         |          | <span data-ttu-id="2a7b2-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-498">1,000.00</span></span> |

<span data-ttu-id="2a7b2-499">รายการสมุดรายวันดอกเบี้ยจ่ายถูกสร้างขึ้นจากกำหนดการตัดบัญชีของหนี้สิน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="2a7b2-500">ดอกเบี้ยจ่าย – 1/31/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="2a7b2-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="2a7b2-501">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-501">Account type</span></span> | <span data-ttu-id="2a7b2-502">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-502">Account number</span></span> | <span data-ttu-id="2a7b2-503">ชั้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-503">Layer</span></span>  | <span data-ttu-id="2a7b2-504">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-504">Account description</span></span>      | <span data-ttu-id="2a7b2-505">เดบิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-505">Debit</span></span> | <span data-ttu-id="2a7b2-506">เครดิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="2a7b2-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-507">Ledger</span></span>       | <span data-ttu-id="2a7b2-508">8</span><span class="sxs-lookup"><span data-stu-id="2a7b2-508">8</span></span>              | <span data-ttu-id="2a7b2-509">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-509">Custom</span></span> | <span data-ttu-id="2a7b2-510">ค่าใช้จ่ายดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-510">Interest expense</span></span>         | <span data-ttu-id="2a7b2-511">94.97</span><span class="sxs-lookup"><span data-stu-id="2a7b2-511">94.97</span></span> |        |
| <span data-ttu-id="2a7b2-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-512">Ledger</span></span>       | <span data-ttu-id="2a7b2-513">7</span><span class="sxs-lookup"><span data-stu-id="2a7b2-513">7</span></span>              | <span data-ttu-id="2a7b2-514">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-514">Custom</span></span> | <span data-ttu-id="2a7b2-515">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-515">Finance lease obligation</span></span> |       | <span data-ttu-id="2a7b2-516">94.97</span><span class="sxs-lookup"><span data-stu-id="2a7b2-516">94.97</span></span>  |

<span data-ttu-id="2a7b2-517">รายการสมุดรายวันค่าเสื่อมราคาถูกสร้างขึ้นจากกำหนดการค่าเสื่อมราคาของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="2a7b2-518">ค่าเสื่อมราคา – 1/31/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="2a7b2-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="2a7b2-519">ชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-519">Account type</span></span> | <span data-ttu-id="2a7b2-520">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-520">Account number</span></span> | <span data-ttu-id="2a7b2-521">ชั้น</span><span class="sxs-lookup"><span data-stu-id="2a7b2-521">Layer</span></span>  | <span data-ttu-id="2a7b2-522">คำอธิบายบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-522">Account description</span></span>      | <span data-ttu-id="2a7b2-523">เดบิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-523">Debit</span></span>  | <span data-ttu-id="2a7b2-524">เครดิต</span><span class="sxs-lookup"><span data-stu-id="2a7b2-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="2a7b2-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-525">Ledger</span></span>       | <span data-ttu-id="2a7b2-526">10</span><span class="sxs-lookup"><span data-stu-id="2a7b2-526">10</span></span>             | <span data-ttu-id="2a7b2-527">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-527">Custom</span></span> | <span data-ttu-id="2a7b2-528">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="2a7b2-528">Depreciation expense</span></span>     | <span data-ttu-id="2a7b2-529">949.75</span><span class="sxs-lookup"><span data-stu-id="2a7b2-529">949.75</span></span> |        |
| <span data-ttu-id="2a7b2-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="2a7b2-530">Ledger</span></span>       | <span data-ttu-id="2a7b2-531">11</span><span class="sxs-lookup"><span data-stu-id="2a7b2-531">11</span></span>             | <span data-ttu-id="2a7b2-532">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-532">Custom</span></span> | <span data-ttu-id="2a7b2-533">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="2a7b2-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="2a7b2-534">949.75</span><span class="sxs-lookup"><span data-stu-id="2a7b2-534">949.75</span></span> |

<span data-ttu-id="2a7b2-535">หลังจากที่มีการสร้างและลงรายการบัญชีสมุดรายวันทั้งหมดนี้แล้ว คุณจะเห็นค่า "ระดับชั้นที่กำหนดเอง 1" ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="2a7b2-536">โปรดทราบว่าคอลัมน์สุดท้ายรวมค่าธรรมเนียมของธนาคาร ค่าใช้จ่ายภาษีมูลค่าเพิ่ม (VAT) และการลดเงินสดจากชั้นก่อนหน้านี้ แต่ไม่รวมรายการสมุดรายวันการรายงานตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="2a7b2-537">ดังนั้น คุณจึงประสบความสำเร็จในการรายงานแบบคู่จริงได้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="2a7b2-538">ณ จุดนี้ บริษัทเพียงแค่ต้องรันงบทดลอง และรวมชั้นปัจจุบันและชั้นแบบกำหนดเองเพื่อสร้างงบทดลองของ IFRS</span><span class="sxs-lookup"><span data-stu-id="2a7b2-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="2a7b2-539">หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a7b2-539">Account No</span></span> | <span data-ttu-id="2a7b2-540">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-540">Description</span></span>              | <span data-ttu-id="2a7b2-541">สมุดบัญชีตามกฎหมาย\-ชั้นปัจจุบัน\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="2a7b2-542">สมุดบัญชีตามกฎหมาย\-ชั้นปัจจุบัน\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="2a7b2-543">สมุดบัญชีตามกฎหมาย\-ชั้นปัจจุบัน\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="2a7b2-544">ชั้นปัจจุบัน \- ผลรวม</span><span class="sxs-lookup"><span data-stu-id="2a7b2-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="2a7b2-545">สมุดบัญชีการกลับรายการ\-ชั้นแบบกำหนดเอง\-J\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="2a7b2-546">สมุดบัญชี IFRS 16\-ชั้นแบบกำหนดเอง\-J\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="2a7b2-547">สมุดบัญชี IFRS 16\-ชั้นแบบกำหนดเอง\-J\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="2a7b2-548">สมุดบัญชี IFRS 16\-ชั้นแบบกำหนดเอง\-J\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="2a7b2-549">สมุดบัญชี IFRS 16\-ชั้นแบบกำหนดเอง\-J\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="2a7b2-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="2a7b2-550">ชั้นแบบกำหนดเอง \+ ชั้นปัจจุบัน \- ผลรวม</span><span class="sxs-lookup"><span data-stu-id="2a7b2-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="2a7b2-551">1</span><span class="sxs-lookup"><span data-stu-id="2a7b2-551">1</span></span>          | <span data-ttu-id="2a7b2-552">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="2a7b2-552">Lease expense</span></span>            | <span data-ttu-id="2a7b2-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="2a7b2-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-554">1,000\.00</span></span>               |   | <span data-ttu-id="2a7b2-555">\-1,000.</span><span class="sxs-lookup"><span data-stu-id="2a7b2-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="2a7b2-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-556">0\.00</span></span>                                   |
| <span data-ttu-id="2a7b2-557">2</span><span class="sxs-lookup"><span data-stu-id="2a7b2-557">2</span></span>          | <span data-ttu-id="2a7b2-558">ค่าธรรมเนียมของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="2a7b2-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="2a7b2-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="2a7b2-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="2a7b2-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-561">3\.00</span></span>                                   |
| <span data-ttu-id="2a7b2-562">3</span><span class="sxs-lookup"><span data-stu-id="2a7b2-562">3</span></span>          | <span data-ttu-id="2a7b2-563">ค่าใช้จ่าย VAT</span><span class="sxs-lookup"><span data-stu-id="2a7b2-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="2a7b2-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="2a7b2-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="2a7b2-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-566">5\.00</span></span>                                   |
| <span data-ttu-id="2a7b2-567">4</span><span class="sxs-lookup"><span data-stu-id="2a7b2-567">4</span></span>          | <span data-ttu-id="2a7b2-568">บัญชีรอการโอน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-568">Clearing account</span></span>         | <span data-ttu-id="2a7b2-569">\-1,000\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="2a7b2-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="2a7b2-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-571">0\.00</span></span>                   |   | <span data-ttu-id="2a7b2-572">1,000</span><span class="sxs-lookup"><span data-stu-id="2a7b2-572">1,000</span></span>                                           |                                                | <span data-ttu-id="2a7b2-573">\-1,000.</span><span class="sxs-lookup"><span data-stu-id="2a7b2-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="2a7b2-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-574">0\.00</span></span>                                   |
| <span data-ttu-id="2a7b2-575">5</span><span class="sxs-lookup"><span data-stu-id="2a7b2-575">5</span></span>          | <span data-ttu-id="2a7b2-576">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="2a7b2-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="2a7b2-577">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="2a7b2-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-578">1,008\.00</span></span>                                         | <span data-ttu-id="2a7b2-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="2a7b2-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-580">0\.00</span></span>                                   |
| <span data-ttu-id="2a7b2-581">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="2a7b2-581">6</span></span>          | <span data-ttu-id="2a7b2-582">สิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2a7b2-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="2a7b2-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="2a7b2-584">22,794</span><span class="sxs-lookup"><span data-stu-id="2a7b2-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="2a7b2-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="2a7b2-585">22,793\.90</span></span>                              |
| <span data-ttu-id="2a7b2-586">7</span><span class="sxs-lookup"><span data-stu-id="2a7b2-586">7</span></span>          | <span data-ttu-id="2a7b2-587">ข้อผูกมัดตามสัญญาเช่าการเงิน</span><span class="sxs-lookup"><span data-stu-id="2a7b2-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="2a7b2-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="2a7b2-589">\-22,794.</span><span class="sxs-lookup"><span data-stu-id="2a7b2-589">\-22,794</span></span>                                       | <span data-ttu-id="2a7b2-590">1,000</span><span class="sxs-lookup"><span data-stu-id="2a7b2-590">1,000</span></span>                                          | <span data-ttu-id="2a7b2-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="2a7b2-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="2a7b2-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="2a7b2-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="2a7b2-593">8</span><span class="sxs-lookup"><span data-stu-id="2a7b2-593">8</span></span>          | <span data-ttu-id="2a7b2-594">ค่าใช้จ่ายดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="2a7b2-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="2a7b2-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="2a7b2-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="2a7b2-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="2a7b2-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="2a7b2-597">94\.97</span></span>                                  |
| <span data-ttu-id="2a7b2-598">9</span><span class="sxs-lookup"><span data-stu-id="2a7b2-598">9</span></span>          | <span data-ttu-id="2a7b2-599">เงินสด</span><span class="sxs-lookup"><span data-stu-id="2a7b2-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="2a7b2-600">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="2a7b2-601">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="2a7b2-602">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="2a7b2-603">10</span><span class="sxs-lookup"><span data-stu-id="2a7b2-603">10</span></span>         | <span data-ttu-id="2a7b2-604">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="2a7b2-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="2a7b2-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="2a7b2-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="2a7b2-606">949\.75</span></span>                                        | <span data-ttu-id="2a7b2-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="2a7b2-607">949\.75</span></span>                                 |
| <span data-ttu-id="2a7b2-608">11</span><span class="sxs-lookup"><span data-stu-id="2a7b2-608">11</span></span>         | <span data-ttu-id="2a7b2-609">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="2a7b2-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="2a7b2-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="2a7b2-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="2a7b2-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="2a7b2-611">\-949\.75</span></span>                                      | <span data-ttu-id="2a7b2-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="2a7b2-612">\-949\.75</span></span>                               |


