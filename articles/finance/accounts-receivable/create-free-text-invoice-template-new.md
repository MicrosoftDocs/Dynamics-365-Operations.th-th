---
title: สร้างเทมเพลตใบแจ้งหนี้ข้อความอิสระ
description: กระบวนงานนี้สาธิตวิธีการสร้างเทมเพลตใบแจ้งหนี้ข้อความอิสระ
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7baa29ad341bdf7ff874bd7f69cf483b7afc075a
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182540"
---
# <a name="create-a-free-text-invoice-template"></a>สร้างเทมเพลตใบแจ้งหนี้ข้อความอิสระ

[!include [banner](../includes/banner.md)]

สำหรับการฝึกปฏิบัตินี้ ใช้บริษัทสาธิต USMF กระบวนงานนี้จัดทำขึ้นสำหรับผู้ใช้ที่รับผิดชอบการจัดการและการประมวลผลใบแจ้งหนี้ A/R

## <a name="create-a-template"></a>สร้างเทมเพลต

1. ไปที่ **บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ที่เกิดซ้ำ > เทมเพลตใบแจ้งหนี้ข้อความอิสระ**
    * ใช้หน้านี้เพื่อสร้างเทมเพลตใบแจ้งหนี้ข้อความอิสระที่สามารถรวมรายการใบแจ้งหนี้ ค่าธรรมเนียม เทมเพลตการกระจายการลงบัญชี และข้อมูลบัญชีแยกประเภท  
2. คลิก **ใหม่** เพื่อสร้างเทมเพลตใบแจ้งหนี้ข้อความอิสระใหม่
3. ในฟิลด์ **ชื่อเทมเพลต** ให้พิมพ์ค่าใดค่าหนึ่ง
    * 'ชื่อเทมเพลต' บ่งชี้เท็มเพลใบแจ้งหนี้ข้อความอิสระโดยเฉพาะ  เทมเพลตสองอันไม่สามารถมี 'ชื่อเทมเพลต' เดียวกัน  
4. ในฟิลด์ **คำอธิบาย** ป้อนคำอธิบายของเทมเพลต
5. ขยายแท็บ **รายการใบแจ้งหนี้**
6. ในฟิลด์ **คำอธิบาย** ป้อนคำอธิบายของรายการใบแจ้งหนี้
7. ในฟิลด์ **บัญชีหลัก** เลือกบัญชีรายได้
    * คุณสามารถเลือกกำหนดบัญชีธุรกรรมออฟเซ็ตของเครดิตลูกค้าสำหรับยอดเงินใบแจ้งหนี้ทั้งหมดรวมในหน้า **โพรไฟล์การลงรายการบัญชีลูกค้า**  
8. ในฟิลด์ **กลุ่มภาษีขาย** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * กลุ่มภาษีขายสำหรับรายการใบแจ้งหนี้ปัจจุบัน เป็นกลุ่มภาษีขายเริ่มต้นสำหรับบัญชีลูกค้า  
9. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
10. ในฟิลด์ **กลุ่มภาษีขาย** เลือกกลุ่มภาษีขายของสินค้าสำหรับรายการใบแจ้งหนี้ปัจจุบัน
11. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
12. ในฟิลด์ **ราคาต่อหน่วย** ป้อนหรือดูราคาต่อหน่วยสำหรับรายการใบแจ้งหนี้
    * ยอดเงินนี้จะถูกคูณด้วยฟิลด์ **ปริมาณ** โดยอัตโนมัติเพื่อกำหนดยอดเงินรายการใบแจ้งหนี้  
13. เพิ่มรายการใหม่สำหรับเทมเพลตใบแจ้งหนี้ข้อความอิสระ
14. ในฟิลด์ **คำอธิบาย** ป้อนคำอธิบายของรายการใบแจ้งหนี้
15. ในฟิลด์ **บัญชีหลัก** เลือกบัญชีรายได้
    * คุณสามารถเลือกกำหนดบัญชีธุรกรรมออฟเซ็ตของเครดิตลูกค้าสำหรับยอดเงินใบแจ้งหนี้ทั้งหมดรวมในหน้า **โพรไฟล์การลงรายการบัญชีลูกค้า**  
16. ในฟิลด์ **กลุ่มภาษีขาย** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * กลุ่มภาษีขายสำหรับรายการใบแจ้งหนี้ปัจจุบัน เป็นกลุ่มภาษีขายเริ่มต้นสำหรับบัญชีลูกค้า  
17. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
18. ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * กลุ่มภาษีขายตามประเภทสินค้าสำหรับรายการใบแจ้งหนี้ปัจจุบัน   
19. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
20. ป้อนหรือดูจำนวนหน่วยสำหรับรายการใบแจ้งหนี้
    * ยอดเงินนี้จะถูกคูณด้วยค่าในฟิลด์ราคาต่อหน่วยเพื่อกำหนดยอดเงินรายการใบแจ้งหนี้  
21. ป้อนหรือดูราคาต่อหน่วยสำหรับรายการใบแจ้งหนี้ 
    * ยอดเงินนี้จะถูกคูณด้วยค่าในฟิลด์ **ปริมาณ** เพื่อกำหนดยอดเงินรายการใบแจ้งหนี้  
22. ดูและแก้ไขการกระจายการลงบัญชีสำหรับแต่ละบรรทัดและรายการรองใดๆ
    * การกระจายการลงบัญชีกำหนดวิธีที่ยอดเงินจะถูกนำมาพิจารณา เช่น วิธีที่รายได้ ภาษี หรือค่าธรรมเนียมจะถูกนำมาพิจารณาสำหรับใบแจ้งหนี้ข้อความอิสระ  
23. อัพเดทการกระจายการลงบัญชีสำหรับรายการใบแจ้งหนี้ที่เลือก
24. คลิก **ปิด**

## <a name="save-a-free-text-invoice-as-a-template"></a>บันทึกใบแจ้งหนี้ข้อความอิสระเป็นเทมเพลต
คุณยังสามารถบันทึกใบแจ้งหนี้ข้อความอิสระที่มีอยู่เป็นเทมเพลตได้ด้วย เมื่อคุณเลือก **บันทึกไปยังเทมเพลต** จากแท็บ **ใบแจ้งหนี้** ใส่ชื่อและคำอธิบายสำหรับเทมเพลต ถ้ามีเทมเพลตที่มีชื่ออยู่แล้ว คุณจะเห็นการแจ้งเตือนว่า มีเทมเพลตที่มีชื่อนั้นอยู่แล้ว คุณยังสามารถคลิก **ตกลง** เพื่อแทนที่ได้ 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
