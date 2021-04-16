---
title: ฟังก์ชัน MOD_97 ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ MOD_97 (ER)
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
ms.openlocfilehash: 1054407addaf6f7c2a7d2f72bf1479e9dc374389
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749176"
---
# <a name="mod_97-er-function"></a><span data-ttu-id="8ef9b-103">ฟังก์ชัน MOD_97 ER</span><span class="sxs-lookup"><span data-stu-id="8ef9b-103">MOD_97 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ef9b-104">ฟังก์ชัน `MOD_97` ส่งกลับค่า *สตริง* ที่แสดงถึงการอ้างอิงของเจ้าหนี้เป็นนิพจน์ MOD97 ตามตัวเลขของหมายเลขใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="8ef9b-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef9b-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="8ef9b-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="8ef9b-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="8ef9b-106">Arguments</span></span>

<span data-ttu-id="8ef9b-107">`invoice number digits`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="8ef9b-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="8ef9b-108">ค่าของข้อความที่แสดงตัวเลขของหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="8ef9b-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="8ef9b-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="8ef9b-109">Return values</span></span>

<span data-ttu-id="8ef9b-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="8ef9b-110">*String*</span></span>

<span data-ttu-id="8ef9b-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="8ef9b-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8ef9b-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8ef9b-112">Example</span></span>

<span data-ttu-id="8ef9b-113">`MOD_97 ("VEND-200002")` ส่งคืน **"20000285"**</span><span class="sxs-lookup"><span data-stu-id="8ef9b-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ef9b-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8ef9b-114">Additional resources</span></span>

[<span data-ttu-id="8ef9b-115">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="8ef9b-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]