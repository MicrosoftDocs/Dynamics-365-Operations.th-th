---
title: ฟังก์ชัน VALUEINLARGE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) VALUEINLARGE
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 1e35c695d697e0d0f42baeaf568548273f9d205b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565819"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="547d2-103">ฟังก์ชัน VALUEINLARGE ER</span><span class="sxs-lookup"><span data-stu-id="547d2-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="547d2-104">ฟังก์ชัน `VALUEINLARGE` กำหนดว่า การป้อนข้อมูลที่ระบุที่ตรงกับค่า *Int64* หรือ *Integer* ใดๆ ของสินค้าที่ระบุในรายการที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="547d2-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="547d2-105">ฟังก์ชันนี้จะส่งกลับค่า *แบบบูลีน* ของ **TRUE** ถ้าข้อมูลที่ป้อนที่ระบุตรงกับผลลัพธ์ของการเรียกใช้นิพจน์ที่ระบุสำหรับอย่างน้อยหนึ่งเรกคอร์ดของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="547d2-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="547d2-106">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="547d2-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="547d2-107">เพื่อทำความเข้าใจความแตกต่างของฟังก์ชัน `VALUEIN` ดูที่ส่วน [หมายเหตุการใช้งาน](#usage_note) ที่อยู่ต่อไปในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="547d2-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="547d2-108">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="547d2-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="547d2-109">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="547d2-109">Arguments</span></span>

<span data-ttu-id="547d2-110">`input`: *ฟิลด์*</span><span class="sxs-lookup"><span data-stu-id="547d2-110">`input`: *Field*</span></span>

<span data-ttu-id="547d2-111">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิด *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="547d2-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="547d2-112">ค่าของรายการนี้จะถูกจับคู่กัน</span><span class="sxs-lookup"><span data-stu-id="547d2-112">The value of this item will be matched.</span></span>

<span data-ttu-id="547d2-113">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="547d2-113">`list`: *Record list*</span></span>

<span data-ttu-id="547d2-114">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="547d2-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="547d2-115">`list item expression`: *นิพจน์*</span><span class="sxs-lookup"><span data-stu-id="547d2-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="547d2-116">นิพจน์ที่มีเงื่อนไขที่ถูกต้องที่ชี้ไป หรือประกอบด้วยฟิลด์เดียวของรายการที่ระบุที่ควรจะใช้สำหรับการจับคู่กัน</span><span class="sxs-lookup"><span data-stu-id="547d2-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="547d2-117">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="547d2-117">Return values</span></span>

<span data-ttu-id="547d2-118">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="547d2-118">*Boolean*</span></span>

<span data-ttu-id="547d2-119">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="547d2-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="547d2-120"><a name="usage_note">บันทึกย่อการใช้งาน</a></span><span class="sxs-lookup"><span data-stu-id="547d2-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="547d2-121">เมื่อข้อมูลที่ป้อนที่ระบุแสดงชนิด *Int64* หรือ *Integer* ของรายการแหล่งข้อมูล จะมีการเรียกไปยังรายการที่แปลได้กับคำสั่ง SQL โดยตรง รายการที่ระบุจะถูกแปลงเป็นตาราง SQL ชั่วคราวและมีการดำเนินการจับคู่ในฐานข้อมูลโดยดำเนินการสอบถาม `EXISTS JOIN` เดียว</span><span class="sxs-lookup"><span data-stu-id="547d2-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="547d2-122">หรือไม่ฟังก์ชันนี้จะทำงานเป็นฟังก์ชัน [`VALUEIN`](er-functions-logical-valuein.md)</span><span class="sxs-lookup"><span data-stu-id="547d2-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="547d2-123">เมื่อข้อมูลที่ป้อนที่ระบุแสดงรายการแหล่งข้อมูลที่ได้รับการออกแบบเป็นรายการอื่นที่ไม่ใช่ชนิด *Int64* และ *Integer* จะเกิดข้อผิดพลาดในเวลาที่ออกแบบเพื่อแจ้งให้คุณทราบว่าฟังก์ชัน `VALUEINLARGE` ไม่สามารถใช้ได้กับนิพจน์ ER ที่ตั้งค่าคอนฟิกไว้</span><span class="sxs-lookup"><span data-stu-id="547d2-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="547d2-124">เมื่อนิพจน์ฟังก์ชัน `VALUEINLARGE` ดำเนินการและมีการใช้ตารางชั่วคราวมากกว่าหนึ่งตารางในขอบเขตของการดำเนินการนี้ จะเกิดข้อผิดพลาดรันไทม์ขึ้น</span><span class="sxs-lookup"><span data-stu-id="547d2-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="547d2-125">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="547d2-125">Example</span></span>

<span data-ttu-id="547d2-126">คุณกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:</span><span class="sxs-lookup"><span data-stu-id="547d2-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="547d2-127">แหล่งข้อมูล **In** ของชนิด *เรกคอร์ดตาราง*</span><span class="sxs-lookup"><span data-stu-id="547d2-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="547d2-128">แหล่งข้อมูลนี้อ้างถึงตาราง **อินทราสแทต**</span><span class="sxs-lookup"><span data-stu-id="547d2-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="547d2-129">ตัวเลือก **ข้ามบริษัท** ตั้งค่าเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="547d2-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="547d2-130">แหล่งข้อมูล **InMemory** ของชนิดของ *ฟิลด์ที่คำนวณได้*</span><span class="sxs-lookup"><span data-stu-id="547d2-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="547d2-131">แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `WHERE (In, In.Port <> "")`</span><span class="sxs-lookup"><span data-stu-id="547d2-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="547d2-132">แหล่งข้อมูล **InFiltered** ของชนิดของ *ฟิลด์ที่คำนวณได้*</span><span class="sxs-lookup"><span data-stu-id="547d2-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="547d2-133">แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`</span><span class="sxs-lookup"><span data-stu-id="547d2-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="547d2-134">เมื่อมีการเรียกแหล่งข้อมูล **InFiltered** ภายใต้บริบทของบริษัท **DEMF** จะมีการสร้างตารางชั่วคราวใหม่ในฐานข้อมูลแอปพลิเคชัน รายการที่รวบรวมไว้ในรายการหน่วยความจำของรหัสการระบุเรกคอร์ดจะถูกแทรกลงในตารางนี้ และมีการสร้างคำสั่ง SQL ต่อไปนี้เพื่อส่งกลับเรกคอร์ดที่กรองของตาราง **อินทราสแทต**</span><span class="sxs-lookup"><span data-stu-id="547d2-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="547d2-135">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="547d2-135">Additional resources</span></span>

[<span data-ttu-id="547d2-136">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="547d2-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="547d2-137">ฟังก์ชัน VALUEIN</span><span class="sxs-lookup"><span data-stu-id="547d2-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]