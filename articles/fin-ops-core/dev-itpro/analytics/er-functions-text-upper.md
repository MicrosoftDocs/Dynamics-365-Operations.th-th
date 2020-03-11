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
ms.openlocfilehash: 77854d645ba5b65a2819437af510fcd67be6d99d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040951"
---
# <span data-ttu-id="ae6ca-103"><a name="UPPER">ฟังก์ชัน UPPER ER</a></span><span class="sxs-lookup"><span data-stu-id="ae6ca-103"><a name="UPPER">UPPER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae6ca-104">ฟังก์ชัน `UPPER` ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากที่ถูกแปลงเป็นตัวพิมพ์ใหญ่</span><span class="sxs-lookup"><span data-stu-id="ae6ca-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae6ca-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="ae6ca-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="ae6ca-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="ae6ca-106">Arguments</span></span>

<span data-ttu-id="ae6ca-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="ae6ca-107">`text`: *String*</span></span>

<span data-ttu-id="ae6ca-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="ae6ca-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ae6ca-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="ae6ca-109">Return values</span></span>

<span data-ttu-id="ae6ca-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="ae6ca-110">*String*</span></span>

<span data-ttu-id="ae6ca-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="ae6ca-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="ae6ca-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ae6ca-112">Example</span></span>

<span data-ttu-id="ae6ca-113">`UPPER ("Sample")` ส่งกลับ **"ตัวอย่าง"**</span><span class="sxs-lookup"><span data-stu-id="ae6ca-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae6ca-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ae6ca-114">Additional resources</span></span>

[<span data-ttu-id="ae6ca-115">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="ae6ca-115">Text functions</span></span>](er-functions-category-text.md)
