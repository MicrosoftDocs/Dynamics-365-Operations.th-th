---
title: ฟังก์ชัน NULLDATE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NULLDATE
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 327a06ab7657c334338073f67cb244cc40bfee31
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682328"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="66f69-103">ฟังก์ชัน NULLDATE ER</span><span class="sxs-lookup"><span data-stu-id="66f69-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66f69-104">ฟังก์ชัน `NULLDATE` ส่งคืนค่า *Date* ที่แสดงถึงวันที่ **ที่เป็นแบบ null** (1 มกราคม 1900)</span><span class="sxs-lookup"><span data-stu-id="66f69-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="66f69-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="66f69-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="66f69-106">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="66f69-106">Return values</span></span>

<span data-ttu-id="66f69-107">*วันที่*</span><span class="sxs-lookup"><span data-stu-id="66f69-107">*Date*</span></span>

<span data-ttu-id="66f69-108">ค่าวันที่ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="66f69-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="66f69-109">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="66f69-109">Example 1</span></span>

<span data-ttu-id="66f69-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` ส่งกลับวันที่ **ที่เป็น null** 1 มกราคม 1900 เป็น **"1900-01-01"** ตามรูปแบบที่กำหนดเองที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="66f69-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="66f69-111">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="66f69-111">Example 2</span></span>

<span data-ttu-id="66f69-112">นิพจน์ `IF( Invoice.DocumentDate = NULLDATE(), true, false)` ส่งคืน **True** เมื่อค่าของฟิลด์ **DocumentDate** เท่ากับวันที่ **ที่เป็น null**</span><span class="sxs-lookup"><span data-stu-id="66f69-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="66f69-113">ในตัวอย่างนี้ **Invoice** เป็นแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ของชนิด **เรกคอร์ด Finance/Table** และอ้างอิงถึงตาราง CustInvoiceJour</span><span class="sxs-lookup"><span data-stu-id="66f69-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="66f69-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="66f69-114">Additional resources</span></span>

[<span data-ttu-id="66f69-115">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="66f69-115">Date and time functions</span></span>](er-functions-category-datetime.md)
