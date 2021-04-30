---
title: ฟังก์ชัน NUMBERFORMAT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ NUMBERFORMAT (ER)
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
ms.openlocfilehash: 4a383b3f7c0ca7c4e5afc609cc8a7b1b07021b02
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890394"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="b9973-103">ฟังก์ชัน NUMBERFORMAT ER</span><span class="sxs-lookup"><span data-stu-id="b9973-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9973-104">ฟังก์ชัน `NUMBERFORMAT` ส่งกลับค่า *สตริง* ที่แสดงหมายเลขที่ระบุในรูปแบบที่ระบุและใน [ภาษา](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="b9973-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="b9973-105">สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](/dotnet/standard/base-types/standard-numeric-format-strings) และ [กำหนดเอง](/dotnet/standard/base-types/custom-numeric-format-strings)</span><span class="sxs-lookup"><span data-stu-id="b9973-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-numeric-format-strings) and [custom](/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b9973-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="b9973-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="b9973-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="b9973-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="b9973-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="b9973-108">Arguments</span></span>

<span data-ttu-id="b9973-109">`number`: *จำนวนเต็ม* หรือ *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="b9973-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="b9973-110">ค่าตัวเลขที่ระบุหมายเลขที่ต้องถูกจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="b9973-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="b9973-111">`format` : *สตริง*</span><span class="sxs-lookup"><span data-stu-id="b9973-111">`format` : *String*</span></span>

<span data-ttu-id="b9973-112">ค่า *สตริง* ที่แสดงถึงรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="b9973-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="b9973-113">`culture`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="b9973-113">`culture`: *String*</span></span>

<span data-ttu-id="b9973-114">ค่า *สตริง* ที่แสดงถึงภาษาที่จะใช้สำหรับการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="b9973-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="b9973-115">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="b9973-115">Return values</span></span>

<span data-ttu-id="b9973-116">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="b9973-116">*String*</span></span>

<span data-ttu-id="b9973-117">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b9973-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b9973-118">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b9973-118">Usage notes</span></span>

<span data-ttu-id="b9973-119">ถ้าภาษาไม่ได้ถูกกำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก บริบทที่มีการเรียกใช้ฟังก์ชันนี้จะกำหนดภาษาที่ใช้ในการจัดรูปแบบตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b9973-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="b9973-120">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="b9973-120">Example 1</span></span>

<span data-ttu-id="b9973-121">สำหรับภาษา **EN-US** `NUMBERFORMAT (0.45, "p")` ส่งกลับค่า **"45.00 %"** และ `NUMBERFORMAT (10.45, "#")` ส่งกลับค่า **"10"**</span><span class="sxs-lookup"><span data-stu-id="b9973-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b9973-122">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="b9973-122">Example 2</span></span>

<span data-ttu-id="b9973-123">`NUMBERFORMAT (10/3, "F2", "de")` ส่งกลับค่า **3,33** ในขณะที่ `NUMBERFORMAT (10/3, "F2", "en-us")` ส่งกลับค่า **3.33**</span><span class="sxs-lookup"><span data-stu-id="b9973-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9973-124">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b9973-124">Additional resources</span></span>

[<span data-ttu-id="b9973-125">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="b9973-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]