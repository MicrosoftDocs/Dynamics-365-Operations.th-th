---
title: สร้างข้อตกลงการหักบัญชีเงินฝากอัตโนมัติสำหรับลูกค้า
description: คำแนะนำของงานนี้แสดงวิธีการสร้างข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ และใช้ในใบแจ้งหนี้
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc3052fdfc6e3dcf2826b3069f6d644201a70c3c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "346904"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="6a5bf-103">สร้างข้อตกลงการหักบัญชีเงินฝากอัตโนมัติสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6a5bf-104">คำแนะนำของงานนี้แสดงวิธีการสร้างข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ และใช้ในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6a5bf-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="6a5bf-105">สร้างบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="6a5bf-105">Create a bank account</span></span>
1. <span data-ttu-id="6a5bf-106">ไปที่บัญชีลูกหนี้ > ลูกค้า > ลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6a5bf-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="6a5bf-107">ตัวอย่างเช่น เลือก สหรัฐอเมริกา-001</span><span class="sxs-lookup"><span data-stu-id="6a5bf-107">For example, select US-001</span></span>
3. <span data-ttu-id="6a5bf-108">ในบานหน้าต่างการดำเนินการ คลิก ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="6a5bf-109">คลิก บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="6a5bf-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="6a5bf-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6a5bf-110">Click New.</span></span>
6. <span data-ttu-id="6a5bf-111">ในฟิลด์บัญชีธนาคาร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="6a5bf-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="6a5bf-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="6a5bf-113">ในฟิลด์ IBAN ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="6a5bf-114">ในฟิลด์สกุลเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="6a5bf-115">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6a5bf-115">Click Save.</span></span>
11. <span data-ttu-id="6a5bf-116">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-116">Close the page.</span></span>
12. <span data-ttu-id="6a5bf-117">ไปที่ การจัดการเงินสดและธนาคาร > บัญชีธนาคาร > บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="6a5bf-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="6a5bf-118">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6a5bf-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="6a5bf-119">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6a5bf-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="6a5bf-120">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="6a5bf-120">Click Edit.</span></span>
16. <span data-ttu-id="6a5bf-121">ขยายส่วนการระบุรหัสประจำตัวเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6a5bf-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="6a5bf-122">ในฟิลด์รหัสการหักบัญชีเงินฝากอัตโนมัติ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="6a5bf-123">ในฟิลด์ IBAN ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="6a5bf-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-124">Close the page.</span></span>
20. <span data-ttu-id="6a5bf-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="6a5bf-126">ระบุวิธีการชำระเงินแบบอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6a5bf-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="6a5bf-127">ไปที่บัญชีลูกหนี้ > การตั้งค่าการชำระเงิน > วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="6a5bf-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="6a5bf-128">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6a5bf-128">Click New.</span></span>
3. <span data-ttu-id="6a5bf-129">ในฟิลด์วิธีการชำระเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="6a5bf-130">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6a5bf-131">ชนิดการชำระเงินสำหรับวิธีข้อตกลงการหักบัญชีเงินฝากอัตโนมัติของการชำระเงินที่ต้องชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6a5bf-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="6a5bf-132">เลือก ใช่ ในฟิลด์ข้อตกลงที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="6a5bf-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="6a5bf-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="6a5bf-134">เพิ่มข้อตกลงการหักบัญชีเงินฝากอัตโนมัติไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="6a5bf-135">ไปที่บัญชีลูกหนี้ > ลูกค้า > ลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6a5bf-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="6a5bf-136">ตัวอย่างเช่น เลือก สหรัฐอเมริกา-001</span><span class="sxs-lookup"><span data-stu-id="6a5bf-136">For example, select US-001</span></span>
3. <span data-ttu-id="6a5bf-137">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="6a5bf-137">Click Edit.</span></span>
4. <span data-ttu-id="6a5bf-138">ขยายส่วนค่าเริ่มต้นของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="6a5bf-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="6a5bf-139">ในฟิลด์วิธีการชำระเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6a5bf-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="6a5bf-140">ขยายส่วนค่าเริ่มต้นของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="6a5bf-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="6a5bf-141">ขยายส่วนข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6a5bf-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="6a5bf-142">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6a5bf-142">Click Add.</span></span>
9. <span data-ttu-id="6a5bf-143">ในฟิลด์บัญชีธนาคาร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6a5bf-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="6a5bf-144">ในฟิลด์บัญชีธนาคารของเจ้าหนี้ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="6a5bf-145">ป้อนหมายเลขของการชำระเงินที่คุณคาดว่าจะดำเนินการสำหรับข้อตกลงนี้</span><span class="sxs-lookup"><span data-stu-id="6a5bf-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="6a5bf-146">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6a5bf-146">Click OK.</span></span>
13. <span data-ttu-id="6a5bf-147">คลิก พิมพ์</span><span class="sxs-lookup"><span data-stu-id="6a5bf-147">Click Print.</span></span>
14. <span data-ttu-id="6a5bf-148">คลิก รายงานข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="6a5bf-148">Click Mandate report.</span></span>
15. <span data-ttu-id="6a5bf-149">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-149">Close the page.</span></span>
16. <span data-ttu-id="6a5bf-150">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="6a5bf-150">Click Edit.</span></span>
17. <span data-ttu-id="6a5bf-151">ในฟิลด์วันที่ที่เซ็นรับรอง ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6a5bf-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="6a5bf-152">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="6a5bf-152">Click Yes.</span></span>
19. <span data-ttu-id="6a5bf-153">ป้อนสถานที่ที่ลงนามข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="6a5bf-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="6a5bf-154">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6a5bf-154">Click OK.</span></span>
21. <span data-ttu-id="6a5bf-155">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6a5bf-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="6a5bf-156">สร้างใบแจ้งหนี้ข้อความอิสระที่มีข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="6a5bf-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="6a5bf-157">ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ข้อความอิสระทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6a5bf-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="6a5bf-158">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6a5bf-158">Click New.</span></span>
3. <span data-ttu-id="6a5bf-159">เลือกลูกค้าที่คุณได้เพิ่มข้อตกลงไว้</span><span class="sxs-lookup"><span data-stu-id="6a5bf-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="6a5bf-160">ในฟิลด์หัสข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6a5bf-160">In the Direct debit mandate ID field, enter or select a value.</span></span>

