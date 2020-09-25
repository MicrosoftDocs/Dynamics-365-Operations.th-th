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
ms.openlocfilehash: b53535d1a000b72577be5c6284cc4676c43d591b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744610"
---
# <a name="abs-er-function"></a><span data-ttu-id="11674-103">ฟังก์ชัน ABS ER</span><span class="sxs-lookup"><span data-stu-id="11674-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11674-104">ฟังก์ชัน `ABS` ส่งกลับค่าเงินเต็ม (โมดูล) ของจำนวนที่ระบุเป็นค่า *จริง*</span><span class="sxs-lookup"><span data-stu-id="11674-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="11674-105">กล่าวคือ ส่งคืนหมายเลขโดยไม่มีเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="11674-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="11674-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="11674-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="11674-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="11674-107">Arguments</span></span>

<span data-ttu-id="11674-108">`number`: *จริง*</span><span class="sxs-lookup"><span data-stu-id="11674-108">`number`: *Real*</span></span>

<span data-ttu-id="11674-109">ค่าตัวเลขที่คุณต้องการโมดูลัส</span><span class="sxs-lookup"><span data-stu-id="11674-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="11674-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="11674-110">Return values</span></span>

<span data-ttu-id="11674-111">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="11674-111">*Real*</span></span>

<span data-ttu-id="11674-112">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="11674-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="11674-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="11674-113">Example</span></span>

<span data-ttu-id="11674-114">`ABS (-1)` ส่งกลับค่า **1**</span><span class="sxs-lookup"><span data-stu-id="11674-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11674-115">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="11674-115">Additional resources</span></span>

[<span data-ttu-id="11674-116">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="11674-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
