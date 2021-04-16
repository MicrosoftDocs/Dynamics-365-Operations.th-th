---
title: ฟังก์ชัน PADLEFT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ PADLEFT (ER)
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
ms.openlocfilehash: 806b1d318f18b0ade01f7b03909c90b1e4fd29b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746254"
---
# <a name="padleft-er-function"></a><span data-ttu-id="8225f-103">ฟังก์ชัน PADLEFT ER</span><span class="sxs-lookup"><span data-stu-id="8225f-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8225f-104">ฟังก์ชัน `PADLEFT` ส่งคืนค่า *สตริง* ของความยาวที่ระบุ ซึ่งมีการเริ่มต้นสตริงที่ระบุด้วยอักขระที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="8225f-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="8225f-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="8225f-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="8225f-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="8225f-106">Arguments</span></span>

<span data-ttu-id="8225f-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="8225f-107">`text`: *String*</span></span>

<span data-ttu-id="8225f-108">ค่า *สตริง* ที่แสดงถึงข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="8225f-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="8225f-109">`length`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="8225f-109">`length`: *Integer*</span></span>

<span data-ttu-id="8225f-110">ค่า *จำนวนเต็ม* ที่แสดงถึงจำนวนสุดท้ายของอักขระในสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="8225f-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="8225f-111">`padding chars`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="8225f-111">`padding chars`: *String*</span></span>

<span data-ttu-id="8225f-112">อักขระที่จะใช้สำหรับการระบุ</span><span class="sxs-lookup"><span data-stu-id="8225f-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="8225f-113">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="8225f-113">Return values</span></span>

<span data-ttu-id="8225f-114">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="8225f-114">*String*</span></span>

<span data-ttu-id="8225f-115">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="8225f-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8225f-116">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8225f-116">Example</span></span>

<span data-ttu-id="8225f-117">`PADLEFT ("1234", 10, "`&nbsp;`")` ส่งคืนสตริงข้อความ **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**</span><span class="sxs-lookup"><span data-stu-id="8225f-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8225f-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8225f-118">Additional resources</span></span>

[<span data-ttu-id="8225f-119">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="8225f-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]