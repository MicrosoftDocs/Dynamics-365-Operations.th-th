---
title: เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้แอพลิเคชันที่เชื่อมต่อ
description: ขั้นตอนในบทความนี้จะอธิบายวิธีการที่ผู้ใช้ Regulatory Configuration Service สามารถออกแบบการแม็ปแบบจำลองการรายงานทางอิเล็กทรอนิกส์ใหม่ โดยใช้ข้อมูลเมตา
author: kfend
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 1a935b96e247978fc2b2f9449d403c92bff35f17
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267886"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>เข้าถึงข้อมูลเมตาของแอพลิเคชันโดยใช้แอพลิเคชันที่เชื่อมต่อ

[!include [banner](../../includes/banner.md)]

ขั้นตอนต่อไปนี้ อธิบายวิธีที่ผู้ใช้ Regulatory configuration service (RCS) ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถออกแบบการแม็ปแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) ใหม่ โดยใช้ข้อมูลเมตาของการเงินและการดำเนินงาน จะมีการเข้าถึงข้อมูลเมตาของแอพลิเคชันแบบออนไลน์โดยใช้แอพลิเคชันที่เชื่อมต่อ RCS จะมีการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ของตัวอย่างเพื่อเข้าถึงธุรกรรมการค้าต่างประเทศ เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ใน RCS อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในบทความ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md) ให้เสร็จสมบูรณ์ ถ้าคุณยังไม่ได้ดำเนินการขั้นตอนในบทความ [ให้เข้าถึงข้อมูลเมตาของแอปลิเคชันโดยใช้การตั้งค่าคอนฟิก ER](access-application-metadata-er-configuration.md) ให้ดาวน์โหลด [ตัวอย่างการรายงานทางอิเล็กทรอนิกส์](https://download.microsoft.com/download/0/4/e/04e13839-e423-442b-a6c2-dd35b1045c2d/Dynamics%20365%20for%20Finance%20and%20Operations%208.1%20Electronic%20reporting%20task%20guides.zip) และบันทึกการตั้งค่าคอนฟิก ER ต่อไปนี้: Foreign trade metadata.xml Foreign trade model.xml Foreign trade mapping.xml และจากนั้น ดำเนินการขั้นตอนต่างๆ ในกระบวนงานให้เสร็จสมบูรณ์

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น
1. ไปที่ **พื้นที่ทำงานทั้งหมด** > **การรายงานทางอิเล็กทรอนิกส์** 
2. ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และถูกทำเครื่องหมายเป็น **ใช้งานอยู่** ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ในกระบวนงาน [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md) ให้เสร็จสมบูรณ์ 

## <a name="get-required-er-configurations"></a>รับการตั้งค่าคอนฟิก ER ที่จำเป็น
1. คลิก **การตั้งค่าคอนฟิกการรายงาน** 
2. หากคุณดำเนินการขั้นตอนต่างๆ ในกระบวนงาน [เข้าถึงข้อมูลเมตาของโปรแกรมประยุกต์โดยใช้การตั้งค่าคอนฟิก ER](access-application-metadata-er-configuration.md) เสร็จสมบูรณ์แล้ว คุณมีการตั้งค่าคอนฟิก ER ที่จำเป็นทั้งหมดแล้ว (ข้อมูลเมตาการค้าต่างประเทศ การตั้งค่าคอนฟิกแบบจำลองและการแม็ป) ในอินสแตนซ์ RCS ปัจจุบัน คุณสามารถข้ามขั้นตอนที่เหลือทั้งหมดของงานย่อยนี้ได้ 
3. คลิก **แลกเปลี่ยน** 
4. คลิก **โหลดจากไฟล์ XML** 
5. คลิก **เรียกดู** และเลือกไฟล์ **Foreign trade metadata.xml** 
6. คลิก **ตกลง** 
7. คลิก **แลกเปลี่ยน** 
8. คลิก **โหลดจากไฟล์ XML** 
9. คลิก **เรียกดู** และเลือกไฟล์ **Foreign trade model.xml** 
10. คลิก **ตกลง** 
11. คลิก **แลกเปลี่ยน** 
12. คลิก **โหลดจากไฟล์ XML** 
13. คลิก **เรียกดู** และเลือกไฟล์ **Foreign trade mapping.xml** 
14. คลิก **ตกลง** 

## <a name="register-a-connected-application"></a>ลงทะเบียนแอพลิเคชันที่เชื่อมต่อแล้ว
1. ปิดหน้า 
2. ปิดหน้า 
3. ไปที่ **พื้นที่ทำงานทั้งหมด** > **การรายงานทางอิเล็กทรอนิกส์** 
4. คลิก **แอพลิเคชันที่เชื่อมต่อ** 
5. ตรวจสอบให้แน่ใจว่าแอพลิเคชันที่ได้รับการตั้งค่าคอนฟิกขึ้นอยู่กับ Azure และสามารถเข้าถึงได้สำหรับผู้ใช้ RCS ปัจจุบัน นอกจากนี้ คุณต้องระบุว่าผู้ใช้ RCS ปัจจุบันมีสิทธิ์เข้าถึงแอพลิเคชันที่เลือก และได้รับการลงทะเบียนเป็นผู้ใช้ของแอพลิเคชันนี้ในการเล่นบทบาทที่ให้สิทธิ์พวกเขาในการเข้าถึงข้อมูลเมตาของแอพลิเคชัน 
6. คลิก **สร้าง** 
7. ในฟิลด์ **ชื่อ** พิมพ์ 'MyConnectedApp' 
8. ในฟิลด์ **แอพลิเคชัน** ให้พิมพ์ 'https:// mycompany.operations.dynamics.com ' 
9. ในฟิลด์ **ผู้เช่า** ให้พิมพ์ 'mycompany.onmicrosoft.com' 
10. คลิก **บันทึก** 
11. เมื่อคุณตรวจสอบการเชื่อมต่อกับแอพลิเคชันที่ตั้งค่าคอนฟิก บนหน้า **เชื่อมต่อกับแอพลิเคชันระยะไกล** คลิกที่ลิงค์ **คลิกที่นี่เพื่อเชื่อมต่อกับแอพลิเคชันระยะไกลที่เลือก** 
12. คลิก **ตรวจสอบการเชื่อมต่อ** 
13. คลิก **ปิด** 
14. เมื่อการตรวจสอบความถูกต้องของการเชื่อมต่อเสร็จเรียบร้อยแล้ว จะมีการปรับปรุงรายการรายละเอียดรุ่นและผู้เช่าสำหรับแอพลิเคชันที่ตั้งค่าคอนฟิกในกริดปัจจุบัน 

## <a name="review-existing-model-mapping-configuration"></a>ตรวจทานการตั้งค่าคอนฟิกการแม็ปแบบจำลองที่มีอยู่
1. ปิดหน้า 
2. คลิก **การตั้งค่าคอนฟิกการรายงาน** 
3. ในแผนภูมิ ขยาย **แบบจำลองการค้าต่างประเทศ** 
4. ในแผนภูมิ ให้เลือก **แบบจำลองการค้าต่างประเทศ\การแม็ปการค้าต่างประเทศ** 
5. ขยายส่วน **ข้อกำหนดเบื้องต้น** 

    > [!NOTE]
    > ในขณะนี้ การแม็ปนี้อ้างอิงถึงการตั้งค่าคอนฟิกข้อมูลเมตา ข้อมูลเมตาของแอพลิเคชันจากการตั้งค่าคอนฟิกนี้จะถูกนำเสนอ ในขณะที่การแม็ปแบบจำลองนี้จะถูกออกแบบ 

6. คลิก **ตัวออกแบบ** 
7. คลิก **ตัวออกแบบ** 
8. ในแผนภูมิ ให้เลือก **Dynamics 365 for Operations\เรกคอร์ดตาราง** 
9. คลิก **เพิ่มราก** 
10. ในฟิลด์ **ตาราง** ให้ป้อนหรือเลือกค่า 

    > [!NOTE]
    > ในขณะนี้ การแม็ปนี้อ้างอิงถึงการตั้งค่าคอนฟิกข้อมูลเมตา ข้อมูลเมตาของแอพลิเคชันจากการตั้งค่าคอนฟิกนี้จะถูกนำเสนอ ในขณะที่การแม็ปแบบจำลองนี้จะถูกออกแบบ 

11. คลิก **ยกเลิก** 
12. ปิดหน้า 
13. ปิดหน้า 

## <a name="assign-connected-application-to-model-mapping"></a>กำหนดแอพลิเคชันที่เชื่อมโยงให้กับการแม็ปแบบจำลอง 
1. คลิก **แก้ไข** 
2. เลือกแอพลิเคชัน **MyConnectedApp** 

    > [!NOTE]
    > ในปัจจุบัน การแม็ปนี้อ้างอิงถึงข้อมูลเมตาของแอพลิเคชันที่เชื่อมต่อที่เลือก เมื่อการแม็ปเดียวกันอ้างอิงถึงการตั้งค่าคอนฟิกข้อมูลเมตาและแอพลิเคชันที่เชื่อมต่อในเวลาเดียวกัน จะมีการใช้ข้อมูลเมตาของแอพลิเคชันที่เชื่อมต่อ 

3. คลิก **ตัวออกแบบ** 
4. คลิก **ตัวออกแบบ** 
5. ในแผนภูมิ ให้เลือก **Dynamics 365 for Operations\เรกคอร์ดตาราง** 
6. คลิก **เพิ่มราก** 
7. ในฟิลด์ **ตาราง** ให้ป้อนหรือเลือกค่า 

    > [!NOTE]
    > มีการนำเสนอตารางแอพลิเคชันมากกว่าสองตารางในขณะนี้ เนื่องจากการแม็ปนี้ใช้ข้อมูลเมตาของแอพลิเคชันที่เชื่อมต่อทั้งหมดที่ได้รับการกำหนดไว้แล้ว 

8. คลิก **ยกเลิก** 
9. คลิก **ตรวจสอบความถูกต้อง** 

    > [!NOTE]
    > เราประสบความสำเร็จในการผูกองค์ประกอบของแบบจำลองข้อมูลกับรายการของแหล่งข้อมูลที่อธิบาย โดยใช้รายละเอียดของข้อมูลเมตาของแอพลิเคชันที่เชื่อมต่อซึ่งได้รับการกำหนดสำหรับการแม็ปนี้ 

10. ปิดหน้า 
11. ปิดหน้า 

เมื่อคุณต้องการประเมินการแม็ปแบบจำลองนี้โดยใช้ข้อมูลเมตาของแอพลิเคชันรุ่นอื่น ลงทะเบียนแอพลิเคชันอื่นที่เชื่อมต่อ กำหนดให้กับการแม็ปแบบจำลองนี้ และตรวจสอบความถูกต้องเทียบกับข้อมูลเมตาใหม่


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

