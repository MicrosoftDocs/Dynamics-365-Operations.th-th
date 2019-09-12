---
title: สร้างข้อตกลงการหักบัญชีเงินฝากอัตโนมัติสำหรับลูกค้า
description: คำแนะนำของงานนี้แสดงวิธีการสร้างข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ และใช้ในใบแจ้งหนี้
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ca5ff2290df2179004ca1cebd11f67fbb7a724e
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916380"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="6e326-103">สร้างข้อตกลงการหักบัญชีเงินฝากอัตโนมัติสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6e326-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e326-104">คำแนะนำของงานนี้แสดงวิธีการสร้างข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ และใช้ในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6e326-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="6e326-105">สร้างบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="6e326-105">Create a bank account</span></span>
1. <span data-ttu-id="6e326-106">ใน **บานหน้าต่างนำทาง** > **โมดูล > บัญชีลูกหนี้ > ลูกค้า > ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e326-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="6e326-107">ในรายการ เลือกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="6e326-107">In the list, select a record.</span></span> <span data-ttu-id="6e326-108">ตัวอย่างเช่น เลือก สหรัฐอเมริกา-001</span><span class="sxs-lookup"><span data-stu-id="6e326-108">For example, select US-001</span></span>
3. <span data-ttu-id="6e326-109">ในบานหน้าต่างการดำเนินการ คลิก **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="6e326-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="6e326-110">คลิก **บัญชีธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="6e326-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="6e326-111">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6e326-111">Click **New**.</span></span>
6. <span data-ttu-id="6e326-112">ในฟิลด์ **บัญชีธนาคาร** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6e326-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="6e326-113">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6e326-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="6e326-114">ในฟิลด์ **IBAN** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6e326-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="6e326-115">ในฟิลด์ **สกุลเงิน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6e326-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="6e326-116">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6e326-116">Click **Save**.</span></span>
11. <span data-ttu-id="6e326-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e326-117">Close the page.</span></span>
12. <span data-ttu-id="6e326-118">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การจัดการเงินสดและธนาคาร > บัญชีธนาคาร > บัญชีธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="6e326-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="6e326-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6e326-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="6e326-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6e326-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="6e326-121">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="6e326-121">Click **Edit**.</span></span>
16. <span data-ttu-id="6e326-122">ขยาย fastTab **การระบุรหัสประจำตัวเพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="6e326-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="6e326-123">ในฟิลด์ **รหัสการหักบัญชีเงินฝากอัตโนมัติ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6e326-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="6e326-124">ในฟิลด์ **IBAN** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6e326-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="6e326-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e326-125">Close the page.</span></span>
20. <span data-ttu-id="6e326-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e326-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="6e326-127">ระบุวิธีการชำระเงินแบบอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6e326-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="6e326-128">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > บัญชีลูกหนี้ > การตั้งค่าการชำระเงิน > วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="6e326-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="6e326-129">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6e326-129">Click **New**.</span></span>
3. <span data-ttu-id="6e326-130">ในฟิลด์ **วิธีการชำระเงิน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6e326-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="6e326-131">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6e326-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="6e326-132">ในฟิลด์ **ชนิดการชำระเงิน** ป้อน 'การชำระเงินทางอิเล็กทรอนิกส์'</span><span class="sxs-lookup"><span data-stu-id="6e326-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="6e326-133">ชนิดการชำระเงินสำหรับวิธีข้อตกลงการหักบัญชีเงินฝากอัตโนมัติของการชำระเงินที่ต้องชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6e326-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="6e326-134">เลือก ใช่ ในฟิลด์ **ต้องใช้ข้อตกลง**</span><span class="sxs-lookup"><span data-stu-id="6e326-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="6e326-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e326-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="6e326-136">เพิ่มข้อตกลงการหักบัญชีเงินฝากอัตโนมัติไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6e326-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="6e326-137">ใน **บานหน้าต่างนำทาง** > **โมดูล > บัญชีลูกหนี้ > ลูกค้า > ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e326-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="6e326-138">ในรายการ เลือกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="6e326-138">In the list, select a record.</span></span> <span data-ttu-id="6e326-139">ตัวอย่างเช่น เลือก สหรัฐอเมริกา-001</span><span class="sxs-lookup"><span data-stu-id="6e326-139">For example, select US-001</span></span>
3. <span data-ttu-id="6e326-140">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="6e326-140">Click **Edit**.</span></span>
4. <span data-ttu-id="6e326-141">ขยาย fastTab **ค่าเริ่มต้นของการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="6e326-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="6e326-142">ในฟิลด์ **วิธีการชำระเงิน** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6e326-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="6e326-143">ขยาย fastTab **ค่าเริ่มต้นของการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="6e326-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="6e326-144">ขยาย fastTab **ข้อบังคับการหักบัญชีเงินฝากอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="6e326-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="6e326-145">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="6e326-145">Click **Add**.</span></span>
9. <span data-ttu-id="6e326-146">ในฟิลด์ **บัญชีธนาคาร** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6e326-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="6e326-147">ในฟิลด์ **บัญชีธนาคารของเจ้าหนี้** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6e326-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="6e326-148">ในฟิลด์ **ความถี่ในการชำระเงิน** ป้อนหมายเลขของการชำระเงินที่คุณคาดว่าจะดำเนินการสำหรับข้อบังคับนี้</span><span class="sxs-lookup"><span data-stu-id="6e326-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="6e326-149">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6e326-149">Click **OK**.</span></span>
13. <span data-ttu-id="6e326-150">คลิก **พิมพ์**</span><span class="sxs-lookup"><span data-stu-id="6e326-150">Click **Print**.</span></span>
14. <span data-ttu-id="6e326-151">คลิก **รายงานข้อบังคับ**</span><span class="sxs-lookup"><span data-stu-id="6e326-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="6e326-152">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e326-152">Close the page.</span></span>
16. <span data-ttu-id="6e326-153">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="6e326-153">Click **Edit**.</span></span>
17. <span data-ttu-id="6e326-154">ในฟิลด์ **วันที่ที่เซ็นรับรอง** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6e326-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="6e326-155">คลิก **ใช่** </span><span class="sxs-lookup"><span data-stu-id="6e326-155">Click **Yes**.</span></span>
19. <span data-ttu-id="6e326-156">ป้อนสถานที่ที่ลงนามข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="6e326-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="6e326-157">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6e326-157">Click **OK**.</span></span>
21. <span data-ttu-id="6e326-158">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e326-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="6e326-159">สร้างใบแจ้งหนี้ข้อความอิสระที่มีข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="6e326-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="6e326-160">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ข้อความอิสระทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e326-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="6e326-161">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6e326-161">Click **New**.</span></span>
3. <span data-ttu-id="6e326-162">เลือกลูกค้าที่คุณได้เพิ่มข้อตกลงไว้</span><span class="sxs-lookup"><span data-stu-id="6e326-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="6e326-163">ในฟิลด์ **รหัสข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6e326-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>

