---
title: ฟังก์ชัน TRANSLATE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TRANSLATE (ER)
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 7e4d6417757e27190ab7cabf2bf01243bb87b55c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746084"
---
# <a name="translate-er-function"></a><span data-ttu-id="d120c-103">ฟังก์ชัน TRANSLATE ER</span><span class="sxs-lookup"><span data-stu-id="d120c-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d120c-104">ฟังก์ชัน `TRANSLATE` ส่งคืนค่า *สตริง* ที่มีผลลัพธ์ของการแทนที่อักขระของข้อความที่ระบุไว้ในอักขระของชุดที่กำหนดไว้อีกชุดหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d120c-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="d120c-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="d120c-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="d120c-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="d120c-106">Arguments</span></span>

<span data-ttu-id="d120c-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="d120c-107">`text`: *String*</span></span>

<span data-ttu-id="d120c-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="d120c-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="d120c-109">`pattern`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="d120c-109">`pattern`: *String*</span></span>

<span data-ttu-id="d120c-110">ข้อความที่จะต้องถูกแทนที่</span><span class="sxs-lookup"><span data-stu-id="d120c-110">The text that must be replaced.</span></span>

<span data-ttu-id="d120c-111">`replacement`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="d120c-111">`replacement`: *String*</span></span>

<span data-ttu-id="d120c-112">ข้อความที่จะใช้เป็นการแทนที่</span><span class="sxs-lookup"><span data-stu-id="d120c-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="d120c-113">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="d120c-113">Return values</span></span>

<span data-ttu-id="d120c-114">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="d120c-114">*String*</span></span>

<span data-ttu-id="d120c-115">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="d120c-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d120c-116">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d120c-116">Usage notes</span></span>

<span data-ttu-id="d120c-117">ฟังก์ชัน `TRANSLATE` จะแทนที่หนึ่งอักขระพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="d120c-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="d120c-118">ฟังก์ชันจะแทนที่อักขระตัวแรกของอาร์กิวเมนต์ `text` โดยใช้อักขระตัวแรกของอาร์กิวเมนต์ `pattern` และอักขระตัวที่สอง และปฏิบัติตามขั้นตอนเดียวกันจนกว่าจะเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="d120c-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="d120c-119">เมื่ออักขระจากอาร์กิวเมนต์ `text` และ `pattern` ตรงกัน จะถูกแทนที่ด้วยอักขระจากอาร์กิวเมนต์ `replacement` ที่อยู่ในตำแหน่งเดียวกันกับอักขระจากอาร์กิวเมนต์ `pattern`</span><span class="sxs-lookup"><span data-stu-id="d120c-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="d120c-120">ถ้าอักขระปรากฏหลายครั้งในอาร์กิวเมนต์ `pattern` การแม็ปอาร์กิวเมนต์ `replacement` ที่สอดคล้องกับการเกิดขึ้นครั้งแรกของอักขระนี้จะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="d120c-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="d120c-121">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="d120c-121">Example 1</span></span>

<span data-ttu-id="d120c-122">`TRANSLATE ("abcdef", "cd", "GH")` แทนที่อักขระ **"c"** ของข้อความ **"abcdef"** ที่ระบุที่มีอักขระ **"G"** ของข้อความ `replacement` อันเนื่องมาจากตัวอย่างต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d120c-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="d120c-123">อักขระ **"c"** จะแสดงอยู่ในข้อความ `pattern` ในตำแหน่งแรก</span><span class="sxs-lookup"><span data-stu-id="d120c-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="d120c-124">ตำแหน่งแรกของข้อความ `replacement` มีอักขระ **"G"**</span><span class="sxs-lookup"><span data-stu-id="d120c-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="d120c-125">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="d120c-125">Example 2</span></span>

<span data-ttu-id="d120c-126">`TRANSLATE ("abcdef", "ccd", "GH")` ส่งกลับค่า **"abGdef"**</span><span class="sxs-lookup"><span data-stu-id="d120c-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="d120c-127">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="d120c-127">Example 3</span></span>

<span data-ttu-id="d120c-128">`TRANSLATE ("abccba", "abc", "123")` ส่งคืน **"123321"**</span><span class="sxs-lookup"><span data-stu-id="d120c-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d120c-129">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d120c-129">Additional resources</span></span>

[<span data-ttu-id="d120c-130">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="d120c-130">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]