---
title: ฟังก์ชัน IF ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) IF
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b8733022b44f3460e34a610140fd6d584ab990c2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687013"
---
# <a name="if-er-function"></a><span data-ttu-id="a5000-103">ฟังก์ชัน IF ER</span><span class="sxs-lookup"><span data-stu-id="a5000-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5000-104">ฟังก์ชัน `IF` ส่งคืนค่าที่ระบุค่าแรก หากตรงตามเงื่อนไขที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a5000-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="a5000-105">มิฉะนั้นจะส่งคืนค่าที่สองที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a5000-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="a5000-106">ค่าที่ถูกส่งกลับอาจเป็นค่าใดๆ ของชนิดข้อมูลที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="a5000-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5000-107">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="a5000-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="a5000-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="a5000-108">Arguments</span></span>

<span data-ttu-id="a5000-109">`condition`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="a5000-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="a5000-110">นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องถูกทดสอบ</span><span class="sxs-lookup"><span data-stu-id="a5000-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="a5000-111">`first value`: *ชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน*</span><span class="sxs-lookup"><span data-stu-id="a5000-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="a5000-112">ผลลัพธ์ที่ถูกส่งกลับถ้าเป็นไปตามเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="a5000-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="a5000-113">`second value`: *ชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน*</span><span class="sxs-lookup"><span data-stu-id="a5000-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="a5000-114">ผลลัพธ์ที่ถูกส่งกลับถ้าไม่เป็นไปตามเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="a5000-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="a5000-115">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="a5000-115">Return values</span></span>

<span data-ttu-id="a5000-116">*ชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน*</span><span class="sxs-lookup"><span data-stu-id="a5000-116">*Any of the supported data types*</span></span>

<span data-ttu-id="a5000-117">ค่าผลลัพธ์ของชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="a5000-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a5000-118">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a5000-118">Usage notes</span></span>

<span data-ttu-id="a5000-119">อาร์กิวเมนต์ `first value` และ `second value` ต้องถูกระบุและโดยใช้ชนิดข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a5000-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="a5000-120">มีข้อยกเว้นเกิดขึ้นในเวลาออกแบบถ้าชนิดข้อมูลของค่าที่ถูกกำหนดค่าไม่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="a5000-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="a5000-121">ถ้าค่าแรกและค่าที่สองคือค่าของชนิดข้อมูลของ *คอนเทนเนอร์ (เรกคอร์ด)* หรือชนิดข้อมูล *รายการเรกคอร์ด* ผลลัพธ์จะมีเฉพาะฟิลด์ที่มีอยู่ในค่าทั้งสองเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a5000-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="a5000-122">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a5000-122">Example</span></span>

<span data-ttu-id="a5000-123">`IF (1=2, "condition is met", "condition is not met")` จะส่งกลับสตริง **"ไม่เป็นไปตามเงื่อนไข"**</span><span class="sxs-lookup"><span data-stu-id="a5000-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5000-124">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a5000-124">Additional resources</span></span>

[<span data-ttu-id="a5000-125">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="a5000-125">Logical functions</span></span>](er-functions-category-logical.md)
