---
title: ฟังก์ชัน ISOCREDREF ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ ISOCREDREF (ER)
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
ms.openlocfilehash: a9378028a4b308aae7796b861b37a5f89ddfe49c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563424"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="7fc28-103">ฟังก์ชัน ISOCREDREF ER</span><span class="sxs-lookup"><span data-stu-id="7fc28-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fc28-104">ฟังก์ชัน `ISOCREDREF` ส่งคืนค่า *สตริง* ที่แสดงการอ้างอิงเจ้าหนี้ขององค์การระหว่างประเทศว่าด้วยการมาตรฐาน (ISO) โดยขึ้นอยู่กับตำแหน่งและสัญลักษณ์เรียงตามลำดับอักษรของหมายเลขใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="7fc28-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fc28-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="7fc28-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="7fc28-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="7fc28-106">Arguments</span></span>

<span data-ttu-id="7fc28-107">`invoice number digits`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="7fc28-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="7fc28-108">ค่าของข้อความที่แสดงตัวเลขของหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="7fc28-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="7fc28-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="7fc28-109">Return values</span></span>

<span data-ttu-id="7fc28-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="7fc28-110">*String*</span></span>

<span data-ttu-id="7fc28-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="7fc28-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7fc28-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7fc28-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="7fc28-113">เพื่อขจัดสัญลักษณ์จากอักษรที่ไม่สอดคล้องกับ ISO อาร์กิวเมนต์ `invoice number digits` จะต้องถูกแปลก่อนที่จะมีการส่งผ่านไปยังฟังก์ชันนี้</span><span class="sxs-lookup"><span data-stu-id="7fc28-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="7fc28-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="7fc28-114">Example</span></span>

<span data-ttu-id="7fc28-115">`ISOCredRef ("VEND-200002")` ส่งคืน **"RF23VEND-200002"**</span><span class="sxs-lookup"><span data-stu-id="7fc28-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fc28-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7fc28-116">Additional resources</span></span>

[<span data-ttu-id="7fc28-117">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="7fc28-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]