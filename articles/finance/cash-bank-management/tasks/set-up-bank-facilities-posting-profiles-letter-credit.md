---
title: ตั้งค่าสินเชื่อธนาคารและการลงรายการบัญชีโพรไฟล์สำหรับเลตเตอร์ออฟเครดิต
description: กระบวนงานนี้นำไปสู่การสร้างสินเชื่อธนาคารและการลงรายการบัญชีโพรไฟล์ที่จำเป็นสำหรับการดำเนินการเลตเตอร์ออฟเครดิต
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
ms.openlocfilehash: 7e72847b9046968c87d9602e141bae6c603c1c63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976349"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="0e16f-103">ตั้งค่าสินเชื่อธนาคารและการลงรายการบัญชีโพรไฟล์สำหรับเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="0e16f-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e16f-104">กระบวนงานนี้นำไปสู่การสร้างสินเชื่อธนาคารและการลงรายการบัญชีโพรไฟล์ที่จำเป็นสำหรับการดำเนินการเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="0e16f-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="0e16f-105">งานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="0e16f-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="0e16f-106">พารามิเตอร์บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="0e16f-106">General ledger parameter</span></span>
1. <span data-ttu-id="0e16f-107">ไปที่การจัดการเงินสดและธนาคาร > การตั้งค่า > พารามิเตอร์การจัดการเงินสดและธนาคาร</span><span class="sxs-lookup"><span data-stu-id="0e16f-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="0e16f-108">ขยายส่วนเอกสารธนาคาร</span><span class="sxs-lookup"><span data-stu-id="0e16f-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="0e16f-109">เลือกตัวเลือกการเปิดใช้งานเลตเตอร์ออฟเครดิตสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="0e16f-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="0e16f-110">เลือกตัวเลือกการเปิดใช้งานเลตเตอร์ออฟเครดิตสำหรับการส่งออก</span><span class="sxs-lookup"><span data-stu-id="0e16f-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="0e16f-111">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0e16f-111">Click Save.</span></span>
6. <span data-ttu-id="0e16f-112">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0e16f-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="0e16f-113">สร้างสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="0e16f-113">Create Bank facility</span></span>
1. <span data-ttu-id="0e16f-114">ไปที่การจัดการเงินสดและธนาคาร > การตั้งค่า > สินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="0e16f-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="0e16f-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0e16f-115">Click New.</span></span>
3. <span data-ttu-id="0e16f-116">ในฟิลด์กลุ่มสินเชื่อธนาคาร ให้เลือกชื่อกลุ่มสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="0e16f-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="0e16f-117">ในฟิลด์คำอธิบาย ให้ป้อนคำอธิบายของกลุ่มสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="0e16f-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="0e16f-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0e16f-118">Click Save.</span></span>
6. <span data-ttu-id="0e16f-119">คลิกแท็บชนิดของสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="0e16f-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="0e16f-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0e16f-120">Click New.</span></span>
8. <span data-ttu-id="0e16f-121">ในฟิลด์ชนิดสินเชื่อ ให้พิมพ์รหัสเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="0e16f-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="0e16f-122">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0e16f-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="0e16f-123">ในฟิลด์กลุ่มสินเชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0e16f-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="0e16f-124">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0e16f-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="0e16f-125">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0e16f-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="0e16f-126">ในฟิลด์ลักษณะสินเชื่อ ให้เลือกลักษณะของสินเชื่อสำหรับสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="0e16f-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="0e16f-127">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0e16f-127">Click Save.</span></span>
15. <span data-ttu-id="0e16f-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0e16f-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="0e16f-129">โพรไฟล์การลงรายการบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="0e16f-129">Bank posting profile</span></span>
1. <span data-ttu-id="0e16f-130">ไปที่การจัดการเงินสดและธนาคาร > การตั้งค่า > โพรไฟล์การลงรายการบัญชีเอกสารธนาคาร</span><span class="sxs-lookup"><span data-stu-id="0e16f-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="0e16f-131">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0e16f-131">Click New.</span></span>
3. <span data-ttu-id="0e16f-132">ในฟิลด์หมายเลขบัญชี/กลุ่ม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0e16f-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0e16f-133">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0e16f-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0e16f-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0e16f-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0e16f-135">เลือกบัญชีหลักสำหรับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0e16f-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="0e16f-136">บัญชีนี้จะใช้เมื่อมีการคำนวณการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="0e16f-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="0e16f-137">ในฟิลด์บัญชีค่าธรรมเนียม ให้เลือกบัญชีสำหรับธุรกรรมค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0e16f-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="0e16f-138">ในฟิลด์บัญชียอดกำไร ให้เลือกบัญชีสำหรับธุรกรรมกำไร</span><span class="sxs-lookup"><span data-stu-id="0e16f-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="0e16f-139">บัญชีนี้จะถูกเดบิตเมื่อลงรายการบัญชีกำไรเปิด และถูกเครดิตเมื่อลงรายการบัญชีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0e16f-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="0e16f-140">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0e16f-140">Click Save.</span></span>

