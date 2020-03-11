---
title: ฟังก์ชัน ISOCREDREF ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ ISOCREDREF (ER)
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
ms.openlocfilehash: dd692720872314d533274f392f84e5ac7d36c7c1
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041388"
---
# <span data-ttu-id="31e30-103"><a name="ISOCREDREF">ฟังก์ชัน ISOCREDREF ER</a></span><span class="sxs-lookup"><span data-stu-id="31e30-103"><a name="ISOCREDREF">ISOCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31e30-104">ฟังก์ชัน `ISOCREDREF` ส่งคืนค่า *สตริง* ที่แสดงการอ้างอิงเจ้าหนี้ขององค์การระหว่างประเทศว่าด้วยการมาตรฐาน (ISO) โดยขึ้นอยู่กับตำแหน่งและสัญลักษณ์เรียงตามลำดับอักษรของหมายเลขใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="31e30-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="31e30-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="31e30-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="31e30-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="31e30-106">Arguments</span></span>

<span data-ttu-id="31e30-107">`invoice number digits`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="31e30-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="31e30-108">ค่าของข้อความที่แสดงตัวเลขของหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="31e30-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="31e30-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="31e30-109">Return values</span></span>

<span data-ttu-id="31e30-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="31e30-110">*String*</span></span>

<span data-ttu-id="31e30-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="31e30-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="31e30-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="31e30-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="31e30-113">เพื่อขจัดสัญลักษณ์จากอักษรที่ไม่สอดคล้องกับ ISO อาร์กิวเมนต์ `invoice number digits` จะต้องถูกแปลก่อนที่จะมีการส่งผ่านไปยังฟังก์ชันนี้</span><span class="sxs-lookup"><span data-stu-id="31e30-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="31e30-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="31e30-114">Example</span></span>

<span data-ttu-id="31e30-115">`ISOCredRef ("VEND-200002")` ส่งคืน **"RF23VEND-200002"**</span><span class="sxs-lookup"><span data-stu-id="31e30-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31e30-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="31e30-116">Additional resources</span></span>

[<span data-ttu-id="31e30-117">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="31e30-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
