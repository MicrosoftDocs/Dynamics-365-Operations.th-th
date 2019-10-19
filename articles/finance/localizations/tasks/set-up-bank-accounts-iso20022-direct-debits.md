---
title: ตั้งค่าลูกค้าและบัญชีธนาคารของลูกค้าสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022
description: 'งานนี้จะช่วยคุณในการตั้งค่าบัญชีธนาคารของลูกค้าและข้อตกลงการหักบัญชีเงินฝากอัตโนมัติของลูกค้าที่จำเป็นในการสร้างไฟล์การชำระเงินของลูกค้า เช่น การหักบัญชีเงินฝากอัตโนมัติ ISO20022 '
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82a8a3eff1f882d0d9b3d4943e352a8f3d1a6ae4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185738"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="51fab-103">ตั้งค่าลูกค้าและบัญชีธนาคารของลูกค้าสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022</span><span class="sxs-lookup"><span data-stu-id="51fab-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51fab-104">งานนี้จะช่วยคุณในการตั้งค่าบัญชีธนาคารของลูกค้าและข้อตกลงการหักบัญชีเงินฝากอัตโนมัติของลูกค้าที่จำเป็นในการสร้างไฟล์การชำระเงินของลูกค้า เช่น การหักบัญชีเงินฝากอัตโนมัติ ISO20022 </span><span class="sxs-lookup"><span data-stu-id="51fab-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="51fab-105">ทั้งนี้ขึ้นอยู่กับรูปแบบการชำระเงินของลูกค้าที่ตั้งค่าไว้ อาจจำเป็นต้องมีรายละเอียดเพิ่มเติมซึ่งไม่ครอบคลุมอยู่ในกระบวนงานนี้สำหรับลูกค้าหรือบัญชีธนาคารของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="51fab-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="51fab-106">งานนี้ถูกสร้างขึ้นโดยใช้บริษัทข้อมูลสาธิต DEMF ที่มีที่อยู่หลักของนิติบุคคลในเยอรมนี</span><span class="sxs-lookup"><span data-stu-id="51fab-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="51fab-107">นี่คือกระบวนงานที่สี่จากกระบวนงานห้ารายการที่แสดงให้เห็นถึงขั้นตอนการชำระเงินของลูกค้าโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="51fab-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="51fab-108">ตั้งค่าบัญชีธนาคารลูกค้า</span><span class="sxs-lookup"><span data-stu-id="51fab-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="51fab-109">ไปที่บัญชีลูกหนี้ > ลูกค้า > ลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="51fab-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="51fab-110">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="51fab-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="51fab-111">เช่น กรองข้อมูลในฟิลด์บัญชี ด้วยค่า 'DE-010'</span><span class="sxs-lookup"><span data-stu-id="51fab-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="51fab-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="51fab-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="51fab-113">ในบานหน้าต่างการดำเนินการ คลิก ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="51fab-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="51fab-114">คลิก บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="51fab-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="51fab-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="51fab-115">Click New.</span></span>
7. <span data-ttu-id="51fab-116">ในฟิลด์บัญชีธนาคาร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="51fab-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="51fab-117">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="51fab-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="51fab-118">ตัวอย่างเช่น ป้อน 'ธนาคาร EUR'</span><span class="sxs-lookup"><span data-stu-id="51fab-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="51fab-119">ในฟิลด์กลุ่มธนาคาร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="51fab-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="51fab-120">ในฟิลด์ IBAN ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="51fab-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="51fab-121">ตัวอย่างเช่น ป้อน 'DE36200400000628808808'</span><span class="sxs-lookup"><span data-stu-id="51fab-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="51fab-122">ในฟิลด์รหัส SWIFT ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="51fab-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="51fab-123">ตัวอย่างเช่น: พิมพ์ 'COBADEFFXXX'</span><span class="sxs-lookup"><span data-stu-id="51fab-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="51fab-124">โปรดทราบว่าไม่จำเป็นต้องใช้ SWIFT \ BIC สำหรับรูปแบบการชำระเงินหลายรายการ อย่างไรก็ตาม ขอแนะนำให้ลงทะเบียนสำหรับบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="51fab-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="51fab-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="51fab-125">Click Save.</span></span>
13. <span data-ttu-id="51fab-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="51fab-126">Close the page.</span></span>
14. <span data-ttu-id="51fab-127">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="51fab-127">Click Edit.</span></span>
15. <span data-ttu-id="51fab-128">ขยายส่วนค่าเริ่มต้นของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="51fab-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="51fab-129">ในฟิลด์บัญชีธนาคาร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="51fab-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="51fab-130">เพิ่มข้อบังคับการหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="51fab-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="51fab-131">ขยายส่วนข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="51fab-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="51fab-132">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="51fab-132">Click Add.</span></span>
3. <span data-ttu-id="51fab-133">ในฟิลด์บัญชีธนาคารของเจ้าหนี้ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="51fab-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="51fab-134">ตัวอย่างเช่น เลือก DEMF OPER</span><span class="sxs-lookup"><span data-stu-id="51fab-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="51fab-135">ในฟิลด์วันที่ที่เซ็นรับรอง ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="51fab-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="51fab-136">คลิก ใช่ เพื่อยืนยันการปรับปรุงวันที่</span><span class="sxs-lookup"><span data-stu-id="51fab-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="51fab-137">ในฟิลด์สถานที่ที่เซ็นรับรอง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="51fab-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="51fab-138">ในฟิลด์การชำระเงินของตัวเลขที่คาดการณ์ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="51fab-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="51fab-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="51fab-139">Click OK.</span></span>
9. <span data-ttu-id="51fab-140">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="51fab-140">Click Save.</span></span>

