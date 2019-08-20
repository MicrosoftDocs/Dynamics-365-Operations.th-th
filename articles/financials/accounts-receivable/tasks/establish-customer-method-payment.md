---
title: จัดทำวิธีการชำระเงินของลูกค้า
description: 'สร้างวิธีการชำระเงินสำหรับลูกค้าการชำระเงินของลูกค้า '
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 477f1ff72fd8012c3403d22aa128d97e45d5559f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842916"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="1656d-103">จัดทำวิธีการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="1656d-103">Establish customer method of payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1656d-104">สร้างวิธีการชำระเงินสำหรับลูกค้าการชำระเงินของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="1656d-104">Create a method of payment for customer payments.</span></span> <span data-ttu-id="1656d-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="1656d-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1656d-106">ไปที่บัญชีลูกหนี้ > การตั้งค่าการชำระเงิน > วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="1656d-106">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="1656d-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="1656d-107">Click New.</span></span>
3. <span data-ttu-id="1656d-108">ในฟิลด์วิธีการชำระเงิน ป้อน ID สำหรับวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="1656d-108">In the Method of payment field, enter an ID for the method of payment.</span></span>
    * <span data-ttu-id="1656d-109">วิธีการชำระเงิน ID จะปรากฏบนใบแจ้งหนี้และการชำระเงิน ดังนั้นให้อธิบายให้เข้าใจถึงชนิดการชำระเงินที่จะถูกบันทึกและสำหรับบัญชีธนาคารใด</span><span class="sxs-lookup"><span data-stu-id="1656d-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="1656d-110">ในฟิลด์คำอธิบาย ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1656d-110">In the Description field, enter a description.</span></span>
5. <span data-ttu-id="1656d-111">เลือกสถานะการชำระเงินที่ต้องใช้สำหรับการชำระเงินที่จะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="1656d-111">Select what payment status is required in order for payments to be posted.</span></span>
    * <span data-ttu-id="1656d-112">เมื่อมีการสร้างการชำระเงินของลูกค้า จึงสามารถลงรายการบัญชีได้เมื่อสถานะการชำระเงินตรงกับสถานะการชำระเงินที่คุณกำหนดที่นี่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1656d-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="1656d-113">เลือกว่าจะสร้างการชำระเงินของลูกค้าสำหรับใบแจ้งหนี้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="1656d-113">Select how customers payments should be created for invoices.</span></span>
    * <span data-ttu-id="1656d-114">ตัวเลือกนี้จะใช้เฉพาะเมื่อมีการเรียกใช้ข้อเสนอการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="1656d-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="1656d-115">ไม่สามารถใช้ข้อเสนอการชำระเงินสำหรับการชำระเงินของลูกค้าเมื่อมีการทำเดบิตโดยตรงและมีการดึงเงินของลูกค้าจากบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="1656d-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="1656d-116">เลือกชนิดของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="1656d-116">Select the type of payment.</span></span>
    * <span data-ttu-id="1656d-117">ชนิดการชำระเงินจะช่วยระบุว่าการตรวจสอบบางอย่างจะเกิดขึ้นหรือไม่ในการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="1656d-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="1656d-118">เลือกชนิดของบัญชีชำระเงินที่จะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="1656d-118">Select what account type payments will post to.</span></span>
    * <span data-ttu-id="1656d-119">โดยทั่วไป ธนาคารจะถูกเลือกสำหรับตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="1656d-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="1656d-120">เลือกบัญชีธนาคารที่การชำระเงินนี้จะถูกบันทึก</span><span class="sxs-lookup"><span data-stu-id="1656d-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="1656d-121">ป้อนชนิดของธุรกรรมธนาคารเพื่อระบุชนิดของการชำระเงินที่ใช้โดยธนาคารของคุณ</span><span class="sxs-lookup"><span data-stu-id="1656d-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span>
    * <span data-ttu-id="1656d-122">ชนิดของธุรกรรมธนาคารใช้ในระหว่างกระบวนการกระทบยอดธนาคารและช่วยทำให้กระทบยอดง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="1656d-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="1656d-123">เลือกว่าการชำระเงินนี้เป็นการลงรายการบัญชีชั่วคราวที่บัญชีระหว่างกาลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1656d-123">Select whether this payment will temporarily post to a bridging account.</span></span>
    * <span data-ttu-id="1656d-124">ถ้าหากคุณต้องการจะใช้อัตราเงินเฟ้อเพื่อชำระหนี้กับทางธนาคารให้ใช้ฟังก์ชันบัญชีระหว่างกาล </span><span class="sxs-lookup"><span data-stu-id="1656d-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="1656d-125">โดยการชำระเงินจะส่งรายการบัญชีชั่วคราวไปที่บัญชีแยกประเภทจนกว่าหนี้สินจะหมด เมื่อถึงตอนนั้นการชำระเงินจะย้ายไปที่บัญชีธนาคารที่คุณกำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="1656d-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="1656d-126">ป้อนบัญชีหลักที่ใช้สำหรับการลงรายการบัญชีระหว่างกาล</span><span class="sxs-lookup"><span data-stu-id="1656d-126">Enter the main account used for the bridging posting.</span></span>
    * <span data-ttu-id="1656d-127">นี่คือบัญชีหลัก ที่การชำระเงินจะถูกส่งมาที่นี้ชั่วคราว เมื่อใช้บัญชีระหว่างกาล</span><span class="sxs-lookup"><span data-stu-id="1656d-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="1656d-128">ใช้แท็บรูปแบบไฟล์เพื่อกำหนดการตั้งค่าสำหรับการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1656d-128">Use the File format tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="1656d-129">ใช้แท็บการควบคุมการชำระเงินเพื่อกำหนดฟิลด์ที่เป็นข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="1656d-129">Use the Payment control tab to define fields that are mandatory.</span></span>
    * <span data-ttu-id="1656d-130">ตัวอย่างเช่น ถ้าคุณต้องการชำระเงินทั้งหมดด้วยวิธีการชำระเงินแบบฝาก คุณสามารถเลือกตัวเลือกนั้นบนแท็บนี้</span><span class="sxs-lookup"><span data-stu-id="1656d-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="1656d-131">ใช้แท็บแอททริบิวต์ของการชำระเงินเพื่อกำหนดแอททริบิวต์ของการชำระเงินที่คุณต้องการใช้สำหรับวิธีการชำระเงินนี้</span><span class="sxs-lookup"><span data-stu-id="1656d-131">Use the Payment atrributes tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="1656d-132">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="1656d-132">Click Save.</span></span>

