---
title: ฟังก์ชัน CH_BANK_MOD_10
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CH_BANK_MOD_10 (ER)
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
ms.openlocfilehash: 21942fa47b968fa10bfc9b07f269d44e495139fe
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564851"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="c1352-103">ฟังก์ชัน CH_BANK_MOD_10 ER</span><span class="sxs-lookup"><span data-stu-id="c1352-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1352-104">ฟังก์ชัน `CH_BANK_MOD_10` ส่งกลับค่า *สตริง* ที่แสดงถึงการอ้างอิงของเจ้าหนี้เป็นนิพจน์ MOD10 ตามตัวเลขของหมายเลขใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="c1352-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1352-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="c1352-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="c1352-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="c1352-106">Arguments</span></span>

<span data-ttu-id="c1352-107">`invoice number digits`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="c1352-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="c1352-108">ค่าของข้อความที่แสดงตัวเลขของหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c1352-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="c1352-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="c1352-109">Return values</span></span>

<span data-ttu-id="c1352-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="c1352-110">*String*</span></span>

<span data-ttu-id="c1352-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="c1352-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c1352-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="c1352-112">Example</span></span>

<span data-ttu-id="c1352-113">`CH_BANK_MOD_10 ("VEND-200002")` ส่งคืน **3**</span><span class="sxs-lookup"><span data-stu-id="c1352-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1352-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c1352-114">Additional resources</span></span>

[<span data-ttu-id="c1352-115">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="c1352-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]