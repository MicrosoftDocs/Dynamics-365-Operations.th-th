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
ms.openlocfilehash: 6adca3c95c10e7d4b3287561925a9d9fe8a74121
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042055"
---
# <span data-ttu-id="d757c-103"><a name="ISEMPTY">ฟังก์ชัน ER ISEMPTY</a></span><span class="sxs-lookup"><span data-stu-id="d757c-103"><a name="ISEMPTY">ISEMPTY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d757c-104">ฟังก์ชัน `ISEMPTY` ส่งกลับค่า *Boolean* ของ **TRUE** ถ้ารายการที่ระบุไม่มีเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="d757c-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="d757c-105">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="d757c-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d757c-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="d757c-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="d757c-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="d757c-107">Arguments</span></span>

<span data-ttu-id="d757c-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="d757c-108">`list`: *Record list*</span></span>

<span data-ttu-id="d757c-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="d757c-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d757c-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="d757c-110">Return values</span></span>

<span data-ttu-id="d757c-111">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="d757c-111">*Boolean*</span></span>

<span data-ttu-id="d757c-112">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="d757c-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="d757c-113">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="d757c-113">Example 1</span></span>

<span data-ttu-id="d757c-114">ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่คำนวณได้* และประกอบด้วยนิพจน์ `SPLIT ("A|B|C", "|")` นิพจน์ `ISEMPTY(DS)` จะส่งกลับค่า **FALSE**</span><span class="sxs-lookup"><span data-stu-id="d757c-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d757c-115">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="d757c-115">Example 2</span></span>

<span data-ttu-id="d757c-116">นิพจน์ `ISEMPTY (SPLIT ("",1))` ส่งกลับค่า **TRUE**</span><span class="sxs-lookup"><span data-stu-id="d757c-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d757c-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d757c-117">Additional resources</span></span>

[<span data-ttu-id="d757c-118">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="d757c-118">List functions</span></span>](er-functions-category-list.md)
