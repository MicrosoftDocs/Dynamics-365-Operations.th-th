---
title: ฟังก์ชัน MOD_97 ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ MOD_97 (ER)
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
ms.openlocfilehash: b58e06a034fc6d26c891b78c26ac53c87a39b92b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744058"
---
# <a name="mod_97-er-function"></a><span data-ttu-id="d11eb-103">ฟังก์ชัน MOD_97 ER</span><span class="sxs-lookup"><span data-stu-id="d11eb-103">MOD_97 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d11eb-104">ฟังก์ชัน `MOD_97` ส่งกลับค่า *สตริง* ที่แสดงถึงการอ้างอิงของเจ้าหนี้เป็นนิพจน์ MOD97 ตามตัวเลขของหมายเลขใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="d11eb-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d11eb-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="d11eb-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="d11eb-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="d11eb-106">Arguments</span></span>

<span data-ttu-id="d11eb-107">`invoice number digits`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="d11eb-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="d11eb-108">ค่าของข้อความที่แสดงตัวเลขของหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="d11eb-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="d11eb-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="d11eb-109">Return values</span></span>

<span data-ttu-id="d11eb-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="d11eb-110">*String*</span></span>

<span data-ttu-id="d11eb-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="d11eb-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d11eb-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d11eb-112">Example</span></span>

<span data-ttu-id="d11eb-113">`MOD_97 ("VEND-200002")` ส่งคืน **"20000285"**</span><span class="sxs-lookup"><span data-stu-id="d11eb-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d11eb-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d11eb-114">Additional resources</span></span>

[<span data-ttu-id="d11eb-115">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="d11eb-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
