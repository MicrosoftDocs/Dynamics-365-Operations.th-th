---
title: ฟังก์ชัน LOWER ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ LOWER (ER)
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: b016feb0c907ef384eae91840791c357d61cf634
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916832"
---
# <span data-ttu-id="21415-103"><a name="LOWER">ฟังก์ชัน LOWER ER</a></span><span class="sxs-lookup"><span data-stu-id="21415-103"><a name="LOWER">LOWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21415-104">ฟังก์ชัน `LOWER` ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากที่ถูกแปลงเป็นตัวพิมพ์เล็ก</span><span class="sxs-lookup"><span data-stu-id="21415-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="21415-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="21415-105">Syntax</span></span>

```
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="21415-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="21415-106">Arguments</span></span>

<span data-ttu-id="21415-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="21415-107">`text`: *String*</span></span>

<span data-ttu-id="21415-108">ค่า *สตริง* ที่ระบุข้อความ</span><span class="sxs-lookup"><span data-stu-id="21415-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="21415-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="21415-109">Return values</span></span>

<span data-ttu-id="21415-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="21415-110">*String*</span></span>

<span data-ttu-id="21415-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="21415-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="21415-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="21415-112">Example</span></span>

<span data-ttu-id="21415-113">`LOWER ("Sample")` ส่งกลับ **"ตัวอย่าง"**</span><span class="sxs-lookup"><span data-stu-id="21415-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21415-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="21415-114">Additional resources</span></span>

[<span data-ttu-id="21415-115">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="21415-115">Text functions</span></span>](er-functions-category-text.md)
