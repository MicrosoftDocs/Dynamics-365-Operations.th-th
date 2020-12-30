---
title: ฟังก์ชัน DAYS ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DAYS
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 66398e624e4b9d69d4dc3ccf3ee8f97758f4f861
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682352"
---
# <a name="days-er-function"></a><span data-ttu-id="b6481-103">ฟังก์ชัน DAYS ER</span><span class="sxs-lookup"><span data-stu-id="b6481-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6481-104">ฟังก์ชัน `DAYS` ส่งคืนค่าที่แสดง *จำนวนเต็ม* ที่แสดงจำนวนของวันระหว่างวันที่ที่ระบุที่หนึ่งกับวันที่ที่ระบุที่สอง</span><span class="sxs-lookup"><span data-stu-id="b6481-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6481-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="b6481-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="b6481-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="b6481-106">Arguments</span></span>

<span data-ttu-id="b6481-107">`date 1`: *วันที่*</span><span class="sxs-lookup"><span data-stu-id="b6481-107">`date 1`: *Date*</span></span>

<span data-ttu-id="b6481-108">ค่าวันที่ที่แสดงถึงวันที่ที่จะใช้สำหรับการคำนวณจำนวนวัน</span><span class="sxs-lookup"><span data-stu-id="b6481-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="b6481-109">`date 2`: *วันที่*</span><span class="sxs-lookup"><span data-stu-id="b6481-109">`date 2`: *Date*</span></span>

<span data-ttu-id="b6481-110">ค่าวันที่ที่แสดงถึงวันที่สิ้นสุดที่จะใช้สำหรับการคำนวณจำนวนวัน</span><span class="sxs-lookup"><span data-stu-id="b6481-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="b6481-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="b6481-111">Return values</span></span>

<span data-ttu-id="b6481-112">*จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="b6481-112">*Integer*</span></span>

<span data-ttu-id="b6481-113">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b6481-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b6481-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b6481-114">Usage notes</span></span>

<span data-ttu-id="b6481-115">ฟังก์ชัน `DAYS` ส่งคืนค่าบวกเมื่อวันที่วันแรกเป็นวันที่หลังจากวันที่ที่สอง ส่งคืน **0** (ศูนย์) เมื่อวันที่วันแรกเท่ากับวันที่ที่สอง หรือส่งคืนค่าลบ เมื่อวันที่วันแรกเป็นวันที่ก่อนวันที่ที่สอง</span><span class="sxs-lookup"><span data-stu-id="b6481-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="b6481-116">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b6481-116">Example</span></span>

<span data-ttu-id="b6481-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` ส่งคืน **-1**</span><span class="sxs-lookup"><span data-stu-id="b6481-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6481-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b6481-118">Additional resources</span></span>

[<span data-ttu-id="b6481-119">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="b6481-119">Date and time functions</span></span>](er-functions-category-datetime.md)
