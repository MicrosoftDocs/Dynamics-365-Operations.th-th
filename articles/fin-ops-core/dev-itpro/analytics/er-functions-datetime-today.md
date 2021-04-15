---
title: ฟังก์ชั่น ER TODAY
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) TODAY
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
ms.openlocfilehash: 45ee4282acf4d6a5febe4b74b6955410e73e86a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746758"
---
# <a name="today-er-function"></a><span data-ttu-id="d3220-103">ฟังก์ชั่น ER TODAY</span><span class="sxs-lookup"><span data-stu-id="d3220-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3220-104">ฟังก์ชัน `TODAY` ส่งคืนค่า *Date* ที่แสดงถึงวันที่เซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d3220-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3220-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="d3220-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="d3220-106">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="d3220-106">Return values</span></span>

<span data-ttu-id="d3220-107">*วันที่*</span><span class="sxs-lookup"><span data-stu-id="d3220-107">*Date*</span></span>

<span data-ttu-id="d3220-108">ค่าวันที่ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="d3220-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="d3220-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d3220-109">Example</span></span>

<span data-ttu-id="d3220-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` ส่งคืนค่าวันที่ซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="d3220-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3220-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d3220-111">Additional resources</span></span>

[<span data-ttu-id="d3220-112">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d3220-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]