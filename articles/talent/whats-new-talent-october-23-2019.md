---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (23 ตุลาคม 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
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
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 66419d9093cff68aa6109b22ab57bcb46ac6c718
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772907"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (23 ตุลาคม 2019)

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract
รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม
รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR

การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2569 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

### <a name="platform-update-30-for-finance-and-operations-apps"></a>การอัพเดตแพลตฟอร์ม 30 สำหรับแอป Finance and Operations

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรในการอัพเดตแพลตฟอร์ม 30 สำหรับแอป Finance and Operations (พฤศจิกายน 2019)](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30)

### <a name="remove-benefits-open-enrollment-preview-feature"></a>ลบคุณลักษณะการแสดงตัวอย่างของการลงทะเบียนแบบเปิดของผลประโยชน์

ในการเข้าร่วมกับการประกาศของเราในประกาศบล็อก [การลงทุนเชิงกลยุทธ์ในความยอดเยี่ยมในการดำเนินงานของไดรฟ์ Core HR](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) Microsoft จะลบคุณลักษณะการลงทะเบียนแบบเปิดของผลประโยชน์ออกจากการแสดงตัวอย่างสาธารณะในวันที่ 18 ตุลาคม 2019 แต่ฟังก์ชันใหม่จะถูกนำออกใช้ในอนาคตแทน การใช้งานการผลิตของคุณลักษณะการลงทะเบียนแบบเปิดของผลประโยชน์ที่ขณะนี้อยู่ในการแสดงตัวอย่างจะไม่ได้รับการสนับสนุน

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>เกิดข้อผิดพลาดขณะเลือกประเทศ/ภูมิภาคบนแบบฟอร์มผู้ปฏิบัติงานครั้งที่สอง (350294)

ด้วยการนำออกใช้ของสัปดาห์นี้ ปัญหานี้ได้รับการแก้ไขแล้วเมื่อเลือกประเทศ/ภูมิภาคบนฟอร์ม **ผู้ปฏิบัติงาน**

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>ค่ามิติทางการเงินเริ่มต้นสำหรับฟิลด์การแสดงชุดข้อมูล เมื่อไม่อนุญาตให้มีการป้อนข้อมูลด้วยตนเองถูกตั้งค่าเป็นจริง (340097)

ด้วยการเปลี่ยนแปลงนี้ เมื่อตั้งค่ามิติทางการเงินและใช้ตัวเลือกเพื่อไม่ให้มีการป้อนข้อมูลด้วยตนเอง ระบบจะกำหนดค่ามิติเริ่มต้นอย่างถูกต้องลงในฟิลด์ **การแสดงชุดข้อมูล**

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>ชนิดของความสัมพันธ์ใหม่ควรถูกเพิ่มเข้าในการค้นหาความสัมพันธ์ในฟอร์มผู้ติดต่อส่วนบุคคล (347691)

การนำออกใช้นี้มีความสามารถใหม่ในการเพิ่มชนิดความสัมพันธ์ใหม่ในตาราง **ชนิดความสัมพันธ์** และสะท้อนถึงการเปลี่ยนแปลงเหล่านั้นในการค้นหาความสัมพันธ์สำหรับผู้ติดต่อส่วนบุคคล

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>ค่ารายการเพิ่มเติมในฟิลด์ที่กำหนดเองไม่มีผลใน Common Data Service (379599)

ด้วยการนำออกใช้ของสัปดาห์นี้ การเพิ่มค่ารายการใหม่ไปยังฟิลด์แบบกำหนดเองที่มีอยู่ซึ่งมีการซิงโครไนส์กับ Common Data Service ขณะนี้ค่าของรายการเบิกสินค้าใหม่จะปรากฏขึ้นหลังจากนำการเปลี่ยนแปลงไปใช้กับเอนทิตี

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>ในหน้าเงื่อนไขการจ้างงาน เงื่อนไขการจ้างงานทั้งหมดของพนักงานจะปรากฏขึ้นหลังจากเลือกเปิดใน Excel (348073)

ด้วยการนำออกใช้นี้ เฉพาะเงื่อนไขการจ้างงานของพนักงานที่เลือกเท่านั้นที่จะเปิดใน Excel การรักษาความปลอดภัยของบริษัททั้งหมดถูกชำระเงินด้วยเช่นกัน

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>ความสัมพันธ์ระหว่างเอนทิตีวันหยุดในปฏิทินงานและเอนทิตีปฏิทินงานขาดหายไปใน Common Data Service (324178)

มีการเพิ่มความสัมพันธ์นี้ด้วยการนำออกใช้ การเปลี่ยนแปลงนี้จะเปิดใช้งานวันทำงานของพนักงานที่จะแสดงใน PowerApps 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>เกิดข้อผิดพลาดเมื่อใช้ลำดับงานแบบบริการตนเองของพนักงานกับลำดับชั้นที่ตั้งค่าคอนฟิกได้ (370132)

ในการนำออกใช้นี้ การส่งข้อความที่ดีขึ้นจะมีอยู่ในวิธีการตั้งค่าคอนฟิกลำดับงานโดยใช้ลำดับชั้นที่ตั้งค่าคอนฟิกได้ 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>ระบบอนุญาตให้มีการสร้างตำแหน่งงานใหม่ที่ซึ่งวันที่พร้อมใช้งานสำหรับการกำหนดอยู่ก่อนหน้าวันที่เรียกใช้ (340103)

การเปลี่ยนแปลงนี้จะแสดงคำเตือน เมื่อวันที่ **พร้อมใช้งานสำหรับการกำหนด** อยู่ก่อนวันที่ **เรียกใช้งาน** ของตำแหน่งงาน

## <a name="coming-soon"></a>เร็วๆ นี้

### <a name="print-performance-reviews"></a>พิมพ์การตรวจทานประสิทธิภาพ

ให้ดูที่ [พิมพ์การตรวจทานประสิทธิภาพ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) ใน Dynamics 365: 2019 แผนเวฟการออกใช้ 2

### <a name="feature-management-workspace"></a>พื้นที่ทำงานการจัดการคุณลักษณะ

จะมีการเพิ่มเติมและปรับปรุงคุณลักษณะทุกครั้งที่นำไปใช้ ประสบการณ์การจัดการคุณลักษณะให้พื้นที่ทำงานที่คุณสามารถดูรายการของคุณลักษณะที่ได้ถูกจัดส่งในการนำออกใช้แต่ละครั้ง ตามค่าเริ่มต้น คุณลักษณะใหม่จะถูกปิด คุณสามารถใช้พื้นที่ทำงานเพื่อเปิดและดูเอกสารประกอบได้

เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการเปลี่ยนแปลงที่มากับการจัดการคุณลักษณะ โปรดดู [ภาพรวมของการจัดการคุณลักษณะ](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)
