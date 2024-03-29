---
title: ER ตั้งค่าคอนฟิกปลายทาง
description: 'กระบวนงานนี้สาธิตวิธีการตั้งค่าและการใช้ปลายทางที่ต่างกัน สำหรับส่วนประกอบเอาท์พุทของการรายงานทางอิเล็กทรอนิกส์ (ER) เช่น โฟลเดอร์ หรือไฟล์ '
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
ms.openlocfilehash: 3c8d03e9783013183fbe76cb36014fa9e1e1cbed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291068"
---
# <a name="er-configure-destinations"></a>ER ตั้งค่าคอนฟิกปลายทาง

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้สาธิตวิธีการตั้งค่าและการใช้ปลายทางที่ต่างกัน สำหรับส่วนประกอบเอาท์พุทของการรายงานทางอิเล็กทรอนิกส์ (ER) เช่น โฟลเดอร์ หรือไฟล์  บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ DEMF ประเทศเยอรมนีเป็นประเทศ\ภูมิภาคของที่อยู่หลักของนิติบุคคล อย่างไรก็ตาม คุณสามารถใช้นิติบุคคลใดๆ สำหรับกระบวนงานนี้ 

รูปแบบที่ใช้ในตัวอย่างนี้คือ การโอนย้ายเครดิต (DE) ISO20022 แต่คุณสามารถใช้รูปแบบใดๆ ที่คุณได้นำเข้ามาแล้วได้  โปรดทราบว่า กระบวนงานนี้เป็นตัวอย่างของไฟล์เดี่ยวและการตั้งค่าปลายทางเดี่ยว  ข้อมูลเพิ่มเติมเกี่ยวกับการจัดการปลายทางการรายงานทางอิเล็กทรอนิกส์สามารถพบได้ในวิธีใช้ Dynamics 365 Finance

1. ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > ปลายทางการรายงานทางอิเล็กทรอนิกส์
2. คลิก ใหม่ เพื่อสร้างชุดใหม่ของปลายทางสำหรับรูปแบบ
3. ในฟิลด์การอ้างอิง ให้เลือกรูปแบบสำหรับรายการที่คุณต้องการตั้งค่าคอนฟิกปลายทาง
    * ถ้าคุณไม่มีค่าที่จะเลือก แสดงว่าคุณไม่ได้นำเข้าการตั้งค่าคอนฟิกรูปแบบการรายงานอิเล็กทรอนิกส์  คุณต้องนำเข้าการตั้งค่าคอนฟิกรูปแบบ ก่อนการตั้งค่าปลายทาง  
4. คลิก สร้าง เพื่อสร้างปลายทางของไฟล์ใหม่
    * โปรดทราบว่าคุณสามารถสร้างปลายทางไฟล์หนึ่งแห่งได้อย่างไรสำหรับแต่ละส่วนประกอบเอาท์พุทของรูปแบบเดียวกัน เช่น โฟลเดอร์ หรือไฟล์  คุณจะสามาระเปิดใช้งานและปิดใช้งานปลายทางโดยแยกกันในการตั้งค่า  
5. ในฟิลด์ชื่อ ให้ป้อนชื่อที่เป็นมิตรของผู้ใช้ของส่วนประกอบเอาท์พุท
    * เราขอแนะนำให้คุณตั้งชื่อที่มีความหมาย เช่น "ไฟล์การชำระเงิน" หรือ "รายงานการควบคุม"  ชื่อเหล่านี้จะถูกแสดงไปยังผู้ใช้ที่รันไทม์ของการตั้งค่าคอนฟิก พร้อมกับการตั้งค่าปลายทาง  
6. ในชื่อไฟล์ ให้เลือกไฟล์หรือโฟลเดอร์ที่เป็นข้อมูลเฉพาะของรูปแบบ
7. คลิกการตั้งค่า
8. เลือก ใช่ ในฟิลด์ เปิดใช้งานแล้ว
    * กล่องกาเครื่องหมายที่เปิดใช้งานบนแท็บแต่ละแท็บ จะเปิดใช้การงานและปิดการใช้งานปลายทางแต่ละแห่งโดยแยกกัน  ในตัวอย่างนี้ คุณจะเปิดใช้งานการส่งไฟล์เอาท์พุทไปยังผู้รับเมล์ เมื่อมีการสร้างไฟล์  
9. คลิกแก้ไข เพื่อตั้งค่าผู้รับอีเมล
10. คลิก เพิ่ม
11. คลิก พิมพ์อีเมลการจัดการ
12. ในฟิลด์ แหล่งที่มาอีเมล ให้เลือกตัวเลือกหนึ่งตัวเลือก
    * คุณสามารถเลือกชนิดแหล่งที่มาอีเมลอื่น เช่น ชนิดลูกค้าหรือผู้จัดจำหน่าย ได้  ซึ่งจะบ่งชี้ชนิดของอาร์กิวเมนต์ที่ถูกส่งคืนโดยสูตรของบัญชีแหล่งที่มาอีเมล  สูตรของบัญชีแหล่งที่มาอีเมลที่อธิบายในขั้นตอนต่อไปนี้ คือที่ซึ่งคุณจะผูกข้อมูลแหล่งที่มาอีเมล  เลือกผู้จัดจำหน่าย ถ้าสูตรของคุณจะส่งคืนไปยังบัญชีผู้จัดจำหน่าย  ใช้ผู้จัดจำหน่าย ถ้าคุณกำลังใช้ตัวอย่างการตั้งค่าคอนฟิกการโอนย้ายเครดิต ISO 20022  
13. คลิกปุ่มผูกข้อมูลแหล่งที่มาอีเมล
14. ในสูตร ให้ป้อนการอ้างอิงเฉพาะเอกสารไปยังชนิดฝ่ายที่คุณเลือกไว้ก่อนหน้านี้
    * แทนที่การพิมพ์ คุณสามารถหาโหนดแหล่งข้อมูลที่แสดงบัญชีฝ่ายได้ แล้วคลิกปุ่มเพิ่มแหล่งข้อมูลเพื่ออัพเดตสูตร  ตัวอย่างเช่น ถ้าคุณใช้การตั้งค่าคอนฟิกการโอนย้ายเครดิต ISO 20022 โหนดที่แสดงบัญชีผู้จัดจำหน่ายคือ '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID หรือ ป้อนค่าสตริงใดๆ เช่น "DE-001" เพื่อบันทึกสูตร  
15. คลิก บันทึก
16. ปิดหน้า
17. คลิกแก้ไขเพื่อตั้งค่าคอนฟิกรายละเอียดผู้ติดต่อสำหรับฝ่าย
18. เลือก ใช่ ในฟิลด์ผู้ติดต่อหลัก
    * คุณอาจใช้ตัวเลือกอื่นเพื่อบ่งชี้ว่าควรใช้ชนิดของผู้ติดต่อของฝ่ายใดเป็นที่อยู่อีเมสำหรับปลายทางนี้  เราใช้ผู้ติดต่อหลักในตัวอย่างนี้  
19. คลิก ตกลง
20. คลิก ตกลง
21. ในฟิลด์ชื่อเรื่อง ให้พิมพ์ค่า
22. คลิก ตกลง



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
