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
ms.openlocfilehash: a7fe2cbb5421da3c6dd1d044316b276836c5e5c1
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917315"
---
# <span data-ttu-id="31734-103"><a name="INDEX">ฟังก์ชัน INDEX ER</a></span><span class="sxs-lookup"><span data-stu-id="31734-103"><a name="INDEX">INDEX ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31734-104">ฟังก์ชัน `INDEX` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่เลือกโดยใช้ดัชนีตัวเลขที่ระบุในรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="31734-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="31734-105">ถ้าดัชนีอยู่นอกช่วสำหรับเรกคอร์ดในรายการที่ระบุ จะมีข้อยกเว้นเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="31734-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="31734-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="31734-106">Syntax</span></span>

```
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="31734-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="31734-107">Arguments</span></span>

<span data-ttu-id="31734-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="31734-108">`list`: *Record list*</span></span>

<span data-ttu-id="31734-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="31734-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="31734-110">`index`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="31734-110">`index`: *Integer*</span></span>

<span data-ttu-id="31734-111">ดัชนีตัวเลขที่ระบุตำแหน่งของเรกคอร์ดที่ต้องการในรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="31734-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="31734-112">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="31734-112">Return values</span></span>

<span data-ttu-id="31734-113">*คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="31734-113">*Container (record)*</span></span>

<span data-ttu-id="31734-114">ค่าเรกคอร์ดที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="31734-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="31734-115">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="31734-115">Example 1</span></span>

<span data-ttu-id="31734-116">ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิดของ *ฟิลด์ที่คำนวณได้* และมีนิพจน์ `SPLIT ("A|B|C", "|")` นิพจน์ `DS.Value` นิพจน์จะส่งคืนค่าข้อความ **B** สำหรับเรกคอร์ดที่สองของรายการเรกคอร์ดนี้</span><span class="sxs-lookup"><span data-stu-id="31734-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="31734-117">นิพจน์ `INDEX (SPLIT ("A|B|C", "|"), 2).Value` ยังส่งกลับค่าข้อความ **B** ด้วย</span><span class="sxs-lookup"><span data-stu-id="31734-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="31734-118">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="31734-118">Example 2</span></span>

<span data-ttu-id="31734-119">ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่คำนวณได้* และประกอบด้วยนิพจน์ `SPLIT ("A|B|C", "|")` นิพจน์ `INDEX (SPLIT ("A|B|C", "|"), 4).Value` จะมีข้อยกเว้นเกิดขึ้นขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="31734-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31734-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="31734-120">Additional resources</span></span>

[<span data-ttu-id="31734-121">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="31734-121">List functions</span></span>](er-functions-category-list.md)
