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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84a62639b49db17fef1abcda75bc5ad7f08d1005
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917062"
---
# <span data-ttu-id="19539-103"><a name="ROUNDUP">ฟังก์ชัน ROUNDUP ER</a></span><span class="sxs-lookup"><span data-stu-id="19539-103"><a name="ROUNDUP">ROUNDUP ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19539-104">ฟังก์ชัน `ROUNDUP` ส่งคืนหมายเลขที่ระบุเป็นค่า *จริง* หลังจากที่ได้ถูกปัดเศษขึ้นเป็นจำนวนทศนิยมที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="19539-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="19539-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="19539-105">Syntax</span></span>

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="19539-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="19539-106">Arguments</span></span>

<span data-ttu-id="19539-107">`number`: *จริง*</span><span class="sxs-lookup"><span data-stu-id="19539-107">`number`: *Real*</span></span>

<span data-ttu-id="19539-108">ค่าตัวเลขที่ต้องถูกปัดเศษขึ้น</span><span class="sxs-lookup"><span data-stu-id="19539-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="19539-109">`decimals`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="19539-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="19539-110">ค่าของข้อความที่แสดงจำนวนของตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="19539-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="19539-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="19539-111">Return values</span></span>

<span data-ttu-id="19539-112">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="19539-112">*Real*</span></span>

<span data-ttu-id="19539-113">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="19539-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="19539-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="19539-114">Usage notes</span></span>

<span data-ttu-id="19539-115">ฟังก์ชันนี้ทำหน้าที่เหมือนกับ [ปัดเศษ](er-functions-mathematical-round.md) แต่จะปัดเศษจำนวนที่ระบุขึ้นเสมอ (ออกจากศูนย์)</span><span class="sxs-lookup"><span data-stu-id="19539-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="19539-116">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="19539-116">Example 1</span></span>

<span data-ttu-id="19539-117">`ROUNDUP (1200.763, 2)` ปัดเศษขึ้นเป็นทศนิยมสองตำแหน่ง และส่งกลับ **1200.77**</span><span class="sxs-lookup"><span data-stu-id="19539-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="19539-118">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="19539-118">Example 2</span></span>

<span data-ttu-id="19539-119">`ROUNDUP (1200.767, -3)` ปัดเศษขึ้นเป็นผลคูณที่ใกล้ที่สุดของ 1,000 และส่งกลับ **2000**</span><span class="sxs-lookup"><span data-stu-id="19539-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19539-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="19539-120">Additional resources</span></span>

[<span data-ttu-id="19539-121">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="19539-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
