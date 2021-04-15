---
title: ฟังก์ชัน CN_GBT_ADDITIONALDIMENSIONID ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CN_GBT_ADDITIONALDIMENSIONID (ER)
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
ms.openlocfilehash: ac0b54476265171b3826e43600f99097701231e1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744402"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="aab83-103">ฟังก์ชัน CN_GBT_ADDITIONALDIMENSIONID ER</span><span class="sxs-lookup"><span data-stu-id="aab83-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aab83-104">ฟังก์ชัน `CN_GBT_ADDITIONALDIMENSIONID` ส่งกลับค่า *สตริง* ที่แสดงถึงรหัสมิติทางการเงินเดียวที่ถูกนำมาจากสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="aab83-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="aab83-105">สตริงที่ระบุแสดงมิติทั้งหมดเป็นรายการของรหัสที่คั่นด้วยเครื่องหมายจุลภาค</span><span class="sxs-lookup"><span data-stu-id="aab83-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="aab83-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="aab83-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="aab83-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="aab83-107">Arguments</span></span>

<span data-ttu-id="aab83-108">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="aab83-108">`text`: *String*</span></span>

<span data-ttu-id="aab83-109">ค่า *สตริง* ที่แสดงมิติทั้งหมดเป็นรายการของรหัสที่คั่นด้วยเครื่องหมายจุลภาค</span><span class="sxs-lookup"><span data-stu-id="aab83-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="aab83-110">`number`: เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="aab83-110">`number`: Integer</span></span>

<span data-ttu-id="aab83-111">ค่า *เลขจำนวนเต็ม* จะกำหนดรหัสลำดับของมิติที่ร้องขอในสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="aab83-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="aab83-112">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="aab83-112">Return values</span></span>

<span data-ttu-id="aab83-113">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="aab83-113">*String*</span></span>

<span data-ttu-id="aab83-114">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="aab83-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="aab83-115">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="aab83-115">Example</span></span>

<span data-ttu-id="aab83-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)`  ส่งคืน **"CC"**</span><span class="sxs-lookup"><span data-stu-id="aab83-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aab83-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="aab83-117">Additional resources</span></span>

[<span data-ttu-id="aab83-118">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="aab83-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]