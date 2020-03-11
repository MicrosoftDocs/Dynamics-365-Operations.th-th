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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41f48fb49b2d28acf69fe05fe87644a4c43e81fe
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070563"
---
# <span data-ttu-id="6d34d-103"><a name="NUMBERFORMAT">ฟังก์ชัน NUMBERFORMAT ER</a></span><span class="sxs-lookup"><span data-stu-id="6d34d-103"><a name="NUMBERFORMAT">NUMBERFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d34d-104">ฟังก์ชัน `NUMBERFORMAT` ส่งกลับค่า *สตริง* ที่แสดงหมายเลขที่ระบุในรูปแบบที่ระบุและใน [ภาษา](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="6d34d-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="6d34d-105">สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) และ [กำหนดเอง](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx)</span><span class="sxs-lookup"><span data-stu-id="6d34d-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="6d34d-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="6d34d-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="6d34d-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="6d34d-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="6d34d-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="6d34d-108">Arguments</span></span>

<span data-ttu-id="6d34d-109">`number`: *จำนวนเต็ม* หรือ *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="6d34d-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="6d34d-110">ค่าตัวเลขที่ระบุหมายเลขที่ต้องถูกจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="6d34d-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="6d34d-111">`format` : *สตริง*</span><span class="sxs-lookup"><span data-stu-id="6d34d-111">`format` : *String*</span></span>

<span data-ttu-id="6d34d-112">ค่า *สตริง* ที่แสดงถึงรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="6d34d-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="6d34d-113">`culture`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="6d34d-113">`culture`: *String*</span></span>

<span data-ttu-id="6d34d-114">ค่า *สตริง* ที่แสดงถึงภาษาที่จะใช้สำหรับการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="6d34d-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="6d34d-115">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="6d34d-115">Return values</span></span>

<span data-ttu-id="6d34d-116">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="6d34d-116">*String*</span></span>

<span data-ttu-id="6d34d-117">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="6d34d-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6d34d-118">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6d34d-118">Usage notes</span></span>

<span data-ttu-id="6d34d-119">ถ้าภาษาไม่ได้ถูกกำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก บริบทที่มีการเรียกใช้ฟังก์ชันนี้จะกำหนดภาษาที่ใช้ในการจัดรูปแบบตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6d34d-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="6d34d-120">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="6d34d-120">Example 1</span></span>

<span data-ttu-id="6d34d-121">สำหรับภาษา **EN-US** `NUMBERFORMAT (0.45, "p")` ส่งกลับค่า **"45.00 %"** และ `NUMBERFORMAT (10.45, "#")` ส่งกลับค่า **"10"**</span><span class="sxs-lookup"><span data-stu-id="6d34d-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6d34d-122">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="6d34d-122">Example 2</span></span>

<span data-ttu-id="6d34d-123">`NUMBERFORMAT (10/3, "F2", "de")` ส่งกลับค่า **3,33** ในขณะที่ `NUMBERFORMAT (10/3, "F2", "en-us")` ส่งกลับค่า **3.33**</span><span class="sxs-lookup"><span data-stu-id="6d34d-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d34d-124">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6d34d-124">Additional resources</span></span>

[<span data-ttu-id="6d34d-125">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="6d34d-125">Text functions</span></span>](er-functions-category-text.md)
