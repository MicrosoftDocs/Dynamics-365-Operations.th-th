--- 
title: "จัดทำค่าธรรมเนียมการชำระเงินของลูกค้า"
description: "สร้างค่าธรรมเนียมในการชำระเงินสำหรับการชำระเงินของลูกค้า "
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 3be8db49bab80fa8765b685d73d54a42975870c3
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="3b6f5-103">จัดทำค่าธรรมเนียมการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3b6f5-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3b6f5-104">สร้างค่าธรรมเนียมในการชำระเงินสำหรับการชำระเงินของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="3b6f5-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="3b6f5-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="3b6f5-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="3b6f5-106">ไปที่บัญชีลูกหนี้ > การตั้งค่าการชำระเงิน > ค่าธรรมเนียมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="3b6f5-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="3b6f5-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3b6f5-107">Click New.</span></span>
3. <span data-ttu-id="3b6f5-108">ในฟิลด์รหัสค่าธรรมเนียม ป้อนรหัสค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="3b6f5-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="3b6f5-109">แสดงรหัสค่าธรรมเนียมในสมุดรายวันการชำระเงิน ดังนั้นให้อธิบายให้เข้าใจถึงค่าธรรมเนียมที่ถูกประเมิน</span><span class="sxs-lookup"><span data-stu-id="3b6f5-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="3b6f5-110">ในฟิลด์ชื่อ ป้อนชื่อค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="3b6f5-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="3b6f5-111">ในฟิลด์คำอธิบายค่าธรรมเนียม ป้อนคำอธิบายของค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="3b6f5-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="3b6f5-112">เลือกว่าจะเรียกเก็บค่าธรรมเนียมที่ลูกค้าหรือบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="3b6f5-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="3b6f5-113">ถ้าลูกค้าประเมินค่าธรรมเนียม ให้เลือกลูกค้า </span><span class="sxs-lookup"><span data-stu-id="3b6f5-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="3b6f5-114">หากค่าธรรมเนียมจะถูกประเมินเป็นค่าใช้จ่ายขององค์กรของคุณ ให้เลือกบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="3b6f5-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="3b6f5-115">สำหรับงานนี้เลือกลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3b6f5-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="3b6f5-116">เลือกชนิดของสมุดรายวันที่สามารถใช้ค่าธรรมเนียมการชำระเงินนี้</span><span class="sxs-lookup"><span data-stu-id="3b6f5-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="3b6f5-117">ถ้าค่าธรรมเนียมเหล่านี้จะใช้สำหรับการชำระเงินของลูกค้า ชนิดสมุดรายวันจะมีแนวโน้มเป็นการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3b6f5-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="3b6f5-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3b6f5-118">Click Save.</span></span>
9. <span data-ttu-id="3b6f5-119">คลิกการตั้งค่าค่าธรรมเนียมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="3b6f5-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="3b6f5-120">การตั้งค่าค่าธรรมเนียมการชำระเงินจะใช้เพื่อกำหนดเกณฑ์สำหรับเมื่อจะถูกประเมินค่า </span><span class="sxs-lookup"><span data-stu-id="3b6f5-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="3b6f5-121">ตัวอย่างเช่น คุณสามารถกำหนดว่าค่าธรรมเนียมจะถูกคำนวณถ้าบัญชีธนาคารเป็น USMF OPER และวิธีการชำระเงินเป็นเช็ค</span><span class="sxs-lookup"><span data-stu-id="3b6f5-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="3b6f5-122">เลือก ตาราง กลุ่ม หรือทั้งหมดเพื่อกำหนดบัญชีธนาคารที่จะถูกประเมินค่าธรรมเนียมนี้</span><span class="sxs-lookup"><span data-stu-id="3b6f5-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="3b6f5-123">ถ้าคุณเลือกทั้งหมด บัญชีธนาคารทั้งหมดจะถูกประเมินค่าธรรมเนียมนี้ </span><span class="sxs-lookup"><span data-stu-id="3b6f5-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="3b6f5-124">ถ้าคุณเลือกตาราง เฉพาะบัญชีธนาคารที่คุณเลือกจะถูกประเมินค่าธรรมเนียมนี้ </span><span class="sxs-lookup"><span data-stu-id="3b6f5-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="3b6f5-125">ถ้าคุณเลือกกลุ่ม เฉพาะบัญชีธนาคารในกลุ่มธนาคารที่เลือกจะถูกประเมินค่าธรรมเนียมนี้</span><span class="sxs-lookup"><span data-stu-id="3b6f5-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="3b6f5-126">เลือกกลุ่มธนาคารหรือบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3b6f5-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="3b6f5-127">ถ้าคุณเลือกตาราง การค้นหาจะแสดงบัญชีธนาคาร </span><span class="sxs-lookup"><span data-stu-id="3b6f5-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="3b6f5-128">ถ้าคุณเลือกกลุ่ม การค้นหาจะแสดงกลุ่มธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3b6f5-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="3b6f5-129">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3b6f5-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="3b6f5-130">เลือกวิธีการชำระเงินที่ค่าธรรมเนียมนี้จะถูกประเมิน</span><span class="sxs-lookup"><span data-stu-id="3b6f5-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="3b6f5-131">ตัวอย่างเช่น คุณอาจประเมินค่าธรรมเนียมให้กับลูกค้าของคุณถ้าพวกเขาส่งรายการชำระเงินเป็นเช็ค มากกว่าการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="3b6f5-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="3b6f5-132">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3b6f5-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="3b6f5-133">ถ้าเกี่ยวข้อง ป้อนสกุลเงินการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="3b6f5-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="3b6f5-134">สกุลเงินของการชำระเงินถูกใช้เป็นเกณฑ์เพิ่มเติมว่าค่าธรรมเนียมจะถูกประเมินหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="3b6f5-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="3b6f5-135">ตัวอย่างเช่น ธนาคารของคุณอาจเรียกเก็บค่าธรรมเนียมเพิ่มเติมสำหรับการชำระเงินในสกุลเงิน USD เนื่องจากโดยปกติพวกเขาจะดำเนินการในสกุลเงินยูโรเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3b6f5-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="3b6f5-136">เลือกว่าค่าธรรมเนียม จะเป็นเปอร์เซ็นต์ ยอดเงิน หรือช่วง</span><span class="sxs-lookup"><span data-stu-id="3b6f5-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="3b6f5-137">ป้อนเปอร์เซ็นต์หรือยอดเงินของค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="3b6f5-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="3b6f5-138">ถ้าฟิลด์เปอร์เซ็นต์/ยอดเงิน เป็นเปอร์เซ็นต์ ดังนั้นค่าที่ป้อนที่นี่จะเป็นเปอร์เซ็นต์ </span><span class="sxs-lookup"><span data-stu-id="3b6f5-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="3b6f5-139">ถ้าฟิลด์เปอร์เซ็นต์/ยอดเงิน เป็นยอดเงิน ค่าคุณป้อนที่นี่จะเป็นยอดเงิน </span><span class="sxs-lookup"><span data-stu-id="3b6f5-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="3b6f5-140">ถ้าฟิลด์เปอร์เซ็นต์/ยอดเงิน เป็นช่วง ใช้แท็บช่วงเพื่อกำหนดระดับ</span><span class="sxs-lookup"><span data-stu-id="3b6f5-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="3b6f5-141">ในฟิลด์สกุลเงินค่าธรรมเนียม เลือกสกุลเงินของค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="3b6f5-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="3b6f5-142">นี่คือสกุลเงินที่จะมีการสร้างค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="3b6f5-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="3b6f5-143">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3b6f5-143">Click Save.</span></span>


