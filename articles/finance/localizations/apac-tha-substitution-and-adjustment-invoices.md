---
title: ใบกำกับภาษีการปรับปรุง/เงินทดแทนสำหรับประเทศไทย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับคุณลักษณะของใบกำกับภาษีการปรับปรุง/เงินทดแทน คุณลักษณะนี้ช่วยให้คุณสามารถติดตามการพิมพ์สำเนาของใบกำกับภาษี นอกจากนี้คุณยังสามารถติดตามการปรับปรุงที่กระทำกับข้อมูลลูกค้าในส่วนหัวของใบกำกับภาษีอีกด้วย
author: EvgenyPopovMBS
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
manager: vastrup
ms.search.form: CustInvoiceJournal, CustInvoiceJourAdjustment, ProjInvoiceListPage, CustParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Thailand
ms.author: epopov
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: e4f0decc74cf1cfb6b22642a01eaeee7d162e329
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5265022"
---
# <a name="substitutionadjustment-tax-invoices-for-thailand"></a><span data-ttu-id="ac93d-105">ใบกำกับภาษีการปรับปรุง/เงินทดแทนสำหรับประเทศไทย</span><span class="sxs-lookup"><span data-stu-id="ac93d-105">Substitution/adjustment tax invoices for Thailand</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac93d-106">คุณสามารถติดตามจำนวนการพิมพ์สำเนาใบกำกับภาษีสำหรับลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="ac93d-106">You can track how many times copies of tax invoices for customers are printed.</span></span> <span data-ttu-id="ac93d-107">ทุกครั้งที่ต้องพิมพ์สำเนาของใบกำกับภาษี คุณจะต้องระบุเหตุผลสำหรับใบแจ้งหนี้ที่พิมพ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="ac93d-107">Whenever a copy of a tax invoice must be printed, the reason for the reprinted invoice must be specified.</span></span> <span data-ttu-id="ac93d-108">ใบแจ้งหนี้ที่พิมพ์ใหม่จะแทนที่ใบแจ้งหนี้ต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="ac93d-108">The reprinted invoice is a substitution for the original invoice.</span></span> <span data-ttu-id="ac93d-109">มีการพิมพ์ข้อคิดเห็นพิเศษบนสำเนาของสำเนาใบกำกับภาษี</span><span class="sxs-lookup"><span data-stu-id="ac93d-109">A special comment is printed on the copy of the tax invoice copy.</span></span> <span data-ttu-id="ac93d-110">ข้อคิดเห็นนี้รวมถึงเหตุผลสำหรับการแทนที่และจำนวนสำเนาที่พิมพ์</span><span class="sxs-lookup"><span data-stu-id="ac93d-110">This comment includes the reason for the substitution and the number of copies that have been printed.</span></span>

<span data-ttu-id="ac93d-111">เมื่อคุณพิมพ์สำเนาของใบแจ้งหนี้ คุณยังสามารถเลือกตัวเลือก **การปรับปรุง** เพื่อปรับปรุงข้อมูลลูกค้าที่ถูกพิมพ์บนใบกำกับภาษีได้</span><span class="sxs-lookup"><span data-stu-id="ac93d-111">When you print a copy of an invoice, you can also select the **Adjustment** option to adjust the customer information that is printed on the tax invoice.</span></span> <span data-ttu-id="ac93d-112">ข้อมูลที่คุณสามารถปรับปรุงรวมถึงชื่อลูกค้า ที่อยู่ ข้อมูลการติดต่อ หมายเลขทะเบียนภาษี หมายเลขสาขา และชื่อสาขา</span><span class="sxs-lookup"><span data-stu-id="ac93d-112">The information that you can adjust includes the customer name, address, contact information, tax registration number, branch number, and branch name.</span></span> <span data-ttu-id="ac93d-113">ใบกำกับภาษีที่ปรับปรุงแล้วจะได้รับหมายเลขใบกำกับภาษีใหม่ และการอ้างอิงถึงใบกำกับภาษีเดิม</span><span class="sxs-lookup"><span data-stu-id="ac93d-113">The adjusted tax invoice receives a new tax invoice number and references the original tax invoice.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ac93d-114">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="ac93d-114">Prerequisites</span></span>

<span data-ttu-id="ac93d-115">ก่อนที่คุณจะสามารถพิมพ์ใบกำกับภาษีเงินทดแทนหรือใบกำกับภาษีการปรับปรุงสำหรับประเทศไทย คุณจะต้องดำเนินการตั้งค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ac93d-115">Before you can print a substitution tax invoice or an adjustment tax invoice for Thailand, you must complete the following setup.</span></span> 

- <span data-ttu-id="ac93d-116">ในหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป** บน FastTab **ภาษีขาย** เปิดใช้งานพารามิเตอร์ **จัดการ VAT ที่รับรู้และที่ยังไม่รับรู้** และ **ใช้สำนักงานสาขาย่อยที่ยื่น**</span><span class="sxs-lookup"><span data-stu-id="ac93d-116">On the **General ledger parameters** page, on the **Sales tax** FastTab, enable the **Manage realized and unrealized VAT** and **Use tax branch** parameters.</span></span>
- <span data-ttu-id="ac93d-117">ในโครงสร้างทางบัญชีสำหรับนิติบุคคล เปิดใช้งานมิติทางการเงิน **Taxbranch**</span><span class="sxs-lookup"><span data-stu-id="ac93d-117">In the account structures for the legal entity, enable the **Taxbranch** financial dimension.</span></span> <span data-ttu-id="ac93d-118">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการทำงานกับแผนภูมิของบัญชีและโครงสร้างทางบัญชี ให้ดูที่ [วางแผนผังบัญชีของคุณ](../general-ledger/plan-chart-of-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="ac93d-118">For more information about how to work with charts of accounts and account structures, see [Plan your chart of accounts](../general-ledger/plan-chart-of-accounts.md).</span></span>
- <span data-ttu-id="ac93d-119">ในหน้า **สำนักงานสาขาย่อยที่ยื่น** สร้างค่าสำหรับค่ามิติทางการเงิน **Taxbranch**</span><span class="sxs-lookup"><span data-stu-id="ac93d-119">On the **Tax branch** page, create the values for the **Taxbranch** financial dimension.</span></span>
- <span data-ttu-id="ac93d-120">ในหน้า **รหัสภาษีขาย** ตั้งค่า **ชนิดภาษี** สำหรับรหัสภาษีขายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ac93d-120">On the **Sales tax codes** page, set the **Tax type** value for applicable sales tax codes.</span></span>
- <span data-ttu-id="ac93d-121">ในหน้า **นิติบุคคล** บน FastTab **การลงทะเบียนภาษี** ตั้งค่า **หมายเลขทะเบียนภาษี** สำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="ac93d-121">On the **Legal entities** page, on the **Tax registration** FastTab, set the **Tax registration number** value for the legal entity.</span></span>
- <span data-ttu-id="ac93d-122">ในหน้า **ประเภทการลงทะเบียน** แม็ปชนิดการลงทะเบียน **THA** เป็นประเภทการลงทะเบียน **รหัสองค์กร (COID)**</span><span class="sxs-lookup"><span data-stu-id="ac93d-122">On the **Registration categories** page, map the **THA** registration type to the **Enterprise ID (COID)** registration category.</span></span>
- <span data-ttu-id="ac93d-123">ตั้งค่ามิติ **Taxbranch** สำหรับลูกค้า ผู้จัดจำหน่าย โครงการ และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="ac93d-123">Set up the **Taxbranch** dimension for customers, vendors, projects, and so on.</span></span>
- <span data-ttu-id="ac93d-124">ในหน้า **จัดการที่อยู่** ตั้งค่าที่อยู่ของลูกค้าและผู้จัดจำหน่าย:</span><span class="sxs-lookup"><span data-stu-id="ac93d-124">On the **Manage addresses** page, set up customer and vendor addresses:</span></span>

    - <span data-ttu-id="ac93d-125">เพิ่มหมายเลขทะเบียนที่มีชนิดทะเบียน **THA**</span><span class="sxs-lookup"><span data-stu-id="ac93d-125">Add registration IDs that have the **THA** registration type.</span></span>
    - <span data-ttu-id="ac93d-126">ในหน้า **ข้อมูลภาษี** ระบุค่า **ชนิดที่อยู่ภาษี** และ **หมายเลขสาขา**</span><span class="sxs-lookup"><span data-stu-id="ac93d-126">On the **Tax information** page, specify the **Tax address type** and **Branch number** values.</span></span>

- <span data-ttu-id="ac93d-127">ในหน้า **พิมพ์การตั้งค่าการจัดการ** ที่เปิดจากหน้า **การตั้งค่าแบบฟอร์ม** ในบัญชีลูกหนี้หรือการจัดการโครงการ และการลงบัญชี ตั้งค่ารูปแบบรายงานสำหรับใบแจ้งหนี้ของลูกค้า ใบแจ้งหนี้ข้อความอิสระ และใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="ac93d-127">On the **Print management setup** page that is opened from the **Form setup** page in either Accounts receivable or Project management and accounting, set up report formats for customer invoices, free text invoices, and project invoices.</span></span> <span data-ttu-id="ac93d-128">เลือก **SalesInvoice.ReportTH**,  **FreeTextInvoice.ReportTH** และ **PSAProjInvoice.ReportTH** ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="ac93d-128">Select **SalesInvoice.ReportTH**, **FreeTextInvoice.ReportTH**, and **PSAProjInvoice.ReportTH**, respectively.</span></span>
- <span data-ttu-id="ac93d-129">ในหน้า **พารามิเตอร์บัญชีลูกหนี้** บนแท็บ **อัพเดต** และ **โครงการ** เลือกกล่องกาเครื่องหมาย **เปิดใช้งานฟังก์ชั่น ใบแทน/การยกเลิกและออกใบใหม่แทน ใบกำกับภาษีเดิม** สำหรับใบแจ้งหนี้ของบัญชีลูกหนี้และใบแจ้งหนี้โครงการ ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="ac93d-129">On the **Accounts receivable parameters** page, on the **Update** and **Project** tabs, select the **Enable tax document's substitution/adjustment function** check box for accounts receivable invoices and project invoices, respectively.</span></span>

## <a name="print-a-substitution-invoice"></a><span data-ttu-id="ac93d-130">พิมพ์ใบแจ้งหนี้การปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="ac93d-130">Print a substitution invoice</span></span>

<span data-ttu-id="ac93d-131">ถ้ามีการเปิดใช้งาน ฟังก์ชันแทน/การปรับปรุงภาษีใบแจ้งหนี้ จะสามารถพิมพ์ใบกำกับภาษีต้นฉบับได้เพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="ac93d-131">If the substitution/adjustment tax invoice functionality is enabled, the original tax invoice can be printed only one time.</span></span> <span data-ttu-id="ac93d-132">ถ้าคุณพยายามที่จะพิมพ์ซ้ำ คุณจะได้รับข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="ac93d-132">If you try to reprint it, you receive an error.</span></span> <span data-ttu-id="ac93d-133">ทำตามขั้นตอนเหล่านี้เพื่อพิมพ์ใบกำกับภาษี</span><span class="sxs-lookup"><span data-stu-id="ac93d-133">Follow these steps to reprint the tax invoice.</span></span>

1. <span data-ttu-id="ac93d-134">ในหน้า **สมุดรายวันใบแจ้งหนี้** เลือกใบแจ้งหนี้เพื่อพิมพ์</span><span class="sxs-lookup"><span data-stu-id="ac93d-134">On the **Invoice journal** page, select the invoice to reprint.</span></span>
2. <span data-ttu-id="ac93d-135">บนบานหน้าต่างการดำเนินการ บนแท็บ **ใบแจ้งหนี้** ให้คลิก **การปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="ac93d-135">On the Action Pane, on the **Invoice** tab, click **Adjustment**.</span></span>
3. <span data-ttu-id="ac93d-136">ในหน้า **ปรับปรุงใบกำกับภาษี** สร้างเรกคอร์ดใหม่ และตั้งค่าฟิลด์ **ชนิดการปรับปรุง** เป็น **การทดแทน**</span><span class="sxs-lookup"><span data-stu-id="ac93d-136">On the **Adjust tax invoice** page, create a new record, and set the **Adjustment type** field to **Substitution**.</span></span> <span data-ttu-id="ac93d-137">ในฟิลด์ **คำอธิบาย** ให้ป้อนเหตุผลสำหรับการทดแทน</span><span class="sxs-lookup"><span data-stu-id="ac93d-137">In the **Description** field, enter the reason for the substitution.</span></span>
4. <span data-ttu-id="ac93d-138">กลับไปที่หน้า **สมุดรายวันใบแจ้งหนี้** และคลิก **มุมมอง** > **แสดง ใบแทน**</span><span class="sxs-lookup"><span data-stu-id="ac93d-138">Return to the **Invoice journal** page, and click **View** > **Substitution preview**.</span></span> <span data-ttu-id="ac93d-139">ยืนยันว่าคุณต้องการพิมพ์ใบแจ้งหนี้การปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="ac93d-139">Confirm that you want to print the substitution invoice.</span></span>

<span data-ttu-id="ac93d-140">ใบกำกับภาษีเงินทดแทนรวมรายละเอียดที่เหมือนกันกับใบกำกับภาษีเดิม แต่มีเครื่องหมาย "การทดแทน"</span><span class="sxs-lookup"><span data-stu-id="ac93d-140">The substitution tax invoice includes the same information as the original tax invoice, but it has a "Substitution" mark.</span></span> <span data-ttu-id="ac93d-141">นอกจากนี้ ข้อคิดเห็นจะถูกเพิ่มที่ด้านล่างของใบกำกับภาษีเงินทดแทน</span><span class="sxs-lookup"><span data-stu-id="ac93d-141">Additionally, a comment is added to the bottom of the substitution tax invoice.</span></span> <span data-ttu-id="ac93d-142">ข้อคิดเห็นนี้รวมถึงเหตุผลสำหรับการทดแทน หมายเลขลำดับ และวันที่ของการทดแทน</span><span class="sxs-lookup"><span data-stu-id="ac93d-142">This comment includes the reason for the substitution, the sequence number, and the date of the substitution.</span></span>

> [!NOTE]
> <span data-ttu-id="ac93d-143">คุณต้องสร้างการทดแทนใหม่ทุกครั้งที่คุณพิมพ์ใบกำกับภาษี</span><span class="sxs-lookup"><span data-stu-id="ac93d-143">You must create a new substitution every time that you reprint a tax invoice.</span></span>

## <a name="adjust-customer-information-on-a-tax-invoice"></a><span data-ttu-id="ac93d-144">ปรับปรุงข้อมูลของลูกค้าในใบกำกับภาษี</span><span class="sxs-lookup"><span data-stu-id="ac93d-144">Adjust customer information on a tax invoice</span></span>

<span data-ttu-id="ac93d-145">ถ้ามีการเปิดใช้งานฟังก์ชันใบกำกับภาษีเงินทดแทน/การปรับปรุง คุณสามารถปรับปรุงข้อมูลลูกค้าที่ถูกพิมพ์บนใบกำกับภาษี และจากนั้นพิมพ์ใบกำกับภาษีใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="ac93d-145">If the substitution/adjustment tax invoice functionality is enabled, you can adjust the customer information that is printed on a tax invoice and then reprint the tax invoice.</span></span> <span data-ttu-id="ac93d-146">คุณสามารถปรับปรุงข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ac93d-146">You can adjust the following information:</span></span>

- <span data-ttu-id="ac93d-147">ชื่อของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="ac93d-147">Customer name</span></span>
- <span data-ttu-id="ac93d-148">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="ac93d-148">Address</span></span>
- <span data-ttu-id="ac93d-149">โทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="ac93d-149">Telephone</span></span>
- <span data-ttu-id="ac93d-150">โทรสาร</span><span class="sxs-lookup"><span data-stu-id="ac93d-150">Fax</span></span>
- <span data-ttu-id="ac93d-151">หมายเลขการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="ac93d-151">Registration number</span></span>
- <span data-ttu-id="ac93d-152">หมายเลขสาขา</span><span class="sxs-lookup"><span data-stu-id="ac93d-152">Branch number</span></span>
- <span data-ttu-id="ac93d-153">ชื่อสาขา</span><span class="sxs-lookup"><span data-stu-id="ac93d-153">Branch name</span></span>

<span data-ttu-id="ac93d-154">ทำตามขั้นตอนเหล่านี้เพื่อปรับปรุงข้อมูลของลูกค้า และพิมพ์ใบกำกับภาษีใหม่</span><span class="sxs-lookup"><span data-stu-id="ac93d-154">Follow these steps to adjust the customer information and reprint the tax invoice.</span></span>

1. <span data-ttu-id="ac93d-155">ในหน้า **สมุดรายวันใบแจ้งหนี้** เลือกใบแจ้งหนี้เพื่อพิมพ์</span><span class="sxs-lookup"><span data-stu-id="ac93d-155">On the **Invoice journal** page, select the invoice to reprint.</span></span>
2. <span data-ttu-id="ac93d-156">บนบานหน้าต่างการดำเนินการ บนแท็บ **ใบแจ้งหนี้** ให้คลิก **การปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="ac93d-156">On the Action Pane, on the **Invoice** tab, click **Adjustment**.</span></span>
3. <span data-ttu-id="ac93d-157">ในหน้า **ปรับปรุงใบกำกับภาษี** สร้างเรกคอร์ดใหม่ และตั้งค่าฟิลด์ **ชนิดการปรับปรุง** เป็น **การปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="ac93d-157">On the **Adjust tax invoice** page, create a new record, and set the **Adjustment type** field to **Adjustment**.</span></span> <span data-ttu-id="ac93d-158">ในฟิลด์ **คำอธิบาย** ให้ป้อนเหตุผลสำหรับการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="ac93d-158">In the **Description** field, enter the reason for the adjustment.</span></span>
4. <span data-ttu-id="ac93d-159">ปรับปรุงฟิลด์ข้อมูลของลูกค้าตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="ac93d-159">Adjust the customer information fields as you require.</span></span>
5. <span data-ttu-id="ac93d-160">กลับไปที่หน้า **สมุดรายวันใบแจ้งหนี้** และคลิก **มุมมอง** > **แสดง ใบใหม่ (แทนใบเดิม)**</span><span class="sxs-lookup"><span data-stu-id="ac93d-160">Return to the **Invoice journal** page, and click **View** > **Adjustment preview**.</span></span> <span data-ttu-id="ac93d-161">ยืนยันว่าคุณต้องการพิมพ์ใบกำกับภาษี</span><span class="sxs-lookup"><span data-stu-id="ac93d-161">Confirm that you want to print the tax invoice.</span></span>

<span data-ttu-id="ac93d-162">ใบกำกับภาษีที่ปรับปรุงรวมถึงหมายเลขใบกำกับภาษีใหม่ และข้อมูลของลูกค้าที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="ac93d-162">The adjusted tax invoice includes a new tax invoice number and adjusted customer information.</span></span> <span data-ttu-id="ac93d-163">ข้อมูลอื่น ๆ ทั้งหมดจะเหมือนกับข้อมูลในใบกำกับภาษีเดิม</span><span class="sxs-lookup"><span data-stu-id="ac93d-163">All other information is the same as the information on the original tax invoice.</span></span> <span data-ttu-id="ac93d-164">ข้อคิดเห็นจะถูกเพิ่มที่ด้านล่างของใบกำกับภาษีที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="ac93d-164">A comment is added to the bottom of the adjusted tax invoice.</span></span> <span data-ttu-id="ac93d-165">ข้อคิดเห็นนี้มีการอ้างอิงถึงใบกำกับภาษีเดิม เหตุผลสำหรับการปรับปรุง และวันที่ของการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="ac93d-165">This comment includes the reference to the original tax invoice, the reason for the adjustment, and the date of the adjustment.</span></span>

<span data-ttu-id="ac93d-166">คุณสามารถปรับปรุงใบกำกับภาษีได้หลายครั้ง</span><span class="sxs-lookup"><span data-stu-id="ac93d-166">You can adjust a tax invoice multiple times.</span></span> <span data-ttu-id="ac93d-167">สำหรับการปรับปรุงแต่ละครั้ง จะมีการปันส่วนหมายเลขใบกำกับภาษีใหม่ และใบแจ้งหนี้ที่ปรับปรุงจะอ้างอิงถึงการปรับปรุงก่อนหน้านี้หรือใบกำกับภาษีเดิม</span><span class="sxs-lookup"><span data-stu-id="ac93d-167">For each adjustment, a new tax invoice number is allocated, and the adjusted invoice references the previous adjustment or the original tax invoice.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]