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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3a5bb33964c70c85c7d8571057060c1c2b9d433
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687731"
---
# <a name="count-er-function"></a><span data-ttu-id="03396-103">ฟังก์ชัน ER COUNT</span><span class="sxs-lookup"><span data-stu-id="03396-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03396-104">ฟังก์ชัน `COUNT` ส่งกลับค่า *จำนวนเต็ม* ที่แสดงถึงจำนวนของเรกคอร์ดในรายการที่ระบุ ถ้ารายการไม่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="03396-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="03396-105">ถ้ารายการว่างเปล่า ฟังก์ชันนี้จะส่งกลับ **0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="03396-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="03396-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="03396-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="03396-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="03396-107">Arguments</span></span>

<span data-ttu-id="03396-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="03396-108">`list`: *Record list*</span></span>

<span data-ttu-id="03396-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="03396-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="03396-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="03396-110">Return values</span></span>

<span data-ttu-id="03396-111">*จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="03396-111">*Integer*</span></span>

<span data-ttu-id="03396-112">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="03396-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="03396-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="03396-113">Example</span></span>

<span data-ttu-id="03396-114">`COUNT (SPLIT("abcd" , 3))` ส่งคืน **2** เนื่องจากฟังก์ชัน `SPLIT` ที่ใช้ในตัวอย่างนี้จะสร้างรายการที่ประกอบด้วยสองเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="03396-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03396-115">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="03396-115">Additional resources</span></span>

[<span data-ttu-id="03396-116">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="03396-116">List functions</span></span>](er-functions-category-list.md)
