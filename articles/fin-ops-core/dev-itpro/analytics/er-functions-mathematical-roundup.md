---
title: ฟังก์ชัน ROUNDUP ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ROUNDUP
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 8ed86e2a848248dd8f2fc99401d12e0a162bf20a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686845"
---
# <a name="roundup-er-function"></a><span data-ttu-id="49d33-103">ฟังก์ชัน ROUNDUP ER</span><span class="sxs-lookup"><span data-stu-id="49d33-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49d33-104">ฟังก์ชัน `ROUNDUP` ส่งคืนหมายเลขที่ระบุเป็นค่า *จริง* หลังจากที่ได้ถูกปัดเศษขึ้นเป็นจำนวนทศนิยมที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="49d33-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="49d33-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="49d33-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="49d33-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="49d33-106">Arguments</span></span>

<span data-ttu-id="49d33-107">`number`: *จริง*</span><span class="sxs-lookup"><span data-stu-id="49d33-107">`number`: *Real*</span></span>

<span data-ttu-id="49d33-108">ค่าตัวเลขที่ต้องถูกปัดเศษขึ้น</span><span class="sxs-lookup"><span data-stu-id="49d33-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="49d33-109">`decimals`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="49d33-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="49d33-110">ค่าของข้อความที่แสดงจำนวนของตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="49d33-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="49d33-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="49d33-111">Return values</span></span>

<span data-ttu-id="49d33-112">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="49d33-112">*Real*</span></span>

<span data-ttu-id="49d33-113">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="49d33-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="49d33-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="49d33-114">Usage notes</span></span>

<span data-ttu-id="49d33-115">ฟังก์ชันนี้ทำหน้าที่เหมือนกับ [ปัดเศษ](er-functions-mathematical-round.md) แต่จะปัดเศษจำนวนที่ระบุขึ้นเสมอ (ออกจากศูนย์)</span><span class="sxs-lookup"><span data-stu-id="49d33-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="49d33-116">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="49d33-116">Example 1</span></span>

<span data-ttu-id="49d33-117">`ROUNDUP (1200.763, 2)` ปัดเศษขึ้นเป็นทศนิยมสองตำแหน่ง และส่งกลับ **1200.77**</span><span class="sxs-lookup"><span data-stu-id="49d33-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="49d33-118">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="49d33-118">Example 2</span></span>

<span data-ttu-id="49d33-119">`ROUNDUP (1200.767, -3)` ปัดเศษขึ้นเป็นผลคูณที่ใกล้ที่สุดของ 1,000 และส่งกลับ **2000**</span><span class="sxs-lookup"><span data-stu-id="49d33-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49d33-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="49d33-120">Additional resources</span></span>

[<span data-ttu-id="49d33-121">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="49d33-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
