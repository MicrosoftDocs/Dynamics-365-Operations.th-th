---
title: ตั้งค่าคอนฟิกเอนทิตีเสมือน Common Data Service
description: หัวข้อนี้แสดงวิธีการตั้งค่าคอนฟิกเอนทิตีเสมือนสำหรับ Dynamics 365 Human Resources สร้างและอัพเดตข้อมูลเอนทิตีเสมือนที่มีอยู่ และวิเคราะห์เอนทิตีที่สร้างและพร้อมใช้งาน
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645612"
---
# <a name="configure-common-data-service-virtual-entities"></a>ตั้งค่าคอนฟิกเอนทิตีเสมือน Common Data Service

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources เป็นแหล่งข้อมูลเสมือนใน Common Data Service ซึ่งให้การดำเนินการส้ราง อ่าน อัปเดต และลบทั้งหมด (CRUD) จาก Common Data Service และ Microsoft Power Platform ข้อมูลสำหรับเอนทิตีเสมือนไม่ได้จัดเก็บไว้ใน Common Data Service แต่อยู่ในฐานข้อมูลใบสมัคร 

เมื่อต้องการเปิดใช้งานการดำเนินงาน CRUD บนเอนทิตีทรัพยากรบุคคลจาก Common Data Service คุณต้องทำให้เอนทิตีพร้อมใช้งานเป็นเอนทิตีเสมือนใน Common Data Service ซึ่งช่วยให้คุณสามารถทำการดำเนินงาน CRUD จาก Common Data Service และ Microsoft Power Platform บนข้อมูลที่อยู่ในทรัพยากรบุคคล การดำเนินงานยังสนับสนุนการตรวจสอบตรรกะทางธุรกิจทั้งหมดของทรัพยากรบุคคล เพื่อให้มั่นใจในความสมบูรณ์ของข้อมูลเมื่อเขียนข้อมูลไปยังเอนทิตี

## <a name="available-virtual-entities-for-human-resources"></a>เอนทิตีเสมือนพร้อมใช้งานสำหรับทรัพยากรบุคคล

เอนทิตี Open Data Protocol (OData) ทั้งหมดในทรัพยากรบุคคลพร้อมใช้งานเป็นเอนทิตีเสมือนใน Common Data Service นอกจากนี้ยังพร้อมใช้งานใน Power Platform ด้วย ขณะนี้ คุณสามารถสร้างแอปและประสบการณ์พร้อมกับข้อมูลโดยตรงจากทรัพยากรบุคคลที่มีความสามารถ CRUD เต็มที่ โดยไม่มีการคัดลอกหรือการซิงโครไนส์ข้อมูลไปยัง Common Data Service คุณสามารถใช้พอร์ทัล Power Apps เพื่อสร้างเว็บไซต์ที่เชื่อมต่อกับภายนอก ซึ่งเปิดใช้งานสถานการณ์การทำงานร่วมกันสำหรับกระบวนการทางธุรกิจในทรัพยากรบุคคล

คุณสามารถดูรายการเอนทิตีเสมือนที่เปิดใช้งานในสภาพแวดล้อม และเริ่มต้นการทำงานกับเอนทิตีใน [Power Apps](https://make.powerapps.com) ในโซลูชัน **เอนทิตีเสมือนของ Dynamics 365 HR**

![เอนทิตีเสมือนของ Dynamics 365 HR ใน Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>เอนทิตีเสมือนกับเอนทิตีธรรมชาติ

เอนทิตีเสมือนสำหรับทรัพยากรบุคคลไม่เหมือนกับเอนทิตี Common Data Service ธรรมชาติที่สร้างขึ้นสำหรับทรัพยากรบุคคล เอนทิตีธรรมชาติสำหรับทรัพยากรบุคคลสร้างขึ้นแยกต่างหาก และรักษาไว้ในโซลูชันทั่วไปของ HCM ใน Common Data Service ด้วยเอนทิตีธรรมชาติ ข้อมูลจะถูกจัดเก็บไว้ใน Common Data Service และต้องมีการซิงโครไนส์กับฐานข้อมูลใบสมัครทรัพยากรบุคคล

> [!NOTE]
> สำหรับรายการของเอนทิตี Common Data Service ธรรมชาติสำหรับทรัพยากรบุคคล ให้ดูที่ [เอนทีตี Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities)

## <a name="setup"></a>ตั้งค่า

ทำตามขั้นตอนการตั้งค่าต่อไปนี้เพื่อเปิดใช้งานเอนทิตีเสมือนในสภาพแวดล้อมของคุณ

### <a name="enable-virtual-entities-in-human-resources"></a>เปิดใช้งานเอนทิตีเสมือนในทรัพยากรบุคคล

ก่อนอื่นคุณต้องเปิดใช้งานเอนทิตีเสมือนในพื้นที่ทำงาน **การจัดการคุณลักษณะ**

1. ในทรัพยากรบุคคล เลือก **การจัดการระบบ**

2. เลือกไทล์ **การจัดการคุณลักษณะ**

3. เลือก **การสนับสนุนเอนทิตีเสมือนใน HR/CDS** แล้วจากนั้น เลือก **เปิดใช้งาน**

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานและการปิดใช้งานคุณลักษณะ ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)

### <a name="register-the-app-in-microsoft-azure"></a>ลงทะเบียนแอปใน Microsoft Azure

คุณต้องลงทะเบียนอินสแตนซ์ทรัพยากรบุคคลของคุณในพอร์ทัล Azure เพื่อให้แพลตฟอร์มข้อมูลเฉพาะของ Microsoft สามารถให้บริการการรับรองความถูกต้องและการตรวจสอบความถูกต้องสำหรับแอปและผู้ใช้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการลงทะเบียนแอปใน Azure ดูที่ [การเริ่มต้นแบบด่วน: ลงทะเบียนโปรแกรมประยุกต์ด้วยฟอร์มข้อมูลเฉพาะของ Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)

1. เปิด [พอร์ทัล Microsoft Azure](https://portal.azure.com)

2. ในรายการบริการ Azure เลือก **การลงทะเบียนแอป**

3. เลือก **การลงทะเบียนใหม่**

4. ในฟิลด์ **ชื่อ** ให้ป้อนชื่อที่เป็นคำอธิบายสำหรับแอป ตัวอย่างเช่น **เอนทีตีเสมือน Dynamics 365 Human Resources**

5. ในฟิลด์ **เปลี่ยนเส้นทาง URI** ให้ป้อน URL พื้นที่ว่างในชื่อของอินสแตนซ์ของทรัพยากรบุคคลของคุณ

6. เลือก **การลงทะเบียน**

7. เมื่อลงทะเบียนเสร็จสมบูรณ์แล้ว พอร์ทัล Azure จะแสดงบานหน้าต่าง **ภาพรวม** ของการลงทะเบียนของแอป ซึ่งรวมถึง **รหัสโปรแกรมประยุกต์ (ไคลเอนต์)** จด **รหัสโปรแกรมประยุกต์ (ไคลเอนต์)** ในขณะนี้ คุณจะป้อนข้อมูลนี้เมื่อคุณ [ตั้งค่าคอนฟิกแหล่งข้อมูลเอนทิตีเสมือน](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)

8. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ใบรับรองและข้อมูลลับ**

9. ในส่วน **ข้อมูลลับของไคลเอนต์** ของหน้า ให้เลือก **ข้อมูลลับของไคลเอนต์ใหม่**

10. ระบุคำอธิบาย เลือกช่วงเวลา และเลือก **เพิ่ม**

11. บันทึกค่าของข้อมูลลับ คุณจะป้อนข้อมูลนี้เมื่อคุณ [ตั้งค่าคอนฟิกแหล่งข้อมูลเอนทิตีเสมือน](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)

    > [!IMPORTANT]
    > ตรวจสอบให้แน่ใจว่าได้จดบันทึกค่าของข้อมูลลับไว้ในขณะนี้ ข้อมูลลับจะไม่มีการแสดงอีกครั้งหลังจากที่คุณออกจากหน้านี้

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>ติดตั้งแอป Dynamics 365 HR Virtual Entity

ติดตั้งแอป Dynamics 365 HR Virtual Entity ในสภาพแวดล้อม Power Apps ของคุณ เพื่อจัดวางแพคเกจโซลูชันเอนทิตีเสมือนไปยัง Common Data Service

1. เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)

2. ในรายการ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม Power Apps ที่สัมพันธ์กับอินสแตนซ์ทรัพยากรบุคคลของคุณ

3. ในส่วน **ทรัพยากร** ของหน้า ให้เลือก **แอป Dynamics 365**

4. เลือกการดำเนินการ **ติดตั้งแอป**

5. เลือก **Dynamics 365 HR Virtual Entity** และเลือก **ถัดไป**

6. ตรวจทานและทำเครื่องหมายเพื่อยอมรับข้อตกลงการให้บริการ

7. เลือก **ติดตั้ง**

การติดตั้งใช้เวลาสองสามนาที เมื่อเสร็จสิ้น ให้ดำเนินการขั้นตอนต่อไป

![ติดตั้งแอป Dynamics 365 HR Virtual Entity จากศูนย์การจัดการ Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>ตั้งค่าคอนฟิกแหล่งข้อมูลสำหรับเอนทิตีเสมือน 

ขั้นตอนต่อไปคือการตั้งค่าคอนฟิกแหล่งข้อมูลสำหรับเอนทิตีเสมือนในสภาพแวดล้อม Power Apps 

1. เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)

2. ในรายการ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม Power Apps ที่สัมพันธ์กับอินสแตนซ์ทรัพยากรบุคคลของคุณ

3. เลือก **URL ของสภาพแวดล้อม** ในส่วน **รายละเอียด** ของหน้า

4. ใน **ฮับความสมบูรณ์ของโซลูชัน** ให้เลือกไอคอน **การค้นหาขั้นสูง** ที่ด้านบนขวาของหน้าโปรแกรมประยุกต์

5. บนหน้า **การค้นหาขั้นสูง** ในรายการแบบเลื่อนลง **ค้นหา** ให้เลือก **การตั้งค่าคอนฟิกแหล่งข้อมูลเสมือน Finance and Operations**

6. เลือก **ผลลัพธ์**

7. เลือกเรกคอร์ด **แหล่งข้อมูล Microsoft HR**

8. ป้อนข้อมูลที่จำเป็นสำหรับการตั้งค่าคอนฟิกแหล่งข้อมูล:

   - **URL เป้าหมาย**: URL ของพื้นที่ว่างในชื่อทรัพยากรบุคคลของคุณ รูปแบบของ URL เป้าหมายคือ:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     ตัวอย่างเช่น:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >ตรวจสอบให้แน่ใจว่าได้รวมอักขระ "**/**" เมื่อสิ้นสุด URL เพื่อหลีกเลี่ยงการรับข้อผิดพลาด

   - **รหัสผู้เช่า**: รหัสผู้เช่า Azure Active Directory (Azure AD)

   - **รหัสโปรแกรมประยุกต์ AAD**: รหัสโปรแกรมประยุกต์ (ไคลเอนต์) ที่สร้างขึ้นสำหรับใบสมัครที่ลงทะเบียนไว้ในพอร์ทัล Microsoft Azure คุณได้รับข้อมูลนี้ก่อนหน้านี้ระหว่างขั้นตอนการ [ลงทะเบียนโปรแกรมประยุกต์ใน Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)

   - **ข้อมูลลับโปรแกรมประยุกต์ AAD**: ข้อมูลลับของไคลเอนต์ที่สร้างขึ้นสำหรับใบสมัครที่ลงทะเบียนไว้ในพอร์ทัล Microsoft Azure คุณได้รับข้อมูลนี้ก่อนหน้านี้ระหว่างขั้นตอนการ [ลงทะเบียนโปรแกรมประยุกต์ใน Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)

   ![แหล่งข้อมูล Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. เลือก **บันทึกและปิด**

### <a name="grant-app-permissions-in-human-resources"></a>ให้สิทธิ์แอปใน Human Resources

ให้สิทธิสำหรับใบสมัคร Azure AD สองใบในทรัพยากรบุคคล:

- แอปที่สร้างขึ้นสำหรับผู้เช่าของคุณในพอร์ทัล Microsoft Azure
- แอป Dynamics 365 HR Virtual Entity ที่ติดตั้งในสภาพแวดล้อม Power Apps 

1. ในทรัพยากรบุคคล ให้เปิดหน้า **ใบสมัคร Azure Active Directory**

2. เลือก **สร้าง** เพื่อสร้างเรกคอร์ดใบสมัครใหม่:

    - ในฟิลด์ **รหัสไคลเอนต์** ให้ป้อนรหัสไคลเอนต์ของแอปที่คุณลงทะเบียนไว้ในพอร์ทัล Microsoft Azure
    - ในฟิลด์ **ชื่อ** ให้ป้อนชื่อของแอปที่คุณลงทะเบียนไว้ในพอร์ทัล Microsoft Azure
    - ในฟิลด์ **รหัสผู้ใช้** ให้เลือกรหัสผู้ใช้ของผู้ใช้ที่มีสิทธิ์ผู้ดูแลระบบในทรัพยากรบุคคลและสภาพแวดล้อม Power Apps

3. เลือก **สร้าง** เพื่อสร้างเรกคอร์ดใบสมัครที่สอง:

    - **รหัสไคลเอนต์**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **ชื่อ**: Dynamics 365 HR Virtual Entity
    - ในฟิลด์ **รหัสผู้ใช้** ให้เลือกรหัสผู้ใช้ของผู้ใช้ที่มีสิทธิ์ผู้ดูแลระบบในทรัพยากรบุคคลและสภาพแวดล้อม Power Apps

## <a name="generate-virtual-entities"></a>สร้างคอนฟิกเอนทิตีเสมือน

เมื่อการตั้งค่าเสร็จสมบูรณ์ คุณสามารถเลือกเอนทิตีเสมือนที่คุณต้องการสร้างและเปิดใช้งานในอินสแตนซ์ Common Data Service ของคุณได้

1. ในทรัพยากรบุคคล ให้เปิดหน้า **การรวม Common Data Service (CDS)**

2. เลือกแท็บ **เอนทิตีเสมือน**

> [!NOTE]
> การสลับ **เปิดใช้งานเอนทิตีเสมือน** จะถูกตั้งค่าเป็น **ใช่** โดยอัตโนมัติเมื่อการตั้งค่าที่จำเป็นทั้งหมดเสร็จสมบูรณ์แล้ว ถ้าการสลับถูกตั้งค่าเป็น **ไม่ใช่** ให้ตรวจสอบขั้นตอนในหัวข้อก่อนหน้านี้ของเอกสารนี้ เพื่อให้แน่ใจว่าการตั้งค่าข้อกำหนดเบื้องต้นทั้งหมดเสร็จสมบูรณ์แล้ว

3. เลือกเอนทิตีหรือเอนทิตีมากกว่าหนึ่งที่คุณต้องการสร้าง Common Data Service

4. เลือก **สร้าง/รีเฟรช**

![การรวม Common Data Service](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a>ตรวจสอบสถานะการสร้างเอนทิตี

เอนทิตีเสมือนมีการสร้างใน Common Data Service โดยผ่านกระบวนการพื้นหลังแบบอะซิงโครนัส การอัปเดตในกระบวนการแสดงในศูนย์การดำเนินการ รายละเอียดเกี่ยวกับกระบวนการ รวมถึงล็อกข้อผิดพลาด จะปรากฏในหน้า **กระบวนการระบบอัตโนมัติ**

1. ในทรัพยากรบุคคล ให้เปิดเพจรายการ **กระบวนการระบบอัตโนมัติ**

2. เลือกแท็บ **กระบวนการแบบเบื้องหลัง**

3. เลือก **กระบวนการแบบเบื้องหลังของการดำเนินงานแบบอะซิงโครนัสในการสำรวจเอนทิตีเสมือน**

4. เลือก **ดูผลลัพธ์ล่าสุด**

บานหน้าต่าง slideout แสดงผลลัพธ์การดำเนินการล่าสุดสำหรับกระบวนการ คุณสามารถดูล็อกสำหรับกระบวนการ รวมถึงข้อผิดพลาดที่ส่งคืนจาก Common Data Service

## <a name="see-also"></a>ดูเพิ่มเติมที่

[Common Data Service คืออะไร](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[ภาพรวมของเอนทิตี](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[ภาพรวมความสัมพันธ์ของเอนทิตี](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[สร้างและแก้ไขเอนทิตีเสมือนที่มีข้อมูลจากแหล่งข้อมูลภายนอก](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[พอร์ทัล Power Apps คืออะไร](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[ภาพรวมของการสร้างแอปใน Power Apps](https://docs.microsoft.com/powerapps/maker/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]