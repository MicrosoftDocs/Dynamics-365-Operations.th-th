---
title: ใช้ฟิลด์ที่กำหนดเองสำหรับแอปมือถือ Microsoft Dynamics 365 Project Timesheet บน iOS และ Android
description: หัวข้อนี้จะให้รูปแบบทั่วไปสำหรับการใช้ส่วนขยายในการใช้ฟิลด์ที่กำหนดเอง
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 19859d8566a8c7840066b2c10c6b08b67f1b83f4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2019
ms.locfileid: "1618007"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="02628-103">ใช้ฟิลด์ที่กำหนดเองสำหรับแอปมือถือ Microsoft Dynamics 365 Project Timesheet บน iOS และ Android</span><span class="sxs-lookup"><span data-stu-id="02628-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02628-104">หัวข้อนี้จะให้รูปแบบทั่วไปสำหรับการใช้ส่วนขยายในการใช้ฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="02628-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="02628-105">จะครอบคลุมหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="02628-105">The following topics are covered:</span></span>

- <span data-ttu-id="02628-106">ชนิดข้อมูลต่างๆ ที่โครงสร้างของฟิลด์ที่กำหนดเองสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="02628-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="02628-107">วิธีการแสดงฟิลด์แบบอ่านอย่างเดียวหรือที่สามารถแก้ไขได้ในรายการแผ่นเวลา และบันทึกค่าที่ผู้ใช้ระบุกลับไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02628-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="02628-108">วิธีการแสดงฟิลด์แบบอ่านอย่างเดียวบนส่วนหัวของแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="02628-109">วิธีการรวมตรรกะทางธุรกิจแบบกำหนดเองอื่นๆ เพื่อป้อนค่าเริ่มต้นในฟิลด์ และทำการตรวจสอบความถูกต้องเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="02628-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="02628-110">ผู้ชม</span><span class="sxs-lookup"><span data-stu-id="02628-110">Audience</span></span>

<span data-ttu-id="02628-111">หัวข้อนี้มีไว้สำหรับนักพัฒนาที่กำลังรวมฟิลด์ที่กำหนดเองของพวกเขาเข้ากับแอพลิเคชันบนมือถือ Microsoft Dynamics 365 Project Timesheet ที่พร้อมใช้งานสำหรับ Apple iOS และ Google Android</span><span class="sxs-lookup"><span data-stu-id="02628-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="02628-112">สมมติฐานคือ ผู้อ่านมีความคุ้นเคยกับการพัฒนา X++ และฟังก์ชันของแผ่นเวลาโครงการ</span><span class="sxs-lookup"><span data-stu-id="02628-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="02628-113">สัญญาข้อมูล – คลาส TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="02628-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="02628-114">คลาส **TSTimesheetCustomField** เป็นคลาสของสัญญาข้อมูล X++ ซึ่งแสดงข้อมูลเกี่ยวกับฟิลด์ที่กำหนดเองสำหรับฟังก์ชันของแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="02628-115">รายการของออบเจ็กต์ของฟิลด์ที่กำหนดเองจะถูกส่งผ่านไปยังทั้งสัญญาข้อมูล TSTimesheetDetails และสัญญาข้อมูล TSTimesheetEntry เพื่อแสดงฟิลด์ที่กำหนดเองในแอปบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="02628-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="02628-116">**TSTimesheetDetails** - สัญญาส่วนหัวของแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="02628-117">**TSTimesheetEntry** - สัญญาของธุรกรรมแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="02628-118">กลุ่มของออบเจ็กต์เหล่านี้ที่มีข้อมูลโครงการเดียวกัน และค่า **timesheetLineRecId** ประกอบด้วยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="02628-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="02628-119">fieldBaseType (ชนิด)</span><span class="sxs-lookup"><span data-stu-id="02628-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="02628-120">คุณสมบัติ **FieldBaseType** บนออบเจ็กต์ **TsTimesheetCustom** กำหนดชนิดของฟิลด์ที่จะปรากฏขึ้นในแอป</span><span class="sxs-lookup"><span data-stu-id="02628-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="02628-121">ค่า **ชนิด** ต่อไปนี้ที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="02628-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="02628-122">มูลค่าชนิด</span><span class="sxs-lookup"><span data-stu-id="02628-122">Types value</span></span> | <span data-ttu-id="02628-123">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02628-123">Type</span></span>              | <span data-ttu-id="02628-124">บันทึกย่อ</span><span class="sxs-lookup"><span data-stu-id="02628-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="02628-125">0</span><span class="sxs-lookup"><span data-stu-id="02628-125">0</span></span>           | <span data-ttu-id="02628-126">สตริง (และ Enum)</span><span class="sxs-lookup"><span data-stu-id="02628-126">String (and Enum)</span></span> | <span data-ttu-id="02628-127">ฟิลด์นี้จะปรากฏเป็นฟิลด์ข้อความ</span><span class="sxs-lookup"><span data-stu-id="02628-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="02628-128">1</span><span class="sxs-lookup"><span data-stu-id="02628-128">1</span></span>           | <span data-ttu-id="02628-129">จำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="02628-129">Integer</span></span>           | <span data-ttu-id="02628-130">ค่าจะแสดงเป็นตัวเลขโดยไม่มีตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="02628-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="02628-131">2</span><span class="sxs-lookup"><span data-stu-id="02628-131">2</span></span>           | <span data-ttu-id="02628-132">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="02628-132">Real</span></span>              | <span data-ttu-id="02628-133">ค่าจะแสดงเป็นตัวเลขที่มีตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="02628-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="02628-134">ถ้าต้องการแสดงมูลค่าจริงเป็นสกุลเงินในแอป ให้ใช้คุณสมบัติ **fieldExtenededType**</span><span class="sxs-lookup"><span data-stu-id="02628-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="02628-135">คุณสามารถใช้คุณสมบัติ **numberOfDecimals** เพื่อตั้งค่าจำนวนของตำแหน่งทศนิยมที่จะแสดง</span><span class="sxs-lookup"><span data-stu-id="02628-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="02628-136">3</span><span class="sxs-lookup"><span data-stu-id="02628-136">3</span></span>           | <span data-ttu-id="02628-137">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="02628-137">Date</span></span>              | <span data-ttu-id="02628-138">รูปแบบวันที่ถูกกำหนดโดยการตั้งค่า **วันที่ เวลา และรูปแบบหมายเลข** ของผู้ใช้ ซึ่งระบุไว้ภายใต้ **การกำหนดลักษณะภาษาและประเทศ/ภูมิภาค** ใน **ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="02628-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="02628-139">4</span><span class="sxs-lookup"><span data-stu-id="02628-139">4</span></span>           | <span data-ttu-id="02628-140">บูลีน</span><span class="sxs-lookup"><span data-stu-id="02628-140">Boolean</span></span>           | |
| <span data-ttu-id="02628-141">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="02628-141">15</span></span>          | <span data-ttu-id="02628-142">GUID</span><span class="sxs-lookup"><span data-stu-id="02628-142">GUID</span></span>              | |
| <span data-ttu-id="02628-143">16</span><span class="sxs-lookup"><span data-stu-id="02628-143">16</span></span>          | <span data-ttu-id="02628-144">Int64</span><span class="sxs-lookup"><span data-stu-id="02628-144">Int64</span></span>             | |

- <span data-ttu-id="02628-145">ถ้าไม่มีคุณสมบัติ **stringOptions** บนออบเจ็กต์ **TSTimesheetCustomField** จะให้ฟิลด์ข้อความอิสระกับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="02628-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="02628-146">คุณสมบัติ **stringLength** สามารถใช้ในการตั้งค่าความยาวของสตริงสูงสุดที่ผู้ใช้สามารถป้อนได้</span><span class="sxs-lookup"><span data-stu-id="02628-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="02628-147">ถ้าให้คุณสมบัติ **stringOptions** บนออบเจ็กต์ **TSTimesheetCustomField** องค์ประกอบรายการเหล่านั้นเป็นค่าเฉพาะที่ผู้ใช้สามารถเลือกได้โดยใช้ปุ่มตัวเลือก (ปุ่ม radio)</span><span class="sxs-lookup"><span data-stu-id="02628-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="02628-148">ในกรณีนี้ ฟิลด์สตริงสามารถทำหน้าที่เป็นค่า enum สำหรับวัตถุประสงค์ของรายการผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="02628-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="02628-149">เมื่อต้องการบันทึกค่าลงในฐานข้อมูลเป็น enum ให้แม็ปค่าสตริงกลับไปยังค่า enum ด้วยตนเอง ก่อนที่คุณจะบันทึกลงในฐานข้อมูลโดยใช้ห่วงโซ่ของคำสั่ง (โปรดดูที่ส่วน "ใช้ห่วงโซ่ของคำสั่งบนคลาส TSTimesheetEntryService เพื่อบันทึกรายการแผ่นเวลาจากแอปกลับไปยังฐานข้อมูล" ในหัวข้อนี้สำหรับตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="02628-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="02628-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="02628-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="02628-151">คุณสามารถใช้คุณสมบัตินี้ในการจัดรูปแบบค่าจริงเป็นสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="02628-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="02628-152">วิธีการนี้สามารถใช้ได้เฉพาะเมื่อค่า **fieldBaseType** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="02628-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="02628-153">**TSCustomFieldExtendedType:ไม่มี** – ไม่มีการนำการจัดรูปแบบไปใช้</span><span class="sxs-lookup"><span data-stu-id="02628-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="02628-154">**TSCustomFieldExtendedType::สกุลเงิน** – จัดรูปแบบค่าเป็นสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="02628-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="02628-155">เมื่อการจัดรูปแบบสกุลเงินเปิดใช้งานอยู่ ฟิลด์ **stringValue** จะสามารถใช้ส่งรหัสสกุลเงินที่ควรจะแสดงในแอป</span><span class="sxs-lookup"><span data-stu-id="02628-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="02628-156">ค่าเป็นค่าแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="02628-156">The value is a read-only value.</span></span>

    <span data-ttu-id="02628-157">ฟิลด์ **realValue** มีจำนวนเงินที่ควรจะถูกบันทึกไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02628-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="02628-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="02628-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="02628-159">คุณสามารถใช้คุณสมบัตินี้เพื่อระบุตำแหน่งฟิลด์ที่กำหนดเองจะปรากฏในแอป</span><span class="sxs-lookup"><span data-stu-id="02628-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="02628-160">**TSCustomFieldSection::ส่วนหัว** – ฟิลด์จะปรากฏในส่วน **ดูรายละเอียดเพิ่มเติม** ในแอป</span><span class="sxs-lookup"><span data-stu-id="02628-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="02628-161">ฟิลด์เหล่านี้เป็นแบบอ่านอย่างเดียวเสมอ</span><span class="sxs-lookup"><span data-stu-id="02628-161">These fields are always read-only.</span></span>
- <span data-ttu-id="02628-162">**TSCustomFieldSection::รายการ** – ฟิลด์จะปรากฏขึ้นหลังจากฟิลด์รายการแบบสำเร็จรูปทั้งหมดในรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="02628-163">ฟิลด์เหล่านี้สามารถแก้ไขได้ หรือเป็นแบบอ่านอย่างเดียว อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="02628-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="02628-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="02628-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="02628-165">คุณสมบัตินี้จะระบุฟิลด์ เมื่อค่าที่แอปให้ถูกบันทึกกลับไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02628-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="02628-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="02628-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="02628-167">คุณสมบัตินี้จะระบุฟิลด์ เมื่อค่าที่แอปให้ถูกบันทึกกลับไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02628-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="02628-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="02628-168">isEditable (NoYes)</span></span>

<span data-ttu-id="02628-169">ตั้งค่าคุณสมบัตินี้เป็น **ใช่** เพื่อระบุว่าฟิลด์ในส่วนรายการแผ่นเวลาควรจะสามารถแก้ไขได้โดยผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="02628-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="02628-170">ตั้งค่าคุณสมบัติเป็น **ไม่** เพื่อทำให้ฟิลด์นี้เป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="02628-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="02628-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="02628-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="02628-172">ตั้งค่าคุณสมบัตินี้เป็น **ใช่** เพื่อระบุว่าฟิลด์ในส่วนรายการแผ่นเวลาควรจะเป็นแบบบังคับ</span><span class="sxs-lookup"><span data-stu-id="02628-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="02628-173">ป้ายชื่อ (str)</span><span class="sxs-lookup"><span data-stu-id="02628-173">label (str)</span></span>

<span data-ttu-id="02628-174">คุณสมบัตินี้จะระบุป้ายชื่อที่แสดงถัดจากฟิลด์ในแอป</span><span class="sxs-lookup"><span data-stu-id="02628-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="02628-175">stringOptions (รายการของสตริง)</span><span class="sxs-lookup"><span data-stu-id="02628-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="02628-176">คุณสมบัตินี้สามารถใช้ได้เฉพาะเมื่อ **fieldBaseType** ถูกตั้งค่าเป็น **สตริง**</span><span class="sxs-lookup"><span data-stu-id="02628-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="02628-177">ถ้ามีการตั้งค่า **stringOptions** ค่าสตริงที่พร้อมใช้งานสำหรับการเลือกผ่านปุ่มตัวเลือก (ปุ่ม radio) จะถูกระบุโดยสตริงในรายการ</span><span class="sxs-lookup"><span data-stu-id="02628-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="02628-178">ถ้าไม่มีการระบุสตริง การให้ป้อนข้อความอิสระในฟิลด์สตริงจะได้รับอนุญาต (โปรดดูที่ส่วน "ใช้ห่วงโซ่ของคำสั่งบนคลาส TSTimesheetEntryService เพื่อบันทึกรายการแผ่นเวลาจากแอปกลับไปยังฐานข้อมูล" ในหัวข้อนี้สำหรับตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="02628-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="02628-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="02628-179">stringLength (int)</span></span>

<span data-ttu-id="02628-180">คุณสมบัตินี้ระบุความยาวสูงสุดสำหรับฟิลด์สตริง</span><span class="sxs-lookup"><span data-stu-id="02628-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="02628-181">สามารถใช้ได้เฉพาะเมื่อ **fieldBaseTyp** ถูกตั้งค่าเป็น **สตริง**</span><span class="sxs-lookup"><span data-stu-id="02628-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="02628-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="02628-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="02628-183">คุณสมบัตินี้จะระบุจำนวนของตำแหน่งทศนิยมที่แสดงสำหรับฟิลด์จริง</span><span class="sxs-lookup"><span data-stu-id="02628-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="02628-184">สามารถใช้ได้เฉพาะเมื่อ **fieldBaseTyp** ถูกตั้งค่าเป็น **จำนวนจริง**</span><span class="sxs-lookup"><span data-stu-id="02628-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="02628-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="02628-185">orderSequence (int)</span></span>

<span data-ttu-id="02628-186">คุณสมบัตินี้ควบคุมใบสั่งที่จะแสดงฟิลด์ที่กำหนดเองในแอป เมื่อมีการระบุฟิลด์ที่กำหนดเองมากกว่าหนึ่งฟิลด์</span><span class="sxs-lookup"><span data-stu-id="02628-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="02628-187">ฟิลด์ที่มีตัวเลขที่ต่ำกว่าจะแสดงขึ้นก่อน</span><span class="sxs-lookup"><span data-stu-id="02628-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="02628-188">booleanValue (บูลีน)</span><span class="sxs-lookup"><span data-stu-id="02628-188">booleanValue (boolean)</span></span>

<span data-ttu-id="02628-189">สำหรับฟิลด์ของชนิด **บูลีน** คุณสมบัตินี้จะส่งค่าบูลีนของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="02628-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="02628-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="02628-190">guidValue (guid)</span></span>

<span data-ttu-id="02628-191">สำหรับฟิลด์ของชนิด **GUID** คุณสมบัตินี้จะส่งค่า Global Unique Identifier (GUID) ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="02628-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="02628-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="02628-192">int64Value (int64)</span></span>

<span data-ttu-id="02628-193">สำหรับฟิลด์ของชนิด **Int64** คุณสมบัตินี้จะส่งค่า Int64 ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="02628-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="02628-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="02628-194">intValue (int)</span></span>

<span data-ttu-id="02628-195">สำหรับฟิลด์ของชนิด **Int** คุณสมบัตินี้จะส่งค่า Int ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="02628-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="02628-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="02628-196">realValue (real)</span></span>

<span data-ttu-id="02628-197">สำหรับฟิลด์ของชนิด **จำนวนจริง** คุณสมบัตินี้จะส่งค่าจำนวนจริงของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="02628-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="02628-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="02628-198">stringValue (str)</span></span>

<span data-ttu-id="02628-199">สำหรับฟิลด์ของชนิด **สตริง** คุณสมบัตินี้จะส่งค่าสตริงของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="02628-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="02628-200">นอกจากนี้ ยังใช้สำหรับฟิลด์ของชนิด **จำนวนจริง** ที่มีการจัดรูปแบบเป็นสกุลเงินด้วย</span><span class="sxs-lookup"><span data-stu-id="02628-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="02628-201">สำหรับฟิลด์เหล่านั้น คุณสมบัตินี้จะถูกใช้ในการส่งรหัสสกุลเงินไปยังแอป</span><span class="sxs-lookup"><span data-stu-id="02628-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="02628-202">dateValue (วันที่)</span><span class="sxs-lookup"><span data-stu-id="02628-202">dateValue (date)</span></span>

<span data-ttu-id="02628-203">สำหรับฟิลด์ของชนิด **วันที่** คุณสมบัตินี้จะส่งค่าวันที่ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="02628-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="02628-204">แสดงและบันทึกฟิลด์ที่กำหนดเองในส่วนของส่วนรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="02628-205">ด้านล่างเป็นภาพหน้าจอจากแอปบนมือถือของการสร้างรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="02628-206">ซึ่งแสดงฟิลด์สำเร็จรูปและฟิลด์ที่กำหนดเองในส่วน "รายการเวลา" ที่เรียกว่า "สตริงการทดสอบ" ด้วยค่า enum ของ "ตัวเลือกที่สอง" ที่กำหนดไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="02628-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![ทดสอบฟิลด์ที่กำหนดเองของสตริงในแอป](media/timesheet-entry.jpg)



<span data-ttu-id="02628-208">ด้านล่างเป็นภาพหน้าจอจากแอปบนมือถือของผู้ใช้ที่เลือกหนึ่งในตัวเลือก enum ที่พร้อมใช้งานสำหรับฟิลด์แบบกำหนดเองของ "สตริงการทดสอบ"</span><span class="sxs-lookup"><span data-stu-id="02628-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="02628-209">ตัวเลือกสองรายการคือ "ตัวเลือกแรก" และ "ตัวเลือกที่สอง" ซึ่งแสดงเป็นปุ่ม radio</span><span class="sxs-lookup"><span data-stu-id="02628-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="02628-210">มีการเลือกตัวเลือกที่สองอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="02628-210">The second option is currently selected.</span></span>

![ปุ่มตัวเลือก (ปุ่ม radio) สำหรับฟิลด์ที่กำหนดเองของสตริงการทดสอบ](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="02628-212">ขยายตาราง TSTimesheetLine เพื่อให้มีฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="02628-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="02628-213">ในสถานการณ์ปกติ อาจเป็นไปได้ว่าข้อมูลสำหรับฟิลด์ที่กำหนดเองในส่วนของการป้อนข้อมูลแผ่นเวลาจะถูกบันทึกไปยังตาราง TSTimesheetLine</span><span class="sxs-lookup"><span data-stu-id="02628-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="02628-214">อย่างไรก็ตาม คุณสามารถใช้ตารางอื่นๆ ได้ ถ้าสามารถดึงข้อมูลได้โดยขึ้นอยู่กับเรกคอร์ด TSTimesheetTrans ที่ระบุ หรือถ้าไม่มีบริบทของเรกคอร์ดเฉพาะ (ตัวอย่างเช่น ถ้ามีการตั้งค่าฟิลด์เป็นแบบอ่านอย่างเดียวในพารามิเตอร์โครงการ)</span><span class="sxs-lookup"><span data-stu-id="02628-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="02628-215">โปรดสังเกตว่าฟิลด์ที่กำหนดเองไม่จำเป็นต้องมีเรกคอร์ดฐานข้อมูลสำรองใดๆ</span><span class="sxs-lookup"><span data-stu-id="02628-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="02628-216">สามารถสร้างขึ้นโดยยึดตามตรรกะ X++ แบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="02628-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="02628-217">วิธีการนี้อาจเป็นประโยชน์ในสถานการณ์แบบอ่านอย่างเดียว (โปรดดูที่ส่วน "ใช้ห่วงโซ่ของคำสั่งบนคลาส TSTimesheetDetails วิธีการ buildCustomFieldListForHeader ในการกรอกข้อมูลในรายละเอียดแผ่นเวลา" สำหรับตัวอย่างของค่าฟิลด์แบบกำหนดเองที่สร้างขึ้นแบบไดนามิก)</span><span class="sxs-lookup"><span data-stu-id="02628-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="02628-218">ด้านล่างเป็นภาพหน้าจอจาก Visual Studio ของ Application Object Tree</span><span class="sxs-lookup"><span data-stu-id="02628-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="02628-219">ซึ่งแสดงส่วนขยายของตาราง TSTimesheetLine ที่มีฟิลด์ TestLineString ที่เพิ่มเป็นฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="02628-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![สตริงรายการ](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="02628-221">ใช้ห่วงโซ่ของคำสั่งในวิธีการ buildCustomFieldList ของคลาส TSTimesheetSettings เพื่อแสดงฟิลด์ในส่วนของการป้อนข้อมูลแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="02628-222">รหัสนี้จะควบคุมการตั้งค่าการแสดงผลสำหรับฟิลด์ในแอป</span><span class="sxs-lookup"><span data-stu-id="02628-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="02628-223">ตัวอย่างเช่น จะควบคุมชนิดของฟิลด์ ป้ายชื่อ ไม่ว่าฟิลด์เป็นฟิลด์บังคับหรือไม่ และส่วนใดของฟิลด์ที่จะปรากฏด้านใน</span><span class="sxs-lookup"><span data-stu-id="02628-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="02628-224">ตัวอย่างต่อไปนี้แสดงฟิลด์สตริงบนรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="02628-225">ฟิลด์นี้มีสองตัวเลือก **ตัวเลือกแรก** และ **ตัวเลือกที่สอง** ซึ่งพร้อมใช้งานผ่านปุ่มตัวเลือก (ปุ่ม radio)</span><span class="sxs-lookup"><span data-stu-id="02628-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="02628-226">ฟิลด์ในแอปเชื่อมโยงกับฟิลด์ **TestLineString** ซึ่งถูกเพิ่มลงในตาราง TSTimesheetLine</span><span class="sxs-lookup"><span data-stu-id="02628-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="02628-227">หมายเหตุ การใช้ของวิธีการ **TSTimesheetCustomField::newFromMetatdata()** เพื่อทำให้การเริ่มต้นคุณสมบัติฟิลด์แบบกำหนดเองเป็นไปได้ง่ายขึ้น: **fieldBaseType** **tableName** **fieldname** **label** **isEditable** **isMandatory** **stringLength** และ **numberOfDecimals**</span><span class="sxs-lookup"><span data-stu-id="02628-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="02628-228">นอกจากนี้ คุณยังสามารถตั้งค่าพารามิเตอร์เหล่านี้ด้วยตนเองได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="02628-228">You can also set these parameters manually, as you prefer.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="02628-229">ใช้ห่วงโซ่ของคำสั่งในวิธีการ buildCustomFieldListForEntry ของคลาส TSTimesheetEntry เพื่อป้อนค่าในการป้อนข้อมูลแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="02628-230">วิธีการ **buildCustomFieldListForEntry** ถูกใช้ในการป้อนค่าในรายการแผ่นเวลาที่บันทึกไว้ในแอปบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="02628-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="02628-231">ใช้เรกคอร์ด TSTimesheetTrans เป็นพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="02628-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="02628-232">สามารถใช้ฟิลด์จากเรกคอร์ดนั้นเพื่อกรอกค่าฟิลด์ที่กำหนดเองในแอป</span><span class="sxs-lookup"><span data-stu-id="02628-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="02628-233">ใช้ห่วงโซ่ของคำสั่งบนคลาส TSTimesheetEntryService เพื่อบันทึกรายการแผ่นเวลาจากแอปกลับไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02628-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="02628-234">เมื่อต้องการบันทึกฟิลด์ที่กำหนดเองกลับไปยังฐานข้อมูลที่ใช้งานโดยทั่วไป คุณต้องขยายวิธีหลายวิธีดังนี้:</span><span class="sxs-lookup"><span data-stu-id="02628-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="02628-235">วิธีการ **timesheetLineNeedsUpdating** ถูกใช้ในการกำหนดว่ามีการเปลี่ยนแปลงเรกคอร์ดรายการโดยผู้ใช้ในแอป และต้องถูกบันทึกไปยังฐานข้อมูลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="02628-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="02628-236">ถ้าประสิทธิภาพไม่เกี่ยวข้อง วิธีการนี้สามารถถูกทำให้ได้ง่ายขึ้นได้เพื่อให้ส่งคืน **จริง** เสมอ</span><span class="sxs-lookup"><span data-stu-id="02628-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="02628-237">วิธีการ **populateTimesheetLineFromEntryDuringCreate** และ **populateTimesheetLineFromEntryDuringUpdate** สามารถขยายเพื่อให้ป้อนค่าในเรกคอร์ดฐานข้อมูล TSTimesheetLine จากเรกคอร์ดสัญญาข้อมูล TSTimesheetEntry ที่ให้</span><span class="sxs-lookup"><span data-stu-id="02628-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="02628-238">ในตัวอย่างต่อไปนี้ โปรดสังเกตวิธีการที่การแม็ประหว่างฟิลด์ฐานข้อมูลและฟิลด์รายการถูกดำเนินการด้วยตนเองโดยใช้รหัส X++</span><span class="sxs-lookup"><span data-stu-id="02628-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="02628-239">นอกจากนี้ ยังสามารถขยายวิธีการ **populateTimesheetWeekFromEntry** ได้ ถ้าฟิลด์แบบกำหนดเองที่ถูกแม็ปไปยังออบเจ็กต์ **TSTimesheetEntry** ต้องเขียนกลับไปยังตารางฐานข้อมูล TSTimesheetLineweek</span><span class="sxs-lookup"><span data-stu-id="02628-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="02628-240">ตัวอย่างต่อไปนี้จะบันทึกค่า **firstOption** หรือ **secondOption** ที่ผู้ใช้เลือกไปยังฐานข้อมูลเป็นค่าสตริงดิบ</span><span class="sxs-lookup"><span data-stu-id="02628-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="02628-241">ถ้าฟิลด์ฐานข้อมูลเป็นฟิลด์ของชนิด **Enum** ค่าเหล่านั้นอาจถูกแม็ปด้วยตนเองไปยังค่า Enum แล้วถูกบันทึกไปยังฟิลด์ Enum บนตารางฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02628-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="02628-242">แสดงฟิลด์ที่กำหนดเองในส่วนของส่วนหัวรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="02628-243">ด้านล่างเป็นภาพหน้าจอจากแอปมือถือของผู้ใช้ที่ดูแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="02628-244">มีการเลือกปุ่ม "ข้อมูลเพิ่มเติม" ในมุมขวาด้านบนเพื่อแสดงตัวเลือก "ดูรายละเอียดเพิ่มเติม"</span><span class="sxs-lookup"><span data-stu-id="02628-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![ดูคำสั่งในรายละเอียดเพิ่มเติม](media/show-more.png)



<span data-ttu-id="02628-246">ด้านล่างเป็นภาพหน้าจอจากแอปมือถือที่แสดงส่วน "เพิ่มเติม" ของแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="02628-247">ฟิลด์แบบกำหนดเองที่เรียกว่า "อัตราการใช้ประโยชน์ของแผ่นเวลานี้ (ฟิลด์แบบกำหนดเองที่คำนวณได้)" ถูกเพิ่มลงในส่วนของส่วนหัวของแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="02628-248">มีการตั้งค่าแบบอ่านอย่างเดียวของ "0.667" บนฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="02628-248">A read-only value of "0.667" is set on the custom field.</span></span>

![ส่วนเพิ่มเติม](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="02628-250">ขยายตาราง TSTimesheetTable เพื่อให้มีฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="02628-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="02628-251">ในสถานการณ์ปกติ อาจเป็นไปได้ว่าข้อมูลสำหรับฟิลด์ที่กำหนดเองในส่วนของส่วนหัวจะถูกดึงข้อมูลจากตาราง TSTimesheetHeader</span><span class="sxs-lookup"><span data-stu-id="02628-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="02628-252">อย่างไรก็ตาม คุณสามารถใช้ตารางอื่นๆ ได้ ถ้าสามารถดึงข้อมูลได้โดยขึ้นอยู่กับเรกคอร์ด TSTimesheetTable ที่ระบุ หรือถ้าไม่มีบริบทของเรกคอร์ดเฉพาะ (ตัวอย่างเช่น ถ้ามีการตั้งค่าฟิลด์เป็นแบบอ่านอย่างเดียวในพารามิเตอร์โครงการ)</span><span class="sxs-lookup"><span data-stu-id="02628-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="02628-253">โปรดสังเกตว่าฟิลด์ที่กำหนดเองไม่จำเป็นต้องมีเรกคอร์ดฐานข้อมูลสำรองใดๆ</span><span class="sxs-lookup"><span data-stu-id="02628-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="02628-254">สามารถสร้างขึ้นโดยยึดตามตรรกะ X++ แบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="02628-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="02628-255">ตัวอย่างต่อจากนี้จะแสดงวิธีการนี้</span><span class="sxs-lookup"><span data-stu-id="02628-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="02628-256">ฟิลด์ในส่วนในส่วนหัวจะเป็นแบบอ่านอย่างเดียวในแอปเสมอ</span><span class="sxs-lookup"><span data-stu-id="02628-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="02628-257">ใช้ห่วงโซ่ของคำสั่งในวิธีการ buildCustomFieldList ของคลาส TSTimesheetSettings เพื่อแสดงฟิลด์ในส่วนของส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="02628-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="02628-258">รหัสนี้จะควบคุมการตั้งค่าการแสดงผลสำหรับฟิลด์ในแอป</span><span class="sxs-lookup"><span data-stu-id="02628-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="02628-259">ตัวอย่างเช่น จะควบคุมชนิดของฟิลด์ ป้ายชื่อ ไม่ว่าฟิลด์เป็นฟิลด์บังคับหรือไม่ และส่วนใดของฟิลด์ที่จะปรากฏด้านใน</span><span class="sxs-lookup"><span data-stu-id="02628-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="02628-260">ตัวอย่างต่อไปนี้จะแสดงค่าที่คำนวณได้ในส่วนของส่วนหัวในแอป</span><span class="sxs-lookup"><span data-stu-id="02628-260">The following example shows a computed value in the header section in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="02628-261">ใช้ห่วงโซ่ของคำสั่งในวิธีการ buildCustomFieldListForHeader ของคลาส TSTimesheetDetails เพื่อกรอกข้อมูลในรายละเอียดแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="02628-262">วิธีการ **buildCustomFieldListForHeader** ถูกใช้ในการกรอกข้อมูลรายละเอียดส่วนหัวของแผ่นเวลาในแอปบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="02628-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="02628-263">ซึ่งใช้เรกคอร์ด TSTimesheetTable เป็นพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="02628-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="02628-264">สามารถใช้ฟิลด์จากเรกคอร์ดนั้นเพื่อกรอกค่าฟิลด์ที่กำหนดเองในแอป</span><span class="sxs-lookup"><span data-stu-id="02628-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="02628-265">ตัวอย่างต่อไปนี้ไม่ได้อ่านค่าใดๆ จากฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02628-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="02628-266">แต่จะใช้ตรรกะ X++ เพื่อสร้างค่าที่มีการคำนวณซึ่งจะแสดงในแอปแทน</span><span class="sxs-lookup"><span data-stu-id="02628-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="02628-267">โอกาสของความสามารถในการตั้งค่าคอนฟิก/ความสามารถในการขยายอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="02628-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="02628-268">การเพิ่มการตรวจสอบความถูกต้องเพิ่มเติมสำหรับแอป</span><span class="sxs-lookup"><span data-stu-id="02628-268">Adding additional validation for the app</span></span>

<span data-ttu-id="02628-269">ตรรกะที่มีอยู่สำหรับฟังก์ชันแผ่นเวลาที่ระดับฐานข้อมูลจะยังคงทำงานตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="02628-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="02628-270">เมื่อต้องการขัดจังหวะความสมบูรณ์ของการบันทึกหรือส่งการดำเนินงาน และแสดงข้อความแสดงข้อผิดพลาดที่ระบุ คุณสามารถเพิ่ม **ส่งข้อผิดพลาด ("ส่งข้อความไปยังผู้ใช้")** ไปยังรหัสผ่านห่วงโซ่ของส่วนขยายคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="02628-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="02628-271">ต่อไปนี้เป็นตัวอย่างสามรายการของวิธีการที่สามารถขยายได้ซึ่งมีประโยชน์:</span><span class="sxs-lookup"><span data-stu-id="02628-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="02628-272">ถ้า **validateWrite** บนตาราง TSTimesheetLine ส่งคืน **เท็จ** ระหว่างการดำเนินงานบันทึกสำหรับรายการแผ่นเวลา ข้อความแสดงข้อผิดพลาดจะถูกแสดงในแอปบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="02628-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="02628-273">ถ้า **validateSubmit** บนตาราง TSTimesheetTable ส่งคืน **เท็จ** ระหว่างการส่งแผ่นเวลาในแอป ข้อความแสดงข้อผิดพลาดจะถูกแสดงไปยังผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="02628-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="02628-274">ตรรกะที่กรอกข้อมูลในฟิลด์ (ตัวอย่างเช่น **คุณสมบัติของรายการ**) ในระหว่างวิธีการ **แทรก** บนตาราง TSTimesheetLine จะยังคงรันอยู่</span><span class="sxs-lookup"><span data-stu-id="02628-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="02628-275">การซ่อนและการทำเครื่องหมายฟิลด์สำเร็จรูปเป็นแบบอ่านอย่างเดียวผ่านทางการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="02628-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="02628-276">จากพารามิเตอร์โครงการ คุณสามารถทำให้ฟิลด์สำเร็จรูปเป็นแบบอ่านอย่างเดียว หรือถูกซ่อนอยู่ในแอปบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="02628-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="02628-277">ตั้งค่าตัวเลือกในส่วน **แผ่นเวลาสำหรับมือถือ** บนแท็บ **แผ่นเวลา** ของหน้า **พารามิเตอร์การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="02628-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![พารามิเตอร์โครงการ](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="02628-279">การเปลี่ยนกิจกรรมที่พร้อมใช้งานสำหรับการเลือกผ่านส่วนขยาย</span><span class="sxs-lookup"><span data-stu-id="02628-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="02628-280">กิจกรรมที่พร้อมใช้งานสำหรับการเลือกสำหรับโครงการจะถูกกรอกข้อมูลโดยผ่านวิธีการ **getActivitiesForProject()** และ **getActivityQuery()** ในคลาส **TsTimesheetProjectService**</span><span class="sxs-lookup"><span data-stu-id="02628-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="02628-281">คุณสามารถใช้ห่วงโซ่ของคำสั่งเพื่อเปลี่ยนลักษณะการทำงานนี้ให้ตรงกับสถานการณ์จำลองทางธุรกิจของคุณ สำหรับกิจกรรมที่พร้อมใช้งานสำหรับการเลือกสำหรับโครงการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="02628-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="02628-282">การป้อนประเภทโครงการเริ่มต้นในรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="02628-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="02628-283">รายการของประเภทโครงการเริ่มต้นในรายการแผ่นเวลาจะเกิดขึ้นในสามระดับ</span><span class="sxs-lookup"><span data-stu-id="02628-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="02628-284">คุณสามารถใช้ห่วงโซ่ของคำสั่งเพื่อขยายลักษณะการทำงานที่ระดับใดๆ เหล่านี้หรือทั้งหมด เพื่อให้เกิดลักษณะการทำงานที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="02628-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="02628-285">มีการใช้ลำดับชั้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="02628-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="02628-286">แอปพยายามที่จะใส่ประเภทเริ่มต้นจากทรัพยากรโครงการ</span><span class="sxs-lookup"><span data-stu-id="02628-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="02628-287">ประเภทเริ่มต้นนี้ถูกตั้งค่าในวิธีการ **getCurrentUserResource** และ **getDelegatedResourcesForCurrentUser** ในคลาส **TSTimesheetSettingsService**</span><span class="sxs-lookup"><span data-stu-id="02628-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="02628-288">ถ้าไม่ได้ระบุประเภทเริ่มต้นที่ระดับทรัพยากรโครงการ แอปจะพยายามดึงข้อมูลจากกิจกรรมโครงการ</span><span class="sxs-lookup"><span data-stu-id="02628-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="02628-289">ประเภทเริ่มต้นนี้ถูกตั้งค่าวิธีการ **getActivitiesForProject** ในคลาส **TSTimesheetProjectService**</span><span class="sxs-lookup"><span data-stu-id="02628-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="02628-290">ถ้าไม่ได้ระบุประเภทเริ่มต้นที่ระดับกิจกรรมโครงการ ประเภทเริ่มต้นจะมาจากพารามิเตอร์โครงการ</span><span class="sxs-lookup"><span data-stu-id="02628-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="02628-291">ประเภทเริ่มต้นนี้ถูกตั้งค่าในวิธีการ **getProjectDetailsbyRule** ในคลาส **TSTimesheetProjectService**</span><span class="sxs-lookup"><span data-stu-id="02628-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
