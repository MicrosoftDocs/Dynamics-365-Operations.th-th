---
title: ฟังก์ชัน ER ISEMPTY
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ISEMPTY
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5b6fde7cbadec7aae052742ef598e1af4dbae793
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745140"
---
# <a name="isempty-er-function"></a><span data-ttu-id="58835-103">ฟังก์ชัน ER ISEMPTY</span><span class="sxs-lookup"><span data-stu-id="58835-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58835-104">ฟังก์ชัน `ISEMPTY` ส่งกลับค่า *Boolean* ของ **TRUE** ถ้ารายการที่ระบุไม่มีเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="58835-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="58835-105">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="58835-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="58835-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="58835-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="58835-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="58835-107">Arguments</span></span>

<span data-ttu-id="58835-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="58835-108">`list`: *Record list*</span></span>

<span data-ttu-id="58835-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="58835-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="58835-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="58835-110">Return values</span></span>

<span data-ttu-id="58835-111">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="58835-111">*Boolean*</span></span>

<span data-ttu-id="58835-112">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="58835-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="58835-113">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="58835-113">Example 1</span></span>

<span data-ttu-id="58835-114">ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่มีการคำนวณ* และประกอบด้วยนิพจน์ `SPLIT ("A|B|C", "|")` นิพจน์ `ISEMPTY(DS)` จะส่งกลับค่า **FALSE**</span><span class="sxs-lookup"><span data-stu-id="58835-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="58835-115">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="58835-115">Example 2</span></span>

<span data-ttu-id="58835-116">นิพจน์ `ISEMPTY (SPLIT ("",1))` ส่งกลับค่า **TRUE**</span><span class="sxs-lookup"><span data-stu-id="58835-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58835-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="58835-117">Additional resources</span></span>

[<span data-ttu-id="58835-118">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="58835-118">List functions</span></span>](er-functions-category-list.md)
