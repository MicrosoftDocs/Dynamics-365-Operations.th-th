---
title: ฟังก์ชั่น STRINGJOIN ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) STRINGJOIN
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
ms.openlocfilehash: ac21651e0f5b5a1579b9335bb7f3217370c4d5a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745532"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="91897-103">ฟังก์ชั่น STRINGJOIN ER</span><span class="sxs-lookup"><span data-stu-id="91897-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91897-104">ฟังก์ชัน `STRINGJOIN` ส่งคืนค่า *สตริง* ที่ประกอบด้วยค่าที่ต่อกันของฟิลด์ที่ระบุจากรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="91897-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="91897-105">ค่าสามารถถูกแบ่งด้วยตัวคั่นที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="91897-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="91897-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="91897-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="91897-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="91897-107">Arguments</span></span>

<span data-ttu-id="91897-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="91897-108">`list`: *Record list*</span></span>

<span data-ttu-id="91897-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="91897-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="91897-110">`field`: *ฟิลด์*</span><span class="sxs-lookup"><span data-stu-id="91897-110">`field`: *Field*</span></span>

<span data-ttu-id="91897-111">เส้นทางที่ถูกต้องของเขตข้อมูลของชนิดข้อมูล *สตริง* ในรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="91897-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="91897-112">`delimiter`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="91897-112">`delimiter`: *String*</span></span>

<span data-ttu-id="91897-113">ตัวคั่นที่ใช้ในการแยกสตริงย่อย</span><span class="sxs-lookup"><span data-stu-id="91897-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="91897-114">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="91897-114">Return values</span></span>

<span data-ttu-id="91897-115">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="91897-115">*String*</span></span>

<span data-ttu-id="91897-116">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="91897-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="91897-117">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="91897-117">Example</span></span>

<span data-ttu-id="91897-118">ถ้าคุณป้อน `SPLIT("abc" , 1)` เป็นแหล่งข้อมูล **DS** นิพจน์`STRINGJOIN (DS, DS.Value, "-")` จะส่งกลับค่า **"a-b-c"**</span><span class="sxs-lookup"><span data-stu-id="91897-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91897-119">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="91897-119">Additional resources</span></span>

[<span data-ttu-id="91897-120">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="91897-120">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]