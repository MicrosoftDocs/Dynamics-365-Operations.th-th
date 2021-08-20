---
title: บทนำ API การรวมบัญชีเงินเดือน
description: หัวข้อนี้อธิบายAPI การรวมบัญชีเงินเดือน Dynamics 365 Human Resources
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7122dc7325c7fb33c4bf90e3d1a6cf1c95bd73e72232b9060f7cc04899223765
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782718"
---
# <a name="payroll-integration-api-introduction"></a>บทนำ API การรวมบัญชีเงินเดือน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

เอกสารนี้อธิบายAPI การรวมบัญชีเงินเดือน Dynamics 365 Human Resources API จะเปิดใช้งานการรวมแบบครอบคลุมที่มีประสิทธิภาพระหว่างทรัพยากรบุคคลและระบบบัญชีเงินเดือนที่เป็นคู่ค้า ประสบการณ์รวมจะเริ่มต้นในทรัพยากรบุคคลพร้อมด้วยโปรไฟล์พนักงาน เงินเดือนและการหักลด และข้อมูลเงินสมทบ เมื่อคุณจ้างงานพนักงานและป้อนโปรไฟล์ที่ต้องใช้และจ่ายข้อมูลเข้าในทรัพยากรบุคคล ระบบบัญชีเงินเดือนจะดึงข้อมูลนี้เพื่อใช้เมื่อประมวลผลค่าจ้าง การอัปเดตใด ๆ ที่พนักงานหรือข้อมูลค่าจ้างจะถูกดึงไว้เพื่อใช้ในการรันค่าจ้างในภายหลังด้วย

[![โฟลว์การรวมบัญชีเงินเดือน](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

เมื่อต้องการเปิดใช้งานการรวม ทรัพยากรบุคคลได้รวมส่วนประกอบต่อไปนี้:

- [ฟังก์ชันในการทำเครื่องหมายพนักงานเป็นพร้อมจ่าย](hr-compensation-payroll.md)
- API การรวมจะเปิดฟังก์ชันใหม่เพื่อรวมใบสมัคร

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

API นี้จะสร้างขึ้นบน Microsoft Dataverse (ซึ่งก่อนหน้านี้เรียกว่า Common Data Service) การโต้ตอบ RESTful ทั้งหมดกับ API นี้กระทำผ่าน Microsoft Dataverse Web API ที่ใช้ OData API นี้เป็นเซ็ตย่อยของ Dataverse Web API Dataverse Web API จะกําหนดลักษณะต่างๆ เช่น การพิสูจน์ตัวจริง SLAs ชุดงาน การควบคุมการเกิดพร้อมกัน และการจัดการข้อผิดพลาด

สำหรับข้อมูลเพิ่มเติมทั่วไปเกี่ยวกับ Microsoft Dataverse Web API ให้ดูที่

- [Microsoft Dataverse คืออะไร](/powerapps/maker/data-platform/data-platform-intro)
- [ใช้ Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse คู่มือสำหรับนักพัฒนา](/powerapps/developer/data-platform)

คู่มือนี้รวมรายละเอียดและแนวทางของนักพัฒนาในการใช้ Dataverse Web API รวมถึงหัวข้อต่อไปนี้:

- [รวจสอบความถูกต้อง Microsoft Dataverse กับ Web API](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [ดําเนินงานโดยใช้ Web API](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [ใช้ Postman กับ Web API](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [ใช้การติดตามการเปลี่ยนแปลงเพื่อซิงโครไนส์ข้อมูลกับระบบภายนอก](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>ตารางเสมือนสำหรับทรัพยากรบุคคล Dataverse

ปลายทางสำหรับ API การรวมค่าจ้างใช้ความสามารถของแพลตฟอร์มตารางเสมือนของ Microsoft Dataverse โดยค่าเริ่มต้น ตารางเสมือนและปลายทาง API ที่เกี่ยวข้องจะไม่ปรับใช้กับสภาพแวดล้อมของทรัพยากรบุคคล การเปิดใช้งานองค์กรเพื่อระบุว่าปลายทาง OData ใดจะแสดงต่อสภาพแวดล้อม เมื่อต้องการใช้ API ตารางเสมือนของเอนทิตี้ทรัพยากรบุคคลจะต้องสร้างให้กับสภาพแวดล้อม

สำหรับข้อมูลเกี่ยวกับการสร้างตารางเสมือนของ API ให้ดูที่ [การตั้งค่าคอนฟิกตารางเสมือน Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md)

## <a name="data-model"></a>แบบจำลองข้อมูล

แผนภาพต่อไปนี้แสดงความสัมพันธ์ภายใน API หลายชนิดมีคีย์นอกไปยังเป็นเอนทิตี้ที่มีอยู่ก่อนอื่นๆในทรัพยากรบุคคลที่ไม่ได้แสดงที่นี่ เอกสารนี้แสดงข้อมูลเกี่ยวกับเอนทิตี้ที่เฉพาะเจาะจงให้กับสถานการณ์การรวมระบบค่าจ้าง อย่างไรก็ตาม มีเอนทิตีอื่นหลายเอนทิตีใน Dataverse Web API สำหรับทรัพยากรบุคคลซึ่งอาจเกี่ยวข้องกับการรวมของคุณด้วย บางเอนทิตีจากเอนทิตีเหล่านี้ถูกอ้างอิงในความสัมพันธ์คีย์นอกหรือคุณสมบัติการนําทาง

[![แบบจำลองข้อมูล API การรวมระบบค่าจ้าง](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>พนักงานค่าจ้างและเอนทิตีที่เกี่ยวข้อง

เอนทิตี้:

- [พนักงานในบัญชีเงินเดือน](hr-admin-integration-payroll-api-payroll-employee.md)
- [ที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [แผนค่าตอบแทนคงที่ของบัญชีเงินเดือน](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [แผนค่าตอบแทนผันแปรในบัญชีเงินเดือน](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [งานของตําแหน่งในบัญชีเงินเดือน](hr-admin-integration-payroll-api-payroll-position-job.md)
- [ตําแหน่งในบัญชีเงินเดือน](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[สร้างและตรวจทานเอนทิตี้บัญชีเงินเดือน](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[ตั้งค่าคอนฟิกพารามิเตอร์ทรัพยากรบุคคล](hr-setup-parameters.md)<br>
[ตั้งค่าคอนฟิกพารามิเตอร์ที่ใช้ร่วมกันของทรัพยากรบุคคล](hr-setup-shared-parameters.md)<br>
[Microsoft Dataverse คืออะไร](/powerapps/maker/data-platform/data-platform-intro)<br>
[ใช้ Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
