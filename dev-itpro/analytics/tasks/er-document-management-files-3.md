--- 
title: "สร้างรูปแบบเพื่อใช้ไฟล์การจัดการเอกสารในรูปแบบผลลัพธ์สำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER "
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 47c7bea976d1052f537068b6bcf79c78ac3befbf
ms.contentlocale: th-th
ms.lasthandoff: 07/27/2017

---
# <a name="create-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>สร้างรูปแบบเพื่อใช้ไฟล์การจัดการเอกสารในรูปแบบผลลัพธ์สำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER  สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ 

เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 2: ขยายรูปแบบจำลองข้อมูล)"

กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611


## <a name="create-a-format-to-process-invoices"></a>สร้างรูปแบบเพื่อเพื่อประมวลผลใบแจ้งหนี้
1. ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์
2. คลิก การตั้งค่าคอนฟิกการรายงาน
3. ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'
4. ในแผนภูมิ เลือก 'Customer invoice model\Customer invoice model (custom)'
    * คุณจะสร้างรูปแบบเพื่อสร้างข้อความทางอิเล็กทรอนิกส์ที่มีข้อมูลเกี่ยวกับไฟล์ใดๆ ที่แนบกับใบสั่งขายที่เกี่ยวข้องกับใบแจ้งหนี้ที่ประมวลผลทางอิเล็กทรอนิกส์  
5. คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง
6. ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองข้อมูล แบบจำลองใบแจ้งหนี้ของลูกค้า (กำหนดเอง)'
7. ในฟิลด์ชื่อ ให้พิมพ์ 'ข้อความตัวอย่างใบแจ้งหนี้ทางอิเล็กทรอนิกส์'
    * ข้อความตัวอย่างใบแจ้งหนี้ทางอิเล็กทรอนิกส์  
8. ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้ป้อนหรือเลือกค่า
    * InvoiceCustomer  
9. คลิก สร้างการตั้งค่าคอนฟิก

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>ออกแบบรูปแบบเพื่อเติมข้อมูลเอกสารแนบลงในข้อความที่สร้างในรูปแบบ MIME
1. คลิก ตัวออกแบบ
2. คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง
3. ในแผนภูมิ เลือก 'XML\องค์ประกอบ'
4. ในฟิลด์ชื่อ ให้พิมพ์ 'ใบแจ้งหนี้'
    * ใบแจ้งหนี้  
5. คลิก ตกลง
6. คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง
7. ในแผนภูมิ เลือก 'XML\แอททริบิวต์'
8. ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'SalesOrder'
    * SalesOrder  
9. คลิก ตกลง
10. คลิก เพิ่มแอททริบิวต์
11. ในฟิลด์ชื่อ ให้พิมพ์ 'InvoiceNumber'
    * InvoiceNumber  
12. คลิก ตกลง
13. คลิก เพิ่มแอททริบิวต์
14. ในฟิลด์ชื่อ ให้พิมพ์ 'InvoiceAmount'
    * InvoiceAmount  
15. คลิก ตกลง
16. คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง
17. ในแผนภูมิ เลือก 'XML\องค์ประกอบ'
18. ในฟิลด์ชื่อ ให้พิมพ์ 'EnclosedDocs'
    * EnclosedDocs  
19. คลิก ตกลง
20. ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs'
21. คลิก เพิ่มองค์ประกอบ
22. ในฟิลด์ชื่อ ให้พิมพ์ 'เอกสาร'
    * เอกสาร  
23. คลิก ตกลง
24. ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document'
25. คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง
26. ในแผนภูมิ เลือก 'XML\แอททริบิวต์'
27. ในฟิลด์ชื่อ ให้พิมพ์ 'ชื่อไฟล์'
    * FileName  
28. คลิก ตกลง
29. คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง
30. ในแผนภูมิ เลือก 'XML\องค์ประกอบ'
31. ในฟิลด์ชื่อ ให้พิมพ์ 'เนื้อหาไฟล์'
    * FileContent  
32. คลิก ตกลง
33. ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document\FileContent'
34. คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง
35. ในแผนภูมิ ให้เลือก 'Text\Base64'
36. คลิก ตกลง

## <a name="map-format-elements-to-data-model-as-data-source"></a>แม็ปองค์ประกอบรูปแบบไปยังแบบจำลองข้อมูลโดยเป็นแหล่งที่มาข้อมูล
1. ในแผนภูมิ ให้เลือก 'Invoice\SalesOrder'
2. คลิกแท็บ การแม็ป
3. ในแผนภูมิ ให้ขยาย 'model'
4. ในแผนภูมิ ให้เลือก 'model\Sales order number(SalesId)'
5. คลิก ผูก
6. ในแผนภูมิ ให้เลือก 'Invoice\InvoiceNumber'
7. ในแผนภูมิ ให้ขยาย 'model\Base invoice(InvoiceBase)'
8. ในแผนภูมิ ให้เลือก 'model\Base invoice(InvoiceBase)\Invoice number(Id)'
9. คลิก ผูก
10. ในแผนภูมิ ให้เลือก 'Invoice\InvoiceAmount'
11. ในแผนภูมิ ให้เลือก 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'
12. คลิก ผูก
13. ในแผนภูมิ ให้ขยาย 'model\Invoice attachments'
14. ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File content'
15. ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document\FileContent\Base64'
16. คลิก ผูก
17. ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File name'
18. ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document\FileName'
19. คลิก ผูก
20. ในแผนภูมิ ให้เลือก 'model\Invoice attachments'
21. ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document'
22. คลิก ผูก
23. คลิก บันทึก
24. ปิดหน้า


