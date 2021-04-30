---
title: รายงานสมุดรายวัน
description: หัวข้อนี้อธิบายวิธีการใช้งานรายงานสมุดรายวันที่เกี่ยวข้องกับนิติบุคคลที่มีที่อยู่หลักในเบลเยียมโดยเฉพาะ
author: anasyash
ms.date: 04/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, VendParameters, CustParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265924
ms.assetid: 829a101f-e329-48b9-baf8-e36670ff43c8
ms.search.region: Thailand
ms.author: anasyash
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4223fb76e70831866c8771642d495e0d04b406cf
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894857"
---
# <a name="journal-reports-posting-journals"></a><span data-ttu-id="a40f1-103">รายงานสมุดรายวัน (การลงรายการบัญชีสมุดรายวัน)</span><span class="sxs-lookup"><span data-stu-id="a40f1-103">Journal reports (Posting journals)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a40f1-104">บริษัทเบลเยียมต้องพิมพ์รายงานของแต่ละสมุดรายวันเป็นระยะ</span><span class="sxs-lookup"><span data-stu-id="a40f1-104">Periodically, Belgian companies must print a report for each journal.</span></span> <span data-ttu-id="a40f1-105">รายงานจะแสดงรายการการลงรายการบัญชีทั้งหมดตามลำดับเวลาในบัญชีแยกประเภททั่วไปของแต่ละสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a40f1-105">The report provides a chronological list of all the postings to the general ledger accounts for each journal.</span></span> <span data-ttu-id="a40f1-106">รายงานเหล่านี้จะพิสูจน์ความถูกต้องของรายการบัญชีและใช้ในการตรวจสอบการเงินเพื่อกระทบยอดการชําระเงิน VAT กับการลงรายการบัญชีในบัญชีแยกประเภททั่วไปที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="a40f1-106">These reports prove the integrity of the accountancy and are used during financial audits to reconcile VAT settlement with the postings on the corresponding general ledger accounts.</span></span>

<span data-ttu-id="a40f1-107">คุณสามารถสร้างรายงานได้ห้าชนิด</span><span class="sxs-lookup"><span data-stu-id="a40f1-107">There are five types of reports you can generate.</span></span>

   - <span data-ttu-id="a40f1-108">**สมุดรายวันการซื้อ**: แสดงภาพรวมของการซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a40f1-108">**Purchase journal**: Provides an overview of all purchases.</span></span>
   - <span data-ttu-id="a40f1-109">**สมุดรายวันการขาย**: แสดงภาพรวมของการขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a40f1-109">**Sales journal**: Provides an overview of all sales.</span></span>
   - <span data-ttu-id="a40f1-110">**สมุดรายวันทางการเงิน**: แสดงภาพรวมของรายการทางการเงินทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a40f1-110">**Financial journal**: Provides an overview of all financial entries.</span></span>
   - <span data-ttu-id="a40f1-111">**สมุดรายวันอื่น**: แสดงภาพรวมของการดําเนินงานที่หลากหลายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a40f1-111">**Other journal**: Provides an overview of all diverse operations.</span></span>
   - <span data-ttu-id="a40f1-112">**ภาพรวมสมุดรายวัน**: แสดงภาพรวมของสมุดรายวันที่พิมพ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a40f1-112">**Overview journal**: Provides an overview of all the printed journals.</span></span>

<span data-ttu-id="a40f1-113">รายงานเหล่านี้สามารถใช้ได้เฉพาะกับนิติบุคคลที่มีที่อยู่หลักอยู่ในเบลเยียมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a40f1-113">These reports are available only to legal entities whose primary address is in Belgium.</span></span>

<span data-ttu-id="a40f1-114">แต่ละรายงานจะประกอบด้วยส่วนและสรุปต่าง ๆ ดังนี้</span><span class="sxs-lookup"><span data-stu-id="a40f1-114">Each report consists of several sections and summaries including:</span></span>

   - <span data-ttu-id="a40f1-115">ภาพรวมโดยละเอียดของการลงรายการบัญชีในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a40f1-115">A detailed overview of the postings to the general ledger accounts.</span></span>
   - <span data-ttu-id="a40f1-116">สรุปของการลงรายการบัญชีในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a40f1-116">A summary of the postings to the general ledger accounts.</span></span>
   - <span data-ttu-id="a40f1-117">ภาพรวมโดยละเอียดของการลงรายการบัญชีภาษี</span><span class="sxs-lookup"><span data-stu-id="a40f1-117">A detailed overview of tax posting.</span></span>
   - <span data-ttu-id="a40f1-118">สรุปการลงรายการบัญชีภาษี</span><span class="sxs-lookup"><span data-stu-id="a40f1-118">A summary of tax posting.</span></span>
   - <span data-ttu-id="a40f1-119">สรุปกล่องจํานวนเงินภาษีที่ใช้ในสมุดรายวันที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a40f1-119">A summary of the tax amount boxes used in the selected journal.</span></span>

<span data-ttu-id="a40f1-120">คุณสามารถตั้งค่าพารามิเตอร์ต่อไปนี้เมื่อคุณสร้างรายงานได้</span><span class="sxs-lookup"><span data-stu-id="a40f1-120">You can set the following parameters when you generate a report.</span></span>

| <span data-ttu-id="a40f1-121">**ฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="a40f1-121">**Field**</span></span> | <span data-ttu-id="a40f1-122">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="a40f1-122">**Description**</span></span> |
|-------------------------|-------------------------|
| <span data-ttu-id="a40f1-123">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a40f1-123">Journal</span></span> | <span data-ttu-id="a40f1-124">เลือกชื่อของสมุดรายวันการขายที่จะใช้ลงรายการบัญชีธุรกรรมที่บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a40f1-124">Select the name of the sales journal to use to post transactions to the general ledger account.</span></span> |
| <span data-ttu-id="a40f1-125">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a40f1-125">From date</span></span> | <span data-ttu-id="a40f1-126">ให้เลือกหรือป้อนวันที่เริ่มต้นของรอบระยะเวลาการรายงาน</span><span class="sxs-lookup"><span data-stu-id="a40f1-126">Select or enter the start date of the reporting period.</span></span> |
| <span data-ttu-id="a40f1-127">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="a40f1-127">To date</span></span> | <span data-ttu-id="a40f1-128">ให้เลือกหรือป้อนวันที่สิ้นสุดของรอบระยะเวลาการรายงาน</span><span class="sxs-lookup"><span data-stu-id="a40f1-128">Select or enter the end date of the reporting period.</span></span> |
| <span data-ttu-id="a40f1-129">เอกสารพิมพ์สุดท้าย</span><span class="sxs-lookup"><span data-stu-id="a40f1-129">Final print</span></span> | <span data-ttu-id="a40f1-130">ตั้งค่าเป็น **ใช่** เพื่อพิมพ์รายงานรุ่นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="a40f1-130">Set to **Yes** to print the final version of the report.</span></span></br><span data-ttu-id="a40f1-131">เมื่อคุณเลือก **เอกสารพิมพ์สุดท้าย** จะเกิดสิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a40f1-131">When you select **Final print**, the following occurs:</span></span></br><ol style="list-style-type: decimal"></br><li><span data-ttu-id="a40f1-132">**วันที่เริ่มต้น** ที่คุณเลือกต้องเป็นของรอบระยะเวลาที่ตามหลังรอบระยะเวลาของวันที่สิ้นสุดของเอกสารพิมพ์สุดท้าย</span><span class="sxs-lookup"><span data-stu-id="a40f1-132">The **From date** you selected must belong to the period following the period of the last final printout end date.</span></span> <span data-ttu-id="a40f1-133">การตรวจสอบความถูกต้องนี้จะขึ้นอยู่กับค่าที่ป้อนไว้ในฟิลด์ **สมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="a40f1-133">This validation depends on the value entered in the **Journal** field.</span></span> <span data-ttu-id="a40f1-134">ถ้าฟิลด์นี้ว่าง สมุดรายวันการลงรายการบัญชีทั้งหมดที่เป็นของชนิดนี้ (การซื้อ การขาย ทางการเงิน หรืออื่น ๆ) จะมีการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a40f1-134">If the field is empty, all of the posting journals that belong to this type (purchase, sales, financial, or other) are validated.</span></span></li></br><li><span data-ttu-id="a40f1-135">หมายเลขหน้าของรายงานเป็นลำดับ</span><span class="sxs-lookup"><span data-stu-id="a40f1-135">The page number of the report is sequential.</span></span> <span data-ttu-id="a40f1-136">หมายเลขหน้าของรอบระยะเวลาก่อนหน้านี้ +1 จะใช้เป็นข้อมูลพื้นฐานใหม่ในการระบุหมายเลข</span><span class="sxs-lookup"><span data-stu-id="a40f1-136">The page number of the previous periods +1 is used as basis for the new numbering.</span></span> <span data-ttu-id="a40f1-137">การระบุหมายเลขหน้าเริ่มต้นเป็นศูนย์สำหรับแต่ละปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="a40f1-137">Page numbering starts at zero for each new fiscal year.</span></span></li></br><li><span data-ttu-id="a40f1-138">รายการใหม่จะถูกเพิ่มในฟอร์มเอกสารพิมพ์สุดท้ายสำหรับแต่ละสมุดรายวันการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="a40f1-138">A new line is added in the final print form for each posting journal.</span></span></li></br></ol> |
| <span data-ttu-id="a40f1-139">บีบอัด</span><span class="sxs-lookup"><span data-stu-id="a40f1-139">Compress</span></span> | <span data-ttu-id="a40f1-140">เลือกตัวเลือกนี้เพื่อจัดกลุ่มยอดเงินในบัญชีแยกประเภทเดียวกันในใบสำคัญเดียวกันเป็นรายการเดียว</span><span class="sxs-lookup"><span data-stu-id="a40f1-140">Select this option to group amounts on the same ledger account in the same voucher into one line.</span></span></br><ul></br><li><span data-ttu-id="a40f1-141">เมื่อตั้งค่าเป็ฯ **ไม่** แต่ละธุรกรรมจะแสดงขึ้นบนรายการแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="a40f1-141">When set to **No**, each transaction is shown on a separate line.</span></span></li></br><li><span data-ttu-id="a40f1-142">เมื่อตั้งค่าเป็น **ใช่** ธุรกรรมจะถูกจัดกลุ่มตามบัญชีและแสดงเป็นรายการสรุปรายการเดียว</span><span class="sxs-lookup"><span data-stu-id="a40f1-142">When set to **Yes**, transactions are grouped by account and shown as one summarized line.</span></span></li></br></ul> |


## <a name="setup"></a><span data-ttu-id="a40f1-143">ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="a40f1-143">Setup</span></span>

<span data-ttu-id="a40f1-144">รายงานจะเชื่อมโยงกับสมุดรายวันการลงบัญชีในบัญชีแยกประเภททั่วไปตามลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="a40f1-144">The reports are linked to the posting journals in the general ledger by number sequences.</span></span> <span data-ttu-id="a40f1-145">สำหรับแต่ละสมุดรายวันการลงรายการบัญชี เลือกชนิดสมุดรายวัน การซื้อ การขาย อื่น ๆ หรือทางการเงิน หรือคุณสามารถปล่อยฟิลด์นี้ว่างไว้ได้</span><span class="sxs-lookup"><span data-stu-id="a40f1-145">For each posting journal, select the journal type, either purchase, sales, other, or financial, or you can leave the field empty.</span></span>

1. <span data-ttu-id="a40f1-146">ไปที่ **บัญชีแยกประเภททั่วไป** > **การตั้งค่าสมุดรายวัน** > **สมุดรายวันการลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="a40f1-146">Go to **General ledger** > **Journal setup** > **Posting journals**.</span></span>
2. <span data-ttu-id="a40f1-147">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างสมุดรายวันการลงรายการบัญชีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a40f1-147">On the Action Pane select **Create** to generate posting journals automatically.</span></span> <span data-ttu-id="a40f1-148">สมุดรายวันการลงบัญชีจะถูกสร้างขึ้นเพื่อให้สอดคล้องกับรหัสลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="a40f1-148">The posting journals are created to correspond with the number sequence codes.</span></span> <span data-ttu-id="a40f1-149">หากต้องการสร้างสมุดรายวันการลงบัญชีด้วยตนเอง เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="a40f1-149">To create a posting journal manually, select **New**.</span></span>
3. <span data-ttu-id="a40f1-150">เลือกสมุดรายวันการลงรายการบัญชีและในส่วน **รายงานสมุดรายวันภาษาเบลเยียม** ในฟิลด์ **ชนิดสมุดรายวัน** ให้เลือกชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a40f1-150">Select a posting journal and in the **Belgian journal reports** section, in the **Journal type** field, select the journal type.</span></span>
4. <span data-ttu-id="a40f1-151">ไปที่ **ภาษี** > **ภาษีทางอ้อม** > **ภาษีขาย** > **กลุ่มภาษีขายตามประเภทสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a40f1-151">Go to **Tax** > **Indirect taxes** > **Sales tax** > **Item sales tax groups**.</span></span>
5. <span data-ttu-id="a40f1-152">เลือกกลุ่มภาษีขายตามประเภทสินค้า และในฟิลด์ **ชนิดการรายงาน** ให้เลือกว่าจํานวนเงินของรายการภาษีขายตามประเภทสินค้าจะรวมอยู่ในรายการขายในสหภาพยุโรป (EU) ที่ใด</span><span class="sxs-lookup"><span data-stu-id="a40f1-152">Select an item sales tax group, and in the **Reporting type** field, select where the item sales tax line amount will be included on the European Union (EU) sales list.</span></span>

    - <span data-ttu-id="a40f1-153">**ว่างเปล่า**: ยอดเงินรายการภาษีขายรวมอยู่ในคอลัมน์ **ไม่ถูกกำหนด**</span><span class="sxs-lookup"><span data-stu-id="a40f1-153">**Blank**: The sales tax line amount is included in the **Not assigned** column.</span></span>
    - <span data-ttu-id="a40f1-154">**สินค้า**: ยอดเงินรายการภาษีขายรวมอยู่ในคอลัมน์ **สินค้า**</span><span class="sxs-lookup"><span data-stu-id="a40f1-154">**Item**: The sales tax line amount is included in the **Items** column.</span></span>
    - <span data-ttu-id="a40f1-155">**บริการ**: ยอดเงินรายการภาษีขายรวมอยู่ในคอลัมน์ **บริการ**</span><span class="sxs-lookup"><span data-stu-id="a40f1-155">**Service**: The sales tax line amount is included in the **Services** column.</span></span>
    - <span data-ttu-id="a40f1-156">**การลงทุน**: ยอดเงินรายการภาษีขายรวมอยู่ในคอลัมน์ **การลงทุน**</span><span class="sxs-lookup"><span data-stu-id="a40f1-156">**Investment**: The sales tax line amount is included in the **Investment** column.</span></span>

## <a name="sales-journals-report"></a><span data-ttu-id="a40f1-157">รายงานสมุดรายวันการขาย</span><span class="sxs-lookup"><span data-stu-id="a40f1-157">Sales journals report</span></span>

<span data-ttu-id="a40f1-158">รายงานน **สมุดรายวันการขาย** แสดงและพิมพ์สรุปธุรกรรมการขาย เช่น ใบแจ้งหนี้การขาย และใบลดหนี้ ที่ลงรายการบัญชีในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a40f1-158">The **Sales journals** report displays and prints a summary of sales transactions, such as sales invoices and credit memos that are posted to the general ledger.</span></span> <span data-ttu-id="a40f1-159">รายงานนี้จะสรุปสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a40f1-159">This report summarizes the following:</span></span>

   - <span data-ttu-id="a40f1-160">ธุรกรรมการจ่ายต่อใบสำคัญและบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a40f1-160">The payment transactions per voucher and general ledger account.</span></span>
   - <span data-ttu-id="a40f1-161">เดบิตและเครดิตโดยรวมต่อบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a40f1-161">The overall debits and credits per general ledger account.</span></span>
   - <span data-ttu-id="a40f1-162">รายละเอียดภาษีต่อรหัสภาษีและหมายเลขใบสำคัญ รวมทั้งยอดเงินฐานภาษีและการกระจายยอดเงินภาษีโดยเทียบกับสินค้า บริการ และการลงทุน</span><span class="sxs-lookup"><span data-stu-id="a40f1-162">The tax details per tax code and voucher number, including the tax base amount and tax amount distribution against goods, services, and investments.</span></span>
   - <span data-ttu-id="a40f1-163">รายการของการลงรายการบัญชีภาษีโดยเรียงลำดับตามรหัสการรายงานภาษีที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="a40f1-163">A list of the tax postings sorted by their corresponding tax reporting codes.</span></span>

<span data-ttu-id="a40f1-164">โดยทั่วไป รายงานนี้จะใช้โดยตัวแทนเรียกเก็บเงิน ผู้จัดการการเรียกเก็บเงิน ประธานเจ้าหน้าที่ฝ่ายการเงิน เจ้าหน้าที่บัญชีลูกหนี้ ผู้จัดการบัญชีลูกหนี้ ผู้ควบคุมการเงิน และผู้ควบคุมการเงิน เพื่อทบทวนสถานะของใบแจ้งหนี้และกระบวนการเงินสด</span><span class="sxs-lookup"><span data-stu-id="a40f1-164">This report is typically used by collections agents, collections managers, chief financial officers, accounts receivable clerks, accounts receivable managers, and financial controllers to review the status of the invoices and the cash process.</span></span>

<span data-ttu-id="a40f1-165">ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันการขาย** และตั้งค่าพารามิเตอร์เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="a40f1-165">Go to **General ledger** > **Inquiries and reports** > **Journal reports** > **Sales journals** and set the parameters to generate the report.</span></span>

## <a name="purchase-journals-report"></a><span data-ttu-id="a40f1-166">รายงานสมุดรายวันการซื้อ</span><span class="sxs-lookup"><span data-stu-id="a40f1-166">Purchase journals report</span></span>

<span data-ttu-id="a40f1-167">รายงาน **สมุดรายวันการซื้อ** แสดงและพิมพ์สรุปของธุรกรรมในสมุดรายวันการซื้อ</span><span class="sxs-lookup"><span data-stu-id="a40f1-167">The **Purchase journals** report displays and prints a summary of the transactions in a purchase journal.</span></span> <span data-ttu-id="a40f1-168">โดยทั่วไป รายงานนี้จะใช้โดยผู้ประสานงานบัญชีเจ้าหนี้และผู้จัดทำบัญชี</span><span class="sxs-lookup"><span data-stu-id="a40f1-168">This report is typically used by accounts payable coordinators and accountants.</span></span>

<span data-ttu-id="a40f1-169">ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันการซื้อ** และตั้งค่าพารามิเตอร์เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="a40f1-169">Go to **General ledger** > **Inquiries and reports** > **Journal reports** > **Purchase journals** and set the parameters to generate the report.</span></span>

## <a name="financial-journal-report"></a><span data-ttu-id="a40f1-170">รายงานสมุดรายวันทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="a40f1-170">Financial journal report</span></span>

<span data-ttu-id="a40f1-171">รายงานน **สมุดรายวันทางการเงิน** แสดงและพิมพ์สรุปธุรกรรมทางการเงิน เช่น การชำระเงินของลูกค้า และการชำระเงินของผู้จัดจำหน่าย ที่ลงรายการบัญชีในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a40f1-171">The **Financial journals** report displays and prints a summary of financial transactions, such as customer payments and vendor payments, that are posted to the general ledger account.</span></span> <span data-ttu-id="a40f1-172">รายงานนี้จะสรุปสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a40f1-172">This report summarizes the following:</span></span>

   - <span data-ttu-id="a40f1-173">ธุรกรรมการจ่ายต่อใบสำคัญและบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a40f1-173">The payment transactions per voucher and general ledger account.</span></span>
   - <span data-ttu-id="a40f1-174">เดบิตและเครดิตโดยรวมต่อบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a40f1-174">The overall debits and credits per general ledger account.</span></span>
   - <span data-ttu-id="a40f1-175">รายละเอียดภาษีต่อรหัสภาษีและหมายเลขใบสำคัญ รวมทั้งยอดเงินฐานภาษีและการกระจายยอดเงินภาษีโดยเทียบกับสินค้า บริการ และการลงทุน</span><span class="sxs-lookup"><span data-stu-id="a40f1-175">The tax details per tax code and voucher number, including the tax base amount and tax amount distribution against goods, services, and investments.</span></span>
   - <span data-ttu-id="a40f1-176">รายการของการลงรายการบัญชีภาษีโดยเรียงลำดับตามรหัสการรายงานภาษีที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="a40f1-176">A list of the tax postings sorted by their corresponding tax reporting codes.</span></span>

<span data-ttu-id="a40f1-177">โดยทั่วไป รายงานนี้จะใช้โดยประธานเจ้าหน้าที่บริหาร ประธานเจ้าหน้าที่ฝ่ายการเงิน ผู้จัดการฝ่ายการปฏิบัติตามกฎระเบียบ ผู้จัดการฝ่ายบัญชี ผู้ควบคุมงานบัญชี และผู้ควบคุมการเงิน เพื่อทบทวนสถานะของกระบวนการบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a40f1-177">This report is typically used by chief executive officers, chief financial officers, compliance managers, accounting managers, accounting supervisors, and financial controllers to review the status of the general ledger process.</span></span>

<span data-ttu-id="a40f1-178">ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันทางการเงิน** และตั้งค่าพารามิเตอร์เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="a40f1-178">Go to **General ledger** > **Inquiries and reports** > **Journal reports** > **Financial journals** and set the parameters to generate the report.</span></span>

## <a name="other-journal-report"></a><span data-ttu-id="a40f1-179">รายงานสมุดรายวันอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a40f1-179">Other journal report</span></span>

<span data-ttu-id="a40f1-180">รายงาน **สมุดรายวันอื่น ๆ** จะแสดงและพิมพ์สรุปของธุรกรรมที่ลงรายการบัญชีแล้ว ซึ่งไม่ได้จัดประเภทภายใต้การขาย การซื้อ หรือทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="a40f1-180">The **Other journal** report displays and prints a summary of the posted transactions that are not categorized under sales, purchases, or financials.</span></span> <span data-ttu-id="a40f1-181">โดยทั่วไป รายงานนี้จะใช้โดยผู้บัญชี ผู้จัดการฝ่ายบัญชี เสมียน ผู้ควบคุมงานบัญชี และผู้จัดการฝ่ายการปฏิบัติตามกฎระเบียบ เพื่อสอบถามเกี่ยวกับธุรกรรมสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a40f1-181">This report is typically used by accountants, accounting managers, clerks, accounting supervisors, and compliance managers to inquire into journal transactions.</span></span>

<span data-ttu-id="a40f1-182">ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันอื่น** และตั้งค่าพารามิเตอร์เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="a40f1-182">Go to **General ledger** > **Inquiries and reports** > **Journal reports** > **Other journals** and set the parameters to generate the report.</span></span>

## <a name="overview-journal-report"></a><span data-ttu-id="a40f1-183">ภาพรวมรายงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a40f1-183">Overview journal report</span></span>

<span data-ttu-id="a40f1-184">รายงาน **สมุดรายวันภาพรวม** จะแสดงและพิมพ์สรุปของธุรกรรมที่ลงรายการบัญชีแล้ว ซึ่งไม่ได้จัดประเภทภายใต้การขาย การซื้อ หรือทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="a40f1-184">The **Overview journal** report displays and prints a summary of the posted transactions that aren't categorized under sales, purchases, or financials.</span></span>

<span data-ttu-id="a40f1-185">โดยทั่วไป รายงานนี้จะใช้โดยผู้บัญชี ผู้จัดการฝ่ายบัญชี เสมียน ผู้ควบคุมงานบัญชี และผู้จัดการฝ่ายการปฏิบัติตามกฎระเบียบ เพื่อสอบถามเกี่ยวกับธุรกรรมสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a40f1-185">This report is typically used by accountants, accounting managers, clerks, accounting supervisors, and compliance managers to inquire into journal transactions.</span></span>

## <a name="example"></a><span data-ttu-id="a40f1-186">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a40f1-186">Example</span></span>

<span data-ttu-id="a40f1-187">ตัวอย่างต่อไปนี้แสดงวิธีที่คุณสามารถตั้งค่าการลงรายการบัญชีสมุดรายวัน และสร้างและพิมพ์รายงานสมุดรายวันการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="a40f1-187">The following example shows how you can set up posting journals and generate and print the posting journals reports.</span></span> <span data-ttu-id="a40f1-188">ตัวอย่างนี้ใช้นิติบุคคล FRRT</span><span class="sxs-lookup"><span data-stu-id="a40f1-188">This example uses the FRRT legal entity.</span></span>

1. <span data-ttu-id="a40f1-189">ไปที่ **การจัดการองค์กร** > **องค์กร**> **นิติบุคคล** และเลือกนิติบุคคล FRRT</span><span class="sxs-lookup"><span data-stu-id="a40f1-189">Go to **Organization administration** > **Organization**> **Legal entities**, and select the FRRT legal entity.</span></span>
2. <span data-ttu-id="a40f1-190">บนแท็บด่วน **ที่อยู่** ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="a40f1-190">On the **Address** FastTab, select **Edit**.</span></span> <span data-ttu-id="a40f1-191">ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือก BEL (เบลเยียม)</span><span class="sxs-lookup"><span data-stu-id="a40f1-191">In the **Country/region** field, select BEL (Belgium).</span></span>
3. <span data-ttu-id="a40f1-192">ไปที่ **บัญชีแยกประเภททั่วไป** > **การตั้งค่าสมุดรายวัน** > **สมุดรายวันการลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="a40f1-192">Go to **General ledger** > **Journal Setup** > **Posting journals**.</span></span>
4. <span data-ttu-id="a40f1-193">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="a40f1-193">On the Action Pane, select **Create**.</span></span>
5. <span data-ttu-id="a40f1-194">ตั้งค่า **ชนิดสมุดรายวัน** ของสมุดรายวันตามตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a40f1-194">Set the **Journal type** for the journals according to the following table.</span></span>

    | <span data-ttu-id="a40f1-195">**สมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="a40f1-195">**Journal**</span></span> | <span data-ttu-id="a40f1-196">**ชนิดสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="a40f1-196">**Journal type**</span></span> |
    |-------------------------|-------------------------|
    | <span data-ttu-id="a40f1-197">Acco_46</span><span class="sxs-lookup"><span data-stu-id="a40f1-197">Acco_46</span></span> | <span data-ttu-id="a40f1-198">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="a40f1-198">Sales</span></span> |
    | <span data-ttu-id="a40f1-199">Acco_67</span><span class="sxs-lookup"><span data-stu-id="a40f1-199">Acco_67</span></span> | <span data-ttu-id="a40f1-200">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="a40f1-200">Purchase</span></span> |
    | <span data-ttu-id="a40f1-201">JourNdF</span><span class="sxs-lookup"><span data-stu-id="a40f1-201">JourNdF</span></span> | <span data-ttu-id="a40f1-202">การเงิน</span><span class="sxs-lookup"><span data-stu-id="a40f1-202">Financial</span></span> |
    | <span data-ttu-id="a40f1-203">ODComptabl</span><span class="sxs-lookup"><span data-stu-id="a40f1-203">ODComptabl</span></span> | <span data-ttu-id="a40f1-204">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a40f1-204">Other</span></span> |

6. <span data-ttu-id="a40f1-205">ไปที่ **ภาษี** > **ภาษีทางอ้อม** > **ภาษีขาย** > **กลุ่มภาษีขายตามประเภทสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a40f1-205">Go to **Tax** > **Indirect taxes** > **Sales tax** > **Item sales tax groups**.</span></span>
7. <span data-ttu-id="a40f1-206">เลือกกลุ่มภาษีขายตามประเภทสินค้า **ปกติ** และในฟิลด์ **ชนิดการรายงาน** ให้เลือก **สินค้า**</span><span class="sxs-lookup"><span data-stu-id="a40f1-206">Select the **NORMAL** item sales tax group and in the **Reporting type** field, select **Item**.</span></span>
8. <span data-ttu-id="a40f1-207">ไปที่ **ภาษี** > **ภาษีทางอ้อม** > **ภาษีขาย** > **หน่วยงานจัดเก็บภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="a40f1-207">Go to **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
9. <span data-ttu-id="a40f1-208">เลือก **TAXFRA** และบนแท็บด่วน **ทั่วไป** ในฟิลด์ **โครงร่างรายงาน** เลือก **โครงร่างรายงานเบลเยียม**</span><span class="sxs-lookup"><span data-stu-id="a40f1-208">Select the **TAXFRA** and on the **General** FastTab, in the **Report layout** field, select **Belgium report layout**.</span></span>
10. <span data-ttu-id="a40f1-209">ไปที่ **ภาษี** > **การตั้งค่า** > **ภาษีขาย** > **รหัสการรายงานภาษีขาย** และสร้างรหัสการรายงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a40f1-209">Go to **Tax** > **Setup** > **Sales tax** > **Sales tax reporting codes** and create the following reporting codes.</span></span>

    | <span data-ttu-id="a40f1-210">**โครงร่างรายงาน**</span><span class="sxs-lookup"><span data-stu-id="a40f1-210">**Reporting layout**</span></span> | <span data-ttu-id="a40f1-211">**รหัสการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="a40f1-211">**Reporting code**</span></span> | <span data-ttu-id="a40f1-212">**ข้อความในรายงาน**</span><span class="sxs-lookup"><span data-stu-id="a40f1-212">**Report text**</span></span> |
    |-------------------------|-------------------------|-------------------------|
    | <span data-ttu-id="a40f1-213">โครงร่างรายงานเบลเยียม</span><span class="sxs-lookup"><span data-stu-id="a40f1-213">Belgium reporting layout</span></span> | <span data-ttu-id="a40f1-214">03</span><span class="sxs-lookup"><span data-stu-id="a40f1-214">03</span></span> | <span data-ttu-id="a40f1-215">ภาษีวัสดุและบริการที่คิดภาษีในอัตราภาษีขาย 21 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="a40f1-215">Taxable supplies and services at a sales tax rate of 21 percent.</span></span></br><span data-ttu-id="a40f1-216">การจัดส่งธุรกรรมผลิตภัณฑ์หรือการบริการที่อัตราภาษีขาย 21 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="a40f1-216">The delivery of a product or service transactions at a sales tax rate of 21 percent.</span></span> |
    | <span data-ttu-id="a40f1-217">โครงร่างรายงานเบลเยียม</span><span class="sxs-lookup"><span data-stu-id="a40f1-217">Belgium reporting layout</span></span> | <span data-ttu-id="a40f1-218">54</span><span class="sxs-lookup"><span data-stu-id="a40f1-218">54</span></span> | <span data-ttu-id="a40f1-219">VAT ที่ค้างจ่ายในอัตราหมุนเวียนที่รวมอยู่ในรหัส **01** **02** และ **03**</span><span class="sxs-lookup"><span data-stu-id="a40f1-219">VAT that is payable on the turnover that is included in codes **01**, **02**, and **03**.</span></span> |
    | <span data-ttu-id="a40f1-220">โครงร่างรายงานเบลเยียม</span><span class="sxs-lookup"><span data-stu-id="a40f1-220">Belgium reporting layout</span></span> | <span data-ttu-id="a40f1-221">81</span><span class="sxs-lookup"><span data-stu-id="a40f1-221">81</span></span> | <span data-ttu-id="a40f1-222">ยอดเงินของการซื้อสินค้า วัตถุดิบ และต้นทุนการซื้อวัสดุทั้งหมด และต้นทุนการซื้อที่เกี่ยวข้อง ไม่รวม VAT ที่สามารถหักได้</span><span class="sxs-lookup"><span data-stu-id="a40f1-222">Amount of all purchases of goods, raw materials, and consumables, and related acquisition costs, excluding VAT deductible.</span></span> |
    | <span data-ttu-id="a40f1-223">โครงร่างรายงานเบลเยียม</span><span class="sxs-lookup"><span data-stu-id="a40f1-223">Belgium reporting layout</span></span> | <span data-ttu-id="a40f1-224">59</span><span class="sxs-lookup"><span data-stu-id="a40f1-224">59</span></span> | <span data-ttu-id="a40f1-225">จำนวนของ VAT ที่ไม่สามารถหักลดได้</span><span class="sxs-lookup"><span data-stu-id="a40f1-225">Amount of deductible VAT.</span></span> |


    <span data-ttu-id="a40f1-226">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่ารหัสการรายงานภาษีขาย](./emea-bel-intervat-tax-declaration.md#set-up-sales-tax-reporting-codes)</span><span class="sxs-lookup"><span data-stu-id="a40f1-226">For more information, see [Set up sales tax reporting codes](./emea-bel-intervat-tax-declaration.md#set-up-sales-tax-reporting-codes).</span></span>

11. <span data-ttu-id="a40f1-227">ไปที่ **ภาษี** > **ภาษีทางอ้อม** > **ภาษีขาย** > **รหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="a40f1-227">Go to **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax codes**.</span></span>
12. <span data-ttu-id="a40f1-228">เลือก **INA19.6** และบนแท็บด่วน **การตั้งค่ารายงาน** ในส่วน **การขาย** ให้เลือกสิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a40f1-228">Select **TVA19.6**, and on the **Report setup** FastTab, in the **Sale** section, select the following:</span></span>

     - <span data-ttu-id="a40f1-229">ในฟิลด์ **การขายที่ต้องเสียภาษี** เลือก 03</span><span class="sxs-lookup"><span data-stu-id="a40f1-229">In the **Taxable sales** field, select 03.</span></span>
     - <span data-ttu-id="a40f1-230">ในฟิลด์ **เจ้าหนี้ภาษีขาย** เลือก 54</span><span class="sxs-lookup"><span data-stu-id="a40f1-230">In the **Sales tax payable** field, select 54.</span></span>

13. <span data-ttu-id="a40f1-231">ในส่วน **การซื้อ** ให้เลือกสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a40f1-231">In the **Purchase** section, select the following:</span></span>

    - <span data-ttu-id="a40f1-232">ในฟิลด์ **ภาษีซื้อ** เลือก 81</span><span class="sxs-lookup"><span data-stu-id="a40f1-232">In the **Tax purchases** field, select 81.</span></span>
    - <span data-ttu-id="a40f1-233">ใน **ลูกหนี้ภาษีขาย** เลือก 59</span><span class="sxs-lookup"><span data-stu-id="a40f1-233">In the **Sales tax receivable**, select 59.</span></span>

### <a name="print-the-sales-journal-report"></a><span data-ttu-id="a40f1-234">พิมพ์รายงานสมุดรายวันการขาย</span><span class="sxs-lookup"><span data-stu-id="a40f1-234">Print the Sales journal report</span></span>

<span data-ttu-id="a40f1-235">เมื่อต้องการพิมพ์รายงาน **สมุดรายวันการขาย** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a40f1-235">To print the **Sales journal** report, follow these steps:</span></span>

1. <span data-ttu-id="a40f1-236">ไปที่ **บัญชีลูกหนี้** > **ใบแจ้งหนี้** > **ใบแจ้งหนี้ข้อความอิสระทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="a40f1-236">Go to **Accounts receivable** > **Invoices** > **All free text invoices**.</span></span>
2. <span data-ttu-id="a40f1-237">เลือก **สร้าง** และสร้างใบแจ้งหนี้ข้อความอิสระใหม่ด้วยข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a40f1-237">Select **New** and create a new free text invoice with the following information:</span></span>

    - <span data-ttu-id="a40f1-238">ในฟิลด์ **บัญชี** **ลูกค้า** เลือก US-1001</span><span class="sxs-lookup"><span data-stu-id="a40f1-238">In the **Customer** **account** field, select 1001.</span></span>
    - <span data-ttu-id="a40f1-239">ใน **ฟิลด์วันที่** เลือก 4/15/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-239">In the **Date field,** select 4/15/2021.</span></span>
    - <span data-ttu-id="a40f1-240">บนแท็บ **บรรทัดใบแจ้งหนี้** ในฟิลด์ **บัญชีหลัก** ให้เลือก **701000**</span><span class="sxs-lookup"><span data-stu-id="a40f1-240">On the **Invoice lines** FastTab, in the **Main account** field, select **701000**.</span></span>
    - <span data-ttu-id="a40f1-241">ในฟิลด์ **กลุ่มภาษีขาย** ให้เลือก VE-DOM</span><span class="sxs-lookup"><span data-stu-id="a40f1-241">In the **Sales tax group** field, select VE-DOM.</span></span>
    - <span data-ttu-id="a40f1-242">ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** เลือก ปกติ</span><span class="sxs-lookup"><span data-stu-id="a40f1-242">In the **Item sales tax group** field, select NORMAL.</span></span>
    - <span data-ttu-id="a40f1-243">ในฟิลด์ **คุณภาพ** ป้อน 1</span><span class="sxs-lookup"><span data-stu-id="a40f1-243">In the **Quality** field, enter 1.</span></span>
    - <span data-ttu-id="a40f1-244">ในฟิลด์ **ราคาต่อหน่วย** ให้ป้อน 100</span><span class="sxs-lookup"><span data-stu-id="a40f1-244">In the **Unit price** field, enter 100.</span></span>

3. <span data-ttu-id="a40f1-245">ลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="a40f1-245">Post the free text invoice.</span></span>
4. <span data-ttu-id="a40f1-246">ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันการขาย**</span><span class="sxs-lookup"><span data-stu-id="a40f1-246">Go to **General ledger** > **Inquiries and reports** > **Journal reports** > **Sales journals.**</span></span>
5. <span data-ttu-id="a40f1-247">ในส่วน **เงื่อนไข** ในฟิลด์ **สมุดรายวัน** ให้เลือก Acco\_46</span><span class="sxs-lookup"><span data-stu-id="a40f1-247">In the **Criteria** section, in the **Journal** field, select Acco\_46.</span></span>
6. <span data-ttu-id="a40f1-248">ในฟิลด์ **วันที่เริ่มต้น** เลือก 4/1/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-248">In the **From date** field, select 4/1/2021.</span></span>
7. <span data-ttu-id="a40f1-249">ในฟิลด์ **วันที่สิ้นสุด** เลือก 4/30/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-249">In the **To date** field, select 4/30/2021.</span></span>
8. <span data-ttu-id="a40f1-250">ในฟิลด์ **เอกสารพิมพ์สุดท้าย** เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="a40f1-250">In the **Final print** field, select **Yes**.</span></span> <span data-ttu-id="a40f1-251">เลือก **ตกลง** เพื่อตรวจทานรายงาน</span><span class="sxs-lookup"><span data-stu-id="a40f1-251">Select **OK** to review the report.</span></span>

    ![รายงานสมุดรายวันการขาย](media/emea-bel-journal-reports-sales-journal-report.png)

### <a name="print-the-purchase-journal-report"></a><span data-ttu-id="a40f1-253">พิมพ์รายงานสมุดรายวันการซื้อ</span><span class="sxs-lookup"><span data-stu-id="a40f1-253">Print the Purchase journal report</span></span>

<span data-ttu-id="a40f1-254">เมื่อต้องการพิมพ์รายงาน **สมุดรายวันการซื้อ** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a40f1-254">To print the **Purchase journal** report, follow these steps:</span></span>

1. <span data-ttu-id="a40f1-255">ไปที่ **บัญชีเจ้าหนี้** &gt; **ใบสั่งซื้อ** &gt; **ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="a40f1-255">Go to **Accounts payable** &gt; **Purchase orders** &gt; **All purchase orders**.</span></span>
2. <span data-ttu-id="a40f1-256">เลือก **สร้าง** และสร้างใบสั่งซื้อใหม่ด้วยข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a40f1-256">Select **New** and create a new purchase order with the following information:</span></span>

    - <span data-ttu-id="a40f1-257">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** เลือก **1001**</span><span class="sxs-lookup"><span data-stu-id="a40f1-257">In the **Vendor account** field, select **1001**.</span></span>
    - <span data-ttu-id="a40f1-258">ในฟิลด์ **หมายเลขสินค้า** ให้เลือก **0001**</span><span class="sxs-lookup"><span data-stu-id="a40f1-258">In the **Item number** field, select **0001**.</span></span>
    - <span data-ttu-id="a40f1-259">ในฟิลด์ **คุณภาพ** ป้อน 3</span><span class="sxs-lookup"><span data-stu-id="a40f1-259">In the **Quality** field, enter 3.</span></span>
    - <span data-ttu-id="a40f1-260">บนแท็บด่วน **รายละเอียดรายการ** บนแท็บ **การตั้งค่า** ในส่วน **ภาษีขาย** ใน **กลุ่มภาษีขายตามประเภทสินค้า** ให้เลือก **ปกติ**</span><span class="sxs-lookup"><span data-stu-id="a40f1-260">On the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, in the **Item sales tax group**, select **NORMAL**.</span></span> <span data-ttu-id="a40f1-261">ใน **กลุ่มภาษีขาย** ให้เลือก **VE-DOM**</span><span class="sxs-lookup"><span data-stu-id="a40f1-261">In the **Sales tax group**, select **VE-DOM**.</span></span>

3. <span data-ttu-id="a40f1-262">ไปที่ **การซื้อ** > **การดำเนินการ** > **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="a40f1-262">Go to **Purchase** > **Actions** > **Confirm**.</span></span>
4. <span data-ttu-id="a40f1-263">ไปที่ **ใบแจ้งหนี้** > **สร้าง** > **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="a40f1-263">Go to **Invoice** > **Generate** > **Invoice**.</span></span>
5. <span data-ttu-id="a40f1-264">ในส่วน **รหัสใบแจ้งหนี้** ในฟิลด์ **หมายเลข** ให้ป้อน INVNUM\_001</span><span class="sxs-lookup"><span data-stu-id="a40f1-264">In the **Invoice identification** section, in the **Number** field, enter INVNUM\_001.</span></span>
6. <span data-ttu-id="a40f1-265">ในส่วน **วันที่ในใบแจ้งหนี้** ในฟิลด์ **วันที่ของใบแจ้งหนี้** ให้เลือก 4/12/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-265">In the **Invoice dates** section, in the **Invoice date** field, select 4/12/2021.</span></span>
7. <span data-ttu-id="a40f1-266">ในฟิลด์ **วันที่ลงรายการบัญชี** เลือก 4/12/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-266">In the **Posting date** field, select 4/12/2021.</span></span>
8. <span data-ttu-id="a40f1-267">ลงรายการบัญชีใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="a40f1-267">Post the order.</span></span>
9. <span data-ttu-id="a40f1-268">ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="a40f1-268">Go to **General ledger** > **Inquiries and reports** > **Journal reports** > **Purchase journals.**</span></span>
10. <span data-ttu-id="a40f1-269">ในส่วน **เงื่อนไข** ในฟิลด์ **สมุดรายวัน** ให้เลือก **Acco\_67**</span><span class="sxs-lookup"><span data-stu-id="a40f1-269">In the **Criteria** section, in the **Journal** field, select **Acco\_67**.</span></span>
11. <span data-ttu-id="a40f1-270">ในฟิลด์ **วันที่เริ่มต้น** เลือก 4/1/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-270">In the **From date** field, select 4/1/2021.</span></span>
12. <span data-ttu-id="a40f1-271">ในฟิลด์ **วันที่สิ้นสุด** เลือก 4/30/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-271">In the **To date** field, select 4/30/2021.</span></span>
13. <span data-ttu-id="a40f1-272">ในฟิลด์ **เอกสารพิมพ์สุดท้าย** เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="a40f1-272">In the **Final print** field, select **Yes**.</span></span> <span data-ttu-id="a40f1-273">เลือก **ตกลง** เพื่อดูรายงาน</span><span class="sxs-lookup"><span data-stu-id="a40f1-273">Select **OK** to view the report.</span></span>

<span data-ttu-id="a40f1-274">![รายงานสมุดรายวันการซื้อหน้า 1](media/emea-bel-journal-reports-purchase-journal-report-1.png)
![รายงานสมุดรายวันการซื้อหน้า 2](media/emea-bel-journal-reports-purchase-journal-report-2.png)
![หน้ารายงานสมุดรายวันการซื้อ 3](media/emea-bel-journal-reports-purchase-journal-report-3.png)
![รายงานสมุดรายวันการซื้อหน้า 4](media/emea-bel-journal-reports-purchase-journal-report-4.png)</span><span class="sxs-lookup"><span data-stu-id="a40f1-274">![Purchase journal report page 1](media/emea-bel-journal-reports-purchase-journal-report-1.png)
![Purchase journal report page 2](media/emea-bel-journal-reports-purchase-journal-report-2.png)
![Purchase journal report page 3](media/emea-bel-journal-reports-purchase-journal-report-3.png)
![Purchase journal report page 4](media/emea-bel-journal-reports-purchase-journal-report-4.png)</span></span>

### <a name="print-the-financial-journal-report"></a><span data-ttu-id="a40f1-275">พิมพ์รายงานสมุดรายวันทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="a40f1-275">Print the Financial journal report</span></span>

<span data-ttu-id="a40f1-276">เมื่อต้องการพิมพ์รายงาน **สมุดรายวันทางการเงิน** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a40f1-276">To print the **Financial journal** report, follow these steps:</span></span>

1. <span data-ttu-id="a40f1-277">ไปที่ **บัญชีแยกประเภททั่วไป** > **รายการสมุดรายวัน** > **สมุดรายวันทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="a40f1-277">Go to **General ledger** > **Journal entries** > **General journals**.</span></span>
2. <span data-ttu-id="a40f1-278">สร้างสมุดรายวันใหม่</span><span class="sxs-lookup"><span data-stu-id="a40f1-278">Create a new journal.</span></span> <span data-ttu-id="a40f1-279">ในฟิลด์ **ชื่อ** ให้เลือก **JourNdF**</span><span class="sxs-lookup"><span data-stu-id="a40f1-279">In the **Name** field, select **JourNdF**.</span></span>
3. <span data-ttu-id="a40f1-280">เลือก **รายการ** และป้อนข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a40f1-280">Select **Lines**, and enter the following information:</span></span>

    - <span data-ttu-id="a40f1-281">ในฟิลด์ **วันที่** เลือก **4/15/2021**</span><span class="sxs-lookup"><span data-stu-id="a40f1-281">In the **Date** field, select **4/15/2021**.</span></span>
    - <span data-ttu-id="a40f1-282">ในฟิลด์ **ชนิดบัญชี** เลือก **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="a40f1-282">In the **Account type** field, select **Customer**.</span></span>
    - <span data-ttu-id="a40f1-283">ในฟิลด์ **บัญชี** เลือก **1001**</span><span class="sxs-lookup"><span data-stu-id="a40f1-283">In the **Account** field, select **1001**.</span></span>
    - <span data-ttu-id="a40f1-284">ในฟิลด์ **เครดิต** ป้อน 100</span><span class="sxs-lookup"><span data-stu-id="a40f1-284">In the **Credit** field, enter 100.</span></span>
    - <span data-ttu-id="a40f1-285">ในฟิลด์ **ชนิดบัญชีตรงข้าม** เลือก **ธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="a40f1-285">In the **Offset account type** field, select **Bank**.</span></span>
    - <span data-ttu-id="a40f1-286">ในฟิลด์ **บัญชีตรงข้าม** เลือก **FRRT OPER**</span><span class="sxs-lookup"><span data-stu-id="a40f1-286">In the **Offset account** field, select **FRRT OPER**.</span></span>
    - <span data-ttu-id="a40f1-287">ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** เลือก **ปกติ**</span><span class="sxs-lookup"><span data-stu-id="a40f1-287">In the **Item sales tax group** field, select **NORMAL**.</span></span>
    - <span data-ttu-id="a40f1-288">ในฟิลด์ **กลุ่มภาษีขาย ให้เลือก** เลือก **VE-DOM**</span><span class="sxs-lookup"><span data-stu-id="a40f1-288">In the **Sales tax group** field, select **VE-DOM**.</span></span>

4. <span data-ttu-id="a40f1-289">ลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a40f1-289">Post the journal.</span></span>
5. <span data-ttu-id="a40f1-290">ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="a40f1-290">Go to **General ledger** > **Inquiries and reports** > **Journal reports** > **Financial journals.**</span></span>
6. <span data-ttu-id="a40f1-291">ในส่วน **เงื่อนไข** ในฟิลด์ **สมุดรายวัน** ให้เลือก **JourNdF**</span><span class="sxs-lookup"><span data-stu-id="a40f1-291">In the **Criteria** section, in the **Journal** field, select **JourNdF**.</span></span>
7. <span data-ttu-id="a40f1-292">ในฟิลด์ **วันที่เริ่มต้น** เลือก 4/1/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-292">In the **From date** field, select 4/1/2021.</span></span>
8. <span data-ttu-id="a40f1-293">ในฟิลด์ **วันที่สิ้นสุด** เลือก 4/30/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-293">In the **To date** field, select 4/30/2021.</span></span>
9. <span data-ttu-id="a40f1-294">ในฟิลด์ **เอกสารพิมพ์สุดท้าย** เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="a40f1-294">In the **Final print** field select **Yes**.</span></span> <span data-ttu-id="a40f1-295">เลือก **ตกลง** เพื่อตรวจทานรายงาน</span><span class="sxs-lookup"><span data-stu-id="a40f1-295">Select **OK** to review the report.</span></span>

![รายงานสมุดรายวันทางการเงินหน้า 1](media/emea-bel-journal-reports-financial-journal-report.png)

![รายงานสมุดรายวันทางการเงินหน้า 2](media/emea-bel-journal-reports-financial-journal-report-2.png)

### <a name="print-the-other-journal-report"></a><span data-ttu-id="a40f1-298">พิมพ์รายงานสมุดรายวันอื่น</span><span class="sxs-lookup"><span data-stu-id="a40f1-298">Print the Other journal report</span></span>

<span data-ttu-id="a40f1-299">เมื่อต้องการพิมพ์รายงาน **สมุดรายวันอื่น** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a40f1-299">To print the **Other journal** report, follow these steps:</span></span>

1. <span data-ttu-id="a40f1-300">ไปที่ **บัญชีแยกประเภททั่วไป** > **รายการสมุดรายวัน** > **สมุดรายวันทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="a40f1-300">Go to **General ledger** > **Journal entries** > **General journals**.</span></span>
2. <span data-ttu-id="a40f1-301">สร้างสมุดรายวันใหม่</span><span class="sxs-lookup"><span data-stu-id="a40f1-301">Create a new journal.</span></span> <span data-ttu-id="a40f1-302">ในฟิลด์ **ชื่อ** ให้เลือก ODComptabl</span><span class="sxs-lookup"><span data-stu-id="a40f1-302">In the **Name** field, select ODComptabl.</span></span>
3. <span data-ttu-id="a40f1-303">ไปที่ **รายการ** และป้อนข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a40f1-303">Go to **Lines** and enter the following information:</span></span>

    - <span data-ttu-id="a40f1-304">ในฟิลด์ **วันที่** เลือก 4/15/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-304">In the **Date** field, select 4/15/2021.</span></span>
    - <span data-ttu-id="a40f1-305">ในฟิลด์ **ชนิดบัญชี** เลือก **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="a40f1-305">In the **Account type** field, select **Customer**.</span></span>
    - <span data-ttu-id="a40f1-306">ในฟิลด์ **บัญชี** เลือก **1001**</span><span class="sxs-lookup"><span data-stu-id="a40f1-306">In the **Account** field, select **1001**.</span></span>
    - <span data-ttu-id="a40f1-307">ในฟิลด์ **เดบิต** ป้อน 100</span><span class="sxs-lookup"><span data-stu-id="a40f1-307">In the **Debit** field, enter 100.</span></span>
    - <span data-ttu-id="a40f1-308">ในฟิลด์ **ชนิดบัญชีตรงข้าม** เลือก **ธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="a40f1-308">In the **Offset account type** field, select **Bank**.</span></span>
    - <span data-ttu-id="a40f1-309">ในฟิลด์ **บัญชีตรงข้าม** เลือก **FRRT OPER**</span><span class="sxs-lookup"><span data-stu-id="a40f1-309">In the **Offset account** field, select **FRRT OPER**.</span></span>
    - <span data-ttu-id="a40f1-310">ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** เลือก **ปกติ**</span><span class="sxs-lookup"><span data-stu-id="a40f1-310">In the **Item sales tax group** field, select **NORMAL**.</span></span>
    - <span data-ttu-id="a40f1-311">ในฟิลด์ **กลุ่มภาษีขาย ให้เลือก** เลือก **VE-DOM**</span><span class="sxs-lookup"><span data-stu-id="a40f1-311">In the **Sales tax group** field, select **VE-DOM**.</span></span>

4. <span data-ttu-id="a40f1-312">ลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a40f1-312">Post the journal.</span></span>
5. <span data-ttu-id="a40f1-313">ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันอื่น**</span><span class="sxs-lookup"><span data-stu-id="a40f1-313">Go to **General ledger** > **Inquiries and reports** > **Journal reports** > **Other journals.**</span></span>
6. <span data-ttu-id="a40f1-314">ในส่วน **เงื่อนไข** ในฟิลด์ **สมุดรายวัน** ให้เลือก ODComptabl</span><span class="sxs-lookup"><span data-stu-id="a40f1-314">In the **Criteria** section, in the **Journal** field, select ODComptabl.</span></span>
7. <span data-ttu-id="a40f1-315">ในฟิลด์ **วันที่เริ่มต้น** เลือก 5/1/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-315">In the **From date** field, select 5/1/2021.</span></span>
8. <span data-ttu-id="a40f1-316">ในฟิลด์ **วันที่สิ้นสุด** เลือก 5/31/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-316">In the **To date** field, select 5/31/2021.</span></span>
9. <span data-ttu-id="a40f1-317">ในฟิลด์ **เอกสารพิมพ์สุดท้าย** เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="a40f1-317">In the **Final print** field, select **Yes**.</span></span>
10. <span data-ttu-id="a40f1-318">เลือก **ตกลง** และตรวจทานผลลัพธ์รายงาน</span><span class="sxs-lookup"><span data-stu-id="a40f1-318">Select **OK** and review the report result.</span></span>

<span data-ttu-id="a40f1-319">![รายงานสมุดรายวันอื่นหน้า 1](media/emea-bel-journal-reports-other-journal-report-1.png)
![รายงานสมุดรายวันอื่นหน้า 2](media/emea-bel-journal-reports-other-journal-report-2.png)</span><span class="sxs-lookup"><span data-stu-id="a40f1-319">![Other journals report page 1](media/emea-bel-journal-reports-other-journal-report-1.png)
![Other journals report page 2](media/emea-bel-journal-reports-other-journal-report-2.png)</span></span>

### <a name="print-overview-journal-report"></a><span data-ttu-id="a40f1-320">พิมพ์รายงานสมุดรายวันภาพรวม</span><span class="sxs-lookup"><span data-stu-id="a40f1-320">Print overview journal report</span></span>

<span data-ttu-id="a40f1-321">เมื่อต้องการพิมพ์รายงาน **สมุดรายวันภาพรวม** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a40f1-321">To print the **Overview journal** report, follow these steps:</span></span>

1. <span data-ttu-id="a40f1-322">ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและรายงาน** > **รายงานสมุดรายวัน** > **สมุดรายวันภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="a40f1-322">Go to **General ledger** > **Inquiries and reports** > **Journal reports** > **Overview journals.**</span></span>
2. <span data-ttu-id="a40f1-323">ในฟิลด์ **วันที่เริ่มต้น** เลือก 4/1/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-323">In the **From date** field, select 4/1/2021.</span></span>
3. <span data-ttu-id="a40f1-324">ในฟิลด์ **วันที่สิ้นสุด** เลือก 5/31/2021</span><span class="sxs-lookup"><span data-stu-id="a40f1-324">In the **To date** field, select 5/31/2021.</span></span>
4. <span data-ttu-id="a40f1-325">เลือก **ตกลง** และตรวจทานผลลัพธ์รายงาน</span><span class="sxs-lookup"><span data-stu-id="a40f1-325">Select **OK** and review the report result.</span></span>

![ภาพรวมรายงานสมุดรายวัน](media/emea-bel-journal-reports-overview-journal-report.png)