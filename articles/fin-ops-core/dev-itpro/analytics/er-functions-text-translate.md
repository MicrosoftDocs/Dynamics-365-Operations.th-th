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
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040928"
---
# <span data-ttu-id="902ed-103"><a name="TRANSLATE">ฟังก์ชัน TRANSLATE ER</a></span><span class="sxs-lookup"><span data-stu-id="902ed-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="902ed-104">ฟังก์ชัน `TRANSLATE` ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากทั้งหมดหรือบางส่วนถูกแทนที่ด้วยสตริงอื่น</span><span class="sxs-lookup"><span data-stu-id="902ed-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="902ed-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="902ed-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="902ed-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="902ed-106">Arguments</span></span>

<span data-ttu-id="902ed-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="902ed-107">`text`: *String*</span></span>

<span data-ttu-id="902ed-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="902ed-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="902ed-109">`pattern`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="902ed-109">`pattern`: *String*</span></span>

<span data-ttu-id="902ed-110">ข้อความที่จะต้องถูกแทนที่</span><span class="sxs-lookup"><span data-stu-id="902ed-110">The text that must be replaced.</span></span>

<span data-ttu-id="902ed-111">`replacement`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="902ed-111">`replacement`: *String*</span></span>

<span data-ttu-id="902ed-112">ข้อความที่จะใช้เป็นการแทนที่</span><span class="sxs-lookup"><span data-stu-id="902ed-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="902ed-113">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="902ed-113">Return values</span></span>

<span data-ttu-id="902ed-114">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="902ed-114">*String*</span></span>

<span data-ttu-id="902ed-115">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="902ed-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="902ed-116">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="902ed-116">Example</span></span>

<span data-ttu-id="902ed-117">`TRANSLATE ("abcdef", "cd", "GH")` แทนที่รูปแบบ **"cd"** ด้วยสตริง **"GH"** และส่งกลับค่า **"abGHef"**</span><span class="sxs-lookup"><span data-stu-id="902ed-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="902ed-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="902ed-118">Additional resources</span></span>

[<span data-ttu-id="902ed-119">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="902ed-119">Text functions</span></span>](er-functions-category-text.md)
