---
title: ฟังก์ชัน REPLACE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ REPLACE (ER)
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
ms.openlocfilehash: 21cdd8532730925b7d5c6f5b3bb565dcd365dd6d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746219"
---
# <a name="replace-er-function"></a><span data-ttu-id="c6740-103">ฟังก์ชัน REPLACE ER</span><span class="sxs-lookup"><span data-stu-id="c6740-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6740-104">ฟังก์ชัน `REPLACE` ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากทั้งหมดหรือบางส่วนถูกแทนที่ด้วยสตริงอื่น</span><span class="sxs-lookup"><span data-stu-id="c6740-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6740-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="c6740-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="c6740-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="c6740-106">Arguments</span></span>

<span data-ttu-id="c6740-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="c6740-107">`text`: *String*</span></span>

<span data-ttu-id="c6740-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="c6740-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="c6740-109">`pattern`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="c6740-109">`pattern`: *String*</span></span>

<span data-ttu-id="c6740-110">ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **เท็จ** อาร์กิวเมนต์นี้ประกอบด้วยข้อความที่ต้องถูกแทนที่</span><span class="sxs-lookup"><span data-stu-id="c6740-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="c6740-111">ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **จริง** อาร์กิวเมนต์นี้ประกอบด้วยนิพจน์ทั่วไปที่กำหนดทั้งรูปแบบการค้นหาและข้อความการแทนที่</span><span class="sxs-lookup"><span data-stu-id="c6740-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="c6740-112">`replacement`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="c6740-112">`replacement`: *String*</span></span>

<span data-ttu-id="c6740-113">ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **เท็จ** อาร์กิวเมนต์นี้ประกอบด้วยข้อความเพื่อใช้เป็นการแทนที่</span><span class="sxs-lookup"><span data-stu-id="c6740-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="c6740-114">ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **จริง** อาร์กิวเมนต์นี้จะไม่ถูกใช้</span><span class="sxs-lookup"><span data-stu-id="c6740-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="c6740-115">`regular expression flag`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="c6740-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="c6740-116">ค่า *บูลีน* ที่บ่งชี้ว่ามีการใช้นิพจน์ทั่วไปเพื่อทำการแทนที่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c6740-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="c6740-117">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="c6740-117">Return values</span></span>

<span data-ttu-id="c6740-118">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="c6740-118">*String*</span></span>

<span data-ttu-id="c6740-119">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="c6740-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c6740-120">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c6740-120">Usage notes</span></span>

<span data-ttu-id="c6740-121">ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **จริง** ฟังก์ชันนี้จะส่งกลับสตริงที่ระบุ หลังจากที่มีการเปลี่ยนแปลงโดยใช้นิพจน์ทั่วไปที่ระบุโดยอาร์กิวเมนต์ `pattern`</span><span class="sxs-lookup"><span data-stu-id="c6740-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="c6740-122">นิพจน์ทั่วไปจะถูกใช้ในการค้นหาอักขระซึ่งต้องถูกแทนที่</span><span class="sxs-lookup"><span data-stu-id="c6740-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="c6740-123">ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **เท็จ** ฟังก์ชันนี้ส่งคืนสตริงที่ระบุหลังจากชุดของอักขระที่กำหนดไว้ในอาร์กิวเมนต์ `pattern` ถูกแทนที่โดยอักขระของอาร์กิวเมนต์ `replacement`</span><span class="sxs-lookup"><span data-stu-id="c6740-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="c6740-124">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="c6740-124">Example 1</span></span>

<span data-ttu-id="c6740-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` ใช้นิพจน์ทั่วไปที่ลบสัญลักษณ์ที่ไม่ใช่ตัวเลขทั้งหมด และส่งกลับ **"19234564971"**</span><span class="sxs-lookup"><span data-stu-id="c6740-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="c6740-126">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="c6740-126">Example 2</span></span>

<span data-ttu-id="c6740-127">`REPLACE ("abcdef", "cd", "GH", false)` แทนที่รูปแบบ **"cd"** ด้วยสตริง **"GH"** และส่งกลับค่า **"abGHef"**</span><span class="sxs-lookup"><span data-stu-id="c6740-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6740-128">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c6740-128">Additional resources</span></span>

[<span data-ttu-id="c6740-129">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="c6740-129">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]