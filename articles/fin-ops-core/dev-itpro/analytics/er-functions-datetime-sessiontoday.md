---
title: ฟังก์ชัน SESSIONTODAY ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SESSIONTODAY
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 6d0fcbbf1a1fb0809e3f76161314f38bcd8a74aa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746784"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="1efd9-103">ฟังก์ชัน SESSIONTODAY ER</span><span class="sxs-lookup"><span data-stu-id="1efd9-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1efd9-104">ฟังก์ชัน `SESSIONTODAY` ส่งคืนค่า *Date* ที่แสดงถึงวันที่เซสชันแอปพลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="1efd9-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="1efd9-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="1efd9-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="1efd9-106">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="1efd9-106">Return values</span></span>

<span data-ttu-id="1efd9-107">*วันที่*</span><span class="sxs-lookup"><span data-stu-id="1efd9-107">*Date*</span></span>

<span data-ttu-id="1efd9-108">ค่าวันที่ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="1efd9-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="1efd9-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="1efd9-109">Example</span></span>

<span data-ttu-id="1efd9-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` ส่งกลับวันที่เซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24-12-2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1efd9-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1efd9-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1efd9-111">Additional resources</span></span>

[<span data-ttu-id="1efd9-112">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="1efd9-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]