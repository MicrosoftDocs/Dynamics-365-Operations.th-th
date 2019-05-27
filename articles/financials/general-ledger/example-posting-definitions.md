---
title: ข้อกำหนดการลงรายการบัญชี
description: บทความนี้แสดงตัวอย่างที่แสดงให้เห็นถึงวิธีใช้ข้อกำหนดการลงรายการบัญชีสำหรับภาระผูกพันของใบสั่งซื้อและการจัดสรรงบประมาณ
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5fb08a86639e9a9a79dca5fc1200e73e5870432
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564704"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="40b95-103">ตัวอย่างข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40b95-104">บทความนี้แสดงตัวอย่างที่แสดงให้เห็นถึงวิธีใช้ข้อกำหนดการลงรายการบัญชีสำหรับภาระผูกพันของใบสั่งซื้อและการจัดสรรงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="40b95-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="40b95-105">ก่อนที่คุณอ่านหัวข้อนี้ คุณควรจะคุ้นเคยกับข้อกำหนดการลงรายการบัญชีและข้อกำหนดการลงรายการบัญชีธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="40b95-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="40b95-106">สำหรับข้อมูล ดู [ข้อกำหนดการลงรายการบัญชี](posting-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="40b95-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="40b95-107">ตัวอย่างต่อไปนี้สามารถตั้งค่าหน้า **ข้อกำหนดการลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="40b95-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="40b95-108">แต่ละตัวอย่างประกอบด้วยส่วนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="40b95-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="40b95-109">ข้อกำหนดการลงรายการบัญชี – เกณฑ์การจับคู่</span><span class="sxs-lookup"><span data-stu-id="40b95-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="40b95-110">ข้อกำหนดการลงรายการบัญชี – รายการสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="40b95-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="40b95-111">ธุรกรรมที่มีบัญชี ค่ามิติ และยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="40b95-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="40b95-112">รายการบัญชีแยกประเภทสร้างขึ้นจากข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="40b95-113">เมื่อการจับคู่เกิดขึ้นระหว่างบัญชีและค่ามิติในบานหน้าต่าง **เกณฑ์การจับคู่** สำหรับข้อกำหนดการลงรายการบัญชีและบัญชี และค่ามิติบนธุรกรรม รายการบัญชีแยกประเภทถูกสร้างขึ้นตามบานหน้าต่าง **รายการที่สร้าง** สำหรับข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="40b95-114">เมื่อต้องการเชื่อมโยงข้อกำหนดการลงรายการบัญชีด้วยชนิดธุรกรรมเฉพาะ ใช้หน้า **ข้อกำหนดการลงรายการบัญชีธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="40b95-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="40b95-115">หลังจากที่คุณเชื่อมโยงข้อกำหนดการลงรายการบัญชีด้วยชนิดธุรกรรมและเลือก **ใช้ข้อกำหนดการลงรายการบัญชี** ในหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป** ธุรกรรมทั้งหมดของชนิดธุรกรรมที่เลือกต้องใช้ข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="40b95-116">ตัวอย่าง: ภาระผูกพันของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="40b95-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="40b95-117">เมื่อคุณเปิดใช้งานการประมวลผลภาระผูกพันโดยการเลือก **เปิดใช้งานกระบวนการภาระผูกพัน** บนหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป** ข้อกำหนดการลงรายการบัญชีต้องถูกใช้เพื่อเรกคอร์ดภาระผูกพันไปที่บัญชีแยกประเภททั่วไปสำหรับบัญชีใดๆ ที่ควรจอง</span><span class="sxs-lookup"><span data-stu-id="40b95-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="40b95-118">ในกรณีส่วนใหญ่ บัญชีค่าใช้จ่ายทั้งหมดถูกจองในงบดุล</span><span class="sxs-lookup"><span data-stu-id="40b95-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="40b95-119">ข้อกำหนดของการลงรายการบัญชีสำหรับภาระผูกพันถูกตั้งค่าสำหรับโมดูล **การซื้อ** ในหน้า **ข้อกำหนดการลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="40b95-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="40b95-120">แล้ว ในพื้นที่ **การซื้อ** ของหน้า **ข้อกำหนดการลงรายการบัญชีธุรกรรม** คุณสามารถเลือกชนิดธุรกรรม **ใบสั่งซื้อ** เพื่อเชื่อมโยงข้อกำหนดการลงรายการบัญชีด้วยใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="40b95-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="40b95-121">ธุรกรรมใบสำคัญทั้งหมดสำหรับภาระผูกพันของใบสั่งซื้อต้องดุล (นั่นคือ เดบิตต้องเท่ากับเครดิต) ในแต่ละมิติเฉพาะในใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="40b95-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="40b95-122">ข้อกำหนดการลงรายการบัญชี – เกณฑ์การจับคู่</span><span class="sxs-lookup"><span data-stu-id="40b95-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="40b95-123">โครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-123">Account structure</span></span>       | <span data-ttu-id="40b95-124">จับคู่หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-124">Match account number</span></span> | <span data-ttu-id="40b95-125">ระดับความสำคัญ </span><span class="sxs-lookup"><span data-stu-id="40b95-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="40b95-126">โครงสร้างทางบัญชี - P&L</span><span class="sxs-lookup"><span data-stu-id="40b95-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="40b95-127">1</span><span class="sxs-lookup"><span data-stu-id="40b95-127">1</span></span>        |

<span data-ttu-id="40b95-128"><em>ค่าว่างในฟิลด์ \**จับคู่หมายเลขบัญชี</em>* หมายความว่า บัญชีการจับคู่ทั้งหมดในโครงสร้างทางบัญชีที่กำหนดไว้ เป็นส่วนหนึ่งของกฎการจับคู่</span><span class="sxs-lookup"><span data-stu-id="40b95-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="40b95-129">ข้อกำหนดการลงรายการบัญชี – รายการสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="40b95-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="40b95-130">โครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-130">Account structure</span></span> | <span data-ttu-id="40b95-131">หมายเลขบัญชีที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="40b95-131">Generated account number</span></span>                    | <span data-ttu-id="40b95-132">เดบิต/เครดิตที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="40b95-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="40b95-133">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="40b95-133">Balance</span></span>           | <span data-ttu-id="40b95-134">300143 - -(บัญชีภาระผูกพัน)</span><span class="sxs-lookup"><span data-stu-id="40b95-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="40b95-135">เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="40b95-135">Same</span></span>                   |
| <span data-ttu-id="40b95-136">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="40b95-136">Balance</span></span>           | <span data-ttu-id="40b95-137">300144 - -(จองสำหรับบัญชีภาระผูกพัน)</span><span class="sxs-lookup"><span data-stu-id="40b95-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="40b95-138">การรักษาสมดุล</span><span class="sxs-lookup"><span data-stu-id="40b95-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="40b95-139">ธุรกรรมที่มีบัญชี ค่ามิติ และยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="40b95-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="40b95-140">บัญชีและค่ามิติอย่างใดอย่างหนึ่งมาจากการกระจายการลงบัญชีที่คุณป้อนสำหรับรายการใบสั่งซื้อ หรือจากบัญชีและมิติที่สร้างขึ้นโดยอัตโนมัติตามการตั้งค่าเริ่มต้นสำหรับผู้จัดจำหน่าย สินค้า ประเภท และเท็มเพลตมิติ</span><span class="sxs-lookup"><span data-stu-id="40b95-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="40b95-141">บัญชี + มิติ</span><span class="sxs-lookup"><span data-stu-id="40b95-141">Account + dimensions</span></span>           | <span data-ttu-id="40b95-142">เดบิต</span><span class="sxs-lookup"><span data-stu-id="40b95-142">Debit</span></span>  | <span data-ttu-id="40b95-143">เครดิต</span><span class="sxs-lookup"><span data-stu-id="40b95-143">Credit</span></span> | <span data-ttu-id="40b95-144">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="40b95-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="40b95-145">606400-OU\_1-OU\_3566-การฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="40b95-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="40b95-146">250.00</span><span class="sxs-lookup"><span data-stu-id="40b95-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="40b95-147">รายการบัญชีแยกประเภทสร้างขึ้นจากข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="40b95-148">รายการบัญชีแยกประเภทที่สร้างขึ้นถูกสร้างเพื่อเรกคอร์ดภาระผูกพัน</span><span class="sxs-lookup"><span data-stu-id="40b95-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="40b95-149">บัญชี + มิติ</span><span class="sxs-lookup"><span data-stu-id="40b95-149">Account + dimensions</span></span>           | <span data-ttu-id="40b95-150">เดบิต</span><span class="sxs-lookup"><span data-stu-id="40b95-150">Debit</span></span>  | <span data-ttu-id="40b95-151">เครดิต</span><span class="sxs-lookup"><span data-stu-id="40b95-151">Credit</span></span> | <span data-ttu-id="40b95-152">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="40b95-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="40b95-153">300143-OU\_1-OU\_3566-การฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="40b95-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="40b95-154">250.00</span><span class="sxs-lookup"><span data-stu-id="40b95-154">250.00</span></span> |        |         |
| <span data-ttu-id="40b95-155">300144-OU\_1-OU\_3566-การฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="40b95-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="40b95-156">250.00</span><span class="sxs-lookup"><span data-stu-id="40b95-156">250.00</span></span> |         |

<span data-ttu-id="40b95-157">ในตัวอย่างนี้ บัญชีใด ๆซึ่งเป็นส่วนหนึ่งของโครงสร้างทางบัญชี - P&L ตรงกับเกณฑ์ข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="40b95-158">ดังนั้น เมื่อ 606500-OU\_1-OU\_3566-การฝึกอบรมถูกประเมิน รายการที่สร้างขึ้นถูกสร้างสำหรับบัญชีที่กำหนดไว้ในบานหน้าต่าง **รายการที่สร้าง** สำหรับข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="40b95-159">ตัวอย่าง: การจัดสรรงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="40b95-159">Example: Budget appropriations</span></span>
<span data-ttu-id="40b95-160">เมื่อคุณเปิดใช้งานการจัดสรรงบประมาณโดยการเลือก **เปิดใช้งานการจัดสรรงบประมาณ** ในหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป** ข้อกำหนดการลงรายการบัญชีต้องถูกใช้เพื่อเรกคอร์ดรายการทะเบียนงบประมาณไปที่บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="40b95-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="40b95-161">เมื่อการตั้งค่าคอนฟิกการควบคุมงบประมาณถูกใช้งานอยู่และถูกเปิด ข้อกำหนดการลงรายการบัญชีและข้อกำหนดการลงรายการบัญชีธุรกรรมสามารถถูกใช้เพื่อสนับสนุนการบันทึกรายการสำหรับการจัดสรร ปรับปรุง โอนย้าย โครงการ สินทรัพย์ถาวร และการจัดหาวัสดุและการคาดการณ์ความต้องการไปที่บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="40b95-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="40b95-162">เพื่อตั้งค่าข้อกำหนดการลงรายการบัญชีสำหรับรายการทะเบียนงบประมาณที่มีชนิดงบประมาณของ **งบประมาณเดิม** และมีการจัดสรรถูกเปิดใช้ เลือกโมดูล **งบประมาณ** ในหน้า **ข้อกำหนดการลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="40b95-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="40b95-163">แล้ว ในพื้นที่ **งบประมาณ** ของหน้า **ข้อกำหนดการลงรายการบัญชีธุรกรรม** คุณสามารถใช้รหัสงบประมาณเพื่อเชื่อมโยงข้อกำหนดการลงรายการบัญชีกับรายการทะเบียนงบประมาณที่มีชนิดงบประมาณของ **งบประมาณเดิม**</span><span class="sxs-lookup"><span data-stu-id="40b95-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="40b95-164">เมื่อการจัดสรรงบประมาณและข้อกำหนดการลงรายการบัญชีถูกเปิดใช้ รายการทะเบียนงบประมาณถูกบันทึกสำหรับการควบคุมงบประมาณและในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="40b95-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="40b95-165">ข้อกำหนดการลงรายการบัญชี – เกณฑ์การจับคู่</span><span class="sxs-lookup"><span data-stu-id="40b95-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="40b95-166">โครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-166">Account structure</span></span>       | <span data-ttu-id="40b95-167">จับคู่หมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-167">Match account number</span></span> | <span data-ttu-id="40b95-168">ระดับความสำคัญ </span><span class="sxs-lookup"><span data-stu-id="40b95-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="40b95-169">โครงสร้างทางบัญชี - P&L</span><span class="sxs-lookup"><span data-stu-id="40b95-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="40b95-170">1</span><span class="sxs-lookup"><span data-stu-id="40b95-170">1</span></span>        |

<span data-ttu-id="40b95-171"><em>ค่าว่างในฟิลด์ \**จับคู่หมายเลขบัญชี</em>* หมายความว่า บัญชีการจับคู่ทั้งหมดในโครงสร้างทางบัญชีที่กำหนดไว้ เป็นส่วนหนึ่งของกฎการจับคู่</span><span class="sxs-lookup"><span data-stu-id="40b95-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="40b95-172">ข้อกำหนดการลงรายการบัญชี – รายการสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="40b95-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="40b95-173">โครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-173">Account structure</span></span> | <span data-ttu-id="40b95-174">หมายเลขบัญชีที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="40b95-174">Generated account number</span></span>              | <span data-ttu-id="40b95-175">เดบิต/เครดิตที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="40b95-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="40b95-176">โครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-176">Account structure</span></span> | <span data-ttu-id="40b95-177">300145 - -(บัญชีรายได้ที่ประเมิน)</span><span class="sxs-lookup"><span data-stu-id="40b95-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="40b95-178">เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="40b95-178">Same</span></span>                   |
| <span data-ttu-id="40b95-179">โครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-179">Account structure</span></span> | <span data-ttu-id="40b95-180">300146 - -(บัญชีปันส่วน)</span><span class="sxs-lookup"><span data-stu-id="40b95-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="40b95-181">การรักษาสมดุล</span><span class="sxs-lookup"><span data-stu-id="40b95-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="40b95-182">ธุรกรรมที่มีบัญชี ค่ามิติ และยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="40b95-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="40b95-183">คุณป้อนบัญชี ค่ามิติ และยอดเงินสำหรับรายการบัญชีงบประมาณในหน้า **รายการทะเบียนงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="40b95-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="40b95-184">บัญชี + มิติ</span><span class="sxs-lookup"><span data-stu-id="40b95-184">Account + dimensions</span></span>           | <span data-ttu-id="40b95-185">เดบิต</span><span class="sxs-lookup"><span data-stu-id="40b95-185">Debit</span></span> | <span data-ttu-id="40b95-186">เครดิต</span><span class="sxs-lookup"><span data-stu-id="40b95-186">Credit</span></span> | <span data-ttu-id="40b95-187">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="40b95-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="40b95-188">606400-OU\_1-OU\_3566-การฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="40b95-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="40b95-189">250.00</span><span class="sxs-lookup"><span data-stu-id="40b95-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="40b95-190">รายการบัญชีแยกประเภทสร้างขึ้นจากข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="40b95-191">รายการบัญชีแยกประเภทที่สร้างขึ้นถูกสร้างเพื่อเรกคอร์ดงบประมาณเดิมในแต่ละมิติ</span><span class="sxs-lookup"><span data-stu-id="40b95-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="40b95-192">บัญชี + มิติ</span><span class="sxs-lookup"><span data-stu-id="40b95-192">Account + dimensions</span></span>           | <span data-ttu-id="40b95-193">เดบิต</span><span class="sxs-lookup"><span data-stu-id="40b95-193">Debit</span></span>  | <span data-ttu-id="40b95-194">เครดิต</span><span class="sxs-lookup"><span data-stu-id="40b95-194">Credit</span></span> | <span data-ttu-id="40b95-195">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="40b95-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="40b95-196">300145-OU\_1-OU\_3566-การฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="40b95-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="40b95-197">250.00</span><span class="sxs-lookup"><span data-stu-id="40b95-197">250.00</span></span> |         |
| <span data-ttu-id="40b95-198">300146-OU\_1-OU\_3566-การฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="40b95-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="40b95-199">250.00</span><span class="sxs-lookup"><span data-stu-id="40b95-199">250.00</span></span> |        |         |

<span data-ttu-id="40b95-200">ในตัวอย่างนี้ บัญชีใด ๆซึ่งเป็นส่วนหนึ่งของโครงสร้างทางบัญชี - P&L ตรงกับเกณฑ์ข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40b95-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="40b95-201">ดังนั้น เมื่อ 606400-OU\_1-OU\_3566-การฝึกอบรมถูกประเมิน รายการบัญชีแยกประเภทที่สร้างขึ้นถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="40b95-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>





