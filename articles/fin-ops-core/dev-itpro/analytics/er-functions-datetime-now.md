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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb5b2fa1b8c466582b15d60a56260f0f7111ebd9
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042354"
---
# <span data-ttu-id="a0b1a-103"><a name="NOW">ฟังก์ชัน NOW ER</a></span><span class="sxs-lookup"><span data-stu-id="a0b1a-103"><a name="NOW">NOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0b1a-104">ฟังก์ชัน `NOW` ส่งคืนค่า *DateTime* ที่แสดงถึงวันที่และเวลาของเซิร์ฟเวอร์แอปลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a0b1a-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b1a-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="a0b1a-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="a0b1a-106">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="a0b1a-106">Return values</span></span>

<span data-ttu-id="a0b1a-107">*วันที่และเวลา*</span><span class="sxs-lookup"><span data-stu-id="a0b1a-107">*DateTime*</span></span>

<span data-ttu-id="a0b1a-108">ค่าวันที่/เวลาที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="a0b1a-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="a0b1a-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a0b1a-109">Example</span></span>

<span data-ttu-id="a0b1a-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` ส่งคืนค่าวันที่/เวลาของเซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="a0b1a-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0b1a-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a0b1a-111">Additional resources</span></span>

[<span data-ttu-id="a0b1a-112">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="a0b1a-112">Date and time functions</span></span>](er-functions-category-datetime.md)
