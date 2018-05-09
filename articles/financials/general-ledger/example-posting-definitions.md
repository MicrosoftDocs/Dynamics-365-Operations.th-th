---
title: "ข้อกำหนดการลงรายการบัญชี"
description: "บทความนี้แสดงตัวอย่างที่แสดงให้เห็นถึงวิธีใช้ข้อกำหนดการลงรายการบัญชีสำหรับภาระผูกพันของใบสั่งซื้อและการจัดสรรงบประมาณ"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b7d4b94e9c0ea27b8a78ea4ed6bbde6bec19ef6e
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="posting-definition-examples"></a><span data-ttu-id="c4d99-103">ตัวอย่างข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4d99-104">บทความนี้แสดงตัวอย่างที่แสดงให้เห็นถึงวิธีใช้ข้อกำหนดการลงรายการบัญชีสำหรับภาระผูกพันของใบสั่งซื้อและการจัดสรรงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="c4d99-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="c4d99-105">ก่อนที่คุณอ่านหัวข้อนี้ คุณควรจะคุ้นเคยกับข้อกำหนดการลงรายการบัญชีและข้อกำหนดการลงรายการบัญชีธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="c4d99-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="c4d99-106">สำหรับข้อมูล ดู [ข้อกำหนดการลงรายการบัญชี](posting-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="c4d99-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="c4d99-107">ตัวอย่างต่อไปนี้สามารถตั้งค่าหน้า **ข้อกำหนดการลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="c4d99-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="c4d99-108">แต่ละตัวอย่างประกอบด้วยส่วนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="c4d99-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="c4d99-109">ข้อกำหนดการลงรายการบัญชี – เกณฑ์การจับคู่</span><span class="sxs-lookup"><span data-stu-id="c4d99-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="c4d99-110">ข้อกำหนดการลงรายการบัญชี – รายการสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c4d99-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="c4d99-111">ธุรกรรมที่มีบัญชี ค่ามิติ และยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="c4d99-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="c4d99-112">รายการบัญชีแยกประเภทสร้างขึ้นจากข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="c4d99-113">เมื่อการจับคู่เกิดขึ้นระหว่างบัญชีและค่ามิติในบานหน้าต่าง **เกณฑ์การจับคู่** สำหรับข้อกำหนดการลงรายการบัญชีและบัญชี และค่ามิติบนธุรกรรม รายการบัญชีแยกประเภทถูกสร้างขึ้นตามบานหน้าต่าง **รายการที่สร้าง** สำหรับข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="c4d99-114">เมื่อต้องการเชื่อมโยงข้อกำหนดการลงรายการบัญชีด้วยชนิดธุรกรรมเฉพาะ ใช้หน้า **ข้อกำหนดการลงรายการบัญชีธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="c4d99-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="c4d99-115">หลังจากที่คุณเชื่อมโยงข้อกำหนดการลงรายการบัญชีด้วยชนิดธุรกรรมและเลือก **ใช้ข้อกำหนดการลงรายการบัญชี** ในหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป** ธุรกรรมทั้งหมดของชนิดธุรกรรมที่เลือกต้องใช้ข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="c4d99-116">ตัวอย่าง: ภาระผูกพันของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="c4d99-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="c4d99-117">เมื่อคุณเปิดใช้งานการประมวลผลภาระผูกพันโดยการเลือก **เปิดใช้งานกระบวนการภาระผูกพัน** บนหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป** ข้อกำหนดการลงรายการบัญชีต้องถูกใช้เพื่อเรกคอร์ดภาระผูกพันไปที่บัญชีแยกประเภททั่วไปสำหรับบัญชีใดๆ ที่ควรจอง</span><span class="sxs-lookup"><span data-stu-id="c4d99-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="c4d99-118">ในกรณีส่วนใหญ่ บัญชีค่าใช้จ่ายทั้งหมดถูกจองในงบดุล</span><span class="sxs-lookup"><span data-stu-id="c4d99-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="c4d99-119">ข้อกำหนดของการลงรายการบัญชีสำหรับภาระผูกพันถูกตั้งค่าสำหรับโมดูล **การซื้อ** ในหน้า **ข้อกำหนดการลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="c4d99-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="c4d99-120">แล้ว ในพื้นที่ **การซื้อ** ของหน้า **ข้อกำหนดการลงรายการบัญชีธุรกรรม** คุณสามารถเลือกชนิดธุรกรรม **ใบสั่งซื้อ** เพื่อเชื่อมโยงข้อกำหนดการลงรายการบัญชีด้วยใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="c4d99-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="c4d99-121">ธุรกรรมใบสำคัญทั้งหมดสำหรับภาระผูกพันของใบสั่งซื้อต้องดุล (นั่นคือ เดบิตต้องเท่ากับเครดิต) ในแต่ละมิติเฉพาะในใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="c4d99-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="c4d99-122">ข้อกำหนดการลงรายการบัญชี – เกณฑ์การจับคู่</span><span class="sxs-lookup"><span data-stu-id="c4d99-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="c4d99-123">โครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-123">Account structure</span></span>       | <span data-ttu-id="c4d99-124">จับคู่หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-124">Match account number</span></span> | <span data-ttu-id="c4d99-125">ระดับความสำคัญ </span><span class="sxs-lookup"><span data-stu-id="c4d99-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="c4d99-126">โครงสร้างทางบัญชี - P&L</span><span class="sxs-lookup"><span data-stu-id="c4d99-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="c4d99-127">1</span><span class="sxs-lookup"><span data-stu-id="c4d99-127">1</span></span>        |

<span data-ttu-id="c4d99-128"><em>ค่าว่างในฟิลด์ \**จับคู่หมายเลขบัญชี</em>* หมายความว่า บัญชีการจับคู่ทั้งหมดในโครงสร้างทางบัญชีที่กำหนดไว้ เป็นส่วนหนึ่งของกฎการจับคู่</span><span class="sxs-lookup"><span data-stu-id="c4d99-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="c4d99-129">ข้อกำหนดการลงรายการบัญชี – รายการสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c4d99-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="c4d99-130">โครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-130">Account structure</span></span> | <span data-ttu-id="c4d99-131">หมายเลขบัญชีที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4d99-131">Generated account number</span></span>                    | <span data-ttu-id="c4d99-132">เดบิต/เครดิตที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4d99-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="c4d99-133">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="c4d99-133">Balance</span></span>           | <span data-ttu-id="c4d99-134">300143 - -(บัญชีภาระผูกพัน)</span><span class="sxs-lookup"><span data-stu-id="c4d99-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="c4d99-135">เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="c4d99-135">Same</span></span>                   |
| <span data-ttu-id="c4d99-136">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="c4d99-136">Balance</span></span>           | <span data-ttu-id="c4d99-137">300144 - -(จองสำหรับบัญชีภาระผูกพัน)</span><span class="sxs-lookup"><span data-stu-id="c4d99-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="c4d99-138">การรักษาสมดุล</span><span class="sxs-lookup"><span data-stu-id="c4d99-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="c4d99-139">ธุรกรรมที่มีบัญชี ค่ามิติ และยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="c4d99-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="c4d99-140">บัญชีและค่ามิติอย่างใดอย่างหนึ่งมาจากการกระจายการลงบัญชีที่คุณป้อนสำหรับรายการใบสั่งซื้อ หรือจากบัญชีและมิติที่สร้างขึ้นโดยอัตโนมัติตามการตั้งค่าเริ่มต้นสำหรับผู้จัดจำหน่าย สินค้า ประเภท และเท็มเพลตมิติ</span><span class="sxs-lookup"><span data-stu-id="c4d99-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="c4d99-141">บัญชี + มิติ</span><span class="sxs-lookup"><span data-stu-id="c4d99-141">Account + dimensions</span></span>           | <span data-ttu-id="c4d99-142">เดบิต</span><span class="sxs-lookup"><span data-stu-id="c4d99-142">Debit</span></span>  | <span data-ttu-id="c4d99-143">เครดิต</span><span class="sxs-lookup"><span data-stu-id="c4d99-143">Credit</span></span> | <span data-ttu-id="c4d99-144">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="c4d99-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="c4d99-145">606400-OU\_1-OU\_3566-การฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="c4d99-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="c4d99-146">250.00</span><span class="sxs-lookup"><span data-stu-id="c4d99-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="c4d99-147">รายการบัญชีแยกประเภทสร้างขึ้นจากข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="c4d99-148">รายการบัญชีแยกประเภทที่สร้างขึ้นถูกสร้างเพื่อเรกคอร์ดภาระผูกพัน</span><span class="sxs-lookup"><span data-stu-id="c4d99-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="c4d99-149">บัญชี + มิติ</span><span class="sxs-lookup"><span data-stu-id="c4d99-149">Account + dimensions</span></span>           | <span data-ttu-id="c4d99-150">เดบิต</span><span class="sxs-lookup"><span data-stu-id="c4d99-150">Debit</span></span>  | <span data-ttu-id="c4d99-151">เครดิต</span><span class="sxs-lookup"><span data-stu-id="c4d99-151">Credit</span></span> | <span data-ttu-id="c4d99-152">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="c4d99-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="c4d99-153">300143-OU\_1-OU\_3566-การฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="c4d99-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="c4d99-154">250.00</span><span class="sxs-lookup"><span data-stu-id="c4d99-154">250.00</span></span> |        |         |
| <span data-ttu-id="c4d99-155">300144-OU\_1-OU\_3566-การฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="c4d99-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="c4d99-156">250.00</span><span class="sxs-lookup"><span data-stu-id="c4d99-156">250.00</span></span> |         |

<span data-ttu-id="c4d99-157">ในตัวอย่างนี้ บัญชีใด ๆซึ่งเป็นส่วนหนึ่งของโครงสร้างทางบัญชี - P&L ตรงกับเกณฑ์ข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="c4d99-158">ดังนั้น เมื่อ 606500-OU\_1-OU\_3566-การฝึกอบรมถูกประเมิน รายการที่สร้างขึ้นถูกสร้างสำหรับบัญชีที่กำหนดไว้ในบานหน้าต่าง **รายการที่สร้าง** สำหรับข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="c4d99-159">ตัวอย่าง: การจัดสรรงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="c4d99-159">Example: Budget appropriations</span></span>
<span data-ttu-id="c4d99-160">เมื่อคุณเปิดใช้งานการจัดสรรงบประมาณโดยการเลือก **เปิดใช้งานการจัดสรรงบประมาณ** ในหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป** ข้อกำหนดการลงรายการบัญชีต้องถูกใช้เพื่อเรกคอร์ดรายการทะเบียนงบประมาณไปที่บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="c4d99-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="c4d99-161">เมื่อการตั้งค่าคอนฟิกการควบคุมงบประมาณถูกใช้งานอยู่และถูกเปิด ข้อกำหนดการลงรายการบัญชีและข้อกำหนดการลงรายการบัญชีธุรกรรมสามารถถูกใช้เพื่อสนับสนุนการบันทึกรายการสำหรับการจัดสรร ปรับปรุง โอนย้าย โครงการ สินทรัพย์ถาวร และการจัดหาวัสดุและการคาดการณ์ความต้องการไปที่บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="c4d99-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="c4d99-162">เพื่อตั้งค่าข้อกำหนดการลงรายการบัญชีสำหรับรายการทะเบียนงบประมาณที่มีชนิดงบประมาณของ **งบประมาณเดิม** และมีการจัดสรรถูกเปิดใช้ เลือกโมดูล **งบประมาณ** ในหน้า **ข้อกำหนดการลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="c4d99-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="c4d99-163">แล้ว ในพื้นที่ **งบประมาณ** ของหน้า **ข้อกำหนดการลงรายการบัญชีธุรกรรม** คุณสามารถใช้รหัสงบประมาณเพื่อเชื่อมโยงข้อกำหนดการลงรายการบัญชีกับรายการทะเบียนงบประมาณที่มีชนิดงบประมาณของ **งบประมาณเดิม**</span><span class="sxs-lookup"><span data-stu-id="c4d99-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="c4d99-164">เมื่อการจัดสรรงบประมาณและข้อกำหนดการลงรายการบัญชีถูกเปิดใช้ รายการทะเบียนงบประมาณถูกบันทึกสำหรับการควบคุมงบประมาณและในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="c4d99-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="c4d99-165">ข้อกำหนดการลงรายการบัญชี – เกณฑ์การจับคู่</span><span class="sxs-lookup"><span data-stu-id="c4d99-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="c4d99-166">โครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-166">Account structure</span></span>       | <span data-ttu-id="c4d99-167">จับคู่หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-167">Match account number</span></span> | <span data-ttu-id="c4d99-168">ระดับความสำคัญ </span><span class="sxs-lookup"><span data-stu-id="c4d99-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="c4d99-169">โครงสร้างทางบัญชี - P&L</span><span class="sxs-lookup"><span data-stu-id="c4d99-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="c4d99-170">1</span><span class="sxs-lookup"><span data-stu-id="c4d99-170">1</span></span>        |

<span data-ttu-id="c4d99-171"><em>ค่าว่างในฟิลด์ \**จับคู่หมายเลขบัญชี</em>* หมายความว่า บัญชีการจับคู่ทั้งหมดในโครงสร้างทางบัญชีที่กำหนดไว้ เป็นส่วนหนึ่งของกฎการจับคู่</span><span class="sxs-lookup"><span data-stu-id="c4d99-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="c4d99-172">ข้อกำหนดการลงรายการบัญชี – รายการสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c4d99-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="c4d99-173">โครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-173">Account structure</span></span> | <span data-ttu-id="c4d99-174">หมายเลขบัญชีที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4d99-174">Generated account number</span></span>              | <span data-ttu-id="c4d99-175">เดบิต/เครดิตที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4d99-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="c4d99-176">โครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-176">Account structure</span></span> | <span data-ttu-id="c4d99-177">300145 - -(บัญชีรายได้ที่ประเมิน)</span><span class="sxs-lookup"><span data-stu-id="c4d99-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="c4d99-178">เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="c4d99-178">Same</span></span>                   |
| <span data-ttu-id="c4d99-179">โครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-179">Account structure</span></span> | <span data-ttu-id="c4d99-180">300146 - -(บัญชีปันส่วน)</span><span class="sxs-lookup"><span data-stu-id="c4d99-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="c4d99-181">การรักษาสมดุล</span><span class="sxs-lookup"><span data-stu-id="c4d99-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="c4d99-182">ธุรกรรมที่มีบัญชี ค่ามิติ และยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="c4d99-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="c4d99-183">คุณป้อนบัญชี ค่ามิติ และยอดเงินสำหรับรายการบัญชีงบประมาณในหน้า **รายการทะเบียนงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="c4d99-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="c4d99-184">บัญชี + มิติ</span><span class="sxs-lookup"><span data-stu-id="c4d99-184">Account + dimensions</span></span>           | <span data-ttu-id="c4d99-185">เดบิต</span><span class="sxs-lookup"><span data-stu-id="c4d99-185">Debit</span></span> | <span data-ttu-id="c4d99-186">เครดิต</span><span class="sxs-lookup"><span data-stu-id="c4d99-186">Credit</span></span> | <span data-ttu-id="c4d99-187">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="c4d99-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="c4d99-188">606400-OU\_1-OU\_3566-การฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="c4d99-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="c4d99-189">250.00</span><span class="sxs-lookup"><span data-stu-id="c4d99-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="c4d99-190">รายการบัญชีแยกประเภทสร้างขึ้นจากข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="c4d99-191">รายการบัญชีแยกประเภทที่สร้างขึ้นถูกสร้างเพื่อเรกคอร์ดงบประมาณเดิมในแต่ละมิติ</span><span class="sxs-lookup"><span data-stu-id="c4d99-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="c4d99-192">บัญชี + มิติ</span><span class="sxs-lookup"><span data-stu-id="c4d99-192">Account + dimensions</span></span>           | <span data-ttu-id="c4d99-193">เดบิต</span><span class="sxs-lookup"><span data-stu-id="c4d99-193">Debit</span></span>  | <span data-ttu-id="c4d99-194">เครดิต</span><span class="sxs-lookup"><span data-stu-id="c4d99-194">Credit</span></span> | <span data-ttu-id="c4d99-195">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="c4d99-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="c4d99-196">300145-OU\_1-OU\_3566-การฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="c4d99-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="c4d99-197">250.00</span><span class="sxs-lookup"><span data-stu-id="c4d99-197">250.00</span></span> |         |
| <span data-ttu-id="c4d99-198">300146-OU\_1-OU\_3566-การฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="c4d99-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="c4d99-199">250.00</span><span class="sxs-lookup"><span data-stu-id="c4d99-199">250.00</span></span> |        |         |

<span data-ttu-id="c4d99-200">ในตัวอย่างนี้ บัญชีใด ๆซึ่งเป็นส่วนหนึ่งของโครงสร้างทางบัญชี - P&L ตรงกับเกณฑ์ข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4d99-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="c4d99-201">ดังนั้น เมื่อ 606400-OU\_1-OU\_3566-การฝึกอบรมถูกประเมิน รายการบัญชีแยกประเภทที่สร้างขึ้นถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="c4d99-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>






