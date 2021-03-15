---
title: ออกแบบการตั้งค่าคอนฟิก ER เพื่อระงับอักขระ BOM ในไฟล์ที่สร้างขึ้น
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานที่ระงับอักขระเครื่องหมายการจัดลำดับไบต์ (BOM)
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19fbbdea4bfdf30b1313a47e65056b536ed73dbe
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060830"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>ออกแบบการตั้งค่าคอนฟิก ER เพื่อระงับอักขระ BOM ในไฟล์ที่สร้างขึ้น

[!include [banner](../includes/banner.md)]

คุณสามารถออกแบบ [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) [โซลูชัน](er-quick-start1-new-solution.md) เพื่อสร้างเอกสารขาออกได้ เมื่อต้องการสร้างเอกสารเป็นไฟล์ข้อความหรือไฟล์ XML โซลูชันต้องรวม [การตั้งค่าคอนฟิก](general-electronic-reporting.md#Configuration) ER ที่มีส่วนประกอบ [รูปแบบ](general-electronic-reporting.md#FormatComponentOutbound) ER เมื่อต้องการระบุ [การเข้ารหัสอักขระ](https://docs.microsoft.com/windows/win32/intl/character-sets) ที่แสดงถึงชุดของอักขระในไฟล์ที่สร้างขึ้น รูปแบบ ER ต้องมีองค์ประกอบรูปแบบ **ทั่วไป\\ไฟล์** เมื่อต้องการตั้งค่าคอนฟิกส่วนประกอบรูปแบบ ER ให้เปิดเวอร์ชัน [แบบร่าง](general-electronic-reporting.md#component-versioning) ของการตั้งค่าคอนฟิก ER ในโปรแกรมออกแบบรูปแบบ ER และเพิ่มองค์ประกอบ **ทั่วไป\\ไฟล์** ในฟิลด์ **การเข้ารหัส** ให้ระบุการเข้ารหัสไฟล์ขาออกที่สร้างขณะรันไทม์ โดยใช้ส่วนประกอบนี้

> [!NOTE]
> ถ้ารูปแบบมีชื่อการเข้ารหัสที่ไม่ถูกต้อง ระบบจะแสดงข้อผิดพลาดเมื่อคุณบันทึกการเปลี่ยนแปลงของคุณไปยังการตั้งค่าของรูปแบบ

![การเพิ่มองค์ประกอบรากบนหน้าตัวออกแบบรูปแบบ](./media/er-suppress-bom-characters-image1.gif)

ถ้าคุณระบุ **UTF-8** **UTF-16** หรือ **UTF-32** เป็นการเข้ารหัส ตัวเลือก **ระงับอักขระ BOM** จะพร้อมใช้งาน ตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อระงับ [เครื่องหมายการจัดลำดับไบต์ (BOM)](https://docs.microsoft.com/globalization/encoding/byte-order-mark) ในไฟล์ขาออกที่สร้างขึ้นขณะรันไทม์ เมื่อรันรูปแบบ ER ที่แก้ไขได้

> [!NOTE]
> ถ้าคุณปล่อยฟิลด์ **การเข้ารหัส** ว่างไว้ จะมีการใช้การเข้ารหัส **UTF-8** ตามค่าเริ่มต้น

![การตั้งค่าตัวเลือกระงับอักขระ BOM ในหน้าโปรแกรมออกแบบรูปแบบ](./media/er-suppress-bom-characters-image2.gif)

หากต้องการทบทวนฟังก์ชันรันไทม์ ให้ปฏิบัติตามขั้นตอนที่เหมาะสม ตัวอย่างเช่น ปฏิบัติตามขั้นตอนต่างๆ ในหัวข้อ [เลื่อนการดำเนินการขององค์ประกอบ XML ในรูปแบบ ER](er-defer-xml-element.md) หลังจากที่คุณได้เสร็จสิ้นขั้นตอนในส่วน [แก้ไขรูปแบบเพื่อให้การคํานวณเป็นไปตามผลลัพธ์ที่สร้างขึ้น](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) ของหัวข้อนั้น ให้ปฏิบัติตามขั้นตอนเพิ่มเติมเหล่านี้

1. ระบุการเข้ารหัส UTF:

    1. เลือกองค์ประกอบ **รายงาน** ของชนิด **ทั่วไป\\ไฟล์**
    2. ในฟิลด์บัญชี **การเข้ารหัส** ให้ระบุการเข้ารหัส **UTF-8**

2. สร้างไฟล์ XML ที่รวมอักขระ BOM:

    1. ตั้งค่าตัวเลือก **ระงับอักขระ BOM** เป็น **ไม่** เพื่อรวมอักขระ BOM ในไฟล์ XML ที่สร้างขึ้น
    2. เสร็จสิ้นขั้นตอนในส่วน [เลื่อนการดำเนินการขององค์ประกอบ XML สรุป เพื่อให้สามารถใช้ยอดรวมที่คำนวณได้](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) ของหัวข้อ [เลื่อนการดำเนินการขององค์ประกอบ XML ในรูปแบบการรายงานทางอิเล็กทรอนิกส์](er-defer-xml-element.md) และบันทึกไฟล์ที่สร้างเป็น **SampleXmlReport.xml**

3. สร้างไฟล์ XML ที่ไม่รวมอักขระ BOM:

    1. ตั้งค่าตัวเลือก **ระงับอักขระ BOM** เป็น **ใช่** เพื่อระงับอักขระ BOM ในไฟล์ XML ที่สร้างขึ้น
    2. เสร็จสิ้นขั้นตอนในส่วน [เลื่อนการดำเนินการขององค์ประกอบ XML สรุป เพื่อให้สามารถใช้ยอดรวมที่คำนวณได้](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) ของหัวข้อ [เลื่อนการดำเนินการขององค์ประกอบ XML ในรูปแบบการรายงานทางอิเล็กทรอนิกส์](er-defer-xml-element.md) และบันทึกไฟล์ที่สร้างเป็น **SampleXmlReport (1).xml**

4. ในยูทิลิตีการเปรียบเทียบไฟล์ ให้เปรียบเทียบไฟล์ที่สร้างขึ้น

    ผลต่างแรกที่คุณจะสังเกตอยู่ในส่วนหัวของไฟล์ ไฟล์ SampleXmlReport.xml มีอักขระ BOM ซึ่งไฟล์ SampleXmlReport (1).xml ไม่มี

    ![เปรียบเทียบไฟล์ที่สร้างขึ้นโดยใช้ยูทิลิตีการเปรียบเทียบไฟล์](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>ดูเพิ่มเติมที่

- [เลื่อนการดำเนินการขององค์ประกอบ XML ในรูปแบบการรายงานทางอิเล็กทรอนิกส์](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]