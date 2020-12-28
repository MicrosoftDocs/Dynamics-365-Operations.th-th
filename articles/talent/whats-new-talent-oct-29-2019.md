---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (29 ตุลาคม 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529695"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (29 ตุลาคม 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR

การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2586 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>ลบฝ่ายที่ไม่มีบทบาทตามค่าเริ่มต้น (371233)

เมื่อคุณจัดเตรียมสภาพแวดล้อมใหม่ใน Talent **ให้ลบฝ่ายออกถ้าไม่มีบทบาท** เปิดอยู่ตามค่าเริ่มต้น เมื่อคุณลบผู้ปฏิบัติงาน ฝ่ายที่เชื่อมโยงกับผู้ปฏิบัติงานจะไม่ถูกลบออกเว้นแต่การตั้งค่านี้เปิดอยู่ การเปลี่ยนแปลงนี้จะจำกัดเรกคอร์ดที่ซ้ำกันในสมุดที่อยู่สากลเมื่อคุณต้องการนำเข้า เปลี่ยนแปลง หรือนำเข้าผู้ปฏิบัติงานอีกครั้ง

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>การร้องขอการลางานแบบร่างและการยกเลิกควรถูกลบใน Common Data Service (376999)

เมื่อมีการเปลี่ยนแปลงนี้คุณสามารถลบการร้องขอที่มีสถานะเป็น **แบบร่าง** หรือ **ถูกยกเลิก** ใน Common Data Service

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>ค่ารายการเพิ่มเติมในฟิลด์ที่กำหนดเองจะไม่มีผลใน Common Data Service หลังจากที่คลิกใช้บนแบบฟอร์มฟิลด์ที่กำหนดเอง (379599)

เมื่อคุณเพิ่มค่ารายการใหม่ไปยังฟิลด์แบบกำหนดเองที่มีอยู่ ซึ่งมีการซิงโครไนส์อยู่แล้วกับ Common Data Service ขณะนี้มีอยู่ใน Common Data Serivce หลังจากที่คุณใช้การเปลี่ยนแปลงในแบบฟอร์ม **ฟิลด์ที่กำหนดเอง**

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>ใช้รายการตรวจสอบความพร้อมสำหรับนิติบุคคลเมื่อมีการจ้างงานมากกว่าหนึ่งรายการ (371270)

ในการนำออกใช้ของสัปดาห์นี้ คุณสามารถใช้รายการตรวจสอบกับพนักงานที่มีการจ้างงานมากกว่าหนึ่งใน **แบบฟอร์มผู้ปฏิบัติงาน > การตรวจสอบ**

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>คุณลักษณะการแสดงตัวอย่างของการลงทะเบียนแบบเปิดของผลประโยชน์ถูกลบออกแล้ว

ในการเข้าร่วมกับการประกาศของเราในประกาศบล็อก [การลงทุนเชิงกลยุทธ์ในความยอดเยี่ยมในการดำเนินงานของไดรฟ์ Core HR](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) Microsoft ได้ลบคุณลักษณะการลงทะเบียนแบบเปิดของผลประโยชน์ออกจากการแสดงตัวอย่างสาธารณะ ฟังก์ชันใหม่จะถูกนำออกใช้ในอนาคตแทน การใช้งานการผลิตของลักษณะการทำงานที่เปิดรับผลประโยชน์ไม่ได้รับการสนับสนุน

## <a name="coming-soon"></a>เร็วๆ นี้

### <a name="print-performance-reviews"></a>พิมพ์การตรวจทานประสิทธิภาพ

ให้ดูที่ [พิมพ์การตรวจทานประสิทธิภาพ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) ใน Dynamics 365: 2019 แผนเวฟการออกใช้ 2

### <a name="feature-management-workspace"></a>พื้นที่ทำงานการจัดการคุณลักษณะ

จะมีการเพิ่มเติมและปรับปรุงคุณลักษณะทุกครั้งที่นำไปใช้ ประสบการณ์การจัดการคุณลักษณะให้พื้นที่ทำงานที่คุณสามารถดูรายการของคุณลักษณะที่ได้ถูกจัดส่งในการนำออกใช้แต่ละครั้ง ตามค่าเริ่มต้น คุณลักษณะใหม่จะถูกปิด คุณสามารถใช้พื้นที่ทำงานเพื่อเปิดและดูเอกสารประกอบได้

เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการเปลี่ยนแปลงที่มากับการจัดการคุณลักษณะ โปรดดู [ภาพรวมของการจัดการคุณลักษณะ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)
