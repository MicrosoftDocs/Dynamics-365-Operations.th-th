---
title: ฟังก์ชัน TRIM ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TRIM (ER)
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
ms.openlocfilehash: 2673b0167f7602a6d6eaa79be639905028e99822
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915544"
---
# <span data-ttu-id="112f4-103"><a name="TRIM">ฟังก์ชัน TRIM ER</a></span><span class="sxs-lookup"><span data-stu-id="112f4-103"><a name="TRIM">TRIM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="112f4-104">ฟังก์ชัน `TRIM` ส่งคืนสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากช่องว่างนำหน้าและต่อท้ายถูกตัดออกแล้ว และหลังจากที่ได้ลบช่องว่างหลายช่องระหว่างคำ</span><span class="sxs-lookup"><span data-stu-id="112f4-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="112f4-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="112f4-105">Syntax</span></span>

```
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="112f4-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="112f4-106">Arguments</span></span>

<span data-ttu-id="112f4-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="112f4-107">`text`: *String*</span></span>

<span data-ttu-id="112f4-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="112f4-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="112f4-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="112f4-109">Return values</span></span>

<span data-ttu-id="112f4-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="112f4-110">*String*</span></span>

<span data-ttu-id="112f4-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="112f4-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="112f4-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="112f4-112">Example</span></span>

<span data-ttu-id="112f4-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` ส่งกลับ **"ข้อความตัวอย่าง"**</span><span class="sxs-lookup"><span data-stu-id="112f4-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="112f4-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="112f4-114">Additional resources</span></span>

[<span data-ttu-id="112f4-115">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="112f4-115">Text functions</span></span>](er-functions-category-text.md)
