---
title: ฟังก์ชัน ER SESSIONNOW
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SESSIONNOW
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
ms.openlocfilehash: 47b88a1ca0ea9fd09c2a82963901d9ace78891bb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746806"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="a0c21-103">ฟังก์ชัน ER SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="a0c21-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0c21-104">ฟังก์ชัน `SESSIONNOW` ส่งคืนค่า *DateTime* ที่แสดงถึงวันที่และเวลาของเซสชันแอปลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a0c21-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0c21-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="a0c21-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="a0c21-106">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="a0c21-106">Return values</span></span>

<span data-ttu-id="a0c21-107">*วันที่และเวลา*</span><span class="sxs-lookup"><span data-stu-id="a0c21-107">*DateTime*</span></span>

<span data-ttu-id="a0c21-108">ค่าวันที่/เวลาที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="a0c21-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="a0c21-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a0c21-109">Example</span></span>

<span data-ttu-id="a0c21-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` ส่งกลับวันที่/เวลาเซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24.12.2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a0c21-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0c21-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a0c21-111">Additional resources</span></span>

[<span data-ttu-id="a0c21-112">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="a0c21-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]