---
title: สร้างบัญชีธนาคารของผู้จัดจำหน่าย
description: 'กระบวนงานนี้แสดงวิธีการสร้างบัญชีธนาคารสำหรับผู้จัดจำหน่าย '
author: kamaybac
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fcf15d798d2ca8e1d36556fbe2c9603f12d2b03
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812025"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="47e4d-103">สร้างบัญชีธนาคารของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="47e4d-103">Create a vendor bank account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="47e4d-104">กระบวนงานนี้แสดงวิธีการสร้างบัญชีธนาคารสำหรับผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="47e4d-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="47e4d-105">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="47e4d-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="47e4d-106">ไปที่ **บานหน้าต่างการนำทาง > โมดูล > การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="47e4d-106">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="47e4d-107">เลือกผู้จัดจำหน่ายที่คุณต้องการสร้างบัญชีธนาคารให้ และจากนั้น คลิกลิงค์ **รหัสบัญชีผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="47e4d-107">Select the vendor that you want to create a bank account for, and then click the link on the **Vendor account ID** field.</span></span>
3. <span data-ttu-id="47e4d-108">บน **บานหน้าต่างการดำเนินการ** คลิก **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="47e4d-108">On the **Action Pane**, click **Vendor**.</span></span>
4. <span data-ttu-id="47e4d-109">คลิก **บัญชีธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="47e4d-109">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="47e4d-110">บน **บานหน้าต่างการดำเนินการ** ให้คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="47e4d-110">On the **Action Pane**, click **New**.</span></span>
6. <span data-ttu-id="47e4d-111">ในฟิลด์ **บัญชีธนาคาร** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="47e4d-111">In the **Bank account** field, type a value.</span></span> <span data-ttu-id="47e4d-112">รหัสนี้จะใช้เพื่อระบุบัญชีธนาคารในบันทึกของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="47e4d-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="47e4d-113">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="47e4d-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="47e4d-114">ในฟิลด์ **กลุ่มธนาคาร** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="47e4d-114">In the **Bank groups** field, enter or select a value.</span></span>
9. <span data-ttu-id="47e4d-115">ในฟิลด์ **ชนิดของหมายเลขการกำหนดเส้นทาง** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="47e4d-115">In the **Routing number type** field, select an option.</span></span> <span data-ttu-id="47e4d-116">นี่คือชนิดของหมายเลขการกำหนดเส้นทางที่ใช้สำหรับการชำระเงินระหว่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="47e4d-116">This is the type of routing number that's used for international payments.</span></span>  
10. <span data-ttu-id="47e4d-117">ในฟิลด์ **หมายเลขบัญชีธนาคาร** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="47e4d-117">In the **Bank account number** field, type a value.</span></span>
11. <span data-ttu-id="47e4d-118">ในฟิลด์ **รหัส SWIFT** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="47e4d-118">In the **SWIFT code** field, type a value.</span></span>
12. <span data-ttu-id="47e4d-119">ในฟิลด์ **IBAN** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="47e4d-119">In the **IBAN** field, type a value.</span></span>
    - <span data-ttu-id="47e4d-120">หมายเลข IBAN ต้องอยู่ในรูปแบบที่ถูกต้อง </span><span class="sxs-lookup"><span data-stu-id="47e4d-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="47e4d-121">ตัวอย่างเช่น คุณสามารถใช้ DE89370400440532013000</span><span class="sxs-lookup"><span data-stu-id="47e4d-121">For example, you could use DE89370400440532013000.</span></span>  
    - <span data-ttu-id="47e4d-122">สถานะของบัญชีธนาคารจะเป็นใช้งานอยู่ถ้าวันที่ใช้งานอยู่ครบกำหนดแล้วแต่ยังไม่เกินวันหมดอายุ </span><span class="sxs-lookup"><span data-stu-id="47e4d-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="47e4d-123">นอกจากนี้ ยังใช้งานอยู่เช่นกัน ถ้าทั้งฟิลด์วันที่ใช้งานอยู่และวันหมดอายุว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="47e4d-123">It's also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="47e4d-124">ถ้าวันที่ทั้งในฟิลด์วันที่ใช้งานอยู่และวันหมดอายุเป็นการชำระเงินทางอิเล็กทรอนิกส์ในอนาคตไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="47e4d-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="47e4d-125">ชนิดการชำระเงินอื่นๆ จะพร้อมใช้งานและบัญชีธนาคารจะเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="47e4d-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="47e4d-126">ขยายส่วน **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="47e4d-126">Expand the **Setup** section.</span></span>
14. <span data-ttu-id="47e4d-127">ในฟิลด์ **รหัสข้อความ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="47e4d-127">In the **Text code** field, type a value.</span></span> <span data-ttu-id="47e4d-128">ฟิลด์นี้ระบุรหัสที่จะปรากฏบนใบแจ้งยอดจากธนาคารของผู้รับ</span><span class="sxs-lookup"><span data-stu-id="47e4d-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="47e4d-129">ในฟิลด์ **ข่าวสารที่ส่งให้ธนาคาร** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="47e4d-129">In the **Message to bank** field, type a value.</span></span>
16. <span data-ttu-id="47e4d-130">ในฟิลด์ **การอ้างอิงอัตราแลกเปลี่ยน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="47e4d-130">In the **Exchange reference** field, type a value.</span></span> <span data-ttu-id="47e4d-131">นี่คือหมายเลขอ้างอิงสำหรับอัตราแลกเปลี่ยนล่วงหน้าหรืออัตราแลกเปลี่ยนคงที่</span><span class="sxs-lookup"><span data-stu-id="47e4d-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>
17. <span data-ttu-id="47e4d-132">ในฟิลด์ **สกุลเงิน** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="47e4d-132">In the **Currency** field, enter or select a value.</span></span> <span data-ttu-id="47e4d-133">เมื่อมีการออกบันทึกย่อ ส่วนนี้จะแสดงภาพรวมของสถานะ (ที่ค้างอยู่หรือได้รับอนุมัติ)</span><span class="sxs-lookup"><span data-stu-id="47e4d-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="47e4d-134">ขยายส่วน **ที่อยู่**</span><span class="sxs-lookup"><span data-stu-id="47e4d-134">Expand the **Address** section.</span></span>
19. <span data-ttu-id="47e4d-135">ขยายส่วน **บันทึกย่อ**</span><span class="sxs-lookup"><span data-stu-id="47e4d-135">Expand the **Prenotes** section.</span></span>
20. <span data-ttu-id="47e4d-136">ขยายส่วน **ข้อมูลผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="47e4d-136">Expand the **Contact information** section.</span></span>
21. <span data-ttu-id="47e4d-137">ในฟิลด์ **โทรศัพท์** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="47e4d-137">In the **Telephone** field, type a value.</span></span>
22. <span data-ttu-id="47e4d-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="47e4d-138">Close the page.</span></span>
23. <span data-ttu-id="47e4d-139">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="47e4d-139">Click **Edit**.</span></span>
24. <span data-ttu-id="47e4d-140">ขยายส่วน **การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="47e4d-140">Expand the **Payment** section.</span></span>
25. <span data-ttu-id="47e4d-141">ในฟิลด์ **บัญชีธนาคาร** เลือกบัญชีที่คุณเพิ่งสร้าง</span><span class="sxs-lookup"><span data-stu-id="47e4d-141">In the **Bank account** field, select the account that you've just created.</span></span>
26. <span data-ttu-id="47e4d-142">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="47e4d-142">Click **Save**.</span></span> <span data-ttu-id="47e4d-143">ที่อยู่อาจถูกสืบทอดมาจากกลุ่มธนาคาร ถ้ามีการกำหนดไว้ หรือคุณสามารถเพิ่มได้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="47e4d-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]