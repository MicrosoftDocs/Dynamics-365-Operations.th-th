---
title: สร้างรายการสมุดรายวันโดยใช้เท็มเพลต
description: 'ใบสำคัญสมุดรายวันที่มีการลงรายการบัญชีสามารถบันทึกเป็นเท็มเพลตใบสำคัญ และนำไปใช้ในใบสำคัญสมุดรายวันใหม่ '
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a749740b62e39202d502a112f947679f85ca085
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562518"
---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="6328c-103">สร้างรายการสมุดรายวันโดยใช้เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="6328c-103">Create a journal entry using template</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6328c-104">ใบสำคัญสมุดรายวันที่มีการลงรายการบัญชีสามารถบันทึกเป็นเท็มเพลตใบสำคัญ และนำไปใช้ในใบสำคัญสมุดรายวันใหม่ </span><span class="sxs-lookup"><span data-stu-id="6328c-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="6328c-105">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="6328c-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="6328c-106">บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="6328c-106">General ledger > Journal entries > General journals.</span></span> <span data-ttu-id="6328c-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6328c-107">Click New.</span></span>
    * <span data-ttu-id="6328c-108">กระบวนงานนี้เริ่มต้นโดยการสร้างและการลงรายการบัญชีใบสำคัญสมุดรายวัน แต่สามารถบันทึกใบสำคัญสมุดรายวันที่มีการลงรายการบัญชีไว้ก่อนหน้านี้ใดๆเป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="6328c-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
2. <span data-ttu-id="6328c-109">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="6328c-109">In the Name field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6328c-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6328c-110">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="6328c-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6328c-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6328c-112">คลิกรายการ</span><span class="sxs-lookup"><span data-stu-id="6328c-112">Click Lines.</span></span>
6. <span data-ttu-id="6328c-113">ป้อนบัญชีสำหรับชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="6328c-113">Enter an account for the Account type.</span></span>
7. <span data-ttu-id="6328c-114">ในฟิลด์คำอธิบาย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6328c-114">In the Description field, type a value.</span></span>
8. <span data-ttu-id="6328c-115">ให้ป้อนจำนวนในฟิลด์เดบิต</span><span class="sxs-lookup"><span data-stu-id="6328c-115">Enter an amount in the Debit field.</span></span>
9. <span data-ttu-id="6328c-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6328c-116">Click New.</span></span>
10. <span data-ttu-id="6328c-117">ป้อนบัญชีที่ต่างกันสำหรับชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="6328c-117">Enter a different account for the Account type.</span></span>
11. <span data-ttu-id="6328c-118">ในฟิลด์คำอธิบาย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6328c-118">In the Description field, type a value.</span></span>
12. <span data-ttu-id="6328c-119">ให้ป้อนจำนวนในฟิลด์เดบิต</span><span class="sxs-lookup"><span data-stu-id="6328c-119">Enter an amount in the Debit field.</span></span>
13. <span data-ttu-id="6328c-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6328c-120">Click New.</span></span>
14. <span data-ttu-id="6328c-121">ในฟิลด์บัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6328c-121">In the Account field, specify the desired values.</span></span>
15. <span data-ttu-id="6328c-122">ในฟิลด์คำอธิบาย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6328c-122">In the Description field, type a value.</span></span>
16. <span data-ttu-id="6328c-123">ป้อนยอดเงินในฟิลด์เครดิตเพื่อคงยอดดุลใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="6328c-123">Enter an amount in the Credit field to balance the voucher.</span></span>
17. <span data-ttu-id="6328c-124">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="6328c-124">Click Post.</span></span>
18. <span data-ttu-id="6328c-125">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="6328c-125">Click Functions.</span></span>
19. <span data-ttu-id="6328c-126">คลิกบันทึกเท็มเพลตใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="6328c-126">Click Save voucher template.</span></span>
20. <span data-ttu-id="6328c-127">กระบวนงานนี้สมมุติชนิดเท็มเพลตเปอร์เซ็นต์ </span><span class="sxs-lookup"><span data-stu-id="6328c-127">This procedure assumes a Percent Template type.</span></span> <span data-ttu-id="6328c-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6328c-128">Click OK.</span></span>
    * <span data-ttu-id="6328c-129">• เปอร์เซ็นต์: ยอดเงินในใบสำคัญจะถูกแปลงเป็นสัดส่วนเปอร์เซ็นต์ ซึ่งทำให้สามารถใช้ยอดเงินเมื่อมีการเลือกเท็มเพลตใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="6328c-129">• Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>  <span data-ttu-id="6328c-130">• ยอด: ยอดเงินจริงจะถูกจัดเก็บและนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="6328c-130">• Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="6328c-131">คลิกสมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="6328c-131">Click General journals.</span></span>
22. <span data-ttu-id="6328c-132">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6328c-132">Click New.</span></span>
23. <span data-ttu-id="6328c-133">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="6328c-133">In the Name field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="6328c-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6328c-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="6328c-135">คลิกรายการ</span><span class="sxs-lookup"><span data-stu-id="6328c-135">Click Lines.</span></span>
26. <span data-ttu-id="6328c-136">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="6328c-136">Click Functions.</span></span>
27. <span data-ttu-id="6328c-137">คลิกการเลือกเท็มเพลตใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="6328c-137">Click Select voucher template.</span></span>
28. <span data-ttu-id="6328c-138">ค้นหาเท็มเพลตที่คุณสร้างไว้ก่อนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="6328c-138">Find the template that you created earlier.</span></span> <span data-ttu-id="6328c-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6328c-139">Click OK.</span></span>
    * <span data-ttu-id="6328c-140">คุณอาจต้องคลิกที่ขั้นตอนก่อนหน้านี้ แล้วเลือกเท็มเพลตที่ถูกต้องถ้ามีเท็มเพลตอื่นอยู่</span><span class="sxs-lookup"><span data-stu-id="6328c-140">You may need to click Previous step and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="6328c-141">ในฟิลด์ยอดเงิน ให้ป้อนยอดเงินจะใช้กับใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="6328c-141">In the Amount field, enter the amount to be applied to the voucher.</span></span>
    * <span data-ttu-id="6328c-142">ฟิลด์ยอดเงินจะแสดงขึ้นเฉพาะเมื่อมีเท็มเพลตใบสำคัญเป็นชนิดเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="6328c-142">The amount field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="6328c-143">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6328c-143">Click OK.</span></span>

