---
title: สร้างรายการสมุดรายวันโดยใช้เท็มเพลต
description: 'ใบสำคัญสมุดรายวันที่มีการลงรายการบัญชีสามารถบันทึกเป็นเท็มเพลตใบสำคัญ และนำไปใช้ในใบสำคัญสมุดรายวันใหม่ '
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3843c165b3fc3030a937ec47a1439b1c1b36206d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216519"
---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="82701-103">สร้างรายการสมุดรายวันโดยใช้เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="82701-103">Create a journal entry using template</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82701-104">ใบสำคัญสมุดรายวันที่มีการลงรายการบัญชีสามารถบันทึกเป็นเท็มเพลตใบสำคัญ และนำไปใช้ในใบสำคัญสมุดรายวันใหม่ </span><span class="sxs-lookup"><span data-stu-id="82701-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="82701-105">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="82701-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="82701-106">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="82701-106">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
2. <span data-ttu-id="82701-107">บน **บานหน้าต่างการดำเนินการ** ให้คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="82701-107">On the **Action pane**, click **New**.</span></span> <span data-ttu-id="82701-108">กระบวนงานนี้เริ่มต้นโดยการสร้างและการลงรายการบัญชีใบสำคัญสมุดรายวัน แต่สามารถบันทึกใบสำคัญสมุดรายวันที่มีการลงรายการบัญชีไว้ก่อนหน้านี้ใดๆเป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="82701-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
3. <span data-ttu-id="82701-109">ในฟิลด์ **ชื่อ** ให้คลิกปุ่มรายการแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="82701-109">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="82701-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="82701-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="82701-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="82701-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="82701-112">คลิก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="82701-112">Click **Lines**.</span></span>
7. <span data-ttu-id="82701-113">ในฟิลด์ **ชนิดบัญชี** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="82701-113">In the **Account type** field, type a value.</span></span>
8. <span data-ttu-id="82701-114">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="82701-114">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="82701-115">ในฟิลด์ **เดบิต** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="82701-115">In the **Debit** field, type a value.</span></span>
10. <span data-ttu-id="82701-116">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="82701-116">Click **New**.</span></span>
11. <span data-ttu-id="82701-117">ในฟิลด์ **ชนิดบัญชี** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="82701-117">In the **Account type** field, type a value.</span></span>
12. <span data-ttu-id="82701-118">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="82701-118">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="82701-119">ในฟิลด์ **เดบิต** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="82701-119">In the **Debit** field, type a value.</span></span>
14. <span data-ttu-id="82701-120">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="82701-120">Click **New**.</span></span>
14. <span data-ttu-id="82701-121">ในฟิลด์ **บัญชี** ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="82701-121">In the **Account** field, specify the desired values.</span></span>
15. <span data-ttu-id="82701-122">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="82701-122">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="82701-123">ในฟิลด์ **เครดิต** พิมพ์ค่าเพื่อคงยอดดุลใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="82701-123">In the **Credit** field, type a value to balance the voucher.</span></span>
17. <span data-ttu-id="82701-124">ใน **บานหน้าต่างการดำเนินการ** คลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="82701-124">On the **Action pane**, click **Post**.</span></span>
18. <span data-ttu-id="82701-125">คลิก **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="82701-125">Click **Functions**.</span></span>
19. <span data-ttu-id="82701-126">คลิกเท็มเพลต **บันทึกใบสำคัญ**</span><span class="sxs-lookup"><span data-stu-id="82701-126">Click **Save voucher** template.</span></span>
20. <span data-ttu-id="82701-127">กระบวนงานนี้สมมุติชนิด **เท็มเพลตเปอร์เซ็นต์**</span><span class="sxs-lookup"><span data-stu-id="82701-127">This procedure assumes a **Percent Template** type.</span></span> <span data-ttu-id="82701-128">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="82701-128">Click OK.</span></span>
    - <span data-ttu-id="82701-129">เปอร์เซ็นต์: ยอดเงินในใบสำคัญจะถูกแปลงเป็นสัดส่วนเปอร์เซ็นต์ ซึ่งทำให้สามารถใช้ยอดเงินใดๆ เมื่อมีการเลือกเท็มเพลตใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="82701-129">Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>
    - <span data-ttu-id="82701-130">ยอดเงิน: ยอดเงินจริงจะถูกจัดเก็บและนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="82701-130">Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="82701-131">คลิก **สมุดรายวันทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="82701-131">Click **General journals**.</span></span>
22. <span data-ttu-id="82701-132">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="82701-132">Click **New**.</span></span>
23. <span data-ttu-id="82701-133">ในฟิลด์ **ชื่อ** ให้คลิกปุ่มรายการแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="82701-133">In the **Name** field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="82701-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="82701-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="82701-135">คลิก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="82701-135">Click **Lines**.</span></span>
26. <span data-ttu-id="82701-136">คลิก **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="82701-136">Click **Functions**.</span></span>
27. <span data-ttu-id="82701-137">คลิก **เลือกเท็มเพลตใบสำคัญ**</span><span class="sxs-lookup"><span data-stu-id="82701-137">Click **Select voucher template**.</span></span>
28. <span data-ttu-id="82701-138">ค้นหาเท็มเพลตที่คุณสร้างไว้ก่อนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="82701-138">Find the template that you created earlier.</span></span> <span data-ttu-id="82701-139">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="82701-139">Click **OK**.</span></span> <span data-ttu-id="82701-140">คุณอาจต้องคลิกที่ **ขั้นตอนก่อนหน้านี้** แล้วจากนั้น เลือกเท็มเพลตที่ถูกต้อง ถ้ามีเท็มเพลตอื่นอยู่</span><span class="sxs-lookup"><span data-stu-id="82701-140">You may need to click **Previous step** and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="82701-141">ในฟิลด์ **ยอดเงิน** ให้ป้อนยอดเงินจะใช้กับใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="82701-141">In the **Amount** field, enter the amount to be applied to the voucher.</span></span> <span data-ttu-id="82701-142">ฟิลด์ **ยอดเงิน** จะแสดงขึ้นเฉพาะเมื่อมีเท็มเพลตใบสำคัญเป็นชนิดเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="82701-142">The **Amount** field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="82701-143">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="82701-143">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]