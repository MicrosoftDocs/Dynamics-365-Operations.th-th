---
title: ฟังก์ชัน INTVALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) INTVALUE
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
ms.openlocfilehash: 2b279de39cf91c3919145735518034fc60cd3341
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917729"
---
# <span data-ttu-id="364cb-103"><a name="INTVALUE">ฟังก์ชัน INTVALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="364cb-103"><a name="INTVALUE">INTVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="364cb-104">ฟังก์ชัน `INTVALUE` ส่งกลับค่า *Int* ที่แสดงถึงสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="364cb-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="364cb-105">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="364cb-105">Syntax 1</span></span>

```
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="364cb-106">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="364cb-106">Syntax 2</span></span>

```
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="364cb-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="364cb-107">Arguments</span></span>

<span data-ttu-id="364cb-108">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="364cb-108">`text`: *String*</span></span>

<span data-ttu-id="364cb-109">ค่าข้อความต้องถูกแปลงเป็นหมายเลย *Int*</span><span class="sxs-lookup"><span data-stu-id="364cb-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="364cb-110">`number`: *จำนวนจริง* หรือ *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="364cb-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="364cb-111">ค่า *จำนวนจริง* or *จำนวนเต็ม* ที่เป็นตัวเลขต้องถูกแปลงเป็นหมายเลย *Int*</span><span class="sxs-lookup"><span data-stu-id="364cb-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="364cb-112">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="364cb-112">Return values</span></span>

<span data-ttu-id="364cb-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="364cb-113">*Int*</span></span>

<span data-ttu-id="364cb-114">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="364cb-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="364cb-115">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="364cb-115">Usage notes</span></span>

<span data-ttu-id="364cb-116">ตำแหน่งทศนิยมใดๆ จะถูกตัดออก</span><span class="sxs-lookup"><span data-stu-id="364cb-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="364cb-117">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="364cb-117">Example 1</span></span>

<span data-ttu-id="364cb-118">`INTVALUE ("100.77")` ส่งกลับค่า *Int* **100**</span><span class="sxs-lookup"><span data-stu-id="364cb-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="364cb-119">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="364cb-119">Example 2</span></span>

<span data-ttu-id="364cb-120">`INTVALUE (-100.77)` ส่งกลับค่า *Int* **-100**</span><span class="sxs-lookup"><span data-stu-id="364cb-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="364cb-121">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="364cb-121">Additional resources</span></span>

[<span data-ttu-id="364cb-122">ฟังก์ชันการแปลงของชนิด</span><span class="sxs-lookup"><span data-stu-id="364cb-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
