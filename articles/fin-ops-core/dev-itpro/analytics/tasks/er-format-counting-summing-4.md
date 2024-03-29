---
title: ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 4 - รันรูปแบบ)
description: บทความนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ เพื่อตรวจนับและรวมตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว (ส่วนที่ 4)
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
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
ms.openlocfilehash: 7610e71346b57a7e624424418b22b40e51f9bb95
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290618"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a>ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 4 - รันรูปแบบ)

[!include [banner](../../includes/banner.md)]

ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว  สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF 

เพื่อทำให้ขั้นตอนเหล่านี้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำให้ขั้นตอนในกระบวนงาน "ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 3: ใช้การคำนวณเพื่อสร้างผลลัพธ์)" ให้เสร็จสมบูรณ์

กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>ทดสอบการตั้งค่าคอนฟิกนี้สำหรับการสร้างรายงานอินทราสแทต
1. ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์
2. คลิก การตั้งค่าคอนฟิกการรายงาน
3. ในแผนภูมิ ขยาย 'Intrastat model'
4. ในแผนภูมิ ขยาย 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)'
5. ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)\อินทราสแทต (DE) ที่มีการตรวจนับ & การรวม'
6. ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ
7. คลิก พารามิเตอร์ผู้ใช้
8. เลือก ใช่ ในฟิลด์ รันการตั้งค่า
9. คลิก ตกลง
10. คลิก แก้ไข
11. เลือก ใช่ ในฟิลด์ รันฉบับร่าง
12. คลิก บันทึก
13. ไปที่ภาษี > การตั้งค่า > การค้าต่างประเทศ > พารามิเตอร์การค้าต่างประเทศ
14. ขยายส่วนการรายงานทางอิเล็กทรอนิกส์
15. เลือกการตั้งค่าคอนฟิก "อินทราสแทต (DE) พร้อมกับการตรวจนับ & การสรุป"
16. เลือกการตั้งค่าคอนฟิก "อินทราสแทต (DE) พร้อมกับการตรวจนับ & การสรุป"
17. คลิก บันทึก
18. ปิดหน้า
19. ไปที่ภาษี > ประกาศต่างๆ > การค้าต่างประเทศ > อินทราสแทต
20. คลิกเอาท์พุท
21. คลิกรายงาน
    * รันกระบวนการสร้างรายงานอินทราสแทต  
22. ในฟิลด์วันที่เริ่มต้น ตั้งค่าวันที่เป็น ' 2000-01-01'
    * กำหนดวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับรอบระยะเวลาการรายงานที่รวมอยู่ในรายการที่มีอยู่ในธุรกรรมแบบฟอร์ม  
23. ในฟิลด์วันที่สิ้นสุด ตั้งค่าวันที่เป็น ' 2022-12-31'
    * กำหนดวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับรอบระยะเวลาการรายงานที่รวมอยู่ในรายการที่มีอยู่ในธุรกรรมแบบฟอร์ม  
24. ในฟิลด์ทิศทาง ให้เลือก 'การมาถึง'
25. เลือก ใช่ ในฟิลด์สร้างไฟล์
26. คลิก ตกลง
    * ตรวจทานผลลัพธ์ที่สร้างไว้ที่มีรายการสรุปในส่วนท้าย  
27. คลิก สร้าง
28. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
29. ในฟิลด์ทิศทาง ให้เลือก 'การจัดส่ง'
30. ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า
31. ในฟิลด์โภคภัณฑ์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
32. ตั้งค่าน้ำหนักเป็น '10'
33. ตั้งค่าจำนวนเงินในใบแจ้งหนี้เป็น '10000'
34. ตั้งค่ายอดเงินตามสถิติเป็น '10000'
35. คลิกเอาท์พุท
36. คลิกรายงาน
37. ในฟิลด์ทิศทาง ให้เลือก 'การจัดส่ง'
38. คลิก ตกลง
    * ตรวจทานผลลัพธ์ที่สร้างไว้ที่มีรายการสรุปในส่วนท้าย โปรดทราบว่าการเปรียบเทียบมีการเปลี่ยนแปลงในการรันครั้งแรก  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>รันการตั้งค่าคอนฟิกนี้ในโหมดดีบักเพื่อตรวจทานการตรวจนับการรับสินค้า & การรวมข้อมูล
1. ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก
2. ในแผนภูมิ ขยาย 'Intrastat model'
3. ในแผนภูมิ ขยาย 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)'
4. ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)\อินทราสแทต (DE) ที่มีการตรวจนับ & การรวม'
5. ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ
6. คลิก พารามิเตอร์ผู้ใช้
7. เลือก ใช่ ในฟิลด์ รันในโหมดดีบัก
8. คลิก ตกลง
9. ปิดหน้า
10. ไปที่ภาษี > ประกาศต่างๆ > การค้าต่างประเทศ > อินทราสแทต
11. คลิกเอาท์พุท
12. คลิกรายงาน
13. คลิก ตกลง
14. ปิดหน้า
15. ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก
16. ในแผนภูมิ ขยาย 'Intrastat model'
17. ในแผนภูมิ ขยาย 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)'
18. ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)\อินทราสแทต (DE) ที่มีการตรวจนับ & การรวม'
19. คลิก ล็อกดีบัก
    * โปรดทราบว่ามีการสร้างเรกคอร์ดล็อกดีบักสำหรับกระบวนการดำเนินการของการจัดโครงแบบที่เลือก  
20. คลิกแนบ
21. คลิก เปิด
    * ตรวจทานไฟล์ XML ที่สร้างขึ้นที่ประกอบด้วยรายละเอียดการตรวจนับและการสรุปที่ได้รวบรวมในระหว่างการดำเนินการจัดโครงแบบที่เลือก  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
