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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a246496eca0d5a8538ac7f1577957e6b9eae4e3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743483"
---
# <a name="and-er-function"></a><span data-ttu-id="ecb5d-103">ฟังก์ชัน AND ER</span><span class="sxs-lookup"><span data-stu-id="ecb5d-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecb5d-104">ฟังก์ชัน `AND` ส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง</span><span class="sxs-lookup"><span data-stu-id="ecb5d-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="ecb5d-105">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="ecb5d-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb5d-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="ecb5d-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="ecb5d-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="ecb5d-107">Arguments</span></span>

<span data-ttu-id="ecb5d-108">`condition 1`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="ecb5d-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="ecb5d-109">นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องถูกทดสอบ</span><span class="sxs-lookup"><span data-stu-id="ecb5d-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="ecb5d-110">ต้องระบุอาร์กิวเมนต์นี้</span><span class="sxs-lookup"><span data-stu-id="ecb5d-110">This argument is required.</span></span>

<span data-ttu-id="ecb5d-111">`condition N`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="ecb5d-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="ecb5d-112">นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องถูกทดสอบ</span><span class="sxs-lookup"><span data-stu-id="ecb5d-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="ecb5d-113">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ecb5d-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="ecb5d-114">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="ecb5d-114">Return values</span></span>

<span data-ttu-id="ecb5d-115">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="ecb5d-115">*Boolean*</span></span>

<span data-ttu-id="ecb5d-116">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="ecb5d-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ecb5d-117">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ecb5d-117">Usage notes</span></span>

<span data-ttu-id="ecb5d-118">ในอาร์กิวเมนต์ของฟังก์ชันตรรกะ คุณสามารถใช้การอ้างอิงแหล่งข้อมูล ค่าตัวเลขและข้อความ ค่าบูลีน ตัวดำเนินการเปรียบเทียบ และฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="ecb5d-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="ecb5d-119">อย่างไรก็ตามอาร์กิวเมนต์ทั้งหมดต้องถูกประเมินเป็นค่า *บูลีน* ของ **TRUE** หรือ **FALSE**</span><span class="sxs-lookup"><span data-stu-id="ecb5d-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="ecb5d-120">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ecb5d-120">Example</span></span>

<span data-ttu-id="ecb5d-121">`AND (1=1, "a"="a")` ส่งกลับค่า **TRUE**</span><span class="sxs-lookup"><span data-stu-id="ecb5d-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="ecb5d-122">`AND (1=2, "a"="a")` ส่งกลับค่า **FALSE**</span><span class="sxs-lookup"><span data-stu-id="ecb5d-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ecb5d-123">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ecb5d-123">Additional resources</span></span>

[<span data-ttu-id="ecb5d-124">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="ecb5d-124">Logical functions</span></span>](er-functions-category-logical.md)
