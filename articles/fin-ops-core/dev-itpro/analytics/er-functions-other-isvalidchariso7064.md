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
ms.openlocfilehash: c858ad72db7afe63baca8288f312548c4fc37d5c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041411"
---
# <span data-ttu-id="0bc90-103"><a name="ISVALIDCHARACTERISO7064">ฟังก์ชัน ISVALIDCHARACTERISO7064 ER</a></span><span class="sxs-lookup"><span data-stu-id="0bc90-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bc90-104">ฟังก์ชัน `ISVALIDCHARACTERISO7064` ส่งกลับค่า *บูลีน* เป็น **จริง** หากสตริงที่ระบุแสดงหมายเลขบัญชีธนาคารระหว่างประเทศที่ถูกต้อง (IBAN)</span><span class="sxs-lookup"><span data-stu-id="0bc90-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="0bc90-105">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="0bc90-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc90-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="0bc90-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="0bc90-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="0bc90-107">Arguments</span></span>

<span data-ttu-id="0bc90-108">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="0bc90-108">`text`: *String*</span></span>

<span data-ttu-id="0bc90-109">ค่าข้อความที่แสดงถึง IBAN</span><span class="sxs-lookup"><span data-stu-id="0bc90-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="0bc90-110">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="0bc90-110">Return values</span></span>

<span data-ttu-id="0bc90-111">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="0bc90-111">*String*</span></span>

<span data-ttu-id="0bc90-112">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="0bc90-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0bc90-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0bc90-113">Example</span></span>

<span data-ttu-id="0bc90-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` ส่งกลับค่า **จริง**</span><span class="sxs-lookup"><span data-stu-id="0bc90-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="0bc90-115">`ISVALIDCHARACTERISO7064 ("AT61")` ส่งกลับค่า **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="0bc90-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0bc90-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0bc90-116">Additional resources</span></span>

[<span data-ttu-id="0bc90-117">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="0bc90-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
