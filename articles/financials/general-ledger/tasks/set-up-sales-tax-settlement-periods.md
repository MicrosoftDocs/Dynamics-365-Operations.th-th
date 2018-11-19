--- 
title: "ตั้งค่ารอบระยะเวลาการชำระภาษีขาย"
description: "รอบระยะเวลาการจ่ายภาษีขาย ประกอบด้วยข้อมูลเกี่ยวกับช่วงรอบระยะเวลาสำหรับที่ภาษีขายจำเป็นต้องถูกรายงานและชำระเงิน "
author: twheeloc
manager: AnnBe
ms.date: 10/15/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 61f737edea3af5281b6d2fd7c3c0899082782067
ms.openlocfilehash: 1087ed78e91b487ca7157bfdac1d72ae3f477875
ms.contentlocale: th-th
ms.lasthandoff: 10/17/2018

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="cbffb-103">ตั้งค่ารอบระยะเวลาการชำระภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="cbffb-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cbffb-104">รอบระยะเวลาการจ่ายภาษีขาย ประกอบด้วยข้อมูลเกี่ยวกับช่วงรอบระยะเวลาสำหรับที่ภาษีขายจำเป็นต้องถูกรายงานและชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="cbffb-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="cbffb-105">สามารถดำเนินการกระบวนการชำระเงินได้สำหรับรอบระยะเวลาการชำระเงินสำหรับช่วงวันที่เฉพาะ </span><span class="sxs-lookup"><span data-stu-id="cbffb-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="cbffb-106">รหัสภาษีทั้งหมดที่เชื่อมโยงกับรอบระยะเวลาการจ่ายเงินจะถูกตั้งค่า </span><span class="sxs-lookup"><span data-stu-id="cbffb-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="cbffb-107">ภาระภาษีจะถูกลงรายการบัญชีของผู้จัดจำหน่ายหรือบัญชีแยกประเภททั่วไปอย่างใดอย่างหนึ่ง ขึ้นอยู่กับการตั้งค่าของหน่วยงานจัดเก็บภาษีขายที่เกี่ยวข้อง </span><span class="sxs-lookup"><span data-stu-id="cbffb-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="cbffb-108">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="cbffb-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="cbffb-109">ไปที่ภาษี > ภาษีทางอ้อม > ภาษีขาย > ระยะเวลาการชำระภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="cbffb-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="cbffb-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="cbffb-110">Click New.</span></span>
3. <span data-ttu-id="cbffb-111">ในฟิลด์ระยะเวลาการชำระเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="cbffb-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="cbffb-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="cbffb-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cbffb-113">ในฟิลด์หน่วยงานจัดเก็บภาษี ให้เลือกหน่วยงานจัดเก็บภาษีที่ได้รับรายงานและการชำระเงินที่สร้างขึ้นสำหรับรอบระยะเวลาการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="cbffb-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="cbffb-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="cbffb-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="cbffb-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cbffb-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cbffb-116">ในฟิลด์เงื่อนไขการชำระเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="cbffb-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cbffb-117">หน่วยงานจัดเก็บภาษีขายที่เกี่ยวข้องสามารถถูกตั้งค่าให้เป็นผู้จัดจำหน่ายและการชำระภาษีขายจะสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายคงค้าง </span><span class="sxs-lookup"><span data-stu-id="cbffb-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="cbffb-118">เงื่อนไขการชำระเงินจะกำหนดวันครบกำหนดชำระสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายคงค้าง</span><span class="sxs-lookup"><span data-stu-id="cbffb-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="cbffb-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="cbffb-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="cbffb-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cbffb-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="cbffb-121">เลือกชนิดสำหรับช่วงรอบระยะเวลาการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="cbffb-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="cbffb-122">ป้อนหมายเลขของหน่วยช่วงรอบระยะเวลาต่อรอบระยะเวลา </span><span class="sxs-lookup"><span data-stu-id="cbffb-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="cbffb-123">ตัวอย่างเช่น หนึ่งไตรมาสมี 3 เดือน</span><span class="sxs-lookup"><span data-stu-id="cbffb-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="cbffb-124">เลือกหรือยกเลิกการใช้การประมวลผลชุดงานสำหรับกล่องกาเครื่องหมายการชำระภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="cbffb-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="cbffb-125">กระบวนการชำระสำหรับรอบระยะเวลาการชำระสามารถประมวลผลเป็นชุดงานในเบื้องหลัง </span><span class="sxs-lookup"><span data-stu-id="cbffb-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="cbffb-126">ซึ่งเหมาะสำหรับธุรกรรมภาษีจำนวนมากภายในช่วงรอบระยะเวลาหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cbffb-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="cbffb-127">เลือก หรือล้างกล่องกาเครื่องหมายการป้องกันไม่ให้สร้างธุรกรรมออฟเซ็ตภาษี</span><span class="sxs-lookup"><span data-stu-id="cbffb-127">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="cbffb-128">โดยค่าเริ่มต้น ระบบจะสร้างธุรกรรมออฟเซ็ตภาษีในระหว่างกระบวนการชำระเงิน ซึ่งทำให้เกิดปัญหาประสิทธิภาพการทำงาน ถ้ามีธุรกรรมภาษีจำนวนมากภายในช่วงรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="cbffb-128">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="cbffb-129">เลือกกล่องกาเครื่องหมายนี้เพื่อป้องกันไม่ให้สร้างธุรกรรมออฟเซ็ตภาษี</span><span class="sxs-lookup"><span data-stu-id="cbffb-129">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="cbffb-130">ขยายแท็บช่วงรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="cbffb-130">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="cbffb-131">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="cbffb-131">Click Add.</span></span>
17. <span data-ttu-id="cbffb-132">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cbffb-132">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="cbffb-133">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cbffb-133">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="cbffb-134">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cbffb-134">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="cbffb-135">คลิกช่วงรอบระยะเวลาใหม่</span><span class="sxs-lookup"><span data-stu-id="cbffb-135">Click New period interval.</span></span>
    * <span data-ttu-id="cbffb-136">เมื่อมีการป้อนรอบระยะเวลาแรก รอบระยะเวลาใหม่จะถูกสร้างโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="cbffb-136">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="cbffb-137">คุณสามารถกลับมาและเพิ่มช่วงรอบระยะเวลาใหม่ตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="cbffb-137">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="cbffb-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cbffb-138">Close the page.</span></span>


