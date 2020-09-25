---
title: ฟังก์ชัน ADDDAYS ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ADDDAYS
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 998cf2c0dac67040814d4a32e433b465ec51f88c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743386"
---
# <a name="adddays-er-function"></a><span data-ttu-id="851fb-103">ฟังก์ชัน ADDDAYS ER</span><span class="sxs-lookup"><span data-stu-id="851fb-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="851fb-104">ฟังก์ชัน `ADDDAYS` คำนวณค่า *DateTime* ที่เป็นจำนวนวันที่ระบุก่อนหรือหลังวันที่เริ่มต้นที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="851fb-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="851fb-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="851fb-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="851fb-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="851fb-106">Arguments</span></span>

<span data-ttu-id="851fb-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="851fb-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="851fb-108">ค่าวันที่/เวลาที่แสดงวันที่ที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="851fb-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="851fb-109">`days`: *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="851fb-109">`days`: *Integer*</span></span>

<span data-ttu-id="851fb-110">จำนวนวันก่อนหรือหลัง `datetime`</span><span class="sxs-lookup"><span data-stu-id="851fb-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="851fb-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="851fb-111">Return values</span></span>

<span data-ttu-id="851fb-112">*วันที่และเวลา*</span><span class="sxs-lookup"><span data-stu-id="851fb-112">*DateTime*</span></span>

<span data-ttu-id="851fb-113">ค่าวันที่/เวลาที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="851fb-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="851fb-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="851fb-114">Usage notes</span></span>

<span data-ttu-id="851fb-115">ค่าบวกสำหรับการทำให้เกิด `days` ในวันที่ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="851fb-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="851fb-116">ค่าลบจะให้ผลตอบแทนวันที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="851fb-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="851fb-117">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="851fb-117">Example 1</span></span>

<span data-ttu-id="851fb-118">`ADDDAYS (NOW(), 7)` ส่งกลับวันและเวลาเจ็ดวันในอนาคต</span><span class="sxs-lookup"><span data-stu-id="851fb-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="851fb-119">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="851fb-119">Example 2</span></span>

<span data-ttu-id="851fb-120">`ADDDAYS (NOW(), -3)` ส่งกลับวันและเวลาสามวันในอดีต</span><span class="sxs-lookup"><span data-stu-id="851fb-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="851fb-121">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="851fb-121">Additional resources</span></span>

[<span data-ttu-id="851fb-122">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="851fb-122">Date and time functions</span></span>](er-functions-category-datetime.md)
