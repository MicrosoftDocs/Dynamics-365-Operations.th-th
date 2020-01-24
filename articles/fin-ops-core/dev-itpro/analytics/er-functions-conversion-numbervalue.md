---
title: ฟังก์ชัน NUMBERVALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NUMBERVALUE
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 80f0606dc3842cdfa56d41e2815eccd7518218b8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916533"
---
# <span data-ttu-id="92fd3-103"><a name="NUMBERVALUE">ฟังก์ชัน NUMBERVALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="92fd3-103"><a name="NUMBERVALUE">NUMBERVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92fd3-104">ฟังก์ชัน `NUMBERVALUE` ส่งกลับค่า *จำนวนจริง* ที่ถูกแปลงจากค่า *สตริง* ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="92fd3-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="92fd3-105">ในระหว่างการแปลงจะมีการพิจารณาตัวแบ่งการจัดกลุ่มทศนิยมและเลขฐานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="92fd3-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="92fd3-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="92fd3-106">Syntax</span></span>

```
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="92fd3-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="92fd3-107">Arguments</span></span>

<span data-ttu-id="92fd3-108">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="92fd3-108">`text`: *String*</span></span>

<span data-ttu-id="92fd3-109">ค่าข้อความต้องถูกแปลงเป็นหมายเลย *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="92fd3-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="92fd3-110">`decimal separator`: สตริง</span><span class="sxs-lookup"><span data-stu-id="92fd3-110">`decimal separator`: String</span></span>

<span data-ttu-id="92fd3-111">ตัวแบ่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="92fd3-111">A decimal separator.</span></span> <span data-ttu-id="92fd3-112">ใช้ในการแยกจำนวนเต็มและเศษส่วนของตัวเลขทศนิยม</span><span class="sxs-lookup"><span data-stu-id="92fd3-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="92fd3-113">`digit grouping separator`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="92fd3-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="92fd3-114">ตัวแบ่งการจัดกลุ่มตัวเลข</span><span class="sxs-lookup"><span data-stu-id="92fd3-114">A digit grouping separator.</span></span> <span data-ttu-id="92fd3-115">ใช้เป็นตัวแบ่งหลักพัน</span><span class="sxs-lookup"><span data-stu-id="92fd3-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="92fd3-116">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="92fd3-116">Return values</span></span>

<span data-ttu-id="92fd3-117">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="92fd3-117">*Real*</span></span>

<span data-ttu-id="92fd3-118">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="92fd3-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="92fd3-119">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="92fd3-119">Example</span></span>

<span data-ttu-id="92fd3-120">`NUMBERVALUE( "1 234,56", ",", " ")` ส่งกลับค่า **1234.56**</span><span class="sxs-lookup"><span data-stu-id="92fd3-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92fd3-121">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="92fd3-121">Additional resources</span></span>

[<span data-ttu-id="92fd3-122">ฟังก์ชันการแปลงของชนิด</span><span class="sxs-lookup"><span data-stu-id="92fd3-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
