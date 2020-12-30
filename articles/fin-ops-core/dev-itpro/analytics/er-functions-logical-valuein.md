---
title: ฟังก์ชัน VALUEIN ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) VALUEIN
author: NickSelin
manager: kfend
ms.date: 08/18/2020
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
ms.openlocfilehash: 0a133067ab74c711084cc1d7f456cbe49acdf79d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686941"
---
# <a name="valuein-er-function"></a><span data-ttu-id="2a901-103">ฟังก์ชัน VALUEIN ER</span><span class="sxs-lookup"><span data-stu-id="2a901-103">VALUEIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a901-104">ฟังก์ชัน `VALUEIN` กำหนดว่าการป้อนข้อมูลที่ระบุที่ตรงกับค่าใดๆ ของสินค้าที่ระบุในรายการที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2a901-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="2a901-105">จะส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าอินพุตที่ระบุตรงกับผลลัพธ์ของการเรียกใช้นิพจน์ที่ระบุสำหรับอย่างน้อยหนึ่งเรกคอร์ดของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="2a901-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="2a901-106">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="2a901-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a901-107">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="2a901-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="2a901-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="2a901-108">Arguments</span></span>

<span data-ttu-id="2a901-109">`input`: *ฟิลด์*</span><span class="sxs-lookup"><span data-stu-id="2a901-109">`input`: *Field*</span></span>

<span data-ttu-id="2a901-110">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิด *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="2a901-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="2a901-111">ค่าของรายการนี้จะถูกจับคู่กัน</span><span class="sxs-lookup"><span data-stu-id="2a901-111">The value of this item will be matched.</span></span>

<span data-ttu-id="2a901-112">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="2a901-112">`list`: *Record list*</span></span>

<span data-ttu-id="2a901-113">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="2a901-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="2a901-114">`list item expression`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="2a901-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="2a901-115">นิพจน์ที่มีเงื่อนไขที่ถูกต้องที่ชี้ไป หรือประกอบด้วยฟิลด์เดียวของรายการที่ระบุที่ควรจะใช้สำหรับการจับคู่กัน</span><span class="sxs-lookup"><span data-stu-id="2a901-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="2a901-116">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="2a901-116">Return values</span></span>

<span data-ttu-id="2a901-117">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="2a901-117">*Boolean*</span></span>

<span data-ttu-id="2a901-118">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="2a901-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2a901-119">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2a901-119">Usage notes</span></span>

<span data-ttu-id="2a901-120">โดยทั่วไป ฟังก์ชัน `VALUEIN` จะถูกแปลเป็นชุดเงื่อนไข **OR**</span><span class="sxs-lookup"><span data-stu-id="2a901-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span> <span data-ttu-id="2a901-121">หากรายการเงื่อนไข **หรือ** มีขนาดใหญ่และเกินความยาวรวมสูงสุดของคำสั่ง SQL ให้ลองพิจารณาการใช้ฟังก์ชัน [`VALUEINLARGE`](er-functions-logical-valueinlarge.md)</span><span class="sxs-lookup"><span data-stu-id="2a901-121">If the list of **OR** conditions is large and the maximum total length of an SQL statement might be exceeded, consider using the [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) function.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="2a901-122">ในบางกรณีสามารถแปลเป็นคำสั่ง SQL ฐานข้อมูลโดยใช้ตัวดำเนินการ `EXISTS JOIN`</span><span class="sxs-lookup"><span data-stu-id="2a901-122">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="2a901-123">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="2a901-123">Example 1</span></span>

<span data-ttu-id="2a901-124">ในการแม็ปแบบจำลองของคุณ คุณสามารถกำหนดแหล่งข้อมูล **รายการ** ของชนิด *ฟิลด์ที่มีการคำนวณ*</span><span class="sxs-lookup"><span data-stu-id="2a901-124">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="2a901-125">แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `SPLIT ("a,b,c", ",")`</span><span class="sxs-lookup"><span data-stu-id="2a901-125">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="2a901-126">เมื่อแหล่งข้อมูลถูกเรียก ถ้ามีการกำหนดค่าเป็นนิพจน์ `VALUEIN ("B", List, List.Value)` จะส่งกลับเป็น **TRUE**</span><span class="sxs-lookup"><span data-stu-id="2a901-126">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="2a901-127">ในกรณีนี้ ฟังก์ชัน `VALUEIN` จะถูกแปลเป็นชุดของเงื่อนไขต่อไปนี้: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**</span><span class="sxs-lookup"><span data-stu-id="2a901-127">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="2a901-128">เมื่อแหล่งข้อมูลถูกเรียก ถ้ามีการกำหนดค่าเป็นนิพจน์ `VALUEIN ("B", List, LEFT(List.Value, 0))` จะส่งกลับเป็น **FALSE**</span><span class="sxs-lookup"><span data-stu-id="2a901-128">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="2a901-129">ในกรณีนี้ ฟังก์ชัน `VALUEIN` จะถูกแปลเป็นเงื่อนไขต่อไปนี้: `("B" = "")` ซึ่งไม่เท่ากับ **TRUE**</span><span class="sxs-lookup"><span data-stu-id="2a901-129">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="2a901-130">ขีดจำกัดสูงสุดสำหรับจำนวนของอักขระในข้อความของเงื่อนไขดังกล่าวคือ 32,768 อักขระ</span><span class="sxs-lookup"><span data-stu-id="2a901-130">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="2a901-131">ดังนั้น คุณไม่ควรสร้างแหล่งข้อมูลที่อาจมีขนาดเกินขีดจำกัดนี้ขณะใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="2a901-131">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="2a901-132">ถ้าเกินขีดจำกัด แอปพลิเคชันจะหยุดทำงาน และจะแสดงข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="2a901-132">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="2a901-133">ตัวอย่างเช่น สถานการณ์นี้อาจเกิดขึ้น ถ้ามีการกำหนดค่าแหล่งข้อมูลเป็น `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` และรายการ **List1** and **List2** ประกอบด้วยเรกคอร์ดจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="2a901-133">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="2a901-134">ในบางกรณี ฟังก์ชัน `VALUEIN` ถูกแปลเป็นคำสั่งฐานข้อมูล โดยใช้ตัวดำเนินการ `EXISTS JOIN`</span><span class="sxs-lookup"><span data-stu-id="2a901-134">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="2a901-135">ลักษณะการทำงานนี้เกิดขึ้นเมื่อการใช้ฟังก์ชัน [`FILTER`](er-functions-list-filter.md) และเป็นไปตามเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2a901-135">This behavior occurs when the [`FILTER`](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="2a901-136">ตัวเลือก **ขอการสอบถาม** ถูกปิดใช้งานสำหรับแหล่งข้อมูลของฟังก์ชัน `VALUEIN` ที่อ้างอิงถึงรายการของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="2a901-136">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="2a901-137">ไม่มีการใช้เงื่อนไขเพิ่มเติมกับแหล่งข้อมูลนี้ในช่วงรันไทม์</span><span class="sxs-lookup"><span data-stu-id="2a901-137">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="2a901-138">ไม่มีนิพจน์แบบซ้อนถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูลของฟังก์ชัน `VALUEIN` ที่อ้างอิงถึงรายการของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="2a901-138">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="2a901-139">สินค้าในรายการของฟังก์ชัน `VALUEIN` อ้างถึงฟิลด์ของแหล่งข้อมูลที่ระบุ ไม่ใช่นิพจน์หรือวิธีการของแหล่งข่อมูลนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="2a901-139">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="2a901-140">พิจารณาการใช้ตัวเลือกนี้แทนฟังก์ชัน [`WHERE`](er-functions-list-where.md) ที่อธิบายไว้ก่อนหน้านี้ในตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="2a901-140">Consider using this option instead of the [`WHERE`](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="2a901-141">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="2a901-141">Example 2</span></span>

<span data-ttu-id="2a901-142">คุณกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:</span><span class="sxs-lookup"><span data-stu-id="2a901-142">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="2a901-143">แหล่งข้อมูล **In** ของชนิด *เรกคอร์ดตาราง*</span><span class="sxs-lookup"><span data-stu-id="2a901-143">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="2a901-144">แหล่งข้อมูลนี้อ้างถึงตาราง Intrastat</span><span class="sxs-lookup"><span data-stu-id="2a901-144">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="2a901-145">แหล่งข้อมูล **Port** ของชนิด *เรกคอร์ดตาราง*</span><span class="sxs-lookup"><span data-stu-id="2a901-145">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="2a901-146">แหล่งข้อมูลนี้อ้างถึงตาราง IntrastatPort</span><span class="sxs-lookup"><span data-stu-id="2a901-146">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="2a901-147">เมื่อแหล่งข้อมูลถูกเรียกว่าถูกตั้งค่าคอนฟิกเป็นนิพจน์ `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` คำสั่ง SQL ต่อไปนี้จะถูกสร้างขึ้นเพื่อส่งคืนเรกคอร์ดที่มีการกรองข้อมูลของตารางอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="2a901-147">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="2a901-148">สำหรับฟิลด์ **dataAreaId** คำสั่ง SQL ขั้นสุดท้ายจะถูกสร้างขึ้นโดยการใช้ตัวดำเนินการ `IN`</span><span class="sxs-lookup"><span data-stu-id="2a901-148">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="2a901-149">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="2a901-149">Example 3</span></span>

<span data-ttu-id="2a901-150">คุณกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:</span><span class="sxs-lookup"><span data-stu-id="2a901-150">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="2a901-151">แหล่งข้อมูล **Le** ของชนิดของ *ฟิลด์ที่มีการคำนวณ*</span><span class="sxs-lookup"><span data-stu-id="2a901-151">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="2a901-152">แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `SPLIT ("DEMF,GBSI,USMF", ",")`</span><span class="sxs-lookup"><span data-stu-id="2a901-152">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="2a901-153">แหล่งข้อมูล **In** ของชนิด *เรกคอร์ดตาราง*</span><span class="sxs-lookup"><span data-stu-id="2a901-153">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="2a901-154">แหล่งข้อมูลนี้อ้างถึงตารางอินทราสแทต และตัวเลือก **ระหว่างบริษัท** ถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2a901-154">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="2a901-155">เมื่อแหล่งข้อมูลถูกเรียกว่าถูกตั้งค่าคอนฟิกเป็นนิพจน์ `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` คำสั่ง SQL ขั้นสุดท้ายประกอบด้วยเงื่อนไขต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2a901-155">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="2a901-156">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2a901-156">Additional resources</span></span>

[<span data-ttu-id="2a901-157">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="2a901-157">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="2a901-158">ฟังก์ชัน VALUEINLARGE</span><span class="sxs-lookup"><span data-stu-id="2a901-158">VALUEINLARGE functions</span></span>](er-functions-logical-valueinlarge.md)
