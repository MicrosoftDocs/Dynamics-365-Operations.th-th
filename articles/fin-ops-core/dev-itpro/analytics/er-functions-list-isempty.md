---
title: ฟังก์ชัน ER ISEMPTY
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ISEMPTY
author: NickSelin
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
ms.openlocfilehash: 9c33e8b613bf5bf5bc17a42a7668d4cc4ee58e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750447"
---
# <a name="isempty-er-function"></a><span data-ttu-id="076bc-103">ฟังก์ชัน ER ISEMPTY</span><span class="sxs-lookup"><span data-stu-id="076bc-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="076bc-104">ฟังก์ชัน `ISEMPTY` ส่งกลับค่า *Boolean* ของ **TRUE** ถ้ารายการที่ระบุไม่มีเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="076bc-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="076bc-105">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="076bc-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="076bc-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="076bc-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="076bc-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="076bc-107">Arguments</span></span>

<span data-ttu-id="076bc-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="076bc-108">`list`: *Record list*</span></span>

<span data-ttu-id="076bc-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="076bc-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="076bc-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="076bc-110">Return values</span></span>

<span data-ttu-id="076bc-111">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="076bc-111">*Boolean*</span></span>

<span data-ttu-id="076bc-112">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="076bc-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="076bc-113">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="076bc-113">Example 1</span></span>

<span data-ttu-id="076bc-114">ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่มีการคำนวณ* และประกอบด้วยนิพจน์ `SPLIT ("A|B|C", "|")` นิพจน์ `ISEMPTY(DS)` จะส่งกลับค่า **FALSE**</span><span class="sxs-lookup"><span data-stu-id="076bc-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="076bc-115">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="076bc-115">Example 2</span></span>

<span data-ttu-id="076bc-116">นิพจน์ `ISEMPTY (SPLIT ("",1))` ส่งกลับค่า **TRUE**</span><span class="sxs-lookup"><span data-stu-id="076bc-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="076bc-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="076bc-117">Additional resources</span></span>

[<span data-ttu-id="076bc-118">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="076bc-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]