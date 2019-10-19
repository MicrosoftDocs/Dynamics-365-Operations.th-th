---
title: สร้างการชำระเงินสำหรับลูกค้าที่มีข้อบังคับการหักบัญชีเงินฝากอัตโนมัติ
description: 'กระบวนงานนี้แสดงวิธีการสร้างไฟล์การชำระเงินการหักบัญชีเงินฝากอัตโนมัติ ISO20022 สำหรับลูกค้าที่มีการตั้งค่าคอนฟิกการหักบัญชีเงินฝากอัตโนมัติและการชำระเงินใบแจ้งหนี้ '
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 129c5291a29994f91ef325aa9b9a3b54a0e958d6
ms.sourcegitcommit: 807dec193cd163c9f5d949e744cfde40f2eb24b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2468966"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="c67e3-103">สร้างการชำระเงินสำหรับลูกค้าที่มีข้อบังคับการหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c67e3-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c67e3-104">กระบวนงานนี้แสดงวิธีการสร้างไฟล์การชำระเงินการหักบัญชีเงินฝากอัตโนมัติ ISO20022 สำหรับลูกค้าที่มีการตั้งค่าคอนฟิกการหักบัญชีเงินฝากอัตโนมัติและการชำระเงินใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="c67e3-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="c67e3-105">การสร้าง และการลงรายการบัญชีใบแจ้งหนี้ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="c67e3-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="c67e3-106">คุณสามารถเลือกข้อบังคับในสมุดรายวันก่อนที่จะสร้างไฟล์การชำระเงิน เพื่อรองรับสถานการณ์ที่ลูกค้าชำระเงินล่วงหน้า แทนการชำระเงินตามใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c67e3-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="c67e3-107">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ DEMF</span><span class="sxs-lookup"><span data-stu-id="c67e3-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="c67e3-108">นี่คือกระบวนงานที่ห้าจากกระบวนงานห้ารายการที่แสดงให้เห็นถึงกระบวนการชำระเงินล่วงหน้าของลูกค้าโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c67e3-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="c67e3-109">ก่อนที่คุณสามารถทำงานนี้ให้เสร็จสมบูรณ์ คุณต้องดำเนินการงานก่อนหน้านี้ให้เสร็จสมบูรณ์ก่อน</span><span class="sxs-lookup"><span data-stu-id="c67e3-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="c67e3-110">อันดับแรกคุณต้องนำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์การชำระเงินล่วงหน้าของลูกค้า ตั้งค่าคอนฟิกวิธีการชำระเงิน และตั้งค่าข้อมูลบริษัทและลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="c67e3-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="c67e3-111">ลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระด้วยข้อมูลการหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c67e3-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="c67e3-112">ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ข้อความอิสระทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c67e3-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="c67e3-113">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c67e3-113">Click New.</span></span>
3. <span data-ttu-id="c67e3-114">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c67e3-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="c67e3-115">ตัวอย่างเช่น เลือก DE-010</span><span class="sxs-lookup"><span data-stu-id="c67e3-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="c67e3-116">ในฟิลด์วิธีการชำระเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c67e3-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="c67e3-117">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="c67e3-117">For example.</span></span> <span data-ttu-id="c67e3-118">เลือก อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c67e3-118">select Electronic.</span></span>  
5. <span data-ttu-id="c67e3-119">ในฟิลด์หัสข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c67e3-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="c67e3-120">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="c67e3-120">Click Add line.</span></span>
7. <span data-ttu-id="c67e3-121">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c67e3-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="c67e3-122">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c67e3-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="c67e3-123">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c67e3-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="c67e3-124">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c67e3-124">Click Post.</span></span>
11. <span data-ttu-id="c67e3-125">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c67e3-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="c67e3-126">สร้างการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c67e3-126">Create a payment</span></span>
1. <span data-ttu-id="c67e3-127">ไปที่บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c67e3-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="c67e3-128">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c67e3-128">Click New.</span></span>
3. <span data-ttu-id="c67e3-129">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c67e3-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="c67e3-130">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="c67e3-130">Click Lines.</span></span>
5. <span data-ttu-id="c67e3-131">คลิก ข้อเสนอการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c67e3-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="c67e3-132">คลิกสร้างข้อเสนอการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c67e3-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="c67e3-133">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="c67e3-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="c67e3-134">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="c67e3-134">Click Filter.</span></span>
9. <span data-ttu-id="c67e3-135">ในรายการ เลือกแถวสำหรับตารางธุรกรรมลูกค้าและฟิลด์วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c67e3-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="c67e3-136">คุณสามารถใช้เงื่อนไขใด ๆ สำหรับการเลือกธุรกรรมลูกค้าเพื่อชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c67e3-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="c67e3-137">สำหรับตัวอย่างนี้ ใช้อิเล็กทรอนิกส์เป็นวิธีการชำระเงินเพื่อกรองธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="c67e3-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="c67e3-138">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c67e3-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="c67e3-139">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="c67e3-139">Click OK.</span></span>
12. <span data-ttu-id="c67e3-140">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="c67e3-140">Click OK.</span></span>
13. <span data-ttu-id="c67e3-141">คลิกสร้างการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c67e3-141">Click Create payments.</span></span>
