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
ms.openlocfilehash: 9e550b0c7634c7aac3f8c597a1c1eac3f8125e3b
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070724"
---
# <span data-ttu-id="61eac-103"><a name="DATETIMEFORMAT">ฟังก์ชั่น DATETIMEFORMAT ER</a></span><span class="sxs-lookup"><span data-stu-id="61eac-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61eac-104">ฟังก์ชัน `DATETIMEFORMAT` ส่งกลับค่า *สตริง* ที่แสดงค่าวันที่/เวลาที่ให้เป็นข้อความในรูปแบบที่ระบุและใน [Culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="61eac-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="61eac-105">สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) และ [กำหนดเอง](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)</span><span class="sxs-lookup"><span data-stu-id="61eac-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="61eac-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="61eac-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="61eac-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="61eac-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="61eac-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="61eac-108">Arguments</span></span>

<span data-ttu-id="61eac-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="61eac-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="61eac-110">ค่าวันที่/เวลาที่แสดงถึงวันที่และเวลาในการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="61eac-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="61eac-111">`format`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="61eac-111">`format`: *String*</span></span>

<span data-ttu-id="61eac-112">รูปแบบของสตริงเอาต์พุต</span><span class="sxs-lookup"><span data-stu-id="61eac-112">The format of the output string.</span></span>

<span data-ttu-id="61eac-113">`culture`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="61eac-113">`culture`: *String*</span></span>

<span data-ttu-id="61eac-114">วัฒนธรรมที่จะใช้สำหรับการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="61eac-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="61eac-115">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="61eac-115">Return values</span></span>

<span data-ttu-id="61eac-116">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="61eac-116">*String*</span></span>

<span data-ttu-id="61eac-117">ค่าสตริงที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="61eac-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="61eac-118">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="61eac-118">Usage notes</span></span>

<span data-ttu-id="61eac-119">เมื่อวัฒนธรรมไม่ได้กำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก ค่าของ `culture` จะถูกกำหนดโดยบริบทการเรียก</span><span class="sxs-lookup"><span data-stu-id="61eac-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="61eac-120">ตัวอย่างเช่น ถ้าฟังก์ชัน `DATETIMEFORMAT` ถูกเรียกโดยใช้ไวยากรณ์ 1 ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับส่วนประกอบ **FILE** ที่ถูกกำหนดค่าให้ใช้วัฒนธรรมเยอรมัน การแปลงจะทำโดยใช้วัฒนธรรมเยอรมัน</span><span class="sxs-lookup"><span data-stu-id="61eac-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="61eac-121">ค่า `culture` เริ่มต้นคือ **EN-US**</span><span class="sxs-lookup"><span data-stu-id="61eac-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="61eac-122">เมื่อฟังก์ชัน `DATETIMEFORMAT` แปลงค่าวันที่/เวลาที่กำหนด จะพิจารณาการตั้งค่าโซนเวลาของผู้ใช้แอพลิเคชันที่กำลังเรียกใช้รูปแบบ ER ที่ฟังก์ชันถูกเรียกในบริบท</span><span class="sxs-lookup"><span data-stu-id="61eac-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="61eac-123">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="61eac-123">Example 1</span></span>

<span data-ttu-id="61eac-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` ส่งคืนค่าวันที่/เวลาของเซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="61eac-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="61eac-125">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="61eac-125">Example 2</span></span>

<span data-ttu-id="61eac-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` ส่งกลับวันที่/เวลาเซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24.12.2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="61eac-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="61eac-127">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="61eac-127">Example 3</span></span>

<span data-ttu-id="61eac-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` ส่งกลับค่าสตริง **2019-11-12T08:00:00.0000000-08:00** เมื่อถูกเรียกในระหว่างกระบวนการที่เริ่มต้นโดยผู้ใช้แอปพลิเคชันที่มีเวลาค่โซนเวลา **(GMT-08:00) เวลาแปซิฟิก (สหรัฐอเมริกา & แคนาดา)** ในส่วน **การกำหนดลักษณะภาษาและประเทศ/ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="61eac-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61eac-129">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="61eac-129">Additional resources</span></span>

[<span data-ttu-id="61eac-130">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="61eac-130">Date and time functions</span></span>](er-functions-category-datetime.md)
