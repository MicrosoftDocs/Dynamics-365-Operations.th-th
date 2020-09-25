---
title: ฟังก์ชัน ISVALIDCHARACTERISO7064 ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ ISVALIDCHARACTERISO7064 (ER)
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
ms.openlocfilehash: 21962952bb3bdd016831dc5e196af27c69ecc6db
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744082"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="5866b-103">ฟังก์ชัน ISVALIDCHARACTERISO7064 ER</span><span class="sxs-lookup"><span data-stu-id="5866b-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5866b-104">ฟังก์ชัน `ISVALIDCHARACTERISO7064` ส่งกลับค่า *บูลีน* เป็น **จริง** หากสตริงที่ระบุแสดงหมายเลขบัญชีธนาคารระหว่างประเทศที่ถูกต้อง (IBAN)</span><span class="sxs-lookup"><span data-stu-id="5866b-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="5866b-105">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="5866b-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5866b-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="5866b-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="5866b-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="5866b-107">Arguments</span></span>

<span data-ttu-id="5866b-108">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="5866b-108">`text`: *String*</span></span>

<span data-ttu-id="5866b-109">ค่าข้อความที่แสดงถึง IBAN</span><span class="sxs-lookup"><span data-stu-id="5866b-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="5866b-110">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="5866b-110">Return values</span></span>

<span data-ttu-id="5866b-111">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="5866b-111">*String*</span></span>

<span data-ttu-id="5866b-112">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="5866b-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5866b-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="5866b-113">Example</span></span>

<span data-ttu-id="5866b-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` ส่งกลับค่า **จริง**</span><span class="sxs-lookup"><span data-stu-id="5866b-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="5866b-115">`ISVALIDCHARACTERISO7064 ("AT61")` ส่งกลับค่า **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="5866b-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5866b-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5866b-116">Additional resources</span></span>

[<span data-ttu-id="5866b-117">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="5866b-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
