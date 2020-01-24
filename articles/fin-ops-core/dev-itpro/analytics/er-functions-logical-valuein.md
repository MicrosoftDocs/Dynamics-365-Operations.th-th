---
title: ฟังก์ชัน VALUEIN ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) VALUEIN
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: cb9a387c8b68d0da4dd485116089f1cf4c5ab72c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915981"
---
# <span data-ttu-id="99e73-103"><a name="VALUEIN">ฟังก์ชัน VALUEIN ER</a></span><span class="sxs-lookup"><span data-stu-id="99e73-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99e73-104">ฟังก์ชัน `VALUEIN` กำหนดว่าการป้อนข้อมูลที่ระบุที่ตรงกับค่าใดๆ ของสินค้าที่ระบุในรายการที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="99e73-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="99e73-105">จะส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าอินพุตที่ระบุตรงกับผลลัพธ์ของการเรียกใช้นิพจน์ที่ระบุสำหรับอย่างน้อยหนึ่งเรกคอร์ดของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="99e73-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="99e73-106">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="99e73-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e73-107">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="99e73-107">Syntax</span></span>

```
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="99e73-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="99e73-108">Arguments</span></span>

<span data-ttu-id="99e73-109">`input`: *ฟิลด์*</span><span class="sxs-lookup"><span data-stu-id="99e73-109">`input`: *Field*</span></span>

<span data-ttu-id="99e73-110">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิด *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="99e73-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="99e73-111">ค่าของรายการนี้จะถูกจับคู่กัน</span><span class="sxs-lookup"><span data-stu-id="99e73-111">The value of this item will be matched.</span></span>

<span data-ttu-id="99e73-112">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="99e73-112">`list`: *Record list*</span></span>

<span data-ttu-id="99e73-113">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="99e73-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="99e73-114">`list item expression`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="99e73-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="99e73-115">นิพจน์ที่มีเงื่อนไขที่ถูกต้องที่ชี้ไป หรือประกอบด้วยฟิลด์เดียวของรายการที่ระบุที่ควรจะใช้สำหรับการจับคู่กัน</span><span class="sxs-lookup"><span data-stu-id="99e73-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="99e73-116">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="99e73-116">Return values</span></span>

<span data-ttu-id="99e73-117">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="99e73-117">*Boolean*</span></span>

<span data-ttu-id="99e73-118">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="99e73-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="99e73-119">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="99e73-119">Usage notes</span></span>

<span data-ttu-id="99e73-120">โดยทั่วไป ฟังก์ชัน `VALUEIN` จะถูกแปลเป็นชุดเงื่อนไข **OR**</span><span class="sxs-lookup"><span data-stu-id="99e73-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="99e73-121">ในบางกรณีสามารถแปลเป็นคำสั่ง SQL ฐานข้อมูลโดยใช้ตัวดำเนินการ `EXISTS JOIN`</span><span class="sxs-lookup"><span data-stu-id="99e73-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="99e73-122">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="99e73-122">Example 1</span></span>

<span data-ttu-id="99e73-123">ในการแม็ปแบบจำลองของคุณ คุณสามารถกำหนดแหล่งข้อมูล **รายการ** ของชนิด *ฟิลด์ที่คำนวณได้*</span><span class="sxs-lookup"><span data-stu-id="99e73-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="99e73-124">แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `SPLIT ("a,b,c", ",")`</span><span class="sxs-lookup"><span data-stu-id="99e73-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="99e73-125">เมื่อแหล่งข้อมูลถูกเรียก ถ้ามีการกำหนดค่าเป็นนิพจน์ `VALUEIN ("B", List, List.Value)` จะส่งกลับเป็น **TRUE**</span><span class="sxs-lookup"><span data-stu-id="99e73-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="99e73-126">ในกรณีนี้ ฟังก์ชัน `VALUEIN` จะถูกแปลเป็นชุดของเงื่อนไขต่อไปนี้: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**</span><span class="sxs-lookup"><span data-stu-id="99e73-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="99e73-127">เมื่อแหล่งข้อมูลถูกเรียก ถ้ามีการกำหนดค่าเป็นนิพจน์ `VALUEIN ("B", List, LEFT(List.Value, 0))` จะส่งกลับเป็น **FALSE**</span><span class="sxs-lookup"><span data-stu-id="99e73-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="99e73-128">ในกรณีนี้ ฟังก์ชัน `VALUEIN` จะถูกแปลเป็นเงื่อนไขต่อไปนี้: `("B" = "")` ซึ่งไม่เท่ากับ **TRUE**</span><span class="sxs-lookup"><span data-stu-id="99e73-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="99e73-129">ขีดจำกัดสูงสุดสำหรับจำนวนของอักขระในข้อความของเงื่อนไขดังกล่าวคือ 32,768 อักขระ</span><span class="sxs-lookup"><span data-stu-id="99e73-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="99e73-130">ดังนั้น คุณไม่ควรสร้างแหล่งข้อมูลที่อาจมีขนาดเกินขีดจำกัดนี้ขณะใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="99e73-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="99e73-131">ถ้าเกินขีดจำกัด แอปพลิเคชันจะหยุดทำงาน และจะแสดงข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="99e73-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="99e73-132">ตัวอย่างเช่น สถานการณ์นี้อาจเกิดขึ้น ถ้ามีการกำหนดค่าแหล่งข้อมูลเป็น `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` และรายการ **List1** and **List2** ประกอบด้วยเรกคอร์ดจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="99e73-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="99e73-133">ในบางกรณี ฟังก์ชัน `VALUEIN` ถูกแปลเป็นคำสั่งฐานข้อมูล โดยใช้ตัวดำเนินการ `EXISTS JOIN`</span><span class="sxs-lookup"><span data-stu-id="99e73-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="99e73-134">ลักษณะการทำงานนี้เกิดขึ้นเมื่อการใช้ฟังก์ชัน [ตัวกรอง](er-functions-list-filter.md) และเป็นไปตามเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="99e73-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="99e73-135">ตัวเลือก **ขอการสอบถาม** ถูกปิดใช้งานสำหรับแหล่งข้อมูลของฟังก์ชัน `VALUEIN` ที่อ้างอิงถึงรายการของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="99e73-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="99e73-136">ไม่มีการใช้เงื่อนไขเพิ่มเติมกับแหล่งข้อมูลนี้ในช่วงรันไทม์</span><span class="sxs-lookup"><span data-stu-id="99e73-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="99e73-137">ไม่มีนิพจน์แบบซ้อนถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูลของฟังก์ชัน `VALUEIN` ที่อ้างอิงถึงรายการของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="99e73-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="99e73-138">สินค้าในรายการของฟังก์ชัน `VALUEIN` อ้างถึงฟิลด์ของแหล่งข้อมูลที่ระบุ ไม่ใช่นิพจน์หรือวิธีการของแหล่งข่อมูลนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="99e73-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="99e73-139">พิจารณาการใช้ตัวเลือกนี้แทนฟังก์ชัน [WHERE](er-functions-list-where.md) ที่อธิบายไว้ก่อนหน้านี้ในตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="99e73-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="99e73-140">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="99e73-140">Example 2</span></span>

<span data-ttu-id="99e73-141">คุณกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:</span><span class="sxs-lookup"><span data-stu-id="99e73-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="99e73-142">แหล่งข้อมูล **In** ของชนิด *เรกคอร์ดตาราง*</span><span class="sxs-lookup"><span data-stu-id="99e73-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="99e73-143">แหล่งข้อมูลนี้อ้างถึงตาราง Intrastat</span><span class="sxs-lookup"><span data-stu-id="99e73-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="99e73-144">แหล่งข้อมูล **Port** ของชนิด *เรกคอร์ดตาราง*</span><span class="sxs-lookup"><span data-stu-id="99e73-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="99e73-145">แหล่งข้อมูลนี้อ้างถึงตาราง IntrastatPort</span><span class="sxs-lookup"><span data-stu-id="99e73-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="99e73-146">เมื่อแหล่งข้อมูลถูกเรียกว่าถูกตั้งค่าคอนฟิกเป็นนิพจน์ `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` คำสั่ง SQL ต่อไปนี้จะถูกสร้างขึ้นเพื่อส่งคืนเรกคอร์ดที่มีการกรองข้อมูลของตารางอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="99e73-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="99e73-147">สำหรับฟิลด์ **dataAreaId** คำสั่ง SQL ขั้นสุดท้ายจะถูกสร้างขึ้นโดยการใช้ตัวดำเนินการ `IN`</span><span class="sxs-lookup"><span data-stu-id="99e73-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="99e73-148">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="99e73-148">Example 3</span></span>

<span data-ttu-id="99e73-149">คุณกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:</span><span class="sxs-lookup"><span data-stu-id="99e73-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="99e73-150">แหล่งข้อมูล **Le** ของชนิดของ *ฟิลด์ที่คำนวณได้*</span><span class="sxs-lookup"><span data-stu-id="99e73-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="99e73-151">แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `SPLIT ("DEMF,GBSI,USMF", ",")`</span><span class="sxs-lookup"><span data-stu-id="99e73-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="99e73-152">แหล่งข้อมูล **In** ของชนิด *เรกคอร์ดตาราง*</span><span class="sxs-lookup"><span data-stu-id="99e73-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="99e73-153">แหล่งข้อมูลนี้อ้างถึงตารางอินทราสแทต และตัวเลือก **ระหว่างบริษัท** ถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="99e73-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="99e73-154">เมื่อแหล่งข้อมูลถูกเรียกว่าถูกตั้งค่าคอนฟิกเป็นนิพจน์ `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` คำสั่ง SQL ขั้นสุดท้ายประกอบด้วยเงื่อนไขต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="99e73-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="99e73-155">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="99e73-155">Additional resources</span></span>

[<span data-ttu-id="99e73-156">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="99e73-156">Logical functions</span></span>](er-functions-category-logical.md)
