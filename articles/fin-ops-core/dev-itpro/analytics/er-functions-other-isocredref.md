---
title: ฟังก์ชัน ISOCREDREF ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ ISOCREDREF (ER)
author: NickSelin
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
ms.openlocfilehash: 51adc6392b07ba4061a475f3072fb35452f15ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748328"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="3bdfb-103">ฟังก์ชัน ISOCREDREF ER</span><span class="sxs-lookup"><span data-stu-id="3bdfb-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3bdfb-104">ฟังก์ชัน `ISOCREDREF` ส่งคืนค่า *สตริง* ที่แสดงการอ้างอิงเจ้าหนี้ขององค์การระหว่างประเทศว่าด้วยการมาตรฐาน (ISO) โดยขึ้นอยู่กับตำแหน่งและสัญลักษณ์เรียงตามลำดับอักษรของหมายเลขใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3bdfb-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bdfb-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="3bdfb-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="3bdfb-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="3bdfb-106">Arguments</span></span>

<span data-ttu-id="3bdfb-107">`invoice number digits`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="3bdfb-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="3bdfb-108">ค่าของข้อความที่แสดงตัวเลขของหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="3bdfb-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="3bdfb-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="3bdfb-109">Return values</span></span>

<span data-ttu-id="3bdfb-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="3bdfb-110">*String*</span></span>

<span data-ttu-id="3bdfb-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="3bdfb-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3bdfb-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3bdfb-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="3bdfb-113">เพื่อขจัดสัญลักษณ์จากอักษรที่ไม่สอดคล้องกับ ISO อาร์กิวเมนต์ `invoice number digits` จะต้องถูกแปลก่อนที่จะมีการส่งผ่านไปยังฟังก์ชันนี้</span><span class="sxs-lookup"><span data-stu-id="3bdfb-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="3bdfb-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3bdfb-114">Example</span></span>

<span data-ttu-id="3bdfb-115">`ISOCredRef ("VEND-200002")` ส่งคืน **"RF23VEND-200002"**</span><span class="sxs-lookup"><span data-stu-id="3bdfb-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3bdfb-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3bdfb-116">Additional resources</span></span>

[<span data-ttu-id="3bdfb-117">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="3bdfb-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]