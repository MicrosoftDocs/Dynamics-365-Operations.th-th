---
title: ฟังก์ชัน ROUNDUP ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ROUNDUP
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
ms.openlocfilehash: 4898f596108ff3c563da55a567a10da987d62d33
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744450"
---
# <a name="roundup-er-function"></a><span data-ttu-id="979e4-103">ฟังก์ชัน ROUNDUP ER</span><span class="sxs-lookup"><span data-stu-id="979e4-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="979e4-104">ฟังก์ชัน `ROUNDUP` ส่งคืนหมายเลขที่ระบุเป็นค่า *จริง* หลังจากที่ได้ถูกปัดเศษขึ้นเป็นจำนวนทศนิยมที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="979e4-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="979e4-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="979e4-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="979e4-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="979e4-106">Arguments</span></span>

<span data-ttu-id="979e4-107">`number`: *จริง*</span><span class="sxs-lookup"><span data-stu-id="979e4-107">`number`: *Real*</span></span>

<span data-ttu-id="979e4-108">ค่าตัวเลขที่ต้องถูกปัดเศษขึ้น</span><span class="sxs-lookup"><span data-stu-id="979e4-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="979e4-109">`decimals`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="979e4-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="979e4-110">ค่าของข้อความที่แสดงจำนวนของตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="979e4-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="979e4-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="979e4-111">Return values</span></span>

<span data-ttu-id="979e4-112">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="979e4-112">*Real*</span></span>

<span data-ttu-id="979e4-113">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="979e4-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="979e4-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="979e4-114">Usage notes</span></span>

<span data-ttu-id="979e4-115">ฟังก์ชันนี้ทำหน้าที่เหมือนกับ [ปัดเศษ](er-functions-mathematical-round.md) แต่จะปัดเศษจำนวนที่ระบุขึ้นเสมอ (ออกจากศูนย์)</span><span class="sxs-lookup"><span data-stu-id="979e4-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="979e4-116">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="979e4-116">Example 1</span></span>

<span data-ttu-id="979e4-117">`ROUNDUP (1200.763, 2)` ปัดเศษขึ้นเป็นทศนิยมสองตำแหน่ง และส่งกลับ **1200.77**</span><span class="sxs-lookup"><span data-stu-id="979e4-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="979e4-118">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="979e4-118">Example 2</span></span>

<span data-ttu-id="979e4-119">`ROUNDUP (1200.767, -3)` ปัดเศษขึ้นเป็นผลคูณที่ใกล้ที่สุดของ 1,000 และส่งกลับ **2000**</span><span class="sxs-lookup"><span data-stu-id="979e4-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="979e4-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="979e4-120">Additional resources</span></span>

[<span data-ttu-id="979e4-121">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="979e4-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]