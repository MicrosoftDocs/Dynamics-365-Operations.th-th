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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3e594138ef8e28f1b3aaf333026fa8f9e55cca0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688352"
---
# <a name="upper-er-function"></a><span data-ttu-id="65b7a-103">ฟังก์ชัน UPPER ER</span><span class="sxs-lookup"><span data-stu-id="65b7a-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65b7a-104">ฟังก์ชัน `UPPER` ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากที่ถูกแปลงเป็นตัวพิมพ์ใหญ่</span><span class="sxs-lookup"><span data-stu-id="65b7a-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b7a-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="65b7a-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="65b7a-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="65b7a-106">Arguments</span></span>

<span data-ttu-id="65b7a-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="65b7a-107">`text`: *String*</span></span>

<span data-ttu-id="65b7a-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="65b7a-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="65b7a-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="65b7a-109">Return values</span></span>

<span data-ttu-id="65b7a-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="65b7a-110">*String*</span></span>

<span data-ttu-id="65b7a-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="65b7a-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="65b7a-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="65b7a-112">Example</span></span>

<span data-ttu-id="65b7a-113">`UPPER ("Sample")` ส่งกลับ **"ตัวอย่าง"**</span><span class="sxs-lookup"><span data-stu-id="65b7a-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65b7a-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="65b7a-114">Additional resources</span></span>

[<span data-ttu-id="65b7a-115">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="65b7a-115">Text functions</span></span>](er-functions-category-text.md)
