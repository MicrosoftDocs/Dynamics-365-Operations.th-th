---
title: การใช้แหล่งข้อมูลบาร์โค้ดเพื่อสร้างรูปภาพของบาร์โค้ด
description: หัวข้อนี้จะอธิบายวิธีการใช้แหล่งข้อมูลบาร์โค้ดเพื่อสร้างรูปภาพของบาร์โค้ด
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: 08b9d03517a600cf46b1093cfa3bc454621eabd0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748376"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a><span data-ttu-id="e9e21-103">การใช้แหล่งข้อมูลบาร์โค้ดเพื่อสร้างรูปภาพของบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="e9e21-103">Use Barcode data sources to generate bar code images</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e9e21-104">คุณสามารถใช้กรอบงาน [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) เพื่อออกแบบ [ส่วนประกอบของรูปแบบ ER](general-electronic-reporting.md#FormatComponentOutbound) ซึ่งคุณสามารถรันเพื่อสร้างเอกสารขาออกอิเล็กทรอนิกส์และแบบพิมพ์ได้ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="e9e21-104">You can use the [Electronic reporting (ER)](general-electronic-reporting.md) framework to design [ER format components](general-electronic-reporting.md#FormatComponentOutbound) that you can run to generate electronic and printable outbound documents that you require.</span></span> <span data-ttu-id="e9e21-105">เมื่อต้องการสร้างเอกสารขาออกในรูปแบบ Microsoft Office คุณต้องระบุโครงร่างของรายงานโดยใช้เอกสาร Microsoft Excel หรือเอกสาร Microsoft Word เป็นเท็มเพลตรายงาน</span><span class="sxs-lookup"><span data-stu-id="e9e21-105">To generate an outbound document in Microsoft Office format, you must specify the layout of the report by using either a Microsoft Excel document or a Microsoft Word document as a report template.</span></span> <span data-ttu-id="e9e21-106">[ตัวออกแบบการดำเนินงาน ER](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) ช่วยให้คุณสามารถแนบเอกสาร Excel หรือ Word เป็นเท็มเพลตสำหรับรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="e9e21-106">The [ER Operations designer](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) lets you attach an Excel or Word document as a template for an ER format.</span></span> <span data-ttu-id="e9e21-107">องค์ประกอบที่มีชื่อต่อไปนี้ในเท็มเพลตที่แนบจะเชื่อมโยงกับองค์ประกอบของส่วนประกอบรูปแบบที่ตั้งค่าคอนฟิก:</span><span class="sxs-lookup"><span data-stu-id="e9e21-107">The following named elements in the attached template are associated with the elements of the configured format component:</span></span>

- <span data-ttu-id="e9e21-108">ตัวควบคุมเนื้อหาใน Word</span><span class="sxs-lookup"><span data-stu-id="e9e21-108">Content controls in Word</span></span>
- <span data-ttu-id="e9e21-109">แผ่นงานที่มีชื่อ ช่วง เซลล์ รูปร่าง และรูปภาพใน Excel</span><span class="sxs-lookup"><span data-stu-id="e9e21-109">Named sheets, ranges, cells, shapes, and images in Excel</span></span>

<span data-ttu-id="e9e21-110">องค์ประกอบที่มีการระบุชื่อเหล่านี้จะใช้เป็นตัวยึดสำหรับข้อมูลที่ถูกป้อนในเอกสารที่สร้างขึ้น เมื่อมีการรันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="e9e21-110">These named elements are used as placeholders for data that is entered in a generated document when an ER format is run.</span></span> <span data-ttu-id="e9e21-111">องค์ประกอบของรูปแบบ ER ถูกเชื่อมโยงไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e9e21-111">ER format elements are bound to data sources.</span></span> <span data-ttu-id="e9e21-112">แหล่งข้อมูลเหล่านี้จะระบุข้อมูลที่จะถูกป้อนลงในเอกสารที่สร้างขึ้นในขณะทำงาน</span><span class="sxs-lookup"><span data-stu-id="e9e21-112">These data sources specify the data that will be entered in the generated documents at runtime.</span></span> <span data-ttu-id="e9e21-113">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ฝังรูปภาพและรูปร่างในเอกสารที่คุณสร้างโดยใช้ ER](electronic-reporting-embed-images-shapes.md)</span><span class="sxs-lookup"><span data-stu-id="e9e21-113">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

<span data-ttu-id="e9e21-114">ปัจจุบัน ER สนับสนุนชนิดแหล่งข้อมูล **บาร์โค้ด**</span><span class="sxs-lookup"><span data-stu-id="e9e21-114">ER now supports the **Barcode** data source type.</span></span> <span data-ttu-id="e9e21-115">ดังนั้น ตอนนี้คุณจึงสามารถสร้างรูปภาพที่แสดงถึงบาร์โค้ดสำหรับข้อความที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="e9e21-115">Therefore, you can now generate an image that represents the bar code for specified text.</span></span> <span data-ttu-id="e9e21-116">เมื่อคุณตั้งค่าคอนฟิกรูปแบบ ER คุณสามารถระบุแหล่งข้อมูลของชนิด **บาร์โค้ด** เพื่อสร้างรูปภาพของบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="e9e21-116">When you configure an ER format, you can specify data sources of the **Barcode** type to generate bar code images.</span></span> <span data-ttu-id="e9e21-117">จากนั้น คุณสามารถเพิ่มรูปภาพเหล่านั้นลงในเอกสารทางธุรกิจที่สร้างขึ้น เช่น ใบสั่ง ใบแจ้งหนี้ บันทึกการจัดส่ง และใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="e9e21-117">You can then add those images to generated business documents, such as orders, invoices, packing slips, and receipts.</span></span> <span data-ttu-id="e9e21-118">นอกจากนี้ คุณยังสามารถเพิ่มในป้ายชื่อชนิดต่างๆ เช่น ป้ายชื่อผลิตภัณฑ์และชั้นวางสินค้า และป้ายชื่อบรรจุภัณฑ์และการจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="e9e21-118">You can also add them to various kind of labels, such as product and shelf labels, and packaging and shipping labels.</span></span>

<span data-ttu-id="e9e21-119">สามารถใช้ตัวยึดตำแหน่งต่อไปนี้ในเท็มเพลตรายงานเพื่อป้อนรูปภาพบาร์โค้ด:</span><span class="sxs-lookup"><span data-stu-id="e9e21-119">The following placeholders can be used in report templates to enter bar code images:</span></span>

- <span data-ttu-id="e9e21-120">ตัวควบคุมเนื้อหา [รูปภาพ](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) สำหรับ Word</span><span class="sxs-lookup"><span data-stu-id="e9e21-120">[Picture](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) content control for Word</span></span>
- <span data-ttu-id="e9e21-121">ออบเจ็กต์ [รูปภาพ](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) ใน Excel</span><span class="sxs-lookup"><span data-stu-id="e9e21-121">[Picture](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) object in Excel</span></span>

<span data-ttu-id="e9e21-122">โดยใช้แหล่งข้อมูลของชนิด **บาร์โค้ด** คุณสามารถสร้างบาร์โค้ดในรูปแบบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e9e21-122">By using a data source of the **Barcode** type, you can generate bar codes in the following formats:</span></span>

- <span data-ttu-id="e9e21-123">บาร์โค้ดหนึ่งมิติ:</span><span class="sxs-lookup"><span data-stu-id="e9e21-123">One-dimensional bar codes:</span></span>

    - <span data-ttu-id="e9e21-124">Codabar</span><span class="sxs-lookup"><span data-stu-id="e9e21-124">Codabar</span></span>
    - <span data-ttu-id="e9e21-125">Code 39</span><span class="sxs-lookup"><span data-stu-id="e9e21-125">Code 39</span></span>
    - <span data-ttu-id="e9e21-126">Code 93</span><span class="sxs-lookup"><span data-stu-id="e9e21-126">Code 93</span></span>
    - <span data-ttu-id="e9e21-127">Code 128</span><span class="sxs-lookup"><span data-stu-id="e9e21-127">Code 128</span></span>
    - <span data-ttu-id="e9e21-128">EAN-8</span><span class="sxs-lookup"><span data-stu-id="e9e21-128">EAN-8</span></span>
    - <span data-ttu-id="e9e21-129">EAN-13</span><span class="sxs-lookup"><span data-stu-id="e9e21-129">EAN-13</span></span>
    - <span data-ttu-id="e9e21-130">ITF-14</span><span class="sxs-lookup"><span data-stu-id="e9e21-130">ITF-14</span></span>
    - <span data-ttu-id="e9e21-131">จดหมายอัจฉริยะ</span><span class="sxs-lookup"><span data-stu-id="e9e21-131">Intelligent Mail</span></span>
    - <span data-ttu-id="e9e21-132">MSI</span><span class="sxs-lookup"><span data-stu-id="e9e21-132">MSI</span></span>
    - <span data-ttu-id="e9e21-133">Plessey</span><span class="sxs-lookup"><span data-stu-id="e9e21-133">Plessey</span></span>
    - <span data-ttu-id="e9e21-134">PDF417</span><span class="sxs-lookup"><span data-stu-id="e9e21-134">PDF417</span></span>
    - <span data-ttu-id="e9e21-135">UPC-A</span><span class="sxs-lookup"><span data-stu-id="e9e21-135">UPC-A</span></span>
    - <span data-ttu-id="e9e21-136">UPC-E</span><span class="sxs-lookup"><span data-stu-id="e9e21-136">UPC-E</span></span>

- <span data-ttu-id="e9e21-137">บาร์โค้ดสองมิติ:</span><span class="sxs-lookup"><span data-stu-id="e9e21-137">Two-dimensional bar codes:</span></span>

    - <span data-ttu-id="e9e21-138">Aztec</span><span class="sxs-lookup"><span data-stu-id="e9e21-138">Aztec</span></span>
    - <span data-ttu-id="e9e21-139">เมทริกซ์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e9e21-139">Data Matrix</span></span>
    - <span data-ttu-id="e9e21-140">รหัส QR</span><span class="sxs-lookup"><span data-stu-id="e9e21-140">QR Code</span></span>

<span data-ttu-id="e9e21-141">เมื่อคุณตั้งค่าคอนฟิกแหล่งข้อมูล **บาร์โค้ด** คุณสามารถกำหนดพารามิเตอร์การแสดงภาพเฉพาะที่ใช้ในการสร้างรูปภาพ:</span><span class="sxs-lookup"><span data-stu-id="e9e21-141">When you configure a **Barcode** data source, you can define specific rendering parameters that are used to generate an image:</span></span>

- <span data-ttu-id="e9e21-142">**ความกว้าง** – ระบุความกว้างของบาร์โค้ดเป็นพิกเซล</span><span class="sxs-lookup"><span data-stu-id="e9e21-142">**Width** – Specify the bar code's width in pixels.</span></span> <span data-ttu-id="e9e21-143">ค่าเป็น **0** (ศูนย์) บ่งชี้ว่ามีการใช้ความกว้างเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e9e21-143">A value of **0** (zero) indicates that the default width is used.</span></span> <span data-ttu-id="e9e21-144">ความหมายอาจแตกต่างกันไปสำหรับรูปแบบที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="e9e21-144">The meaning can vary for different formats.</span></span>
- <span data-ttu-id="e9e21-145">**ความสูง** – ระบุความสูงของบาร์โค้ดเป็นพิกเซล</span><span class="sxs-lookup"><span data-stu-id="e9e21-145">**Height** – Specify the bar code's height in pixels.</span></span> <span data-ttu-id="e9e21-146">ค่าเป็น **0** (ศูนย์) บ่งชี้ว่ามีการใช้ความสูงเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e9e21-146">A value of **0** (zero) indicates that the default height is used.</span></span> <span data-ttu-id="e9e21-147">ความหมายอาจแตกต่างกันไปสำหรับรูปแบบที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="e9e21-147">The meaning can vary for different formats.</span></span>
- <span data-ttu-id="e9e21-148">**ระยะขอบ** – ระบุขนาดของระยะขอบของบาร์โค้ดเป็นพิกเซล</span><span class="sxs-lookup"><span data-stu-id="e9e21-148">**Margin** – Specify the size of the bar code's margin in pixels.</span></span> <span data-ttu-id="e9e21-149">ระยะขอบคือพื้นที่ในแต่ละด้านของบาร์โค้ดที่ต้องมีการเว้นไว้ (โซนเงียบ)</span><span class="sxs-lookup"><span data-stu-id="e9e21-149">The margin is the area on each side of a bar code that must be kept clear (quiet zone).</span></span> <span data-ttu-id="e9e21-150">ค่าเป็น **0** (ศูนย์) บ่งชี้ว่ามีการใช้ระยะขอบเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e9e21-150">A value of **0** (zero) indicates that the default margin is used.</span></span> <span data-ttu-id="e9e21-151">ความหมายอาจแตกต่างกันไปสำหรับรูปแบบที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="e9e21-151">The meaning can vary for different formats.</span></span>
- <span data-ttu-id="e9e21-152">**เนื้อหาของเอาต์พุต** – ตั้งค่าเป็น **ใช่** เพื่อสร้างรูปบาร์โค้ดที่มีข้อมูลที่เข้ารหัสเป็นข้อความ</span><span class="sxs-lookup"><span data-stu-id="e9e21-152">**Output content** – Set the value to **Yes** to generate a bar code image that contains the encoded information as text.</span></span> <span data-ttu-id="e9e21-153">ค่าเริ่มต้นคือ **ไม่**</span><span class="sxs-lookup"><span data-stu-id="e9e21-153">The default value is **No**.</span></span>
- <span data-ttu-id="e9e21-154">**การเข้ารหัส** – ระบุชนิดของอักขระที่ถูกเข้ารหัสในรูปของบาร์โค้ดที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="e9e21-154">**Encoding** – Specify the type of characters that are encoded in the generated bar code image.</span></span> <span data-ttu-id="e9e21-155">โดยค่าเริ่มต้น การเข้ารหัส **UTF-8** จะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="e9e21-155">By default, the **UTF-8** encoding is used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9e21-156">เมื่อคุณเพิ่มแหล่งข้อมูล **บาร์โค้ด** ใหม่ คุณต้องวางไว้ภายใต้สินค้าอื่น (คอนเทนเนอร์) เป็นองค์ประกอบที่ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="e9e21-156">When you add a new **Barcode** data source, you must place it under another item (container) as a nested element.</span></span>
>
> <span data-ttu-id="e9e21-157">เมื่อคุณผูกแหล่งข้อมูล **บาร์โค้ด** เข้ากับองค์ประกอบเซลล์ในรูปแบบ และองค์ประกอบเซลล์แสดงตัวควบคุมเนื้อหาของ Word หรือรูปภาพ Excel แหล่งข้อมูลจะแสดงอยู่ในการผูกข้อมูลนั้นเป็นฟังก์ชันที่มีพารามิเตอร์เดียวของชนิด **สตริง**</span><span class="sxs-lookup"><span data-stu-id="e9e21-157">When you bind a **Barcode** data source to a cell element in a format, and the cell element represents either a Word content control or an Excel picture, the data source is presented in that binding as a function that has a single parameter of the **String** type.</span></span> <span data-ttu-id="e9e21-158">คุณต้องใช้พารามิเตอร์นี้เพื่อระบุข้อความที่ควรถูกแปลงเป็นรูปบาร์โค้ด และอ่านเมื่อมีการสแกนบาร์โค้ดที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="e9e21-158">You must use this parameter to specify the text that should be transformed into a bar code image and read when a generated bar code is scanned.</span></span>

<span data-ttu-id="e9e21-159">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ให้ดำเนินการตัวอย่างในหัวข้อนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e9e21-159">For more information about this feature, complete the examples in this topic.</span></span>

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a><span data-ttu-id="e9e21-160">ตัวอย่าง: สร้างเช็คการชำระเงินที่มีบาร์โค้ดที่เข้ารหัสยอดเงินเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="e9e21-160">Example: Generate a payment check that contains a bar code that encodes the payable amount</span></span>

<span data-ttu-id="e9e21-161">ตัวอย่างนี้แสดงให้เห็นถึงวิธีการที่ผู้ใช้ในบทบาท **ผู้ดูแลระบบ** หรือ **ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์** สามารถตั้งค่าคอนฟิกรูปแบบ ER ซึ่งประกอบด้วยเท็มเพลตที่ใช้เพื่อสร้างเอกสารขาออกในรูปแบบ Excel ที่มีบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="e9e21-161">This example shows how a user in the **System administrator** or **Electronic reporting functional consultant** role can configure an ER format that contains a template that is used to generate an outbound document in Excel format that contains a bar code.</span></span> <span data-ttu-id="e9e21-162">ต่อไปนี้เป็นภาพรวมของขั้นตอนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="e9e21-162">Here is an overview of the steps that are involved.</span></span>

1. <span data-ttu-id="e9e21-163">[ดำเนินการข้อกำหนดเบื้องต้นให้เสร็จสมบูรณ์](#ExamplePrerequisites)</span><span class="sxs-lookup"><span data-stu-id="e9e21-163">[Complete the prerequisites](#ExamplePrerequisites).</span></span>
2. <span data-ttu-id="e9e21-164">[เรียกใช้ผู้ให้บริการการตั้งค่าคอนฟิก](#ExampleProvider)</span><span class="sxs-lookup"><span data-stu-id="e9e21-164">[Activate a configuration provider](#ExampleProvider).</span></span>
3. <span data-ttu-id="e9e21-165">[นำเข้าโซลูชัน ER ที่ระบุ](#ExampleImportSolution)</span><span class="sxs-lookup"><span data-stu-id="e9e21-165">[Import the provided ER solution](#ExampleImportSolution).</span></span>
4. <span data-ttu-id="e9e21-166">[สร้างเช็คการชำระเงิน](#ExampleGenerateCheque)</span><span class="sxs-lookup"><span data-stu-id="e9e21-166">[Generate a payment check](#ExampleGenerateCheque).</span></span>
5. <span data-ttu-id="e9e21-167">[รีวิวเช็คการชำระเงินที่สร้างขึ้น](#ExampleReviewGeneratedCheque)</span><span class="sxs-lookup"><span data-stu-id="e9e21-167">[Review the generated payment check](#ExampleReviewGeneratedCheque).</span></span>
6. <span data-ttu-id="e9e21-168">[ปรับเปลี่ยนรูปแบบของโซลูชัน ER ที่ระบุ](#ExampleModifyFormat)</span><span class="sxs-lookup"><span data-stu-id="e9e21-168">[Modify the format of the provided ER solution](#ExampleModifyFormat).</span></span>

    1. <span data-ttu-id="e9e21-169">[ใช้เท็มเพลตเช็คใหม่](#ExampleModifyFormatApplyTemplate)</span><span class="sxs-lookup"><span data-stu-id="e9e21-169">[Apply a new check template](#ExampleModifyFormatApplyTemplate).</span></span>
    2. <span data-ttu-id="e9e21-170">[เพิ่มแหล่งข้อมูลบาร์โค้ดใหม่](#ExampleModifyFormatAddDataSource)</span><span class="sxs-lookup"><span data-stu-id="e9e21-170">[Add a new Barcode data source](#ExampleModifyFormatAddDataSource).</span></span>
    3. <span data-ttu-id="e9e21-171">[ผูกองค์ประกอบรูปแบบใหม่](#ExampleModifyFormatBindFormatElement)</span><span class="sxs-lookup"><span data-stu-id="e9e21-171">[Bind a new format element](#ExampleModifyFormatBindFormatElement).</span></span>
    4. <span data-ttu-id="e9e21-172">[ทำให้รุ่นที่แก้ไขพร้อมใช้งานสำหรับการรันการทดสอบ](#ExampleModifyFormatMakeVersionAvailable)</span><span class="sxs-lookup"><span data-stu-id="e9e21-172">[Make the modified version available for test runs](#ExampleModifyFormatMakeVersionAvailable).</span></span>

        1. <span data-ttu-id="e9e21-173">[ดำเนินการรุ่นของรูปแบบที่แก้ไขให้เสร็จสมบูรณ์](#CompleteToRun)</span><span class="sxs-lookup"><span data-stu-id="e9e21-173">[Complete the modified format version](#CompleteToRun).</span></span>
        2. <span data-ttu-id="e9e21-174">[ทำให้รุ่นแบบร่างพร้อมสำหรับการใช้งาน](#MarkToRun)</span><span class="sxs-lookup"><span data-stu-id="e9e21-174">[Make the draft version available for use](#MarkToRun).</span></span>

7. <span data-ttu-id="e9e21-175">[สร้างเช็คการชำระเงิน](#ExampleGenerateCheque2)</span><span class="sxs-lookup"><span data-stu-id="e9e21-175">[Generate a payment check](#ExampleGenerateCheque2).</span></span>
8. <span data-ttu-id="e9e21-176">[แปลงเช็คที่สร้างขึ้นเป็น PDF](#ExampleConvertToPDF)</span><span class="sxs-lookup"><span data-stu-id="e9e21-176">[Convert the generated check to a PDF](#ExampleConvertToPDF).</span></span>

<span data-ttu-id="e9e21-177">ในตัวอย่างนี้ คุณจะใช้โซลูชัน ER ที่ระบุซึ่งถูกตั้งค่าคอนฟิกไว้เพื่อสร้างเช็คการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e9e21-177">In this example, you will use the provided ER solution that has been configured to generate payment checks.</span></span> <span data-ttu-id="e9e21-178">โซลูชันนี้จะสร้างเช็คการชำระเงินที่มีการเขียนยอดเงินเจ้าหนี้ทั้งเป็นตัวเลขและเป็นข้อความ</span><span class="sxs-lookup"><span data-stu-id="e9e21-178">This solution generates payment checks where the payable amount is written both as a number and as text.</span></span> <span data-ttu-id="e9e21-179">คุณจะปรับเปลี่ยนโซลูชัน ER นี้เพื่อให้เช็ครวมบาร์โค้ดที่สร้างขึ้นโดยที่มีการเข้ารหัสยอดเงินเจ้าหนี้และสามารถอ่านได้โดยใช้เครื่องสแกนบาร์โค้ดด้วย</span><span class="sxs-lookup"><span data-stu-id="e9e21-179">You will modify this ER solution so that the check also includes a generated bar code where the payable amount is encoded and can be read by using a bar code scanner.</span></span>

<span data-ttu-id="e9e21-180">ขั้นตอนสามารถถูกดำเนินการให้เสร็จสมบูรณ์ได้ในบริษัท **USMF** ใน Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="e9e21-180">The steps can be completed in the **USMF** company in Microsoft Dynamics 365 Finance.</span></span>

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a><span data-ttu-id="e9e21-181">ดำเนินการข้อกำหนดเบื้องต้นให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e9e21-181">Complete the prerequisites</span></span>

<span data-ttu-id="e9e21-182">เมื่อต้องการทำให้ตัวอย่างนี้เสร็จสมบูรณ์ คุณต้องเข้าถึงบริษัท USMF ในการเงินสำหรับหนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e9e21-182">To complete this example, you must have access to the USMF company in Finance for one of the following roles:</span></span>

- <span data-ttu-id="e9e21-183">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="e9e21-183">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="e9e21-184">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="e9e21-184">System administrator</span></span>

<span data-ttu-id="e9e21-185">ถ้าคุณยังไม่ได้ทำให้ตัวอย่างเสร็จสมบูรณ์ในหัวข้อ [ฝังข้อมูลและรูปร่างในเอกสารที่คุณสร้างโดยใช้ ER](electronic-reporting-embed-images-shapes.md) ให้ดาวน์โหลดการตั้งค่าคอนฟิกต่อไปนี้ของโซลูชัน ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e9e21-185">If you haven't yet completed the example in the [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md) topic, download the following configurations of the sample ER solution.</span></span>

| <span data-ttu-id="e9e21-186">คำอธิบายเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="e9e21-186">Content description</span></span>         | <span data-ttu-id="e9e21-187">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="e9e21-187">File name</span></span>                   |
|-----------------------------|-----------------------------|
| <span data-ttu-id="e9e21-188">การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER</span><span class="sxs-lookup"><span data-stu-id="e9e21-188">ER data model configuration</span></span> | <span data-ttu-id="e9e21-189">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="e9e21-189">Model for cheques.xml</span></span>       |
| <span data-ttu-id="e9e21-190">การตั้งค่าคอนฟิกรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="e9e21-190">ER format configuration</span></span>     | <span data-ttu-id="e9e21-191">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="e9e21-191">Cheques printing format.xml</span></span> |

<span data-ttu-id="e9e21-192">นอกจากนี้ ให้ดาวน์โหลดไฟล์ Excel ต่อไปนี้ที่มีเท็มเพลตที่แก้ไขสำหรับโซลูชัน ER ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="e9e21-192">Additionally, download the following Excel file that contains the modified template for the provided ER solution.</span></span>

| <span data-ttu-id="e9e21-193">คำอธิบายเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="e9e21-193">Content description</span></span> | <span data-ttu-id="e9e21-194">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="e9e21-194">File name</span></span>                 |
|---------------------|---------------------------|
| <span data-ttu-id="e9e21-195">เท็มเพลตรายงาน</span><span class="sxs-lookup"><span data-stu-id="e9e21-195">Report template</span></span>     | <span data-ttu-id="e9e21-196">Check template Excel.xlsx</span><span class="sxs-lookup"><span data-stu-id="e9e21-196">Check template Excel.xlsx</span></span> |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a><span data-ttu-id="e9e21-197">เรียกใช้ผู้ให้บริการการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="e9e21-197">Activate a configuration provider</span></span>

1. <span data-ttu-id="e9e21-198">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="e9e21-198">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e9e21-199">ในหน้า **การตั้งค่าคอนฟิกการแปลเป็นภาษาท้องถิ่น** ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** ตรวจสอบให้แน่ใจว่า [ผู้ให้บริการการตั้งค่าคอนฟิก](general-electronic-reporting.md#Provider) สำหรับบริษัทตัวอย่าง **Litware, Inc.** ถูกแสดงรายการและมีการทำเครื่องหมายเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="e9e21-199">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the [configuration provider](general-electronic-reporting.md#Provider) for the **Litware, Inc.** sample company is listed, and that it's marked as active.</span></span> <span data-ttu-id="e9e21-200">ถ้าไม่มีการแสดงรายการ หรือถ้าไม่ถูกทำเครื่องหมายเป็นใช้งานอยู่ ให้ทำตามขั้นตอนในหัวข้อ [สร้างผู้ให้บริการการตั้งค่าคอนฟิกและทำเครื่องหมายเป็นใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="e9e21-200">If it isn't listed, or if it isn't marked as active, follow the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic.</span></span>

![การตั้งค่าบริษัทตัวอย่างเป็นใช้งานอยู่ในหน้าการตั้งค่าคอนฟิกการแปลเป็นภาษาท้องถิ่น](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a><span data-ttu-id="e9e21-202">นำเข้าโซลูชัน ER ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="e9e21-202">Import the provided ER solution</span></span>

1. <span data-ttu-id="e9e21-203">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="e9e21-203">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e9e21-204">บนหน้า **การตั้งค่าคอนฟิกการแปลเป็นภาษาท้องถิ่น** ในส่วน **การตั้งค่าคอนฟิก** เลือกไทล์ **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="e9e21-204">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="e9e21-205">ในหน้า **การตั้งค่าคอนฟิก** ถ้าการตั้งค่าคอนฟิก **แบบจำลองสำหรับคิว** ไม่พร้อมใช้งานในแผนภูมิการตั้งค่าคอนฟิก ให้ทำตามขั้นตอนเหล่านี้เพื่อนำเข้าการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER</span><span class="sxs-lookup"><span data-stu-id="e9e21-205">On the **Configurations** page, if the **Model for cheques** configuration isn't available in the configuration tree, follow these steps to import the ER data model configuration:</span></span>

    1. <span data-ttu-id="e9e21-206">ในบานหน้าต่างการดำเนินการ เลือก **แลกเปลี่ยน** \> **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="e9e21-206">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="e9e21-207">ในกล่องโต้ตอบ เลือก **เรียกดู** ค้นหา และเลือกไฟล์ **Model for cheques.xml** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e9e21-207">In the dialog box, select **Browse**, find and select the **Model for cheques.xml** file, and then select **OK**.</span></span>

4. <span data-ttu-id="e9e21-208">ถ้าการตั้งค่าคอนฟิก **รูปแบบการพิมพ์เช็ค** ไม่พร้อมใช้งานในแผนภูมิการตั้งค่าคอนฟิก ให้ทำตามขั้นตอนเหล่านี้เพื่อนำเข้าการตั้งค่าคอนฟิกรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="e9e21-208">If the **Cheques printing format** configuration isn't available in the configuration tree, follow these steps to import the ER format configuration:</span></span>

    1. <span data-ttu-id="e9e21-209">ในบานหน้าต่างการดำเนินการ เลือก **แลกเปลี่ยน** \> **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="e9e21-209">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="e9e21-210">ในกล่องโต้ตอบ เลือก **เรียกดู** ค้นหา และเลือกไฟล์ **Cheques printing format.xml** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e9e21-210">In the dialog box, select **Browse**, find and select the **Cheques printing format.xml** file, and then select **OK**.</span></span>

5. <span data-ttu-id="e9e21-211">ในแผนภูมิการตั้งค่าคอนฟิก ขยาย **แบบจำลองสำหรับเช็ค**</span><span class="sxs-lookup"><span data-stu-id="e9e21-211">In the configuration tree, expand **Model for cheques**.</span></span>
6. <span data-ttu-id="e9e21-212">ตรวจทานรายการของการตั้งค่าคอนฟิก ER ที่นำเข้าในแผนภูมิการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="e9e21-212">Review the list of imported ER configurations in the configuration tree.</span></span>

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a><span data-ttu-id="e9e21-213">สร้างเช็คการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e9e21-213">Generate a payment check</span></span>

1. <span data-ttu-id="e9e21-214">ไปที่ **การจัดการเงินสดและธนาคาร** \> **บัญชีธนาคาร** \> **บัญชีธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="e9e21-214">Go to **Cash and bank management** \> **Bank accounts** \> **Bank accounts**.</span></span>
2. <span data-ttu-id="e9e21-215">บนหน้า **บัญชีธนาคาร** ให้เลือกบัญชี **USMF OPER**</span><span class="sxs-lookup"><span data-stu-id="e9e21-215">On the **Bank accounts** page, select the **USMF OPER** account.</span></span>
3. <span data-ttu-id="e9e21-216">ในหน้ารายละเอียดบัญชีธนาคาร บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่า** ในกลุ่ม **โครงร่าง** เลือก **เช็ค**</span><span class="sxs-lookup"><span data-stu-id="e9e21-216">On the bank account details page, on the Action Pane, on the **Set up** tab, in the **Layout** group, select **Check**.</span></span>
4. <span data-ttu-id="e9e21-217">บนหน้า **โครงร่างเช็ค** เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="e9e21-217">On the **Check layout** page, select **Edit**.</span></span>
5. <span data-ttu-id="e9e21-218">บน FastTab **ทั่วไป** ให้ตั้งค่าตัวเลือก **รูปแบบการส่งออกทางอิเล็กทรอนิกส์ทั่วไป** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="e9e21-218">On the **General** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
6. <span data-ttu-id="e9e21-219">ในฟิลด์ **การตั้งค่าคอนฟิกส่งออกรูปแบบ** ให้เลือกรูปแบบ ER **รูปแบบการพิมพ์เช็ค** ที่คุณนำเข้าก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e9e21-219">In the **Export format configuration** field, select the **Cheques printing format** ER format that you imported earlier.</span></span>
7. <span data-ttu-id="e9e21-220">ในบานหน้าต่างการดำเนินการ เลือก **การทดสอบการพิมพ์**</span><span class="sxs-lookup"><span data-stu-id="e9e21-220">On the Action Pane, select **Print test**.</span></span>
8. <span data-ttu-id="e9e21-221">ในกล่องโต้ตอบ ให้ตั้งค่าตัวเลือก **รูปแบบเช็คที่เปลี่ยนมือได้** เป็น **ใช่** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e9e21-221">In the dialog box, set the **Negotiable check format** option to **Yes**, and then select **OK**.</span></span>

    ![กล่องโต้ตอบโครงร่างเช็ค - การทดสอบการพิมพ์](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a><span data-ttu-id="e9e21-223">รีวิวเช็คการชำระเงินที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="e9e21-223">Review the generated payment check</span></span>

- <span data-ttu-id="e9e21-224">เปิดเช็คที่สร้างขึ้นใน Excel</span><span class="sxs-lookup"><span data-stu-id="e9e21-224">Open the generated check in Excel.</span></span>
2. <span data-ttu-id="e9e21-225">รีวิวเช็คที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="e9e21-225">Review the generated check.</span></span>

    ![เช็คการชำระเงินที่สร้างขึ้นใน Excel](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a><span data-ttu-id="e9e21-227">ปรับเปลี่ยนรูปแบบของโซลูชัน ER ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="e9e21-227">Modify the format of the provided ER solution</span></span>

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a><span data-ttu-id="e9e21-228">ใช้เท็มเพลตเช็คใหม่</span><span class="sxs-lookup"><span data-stu-id="e9e21-228">Apply a new check template</span></span>

<span data-ttu-id="e9e21-229">คุณสามารถใช้แอปพลิเคชันบนเดสก์ท็อปของ Excel เพื่อเปิดไฟล์ **Cheque template Excel.xlsx** ที่คุณนำเข้ามาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e9e21-229">You can use the Excel desktop application to open the **Cheque template Excel.xlsx** file that you imported earlier.</span></span> <span data-ttu-id="e9e21-230">โปรดสังเกตว่าเท็มเพลตนี้แตกต่างจากเท็มเพลตที่คุณใช้ในการสร้างเช็คการชำระเงินในโซลูชัน ER ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="e9e21-230">Notice that this template differs from the template that you used to generate a payment check in the provided ER solution.</span></span> <span data-ttu-id="e9e21-231">นอกจากนี้ ยังมีองค์ประกอบ **AmountBarcode** สำหรับรูปบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="e9e21-231">In addition, it includes an **AmountBarcode** element for the bar code image.</span></span>

![องค์ประกอบ AmountBarcode ในเท็มเพลต Excel](./media/er-barcode-data-source-cheque2.png)

<span data-ttu-id="e9e21-233">ขณะนี้คุณต้องปรับเปลี่ยนโซลูชัน ER แล้วจากนั้น [นำไปใช้อีกครั้ง](modify-electronic-reporting-format-reapply-excel-template.md) เท็มเพลตที่แก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="e9e21-233">You must now modify the ER solution and then [reapply](modify-electronic-reporting-format-reapply-excel-template.md) the modified template.</span></span>

1. <span data-ttu-id="e9e21-234">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="e9e21-234">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e9e21-235">บนหน้า **การตั้งค่าคอนฟิกการแปลเป็นภาษาท้องถิ่น** ในส่วน **การตั้งค่าคอนฟิก** เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="e9e21-235">On the **Localization configurations** page, in the **Configurations** section, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="e9e21-236">ในหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก ขยาย **แบบจำลองสำหรับเช็ค** และเลือก **รูปแบบการพิมพ์เช็ค**</span><span class="sxs-lookup"><span data-stu-id="e9e21-236">On the **Configurations** page, in the configuration tree, expand **Model for cheques**, and select **Cheques printing format**.</span></span>
4. <span data-ttu-id="e9e21-237">บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="e9e21-237">On the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="e9e21-238">ในตัวออกแบบการดำเนินงาน ER เลือกแท็บ **การแม็ป** ทางด้านขวาของหน้า และจากนั้น ในบานหน้าต่างแผนภูมิรูปแบบทางด้านซ้าย ให้เลือก **ขยาย/ยุบ**</span><span class="sxs-lookup"><span data-stu-id="e9e21-238">In the ER Operations designer, select the **Mapping** tab on the right side of the page, and then, in the format tree pane on the left, select **Expand/collapse**.</span></span>
6. <span data-ttu-id="e9e21-239">โปรดสังเกตว่าองค์ประกอบรูปแบบเซลล์ทั้งหมดจะถูกผูกไว้กับแหล่งข้อมูลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="e9e21-239">Notice that all cell format elements are bound to the appropriate data sources.</span></span>

    ![การผูกองค์ประกอบรูปแบบเซลล์กับแหล่งข้อมูลในตัวออกแบบการดำเนินการ ER](./media/er-barcode-data-source-cells-bound.png)

7. <span data-ttu-id="e9e21-241">เลือกแท็บ **รูปแบบ** ทางด้านขวาของหน้า</span><span class="sxs-lookup"><span data-stu-id="e9e21-241">Select the **Format** tab on the right side of the page.</span></span>
8. <span data-ttu-id="e9e21-242">ในบานหน้าต่างการดำเนินการ ให้เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="e9e21-242">On the Action Pane, select the ellipsis (**...**), and then select **Import**.</span></span>
9. <span data-ttu-id="e9e21-243">ในกลุ่ม **นำเข้า** เลือก **ปรับปรุงจาก Excel** และจากนั้น เลือก **ปรับปรุงเท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="e9e21-243">In the **Import** group, select **Update from Excel**, and then select **Update template**.</span></span>
10. <span data-ttu-id="e9e21-244">ในกล่องโต้ตอบ ให้เลือกดูไฟล์ **Cheque template Excel.xlsx** ที่บันทึกไว้บนคอมพิวเตอร์ของคุณ ให้เลือกไฟล์นั้น และจากนั้น เลือก **ตกลง** เพื่อยืนยันว่าควรใช้เท็มเพลตที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e9e21-244">In the dialog box, browse to the **Cheque template Excel.xlsx** file that is saved on your computer, select it, and then select **OK** to confirm that the selected template should be applied.</span></span>
11. <span data-ttu-id="e9e21-245">เลือกแท็บ **การแม็ป** ทางด้านขวาของหน้า และจากนั้น ในบานหน้าต่างแผนภูมิรูปแบบทางด้านซ้าย ให้เลือก **ขยาย/ยุบ**</span><span class="sxs-lookup"><span data-stu-id="e9e21-245">Select the **Mapping** tab on the right side of the page, and then, in the format tree pane on the left, select **Expand/collapse**.</span></span>
12. <span data-ttu-id="e9e21-246">โปรดสังเกตว่ามีการเพิ่มองค์ประกอบเซลล์ **AmountBarcode** ลงในรูปแบบแล้ว</span><span class="sxs-lookup"><span data-stu-id="e9e21-246">Notice that the **AmountBarcode** cell element has been added to the format.</span></span> <span data-ttu-id="e9e21-247">องค์ประกอบนี้สัมพันธ์กับองค์ประกอบ **AmountBarcode** ซึ่งถูกเพิ่มลงในเท็มเพลต Excel ที่แก้ไขแล้วเป็นตัวยึดสำหรับรูปบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="e9e21-247">This element is associated with the **AmountBarcode** element that has been added to the modified Excel template as a placeholder for a bar code image.</span></span>

    ![มีการเพิ่มองค์ประกอบเซลล์ AmountBarcode ไปยังรูปแบบในตัวออกแบบการดำเนินการ ER](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a><span data-ttu-id="e9e21-249">เพิ่มแหล่งข้อมูลบาร์โค้ดใหม่</span><span class="sxs-lookup"><span data-stu-id="e9e21-249">Add a new Barcode data source</span></span>

<span data-ttu-id="e9e21-250">ถัดไป คุณต้องเพิ่มแหล่งข้อมูลใหม่ของชนิด **บาร์โค้ด**</span><span class="sxs-lookup"><span data-stu-id="e9e21-250">Next, you must add a new data source of the **Barcode** type.</span></span>

1. <span data-ttu-id="e9e21-251">ในตัวออกแบบการดำเนินการ ER บนแท็บ **การแม็ป** ทางด้านขวาของหน้า ให้เลือกแหล่งข้อมูล **พิมพ์**</span><span class="sxs-lookup"><span data-stu-id="e9e21-251">In the ER Operations designer, on the **Mapping** tab on the right side of the page, select the **print** data source.</span></span>
2. <span data-ttu-id="e9e21-252">เลือก **เพิ่ม** และจากนั้น ในกลุ่ม **ฟังก์ชัน** ให้เลือกชนิดแหล่งข้อมูลของ **บาร์โค้ด**</span><span class="sxs-lookup"><span data-stu-id="e9e21-252">Select **Add**, and then, in the **Functions** group, select the **Barcode** data source type.</span></span>

    ![การเลือกชนิดแหล่งข้อมูลของบาร์โค้ด](./media/er-barcode-data-source-add.png)

3. <span data-ttu-id="e9e21-254">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **บาร์โค้ด**</span><span class="sxs-lookup"><span data-stu-id="e9e21-254">In the dialog box, in the **Name** field, enter **barcode**.</span></span>
4. <span data-ttu-id="e9e21-255">ใน **รูปแบบบาร์โค้ด** เลือก **รหัส 128**</span><span class="sxs-lookup"><span data-stu-id="e9e21-255">In the **Barcode format**, select **Code 128**.</span></span>
5. <span data-ttu-id="e9e21-256">ในฟิลด์ **ความกว้าง** ป้อน **500**</span><span class="sxs-lookup"><span data-stu-id="e9e21-256">In the **Width** field, enter **500**.</span></span>
6. <span data-ttu-id="e9e21-257">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e9e21-257">Select **OK**.</span></span>

    ![กล่องโต้ตอบคุณสมบัติแหล่งข้อมูล](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a><span data-ttu-id="e9e21-259">ผูกองค์ประกอบรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="e9e21-259">Bind a new format element</span></span>

<span data-ttu-id="e9e21-260">ถัดไป คุณต้องผูกองค์ประกอบรูปแบบใหม่ไปยังแหล่งข้อมูลที่คุณเพิ่งเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="e9e21-260">Next, you must bind the new format element to the data source that you just added.</span></span>

1. <span data-ttu-id="e9e21-261">ในตัวออกแบบการดำเนินการ ER บนแท็บ **การแม็ป** ทางด้านขวาของหน้า ให้เลือกแหล่งข้อมูล **พิมพ์\\บาร์โค้ด**</span><span class="sxs-lookup"><span data-stu-id="e9e21-261">In the ER Operations designer, on the **Mapping** tab on the right side of the page, select the **print\\barcode** data source.</span></span>
2. <span data-ttu-id="e9e21-262">ในบานหน้าต่างแผนภูมิรูปแบบทางด้านซ้าย ให้เลือกองค์ประกอบเซลล์ **AmountBarcode** แล้วจากนั้น เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="e9e21-262">In the format tree pane on the left, select the **AmountBarcode** cell element, and then select **Bind**.</span></span>
3. <span data-ttu-id="e9e21-263">บนบานหน้าต่างการดำเนินการ เลือก **แสดงรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="e9e21-263">On the Action Pane, select **Show details**.</span></span>
4. <span data-ttu-id="e9e21-264">โปรดสังเกตว่า เนื่องจากแหล่งข้อมูล **บาร์โค้ด** แสดงอยู่ในการผูกข้อมูลเป็นฟังก์ชันที่มีพารามิเตอร์เดียว มีการใช้ชื่อขององค์ประกอบรูปแบบที่ผูกข้อมูลเป็นอาร์กิวเมนต์ของพารามิเตอร์ดังกล่าวโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e9e21-264">Notice that, because the **Barcode** data source is represented in the binding as a function that contains a single parameter, the name of the bound format element has been automatically taken as the argument of that parameter.</span></span>

    ![รายละเอียดของแหล่งข้อมูลบาร์โค้ดในโปรแกรมออกแบบการดำเนินการ ER](./media/er-barcode-data-source-bind1.png)

5. <span data-ttu-id="e9e21-266&quot;>เลือก **แก้ไขสูตร** เพื่อปรับปรุงการผูกข้อมูล</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e9e21-266&quot;>Select **Edit formula** to adjust the binding.</span></span>

    <span data-ttu-id=&quot;e9e21-267&quot;>คุณไม่ต้องการให้มีการส่งคืนชื่อขององค์ประกอบเซลล์</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e9e21-267&quot;>You don't want the name of the cell element to be returned.</span></span> <span data-ttu-id=&quot;e9e21-268&quot;>ดังนั้น คุณต้องตั้งค่าคอนฟิกนิพจน์ที่ส่งคืนข้อความที่มียอดเงินเจ้าหนี้ของเช็คปัจจุบัน</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e9e21-268&quot;>Therefore, you must configure an expression that returns text that contains the payable amount of the current check.</span></span> <span data-ttu-id=&quot;e9e21-269&quot;>เนื่องจากช่วง **ChequeLines** หลักถูกผูกไว้กับแหล่งข้อมูล **model.cheques** ยอดเงินเจ้าหนี้ของเช็คปัจจุบันจะพร้อมใช้งานในฟิลด์ **model.cheques.attributes.amount** ของชนิดข้อมูล **จริง**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e9e21-269&quot;>Because the parent **ChequeLines** range is bound to the **model.cheques** data source, the payable amount of the current check is available in the **model.cheques.attributes.amount** field of the **Real** data type.</span></span>

6. <span data-ttu-id=&quot;e9e21-270&quot;>ในฟิลด์ **สูตร** ให้ป้อน **print.barcode(NUMBERFORMAT(@.attributes.amount, &quot;F2"))**</span><span class="sxs-lookup"><span data-stu-id="e9e21-270">In the **Formula** field, enter **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))**.</span></span>
7. <span data-ttu-id="e9e21-271">เลือก **บันทึก** และจากนั้น ปิด [ตัวออกแบบสูตร ER](general-electronic-reporting-formula-designer.md)</span><span class="sxs-lookup"><span data-stu-id="e9e21-271">Select **Save**, and then close the [ER Formula designer](general-electronic-reporting-formula-designer.md).</span></span>
8. <span data-ttu-id="e9e21-272">โปรดสังเกตว่ามีการปรับปรุงการผูกข้อมูลแล้ว</span><span class="sxs-lookup"><span data-stu-id="e9e21-272">Notice that the binding has been adjusted.</span></span>

    ![การผูกข้อมูลที่ปรับปรุงในตัวออกแบบการดำเนินการ ER](./media/er-barcode-data-source-bind2.png)

9. <span data-ttu-id="e9e21-274">เลือก **บันทึก** และจากนั้น ปิดตัวออกแบบการดำเนินการ ER</span><span class="sxs-lookup"><span data-stu-id="e9e21-274">Select **Save**, and then close the ER Operations designer.</span></span>

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a><span data-ttu-id="e9e21-275">ทำให้รุ่นที่แก้ไขพร้อมใช้งานสำหรับการรันการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="e9e21-275">Make the modified version available for test runs</span></span>

<span data-ttu-id="e9e21-276">โดยค่าเริ่มต้น จะมีการใช้เฉพาะรุ่นที่มีสถานะเป็น **เสร็จสมบูรณ์** และ **ใช้ร่วมกัน** เมื่อคุณรันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="e9e21-276">By default, the only versions that have a status of **Completed** and **Shared** are used when you run an ER format.</span></span>

<span data-ttu-id="e9e21-277">ถ้าคุณได้ทำการเปลี่ยนแปลงขั้นสุดท้ายแล้ว คุณสามารถทำงานของคุณให้เสร็จสมบูรณ์ได้โดยใช้รุ่นแบบร่างปัจจุบันและทำให้การเปลี่ยนแปลงของคุณพร้อมสำหรับการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e9e21-277">If you've finalized your changes, you can complete your work with the current draft version and make your changes available for use.</span></span> <span data-ttu-id="e9e21-278">สำหรับคำแนะนำ ให้ดูที่ส่วน [ทำให้รุ่นของรูปแบบที่แก้ไขเสร็จสมบูรณ์](#CompleteToRun) ที่อยู่ในลำดับต่อมา</span><span class="sxs-lookup"><span data-stu-id="e9e21-278">For instructions, see the [Complete the modified format version](#CompleteToRun) section that follows.</span></span>

<span data-ttu-id="e9e21-279">ถ้าคุณต้องการทำงานกับรุ่นแบบร่างปัจจุบันต่อไป แต่คุณต้องใช้ในการสร้างเช็ค คุณจะต้องระบุอย่างชัดแจ้งว่าคุณต้องการใช้รุ่นแบบร่างของรูปแบบสำหรับการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="e9e21-279">If you want to continue to work with the current draft version, but you have to use it to generate checks, you must explicitly specify that you want to use the draft version of the format for execution.</span></span> <span data-ttu-id="e9e21-280">สำหรับคำแนะนำ ให้ดูที่ส่วน [ทำให้รุ่นแบบร่างพร้อมสำหรับการใช้งาน](#MarkToRun)</span><span class="sxs-lookup"><span data-stu-id="e9e21-280">For instructions, see the [Make the draft version available for use](#MarkToRun) section.</span></span>

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a><span data-ttu-id="e9e21-281">ดำเนินการรุ่นของรูปแบบที่แก้ไขให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e9e21-281">Complete the modified format version</span></span>

1. <span data-ttu-id="e9e21-282">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="e9e21-282">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e9e21-283">บนหน้า **การตั้งค่าคอนฟิกการแปลเป็นภาษาท้องถิ่น** ในส่วน **การตั้งค่าคอนฟิก** เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="e9e21-283">On the **Localization configurations** page, in the **Configurations** section, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="e9e21-284">ในหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก ขยาย **แบบจำลองสำหรับเช็ค** และเลือก **รูปแบบการพิมพ์เช็ค**</span><span class="sxs-lookup"><span data-stu-id="e9e21-284">On the **Configurations** page, in the configuration tree, expand **Model for cheques**, and select **Cheques printing format**.</span></span>
4. <span data-ttu-id="e9e21-285">บน FastTab **รุ่น** ให้เลือกเรกคอร์ดที่มีสถานะเป็น **ร่าง**</span><span class="sxs-lookup"><span data-stu-id="e9e21-285">On the **Versions** FastTab, select the record that has a status of **Draft**.</span></span>
5. <span data-ttu-id="e9e21-286">เลือก **เปลี่ยนสถานะ** และจากนั้น เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="e9e21-286">Select **Change status**, and then select **Complete**.</span></span>
6. <span data-ttu-id="e9e21-287">ในกล่องโต้ตอบ ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e9e21-287">In the dialog box, select **OK**.</span></span>

<span data-ttu-id="e9e21-288">สถานะของรุ่นปัจจุบันถูกเปลี่ยนจาก **ร่าง** เป็น **เสร็จสมบูรณ์** และมีการสร้างรุ่นใหม่ที่มีสถานะเป็น **ร่าง**</span><span class="sxs-lookup"><span data-stu-id="e9e21-288">The status of the current version is changed from **Draft** to **Completed**, and a new version that has a status of **Draft** is created.</span></span> <span data-ttu-id="e9e21-289">คุณสามารถใช้รุ่นแบบร่างใหม่นี้เพื่อใช้การเปลี่ยนแปลงเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="e9e21-289">You can use this new draft version to apply additional changes.</span></span>

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a><span data-ttu-id="e9e21-290">ทำให้รุ่นแบบร่างพร้อมสำหรับการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e9e21-290">Make the draft version available for use</span></span>

1. <span data-ttu-id="e9e21-291">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="e9e21-291">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e9e21-292">บนหน้า **การตั้งค่าคอนฟิกการแปลเป็นภาษาท้องถิ่น** ในส่วน **การตั้งค่าคอนฟิก** เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="e9e21-292">On the **Localization configurations** page, in the **Configurations** section, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="e9e21-293">บนหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ ในแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าขั้นสูง** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="e9e21-293">On the **Configurations** page, on the Action Pane, in the **Configurations** tab, in the **Advance settings** group, select **User parameters**.</span></span>
4. <span data-ttu-id="e9e21-294">ในกล่องโต้ตอบ ให้ตั้งค่าตัวเลือก **เรียกใช้การตั้งค่า** เป็น **ใช่** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e9e21-294">In the dialog box, set the **Run setting** options to **Yes**, and then select **OK**.</span></span>
5. <span data-ttu-id="e9e21-295">ในแผนภูมิการตั้งค่าคอนฟิก ขยาย **แบบจำลองสำหรับเช็ค** และเลือก **รูปแบบการพิมพ์เช็ค**</span><span class="sxs-lookup"><span data-stu-id="e9e21-295">In the configuration tree, expand **Model for cheques**, and select **Cheques printing format**.</span></span>
6. <span data-ttu-id="e9e21-296">ตั้งค่าตัวเลือก **เรียกใช้แบบร่าง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="e9e21-296">Set the **Run draft** option to **Yes**.</span></span>
7. <span data-ttu-id="e9e21-297">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="e9e21-297">Select **Save**.</span></span>

<span data-ttu-id="e9e21-298">รุ่นแบบร่างของรูปแบบที่เลือกถูกทำเครื่องหมายเป็นพร้อมสำหรับการใช้งาน เมื่อมีการรันรูปแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e9e21-298">The draft version of the selected format is marked as available for use when the selected format is run.</span></span>

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a><span data-ttu-id="e9e21-299">สร้างเช็คการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e9e21-299">Generate a payment check</span></span>

1. <span data-ttu-id="e9e21-300">ไปที่ **การจัดการเงินสดและธนาคาร** \> **บัญชีธนาคาร** \> **บัญชีธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="e9e21-300">Go to **Cash and bank management** \> **Bank accounts** \> **Bank accounts**.</span></span>
2. <span data-ttu-id="e9e21-301">บนหน้า **บัญชีธนาคาร** ให้เลือกบัญชี **USMF OPER**</span><span class="sxs-lookup"><span data-stu-id="e9e21-301">On the **Bank accounts** page, select the **USMF OPER** account.</span></span>
3. <span data-ttu-id="e9e21-302">ในหน้ารายละเอียดบัญชีธนาคาร บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่า** ในกลุ่ม **โครงร่าง** เลือก **เช็ค**</span><span class="sxs-lookup"><span data-stu-id="e9e21-302">On the bank account details page, on the Action Pane, on the **Set up** tab, in the **Layout** group, select **Check**.</span></span>
4. <span data-ttu-id="e9e21-303">บนหน้า **โครงร่างเช็ค** บนบานหน้าต่างการดำเนินการ ให้เลือก **การทดสอบการพิมพ์**</span><span class="sxs-lookup"><span data-stu-id="e9e21-303">On the **Check layout** page, on the Action Pane, select **Print test**.</span></span>
5. <span data-ttu-id="e9e21-304">ในกล่องโต้ตอบ ให้ตั้งค่าตัวเลือก **รูปแบบเช็คที่เปลี่ยนมือได้** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="e9e21-304">In the dialog box, set the **Negotiable check format** option to **Yes**.</span></span>
6. <span data-ttu-id="e9e21-305">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e9e21-305">Select **OK**.</span></span>
7. <span data-ttu-id="e9e21-306">รีวิวเช็คที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="e9e21-306">Review the generated check.</span></span> <span data-ttu-id="e9e21-307">โปรดสังเกตว่ามีการสร้างบาร์โค้ดเพื่อเข้ารหัสยอดเงินเจ้าหนี้ของเช็ค</span><span class="sxs-lookup"><span data-stu-id="e9e21-307">Notice that a bar code has been generated to encode the payable amount of the check.</span></span>

    ![เช็คการชำระเงินที่สร้างโดยมีบาร์โค้ดใน Excel](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> <span data-ttu-id="e9e21-309">ข้อยกเว้นแสดงขึ้น ถ้าอาร์กิวเมนต์ของแหล่งข้อมูล **บาร์โค้ด** ไม่สอดคล้องกับความต้องการที่เหมาะสมที่เฉพาะเจาะจงสำหรับรูปแบบบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="e9e21-309">An exception is thrown if the argument of a **Barcode** data source doesn't comply with the appropriate requirements that are specific to the bar code format.</span></span> <span data-ttu-id="e9e21-310">ตัวอย่างเช่น เมื่อมีการเรียกแหล่งข้อมูล **บาร์โค้ด** เพื่อสร้างบาร์โค้ด [EAN-8](https://wikipedia.org/wiki/EAN-8) สำหรับข้อความที่ระบุ ข้อยกเว้นจะแสดงขึ้น ถ้าความยาวของข้อความเกินเจ็ดอักขระ</span><span class="sxs-lookup"><span data-stu-id="e9e21-310">For example, when the **Barcode** data source is called to generate an [EAN-8](https://wikipedia.org/wiki/EAN-8) bar code for the provided text, an exception is thrown if the length of the text exceeds seven characters.</span></span>

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a><span data-ttu-id="e9e21-311">แปลงเช็คที่สร้างขึ้นเป็น PDF</span><span class="sxs-lookup"><span data-stu-id="e9e21-311">Convert the generated check to a PDF</span></span>

<span data-ttu-id="e9e21-312">ตามที่อธิบายไว้ในหัวข้อ [สร้างฟอร์ม FTI ที่สามารถพิมพ์ได้](er-generate-printable-fti-forms.md#finland) คุณสามารถใช้แบบอักษรพิเศษในการผลิตบาร์โค้ดในเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="e9e21-312">As described in the [Generate printable FTI forms](er-generate-printable-fti-forms.md#finland) topic, you can use a special font to produce bar codes in a generated document.</span></span> <span data-ttu-id="e9e21-313">ในกรณีนี้ การแปลงเพิ่มเติมของเอกสารที่สร้างขึ้นอาจขึ้นอยู่กับความพร้อมใช้งานของแบบอักษรดังกล่าวในสภาพแวดล้อมการแปลง</span><span class="sxs-lookup"><span data-stu-id="e9e21-313">In this case, additional transformations of the generated document might depend on the availability of that font in the transformation environment.</span></span> <span data-ttu-id="e9e21-314">ตัวอย่างเช่น ถ้าคุณพยายามแปลงเอกสารเป็นรูปแบบ PDF หรือพรีวิวในสภาพแวดล้อมที่ซึ่งแบบอักษรขาดหายไป บาร์โค้ดจะไม่ถูกแสดงอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e9e21-314">For example, if you try to convert a document to PDF format or preview it in an environment where the font is missing, bar codes won't be rendered correctly.</span></span>

<span data-ttu-id="e9e21-315">อย่างไรก็ตาม เมื่อคุณใช้แหล่งข้อมูล **บาร์โค้ด** เพื่อผลิตบาร์โค้ด การแสดงภาพของบาร์โค้ดเหล่านั้นจะไม่ขึ้นอยู่กับแบบอักษรใดๆ</span><span class="sxs-lookup"><span data-stu-id="e9e21-315">However, when you use the **Barcode** data source to produce bar codes, the rendering of those bar codes doesn't depend on any font.</span></span> <span data-ttu-id="e9e21-316">ดังนั้น คุณจึงสามารถแปลงเอกสารที่มีบาร์โค้ดเป็นรูปแบบไฟล์ PDF ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="e9e21-316">Therefore, you can easily convert documents that contain the bar codes to PDF format.</span></span> <span data-ttu-id="e9e21-317">ภาพประกอบต่อไปนี้แสดงพรีวิวของเช็คการชำระเงินที่สร้างขึ้น ซึ่งมีการ [แปลง](electronic-reporting-destinations.md#OutputConversionToPDF) เป็น PDF โดยยึดตามการตั้งค่าของ [ปลายทาง](electronic-reporting-destinations.md) ER ที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="e9e21-317">The following illustration shows the preview of a generated payment check that has been [converted](electronic-reporting-destinations.md#OutputConversionToPDF) to a PDF, based on the setting of the configured ER [destination](electronic-reporting-destinations.md).</span></span>

![พรีวิวของ PDF ของเช็คการชำระเงิน](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a><span data-ttu-id="e9e21-319">การจำกัด</span><span class="sxs-lookup"><span data-stu-id="e9e21-319">Limitations</span></span>

> [!NOTE]
> <span data-ttu-id="e9e21-320">บาร์โค้ดบางชนิดที่ถูกสร้างไว้ มีอัตราส่วนกว้างยาวคงที่</span><span class="sxs-lookup"><span data-stu-id="e9e21-320">Some types of bar codes that are generated have a fixed aspect ratio.</span></span> <span data-ttu-id="e9e21-321">ลักษณะการทำงานเหมาะสม หากคุณได้เปิดใช้งานคุณลักษณะ **เปิดการใช้งานไลบรารี EPPlus ในกรอบงานการรายงานทางอิเล็กทรอนิกส์** เพื่อทำงานกับเอกสาร EXCEL ใน ER</span><span class="sxs-lookup"><span data-stu-id="e9e21-321">This behavior makes sense if you've turned on the **Enable usage of EPPlus library in Electronic reporting framework** feature to work with Excel documents in ER.</span></span> <span data-ttu-id="e9e21-322">ในกรณีดังกล่าว จะมีการป้อนรูปภาพเป็นตัวยึดตำแหน่งที่มีอัตราส่วนกว้างยาวที่ถูกล็อค</span><span class="sxs-lookup"><span data-stu-id="e9e21-322">In that case, an image is entered into a placeholder that has a locked aspect ratio.</span></span> <span data-ttu-id="e9e21-323">ดังนั้น เมื่อมิติของตัวยึดตำแหน่งในเท็มเพลตสอดคล้องกับอัตราส่วนของรูปภาพที่ป้อนไว้ ภาพจริงในเอกสารที่สร้างขึ้นอาจถูกปรับขนาดเพื่อรักษาอัตราส่วนกว้างยาวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="e9e21-323">Therefore, when the dimensions of a placeholder in a template correspond to the ratio of an image that is entered, a real picture in a generated document might be resized to maintain the required aspect ratio.</span></span> <span data-ttu-id="e9e21-324">เมื่อต้องการป้องกันการปรับขนาดรูปภาพ ให้ใช้ตัวยึดตำแหน่งที่มีอัตราส่วนกว้างยาวที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="e9e21-324">To prevent picture resizing, use a placeholder that has an expected aspect ratio.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9e21-325">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e9e21-325">Additional resources</span></span>

- [<span data-ttu-id="e9e21-326">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="e9e21-326">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e9e21-327">ปลายทางการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="e9e21-327">Electronic Reporting destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="e9e21-328">ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="e9e21-328">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="e9e21-329">ฟังก์ชัน NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="e9e21-329">NUMBERFORMAT function</span></span>](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]