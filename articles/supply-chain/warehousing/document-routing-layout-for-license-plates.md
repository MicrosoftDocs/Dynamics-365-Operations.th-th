---
title: โครงร่างการกำหนดเส้นทางเอกสารสำหรับป้ายชื่อทะเบียน
description: หัวข้อนี้จะอธิบายวิธีการใช้วิธีการจัดรูปแบบเพื่อพิมพ์ค่าบนป้ายชื่อ
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 66ba73ab5c790aa4a67419842f63f6f741bf0d3a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973771"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="4f838-103">โครงร่างการกำหนดเส้นทางเอกสารสำหรับป้ายชื่อทะเบียน</span><span class="sxs-lookup"><span data-stu-id="4f838-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f838-104">โครงร่างการกำหนดเส้นทางเอกสารจะกำหนดโครงร่างของป้ายชื่อทะเบียนและข้อมูลที่พิมพ์ไว้</span><span class="sxs-lookup"><span data-stu-id="4f838-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="4f838-105">คุณตั้งค่าคอนฟิกจุดทริกเกอร์การพิมพ์เมื่อคุณตั้งค่ารายการเมนูของอุปกรณ์เคลื่อนที่และเท็มเพลตการทำงาน</span><span class="sxs-lookup"><span data-stu-id="4f838-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="4f838-106">ในสถานการณ์ปกติ เจ้าหน้าที่รับสินค้าของคลังสินค้าพิมพ์ป้ายชื่อทะเบียนทันทีหลังจากที่บันทึกเนื้อหาของแท่นวางสินค้าที่มาถึงในพื้นที่ที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="4f838-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="4f838-107">ป้ายชื่อที่มีอยู่จริงจะใช้กับแท่นวางสินค้า</span><span class="sxs-lookup"><span data-stu-id="4f838-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="4f838-108">จากนั้นจึงสามารถใช้สำหรับการตรวจสอบความถูกต้องโดยเป็นส่วนหนึ่งของกระบวนการสำรองที่ตามมาและการดำเนินการเบิกสินค้าขาออกในอนาคต</span><span class="sxs-lookup"><span data-stu-id="4f838-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="4f838-109">คุณสามารถพิมพ์ป้ายชื่อที่ซับซ้อนสูงได้ ซึ่งอุปกรณ์การพิมพ์สามารถแปลข้อความที่ส่งไปได้</span><span class="sxs-lookup"><span data-stu-id="4f838-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="4f838-110">ตัวอย่างเช่น โครงร่างภาษา (ZPL) ของการเขียนโปรแกรม Zebra (ZPL) ซึ่งรวมบาร์โค้ด อาจคล้ายกับตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f838-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="4f838-111">โดยเป็นส่วนหนึ่งของกระบวนการพิมพ์ป้ายชื่อ ข้อความ `$LicensePlateId$` ในตัวอย่างนี้จะถูกแทนที่ด้วยค่าข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4f838-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="4f838-112">เมื่อต้องการดูค่าที่จะพิมพ์ ให้ไปที่ **การจัดการคลังสินค้า \> การสอบถามและรายงาน \> ป้ายชื่อทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="4f838-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="4f838-113">เครื่องมือการสร้างป้ายชื่อที่มีอยู่หลายตัวสามารถช่วยคุณจัดรูปแบบข้อความสำหรับโครงร่างป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="4f838-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="4f838-114">หลายๆ เครื่องมือเหล่านี้สนับสนุนรูปแบบ `$FieldName$`</span><span class="sxs-lookup"><span data-stu-id="4f838-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="4f838-115">นอกจากนี้ Microsoft Dynamics 365 Supply Chain Management ยังใช้ตรรกะการจัดรูปแบบพิเศษ โดยเป็นส่วนหนึ่งของการแม็ปฟิลด์สำหรับโครงร่างการกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="4f838-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="4f838-116">รูปแบบตัวเลขที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4f838-116">Custom number formats</span></span>

<span data-ttu-id="4f838-117">คุณสามารถเลือกกำหนดการจัดรูปแบบของค่าฟิลด์ตัวเลขที่พิมพ์โดยใช้รหัสที่มีรูปแบบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f838-117">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="4f838-118">ต่อไปนี้เป็นคำอธิบายของรูปแบบนี้:</span><span class="sxs-lookup"><span data-stu-id="4f838-118">Here is an explanation of this format:</span></span>

- <span data-ttu-id="4f838-119">`FieldName` คือชื่อของฟิลด์ข้อมูล (เช่น **ปริมาณ**)</span><span class="sxs-lookup"><span data-stu-id="4f838-119">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="4f838-120">`FormatString` กำหนดว่าต้องพิมพ์ข้อมูลอย่างไร</span><span class="sxs-lookup"><span data-stu-id="4f838-120">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="4f838-121">ตัวอย่างต่อไปนี้แสดงวิธีการที่คุณสามารถกำหนดฟิลด์ปริมาณงาน (**ปริมาณ**):</span><span class="sxs-lookup"><span data-stu-id="4f838-121">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="4f838-122">เมื่อต้องการแสดงตัวเลขสี่หลักเสมอ (โดยใช้เลขศูนย์เป็นตัวยึดตำแหน่ง) ให้ใช้ `$Qty:0000$`</span><span class="sxs-lookup"><span data-stu-id="4f838-122">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="4f838-123">ตัวอย่างเช่น ถ้าปริมาณคือ 10 ป้ายชื่อจะแสดง "0010"</span><span class="sxs-lookup"><span data-stu-id="4f838-123">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="4f838-124">เมื่อต้องการแสดงตำแหน่งทศนิยมสองตำแหน่งเสมอ ให้ใช้ `$Qty:0.00$`</span><span class="sxs-lookup"><span data-stu-id="4f838-124">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="4f838-125">ตัวอย่างเช่น ถ้าปริมาณคือ 10 ป้ายชื่อจะแสดง "10.00"</span><span class="sxs-lookup"><span data-stu-id="4f838-125">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="4f838-126">สำหรับรายการทั้งหมดของสตริงรูปแบบตัวเลขที่พร้อมใช้งาน ให้ดูที่ [สตริงรูปแบบตัวเลขที่กำหนดเอง](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings)</span><span class="sxs-lookup"><span data-stu-id="4f838-126">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="4f838-127">รูปแบบสตริงที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4f838-127">Custom string formats</span></span>

<span data-ttu-id="4f838-128">คุณสามารถลบอักขระตัวแรกของสตริงโดยการใช้ฟิลด์และรหัสรูปแบบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f838-128">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="4f838-129">ที่นี่ `#` ระบุจำนวนของอักขระที่จะข้าม</span><span class="sxs-lookup"><span data-stu-id="4f838-129">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="4f838-130">ตัวอย่างเช่น ถ้าต้องการพิมพ์หมายเลขป้ายทะเบียนรหัสคอนเทนเนอร์ประจำสินค้า (SSCC) ที่ไม่มีอักขระสองตัวแรก ให้ใช้ `$LicensePlateId:2..$`</span><span class="sxs-lookup"><span data-stu-id="4f838-130">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="4f838-131">ในกรณีนี้ หมายเลขป้ายทะเบียน 0011111111111222221 จะถูกพิมพ์เป็น "11111111111222221"</span><span class="sxs-lookup"><span data-stu-id="4f838-131">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="4f838-132">รูปแบบวันที่/เวลาแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4f838-132">Custom date/time formats</span></span>

<span data-ttu-id="4f838-133">ตัวอย่างต่อไปนี้แสดงวิธีการที่คุณสามารถควบคุมรูปแบบที่ใช้ในการพิมพ์วันที่</span><span class="sxs-lookup"><span data-stu-id="4f838-133">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="4f838-134">ในตัวอย่างนี้ วันที่ 30 เมษายน 2020 จะถูกพิมพ์เป็น "30-04-2020"</span><span class="sxs-lookup"><span data-stu-id="4f838-134">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="4f838-135">สำหรับรายการทั้งหมดของรูปแบบวันที่/เวลาที่พร้อมใช้งาน ให้ดูที่ [สตริงรูปแบบเวลาและวันที่ที่กำหนดเอง](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings)</span><span class="sxs-lookup"><span data-stu-id="4f838-135">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="4f838-136">พิมพ์แต่ละบรรทัดจากข้อมูลหลายบรรทัด</span><span class="sxs-lookup"><span data-stu-id="4f838-136">Print individual lines from multiline data</span></span>

<span data-ttu-id="4f838-137">ถ้าฟิลด์ข้อมูลมีหลายบรรทัด (นั่นคือบรรทัดที่คั่นด้วยตัวแบ่งบรรทัด) คุณสามารถพิมพ์แต่ละบรรทัดได้โดยใช้รูปแบบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f838-137">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="4f838-138">ที่นี่ `#` คือหมายเลขรายการที่คุณต้องการพิมพ์</span><span class="sxs-lookup"><span data-stu-id="4f838-138">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="4f838-139">(ใช้ 1 สำหรับบรรทัดแรก)</span><span class="sxs-lookup"><span data-stu-id="4f838-139">(Use 1 for the first line.)</span></span>

<span data-ttu-id="4f838-140">ตัวอย่างเช่น ระบบของคุณมีฟิลด์ `AdditionalAddress` ที่จัดเก็บที่อยู่หลายบรรทัดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4f838-140">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="4f838-141">Contoso Inc</span><span class="sxs-lookup"><span data-stu-id="4f838-141">Contoso Inc.</span></span>  
<span data-ttu-id="4f838-142">ชื่อถนน 123</span><span class="sxs-lookup"><span data-stu-id="4f838-142">123 Street Name</span></span>  
<span data-ttu-id="4f838-143">บางเมือง บางรัฐ</span><span class="sxs-lookup"><span data-stu-id="4f838-143">Some City, Some State</span></span>

<span data-ttu-id="4f838-144">คุณสามารถพิมพ์ที่อยู่นี้ หนึ่งบรรทัดในแต่ละครั้ง โดยใช้รหัสดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f838-144">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="4f838-145">รหัส</span><span class="sxs-lookup"><span data-stu-id="4f838-145">Code</span></span> | <span data-ttu-id="4f838-146">ข้อความที่พิมพ์</span><span class="sxs-lookup"><span data-stu-id="4f838-146">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="4f838-147">Contoso Inc</span><span class="sxs-lookup"><span data-stu-id="4f838-147">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="4f838-148">ชื่อถนน 123</span><span class="sxs-lookup"><span data-stu-id="4f838-148">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="4f838-149">บางเมือง บางรัฐ</span><span class="sxs-lookup"><span data-stu-id="4f838-149">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="4f838-150">พิมพ์และจัดรูปแบบจากวิธีการแสดง</span><span class="sxs-lookup"><span data-stu-id="4f838-150">Print and format from a display method</span></span>

<span data-ttu-id="4f838-151">คุณสามารถพิมพ์จากวิธีการแสดงโดยใช้รูปแบบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f838-151">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="4f838-152">คุณสามารถรวมรูปแบบนี้กับชนิดอื่นๆ ที่อธิบายไว้ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="4f838-152">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="4f838-153">ตัวอย่างเช่น คุณมีวิธีการแสดงที่มีการระบุชื่อ `DisplayListOfItemsNumbers()` และคุณต้องการพิมพ์หมายเลขสินค้าแรกของวิธีการนี้</span><span class="sxs-lookup"><span data-stu-id="4f838-153">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="4f838-154">ในกรณีนี้ คุณสามารถใช้รหัสต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f838-154">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="4f838-155">ข้อมูลเพิ่มเติมเกี่ยวกับวิธีการพิมพ์ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="4f838-155">More information about how to print labels</span></span>

<span data-ttu-id="4f838-156">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าและพิมพ์ป้ายชื่อ ให้ดูที่ [การเปิดใช้งานการพิมพ์ป้ายชื่อทะเบียน](tasks/license-plate-label-printing.md)</span><span class="sxs-lookup"><span data-stu-id="4f838-156">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>
