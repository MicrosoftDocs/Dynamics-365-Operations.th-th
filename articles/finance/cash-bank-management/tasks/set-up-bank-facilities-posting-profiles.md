---
title: ตั้งค่าสินเชื่อธนาคารและการลงรายการบัญชีโพรไฟล์สำหรับหนังสือค้ำประกัน
description: 'งานนี้สร้างสินเชื่อของธนาคารและการลงรายการบัญชีโพรไฟล์ ที่จำเป็นสำหรับการประมวลผลหนังสือค้ำประกัน '
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b72a412aaaf1c70b4414d00e99b923380f7dd86
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225308"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="4569b-103">ตั้งค่าสินเชื่อธนาคารและการลงรายการบัญชีโพรไฟล์สำหรับหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="4569b-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4569b-104">งานนี้สร้างสินเชื่อของธนาคารและการลงรายการบัญชีโพรไฟล์ ที่จำเป็นสำหรับการประมวลผลหนังสือค้ำประกัน </span><span class="sxs-lookup"><span data-stu-id="4569b-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="4569b-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="4569b-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="4569b-106">พารามิเตอร์บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="4569b-106">General ledger parameter</span></span>
1. <span data-ttu-id="4569b-107">ไปที่การจัดการเงินสดและธนาคาร > การตั้งค่า > พารามิเตอร์การจัดการเงินสดและธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4569b-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="4569b-108">ขยายส่วนเอกสารธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4569b-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="4569b-109">เลือกตัวเลือกการเปิดใช้งานหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="4569b-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="4569b-110">ในฟิลด์สมุดรายวันธุรกรรม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4569b-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4569b-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4569b-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="4569b-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4569b-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4569b-113">คลิกแท็บลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="4569b-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="4569b-114">กำหนดรหัสลำดับหมายเลข สำหรับการอ้างอิงหมายเลขหนังสือค้ำประกันและธุรกรรมหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="4569b-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="4569b-115">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4569b-115">Click Save.</span></span>
9. <span data-ttu-id="4569b-116">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4569b-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="4569b-117">สร้างสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4569b-117">Create Bank facility</span></span>
1. <span data-ttu-id="4569b-118">ไปที่การจัดการเงินสดและธนาคาร > การตั้งค่า > สินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4569b-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="4569b-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4569b-119">Click New.</span></span>
3. <span data-ttu-id="4569b-120">ในฟิลด์กลุ่มสินเชื่อ ให้ป้อนชื่อกลุ่มสินเชื่อธนาคารสำหรับธุรกรรมหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="4569b-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="4569b-121">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4569b-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4569b-122">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4569b-122">Click Save.</span></span>
6. <span data-ttu-id="4569b-123">คลิกแท็บชนิดของสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="4569b-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="4569b-124">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4569b-124">Click New.</span></span>
8. <span data-ttu-id="4569b-125">ในฟิลด์ชนิดของสินเชื่อ ให้ป้อนชื่อของชนิดของสินเชื่อธนาคารที่สัมพันธ์กับข้อตกลงสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4569b-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="4569b-126">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4569b-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="4569b-127">ในฟิลด์กลุ่มสินเชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4569b-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="4569b-128">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4569b-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="4569b-129">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4569b-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="4569b-130">ในฟิลด์ลักษณะสินเชื่อ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="4569b-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="4569b-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4569b-131">Click Save.</span></span>
15. <span data-ttu-id="4569b-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4569b-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="4569b-133">โพรไฟล์การลงรายการบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4569b-133">Bank posting profile</span></span>
1. <span data-ttu-id="4569b-134">ไปที่การจัดการเงินสดและธนาคาร > การตั้งค่า > โพรไฟล์การลงรายการบัญชีเอกสารธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4569b-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="4569b-135">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4569b-135">Click New.</span></span>
3. <span data-ttu-id="4569b-136">ในฟิลด์หมายเลขบัญชี/กลุ่ม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4569b-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4569b-137">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4569b-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4569b-138">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4569b-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4569b-139">ในฟิลด์การตัดรายการบัญชี ให้เลือกบัญชีหลักสำหรับการจ่ายเงิน</span><span class="sxs-lookup"><span data-stu-id="4569b-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="4569b-140">ในฟิลด์บัญชีค่าธรรมเนียม ให้เลือกบัญชีสำหรับธุรกรรมค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4569b-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="4569b-141">ในฟิลด์บัญชียอดกำไร ให้เลือกบัญชีสำหรับธุรกรรมกำไร</span><span class="sxs-lookup"><span data-stu-id="4569b-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="4569b-142">ในฟิลด์บัญชีการชำระบัญชี ให้เลือกบัญชีการชำระบัญชีสำหรับธุรกรรมหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="4569b-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="4569b-143">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="4569b-143">Click Save.</span></span>
11. <span data-ttu-id="4569b-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4569b-144">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]