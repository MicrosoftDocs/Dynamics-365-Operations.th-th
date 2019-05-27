---
title: ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย
description: 'คุณสามารถลงทะเบียนรายละเอียดเกี่ยวกับเช็คลงวันที่ล่วงหน้าก่อนที่จะออกเช็คให้กับผู้จัดจำหน่ายโดยการใช้ใบสำคัญสมุดรายวัน '
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5788948c40f20e686565198c84facd68a935d9c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566075"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="c4ceb-103">ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c4ceb-103">Register and post a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4ceb-104">คุณสามารถลงทะเบียนรายละเอียดเกี่ยวกับเช็คลงวันที่ล่วงหน้าก่อนที่จะออกเช็คให้กับผู้จัดจำหน่ายโดยการใช้ใบสำคัญสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="c4ceb-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="c4ceb-105">คุณสามารถลงรายการบัญชีเช็คลงวันที่ล่วงหน้าและสร้างธุรกรรมทางการเงิน </span><span class="sxs-lookup"><span data-stu-id="c4ceb-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="c4ceb-106">คุณต้องดำเนินงานต่อไปนี้ให้เสร็จสมบูรณ์ก่อนที่คุณจะลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าจากผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="c4ceb-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="c4ceb-107">ให้ตั้งค่าวิธีการชำระเงินสำหรับเช็คลงวันที่ล่วงหน้าในหน้าเงินสดและการจัดการธนาคาร </span><span class="sxs-lookup"><span data-stu-id="c4ceb-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="c4ceb-108">บทบาทสำหรับกระบวนงานนี้คือฝ่ายการเงิน </span><span class="sxs-lookup"><span data-stu-id="c4ceb-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="c4ceb-109">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="c4ceb-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c4ceb-110">ไปที่ บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c4ceb-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="c4ceb-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4ceb-111">Click New.</span></span>
3. <span data-ttu-id="c4ceb-112">ในฟิลด์ชื่อ ให้พิมพ์ 'VendPay'</span><span class="sxs-lookup"><span data-stu-id="c4ceb-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="c4ceb-113">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="c4ceb-113">Click Lines.</span></span>
5. <span data-ttu-id="c4ceb-114">ในฟิลด์บัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c4ceb-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="c4ceb-115">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4ceb-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="c4ceb-116">ในฟิลด์เดบิต ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c4ceb-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="c4ceb-117">ในฟิลด์วิธีการชำระเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c4ceb-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c4ceb-118">เลือกวิธีการชำระเงินสำหรับเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="c4ceb-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="c4ceb-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c4ceb-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c4ceb-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4ceb-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="c4ceb-121">คลิกแท็บเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="c4ceb-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="c4ceb-122">ในฟิลด์หมายเลขเช็ค ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c4ceb-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="c4ceb-123">ให้ป้อนหรือแก้ไข หมายเลขของเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="c4ceb-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="c4ceb-124">ในฟิลด์ชื่อธนาคารผู้ออก ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c4ceb-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="c4ceb-125">ป้อนรายละเอียดธนาคารสำหรับธนาคารผู้เปิดแอลซี</span><span class="sxs-lookup"><span data-stu-id="c4ceb-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="c4ceb-126">คลิกแท็บรายการ</span><span class="sxs-lookup"><span data-stu-id="c4ceb-126">Click the List tab.</span></span>
15. <span data-ttu-id="c4ceb-127">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4ceb-127">Click Post.</span></span>
16. <span data-ttu-id="c4ceb-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c4ceb-128">Close the page.</span></span>
17. <span data-ttu-id="c4ceb-129">คลิกแท็บเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="c4ceb-129">Click the Postdated checks tab.</span></span>

