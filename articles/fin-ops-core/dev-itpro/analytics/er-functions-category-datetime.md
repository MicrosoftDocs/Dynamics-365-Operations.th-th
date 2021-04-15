---
title: รายการของฟังก์ชั่น ER ในประเภทวันที่และเวลา
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันวันที่และเวลาที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 2dd8524c9cd368f0fe64347e3212b419bb0902b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744572"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="c7feb-103">รายการของฟังก์ชั่น ER ในประเภทวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c7feb-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7feb-104">ฟังก์ชันวันและเวลาของการรายงานทางอิเล็กทรอนิกส์ (ER) สามารถใช้เพื่อดึงข้อมูลจากค่าวันที่และเวลาและเพื่อมาดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="c7feb-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="c7feb-105">หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c7feb-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="c7feb-106">รายการฟังก์ชันที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="c7feb-106">List of supported functions</span></span>

| <span data-ttu-id="c7feb-107">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="c7feb-107">Function</span></span> | <span data-ttu-id="c7feb-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c7feb-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="c7feb-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="c7feb-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="c7feb-110">ฟังก์ชันนี้ส่งคืนค่า *DateTime* ที่เป็นจำนวนวันที่ระบุก่อนหรือหลังวันที่เริ่มต้นที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="c7feb-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="c7feb-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="c7feb-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="c7feb-112">ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงค่าวันที่ที่ให้เป็นข้อความในรูปแบบที่ระบุและใน Culture ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="c7feb-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="c7feb-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c7feb-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="c7feb-114">ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงค่าวันที่/เวลาที่ให้เป็นข้อความในรูปแบบที่ระบุและใน Culture ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="c7feb-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="c7feb-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="c7feb-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="c7feb-116">ฟังก์ชันนี้ส่งกลับค่า *DateTime* ที่แปลงจากค่าข้อความที่ให้ในรูปแบบที่ระบุและใน Culture ไปยังค่าวันที่/เวลาที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="c7feb-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="c7feb-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="c7feb-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="c7feb-118">ฟังก์ชันนี้ส่งกลับค่า *DateTime* ที่ถูกแปลงจากค่าวันที่ที่กำหนดให้เป็นค่าวันที่/เวลาในเวลาสากล (เวลามาตรฐานกรีนิช \[GMT\])</span><span class="sxs-lookup"><span data-stu-id="c7feb-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="c7feb-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="c7feb-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="c7feb-120">ฟังก์ชันนี้ส่งกลับค่า *Date* ที่แปลงจากค่าข้อความที่ให้ในรูปแบบที่ระบุและใน Culture ไปยังค่าวันที่ที่ระบุเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="c7feb-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="c7feb-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="c7feb-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="c7feb-122">ฟังก์ชันนี้ส่งคืนค่าที่แสดง *จำนวนเต็ม* ของวันระหว่างวันที่ 1 มกราคมและวันที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="c7feb-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="c7feb-123">วัน</span><span class="sxs-lookup"><span data-stu-id="c7feb-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="c7feb-124">ฟังก์ชันนี้ส่งคืนค่าที่แสดง *จำนวนเต็ม* ที่แสดงจำนวนของวันระหว่างวันที่ที่ระบุที่หนึ่งกับวันที่ที่ระบุที่สอง</span><span class="sxs-lookup"><span data-stu-id="c7feb-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="c7feb-125">Now</span><span class="sxs-lookup"><span data-stu-id="c7feb-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="c7feb-126">ฟังก์ชันนี้ส่งคืนค่า *DateTime* ที่แสดงถึงวันที่และเวลาของเซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="c7feb-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="c7feb-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="c7feb-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="c7feb-128">ฟังก์ชันนี้ส่งคืนค่า *Date* ที่แสดงถึงวันที่ **ที่เป็นแบบ null** (1 มกราคม 1900)</span><span class="sxs-lookup"><span data-stu-id="c7feb-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="c7feb-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="c7feb-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="c7feb-130">ฟังก์ชันนี้ส่งกลับค่า *DateTime* ที่แสดงค่าวัน/เวลา **ที่เป็น null** (1 มกราคม 1900) ในเวลาสากลที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="c7feb-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="c7feb-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="c7feb-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="c7feb-132">ฟังก์ชันนี้ส่งคืนค่า *DateTime* ที่แสดงถึงวันที่และเวลาของเซสชันแอปพลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="c7feb-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="c7feb-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="c7feb-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="c7feb-134">ฟังก์ชันนี้ส่งคืนค่า *Date* ที่แสดงถึงวันที่เซสชันแอปพลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="c7feb-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="c7feb-135">วันนี้</span><span class="sxs-lookup"><span data-stu-id="c7feb-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="c7feb-136">ฟังก์ชันนี้ส่งคืนค่า *Date* ที่แสดงถึงวันที่เซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="c7feb-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="c7feb-137">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c7feb-137">Additional resources</span></span>

[<span data-ttu-id="c7feb-138">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c7feb-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="c7feb-139">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c7feb-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="c7feb-140">ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c7feb-140">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]