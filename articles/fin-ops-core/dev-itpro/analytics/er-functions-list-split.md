---
title: ฟังก์ชัน ER SPLIT
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SPLIT
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
ms.openlocfilehash: 31caf7c728a92d31428f47320c074fa9fc35bda6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916119"
---
# <span data-ttu-id="a3506-103"><a name="SPLIT">ฟังก์ชัน ER SPLIT</a></span><span class="sxs-lookup"><span data-stu-id="a3506-103"><a name="SPLIT">SPLIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3506-104">ฟังก์ชัน `SPLIT` แบ่งค่าสตริงการป้อนที่ระบุลงในสตริงย่อยและส่งกลับผลลัพธ์เป็นค่า *รายการเรกคอร์ด* ใหม่</span><span class="sxs-lookup"><span data-stu-id="a3506-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="a3506-105">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="a3506-105">Syntax 1</span></span>

```
SPLIT (input, length)
```

<span data-ttu-id="a3506-106">ไวยากรณ์นี้แบ่งสตริงที่ระบุเป็นสตริงย่อยซึ่งมีความยาวที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a3506-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="a3506-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="a3506-107">Syntax 2</span></span>

```
SPLIT (input, delimiter)
```

<span data-ttu-id="a3506-108">ไวยากรณ์นี้ใช้แบ่งสตริงย่อยที่ระบุออกเป็นสตริงย่อยตามตั่วคั่นที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a3506-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="a3506-109">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="a3506-109">Arguments</span></span>

<span data-ttu-id="a3506-110">`input`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="a3506-110">`input`: *String*</span></span>

<span data-ttu-id="a3506-111">ข้อความที่จะแบ่ง</span><span class="sxs-lookup"><span data-stu-id="a3506-111">The text to split.</span></span>

<span data-ttu-id="a3506-112">`length`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="a3506-112">`length`: *Integer*</span></span>

<span data-ttu-id="a3506-113">ความยาวสูงสุดของสตริงย่อยเดียว</span><span class="sxs-lookup"><span data-stu-id="a3506-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="a3506-114">`delimiter`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="a3506-114">`delimiter`: *String*</span></span>

<span data-ttu-id="a3506-115">ตัวคั่นที่ใช้ในการแยกสตริงย่อย</span><span class="sxs-lookup"><span data-stu-id="a3506-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="a3506-116">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="a3506-116">Return values</span></span>

<span data-ttu-id="a3506-117">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="a3506-117">*Record list*</span></span>

<span data-ttu-id="a3506-118">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="a3506-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a3506-119">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a3506-119">Usage notes</span></span>

<span data-ttu-id="a3506-120">โครงสร้างเรกคอร์ดของรายการที่ถูกส่งกลับประกอบด้วยฟิลด์ **ค่า** ของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="a3506-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="a3506-121">ทุกเรกคอร์ดของรายการที่ถูกส่งกลับประกอบด้วยสตริงย่อยที่สร้างขึ้นในฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="a3506-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="a3506-122">ถ้าอาร์กิวเมนต์ `delimiter` ว่าง รายการใหม่ที่ถูกส่งกลับที่ประกอบด้วยเรกคอร์ดหนึ่งรายการที่มีฟิลด์ **ค่า** ของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="a3506-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="a3506-123">ฟิลด์นี้ประกอบด้วยข้อความป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="a3506-123">This field contains the input text.</span></span>

<span data-ttu-id="a3506-124">ถ้าอาร์กิวเมนต์ `input` ว่างเปล่า จะมีการส่งคืนรายการที่ว่างเปล่าใหม่</span><span class="sxs-lookup"><span data-stu-id="a3506-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="a3506-125">ถ้าไม่สามารถระบุอาร์กิวเมนต์ `input` หรือ `delimiter` (null) จะมีข้อยกเว้นแอปพลิเคชันเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a3506-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="a3506-126">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="a3506-126">Example 1</span></span>

<span data-ttu-id="a3506-127">`SPLIT ("abcd", 3)` ส่งคืนรายการใหม่ที่ประกอบด้วยสองเรกคอร์ดที่มีฟิลด์ **ค่า** ของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="a3506-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="a3506-128">ฟิลด์ **ค่า** ในเรกคอร์ดแรกประกอบด้วยข้อความ **"abc"** และฟิลด์ **ค่า** ในเรกคอร์ดที่สองประกอบด้วยข้อความ **"d"**</span><span class="sxs-lookup"><span data-stu-id="a3506-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a3506-129">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="a3506-129">Example 2</span></span>

<span data-ttu-id="a3506-130">`SPLIT ("XAb aBy", "aB")` ส่งคืนรายการใหม่ที่ประกอบด้วยสามเรกคอร์ดที่มีฟิลด์ **ค่า** ของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="a3506-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="a3506-131">ฟิลด์ **ค่า** ในเรกคอร์ดแรกประกอบด้วยข้อความ **"X"** ฟิลด์ **ค่า** ในเรกคอร์ดที่สองประกอบด้วยข้อความ **"&nbsp;"** และฟิลด์ **ค่า** ในเรกคอร์ดที่สามประกอบด้วยข้อความ **"y"**</span><span class="sxs-lookup"><span data-stu-id="a3506-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="a3506-132">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a3506-132">Additional resources</span></span>

[<span data-ttu-id="a3506-133">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="a3506-133">List functions</span></span>](er-functions-category-list.md)
