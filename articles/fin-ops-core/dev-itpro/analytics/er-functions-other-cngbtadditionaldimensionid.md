---
title: ฟังก์ชัน CN_GBT_ADDITIONALDIMENSIONID ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CN_GBT_ADDITIONALDIMENSIONID (ER)
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
ms.openlocfilehash: 7fdc4527bc6115bdb3fca9d6a92d3d77a7c264c2
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744442"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="c9b45-103">ฟังก์ชัน CN_GBT_ADDITIONALDIMENSIONID ER</span><span class="sxs-lookup"><span data-stu-id="c9b45-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9b45-104">ฟังก์ชัน `CN_GBT_ADDITIONALDIMENSIONID` ส่งกลับค่า *สตริง* ที่แสดงถึงรหัสมิติทางการเงินเดียวที่ถูกนำมาจากสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="c9b45-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="c9b45-105">สตริงที่ระบุแสดงมิติทั้งหมดเป็นรายการของรหัสที่คั่นด้วยเครื่องหมายจุลภาค</span><span class="sxs-lookup"><span data-stu-id="c9b45-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b45-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="c9b45-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="c9b45-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="c9b45-107">Arguments</span></span>

<span data-ttu-id="c9b45-108">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="c9b45-108">`text`: *String*</span></span>

<span data-ttu-id="c9b45-109">ค่า *สตริง* ที่แสดงมิติทั้งหมดเป็นรายการของรหัสที่คั่นด้วยเครื่องหมายจุลภาค</span><span class="sxs-lookup"><span data-stu-id="c9b45-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="c9b45-110">`number`: เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="c9b45-110">`number`: Integer</span></span>

<span data-ttu-id="c9b45-111">ค่า *เลขจำนวนเต็ม* จะกำหนดรหัสลำดับของมิติที่ร้องขอในสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="c9b45-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="c9b45-112">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="c9b45-112">Return values</span></span>

<span data-ttu-id="c9b45-113">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="c9b45-113">*String*</span></span>

<span data-ttu-id="c9b45-114">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="c9b45-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c9b45-115">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="c9b45-115">Example</span></span>

<span data-ttu-id="c9b45-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)`  ส่งคืน **"CC"**</span><span class="sxs-lookup"><span data-stu-id="c9b45-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9b45-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c9b45-117">Additional resources</span></span>

[<span data-ttu-id="c9b45-118">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="c9b45-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
