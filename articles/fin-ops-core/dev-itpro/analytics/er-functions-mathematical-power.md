---
title: ฟังก์ชัน POWER ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) POWER
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
ms.openlocfilehash: 858f59cf0bc6387b09cbb6f0c59f58ba8107582c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683340"
---
# <a name="power-er-function"></a><span data-ttu-id="be974-103">ฟังก์ชัน POWER ER</span><span class="sxs-lookup"><span data-stu-id="be974-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be974-104">ฟังก์ชัน `POWER` ส่งกลับค่า *จริง* ที่แสดงถึงผลของการเพิ่มจำนวนบวกที่ระบุให้กับพลังงานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="be974-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="be974-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="be974-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="be974-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="be974-106">Arguments</span></span>

<span data-ttu-id="be974-107">`number`: *จำนวนจริง* หรือ *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="be974-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="be974-108">ค่าตัวเลขที่ต้องถูกยกขึ้นกับพลังงานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="be974-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="be974-109">`power`: *จำนวนจริง* หรือ *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="be974-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="be974-110">ค่าตัวเลขที่แสดงถึงพลังงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="be974-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="be974-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="be974-111">Return values</span></span>

<span data-ttu-id="be974-112">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="be974-112">*Real*</span></span>

<span data-ttu-id="be974-113">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="be974-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="be974-114">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="be974-114">Example 1</span></span>

<span data-ttu-id="be974-115">`POWER (10, 2)` ส่งกลับค่า **100**</span><span class="sxs-lookup"><span data-stu-id="be974-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="be974-116">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="be974-116">Example 2</span></span>

<span data-ttu-id="be974-117">`POWER (4, 0.5)` ส่งกลับค่า **2**</span><span class="sxs-lookup"><span data-stu-id="be974-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be974-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="be974-118">Additional resources</span></span>

[<span data-ttu-id="be974-119">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="be974-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
