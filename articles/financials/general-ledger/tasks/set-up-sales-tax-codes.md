---
title: ตั้งค่ารหัสภาษีขาย
description: 'รหัสภาษีขายจะถูกสร้างขึ้นสำหรับแต่ละภาษีทางอ้อมหรือภาษีที่นิติบุคคลมีหน้าที่ต้องคำนวณ เรียกเก็บ และชำระให้แก่หน่วยงานจัดเก็บภาษีขาย '
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f29442c2ef2e3d0008a74298fda218e4cbd93f8e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "349181"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="f2c11-103">ตั้งค่ารหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="f2c11-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2c11-104">รหัสภาษีขายจะถูกสร้างขึ้นสำหรับแต่ละภาษีทางอ้อมหรือภาษีที่นิติบุคคลมีหน้าที่ต้องคำนวณ เรียกเก็บ และชำระให้แก่หน่วยงานจัดเก็บภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="f2c11-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="f2c11-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="f2c11-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="f2c11-106">ไปที่ภาษี > ภาษีทางอ้อม > ภาษีขาย > รหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="f2c11-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="f2c11-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f2c11-107">Click New.</span></span>
3. <span data-ttu-id="f2c11-108">ในฟิลด์รหัสภาษีขาย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f2c11-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="f2c11-109">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="f2c11-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f2c11-110">เลือกรอบระยะเวลาการชำระเงินเพื่อระบุหน่วยงานที่เก็บภาษีขาย และช่วงเวลาใดที่ภาษีขายนี้จำเป็นต้องมีการรายงานและการชำระ</span><span class="sxs-lookup"><span data-stu-id="f2c11-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="f2c11-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f2c11-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f2c11-112">เลือกกลุ่มการลงรายการบัญชีแยกประเภทเพื่อระบุบัญชีหลักที่จะลงรายการบัญชีภาษีขายในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="f2c11-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="f2c11-113">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f2c11-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f2c11-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f2c11-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="f2c11-115">ขยายแท็บด่วนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="f2c11-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="f2c11-116">แท็บด่วนการคำนวณจะมีหลายฟิลด์ซึ่งควบคุมวิธีการคำนวณยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="f2c11-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="f2c11-117">ในบานหน้าต่างการดำเนินการ คลิกที่รหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="f2c11-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="f2c11-118">คลิกที่ค่า</span><span class="sxs-lookup"><span data-stu-id="f2c11-118">Click Values.</span></span>
13. <span data-ttu-id="f2c11-119">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f2c11-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="f2c11-120">ป้อนค่าสำหรับรหัสภาษีนี้</span><span class="sxs-lookup"><span data-stu-id="f2c11-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="f2c11-121">ที่แท็บด่วนการคำนวณในฟิลด์จุดเริ่มต้น ถ้ามีการเลือกยอดเงินต่อหน่วย ค่าจะถูกคูณด้วยปริมาณในธุรกรรมเพื่อคำนวณยอดภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="f2c11-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="f2c11-122">ถ้ารหัสภาษีไม่ใช่ภาษีตามหน่วย ค่าจะเป็นเปอร์เซ็นต์ที่จะใช้ในจุดเริ่มต้นสำหรับรหัสภาษีนี้เพื่อคำนวณยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="f2c11-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="f2c11-123">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f2c11-123">Click Save.</span></span>
16. <span data-ttu-id="f2c11-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f2c11-124">Close the page.</span></span>
17. <span data-ttu-id="f2c11-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f2c11-125">Click Save.</span></span>

