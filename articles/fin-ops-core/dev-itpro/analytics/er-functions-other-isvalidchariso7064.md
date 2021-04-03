---
title: ฟังก์ชัน ISVALIDCHARACTERISO7064 ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ ISVALIDCHARACTERISO7064 (ER)
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 26300adce5f9a8a567510885577c6cfb9b1c859a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563377"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="7419a-103">ฟังก์ชัน ISVALIDCHARACTERISO7064 ER</span><span class="sxs-lookup"><span data-stu-id="7419a-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7419a-104">ฟังก์ชัน `ISVALIDCHARACTERISO7064` ส่งกลับค่า *บูลีน* เป็น **จริง** หากสตริงที่ระบุแสดงหมายเลขบัญชีธนาคารระหว่างประเทศที่ถูกต้อง (IBAN)</span><span class="sxs-lookup"><span data-stu-id="7419a-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="7419a-105">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="7419a-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7419a-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="7419a-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="7419a-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="7419a-107">Arguments</span></span>

<span data-ttu-id="7419a-108">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="7419a-108">`text`: *String*</span></span>

<span data-ttu-id="7419a-109">ค่าข้อความที่แสดงถึง IBAN</span><span class="sxs-lookup"><span data-stu-id="7419a-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="7419a-110">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="7419a-110">Return values</span></span>

<span data-ttu-id="7419a-111">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="7419a-111">*String*</span></span>

<span data-ttu-id="7419a-112">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="7419a-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7419a-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="7419a-113">Example</span></span>

<span data-ttu-id="7419a-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` ส่งกลับค่า **จริง**</span><span class="sxs-lookup"><span data-stu-id="7419a-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="7419a-115">`ISVALIDCHARACTERISO7064 ("AT61")` ส่งกลับค่า **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="7419a-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7419a-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7419a-116">Additional resources</span></span>

[<span data-ttu-id="7419a-117">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="7419a-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]