---
title: ฟังก์ชั่น STRINGJOIN ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) STRINGJOIN
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
ms.openlocfilehash: 586dbcb98d237325188f4b0384580613ab7a9347
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683757"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="a6ab2-103">ฟังก์ชั่น STRINGJOIN ER</span><span class="sxs-lookup"><span data-stu-id="a6ab2-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6ab2-104">ฟังก์ชัน `STRINGJOIN` ส่งคืนค่า *สตริง* ที่ประกอบด้วยค่าที่ต่อกันของฟิลด์ที่ระบุจากรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a6ab2-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="a6ab2-105">ค่าสามารถถูกแบ่งด้วยตัวคั่นที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a6ab2-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ab2-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="a6ab2-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="a6ab2-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="a6ab2-107">Arguments</span></span>

<span data-ttu-id="a6ab2-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="a6ab2-108">`list`: *Record list*</span></span>

<span data-ttu-id="a6ab2-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="a6ab2-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="a6ab2-110">`field`: *ฟิลด์*</span><span class="sxs-lookup"><span data-stu-id="a6ab2-110">`field`: *Field*</span></span>

<span data-ttu-id="a6ab2-111">เส้นทางที่ถูกต้องของเขตข้อมูลของชนิดข้อมูล *สตริง* ในรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a6ab2-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="a6ab2-112">`delimiter`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="a6ab2-112">`delimiter`: *String*</span></span>

<span data-ttu-id="a6ab2-113">ตัวคั่นที่ใช้ในการแยกสตริงย่อย</span><span class="sxs-lookup"><span data-stu-id="a6ab2-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="a6ab2-114">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="a6ab2-114">Return values</span></span>

<span data-ttu-id="a6ab2-115">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="a6ab2-115">*String*</span></span>

<span data-ttu-id="a6ab2-116">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="a6ab2-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a6ab2-117">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a6ab2-117">Example</span></span>

<span data-ttu-id="a6ab2-118">ถ้าคุณป้อน `SPLIT("abc" , 1)` เป็นแหล่งข้อมูล **DS** นิพจน์`STRINGJOIN (DS, DS.Value, "-")` จะส่งกลับค่า **"a-b-c"**</span><span class="sxs-lookup"><span data-stu-id="a6ab2-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6ab2-119">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a6ab2-119">Additional resources</span></span>

[<span data-ttu-id="a6ab2-120">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="a6ab2-120">List functions</span></span>](er-functions-category-list.md)
