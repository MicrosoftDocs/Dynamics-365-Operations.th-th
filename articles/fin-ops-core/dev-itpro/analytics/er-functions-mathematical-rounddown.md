---
title: ฟังก์ชัน ROUNDDOWN ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ROUNDDOWN
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9221476c1c12a7cc3fe2367cdee3ad44e5cbe381
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686893"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="4d6b7-103">ฟังก์ชัน ROUNDDOWN ER</span><span class="sxs-lookup"><span data-stu-id="4d6b7-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d6b7-104">ฟังก์ชัน `ROUNDDOWN` ส่งคืนหมายเลขที่ระบุเป็นค่า *จริง* หลังจากที่ได้ถูกปัดเศษลงเป็นจำนวนทศนิยมที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="4d6b7-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d6b7-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="4d6b7-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="4d6b7-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="4d6b7-106">Arguments</span></span>

<span data-ttu-id="4d6b7-107">`number`: *จริง*</span><span class="sxs-lookup"><span data-stu-id="4d6b7-107">`number`: *Real*</span></span>

<span data-ttu-id="4d6b7-108">ค่าตัวเลขที่ต้องถูกปัดเศษลง</span><span class="sxs-lookup"><span data-stu-id="4d6b7-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="4d6b7-109">`decimals`: *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="4d6b7-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="4d6b7-110">ค่าของข้อความที่แสดงจำนวนของตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="4d6b7-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="4d6b7-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="4d6b7-111">Return values</span></span>

<span data-ttu-id="4d6b7-112">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="4d6b7-112">*Real*</span></span>

<span data-ttu-id="4d6b7-113">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="4d6b7-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4d6b7-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4d6b7-114">Usage notes</span></span>

<span data-ttu-id="4d6b7-115">ฟังก์ชันนี้ทำหน้าที่เหมือนกับ [ปัดเศษ](er-functions-mathematical-round.md) แต่จะปัดเศษจำนวนที่ระบุลงเสมอ (ไปยังศูนย์)</span><span class="sxs-lookup"><span data-stu-id="4d6b7-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="4d6b7-116">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="4d6b7-116">Example 1</span></span>

<span data-ttu-id="4d6b7-117">`ROUNDDOWN (1200.767, 2)` ปัดเศษลงเป็นทศนิยมสองตำแหน่ง และส่งกลับ **1200.76**</span><span class="sxs-lookup"><span data-stu-id="4d6b7-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="4d6b7-118">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="4d6b7-118">Example 2</span></span>

<span data-ttu-id="4d6b7-119">`ROUNDDOWN (1700.767, -3)` ปัดเศษลงเป็นผลคูณที่ใกล้ที่สุดของ 1,000 และส่งกลับ **1000**</span><span class="sxs-lookup"><span data-stu-id="4d6b7-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d6b7-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4d6b7-120">Additional resources</span></span>

[<span data-ttu-id="4d6b7-121">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="4d6b7-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
