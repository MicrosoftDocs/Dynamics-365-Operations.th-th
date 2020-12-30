---
title: ฟังก์ชัน NOW ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ NOW (ER)
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
ms.openlocfilehash: 0c3cfefd36db44608f05225746704aa3fbe4fc2c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682376"
---
# <a name="now-er-function"></a><span data-ttu-id="d9de1-103">ฟังก์ชัน NOW ER</span><span class="sxs-lookup"><span data-stu-id="d9de1-103">NOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9de1-104">ฟังก์ชัน `NOW` ส่งคืนค่า *DateTime* ที่แสดงถึงวันที่และเวลาของเซิร์ฟเวอร์แอปลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d9de1-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9de1-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="d9de1-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="d9de1-106">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="d9de1-106">Return values</span></span>

<span data-ttu-id="d9de1-107">*วันที่และเวลา*</span><span class="sxs-lookup"><span data-stu-id="d9de1-107">*DateTime*</span></span>

<span data-ttu-id="d9de1-108">ค่าวันที่/เวลาที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="d9de1-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="d9de1-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d9de1-109">Example</span></span>

<span data-ttu-id="d9de1-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` ส่งคืนค่าวันที่/เวลาของเซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="d9de1-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9de1-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d9de1-111">Additional resources</span></span>

[<span data-ttu-id="d9de1-112">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d9de1-112">Date and time functions</span></span>](er-functions-category-datetime.md)
