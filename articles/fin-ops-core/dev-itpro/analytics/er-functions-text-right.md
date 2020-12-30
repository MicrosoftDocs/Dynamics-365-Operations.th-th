---
title: ฟังก์ชั่น RIGHT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ RIGHT (ER)
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 13884182cb986564e81f310993747997341ffc07
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682954"
---
# <a name="right-er-function"></a><span data-ttu-id="fce78-103">ฟังก์ชั่น RIGHT ER</span><span class="sxs-lookup"><span data-stu-id="fce78-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fce78-104">ฟังก์ชัน `RIGHT` ส่งกลับค่า *สตริง* ที่แสดงจำนวนอักขระที่ระบุจากจุดสิ้นสุดของสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="fce78-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce78-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="fce78-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="fce78-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="fce78-106">Arguments</span></span>

<span data-ttu-id="fce78-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="fce78-107">`text`: *String*</span></span>

<span data-ttu-id="fce78-108">ค่า *สตริง* ที่แสดงถึงข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="fce78-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="fce78-109">`number`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="fce78-109">`number`: *Integer*</span></span>

<span data-ttu-id="fce78-110">จำนวนอักขระที่ต้องถูกส่งกลับจากจุดสิ้นสุดของข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="fce78-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="fce78-111">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="fce78-111">Return values</span></span>

<span data-ttu-id="fce78-112">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="fce78-112">*String*</span></span>

<span data-ttu-id="fce78-113">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="fce78-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="fce78-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="fce78-114">Example</span></span>

<span data-ttu-id="fce78-115">`RIGHT ("Sample", 3)` ส่งกลับค่า **"ple"**</span><span class="sxs-lookup"><span data-stu-id="fce78-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fce78-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fce78-116">Additional resources</span></span>

[<span data-ttu-id="fce78-117">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="fce78-117">Text functions</span></span>](er-functions-category-text.md)
