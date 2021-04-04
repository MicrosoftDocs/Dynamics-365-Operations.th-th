---
title: ฟังก์ชัน ER SPLIT
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SPLIT
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 806a0995f0c138f4e80396bb993bc6f41bc7c827
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567353"
---
# <a name="split-er-function"></a><span data-ttu-id="1080c-103">ฟังก์ชัน ER SPLIT</span><span class="sxs-lookup"><span data-stu-id="1080c-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1080c-104">ฟังก์ชัน `SPLIT` แบ่งค่าสตริงการป้อนที่ระบุลงในสตริงย่อยและส่งกลับผลลัพธ์เป็นค่า *รายการเรกคอร์ด* ใหม่</span><span class="sxs-lookup"><span data-stu-id="1080c-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="1080c-105">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="1080c-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="1080c-106">ไวยากรณ์นี้แบ่งสตริงที่ระบุเป็นสตริงย่อยซึ่งมีความยาวที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1080c-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="1080c-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="1080c-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="1080c-108">ไวยากรณ์นี้ใช้แบ่งสตริงย่อยที่ระบุออกเป็นสตริงย่อยตามตั่วคั่นที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1080c-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="1080c-109">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="1080c-109">Arguments</span></span>

<span data-ttu-id="1080c-110">`input`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1080c-110">`input`: *String*</span></span>

<span data-ttu-id="1080c-111">ข้อความที่จะแบ่ง</span><span class="sxs-lookup"><span data-stu-id="1080c-111">The text to split.</span></span>

<span data-ttu-id="1080c-112">`length`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="1080c-112">`length`: *Integer*</span></span>

<span data-ttu-id="1080c-113">ความยาวสูงสุดของสตริงย่อยเดียว</span><span class="sxs-lookup"><span data-stu-id="1080c-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="1080c-114">`delimiter`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1080c-114">`delimiter`: *String*</span></span>

<span data-ttu-id="1080c-115">ตัวคั่นที่ใช้ในการแยกสตริงย่อย</span><span class="sxs-lookup"><span data-stu-id="1080c-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="1080c-116">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="1080c-116">Return values</span></span>

<span data-ttu-id="1080c-117">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="1080c-117">*Record list*</span></span>

<span data-ttu-id="1080c-118">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="1080c-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1080c-119">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1080c-119">Usage notes</span></span>

<span data-ttu-id="1080c-120">โครงสร้างเรกคอร์ดของรายการที่ถูกส่งกลับประกอบด้วยฟิลด์ **ค่า** ของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1080c-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="1080c-121">ทุกเรกคอร์ดของรายการที่ถูกส่งกลับประกอบด้วยสตริงย่อยที่สร้างขึ้นในฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="1080c-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="1080c-122">ถ้าอาร์กิวเมนต์ `delimiter` ว่าง รายการใหม่ที่ถูกส่งกลับที่ประกอบด้วยเรกคอร์ดหนึ่งรายการที่มีฟิลด์ **ค่า** ของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1080c-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="1080c-123">ฟิลด์นี้ประกอบด้วยข้อความป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="1080c-123">This field contains the input text.</span></span>

<span data-ttu-id="1080c-124">ถ้าอาร์กิวเมนต์ `input` ว่างเปล่า จะมีการส่งคืนรายการที่ว่างเปล่าใหม่</span><span class="sxs-lookup"><span data-stu-id="1080c-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="1080c-125">ถ้าไม่สามารถระบุอาร์กิวเมนต์ `input` หรือ `delimiter` (null) จะมีข้อยกเว้นแอปพลิเคชันเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="1080c-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="1080c-126">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="1080c-126">Example 1</span></span>

<span data-ttu-id="1080c-127">`SPLIT ("abcd", 3)` ส่งคืนรายการใหม่ที่ประกอบด้วยสองเรกคอร์ดที่มีฟิลด์ **ค่า** ของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1080c-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="1080c-128">ฟิลด์ **ค่า** ในเรกคอร์ดแรกประกอบด้วยข้อความ **"abc"** และฟิลด์ **ค่า** ในเรกคอร์ดที่สองประกอบด้วยข้อความ **"d"**</span><span class="sxs-lookup"><span data-stu-id="1080c-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1080c-129">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="1080c-129">Example 2</span></span>

<span data-ttu-id="1080c-130">`SPLIT ("XAb aBy", "aB")` ส่งคืนรายการใหม่ที่ประกอบด้วยสามเรกคอร์ดที่มีฟิลด์ **ค่า** ของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1080c-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="1080c-131">ฟิลด์ **ค่า** ในเรกคอร์ดแรกประกอบด้วยข้อความ **"X"** ฟิลด์ **ค่า** ในเรกคอร์ดที่สองประกอบด้วยข้อความ **"&nbsp;"** และฟิลด์ **ค่า** ในเรกคอร์ดที่สามประกอบด้วยข้อความ **"y"**</span><span class="sxs-lookup"><span data-stu-id="1080c-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="1080c-132">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1080c-132">Additional resources</span></span>

[<span data-ttu-id="1080c-133">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="1080c-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]