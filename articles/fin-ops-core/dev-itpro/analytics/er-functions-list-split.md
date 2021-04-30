---
title: ฟังก์ชัน ER SPLIT
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SPLIT
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 26b6ddeb2880fc220283b6389327a497549a4511
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853454"
---
# <a name="split-er-function"></a><span data-ttu-id="b6fec-103">ฟังก์ชัน ER SPLIT</span><span class="sxs-lookup"><span data-stu-id="b6fec-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6fec-104">ฟังก์ชัน `SPLIT` แบ่งค่าสตริงการป้อนที่ระบุลงในสตริงย่อยและส่งกลับผลลัพธ์เป็นค่า *รายการเรกคอร์ด* ใหม่</span><span class="sxs-lookup"><span data-stu-id="b6fec-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b6fec-105">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="b6fec-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="b6fec-106">ไวยากรณ์นี้แบ่งสตริงที่ระบุเป็นสตริงย่อยซึ่งมีความยาวที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="b6fec-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="b6fec-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="b6fec-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="b6fec-108">ไวยากรณ์นี้ใช้แบ่งสตริงย่อยที่ระบุออกเป็นสตริงย่อยตามตั่วคั่นที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="b6fec-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="b6fec-109">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="b6fec-109">Arguments</span></span>

<span data-ttu-id="b6fec-110">`input`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="b6fec-110">`input`: *String*</span></span>

<span data-ttu-id="b6fec-111">ข้อความที่จะแบ่ง</span><span class="sxs-lookup"><span data-stu-id="b6fec-111">The text to split.</span></span>

<span data-ttu-id="b6fec-112">`length`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="b6fec-112">`length`: *Integer*</span></span>

<span data-ttu-id="b6fec-113">ความยาวสูงสุดของสตริงย่อยเดียว</span><span class="sxs-lookup"><span data-stu-id="b6fec-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="b6fec-114">`delimiter`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="b6fec-114">`delimiter`: *String*</span></span>

<span data-ttu-id="b6fec-115">ตัวคั่นที่ใช้ในการแยกสตริงย่อย</span><span class="sxs-lookup"><span data-stu-id="b6fec-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="b6fec-116">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="b6fec-116">Return values</span></span>

<span data-ttu-id="b6fec-117">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="b6fec-117">*Record list*</span></span>

<span data-ttu-id="b6fec-118">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="b6fec-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b6fec-119">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b6fec-119">Usage notes</span></span>

<span data-ttu-id="b6fec-120">โครงสร้างเรกคอร์ดของรายการที่ถูกส่งกลับประกอบด้วยฟิลด์ **ค่า** ของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="b6fec-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="b6fec-121">ทุกเรกคอร์ดของรายการที่ถูกส่งกลับประกอบด้วยสตริงย่อยที่สร้างขึ้นในฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="b6fec-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="b6fec-122">ถ้าอาร์กิวเมนต์ `delimiter` ว่าง รายการใหม่ที่ถูกส่งกลับที่ประกอบด้วยเรกคอร์ดหนึ่งรายการที่มีฟิลด์ **ค่า** ของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="b6fec-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="b6fec-123">ฟิลด์นี้ประกอบด้วยข้อความป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="b6fec-123">This field contains the input text.</span></span>

<span data-ttu-id="b6fec-124">ถ้าอาร์กิวเมนต์ `input` ว่างเปล่า จะมีการส่งคืนรายการที่ว่างเปล่าใหม่</span><span class="sxs-lookup"><span data-stu-id="b6fec-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="b6fec-125">ถ้าไม่สามารถระบุอาร์กิวเมนต์ `input` หรือ `delimiter` (null) จะมีข้อยกเว้นแอปพลิเคชันเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="b6fec-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="b6fec-126">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="b6fec-126">Example 1</span></span>

<span data-ttu-id="b6fec-127">`SPLIT ("abcd", 3)` ส่งคืนรายการใหม่ที่ประกอบด้วยสองเรกคอร์ดที่มีฟิลด์ **ค่า** ของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="b6fec-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="b6fec-128">ฟิลด์ **ค่า** ในเรกคอร์ดแรกประกอบด้วยข้อความ **"abc"** และฟิลด์ **ค่า** ในเรกคอร์ดที่สองประกอบด้วยข้อความ **"d"**</span><span class="sxs-lookup"><span data-stu-id="b6fec-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b6fec-129">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="b6fec-129">Example 2</span></span>

<span data-ttu-id="b6fec-130">`SPLIT ("XAb aBy", "aB")` ส่งคืนรายการใหม่ที่ประกอบด้วยสามเรกคอร์ดที่มีฟิลด์ **ค่า** ของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="b6fec-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="b6fec-131">ฟิลด์ **ค่า** ในเรกคอร์ดแรกประกอบด้วยข้อความ **"X"** ฟิลด์ **ค่า** ในเรกคอร์ดที่สองประกอบด้วยข้อความ **"&nbsp;"** และฟิลด์ **ค่า** ในเรกคอร์ดที่สามประกอบด้วยข้อความ **"y"**</span><span class="sxs-lookup"><span data-stu-id="b6fec-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="b6fec-132">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="b6fec-132">Example 3</span></span>

<span data-ttu-id="b6fec-133">คุณสามารถใช้ฟังก์ชัน [INDEX](er-functions-list-index.md) เพื่อเข้าถึงแต่ละองค์ประกอบของสตริงอินพุทที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="b6fec-133">Yo can use the [INDEX](er-functions-list-index.md) function to access individual elements of the specified input string.</span></span> <span data-ttu-id="b6fec-134">ถ้าคุณป้อนแหล่งข้อมูล **MyList** ของชนิด **ฟิลด์ที่มีการคำนวณ** และกำหนดด้วยนิพจน์ `SPLIT("abc", 1)` นิพจน์ `INDEX(MyList,2).Value` จะส่งกลับค่าข้อความ **"b"**</span><span class="sxs-lookup"><span data-stu-id="b6fec-134">If you enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, the expression `INDEX(MyList,2).Value` returns the text **"b"**.</span></span>

## <a name="example-4"></a><span data-ttu-id="b6fec-135">ตัวอย่างที่ 4</span><span class="sxs-lookup"><span data-stu-id="b6fec-135">Example 4</span></span>

<span data-ttu-id="b6fec-136">ฟังก์ชัน [ENUMERATE](er-functions-list-enumerate.md) สามารถช่วยคุณเข้าถึงแต่ละองค์ประกอบของสตริงอินพุทที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="b6fec-136">The [ENUMERATE](er-functions-list-enumerate.md) function can also help you access individual elements of the specified input string.</span></span> <span data-ttu-id="b6fec-137">ถ้าคุณป้อนแหล่งข้อมูล **MyList** ของชนิด **ฟิลด์ที่มีการคำนวณ** และกำหนดด้วยนิพจน์ `SPLIT("abc", 1)` แล้วป้อนแหล่งข้อมูล **EnumeratedList** ของชนิด **ฟิลด์ที่มีการคำนวณ** และกำหนดด้วยนิพจน์ `ENUMERATE(MyList)` นิพจน์ `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` จะส่งคืนข้อความ **"b"**</span><span class="sxs-lookup"><span data-stu-id="b6fec-137">If you first enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, and then enter the **EnumeratedList** data source of the **Calculated field** type and configure for it the `ENUMERATE(MyList)` expression, the expression `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` returns the text **"b"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6fec-138">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b6fec-138">Additional resources</span></span>

[<span data-ttu-id="b6fec-139">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="b6fec-139">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
