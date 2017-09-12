--- 
title: "ตั้งค่ารหัสภาษีขาย"
description: "รหัสภาษีขายจะถูกสร้างขึ้นสำหรับแต่ละภาษีทางอ้อมหรือภาษีที่นิติบุคคลมีหน้าที่ต้องคำนวณ เรียกเก็บ และชำระให้แก่หน่วยงานจัดเก็บภาษีขาย "
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c8f1eea5e257ccb8f2e7fe900e2c8c68bdd5148f
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="915c1-103">ตั้งค่ารหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="915c1-103">Set up sales tax codes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="915c1-104">รหัสภาษีขายจะถูกสร้างขึ้นสำหรับแต่ละภาษีทางอ้อมหรือภาษีที่นิติบุคคลมีหน้าที่ต้องคำนวณ เรียกเก็บ และชำระให้แก่หน่วยงานจัดเก็บภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="915c1-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="915c1-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="915c1-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="915c1-106">ไปที่ภาษี > ภาษีทางอ้อม > ภาษีขาย > รหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="915c1-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="915c1-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="915c1-107">Click New.</span></span>
3. <span data-ttu-id="915c1-108">ในฟิลด์รหัสภาษีขาย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="915c1-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="915c1-109">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="915c1-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="915c1-110">เลือกรอบระยะเวลาการชำระเงินเพื่อระบุหน่วยงานที่เก็บภาษีขาย และช่วงเวลาใดที่ภาษีขายนี้จำเป็นต้องมีการรายงานและการชำระ</span><span class="sxs-lookup"><span data-stu-id="915c1-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="915c1-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="915c1-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="915c1-112">เลือกกลุ่มการลงรายการบัญชีแยกประเภทเพื่อระบุบัญชีหลักที่จะลงรายการบัญชีภาษีขายในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="915c1-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="915c1-113">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="915c1-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="915c1-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="915c1-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="915c1-115">ขยายแท็บด่วนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="915c1-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="915c1-116">แท็บด่วนการคำนวณจะมีหลายฟิลด์ซึ่งควบคุมวิธีการคำนวณยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="915c1-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="915c1-117">ในบานหน้าต่างการดำเนินการ คลิกที่รหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="915c1-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="915c1-118">คลิกที่ค่า</span><span class="sxs-lookup"><span data-stu-id="915c1-118">Click Values.</span></span>
13. <span data-ttu-id="915c1-119">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="915c1-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="915c1-120">ป้อนค่าสำหรับรหัสภาษีนี้</span><span class="sxs-lookup"><span data-stu-id="915c1-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="915c1-121">ที่แท็บด่วนการคำนวณในฟิลด์จุดเริ่มต้น ถ้ามีการเลือกยอดเงินต่อหน่วย ค่าจะถูกคูณด้วยปริมาณในธุรกรรมเพื่อคำนวณยอดภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="915c1-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="915c1-122">ถ้ารหัสภาษีไม่ใช่ภาษีตามหน่วย ค่าจะเป็นเปอร์เซ็นต์ที่จะใช้ในจุดเริ่มต้นสำหรับรหัสภาษีนี้เพื่อคำนวณยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="915c1-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="915c1-123">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="915c1-123">Click Save.</span></span>
16. <span data-ttu-id="915c1-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="915c1-124">Close the page.</span></span>
17. <span data-ttu-id="915c1-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="915c1-125">Click Save.</span></span>


