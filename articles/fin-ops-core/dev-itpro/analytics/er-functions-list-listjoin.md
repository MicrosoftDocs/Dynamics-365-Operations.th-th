---
title: ฟังก์ชัน LISTJOIN ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) LISTJOIN
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249046"
---
# <a name=""></a><span data-ttu-id="0f0b6-103"><a name="LISTJOIN">ฟังก์ชัน LISTJOIN ER</a></span><span class="sxs-lookup"><span data-stu-id="0f0b6-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f0b6-104">ฟังก์ชัน `LISTJOIN` ส่งกลับค่า *รายการเรกคอร์ด* ที่แสดงรายการเข้าร่วมใหม่ของเรกคอร์ดที่สร้างขึ้นจากอาร์กิวเมนต์ที่ระบุของชนิด</span><span class="sxs-lookup"><span data-stu-id="0f0b6-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0b6-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="0f0b6-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="0f0b6-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="0f0b6-106">Arguments</span></span>

<span data-ttu-id="0f0b6-107">`list 1`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="0f0b6-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="0f0b6-108">การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="0f0b6-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="0f0b6-109">อาร์กิวเมนต์นี้เป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="0f0b6-109">This argument is mandatory.</span></span>

<span data-ttu-id="0f0b6-110">`list N`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="0f0b6-110">`list N`: *Record list*</span></span>

<span data-ttu-id="0f0b6-111">การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="0f0b6-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="0f0b6-112">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="0f0b6-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="0f0b6-113">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="0f0b6-113">Return values</span></span>

<span data-ttu-id="0f0b6-114">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="0f0b6-114">*Record list*</span></span>

<span data-ttu-id="0f0b6-115">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="0f0b6-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0f0b6-116">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0f0b6-116">Usage notes</span></span>

<span data-ttu-id="0f0b6-117">โครงสร้างของรายการที่สร้างขึ้นมีเฉพาะฟิลด์ที่แสดงในโครงสร้างของรายการเรกคอร์ดทั้งหมดที่มีการอ้างถึงในอาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="0f0b6-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="0f0b6-118">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0f0b6-118">Example</span></span>

<span data-ttu-id="0f0b6-119">คุณป้อนแหล่งข้อมูล **เรกคอร์ด 1** ของชนิดของ `Container`</span><span class="sxs-lookup"><span data-stu-id="0f0b6-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="0f0b6-120">แหล่งข้อมูลนี้ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิดฟิลด์ `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="0f0b6-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="0f0b6-121">**Code**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `String`</span><span class="sxs-lookup"><span data-stu-id="0f0b6-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="0f0b6-122">**Amount**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `Real`</span><span class="sxs-lookup"><span data-stu-id="0f0b6-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="0f0b6-123">จากนั้นคุณป้อนแหล่งข้อมูล **เรกคอร์ด 2** ของชนิดของ `Container`</span><span class="sxs-lookup"><span data-stu-id="0f0b6-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="0f0b6-124">แหล่งข้อมูลนี้ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิดฟิลด์ `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="0f0b6-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="0f0b6-125">**Amount**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `Real`</span><span class="sxs-lookup"><span data-stu-id="0f0b6-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="0f0b6-126">**IsValid**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `Boolean`</span><span class="sxs-lookup"><span data-stu-id="0f0b6-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

<span data-ttu-id="0f0b6-127">ในกรณีนี้นิพจน์ `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` ส่งกลับรายการใหม่ที่ประกอบด้วยสองเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="0f0b6-127">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span> <span data-ttu-id="0f0b6-128">โครงสร้างของรายการนี้ประกอบด้วยฟิลด์ **ยอดเงิน** เดียวของชนิด `Real` เนื่องจากฟิลด์นี้เป็นฟิลด์เดียวที่จะแสดงในทุกอาร์กิวเมนต์ของฟังก์ชันที่เรียก</span><span class="sxs-lookup"><span data-stu-id="0f0b6-128">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f0b6-129">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0f0b6-129">Additional resources</span></span>

[<span data-ttu-id="0f0b6-130">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="0f0b6-130">List functions</span></span>](er-functions-category-list.md)
