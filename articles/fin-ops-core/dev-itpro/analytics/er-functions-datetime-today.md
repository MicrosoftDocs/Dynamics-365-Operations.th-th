---
title: ฟังก์ชั่น ER TODAY
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) TODAY
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
ms.openlocfilehash: 94ef15d1971287e8bf13944bc8f693b567950031
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411448"
---
# <a name=""></a><span data-ttu-id="b1b30-103"><a name="TODAY">ฟังก์ชั่น ER TODAY</a></span><span class="sxs-lookup"><span data-stu-id="b1b30-103"><a name="TODAY">TODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1b30-104">ฟังก์ชัน `TODAY` ส่งคืนค่า *Date* ที่แสดงถึงวันที่เซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b1b30-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1b30-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="b1b30-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="b1b30-106">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="b1b30-106">Return values</span></span>

<span data-ttu-id="b1b30-107">*วันที่*</span><span class="sxs-lookup"><span data-stu-id="b1b30-107">*Date*</span></span>

<span data-ttu-id="b1b30-108">ค่าวันที่ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b1b30-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="b1b30-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b1b30-109">Example</span></span>

<span data-ttu-id="b1b30-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` ส่งคืนค่าวันที่ซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="b1b30-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1b30-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b1b30-111">Additional resources</span></span>

[<span data-ttu-id="b1b30-112">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="b1b30-112">Date and time functions</span></span>](er-functions-category-datetime.md)
