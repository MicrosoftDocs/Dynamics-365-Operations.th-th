---
title: ฟังก์ชัน ROUNDDOWN ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ROUNDDOWN
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 89fc134ec11a47506211ce68ec3aaf966d9a308b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744474"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="5245d-103">ฟังก์ชัน ROUNDDOWN ER</span><span class="sxs-lookup"><span data-stu-id="5245d-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5245d-104">ฟังก์ชัน `ROUNDDOWN` ส่งคืนหมายเลขที่ระบุเป็นค่า *จริง* หลังจากที่ได้ถูกปัดเศษลงเป็นจำนวนทศนิยมที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="5245d-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="5245d-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="5245d-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="5245d-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="5245d-106">Arguments</span></span>

<span data-ttu-id="5245d-107">`number`: *จริง*</span><span class="sxs-lookup"><span data-stu-id="5245d-107">`number`: *Real*</span></span>

<span data-ttu-id="5245d-108">ค่าตัวเลขที่ต้องถูกปัดเศษลง</span><span class="sxs-lookup"><span data-stu-id="5245d-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="5245d-109">`decimals`: *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="5245d-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="5245d-110">ค่าของข้อความที่แสดงจำนวนของตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="5245d-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="5245d-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="5245d-111">Return values</span></span>

<span data-ttu-id="5245d-112">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="5245d-112">*Real*</span></span>

<span data-ttu-id="5245d-113">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="5245d-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5245d-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="5245d-114">Usage notes</span></span>

<span data-ttu-id="5245d-115">ฟังก์ชันนี้ทำหน้าที่เหมือนกับ [ปัดเศษ](er-functions-mathematical-round.md) แต่จะปัดเศษจำนวนที่ระบุลงเสมอ (ไปยังศูนย์)</span><span class="sxs-lookup"><span data-stu-id="5245d-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="5245d-116">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="5245d-116">Example 1</span></span>

<span data-ttu-id="5245d-117">`ROUNDDOWN (1200.767, 2)` ปัดเศษลงเป็นทศนิยมสองตำแหน่ง และส่งกลับ **1200.76**</span><span class="sxs-lookup"><span data-stu-id="5245d-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="5245d-118">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="5245d-118">Example 2</span></span>

<span data-ttu-id="5245d-119">`ROUNDDOWN (1700.767, -3)` ปัดเศษลงเป็นผลคูณที่ใกล้ที่สุดของ 1,000 และส่งกลับ **1000**</span><span class="sxs-lookup"><span data-stu-id="5245d-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5245d-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5245d-120">Additional resources</span></span>

[<span data-ttu-id="5245d-121">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="5245d-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]