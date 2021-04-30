---
title: ฟังก์ชั่น DATEFORMAT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATEFORMAT
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 1b3a0a2608328b233004034f7ab2ccfa833c17e3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890921"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="4fcdb-103">ฟังก์ชั่น DATEFORMAT ER</span><span class="sxs-lookup"><span data-stu-id="4fcdb-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fcdb-104">ฟังก์ชัน `DATEFORMAT` ส่งกลับค่า *สตริง* ที่แสดงค่าวันที่ที่ให้เป็นข้อความในรูปแบบที่ระบุและใน [Culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="4fcdb-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="4fcdb-105">สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](/dotnet/standard/base-types/standard-date-and-time-format-strings) และ [กำหนดเอง](/dotnet/standard/base-types/custom-date-and-time-format-strings)</span><span class="sxs-lookup"><span data-stu-id="4fcdb-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="4fcdb-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="4fcdb-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="4fcdb-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="4fcdb-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="4fcdb-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="4fcdb-108">Arguments</span></span>

<span data-ttu-id="4fcdb-109">`date`: *วันที่*</span><span class="sxs-lookup"><span data-stu-id="4fcdb-109">`date`: *Date*</span></span>

<span data-ttu-id="4fcdb-110">ค่าวันที่ที่แสดงวันที่ที่เป็นรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="4fcdb-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="4fcdb-111">`format`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="4fcdb-111">`format`: *String*</span></span>

<span data-ttu-id="4fcdb-112">รูปแบบของสตริงเอาต์พุต</span><span class="sxs-lookup"><span data-stu-id="4fcdb-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="4fcdb-113">สตริงรูปแบบจะคำนึงถึงตัวพิมพ์ เมื่อคุณใช้รูปแบบมาตรฐานหรือรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4fcdb-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="4fcdb-114">ตัวอย่างเช่น ตัวระบุรูปแบบ "d" [มาตรฐาน](/dotnet/standard/base-types/standard-date-and-time-format-strings) จะส่งคืนวันที่โดยใช้รูปแบบวันที่แบบย่อ ในขณะที่ตัวระบุรูปแบบ "D" มาตรฐาน จะส่งคืนวันที่โดยใช้รูปแบบวันที่ที่ยาว</span><span class="sxs-lookup"><span data-stu-id="4fcdb-114">For example, the [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="4fcdb-115">นอกจากนี้ ตัวระบุรูปแบบ "M" [แบบกำหนดเอง](/dotnet/standard/base-types/custom-date-and-time-format-strings) จะส่งคืนเดือน ตั้งแต่ 1 ถึง 12 ในขณะที่ตัวระบุรูปแบบ "m" แบบกำหนดเอง จะส่งคืนนาที ตั้งแต่ 0 ถึง 59</span><span class="sxs-lookup"><span data-stu-id="4fcdb-115">Additionally, the [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="4fcdb-116">`culture`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="4fcdb-116">`culture`: *String*</span></span>

<span data-ttu-id="4fcdb-117">วัฒนธรรมที่จะใช้สำหรับการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="4fcdb-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="4fcdb-118">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="4fcdb-118">Return values</span></span>

<span data-ttu-id="4fcdb-119">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="4fcdb-119">*String*</span></span>

<span data-ttu-id="4fcdb-120">ค่าสตริงที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="4fcdb-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4fcdb-121">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4fcdb-121">Usage notes</span></span>

<span data-ttu-id="4fcdb-122">หากวัฒนธรรมไม่ได้กำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก ค่าของ `culture` จะถูกกำหนดโดยบริบทการเรียก</span><span class="sxs-lookup"><span data-stu-id="4fcdb-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="4fcdb-123">ตัวอย่างเช่น ถ้าฟังก์ชัน `DATEFORMAT` ถูกเรียกโดยใช้ไวยากรณ์ 1 ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับส่วนประกอบ **FILE** ที่ถูกกำหนดค่าให้ใช้วัฒนธรรมเยอรมัน การแปลงจะทำโดยใช้วัฒนธรรมเยอรมัน</span><span class="sxs-lookup"><span data-stu-id="4fcdb-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="4fcdb-124">ค่า `culture` เริ่มต้นคือ **EN-US**</span><span class="sxs-lookup"><span data-stu-id="4fcdb-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="4fcdb-125">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="4fcdb-125">Example 1</span></span>

<span data-ttu-id="4fcdb-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` ส่งคืนค่าวันที่ซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="4fcdb-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="4fcdb-127">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="4fcdb-127">Example 2</span></span>

<span data-ttu-id="4fcdb-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` ส่งกลับวันที่เซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24-12-2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="4fcdb-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4fcdb-129">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4fcdb-129">Additional resources</span></span>

[<span data-ttu-id="4fcdb-130">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="4fcdb-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]