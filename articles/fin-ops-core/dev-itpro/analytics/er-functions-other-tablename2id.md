---
title: ฟังก์ชัน TABLENAME2ID ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TABLENAME2ID (ER)
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 0f94d00d9d40830d895e906ffbaa2a236f1efc43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746566"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="2ff36-103">ฟังก์ชัน TABLENAME2ID ER</span><span class="sxs-lookup"><span data-stu-id="2ff36-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ff36-104">ฟังก์ชัน `TABLENAME2ID` ส่งกลับการแสดงตัวเลขของรหัสตารางสำหรับชื่อตารางที่ระบุเป็นค่า *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="2ff36-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff36-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="2ff36-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="2ff36-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="2ff36-106">Arguments</span></span>

<span data-ttu-id="2ff36-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="2ff36-107">`text`: *String*</span></span>

<span data-ttu-id="2ff36-108">ค่าข้อความที่แสดงชื่อตารางที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2ff36-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="2ff36-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="2ff36-109">Return values</span></span>

<span data-ttu-id="2ff36-110">*จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="2ff36-110">*Integer*</span></span>

<span data-ttu-id="2ff36-111">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="2ff36-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2ff36-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2ff36-112">Usage notes</span></span>

<span data-ttu-id="2ff36-113">การดำเนินการของฟังก์ชันนี้สามารถมีผลลัพธ์ที่แตกต่างกันในอินสแตนซ์ต่างๆ ของ Microsoft Dynamics 365 Finance แม้ว่าจะมีการใช้ชื่อบริษัทเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="2ff36-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="2ff36-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="2ff36-114">Example</span></span>

<span data-ttu-id="2ff36-115">`TABLENAME2ID ("Intrastat")` ส่งกลับค่า **1510**</span><span class="sxs-lookup"><span data-stu-id="2ff36-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ff36-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2ff36-116">Additional resources</span></span>

[<span data-ttu-id="2ff36-117">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="2ff36-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]