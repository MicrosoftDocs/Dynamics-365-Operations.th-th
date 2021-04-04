---
title: ฟังก์ชัน CURCREDREF ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CURCREDREF (ER)
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
ms.openlocfilehash: d5f126d71abdc9e3e488b4e8476850dc7763fe5a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567627"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="75d8e-103">ฟังก์ชัน CURCREDREF ER</span><span class="sxs-lookup"><span data-stu-id="75d8e-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75d8e-104">ฟังก์ชัน `CURCREDREF` ส่งกลับค่า *สตริง* ที่แสดงถึงการอ้างอิงของเจ้าหนี้ตามตัวเลขของหมายเลขใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="75d8e-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d8e-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="75d8e-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="75d8e-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="75d8e-106">Arguments</span></span>

<span data-ttu-id="75d8e-107">`invoice number digits`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="75d8e-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="75d8e-108">ค่าของข้อความที่แสดงตัวเลขของหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="75d8e-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="75d8e-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="75d8e-109">Return values</span></span>

<span data-ttu-id="75d8e-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="75d8e-110">*String*</span></span>

<span data-ttu-id="75d8e-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="75d8e-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="75d8e-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="75d8e-112">Example</span></span>

<span data-ttu-id="75d8e-113">`CURCredRef ("VEND-200002")` ส่งคืน **"2200002"**</span><span class="sxs-lookup"><span data-stu-id="75d8e-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75d8e-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="75d8e-114">Additional resources</span></span>

[<span data-ttu-id="75d8e-115">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="75d8e-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]