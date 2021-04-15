---
title: ฟังก์ชัน ROUND ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ROUND
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ce0f50cd5e544455626862e44b774dba39cf6e57
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744498"
---
# <a name="round-er-function"></a><span data-ttu-id="0246e-103">ฟังก์ชัน ROUND ER</span><span class="sxs-lookup"><span data-stu-id="0246e-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0246e-104">ฟังก์ชัน `ROUND` ส่งคืนหมายเลขที่ระบุเป็นค่า *จริง* หลังจากที่ได้ถูกปัดเศษเป็นจำนวนทศนิยมที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="0246e-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="0246e-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="0246e-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="0246e-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="0246e-106">Arguments</span></span>

<span data-ttu-id="0246e-107">`number`: *จริง*</span><span class="sxs-lookup"><span data-stu-id="0246e-107">`number`: *Real*</span></span>

<span data-ttu-id="0246e-108">ค่าตัวเลขที่ต้องถูกปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="0246e-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="0246e-109">`decimals`: *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="0246e-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="0246e-110">ค่าของข้อความที่แสดงจำนวนของตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="0246e-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="0246e-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="0246e-111">Return values</span></span>

<span data-ttu-id="0246e-112">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="0246e-112">*Real*</span></span>

<span data-ttu-id="0246e-113">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="0246e-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0246e-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0246e-114">Usage notes</span></span>

<span data-ttu-id="0246e-115">ถ้าค่าของพารามิเตอร์อาร์กิวเมนต์ `decimals` มากกว่า 0 (ศูนย์) หมายเลขที่ระบุจะถูกปัดเศษเป็นจำนวนทศนิยมหลายตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="0246e-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="0246e-116">ถ้าค่าของอาร์กิวเมนต์ `decimals` เป็น **0** (ศูนย์) หมายเลขที่ระบุจะถูกปัดเศษเป็นจำนวนเต็มคู่ที่ใกล้เคียงที่สุด</span><span class="sxs-lookup"><span data-stu-id="0246e-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="0246e-117">ถ้าค่าของอาร์กิวเมนต์ `decimals` น้อยกว่า 0 (ศูนย์) หมายเลขที่ระบุจะถูกปัดเศษเป็นจำนวนทศนิยมปัดขึ้น</span><span class="sxs-lookup"><span data-stu-id="0246e-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="0246e-118">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="0246e-118">Example 1</span></span>

<span data-ttu-id="0246e-119">`ROUND (1200.767, 2)` ปัดเศษเป็นทศนิยมสองตำแหน่ง และส่งกลับ **1200.77**</span><span class="sxs-lookup"><span data-stu-id="0246e-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0246e-120">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="0246e-120">Example 2</span></span>

<span data-ttu-id="0246e-121">`ROUND (1200.767, -3)` ปัดเศษเป็นผลคูณที่ใกล้ที่สุดของ 1,000 และส่งกลับ **1000**</span><span class="sxs-lookup"><span data-stu-id="0246e-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="0246e-122">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="0246e-122">Example 3</span></span>

<span data-ttu-id="0246e-123">`ROUND (1200.5, 0)` ปัดเศษเป็นจำนวนเต็มคู่ที่ใกล้เคียงที่สุดและส่งคืน **1200** ขณะที่ `ROUND (1201.5, 0)` ทำเหมือนกันและส่งคืน **1202**</span><span class="sxs-lookup"><span data-stu-id="0246e-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0246e-124">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0246e-124">Additional resources</span></span>

[<span data-ttu-id="0246e-125">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="0246e-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]