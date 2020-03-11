---
title: ฟังก์ชัน LOWER ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ LOWER (ER)
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6784384bac31d8c7cdc9c6f71b7dbab79c15a934
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041112"
---
# <span data-ttu-id="79a9d-103"><a name="LOWER">ฟังก์ชัน LOWER ER</a></span><span class="sxs-lookup"><span data-stu-id="79a9d-103"><a name="LOWER">LOWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79a9d-104">ฟังก์ชัน `LOWER` ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากที่ถูกแปลงเป็นตัวพิมพ์เล็ก</span><span class="sxs-lookup"><span data-stu-id="79a9d-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="79a9d-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="79a9d-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="79a9d-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="79a9d-106">Arguments</span></span>

<span data-ttu-id="79a9d-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="79a9d-107">`text`: *String*</span></span>

<span data-ttu-id="79a9d-108">ค่า *สตริง* ที่ระบุข้อความ</span><span class="sxs-lookup"><span data-stu-id="79a9d-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="79a9d-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="79a9d-109">Return values</span></span>

<span data-ttu-id="79a9d-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="79a9d-110">*String*</span></span>

<span data-ttu-id="79a9d-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="79a9d-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="79a9d-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="79a9d-112">Example</span></span>

<span data-ttu-id="79a9d-113">`LOWER ("Sample")` ส่งกลับ **"ตัวอย่าง"**</span><span class="sxs-lookup"><span data-stu-id="79a9d-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79a9d-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="79a9d-114">Additional resources</span></span>

[<span data-ttu-id="79a9d-115">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="79a9d-115">Text functions</span></span>](er-functions-category-text.md)
