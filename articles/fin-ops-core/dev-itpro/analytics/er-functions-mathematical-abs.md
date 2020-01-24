---
title: ฟังก์ชัน ABS ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ABS
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
ms.openlocfilehash: 9b32c5e8a413be3583177f565e2d4909330ad1e0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917108"
---
# <span data-ttu-id="e3570-103"><a name="ABS">ฟังก์ชัน ABS ER</a></span><span class="sxs-lookup"><span data-stu-id="e3570-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3570-104">ฟังก์ชัน `ABS` ส่งกลับค่าเงินเต็ม (โมดูล) ของจำนวนที่ระบุเป็นค่า *จริง*</span><span class="sxs-lookup"><span data-stu-id="e3570-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="e3570-105">กล่าวคือ ส่งคืนหมายเลขโดยไม่มีเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="e3570-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3570-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="e3570-106">Syntax</span></span>

```
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="e3570-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="e3570-107">Arguments</span></span>

<span data-ttu-id="e3570-108">`number`: *จริง*</span><span class="sxs-lookup"><span data-stu-id="e3570-108">`number`: *Real*</span></span>

<span data-ttu-id="e3570-109">ค่าตัวเลขที่คุณต้องการโมดูลัส</span><span class="sxs-lookup"><span data-stu-id="e3570-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="e3570-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="e3570-110">Return values</span></span>

<span data-ttu-id="e3570-111">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="e3570-111">*Real*</span></span>

<span data-ttu-id="e3570-112">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="e3570-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="e3570-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e3570-113">Example</span></span>

<span data-ttu-id="e3570-114">`ABS (-1)` ส่งกลับค่า **1**</span><span class="sxs-lookup"><span data-stu-id="e3570-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3570-115">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e3570-115">Additional resources</span></span>

[<span data-ttu-id="e3570-116">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="e3570-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
