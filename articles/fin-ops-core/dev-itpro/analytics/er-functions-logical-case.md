---
title: ฟังก์ชัน CASE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) CASE
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
ms.openlocfilehash: 38b51a4d8bf8dc997bae2ae9206d8e71ca48dec6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916073"
---
# <span data-ttu-id="8499a-103"><a name="CASE">ฟังก์ชัน CASE ER</a></span><span class="sxs-lookup"><span data-stu-id="8499a-103"><a name="CASE">CASE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8499a-104">ฟังก์ชัน `CASE` ประเมินค่าของนิพจน์ที่ระบุกับตัวเลือกอื่นที่ระบุและส่งกลับผลลัพธ์ของตัวเลือกแรกที่เท่ากับค่าของนิพจน์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="8499a-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="8499a-105">มิฉะนั้นจะส่งกลับผลลัพธ์เริ่มต้นที่เป็นตัวเลือกหากมีการระบุผลลัพธ์เริ่มต้นเป็นอาร์กิวเมนต์สุดท้ายของฟังก์ชันที่เรียกว่าไม่ได้นำหน้าด้วยตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="8499a-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="8499a-106">ค่าที่ถูกส่งกลับอาจเป็นค่าใดๆ ของชนิดข้อมูลที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="8499a-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="8499a-107">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="8499a-107">Syntax</span></span>

```
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="8499a-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="8499a-108">Arguments</span></span>

<span data-ttu-id="8499a-109">`expression`: *ชนิดข้อมูลดั้งเดิม* (บูลีน ตัวเลข หรือข้อความ)</span><span class="sxs-lookup"><span data-stu-id="8499a-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="8499a-110">นิพจน์ที่ถูกต้องที่ส่งกลับค่าของชนิดข้อมูลดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="8499a-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="8499a-111">`option 1`: *ชนิดข้อมูลดั้งเดิม* (บูลีน ตัวเลข หรือข้อความ)</span><span class="sxs-lookup"><span data-stu-id="8499a-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="8499a-112">นิพจน์ที่ถูกต้องที่ส่งกลับค่าของชนิดข้อมูลดั้งเดิมเดียวกันเป็นอาร์กิวเมนต์ `expression` ของฟังก์ชันที่เรียก</span><span class="sxs-lookup"><span data-stu-id="8499a-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="8499a-113">ต้องระบุอาร์กิวเมนต์นี้</span><span class="sxs-lookup"><span data-stu-id="8499a-113">This argument is required.</span></span>

<span data-ttu-id="8499a-114">`result 1`: *ชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน*</span><span class="sxs-lookup"><span data-stu-id="8499a-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="8499a-115">ผลลัพธ์ที่ส่งกลับที่สอดคล้องกับตัวเลือกก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="8499a-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="8499a-116">ต้องระบุอาร์กิวเมนต์นี้</span><span class="sxs-lookup"><span data-stu-id="8499a-116">This argument is required.</span></span>

<span data-ttu-id="8499a-117">`option N`: *ชนิดข้อมูลดั้งเดิม* (บูลีน ตัวเลข หรือข้อความ)</span><span class="sxs-lookup"><span data-stu-id="8499a-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="8499a-118">นิพจน์ที่ถูกต้องที่ส่งกลับค่าของชนิดข้อมูลดั้งเดิมเดียวกันเป็นอาร์กิวเมนต์ `expression` ของฟังก์ชันที่เรียก</span><span class="sxs-lookup"><span data-stu-id="8499a-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="8499a-119">อาร์กิวเมนต์นี้ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="8499a-119">This argument is optional.</span></span>

<span data-ttu-id="8499a-120">`result N`: *ชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน*</span><span class="sxs-lookup"><span data-stu-id="8499a-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="8499a-121">ผลลัพธ์ที่ส่งกลับที่สอดคล้องกับตัวเลือกก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="8499a-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="8499a-122">อาร์กิวเมนต์นี้ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="8499a-122">This argument is optional.</span></span>

<span data-ttu-id="8499a-123">`default result`: *ชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน*</span><span class="sxs-lookup"><span data-stu-id="8499a-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="8499a-124">ผลที่ควรจะถูกส่งกลับถ้าไม่มีการจับคู่</span><span class="sxs-lookup"><span data-stu-id="8499a-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="8499a-125">อาร์กิวเมนต์นี้ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="8499a-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="8499a-126">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="8499a-126">Return values</span></span>

<span data-ttu-id="8499a-127">*ชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน*</span><span class="sxs-lookup"><span data-stu-id="8499a-127">*Any of the supported data types*</span></span>

<span data-ttu-id="8499a-128">ค่าผลลัพธ์ของชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="8499a-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8499a-129">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8499a-129">Usage notes</span></span>

<span data-ttu-id="8499a-130">มีข้อยกเว้นเมื่อรันไทม์ถ้าไม่มีการจับคู่และไม่ได้กำหนดผลลัพธ์เริ่มต้นที่เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="8499a-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="8499a-131">อาร์กิวเมนต์ทั้งหมดต้องถูกระบุและโดยใช้ชนิดข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8499a-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="8499a-132">มีข้อยกเว้นเกิดขึ้นในเวลาออกแบบถ้าชนิดข้อมูลของผลลัพธ์ที่ถูกกำหนดค่าไม่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="8499a-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="8499a-133">ถ้าค่าผลลัพธ์แรกและค่าผลลัพธ์ที่ *N* คือค่าของชนิดข้อมูลของ *คอนเทนเนอร์ (เรกคอร์ด)* หรือชนิดข้อมูล *รายการเรกคอร์ด* ผลลัพธ์จะมีเฉพาะฟิลด์ที่มีอยู่ในค่าทั้งสองเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8499a-133">If the first result value and the *N*th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="8499a-134">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8499a-134">Example</span></span>

<span data-ttu-id="8499a-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` ส่งกลับสตริง **"WINTER"** ถ้าวันที่รอบเวลาของแอปพลิเคชันปัจจุบันอยู่ระหว่างเดือนตุลาคมและเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="8499a-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="8499a-136">มิฉะนั้น ส่งกลับสตริงที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="8499a-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8499a-137">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8499a-137">Additional resources</span></span>

[<span data-ttu-id="8499a-138">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="8499a-138">Logical functions</span></span>](er-functions-category-logical.md)
