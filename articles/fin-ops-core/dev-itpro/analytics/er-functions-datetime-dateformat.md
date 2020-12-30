---
title: ฟังก์ชั่น DATEFORMAT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATEFORMAT
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fa6bdef2168112aeb17e0edb9f9a6d1b3bd45c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684948"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="9d4f0-103">ฟังก์ชั่น DATEFORMAT ER</span><span class="sxs-lookup"><span data-stu-id="9d4f0-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d4f0-104">ฟังก์ชัน `DATEFORMAT` ส่งกลับค่า *สตริง* ที่แสดงค่าวันที่ที่ให้เป็นข้อความในรูปแบบที่ระบุและใน [Culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="9d4f0-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="9d4f0-105">สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) และ [กำหนดเอง](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)</span><span class="sxs-lookup"><span data-stu-id="9d4f0-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="9d4f0-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="9d4f0-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="9d4f0-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="9d4f0-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="9d4f0-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="9d4f0-108">Arguments</span></span>

<span data-ttu-id="9d4f0-109">`date`: *วันที่*</span><span class="sxs-lookup"><span data-stu-id="9d4f0-109">`date`: *Date*</span></span>

<span data-ttu-id="9d4f0-110">ค่าวันที่ที่แสดงวันที่ที่เป็นรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="9d4f0-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="9d4f0-111">`format`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="9d4f0-111">`format`: *String*</span></span>

<span data-ttu-id="9d4f0-112">รูปแบบของสตริงเอาต์พุต</span><span class="sxs-lookup"><span data-stu-id="9d4f0-112">The format of the output string.</span></span>

<span data-ttu-id="9d4f0-113">`culture`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="9d4f0-113">`culture`: *String*</span></span>

<span data-ttu-id="9d4f0-114">วัฒนธรรมที่จะใช้สำหรับการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="9d4f0-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="9d4f0-115">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="9d4f0-115">Return values</span></span>

<span data-ttu-id="9d4f0-116">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="9d4f0-116">*String*</span></span>

<span data-ttu-id="9d4f0-117">ค่าสตริงที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="9d4f0-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9d4f0-118">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9d4f0-118">Usage notes</span></span>

<span data-ttu-id="9d4f0-119">เมื่อวัฒนธรรมไม่ได้กำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก ค่าของ `culture` จะถูกกำหนดโดยบริบทการเรียก</span><span class="sxs-lookup"><span data-stu-id="9d4f0-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="9d4f0-120">ตัวอย่างเช่น ถ้าฟังก์ชัน `DATEFORMAT` ถูกเรียกโดยใช้ไวยากรณ์ 1 ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับส่วนประกอบ **FILE** ที่ถูกกำหนดค่าให้ใช้วัฒนธรรมเยอรมัน การแปลงจะทำโดยใช้วัฒนธรรมเยอรมัน</span><span class="sxs-lookup"><span data-stu-id="9d4f0-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="9d4f0-121">ค่า `culture` เริ่มต้นคือ **EN-US**</span><span class="sxs-lookup"><span data-stu-id="9d4f0-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="9d4f0-122">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="9d4f0-122">Example 1</span></span>

<span data-ttu-id="9d4f0-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` ส่งคืนค่าวันที่ซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="9d4f0-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="9d4f0-124">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="9d4f0-124">Example 2</span></span>

<span data-ttu-id="9d4f0-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` ส่งกลับวันที่เซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง  **"24-12-2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="9d4f0-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d4f0-126">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9d4f0-126">Additional resources</span></span>

[<span data-ttu-id="9d4f0-127">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="9d4f0-127">Date and time functions</span></span>](er-functions-category-datetime.md)
