---
title: สร้างรายการงานและเพิ่มงาน
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างรายการงานและเพิ่มงานไปยังรายการใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cca5e0efd6516d02c372e8a616b6bb0c39f3088c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006221"
---
# <a name="create-task-lists-and-add-tasks"></a>สร้างรายการงานและเพิ่มงาน

[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการสร้างรายการงานและเพิ่มงานไปยังรายการใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

*งาน* หมายถึง ชิ้นงานหรือการดำเนินการเฉพาะที่ผู้ใช้ต้องดำเนินการให้เสร็จสมบูรณ์ในวันหรือก่อนวันที่ครบกำหนดที่ระบุ ใน Dynamics 365 Commerce งานจะมีคำแนะนำและข้อมูลโดยละเอียดเกี่ยวกับผู้ติดต่อ รวมถึงลิงก์ไปยังการดำเนินงานของฝ่ายสนับสนุน การดำเนินงานของการขายหน้าร้าน (POS) หรือหน้าไซต์ เพื่อช่วยปรับปรุงประสิทธิภาพการทำงานและจัดหาบริบทที่เจ้าของงานต้องทำงานให้เสร็จสมบูรณ์ได้อย่างมีประสิทธิภาพ

*รายการงาน* เป็นชุดของงานที่ต้องทำให้เสร็จสมบูรณ์โดยเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ ตัวอย่างเช่น อาจมีรายการงานที่ผู้ปฏิบัติงานใหม่ต้องดำเนินการให้เสร็จสมบูรณ์ในระหว่างการเตรียมความพร้อม รายการงานสำหรับแคชเชียร์ที่ทำงานกะเย็น หรือรายการงานที่ต้องทำให้เสร็จสมบูรณ์เพื่อจัดเตรียมร้านสำหรับฤดูกาลวันหยุดที่กำลังจะมาถึง ใน Commerce รายการงานทุกรายการที่มีวันที่เป้าหมายสามารถกำหนดให้กับร้านค้าหรือพนักงานจำนวนเท่าใดก็ได้ และคุณสามารถตั้งค่าคอนฟิกให้มีการเกิดซ้ำได้

ผู้จัดการและผู้ปฏิบัติงานสามารถสร้างรายการงานในฝ่ายสนับสนุนการค้า แล้วกำหนดให้กับชุดของร้านค้า

## <a name="create-a-task-list"></a>สร้างรายการงาน

ในการสร้างรายการงาน ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> การจัดการดูแลการจัดการงาน**
1. เลือก **สร้าง** แล้วป้อนค่าในฟิลด์ **ชื่อ** **คำอธิบาย** และ **เจ้าของ**
1. เลือก **บันทึก**

## <a name="add-tasks-to-a-task-list"></a>เพิ่มงานลงในรายการงาน

เมื่อต้องการเพิ่มงานไปยังรายการงาน ให้ทำตามขั้นตอนเหล่านี้
 
1. บนแท็บด่วน **งาน** ของรายการงานที่มีอยู่ ให้เลือก **สร้าง** เพื่อเพิ่มงาน
1. ในกล่องโต้ตอบ **สร้างงานใหม่** ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับงานนั้น
1. ในฟิลด์ **ออฟเซ็ตข้อมูลที่ครบกำหนด** ให้ป้อนค่าจำนวนเต็มค่าบวกหรือค่าลบ ตัวอย่างเช่น ป้อน **-2** ถ้าควรดำเนินการงานให้เสร็จสมบูรณ์ในสองวันก่อนวันที่ครบกำหนดของรายการงาน
1. ในฟิลด์ **บันทึกย่อ** ให้ป้อนคำแนะนำโดยละเอียด
1. ในฟิลด์ **ผู้ติดต่อ** ให้ป้อนชื่อของผู้เชี่ยวชาญเรื่องตามเรื่องที่เจ้าของงานสามารถติดต่อได้ ถ้าเขาหรือเธอต้องการความช่วยเหลือ
1. ในฟิลด์ **ลิงก์งาน** ให้ป้อนลิงก์ตามลักษณะของงาน

> [!TIP]
> ถึงแม้ว่าคุณจะสามารถใช้ฟิลด์ **ที่กำหนดให้** เพื่อกำหนดงานให้กับบุคคลในขณะที่คุณกำลังสร้างรายการงานได้ เราขอแนะนำว่าคุณควรหลีกเลี่ยงการกำหนดงานระหว่างการสร้างรายการงาน ให้กำหนดงานหลังจากที่มีการสร้างอินสแตนซ์ของรายการสำหรับร้านค้าแต่ละร้านแทน

## <a name="use-task-links-to-help-improve-worker-productivity"></a>ใช้ลิงก์งานเพื่อช่วยปรับปรุงประสิทธิภาพการทำงานของผู้ปฏิบัติงาน

Commerce จะช่วยให้คุณสามารถเชื่อมโยงงานกับการดำเนินงานของ POS เช่น การรันรายงานการขาย การดูวิดีโอการฝึกอบรมทางออนไลน์สำหรับการปฐมนิเทศพนักงานใหม่ หรือการดำเนินงานของฝ่ายสนับสนุน คุณลักษณะนี้จะช่วยให้เจ้าของงานได้รับข้อมูลที่จำเป็นต้องใช้ในการทำงานให้เสร็จสมบูรณ์ได้อย่างมีประสิทธิภาพ

เมื่อต้องการเพิ่มลิงก์ของงานในระหว่างที่คุณสร้างงาน ให้ทำตามขั้นตอนต่อไปนี้

1. บนแท็บด่วน **งาน** ของรายการงานที่มีอยู่ ให้เลือก **แก้ไข**
1. ในกล่องโต้ตอบ **แก้ไขงาน** ในฟิลด์ **ลิงก์งาน** ให้เลือกตัวเลือกต่อไปนี้หนึ่งตัวเลือกขึ้นไป

    - เลือก **รายการเมนู** เพื่อตั้งค่าคอนฟิกการดำเนินงานฝ่ายสนับสนุน เช่น "ชุดผลิตภัณฑ์"
    - เลือก **การดำเนินงาน POS** เพื่อตั้งค่าคอนฟิกการดำเนินงาน POS เช่น "รายงานการขาย"
    - เลือก **URL** เพื่อตั้งค่าคอนฟิก URL แบบเต็ม

ภาพประกอบต่อไปนี้แสดงการเลือกลิงก์ของงานในกล่องโต้ตอบ **แก้ไขงาน**

![การเลือกลิงก์งานในกล่องโต้ตอบแก้ไขงาน](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>ตั้งค่าคอนฟิกการดำเนินงาน POS เพื่อให้สามารถเชื่อมโยงกับงานได้

หากต้องการตั้งค่าคอนฟิกการดำเนินงาน POS เพื่อให้สามารถเชื่อมโยงกับงานได้ ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> POS \> การดำเนินการ POS**
1. เลือก **แก้ไข** ค้นหาการดำเนินงาน POS และเลือกกล่องกาเครื่องหมาย **เปิดใช้งานการจัดการงาน**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของการจัดการงาน](task-mgmt-overview.md)

[ตั้งค่าคอนฟิกการจัดการงาน](task-mgmt-configure.md)

[กำหนดรายการงานให้กับร้านค้าหรือพนักงาน](task-mgmt-assign-lists.md)

[การจัดการงานใน POS](task-mgmt-POS.md)
