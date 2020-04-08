---
title: ตั้งค่ารหัสภาษีขาย
description: หัวข้อนี้อธิบายวิธีการตั้งค่ารหัสภาษีขายใน Dynamics 365 Finance
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26dc61e340afcf1ce99d37c43d5942dc8792b765
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144754"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="55cbc-103">ตั้งค่ารหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="55cbc-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55cbc-104">หัวข้อนี้อธิบายวิธีการตั้งค่ารหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="55cbc-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="55cbc-105">รหัสภาษีขายจะถูกสร้างขึ้นสำหรับแต่ละภาษีทางอ้อมหรือภาษีที่นิติบุคคลมีหน้าที่ต้องคำนวณ เรียกเก็บ และชำระให้แก่หน่วยงานจัดเก็บภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="55cbc-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="55cbc-106">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="55cbc-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="55cbc-107">ไปที่ **บานหน้าต่างนำทาง > ภาษี > ภาษีทางอ้อม > ภาษีขาย > รหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="55cbc-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="55cbc-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="55cbc-108">Select **New**.</span></span>
3. <span data-ttu-id="55cbc-109">ในฟิลด์ **รหัสภาษีขาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="55cbc-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="55cbc-110">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="55cbc-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="55cbc-111">เลือก **รอบระยะเวลาการชำระเงิน** โดยการเปิดรายการแบบดึงลง เพื่อระบุหน่วยงานที่เก็บภาษีขาย และช่วงเวลาที่ภาษีขายนี้จำเป็นต้องมีการรายงานและการชำระ</span><span class="sxs-lookup"><span data-stu-id="55cbc-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="55cbc-112">เลือก **กลุ่มการลงรายการบัญชีแยกประเภท** เพื่อระบุบัญชีหลักที่จะลงรายการบัญชีภาษีขายในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="55cbc-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="55cbc-113">ขยาย FastTab **การคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="55cbc-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="55cbc-114">นี่รวมถึงฟิลด์หลายฟิลด์ซึ่งควบคุมวิธีการคำนวณยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="55cbc-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="55cbc-115">กรอกข้อมูลในฟิลด์เหล่านี้ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="55cbc-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="55cbc-116">ใน **บานหน้าต่างการดำเนินการ** ที่ด้านบนของอินเทอร์เฟส ให้เลือก **รหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="55cbc-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="55cbc-117">เลือก **ค่า**</span><span class="sxs-lookup"><span data-stu-id="55cbc-117">Select **Values**.</span></span>
10. <span data-ttu-id="55cbc-118">ป้อนค่าสำหรับรหัสภาษีนี้ในคอลัมน์ **ค่า**</span><span class="sxs-lookup"><span data-stu-id="55cbc-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="55cbc-119">บน FastTab **การคำนวณ** ในฟิลด์จุดเริ่มต้น ถ้ามีการเลือกยอดเงินต่อหน่วย ค่าจะถูกคูณด้วยปริมาณในธุรกรรมเพื่อคำนวณยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="55cbc-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="55cbc-120">ถ้ารหัสภาษีไม่ใช่ภาษีตามหน่วย ค่าจะเป็นเปอร์เซ็นต์ที่จะใช้ในจุดเริ่มต้นสำหรับรหัสภาษีนี้เพื่อคำนวณยอดภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="55cbc-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="55cbc-121">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="55cbc-121">Select **Save**.</span></span>
12. <span data-ttu-id="55cbc-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="55cbc-122">Close the page.</span></span>
13. <span data-ttu-id="55cbc-123">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="55cbc-123">Select **Save**.</span></span>

