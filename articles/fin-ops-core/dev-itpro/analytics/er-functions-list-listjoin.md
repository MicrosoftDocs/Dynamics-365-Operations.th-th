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
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28f03e5e6af0f252a994f2e54b57a5ef654f4e67
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682254"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="c420d-103">ฟังก์ชัน LISTJOIN ER</span><span class="sxs-lookup"><span data-stu-id="c420d-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c420d-104">ฟังก์ชัน `LISTJOIN` ส่งกลับค่า *รายการเรกคอร์ด* ที่แสดงรายการเข้าร่วมใหม่ของเรกคอร์ดที่สร้างขึ้นจากอาร์กิวเมนต์ที่ระบุของชนิด</span><span class="sxs-lookup"><span data-stu-id="c420d-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="c420d-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="c420d-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="c420d-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="c420d-106">Arguments</span></span>

<span data-ttu-id="c420d-107">`list 1`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="c420d-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="c420d-108">การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="c420d-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="c420d-109">อาร์กิวเมนต์นี้เป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="c420d-109">This argument is mandatory.</span></span>

<span data-ttu-id="c420d-110">`list N`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="c420d-110">`list N`: *Record list*</span></span>

<span data-ttu-id="c420d-111">การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="c420d-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="c420d-112">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c420d-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="c420d-113">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="c420d-113">Return values</span></span>

<span data-ttu-id="c420d-114">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="c420d-114">*Record list*</span></span>

<span data-ttu-id="c420d-115">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c420d-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c420d-116">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c420d-116">Usage notes</span></span>

<span data-ttu-id="c420d-117">โครงสร้างของรายการที่สร้างขึ้นมีเฉพาะฟิลด์ที่แสดงในโครงสร้างของรายการเรกคอร์ดทั้งหมดที่มีการอ้างถึงในอาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="c420d-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="c420d-118">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="c420d-118">Example</span></span>

<span data-ttu-id="c420d-119">คุณป้อนแหล่งข้อมูล **เรกคอร์ด 1** ของชนิดของ `Container`</span><span class="sxs-lookup"><span data-stu-id="c420d-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="c420d-120">แหล่งข้อมูลนี้ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิดฟิลด์ `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="c420d-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="c420d-121">**Code**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `String`</span><span class="sxs-lookup"><span data-stu-id="c420d-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="c420d-122">**Amount**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `Real`</span><span class="sxs-lookup"><span data-stu-id="c420d-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="c420d-123">จากนั้นคุณป้อนแหล่งข้อมูล **เรกคอร์ด 2** ของชนิดของ `Container`</span><span class="sxs-lookup"><span data-stu-id="c420d-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="c420d-124">แหล่งข้อมูลนี้ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิดฟิลด์ `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="c420d-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="c420d-125">**Amount**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `Real`</span><span class="sxs-lookup"><span data-stu-id="c420d-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="c420d-126">**IsValid**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `Boolean`</span><span class="sxs-lookup"><span data-stu-id="c420d-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![เพจตัวออกแบบการแม็ปแบบจำลอง ER](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="c420d-128">ในกรณีนี้นิพจน์ `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` ส่งกลับรายการใหม่ที่ประกอบด้วยสองเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c420d-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![หน้าตัวออกแบบการแม็ปแบบจำลอง ER ที่มีสองเรกคอร์ด](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="c420d-130">โครงสร้างของรายการนี้ประกอบด้วยฟิลด์ **ยอดเงิน** เดียวของชนิด `Real` เนื่องจากฟิลด์นี้เป็นฟิลด์เดียวที่จะแสดงในทุกอาร์กิวเมนต์ของฟังก์ชันที่เรียก</span><span class="sxs-lookup"><span data-stu-id="c420d-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![ฟิลด์จำนวนเงินของหน้าตัวออกแบบการแม็ปแบบจำลอง ER](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="c420d-132">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c420d-132">Additional resources</span></span>

[<span data-ttu-id="c420d-133">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="c420d-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="c420d-134">ดีบักแหล่งข้อมูลของรูปแบบ ER ที่ดําเนินการ เพื่อวิเคราะห์การแปลงและลำดับของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c420d-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)
