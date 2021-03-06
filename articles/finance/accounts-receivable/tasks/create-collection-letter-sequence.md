---
title: สร้างลำดับของจดหมายเรียกเก็บเงิน
description: 'ใช้คำแนะนำของงานนี้เพื่อสร้างลำดับจดหมายเรียกเก็บเงิน '
author: mikefalkner
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2500bdaa7107c24f7cb95249208b7ac2a2958fed
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971564"
---
# <a name="create-a-collection-letter-sequence"></a>สร้างลำดับของจดหมายเรียกเก็บเงิน

[!include [banner](../../includes/banner.md)]

ใช้คำแนะนำของงานนี้เพื่อสร้างลำดับจดหมายเรียกเก็บเงิน  งานนี้ใช้บริษัทสาธิต USMF 

1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล >สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > ตั้งค่าลำดับจดหมายเรียกเก็บเงิน**
2. คลิก **สร้าง**
3. ในฟิลด์ **ลำดับจดหมายเรียกเก็บเงิน** ป้อนรหัสลำดับที่จะแสดงถึงลำดับ มันจะถูกใช้เมื่อคุณตั้งค่าโพรไฟล์การลงรายการบัญชี
4. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง  เงื่อนไขการชำระเงินไม่จำเป็นต้องระบุ  ถ้าคุณป้อนค่าที่นี่ ใบแจ้งหนี้ค่าธรรมเนียมของจดหมายเรียกเก็บเงินจะใช้เงื่อนไขการชำระเงินเหล่านี้แทนเงื่อนไขการชำระเงินที่จัดเก็บไว้กับลูกค้า  
5. ในฟิลด์ **รหัสจดหมายเรียกเก็บเงิน** เลือกรหัสสำหรับจดหมายเรียกเก็บเงินแรกที่คุณต้องการส่ง จดหมายเรียกเก็บเงินฉบับแรกถูกสร้างตามวันครบกำหนดชำระในใบแจ้งหนี้ ค่าที่คุณป้อนสำหรับระยะเวลาผ่อนผันในฟิลด์วันที่ของบรรทัดนี้ และข้อมูลอื่นๆที่คุณป้อนในบรรทัดนี้  
6. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง สกุลเงินสำหรับค่าธรรมเนียมเป็นค่าเริ่มต้นของสกุลเงินของลูกค้า  รหัสสกุลเงินนี้อาจแตกต่างจากสกุลเงินของใบแจ้งหนี้  
7. คลิก **เพิ่ม** เพื่อเพิ่มจดหมายเรียกเก็บเงินถัดไปที่จะถูกส่งในลำดับ ในหลายกรณี จดหมายเรียกเก็บเงินแรกเป็นเพียงคำเตือน  คุณสามารถเพิ่มค่าธรรมเนียมได้ถ้าจำเป็น  
8. ในฟิลด์รหัสจดหมายเรียกเก็บเงิน เลือกรหัสของจดหมายเรียกเก็บเงินถัดไปที่คุณต้องการส่งในลำดับ
9. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
10. ในฟิลด์ **บัญชีหลัก** เลือกบัญชีรายได้ที่จะใช้สำหรับค่าธรรมเนียม
11. ป้อนค่าธรรมเนียมที่จะคิดค่าธรรมเนียมเมื่อจดหมายเรียกเก็บเงินนี้ถูกการลงรายการบัญชี
12. ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา เลือกกลุ่มภาษีขายของสินค้าถ้าต้องคำนวณภาษีขายของค่าธรรมเนียม  
13. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
14. ในฟิลด์ **ยอดดุลพ้นกำหนดชำระต่ำสุด** ให้ป้อนยอดดุลที่พ้นกำหนดชำระต่ำสุดที่จำเป็น ก่อนที่จะมีการส่งจดหมายเรียกเก็บเงิน
15. ในฟิลด์ **จำนวนวัน** ป้อนจำนวนของวันปลอดหนี้ที่คุณจะอนุญาต นี่คือจำนวนวันหลังจากวันครบกำหนดที่สามารถสร้างจดหมายเรียกเก็บเงินได้  วันครบกำหนดที่จะใช้สำหรับการคำนวณจะขึ้นอยู่กับตำแหน่งของจดหมายเรียกเก็บเงินในลำดับจดหมายเรียกเก็บเงิน:
    - ระยะเวลาผ่อนผันสำหรับจดหมายเรียกเก็บเงิน 1 จะสัมพันธ์กับวันครบกำหนดชำระบนใบแจ้งหนี้
    - ระยะเวลาผ่อนผันสำหรับจดหมายเรียกเก็บเงิน 2 และสูงกว่านี้ จะสัมพันธ์กับวันที่ที่จดหมายเรียกเก็บเงินก่อนหน้าถูกลงรายการบัญชีหรือถูกพิมพ์ โดยขึ้นอยู่กับการเลือกในฟิลด์ปรับปรุงรหัสจดหมายเรียกเก็บเงินในหน้าพารามิเตอร์บัญชีลูกหนี้  
16. คลิก **เพิ่ม** เพื่อเพิ่มจดหมายเรียกเก็บเงินล่าสุดในลำดับ คุณสามารถเพิ่มรหัสจดหมายเรียกเก็บเงินได้มากถึง 5 รหัสสำหรับลำดับจดหมายเรียกเก็บเงิน  
17. ในฟิลด์ **รหัสจดหมายเรียกเก็บเงิน** เลือกรหัสของจดหมายเรียกเก็บเงินถัดไปที่คุณต้องการส่งในลำดับ
18. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
19. ในฟิลด์ **บัญชีหลัก** ระบุค่าที่ต้องการ
20. ในฟิลด์ **ค่าธรรมเนียมในสกุลเงิน** ให้ป้อนหมายเลข
21. ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
22. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
23. ในฟิลด์ **ยอดดุลที่พ้นกำหนดชำระต่ำสุด** ให้ป้อนหมายเลข
24. ในฟิลด์ **จำนวนวัน** ป้อนตัวเลข
25. เลือกกล่องกาเครื่องหมาย **บล็อค** เพื่อหยุดลูกค้าไม่ให้จัดส่งและออกใบแจ้งหนี้เพิ่มเติม เพื่อเลิกบล็อกบัญชี เลือก **ไม่** ในฟิลด์การระงับการจัดส่งและการออกใบแจ้งหนี้ในหน้าลูกค้า  
26. ขยาย fastTab ของ **บันทึกย่อ**
27. ป้อนข้อความที่จะปรากฏบนจดหมายเรียกเก็บเงินสำหรับรหัสจดหมายเรียกเก็บเงินที่เลือก คุณสามารถแปลข้อความนี้ได้หลายภาษาโดยใช้เมนูแปลเหนือกล่องหมายเหตุ  

