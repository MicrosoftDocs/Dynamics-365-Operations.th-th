---
title: ฟังก์ชั่น DATETIMEFORMAT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATETIMEFORMAT
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
ms.openlocfilehash: 90bd2900434b1be509f72ec82375e52ea32bc424
ms.sourcegitcommit: 7cfe8931dd454e811a691f5118a4ecae7ba4b478
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/04/2021
ms.locfileid: "4825384"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="0d319-103">ฟังก์ชั่น DATETIMEFORMAT ER</span><span class="sxs-lookup"><span data-stu-id="0d319-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d319-104">ฟังก์ชัน `DATETIMEFORMAT` ส่งกลับค่า *สตริง* ที่แสดงค่าวันที่/เวลาที่ให้เป็นข้อความในรูปแบบที่ระบุและใน [Culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="0d319-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="0d319-105">สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) และ [กำหนดเอง](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)</span><span class="sxs-lookup"><span data-stu-id="0d319-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="0d319-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="0d319-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="0d319-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="0d319-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="0d319-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="0d319-108">Arguments</span></span>

<span data-ttu-id="0d319-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="0d319-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="0d319-110">ค่าวันที่/เวลาที่แสดงถึงวันที่และเวลาในการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="0d319-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="0d319-111">`format`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="0d319-111">`format`: *String*</span></span>

<span data-ttu-id="0d319-112">รูปแบบของสตริงเอาต์พุต</span><span class="sxs-lookup"><span data-stu-id="0d319-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="0d319-113">สตริงรูปแบบจะคำนึงถึงตัวพิมพ์ เมื่อคุณใช้รูปแบบมาตรฐานหรือรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="0d319-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="0d319-114">ตัวอย่างเช่น ตัวระบุรูปแบบ "d" [มาตรฐาน](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) จะส่งคืนวันที่โดยใช้รูปแบบวันที่แบบย่อ ในขณะที่ตัวระบุรูปแบบ "D" มาตรฐาน จะส่งคืนวันที่โดยใช้รูปแบบวันที่ที่ยาว</span><span class="sxs-lookup"><span data-stu-id="0d319-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="0d319-115">นอกจากนี้ ตัวระบุรูปแบบ "M" [แบบกำหนดเอง](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) จะส่งคืนเดือน ตั้งแต่ 1 ถึง 12 ในขณะที่ตัวระบุรูปแบบ "m" แบบกำหนดเอง จะส่งคืนนาที ตั้งแต่ 0 ถึง 59</span><span class="sxs-lookup"><span data-stu-id="0d319-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="0d319-116">`culture`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="0d319-116">`culture`: *String*</span></span>

<span data-ttu-id="0d319-117">วัฒนธรรมที่จะใช้สำหรับการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="0d319-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="0d319-118">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="0d319-118">Return values</span></span>

<span data-ttu-id="0d319-119">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="0d319-119">*String*</span></span>

<span data-ttu-id="0d319-120">ค่าสตริงที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="0d319-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0d319-121">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0d319-121">Usage notes</span></span>

<span data-ttu-id="0d319-122">หากวัฒนธรรมไม่ได้กำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก ค่าของ `culture` จะถูกกำหนดโดยบริบทการเรียก</span><span class="sxs-lookup"><span data-stu-id="0d319-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="0d319-123">ตัวอย่างเช่น ถ้าฟังก์ชัน `DATETIMEFORMAT` ถูกเรียกโดยใช้ไวยากรณ์ 1 ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับส่วนประกอบ **FILE** ที่ถูกกำหนดค่าให้ใช้วัฒนธรรมเยอรมัน การแปลงจะทำโดยใช้วัฒนธรรมเยอรมัน</span><span class="sxs-lookup"><span data-stu-id="0d319-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="0d319-124">ค่า `culture` เริ่มต้นคือ **EN-US**</span><span class="sxs-lookup"><span data-stu-id="0d319-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="0d319-125">เมื่อฟังก์ชัน `DATETIMEFORMAT` แปลงค่าวันที่/เวลาที่กำหนด จะพิจารณาการตั้งค่าโซนเวลาของผู้ใช้แอพลิเคชันที่กำลังเรียกใช้รูปแบบ ER ที่ฟังก์ชันถูกเรียกในบริบท</span><span class="sxs-lookup"><span data-stu-id="0d319-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="0d319-126">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="0d319-126">Example 1</span></span>

<span data-ttu-id="0d319-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` ส่งคืนค่าวันที่/เวลาของเซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="0d319-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="0d319-128">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="0d319-128">Example 2</span></span>

<span data-ttu-id="0d319-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` ส่งกลับวันที่/เวลาเซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24.12.2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="0d319-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="0d319-130">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="0d319-130">Example 3</span></span>

<span data-ttu-id="0d319-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` ส่งกลับค่าสตริง **2019-11-12T08:00:00.0000000-08:00** เมื่อฟังก์ชันถูกเรียกในระหว่างกระบวนการที่เริ่มต้นโดยผู้ใช้แอปพลิเคชันที่มีเวลาค่โซนเวลา **(GMT-08:00) เวลาแปซิฟิก (สหรัฐอเมริกา & แคนาดา)** ในส่วน **การกำหนดลักษณะภาษาและประเทศ/ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="0d319-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d319-132">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0d319-132">Additional resources</span></span>

[<span data-ttu-id="0d319-133">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="0d319-133">Date and time functions</span></span>](er-functions-category-datetime.md)
