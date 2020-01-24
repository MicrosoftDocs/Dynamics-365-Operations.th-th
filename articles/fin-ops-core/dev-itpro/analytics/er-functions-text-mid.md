---
title: ฟังก์ชัน MID ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ MID (ER)
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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915613"
---
# <span data-ttu-id="1b052-103"><a name="MID">ฟังก์ชัน MID ER</a></span><span class="sxs-lookup"><span data-stu-id="1b052-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b052-104">ฟังก์ชัน `MID` ส่งกลับค่า *สตริง* ที่แสดงจำนวนอักขระที่ระบุจากสตริงที่ระบุซึ่งเริ่มต้นที่ตำแหน่งที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1b052-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b052-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="1b052-105">Syntax</span></span>

```
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="1b052-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="1b052-106">Arguments</span></span>

<span data-ttu-id="1b052-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1b052-107">`text`: *String*</span></span>

<span data-ttu-id="1b052-108">ค่า *สตริง* ที่ระบุข้อความที่จะส่งกลับอักขระ</span><span class="sxs-lookup"><span data-stu-id="1b052-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="1b052-109">`starting position`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="1b052-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="1b052-110">ค่า *เลขจำนวนเต็ม* ที่ระบุตำแหน่งของอักขระตัวแรกที่ต้องถูกส่งกลับจากข้อความที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1b052-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="1b052-111">`number of characters`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="1b052-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="1b052-112">ค่า *เลขจำนวนเต็ม* ที่ระบุจำนวนของอักขระที่ต้องถูกส่งกลับ ซึ่งเริ่มต้นที่ตำแหน่งเริ่มต้นที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1b052-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="1b052-113">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="1b052-113">Return values</span></span>

<span data-ttu-id="1b052-114">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="1b052-114">*String*</span></span>

<span data-ttu-id="1b052-115">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="1b052-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1b052-116">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1b052-116">Usage notes</span></span>

<span data-ttu-id="1b052-117">ถ้าค่าของอาร์กิวเมนต์ `starting position` น้อยกว่า 0 (ศูนย์) อักขระที่ถูกส่งกลับจะถูกนับจากตำแหน่งแรกในสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1b052-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="1b052-118">ถ้าค่าของอาร์กิวเมนต์ `starting position` เกินความยาวของสตริงที่ระบุ สตริงที่ว่างจะถูกส่งกลับ</span><span class="sxs-lookup"><span data-stu-id="1b052-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="1b052-119">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="1b052-119">Example</span></span>

<span data-ttu-id="1b052-120">`MID ("Sample", 2, 3)`ส่งกลับค่า **"amp"**</span><span class="sxs-lookup"><span data-stu-id="1b052-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b052-121">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1b052-121">Additional resources</span></span>

[<span data-ttu-id="1b052-122">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="1b052-122">Text functions</span></span>](er-functions-category-text.md)
