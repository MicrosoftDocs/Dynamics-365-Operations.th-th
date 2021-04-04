---
title: ฟังก์ชัน NULLDATE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NULLDATE
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 79d37247653aa297fdee2c770180916b9a9a5fc5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563473"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="3062c-103">ฟังก์ชัน NULLDATE ER</span><span class="sxs-lookup"><span data-stu-id="3062c-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3062c-104">ฟังก์ชัน `NULLDATE` ส่งคืนค่า *Date* ที่แสดงถึงวันที่ **ที่เป็นแบบ null** (1 มกราคม 1900)</span><span class="sxs-lookup"><span data-stu-id="3062c-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="3062c-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="3062c-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="3062c-106">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="3062c-106">Return values</span></span>

<span data-ttu-id="3062c-107">*วันที่*</span><span class="sxs-lookup"><span data-stu-id="3062c-107">*Date*</span></span>

<span data-ttu-id="3062c-108">ค่าวันที่ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="3062c-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="3062c-109">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="3062c-109">Example 1</span></span>

<span data-ttu-id="3062c-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` ส่งกลับวันที่ **ที่เป็น null** 1 มกราคม 1900 เป็น **"1900-01-01"** ตามรูปแบบที่กำหนดเองที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3062c-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="3062c-111">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="3062c-111">Example 2</span></span>

<span data-ttu-id="3062c-112">นิพจน์ `IF( Invoice.DocumentDate = NULLDATE(), true, false)` ส่งคืน **True** เมื่อค่าของฟิลด์ **DocumentDate** เท่ากับวันที่ **ที่เป็น null**</span><span class="sxs-lookup"><span data-stu-id="3062c-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="3062c-113">ในตัวอย่างนี้ **Invoice** เป็นแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ของชนิด **เรกคอร์ด Finance/Table** และอ้างอิงถึงตาราง CustInvoiceJour</span><span class="sxs-lookup"><span data-stu-id="3062c-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3062c-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3062c-114">Additional resources</span></span>

[<span data-ttu-id="3062c-115">ฟังก์ชันวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="3062c-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]