---
title: ฟังก์ชัน CH_BANK_MOD_10
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CH_BANK_MOD_10 (ER)
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bca82cd596ba1e3ec42b3dba91ee6c4871ff8601
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686869"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="cfc7a-103">ฟังก์ชัน CH_BANK_MOD_10 ER</span><span class="sxs-lookup"><span data-stu-id="cfc7a-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cfc7a-104">ฟังก์ชัน `CH_BANK_MOD_10` ส่งกลับค่า *สตริง* ที่แสดงถึงการอ้างอิงของเจ้าหนี้เป็นนิพจน์ MOD10 ตามตัวเลขของหมายเลขใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="cfc7a-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfc7a-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="cfc7a-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="cfc7a-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="cfc7a-106">Arguments</span></span>

<span data-ttu-id="cfc7a-107">`invoice number digits`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="cfc7a-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="cfc7a-108">ค่าของข้อความที่แสดงตัวเลขของหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="cfc7a-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="cfc7a-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="cfc7a-109">Return values</span></span>

<span data-ttu-id="cfc7a-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="cfc7a-110">*String*</span></span>

<span data-ttu-id="cfc7a-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="cfc7a-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="cfc7a-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="cfc7a-112">Example</span></span>

<span data-ttu-id="cfc7a-113">`CH_BANK_MOD_10 ("VEND-200002")` ส่งคืน **3**</span><span class="sxs-lookup"><span data-stu-id="cfc7a-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cfc7a-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cfc7a-114">Additional resources</span></span>

[<span data-ttu-id="cfc7a-115">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="cfc7a-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
