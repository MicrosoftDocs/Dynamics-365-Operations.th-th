---
title: คำนวณการคาดการณ์สินค้า
description: หัวข้อนี้อธิบายวิธีการคำนวณการคาดการณ์สินค้าในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 155dc720804196ccc44fad5eaf71e3563a9c68cf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022569"
---
# <a name="calculate-item-forecast"></a>คำนวณการคาดการณ์สินค้า

[!include [banner](../../includes/banner.md)]

 

เช่นเดียวกับที่คุณสามารถคำนวณการใช้กำลังการผลิต ซึ่งอธิบายไว้ในส่วนก่อนหน้า คุณยังสามารถทำการคำนวณการคาดการณ์สินค้าบน:

- รายการกำหนดการบำรุงรักษา  
- ใบสั่งงานที่ยังไม่ได้ถูกจัดกำหนดการ  
- ใบสั่งงานที่จัดกำหนดการ

การทำเช่นนี้มีประโยชน์ถ้าคุณต้องการดูภาพรวมของรายการปริมาณการใช้ที่คาดไว้ (อะไหล่สำลอง และสินค้าอื่นๆที่จำเป็นสำหรับการดำเนินการใบสั่งงานให้เสร็จสมบูรณ์) สำหรับรอบระยะเวลาที่ระบุ การคำนวณการคาดการณ์สินค้าสามารถทำได้ในสินทรัพย์ทั้งหมดหรือสินทรัพย์ที่เลือก นอกจากนี้คุณยังสามารถทำการคำนวณบนกิจกรรมการหยุดทำงานของการบำรุงรักษา (**กิจกรรมการหยุดทำงานของการบำรุงรักษาทั้งหมด** หรือ **กิจกรรมการหยุดทำงานของการบำรุงรักษาที่เปิดใช้งานอยู่**) หรือ กลุ่มใบสั่งงาน (**กลุ่มใบสั่งงานทั้งหมด** หรือ **กลุ่มใบสั่งงานที่เปิดใช้งานอยู่**)

1. คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **การคาดการณ์สินค้า** หรือ **การจัดการสินทรัพย์** > **ทั่วไป** > **กลุ่มใบสั่งงาน** > **กลุ่มใบสั่งงานทั้งหมด** / **กลุ่มใบสั่งงานที่เปิดใช้งานอยู่** > เลือกใบสั่งงานกลุ่มในรายการปุ่ม > **การคาดการณ์สินค้า** หรือ **การจัดการสินทรัพย์** > **ทั่วไป** > **กิจกรรมการหยุดทำงานของการบำรุงรักษา** > **กิจกรรมการหยุดทำงานของการบำรุงรักษาทั้งหมด** / **กิจกรรมการหยุดทำงานของการบำรุงรักษาที่เปิดใช้งานอยู่** > เลือกกิจกรรมการหยุดทำงานของการบำรุงรักษาในรายการปุ่ม > **การคาดการณ์สินค้า**

2. ในกล่องโต้ตอบ **คำนวณการคาดการณ์สินค้า** เลือกรอบระยะเวลาสำหรับการคำนวณในฟิลด์ **วัน/เวลาที่เริ่มต้น** เเละ **วัน/เวลาที่สิ้นสุด**

3. เลือก "ใช่" บนปุ่มสลับ **รวมกำหนดการบำรุงรักษา** ถ้าคุณต้องการรวมรายการกำหนดการบำรุงรักษาในการคำนวณการคาดการณ์

4. เลือก "ใช่" บนปุ่มสลับ **รวมใบสั่งงาน** ถ้าคุณต้องการรวมรายการใบสั่งงานในการคำนวณการคาดการณ์

5. คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้รายการการคาดการณ์สินค้าเกี่ยวกับตำเเหน่งที่ทำงานมากเพียงใด 

      ตัวอย่างเช่น หากคุณใส่หมายเลข "1" ในฟิลด์ และคุณมีโครงสร้างตำเเหน่งที่ทำงานหลายระดับ รายการกำหนดการบำรุงรักษาทั้งหมด เเละใบสั่งงานสำหรับตำเเหน่งที่ทำงานจะเเสดงขึ้นบนระดับสูงสุด เเละดังนั้นชั่วโมงในรายการอาจมีการเพิ่มเติมจากตำเเหน่งที่ทำงานที่อยู่ในระดับต่ำกว่า 
  
      หากคุณแทรกหมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดแสดงรายการกำหนดการบำรุงรักษาทั้งหมด เเละใบสั่งงานทั้งหมดบนระดับตำเเหน่งที่อยู่ทั้งหมดที่เกี่ยวข้อง

6. คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณ

7. ในกลุ่ม **กลุ่มโดย...** คลิกปุ่มที่เกี่ยวข้องเพื่อแสดงระดับรายละเอียดที่จำเป็นต้องใช้ในการคำนวณ ในภาพหน้าจอด้านล่าง ปุ่ม **กลุ่มที่** จะถูกเน้นด้วยสีน้ำเงิน คลิกบนปุ่มเพื่อเรียกใช้งานหรือยกเลิกการเรียกใช้งาน

8. คลิกปุ่ม **เเสดงมิติ** ถ้าคุณต้องการดูผลิตภัณฑ์ การจัดเก็บ หรือมิติการติดตามที่เกี่ยวข้องกับสินค้า เลือกกล่องกาเครื่องหมายที่เกี่ยวข้อง เเละ คลิก **ตกลง**

![รูปที่ 1](media/02-capacity-planning.png)
