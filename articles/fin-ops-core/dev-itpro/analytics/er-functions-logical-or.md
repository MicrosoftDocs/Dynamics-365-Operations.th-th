---
title: ฟังก์ชัน OR ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) OR
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 7c2f110185330ee1e0cc6dc9ac534ae697e4b19b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565867"
---
# <a name="or-er-function"></a><span data-ttu-id="663de-103">ฟังก์ชัน OR ER</span><span class="sxs-lookup"><span data-stu-id="663de-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="663de-104">ฟังก์ชัน `OR` ส่งกลับค่า *บูลีน* ของ **FALSE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="663de-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="663de-105">ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง ฟังก์ชันจะส่งกลับค่า *บูลีน* ของ **TRUE**</span><span class="sxs-lookup"><span data-stu-id="663de-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="663de-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="663de-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="663de-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="663de-107">Arguments</span></span>

<span data-ttu-id="663de-108">`condition 1`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="663de-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="663de-109">นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องถูกทดสอบ</span><span class="sxs-lookup"><span data-stu-id="663de-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="663de-110">ต้องระบุอาร์กิวเมนต์นี้</span><span class="sxs-lookup"><span data-stu-id="663de-110">This argument is required.</span></span>

<span data-ttu-id="663de-111">`condition N`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="663de-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="663de-112">นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องถูกทดสอบ</span><span class="sxs-lookup"><span data-stu-id="663de-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="663de-113">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="663de-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="663de-114">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="663de-114">Return values</span></span>

<span data-ttu-id="663de-115">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="663de-115">*Boolean*</span></span>

<span data-ttu-id="663de-116">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="663de-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="663de-117">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="663de-117">Example</span></span>

<span data-ttu-id="663de-118">`OR (1=2, "a"="a")` ส่งกลับค่า **TRUE**</span><span class="sxs-lookup"><span data-stu-id="663de-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="663de-119">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="663de-119">Additional resources</span></span>

[<span data-ttu-id="663de-120">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="663de-120">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]