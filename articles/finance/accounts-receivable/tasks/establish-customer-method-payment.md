---
title: จัดทำวิธีการชำระเงินของลูกค้า
description: หัวข้อนี้จะอธิบายเกี่ยวกับวิธีการสร้างวิธีการชำระเงินสำหรับการชำระเงินของลูกค้า
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
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
ms.openlocfilehash: 22680a3033c1518735eb9edb4c6f22f310509aba
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188820"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="f39eb-103">จัดทำวิธีการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="f39eb-103">Establish customer method of payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f39eb-104">หัวข้อนี้จะอธิบายเกี่ยวกับวิธีการสร้างวิธีการชำระเงินสำหรับการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="f39eb-104">This topic explains how to create a method of payment for customer payments.</span></span> <span data-ttu-id="f39eb-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="f39eb-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="f39eb-106">ใน บานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีลูกหนี้ > การตั้งค่าการชำระเงิน > วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="f39eb-106">In the navigation pane, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="f39eb-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f39eb-107">Select **New**.</span></span>
3. <span data-ttu-id="f39eb-108">ในฟิลด์ **วิธีการชำระเงิน** ป้อน ID สำหรับวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f39eb-108">In the **Method of payment** field, enter an ID for the method of payment.</span></span> <span data-ttu-id="f39eb-109">วิธีการชำระเงิน ID จะปรากฏบนใบแจ้งหนี้และการชำระเงิน ดังนั้นให้อธิบายให้เข้าใจถึงชนิดการชำระเงินที่จะถูกบันทึกและสำหรับบัญชีธนาคารใด</span><span class="sxs-lookup"><span data-stu-id="f39eb-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="f39eb-110">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f39eb-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f39eb-111">เลือกสถานะการชำระเงินที่ต้องใช้สำหรับการชำระเงินที่จะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="f39eb-111">Select what payment status is required in order for payments to be posted.</span></span> <span data-ttu-id="f39eb-112">เมื่อมีการสร้างการชำระเงินของลูกค้า จึงสามารถลงรายการบัญชีได้เมื่อสถานะการชำระเงินตรงกับสถานะการชำระเงินที่คุณกำหนดที่นี่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f39eb-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="f39eb-113">เลือกว่าจะสร้างการชำระเงินของลูกค้าสำหรับใบแจ้งหนี้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="f39eb-113">Select how customers payments should be created for invoices.</span></span> <span data-ttu-id="f39eb-114">ตัวเลือกนี้จะใช้เฉพาะเมื่อมีการเรียกใช้ข้อเสนอการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="f39eb-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="f39eb-115">ไม่สามารถใช้ข้อเสนอการชำระเงินสำหรับการชำระเงินของลูกค้าเมื่อมีการทำเดบิตโดยตรงและมีการดึงเงินของลูกค้าจากบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="f39eb-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="f39eb-116">เลือกชนิดของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f39eb-116">Select the type of payment.</span></span> <span data-ttu-id="f39eb-117">ชนิดการชำระเงินจะช่วยระบุว่าการตรวจสอบบางอย่างจะเกิดขึ้นหรือไม่ในการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f39eb-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="f39eb-118">เลือกชนิดของบัญชีชำระเงินที่จะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="f39eb-118">Select what account type payments will post to.</span></span> <span data-ttu-id="f39eb-119">โดยทั่วไป ธนาคารจะถูกเลือกสำหรับตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="f39eb-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="f39eb-120">เลือกบัญชีธนาคารที่การชำระเงินนี้จะถูกบันทึก</span><span class="sxs-lookup"><span data-stu-id="f39eb-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="f39eb-121">ป้อนชนิดของธุรกรรมธนาคารเพื่อระบุชนิดของการชำระเงินที่ใช้โดยธนาคารของคุณ</span><span class="sxs-lookup"><span data-stu-id="f39eb-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span> <span data-ttu-id="f39eb-122">ชนิดของธุรกรรมธนาคารใช้ในระหว่างกระบวนการกระทบยอดธนาคารและช่วยทำให้กระทบยอดง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="f39eb-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="f39eb-123">เลือกว่าการชำระเงินนี้เป็นการลงรายการบัญชีชั่วคราวที่บัญชีระหว่างกาลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f39eb-123">Select whether this payment will temporarily post to a bridging account.</span></span> <span data-ttu-id="f39eb-124">ถ้าหากคุณต้องการจะใช้อัตราเงินเฟ้อเพื่อชำระหนี้กับทางธนาคารให้ใช้ฟังก์ชันบัญชีระหว่างกาล </span><span class="sxs-lookup"><span data-stu-id="f39eb-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="f39eb-125">โดยการชำระเงินจะส่งรายการบัญชีชั่วคราวไปที่บัญชีแยกประเภทจนกว่าหนี้สินจะหมด เมื่อถึงตอนนั้นการชำระเงินจะย้ายไปที่บัญชีธนาคารที่คุณกำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="f39eb-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="f39eb-126">ป้อนบัญชีหลักที่ใช้สำหรับการลงรายการบัญชีระหว่างกาล</span><span class="sxs-lookup"><span data-stu-id="f39eb-126">Enter the main account used for the bridging posting.</span></span> <span data-ttu-id="f39eb-127">นี่คือบัญชีหลัก ที่การชำระเงินจะถูกส่งมาที่นี้ชั่วคราว เมื่อใช้บัญชีระหว่างกาล</span><span class="sxs-lookup"><span data-stu-id="f39eb-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="f39eb-128">ใช้แท็บ **รูปแบบไฟล์** เพื่อกำหนดการตั้งค่าสำหรับการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f39eb-128">Use the **File format** tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="f39eb-129">ใช้แท็บ **การควบคุมการชำระเงิน** เพื่อกำหนดฟิลด์ที่เป็นข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="f39eb-129">Use the **Payment control** tab to define fields that are mandatory.</span></span> <span data-ttu-id="f39eb-130">ตัวอย่างเช่น ถ้าคุณต้องการชำระเงินทั้งหมดด้วยวิธีการชำระเงินแบบฝาก คุณสามารถเลือกตัวเลือกนั้นบนแท็บนี้</span><span class="sxs-lookup"><span data-stu-id="f39eb-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="f39eb-131">ใช้แท็บ **แอททริบิวต์ของการชำระเงิน** เพื่อกำหนดแอททริบิวต์ของการชำระเงินที่คุณต้องการใช้สำหรับวิธีการชำระเงินนี้</span><span class="sxs-lookup"><span data-stu-id="f39eb-131">Use the **Payment atrributes** tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="f39eb-132">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f39eb-132">Select **Save**.</span></span>

