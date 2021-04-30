---
title: ออกแบบการตั้งค่าคอนฟิก ER เพื่อระงับอักขระ BOM ในไฟล์ที่สร้างขึ้น
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานที่ระงับอักขระเครื่องหมายการจัดลำดับไบต์ (BOM)
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5ada93c0192aadac70c38c8c8c4f3af86ff6fc3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893287"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="c896d-103">ออกแบบการตั้งค่าคอนฟิก ER เพื่อระงับอักขระ BOM ในไฟล์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c896d-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c896d-104">คุณสามารถออกแบบ [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) [โซลูชัน](er-quick-start1-new-solution.md) เพื่อสร้างเอกสารขาออกได้</span><span class="sxs-lookup"><span data-stu-id="c896d-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="c896d-105">เมื่อต้องการสร้างเอกสารเป็นไฟล์ข้อความหรือไฟล์ XML โซลูชันต้องรวม [การตั้งค่าคอนฟิก](general-electronic-reporting.md#Configuration) ER ที่มีส่วนประกอบ [รูปแบบ](general-electronic-reporting.md#FormatComponentOutbound) ER</span><span class="sxs-lookup"><span data-stu-id="c896d-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="c896d-106">เมื่อต้องการระบุ [การเข้ารหัสอักขระ](/windows/win32/intl/character-sets) ที่แสดงถึงชุดของอักขระในไฟล์ที่สร้างขึ้น รูปแบบ ER ต้องมีองค์ประกอบรูปแบบ **ทั่วไป\\ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="c896d-106">To specify the [character encoding](/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="c896d-107">เมื่อต้องการตั้งค่าคอนฟิกส่วนประกอบรูปแบบ ER ให้เปิดเวอร์ชัน [แบบร่าง](general-electronic-reporting.md#component-versioning) ของการตั้งค่าคอนฟิก ER ในโปรแกรมออกแบบรูปแบบ ER และเพิ่มองค์ประกอบ **ทั่วไป\\ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="c896d-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="c896d-108">ในฟิลด์ **การเข้ารหัส** ให้ระบุการเข้ารหัสไฟล์ขาออกที่สร้างขณะรันไทม์ โดยใช้ส่วนประกอบนี้</span><span class="sxs-lookup"><span data-stu-id="c896d-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="c896d-109">ถ้ารูปแบบมีชื่อการเข้ารหัสที่ไม่ถูกต้อง ระบบจะแสดงข้อผิดพลาดเมื่อคุณบันทึกการเปลี่ยนแปลงของคุณไปยังการตั้งค่าของรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="c896d-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![การเพิ่มองค์ประกอบรากบนหน้าตัวออกแบบรูปแบบ](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="c896d-111">ถ้าคุณระบุ **UTF-8** **UTF-16** หรือ **UTF-32** เป็นการเข้ารหัส ตัวเลือก **ระงับอักขระ BOM** จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c896d-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="c896d-112">ตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อระงับ [เครื่องหมายการจัดลำดับไบต์ (BOM)](/globalization/encoding/byte-order-mark) ในไฟล์ขาออกที่สร้างขึ้นขณะรันไทม์ เมื่อรันรูปแบบ ER ที่แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="c896d-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="c896d-113">ถ้าคุณปล่อยฟิลด์ **การเข้ารหัส** ว่างไว้ จะมีการใช้การเข้ารหัส **UTF-8** ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c896d-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![การตั้งค่าตัวเลือกระงับอักขระ BOM ในหน้าโปรแกรมออกแบบรูปแบบ](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="c896d-115">หากต้องการทบทวนฟังก์ชันรันไทม์ ให้ปฏิบัติตามขั้นตอนที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="c896d-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="c896d-116">ตัวอย่างเช่น ปฏิบัติตามขั้นตอนต่างๆ ในหัวข้อ [เลื่อนการดำเนินการขององค์ประกอบ XML ในรูปแบบ ER](er-defer-xml-element.md)</span><span class="sxs-lookup"><span data-stu-id="c896d-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="c896d-117">หลังจากที่คุณได้เสร็จสิ้นขั้นตอนในส่วน [แก้ไขรูปแบบเพื่อให้การคํานวณเป็นไปตามผลลัพธ์ที่สร้างขึ้น](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) ของหัวข้อนั้น ให้ปฏิบัติตามขั้นตอนเพิ่มเติมเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c896d-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="c896d-118">ระบุการเข้ารหัส UTF:</span><span class="sxs-lookup"><span data-stu-id="c896d-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="c896d-119">เลือกองค์ประกอบ **รายงาน** ของชนิด **ทั่วไป\\ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="c896d-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="c896d-120">ในฟิลด์บัญชี **การเข้ารหัส** ให้ระบุการเข้ารหัส **UTF-8**</span><span class="sxs-lookup"><span data-stu-id="c896d-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="c896d-121">สร้างไฟล์ XML ที่รวมอักขระ BOM:</span><span class="sxs-lookup"><span data-stu-id="c896d-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="c896d-122">ตั้งค่าตัวเลือก **ระงับอักขระ BOM** เป็น **ไม่** เพื่อรวมอักขระ BOM ในไฟล์ XML ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c896d-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="c896d-123">เสร็จสิ้นขั้นตอนในส่วน [เลื่อนการดำเนินการขององค์ประกอบ XML สรุป เพื่อให้สามารถใช้ยอดรวมที่คำนวณได้](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) ของหัวข้อ [เลื่อนการดำเนินการขององค์ประกอบ XML ในรูปแบบการรายงานทางอิเล็กทรอนิกส์](er-defer-xml-element.md) และบันทึกไฟล์ที่สร้างเป็น **SampleXmlReport.xml**</span><span class="sxs-lookup"><span data-stu-id="c896d-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="c896d-124">สร้างไฟล์ XML ที่ไม่รวมอักขระ BOM:</span><span class="sxs-lookup"><span data-stu-id="c896d-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="c896d-125">ตั้งค่าตัวเลือก **ระงับอักขระ BOM** เป็น **ใช่** เพื่อระงับอักขระ BOM ในไฟล์ XML ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c896d-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="c896d-126">เสร็จสิ้นขั้นตอนในส่วน [เลื่อนการดำเนินการขององค์ประกอบ XML สรุป เพื่อให้สามารถใช้ยอดรวมที่คำนวณได้](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) ของหัวข้อ [เลื่อนการดำเนินการขององค์ประกอบ XML ในรูปแบบการรายงานทางอิเล็กทรอนิกส์](er-defer-xml-element.md) และบันทึกไฟล์ที่สร้างเป็น **SampleXmlReport (1).xml**</span><span class="sxs-lookup"><span data-stu-id="c896d-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="c896d-127">ในยูทิลิตีการเปรียบเทียบไฟล์ ให้เปรียบเทียบไฟล์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c896d-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="c896d-128">ผลต่างแรกที่คุณจะสังเกตอยู่ในส่วนหัวของไฟล์</span><span class="sxs-lookup"><span data-stu-id="c896d-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="c896d-129">ไฟล์ SampleXmlReport.xml มีอักขระ BOM ซึ่งไฟล์ SampleXmlReport (1).xml ไม่มี</span><span class="sxs-lookup"><span data-stu-id="c896d-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![เปรียบเทียบไฟล์ที่สร้างขึ้นโดยใช้ยูทิลิตีการเปรียบเทียบไฟล์](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="c896d-131">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="c896d-131">See also</span></span>

- [<span data-ttu-id="c896d-132">เลื่อนการดำเนินการขององค์ประกอบ XML ในรูปแบบการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c896d-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]