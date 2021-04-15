---
title: ฟังก์ชัน NUMERALSTOTEXT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ NUMERALSTOTEXT (ER)
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: e26890a0d99e0df631a3b3350d284e63aaed8e09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746158"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="45973-103">ฟังก์ชัน NUMERALSTOTEXT ER</span><span class="sxs-lookup"><span data-stu-id="45973-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45973-104">ฟังก์ชัน `NUMERALSTOTEXT` ส่งกลับหมายเลขที่ระบุเป็นค่า *สตริง* หลังจากที่ถูกสะกด (นั่นคือ ถูกแปลงเป็นสตริงข้อความ) ในภาษาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="45973-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="45973-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="45973-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="45973-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="45973-106">Arguments</span></span>

<span data-ttu-id="45973-107">`number`: *จำนวนเต็ม* หรือ *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="45973-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="45973-108">ค่าตัวเลขที่ระบุหมายเลขที่ต้องถูกสะกด</span><span class="sxs-lookup"><span data-stu-id="45973-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="45973-109">`language`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="45973-109">`language`: *String*</span></span>

<span data-ttu-id="45973-110">ค่า *สตริง* ที่แสดงถึงรหัสภาษา</span><span class="sxs-lookup"><span data-stu-id="45973-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="45973-111">`currency`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="45973-111">`currency`: *String*</span></span>

<span data-ttu-id="45973-112">ค่า *สตริง* ที่แสดงถึงรหัสสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="45973-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="45973-113">`print currency name flag`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="45973-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="45973-114">ค่า *บูลีน* ที่บ่งชี้ว่าต้องเพิ่มชื่อสกุลเงินในข้อความที่สะกดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="45973-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="45973-115">`decimal points`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="45973-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="45973-116">ค่า *เลขจำนวนเต็ม* ที่ระบุจำนวนของตำแหน่งทศนิยมที่ข้อความที่สะกดควรมี</span><span class="sxs-lookup"><span data-stu-id="45973-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="45973-117">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="45973-117">Return values</span></span>

<span data-ttu-id="45973-118">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="45973-118">*String*</span></span>

<span data-ttu-id="45973-119">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="45973-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="45973-120">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="45973-120">Usage notes</span></span>

<span data-ttu-id="45973-121">ไม่จำเป็นต้องระบุรหัสภาษา</span><span class="sxs-lookup"><span data-stu-id="45973-121">The language code is optional.</span></span> <span data-ttu-id="45973-122">หากมีการกำหนดเป็นสตริงว่าง รหัสภาษาสำหรับบริบทที่รันจะถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="45973-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="45973-123">รหัสภาษาเริ่มต้นคือ **EN-US**</span><span class="sxs-lookup"><span data-stu-id="45973-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="45973-124">รหัสภาษาสำหรับบริบทที่กำลังทำงานอยู่ถูกกำหนดในองค์ประกอบ **โฟลเดอร์** หรือ **ไฟล์** ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่กำลังทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="45973-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="45973-125">ไม่จำเป็นต้องระบุรหัสสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="45973-125">The currency code is optional.</span></span> <span data-ttu-id="45973-126">หากมีการกำหนดเป็นสตริงว่าง สกุลเงินของบริษัทสำหรับบริบทที่รันจะถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="45973-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="45973-127">อาร์กิวเมนต์ `print currency name flag` และ `decimal points` ถูกวิเคราะห์สำหรับรหัสภาษาต่อไปนี้เท่านั้น: **CS** **ET** **HU** **LT** **LV** **PL** และ **RU**</span><span class="sxs-lookup"><span data-stu-id="45973-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="45973-128">นอกจากนี้ อาร์กิวเมนต์ `print currency name flag` จะถูกวิเคราะห์สำหรับบริษัทที่บริบทของประเทศหรือของภูมิภาคสนับสนุนการกระจายของชื่อสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="45973-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="45973-129">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="45973-129">Example 1</span></span>

<span data-ttu-id="45973-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` ส่งกลับค่า **"หนึ่งพันสองร้อยสามสิบสี่และ 56"**</span><span class="sxs-lookup"><span data-stu-id="45973-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="45973-131">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="45973-131">Example 2</span></span>

<span data-ttu-id="45973-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` ส่งกลับค่า **"Sto dwadzieścia"**</span><span class="sxs-lookup"><span data-stu-id="45973-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="45973-133">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="45973-133">Example 3</span></span>

<span data-ttu-id="45973-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` ส่งกลับค่า **"Сто двадцать евро 21 евроцент"**</span><span class="sxs-lookup"><span data-stu-id="45973-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45973-135">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="45973-135">Additional resources</span></span>

[<span data-ttu-id="45973-136">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="45973-136">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]