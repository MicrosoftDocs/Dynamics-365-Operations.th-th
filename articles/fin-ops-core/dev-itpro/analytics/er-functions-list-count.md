---
title: ฟังก์ชัน ER COUNT
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) COUNT
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
ms.openlocfilehash: 72d2ea1b26c295c97575a3c7a479ee4e06762424
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042216"
---
# <span data-ttu-id="f400b-103"><a name="COUNT">ฟังก์ชัน ER COUNT</a></span><span class="sxs-lookup"><span data-stu-id="f400b-103"><a name="COUNT">COUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f400b-104">ฟังก์ชัน `COUNT` ส่งกลับค่า *จำนวนเต็ม* ที่แสดงถึงจำนวนของเรกคอร์ดในรายการที่ระบุ ถ้ารายการไม่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="f400b-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="f400b-105">ถ้ารายการว่างเปล่า ฟังก์ชันนี้จะส่งกลับ **0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="f400b-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="f400b-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="f400b-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="f400b-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="f400b-107">Arguments</span></span>

<span data-ttu-id="f400b-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="f400b-108">`list`: *Record list*</span></span>

<span data-ttu-id="f400b-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="f400b-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f400b-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="f400b-110">Return values</span></span>

<span data-ttu-id="f400b-111">*จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="f400b-111">*Integer*</span></span>

<span data-ttu-id="f400b-112">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="f400b-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="f400b-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f400b-113">Example</span></span>

<span data-ttu-id="f400b-114">`COUNT (SPLIT("abcd" , 3))` ส่งคืน **2** เนื่องจากฟังก์ชัน `SPLIT` ที่ใช้ในตัวอย่างนี้จะสร้างรายการที่ประกอบด้วยสองเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="f400b-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f400b-115">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f400b-115">Additional resources</span></span>

[<span data-ttu-id="f400b-116">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="f400b-116">List functions</span></span>](er-functions-category-list.md)
