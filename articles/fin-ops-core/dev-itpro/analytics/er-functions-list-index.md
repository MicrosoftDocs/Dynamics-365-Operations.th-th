---
title: ฟังก์ชัน INDEX ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) INDEX
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
ms.openlocfilehash: 051e22daa3fe2d6c328e36403201d940f724bd29
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745194"
---
# <a name="index-er-function"></a><span data-ttu-id="603a8-103">ฟังก์ชัน INDEX ER</span><span class="sxs-lookup"><span data-stu-id="603a8-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="603a8-104">ฟังก์ชัน `INDEX` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่เลือกโดยใช้ดัชนีตัวเลขที่ระบุในรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="603a8-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="603a8-105">ถ้าดัชนีอยู่นอกช่วสำหรับเรกคอร์ดในรายการที่ระบุ จะมีข้อยกเว้นเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="603a8-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="603a8-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="603a8-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="603a8-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="603a8-107">Arguments</span></span>

<span data-ttu-id="603a8-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="603a8-108">`list`: *Record list*</span></span>

<span data-ttu-id="603a8-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="603a8-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="603a8-110">`index`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="603a8-110">`index`: *Integer*</span></span>

<span data-ttu-id="603a8-111">ดัชนีตัวเลขที่ระบุตำแหน่งของเรกคอร์ดที่ต้องการในรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="603a8-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="603a8-112">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="603a8-112">Return values</span></span>

<span data-ttu-id="603a8-113">*คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="603a8-113">*Container (record)*</span></span>

<span data-ttu-id="603a8-114">ค่าเรกคอร์ดที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="603a8-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="603a8-115">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="603a8-115">Example 1</span></span>

<span data-ttu-id="603a8-116">ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิดของ *ฟิลด์ที่มีการคำนวณ* และมีนิพจน์ `SPLIT ("A|B|C", "|")` นิพจน์ `DS.Value` นิพจน์จะส่งคืนค่าข้อความ **B** สำหรับเรกคอร์ดที่สองของรายการเรกคอร์ดนี้</span><span class="sxs-lookup"><span data-stu-id="603a8-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="603a8-117">นิพจน์ `INDEX (SPLIT ("A|B|C", "|"), 2).Value` ยังส่งกลับค่าข้อความ **B** ด้วย</span><span class="sxs-lookup"><span data-stu-id="603a8-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="603a8-118">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="603a8-118">Example 2</span></span>

<span data-ttu-id="603a8-119">ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่มีการคำนวณ* และประกอบด้วยนิพจน์ `SPLIT ("A|B|C", "|")` นิพจน์ `INDEX (SPLIT ("A|B|C", "|"), 4).Value` จะมีข้อยกเว้นเกิดขึ้นขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="603a8-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="603a8-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="603a8-120">Additional resources</span></span>

[<span data-ttu-id="603a8-121">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="603a8-121">List functions</span></span>](er-functions-category-list.md)
