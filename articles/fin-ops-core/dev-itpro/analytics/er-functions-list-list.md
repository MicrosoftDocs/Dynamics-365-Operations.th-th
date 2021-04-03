---
title: ฟังก์ชัน LIST ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) LIST
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 4945ffd0e7bb7bbd238e2d3156c5599d3d423046
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563859"
---
# <a name="list-er-function"></a><span data-ttu-id="78905-103">ฟังก์ชัน LIST ER</span><span class="sxs-lookup"><span data-stu-id="78905-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78905-104">ฟังก์ชัน `LIST` ส่งกลับค่า *รายการเรกคอร์ด* ที่ประกอบด้วยรายการใหม่ของเรกคอร์ดที่สร้างขึ้นจากอาร์กิวเมนต์ที่ระบุของชนิด</span><span class="sxs-lookup"><span data-stu-id="78905-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="78905-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="78905-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="78905-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="78905-106">Arguments</span></span>

<span data-ttu-id="78905-107">`record 1`: *คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="78905-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="78905-108">การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *เรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="78905-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="78905-109">ต้องระบุอาร์กิวเมนต์นี้</span><span class="sxs-lookup"><span data-stu-id="78905-109">This argument is required.</span></span>

<span data-ttu-id="78905-110">`record N`: *คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="78905-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="78905-111">การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *เรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="78905-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="78905-112">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="78905-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="78905-113">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="78905-113">Return values</span></span>

<span data-ttu-id="78905-114">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="78905-114">*Record list*</span></span>

<span data-ttu-id="78905-115">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="78905-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="78905-116">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="78905-116">Usage notes</span></span>

<span data-ttu-id="78905-117">โครงสร้างของรายการที่สร้างขึ้นมีเฉพาะฟิลด์ที่ถูกนำเสนอในโครงสร้างของเรกคอร์ดทั้งหมดที่กล่าวถึงในอาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="78905-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="78905-118">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="78905-118">Example</span></span>

<span data-ttu-id="78905-119">คุณป้อนเรกคอร์ดแหล่งข้อมูล **เรกคอร์ด 1** ของชนิดของ *คอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="78905-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="78905-120">แหล่งข้อมูลนี้ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิด *ฟิลด์ที่มีการคำนวณ*</span><span class="sxs-lookup"><span data-stu-id="78905-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="78905-121">**รหัส:** ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="78905-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="78905-122">**จำนวน:** ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="78905-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="78905-123">จากนั้นให้คุณป้อนแหล่งข้อมูล **เรกคอร์ด 2** ของชนิดของ *คอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="78905-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="78905-124">แหล่งข้อมูลนี้ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิด *ฟิลด์ที่มีการคำนวณ*</span><span class="sxs-lookup"><span data-stu-id="78905-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="78905-125">**จำนวน:** ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="78905-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="78905-126">**IsValid:** ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="78905-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="78905-127">ในกรณีนี้นิพจน์ `LIST('Record 1', 'Record 2')` ส่งกลับรายการใหม่ที่ประกอบด้วยสองเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="78905-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="78905-128">โครงสร้างของรายการนี้ประกอบด้วยฟิลด์ **ยอดเงิน** ของชนิด *จำนวนจริง* เนื่องจากฟิลด์นี้เป็นฟิลด์เดียวที่จะแสดงในทุกอาร์กิวเมนต์ของฟังก์ชันที่เรียก</span><span class="sxs-lookup"><span data-stu-id="78905-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="78905-129">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="78905-129">Additional resources</span></span>

[<span data-ttu-id="78905-130">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="78905-130">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]