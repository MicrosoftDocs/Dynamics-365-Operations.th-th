---
title: ฟังก์ชัน TABLENAME2ID ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TABLENAME2ID (ER)
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
ms.openlocfilehash: d9f9e38f46df8a93b5cb16b8d0d5e5afbff8558a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744010"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="98557-103">ฟังก์ชัน TABLENAME2ID ER</span><span class="sxs-lookup"><span data-stu-id="98557-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98557-104">ฟังก์ชัน `TABLENAME2ID` ส่งกลับการแสดงตัวเลขของรหัสตารางสำหรับชื่อตารางที่ระบุเป็นค่า *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="98557-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="98557-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="98557-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="98557-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="98557-106">Arguments</span></span>

<span data-ttu-id="98557-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="98557-107">`text`: *String*</span></span>

<span data-ttu-id="98557-108">ค่าข้อความที่แสดงชื่อตารางที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="98557-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="98557-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="98557-109">Return values</span></span>

<span data-ttu-id="98557-110">*จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="98557-110">*Integer*</span></span>

<span data-ttu-id="98557-111">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="98557-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="98557-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="98557-112">Usage notes</span></span>

<span data-ttu-id="98557-113">การดำเนินการของฟังก์ชันนี้สามารถมีผลลัพธ์ที่แตกต่างกันในอินสแตนซ์ต่างๆ ของ Microsoft Dynamics 365 Finance แม้ว่าจะมีการใช้ชื่อบริษัทเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="98557-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="98557-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="98557-114">Example</span></span>

<span data-ttu-id="98557-115">`TABLENAME2ID ("Intrastat")` ส่งกลับค่า **1510**</span><span class="sxs-lookup"><span data-stu-id="98557-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98557-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="98557-116">Additional resources</span></span>

[<span data-ttu-id="98557-117">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="98557-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
