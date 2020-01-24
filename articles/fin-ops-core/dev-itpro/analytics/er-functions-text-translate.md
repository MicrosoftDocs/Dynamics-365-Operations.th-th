---
title: ฟังก์ชัน TRANSLATE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TRANSLATE (ER)
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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916717"
---
# <span data-ttu-id="0a22a-103"><a name="TRANSLATE">ฟังก์ชัน TRANSLATE ER</a></span><span class="sxs-lookup"><span data-stu-id="0a22a-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a22a-104">ฟังก์ชัน `TRANSLATE` ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากทั้งหมดหรือบางส่วนถูกแทนที่ด้วยสตริงอื่น</span><span class="sxs-lookup"><span data-stu-id="0a22a-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a22a-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="0a22a-105">Syntax</span></span>

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="0a22a-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="0a22a-106">Arguments</span></span>

<span data-ttu-id="0a22a-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="0a22a-107">`text`: *String*</span></span>

<span data-ttu-id="0a22a-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="0a22a-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="0a22a-109">`pattern`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="0a22a-109">`pattern`: *String*</span></span>

<span data-ttu-id="0a22a-110">ข้อความที่จะต้องถูกแทนที่</span><span class="sxs-lookup"><span data-stu-id="0a22a-110">The text that must be replaced.</span></span>

<span data-ttu-id="0a22a-111">`replacement`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="0a22a-111">`replacement`: *String*</span></span>

<span data-ttu-id="0a22a-112">ข้อความที่จะใช้เป็นการแทนที่</span><span class="sxs-lookup"><span data-stu-id="0a22a-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="0a22a-113">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="0a22a-113">Return values</span></span>

<span data-ttu-id="0a22a-114">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="0a22a-114">*String*</span></span>

<span data-ttu-id="0a22a-115">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="0a22a-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0a22a-116">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0a22a-116">Example</span></span>

<span data-ttu-id="0a22a-117">`TRANSLATE ("abcdef", "cd", "GH")` แทนที่รูปแบบ **"cd"** ด้วยสตริง **"GH"** และส่งกลับค่า **"abGHef"**</span><span class="sxs-lookup"><span data-stu-id="0a22a-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a22a-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0a22a-118">Additional resources</span></span>

[<span data-ttu-id="0a22a-119">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="0a22a-119">Text functions</span></span>](er-functions-category-text.md)
