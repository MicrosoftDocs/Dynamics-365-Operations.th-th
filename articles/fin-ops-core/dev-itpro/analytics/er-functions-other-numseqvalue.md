---
title: ฟังก์ชัน NUMSEQVALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ NUMSEQVALUE (ER)
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 23dc112651e4425b8020ee5c843509b4df83e810
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563329"
---
# <a name="numseqvalue-er-function"></a><span data-ttu-id="87fa3-103">ฟังก์ชัน NUMSEQVALUE ER</span><span class="sxs-lookup"><span data-stu-id="87fa3-103">NUMSEQVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87fa3-104">ฟังก์ชัน `NUMSEQVALUE` ส่งกลับค่า *สตริง* ที่แสดงถึงค่าที่สร้างขึ้นใหม่ของลำดับหมายเลข ตามลำดับหมายเลข ขอบเขต และรหัสขอบเขตที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="87fa3-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="87fa3-105">รหัสขอบเขตจะเท่ากับรหัสบริษัทที่จัดหาโดยบริบทที่เรียกใช้รูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="87fa3-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="87fa3-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="87fa3-106">Syntax 1</span></span>

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="87fa3-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="87fa3-107">Syntax 2</span></span>

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="87fa3-108">ไวยากรณ์ 3</span><span class="sxs-lookup"><span data-stu-id="87fa3-108">Syntax 3</span></span>

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="87fa3-109">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="87fa3-109">Arguments</span></span>

<span data-ttu-id="87fa3-110">`number sequence code`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="87fa3-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="87fa3-111">ค่าข้อความที่แสดงรหัสของลำดับหมายเลขที่จำเป็นต้องใช้ค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="87fa3-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="87fa3-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="87fa3-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="87fa3-113">ค่า *Int64* ที่แสดงถึงรหัสเรกคอร์ดของเรกคอร์ดในตาราง NumberSequenceTable ที่มีคำนิยามของลำดับหมายเลขที่จำเป็นต้องใช้ค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="87fa3-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="87fa3-114">`scope type`: *ค่า Enum*</span><span class="sxs-lookup"><span data-stu-id="87fa3-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="87fa3-115">ค่าการแจงนับของการแจงนับ **ERExpressionNumberSequenceScopeType** ที่กำหนดขอบเขตของลำดับหมายเลขที่จำเป็นต้องใช้ค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="87fa3-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="87fa3-116">ชนิดขอบเขตที่พร้อมใช้งานจะ **ถูกใช้ร่วมกัน** **นิติบุคคล** และ **บริษัท**</span><span class="sxs-lookup"><span data-stu-id="87fa3-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="87fa3-117">`scope ID`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="87fa3-117">`scope ID`: *String*</span></span>

<span data-ttu-id="87fa3-118">ค่า *สตริง* ที่ระบุขอบเขต ตามชนิดขอบเขตที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="87fa3-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="87fa3-119">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="87fa3-119">Return values</span></span>

<span data-ttu-id="87fa3-120">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="87fa3-120">*String*</span></span>

<span data-ttu-id="87fa3-121">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="87fa3-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="87fa3-122">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="87fa3-122">Usage notes</span></span>

<span data-ttu-id="87fa3-123">สำหรับชนิดขอบข่าย **ที่ใช้ร่วมกัน** ระบุสตริงที่ว่างเป็นรหัสขอบเขต</span><span class="sxs-lookup"><span data-stu-id="87fa3-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="87fa3-124">สำหรับชนิดขอบเขต **บริษัท** และ **นิติบุคคล** ระบุรหัสบริษัทเป็นรหัสขอบเขต</span><span class="sxs-lookup"><span data-stu-id="87fa3-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="87fa3-125">ถ้าคุณระบุสตริงที่ว่างเป็นรหัสขอบเขตสำหรับชนิดขอบเขตนี้ จะมีการใช้รหัสบริษัทปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="87fa3-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="87fa3-126">เมื่อมีการใช้ไวยากรณ์ 1 ลำดับหมายเลขจะถูกร้องขอสำหรับชนิดขอบเขตของ **บริษัท** และรหัสบริษัทจะถูกจัดหาโดยบริบทที่มีการรันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="87fa3-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="87fa3-127">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="87fa3-127">Example 1</span></span>

<span data-ttu-id="87fa3-128">ในรูปแบบ ER ของคุณ คุณสามารถกำหนดแหล่งข้อมูล **AskNumSeq** ของชนิด *พารามิเตอร์ป้อนเข้าของผู้ใช้*</span><span class="sxs-lookup"><span data-stu-id="87fa3-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="87fa3-129">แหล่งข้อมูลนี้อ้างอิงถึงชนิดข้อมูลแบบขยาย (EDT) ของ **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="87fa3-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="87fa3-130">ถัดไป คุณกำหนดแหล่งข้อมูล **NumSeq** ของชนิดของ *ฟิลด์ที่มีการคำนวณ*</span><span class="sxs-lookup"><span data-stu-id="87fa3-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="87fa3-131">แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `NUMSEQVALUE (AskNumSeq)`</span><span class="sxs-lookup"><span data-stu-id="87fa3-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="87fa3-132">เมื่อแหล่งข้อมูล **NumSeq** ถูกเรียก จะส่งกลับค่าที่สร้างขึ้นใหม่ของลำดับหมายเลขที่ระบุไว้ในขณะทำงานโดยการป้อนรหัสในกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="87fa3-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="87fa3-133">มีการร้องขอลำดับหมายเลขสำหรับชนิดขอบเขตของ **บริษัท**</span><span class="sxs-lookup"><span data-stu-id="87fa3-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="87fa3-134">รหัสบริษัทจะถูกจัดหาโดยบริบทที่มีการรันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="87fa3-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="87fa3-135">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="87fa3-135">Example 2</span></span>

<span data-ttu-id="87fa3-136">มีการกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:</span><span class="sxs-lookup"><span data-stu-id="87fa3-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="87fa3-137">แหล่งข้อมูล **LedgerParms** ของชนิด *ตาราง*</span><span class="sxs-lookup"><span data-stu-id="87fa3-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="87fa3-138">แหล่งข้อมูลนี้อ้างถึงตาราง LedgerParameters</span><span class="sxs-lookup"><span data-stu-id="87fa3-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="87fa3-139">แหล่งข้อมูล **NumSeq** ของชนิดของ *ฟิลด์ที่มีการคำนวณ*</span><span class="sxs-lookup"><span data-stu-id="87fa3-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="87fa3-140">แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`</span><span class="sxs-lookup"><span data-stu-id="87fa3-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="87fa3-141">เมื่อมีการเรียกแหล่งข้อมูล **NumSeq** จะส่งกลับค่าที่สร้างขึ้นใหม่ของลำดับหมายเลขที่ถูกตั้งค่าคอนฟิกในพารามิเตอร์บัญชีแยกประเภททั่วไป สำหรับบริษัทที่ให้บริบทที่รันเหนือรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="87fa3-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="87fa3-142">ลำดับหมายเลขนี้ระบุสมุดรายวันโดยไม่ซ้ำกัน และทำหน้าที่เป็นหมายเลขชุดงานที่เชื่อมโยงธุรกรรมร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="87fa3-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="87fa3-143">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="87fa3-143">Example 3</span></span>

<span data-ttu-id="87fa3-144">มีการกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:</span><span class="sxs-lookup"><span data-stu-id="87fa3-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="87fa3-145">แหล่งข้อมูล **enumScope** ของชนิด *การแจงนับ* ของ Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="87fa3-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="87fa3-146">แหล่งข้อมูลนี้อ้างอิงถึงการแจงนับ **ERExpressionNumberSequenceScopeType**</span><span class="sxs-lookup"><span data-stu-id="87fa3-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="87fa3-147">แหล่งข้อมูล **NumSeq** ของชนิดของ *ฟิลด์ที่มีการคำนวณ*</span><span class="sxs-lookup"><span data-stu-id="87fa3-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="87fa3-148">แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`</span><span class="sxs-lookup"><span data-stu-id="87fa3-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="87fa3-149">เมื่อมีการเรียกแหล่งข้อมูล **NumSeq** จะส่งกลับค่าที่สร้างขึ้นใหม่ของลำดับหมายเลข **Gene\_1** ที่ถูกตั้งค่าคอนฟิกสำหรับบริษัทที่ให้บริบทที่รันเหนือรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="87fa3-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87fa3-150">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="87fa3-150">Additional resources</span></span>

[<span data-ttu-id="87fa3-151">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="87fa3-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]