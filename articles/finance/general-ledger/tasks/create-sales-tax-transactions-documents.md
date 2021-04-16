---
title: สร้างเอกสารเกี่ยวกับธุรกรรมภาษีขาย
description: 'มีการคำนวณภาษีขายบนเอกสารโดยการกำหนดกลุ่มภาษีขายและกลุ่มภาษีขายตามประเภทสินค้าบนรายการเอกสาร '
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 061949dedde763c188e13c07cec750895cbef175
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836996"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="2e3bb-103">สร้างเอกสารเกี่ยวกับธุรกรรมภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="2e3bb-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e3bb-104">มีการคำนวณภาษีขายบนเอกสารโดยการกำหนดกลุ่มภาษีขายและกลุ่มภาษีขายตามประเภทสินค้าบนรายการเอกสาร </span><span class="sxs-lookup"><span data-stu-id="2e3bb-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="2e3bb-105">ค่าเริ่มต้นเหล่านี้จากข้อมูลหลัก แต่สามารถเปลี่ยนได้ด้วยตนเองหากจำเป็น </span><span class="sxs-lookup"><span data-stu-id="2e3bb-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="2e3bb-106">สามารถตรวจสอบภาษีขายที่คำนวณได้ในระดับรายการและเอกสาร </span><span class="sxs-lookup"><span data-stu-id="2e3bb-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="2e3bb-107">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="2e3bb-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="2e3bb-108">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2e3bb-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="2e3bb-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2e3bb-109">Click New.</span></span>
3. <span data-ttu-id="2e3bb-110">ในฟิลด์บัญชีลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2e3bb-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2e3bb-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2e3bb-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2e3bb-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2e3bb-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2e3bb-113">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2e3bb-113">Click OK.</span></span>
7. <span data-ttu-id="2e3bb-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2e3bb-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="2e3bb-115">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2e3bb-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="2e3bb-116">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2e3bb-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="2e3bb-117">ในฟิลด์ราคาต่อหน่วย ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="2e3bb-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="2e3bb-118">ขยายหรือยุบส่วนรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="2e3bb-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="2e3bb-119">คลิกแท็บการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="2e3bb-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="2e3bb-120">ในฟิลด์กลุ่มภาษีขายตามประเภทสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2e3bb-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="2e3bb-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2e3bb-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="2e3bb-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2e3bb-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="2e3bb-123">คลิกข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="2e3bb-123">Click Financials.</span></span>
17. <span data-ttu-id="2e3bb-124">คลิกภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="2e3bb-124">Click Sales tax.</span></span>
18. <span data-ttu-id="2e3bb-125">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2e3bb-125">Click OK.</span></span>
19. <span data-ttu-id="2e3bb-126">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="2e3bb-126">Click Add line.</span></span>
20. <span data-ttu-id="2e3bb-127">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2e3bb-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="2e3bb-128">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2e3bb-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="2e3bb-129">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2e3bb-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="2e3bb-130">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2e3bb-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="2e3bb-131">ในฟิลด์ราคาต่อหน่วย ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="2e3bb-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="2e3bb-132">ในฟิลด์กลุ่มภาษีขายตามประเภทสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2e3bb-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="2e3bb-133">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2e3bb-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="2e3bb-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2e3bb-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="2e3bb-135">ในบานหน้าต่างการดำเนินการ คลิกขาย</span><span class="sxs-lookup"><span data-stu-id="2e3bb-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="2e3bb-136">คลิกภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="2e3bb-136">Click Sales tax.</span></span>
30. <span data-ttu-id="2e3bb-137">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2e3bb-137">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]