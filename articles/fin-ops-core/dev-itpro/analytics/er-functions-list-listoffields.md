---
title: ฟังก์ชัน LISTOFFIELDS ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) LISTOFFIELDS
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
ms.openlocfilehash: 0d51b59c437bd216c6d229546136bb604239fa92
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042009"
---
# <span data-ttu-id="46e66-103"><a name="LISTOFFIELDS">ฟังก์ชัน LISTOFFIELDS ER</a></span><span class="sxs-lookup"><span data-stu-id="46e66-103"><a name="LISTOFFIELDS">LISTOFFIELDS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46e66-104">ฟังก์ชัน `LISTOFFIELDS` ส่งกลับค่า *รายการเรกคอร์ด* ที่สร้างขึ้นตามโครงสร้างของอาร์กิวเมนต์ที่ระบุของชนิด *การแจงนับ* หรือ *คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="46e66-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="46e66-105">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="46e66-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="46e66-106">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="46e66-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="46e66-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="46e66-107">Arguments</span></span>

<span data-ttu-id="46e66-108">`path`: การอ้างอิงแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="46e66-108">`path`: Data source reference</span></span>

<span data-ttu-id="46e66-109">พาธอ้างอิงที่ถูกต้องของแหล่งข้อมูลของหนึ่งในชนิดข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="46e66-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="46e66-110">การแจงนับแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="46e66-110">Model enumeration</span></span>
- <span data-ttu-id="46e66-111">การแจงนับรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="46e66-111">Format enumeration</span></span>
- <span data-ttu-id="46e66-112">การแจงนับแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="46e66-112">Application enumeration</span></span>
- <span data-ttu-id="46e66-113">คอนเทนเนอร์ (เรกคอร์ด)</span><span class="sxs-lookup"><span data-stu-id="46e66-113">Container (record)</span></span>

<span data-ttu-id="46e66-114">`language`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="46e66-114">`language`: *String*</span></span>

<span data-ttu-id="46e66-115">ข้อความที่แสดงถึงรหัสภาษา</span><span class="sxs-lookup"><span data-stu-id="46e66-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="46e66-116">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="46e66-116">Return values</span></span>

<span data-ttu-id="46e66-117">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="46e66-117">*Record list*</span></span>

<span data-ttu-id="46e66-118">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="46e66-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="46e66-119">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="46e66-119">Usage notes</span></span>

<span data-ttu-id="46e66-120">รายการที่สร้างขึ้นประกอบด้วยเรกคอร์ดที่มีฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="46e66-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="46e66-121">**ชื่อ** (ชนิดข้อมูล *สตริง*)</span><span class="sxs-lookup"><span data-stu-id="46e66-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="46e66-122">**ป้ายกำกับ** (ชนิดข้อมูล *สตริง*)</span><span class="sxs-lookup"><span data-stu-id="46e66-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="46e66-123">**คำอธิบาย** (ชนิดข้อมูล *สตริง*)</span><span class="sxs-lookup"><span data-stu-id="46e66-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="46e66-124">**IsTranslated** (ชนิดข้อมูล *บูลีน*)</span><span class="sxs-lookup"><span data-stu-id="46e66-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="46e66-125">ถ้าอาร์กิวเมนต์ `path` อ้างอิงถึงแหล่งข้อมูลของชนิด *คอนเทนเนอร์ (Record)* สำหรับทุกฟิลด์ของเรกคอร์ดคอนเทนเนอร์ที่อ้างอิง เรกคอร์ดใหม่จะถูกเพิ่มลงในรายการที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="46e66-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="46e66-126">สำหรับทุกเรกคอร์ดที่สร้างขึ้น ฟิลด์ **ชื่อ** จะส่งกลับชื่อของฟิลด์ของเรกคอร์ดคอนเทนเนอร์ที่อ้างอิงที่มีการสร้างเร็กคอร์ดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="46e66-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="46e66-127">ถ้าอาร์กิวเมนต์ `path` อ้างอิงถึงแหล่งข้อมูลของชนิด *การแจงนับ* สำหรับทุกค่าการแจงนับของการแจงนับที่อ้างอิง เรกคอร์ดใหม่จะถูกเพิ่มลงในรายการที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="46e66-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="46e66-128">สำหรับทุกเรกคอร์ดที่ถูกสร้าง ฟิลด์ **ชื่อ** จะส่งกลับค่าของการแจงนับอ้างอิงที่มีการสร้างเร็กคอร์ดปัจจุบัน ฟิลด์ **คำอธิบาย** ส่งกลับคำอธิบายของการแจงนับนั้น และฟิลด์ **ป้ายชื่อ** ส่งกลับป้ายชื่อของการแจงนับนั้น</span><span class="sxs-lookup"><span data-stu-id="46e66-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="46e66-129">ขณะรันไทม์เมื่อมีใช้ไวยากรณ์ 1 ฟิลด์ **ป้ายชื่อ** และ **คำอธิบาย** จะต้องส่งคืนค่าที่ขึ้นอยู่กับการตั้งค่าภาษาของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่กำลังทำงานอยู่:</span><span class="sxs-lookup"><span data-stu-id="46e66-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="46e66-130">ถ้าป้ายชื่อและคำอธิบายสำหรับภาษาที่ร้องขอพร้อมใช้งานฟิลด์ **ป้ายชื่อ** และ **คำอธิบาย** จะส่งกลับค่าที่เป็นไปตามภาษา และฟิลด์ **IsTranslated** ส่งคืนเป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="46e66-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="46e66-131">ถ้าป้ายชื่อและคำอธิบายสำหรับภาษาที่ร้องขอไม่พร้อมใช้งาน ฟิลด์ **ป้ายชื่อ** และ **คำอธิบาย** จะส่งกลับค่าที่เป็นไปตามภาษาเริ่มต้น **EN-US** และฟิลด์ **IsTranslated** ส่งคืนเป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="46e66-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="46e66-132">ขณะรันไทม์เมื่อมีใช้ไวยากรณ์ 2 ฟิลด์ **ป้ายชื่อ** และ **คำอธิบาย** จะต้องส่งคืนค่าที่ขึ้นอยู่กับการตั้งค่าภาษาที่ระบุเป็นอาร์กิวเมนต์รองของฟังก์ชันที่เรียกใช้:</span><span class="sxs-lookup"><span data-stu-id="46e66-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="46e66-133">ถ้าป้ายชื่อและคำอธิบายสำหรับภาษาที่ร้องขอพร้อมใช้งานฟิลด์ **ป้ายชื่อ** และ **คำอธิบาย** จะส่งกลับค่าที่เป็นไปตามภาษา และฟิลด์ **IsTranslated** ส่งคืนเป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="46e66-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="46e66-134">ถ้าป้ายชื่อและคำอธิบายสำหรับภาษาที่ร้องขอไม่พร้อมใช้งาน ฟิลด์ **ป้ายชื่อ** และ **คำอธิบาย** จะส่งกลับค่าที่เป็นไปตามภาษา **EN-US** และฟิลด์ **IsTranslated** ส่งคืนเป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="46e66-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="46e66-135">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="46e66-135">Example 1</span></span>

<span data-ttu-id="46e66-136">ในแผนภาพต่อไปนี้ การแจงนับถูกนำมาใช้ในแบบจำลองข้อมูล ER</span><span class="sxs-lookup"><span data-stu-id="46e66-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="46e66-137">ภาพประกอบต่อไปนี้แสดงรายละเอียดเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="46e66-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="46e66-138">การแจงนับแบบจำลองถูกใส่ลงในรายงานเป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="46e66-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="46e66-139">นิพจน์ ER ใช้การแจงนับแบบจำลองเป็นพารามิเตอร์ของฟังก์ชัน `LISTOFFIELDS`</span><span class="sxs-lookup"><span data-stu-id="46e66-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="46e66-140">แหล่งข้อมูลของชนิด *รายการเรกคอร์ด* ถูกแทรกลงในรายงานโดยใช้นิพจน์ ER ที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="46e66-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="46e66-141">ตัวอย่างต่อไปนี้แสดงองค์ประกอบรูปแบบ ER ที่ผูกอยู่กับแหล่งข้อมูลของ *ชนิดรายการเรกคอร์ด* ที่ถูกสร้างโดยใช้ฟังก์ชัน `LISTOFFIELDS`</span><span class="sxs-lookup"><span data-stu-id="46e66-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="46e66-142">ภาพประกอบต่อไปนี้แสดงผลลัพธ์ เมื่อมีการรันรูปแบบที่มีการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="46e66-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="46e66-143">โดยสอดคล้องกับการตั้งค่าภาษาของ **FILE** หลักและองค์ประกอบรูปแบบ **FOLDER** ข้อความที่แปลสำหรับป้ายชื่อและคำอธิบายจะถูกป้อนลงในผลลัพธ์ของรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="46e66-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="46e66-144">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="46e66-144">Example 2</span></span>

<span data-ttu-id="46e66-145">คุณใช้ชนิดแหล่งข้อมูล *ฟิลด์ที่คำนวณได้* เพื่อตั้งค่าคอนฟิกแหล่งข้อมูล **enumType\_de** และ **enumType\_deCH** สำหรับการแจงนับแบบจำลองข้อมูล **enumType**</span><span class="sxs-lookup"><span data-stu-id="46e66-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="46e66-146">**enumType\_เดอ** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="46e66-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="46e66-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="46e66-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="46e66-148">ในกรณีนี้ คุณสามารถใช้นิพจน์ต่อไปนี้ในการเรียกใช้ป้ายชื่อของค่าการแจงนับในภาษาเยอรมันสวิสได้ ถ้าการแปลนี้พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="46e66-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="46e66-149">ถ้าไม่มีการแปลภาษาเยอรมันสวิส ป้ายชื่อจะอยู่ในภาษาเยอรมัน</span><span class="sxs-lookup"><span data-stu-id="46e66-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="46e66-150">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="46e66-150">Additional resources</span></span>

[<span data-ttu-id="46e66-151">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="46e66-151">List functions</span></span>](er-functions-category-list.md)
