--- 
title: "ขยายแบบจำลองข้อมูลเพื่อใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ"
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bde8c612af22ba6bf4561732399fcf2cb1b5c9b3
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs"></a>ขยายแบบจำลองข้อมูลเพื่อใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER  สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ 

เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในคู่มืองาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 1: เตรียมแบบจำลองข้อมูล)"

กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>ขยายแบบจำลองข้อมูลเพื่อแสดงไฟล์การจัดการเอกสาร
1. ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์
2. คลิก การตั้งค่าคอนฟิกการรายงาน
3. ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'
4. ในแผนภูมิ เลือก 'Customer invoice model\Customer invoice model (custom)'
5. คลิก ตัวออกแบบ
6. ในแผนภูมิ ให้เลือก 'Customer invoice(InvoiceCustomer)'
    * เราจะขยายแบบจำลองข้อมูลนี้เพื่อแสดงข้อมูลในไฟล์ใดๆ ที่แนบมากับใบสั่งขายที่เกี่ยวข้องกับใบแจ้งหนี้ที่ประมวลผลทางอิเล็กทรอนิกส์  
7. คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง
8. ในฟิลด์ชื่อ ให้พิมพ์ 'เอกสารแนบใบแจ้งหนี้'
    * เอกสารแนบใบแจ้งหนี้  
9. ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'
10. คลิก เพิ่ม
11. คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง
12. ในฟิลด์ชื่อ ให้พิมพ์ 'เนื้อหาไฟล์'
    * เนื้อหาไฟล์  
13. ในฟิลด์ประเภทสินค้า ให้เลือก 'คอนเทนเนอร์'
14. คลิก เพิ่ม
15. คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง
16. ในฟิลด์ชื่อ ให้พิมพ์ 'ชื่อไฟล์'
    * ชื่อไฟล์  
17. ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'
18. คลิก เพิ่ม

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a>แม็ปองค์ประกอบแบบจำลองข้อมูลใหม่ไปยังแหล่งข้อมูล Dynamics 365 for Finance and Operations
1. คลิก แม็ปแบบจำลองกับแหล่งข้อมูล
2. ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์คำนิยามด้วยค่า 'InvoiceCustomer'
    * InvoiceCustomer  
    * เราจะแม็ปองค์ประกอบแบบจำลองใหม่ไปยังแหล่งข้อมูลที่เหมาะสม  
3. คลิก ตัวออกแบบ
4. ในแผนภูมิ ให้เลือก 'เอกสารแนบใบแจ้งหนี้'
5. ในแผนภูมิ ให้ขยาย 'เอกสารแนบใบแจ้งหนี้'
6. ในแผนภูมิ ให้เลือก 'Invoice attachments\File name'
7. คลิก แก้ไข
8. ในฟิลด์สูตร ให้ป้อน 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. คลิก บันทึก
10. ปิดหน้า
11. ในแผนภูมิ ให้เลือก 'Invoice attachments\File content'
12. คลิก แก้ไข
13. ในฟิลด์สูตร ให้ป้อน 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. คลิก บันทึก
15. ปิดหน้า
16. ในแผนภูมิ ให้เลือก 'เอกสารแนบใบแจ้งหนี้'
17. คลิก แก้ไข
18. ในฟิลด์สูตร ให้ป้อน 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. คลิก บันทึก
20. ปิดหน้า
21. คลิก บันทึก
22. ปิดหน้า
23. ปิดหน้า
24. ปิดหน้า
25. คลิก เปลี่ยนแปลงสถานะ
26. คลิกเสร็จสมบูรณ์
27. คลิก ตกลง


