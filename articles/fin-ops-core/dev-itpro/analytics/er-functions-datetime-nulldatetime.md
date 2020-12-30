---
title: ฟังก์ชัน NULLDATETIME ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NULLDATETIME
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
ms.openlocfilehash: 65e9ef92dc30e46c297d93e262bad8878df47a0c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682304"
---
# <a name="nulldatetime-er-function"></a><span data-ttu-id="607d8-103">ฟังก์ชัน NULLDATETIME ER</span><span class="sxs-lookup"><span data-stu-id="607d8-103">NULLDATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="607d8-104">ฟังก์ชัน `NULLDATETIME` ส่งกลับค่า *DateTime* ที่แสดงค่าวัน/เวลา **ที่เป็น null** (1 มกราคม 1900) ในเวลาสากลที่สอดคล้องกัน (เวลามาตรฐานกรีนิช \[GMT\])</span><span class="sxs-lookup"><span data-stu-id="607d8-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="607d8-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="607d8-105">Syntax</span></span>

```vb
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="607d8-106">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="607d8-106">Return values</span></span>

<span data-ttu-id="607d8-107">*วันที่และเวลา*</span><span class="sxs-lookup"><span data-stu-id="607d8-107">*DateTime*</span></span>

<span data-ttu-id="607d8-108">ค่าวันที่/เวลาที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="607d8-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="607d8-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="607d8-109">Example</span></span>

<span data-ttu-id="607d8-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` ส่งกลับค่าสตริง **1900-01-01T00:00:00.0000000+00:00** ที่ถูกเรียกในระหว่างกระบวนการที่เริ่มต้นโดยผู้ใช้แอปพลิเคชันที่มีเวลาโซนเวลา **เวลามาตรฐานสากล (GMT)** ในส่วน **การกำหนดลักษณะภาษาและประเทศ/ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="607d8-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="607d8-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="607d8-111">Additional resources</span></span>

[<span data-ttu-id="607d8-112">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="607d8-112">Date and time functions</span></span>](er-functions-category-datetime.md)
