---
title: "ลำดับหมายเลข"
description: "ลำดับหมายเลขที่ใช้ในการสร้างตัวระบุเฉพาะที่สามารถอ่านได้สำหรับเร็กคอร์ดข้อมูลหลักและเรกคอร์ดธุรกรรมที่จำเป็นต้องมีตัวระบุ"
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: 8e3899e1ad5f4be754687c0e2d59348e7a773fd8
ms.contentlocale: th-th
ms.lasthandoff: 01/12/2018

---

# <a name="number-sequences"></a><span data-ttu-id="ae5c2-103">ลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ae5c2-103">Number sequences</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ae5c2-104">ลำดับหมายเลขที่ใช้ในการสร้างตัวระบุเฉพาะที่สามารถอ่านได้สำหรับเร็กคอร์ดข้อมูลหลักและเรกคอร์ดธุรกรรมที่จำเป็นต้องมีตัวระบุ</span><span class="sxs-lookup"><span data-stu-id="ae5c2-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="ae5c2-105">เรกคอร์ดข้อมูลหลักหรือเรกคอร์ดธุรกรรมที่จำเป็นต้องมีตัวระบุจะถูกอ้างเป็น *การอ้างอิง*</span><span class="sxs-lookup"><span data-stu-id="ae5c2-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="ae5c2-106">ก่อนที่คุณจะสามารถสร้างเรกคอร์ดใหม่สำหรับการอ้างอิงได้ คุณต้องตั้งค่าลำดับหมายเลขและเชื่อมโยงกับการอ้างอิงนั้น</span><span class="sxs-lookup"><span data-stu-id="ae5c2-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="ae5c2-107">เราขอแนะนำให้คุณใช้หน้าต่างๆใน **การจัดการองค์กร** เพื่อตั้งค่าลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ae5c2-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="ae5c2-108">ถ้าจำเป็นต้องมีการตั้งค่าเฉพาะของโมดูล คุณสามารถใช้หน้าพารามิเตอร์ในโมดูลเพื่อระบุลำดับหมายเลขสำหรับการอ้างอิงในโมดูลนั้น</span><span class="sxs-lookup"><span data-stu-id="ae5c2-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="ae5c2-109">ตัวอย่างเช่น ใน **บัญชีลูกหนี้** และ **บัญชีเจ้าหนี้**คุณสามารถตั้งค่ากลุ่มลำดับหมายเลขเพื่อปันส่วนลำดับหมายเลขเฉพาะให้กับลูกค้าหรือผู้จัดจำหน่ายที่เฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="ae5c2-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="ae5c2-110">เมื่อคุณตั้งค่าลำดับหมายเลข คุณต้องระบุ ขอบเขต ซึ่งกำหนดองค์กรที่ใช้ลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ae5c2-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="ae5c2-111">ขอบเขตสามารถเป็น **ใช้ร่วมกัน**, **บริษัท**, **นิติบุคคล**หรือ **หน่วยปฏิบัติ**</span><span class="sxs-lookup"><span data-stu-id="ae5c2-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="ae5c2-112">**นิติบุคคล** และ **บริษัท** ขอบเขตสามารถรวมกับ **รอบระยะเวลาปฏิทินทางการเงิน** เพื่อสร้างลำดับหมายเลขที่เฉพาะเจาะจงมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="ae5c2-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="ae5c2-113">รูปแบบลำดับหมายเลขประกอบด้วยเซ็กเมนต์ต่างๆ</span><span class="sxs-lookup"><span data-stu-id="ae5c2-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="ae5c2-114">ลำดับหมายเลขที่มีขอบเขตนอกเหนือจาก **ใช้ร่วมกัน** สามารถประกอบด้วยเซกเมนต์ที่สอดคล้องกับขอบเขตได้</span><span class="sxs-lookup"><span data-stu-id="ae5c2-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="ae5c2-115">ตัวอย่างเช่น ลำดับหมายเลขกับขอบเขตของ **นิติบุคคล** สามารถประกอบด้วยเซ็กเมนต์นิติบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="ae5c2-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="ae5c2-116">โดยการรวมเซ็กเมนต์ขอบเขตในรูปแบบลำดับหมายเลข คุณสามารถระบุขอบเขตของเรกคอร์ดเฉพาะโดยการดูที่หมายเลข</span><span class="sxs-lookup"><span data-stu-id="ae5c2-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="ae5c2-117">นอกจากเซ็กเมนต์ที่สอดคล้องกับขอบเขต รูปแบบลำดับหมายเลขสามารถประกอบด้วย **คงที่** และ **เซ็กเมนต์ตัวอักษรและตัวเลข**</span><span class="sxs-lookup"><span data-stu-id="ae5c2-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="ae5c2-118">เซ็กเมนต์ **คงที่** ประกอบด้วยชุดของตัวอักษร หมายเลข หรือสัญลักษณ์ที่ไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="ae5c2-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="ae5c2-119">เซ็กเมนต์ **ตัวอักษรและตัวเลข** ประกอบด้วยชุดของตัวอักษรหรือตัวเลขที่เพิ่มขึ้นทุกครั้งที่มีใช้หมายเลข</span><span class="sxs-lookup"><span data-stu-id="ae5c2-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="ae5c2-120">ใช้เครื่องหมายตัวเลข (\#) เพื่อแสดงถึงตัวเลขที่เพิ่มขึ้นและเครื่องหมาย (&) เพื่อแสดงถึงตัวอักษรที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="ae5c2-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="ae5c2-121">ตัวอย่างเช่น รูปแบบ \#\#\#\#\#\_2017 สร้างลำดับ 00001\_2017, 00002\_2017 และต่อไปเรื่อยๆ</span><span class="sxs-lookup"><span data-stu-id="ae5c2-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="ae5c2-122">ตัวอย่างของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ae5c2-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="ae5c2-123">ตัวอย่างต่อไปนี้แสดงวิธีการใช้เซ็กเมนต์เพื่อสร้างรูปแบบลำดับหมายเลข </span><span class="sxs-lookup"><span data-stu-id="ae5c2-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="ae5c2-124">โดยเฉพาะอย่างยิ่ง ตัวอย่างแสดงให้เห็นถึงผลกระทบของการใช้เซ็กเมนต์ขอบเขต</span><span class="sxs-lookup"><span data-stu-id="ae5c2-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="ae5c2-125">หมายเลขรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="ae5c2-125">Expense report numbers</span></span>

<span data-ttu-id="ae5c2-126">ในตัวอย่างต่อไปนี้ หมายเลขรายงานค่าใช้จ่ายถูกตั้งค่าสำหรับนิติบุคคลที่มีชื่อว่า **CS**</span><span class="sxs-lookup"><span data-stu-id="ae5c2-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="ae5c2-127">**พื้นที่:** การเดินทางและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="ae5c2-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="ae5c2-128">**การอ้างอิง:** หมายเลขรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="ae5c2-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="ae5c2-129">**ขอบเขต:** นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="ae5c2-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="ae5c2-130">**นิติบุคคล:** CS</span><span class="sxs-lookup"><span data-stu-id="ae5c2-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="ae5c2-131">เซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="ae5c2-131">Segments</span></span>  | <span data-ttu-id="ae5c2-132">ชนิดของเซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="ae5c2-132">Segment type</span></span> | <span data-ttu-id="ae5c2-133">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="ae5c2-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="ae5c2-134">เซ็กเมนต์ 1</span><span class="sxs-lookup"><span data-stu-id="ae5c2-134">Segment 1</span></span> | <span data-ttu-id="ae5c2-135">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="ae5c2-135">Legal entity</span></span> | <span data-ttu-id="ae5c2-136">CS</span><span class="sxs-lookup"><span data-stu-id="ae5c2-136">CS</span></span>        |
| <span data-ttu-id="ae5c2-137">เซ็กเมนต์ 2</span><span class="sxs-lookup"><span data-stu-id="ae5c2-137">Segment 2</span></span> | <span data-ttu-id="ae5c2-138">คงที่</span><span class="sxs-lookup"><span data-stu-id="ae5c2-138">Constant</span></span>     | <span data-ttu-id="ae5c2-139">-ค่าใช้จ่าย-</span><span class="sxs-lookup"><span data-stu-id="ae5c2-139">-EXPENSE-</span></span> |
| <span data-ttu-id="ae5c2-140">เซ็กเมนต์ 3</span><span class="sxs-lookup"><span data-stu-id="ae5c2-140">Segment 3</span></span> | <span data-ttu-id="ae5c2-141">ตัวอักษรและตัวเลข</span><span class="sxs-lookup"><span data-stu-id="ae5c2-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="ae5c2-142">**ตัวอย่างของหมายเลขที่มีการจัดรูปแบบ**: CS-ค่าใช้จ่าย-0039</span><span class="sxs-lookup"><span data-stu-id="ae5c2-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="ae5c2-143">เนื่องจากขอบเขตเป็นรูปแบบลำดับหมายเลขจะถูกใช้ทั้งองค์กร คุณไม่สามารถตั้งค่ารูปแบบลำดับหมายเลขที่แตกต่างสำหรับส่วนต่างๆ ขององค์กร</span><span class="sxs-lookup"><span data-stu-id="ae5c2-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="ae5c2-144">ตัวอย่างเช่น สำหรับนิติบุคคลที่ชื่อ **RW**ถ้าคุณเปลี่ยนเฉพาะค่าของเซ็กเมนต์นิติบุคคล หมายเลขการจัดรูปแบบจะเป็น RW-ค่าใช้จ่าย-0039.</span><span class="sxs-lookup"><span data-stu-id="ae5c2-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="ae5c2-145">คุณยังสามารถเปลี่ยนรูปแบบลำดับเลขจำนวนเต็มสำหรับนิติบุคคลอื่นๆได้</span><span class="sxs-lookup"><span data-stu-id="ae5c2-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="ae5c2-146">ตัวอย่างเช่น คุณสามารถข้ามเซ็กเมนต์ขอบเขตนิติบุคคลเพื่อสร้างหมายเลขรูปแบบเช่น Exp-0001.</span><span class="sxs-lookup"><span data-stu-id="ae5c2-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="ae5c2-147">หมายเลขใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="ae5c2-147">Sales order numbers</span></span>

<span data-ttu-id="ae5c2-148">ในตัวอย่างต่อไปนี้ หมายเลขใบสั่งขายถูกตั้งค่าสำหรับรหัสบริษัท **CEU**</span><span class="sxs-lookup"><span data-stu-id="ae5c2-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="ae5c2-149">**พื้นที่:**ขาย</span><span class="sxs-lookup"><span data-stu-id="ae5c2-149">**Area:** Sales</span></span> 
- <span data-ttu-id="ae5c2-150">**การอ้างอิง:** ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="ae5c2-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="ae5c2-151">**ขอบเขต:**บริษัท</span><span class="sxs-lookup"><span data-stu-id="ae5c2-151">**Scope:** Company</span></span> 
- <span data-ttu-id="ae5c2-152">**บริษัท:** CEU</span><span class="sxs-lookup"><span data-stu-id="ae5c2-152">**Company:** CEU</span></span>

| <span data-ttu-id="ae5c2-153">เซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="ae5c2-153">Segments</span></span>  | <span data-ttu-id="ae5c2-154">ชนิดเช็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="ae5c2-154">Segment type</span></span> | <span data-ttu-id="ae5c2-155">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="ae5c2-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="ae5c2-156">เซ็กเมนต์ 1</span><span class="sxs-lookup"><span data-stu-id="ae5c2-156">Segment 1</span></span> | <span data-ttu-id="ae5c2-157">คงที่</span><span class="sxs-lookup"><span data-stu-id="ae5c2-157">Constant</span></span>     | <span data-ttu-id="ae5c2-158">SO-</span><span class="sxs-lookup"><span data-stu-id="ae5c2-158">SO-</span></span>      |
| <span data-ttu-id="ae5c2-159">เซ็กเมนต์ 2</span><span class="sxs-lookup"><span data-stu-id="ae5c2-159">Segment 2</span></span> | <span data-ttu-id="ae5c2-160">ตัวอักษรและตัวเลข</span><span class="sxs-lookup"><span data-stu-id="ae5c2-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="ae5c2-161">**ตัวอย่างของการจัดรูปแบบหมายเลข**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="ae5c2-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="ae5c2-162">ถึงแม้ว่าเซ็กเมนต์ขอบเขตจะไม่รวมอยู่ในรูปแบบ แต่การกำหนดหมายเลขจะเริ่มต้นใหม่สำหรับแต่ละรหัสบริษัท</span><span class="sxs-lookup"><span data-stu-id="ae5c2-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="ae5c2-163">ถ้าคุณใช้รูปแบบเดียวกันสำหรับรหัสบริษัททั้งหมด หมายเลขเดียวกันจะถูกใช้ในแต่ละบริษัท</span><span class="sxs-lookup"><span data-stu-id="ae5c2-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="ae5c2-164">ตัวอย่างเช่น หมายเลขใบสั่งขาย SO-0029 ถูกใช้ในแต่ละบริษัท</span><span class="sxs-lookup"><span data-stu-id="ae5c2-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="ae5c2-165">คุณยังสามารถเปลี่ยนรูปแบบลำดับเลขจำนวนเต็มสำหรับรหัสบริษัทอื่นได้</span><span class="sxs-lookup"><span data-stu-id="ae5c2-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="ae5c2-166">หมายเลขใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="ae5c2-166">Purchase requisition numbers</span></span>

<span data-ttu-id="ae5c2-167">ในตัวอย่างต่อไปนี้ หมายเลขใบขอซื้อเป็นแบบทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="ae5c2-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="ae5c2-168">**พื้นที่:**ซื้อ</span><span class="sxs-lookup"><span data-stu-id="ae5c2-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="ae5c2-169">**การอ้างอิง:** ใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="ae5c2-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="ae5c2-170">**ขอบเขต:** ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="ae5c2-170">**Scope:** Shared</span></span>

| <span data-ttu-id="ae5c2-171">เซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="ae5c2-171">Segments</span></span>  | <span data-ttu-id="ae5c2-172">ชนิดเช็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="ae5c2-172">Segment type</span></span> | <span data-ttu-id="ae5c2-173">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="ae5c2-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="ae5c2-174">เซ็กเมนต์ 1</span><span class="sxs-lookup"><span data-stu-id="ae5c2-174">Segment 1</span></span> | <span data-ttu-id="ae5c2-175">คงที่</span><span class="sxs-lookup"><span data-stu-id="ae5c2-175">Constant</span></span>     | <span data-ttu-id="ae5c2-176">Req</span><span class="sxs-lookup"><span data-stu-id="ae5c2-176">Req</span></span>      |
| <span data-ttu-id="ae5c2-177">เซ็กเมนต์ 2</span><span class="sxs-lookup"><span data-stu-id="ae5c2-177">Segment 2</span></span> | <span data-ttu-id="ae5c2-178">ตัวอักษรและตัวเลข</span><span class="sxs-lookup"><span data-stu-id="ae5c2-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="ae5c2-179">**ตัวอย่างของการจัดรูปแบบหมายเลข**: Req0052</span><span class="sxs-lookup"><span data-stu-id="ae5c2-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="ae5c2-180">เนื่องจากขอบเขตเป็น **ใช้ร่วมกัน**รูปแบบลำดับหมายเลขจะถูกใช้ในองค์กร</span><span class="sxs-lookup"><span data-stu-id="ae5c2-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="ae5c2-181">คุณไม่สามารถตั้งค่ารูปแบบลำดับหมายเลขที่แตกต่างสำหรับส่วนต่างๆขององค์กรได้ </span><span class="sxs-lookup"><span data-stu-id="ae5c2-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="ae5c2-182">การพิจารณาประสิทธิภาพสำหรับลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ae5c2-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="ae5c2-183">พิจารณาข้อมูลต่อไปนี้เกี่ยวกับผลกระทบของการตั้งค่าคอนฟิกของลำดับหมายเลขที่มีต่อประสิทธิภาพของระบบก่อนที่คุณจะตั้งค่าลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ae5c2-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="ae5c2-184">ลำดับหมายเลขที่ต่อเนื่องและไม่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="ae5c2-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="ae5c2-185">ลำดับหมายเลขอาจต่อเนื่องหรือไม่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="ae5c2-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="ae5c2-186">ลำดับหมายเลขที่ต่อเนื่องจะไม่ข้ามหมายเลขใดๆ แต่อาจไม่สามารถใช้หมายเลขตามลำดับได้</span><span class="sxs-lookup"><span data-stu-id="ae5c2-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="ae5c2-187">หมายเลขจากลำดับหมายเลขที่ไม่ต่อเนื่องจะถูกใช้โดยเรียงลำดับ แต่ลำดับหมายเลขอาจข้ามหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ae5c2-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="ae5c2-188">ตัวอย่างเช่น ถ้าผู้ใช้ยกเลิกธุรกรรม มีการสร้างหมายเลข แต่ไม่ได้ใช้</span><span class="sxs-lookup"><span data-stu-id="ae5c2-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="ae5c2-189">ในลำดับหมายเลขที่ต่อเนื่อง หมายเลขดังกล่าวจะถูกนำกลับมาใช้ใหม่ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="ae5c2-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="ae5c2-190">ในลำดับหมายเลขที่ไม่ต่อเนื่อง หมายเลขนั้นจะไม่ถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="ae5c2-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="ae5c2-191">โดยทั่วไปจำเป็นต้องใช้ลำดับหมายเลขที่ต่อเนื่องสำหรับเอกสารภายนอก เช่น ใบสั่งซื้อ ใบสั่งขาย และใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ae5c2-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="ae5c2-192">อย่างไรก็ตาม ลำดับหมายเลขที่ต่อเนื่องสามารถส่งผลกระทบต่อเวลาในการตอบสนองของระบบได้ เนื่องจากระบบต้องขอหมายเลขจากฐานข้อมูลทุกครั้งที่จะสร้างเอกสารหรือเรกคอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="ae5c2-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="ae5c2-193">ถ้าคุณใช้ลำดับหมายเลขที่ไม่ต่อเนื่อง คุณสามารถเปิดใช้งาน **การปันส่วนล่วงหน้า** บนแท็บด่วน **ประสิทธิภาพ** ของหน้า **ลำดับหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="ae5c2-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="ae5c2-194">เมื่อคุณระบุปริมาณของหมายเลขที่จะปันส่วนล่วงหน้า ระบบจะเลือกหมายเลขดังกล่าวและจัดเก็บในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="ae5c2-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="ae5c2-195">หมายเลขใหม่จะถูกร้องขอจากฐานข้อมูลหลังจากมีการใช้ปริมาณที่ปันส่วนล่วงหน้าแล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ae5c2-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="ae5c2-196">เว้นแต่จะมีข้อบังคับให้คุณใช้ลำดับหมายเลขที่ต่อเนื่อง เราขอแนะนำให้คุณใช้ลำดับหมายเลขที่ไม่ต่อเนื่องเพื่อประสิทธิภาพที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="ae5c2-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="ae5c2-197">การล้างข้อมูลลำดับหมายเลขอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ae5c2-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="ae5c2-198">ในกรณีที่เกิดไฟฟ้าขัดข้อง ข้อผิดพลาดของแอพลิเคชัน หรือความล้มเหลวที่ไม่คาดคิดอื่นๆ ระบบไม่สามารถนำหมายเลขกลับมาใช้ใหม่โดยอัตโนมัติสำหรับลำดับหมายเลขที่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="ae5c2-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="ae5c2-199">คุณสามารถรันกระบวนการล้างข้อมูลโดยอัตโนมัติหรือด้วยตนเองได้เพื่อกู้คืนหมายเลขที่หายไปได้</span><span class="sxs-lookup"><span data-stu-id="ae5c2-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="ae5c2-200">พิจารณาการใช้เซิร์ฟเวอร์อย่างระมัดระวังเมื่อคุณวางแผนกระบวนการล้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ae5c2-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="ae5c2-201">ขอแนะนำให้คุณทำการล้างข้อมูลเป็นชุดงานในระหว่างช่วงเวลาที่ระบบมีปริมาณงานไม่มากนัก</span><span class="sxs-lookup"><span data-stu-id="ae5c2-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>






