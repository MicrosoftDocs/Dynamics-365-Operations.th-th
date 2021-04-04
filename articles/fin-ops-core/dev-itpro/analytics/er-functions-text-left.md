---
title: ฟังก์ชัน LEFT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ LEFT (ER)
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6f1ec7a21a16c3a34bed9779b05f20f21815ab9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570003"
---
# <a name="left-er-function"></a><span data-ttu-id="a4d52-103">ฟังก์ชัน LEFT ER</span><span class="sxs-lookup"><span data-stu-id="a4d52-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4d52-104">ฟังก์ชัน `LEFT` ส่งกลับค่า *สตริง* ที่แสดงจำนวนอักขระที่ระบุจากจุดเริ่มต้นของสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a4d52-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d52-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="a4d52-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="a4d52-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="a4d52-106">Arguments</span></span>

<span data-ttu-id="a4d52-107">`text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="a4d52-107">`text`: *String*</span></span>

<span data-ttu-id="a4d52-108">ค่า *สตริง* ที่แสดงถึงข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="a4d52-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="a4d52-109">`number`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="a4d52-109">`number`: *Integer*</span></span>

<span data-ttu-id="a4d52-110">จำนวนอักขระที่ต้องถูกส่งกลับจากจุดเริ่มต้นของข้อความต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="a4d52-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="a4d52-111">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="a4d52-111">Return values</span></span>

<span data-ttu-id="a4d52-112">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="a4d52-112">*String*</span></span>

<span data-ttu-id="a4d52-113">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="a4d52-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a4d52-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a4d52-114">Example</span></span>

<span data-ttu-id="a4d52-115">`LEFT ("Sample", 3)` ส่งกลับ **"Sam"**</span><span class="sxs-lookup"><span data-stu-id="a4d52-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4d52-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a4d52-116">Additional resources</span></span>

[<span data-ttu-id="a4d52-117">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="a4d52-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]