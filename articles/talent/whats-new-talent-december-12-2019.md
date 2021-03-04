---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (10 ธันวาคม 2019)
description: บทความนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
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
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528182"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (10 ธันวาคม 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR

การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2660 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

### <a name="feature-management-workspace"></a>พื้นที่ทำงานการจัดการคุณลักษณะ

พื้นที่ **การจัดการลักษณะการทำงาน** แสดงรายการของลักษณะการทำงานที่จัดส่งในแต่ละรุ่น ตามค่าเริ่มต้น คุณลักษณะใหม่จะถูกปิด คุณสามารถใช้พื้นที่ทำงานเพื่อเปิดและดูเอกสารประกอบได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการคุณลักษณะ ดูที่ [ภาพรวมของการจัดการคุณลักษณะ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)

ลักษณะการทำงานใหม่ทั้งหมดยังคงอยู่ในการแสดงตัวอย่างอย่างน้อย 30 วัน และโดยปกติจะคงอยู่ 30-60 วัน ลักษณะการทำงานที่สำคัญโดยทั่วไปจะมีอยู่ในเดือนตุลาคมและเดือนเมษายนของแต่ละปีตามรอบระยะเวลาการแสดงตัวอย่าง ทันทีที่คุณเห็นความสามารถใหม่ในพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** คุณสามารถเปิดใช้งานได้ ลักษณะการทำงานบางอย่างอาจเปิดใช้งานตามค่าเริ่มต้น
 
เมื่อเวลาผ่านไป ลักษณะการทำงานที่สำคัญจะเปิดใช้งานโดยค่าเริ่มต้นและไม่สามารถปิดได้ (ตัวอย่างเช่น พื้นที่ทำงาน **การจัดการลักษณะการทำงาน**)
 
เมื่อมีลักษณะการทำงานที่พร้อมใช้งาน โดยทั่วไปจะสามารถเปิดหรือปิดใช้งานได้ในสภาพแวดล้อมการผลิต พื้นที่ทำงาน **การจัดการลักษณะการทำงาน** บ่งชี้ว่าลักษณะการทำงานในการแสดงตัวอย่างจะกลายเป็นข้อบังคับ โดยปกติแล้ววันที่นี้จะเป็นวันที่ 1 ตุลาคม หรือ 1 เมษายน เพื่อให้สอดคล้องกับแผนการวางจำหน่ายรายย่อย คุณไม่สามารถเปิดหรือปิดคุณลักษณะบังคับได้ คุณไม่สามารถเปิดและปิดลักษณะการทำงานในสภาพแวดล้อมทั้งหมดได้จนกว่าจะเป็นข้อบังคับ

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>ฟอร์มผู้ปฏิบัติงานที่มีประสิทธิภาพได้ย้ายไปยังพื้นที่ทำงานการจัดการคุณลักษณะ (390583)

ด้วยการเปลี่ยนแปลงนี้ ขณะนี้คุณสามารถเปิดใช้งานฟอร์มผู้ปฏิบัติงานที่มีประสิทธิภาพในพื้นที่ทำงาน **การจัดการคุณลักษณะ** คุณลักษณะนี้ได้ถูกย้ายจากฟอร์ม **พารามิเตอร์ระบบ** ใน **การจัดการระบบ**

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>ป้องกันไม่ให้มีการเขียนเรกคอร์ด HcmWorkerPayrollInfo โดยที่ไม่มีค่าผู้ปฏิบัติงาน (394526)

ด้วยรุ่นนี้ เรกคอร์ด **HcmWorkerPayrollInfo** จะไม่ถูกสร้างขึ้นภายใต้อีกต่อไปโดยไม่มีการอ้างอิงผู้ปฏิบัติงานในสถานการณ์นี้ 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>ล็อกข้อความที่เกี่ยวข้องกับการดำเนินการไม่ได้ถูกเติมข้อมูล เมื่อการดำเนินการไม่เสร็จสมบูรณ์ (374007)

รุ่นนี้มีการเปลี่ยนแปลงเพื่อเติมข้อมูลล็อกข้อความเกี่ยวกับการดำเนินการ เมื่อการดำเนินการล้มเหลวในบางสถานการณ์ 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>การสร้างชุดงานการรวม Common Data Service (388030)

ด้วยการเปลี่ยนแปลงนี้ ชุดงานสำหรับการรวม Common Data Service จะถูกสร้างขึ้น เมื่อเปิดใช้งานบริการ

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>ค่ารายการการเบิกสินค้าเพิ่มเติมไปยังฟิลด์ที่กำหนดเองจะไม่มีผลใน Common Data Service หลังจากที่คลิกใช้บนฟอร์มฟิลด์ที่กำหนดเอง (379599)

ด้วยการเปลี่ยนแปลงนี้ ขณะนี้ค่ารายการการเบิกสินค้าใหม่ใน Talent ถูกซิงโครไนส์ไปยัง Common Data Service เมื่อคุณใช้การเปลี่ยนแปลงของคุณ

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>การปรับปรุงไปยัง Common Data Service สำหรับเอนทิตีธุรกรรมการออกจากธนาคารจะกลายเป็นการแทรกบนด้าน Talent (352938)

การเปลี่ยนแปลงนี้แก้ไขปัญหาที่ซึ่งการปรับปรุงไปยังธุรกรรมธนาคารที่ปล่อยจะสร้างเรกคอร์ดใหม่ใน Talent

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

คุณลักษณะการแสดงตัวอย่างจะพร้อมใช้งานเฉพาะในสภาพแวดล้อม **Sandbox** เท่านั้น

### <a name="print-performance-reviews"></a>พิมพ์การตรวจทานประสิทธิภาพ

ให้ดูที่ [พิมพ์การตรวจทานประสิทธิภาพ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) ใน Dynamics 365: 2019 แผนเวฟการออกใช้ 2



[!INCLUDE[footer-include](../includes/footer-banner.md)]