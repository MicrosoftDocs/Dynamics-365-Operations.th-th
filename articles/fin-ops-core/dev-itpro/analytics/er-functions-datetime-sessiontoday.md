---
title: ฟังก์ชัน SESSIONTODAY ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SESSIONTODAY
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 483ff46a27068bc2d70c80a848f0329861c914b3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042285"
---
# <span data-ttu-id="108e6-103"><a name="SESSIONTODAY">ฟังก์ชัน SESSIONTODAY ER</a></span><span class="sxs-lookup"><span data-stu-id="108e6-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="108e6-104">ฟังก์ชัน `SESSIONTODAY` ส่งคืนค่า *Date* ที่แสดงถึงวันที่เซสชันแอปพลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="108e6-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="108e6-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="108e6-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="108e6-106">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="108e6-106">Return values</span></span>

<span data-ttu-id="108e6-107">*วันที่*</span><span class="sxs-lookup"><span data-stu-id="108e6-107">*Date*</span></span>

<span data-ttu-id="108e6-108">ค่าวันที่ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="108e6-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="108e6-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="108e6-109">Example</span></span>

<span data-ttu-id="108e6-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` ส่งกลับวันที่เซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24-12-2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="108e6-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="108e6-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="108e6-111">Additional resources</span></span>

[<span data-ttu-id="108e6-112">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="108e6-112">Date and time functions</span></span>](er-functions-category-datetime.md)
