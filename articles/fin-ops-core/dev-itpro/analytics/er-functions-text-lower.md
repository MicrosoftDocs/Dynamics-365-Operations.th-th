---
title: ฟังก์ชัน LOWER ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ LOWER (ER)
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: e507a17f5125a3cba0d2434a1aaec0f04f0cd388
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562794"
---
# <a name="lower-er-function"></a><span data-ttu-id="b2e2e-103">ฟังก์ชัน LOWER ER</span><span class="sxs-lookup"><span data-stu-id="b2e2e-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2e2e-104">ฟังก์ชัน `LOWER` ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากที่ถูกแปลงเป็นตัวพิมพ์เล็ก</span><span class="sxs-lookup"><span data-stu-id="b2e2e-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e2e-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="b2e2e-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="b2e2e-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="b2e2e-106">Arguments</span></span>

<span data-ttu-id="b2e2e-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="b2e2e-107">`text`: *String*</span></span>

<span data-ttu-id="b2e2e-108">ค่า *สตริง* ที่ระบุข้อความ</span><span class="sxs-lookup"><span data-stu-id="b2e2e-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="b2e2e-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="b2e2e-109">Return values</span></span>

<span data-ttu-id="b2e2e-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="b2e2e-110">*String*</span></span>

<span data-ttu-id="b2e2e-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b2e2e-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b2e2e-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b2e2e-112">Example</span></span>

<span data-ttu-id="b2e2e-113">`LOWER ("Sample")` ส่งกลับ **"ตัวอย่าง"**</span><span class="sxs-lookup"><span data-stu-id="b2e2e-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2e2e-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b2e2e-114">Additional resources</span></span>

[<span data-ttu-id="b2e2e-115">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="b2e2e-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]