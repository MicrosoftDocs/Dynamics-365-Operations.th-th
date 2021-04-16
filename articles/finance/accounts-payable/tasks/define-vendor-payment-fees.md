---
title: กำหนดค่าธรรมเนียมการชำระเงินให้แก่ผู้จัดจำหน่าย
description: 'ตั้งค่าค่าธรรมเนียมการชำระเงินให้แก่ผู้จัดจำหน่าย '
author: abruer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e0871e0889b078c08e4bcbd86bf749bcfe39463
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837283"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="c6766-103">กำหนดค่าธรรมเนียมการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c6766-103">Define vendor payment fees</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6766-104">ตั้งค่าค่าธรรมเนียมการชำระเงินให้แก่ผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="c6766-104">Set up vendor payment fees.</span></span> <span data-ttu-id="c6766-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="c6766-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c6766-106">ไปที่บัญชีเจ้าหนี้ > การตั้งค่าการชำระเงิน > ค่าธรรมเนียมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c6766-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="c6766-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c6766-107">Click New.</span></span>
3. <span data-ttu-id="c6766-108">ในฟิลด์รหัสค่าธรรมเนียม ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c6766-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="c6766-109">รหัสค่าธรรมเนียมควรอธิบายถึงเมื่อค่าธรรมเนียมนี้จะถูกใช้ เช่น "EFT_Fee"</span><span class="sxs-lookup"><span data-stu-id="c6766-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="c6766-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="c6766-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c6766-111">ในฟิลด์คำอธิบายค่าธรรมเนียม ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c6766-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="c6766-112">เพิ่มคำอธิบายเพื่อแสดงรายละเอียดเพิ่มเติมเมื่อมีประเมินค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="c6766-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="c6766-113">ในฟิลด์ค่าธรรมเนียม เลือกผู้จัดจำหน่ายหรือบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="c6766-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="c6766-114">บัญชีแยกประเภทถูกใช้เมื่อค่าธรรมเนียมจะถูกจ่ายไปยังองค์กรของคุณ </span><span class="sxs-lookup"><span data-stu-id="c6766-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="c6766-115">ผู้จัดจำหน่ายถูกใช้เมื่อค่าธรรมเนียมจะถูกประเมินไปยังผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c6766-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="c6766-116">ป้อนบัญชีหลักสำหรับที่ที่ค่าธรรมเนียมจะถูกจ่าย</span><span class="sxs-lookup"><span data-stu-id="c6766-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="c6766-117">ตัวเลือกนี้จะใช้ได้เฉพาะเมื่อมีการเลือกบัญชีแยกประเภทเป็นตัวเลือกค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="c6766-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="c6766-118">เลือกสมุดรายวันที่ค่าธรรมเนียมนี้สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="c6766-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="c6766-119">สำหรับค่าธรรมเนียมการชำระเงินของผู้จัดจำหน่าย คุณอาจเลือกสมุดรายวัน 'การเบิกจ่ายเงินให้แก่ผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="c6766-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="c6766-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c6766-120">Click Save.</span></span>
10. <span data-ttu-id="c6766-121">คลิกการตั้งค่าค่าธรรมเนียมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c6766-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="c6766-122">ดำเนินต่อกับการตั้งค่าค่าธรรมเนียมการชำระเงินเพื่อกำหนดว่าค่าธรรมเนียมควรเริ่มต้นที่สมุดรายวันที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="c6766-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="c6766-123">เลือกตาราง กลุ่ม หรือทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c6766-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="c6766-124">ตารางถูกใช้เพื่อเลือกบัญชีธนาคารหนึ่งๆ กลุ่มถูกใช้เพื่อเลือกกลุ่มธนาคาร และทั้งหมดจะใช้การตั้งค่าค่าธรรมเนียมสำหรับบัญชีธนาคารทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c6766-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="c6766-125">เลือกกลุ่มธนาคารหรือบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="c6766-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="c6766-126">การค้นหาจะแสดงกลุ่มธนาคาร ถ้าคุณเลือกกลุ่ม และการค้นหาจะแสดงบัญชีธนาคาร ถ้าคุณเลือกตาราง</span><span class="sxs-lookup"><span data-stu-id="c6766-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="c6766-127">เลือกวิธีการชำระเงินที่ค่าธรรมเนียมนี้จะถูกประเมิน</span><span class="sxs-lookup"><span data-stu-id="c6766-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="c6766-128">เลือกข้อมูลจำเพาะเกี่ยวกับการชำระเงินสำหรับวิธีการชำระเงินที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c6766-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="c6766-129">ข้อมูลจำเพาะเกี่ยวกับการชำระเงินถูกใช้กับการชำระเงินโดยวิธีการโอนเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c6766-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="c6766-130">เลือกว่าค่าธรรมเนียมจะเป็นเปอร์เซ็นต์ ยอดเงิน หรือช่วง</span><span class="sxs-lookup"><span data-stu-id="c6766-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="c6766-131">ป้อนเปอร์เซ็นต์ของยอดเงินของค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="c6766-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="c6766-132">ถ้าค่าธรรมเนียมเป็นเปอร์เซ็นต์ ป้อนเปอร์เซ็นต์ </span><span class="sxs-lookup"><span data-stu-id="c6766-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="c6766-133">ถ้าค่าธรรมเนียมเป็นยอดเงิน ป้อนยอดเงินของค่าธรรมเนียม </span><span class="sxs-lookup"><span data-stu-id="c6766-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="c6766-134">หากค่าธรรมเนียมเป็นช่วง ใช้แท็บช่วงเพื่อกำหนดค่าธรรมเนียมจัดระดับ</span><span class="sxs-lookup"><span data-stu-id="c6766-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="c6766-135">ในฟิลด์สกุลเงินของค่าธรรมเนียม เลือกสกุลเงินที่จะประเมินค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="c6766-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="c6766-136">สกุลเงินนี้ใช้สำหรับค่าธรรมเนียม </span><span class="sxs-lookup"><span data-stu-id="c6766-136">This currency is for the fee.</span></span> <span data-ttu-id="c6766-137">สกุลเงินการชำระเงินใช้เพื่อกำหนดว่าค่าธรรมเนียมจะถูกประเมินโดยอาศัยสกุลเงินของการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="c6766-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="c6766-138">ตัวอย่างเช่น ธนาคารของคุณอาจเรียกเก็บค่าธรรมเนียมเมื่อการชำระเงินเป็น EUR แต่การชำระเงินอื่นๆ ทั้งหมดจะไม่ถูกประเมิน</span><span class="sxs-lookup"><span data-stu-id="c6766-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="c6766-139">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c6766-139">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]