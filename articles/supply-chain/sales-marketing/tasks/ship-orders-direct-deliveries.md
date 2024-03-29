---
title: จัดส่งสินค้าตามการจัดส่งสินค้าโดยตรง
description: บทความนี้แสดงวิธีการสร้างการจัดส่งโดยตรงสำหรับใบสั่งขาย
author: Henrikan
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart, PurchEditLines, PurchTable, PurchTableReferences, MCRDropShipWorkbench, SalesShippingLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5f145bacecc47a782c60335c6ff5b79f978007c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875172"
---
# <a name="ship-orders-as-direct-deliveries"></a>จัดส่งสินค้าตามการจัดส่งสินค้าโดยตรง

[!include [banner](../../includes/banner.md)]

บทความนี้แสดงวิธีการสร้างการจัดส่งโดยตรงสำหรับใบสั่งขาย คุณใช้การจัดส่งโดยตรงเมื่อคุณต้องการจัดส่งสินค้าให้กับลูกค้าโดยตรงจากผู้จัดจำหน่าย แทนที่จะเป็นการจัดส่งไปยังคลังสินค้าของคุณก่อน  คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง เพื่อทำให้งานย่อยที่สอง "สร้างการจัดส่งโดยตรงจากเวิร์กเบนซ์" เสร็จสมบูรณ์ ตรวจสอบให้มั่นใจว่า สินค้าที่คุณเลือกในใบสั่งขายมีค่าเริ่มต้นของผู้จัดจำหน่ายที่ระบุไว้บนแท็บด่วนการซื้อของผลิตภัณฑ์หลักที่นำออกมาใช้

## <a name="set-an-individual-order-for-direct-delivery"></a>ตั้งค่าใบสั่งแต่ละรายการสำหรับการจัดส่งโดยตรง
1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีลูกหนี้ > ใบสั่ง > ใบสั่งขายทั้งหมด**
2. เลือก **ใหม่**
3. ป้อนหรือเลือกค่าในฟิลด์ **บัญชีลูกค้า** จากนั้น เลือก **ตกลง**
4. ป้อนหรือเลือกค่าในฟิลด์ **หมายเลขสินค้า** และฟิลด์ **ไซต์** จากนั้น เลือก **บันทึก**
5. บนบานหน้าต่างการดำเนินการ เลือก **ใบสั่งขาย** จากนั้น เลือก **การจัดส่งโดยตรง** หน้าการสร้างการจัดส่งแสดงรายการใบสั่งขายที่เปิดค้างไว้ทั้งหมดตามที่คัดลอกมาจากใบสั่งขาย  คุณสามารถทบทวนรายละเอียดใบสั่ง และถ้าจำเป็น คุณสามารถปรับเปลี่ยนรายละเอียดเช่น ปริมาณการซื้อและเงื่อนไขการกำหนดราคาก่อนที่คุณสร้างการจัดส่งโดยตรง  
6. เลือก **ใช่** ในฟิลด์ **รวมทั้งหมด**
    - ถ้าคุณต้องการสร้างการจัดส่งสินค้าโดยตรงสำหรับเฉพาะชุดย่อยของรายการใบสั่งขาย ให้เลือกรายการเหล่านี้ทีละรายการ  
    - ฟิลด์ **บัญชีผู้จัดจำหน่าย** อาจมีการเติมหรืออาจไม่มีการเติมข้อมูลด้วยหมายเลขผู้จัดจำหน่ายอยู่แล้ว ถ้าผู้จัดจำหน่ายเริ่มต้นมีการตั้งค่าไว้สำหรับผลิตภัณฑ์ (ในความครอบคลุมสินค้าที่เกี่ยวข้อง) แล้วผู้จัดจำหน่ายนี้จะถูกคัดลอกไปยังรายการ มิฉะนั้น คุณต้องป้อนผู้จัดจำหน่ายด้วยตนเอง ในตัวอย่างนี้ เราจะเลือกผู้จัดจำหน่ายใหม่ในขั้นตอนถัดไป แม้ว่าผู้จัดจำหน่ายจะถูกเติมไปแล้ว   
7. ป้อนหรือเลือกค่าในฟิลด์ **บัญชีผู้จัดจำหน่าย** จากนั้น เลือก **ตกลง** ข้อความแจ้งให้คุณทราบว่าขณะนี้ได้มีการสร้างใบสั่งซื้อแล้ว   
8. ขยายส่วน **รายละเอียดรายการ**
9. เลือกแท็บ **การจัดส่ง** และตรวจสอบว่ามีการตั้งค่าฟิลด์ **การจัดส่งโดยตรง** เป็น **ใช่**
10. ในบานหน้าต่างการดำเนินการ เลือก **ทั่วไป**
11. เลือก **ใบสั่งที่เกี่ยวข้อง**
12. เลือกลิงค์ในฟิลด์ **ใบสั่งซื้อ**
13. ขยายส่วน **รายละเอียดของรายการ** และเลือกแท็บ **ที่อยู่**
    - ที่อยู่การจัดส่งสำหรับรายการใบสั่งซื้อนี้เป็นที่อยู่การจัดส่งของลูกค้า และไม่ใช้ที่อยู่ของบริษัทของคุณ  
    - ถ้าคุณเปลี่ยนที่อยู่การจัดส่งบนรายการใบสั่งซื้อหรือรายการใบสั่งขายเริ่มต้นอย่างใดอย่างหนึ่ง ที่อยู่ที่สอดคล้องกับรายการสั่งซื้อจะถูกอัพเดตโดยอัตโนมัติ  
14. เลือกแท็บ **การจัดส่ง**
    - เช่นเดียวกับรายการใบสั่งขาย ชนิดรายการใบสั่งซื้อที่เกี่ยวข้องจะถูกตั้งค่าเป็นการจัดส่งโดยตรง  
    - วันจัดส่งใบสั่งซื้อของรายการและวันที่จัดส่งที่ยืนยันได้ตั้งค่าไปยังวันรับสินค้าที่ร้องขอสำหรับรายการใบสั่งขายเริ่มต้นตามลำดับ   
    - ถ้าคุณอัพเดตวันที่ใดวันที่หนึ่งของวันที่เหล่านี้บนรายการการซื้อหรือรายการการขาย วันที่ในใบสั่งที่สอดคล้องกันจะถูกอัพเดตโดยอัตโนมัติ     
    - ใบสั่งซื้อที่มีการตั้งค่าให้จัดส่งสินค้าโดยตรงไปยังลูกค้าจะเชื่อมโยงกับใบสั่งขายเริ่มต้นด้วยวิธีการเชื่อมโยงพิเศษ การเชื่อมโยงนี้มีกฎเรียกเก็บบันทึกการจัดส่งการอัพเดทของใบสั่งขายที่ไม่สามารถดำเนินการสำเร็จจากใบสั่งขายเอง และต้องดำเนินการโดยใช้ใบสั่งซื้อ อย่างไรก็ตาม การออกใบแจ้งหนี้ต้องถูกดำเนินการจากใบสั่งขาย  
15. บนบานหน้าต่างการดำเนินการ เลือก **ซื้อ**
16. เลือก **การยืนยัน**
17. เลือก **ตกลง**
18. ในบานหน้าต่างการดำเนินการ เลือก **รับ**
19. เลือก **ใบรับผลิตภัณฑ์**
20. ในฟิลด์ **ใบรับสินค้า** ให้พิมพ์ค่า
21. เลือก **ตกลง**
22. ในบานหน้าต่างการดำเนินการ เลือก **ทั่วไป**
23. เลือก **ใบสั่งที่เกี่ยวข้อง** และเน้นเรกคอร์ดที่ต้องการ
    - หลังจากที่ใบสั่งซื้อมีการอัพเดเป็นได้รับแล้ว หรือกล่าวได้อีกอย่างหนึ่งว่า หลังจากที่ผู้จัดจำหน่ายได้มีการจัดส่งสินค้าไปยังที่อยู่ของลูกค้าแล้ว สถานะของใบสั่งขายเริ่มต้นจะมีการอัพเดตโดยอัตโนมัติเป็นจัดส่งแล้ว  
    - ขณะนี้ใบสั่งขายสามารถออกใบแจ้งหนี้ได้    
24. เลือก **ตกลง**
25. ปิดหน้า
26. เลือก **ตกลง** ปิดหน้า และกลับไปที่โฮมเพจ

## <a name="create-direct-deliveries-from-the-workbench"></a>สร้างการจัดส่งโดยตรงจากเวิร์กเบนซ์
1. ไปที่ **การนำทาง > โมดูล > บัญชีลูกหนี้ > ใบสั่ง > ใบสั่งขายทั้งหมด**
2. เลือก **ใหม่**
3. ป้อนหรือเลือกค่าในฟิลด์ **บัญชีลูกค้า** จากนั้น เลือก **ตกลง**
4. ให้ป้อนหรือเลือกค่าใดค่าหนึ่งในฟิลด์ **หมายเลขสินค้า** และฟิลด์ **ไซต์**
5. ขยายส่วน **รายละเอียดของรายการ** จากนั้น เลือกแท็บ **การจัดส่ง** แทนที่จะสร้างการจัดส่งโดยตรงให้เป็นส่วนหนึ่งของใบสั่งขายที่ดำเนินการในกระบวนงานก่อนหน้านี้ คุณสามารถส่งมอบงานนี้ให้กับผู้เชี่ยวชาญด้านการจัดซื้อ เมื่อต้องการรวมรายการใบสั่งขายในกระบวนการการส่งมอบการจัดส่งโดยตรง คุณต้องทำเครื่องหมายรายการสำหรับการจัดส่งโดยตรง  
6. เลือก **ใช่** ในฟิลด์ **การจัดส่งโดยตรง**
    - ถ้าสินค้ามีการตั้งค่าไว้แล้วตามค่าเริ่มต้นสำหรับการจัดส่งโดยตรง ฟิลด์จะถูกตั้งเป็น ใช่ โดยอัตโนมัติที่รายการบรรทัดใบสั่ง  คุณสามารถตั้งค่าสินค้าสำหรับการจัดส่งสินค้าโดยตรงในข้อมูลหลักของผลิตภัณฑ์ที่นำออกใช้ โดยการตั้งค่าตัวเลือกการจัดส่งโดยตรงเป็น ใช่ และโดยการเลือกคลังสินค้าการจัดส่งโดยตรงเป็นแบบเริ่มต้น  
    - เนื่องจากยังไม่มีการสร้างใบสั่งซื้อ สถานะการจัดส่งโดยตรงจะถูกกำหนดเป็น "จะมีการจัดส่งโดยตรง"   
7. เลือก **บันทึก**
8. ปิดหน้า จนกว่าคุณจะกลับไปที่โฮมเพจ
9. ป้อน `Direct delivery` ในแถบค้นหา
    - หน้าการจัดส่งโดยตรงที่ทำหน้าที่เป็นเวิร์กเบนซ์ที่ให้ภาพรวมของรายการใบสั่งขายทั้งหมดที่จะมีการจัดส่งโดยตรงแก่เจ้าหน้าที่จัดซื้อ  นอกจากนี้ยังสามารถดูการจัดส่งโดยตรงที่เปิดค้างไว้และใบสั่งที่ได้รับดารยืนยันแล้วบนแท็บการยืนยันการขายและการจัดส่ง  
    - หลังจากที่คุณได้สร้างใบสั่งจัดส่งโดยตรงแล้ว จะมีการย้ายไปยังแท็บการยืนยันโดยอัตโนมัติ คุณสามารถเลือกที่จะยืนยันใบสั่งโดยตรงจากหน้านี้ เมื่อมีการยืนยันการซื้อ จะมีการย้ายโดยอัตโนมัติซึ่งจะเปลี่ยนไปแท็บการจัดส่ง ซึ่งคุณสามารถทำการลงทะเบียนการรับสินค้า  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]