---
title: ฟังก์ชัน ER DATEVALUE
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATEVALUE
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 700a48d2c5a77398267e6daaaea3ecb6c95e7f6e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916372"
---
# <span data-ttu-id="c9818-103"><a name="DATEVALUE">ฟังก์ชัน ER DATEVALUE</a></span><span class="sxs-lookup"><span data-stu-id="c9818-103"><a name="DATEVALUE">DATEVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9818-104">ฟังก์ชัน `DATEVALUE` ส่งกลับค่า *Date* ที่แปลงจากค่าข้อความที่ให้ในรูปแบบที่ระบุและใน [Culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือกไปยังค่าวันที่</span><span class="sxs-lookup"><span data-stu-id="c9818-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="c9818-105">สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) และ [กำหนดเอง](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)</span><span class="sxs-lookup"><span data-stu-id="c9818-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="c9818-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="c9818-106">Syntax 1</span></span>

```
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="c9818-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="c9818-107">Syntax 2</span></span>

```
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="c9818-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="c9818-108">Arguments</span></span>

<span data-ttu-id="c9818-109">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="c9818-109">`text`: *String*</span></span>

<span data-ttu-id="c9818-110">ข้อความที่แสดงถึงค่าไปยังรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="c9818-110">Text that represents the value to format.</span></span>

<span data-ttu-id="c9818-111">`format`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="c9818-111">`format`: *String*</span></span>

<span data-ttu-id="c9818-112">รูปแบบของข้อความที่ให้</span><span class="sxs-lookup"><span data-stu-id="c9818-112">The format of the given text.</span></span>

<span data-ttu-id="c9818-113">`culture`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="c9818-113">`culture`: *String*</span></span>

<span data-ttu-id="c9818-114">วัฒนธรรมที่ใช้สำหรับการจัดรูปแบบของข้อความที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="c9818-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="c9818-115">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="c9818-115">Return values</span></span>

<span data-ttu-id="c9818-116">*วันที่*</span><span class="sxs-lookup"><span data-stu-id="c9818-116">*Date*</span></span>

<span data-ttu-id="c9818-117">ค่าวันที่ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="c9818-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c9818-118">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c9818-118">Usage notes</span></span>

<span data-ttu-id="c9818-119">เมื่อวัฒนธรรมไม่ได้กำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก ค่าของ `culture` จะถูกกำหนดโดยบริบทการเรียก</span><span class="sxs-lookup"><span data-stu-id="c9818-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="c9818-120">ตัวอย่างเช่น ถ้าฟังก์ชัน `DATEVALUE` ถูกเรียกโดยใช้ไวยากรณ์ 1 ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับส่วนประกอบ **FILE** ที่ถูกกำหนดค่าให้ใช้วัฒนธรรมเยอรมัน การแปลงจะทำโดยใช้วัฒนธรรมเยอรมัน</span><span class="sxs-lookup"><span data-stu-id="c9818-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="c9818-121">ค่า `culture` เริ่มต้นคือ **EN-US**</span><span class="sxs-lookup"><span data-stu-id="c9818-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="c9818-122">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="c9818-122">Example 1</span></span>

<span data-ttu-id="c9818-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` ส่งกลับค่าวันที่ **21 ธันวาคม 2016** ขึ้นอยู่กับรูปแบบที่กำหนดเองที่ระบุและวัฒนธรรม **EN-US** ของแอปพลิเคชันเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c9818-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="c9818-124">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="c9818-124">Example 2</span></span>

<span data-ttu-id="c9818-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` ส่งกลับค่า **วันที่ 21 มกราคม 2016** ตามรูปแบบและวัฒนธรรมที่กำหนดเองที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="c9818-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="c9818-126">อย่างไรก็ตาม `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` จะส่งข้อยกเว้นเพื่อแจ้งผู้ใช้ว่าไม่รับรู้สตริงที่ระบุว่าเป็นค่าวันที่สำหรับวัฒนธรรมที่ระบุที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="c9818-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9818-127">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c9818-127">Additional resources</span></span>

[<span data-ttu-id="c9818-128">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c9818-128">Date and time functions</span></span>](er-functions-category-datetime.md)
