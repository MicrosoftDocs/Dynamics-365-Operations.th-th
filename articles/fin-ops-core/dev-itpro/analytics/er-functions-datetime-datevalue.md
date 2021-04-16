---
title: ฟังก์ชัน ER DATEVALUE
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATEVALUE
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: d760c3f874bfebad11b9497b136cb67df4e9ea61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746950"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="4bc78-103">ฟังก์ชัน ER DATEVALUE</span><span class="sxs-lookup"><span data-stu-id="4bc78-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bc78-104">ฟังก์ชัน `DATEVALUE` ส่งกลับค่า *Date* ที่แปลงจากค่าข้อความที่ให้ในรูปแบบที่ระบุและใน [Culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือกไปยังค่าวันที่</span><span class="sxs-lookup"><span data-stu-id="4bc78-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="4bc78-105">สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) และ [กำหนดเอง](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)</span><span class="sxs-lookup"><span data-stu-id="4bc78-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="4bc78-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="4bc78-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="4bc78-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="4bc78-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="4bc78-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="4bc78-108">Arguments</span></span>

<span data-ttu-id="4bc78-109">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="4bc78-109">`text`: *String*</span></span>

<span data-ttu-id="4bc78-110">ข้อความที่แสดงถึงค่าไปยังรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="4bc78-110">Text that represents the value to format.</span></span>

<span data-ttu-id="4bc78-111">`format`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="4bc78-111">`format`: *String*</span></span>

<span data-ttu-id="4bc78-112">รูปแบบของข้อความที่ให้</span><span class="sxs-lookup"><span data-stu-id="4bc78-112">The format of the given text.</span></span>

<span data-ttu-id="4bc78-113">`culture`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="4bc78-113">`culture`: *String*</span></span>

<span data-ttu-id="4bc78-114">วัฒนธรรมที่ใช้สำหรับการจัดรูปแบบของข้อความที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="4bc78-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="4bc78-115">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="4bc78-115">Return values</span></span>

<span data-ttu-id="4bc78-116">*วันที่*</span><span class="sxs-lookup"><span data-stu-id="4bc78-116">*Date*</span></span>

<span data-ttu-id="4bc78-117">ค่าวันที่ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="4bc78-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4bc78-118">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4bc78-118">Usage notes</span></span>

<span data-ttu-id="4bc78-119">เมื่อวัฒนธรรมไม่ได้กำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก ค่าของ `culture` จะถูกกำหนดโดยบริบทการเรียก</span><span class="sxs-lookup"><span data-stu-id="4bc78-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="4bc78-120">ตัวอย่างเช่น ถ้าฟังก์ชัน `DATEVALUE` ถูกเรียกโดยใช้ไวยากรณ์ 1 ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับส่วนประกอบ **FILE** ที่ถูกกำหนดค่าให้ใช้วัฒนธรรมเยอรมัน การแปลงจะทำโดยใช้วัฒนธรรมเยอรมัน</span><span class="sxs-lookup"><span data-stu-id="4bc78-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="4bc78-121">ค่า `culture` เริ่มต้นคือ **EN-US**</span><span class="sxs-lookup"><span data-stu-id="4bc78-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="4bc78-122">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="4bc78-122">Example 1</span></span>

<span data-ttu-id="4bc78-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` ส่งกลับค่าวันที่ **21 ธันวาคม 2016** ขึ้นอยู่กับรูปแบบที่กำหนดเองที่ระบุและวัฒนธรรม **EN-US** ของแอปพลิเคชันเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4bc78-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="4bc78-124">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="4bc78-124">Example 2</span></span>

<span data-ttu-id="4bc78-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` ส่งกลับค่า **วันที่ 21 มกราคม 2016** ตามรูปแบบและวัฒนธรรมที่กำหนดเองที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="4bc78-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="4bc78-126">อย่างไรก็ตาม `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` จะส่งข้อยกเว้นเพื่อแจ้งผู้ใช้ว่าไม่รับรู้สตริงที่ระบุว่าเป็นค่าวันที่สำหรับวัฒนธรรมที่ระบุที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="4bc78-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4bc78-127">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4bc78-127">Additional resources</span></span>

[<span data-ttu-id="4bc78-128">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="4bc78-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]