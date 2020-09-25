---
title: ฟังก์ชัน DATETODATETIME ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATETODATETIME
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
ms.openlocfilehash: eac09c9b410815ad9ae71dec53fc0416b020ca1e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744826"
---
# <a name="datetodatetime-er-function"></a><span data-ttu-id="837f5-103">ฟังก์ชัน DATETODATETIME ER</span><span class="sxs-lookup"><span data-stu-id="837f5-103">DATETODATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="837f5-104">ฟังก์ชัน `DATETODATETIME` ส่งกลับค่า *DateTime* ที่ถูกแปลงจากค่าวันที่ที่กำหนดให้เป็นค่าวันที่/เวลาในเวลาสากล (เวลามาตรฐานกรีนิช \[GMT\])</span><span class="sxs-lookup"><span data-stu-id="837f5-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="837f5-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="837f5-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="837f5-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="837f5-106">Arguments</span></span>

<span data-ttu-id="837f5-107">`date`: *วันที่*</span><span class="sxs-lookup"><span data-stu-id="837f5-107">`date`: *Date*</span></span>

<span data-ttu-id="837f5-108">ค่าวันที่ที่แสดงวันที่ที่แปลง</span><span class="sxs-lookup"><span data-stu-id="837f5-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="837f5-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="837f5-109">Return values</span></span>

<span data-ttu-id="837f5-110">*วันที่และเวลา*</span><span class="sxs-lookup"><span data-stu-id="837f5-110">*DateTime*</span></span>

<span data-ttu-id="837f5-111">ค่าวันที่/เวลาที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="837f5-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="837f5-112">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="837f5-112">Example 1</span></span>

<span data-ttu-id="837f5-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` ส่งกลับวันที่ของเซสชัน Microsoft Dynamics 365 Finance ปัจจุบัน, 24 ธันวาคม 2015 เป็น **12/24/2015 12:00:00 น**</span><span class="sxs-lookup"><span data-stu-id="837f5-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="837f5-114">ในตัวอย่างนี้ **CompInfo** เป็นแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ของชนิด **Finance and Operations/Table** และอ้างอิงถึงตาราง CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="837f5-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="837f5-115">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="837f5-115">Example 2</span></span>

<span data-ttu-id="837f5-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` ส่งกลับค่าวันที่/เวลา **11/12/2019 12:00:00 น.**</span><span class="sxs-lookup"><span data-stu-id="837f5-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="837f5-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="837f5-117">Additional resources</span></span>

[<span data-ttu-id="837f5-118">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="837f5-118">Date and time functions</span></span>](er-functions-category-datetime.md)
