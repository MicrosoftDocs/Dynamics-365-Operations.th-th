---
title: ชนิดข้อมูลพื้นฐานที่ได้รับการสนับสนุนสําหรับสูตรการรายงานทางอิเล็กทรอนิกส์
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับชนิดข้อมูลพื้นฐานที่รองรับในสูตรการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d5e6bb5e070ebbcdb7e99b1b70010acd5fca5ac
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224117"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a><span data-ttu-id="d811c-103">ชนิดข้อมูลพื้นฐานที่ได้รับการสนับสนุนสําหรับสูตรการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d811c-103">Supported primitive data types for Electronic reporting formulas</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d811c-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับชนิดข้อมูลพื้นฐานที่รองรับในนิพจ [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md)</span><span class="sxs-lookup"><span data-stu-id="d811c-104">This topic provides information about the primitive data types that are supported in [Electronic reporting (ER)](general-electronic-reporting.md) expressions.</span></span> <span data-ttu-id="d811c-105">นี่คือรายการของชนิดข้อมูลพื้นฐาน:</span><span class="sxs-lookup"><span data-stu-id="d811c-105">Here is a list of the primitive data types:</span></span>

- [<span data-ttu-id="d811c-106">แบบบูลีน</span><span class="sxs-lookup"><span data-stu-id="d811c-106">boolean</span></span>](#boolean)
- [<span data-ttu-id="d811c-107">วันที่</span><span class="sxs-lookup"><span data-stu-id="d811c-107">date</span></span>](#date)
- [<span data-ttu-id="d811c-108">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d811c-108">datetime</span></span>](#datetime)
- [<span data-ttu-id="d811c-109">การแจงนับ</span><span class="sxs-lookup"><span data-stu-id="d811c-109">enumeration</span></span>](#enumeration)
- [<span data-ttu-id="d811c-110">Guid</span><span class="sxs-lookup"><span data-stu-id="d811c-110">guid</span></span>](#guid)
- [<span data-ttu-id="d811c-111">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="d811c-111">integer</span></span>](#integer)
- [<span data-ttu-id="d811c-112">int64</span><span class="sxs-lookup"><span data-stu-id="d811c-112">int64</span></span>](#int64)
- [<span data-ttu-id="d811c-113">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="d811c-113">real</span></span>](#real)
- [<span data-ttu-id="d811c-114">สตริง</span><span class="sxs-lookup"><span data-stu-id="d811c-114">string</span></span>](#string)

## <a name="boolean"></a><a name="boolean"></a><span data-ttu-id="d811c-115">บูลีน</span><span class="sxs-lookup"><span data-stu-id="d811c-115">Boolean</span></span>

<span data-ttu-id="d811c-116">ชนิดข้อมูลพื้นฐาน *แบบบูลีน* มีค่าที่ถูกประเมินว่าเป็น *จริง* หรือ *เท็จ*</span><span class="sxs-lookup"><span data-stu-id="d811c-116">The *boolean* primitive data type contains a value that is evaluated as either *true* or *false*.</span></span> <span data-ttu-id="d811c-117">คุณสามารถใช้คําสําคัญที่สงวนไว้ตามคำสำคัญ **จริง** และ **เท็จ** ได้ทุกที่ที่คาดว่าจะใช้นิพจน์ *แบบบูลีน*</span><span class="sxs-lookup"><span data-stu-id="d811c-117">You can use the reserved literal keywords **True** and **False** wherever a *boolean* expression is expected.</span></span> <span data-ttu-id="d811c-118">ค่าเริ่มต้นคือ *เท็จ*</span><span class="sxs-lookup"><span data-stu-id="d811c-118">The default value is *false*.</span></span>

<span data-ttu-id="d811c-119">การแสดงภายในของ *แบบบูลีม* คือ *จํานวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="d811c-119">The internal representation of a *boolean* is an *integer*.</span></span> <span data-ttu-id="d811c-120">ค่า *จํานวนเต็ม* 0 (ศูนย์) จะถูกประเมินเป็น *เท็จ* และค่า *จํานวนเต็ม* อื่นๆ ทั้งหมดจะถูกประเมินเป็น *จริง*</span><span class="sxs-lookup"><span data-stu-id="d811c-120">The *integer* value 0 (zero) is evaluated as *false*, and all other *integer* values are evaluated as *true*.</span></span> <span data-ttu-id="d811c-121">เมื่อคุณ [ตรวจสอบความถูกต้อง](general-electronic-reporting-formula-designer.md#TestFormula) ของนิพจน์ที่ตั้งค่าคอนฟิกที่ส่งกลับ *บูลีน* ใน [ตัวออกแบบสูตร ER](er-advanced-formula-editor.md) บานหน้าต่างผลการทดสอบจะแสดง *0* (ศูนย์) เมื่อนิพจน์ส่งกลับ *เท็จ*</span><span class="sxs-lookup"><span data-stu-id="d811c-121">When you [validate](general-electronic-reporting-formula-designer.md#TestFormula) a configured expression that returns a *boolean* in the [ER formula designer](er-advanced-formula-editor.md), the test result pane presents *0* (zero) when an expression returns *false*.</span></span> <span data-ttu-id="d811c-122">มิฉะนั้น บานหน้าต่างผลการทดสอบจะแสดง *1*</span><span class="sxs-lookup"><span data-stu-id="d811c-122">Otherwise, the test result pane presents *1*.</span></span>

<span data-ttu-id="d811c-123">*แบบบูลีน* ไม่มีการแปลงโดยนัย</span><span class="sxs-lookup"><span data-stu-id="d811c-123">A *boolean* has no implicit conversions.</span></span> <span data-ttu-id="d811c-124">อย่างไรก็ตาม คุณสามารถใช้ฟังก์ชัน [TEXT](er-functions-text-text.md) เพื่อแปลง *บูลีน* เป็น *สตริง* อย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="d811c-124">However, you can use the [TEXT](er-functions-text-text.md) function to explicitly converts a *boolean* to a *string*:</span></span>

- <span data-ttu-id="d811c-125">ค่า *เท็จ* จะถูกแปลงเป็นสตริงข้อความ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="d811c-125">The *false* value is converted to the text string **False**.</span></span>
- <span data-ttu-id="d811c-126">ค่า *จริง* จะถูกแปลงเป็นสตริงข้อความ **จริง**</span><span class="sxs-lookup"><span data-stu-id="d811c-126">The *true* value is converted to the text string **True**.</span></span>

> [!NOTE]
> <span data-ttu-id="d811c-127">การแปลงนี้ไม่ได้ขึ้นอยู่กับ [บริบท](er-design-multilingual-reports.md) ภาษาและวัฒนธรรมที่ให้ไว้</span><span class="sxs-lookup"><span data-stu-id="d811c-127">This conversion doesn't depend on the provided language and culture [context](er-design-multilingual-reports.md).</span></span>

<span data-ttu-id="d811c-128">[ตัวดําเนินการ](er-formula-language.md#Operators) เปรียบเทียบเป็นตัวดําเนินการชนิดเดียวที่สามารถใช้กับชนิดข้อมูล *แบบบูลีน* ได้</span><span class="sxs-lookup"><span data-stu-id="d811c-128">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *boolean* data type.</span></span> <span data-ttu-id="d811c-129">ตัวดําเนินการต่อไปนี้สามารถใช้เพื่อเปรียบเทียบค่า *แบบบูลีน* สองค่า ได้แก่ \<\> และ =</span><span class="sxs-lookup"><span data-stu-id="d811c-129">The following operators can be used to compare two *boolean* values: \<\> and =.</span></span>

## <a name="date"></a><a name="date"></a><span data-ttu-id="d811c-130">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="d811c-130">Date</span></span>

<span data-ttu-id="d811c-131">ชนิดข้อมูลพื้นฐาน *วันที่* ประกอบด้วยวัน เดือน และปี</span><span class="sxs-lookup"><span data-stu-id="d811c-131">The *date* primitive data type contains the day, month, and year.</span></span> <span data-ttu-id="d811c-132">วันที่สามารถเริ่มโดยใช้ฟังก์ชันต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d811c-132">Dates can be initiated by using the following functions:</span></span>

- [<span data-ttu-id="d811c-133">DATEVALUE</span><span class="sxs-lookup"><span data-stu-id="d811c-133">DATEVALUE</span></span>](er-functions-datetime-datevalue.md)
- [<span data-ttu-id="d811c-134">NULLDATE</span><span class="sxs-lookup"><span data-stu-id="d811c-134">NULLDATE</span></span>](er-functions-datetime-nulldate.md)
- [<span data-ttu-id="d811c-135">SESSIONTODAY</span><span class="sxs-lookup"><span data-stu-id="d811c-135">SESSIONTODAY</span></span>](er-functions-datetime-sessiontoday.md)
- [<span data-ttu-id="d811c-136">TODAY</span><span class="sxs-lookup"><span data-stu-id="d811c-136">TODAY</span></span>](er-functions-datetime-today.md)

<span data-ttu-id="d811c-137">ชนิดข้อมูล *วันที่* สามารถเก็บวันที่ระหว่างวันที่ 1 มกราคม 1900 ถึง 31 ธันวาคม 2154</span><span class="sxs-lookup"><span data-stu-id="d811c-137">The *date* data type can hold dates between January 1, 1900, and December 31, 2154.</span></span> <span data-ttu-id="d811c-138">ค่าเริ่มต้นคือ **null** และการแสดงภายในคือวันที่ 1 มกราคม 1900</span><span class="sxs-lookup"><span data-stu-id="d811c-138">The default value is **null**, and the internal representation is the date January 1, 1900.</span></span>

<span data-ttu-id="d811c-139">*วันที่* ไม่มีการแปลงโดยนัย</span><span class="sxs-lookup"><span data-stu-id="d811c-139">A *date* has no implicit conversions.</span></span> <span data-ttu-id="d811c-140">อย่างไรก็ตาม คุณสามารถใช้ฟังก์ชันการแปลงที่ชัดเจนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d811c-140">However, you can use the following explicit conversion functions:</span></span>

- [<span data-ttu-id="d811c-141">DATEFORMAT</span><span class="sxs-lookup"><span data-stu-id="d811c-141">DATEFORMAT</span></span>](er-functions-datetime-dateformat.md)
- [<span data-ttu-id="d811c-142">DATETODATETIME</span><span class="sxs-lookup"><span data-stu-id="d811c-142">DATETODATETIME</span></span>](er-functions-datetime-datetodatetime.md)
- [<span data-ttu-id="d811c-143">TEXT</span><span class="sxs-lookup"><span data-stu-id="d811c-143">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="d811c-144">ฟังก์ชัน [ADDDAYS](er-functions-datetime-adddays.md) ช่วยให้คุณสามารถเพิ่มและลบวันจากวันที่ได้</span><span class="sxs-lookup"><span data-stu-id="d811c-144">The [ADDDAYS](er-functions-datetime-adddays.md) function lets you add and subtract days from dates.</span></span> <span data-ttu-id="d811c-145">ด้วยวิธีนี้ คุณสามารถย้ายวันที่ที่ระบุเป็นจํานวนวันในอนาคตและวันในอดีตได้</span><span class="sxs-lookup"><span data-stu-id="d811c-145">In this way, you can move the date a specific number of days into the future and the past.</span></span> <span data-ttu-id="d811c-146">ฟังก์ชัน [DAYS](er-functions-datetime-days.md) จะช่วยให้คุณสามารถลบวันที่ออกจากกัน และคํานวณผลต่างของวัน</span><span class="sxs-lookup"><span data-stu-id="d811c-146">The [DAYS](er-functions-datetime-days.md) function lets you subtract dates from each other and calculate the difference in days.</span></span> <span data-ttu-id="d811c-147">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแปลงค่า *วันที่* โปรดดูที่ [รายการของฟังก์ชัน ER ในประเภทวันที่และเวลา](er-functions-category-datetime.md)</span><span class="sxs-lookup"><span data-stu-id="d811c-147">For more information about the transformation of *date* values, see [List of ER functions in the Date and time category](er-functions-category-datetime.md).</span></span>

<span data-ttu-id="d811c-148">[ตัวดําเนินการ](er-formula-language.md#Operators) เปรียบเทียบเป็นตัวดําเนินการชนิดเดียวที่สามารถใช้กับชนิดข้อมูล *วันที่* ได้</span><span class="sxs-lookup"><span data-stu-id="d811c-148">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *date* data type.</span></span> <span data-ttu-id="d811c-149">ตัวดําเนินการต่อไปนี้สามารถใช้เพื่อเปรียบเทียบค่า *วันที่* สองค่า ได้แก่ \<\>, \<, \<=, =, \> และ \>=</span><span class="sxs-lookup"><span data-stu-id="d811c-149">The following operators can be used to compare two *date* values: \<\>, \<, \<=, =, \>, and \>=.</span></span>

## <a name="datetime"></a><a name="datetime"></a><span data-ttu-id="d811c-150">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d811c-150">Datetime</span></span>

<span data-ttu-id="d811c-151">ชนิดข้อมูลพื้นฐาน *วันที่และเวลา* จะรวมชนิด *วันที่* และค่าที่แสดงถึงเวลาที่ผ่านไปนับตั้งแต่เที่ยงคืน</span><span class="sxs-lookup"><span data-stu-id="d811c-151">The *datetime* primitive data type combines the *date* type and a value that represents the time that has passed since midnight.</span></span> <span data-ttu-id="d811c-152">เวลาจะแสดงเป็นชั่วโมง นาที วินาที และเศษส่วนของวินาที</span><span class="sxs-lookup"><span data-stu-id="d811c-152">The time is expressed in hours, minutes, seconds, and fractions of a second.</span></span> <span data-ttu-id="d811c-153">ค่า *วันที่และเวลา* ยังเก็บข้อมูลเกี่ยวกับโซนเวลาด้วย</span><span class="sxs-lookup"><span data-stu-id="d811c-153">A *datetime* value also holds information about the time zone.</span></span>

<span data-ttu-id="d811c-154">ชนิดข้อมูล *วันที่และเวลา* สามารถมีวันที่ระหว่าง 1 มกราคม 1900 (1900-01-01T00:00:00.0000000+00:00 ใน [รูปแบบ](/dotnet/standard/base-types/standard-date-and-time-format-strings) การเดินทางไปกลับ) และ 31 ธันวาคม 2154 (2154/12/31T11:59:59.9999999+00:00 ในรูปแบบการเดินทางไปกลับ)</span><span class="sxs-lookup"><span data-stu-id="d811c-154">The *datetime* data type can hold dates between January 1, 1900 (1900-01-01T00:00:00.0000000+00:00 in the round-trip [format](/dotnet/standard/base-types/standard-date-and-time-format-strings)) and December 31, 2154 (2154/12/31T11:59:59.9999999+00:00 in the round-trip format).</span></span> <span data-ttu-id="d811c-155">หน่วยเวลาที่เล็กที่สุดใน *วันที่และเวลา* คือหนึ่งสิบล้านของวินาที</span><span class="sxs-lookup"><span data-stu-id="d811c-155">The smallest unit of time in a *datetime* is one ten millionth of a second.</span></span>

> [!NOTE]
> <span data-ttu-id="d811c-156">เมื่อมีการใช้ **hh** [ตัวระบุ](/dotnet/standard/base-types/standard-date-and-time-format-strings) เป็นชั่วโมง ค่าเวลาที่สูงกว่า 12:59:59:9999999 ไม่สามารถแปลเป็นเวลาที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d811c-156">When the **hh** [specifier](/dotnet/standard/base-types/standard-date-and-time-format-strings) is used for hours, time values above 12:59:59:9999999 can't be interpreted as valid times.</span></span>
>
> <span data-ttu-id="d811c-157">เมื่อมีการใช้ตัวระบุ **HH** เป็นชั่วโมง ค่าเวลาที่สูงกว่า 23:59:59:9999999 ไม่สามารถแปลเป็นเวลาที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d811c-157">When the **HH** specifier is used for hours, time values above 23:59:59:9999999 can't be interpreted as valid times.</span></span>

<span data-ttu-id="d811c-158">ค่าเริ่มต้นเป็น **null** และการแสดงภายในคือวันที่ 1 มกราคม 1900 (1900-01-01T00:00:00.0000000+00:00 ในรูปแบบการเดินทางไปกลับ)</span><span class="sxs-lookup"><span data-stu-id="d811c-158">The default value is **null**, and the internal representation is the date January 1, 1900 (1900-01-01T00:00:00.0000000+00:00 in the round-trip format).</span></span>

<span data-ttu-id="d811c-159">วันที่และเวลาสามารถเริ่มโดยใช้ฟังก์ชันต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d811c-159">Datetimes can be initiated by using the following functions:</span></span>

- [<span data-ttu-id="d811c-160">DATETIMEVALUE</span><span class="sxs-lookup"><span data-stu-id="d811c-160">DATETIMEVALUE</span></span>](er-functions-datetime-datetimevalue.md)
- [<span data-ttu-id="d811c-161">NULNULLDATETIMELDATE</span><span class="sxs-lookup"><span data-stu-id="d811c-161">NULNULLDATETIMELDATE</span></span>](er-functions-datetime-nulldatetime.md)
- [<span data-ttu-id="d811c-162">SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="d811c-162">SESSIONNOW</span></span>](er-functions-datetime-sessionnow.md)
- [<span data-ttu-id="d811c-163">NOW</span><span class="sxs-lookup"><span data-stu-id="d811c-163">NOW</span></span>](er-functions-datetime-now.md)

<span data-ttu-id="d811c-164">*วันที่และเวลา* ไม่มีการแปลงโดยนัย</span><span class="sxs-lookup"><span data-stu-id="d811c-164">A *datetime* has no implicit conversions.</span></span> <span data-ttu-id="d811c-165">อย่างไรก็ตาม คุณสามารถใช้ฟังก์ชันการแปลงที่ชัดเจนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d811c-165">However, you can use the following explicit conversion functions:</span></span>

- [<span data-ttu-id="d811c-166">DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="d811c-166">DATETIMEFORMAT</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="d811c-167">TEXT</span><span class="sxs-lookup"><span data-stu-id="d811c-167">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="d811c-168">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแปลงค่า *วันที่และเวลา* โปรดดูที่ [รายการของฟังก์ชัน ER ในประเภทวันที่และเวลา](er-functions-category-datetime.md)</span><span class="sxs-lookup"><span data-stu-id="d811c-168">For more information about the transformation of *datetime* values, see [List of ER functions in the Date and time category](er-functions-category-datetime.md).</span></span>

<span data-ttu-id="d811c-169">[ตัวดําเนินการ](er-formula-language.md#Operators) เปรียบเทียบเป็นตัวดําเนินการชนิดเดียวที่สามารถใช้กับชนิดข้อมูล *วันที่และเวลา* ได้</span><span class="sxs-lookup"><span data-stu-id="d811c-169">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *datetime* data type.</span></span> <span data-ttu-id="d811c-170">ตัวดําเนินการต่อไปนี้สามารถใช้เพื่อเปรียบเทียบค่า *วันที่และเวลา* สองค่า ได้แก่ \<\>, \<, \<=, =, \> และ \>=</span><span class="sxs-lookup"><span data-stu-id="d811c-170">The following operators can be used to compare two *datetime* values: \<\>, \<, \<=, =, \>, and \>=.</span></span>

## <a name="enumeration"></a><a name="enumeration"></a><span data-ttu-id="d811c-171">การแจงนับ</span><span class="sxs-lookup"><span data-stu-id="d811c-171">Enumeration</span></span>

<span data-ttu-id="d811c-172">ชนิดข้อมูลพื้นฐาน *การแจงนับ* คือรายการสัญพจน์</span><span class="sxs-lookup"><span data-stu-id="d811c-172">The *enumeration* primitive data type is a list of literals.</span></span> <span data-ttu-id="d811c-173">คุณสามารถใช้การแจงนับที่กําหนดใน [รหัสต้นทาง](../dev-ref/xpp-data-primitive.md#enum) ของแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="d811c-173">You can use enumerations that are defined in the application [source code](../dev-ref/xpp-data-primitive.md#enum).</span></span> <span data-ttu-id="d811c-174">คุณยังสามารถแนะนำการแจงนับของคุณเองใน [รูปแบบข้อมูล](general-electronic-reporting.md#data-model-and-model-mapping-components) ER และส่วนประกอบ [รูปแบบ](general-electronic-reporting.md#FormatComponentOutbound) ER</span><span class="sxs-lookup"><span data-stu-id="d811c-174">You can also introduce your own enumerations in the ER [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) and ER [format](general-electronic-reporting.md#FormatComponentOutbound) components.</span></span>

<span data-ttu-id="d811c-175">*การแจงนับ* แอปพลิเคชันสามารถใช้ในนิพจน์ของการแม็ปแบบจำลอง ER และรูปแบบ ER ใดๆ</span><span class="sxs-lookup"><span data-stu-id="d811c-175">An application *enumeration* can be used in expressions of any ER model mapping and ER format.</span></span>

<span data-ttu-id="d811c-176">รูปภาพประกอบต่อไปนี้จะแสดงวิธีการที่คุณสามารถเพิ่มการแจงนับแบบจำลอง **CustVendCorrectiveReasonCode** ลงในรูปแบบข้อมูล ER ที่แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="d811c-176">The following illustration shows how you can add the **CustVendCorrectiveReasonCode** model enumeration to the editable ER data model.</span></span>

<span data-ttu-id="d811c-177">[![การกำหนดค่าการแจงนับแบบจำลองในตัวออกแบบรูปแบบข้อมูล ER](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)</span><span class="sxs-lookup"><span data-stu-id="d811c-177">[![Configuring a model enumeration in the ER data model designer](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)</span></span>

<span data-ttu-id="d811c-178">*การแจงนับ* แบบจำลองสามารถใช้ในนิพจน์ของการแม็ปแบบจำลอง ER และรูปแบบ ER ใดๆ ที่สร้างขึ้นภายใต้รูปแบบข้อมูลที่มีการใช้ *การแจงนับ*</span><span class="sxs-lookup"><span data-stu-id="d811c-178">A model *enumeration* can be used in expressions of any ER model mapping and ER format that were created under a data model where the *enumeration* was introduced.</span></span>

<span data-ttu-id="d811c-179">ภาพประกอบต่อไปนี้แสดงวิธีการที่คุณสามารถเพิ่มการแจงนับรูปแบบ **รายการของประเภทย่อยของค่าธรรมเนียมย้อนกลับ** ในรูปแบบ ER ที่แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="d811c-179">The following illustration shows how you can add the **List of Natura reverse charge subcategories** format enumeration to the editable ER format.</span></span>

<span data-ttu-id="d811c-180">[![การกำหนดค่าการแจงนับรูปแบบในตัวออกแบบรูปแบบ ER](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)</span><span class="sxs-lookup"><span data-stu-id="d811c-180">[![Configuring a format enumeration in the ER format designer](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)</span></span>

<span data-ttu-id="d811c-181">*การแจงนับ* รูปแบบสามารถใช้ในนิพจน์ของรูปแบบ ER ที่มีการใช้ *การแจงนับ* เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d811c-181">A format *enumeration* can be used only in expressions of the ER format where the *enumeration* was introduced.</span></span>

<span data-ttu-id="d811c-182">คุณต้องใช้แหล่งข้อมูล ER ชนิดที่เหมาะสมเพื่อเตรียมการแจงหมายเลขเฉพาะให้กับส่วนประกอบ ER ที่ตั้งค่าคอนฟิกเป็นค่าคงที่ หรือเป็นค่าที่ผู้ใช้รันโซลูชัน ER ที่กําหนดในกล่องโต้ตอบรันไทม์</span><span class="sxs-lookup"><span data-stu-id="d811c-182">You must use the appropriate type of ER data sources to bring a specific enumeration to a configured ER component as a constant or as a value that the user who is running an ER solution defined in the dialog box at runtime.</span></span>

- <span data-ttu-id="d811c-183">สามารถเข้าถึงการแจงนับแอปพลิเคชันได้โดยใช้แหล่งข้อมูล **Dynamics 365 for Operations \ การแจงนับ** และ **พารามิเตอร์ที่ผู้ใช้ป้อน/ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="d811c-183">Application enumerations can be accessed by using the **Dynamics 365 for Operations \ Enumeration** and **General \ User input parameters** data sources.</span></span> <span data-ttu-id="d811c-184">ภาพประกอบต่อไปนี้แสดงวิธีการที่คุณสามารถเพิ่มในรูปแบบ ER ที่แก้ไขได้ **appenumNoYes** และแหล่งข้อมูล **uipNoYes** ที่อ้างอิงถึงการแจงนับแอปพลิเคชัน **NoYes**</span><span class="sxs-lookup"><span data-stu-id="d811c-184">The following illustration shows how you can add to the editable ER format the **appenumNoYes** and **uipNoYes** data sources that refer to the **NoYes** application enumeration.</span></span>

    <span data-ttu-id="d811c-185">[![การเพิ่มแหล่งข้อมูลการแจงนับแอปพลิเคชันตัวออกแบบรูปแบบ ER](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)</span><span class="sxs-lookup"><span data-stu-id="d811c-185">[![Adding application enumeration data sources in the ER format designer](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)</span></span>

- <span data-ttu-id="d811c-186">การแจงนับรูปแบบข้อมูลสามารถเข้าถึงได้โดยใช้แหล่งข้อมูล **รูปแบบข้อมูล \ การแจงนับ** และ **พารามิเตอร์ที่ผู้ใช้ป้อนการแจงนับ/รูปแบบข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d811c-186">Data model enumerations can be accessed by using the **Data model \ Enumeration** and **Data model \ Enumeration user input parameters** data sources.</span></span> <span data-ttu-id="d811c-187">ภาพประกอบต่อไปนี้แสดงวิธีการที่คุณสามารถเพิ่มในรูปแบบ ER ที่แก้ไขได้ แหล่งข้อมูล **CustVendCorrectiveReasonCode** ที่อ้างอิงถึงการแจงนับรูปแบบข้อมูล **CustVendCorrectiveReasonCode**</span><span class="sxs-lookup"><span data-stu-id="d811c-187">The following illustration shows how you can add to the editable ER format the **CustVendCorrectiveReasonCode** data source that refers to the **CustVendCorrectiveReasonCode** data model enumeration.</span></span>

    <span data-ttu-id="d811c-188">[![การเพิ่มแหล่งข้อมูลการแจงนับแบบจำลองตัวออกแบบรูปแบบ ER](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)</span><span class="sxs-lookup"><span data-stu-id="d811c-188">[![Adding model enumeration data sources in the ER format designer](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)</span></span>

- <span data-ttu-id="d811c-189">การแจงนับรูปแบบสามารถเข้าถึงได้โดยใช้แหล่งข้อมูล **รูปแบบ \ การแจงนับ** และ **พารามิเตอร์การป้อนของผู้ใช้รูปแบบ \ การแจงนับ**</span><span class="sxs-lookup"><span data-stu-id="d811c-189">Format enumerations can be accessed by using the **Format \ Enumeration** and **Format \ Enumeration user input parameters** data sources.</span></span> <span data-ttu-id="d811c-190">ภาพประกอบต่อไปนี้แสดงวิธีการที่คุณสามารถเพิ่มในรูปแบบ ER ที่แก้ไขได้ แหล่งข้อมูล **NaturaReverseCharge** ที่อ้างอิงถึงการแจงนับรูปแบบ **Natura reverse charge subcategories**</span><span class="sxs-lookup"><span data-stu-id="d811c-190">The following illustration shows how you can add to the editable ER format the **NaturaReverseCharge** data source that refers to the **Natura reverse charge subcategories** format enumeration.</span></span>

    <span data-ttu-id="d811c-191">[![การเพิ่มแหล่งข้อมูลการแจงนับรูปแบบในตัวออกแบบรูปแบบ ER](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)</span><span class="sxs-lookup"><span data-stu-id="d811c-191">[![Adding format enumeration data sources in the ER format designer](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)</span></span>

<span data-ttu-id="d811c-192">*การแจงนับ* ไม่มีการแปลงโดยนัย</span><span class="sxs-lookup"><span data-stu-id="d811c-192">An *enumeration* has no implicit conversions.</span></span> <span data-ttu-id="d811c-193">อย่างไรก็ตาม คุณสามารถใช้ฟังก์ชันการแปลง [TEXT](er-functions-text-text.md) เพื่อแปลง *การแจงนับ* เป็นสตริงข้อความได้</span><span class="sxs-lookup"><span data-stu-id="d811c-193">However, you can use the [TEXT](er-functions-text-text.md) conversion function to convert an *enumeration* to a text string.</span></span> <span data-ttu-id="d811c-194">การแปลงนี้ไม่ขึ้นอยู่กับภาษา</span><span class="sxs-lookup"><span data-stu-id="d811c-194">This conversion isn't language dependent.</span></span> <span data-ttu-id="d811c-195">หากต้องการทราบวิธีการที่คุณสามารถเชื่อมโยงค่า *การแจงนับ* กับป้ายชื่อเฉพาะภาษาที่เหมาะสม โปรดดูตัวอย่างการใช้ของฟังก์ชัน [LISTOFFIELDS](er-functions-list-listoffields.md) และ [GETENUMVALUTBYNAME](er-functions-text-getenumvaluebyname.md)</span><span class="sxs-lookup"><span data-stu-id="d811c-195">To learn how you can associate an *enumeration* value with the appropriate language-specific labels, see the usage examples for the [LISTOFFIELDS](er-functions-list-listoffields.md) and [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md) functions.</span></span>

<span data-ttu-id="d811c-196">[ตัวดําเนินการ](er-formula-language.md#Operators) เปรียบเทียบเป็นตัวดําเนินการชนิดเดียวที่สามารถใช้กับชนิดข้อมูล *การแจงนับ* ได้</span><span class="sxs-lookup"><span data-stu-id="d811c-196">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *enumeration* data type.</span></span> <span data-ttu-id="d811c-197">ตัวดําเนินการต่อไปนี้สามารถใช้เพื่อเปรียบเทียบค่า *การแจงนับ* สองค่า ได้แก่ \<\> และ =</span><span class="sxs-lookup"><span data-stu-id="d811c-197">The following operators can be used to compare two *enumeration* values: \<\> and =.</span></span>

## <a name="guid"></a><a name="guid"></a><span data-ttu-id="d811c-198">GUID</span><span class="sxs-lookup"><span data-stu-id="d811c-198">Guid</span></span>

<span data-ttu-id="d811c-199">ชนิดข้อมูลพื้นฐาน *guid* จะเก็บค่ารหัสเฉพาะสากล (GUID)</span><span class="sxs-lookup"><span data-stu-id="d811c-199">The *guid* primitive data type holds a globally unique identifier (GUID) value.</span></span> <span data-ttu-id="d811c-200">GUID คือค่าที่สามารถใช้ได้ระหว่างคอมพิวเตอร์และเครือข่ายทุกเครื่อง ทุกแห่งที่ต้องมีรหัสเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="d811c-200">A GUID is a value that can be used across all computers and networks, wherever a unique identifier is required.</span></span> <span data-ttu-id="d811c-201">ไม่อาจคัดลอกตัวเลขได้</span><span class="sxs-lookup"><span data-stu-id="d811c-201">It's unlikely that the number will be duplicated.</span></span> <span data-ttu-id="d811c-202">GUID ที่ถูกต้องตรงตามข้อมูลจำเพาะต่อไปนี้ทั้งหมด:</span><span class="sxs-lookup"><span data-stu-id="d811c-202">A valid GUID meets all the following specifications:</span></span>

- <span data-ttu-id="d811c-203">ต้องมีตัวเลขฐานสิบหก 32 หลัก</span><span class="sxs-lookup"><span data-stu-id="d811c-203">There must be 32 hexadecimal digits.</span></span>
- <span data-ttu-id="d811c-204">นอกจากนี้ ต้องมีอักขระเครื่องหมายขีดคั่นสี่ตัวที่ฝังอยู่ในตำแหน่งต่อไปนี้ 8-4-4-4-12</span><span class="sxs-lookup"><span data-stu-id="d811c-204">In addition, there must be four dash characters that are embedded at the following locations: 8-4-4-4-12.</span></span>
- <span data-ttu-id="d811c-205">นอกจากนี้ คุณยังสามารถเพิ่มวงเล็บปีกกา \{\} เสริมได้ที่จุดเริ่มต้นและจุดสิ้นสุดของสตริง</span><span class="sxs-lookup"><span data-stu-id="d811c-205">In addition, optional braces \{\} can be added at the beginning and end of the string.</span></span> <span data-ttu-id="d811c-206">ตัวอย่างเช่น ทั้ง **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** และ **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** เป็นสตริง GUID ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d811c-206">For example, both **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** and **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** are valid GUID strings.</span></span>
- <span data-ttu-id="d811c-207">ดังนั้น ต้องมีอักขระรวม 36 หรือ 38 ตัว ทั้งนี้ขึ้นอยู่กับว่ามีการเพิ่มวงเล็บปีกกาหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d811c-207">Therefore, there must be a total of 36 or 38 characters, depending on whether braces are added.</span></span>
- <span data-ttu-id="d811c-208">ตัวอักษรที่ใช้เป็นตัวเลขฐานสิบหกสามารถเป็นตัวพิมพ์ใหญ่ (A–F) ตัวพิมพ์เล็ก (a–f) หรือผสม</span><span class="sxs-lookup"><span data-stu-id="d811c-208">The letters that are used as hexadecimal digits can be uppercase (A–F), lowercase (a–f), or mixed.</span></span>

<span data-ttu-id="d811c-209">ฟังก์ชันการแปลงที่ชัดเจนต่อไปนี้สามารถใช้ได้:</span><span class="sxs-lookup"><span data-stu-id="d811c-209">The following explicit conversion functions can be used:</span></span>

- [<span data-ttu-id="d811c-210">GUIDVALUE</span><span class="sxs-lookup"><span data-stu-id="d811c-210">GUIDVALUE</span></span>](er-functions-text-guidvalue.md)
- [<span data-ttu-id="d811c-211">TEXT</span><span class="sxs-lookup"><span data-stu-id="d811c-211">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="d811c-212">[ตัวดําเนินการ](er-formula-language.md#Operators) เปรียบเทียบเป็นตัวดําเนินการชนิดเดียวที่สามารถใช้กับชนิดข้อมูล *guid* ได้</span><span class="sxs-lookup"><span data-stu-id="d811c-212">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *guid* data type.</span></span> <span data-ttu-id="d811c-213">ตัวดําเนินการต่อไปนี้สามารถใช้เพื่อเปรียบเทียบค่า *guid* สองค่า ได้แก่ \<\> และ =</span><span class="sxs-lookup"><span data-stu-id="d811c-213">The following operators can be used to compare two *guid* values: \<\> and =.</span></span>

## <a name="integer"></a><a name="integer"></a><span data-ttu-id="d811c-214">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="d811c-214">Integer</span></span>

<span data-ttu-id="d811c-215">ชนิดข้อมูลพื้นฐาน *จํานวนเต็ม* แสดงถึงตัวเลขที่ไม่มีทศนิยม</span><span class="sxs-lookup"><span data-stu-id="d811c-215">The *integer* primitive data type represents a number that has no decimal places.</span></span> <span data-ttu-id="d811c-216">จํานวนเต็มจะใช้เป็นตัวแปรควบคุมในรายงานซ้ำกัน หรือเป็นดัชนีในรายการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="d811c-216">Integers are used as control variables in repetitive statements or as indexes in record lists.</span></span>

<span data-ttu-id="d811c-217">ตัวอักษร *จํานวนเต็ม* คือจํานวนเต็มตามที่ป้อนโดยตรงใน [นิพจน์](general-electronic-reporting-formula-designer.md#formula-designer-overview) ER (สูตร) เช่น **12345**</span><span class="sxs-lookup"><span data-stu-id="d811c-217">An *integer* literal is the integer as it's entered directly in an ER [expression](general-electronic-reporting-formula-designer.md#formula-designer-overview) (formula), such as **12345**.</span></span> <span data-ttu-id="d811c-218">*จํานวนเต็ม* กว้าง 32 บิต</span><span class="sxs-lookup"><span data-stu-id="d811c-218">An *integer* is 32-bits wide.</span></span> <span data-ttu-id="d811c-219">ค่าเริ่มต้นคือ **0** และการแสดงภายในเป็นตัวเลขแบบยาว</span><span class="sxs-lookup"><span data-stu-id="d811c-219">The default value is **0**, and the internal representation is a long number.</span></span> <span data-ttu-id="d811c-220">*จํานวนเต็ม* จะถูกแปลงเป็น *จํานวนจริง* โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d811c-220">An *integer* is automatically converted to a *real*.</span></span>

<span data-ttu-id="d811c-221">นอกจากนี้ ฟังก์ชันการแปลงที่ชัดเจนต่อไปนี้สามารถใช้ได้:</span><span class="sxs-lookup"><span data-stu-id="d811c-221">Additionally, the following explicit conversion functions can be used:</span></span>

- [<span data-ttu-id="d811c-222">INTVALUE</span><span class="sxs-lookup"><span data-stu-id="d811c-222">INTVALUE</span></span>](er-functions-conversion-intvalue.md)
- [<span data-ttu-id="d811c-223">NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="d811c-223">NUMBERFORMAT</span></span>](er-functions-text-numberformat.md)
- [<span data-ttu-id="d811c-224">TEXT</span><span class="sxs-lookup"><span data-stu-id="d811c-224">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="d811c-225">ช่วงของ *จํานวนเต็ม* คือ \[-2,147,483,647 : 2,147,483,647\]</span><span class="sxs-lookup"><span data-stu-id="d811c-225">The range of an *integer* is \[-2,147,483,647 : 2,147,483,647\].</span></span> <span data-ttu-id="d811c-226">จํานวนเต็มของช่วงนี้สามารถใช้เป็นตัวอักษรได้</span><span class="sxs-lookup"><span data-stu-id="d811c-226">All integers of this range can be used as literals.</span></span>

<span data-ttu-id="d811c-227">[ตัวดำเนินการ](er-formula-language.md#Operators) การเปรียบเทียบและคณิตศาสตร์ทั้งหมดกับชนิดข้อมูล *จํานวนเต็ม* ได้</span><span class="sxs-lookup"><span data-stu-id="d811c-227">All comparison and mathematical [operators](er-formula-language.md#Operators) can be used with the *integer* data type.</span></span>

## <a name="int64"></a><a name="int64"></a><span data-ttu-id="d811c-228">Int64</span><span class="sxs-lookup"><span data-stu-id="d811c-228">Int64</span></span>

<span data-ttu-id="d811c-229">ชนิดข้อมูลพื้นฐาน *int64* แสดงถึงตัวเลขที่ไม่มีทศนิยม</span><span class="sxs-lookup"><span data-stu-id="d811c-229">The *int64* primitive data type represents a number that has no decimal places.</span></span> <span data-ttu-id="d811c-230">ค่า *Int64* จะใช้เป็นตัวแปรควบคุมในรายงานซ้ำกัน หรือเป็นตัวระบุเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="d811c-230">*Int64* values are used as control variables in repetitive statements or as record identifiers.</span></span>

<span data-ttu-id="d811c-231">*int64* กว้าง 64 บิต</span><span class="sxs-lookup"><span data-stu-id="d811c-231">An *int64* is 64-bits wide.</span></span> <span data-ttu-id="d811c-232">ค่าเริ่มต้นคือ **0** และการแสดงภายในเป็นตัวเลขแบบยาว</span><span class="sxs-lookup"><span data-stu-id="d811c-232">The default value is **0**, and the internal representation is a long number.</span></span> <span data-ttu-id="d811c-233">*int64* จะถูกแปลงเป็น *จํานวนจริง* โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d811c-233">An *int64* is automatically converted to a *real*.</span></span>

<span data-ttu-id="d811c-234">นอกจากนี้ ฟังก์ชันการแปลงที่ชัดเจนต่อไปนี้สามารถใช้ได้:</span><span class="sxs-lookup"><span data-stu-id="d811c-234">Additionally, the following explicit conversion functions can be used:</span></span>

- [<span data-ttu-id="d811c-235">INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="d811c-235">INT64VALUE</span></span>](er-functions-conversion-int64value.md)
- [<span data-ttu-id="d811c-236">NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="d811c-236">NUMBERFORMAT</span></span>](er-functions-text-numberformat.md)
- [<span data-ttu-id="d811c-237">TEXT</span><span class="sxs-lookup"><span data-stu-id="d811c-237">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="d811c-238">ช่วงของ *int64* คือ \[-9,223,372,036,854,775,807 : 9,223,372,036,854,775,807\]</span><span class="sxs-lookup"><span data-stu-id="d811c-238">The range of an *int64* is \[-9,223,372,036,854,775,807 : 9,223,372,036,854,775,807\].</span></span>

<span data-ttu-id="d811c-239">[ตัวดำเนินการ](er-formula-language.md#Operators) การเปรียบเทียบและคณิตศาสตร์ทั้งหมดกับชนิดข้อมูล *int64* ได้</span><span class="sxs-lookup"><span data-stu-id="d811c-239">All comparison and mathematical [operators](er-formula-language.md#Operators) can be used with the *int64* data type.</span></span>

## <a name="real"></a><a name="real"></a><span data-ttu-id="d811c-240">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="d811c-240">Real</span></span>

<span data-ttu-id="d811c-241">ชนิดข้อมูลพื้นฐาน *จริง* สามารถมีค่าทศนิยมนอกเหนือจากจํานวนเต็มได้</span><span class="sxs-lookup"><span data-stu-id="d811c-241">The *real* primitive data type can hold decimal values in addition to integers.</span></span> <span data-ttu-id="d811c-242">คุณสามารถใช้ตัวอักษรทศนิยมในที่คาดหวัง *ค่าจริง*</span><span class="sxs-lookup"><span data-stu-id="d811c-242">You can use decimal literals anywhere that a *real* is expected.</span></span> <span data-ttu-id="d811c-243">ตัวอักษรทศนิยมคือทศนิยม ตามที่ป้อนไว้โดยตรงในรหัส เช่น **2.19**</span><span class="sxs-lookup"><span data-stu-id="d811c-243">A decimal literal is the decimal as it's entered directly in code, such as **2.19**.</span></span>

> [!NOTE]
> <span data-ttu-id="d811c-244">ในนิพจน์ ER จะใช้จุด (.) เป็นตัวแบ่งทศนิยมเสมอ</span><span class="sxs-lookup"><span data-stu-id="d811c-244">In ER expressions, a period (.) is always used as the decimal separator.</span></span>

<span data-ttu-id="d811c-245">คุณสามารถใช้ตัวเลขจริงในนิพจน์ทั้งหมด และสามารถใช้ค่าจริงกับทั้งตัวดำเนินการเปรียบเทียบและเลขคณิต</span><span class="sxs-lookup"><span data-stu-id="d811c-245">Reals can be used in all expressions, and they can be used with both comparison and arithmetic operators.</span></span> <span data-ttu-id="d811c-246">ตัวเลข *จริง* มีตัวเลขที่สําคัญ 16 หลัก</span><span class="sxs-lookup"><span data-stu-id="d811c-246">A *real* has a precision of 16 significant digits.</span></span> <span data-ttu-id="d811c-247">ค่าเริ่มต้นของตัวเลข *จริง* คือ **0.0** และการแสดงภายในคือหมายเลขดิจิทัล (BCD) ที่มีรหัสฐานสอง</span><span class="sxs-lookup"><span data-stu-id="d811c-247">The default value for a *real* is **0.0**, and the internal representation is a binary-coded digital (BCD) number.</span></span> <span data-ttu-id="d811c-248">การเข้ารหัส BCD จะช่วยให้สามารถแสดงค่าที่เป็นตัวคูณของ 0.1 ที่แน่นอน</span><span class="sxs-lookup"><span data-stu-id="d811c-248">The BCD encoding enables exact representations of values that are multiples of 0.1.</span></span> <span data-ttu-id="d811c-249">ช่วงของตัวแปร *จริง* คือ -(10)<sup>127</sup> through (10)<sup>127</sup></span><span class="sxs-lookup"><span data-stu-id="d811c-249">The range of a *real* variable is -(10)<sup>127</sup> through (10)<sup>127</sup>.</span></span> <span data-ttu-id="d811c-250">ตัวเลขจริงทั้งหมดในช่วงนี้สามารถใช้เป็นตัวอักษรในนิพจน์ ER</span><span class="sxs-lookup"><span data-stu-id="d811c-250">All reals in this range can be used as literals in ER expressions.</span></span>

<span data-ttu-id="d811c-251">ค่า *จริง* ไม่มีการแปลงโดยนัย</span><span class="sxs-lookup"><span data-stu-id="d811c-251">A *real* has no implicit conversions.</span></span> <span data-ttu-id="d811c-252">อย่างไรก็ตาม คุณสามารถใช้ฟังก์ชันต่อไปนี้เพื่อแปลงชนิดข้อมูล *จริง* เป็นชนิดข้อมูลอื่นๆ และชนิดข้อมูลอื่นๆ เป็นชนิดข้อมูล *จริง* ได้</span><span class="sxs-lookup"><span data-stu-id="d811c-252">However, you can use the following functions to explicitly convert a *real* to other data types and other data types to a *real*:</span></span>

- [<span data-ttu-id="d811c-253">INTVALUE</span><span class="sxs-lookup"><span data-stu-id="d811c-253">INTVALUE</span></span>](er-functions-conversion-intvalue.md)
- [<span data-ttu-id="d811c-254">INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="d811c-254">INT64VALUE</span></span>](er-functions-conversion-int64value.md)
- [<span data-ttu-id="d811c-255">NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="d811c-255">NUMBERFORMAT</span></span>](er-functions-text-numberformat.md)
- [<span data-ttu-id="d811c-256">TEXT</span><span class="sxs-lookup"><span data-stu-id="d811c-256">TEXT</span></span>](er-functions-text-text.md)
- [<span data-ttu-id="d811c-257">VALUE</span><span class="sxs-lookup"><span data-stu-id="d811c-257">VALUE</span></span>](er-functions-conversion-value.md)

<span data-ttu-id="d811c-258">[ตัวดำเนินการ](er-formula-language.md#Operators) การเปรียบเทียบและคณิตศาสตร์ทั้งหมดกับชนิดข้อมูล *จริง* ได้</span><span class="sxs-lookup"><span data-stu-id="d811c-258">All comparison and mathematical [operators](er-formula-language.md#Operators) can be used with the *real* data type.</span></span>

## <a name="string"></a><a name="string"></a><span data-ttu-id="d811c-259">สตริง</span><span class="sxs-lookup"><span data-stu-id="d811c-259">String</span></span>

<span data-ttu-id="d811c-260">ชนิดข้อมูลพื้นฐาน *สตริง* แสดงถึงลำดับของอักขระที่ใช้เป็นข้อความ หมายเลขบัญชี ที่อยู่ และหมายเลขโทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="d811c-260">The *string* primitive data type represents a sequence of characters that are used as texts, account numbers, addresses, and telephone numbers.</span></span>

<span data-ttu-id="d811c-261">ตัวอักษร *สตริง* คืออักขระที่แนบอยู่ในเครื่องหมายอัญประกาศ ("")</span><span class="sxs-lookup"><span data-stu-id="d811c-261">*String* literals are characters that are enclosed in quotation marks ("").</span></span> <span data-ttu-id="d811c-262">ตัวอักษร *สตริง* สามารถใช้ในที่ใดๆ ที่คาดหวังค่า *สตริง* ในนิพจน์ ER</span><span class="sxs-lookup"><span data-stu-id="d811c-262">*String* literals can be used wherever *string* values are expected in ER expressions.</span></span> <span data-ttu-id="d811c-263">คุณสามารถใช้สตริงในนิพจน์ทางตรรกะ เช่น การเปรียบเทียบ</span><span class="sxs-lookup"><span data-stu-id="d811c-263">You can use strings in logical expressions, such as comparisons.</span></span> <span data-ttu-id="d811c-264">นอกจากนี้คุณยังสามารถรวมค่า *สตริง* ต่างๆ ให้รวมไว้โดยใช้ตัวดำเนินการ **\&** หรือฟังก์ชัน [CONCATENATE](er-functions-text-concatenate.md)</span><span class="sxs-lookup"><span data-stu-id="d811c-264">You can also concatenate *string* values by using the **\&** operator or the [CONCATENATE](er-functions-text-concatenate.md) function.</span></span>

> [!NOTE]
> <span data-ttu-id="d811c-265">ถ้าคุณรวมค่า *สตริง* สองค่าไว้และคุณต้องการให้ *สตริง* ผลลัพธ์ครอบคลุมมากกว่าหนึ่งรายการ ให้ใช้ตัวแบ่งบรรทัดระหว่างค่าต่างๆ</span><span class="sxs-lookup"><span data-stu-id="d811c-265">If you concatenate two *string* values, and you want the resulting *string* to span more than one line, use the line break separator between the values.</span></span> <span data-ttu-id="d811c-266">ใช้เอาท์พุท TEXT ตัวแบ่งนี้สามารถเป็นอักขระที่สร้างโดยใช้นิพจน์ [CHAR](er-functions-text-char.md)(10) หรือ CHAR(13)</span><span class="sxs-lookup"><span data-stu-id="d811c-266">For the TEXT output, this separator can be a character that is generated by using the [CHAR](er-functions-text-char.md)(10) or CHAR(13) expression.</span></span> <span data-ttu-id="d811c-267">สำหรับ HTML สามารถเป็นแท็ก **\<br\>** ได้</span><span class="sxs-lookup"><span data-stu-id="d811c-267">For HTML, it can be the **\<br\>** tag.</span></span>

<span data-ttu-id="d811c-268">ค่าเริ่มต้นของ *สตริง* คือสตริงข้อความที่ว่างเปล่าที่ไม่มีอักขระ และการแสดงภายในเป็นรายการอักขระ</span><span class="sxs-lookup"><span data-stu-id="d811c-268">The default value for a *string* is a blank text string that has no characters, and the internal representation is a list of characters.</span></span>

<span data-ttu-id="d811c-269">ไม่มีการแปลงอัตโนมัติของสตริง</span><span class="sxs-lookup"><span data-stu-id="d811c-269">There are no automatic conversions for strings.</span></span> <span data-ttu-id="d811c-270">อย่างไรก็ตาม ฟังก์ชันการแปลงที่ชัดเจนต่อไปนี้สามารถใช้ได้:</span><span class="sxs-lookup"><span data-stu-id="d811c-270">However, the following explicit conversion functions can be used:</span></span>

- [<span data-ttu-id="d811c-271">CHAR</span><span class="sxs-lookup"><span data-stu-id="d811c-271">CHAR</span></span>](er-functions-text-char.md)
- [<span data-ttu-id="d811c-272">FORMAT</span><span class="sxs-lookup"><span data-stu-id="d811c-272">FORMAT</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="d811c-273">LEFT</span><span class="sxs-lookup"><span data-stu-id="d811c-273">LEFT</span></span>](er-functions-text-left.md)
- [<span data-ttu-id="d811c-274">LEN</span><span class="sxs-lookup"><span data-stu-id="d811c-274">LEN</span></span>](er-functions-text-len.md)
- [<span data-ttu-id="d811c-275">MID</span><span class="sxs-lookup"><span data-stu-id="d811c-275">MID</span></span>](er-functions-text-mid.md)
- [<span data-ttu-id="d811c-276">PADLEFT</span><span class="sxs-lookup"><span data-stu-id="d811c-276">PADLEFT</span></span>](er-functions-text-padleft.md)
- [<span data-ttu-id="d811c-277">REPLACE</span><span class="sxs-lookup"><span data-stu-id="d811c-277">REPLACE</span></span>](er-functions-text-replace.md)
- [<span data-ttu-id="d811c-278">RIGHT</span><span class="sxs-lookup"><span data-stu-id="d811c-278">RIGHT</span></span>](er-functions-text-right.md)
- [<span data-ttu-id="d811c-279">TEXT</span><span class="sxs-lookup"><span data-stu-id="d811c-279">TEXT</span></span>](er-functions-text-text.md)
- [<span data-ttu-id="d811c-280">TRANSLATE</span><span class="sxs-lookup"><span data-stu-id="d811c-280">TRANSLATE</span></span>](er-functions-text-translate.md)
- [<span data-ttu-id="d811c-281">TRIM</span><span class="sxs-lookup"><span data-stu-id="d811c-281">TRIM</span></span>](er-functions-text-trim.md)
- [<span data-ttu-id="d811c-282">UPPER</span><span class="sxs-lookup"><span data-stu-id="d811c-282">UPPER</span></span>](er-functions-text-upper.md)

<span data-ttu-id="d811c-283">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแปลงค่า *สตริง* โปรดดูที่ [รายการของฟังก์ชัน ER ในประเภทข้อความ](er-functions-category-text.md)</span><span class="sxs-lookup"><span data-stu-id="d811c-283">For more about the transformation of *string* values, see [List of ER functions of the text category](er-functions-category-text.md).</span></span>

<span data-ttu-id="d811c-284">*สตริง* สามารถมีจํานวนอักขระไม่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="d811c-284">A *string* can hold an indefinite number of characters.</span></span>

<span data-ttu-id="d811c-285">[ตัวดำเนินการ](er-formula-language.md#Operators) การเปรียบเทียบทั้งหมดกับชนิดข้อมูล *สตริง* ได้</span><span class="sxs-lookup"><span data-stu-id="d811c-285">All comparison [operators](er-formula-language.md#Operators) can be used with the *string* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d811c-286">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d811c-286">Additional resources</span></span>

- [<span data-ttu-id="d811c-287">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d811c-287">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="d811c-288">ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d811c-288">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="d811c-289">ชนิดข้อมูลแบบรวมที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="d811c-289">Supported composite data types</span></span>](er-formula-supported-data-types-composite.md)
