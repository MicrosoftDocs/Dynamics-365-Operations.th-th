---
title: ออกแบบนิพจน์ ER เพื่อเรียกใช้วิธีการของคลาสแอพลิเคชัน
description: หัวข้อนี้อธิบายวิธีการใช้ซ้ำตรรกะแอปพลิเคชันที่มีอยู่ในการตั้งค่าคอนฟิกการรายงานอิเล็กทรอนิกส์ โดยการเรียกใช้วิธีที่ต้องการของคลาสแอปพลิเคชัน
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2de6464aaceadd60a82a70f428f42cd4f864eb8
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092096"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>ออกแบบนิพจน์ ER เพื่อเรียกใช้วิธีการของคลาสแอพลิเคชัน

[!include [banner](../../includes/banner.md)]

คู่มือนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ซ้ำตรรกะแอพลิเคชันที่มีอยู่ในการตั้งค่าคอนฟิกการรายงานอิเล็กทรอนิกส์ (ER) โดยการเรียกใช้วิธีที่ต้องการของคลาสแอพลิเคชันในนิพจน์ ER ค่าของอาร์กิวเมนต์สำหรับการเรียกคลาสที่สามารถถูกกำหนดแบบไดนามิกได้ในขณะทำงาน: ตัวอย่างเช่น ตามข้อมูลในเอกสารแยกวิเคราะห์เพื่อให้มั่นใจถึงความถูกต้อง ในคู่มือนี้ คุณจะสร้างการตั้งค่าคอนฟิก ER ที่จำเป็นสำหรับบริษัทตัวอย่าง Litware, inc กระบวนงานนี้จะถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทของผู้ดูแลระบบหรือนักพัฒนารายงานทางอิเล็กทรอนิกส์ที่ได้รับมอบหมาย 

ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูลใดๆ นอกจากนี้คุณต้องดาวน์โหลด และบันทึกไฟล์ต่อไปนี้ไว้ภายในเครื่อง: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt

เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "ER สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์

1. ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์
    * ตรวจสอบว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง 'Litware, Inc.' พร้อมใช้งาน และทำเครื่องหมายเป็น ใช้งานอยู่ ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ ก่อนอื่นคุณต้องดำเนินขั้นตอนต่างๆ ในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์   
    * คุณกำลังออกแบบกระบวนการสำหรับการแยกวิเคราะห์ใบแจ้งยอดจากธนาคารขาเข้าสำหรับการปรับปรุงข้อมูลแอพลิเคชัน คุณจะได้รับใบแจ้งยอดจากธนาคารขาเข้าเป็นไฟล์ TXT ที่ประกอบด้วยรหัส IBAN ในฐานะที่เป็นส่วนหนึ่งของกระบวนการนำเข้าใบแจ้งยอดจากธนาคาร คุณต้องตรวจสอบความถูกต้องของรหัส IBAN นี้โดยใช้ตรรกะที่มีอยู่แล้ว   

## <a name="import-a-new-er-model-configuration"></a>นำเข้าการตั้งค่าคอนฟิกแบบจำลองของ ER ใหม่
1. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกไทล์ผู้ให้บริการของ Microsoft  
2. คลิก ที่เก็บ
3. คลิกแสดงตัวกรอง
4. เพิ่มฟิลด์ตัวกรอง 'พิมพ์ชื่อ' ในฟิลด์ชื่อ ป้อนค่า "ทรัพยากร" เลือกตัวดำเนินการตัวกรอง "ประกอบด้วย" และจากนั้นคลิก ใช้งาน
5. คลิก เปิด
6. ในแผนภูมิ เลือก 'แบบจำลองการชำระเงิน'
    * ถ้าไม่ได้เปิดใช้งานปุ่มนำเข้าบน FastTab รุ่น คุณได้นำเข้ารุ่น 1 หนึ่งในการตั้งค่าคอนฟิก ER 'แบบจำลองการชำระเงิน' คุณสามารถข้ามขั้นตอนที่เหลือในงานย่อยนี้ได้   
7. คลิก นำเข้า
8. คลิก ใช่
9. ปิดหน้า
10. ปิดหน้า

## <a name="add-a-new-er-format-configuration"></a>เพิ่มการตั้งค่าคอนฟิกรูปแบบของ ER ใหม่
1. คลิก การตั้งค่าคอนฟิกการรายงาน
    * เพิ่มรูปแบบ ER ใหม่เพื่อแยกวิเคราะห์ใบแจ้งยอดจากธนาคารขาเข้าในรูปแบบ TXT  
2. ในแผนภูมิ เลือก 'แบบจำลองการชำระเงิน'
3. คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดเมนูกล่องโต้ตอบ
4. ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามข้อมูลแบบจำลอง แบบจำลองการชำระเงิน'
5. ในฟิลด์ชื่อ ชนิด 'รูปแบบการนำเข้าใบแจ้งยอดจากธนาคาร (ตัวอย่าง)'
    * รูปแบบการนำเข้าสำหรับใบแจ้งยอดจากธนาคาร (ตัวอย่าง)  
6. เลือก ใช่ ในฟิลด์สนับสนุนการนำเข้าข้อมูล
7. คลิก สร้างการตั้งค่าคอนฟิก

## <a name="design-the-er-format-configuration---format"></a>ออกแบบการตั้งค่าคอนฟิกรูปแบบ ER - รูปแบบ
1. คลิก ตัวออกแบบ
    * รูปแบบที่ได้รับการออกแบบแสดงถึงโครงสร้างของไฟล์ภายนอกที่คาดไว้ในรูปแบบ TXT  
2. คลิกเพิ่มรากเพื่อเปิดเมนูกล่องโต้ตอบ
3. ในแผนภูมิ ให้เลือก 'ข้อความ\ลำดับ'
4. ในฟิลด์ ชื่อ ให้พิมพ์ 'Root'
    * ราก  
5. ในฟิลด์อักขระพิเศษ ให้เลือก 'รายการใหม่ - Windows (CR LF)'
    * ตัวเลือก 'รายการใหม่ - Windows (CR LF)' ได้ถูกเลือกในฟิลด์ ‘อักขระพิเศษ’ โดยขึ้นอยู่กับการตั้งค่านี้ แต่ละรายการในไฟล์แยกวิเคราะห์จะถือว่าเป็นเรกคอร์ดแยกต่างหาก  
6. คลิก ตกลง
7. คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง
8. ในแผนภูมิ ให้เลือก 'ข้อความ\ลำดับ'
9. ในฟิลด์ชื่อ ให้พิมพ์ชื่อ 'แถว'
    * แถว  
10. ในฟิลด์ความหลากหลาย ให้เลือก 'หนึ่งต่อหลายรายการ'
    * มีการเลือกตัวเลือก 'หนึ่งต่อหลายรายการ' ในฟิลด์ 'ความหลากหลาย' โดยขึ้นอยู่กับการตั้งค่านี้ มีการคาดหวังว่า รายการอย่างน้อยหนึ่งรายการจะปรากฏในไฟล์แยกวิเคราะห์  
11. คลิก ตกลง
12. ในแผนภูมิ ให้เลือก 'ราก\แถว'
13. คลิก เพิ่มลำดับ
14. ในฟิลด์ชื่อ ให้พิมพ์ 'ฟิลด์'
    * ฟิลด์  
15. ในฟิลด์ความหลากหลาย ให้เลือก 'เพียงรายการเดียว'
16. คลิก ตกลง
17. ในแผนภูมิ ให้เลือก 'ราก\แถว\ฟิลด์'
18. คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง
19. ในแผนภูมิ ให้เลือก 'ข้อความ\สตริง'
20. ในฟิลด์ชื่อ ให้พิมพ์ 'IBAN'
    * IBAN  
21. คลิก ตกลง
    * มีการตั้งค่าคอนฟิกที่แต่ละรายการในไฟล์แยกวิเคราะห์ประกอบด้วยรหัส IBAN เท่านั้น  
22. คลิก บันทึก

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>ออกแบบการตั้งค่าคอนฟิกรูปแบบของ ER – การแม็ปไปยังแบบจำลองข้อมูล
1. คลิก แม็ปรูปแบบไปยังแบบจำลอง
2. คลิก สร้าง
3. ในฟิลด์คำนิยาม พิมพ์ 'BankToCustomerDebitCreditNotificationInitiation'
    * BankToCustomerDebitCreditNotificationInitiation  
4. แก้ไขการเปลี่ยนแปลงของคำนิยาม
5. ในฟิลด์ชื่อ ให้พิมพ์ 'การแม็ปไปยังแบบจำลองข้อมูล'
    * การแม็ปไปยังแบบจำลองข้อมูล  
6. คลิก บันทึก
7. คลิก ตัวออกแบบ
8. ในแผนภูมิ เลือก 'Dynamics 365 for Operations\Class'
9. คลิก เพิ่มราก
    * เพิ่มแหล่งข้อมูลใหม่เพื่อเรียกตรรกะแอพลิเคชันที่มีอยู่สำหรับการตรวจสอบรหัส IBAN  
10. ในฟิลด์ชื่อ พิมพ์ 'ตรวจสอบรหัส'
    * ตรวจสอบรหัส  
11. ในฟิลด์คลาส ให้พิมพ์ 'ISO7064'
    * ISO7064  
12. คลิก ตกลง
13. ในแผนภูมิ ให้ขยาย 'รูปแบบ'
14. ในแผนภูมิ ขยาย 'รูปแบบ\ราก: ลำดับ(ราก)'
15. ในแผนภูมิ เลือก 'รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..* (แถว)'
16. คลิก ผูก
17. ในแผนภูมิ ขยาย 'รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..* (แถว)'
18. ในแผนภูมิ ขยาย ' รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..* (แถว)\ฟิลด์: 1..1 ลำดับ (ฟิลด์)'
19. ในแผนภูมิ เลือก ' รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..* (แถว)\ฟิลด์: ลำดับ 1..1 (ฟิลด์)\IBAN: สตริง(IBAN)'
20. ในแผนภูมิ ขยาย 'การชำระเงิน: รูปแบบ.ราก.แถว'
21. ในแผนภูมิ ขยาย 'การชำระเงิน = รูปแบบ.ราก.แถว\บัญชีเจ้าหนี้(CreditorAccount)'
22. ในแผนภูมิ ขยาย 'การชำระเงิน = รูปแบบ.ราก.แถว\บัญชีเจ้าหนี้(CreditorAccount)\การระบุรหัสประจำตัว'
23. ในแผนภูมิ เลือก 'การชำระเงิน = รูปแบบ.ราก.แถว\บัญชีเจ้าหนี้(CreditorAccount)\การระบุรหัสประจำตัว\IBAN'
24. คลิก ผูก
25. คลิกแท็บ การตรวจสอบความถูกต้อง
26. คลิก สร้าง
    * เพิ่มกฎการตรวจสอบใหม่ที่แสดงข้อผิดพลาดสำหรับรายการใดๆ ในไฟล์แยกวิเคราะห์ที่ประกอบด้วยรหัส IBAN ที่ไม่ถูกต้อง  
27. คลิก แก้ไขเงื่อนไข
28. ในแผนภูมิ ขยาย 'ตรวจสอบรหัส'
29. ในแผนภูมิ เลือก 'check_codes\verifyMOD1271_36'
30. คลิก เพิ่มแหล่งข้อมูล
31. ในฟิลด์สูตร ป้อน 'check_codes.verifyMOD1271_36('
    * check_codes.verifyMOD1271_36(  
32. ในแผนภูมิ ให้ขยาย 'รูปแบบ'
33. ในแผนภูมิ ขยาย 'รูปแบบ\ราก: ลำดับ(ราก)'
34. ในแผนภูมิ ขยาย 'รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..* (แถว)'
35. ในแผนภูมิ ขยาย ' รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..* (แถว)\ฟิลด์: 1..1 ลำดับ (ฟิลด์)'
36. ในแผนภูมิ เลือก ' รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..* (แถว)\ฟิลด์: ลำดับ 1..1 (ฟิลด์)\IBAN: สตริง(IBAN)'
37. คลิก เพิ่มแหล่งข้อมูล
38. ในฟิลด์สูตร ป้อน 'check_codes.verifyMOD1271_36 (รูปแบบ.ราก.แถว.ฟิลด์.IBAN)'
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. คลิก บันทึก
40. ปิดหน้า
    * เงื่อนไขในการตรวจสอบได้ถูกตั้งค่าคอนฟิกเพื่อส่งคืนค่า เท็จ สำหรับรหัส IBAN ที่ไม่ถูกต้องใดๆ โดยการเรียกวิธีการที่มีอยู่ 'verifyMOD1271_36' ของคลาสแอพลิเคชัน 'ISO7064' หมายเหตุว่า ค่าของรหัส IBAN ถูกกำหนดแบบไดนามิกขณะรันไทม์เป็นอาร์กิวเมนต์ของวิธีการเรียก โดยยึดตามเนื้อหาของไฟล์ TXT ที่แยกวิเคราะห์   
41. คลิกแก้ไขข้อความ
42. ในฟิลด์สูตร ป้อน ' CONCATENATE ("พบรหัส IBAN ที่ไม่ถูกต้อง: ", รูปแบบ.ราก.แถว.ฟิลด์.IBAN)'
    * CONCATENATE("พบรหัส IBAN ที่ไม่ถูกต้อง: ", รูปแบบ.ราก.แถว.ฟิลด์.IBAN)'  
43. คลิก บันทึก
44. ปิดหน้า
45. คลิก บันทึก
46. ปิดหน้า

## <a name="run-the-format-mapping"></a>รันการแม็ปรูปแบบ
เพื่อวัตถุประสงค์ในการทดสอบ ดำเนินการแม็ปรูปแบบโดยใช้แฟ้ม SampleIncomingMessage.txt ซึ่งคุณดาวน์โหลดไว้ เอาท์พุทที่สร้างขึ้นรวมข้อมูลที่จะถูกนำเข้าจากไฟล์ TXT ที่เลือก และจะถูกเติมข้อมูลไปยังแบบจำลองข้อมูลที่กำหนดเองในระหว่างการนำเข้าจริง   
1. คลิก เรียกใช้
    * คลิก เรียกดู และนำทางไปยังไฟล์ SampleIncomingMessage.txt ที่คุณดาวน์โหลดไว้ก่อนหน้านี้  
2. คลิก ตกลง
    * ตรวจสอบเอาท์พุทในรูปแบบ XML ซึ่งแสดงข้อมูลที่ได้ถูกนำเข้าจากไฟล์ที่เลือก และถูกนำไปยังแบบจำลองข้อมูล โปรดทราบว่า มีการประมวลผลรายการของไฟล์ TXT ที่นำเข้า 3 รายการเท่านั้น รหัส IBAN บนรายการที่ 4 ที่ไม่ถูกต้อง ถูกข้าม และมีการระบุข้อความแสดงข้อผิดพลาดใน Infolog  

