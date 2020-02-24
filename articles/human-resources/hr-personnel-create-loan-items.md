---
title: สร้างสินค้าที่ให้กู้ยืม
description: 'สินค้าที่ให้กู้ยืมเป็นเรกคอร์ดที่ช่วยให้คุณติดตามสินค้าที่มีอยู่จริง เช่นโทรศัพท์หรือคอมพิวเตอร์ ที่บริษัทของคุณให้ยืมกับผู้ปฏิบัติงาน '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5245b82c81178ff41d5351cd8f73650aa497d555
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010710"
---
# <a name="create-loan-items"></a><span data-ttu-id="70845-103">สร้างสินค้าที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="70845-103">Create loan items</span></span>



<span data-ttu-id="70845-104">สินค้าที่ให้กู้ยืมเป็นเรกคอร์ดที่ช่วยให้คุณติดตามสินค้าที่มีอยู่จริง เช่นโทรศัพท์หรือคอมพิวเตอร์ ที่บริษัทของคุณให้ยืมกับผู้ปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="70845-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="70845-105">สินค้าที่มีอยู่จริงแต่ละรายการต้องมีสินค้าให้กู้ยืมที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="70845-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="70845-106">แต่ละเรกคอร์ดสินค้ากู้ยืมควรอธิบายถึงสิ่งที่กู้ยืม ผู้ที่รับผิดชอบต่อการกู้ยืม และจำนวนวันที่สามารถกู้ยืมสินค้าได้ </span><span class="sxs-lookup"><span data-stu-id="70845-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="70845-107">คุณสามารถสร้างรายการสินค้ากู้ยืมได้หลายรายการในเวลาเดียวกัน เช่น กุญแจ บัตรผ่าน หรือ เครื่องแบบพนักงาน </span><span class="sxs-lookup"><span data-stu-id="70845-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="70845-108">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="70845-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="70845-109">สร้างชนิดของการกู้ยืม</span><span class="sxs-lookup"><span data-stu-id="70845-109">Create Loan types</span></span>
1. <span data-ttu-id="70845-110">ไปที่ ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > สินค้าที่ให้กู้ยืม > อุปกรณ์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="70845-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="70845-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="70845-111">Click New.</span></span>
3. <span data-ttu-id="70845-112">ในฟิลด์ชนิดของเงินกู้ยืม ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="70845-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="70845-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="70845-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="70845-114">ป้อนจำนวนวัน ที่รายการถูกกำหนดให้กับชนิดของการยืมที่สามารถพ้นกำหนด</span><span class="sxs-lookup"><span data-stu-id="70845-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="70845-115">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="70845-115">Click Save.</span></span>
7. <span data-ttu-id="70845-116">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="70845-116">Close the page.</span></span>
8. <span data-ttu-id="70845-117">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="70845-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="70845-118">สร้างสินค้าที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="70845-118">Create Loan items</span></span>
1. <span data-ttu-id="70845-119">ไปที่ ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > สินค้าที่ให้กู้ยืม > สินค้าที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="70845-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="70845-120">คลิก สร้างสินค้าที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="70845-120">Click Create loan items.</span></span>
3. <span data-ttu-id="70845-121">ในฟิลด์จำนวน ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="70845-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="70845-122">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="70845-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="70845-123">ในฟิลด์ชนิดของการยืม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="70845-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="70845-124">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="70845-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="70845-125">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="70845-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="70845-126">ป้อนจำนวนวันที่สามารถกู้ยืมสินค้าได้ </span><span class="sxs-lookup"><span data-stu-id="70845-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="70845-127">ค่าเริ่มต้นสำหรับฟิลด์การส่งคืนที่วางแผนไว้บนหน้าอุปกรณ์ที่ให้ยืมจะถูกคำนวณ ณ วันปัจจุบันบวกด้วยตัวเลขนี้</span><span class="sxs-lookup"><span data-stu-id="70845-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="70845-128">ในฟิลด์ผู้รับผิดชอบ คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="70845-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="70845-129">คลิก เลือก</span><span class="sxs-lookup"><span data-stu-id="70845-129">Click Select.</span></span>
11. <span data-ttu-id="70845-130">ในฟิลด์ค่าเริ่มต้น ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="70845-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="70845-131">ในฟิลด์ช่วงเวลา ให้ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="70845-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="70845-132">ในฟิลด์รูแแบบ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="70845-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="70845-133">ตัวอย่างเช่น ถ้าหมายเลขเริ่มต้นสำหรับสินค้าที่ให้กู้ยืมคือ 10 ป้อนสัญลักษณ์สองตัวเลขในฟิลด์รูปแบบ</span><span class="sxs-lookup"><span data-stu-id="70845-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="70845-134">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="70845-134">Click OK.</span></span>
15. <span data-ttu-id="70845-135">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="70845-135">Refresh the page.</span></span>

