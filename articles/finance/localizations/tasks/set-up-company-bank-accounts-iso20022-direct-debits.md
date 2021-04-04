---
title: ตั้งค่าบัญชีธนาคารของบริษัทสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022
description: 'งานนี้จะช่วยคุณในการตั้งค่าข้อมูลบัญชีธนาคารเฉพาะบริษัทที่จำเป็นสำหรับการสร้างไฟล์การชำระเงินของลูกค้า '
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8079dadd09f3e781bcfde21974882cdd59dec809
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256607"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="8fd2a-103">ตั้งค่าบัญชีธนาคารของบริษัทสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022</span><span class="sxs-lookup"><span data-stu-id="8fd2a-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8fd2a-104">งานนี้จะช่วยคุณในการตั้งค่าข้อมูลบัญชีธนาคารเฉพาะบริษัทที่จำเป็นสำหรับการสร้างไฟล์การชำระเงินของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="8fd2a-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="8fd2a-105">กระบวนงานนี้ใช้รูปแบบการหักบัญชีเงินฝากอัตโนมัติ ISO 20022 เป็นตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8fd2a-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="8fd2a-106">รูปแบบอื่นๆ อาจจำเป็นต้องมีการตั้งค่าข้อมูลเพิ่มเติม เช่น รหัสบริษัทหรือรหัสเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="8fd2a-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="8fd2a-107">งานนี้ถูกสร้างขึ้นโดยใช้บริษัทข้อมูลสาธิต DEMF</span><span class="sxs-lookup"><span data-stu-id="8fd2a-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="8fd2a-108">นี่คือกระบวนงานที่สองจากกระบวนงานห้ารายการที่แสดงให้เห็นถึงขั้นตอนการชำระเงินของลูกค้าโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="8fd2a-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="8fd2a-109">ตั้งค่ารหัส IBAN และ SWIFT</span><span class="sxs-lookup"><span data-stu-id="8fd2a-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="8fd2a-110">ไปที่การจัดการเงินสดและธนาคาร > บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="8fd2a-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="8fd2a-111">ใช้ตัวกรองด่วนเพื่อกรองฟิลด์บัญชีธนาคาร ด้วยค่า 'DEMF OPER'</span><span class="sxs-lookup"><span data-stu-id="8fd2a-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="8fd2a-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8fd2a-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8fd2a-113">ตัวอย่างเช่น คลิก 'DEMF OPER' เพื่อเปิดรายละเอียดบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="8fd2a-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="8fd2a-114">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="8fd2a-114">Click Edit.</span></span>
5. <span data-ttu-id="8fd2a-115">ขยายหรือยุบส่วนการระบุรหัสประจำตัวเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8fd2a-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="8fd2a-116">ในฟิลด์ IBAN ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8fd2a-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="8fd2a-117">ตัวอย่างเช่น ป้อน 'DE89370400440532013000'</span><span class="sxs-lookup"><span data-stu-id="8fd2a-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="8fd2a-118">ในฟิลด์รหัส SWIFT ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8fd2a-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="8fd2a-119">ตัวอย่างเช่น ป้อน 'DEUTDEFF' </span><span class="sxs-lookup"><span data-stu-id="8fd2a-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="8fd2a-120">โปรดทราบว่าไม่จำเป็นต้องใช้ SWIFT \ BIC สำหรับรูปแบบการชำระเงินหลายรายการ อย่างไรก็ตาม ขอแนะนำให้ลงทะเบียนสำหรับบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="8fd2a-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="8fd2a-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="8fd2a-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="8fd2a-122">ตั้งค่าบัญชีธนาคารสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="8fd2a-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="8fd2a-123">ไปที่การจัดการองค์กร > องค์กร > นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="8fd2a-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="8fd2a-124">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="8fd2a-124">Click Edit.</span></span>
3. <span data-ttu-id="8fd2a-125">ขยายหรือยุบส่วนของข้อมูลบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="8fd2a-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="8fd2a-126">ในฟิลด์บัญชีธนาคาร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8fd2a-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8fd2a-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8fd2a-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8fd2a-128">ตัวอย่างเช่น เลือกบัญชีธนาคาร "DEMF OPER"</span><span class="sxs-lookup"><span data-stu-id="8fd2a-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="8fd2a-129">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="8fd2a-129">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]