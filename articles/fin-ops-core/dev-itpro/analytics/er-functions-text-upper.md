---
title: ฟังก์ชัน UPPER ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ UPPER (ER)
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 672abf4938df7d96c0190bfd5325689b381e2764
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744346"
---
# <a name="upper-er-function"></a><span data-ttu-id="cf399-103">ฟังก์ชัน UPPER ER</span><span class="sxs-lookup"><span data-stu-id="cf399-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf399-104">ฟังก์ชัน `UPPER` ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากที่ถูกแปลงเป็นตัวพิมพ์ใหญ่</span><span class="sxs-lookup"><span data-stu-id="cf399-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf399-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="cf399-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="cf399-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="cf399-106">Arguments</span></span>

<span data-ttu-id="cf399-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="cf399-107">`text`: *String*</span></span>

<span data-ttu-id="cf399-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="cf399-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="cf399-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="cf399-109">Return values</span></span>

<span data-ttu-id="cf399-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="cf399-110">*String*</span></span>

<span data-ttu-id="cf399-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="cf399-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="cf399-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="cf399-112">Example</span></span>

<span data-ttu-id="cf399-113">`UPPER ("Sample")` ส่งกลับ **"ตัวอย่าง"**</span><span class="sxs-lookup"><span data-stu-id="cf399-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf399-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cf399-114">Additional resources</span></span>

[<span data-ttu-id="cf399-115">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="cf399-115">Text functions</span></span>](er-functions-category-text.md)
