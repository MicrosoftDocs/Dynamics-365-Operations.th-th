---
title: ฟังก์ชัน VALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) VALUE
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
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917637"
---
# <span data-ttu-id="453fb-103"><a name="VALUE">ฟังก์ชัน VALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="453fb-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="453fb-104">ฟังก์ชัน `VALUE` ส่งกลับค่า *จริง* ที่ถูกแปลงจากสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="453fb-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="453fb-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="453fb-105">Syntax</span></span>

```
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="453fb-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="453fb-106">Arguments</span></span>

<span data-ttu-id="453fb-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="453fb-107">`text`: *String*</span></span>

<span data-ttu-id="453fb-108">ไม่สามารถแปลงค่าสตริงเป็นค่าตัวเลข</span><span class="sxs-lookup"><span data-stu-id="453fb-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="453fb-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="453fb-109">Return values</span></span>

<span data-ttu-id="453fb-110">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="453fb-110">*Real*</span></span>

<span data-ttu-id="453fb-111">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="453fb-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="453fb-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="453fb-112">Usage notes</span></span>

<span data-ttu-id="453fb-113">เครื่องหมายจุลภาคและอักขระจุด (.) ถือเป็นตัวแบ่งทศนิยม และยุติภังค์นำหน้า (-) จะถูกใช้เป็นเครื่องหมายลบ</span><span class="sxs-lookup"><span data-stu-id="453fb-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="453fb-114">มีข้อยกเว้นเกิดขึ้นในขณะรันไทม์ ถ้าสตริงที่ระบุประกอบด้วยอักขระที่ไม่ใช่ตัวเลขอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="453fb-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="453fb-115">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="453fb-115">Example 1</span></span>

<span data-ttu-id="453fb-116">`VALUE ("1 234,56")` เกิดข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="453fb-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="453fb-117">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="453fb-117">Example 2</span></span>

<span data-ttu-id="453fb-118">`VALUE ("1234,56")` ส่งกลับค่า **1234.56**</span><span class="sxs-lookup"><span data-stu-id="453fb-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="453fb-119">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="453fb-119">Additional resources</span></span>

[<span data-ttu-id="453fb-120">ฟังก์ชันการแปลงของชนิด</span><span class="sxs-lookup"><span data-stu-id="453fb-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
