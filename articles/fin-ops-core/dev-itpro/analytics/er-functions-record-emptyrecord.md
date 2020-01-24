---
title: ฟังก์ชัน EMPTYRECORD ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ EMPTYRECORD (ER)
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
ms.openlocfilehash: 1cf23f11fa92adfb7a050efd9c68e80e1bee621f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916901"
---
# <span data-ttu-id="40a3d-103"><a name="EMPTYRECORD">ฟังก์ชัน EMPTYRECORD ER</a></span><span class="sxs-lookup"><span data-stu-id="40a3d-103"><a name="EMPTYRECORD">EMPTYRECORD ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40a3d-104">ฟังก์ชัน `EMPTYRECORD` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่เป็น null ซึ่งมีโครงสร้างเดียวกันกับรายการเรกคอร์ดหรือเรกคอร์ดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="40a3d-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="40a3d-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="40a3d-105">Syntax</span></span>

```
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="40a3d-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="40a3d-106">Arguments</span></span>

<span data-ttu-id="40a3d-107">`list`: *รายการเรกคอร์ด* หรือ *คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="40a3d-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="40a3d-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *รายการเรกคอร์ด* หรือ *คอนเทนเนอร์ (เรกคอร์ด)* อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="40a3d-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="40a3d-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="40a3d-109">Return values</span></span>

<span data-ttu-id="40a3d-110">*คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="40a3d-110">*Container (record)*</span></span>

<span data-ttu-id="40a3d-111">ค่าเรกคอร์ดที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="40a3d-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="40a3d-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="40a3d-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="40a3d-113">เรกคอร์ด null เป็นเรกคอร์ดที่ฟิลด์ทั้งหมดมีค่าว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="40a3d-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="40a3d-114">ค่าว่างเปล่า **0** (ศูนย์) สำหรับตัวเลข สตริงว่างสำหรับสตริงที่ และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="40a3d-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="40a3d-115">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="40a3d-115">Example</span></span>

<span data-ttu-id="40a3d-116">`EMPTYRECORD (SPLIT ("abc", 1))` ส่งคืนเรกคอร์ดที่ว่างเปล่าใหม่ที่มีโครงสร้างเดียวกันกับรายการที่ถูกส่งคืนโดยฟังก์ชัน `SPLIT`</span><span class="sxs-lookup"><span data-stu-id="40a3d-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="40a3d-117">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [SPLIT](er-functions-list-split.md)</span><span class="sxs-lookup"><span data-stu-id="40a3d-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40a3d-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="40a3d-118">Additional resources</span></span>

[<span data-ttu-id="40a3d-119">ฟังก์ชันเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="40a3d-119">Record functions</span></span>](er-functions-category-record.md)
