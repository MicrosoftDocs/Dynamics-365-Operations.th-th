---
title: บทนํา API การรวมระบบการติดตามผู้สมัคร
description: 'หัวข้อนี้อธิบายระบบติดตามผู้สมัคร (ATS) Dynamics 365 Human Resources การรวม API '
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61d8502a8f420d387b5b7f48fca2f8a680f6f3f8
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464043"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>บทนํา API การรวมระบบการติดตามผู้สมัคร

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายระบบติดตามผู้สมัคร (ATS) Dynamics 365 Human Resources การรวม API  วัตถุประสงค์ของ API คือการเปิดใช้งานการรวมอย่างมีประสิทธิภาพระหว่าง Dynamics 365 Human Resources และการเป็นพันธมิตร ATS

![ลำดับการรวม ATS](media/hr-admin-integration-ats-api-introduction-flow.png)

ประสบการณ์แบบรวมจะเริ่มต้นในทรัพยากรบุคคลเมื่อผู้จัดการการว่าจ้างสร้างคำขอการสรรหาบุคลากร เมื่อคำขอถูกเปิดใช้งาน ATS จะดึงรายละเอียดสำหรับคำขอเพื่อสร้างโครงการสรรหาบุคลากร จากนั้นจะติดตามไปป์ไลน์การสรรหาบุคลากรเพื่อเลือกและจ้างผู้สมัครสำหรับตําแหน่งงานต่างๆ ในขั้นตอนสุดท้าย ATS จะทำการรวมแบบไปกลับให้เสร็จสมบูรณ์โดยการส่งเรกคอร์ดของผู้สมัครที่เลือกไปยังฝ่ายทรัพยากรบุคคล จากนั้นเรกคอร์ดผู้สมัครจะสามารถผ่านการตรวจสอบความถูกต้องและการจัดเรียงลำดับงานเพื่อสร้างเรกคอร์ดพนักงานได้

เมื่อต้องการเปิดใช้งานการรวม ทรัพยากรบุคคลได้เพิ่มส่วนประกอบต่อไปนี้

1.  ฟังก์ชันในการสร้างคำขอการสรรหาบุคลากร
2.  โพรไฟล์ผู้สมัครที่ขยายและที่เกี่ยวข้องกับลำดับงาน
3.  API การรวมจะเปิดฟังก์ชันใหม่เพื่อรวมใบสมัคร

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าและการใช้คำขอการสรรหาบุคลากรและฟังก์ชันผู้สมัคร โปรดดูที่ [สรรหาผู้สมัครงาน](hr-personnel-recruit.md)

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

API นี้จะสร้างขึ้นบน Microsoft Dataverse (ซึ่งก่อนหน้านี้เรียกว่า Common Data Service) การโต้ตอบ RESTful ทั้งหมดกับ API นี้กระทำผ่าน Microsoft Dataverse Web API ที่ใช้ OData API นี้เป็นเซ็ตย่อยของ Dataverse Web API Dataverse Web API จะกําหนดลักษณะต่างๆ เช่น การพิสูจน์ตัวจริง SLAs ชุดงาน การควบคุมการเกิดพร้อมกัน และการจัดการข้อผิดพลาด

สำหรับข้อมูลเพิ่มเติมทั่วไปเกี่ยวกับ Microsoft Dataverse Web API ให้ดูที่

- [Microsoft Dataverse คืออะไร](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [ใช้ Microsoft Dataverse Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse คู่มือสำหรับนักพัฒนา](https://docs.microsoft.com/powerapps/developer/data-platform)

เอกสารข้างต้นจะประกอบด้วยรายละเอียดและแนวทางของนักพัฒนาในการใช้ Dataverse Web API เช่น [การจัดการการพิสูจน์ตัวจริง](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api) [การดำเนินงาน](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api) [การใช้บุรุษไปรษณีย์กับ API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) และ [การใช้การเปลี่ยนแปลงการติดตามหรือโทเคนที่ว่างเปล่า](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) กับ the API

### <a name="option-sets"></a>ชุดตัวเลือก

แบบจำลองข้อมูลสำหรับการรวม ATS API อธิบายไว้ในเอกสารนี้รวมถึงชุดตัวเลือกที่ระบุค่าที่ระบุหมายเลขที่สัมพันธ์กับคุณสมบัติเอนทิตี้ สำหรับรายละเอียดเกี่ยวกับชุดตัวเลือกใน Dataverse Web API ให้ดูที่ [ชุดตัวเลือกการสร้างและการอัพเดตโดยใช้ Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets) ชุดตัวเลือกถูกกําหนดไว้ให้กับ Dataverse แต่ละสภาพแวดล้อม

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>ตารางเสมือนสำหรับทรัพยากรบุคคล Dataverse

ปลายทางสำหรับ API การรวม ATS ใช้ความสามารถของแพลตฟอร์มตารางเสมือนของ Microsoft Dataverse โดยค่าเริ่มต้น ตารางเสมือนและปลายทาง API ที่เกี่ยวข้องจะไม่ปรับใช้กับสภาพแวดล้อมของทรัพยากรบุคคล การเปิดใช้งานองค์กรเพื่อระบุว่าปลายทาง OData ใดจะแสดงต่อสภาพแวดล้อม เมื่อต้องการใช้ API ตารางเสมือนของเอนทิตี้ทรัพยากรบุคคลจะต้องสร้างให้กับสภาพแวดล้อม 

สำหรับข้อมูลเกี่ยวกับการสร้างตารางเสมือนของ API ให้ดูที่ [การตั้งค่าคอนฟิกตารางเสมือน Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities)

## <a name="data-model"></a>แบบจำลองข้อมูล

แบบจำลองข้อมูลมีศูนย์กลางอยู่ประมาณเอนทิตี้หลักสองเอนทิตี้

- **RecruitingRequest** แสดงถึงคำขอของ ATS เพื่อสรรหาบุคลากรในตําแหน่งที่เปิดรับอย่างน้อยหนึ่งตําแหน่ง ตัวอย่างเช่นการสอบถาม ให้ดูที่ [ตัวอย่างการสอบถามสำหรับคำขอการสรรหาบุคคลากร](hr-admin-integration-ats-api-recruiting-request-example-query.md)
- **CandidateToHire** แสดงถึงรายละเอียดของผู้สมัครที่ได้ยอมรับข้อเสนอในตําแหน่งงาน **บุคคล** แสดงถึงบุคคลที่เป็นผู้สมัคร บุคคลสามารถมีบทบาทในบริษัทได้หลายบทบาท เช่น ผู้สมัคร ผู้ปฏิบัติงาน พนักงาน หรือผู้รับเหมา สำหรับตัวอย่างการสอบถาม ให้ดูที่ [ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

แผนภาพต่อไปนี้แสดงความสัมพันธ์ภายใน API หลายชนิดมีคีย์นอกไปยังเป็นเอนทิตี้ที่มีอยู่ก่อนอื่นๆในทรัพยากรบุคคลที่ไม่ได้แสดงที่นี่ เอกสารนี้แสดงข้อมูลเกี่ยวกับเอนทิตี้ที่เฉพาะเจาะจงให้กับสถานการณ์การรวมการสรรหาบุคลากร อย่างไรก็ตาม มีเอนทิตี้อื่นหลายเอนทิตี้ใน Dataverse Web API สำหรับ Dynamics 365 Human Resources ซึ่งอาจเกี่ยวข้องกับการรวมของคุณด้วย ตัวอย่างเช่น คุณอาจต้องการรายละเอียดเกี่ยวกับผู้ปฏิบัติงาน งาน ตําแหน่งงาน หรือเอนทิตี้อื่นๆที่ไม่ได้กําหนดที่นี่ด้วย เอนทิตี้จากเอนทิตี้เหล่านี้ถูกอ้างอิงในความสัมพันธ์คีย์นอกหรือคุณสมบัติการนําทาง

![แบบจำลองข้อมูล API การรวม ATS](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>คำขอการสรรหาบุคลากรและเอนทิตี้และชุดตัวเลือกที่เกี่ยวข้อง

ตัวอย่างการสอบถาม 

- [ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request-example-query.md)

เอนทิตี้:

- [คำขอสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request.md)
- [ตำแหน่งของคำขอสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request-position.md)
- [การสรรหาบุคลากรที่มีคำขอทักษะ](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [การสรรหาบุคลากรที่มีคำขอการศึกษา](hr-admin-integration-ats-api-recruiting-request-education.md)
- [ที่ตั้งของคำขอสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request-location.md)

ชุดตัวเลือก

- [สถานะยกเว้นงาน](hr-admin-integration-ats-api-job-exempt-status.md)
- [สถานะการสรรหาบุคลากรที่มีคำขอตำแหน่ง](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [สถานะคำขอขการสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request-status.md)
- [ประเภทงานตามระเบียบบังคับ](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>ผู้สมัครที่จะว่าจ้างและเอนทิตี้และชุดตัวเลือกที่เกี่ยวข้อง

ตัวอย่างการสอบถาม

- [ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

เอนทิตี้:

- [ผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire.md)
- [บุคคล](hr-admin-integration-ats-api-person.md)
- [การศึกษาของบุคคล](hr-admin-integration-ats-api-person-education.md)
- [ประสบการณ์การทำงานของบุคคล](hr-admin-integration-ats-api-person-professional-experience.md)
- [ที่อยู่ของบุคคล](hr-admin-integration-ats-api-person-address.md)
- [ผู้ติดต่อฝ่าย](hr-admin-integration-ats-api-party-contact.md)
- [ทักษะของบุคคล](hr-admin-integration-ats-api-person-skill.md)
- [ระดับการประเมิน](hr-admin-integration-ats-api-rating-level.md)
- [ใบรับรองของบุคคล](hr-admin-integration-ats-api-person-certificate.md)
- [ชนิดของประกาศนียบัตร](hr-admin-integration-ats-api-certificate-type.md)
- [การคัดเลือกบุคคล](hr-admin-integration-ats-api-person-screening.md)
- [ชนิดการคัดเลือก](hr-admin-integration-ats-api-screening-types.md)
- [หมายเลขการระบุรหัสประจำตัวบุคคล](hr-admin-integration-ats-api-person-identification-number.md)

ชุดตัวเลือก

- [ผลการรวมผู้สมัคร](hr-admin-integration-ats-api-applicant-integration-result.md)
- [ว่าง ใช่ ไม่ใช่](hr-admin-integration-ats-api-blank-yes-no.md)
- [สถานะการเสร็จสมบูรณ์](hr-admin-integration-ats-api-completion-status.md)
- [ชนิดผู้ติดต่อ](hr-admin-integration-ats-api-contact-type.md)
- [เกณฑ์หน่วยกิตการศึกษา](hr-admin-integration-ats-api-education-credit-basis.md)
- [เพศ](hr-admin-integration-ats-api-gender.md)
- [สถานภาพการสมรส](hr-admin-integration-ats-api-marital-status.md)
- [เดือนของปี](hr-admin-integration-ats-api-months-of-year.md)
- [ไม่ ใช่](hr-admin-integration-ats-api-no-yes.md)
- [หน่วยของรอบระยะเวลา](hr-admin-integration-ats-api-period-unit.md)
- [ความถี่ในการคัดกรอง](hr-admin-integration-ats-api-screening-frequency.md)
- [ความถี่ในการคัดกรองที่สร้างจาก](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [ชนิดระดับทักษะ](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[สรรหาผู้สมัครงาน](hr-personnel-recruit.md)<br>
[Microsoft Dataverse คืออะไร](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[ใช้ Microsoft Dataverse Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[สร้างและอัพเดตชุดตัวเลือกโดยใช้ Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]