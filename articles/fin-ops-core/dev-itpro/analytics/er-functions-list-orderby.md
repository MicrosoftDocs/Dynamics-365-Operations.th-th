---
title: ฟังก์ชัน ORDERBY ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ORDERBY
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
ms.openlocfilehash: 0a6b5cddc325625dc5b3d677ffcc1da1f8b829cd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041963"
---
# <span data-ttu-id="19c84-103"><a name="ORDERBY">ฟังก์ชัน ORDERBY ER</a></span><span class="sxs-lookup"><span data-stu-id="19c84-103"><a name="ORDERBY">ORDERBY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19c84-104">ฟังก์ชัน `ORDERBY` ส่งกลับรายการที่ระบุเป็นค่า *รายการเรกคอร์ด* หลังจากที่ถูกเรียงลำดับตามอาร์กิวเมนต์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="19c84-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="19c84-105">อาร์กิวเมนต์เหล่านี้สามารถถูกกำหนดเป็นนิพจน์ได้</span><span class="sxs-lookup"><span data-stu-id="19c84-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c84-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="19c84-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="19c84-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="19c84-107">Arguments</span></span>

<span data-ttu-id="19c84-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="19c84-108">`list`: *Record list*</span></span>

<span data-ttu-id="19c84-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="19c84-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="19c84-110">`expression 1`: *ฟิลด์*</span><span class="sxs-lookup"><span data-stu-id="19c84-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="19c84-111">เส้นทางที่ถูกต้องของฟิลด์ของแหล่งข้อมูลที่ถูกอ้างอิงโดยอาร์กิวเมนต์ `list` ของฟังก์ชันที่เรียก</span><span class="sxs-lookup"><span data-stu-id="19c84-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="19c84-112">ฟิลด์ที่อ้างอิงต้องเป็นฟิลด์ของชนิดข้อมูลดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="19c84-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="19c84-113">ต้องระบุอาร์กิวเมนต์นี้</span><span class="sxs-lookup"><span data-stu-id="19c84-113">This argument is required.</span></span>

<span data-ttu-id="19c84-114">`expression N`: *ฟิลด์*</span><span class="sxs-lookup"><span data-stu-id="19c84-114">`expression N`: *Field*</span></span>

<span data-ttu-id="19c84-115">เส้นทางที่ถูกต้องของฟิลด์ของแหล่งข้อมูลที่ถูกอ้างอิงโดยอาร์กิวเมนต์ `list` ของฟังก์ชันที่เรียก</span><span class="sxs-lookup"><span data-stu-id="19c84-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="19c84-116">ฟิลด์ที่อ้างอิงต้องเป็นฟิลด์ของชนิดข้อมูลดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="19c84-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="19c84-117">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="19c84-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="19c84-118">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="19c84-118">Return values</span></span>

<span data-ttu-id="19c84-119">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="19c84-119">*Record list*</span></span>

<span data-ttu-id="19c84-120">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="19c84-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="19c84-121">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="19c84-121">Example 1</span></span>

<span data-ttu-id="19c84-122">ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่คำนวณได้* และประกอบด้วยนิพจน์ `SPLIT ("C|B|A", "|")` นิพจน์ `FIRST( ORDERBY( DS, DS. Value)).Value` จะส่งกลับค่าข้อความ **A**</span><span class="sxs-lookup"><span data-stu-id="19c84-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="19c84-123">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="19c84-123">Example 2</span></span>

<span data-ttu-id="19c84-124">ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ที่อ้างอิงถึงตาราง VendTable นิพจน์ `ORDERBY (Vendors, Vendors.'name()')` จะส่งกลับรายการของผู้จัดจำหน่ายที่เรียงลำดับตามชื่อในลำดับจากน้อยไปมาก</span><span class="sxs-lookup"><span data-stu-id="19c84-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19c84-125">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="19c84-125">Additional resources</span></span>

[<span data-ttu-id="19c84-126">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="19c84-126">List functions</span></span>](er-functions-category-list.md)
