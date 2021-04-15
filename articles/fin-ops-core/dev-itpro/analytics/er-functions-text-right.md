---
title: ฟังก์ชั่น RIGHT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ RIGHT (ER)
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
ms.openlocfilehash: f59b12f0b3f7b100b953b2072677c83c836746ff
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746134"
---
# <a name="right-er-function"></a><span data-ttu-id="d3909-103">ฟังก์ชั่น RIGHT ER</span><span class="sxs-lookup"><span data-stu-id="d3909-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3909-104">ฟังก์ชัน `RIGHT` ส่งกลับค่า *สตริง* ที่แสดงจำนวนอักขระที่ระบุจากจุดสิ้นสุดของสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="d3909-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3909-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="d3909-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="d3909-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="d3909-106">Arguments</span></span>

<span data-ttu-id="d3909-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="d3909-107">`text`: *String*</span></span>

<span data-ttu-id="d3909-108">ค่า *สตริง* ที่แสดงถึงข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="d3909-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="d3909-109">`number`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="d3909-109">`number`: *Integer*</span></span>

<span data-ttu-id="d3909-110">จำนวนอักขระที่ต้องถูกส่งกลับจากจุดสิ้นสุดของข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="d3909-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="d3909-111">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="d3909-111">Return values</span></span>

<span data-ttu-id="d3909-112">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="d3909-112">*String*</span></span>

<span data-ttu-id="d3909-113">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="d3909-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d3909-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d3909-114">Example</span></span>

<span data-ttu-id="d3909-115">`RIGHT ("Sample", 3)` ส่งกลับค่า **"ple"**</span><span class="sxs-lookup"><span data-stu-id="d3909-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3909-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d3909-116">Additional resources</span></span>

[<span data-ttu-id="d3909-117">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="d3909-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]