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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89c4a8d3cb504df97bad5679bf12b3cdb5931d95
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185715"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="80541-103">ตั้งค่าบัญชีธนาคารของบริษัทสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022</span><span class="sxs-lookup"><span data-stu-id="80541-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="80541-104">งานนี้จะช่วยคุณในการตั้งค่าข้อมูลบัญชีธนาคารเฉพาะบริษัทที่จำเป็นสำหรับการสร้างไฟล์การชำระเงินของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="80541-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="80541-105">กระบวนงานนี้ใช้รูปแบบการหักบัญชีเงินฝากอัตโนมัติ ISO 20022 เป็นตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="80541-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="80541-106">รูปแบบอื่นๆ อาจจำเป็นต้องมีการตั้งค่าข้อมูลเพิ่มเติม เช่น รหัสบริษัทหรือรหัสเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="80541-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="80541-107">งานนี้ถูกสร้างขึ้นโดยใช้บริษัทข้อมูลสาธิต DEMF</span><span class="sxs-lookup"><span data-stu-id="80541-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="80541-108">นี่คือกระบวนงานที่สองจากกระบวนงานห้ารายการที่แสดงให้เห็นถึงขั้นตอนการชำระเงินของลูกค้าโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="80541-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="80541-109">ตั้งค่ารหัส IBAN และ SWIFT</span><span class="sxs-lookup"><span data-stu-id="80541-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="80541-110">ไปที่การจัดการเงินสดและธนาคาร > บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="80541-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="80541-111">ใช้ตัวกรองด่วนเพื่อกรองฟิลด์บัญชีธนาคาร ด้วยค่า 'DEMF OPER'</span><span class="sxs-lookup"><span data-stu-id="80541-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="80541-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="80541-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="80541-113">ตัวอย่างเช่น คลิก 'DEMF OPER' เพื่อเปิดรายละเอียดบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="80541-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="80541-114">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="80541-114">Click Edit.</span></span>
5. <span data-ttu-id="80541-115">ขยายหรือยุบส่วนการระบุรหัสประจำตัวเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="80541-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="80541-116">ในฟิลด์ IBAN ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="80541-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="80541-117">ตัวอย่างเช่น ป้อน 'DE89370400440532013000'</span><span class="sxs-lookup"><span data-stu-id="80541-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="80541-118">ในฟิลด์รหัส SWIFT ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="80541-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="80541-119">ตัวอย่างเช่น ป้อน 'DEUTDEFF' </span><span class="sxs-lookup"><span data-stu-id="80541-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="80541-120">โปรดทราบว่าไม่จำเป็นต้องใช้ SWIFT \ BIC สำหรับรูปแบบการชำระเงินหลายรายการ อย่างไรก็ตาม ขอแนะนำให้ลงทะเบียนสำหรับบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="80541-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="80541-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="80541-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="80541-122">ตั้งค่าบัญชีธนาคารสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="80541-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="80541-123">ไปที่การจัดการองค์กร > องค์กร > นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="80541-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="80541-124">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="80541-124">Click Edit.</span></span>
3. <span data-ttu-id="80541-125">ขยายหรือยุบส่วนของข้อมูลบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="80541-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="80541-126">ในฟิลด์บัญชีธนาคาร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="80541-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="80541-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="80541-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="80541-128">ตัวอย่างเช่น เลือกบัญชีธนาคาร "DEMF OPER"</span><span class="sxs-lookup"><span data-stu-id="80541-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="80541-129">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="80541-129">Click Save.</span></span>

