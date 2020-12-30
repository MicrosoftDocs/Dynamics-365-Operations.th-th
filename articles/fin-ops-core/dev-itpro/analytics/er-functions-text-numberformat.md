---
title: ฟังก์ชัน NUMBERFORMAT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ NUMBERFORMAT (ER)
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 2c3907d1d2c74c852f4f90731e5f4bc23bfbd717
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680277"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="d1499-103">ฟังก์ชัน NUMBERFORMAT ER</span><span class="sxs-lookup"><span data-stu-id="d1499-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1499-104">ฟังก์ชัน `NUMBERFORMAT` ส่งกลับค่า *สตริง* ที่แสดงหมายเลขที่ระบุในรูปแบบที่ระบุและใน [ภาษา](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="d1499-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="d1499-105">สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) และ [กำหนดเอง](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx)</span><span class="sxs-lookup"><span data-stu-id="d1499-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d1499-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="d1499-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="d1499-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="d1499-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="d1499-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="d1499-108">Arguments</span></span>

<span data-ttu-id="d1499-109">`number`: *จำนวนเต็ม* หรือ *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="d1499-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="d1499-110">ค่าตัวเลขที่ระบุหมายเลขที่ต้องถูกจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="d1499-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="d1499-111">`format` : *สตริง*</span><span class="sxs-lookup"><span data-stu-id="d1499-111">`format` : *String*</span></span>

<span data-ttu-id="d1499-112">ค่า *สตริง* ที่แสดงถึงรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="d1499-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="d1499-113">`culture`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="d1499-113">`culture`: *String*</span></span>

<span data-ttu-id="d1499-114">ค่า *สตริง* ที่แสดงถึงภาษาที่จะใช้สำหรับการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="d1499-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="d1499-115">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="d1499-115">Return values</span></span>

<span data-ttu-id="d1499-116">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="d1499-116">*String*</span></span>

<span data-ttu-id="d1499-117">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="d1499-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d1499-118">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d1499-118">Usage notes</span></span>

<span data-ttu-id="d1499-119">ถ้าภาษาไม่ได้ถูกกำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก บริบทที่มีการเรียกใช้ฟังก์ชันนี้จะกำหนดภาษาที่ใช้ในการจัดรูปแบบตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d1499-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="d1499-120">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="d1499-120">Example 1</span></span>

<span data-ttu-id="d1499-121">สำหรับภาษา **EN-US** `NUMBERFORMAT (0.45, "p")` ส่งกลับค่า **"45.00 %"** และ `NUMBERFORMAT (10.45, "#")` ส่งกลับค่า **"10"**</span><span class="sxs-lookup"><span data-stu-id="d1499-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d1499-122">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="d1499-122">Example 2</span></span>

<span data-ttu-id="d1499-123">`NUMBERFORMAT (10/3, "F2", "de")` ส่งกลับค่า **3,33** ในขณะที่ `NUMBERFORMAT (10/3, "F2", "en-us")` ส่งกลับค่า **3.33**</span><span class="sxs-lookup"><span data-stu-id="d1499-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1499-124">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d1499-124">Additional resources</span></span>

[<span data-ttu-id="d1499-125">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="d1499-125">Text functions</span></span>](er-functions-category-text.md)
