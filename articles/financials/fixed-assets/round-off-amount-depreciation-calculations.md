---
title: "จำนวนที่ปัดเศษสำหรับการคำนวณค่าเสื่อมราคา"
description: "บทความนี้อธิบายฟิลด์การปัดเศษค่าเสื่อมราคาที่พบในหน้าการตั้งค่าสมุดบัญชี"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0ad57b076542c38d3c29dba4caacf830de6f7200
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="fea86-103">จำนวนที่ปัดเศษสำหรับการคำนวณค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="fea86-103">Round-off amount for depreciation calculations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fea86-104">บทความนี้อธิบายฟิลด์การปัดเศษค่าเสื่อมราคาที่พบในหน้าการตั้งค่าสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="fea86-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="fea86-105">จำนวนค่าเสื่อมราคาที่ปัดเศษถูกตั้งค่าสำหรับแต่ละแบบสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="fea86-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="fea86-106">จำนวนค่าเสื่อมราคาที่ปัดเศษถูกใช้ในค่าเสื่อมราคาของสินทรัพย์ถาวรที่แสดงมูลค่าของค่าเสื่อมราคาในอนาคตและมูลค่าของสินทรัพย์ถาวร และใช้ในข้อเสนอค่าเสื่อมราคาด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="fea86-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="fea86-107">ป้อนจำนวนค่าเสื่อมราคาต่ำสุดที่ได้รับอนุญาตสำหรับสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="fea86-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="fea86-108">โดยไม่คำนึงถึงการปัดเศษที่ถูกตั้งค่าไว้ จำนวนค่าเสื่อมราคาในรอบระยะเวลาของค่าเสื่อมราคาครั้งหลังสุดจะไม่ถูกปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="fea86-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="fea86-109">เมื่อสิ้นสุดของรอบระยะเวลาของค่าเสื่อมราคาครั้งหลังสุด มูลค่าของสินทรัพย์ถาวรต้องเป็น 0 (ศูนย์) หรือมูลค่าซาก ถ้ามูลค่าซากถูกใช้</span><span class="sxs-lookup"><span data-stu-id="fea86-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="fea86-110">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="fea86-110">Example</span></span>

<span data-ttu-id="fea86-111">ค่าเสื่อมราคาที่ไม่มีการปัดเศษถูกคำนวณเป็น 2,444.44</span><span class="sxs-lookup"><span data-stu-id="fea86-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="fea86-112">ดังที่ตารางต่อไปนี้แสดง จำนวนดังกล่าวที่ถูกเสนอนั้นแตกต่างกัน ขึ้นอยู่กับว่าวิธีการปัดเศษถูกตั้งค่าอย่างไร</span><span class="sxs-lookup"><span data-stu-id="fea86-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="fea86-113">วิธีการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="fea86-113">Rounding method</span></span> | <span data-ttu-id="fea86-114">ยอดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="fea86-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="fea86-115">การปัดเศษ 0.1</span><span class="sxs-lookup"><span data-stu-id="fea86-115">Rounding 0.1</span></span>    | <span data-ttu-id="fea86-116">2,444.40</span><span class="sxs-lookup"><span data-stu-id="fea86-116">2,444.40</span></span>            |
| <span data-ttu-id="fea86-117">การปัดเศษ 1.00</span><span class="sxs-lookup"><span data-stu-id="fea86-117">Rounding 1.00</span></span>   | <span data-ttu-id="fea86-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="fea86-118">2,444.00</span></span>            |
| <span data-ttu-id="fea86-119">การปัดเศษ 10.00</span><span class="sxs-lookup"><span data-stu-id="fea86-119">Rounding 10.00</span></span>  | <span data-ttu-id="fea86-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="fea86-120">2,440.00</span></span>            |
| <span data-ttu-id="fea86-121">การปัดเศษ 100.00</span><span class="sxs-lookup"><span data-stu-id="fea86-121">Rounding 100.00</span></span> | <span data-ttu-id="fea86-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="fea86-122">2,400.00</span></span>            |






