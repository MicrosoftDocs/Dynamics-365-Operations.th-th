---
title: ฟังก์ชัน ABS ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ABS
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
ms.openlocfilehash: 12165174806395b3c36a1dbb227ed7a86def77b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565795"
---
# <a name="abs-er-function"></a><span data-ttu-id="20618-103">ฟังก์ชัน ABS ER</span><span class="sxs-lookup"><span data-stu-id="20618-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20618-104">ฟังก์ชัน `ABS` ส่งกลับค่าเงินเต็ม (โมดูล) ของจำนวนที่ระบุเป็นค่า *จริง*</span><span class="sxs-lookup"><span data-stu-id="20618-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="20618-105">กล่าวคือ ส่งคืนหมายเลขโดยไม่มีเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="20618-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="20618-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="20618-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="20618-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="20618-107">Arguments</span></span>

<span data-ttu-id="20618-108">`number`: *จริง*</span><span class="sxs-lookup"><span data-stu-id="20618-108">`number`: *Real*</span></span>

<span data-ttu-id="20618-109">ค่าตัวเลขที่คุณต้องการโมดูลัส</span><span class="sxs-lookup"><span data-stu-id="20618-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="20618-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="20618-110">Return values</span></span>

<span data-ttu-id="20618-111">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="20618-111">*Real*</span></span>

<span data-ttu-id="20618-112">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="20618-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="20618-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="20618-113">Example</span></span>

<span data-ttu-id="20618-114">`ABS (-1)` ส่งกลับค่า **1**</span><span class="sxs-lookup"><span data-stu-id="20618-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20618-115">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="20618-115">Additional resources</span></span>

[<span data-ttu-id="20618-116">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="20618-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]