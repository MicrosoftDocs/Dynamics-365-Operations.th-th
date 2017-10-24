--- 
title: "สร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระ"
description: "การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9c9811b348d81cd735c5b75ca48e0a56a8d52be
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="44ec9-103">สร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="44ec9-103">Create a free text invoice template</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="44ec9-104">การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="44ec9-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="44ec9-105">การบันทึกจัดทำขึ้นสำหรับผู้ใช้ที่รับผิดชอบการจัดการ และประมวลผลใบแจ้งหนี้ A/R</span><span class="sxs-lookup"><span data-stu-id="44ec9-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="44ec9-106">ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ที่เกิดซ้ำ > เท็มเพลตใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="44ec9-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="44ec9-107">ใช้แบบฟอร์มนี้เพื่อสร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระที่สามารถรวมรายการใบแจ้งหนี้ ค่าธรรมเนียม เท็มเพลตการกระจายการลงบัญชี และข้อมูลบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="44ec9-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="44ec9-108">คลิก 'สร้าง' เพื่อสร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระใหม่</span><span class="sxs-lookup"><span data-stu-id="44ec9-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="44ec9-109">ในฟิลด์ชื่อเท็มเพลต ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="44ec9-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="44ec9-110">'ชื่อเท็มเพลต' บ่งชี้เท็มเพลใบแจ้งหนี้ข้อความอิสระโดยเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="44ec9-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="44ec9-111">เท็มเพลตสองอันไม่สามารถมี 'ชื่อเท็มเพลต' เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="44ec9-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="44ec9-112">ในฟิลด์คำอธิบาย ป้อนคำอธิบายของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="44ec9-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="44ec9-113">ขยายแท็บรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="44ec9-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="44ec9-114">ในฟิลด์คำอธิบาย ป้อนคำอธิบายของรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="44ec9-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="44ec9-115">ในฟิลด์บัญชีหลัก เลือกบัญชีรายได้</span><span class="sxs-lookup"><span data-stu-id="44ec9-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="44ec9-116">คุณสามารถเลือกกำหนดบัญชีธุรกรรมออฟเซ็ตของเครดิตลูกค้าสำหรับยอดเงินใบแจ้งหนี้ทั้งหมดรวมในหน้าโพรไฟล์การลงรายการบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="44ec9-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="44ec9-117">ในฟิลด์กลุ่มภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="44ec9-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="44ec9-118">กลุ่มภาษีขายสำหรับรายการใบแจ้งหนี้ปัจจุบัน เป็นกลุ่มภาษีขายเริ่มต้นสำหรับบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="44ec9-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="44ec9-119">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="44ec9-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="44ec9-120">ในฟิลด์กลุ่มภาษีขาย เลือกกลุ่มภาษีขายของสินค้าสำหรับรายการใบแจ้งหนี้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="44ec9-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="44ec9-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="44ec9-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="44ec9-122">ในฟิลด์ราคาต่อหน่วย ป้อนหรือดูราคาต่อหน่วยสำหรับรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="44ec9-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="44ec9-123">ยอดเงินนี้จะถูกคูณด้วยฟิลด์ปริมาณโดยอัตโนมัติเพื่อกำหนดยอดเงินรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="44ec9-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="44ec9-124">เพิ่มรายการใหม่สำหรับเท็มเพลตใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="44ec9-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="44ec9-125">ในฟิลด์คำอธิบาย ป้อนคำอธิบายของรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="44ec9-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="44ec9-126">ในฟิลด์บัญชีหลัก เลือกบัญชีรายได้</span><span class="sxs-lookup"><span data-stu-id="44ec9-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="44ec9-127">คุณสามารถเลือกกำหนดบัญชีธุรกรรมออฟเซ็ตของเครดิตลูกค้าสำหรับยอดเงินใบแจ้งหนี้ทั้งหมดรวมในหน้าโพรไฟล์การลงรายการบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="44ec9-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="44ec9-128">ในฟิลด์กลุ่มภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="44ec9-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="44ec9-129">กลุ่มภาษีขายสำหรับรายการใบแจ้งหนี้ปัจจุบัน เป็นกลุ่มภาษีขายเริ่มต้นสำหรับบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="44ec9-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="44ec9-130">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="44ec9-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="44ec9-131">ในฟิลด์กลุ่มภาษีขายตามประเภทสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="44ec9-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="44ec9-132">กลุ่มภาษีขายตามประเภทสินค้าสำหรับรายการใบแจ้งหนี้ปัจจุบัน </span><span class="sxs-lookup"><span data-stu-id="44ec9-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="44ec9-133">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="44ec9-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="44ec9-134">ป้อนหรือดูจำนวนหน่วยสำหรับรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="44ec9-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="44ec9-135">ยอดเงินนี้จะถูกคูณด้วยค่าในฟิลด์ราคาต่อหน่วยเพื่อกำหนดยอดเงินรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="44ec9-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="44ec9-136">ป้อนหรือดูราคาต่อหน่วยสำหรับรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="44ec9-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="44ec9-137">ยอดเงินนี้จะถูกคูณด้วยค่าในฟิลด์ปริมาณเพื่อกำหนดยอดเงินรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="44ec9-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="44ec9-138">ดูและแก้ไขการกระจายการลงบัญชีสำหรับแต่ละบรรทัดและรายการรองใดๆ</span><span class="sxs-lookup"><span data-stu-id="44ec9-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="44ec9-139">การกระจายการลงบัญชีกำหนดวิธีที่ยอดเงินจะถูกนำมาพิจารณา เช่น วิธีที่รายได้ ภาษี หรือค่าธรรมเนียมจะถูกนำมาพิจารณาสำหรับใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="44ec9-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="44ec9-140">อัพเดทการกระจายการลงบัญชีสำหรับรายการใบแจ้งหนี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="44ec9-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="44ec9-141">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="44ec9-141">Click Close.</span></span>


