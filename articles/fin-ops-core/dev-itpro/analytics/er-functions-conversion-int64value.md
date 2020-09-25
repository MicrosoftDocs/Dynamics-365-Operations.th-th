---
title: ฟังก์ชัน INT64VALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) INT64VALUE
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 78b69b5280fb8c7ed99d73568097cd0c080a807a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744850"
---
# <a name="int64value-er-function"></a><span data-ttu-id="601e4-103">ฟังก์ชัน INT64VALUE ER</span><span class="sxs-lookup"><span data-stu-id="601e4-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="601e4-104">ฟังก์ชัน `INT64VALUE` ส่งกลับค่า *Int64* ที่แสดงถึงสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="601e4-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="601e4-105">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="601e4-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="601e4-106">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="601e4-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="601e4-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="601e4-107">Arguments</span></span>

<span data-ttu-id="601e4-108">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="601e4-108">`text`: *String*</span></span>

<span data-ttu-id="601e4-109">ค่าข้อความต้องถูกแปลงเป็นหมายเลย *Int64*</span><span class="sxs-lookup"><span data-stu-id="601e4-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="601e4-110">`number`: *จำนวนจริง* หรือ *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="601e4-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="601e4-111">ค่า *จำนวนจริง* or *จำนวนเต็ม* ที่เป็นตัวเลขต้องถูกแปลงเป็นหมายเลย *Int64*</span><span class="sxs-lookup"><span data-stu-id="601e4-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="601e4-112">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="601e4-112">Return values</span></span>

<span data-ttu-id="601e4-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="601e4-113">*Int64*</span></span>

<span data-ttu-id="601e4-114">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="601e4-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="601e4-115">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="601e4-115">Usage notes</span></span>

<span data-ttu-id="601e4-116">ตำแหน่งทศนิยมใดๆ จะถูกตัดออก</span><span class="sxs-lookup"><span data-stu-id="601e4-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="601e4-117">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="601e4-117">Example 1</span></span>

<span data-ttu-id="601e4-118">`INT64VALUE ("22565422744")` ส่งกลับค่า *Int64* **22565422744**</span><span class="sxs-lookup"><span data-stu-id="601e4-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="601e4-119">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="601e4-119">Example 2</span></span>

<span data-ttu-id="601e4-120">`INT64VALUE ( VALUE("22565422744.77"))` ส่งกลับค่า *Int64* **22565422744**</span><span class="sxs-lookup"><span data-stu-id="601e4-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="601e4-121">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="601e4-121">Additional resources</span></span>

[<span data-ttu-id="601e4-122">ฟังก์ชันการแปลงของชนิด</span><span class="sxs-lookup"><span data-stu-id="601e4-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
