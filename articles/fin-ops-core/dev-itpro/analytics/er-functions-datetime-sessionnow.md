---
title: ฟังก์ชัน ER SESSIONNOW
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SESSIONNOW
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4dff6daa8fbd60ef1fc84d783e428d69477aac6d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916280"
---
# <span data-ttu-id="24472-103"><a name="">ฟังก์ชัน ER SESSIONNOW</a></span><span class="sxs-lookup"><span data-stu-id="24472-103"><a name="">SESSIONNOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24472-104">ฟังก์ชัน `SESSIONNOW` ส่งคืนค่า *DateTime* ที่แสดงถึงวันที่และเวลาของเซสชันแอปลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="24472-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="24472-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="24472-105">Syntax</span></span>

```
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="24472-106">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="24472-106">Return values</span></span>

<span data-ttu-id="24472-107">*วันที่และเวลา*</span><span class="sxs-lookup"><span data-stu-id="24472-107">*DateTime*</span></span>

<span data-ttu-id="24472-108">ค่าวันที่/เวลาที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="24472-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="24472-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="24472-109">Example</span></span>

<span data-ttu-id="24472-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` ส่งกลับวันที่/เวลาเซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24.12.2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="24472-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24472-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="24472-111">Additional resources</span></span>

[<span data-ttu-id="24472-112">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="24472-112">Date and time functions</span></span>](er-functions-category-datetime.md)
