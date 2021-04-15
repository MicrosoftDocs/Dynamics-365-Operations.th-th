---
title: ฟังก์ชัน ABS ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ABS
author: NickSelin
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
ms.openlocfilehash: 2a3613483d53fb265741b5d6a34a91da443dcef7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753155"
---
# <a name="abs-er-function"></a><span data-ttu-id="a0203-103">ฟังก์ชัน ABS ER</span><span class="sxs-lookup"><span data-stu-id="a0203-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0203-104">ฟังก์ชัน `ABS` ส่งกลับค่าเงินเต็ม (โมดูล) ของจำนวนที่ระบุเป็นค่า *จริง*</span><span class="sxs-lookup"><span data-stu-id="a0203-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="a0203-105">กล่าวคือ ส่งคืนหมายเลขโดยไม่มีเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="a0203-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0203-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="a0203-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="a0203-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="a0203-107">Arguments</span></span>

<span data-ttu-id="a0203-108">`number`: *จริง*</span><span class="sxs-lookup"><span data-stu-id="a0203-108">`number`: *Real*</span></span>

<span data-ttu-id="a0203-109">ค่าตัวเลขที่คุณต้องการโมดูลัส</span><span class="sxs-lookup"><span data-stu-id="a0203-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="a0203-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="a0203-110">Return values</span></span>

<span data-ttu-id="a0203-111">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="a0203-111">*Real*</span></span>

<span data-ttu-id="a0203-112">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="a0203-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="a0203-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a0203-113">Example</span></span>

<span data-ttu-id="a0203-114">`ABS (-1)` ส่งกลับค่า **1**</span><span class="sxs-lookup"><span data-stu-id="a0203-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0203-115">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a0203-115">Additional resources</span></span>

[<span data-ttu-id="a0203-116">ฟังก์ชันคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="a0203-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]