---
title: สร้างการตั้งค่าคอนฟิกการแม็ปแบบจำลองในการรายงานทางอิเล็กทรอนิกส์ (ER)
description: ใช้กระบวนงานนี้เพื่อออกแบบการตั้งค่าคอนฟิกการแม็ปแบบจำลอง (ER) ของการรายงานทางอิเล็กทรอนิกส์ใหม่ และใช้ฟังก์ชัน ER ภายในสำหรับการคำนวณรวมที่มีประสิทธิภาพ
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
ms.openlocfilehash: 23bc3a525be9f65b7e5100114d02f6b79a286fb5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682080"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>สร้างการตั้งค่าคอนฟิกการแม็ปแบบจำลองในการรายงานทางอิเล็กทรอนิกส์ (ER)

[!include [banner](../../includes/banner.md)]

ใช้กระบวนงานนี้เพื่อออกแบบการตั้งค่าคอนฟิกการแม็ปแบบจำลอง (ER) ของการรายงานทางอิเล็กทรอนิกส์ใหม่ และใช้ฟังก์ชัน ER ภายในสำหรับการคำนวณรวมที่มีประสิทธิภาพ ในกระบวนงานนี้ คุณจะสร้างการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. 

กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทของผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่ได้รับมอบหมาย

ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูลใดๆ เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์

1. ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์
    * ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และทำเครื่องหมายเป็น ใช้งานอยู่ ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์  
2. คลิก การตั้งค่าคอนฟิกการรายงาน
3. คลิกแสดงตัวกรอง
4. ในฟิลด์ "ชื่อ" ป้อนค่าตัวกรอง "อินทราสแทต" และใช้ตัวดำเนินการตัวกรอง "ขึ้นต้นด้วย"
    * ใช้ตัวกรองข้อมูลนี้เพื่อค้นหาการตั้งค่าคอนฟิกแบบจำลองข้อมูล 'อินทราสแทต' แบบจำลองนี้อาจมีอยู่แล้วในแผนภูมิการตั้งค่าคอนฟิก ถ้ามี ให้ข้ามงานย่อยถัดไป   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>เรียกการตั้งค่าคอนฟิกแบบจำลองอินทราสแทตที่จัดเตรียมให้โดย Microsoft
1. ปิดหน้า
2. ปิดหน้า
3. ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกไทล์ผู้ให้บริการของ Microsoft  
5. คลิก ที่เก็บ
    * คลิก ที่เก็บ ในไทล์ผู้ให้บริการ Microsoft  
6. คลิกแสดงตัวกรอง
7. ในฟิลด์ "พิมพ์ชื่อ" ป้อนค่าตัวกรอง "ทรัพยากร" และใช้ตัวดำเนินการตัวกรอง "ประกอบด้วย" 
8. คลิก เปิด
9. ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต'
10. คลิก นำเข้า
11. คลิก ใช่
    * คุณนำเข้าการตั้งค่าคอนฟิกแบบจำลอง ER ที่ประกอบด้วยรูปแบบจำลองข้อมูลที่คุณจะใช้เพื่อสำรวจวิธีการใช้ฟังก์ชัน ER ใหม่  
12. ปิดหน้า
13. ปิดหน้า
14. คลิก การตั้งค่าคอนฟิกการรายงาน

## <a name="add-a-new-model-mapping-configuration"></a>เพิ่มการตั้งค่าคอนฟิกการแม็ปแบบจำลองของใหม่
1. ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต'
2. คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง
3. ในฟิลด์ใหม่ ป้อน 'การแม็ปแบบจำลองข้อมูลตามอินทราสแทตแบบจำลองข้อมูล'
4. ในฟิลด์ชื่อ พิมพ์ 'การแม็บตัวอย่างอินทราสแทต'
    * การแม็ปตัวอย่างอินทราสแทต  
5. คลิก สร้างการตั้งค่าคอนฟิก



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]