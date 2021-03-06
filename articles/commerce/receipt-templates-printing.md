---
title: ตั้งค่าและออกแบบรูปแบบใบเสร็จ
description: บทความนี้อธิบายวิธีการแก้ไขโครงร่างแบบฟอร์มเพื่อควบคุมวิธีพิมพ์ใบเสร็จ ใบแจ้งหนี้ และเอกสารอื่นๆ ได้ รวมถึงการออกแบบโครงร่างแบบฟอร์มที่คุณสามารถใช้เพื่อสร้าง  Dynamics 365 Commerce รวมตัวออกแบบโครงร่างฟอร์มที่คุณสามารถใช้ เพื่อสร้างหรือปรับเปลี่ยนชนิดต่างๆ ของโครงร่างฟอร์มได้อย่างง่ายดาย
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a66590f18df04d2be0500b7fb1ab183cf64718e8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979764"
---
# <a name="set-up-and-design-receipt-formats"></a>ตั้งค่าและออกแบบรูปแบบใบเสร็จ

[!include [banner](includes/banner.md)]

บทความนี้อธิบายวิธีการแก้ไขโครงร่างแบบฟอร์มเพื่อควบคุมวิธีพิมพ์ใบเสร็จ ใบแจ้งหนี้ และเอกสารอื่นๆ ได้ รวมถึงการออกแบบโครงร่างแบบฟอร์มที่คุณสามารถใช้เพื่อสร้าง  Dynamics 365 Commerce ประกอบด้วยโปรแกรมออกแบบโครงร่างแบบฟอร์มที่คุณสามารถใช้เพื่อสร้างและแก้ไขโครงร่างแบบฟอร์มชนิดต่าง ๆ ได้อย่างง่ายดาย

> [!IMPORTANT]
> คุณต้องตั้งค่าโครงร่างฟอร์มและโพรไฟล์ใบรับเพื่อพิมพ์ใบรับและเอกสารอื่นๆ จาก Retail Modern POS และ Cloud POS คุณสามารถรวมโครงร่างแบบฟอร์มหลายแบบฟอร์มในโพรไฟล์ใบเสร็จ จากนั้นคุณสามารถกำหนดโพรไฟล์ใบเสร็จไปยังเครื่องพิมพ์โดยการปรับเปลี่ยนโพรไฟล์ฮาร์ดแวร์

## <a name="set-up-a-receipt-format"></a>ตั้งค่ารูปแบบใบเสร็จ

1. คลิก **การขายปลีกและการค้า** &gt; **การตั้งค่าช่องทาง** &gt; **การตั้งค่า POS** &gt; **POS** &gt; **รูปแบบใบเสร็จ**
2. ในหน้า **รูปแบบใบเสร็จ** ให้คลิก **ใหม่** เพื่อสร้างโครงร่างแบบฟอร์มใหม่หรือเลือกโครงร่างแบบฟอร์มที่มีอยู่
3. ในฟิลด์ **รูปแบบใบเสร็จ** ให้ป้อนตัวระบุสำหรับโครงร่างแบบฟอร์ม และจากนั้นเลือกชนิดของใบเสร็จที่ใช้สำหรับโครงร่างนี้ คุณยังสามารถป้อนคำอธิบายและชื่อย่อสำหรับใบเสร็จในฟิลด์ **ชื่อ** ได้
4. ใน FastTab **ทั่วไป** ให้เลือกตัวเลือกเพื่อกำหนดลักษณะการพิมพ์:

    - **พิมพ์เสมอ**– พิมพ์ใบเสร็จโดยอัตโนมัติ ตามความเหมาะสม
    - **ไม่ต้องพิมพ์**– ไม่มีการพิมพ์ใบเสร็จ
    - **พร้อมต์ผู้ใช้**– มีการเตือนผู้ใช้ให้พิมพ์ใบเสร็จ
    - **ตามความจำเป็น**– ตัวเลือกนี้จะใช้สำหรับใบรับของขวัญเท่านั้น เมื่อมีการเลือกตัวเลือกนี้ ผู้ใช้สามารถพิมพ์ใบรับของขวัญจากหน้า **เปลี่ยน** ถ้าต้องการใบรับของขวัญ

## <a name="print-images"></a>พิมพ์รูปภาพ

ผู้ออกแบบใบเสร็จมีตัวแปร **โลโก้** ที่สามารถใช้เพื่อระบุรูปภาพที่จะพิมพ์บนใบเสร็จได้ รูปภาพที่รวมอยู่ในการรับสินค้าโดยใช้ตัวแปร **โลโก้** ควรเป็นชนิดไฟล์บิตแมป (.bmp) ใหม่ ถ้ามีการระบุรูปภาพ .bmp โปรแกรมออกแบบใบเสร็จ แต่ไม่ได้พิมพ์เมื่อส่งไปยังเครื่องพิมพ์ ขนาดไฟล์อาจใหญ่เกินไปหรือมิติพิกเซลบนรูปภาพไม่เข้ากันกับเครื่องพิมพ์ หากเกิดกรณีนี้ ให้ลองลดความละเอียดของไฟล์รูปภาพ   

## <a name="design-a-receipt-format"></a>ออกแบบรูปแบบใบเสร็จ

ใช้โปรแกรมออกแบบโครงร่างแบบฟอร์มเพื่อสร้างโครงร่างของเอกสารแบบฟอร์มแบบกราฟิก หน้า **ตัวออกแบบรูปแบบใบเสร็จ** มีสามส่วน: **ส่วนหัว** **รายการ** และ **ส่วนหัว** บางชนิดของโครงร่างแบบฟอร์มใช้องค์ประกอบจากทั้งหมดสามส่วน ในขณะที่ชนิดอื่นๆใช้องค์ประกอบจากหนึ่งส่วนหรือสองส่วนเท่านั้น เมื่อต้องการดูองค์ประกอบที่พร้อมใช้งานสำหรับแต่ละส่วน ให้คลิกปุ่มที่เหมาะสมในบานหน้าต่างนำทางทางด้านซ้ายของหน้า

1. คลิก **การขายปลีกและการค้า** &gt; **การตั้งค่าช่องทาง** &gt; **การตั้งค่า POS** &gt; **POS** &gt; **รูปแบบใบเสร็จ**
2. ในหน้า **รูปแบบใบเสร็จ** เลือกโครงร่างแบบฟอร์ม และจากนั้นคลิก **ตัวออกแบบ**
3. คลิก **ดำเนินการ** เพื่อเริ่มต้นการติดตั้งโฮสต์ตัวออกแบบการค้า
4. บนแถบการแจ้งเตือนที่ปรากฏที่ด้านล่างของหน้าต่าง Internet Explorer คลิก **เปิด** เพื่อเริ่มต้นติดตั้งตัวออกแบบด้วยคลิกเดียว (แถบการแจ้งเตือนอาจปรากฏในตำแหน่งที่ตั้งอื่นในเบราว์เซอร์อื่น) ตัวบ่งชี้ความคืบหน้าแสดงความคืบหน้าของกระบวนการติดตั้ง
5. หลังจากการติดตั้งเสร็จสิ้นป้อนชื่อผู้ใช้การค้าและรหัสผ่านของคุณและจากนั้นคลิก **ลงชื่อเข้าใช้** เพื่อเริ่มต้นตัวออกแบบ
6. หลังจากที่มีการตรวจสอบข้อมูลประจำตัวของคุณและมีการเริ่มต้นตัวออกแบบ คุณสามารถเริ่มออกแบบรูปแบบใบเสร็จหรือปรับเปลี่ยนรูปแบบที่มีอยู่
7. การสร้างองค์ประกอบของแบบฟอร์ม ส่วน **หัว** **รายการ** หรือ **ท้าย** และจากนั้นลากองค์ประกอบจากส่วนนั้นไปยังพื้นที่ทำงาน องค์ประกอบส่วนใหญ่ประกอบด้วยตัวแปรที่จะถูกเติมโดยอัตโนมัติด้วยข้อมูลจากฐานข้อมูล องค์ประกอบอื่นๆเช่น **ข้อความ** ช่วยให้คุณสามารถพิมพ์ข้อความที่กำหนดเองบนใบเสร็จได้

    > [!NOTE]
    > คุณสามารถระบุจำนวนรายการแต่ละส่วนที่ครอบคลุม โดยการปรับตัวเลขมุมขวาล่างของหัวข้อนั้นได้  เพื่อทำให้แก้ไขส่วนได้ง่ายขึ้น ให้เพิ่มความสูงโดยการลากแถบปรับขนาดที่ด้านล่างของส่วน ความสูงของส่วนในพื้นที่ทำงานไม่มีผลต่อจำนวนรายการบนใบเสร็จจริง

8. หลังจากที่คุณลากองค์ประกอบไปยังพื้นที่ทำงาน ให้ตั้งค่าคุณสมบัติสำหรับส่วนที่อยู่ในบานหน้าต่าง **ข้อมูลวัตถุ** ที่ด้านล่างของแบบฟอร์ม ป้อนการตั้งค่าต่อไปนี้อย่างน้อยหนึ่งรายการขึ้นไป:

    - **การปรับแนว** – ตั้งค่าการปรับแนวของฟิลด์ให้เป็น **ซ้าย** หรือ **ขวา**
    - **อักขระเติม**– ระบุอักขระช่องว่าง โดยค่าเริ่มต้น ใช้พื้นที่ว่าง แต่คุณสามารถป้อนอักขระใดๆได้
    - **คำนำหน้า**– ป้อนค่าที่ปรากฏที่จุดเริ่มต้นของฟิลด์ การตั้งค่านี้ใช้เฉพาะกับส่วน **รายการ** ของโครงร่าง
    - **อักขระ**– ระบุจำนวนสูงสุดของอักขระที่ฟิลด์สามารถบรรจุได้ถ้าองค์ประกอบประกอบด้วยตัวแปร ถ้าข้อความในฟิลด์มีขนาดยาวเกินจำนวนอักขระที่คุณระบุ ข้อความจะถูกตัดให้สั้นลงให้พอดีกับฟิลด์
    - **ตัวแปร** –กล่องกาเครื่องหมายนี้จะถูกเลือกโดยอัตโนมัติถ้าองค์ประกอบประกอบด้วยตัวแปรและไม่สามารถถูกกำหนดเองได้
    - **ชนิดแบบอักษร**– ตั้งค่าลักษณะแบบอักษรเป็น **ปกติ** หรือ **ตัวหนา** อักษรตัวหนาใช้เนื้อที่เป็นสองเท่าของตัวอักษรปกติ ดังนั้น อักขระบางตัวอาจถูกตัดทิ้ง
    - **ขนาดแบบอักษร**– ตั้งค่าขนาดแบบอักษรเป็น **ปกติ** หรือ **ใหญ่** ตัวอักษรขนาดใหญ่สูงเป็นสองเท่าของตัวอักษรขนาดปกติ ดังนั้น การใช้ตัวอักษรขนาดใหญ่อาจทำให้ข้อความทับซ้อนกันในใบเสร็จ
    - **ลบ** – คลิกปุ่มนี้เพื่อลบส่วนที่เลือกจากโครงร่างแบบฟอร์ม

## <a name="assign-receipt-profiles"></a>กำหนดโพรไฟล์ใบเสร็จ

มีการกำหนดโพรไฟล์ใบเสร็จโดยตรงกับเครื่องพิมพ์ผ่านโพรไฟล์ฮาร์ดแวร์

1. เปิดโพรไฟล์ฮาร์ดแวร์ โดยการคลิก **การขายปลีกและการค้า** &gt; **การตั้งค่าช่องทาง** &gt; **การตั้งค่า POS** &gt; **โพรไฟล์ POS** &gt; **โพรไฟล์ฮาร์ดแวร์**
2. เลือกเครื่องพิมพ์ จากนั้นในฟิลด์ **โพรไฟล์ใบเสร็จ** ให้กำหนดโพรไฟล์ใบเสร็จที่จะใช้ในการลงทะเบียน

> [!NOTE]
> ถ้ามีการใช้เครื่องพิมพ์สองเครื่อง เครื่องพิมพ์หนึ่งสามารถใช้เพื่อพิมพ์ใบรับทางความร้อน 40 คอลัมน์มาตรฐานได้  โดยทั่วไปจะมีใช้เครื่องพิมพ์เครื่องที่สองเพื่อพิมพ์ใบเสร็จแบบเต็มหน้าที่ต้องการข้อมูลเพิ่มเติม ชนิดใบเสร็จเหล่านี้รวมการรับใบสั่งของลูกค้าและใบแจ้งหนี้ของลูกค้า
