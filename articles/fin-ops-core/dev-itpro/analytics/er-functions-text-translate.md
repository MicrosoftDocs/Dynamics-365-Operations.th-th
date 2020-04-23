---
title: ฟังก์ชัน TRANSLATE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TRANSLATE (ER)
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 415444bda097c00522155d1b37988a79da836902
ms.sourcegitcommit: fb8ad8e2b142441a6530b364f3258bbcc0c724d2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201123"
---
# <a name=""></a><span data-ttu-id="51a36-103"><a name="TRANSLATE">ฟังก์ชัน TRANSLATE ER</a></span><span class="sxs-lookup"><span data-stu-id="51a36-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51a36-104">ฟังก์ชัน `TRANSLATE` ส่งคืนค่า *สตริง* ที่มีผลลัพธ์ของการแทนที่อักขระของข้อความที่ระบุไว้ในอักขระของชุดที่กำหนดไว้อีกชุดหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="51a36-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="51a36-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="51a36-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="51a36-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="51a36-106">Arguments</span></span>

<span data-ttu-id="51a36-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="51a36-107">`text`: *String*</span></span>

<span data-ttu-id="51a36-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="51a36-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="51a36-109">`pattern`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="51a36-109">`pattern`: *String*</span></span>

<span data-ttu-id="51a36-110">ข้อความที่จะต้องถูกแทนที่</span><span class="sxs-lookup"><span data-stu-id="51a36-110">The text that must be replaced.</span></span>

<span data-ttu-id="51a36-111">`replacement`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="51a36-111">`replacement`: *String*</span></span>

<span data-ttu-id="51a36-112">ข้อความที่จะใช้เป็นการแทนที่</span><span class="sxs-lookup"><span data-stu-id="51a36-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="51a36-113">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="51a36-113">Return values</span></span>

<span data-ttu-id="51a36-114">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="51a36-114">*String*</span></span>

<span data-ttu-id="51a36-115">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="51a36-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="51a36-116">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="51a36-116">Usage notes</span></span>

<span data-ttu-id="51a36-117">ฟังก์ชัน `TRANSLATE` จะแทนที่หนึ่งอักขระพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="51a36-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="51a36-118">ฟังก์ชันจะแทนที่อักขระตัวแรกของอาร์กิวเมนต์ `text` โดยใช้อักขระตัวแรกของอาร์กิวเมนต์ `pattern` และอักขระตัวที่สอง และปฏิบัติตามขั้นตอนเดียวกันจนกว่าจะเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="51a36-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="51a36-119">เมื่ออักขระจากอาร์กิวเมนต์ `text` และ `pattern` ตรงกัน จะถูกแทนที่ด้วยอักขระจากอาร์กิวเมนต์ `replacement` ที่อยู่ในตำแหน่งเดียวกันกับอักขระจากอาร์กิวเมนต์ `pattern`</span><span class="sxs-lookup"><span data-stu-id="51a36-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="51a36-120">ถ้าอักขระปรากฏหลายครั้งในอาร์กิวเมนต์ `pattern` การแม็ปอาร์กิวเมนต์ `replacement` ที่สอดคล้องกับการเกิดขึ้นครั้งแรกของอักขระนี้จะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="51a36-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="51a36-121">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="51a36-121">Example 1</span></span>

<span data-ttu-id="51a36-122">`TRANSLATE ("abcdef", "cd", "GH")` แทนที่อักขระ **"c"** ของข้อความ **"abcdef"** ที่ระบุที่มีอักขระ **"G"** ของข้อความ `replacement` อันเนื่องมาจากตัวอย่างต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="51a36-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="51a36-123">อักขระ **"c"** จะแสดงอยู่ในข้อความ `pattern` ในตำแหน่งแรก</span><span class="sxs-lookup"><span data-stu-id="51a36-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="51a36-124">ตำแหน่งแรกของข้อความ `replacement` มีอักขระ **"G"**</span><span class="sxs-lookup"><span data-stu-id="51a36-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="51a36-125">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="51a36-125">Example 2</span></span>

<span data-ttu-id="51a36-126">`TRANSLATE ("abcdef", "ccd", "GH")` ส่งกลับค่า **"abGdef"**</span><span class="sxs-lookup"><span data-stu-id="51a36-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="51a36-127">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="51a36-127">Example 3</span></span>

<span data-ttu-id="51a36-128">`TRANSLATE ("abccba", "abc", "123")` ส่งคืน **"123321"**</span><span class="sxs-lookup"><span data-stu-id="51a36-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51a36-129">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="51a36-129">Additional resources</span></span>

[<span data-ttu-id="51a36-130">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="51a36-130">Text functions</span></span>](er-functions-category-text.md)
