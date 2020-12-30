---
title: ฟังก์ชัน AND ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) AND
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
ms.openlocfilehash: 8ccb7feb1d0f6836e7e8001870034900f6a1f598
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687085"
---
# <a name="and-er-function"></a><span data-ttu-id="8df3b-103">ฟังก์ชัน AND ER</span><span class="sxs-lookup"><span data-stu-id="8df3b-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8df3b-104">ฟังก์ชัน `AND` ส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง</span><span class="sxs-lookup"><span data-stu-id="8df3b-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="8df3b-105">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="8df3b-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df3b-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="8df3b-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="8df3b-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="8df3b-107">Arguments</span></span>

<span data-ttu-id="8df3b-108">`condition 1`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="8df3b-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="8df3b-109">นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องถูกทดสอบ</span><span class="sxs-lookup"><span data-stu-id="8df3b-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="8df3b-110">ต้องระบุอาร์กิวเมนต์นี้</span><span class="sxs-lookup"><span data-stu-id="8df3b-110">This argument is required.</span></span>

<span data-ttu-id="8df3b-111">`condition N`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="8df3b-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="8df3b-112">นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องถูกทดสอบ</span><span class="sxs-lookup"><span data-stu-id="8df3b-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="8df3b-113">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="8df3b-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="8df3b-114">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="8df3b-114">Return values</span></span>

<span data-ttu-id="8df3b-115">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="8df3b-115">*Boolean*</span></span>

<span data-ttu-id="8df3b-116">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="8df3b-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8df3b-117">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8df3b-117">Usage notes</span></span>

<span data-ttu-id="8df3b-118">ในอาร์กิวเมนต์ของฟังก์ชันตรรกะ คุณสามารถใช้การอ้างอิงแหล่งข้อมูล ค่าตัวเลขและข้อความ ค่าบูลีน ตัวดำเนินการเปรียบเทียบ และฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="8df3b-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="8df3b-119">อย่างไรก็ตามอาร์กิวเมนต์ทั้งหมดต้องถูกประเมินเป็นค่า *บูลีน* ของ **TRUE** หรือ **FALSE**</span><span class="sxs-lookup"><span data-stu-id="8df3b-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="8df3b-120">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8df3b-120">Example</span></span>

<span data-ttu-id="8df3b-121">`AND (1=1, "a"="a")` ส่งกลับค่า **TRUE**</span><span class="sxs-lookup"><span data-stu-id="8df3b-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="8df3b-122">`AND (1=2, "a"="a")` ส่งกลับค่า **FALSE**</span><span class="sxs-lookup"><span data-stu-id="8df3b-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8df3b-123">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8df3b-123">Additional resources</span></span>

[<span data-ttu-id="8df3b-124">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="8df3b-124">Logical functions</span></span>](er-functions-category-logical.md)
