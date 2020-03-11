---
title: ฟังก์ชัน ROUND ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ROUND
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
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041618"
---
# <span data-ttu-id="78051-103"><a name="ROUND">ฟังก์ชัน ROUND ER</a></span><span class="sxs-lookup"><span data-stu-id="78051-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78051-104">ฟังก์ชัน `ROUND` ส่งคืนหมายเลขที่ระบุเป็นค่า *จริง* หลังจากที่ได้ถูกปัดเศษเป็นจำนวนทศนิยมที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="78051-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="78051-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="78051-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="78051-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="78051-106">Arguments</span></span>

<span data-ttu-id="78051-107">`number`: *จริง*</span><span class="sxs-lookup"><span data-stu-id="78051-107">`number`: *Real*</span></span>

<span data-ttu-id="78051-108">ค่าตัวเลขที่ต้องถูกปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="78051-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="78051-109">`decimals`: *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="78051-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="78051-110">ค่าของข้อความที่แสดงจำนวนของตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="78051-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="78051-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="78051-111">Return values</span></span>

<span data-ttu-id="78051-112">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="78051-112">*Real*</span></span>

<span data-ttu-id="78051-113">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="78051-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="78051-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="78051-114">Usage notes</span></span>

<span data-ttu-id="78051-115">ถ้าค่าของพารามิเตอร์อาร์กิวเมนต์ `decimals` มากกว่า 0 (ศูนย์) หมายเลขที่ระบุจะถูกปัดเศษเป็นจำนวนทศนิยมหลายตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="78051-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="78051-116">ถ้าค่าของอาร์กิวเมนต์ `decimals` เป็น **0** (ศูนย์) หมายเลขที่ระบุจะถูกปัดเศษเป็นจำนวนเต็มที่ใกล้เคียงที่สุด</span><span class="sxs-lookup"><span data-stu-id="78051-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="78051-117">ถ้าค่าของอาร์กิวเมนต์ `decimals` น้อยกว่า 0 (ศูนย์) หมายเลขที่ระบุจะถูกปัดเศษเป็นจำนวนทศนิยมปัดขึ้น</span><span class="sxs-lookup"><span data-stu-id="78051-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="78051-118">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="78051-118">Example 1</span></span>

<span data-ttu-id="78051-119">`ROUND (1200.767, 2)` ปัดเศษเป็นทศนิยมสองตำแหน่ง และส่งกลับ **1200.77**</span><span class="sxs-lookup"><span data-stu-id="78051-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="78051-120">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="78051-120">Example 2</span></span>

<span data-ttu-id="78051-121">`ROUND (1200.767, -3)` ปัดเศษเป็นผลคูณที่ใกล้ที่สุดของ 1,000 และส่งกลับ **1000**</span><span class="sxs-lookup"><span data-stu-id="78051-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="78051-122">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="78051-122">Additional resources</span></span>

[<span data-ttu-id="78051-123">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="78051-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
