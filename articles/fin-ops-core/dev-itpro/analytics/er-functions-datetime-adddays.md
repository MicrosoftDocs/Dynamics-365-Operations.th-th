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
ms.openlocfilehash: dd1290538c506cd0db6eb21a304ff9812c808f17
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916464"
---
# <span data-ttu-id="a4b4b-103"><a name="ADDDAYS">ฟังก์ชัน ADDDAYS ER</a></span><span class="sxs-lookup"><span data-stu-id="a4b4b-103"><a name="ADDDAYS">ADDDAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4b4b-104">ฟังก์ชัน `ADDDAYS` คำนวณค่า *DateTime* ที่เป็นจำนวนวันที่ระบุก่อนหรือหลังวันที่เริ่มต้นที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a4b4b-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b4b-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="a4b4b-105">Syntax</span></span>

```
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="a4b4b-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="a4b4b-106">Arguments</span></span>

<span data-ttu-id="a4b4b-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="a4b4b-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="a4b4b-108">ค่าวันที่/เวลาที่แสดงวันที่ที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a4b4b-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="a4b4b-109">`days`: *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="a4b4b-109">`days`: *Integer*</span></span>

<span data-ttu-id="a4b4b-110">จำนวนวันก่อนหรือหลัง `datetime`</span><span class="sxs-lookup"><span data-stu-id="a4b4b-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="a4b4b-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="a4b4b-111">Return values</span></span>

<span data-ttu-id="a4b4b-112">*วันที่และเวลา*</span><span class="sxs-lookup"><span data-stu-id="a4b4b-112">*DateTime*</span></span>

<span data-ttu-id="a4b4b-113">ค่าวันที่/เวลาที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="a4b4b-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a4b4b-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a4b4b-114">Usage notes</span></span>

<span data-ttu-id="a4b4b-115">ค่าบวกสำหรับการทำให้เกิด `days` ในวันที่ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="a4b4b-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="a4b4b-116">ค่าลบจะให้ผลตอบแทนวันที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="a4b4b-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="a4b4b-117">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="a4b4b-117">Example 1</span></span>

<span data-ttu-id="a4b4b-118">`ADDDAYS (NOW(), 7)` ส่งกลับวันและเวลาเจ็ดวันในอนาคต</span><span class="sxs-lookup"><span data-stu-id="a4b4b-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="a4b4b-119">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="a4b4b-119">Example 2</span></span>

<span data-ttu-id="a4b4b-120">`ADDDAYS (NOW(), -3)` ส่งกลับวันและเวลาสามวันในอดีต</span><span class="sxs-lookup"><span data-stu-id="a4b4b-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4b4b-121">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a4b4b-121">Additional resources</span></span>

[<span data-ttu-id="a4b4b-122">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="a4b4b-122">Date and time functions</span></span>](er-functions-category-datetime.md)
