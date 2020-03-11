---
title: ฟังก์ชัน LEN ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ LEN (ER)
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
ms.openlocfilehash: 3e0ba19e762574dde4f9038b87ce352d13f714f4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041066"
---
# <span data-ttu-id="72f50-103"><a name="LEN">ฟังก์ชัน LEN ER</a></span><span class="sxs-lookup"><span data-stu-id="72f50-103"><a name="LEN">LEN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72f50-104">ฟังก์ชัน `LEN` ส่งกลับจำนวนอักขระในสตริงที่ระบุเป็นค่า *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="72f50-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f50-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="72f50-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="72f50-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="72f50-106">Arguments</span></span>

<span data-ttu-id="72f50-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="72f50-107">`text`: *String*</span></span>

<span data-ttu-id="72f50-108">ค่า *สตริง* ที่ระบุข้อความ</span><span class="sxs-lookup"><span data-stu-id="72f50-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="72f50-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="72f50-109">Return values</span></span>

<span data-ttu-id="72f50-110">*จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="72f50-110">*Integer*</span></span>

<span data-ttu-id="72f50-111">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="72f50-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="72f50-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="72f50-112">Example</span></span>

<span data-ttu-id="72f50-113">`LEN ("Sample")` ส่งกลับค่า **6**</span><span class="sxs-lookup"><span data-stu-id="72f50-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72f50-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="72f50-114">Additional resources</span></span>

[<span data-ttu-id="72f50-115">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="72f50-115">Text functions</span></span>](er-functions-category-text.md)
