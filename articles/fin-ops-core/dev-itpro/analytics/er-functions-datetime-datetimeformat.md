---
title: ฟังก์ชั่น DATETIMEFORMAT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATETIMEFORMAT
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
ms.openlocfilehash: 8044f81ee59af4a11bfab38525afdac5a46acd2c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891268"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="fa4a8-103">ฟังก์ชั่น DATETIMEFORMAT ER</span><span class="sxs-lookup"><span data-stu-id="fa4a8-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa4a8-104">ฟังก์ชัน `DATETIMEFORMAT` ส่งกลับค่า *สตริง* ที่แสดงค่าวันที่/เวลาที่ให้เป็นข้อความในรูปแบบที่ระบุและใน [Culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="fa4a8-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="fa4a8-105">สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](/dotnet/standard/base-types/standard-date-and-time-format-strings) และ [กำหนดเอง](/dotnet/standard/base-types/custom-date-and-time-format-strings)</span><span class="sxs-lookup"><span data-stu-id="fa4a8-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="fa4a8-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="fa4a8-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="fa4a8-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="fa4a8-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="fa4a8-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="fa4a8-108">Arguments</span></span>

<span data-ttu-id="fa4a8-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="fa4a8-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="fa4a8-110">ค่าวันที่/เวลาที่แสดงถึงวันที่และเวลาในการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="fa4a8-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="fa4a8-111">`format`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="fa4a8-111">`format`: *String*</span></span>

<span data-ttu-id="fa4a8-112">รูปแบบของสตริงเอาต์พุต</span><span class="sxs-lookup"><span data-stu-id="fa4a8-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="fa4a8-113">สตริงรูปแบบจะคำนึงถึงตัวพิมพ์ เมื่อคุณใช้รูปแบบมาตรฐานหรือรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="fa4a8-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="fa4a8-114">ตัวอย่างเช่น ตัวระบุรูปแบบ "d" [มาตรฐาน](/dotnet/standard/base-types/standard-date-and-time-format-strings) จะส่งคืนวันที่โดยใช้รูปแบบวันที่แบบย่อ ในขณะที่ตัวระบุรูปแบบ "D" มาตรฐาน จะส่งคืนวันที่โดยใช้รูปแบบวันที่ที่ยาว</span><span class="sxs-lookup"><span data-stu-id="fa4a8-114">For example, the [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="fa4a8-115">นอกจากนี้ ตัวระบุรูปแบบ "M" [แบบกำหนดเอง](/dotnet/standard/base-types/custom-date-and-time-format-strings) จะส่งคืนเดือน ตั้งแต่ 1 ถึง 12 ในขณะที่ตัวระบุรูปแบบ "m" แบบกำหนดเอง จะส่งคืนนาที ตั้งแต่ 0 ถึง 59</span><span class="sxs-lookup"><span data-stu-id="fa4a8-115">Additionally, the [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="fa4a8-116">`culture`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="fa4a8-116">`culture`: *String*</span></span>

<span data-ttu-id="fa4a8-117">วัฒนธรรมที่จะใช้สำหรับการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="fa4a8-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="fa4a8-118">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="fa4a8-118">Return values</span></span>

<span data-ttu-id="fa4a8-119">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="fa4a8-119">*String*</span></span>

<span data-ttu-id="fa4a8-120">ค่าสตริงที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="fa4a8-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fa4a8-121">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fa4a8-121">Usage notes</span></span>

<span data-ttu-id="fa4a8-122">หากวัฒนธรรมไม่ได้กำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก ค่าของ `culture` จะถูกกำหนดโดยบริบทการเรียก</span><span class="sxs-lookup"><span data-stu-id="fa4a8-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="fa4a8-123">ตัวอย่างเช่น ถ้าฟังก์ชัน `DATETIMEFORMAT` ถูกเรียกโดยใช้ไวยากรณ์ 1 ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับส่วนประกอบ **FILE** ที่ถูกกำหนดค่าให้ใช้วัฒนธรรมเยอรมัน การแปลงจะทำโดยใช้วัฒนธรรมเยอรมัน</span><span class="sxs-lookup"><span data-stu-id="fa4a8-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="fa4a8-124">ค่า `culture` เริ่มต้นคือ **EN-US**</span><span class="sxs-lookup"><span data-stu-id="fa4a8-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="fa4a8-125">เมื่อฟังก์ชัน `DATETIMEFORMAT` แปลงค่าวันที่/เวลาที่กำหนด จะพิจารณาการตั้งค่าโซนเวลาของผู้ใช้แอพลิเคชันที่กำลังเรียกใช้รูปแบบ ER ที่ฟังก์ชันถูกเรียกในบริบท</span><span class="sxs-lookup"><span data-stu-id="fa4a8-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="fa4a8-126">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="fa4a8-126">Example 1</span></span>

<span data-ttu-id="fa4a8-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` ส่งคืนค่าวันที่/เวลาของเซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="fa4a8-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="fa4a8-128">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="fa4a8-128">Example 2</span></span>

<span data-ttu-id="fa4a8-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` ส่งกลับวันที่/เวลาเซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24.12.2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="fa4a8-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="fa4a8-130">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="fa4a8-130">Example 3</span></span>

<span data-ttu-id="fa4a8-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` ส่งกลับค่าสตริง **2019-11-12T08:00:00.0000000-08:00** เมื่อฟังก์ชันถูกเรียกในระหว่างกระบวนการที่เริ่มต้นโดยผู้ใช้แอปพลิเคชันที่มีเวลาค่โซนเวลา **(GMT-08:00) เวลาแปซิฟิก (สหรัฐอเมริกา & แคนาดา)** ในส่วน **การกำหนดลักษณะภาษาและประเทศ/ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="fa4a8-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa4a8-132">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fa4a8-132">Additional resources</span></span>

[<span data-ttu-id="fa4a8-133">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="fa4a8-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]