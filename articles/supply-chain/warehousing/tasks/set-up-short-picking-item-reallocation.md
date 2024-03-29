---
title: ตั้งค่าการปันส่วนใหม่ของสินค้าสำหรับการเบิกสินค้าที่ขาด
description: บทความนี้แสดงวิธีการเปิดใช้งานให้ผู้ปฏิบัติงานคลังสินค้าสามารถค้นหาสถานที่สำรองได้อย่างรวดเร็ว ถ้ามีสินค้าคงคลังไม่เพียงพอที่สถานที่ที่พวกเขาได้รับการสั่งการให้ไป
author: Mirzaab
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4e6d7f9b09434346cb0f3670d10437ef8197822
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875027"
---
# <a name="set-up-short-picking-item-reallocation"></a>ตั้งค่าการปันส่วนใหม่ของสินค้าสำหรับการเบิกสินค้าที่ขาด

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการเปิดใช้งานให้ผู้ปฏิบัติงานคลังสินค้าสามารถค้นหาสถานที่สำรองได้อย่างรวดเร็ว ถ้ามีสินค้าคงคลังไม่เพียงพอที่สถานที่ที่พวกเขาได้รับการสั่งการให้ไป 

กระบวนการปันส่วนใหม่จะถูกควบคุมโดย **ข้อยกเว้นของงาน** และใช้โดย **ผู้ปฏิบัติงาน** คลังสินค้า

คุณสามารถใช้กระบวนการปันส่วนใหม่แบบอัตโนมัติ ด้วยตนเอง หรือทั้งสองกระบวนการ:

- การปันส่วนใหม่แบบอัตโนมัติ - คำสั่งสถานที่ถูกใช้เพื่อกำหนดว่าสินค้าพร้อมใช้งานที่สถานที่อื่นหรือไม่ ถ้าเป็นไปได้ จะมีการปรับปรุงงานและผู้ใช้คลังสินค้าจะถูกสั่งการไปยังสถานที่อื่น
- การปันส่วนด้วยตนเอง - อนุญาตให้ผู้ใช้คลังสินค้าสามารถเลือกจากสถานที่หนึ่งแห่งขึ้นไปที่มีปริมาณของสินค้าที่ไม่ได้จอง 
- แบบอัตโนมัติและด้วยตนเอง - ถ้าระบบไม่สามารถดำเนินการปันส่วนใหม่แบบอัตโนมัติ และสถานที่พร้อมใช้งานโดยมีปริมาณที่ไม่ได้จอง ผู้ใช้จะได้รับการแจ้งเตือนให้เลือกสถานที่

## <a name="set-up-work-exceptions"></a>ตั้งค่าข้อยกเว้นของงาน
สามารถกำหนดข้อยกเว้นของงานต่างๆ ด้วยนโยบายการปันส่วนใหม่ของสินค้าที่แตกต่างกัน เพื่อให้ผู้ปฏิบัติงานคลังสินค้าสามารถเลือกได้ตามความจำเป็นในการจัดส่งสินค้าที่กำลังประมวลผลอยู่

บริษัทข้อมูลสาธิต USMF ถูกนำมาใช้ในการสร้างกระบวนงานนี้

1. ใน **บานหน้าต่างนำทาง** ไปที่ **การจัดการคลังสินค้า > การตั้งค่า > งาน > ข้อยกเว้นของงาน**
2. คลิก **สร้าง** 
3. ในฟิลด์ **รหัสข้อยกเว้นของงาน** ให้พิมพ์ค่า นี่จะเป็นชื่อเรื่องของข้อยกเว้นนี้ ตัวอย่างเช่น การเบิกสินค้าที่ขาดด้วยตนเอง
4. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง นี่จะเป็นคำอธิบายโดยย่อของการใช้งานข้อยกเว้นนี้ ตัวอย่างเช่น การเบิกสินค้าที่ขาด - สินค้าไม่พร้อมใช้งาน
5. ในฟิลด์ชนิด **ข้อยกเว้น** เลือก **การเบิกสินค้าที่ขาด**
6. เลือกกล่องกาเครื่องหมาย **ปรับปรุงสินค้าคงคลัง** ถ้ามีการเลือก สินค้าคงคลังจะถูกปรับปรุงเป็น 0 ที่สถานที่ที่มีการเบิกสินค้าที่ขาด
7. ในฟิลด์ **รหัสชนิดการปรับปรุงค่าเริ่มต้น** ให้ป้อนหรือเลือกค่า ตัวอย่างเช่น ใน USMF คุณสามารถเลือก **Remove Res Adj Out** รหัสชนิดการปรับปรุงแต่ละรหัสมีลักษณะสี่อย่าง ได้แก่ ชื่อ คำอธิบาย ชื่อสมุดรายวันสินค้าคงคลัง และ **ลบการจอง** ถ้า **ลบการจอง** ถูกเปิดใช้งาน การจองของรายการใบสั่งที่มีการเบิกสินค้าที่ขาดจะถูกลบออก  
8. ในฟิลด์ **การปันส่วนสินค้าใหม่** เลือกค่า เช่น ด้วยตนเอง ถ้าคุณเลือก ด้วยตนเอง หรือ โดยอัตโนมัติและด้วยตนเอง จะต้องอนุญาตให้ผู้ปฏิบัติงานคลังสินค้าสามารถใช้การปันส่วนด้วยตนเองใหม่

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>ตั้งค่าผู้ปฏิบัติงานที่จะใช้การปันส่วนสินค้าด้วยตนเองใหม่

บริษัทข้อมูลสาธิต USMF ถูกนำมาใช้ในการสร้างกระบวนงานนี้

1. ปิดหน้า
2. ใน **บานหน้าต่างนำทาง** ไปที่ **การจัดการคลังสินค้า > การตั้งค่า > งาน > ผู้ปฏิบัติงาน**
3. คลิก **แก้ไข**
4. ในรายการนี้ ให้เลือกผู้ปฏิบัติงาน ตัวอย่างเช่น Julia Funderburk
5. ขยาย FastTab **ผู้ใช้**
6. ในรายการ เลือก **รหัสผู้ใช้** ตัวอย่างเช่น 24
7. ขยาย FastTab **งาน**
8. เลือก **ใช่** ในฟิลด์ **อนุญาตการปันส่วนสินค้าด้วยตนเองใหม่**


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]