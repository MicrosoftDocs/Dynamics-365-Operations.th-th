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
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042699"
---
# <span data-ttu-id="0c6b1-103"><a name="INT64VALUE">ฟังก์ชัน INT64VALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="0c6b1-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c6b1-104">ฟังก์ชัน `INT64VALUE` ส่งกลับค่า *Int64* ที่แสดงถึงสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="0c6b1-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="0c6b1-105">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="0c6b1-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="0c6b1-106">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="0c6b1-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="0c6b1-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="0c6b1-107">Arguments</span></span>

<span data-ttu-id="0c6b1-108">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="0c6b1-108">`text`: *String*</span></span>

<span data-ttu-id="0c6b1-109">ค่าข้อความต้องถูกแปลงเป็นหมายเลย *Int64*</span><span class="sxs-lookup"><span data-stu-id="0c6b1-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="0c6b1-110">`number`: *จำนวนจริง* หรือ *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="0c6b1-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="0c6b1-111">ค่า *จำนวนจริง* or *จำนวนเต็ม* ที่เป็นตัวเลขต้องถูกแปลงเป็นหมายเลย *Int64*</span><span class="sxs-lookup"><span data-stu-id="0c6b1-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="0c6b1-112">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="0c6b1-112">Return values</span></span>

<span data-ttu-id="0c6b1-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="0c6b1-113">*Int64*</span></span>

<span data-ttu-id="0c6b1-114">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="0c6b1-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0c6b1-115">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0c6b1-115">Usage notes</span></span>

<span data-ttu-id="0c6b1-116">ตำแหน่งทศนิยมใดๆ จะถูกตัดออก</span><span class="sxs-lookup"><span data-stu-id="0c6b1-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="0c6b1-117">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="0c6b1-117">Example 1</span></span>

<span data-ttu-id="0c6b1-118">`INT64VALUE ("22565422744")` ส่งกลับค่า *Int64* **22565422744**</span><span class="sxs-lookup"><span data-stu-id="0c6b1-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0c6b1-119">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="0c6b1-119">Example 2</span></span>

<span data-ttu-id="0c6b1-120">`INT64VALUE ( VALUE("22565422744.77"))` ส่งกลับค่า *Int64* **22565422744**</span><span class="sxs-lookup"><span data-stu-id="0c6b1-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c6b1-121">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0c6b1-121">Additional resources</span></span>

[<span data-ttu-id="0c6b1-122">ฟังก์ชันการแปลงของชนิด</span><span class="sxs-lookup"><span data-stu-id="0c6b1-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
