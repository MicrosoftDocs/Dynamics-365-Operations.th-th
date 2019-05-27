---
title: สร้างบัญชีธนาคารของผู้จัดจำหน่าย
description: 'กระบวนงานนี้แสดงวิธีการสร้างบัญชีธนาคารสำหรับผู้จัดจำหน่าย '
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deb3587667ac13b95617ec219995bfef931df00c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546144"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="20e4b-103">สร้างบัญชีธนาคารของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="20e4b-103">Create a vendor bank account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20e4b-104">กระบวนงานนี้แสดงวิธีการสร้างบัญชีธนาคารสำหรับผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="20e4b-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="20e4b-105">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="20e4b-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="20e4b-106">ไปที่การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="20e4b-106">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="20e4b-107">เลือกผู้จัดจำหน่ายที่คุณต้องการสร้างบัญชีธนาคาร และจากนั้น คลิกลิงค์ในรหัสบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="20e4b-107">Select the vendor that you want to create a bank account for, and then click the link on the Vendor account ID.</span></span>
3. <span data-ttu-id="20e4b-108">ในบานหน้าต่างการดำเนินการ คลิกผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="20e4b-108">On the Action Pane, click Vendor.</span></span>
4. <span data-ttu-id="20e4b-109">คลิก บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="20e4b-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="20e4b-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="20e4b-110">Click New.</span></span>
6. <span data-ttu-id="20e4b-111">ในฟิลด์บัญชีธนาคาร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="20e4b-111">In the Bank account field, type a value.</span></span>
    * <span data-ttu-id="20e4b-112">รหัสนี้จะใช้เพื่อระบุบัญชีธนาคารในบันทึกของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="20e4b-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="20e4b-113">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="20e4b-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="20e4b-114">ในฟิลด์กลุ่มธนาคาร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="20e4b-114">In the Bank groups field, enter or select a value.</span></span>
9. <span data-ttu-id="20e4b-115">ในฟิลด์ชนิดของหมายเลขเส้นทาง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="20e4b-115">In the Routing number type field, select an option.</span></span>
    * <span data-ttu-id="20e4b-116">นี่คือชนิดของหมายเลขเส้นทางที่ใช้สำหรับการชำระเงินระหว่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="20e4b-116">This is the type of routing number that’s used for international payments.</span></span>  
10. <span data-ttu-id="20e4b-117">ในฟิลด์หมายเลขบัญชีธนาคาร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="20e4b-117">In the Bank account number field, type a value.</span></span>
11. <span data-ttu-id="20e4b-118">ในฟิลด์รหัส SWIFT ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="20e4b-118">In the SWIFT code field, type a value.</span></span>
12. <span data-ttu-id="20e4b-119">ในฟิลด์ IBAN ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="20e4b-119">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="20e4b-120">หมายเลข IBAN ต้องอยู่ในรูปแบบที่ถูกต้อง </span><span class="sxs-lookup"><span data-stu-id="20e4b-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="20e4b-121">ตัวอย่างเช่น คุณสามารถใช้ DE89370400440532013000</span><span class="sxs-lookup"><span data-stu-id="20e4b-121">For example, you could use DE89370400440532013000.</span></span>  
    * <span data-ttu-id="20e4b-122">สถานะของบัญชีธนาคารจะเป็นใช้งานอยู่ถ้าวันที่ใช้งานอยู่ครบกำหนดแล้วแต่ยังไม่เกินวันหมดอายุ </span><span class="sxs-lookup"><span data-stu-id="20e4b-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="20e4b-123">และจะเป็นใช้งานอยู่เช่นกันถ้าทั้งฟิลด์วันที่ใช้งานอยู่และวันหมดอายุว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="20e4b-123">It’s also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="20e4b-124">ถ้าวันที่ทั้งในฟิลด์วันที่ใช้งานอยู่และวันหมดอายุเป็นการชำระเงินทางอิเล็กทรอนิกส์ในอนาคตไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="20e4b-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="20e4b-125">ชนิดการชำระเงินอื่นๆ จะพร้อมใช้งานและบัญชีธนาคารจะเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="20e4b-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="20e4b-126">ขยายส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="20e4b-126">Expand the Setup section.</span></span>
14. <span data-ttu-id="20e4b-127">ในฟิลด์รหัสข้อความ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="20e4b-127">In the Text code field, type a value.</span></span>
    * <span data-ttu-id="20e4b-128">ฟิลด์นี้ระบุรหัสที่จะปรากฏบนใบแจ้งยอดจากธนาคารของผู้รับ</span><span class="sxs-lookup"><span data-stu-id="20e4b-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="20e4b-129">ในฟิลด์ข่าวสารที่ส่งให้ธนาคาร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="20e4b-129">In the Message to bank field, type a value.</span></span>
16. <span data-ttu-id="20e4b-130">ในฟิลด์การอ้างอิงอัตราแลกเปลี่ยน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="20e4b-130">In the Exchange reference field, type a value.</span></span>
    * <span data-ttu-id="20e4b-131">นี่คือหมายเลขอ้างอิงสำหรับอัตราแลกเปลี่ยนล่วงหน้าหรืออัตราแลกเปลี่ยนคงที่</span><span class="sxs-lookup"><span data-stu-id="20e4b-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>  
17. <span data-ttu-id="20e4b-132">ในฟิลด์สกุลเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="20e4b-132">In the Currency field, enter or select a value.</span></span>
    * <span data-ttu-id="20e4b-133">เมื่อมีการออกบันทึกย่อ ส่วนนี้จะแสดงภาพรวมของสถานะ (ที่ค้างอยู่หรือได้รับอนุมัติ)</span><span class="sxs-lookup"><span data-stu-id="20e4b-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="20e4b-134">ขยายส่วนที่อยู่</span><span class="sxs-lookup"><span data-stu-id="20e4b-134">Expand the Address section.</span></span>
19. <span data-ttu-id="20e4b-135">ขยายส่วนบันทึกย่อ</span><span class="sxs-lookup"><span data-stu-id="20e4b-135">Expand the Prenotes section.</span></span>
20. <span data-ttu-id="20e4b-136">ขยายส่วนข้อมูลผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="20e4b-136">Expand the Contact information section.</span></span>
21. <span data-ttu-id="20e4b-137">ในฟิลด์โทรศัพท์ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="20e4b-137">In the Telephone field, type a value.</span></span>
22. <span data-ttu-id="20e4b-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="20e4b-138">Close the page.</span></span>
23. <span data-ttu-id="20e4b-139">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="20e4b-139">Click Edit.</span></span>
24. <span data-ttu-id="20e4b-140">ขยายส่วนการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="20e4b-140">Expand the Payment section.</span></span>
25. <span data-ttu-id="20e4b-141">ในฟิลด์บัญชีธนาคาร เลือกบัญชีที่คุณเพิ่งสร้าง</span><span class="sxs-lookup"><span data-stu-id="20e4b-141">In the Bank  account field, select the account that you’ve just created.</span></span>
26. <span data-ttu-id="20e4b-142">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="20e4b-142">Click Save.</span></span>
    * <span data-ttu-id="20e4b-143">ที่อยู่อาจถูกสืบทอดมาจากกลุ่มธนาคาร ถ้ามีการกำหนดไว้ หรือคุณสามารถเพิ่มได้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="20e4b-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  

