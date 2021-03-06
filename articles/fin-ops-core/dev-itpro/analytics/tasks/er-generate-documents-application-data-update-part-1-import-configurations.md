---
title: นำเข้าการตั้งค่าคอนฟิกเพื่อสร้างเอกสารที่มีข้อมูลแอพลิเคชัน
description: เพื่อทำขั้นตอนเหล่านี้ในกระบวนงานให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำกระบวนงาน "ER สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f919d953c3aa0c8d16366167a12e52d35f32cdf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684630"
---
# <a name="import-configurations-to-generate-documents-that-have-application-data"></a>นำเข้าการตั้งค่าคอนฟิกเพื่อสร้างเอกสารที่มีข้อมูลแอพลิเคชัน

[!include [banner](../../includes/banner.md)]

เพื่อทำขั้นตอนเหล่านี้ในกระบวนงานให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำกระบวนงาน "ER สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์

ขั้นตอนต่าง ๆ ในกระบวนงานนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารอิเล็กทรอนิกส์ ในกระบวนงานนี้ คุณจะนำเข้าการตั้งค่าคอนฟิก ER ที่กำหนดที่สร้างขึ้นสำหรับบริษัทตัวอย่าง Litware, Inc. และใช้ในการสร้างเอกสารทางอิเล็กทรอนิกส์ กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูล DEMF ก่อนที่คุณจะเริ่มต้น ให้ดาวน์โหลดและบันทึกไฟล์ที่แสดงรายการอยู่ในหัวข้อวิธีใช้ "สร้างเอกสารอิเล็กทรอนิกส์ และปรับปรุงข้อมูลแอพลิเคชันด้วยเครื่องมือ ER" (generate-electronic-documents-update-application-data/) ไฟล์คือ อินทราสแทต (แบบจำลอง).xml อินทราสแทต (การแม็ป).xml และอินทราสแทต (รูปแบบ).xml

1. ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์
    * ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และทำเครื่องหมายเป็น ใช้งานอยู่ ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ในกระบวนงาน สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่ ให้เสร็จสมบูรณ์  
    * ขั้นตอนต่างๆ ในกระบวนงานนี้ แสดงวิธีการใช้ความสามารถของ ER ในการดำเนินการอัพเดตข้อมูลแอพพลิเคชันและวิธีการสร้างรายงานอินทราสแทต รายละเอียดเกี่ยวกับกระบวนการรายงานจะถูกเก็บถาวรไว้ในตารางแอพพลิเคชัน ในปัจจุบัน เมื่อมีการเปิดใช้งานกระบวนการรายงานอินทราสแทตในแบบฟอร์มอินทราสแทต การเก็บถาวรจะเสร็จสิ้นตามตรรกะที่มีการวางโปรแกรมไว้ในรหัสต้นทางที่มีอยู่ ในกระบวนงานนี้ คุณจะตั้งค่าคอนฟิกตรรกะที่ง่ายแต่มีความคล้ายคลึงกันของข้อมูลแอพพลิเคชันโดยใช้เพียงกรอบงาน ER จะไม่มีสามารถเปลี่ยนแปลงรหัสต้นทาง   

## <a name="import-er-configurations"></a>นำเข้าการตั้งค่าคอนฟิกของ ER
1. คลิก การตั้งค่าคอนฟิกการรายงาน
2. คลิก แลกเปลี่ยน
3. คลิก โหลดจากไฟล์ XML
    * นำเข้าการตั้งค่าคอนฟิกแบบจำลอง ER ที่ประกอบด้วยแบบจำลองข้อมูลที่มีวัตถุประสงค์เพื่อใช้เป็นแหล่งข้อมูลสำหรับการสร้างรายงานอินทราสแทต ภายหลัง คุณจะขยายคำนิยามของแบบจำลองข้อมูลนี้เพื่อใช้สำหรับการอัพเดตข้อมูลแอพพลิเคชันเพื่อเก็บรายละเอียดของกระบวนการรายงานอินทราสแทต   
    * คลิก เรียกดู และเลือกไฟล์ อินทราสแทต (แบบจำลอง).xml  
4. คลิก ตกลง
5. ในแผนภูมิ เลือก 'อินทราสแทต (แบบจำลอง)'
6. คลิก ตัวออกแบบ
7. ในแผนภูมิ ขยาย 'สำหรับเอกสารขาออก'
8. ในแผนภูมิ ขยาย 'สำหรับเอกสารขาออก\ธุรกรรม'
    * ตรวจทานโครงสร้างของแบบจำลองข้อมูลที่นำเข้า หมายเหตุว่ามีการกำหนดรายการราก 'สำหรับเอกสารขาออก' เพื่อระบุลำดับข้อมูล สำหรับการเรียกข้อมูลจากแอพลิเคชันและการใช้เป็นแหล่งข้อมูลในการสร้างรายงานอินทราสแทต 'ธุรกรรม (รายการเรกคอร์ด)' จะถูกใช้เพื่อแสดงรายการธุรกรรมอินทราสแทตที่ต้องรายงาน เนื่องจากคุณจะเก็บรหัสโภคภัณฑ์ที่รายงาน จำเป็นต้องใช้ตัวระบุเฉพาะของรหัสโภคภัณฑ์เดียว 'รหัสเรกคอร์ดโภคภัณฑ์ (Int64)' ในโฟลว์ข้อมูลนี้   
9. ปิดหน้า
10. คลิก แลกเปลี่ยน
11. คลิก โหลดจากไฟล์ XML
    * นำเข้าการตั้งค่าคอนฟิกการแม็ป ER ที่ระบุลำดับข้อมูลสำหรับการเรียกข้อมูลจากแอพลิเคชัน และการใช้ในการสร้างรายงานอินทราสแทต ภายหลัง คุณจะขยายคำนิยามของการแม็ปแบบจำลองนี้เพื่อรับข้อมูลจากรายงานอินทราสแทต และใช้สำหรับการอัพเดตข้อมูลแอพพลิเคชันเพื่อเก็บรายละเอียดของกระบวนการรายงานอินทราสแทต   
    * คลิก เรียกดู และเลือกไฟล์ อินทราสแทต (การแม็ป).xml  
12. คลิก ตกลง
13. ในแผนภูมิ ขยาย 'อินทราสแทต (แบบจำลอง)'
14. ในแผนภูมิ เลือก 'อินทราสแทต (แบบจำลอง)\อินทราสแทต (การแม็ป)'
15. คลิก ตัวออกแบบ
    * หมายเหตุว่าการแม็ปแบบจำลองปัจจุบันประกอบด้วยค่า 'ไปยังแบบจำลอง' ในฟิลด์ทิศทาง ซึ่งหมายความว่าการแม็ปแบบจำลองนี้ถูกออกแบบสำหรับการเรียกข้อมูลจากแอพลิเคชันและการจัดเก็บไว้ในแบบจำลองข้อมูล  
16. คลิก ตัวออกแบบ
17. ในแผนภูมิ ให้ขยาย 'รายการ'
18. ในแผนภูมิ ขยาย 'ธุรกรรม= รายการ'
    * ตรวจทานโครงสร้างของการแม็ปแบบจำลองที่ใช้แบบจำลองข้อมูลที่มีการกรองข้อมูลตามรายการราก 'สำหรับเอกสารขาออก' หมายเหตุว่าแหล่งข้อมูลที่เพิ่มเข้ามา 'รายการ' ให้สิทธิ์การเข้าถึงข้อมูลแอพลิเคชันที่จำเป็น ซึ่งก็คือรายการของเรกคอร์ดจากตารางอินทราสแทต  
19. ปิดหน้า
20. ปิดหน้า
21. คลิก แลกเปลี่ยน
22. คลิก โหลดจากไฟล์ XML
    * นำเข้าการตั้งค่าคอนฟิกรูปแบบ ER ที่ระบุโครงร่างของรายงานอินทราสแทตและกระบวนการของการเติมข้อมูลในรายงาน จากนั้น คุณจะขยายคำนิยามของรูปแบบนี้เพื่อใส่ข้อมูลจากรายงานอินทราสแทตลงในแบบจำลองข้อมูลและจากนั้นใช้เพื่ออัพเดตข้อมูลแอพพลิเคชันเพื่อเก็บรายละเอียดของกระบวนการรายงานอินทราสแทต   
    * คลิก เรียกดู และเลือกไฟล์ อินทราสแทต (รูปแบบ).xml  
23. คลิก ตกลง
24. ในแผนภูมิ เลือก 'อินทราสแทต (แบบจำลอง)\อินทราสแทต (รูปแบบ)'
25. คลิก ตัวออกแบบ
26. คลิก ขยาย/ยุบ
27. ในแผนภูมิ  ให้เลือก 'ไฟล์\การประกาศ'
28. คลิกแท็บ การแม็ป
29. ในแผนภูมิ ให้เลือก 'ไฟล์'
    * ตรวจทานโครงสร้างของรูปแบบที่ใช้ในการสร้างรายงานอินทราสแทต หมายเหตุว่าสิ่งนี้ได้รับการออกแบบมาเพื่อสร้างไฟล์ XML ด้วยการเติมข้อมูลจากแบบจำลองข้อมูล ซึ่งขึ้นอยู่กับรายการราก 'สำหรับเอกสารขาออก' ตรวจสอบว่ามีการกำหนดชื่อสำหรับไฟล์ที่สร้างขึ้นบนฟอร์มกล่องโต้ตอบผู้ใช้ (มีการใช้แหล่งข้อมูล 'fn' สำหรับรายการดังกล่าว)   
30. ปิดหน้า



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]