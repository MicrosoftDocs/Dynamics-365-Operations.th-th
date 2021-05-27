---
title: มีการลงรายการบัญชีภาษีไปที่บัญชีแยกประเภทในใบสำคัญที่ไม่ถูกต้อง
description: หัวข้อนี้มีข้อมูลการแก้ไขปัญหาเบื้องต้นที่สามารถช่วยได้เมื่อลงรายการบัญชีภาษีในบัญชีแยกประเภทที่ไม่ถูกต้องในใบสำคัญ
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020102"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="3d50b-103">มีการลงรายการบัญชีภาษีไปที่บัญชีแยกประเภทในใบสำคัญที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3d50b-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d50b-104">ในระหว่างการลงรายการบัญชี มีการลงรายการบัญชีภาษีไปที่บัญชีแยกประเภทในใบสำคัญที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3d50b-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="3d50b-105">เมื่อต้องการแก้ไขปัญหานี้ ให้ปฏิบัติตามขั้นตอนในส่วนต่อไปนี้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="3d50b-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="3d50b-106">ตัวอย่างในหัวข้อนี้ใช้ใบสั่งขายเป็นเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3d50b-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="3d50b-107">ค้นหารหัสภาษีขายของธุรกรรมที่ลงรายการบัญชีไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3d50b-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="3d50b-108">บนหน้า **ธุรกรรมใบสำคัญ** ให้เลือกธุรกรรมที่คุณต้องการใช้งาน แล้วเลือก **ภาษีขายที่ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="3d50b-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="3d50b-109">[![ปุ่มภาษีขายที่ลงรายการบัญชีบนหน้าธุรกรรมใบสำคัญ](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="3d50b-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="3d50b-110">ให้ตรวจสอบค่าในฟิลด์ **รหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="3d50b-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="3d50b-111">ในตัวอย่างนี้ **VAT 19**</span><span class="sxs-lookup"><span data-stu-id="3d50b-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="3d50b-112">[![ฟิลด์รหัสภาษีขายในหน้าภาษีขายที่ลงรายการบัญชี](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="3d50b-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="3d50b-113">ตรวจสอบกลุ่มการลงรายการบัญชีแยกประเภทสำหรับรหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="3d50b-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="3d50b-114">ไปที่ **ภาษี** \> **ภาษีทางอ้อม** \> **ภาษีขาย** \> **รหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="3d50b-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="3d50b-115">ค้นหาและเลือกรหัสภาษี แล้วตรวจทานค่าในฟิลด์ **กลุ่มการลงรายการบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="3d50b-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="3d50b-116">ในตัวอย่างนี้ **VAT**</span><span class="sxs-lookup"><span data-stu-id="3d50b-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="3d50b-117">[![ฟิลด์กลุ่มการลงรายการบัญชีแยกประเภทบนหน้ารหัสภาษีขาย](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="3d50b-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="3d50b-118">ค่าในฟิลด์ **กลุ่มการลงรายการบัญชีแยกประเภท** เป็นลิงค์</span><span class="sxs-lookup"><span data-stu-id="3d50b-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="3d50b-119">เลือกลิงค์นั้นหากต้องการดูรายละเอียดของการตั้งค่าคอนฟิกของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="3d50b-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="3d50b-120">หรือเลือกระงับ (หรือคลิกขวา) ในฟิลด์ แล้วเลือก **ดูรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="3d50b-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="3d50b-121">[![ดูคำสั่งในรายละเอียด](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="3d50b-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="3d50b-122">ในฟิลด์ **เจ้าหนี้ภาษีขาย** ให้ตรวจสอบว่าหมายเลขบัญชีถูกต้องตามชนิดของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3d50b-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="3d50b-123">ถ้าไม่ ให้เลือกบัญชีที่ถูกต้องที่จะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="3d50b-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="3d50b-124">ในตัวอย่างนี้ ภาษีขายของใบสั่งขายควรได้รับการลงรายการบัญชีไปยังบัญชีเจ้าหนี้ภาษีขาย 222200</span><span class="sxs-lookup"><span data-stu-id="3d50b-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="3d50b-125">[![ฟิลด์เจ้าหนี้ภาษีขายในหน้ากลุ่มการลงรายการบัญชีแยกประเภท](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="3d50b-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="3d50b-126">ตารางต่อไปนี้จะให้ข้อมูลเกี่ยวกับแต่ละฟิลด์ในหน้า **กลุ่มการลงรายการบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="3d50b-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="3d50b-127">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="3d50b-127">Field</span></span>                  | <span data-ttu-id="3d50b-128">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3d50b-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="3d50b-129">เจ้าหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3d50b-129">Sales tax payable</span></span>      | <span data-ttu-id="3d50b-130">บัญชีหลักสำหรับภาษีขายขาออกที่ต้องชำระให้แก่หน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="3d50b-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="3d50b-131">ลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3d50b-131">Sales tax receivable</span></span>   | <span data-ttu-id="3d50b-132">บัญชีหลักสำหรับภาษีขาเข้าที่ได้รับจากหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="3d50b-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="3d50b-133">ค่าใช้จ่ายภาษีนำเข้า</span><span class="sxs-lookup"><span data-stu-id="3d50b-133">Use tax expense</span></span>        | <span data-ttu-id="3d50b-134">บัญชีหลักที่ใช้ลงรายการบัญชีภาษีการใช้ที่หักลดได้ ซึ่งผู้ขนส่งไม่ต้องขอคืนหรือรายงานต่อหน่วยงานจัดเก็บภาษี โดยเป็นส่วนหนึ่งของภาษีสินค้าและบริการที่กลับรายการในสหภาพยุโรป (EU) (GST)/ภาษีขายที่สอดคล้อง (HST)</span><span class="sxs-lookup"><span data-stu-id="3d50b-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="3d50b-135">**ภาษีนำเข้า** ต้องถูกเลือกสำหรับรหัสภาษีขายในกลุ่มภาษีขายที่ถูกใช้ในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3d50b-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="3d50b-136">ฟิลด์นี้จะไม่พร้อมใช้งาน ถ้ามีการเลือก **ใช้กฎภาษีสำหรับภาษีขาย** ในหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="3d50b-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="3d50b-137">เจ้าหนี้ภาษีนำเข้า</span><span class="sxs-lookup"><span data-stu-id="3d50b-137">Use tax payable</span></span>        | <span data-ttu-id="3d50b-138">บัญชีหลักที่ใช้ลงรายการบัญชีภาษีการใช้ขาเข้าที่เป็นเจ้าหนี้หน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="3d50b-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="3d50b-139">บัญชีการจ่ายเงิน</span><span class="sxs-lookup"><span data-stu-id="3d50b-139">Settlement account</span></span>     | <span data-ttu-id="3d50b-140">บัญชีหลักที่ใช้ในการลงรายการบัญชีของยอดดุลสุทธิของบัญชีแยกประเภทที่ระบุในฟิลด์ **เจ้าหนี้ภาษีนำเข้า** และ **ลูกหนี้ภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="3d50b-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="3d50b-141">ส่วนลดเงินสดของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="3d50b-141">Vendor cash discount</span></span>   | <span data-ttu-id="3d50b-142">บัญชีหลักที่ใช้ลงรายการบัญชีส่วนลดเงินสดสำหรับรหัสภาษีขายที่เชื่อมโยงกับกลุ่มการลงรายการบัญชีแยกประเภทนี้</span><span class="sxs-lookup"><span data-stu-id="3d50b-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="3d50b-143">ส่วนลดเงินสดสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3d50b-143">Customer case discount</span></span> | <span data-ttu-id="3d50b-144">บัญชีหลักที่ใช้ลงรายการบัญชีส่วนลดเงินสดสำหรับรหัสภาษีขายที่เชื่อมโยงกับกลุ่มการลงรายการบัญชีแยกประเภทนี้</span><span class="sxs-lookup"><span data-stu-id="3d50b-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="3d50b-145">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่ากลุ่มการลงรายการบัญชีแยกประเภทสำหรับภาษีขาย](tasks/set-up-ledger-posting-groups-sales-tax.md)</span><span class="sxs-lookup"><span data-stu-id="3d50b-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="3d50b-146">ดีบักในรหัสเพื่อตรวจสอบมิติบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="3d50b-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="3d50b-147">ในรหัส บัญชีการลงรายการบัญชีจะขึ้นอยู่กับมิติบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="3d50b-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="3d50b-148">มิติบัญชีแยกประเภทจะบันทึกรหัสเรกคอร์ดของบัญชีในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3d50b-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="3d50b-149">สำหรับใบสั่งขาย ให้เพิ่มจุดสั่งหยุดที่วิธีการ **Tax::saveAndPost()** และ **Tax::post()**</span><span class="sxs-lookup"><span data-stu-id="3d50b-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="3d50b-150">ให้ความสำคัญกับค่าของ **\_ledgerDimension**</span><span class="sxs-lookup"><span data-stu-id="3d50b-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="3d50b-151">[![ตัวอย่างรหัสใบสั่งขายที่มีจุดสั่งหยุด](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="3d50b-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="3d50b-152">ในใบสั่งซื้อ ให้เพิ่มจุดสั่งหยุดที่วิธีการ **TaxPost::saveAndPost()** และ **TaxPost::postToTaxTrans()**</span><span class="sxs-lookup"><span data-stu-id="3d50b-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="3d50b-153">ให้ความสำคัญกับค่าของ **\_ledgerDimension**</span><span class="sxs-lookup"><span data-stu-id="3d50b-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="3d50b-154">[![ตัวอย่างรหัสใบสั่งซื้อที่มีจุดสั่งหยุด](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="3d50b-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="3d50b-155">รันการสอบถาม SQL ต่อไปนี้เพื่อค้นหาค่าที่แสดงของบัญชีในฐานข้อมูล ตามรหัสเรกคอร์ดที่บันทึกโดยมิติบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="3d50b-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="3d50b-156">[![แสดงค่าของรหัสเรกคอร์ด](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="3d50b-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="3d50b-157">ตรวจสอบ callstack เพื่อดูว่า **_ledgerDimension** ถูกมอบหมายจากที่ใด</span><span class="sxs-lookup"><span data-stu-id="3d50b-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="3d50b-158">โดยปกติแล้ว ค่านี้จะมาจาก **TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="3d50b-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="3d50b-159">ในกรณีนี้ คุณควรเพิ่มจุดสั่งหยุดที่ **TmpTaxWorkTrans::insert()** และ **TmpTaxWorkTrans::update()** เพื่อค้นหาสถานที่ที่มอบหมายค่า</span><span class="sxs-lookup"><span data-stu-id="3d50b-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="3d50b-160">ระบุว่ามีการเลือกเองอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3d50b-160">Determine whether customization exists</span></span>

<span data-ttu-id="3d50b-161">หากคุณได้เสร็จสิ้นขั้นตอนในส่วนก่อนหน้านี้แต่ไม่พบปัญหา ให้ระบุว่ามีการเลือกเองอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3d50b-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="3d50b-162">ถ้าไม่มีการเลือกเองอยู่ ให้สร้างคำขอบริการของ Microsoft เพื่อขอความช่วยเหลือเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3d50b-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
