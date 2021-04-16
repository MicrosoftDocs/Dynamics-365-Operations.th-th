---
title: ฟังก์ชัน DAYOFYEAR ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DAYOFYEAR
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 569e988db91ff992fb7db6e7fd6e8c6aa6a1a3e8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746926"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="85e9a-103">ฟังก์ชัน DAYOFYEAR ER</span><span class="sxs-lookup"><span data-stu-id="85e9a-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85e9a-104">ฟังก์ชัน `DAYOFYEAR` ส่งคืนค่าที่แสดง *จำนวนเต็ม* ของวันระหว่างวันที่ 1 มกราคมและวันที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="85e9a-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="85e9a-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="85e9a-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="85e9a-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="85e9a-106">Arguments</span></span>

<span data-ttu-id="85e9a-107">`date`: *วันที่*</span><span class="sxs-lookup"><span data-stu-id="85e9a-107">`date`: *Date*</span></span>

<span data-ttu-id="85e9a-108">ค่าวันที่ที่แสดงถึงวันที่ที่จะใช้สำหรับการคำนวณจำนวนวัน</span><span class="sxs-lookup"><span data-stu-id="85e9a-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="85e9a-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="85e9a-109">Return values</span></span>

<span data-ttu-id="85e9a-110">*จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="85e9a-110">*Integer*</span></span>

<span data-ttu-id="85e9a-111">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="85e9a-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="85e9a-112">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="85e9a-112">Example 1</span></span>

<span data-ttu-id="85e9a-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` ส่งกลับค่า **61**</span><span class="sxs-lookup"><span data-stu-id="85e9a-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="85e9a-114">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="85e9a-114">Example 2</span></span>

<span data-ttu-id="85e9a-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` ส่งกลับค่า **1**</span><span class="sxs-lookup"><span data-stu-id="85e9a-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85e9a-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="85e9a-116">Additional resources</span></span>

[<span data-ttu-id="85e9a-117">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="85e9a-117">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]