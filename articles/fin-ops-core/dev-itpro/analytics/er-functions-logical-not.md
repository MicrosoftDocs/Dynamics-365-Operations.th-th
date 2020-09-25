---
title: ฟังก์ชัน NOT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NOT
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
ms.openlocfilehash: af588c3714069040fa339d3121e6eb404b9be979
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744658"
---
# <a name="not-er-function"></a><span data-ttu-id="5d125-103">ฟังก์ชัน NOT ER</span><span class="sxs-lookup"><span data-stu-id="5d125-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d125-104">ฟังก์ชัน `NOT` ส่งกลับค่าตรรกศาสตร์ที่ถูกย้อนกลับของเงื่อนไขที่ระบุเป็นค่า *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="5d125-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d125-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="5d125-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="5d125-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="5d125-106">Arguments</span></span>

<span data-ttu-id="5d125-107">`condition`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="5d125-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="5d125-108">นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="5d125-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="5d125-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="5d125-109">Return values</span></span>

<span data-ttu-id="5d125-110">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="5d125-110">*Boolean*</span></span>

<span data-ttu-id="5d125-111">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="5d125-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="5d125-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="5d125-112">Example</span></span>

<span data-ttu-id="5d125-113">`NOT (TRUE)` ส่งกลับค่า **FALSE**</span><span class="sxs-lookup"><span data-stu-id="5d125-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d125-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5d125-114">Additional resources</span></span>

[<span data-ttu-id="5d125-115">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="5d125-115">Logical functions</span></span>](er-functions-category-logical.md)
