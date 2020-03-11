---
title: ฟังก์ชัน REPLACE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ REPLACE (ER)
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: ba2590635ba465dae9ea50d3e4da989365548f3b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040997"
---
# <span data-ttu-id="3c089-103"><a name="REPLACE">ฟังก์ชัน REPLACE ER</a></span><span class="sxs-lookup"><span data-stu-id="3c089-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c089-104">ฟังก์ชัน `REPLACE` ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากทั้งหมดหรือบางส่วนถูกแทนที่ด้วยสตริงอื่น</span><span class="sxs-lookup"><span data-stu-id="3c089-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c089-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="3c089-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="3c089-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="3c089-106">Arguments</span></span>

<span data-ttu-id="3c089-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="3c089-107">`text`: *String*</span></span>

<span data-ttu-id="3c089-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="3c089-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="3c089-109">`pattern`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="3c089-109">`pattern`: *String*</span></span>

<span data-ttu-id="3c089-110">ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **เท็จ** อาร์กิวเมนต์นี้ประกอบด้วยข้อความที่ต้องถูกแทนที่</span><span class="sxs-lookup"><span data-stu-id="3c089-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="3c089-111">ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **จริง** อาร์กิวเมนต์นี้ประกอบด้วยนิพจน์ทั่วไปที่กำหนดทั้งรูปแบบการค้นหาและข้อความการแทนที่</span><span class="sxs-lookup"><span data-stu-id="3c089-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="3c089-112">`replacement`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="3c089-112">`replacement`: *String*</span></span>

<span data-ttu-id="3c089-113">ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **เท็จ** อาร์กิวเมนต์นี้ประกอบด้วยข้อความเพื่อใช้เป็นการแทนที่</span><span class="sxs-lookup"><span data-stu-id="3c089-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="3c089-114">ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **จริง** อาร์กิวเมนต์นี้จะไม่ถูกใช้</span><span class="sxs-lookup"><span data-stu-id="3c089-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="3c089-115">`regular expression flag`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="3c089-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="3c089-116">ค่า *บูลีน* ที่บ่งชี้ว่ามีการใช้นิพจน์ทั่วไปเพื่อทำการแทนที่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3c089-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="3c089-117">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="3c089-117">Return values</span></span>

<span data-ttu-id="3c089-118">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="3c089-118">*String*</span></span>

<span data-ttu-id="3c089-119">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="3c089-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3c089-120">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3c089-120">Usage notes</span></span>

<span data-ttu-id="3c089-121">ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **จริง** ฟังก์ชันนี้จะส่งกลับสตริงที่ระบุ หลังจากที่มีการเปลี่ยนแปลงโดยใช้นิพจน์ทั่วไปที่ระบุโดยอาร์กิวเมนต์ `pattern`</span><span class="sxs-lookup"><span data-stu-id="3c089-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="3c089-122">นิพจน์ทั่วไปจะถูกใช้ในการค้นหาอักขระซึ่งต้องถูกแทนที่</span><span class="sxs-lookup"><span data-stu-id="3c089-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="3c089-123">หากอาร์กิวเมนต์ `regular expression flag` เป็น **เท็จ** ฟังก์ชันนี้จะทำงานเช่นเดียวกับ [TRANSLATE](er-functions-text-translate.md)</span><span class="sxs-lookup"><span data-stu-id="3c089-123">If the `regular expression flag` argument is **FALSE**, this function behaves like [TRANSLATE](er-functions-text-translate.md).</span></span> <span data-ttu-id="3c089-124">อักขระที่ถูกที่ระบุโดยอาร์กิวเมนต์ `replacement` ถูกใช้ในการแทนที่อักขระที่พบ</span><span class="sxs-lookup"><span data-stu-id="3c089-124">The characters that are specified by the `replacement` argument are used to replace the characters that are found.</span></span> 

## <a name="example-1"></a><span data-ttu-id="3c089-125">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="3c089-125">Example 1</span></span>

<span data-ttu-id="3c089-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` ใช้นิพจน์ทั่วไปที่ลบสัญลักษณ์ที่ไม่ใช่ตัวเลขทั้งหมด และส่งกลับ **"19234564971"**</span><span class="sxs-lookup"><span data-stu-id="3c089-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="3c089-127">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="3c089-127">Example 2</span></span>

<span data-ttu-id="3c089-128">`REPLACE ("abcdef", "cd", "GH", false)` แทนที่รูปแบบ **"cd"** ด้วยสตริง **"GH"** และส่งกลับค่า **"abGHef"**</span><span class="sxs-lookup"><span data-stu-id="3c089-128">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c089-129">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3c089-129">Additional resources</span></span>

[<span data-ttu-id="3c089-130">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="3c089-130">Text functions</span></span>](er-functions-category-text.md)
