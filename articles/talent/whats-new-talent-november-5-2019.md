---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (5 พฤศจิกายน 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 48de07178acfaccf11e0a02b2848bf24e6ccc117
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896784"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (5 พฤศจิกายน 2019)

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR

การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2598 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

### <a name="copy-a-core-hr-instance"></a>การคัดลอกอินสแตนซ์ของ Core HR

ในวันที่นำออกใช้ของสัปดาห์นี้ คุณสามารถใช้ Microsoft Dynamics Lifecycle Services (LCS) เพื่อคัดลอกฐานข้อมูล Microsoft Dynamics 365 Talent: Core HR ไปยังสภาพแวดล้อม Sandbox ถ้าคุณมีสภาพแวดล้อม Sandbox อื่นคุณยังสามารถคัดลอกฐานข้อมูลจากสภาพแวดล้อมดังกล่าวไปยังสภาพแวดล้อม Sandbox ที่กำหนดเป้าหมาย สำหรับข้อมูลเพิ่มเติม ให้ดูที่ 

- [การจัดการสภาพแวดล้อมที่กว้างกว่า](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) ใน Dynamics 365: 2019 จะนำแผนเวฟ 2 ออกใช้

- [การคัดลอกอินสแตนซ์ Core HR](hr-copy-instance.md) ในเอกสาร Talent

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>ชุดงานการรวม Common Data Service ไม่ได้ถูกสร้างขึ้นเมื่อการรวม Common Data Service มีการเปิดใช้งาน (388030)

การเปลี่ยนแปลงนี้จะสร้างชุดงานสำหรับการรวม Common Data Service เมื่อเปิดใช้งาน

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity ไม่ปรับขนาดรูปภาพของบุคคลเมื่ออัพโหลด (369469)

การนำออกใช้ของสัปดาห์นี้เปลี่ยนวิธีการปรับขนาดรูปภาพเพื่อประสิทธิภาพที่ดียิ่งขึ้นเมื่อนำเข้าโดยใช้การจัดการข้อมูล

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>ตำแหน่งที่พร้อมใช้งานสำหรับวันที่กำหนดสามารถเป็นวันก่อนหน้าวันที่เรียกใช้ (340103)

ด้วยการเปลี่ยนแปลงนี้ คำเตือนจะปรากฏขึ้นถ้าคุณเลือก **พร้อมใช้งานสำหรับวันที่กำหนด** ที่อยู่ก่อนหน้าตำแหน่ง **วันที่มีการเรียกใช้**

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>ไม่สามารถสร้างคำขอเปลี่ยนแปลงค่าตอบแทนในบริการตนเองของพนักงานสำหรับแผนตามขั้นตอน (376872)

รุ่นนี้แก้ไขปัญหาเมื่อร้องขอการเปลี่ยนแปลงค่าตอบแทนผ่านทางบริการตนเองของพนักงานสำหรับแผนตามขั้นตอน 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>รหัสเหตุผลไม่มีการซิงค์กับ Common Data Service ถ้าคำอธิบายยาวเกิน 30 อักขระ Core HR อนุญาตให้มีได้แค่ 60 (352682)

เมื่อมีการเปลี่ยนแปลง รหัสเหตุผลที่มีอักขระมากกว่า 30 อักขระจะถูกอัพเดตใน Common Data Service การเปลี่ยนแปลงที่ทำใน Common Data Service จะถูกสะท้อนให้เห็นอีกครั้งใน Talent

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>การรวมที่อยู่จาก Talent ไปยัง Finance and Operations (351961)

รุ่นนี้แก้ไขปัญหาที่ที่อยู่อัพเดตใน Talent ไม่อัพเดตใน Finance and Operations การเปลี่ยนแปลงบล็อกที่อยู่จะอัพเดตในขณะนี้

## <a name="coming-soon"></a>เร็วๆ นี้

### <a name="print-performance-reviews"></a>พิมพ์การตรวจทานประสิทธิภาพ

ให้ดูที่ [พิมพ์การตรวจทานประสิทธิภาพ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) ใน Dynamics 365: 2019 แผนเวฟการออกใช้ 2

### <a name="feature-management-workspace"></a>พื้นที่ทำงานการจัดการคุณลักษณะ

จะมีการเพิ่มเติมและปรับปรุงคุณลักษณะทุกครั้งที่นำไปใช้ ประสบการณ์การจัดการคุณลักษณะให้พื้นที่ทำงานที่คุณสามารถดูรายการของคุณลักษณะที่ได้ถูกจัดส่งในการนำออกใช้แต่ละครั้ง ตามค่าเริ่มต้น คุณลักษณะใหม่จะถูกปิด คุณสามารถใช้พื้นที่ทำงานเพื่อเปิดและดูเอกสารประกอบได้

เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการเปลี่ยนแปลงที่มากับการจัดการคุณลักษณะ โปรดดู [ภาพรวมของการจัดการคุณลักษณะ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)
