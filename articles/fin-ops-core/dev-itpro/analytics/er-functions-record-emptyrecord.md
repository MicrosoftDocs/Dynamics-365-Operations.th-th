---
title: ฟังก์ชัน EMPTYRECORD ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ EMPTYRECORD (ER)
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
ms.openlocfilehash: e614c06b4cfad628bbd8a966719ed994ce05b792
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746542"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="8105f-103">ฟังก์ชัน EMPTYRECORD ER</span><span class="sxs-lookup"><span data-stu-id="8105f-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8105f-104">ฟังก์ชัน `EMPTYRECORD` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่เป็น null ซึ่งมีโครงสร้างเดียวกันกับรายการเรกคอร์ดหรือเรกคอร์ดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="8105f-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8105f-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="8105f-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="8105f-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="8105f-106">Arguments</span></span>

<span data-ttu-id="8105f-107">`list`: *รายการเรกคอร์ด* หรือ *คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="8105f-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="8105f-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *รายการเรกคอร์ด* หรือ *คอนเทนเนอร์ (เรกคอร์ด)* อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8105f-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="8105f-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="8105f-109">Return values</span></span>

<span data-ttu-id="8105f-110">*คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="8105f-110">*Container (record)*</span></span>

<span data-ttu-id="8105f-111">ค่าเรกคอร์ดที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="8105f-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8105f-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8105f-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="8105f-113">เรกคอร์ด null เป็นเรกคอร์ดที่ฟิลด์ทั้งหมดมีค่าว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="8105f-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="8105f-114">ค่าว่างเปล่า **0** (ศูนย์) สำหรับตัวเลข สตริงว่างสำหรับสตริงที่ และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="8105f-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="8105f-115">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8105f-115">Example</span></span>

<span data-ttu-id="8105f-116">`EMPTYRECORD (SPLIT ("abc", 1))` ส่งคืนเรกคอร์ดที่ว่างเปล่าใหม่ที่มีโครงสร้างเดียวกันกับรายการที่ถูกส่งคืนโดยฟังก์ชัน `SPLIT`</span><span class="sxs-lookup"><span data-stu-id="8105f-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="8105f-117">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [SPLIT](er-functions-list-split.md)</span><span class="sxs-lookup"><span data-stu-id="8105f-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8105f-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8105f-118">Additional resources</span></span>

[<span data-ttu-id="8105f-119">ฟังก์ชันเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="8105f-119">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]