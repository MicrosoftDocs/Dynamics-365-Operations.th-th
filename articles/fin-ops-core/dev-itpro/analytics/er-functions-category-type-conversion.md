---
title: รายการของฟังก์ชั่น ER ในประเภทการแปลงข้อมูล
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันการแปลงที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2cfa5deb3b2c00565759e4334a002bf112f888ac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917660"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="531d1-103">รายการของฟังก์ชั่น ER ในประเภทการแปลงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="531d1-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="531d1-104">ฟังก์ชันการแปลงชนิดของการรายงานทางอิเล็กทรอนิกส์ (ER) สามารถใช้เพื่อแปลงค่าระหว่างชนิด</span><span class="sxs-lookup"><span data-stu-id="531d1-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="531d1-105">หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="531d1-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="531d1-106">ฟังก์ชันการแปลงของชนิด</span><span class="sxs-lookup"><span data-stu-id="531d1-106">Type conversion functions</span></span>

| <span data-ttu-id="531d1-107">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="531d1-107">Function</span></span> | <span data-ttu-id="531d1-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="531d1-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="531d1-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="531d1-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="531d1-110">ฟังก์ชันนี้ส่งกลับค่า *Int64* ที่แสดงถึงสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="531d1-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="531d1-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="531d1-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="531d1-112">ฟังก์ชันนี้ส่งกลับค่า *Int* ที่แสดงถึงสตริงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="531d1-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="531d1-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="531d1-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="531d1-114">ฟังก์ชันนี้ส่งกลับค่า *จำนวนจริง* ที่ถูกแปลงจากค่า *สตริง* ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="531d1-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="531d1-115">ในระหว่างการแปลงจะมีการพิจารณาตัวแบ่งการจัดกลุ่มทศนิยมและเลขฐานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="531d1-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="531d1-116">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="531d1-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="531d1-117">ฟังก์ชันนี้ส่งกลับค่า *จำนวนจริง* ที่ถูกแปลงจากค่า *สตริง* ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="531d1-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="531d1-118">ฟังก์ชันการแปลงชนิดในประเภทวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="531d1-118">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="531d1-119">ตารางต่อไปนี้อธิบายฟังก์ชันการแปลงชนิดใน [ประเภทวันที่และเวลา](er-functions-category-datetime.md)</span><span class="sxs-lookup"><span data-stu-id="531d1-119">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="531d1-120">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="531d1-120">Function</span></span> | <span data-ttu-id="531d1-121">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="531d1-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="531d1-122">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="531d1-122">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="531d1-123">ฟังก์ชันนี้ส่งกลับค่า *DateTime* ที่แปลงจากค่า *สตริง* ที่ให้ในรูปแบบที่ระบุและใน Culture ที่ระบุเป็นทางเลือกเป็นค่าวันที่/เวลา</span><span class="sxs-lookup"><span data-stu-id="531d1-123">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="531d1-124">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="531d1-124">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="531d1-125">ฟังก์ชันนี้ส่งกลับค่า *DateTime* ที่ถูกแปลงจากค่า *วันที่* ที่กำหนดให้เป็นค่าวันที่/เวลาในเวลาสากล (เวลามาตรฐานกรีนิช \[GMT\])</span><span class="sxs-lookup"><span data-stu-id="531d1-125">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="531d1-126">DateValue</span><span class="sxs-lookup"><span data-stu-id="531d1-126">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="531d1-127">ฟังก์ชันนี้ส่งกลับค่า *Date* ที่แปลงจากค่า *สตริง* ที่ให้ในรูปแบบที่ระบุและใน Culture ที่ระบุเป็นทางเลือกเป็นค่าวันที่/เวลา</span><span class="sxs-lookup"><span data-stu-id="531d1-127">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="531d1-128">ฟังก์ชั่นการสนทนาของชนิดในประเภทการ</span><span class="sxs-lookup"><span data-stu-id="531d1-128">Type conversion functions in the list category</span></span>

<span data-ttu-id="531d1-129">ตารางต่อไปนี้อธิบายฟังก์ชันการแปลงชนิดใน [รายการประเภท](er-functions-category-list.md)</span><span class="sxs-lookup"><span data-stu-id="531d1-129">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="531d1-130">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="531d1-130">Function</span></span> | <span data-ttu-id="531d1-131">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="531d1-131">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="531d1-132">รายการ</span><span class="sxs-lookup"><span data-stu-id="531d1-132">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="531d1-133">ฟังก์ชันนี้ส่งกลับค่า *รายการเรกคอร์ด* เป็นรายการใหม่ที่สร้างขึ้นจากอาร์กิวเมนต์ที่ระบุของชนิด *คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="531d1-133">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="531d1-134">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="531d1-134">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="531d1-135">ฟังก์ชันนี้ส่งกลับค่า *รายการเรกคอร์ด* ที่สร้างขึ้นตามโครงสร้างของอาร์กิวเมนต์ที่ให้ชนิดของ *การแจงนับ* หรือ *คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="531d1-135">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="531d1-136">การแบ่ง</span><span class="sxs-lookup"><span data-stu-id="531d1-136">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="531d1-137">ฟังก์ชันนี้แบ่งค่า *สตริง* ที่ระบุลงในสตริงย่อยและส่งกลับผลลัพธ์เป็นค่า *ค่ารายการเรกคอร์ด* ใหม่</span><span class="sxs-lookup"><span data-stu-id="531d1-137">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="531d1-138">StringJoin</span><span class="sxs-lookup"><span data-stu-id="531d1-138">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="531d1-139">ฟังก์ชันนี้ส่งคืนค่า *สตริง* ที่ประกอบด้วยค่าที่ต่อกันของฟิลด์ที่ระบุจากค่า *รายการเรกคอร์ด* ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="531d1-139">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="531d1-140">ค่าสามารถถูกแบ่งด้วยตัวคั่นที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="531d1-140">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="531d1-141">ฟังก์ชั่นการสนทนาของชนิดในประเภทข้อความ</span><span class="sxs-lookup"><span data-stu-id="531d1-141">Type conversion functions in the text category</span></span>

<span data-ttu-id="531d1-142">ตารางต่อไปนี้อธิบายฟังก์ชันการแปลงชนิดใน [ประเภทข้อความ](er-functions-category-text.md)</span><span class="sxs-lookup"><span data-stu-id="531d1-142">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="531d1-143">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="531d1-143">Function</span></span> | <span data-ttu-id="531d1-144">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="531d1-144">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="531d1-145">Char</span><span class="sxs-lookup"><span data-stu-id="531d1-145">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="531d1-146">ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงอักขระเดี่ยวที่ถูกอ้างอิงโดยหมายเลข Unicode ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="531d1-146">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="531d1-147">GuidValue</span><span class="sxs-lookup"><span data-stu-id="531d1-147">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="531d1-148">ฟังก์ชันนี้แปลงอินพุตที่ระบุของชนิด *สตริง* เป็นรายการข้อมูลของชนิด *GUID*</span><span class="sxs-lookup"><span data-stu-id="531d1-148">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="531d1-149">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="531d1-149">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="531d1-150">ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงหมายเลขที่ระบุในรูปแบบที่ระบุและในวัฒนธรรมที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="531d1-150">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="531d1-151">QrCode</span><span class="sxs-lookup"><span data-stu-id="531d1-151">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="531d1-152">ฟังก์ชันนี้ส่งกลับค่า *คอนเทนเนอร์* ที่แสดงรูป Quick Response code (QR code) สำหรับสตริงที่ระบุในรูปแบบไบนารี</span><span class="sxs-lookup"><span data-stu-id="531d1-152">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="531d1-153">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="531d1-153">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="531d1-154">ฟังก์ชันนี้ส่งคืนตัวเลขที่ระบุเป็นค่า *สตริง* ที่แสดงถึงตัวเลขที่ระบุ หลังจากที่ได้ถูกแปลงเป็นข้อความแบบสตริงที่ถูกจัดรูปแบบตามการตั้งค่าตำแหน่งที่ตั้งของเซิร์ฟเวอร์ของอินสแตนซ์ของแอปพลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="531d1-154">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="531d1-155">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="531d1-155">Additional resources</span></span>

[<span data-ttu-id="531d1-156">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="531d1-156">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="531d1-157">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="531d1-157">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="531d1-158">ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="531d1-158">Electronic reporting formula language</span></span>](er-formula-language.md)
