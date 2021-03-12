---
title: ฟังก์ชั่น DATEFORMAT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATEFORMAT
author: NickSelin
manager: kfend
ms.date: 01/04/2021
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
ms.openlocfilehash: cdc1671f818bc2c4d8a78d0a35337298e83c5060
ms.sourcegitcommit: 7cfe8931dd454e811a691f5118a4ecae7ba4b478
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/04/2021
ms.locfileid: "4826022"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="0c84e-103">ฟังก์ชั่น DATEFORMAT ER</span><span class="sxs-lookup"><span data-stu-id="0c84e-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c84e-104">ฟังก์ชัน `DATEFORMAT` ส่งกลับค่า *สตริง* ที่แสดงค่าวันที่ที่ให้เป็นข้อความในรูปแบบที่ระบุและใน [Culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="0c84e-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="0c84e-105">สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) และ [กำหนดเอง](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)</span><span class="sxs-lookup"><span data-stu-id="0c84e-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="0c84e-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="0c84e-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="0c84e-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="0c84e-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="0c84e-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="0c84e-108">Arguments</span></span>

<span data-ttu-id="0c84e-109">`date`: *วันที่*</span><span class="sxs-lookup"><span data-stu-id="0c84e-109">`date`: *Date*</span></span>

<span data-ttu-id="0c84e-110">ค่าวันที่ที่แสดงวันที่ที่เป็นรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="0c84e-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="0c84e-111">`format`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="0c84e-111">`format`: *String*</span></span>

<span data-ttu-id="0c84e-112">รูปแบบของสตริงเอาต์พุต</span><span class="sxs-lookup"><span data-stu-id="0c84e-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="0c84e-113">สตริงรูปแบบจะคำนึงถึงตัวพิมพ์ เมื่อคุณใช้รูปแบบมาตรฐานหรือรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="0c84e-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="0c84e-114">ตัวอย่างเช่น ตัวระบุรูปแบบ "d" [มาตรฐาน](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) จะส่งคืนวันที่โดยใช้รูปแบบวันที่แบบย่อ ในขณะที่ตัวระบุรูปแบบ "D" มาตรฐาน จะส่งคืนวันที่โดยใช้รูปแบบวันที่ที่ยาว</span><span class="sxs-lookup"><span data-stu-id="0c84e-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="0c84e-115">นอกจากนี้ ตัวระบุรูปแบบ "M" [แบบกำหนดเอง](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) จะส่งคืนเดือน ตั้งแต่ 1 ถึง 12 ในขณะที่ตัวระบุรูปแบบ "m" แบบกำหนดเอง จะส่งคืนนาที ตั้งแต่ 0 ถึง 59</span><span class="sxs-lookup"><span data-stu-id="0c84e-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="0c84e-116">`culture`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="0c84e-116">`culture`: *String*</span></span>

<span data-ttu-id="0c84e-117">วัฒนธรรมที่จะใช้สำหรับการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="0c84e-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="0c84e-118">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="0c84e-118">Return values</span></span>

<span data-ttu-id="0c84e-119">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="0c84e-119">*String*</span></span>

<span data-ttu-id="0c84e-120">ค่าสตริงที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="0c84e-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0c84e-121">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0c84e-121">Usage notes</span></span>

<span data-ttu-id="0c84e-122">หากวัฒนธรรมไม่ได้กำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก ค่าของ `culture` จะถูกกำหนดโดยบริบทการเรียก</span><span class="sxs-lookup"><span data-stu-id="0c84e-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="0c84e-123">ตัวอย่างเช่น ถ้าฟังก์ชัน `DATEFORMAT` ถูกเรียกโดยใช้ไวยากรณ์ 1 ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับส่วนประกอบ **FILE** ที่ถูกกำหนดค่าให้ใช้วัฒนธรรมเยอรมัน การแปลงจะทำโดยใช้วัฒนธรรมเยอรมัน</span><span class="sxs-lookup"><span data-stu-id="0c84e-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="0c84e-124">ค่า `culture` เริ่มต้นคือ **EN-US**</span><span class="sxs-lookup"><span data-stu-id="0c84e-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="0c84e-125">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="0c84e-125">Example 1</span></span>

<span data-ttu-id="0c84e-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` ส่งคืนค่าวันที่ซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="0c84e-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="0c84e-127">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="0c84e-127">Example 2</span></span>

<span data-ttu-id="0c84e-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` ส่งกลับวันที่เซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24-12-2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="0c84e-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c84e-129">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0c84e-129">Additional resources</span></span>

[<span data-ttu-id="0c84e-130">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="0c84e-130">Date and time functions</span></span>](er-functions-category-datetime.md)
