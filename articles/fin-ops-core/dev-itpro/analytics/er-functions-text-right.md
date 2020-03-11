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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040882"
---
# <span data-ttu-id="03aa9-103"><a name="RIGHT">ฟังก์ชั่น RIGHT ER</a></span><span class="sxs-lookup"><span data-stu-id="03aa9-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03aa9-104">ฟังก์ชัน `RIGHT` ส่งกลับค่า *สตริง* ที่แสดงจำนวนอักขระที่ระบุจากจุดสิ้นสุดของสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="03aa9-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="03aa9-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="03aa9-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="03aa9-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="03aa9-106">Arguments</span></span>

<span data-ttu-id="03aa9-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="03aa9-107">`text`: *String*</span></span>

<span data-ttu-id="03aa9-108">ค่า *สตริง* ที่แสดงถึงข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="03aa9-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="03aa9-109">`number`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="03aa9-109">`number`: *Integer*</span></span>

<span data-ttu-id="03aa9-110">จำนวนอักขระที่ต้องถูกส่งกลับจากจุดสิ้นสุดของข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="03aa9-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="03aa9-111">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="03aa9-111">Return values</span></span>

<span data-ttu-id="03aa9-112">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="03aa9-112">*String*</span></span>

<span data-ttu-id="03aa9-113">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="03aa9-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="03aa9-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="03aa9-114">Example</span></span>

<span data-ttu-id="03aa9-115">`RIGHT ("Sample", 3)` ส่งกลับค่า **"ple"**</span><span class="sxs-lookup"><span data-stu-id="03aa9-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03aa9-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="03aa9-116">Additional resources</span></span>

[<span data-ttu-id="03aa9-117">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="03aa9-117">Text functions</span></span>](er-functions-category-text.md)
