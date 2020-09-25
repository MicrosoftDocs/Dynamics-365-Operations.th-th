---
title: ฟังก์ชัน ROUNDAMOUNT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ ROUNDAMOUNT (ER)
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31a28279037ee6bfecd69b9d1e816afbd0de7894
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743986"
---
# <a name="roundamount-er-function"></a><span data-ttu-id="d370a-103">ฟังก์ชัน ROUNDAMOUNT ER</span><span class="sxs-lookup"><span data-stu-id="d370a-103">ROUNDAMOUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d370a-104">ฟังก์ชัน `ROUNDAMOUNT` ส่งกลับค่า *จำนวนจริง* เป็นผลลัพธ์ของการปัดเศษของหมายเลขที่ระบุเป็นผลคูณที่ใกล้เคียงที่สุดของหมายเลขอื่นตามกฎการปัดเศษที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="d370a-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="d370a-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="d370a-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="d370a-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="d370a-106">Arguments</span></span>

<span data-ttu-id="d370a-107">`number`: *เลขจำนวนเต็ม* หรือ *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="d370a-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="d370a-108">ค่าตัวเลขที่ต้องถูกปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="d370a-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="d370a-109">`decimals`: *เลขจำนวนเต็ม* หรือ *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="d370a-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="d370a-110">หมายเลขที่ค่าของพารามิเตอร์ `number` ต้องถูกปัดเศษเป็นผลคูณ</span><span class="sxs-lookup"><span data-stu-id="d370a-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="d370a-111">`round rule`: *ค่า Enum*</span><span class="sxs-lookup"><span data-stu-id="d370a-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="d370a-112">ค่าการแจงนับของการแจงนับ **RoundOffType** ที่กำหนดกฎการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="d370a-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="d370a-113">การแจงนับนี้มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d370a-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="d370a-114">ปกติ (ปกติ)</span><span class="sxs-lookup"><span data-stu-id="d370a-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="d370a-115">ลงข้างล่าง (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="d370a-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="d370a-116">การปัดเศษขึ้น (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="d370a-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="d370a-117">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="d370a-117">Return values</span></span>

<span data-ttu-id="d370a-118">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="d370a-118">*Real*</span></span>

<span data-ttu-id="d370a-119">ค่าตัวเลขที่เป็นผลลัพธ์คือผลคูณของค่าที่ระบุโดยพารามิเตอร์ `decimals` และใกล้เคียงที่สุดกับค่าที่ระบุโดยพารามิเตอร์ `number`</span><span class="sxs-lookup"><span data-stu-id="d370a-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d370a-120">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d370a-120">Usage notes</span></span>

<span data-ttu-id="d370a-121">เมื่อพารามิเตอร์ `number` เป็นศูนย์ ฟังก์ชันนี้จะคืนค่าศูนย์เสมอ</span><span class="sxs-lookup"><span data-stu-id="d370a-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="d370a-122">เมื่อพารามิเตอร์ `decimals` เป็นศูนย์ ฟังก์ชันนี้จะปัดเศษเป็นค่าการปัดเศษเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d370a-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="d370a-123">เมื่อพารามิเตอร์ `round rule` ถูกตั้งค่าเป็น **RoundOffType.Ordinary** ค่าการปัดเศษเริ่มต้นคือ **0.01**</span><span class="sxs-lookup"><span data-stu-id="d370a-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="d370a-124">มิฉะนั้น ค่าการปัดเศษเริ่มต้นคือ **1.0**</span><span class="sxs-lookup"><span data-stu-id="d370a-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="d370a-125">เมื่อพารามิเตอร์ `round rule` ถูกตั้งค่าเป็น **RoundOffType.Ordinary** ฟังก์ชันนี้ปัดเศษเป็นจำนวนที่ปัดเศษที่ใกล้ที่สุด</span><span class="sxs-lookup"><span data-stu-id="d370a-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="d370a-126">เมื่อพารามิเตอร์ `round rule` ถูกตั้งค่าเป็น **RoundOffType.RoundDown** ฟังก์ชันนี้ปัดเศษไปยังศูนย์เป็นจำนวนที่ปัดเศษที่ใกล้ที่สุด</span><span class="sxs-lookup"><span data-stu-id="d370a-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="d370a-127">เมื่อพารามิเตอร์ `round rule` ถูกตั้งค่าเป็น **RoundOffType.RoundUp** ฟังก์ชันนี้ปัดเศษออกจากศูนย์เป็นจำนวนที่ปัดเศษที่ใกล้ที่สุด</span><span class="sxs-lookup"><span data-stu-id="d370a-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="d370a-128">เมื่อพารามิเตอร์ `round rule` ถูกตั้งค่าเป็น **RoundOffType.Ordinary** ฟังก์ชันนี้ทำงานเช่นเดียวกับฟังก์ชัน Excel [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) และฟังก์ชัน X ++ [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round)</span><span class="sxs-lookup"><span data-stu-id="d370a-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="d370a-129">ข้อสังเกต</span><span class="sxs-lookup"><span data-stu-id="d370a-129">Remarks</span></span>

<span data-ttu-id="d370a-130">หากต้องการปัดเศษค่าตัวเลขให้เป็นตำแหน่งทศนิยมที่ระบุ ให้ใช้ฟังก์ชัน [ROUND](er-functions-mathematical-round.md)</span><span class="sxs-lookup"><span data-stu-id="d370a-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="d370a-131">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d370a-131">Example</span></span>

<span data-ttu-id="d370a-132">ถ้าพารามิเตอร์ **model.RoundOff** ถูกตั้งค่าเป็น **RoundOffType.Ordinary** `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` ส่งกลับค่า 7.35</span><span class="sxs-lookup"><span data-stu-id="d370a-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="d370a-133">ถ้าพารามิเตอร์ **model.RoundOff** ถูกตั้งค่าเป็น **RoundOffType.RoundDown** `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` ส่งกลับค่า 7.35</span><span class="sxs-lookup"><span data-stu-id="d370a-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="d370a-134">ถ้าพารามิเตอร์ **model.RoundOff** ถูกตั้งค่าเป็น **RoundOffType.RoundUp** `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` ส่งกลับค่า 8.4</span><span class="sxs-lookup"><span data-stu-id="d370a-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d370a-135">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d370a-135">Additional resources</span></span>

[<span data-ttu-id="d370a-136">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="d370a-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="d370a-137">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="d370a-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)
