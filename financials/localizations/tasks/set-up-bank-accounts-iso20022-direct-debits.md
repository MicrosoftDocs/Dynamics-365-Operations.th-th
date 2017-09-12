--- 
title: "ตั้งค่าลูกค้าและบัญชีธนาคารของลูกค้าสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022"
description: "งานนี้จะช่วยคุณในการตั้งค่าบัญชีธนาคารของลูกค้าและข้อตกลงการหักบัญชีเงินฝากอัตโนมัติของลูกค้าที่จำเป็นในการสร้างไฟล์การชำระเงินของลูกค้า เช่น การหักบัญชีเงินฝากอัตโนมัติ ISO20022 "
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 52970c54849e91c5052ad61ffc6458e646cbb262
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="57467-103">ตั้งค่าลูกค้าและบัญชีธนาคารของลูกค้าสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022</span><span class="sxs-lookup"><span data-stu-id="57467-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57467-104">งานนี้จะช่วยคุณในการตั้งค่าบัญชีธนาคารของลูกค้าและข้อตกลงการหักบัญชีเงินฝากอัตโนมัติของลูกค้าที่จำเป็นในการสร้างไฟล์การชำระเงินของลูกค้า เช่น การหักบัญชีเงินฝากอัตโนมัติ ISO20022 </span><span class="sxs-lookup"><span data-stu-id="57467-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="57467-105">ทั้งนี้ขึ้นอยู่กับรูปแบบการชำระเงินของลูกค้าที่ตั้งค่าไว้ อาจจำเป็นต้องมีรายละเอียดเพิ่มเติมซึ่งไม่ครอบคลุมอยู่ในกระบวนงานนี้สำหรับลูกค้าหรือบัญชีธนาคารของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="57467-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="57467-106">งานนี้ถูกสร้างขึ้นโดยใช้บริษัทข้อมูลสาธิต DEMF ที่มีที่อยู่หลักของนิติบุคคลในเยอรมนี</span><span class="sxs-lookup"><span data-stu-id="57467-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="57467-107">นี่คือกระบวนงานที่สี่จากกระบวนงานห้ารายการที่แสดงให้เห็นถึงขั้นตอนการชำระเงินของลูกค้าโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="57467-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="57467-108">ตั้งค่าบัญชีธนาคารลูกค้า</span><span class="sxs-lookup"><span data-stu-id="57467-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="57467-109">ไปที่บัญชีลูกหนี้ > ลูกค้า > ลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="57467-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="57467-110">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="57467-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="57467-111">เช่น กรองข้อมูลในฟิลด์บัญชี ด้วยค่า 'DE-010'</span><span class="sxs-lookup"><span data-stu-id="57467-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="57467-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="57467-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="57467-113">ในบานหน้าต่างการดำเนินการ คลิก ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="57467-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="57467-114">คลิก บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="57467-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="57467-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="57467-115">Click New.</span></span>
7. <span data-ttu-id="57467-116">ในฟิลด์บัญชีธนาคาร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="57467-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="57467-117">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="57467-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="57467-118">ตัวอย่างเช่น ป้อน 'ธนาคาร EUR'</span><span class="sxs-lookup"><span data-stu-id="57467-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="57467-119">ในฟิลด์กลุ่มธนาคาร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="57467-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="57467-120">ในฟิลด์ IBAN ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="57467-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="57467-121">ตัวอย่างเช่น ป้อน 'DE36200400000628808808'</span><span class="sxs-lookup"><span data-stu-id="57467-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="57467-122">ในฟิลด์รหัส SWIFT ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="57467-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="57467-123">ตัวอย่างเช่น: พิมพ์ 'COBADEFFXXX'</span><span class="sxs-lookup"><span data-stu-id="57467-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="57467-124">โปรดทราบว่าไม่จำเป็นต้องใช้ SWIFT \ BIC สำหรับรูปแบบการชำระเงินหลายรายการ อย่างไรก็ตาม ขอแนะนำให้ลงทะเบียนสำหรับบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="57467-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="57467-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="57467-125">Click Save.</span></span>
13. <span data-ttu-id="57467-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="57467-126">Close the page.</span></span>
14. <span data-ttu-id="57467-127">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="57467-127">Click Edit.</span></span>
15. <span data-ttu-id="57467-128">ขยายส่วนค่าเริ่มต้นของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="57467-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="57467-129">ในฟิลด์บัญชีธนาคาร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="57467-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="57467-130">เพิ่มข้อบังคับการหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="57467-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="57467-131">ขยายส่วนข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="57467-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="57467-132">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="57467-132">Click Add.</span></span>
3. <span data-ttu-id="57467-133">ในฟิลด์บัญชีธนาคารของเจ้าหนี้ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="57467-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="57467-134">ตัวอย่างเช่น เลือก DEMF OPER</span><span class="sxs-lookup"><span data-stu-id="57467-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="57467-135">ในฟิลด์วันที่ที่เซ็นรับรอง ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="57467-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="57467-136">คลิก ใช่ เพื่อยืนยันการปรับปรุงวันที่</span><span class="sxs-lookup"><span data-stu-id="57467-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="57467-137">ในฟิลด์สถานที่ที่เซ็นรับรอง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="57467-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="57467-138">ในฟิลด์การชำระเงินของตัวเลขที่คาดการณ์ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="57467-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="57467-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="57467-139">Click OK.</span></span>
9. <span data-ttu-id="57467-140">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="57467-140">Click Save.</span></span>


