---
title: ฟังก์ชั่น DATETIMEFORMAT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATETIMEFORMAT
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 65b988e6c58aed35577288e01157b8c1f76e6efd
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744874"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="d6d3e-103">ฟังก์ชั่น DATETIMEFORMAT ER</span><span class="sxs-lookup"><span data-stu-id="d6d3e-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6d3e-104">ฟังก์ชัน `DATETIMEFORMAT` ส่งกลับค่า *สตริง* ที่แสดงค่าวันที่/เวลาที่ให้เป็นข้อความในรูปแบบที่ระบุและใน [Culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="d6d3e-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="d6d3e-105">สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) และ [กำหนดเอง](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)</span><span class="sxs-lookup"><span data-stu-id="d6d3e-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d6d3e-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="d6d3e-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="d6d3e-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="d6d3e-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="d6d3e-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="d6d3e-108">Arguments</span></span>

<span data-ttu-id="d6d3e-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="d6d3e-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="d6d3e-110">ค่าวันที่/เวลาที่แสดงถึงวันที่และเวลาในการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="d6d3e-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="d6d3e-111">`format`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="d6d3e-111">`format`: *String*</span></span>

<span data-ttu-id="d6d3e-112">รูปแบบของสตริงเอาต์พุต</span><span class="sxs-lookup"><span data-stu-id="d6d3e-112">The format of the output string.</span></span>

<span data-ttu-id="d6d3e-113">`culture`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="d6d3e-113">`culture`: *String*</span></span>

<span data-ttu-id="d6d3e-114">วัฒนธรรมที่จะใช้สำหรับการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="d6d3e-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="d6d3e-115">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="d6d3e-115">Return values</span></span>

<span data-ttu-id="d6d3e-116">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="d6d3e-116">*String*</span></span>

<span data-ttu-id="d6d3e-117">ค่าสตริงที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="d6d3e-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d6d3e-118">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d6d3e-118">Usage notes</span></span>

<span data-ttu-id="d6d3e-119">เมื่อวัฒนธรรมไม่ได้กำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก ค่าของ `culture` จะถูกกำหนดโดยบริบทการเรียก</span><span class="sxs-lookup"><span data-stu-id="d6d3e-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="d6d3e-120">ตัวอย่างเช่น ถ้าฟังก์ชัน `DATETIMEFORMAT` ถูกเรียกโดยใช้ไวยากรณ์ 1 ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับส่วนประกอบ **FILE** ที่ถูกกำหนดค่าให้ใช้วัฒนธรรมเยอรมัน การแปลงจะทำโดยใช้วัฒนธรรมเยอรมัน</span><span class="sxs-lookup"><span data-stu-id="d6d3e-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="d6d3e-121">ค่า `culture` เริ่มต้นคือ **EN-US**</span><span class="sxs-lookup"><span data-stu-id="d6d3e-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="d6d3e-122">เมื่อฟังก์ชัน `DATETIMEFORMAT` แปลงค่าวันที่/เวลาที่กำหนด จะพิจารณาการตั้งค่าโซนเวลาของผู้ใช้แอพลิเคชันที่กำลังเรียกใช้รูปแบบ ER ที่ฟังก์ชันถูกเรียกในบริบท</span><span class="sxs-lookup"><span data-stu-id="d6d3e-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="d6d3e-123">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="d6d3e-123">Example 1</span></span>

<span data-ttu-id="d6d3e-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` ส่งคืนค่าวันที่/เวลาของเซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="d6d3e-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="d6d3e-125">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="d6d3e-125">Example 2</span></span>

<span data-ttu-id="d6d3e-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` ส่งกลับวันที่/เวลาเซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24.12.2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="d6d3e-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="d6d3e-127">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="d6d3e-127">Example 3</span></span>

<span data-ttu-id="d6d3e-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` ส่งกลับค่าสตริง **2019-11-12T08:00:00.0000000-08:00** เมื่อถูกเรียกในระหว่างกระบวนการที่เริ่มต้นโดยผู้ใช้แอปพลิเคชันที่มีเวลาค่โซนเวลา **(GMT-08:00) เวลาแปซิฟิก (สหรัฐอเมริกา & แคนาดา)** ในส่วน **การกำหนดลักษณะภาษาและประเทศ/ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="d6d3e-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d6d3e-129">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d6d3e-129">Additional resources</span></span>

[<span data-ttu-id="d6d3e-130">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d6d3e-130">Date and time functions</span></span>](er-functions-category-datetime.md)
