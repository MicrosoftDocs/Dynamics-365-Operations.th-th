---
title: สร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระ
description: กระบวนงานนี้สาธิตวิธีการสร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระ
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee4fff7b148396faecef899c7a75365d3e1f47f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991176"
---
# <a name="create-a-free-text-invoice-template"></a>สร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระ

[!include [banner](../includes/banner.md)]

สำหรับการฝึกปฏิบัตินี้ ใช้บริษัทสาธิต USMF กระบวนงานนี้จัดทำขึ้นสำหรับผู้ใช้ที่รับผิดชอบการจัดการและการประมวลผลใบแจ้งหนี้ A/R

## <a name="create-a-template"></a>สร้างเท็มเพลต

1. ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ที่เกิดซ้ำ > เท็มเพลตใบแจ้งหนี้ข้อความอิสระ
    * ใช้แบบฟอร์มนี้เพื่อสร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระที่สามารถรวมรายการใบแจ้งหนี้ ค่าธรรมเนียม เท็มเพลตการกระจายการลงบัญชี และข้อมูลบัญชีแยกประเภท  
2. คลิก 'สร้าง' เพื่อสร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระใหม่
3. ในฟิลด์ชื่อเท็มเพลต ให้พิมพ์ค่า
    * 'ชื่อเท็มเพลต' บ่งชี้เท็มเพลใบแจ้งหนี้ข้อความอิสระโดยเฉพาะ  เท็มเพลตสองอันไม่สามารถมี 'ชื่อเท็มเพลต' เดียวกัน  
4. ในฟิลด์คำอธิบาย ป้อนคำอธิบายของเท็มเพลต
5. ขยายแท็บรายการใบแจ้งหนี้
6. ในฟิลด์คำอธิบาย ป้อนคำอธิบายของรายการใบแจ้งหนี้
7. ในฟิลด์บัญชีหลัก เลือกบัญชีรายได้
    * คุณสามารถเลือกกำหนดบัญชีธุรกรรมออฟเซ็ตของเครดิตลูกค้าสำหรับยอดเงินใบแจ้งหนี้ทั้งหมดรวมในหน้าโพรไฟล์การลงรายการบัญชีลูกค้า  
8. ในฟิลด์กลุ่มภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * กลุ่มภาษีขายสำหรับรายการใบแจ้งหนี้ปัจจุบัน เป็นกลุ่มภาษีขายเริ่มต้นสำหรับบัญชีลูกค้า  
9. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
10. ในฟิลด์กลุ่มภาษีขาย เลือกกลุ่มภาษีขายของสินค้าสำหรับรายการใบแจ้งหนี้ปัจจุบัน
11. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
12. ในฟิลด์ราคาต่อหน่วย ป้อนหรือดูราคาต่อหน่วยสำหรับรายการใบแจ้งหนี้
    * ยอดเงินนี้จะถูกคูณด้วยฟิลด์ปริมาณโดยอัตโนมัติเพื่อกำหนดยอดเงินรายการใบแจ้งหนี้  
13. เพิ่มรายการใหม่สำหรับเท็มเพลตใบแจ้งหนี้ข้อความอิสระ
14. ในฟิลด์คำอธิบาย ป้อนคำอธิบายของรายการใบแจ้งหนี้
15. ในฟิลด์บัญชีหลัก เลือกบัญชีรายได้
    * คุณสามารถเลือกกำหนดบัญชีธุรกรรมออฟเซ็ตของเครดิตลูกค้าสำหรับยอดเงินใบแจ้งหนี้ทั้งหมดรวมในหน้าโพรไฟล์การลงรายการบัญชีลูกค้า  
16. ในฟิลด์กลุ่มภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * กลุ่มภาษีขายสำหรับรายการใบแจ้งหนี้ปัจจุบัน เป็นกลุ่มภาษีขายเริ่มต้นสำหรับบัญชีลูกค้า  
17. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
18. ในฟิลด์กลุ่มภาษีขายตามประเภทสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา 
    * กลุ่มภาษีขายตามประเภทสินค้าสำหรับรายการใบแจ้งหนี้ปัจจุบัน   
19. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
20. ป้อนหรือดูจำนวนหน่วยสำหรับรายการใบแจ้งหนี้
    * ยอดเงินนี้จะถูกคูณด้วยค่าในฟิลด์ราคาต่อหน่วยเพื่อกำหนดยอดเงินรายการใบแจ้งหนี้  
21. ป้อนหรือดูราคาต่อหน่วยสำหรับรายการใบแจ้งหนี้ 
    * ยอดเงินนี้จะถูกคูณด้วยค่าในฟิลด์ปริมาณเพื่อกำหนดยอดเงินรายการใบแจ้งหนี้  
22. ดูและแก้ไขการกระจายการลงบัญชีสำหรับแต่ละบรรทัดและรายการรองใดๆ
    * การกระจายการลงบัญชีกำหนดวิธีที่ยอดเงินจะถูกนำมาพิจารณา เช่น วิธีที่รายได้ ภาษี หรือค่าธรรมเนียมจะถูกนำมาพิจารณาสำหรับใบแจ้งหนี้ข้อความอิสระ  
23. อัพเดทการกระจายการลงบัญชีสำหรับรายการใบแจ้งหนี้ที่เลือก
24. คลิก ปิด

## <a name="save-a-free-text-invoice-as-a-template"></a>บันทึกใบแจ้งหนี้ข้อความอิสระเป็นเท็มเพลต
คุณยังสามารถบันทึกใบแจ้งหนี้ข้อความอิสระที่มีอยู่เป็นเท็มเพลตได้ด้วย เมื่อคุณเลือกบันทึกไปยังเท็มเพลตจากแท็บใบแจ้งหนี้ ใส่ชื่อและคำอธิบายสำหรับเท็มเพลต ถ้ามีเท็มเพลตที่มีชื่ออยู่แล้ว คุณจะเห็นการแจ้งเตือนว่า มีเท็มเพลตที่มีชื่อนั้นอยู่แล้ว คุณยังสามารถคลิกตกลงเพื่อแทนที่ได้ 
