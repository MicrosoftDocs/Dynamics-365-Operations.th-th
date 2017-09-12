--- 
title: "ข้อมูลใบแจ้งหนี้ที่สำคัญในบัญชีเจ้าหนี้โดยใช้สมุดรายวันการอนุมัติ"
description: "คู่มือของงานนี้จะแสดงวิธีการใช้ทะเบียนใบแจ้งหนี้เพื่อสร้างใบแจ้งหนี้ และใช้สมุดรายวันการอนุมัติสำหรับการอัพเดตบัญชีค่าใช้จ่าย"
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 604345d357e5019e334017b2b6d0413f40818acc
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="6e580-103">ข้อมูลใบแจ้งหนี้ที่สำคัญในบัญชีเจ้าหนี้โดยใช้สมุดรายวันการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="6e580-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e580-104">คู่มือของงานนี้จะแสดงวิธีการใช้ทะเบียนใบแจ้งหนี้เพื่อสร้างใบแจ้งหนี้ และใช้สมุดรายวันการอนุมัติสำหรับการอัพเดตบัญชีค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="6e580-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="6e580-105">สร้างและลงรายการบัญชีและใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6e580-105">Create and post and invoice</span></span>
1. <span data-ttu-id="6e580-106">ไปที่บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > ทะเบียนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6e580-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="6e580-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6e580-107">Click New.</span></span>
3. <span data-ttu-id="6e580-108">เลือกชื่อทะเบียนใบแจ้งหนี้ที่คุณต้องการจะใช้</span><span class="sxs-lookup"><span data-stu-id="6e580-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="6e580-109">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6e580-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6e580-110">คลิกที่รายการเพื่อเปิดการลงทะเบียนและป้อนรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="6e580-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="6e580-111">เลือกผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="6e580-111">Select a vendor.</span></span> <span data-ttu-id="6e580-112">ตัวอย่างเช่น ป้อนหรือเลือก US-104</span><span class="sxs-lookup"><span data-stu-id="6e580-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="6e580-113">ในฟิลด์ใบแจ้งหนี้ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6e580-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="6e580-114">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6e580-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="6e580-115">ในฟิลด์เครดิต ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="6e580-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="6e580-116">ในฟิลด์อนุมัติโดย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="6e580-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="6e580-117">ให้เน้นที่ผู้อนุมัติและคลิกที่เลือกเพื่อเลือกผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="6e580-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="6e580-118">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="6e580-118">Click Post.</span></span>
13. <span data-ttu-id="6e580-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e580-119">Close the page.</span></span>
14. <span data-ttu-id="6e580-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e580-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="6e580-121">อนุมัติใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6e580-121">Approve an invoice</span></span>
1. <span data-ttu-id="6e580-122">ไปที่บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > การอนุมัติใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6e580-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="6e580-123">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6e580-123">Click New.</span></span>
3. <span data-ttu-id="6e580-124">เลือกชื่อสมุดรายวันการอนุมัติใบแจ้งหนี้ที่คุณต้องการจะใช้</span><span class="sxs-lookup"><span data-stu-id="6e580-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="6e580-125">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6e580-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6e580-126">คลิกที่รายการเพื่อแสดงหน้าที่คุณจะสามารถเลือกใบแจ้งหนี้ที่คุณต้องการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="6e580-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="6e580-127">เลือกค้นหาใบสำคัญเพื่อแสดงใบแจ้งหนี้ทั้งหมดที่พร้อมสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="6e580-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="6e580-128">ทำเครื่องหมายใบแจ้งหนี้ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6e580-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="6e580-129">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="6e580-129">Click Select.</span></span>
    * <span data-ttu-id="6e580-130">ใบสำคัญที่คุณเลือกไว้ด้านบนจะถูกย้ายไปยังรายการนี้หลังจากที่คุณทำการเลือก</span><span class="sxs-lookup"><span data-stu-id="6e580-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="6e580-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6e580-131">Click OK.</span></span>
10. <span data-ttu-id="6e580-132">คลิกที่ฟิลด์หมายเลขบัญชีเพื่อเพิ่มบัญชีค่าใช้จ่ายในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6e580-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="6e580-133">ป้อนหมายเลขบัญชีและปิดฟิลด์ </span><span class="sxs-lookup"><span data-stu-id="6e580-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="6e580-134">ตัวอย่างเช่น ป้อน 600120</span><span class="sxs-lookup"><span data-stu-id="6e580-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="6e580-135">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="6e580-135">Click Post.</span></span>
13. <span data-ttu-id="6e580-136">คลิกใบสำคัญเพื่อดูรายการที่ลงรายการบัญชีไว้</span><span class="sxs-lookup"><span data-stu-id="6e580-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="6e580-137">บัญชีการอนุมัติใบแจ้งหนี้ที่ค้างอยู่เป็นการกลับรายการและแทนที่ด้วยบัญชีค่าใช้จ่ายจริง</span><span class="sxs-lookup"><span data-stu-id="6e580-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  


