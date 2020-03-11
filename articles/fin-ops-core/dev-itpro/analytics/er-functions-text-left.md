---
title: ฟังก์ชัน LEFT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ LEFT (ER)
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 4293db244d04debf3679cf2bde0b892bd74e8ead
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041135"
---
# <span data-ttu-id="5c433-103"><a name="LEFT">ฟังก์ชัน LEFT ER</a></span><span class="sxs-lookup"><span data-stu-id="5c433-103"><a name="LEFT">LEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c433-104">ฟังก์ชัน `LEFT` ส่งกลับค่า *สตริง* ที่แสดงจำนวนอักขระที่ระบุจากจุดเริ่มต้นของสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="5c433-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c433-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="5c433-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="5c433-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="5c433-106">Arguments</span></span>

<span data-ttu-id="5c433-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="5c433-107">`text`: *String*</span></span>

<span data-ttu-id="5c433-108">ค่า *สตริง* ที่แสดงถึงข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="5c433-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="5c433-109">`number`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="5c433-109">`number`: *Integer*</span></span>

<span data-ttu-id="5c433-110">จำนวนอักขระที่ต้องถูกส่งกลับจากจุดเริ่มต้นของข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="5c433-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="5c433-111">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="5c433-111">Return values</span></span>

<span data-ttu-id="5c433-112">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="5c433-112">*String*</span></span>

<span data-ttu-id="5c433-113">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="5c433-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5c433-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="5c433-114">Example</span></span>

<span data-ttu-id="5c433-115">`LEFT ("Sample", 3)` ส่งกลับ **"Sam"**</span><span class="sxs-lookup"><span data-stu-id="5c433-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c433-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5c433-116">Additional resources</span></span>

[<span data-ttu-id="5c433-117">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="5c433-117">Text functions</span></span>](er-functions-category-text.md)
