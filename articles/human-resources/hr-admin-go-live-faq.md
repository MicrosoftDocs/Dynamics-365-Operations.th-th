---
title: FAQ เกี่ยวกับการเริ่มใช้งานจริง
description: หัวข้อนี้จะแสดงรายการคำถามที่ถามบ่อยเกี่ยวกับการเริ่มใช้งานจริงกับโครงการการใช้งาน Dynamics 365 Human Resources
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5041d515b261bb3e4b14885e0ec0ce788edf729
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114427"
---
# <a name="go-live-faq"></a>FAQ เกี่ยวกับการเริ่มใช้งานจริง 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้จะแสดงรายการคำถามที่ถามบ่อยเกี่ยวกับการเริ่มใช้งานจริงกับโครงการการใช้งาน Dynamics 365 Human Resources 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>ฉันสามารถตั้งค่าคอนฟิกและร้องขอสภาพแวดล้อมการผลิตของฉันได้เมื่อใด 

โดยทั่วไป สภาพแวดล้อมการผลิตมีการจัดวางหลังจากมีคุณสมบัติตรงตามเงื่อนไขต่อไปนี้:

- การกำหนดทั้งหมดเป็นรหัสที่สมบูรณ์
- การทดสอบการยอมรับของผู้ใช้ (UAT) เสร็จสมบูรณ์แล้ว
- ลูกค้าได้ลงชื่อออกจากโซลูชันแล้ว
- ไม่มีปัญหาการบล็อคสำหรับการเริ่มใช้งานจริง 

เมื่อลูกค้าที่มีคุณสมบัติตรงตามระยะนี้ ทีม Microsoft FastTrack จะทำงานร่วมกับทีมโครงการเพื่อให้การประเมินผลการเริ่มใช้งานจริง 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>ข้อกำหนดเบื้องต้นในการปรับใช้สภาพแวดล้อมการผลิตมีอะไรบ้าง 

สำหรับรายการของข้อกำหนดเบื้องต้น ให้ดูที่  [เตรียมพร้อมสำหรับการใช้งานจริง](hr-admin-go-live-prepare.md) 

## <a name="what-is-a-go-live-assessment"></a>การประเมินการเริ่มใช้งานจริงคืออะไร  

การประเมินการเริ่มใช้งานจริงเป็นส่วนหนึ่งของ  [โปรแกรม Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview) ในระหว่างการรีวิวนี้ สถาปนิกโซลูชันประเมินว่าโครงการที่ใช้งานพร้อมสำหรับการตัดและการเริ่มใช้งานจริงที่ประสบความสำเร็จหรือไม่ การรีวิวนี้บังคับสำหรับโครงการที่ใช้งานอยู่ทั้งหมดก่อนที่คุณจะสามารถร้องขอให้ดำเนินการเริ่มใช้งานจริงต่อไปในสภาพแวดล้อมการผลิตได้ 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>สภาพแวดล้อม Sandbox ของเราจะถูกจัดวางในศูนย์ข้อมูลที่ของสหรัฐอเมริกากลาง เราต้องการให้สภาพแวดล้อมการผลิตของเราถูกปรับใช้ในศูนย์ข้อมูลของสหรัฐตะวันตก ฉันสามารถเลือกสหรัฐอเมริกาตะวันออกเป็นศูนย์ข้อมูลในการตั้งค่าคอนฟิกการผลิตของฉันได้หรือไม่ 

LCS ไม่จำกัดคุณจากการเลือกศูนย์ข้อมูลอื่นเมื่อคุณปรับใช้สภาพแวดล้อมของทรัพยากรบุคคลแต่เราขอแนะนำว่าไม่ควรเลือกศูนย์ข้อมูลอื่น  

ถ้าคุณต้องการให้สภาพแวดล้อมการผลิตของคุณเป็นศูนย์ข้อมูลของสหรัฐตะวันตก คุณควรจัดวางสภาพแวดล้อม Sandbox ของคุณใหม่ให้กับศูนย์ข้อมูลของสหรัฐอเมริกาฝั่งตะวันตก แล้วทดสอบ และลงชื่อออก 

สำหรับข้อมูลเกี่ยวกับการเลือกศูนย์ข้อมูลที่ถูกต้อง ให้ดูที่ [ข้อกำหนดของเครือข่าย](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements) 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>ระดับการเข้าถึงใดที่ฉันต้องมีกับทรัพยากร Azure สำหรับสภาพแวดล้อมของทรัพยากรบุคคลของฉัน  

การเข้าถึงสภาพแวดล้อมของฝ่ายทรัพยากรบุคคลถูกจำกัด คุณไม่สามารถเข้าถึงเครื่องเสมือน (VM) หรือ Microsoft Internet Information Services (IIS) นอกจากนี้คุณยังไม่สามารถเข้าถึงฐานข้อมูลผ่าน Microsoft SQL Server Management Studio 

ถึงแม้ว่าคุณจะไม่สามารถเข้าถึงทรัพยากร Azure หรือสภาพแวดล้อม Dynamics 365 Human Resources ของคุณได้โดยตรง มีคุณลักษณะเพิ่มเติมที่คุณสามารถใช้ในการเข้าถึงข้อมูลของคุณ

- คุณสามารถปรับใช้ฐานข้อมูล SQL Azure ในผู้เช่า Azure ของคุณเอง และใช้ลักษณะการทำงานของฐานข้อมูลของคุณเอง (BYOD) เพื่อซิงโครไนส์ข้อมูล สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การใช้ฐานข้อมูลของคุณเอง (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database)

- คุณสามารถใช้การรวม Dataverse กับการซิงโครไนส์เอนทิตีที่เลือกลงในฐานข้อมูล Dataverse สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [Dataverse ตาราง](hr-developer-entities.md) 

## <a name="how-often-is-my-production-database-backed-up"></a>การสำรองฐานข้อมูลการผลิตของฉันบ่อยเพียงใด 

ฐานข้อมูลมีการป้องกันโดยสำเนาสำรองโดยอัตโนมัติที่ความถี่ดังต่อไปนี้:

| ชนิดของการสำรอง | ความถี่ |
| --- | --- |
| สำเนาสำรองฐานข้อมูลแบบเต็ม | รายสัปดาห์ |
| การสำรองฐานข้อมูลส่วนที่แตกต่าง | ทุกๆ 12-24 ชั่วโมง |
| สำเนาสำรองล็อกธุรกรรม | ทุกๆ 5 ถึง10 นาที |

Microsoft ยังคงมีสำเนาสำรองที่เพียงพอสำหรับการอนุญาตให้มีการคืนสภาพเวลา (PITR) ภายใน 14 วันหลังสุด 

สำหรับข้อมูลเพิ่มเติม ดูที่  [เรียนรู้เกี่ยวกับการสำรองข้อมูลฐานข้อมูล SQL อัตโนมัติ](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database) 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>ฉันสามารถร้องขอสำเนาของการสำรองของฐานข้อมูลการผลิตของฉันได้หรือไม่ 

ลำดับที่ คุณสามารถส่งคำขอการรีเฟรชฐานข้อมูลเพื่อคัดลอกสภาพแวดล้อมการผลิตของคุณไปยังสภาพแวดล้อม Sandbox อย่างไรก็ตาม คุณสามารถปรับใช้ฐานข้อมูล SQL Azure ในผู้เช่า Azure ของคุณเอง และใช้ลักษณะการทำงาน BYOD เพื่อซิงโครไนส์ข้อมูลจากสภาพแวดล้อมการผลิตของคุณ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การใช้ฐานข้อมูลของคุณเอง (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database) 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>ฉันจะย้ายสภาพแวดล้อม Sandbox ของฉันไปยังการผลิตสำหรับการเริ่มใช้งานจริงได้อย่างไร 

เนื่องจากมีลักษณะการทำงานที่ไม่พร้อมใช้งานเมื่อต้องการย้ายสภาพแวดล้อมของคุณจาก Sandbox ไปยังสภาพแวดล้อมการผลิต คุณต้องใช้แพคเกจข้อมูลเพื่อย้ายข้อมูลไปยังสภาพแวดล้อมการผลิตของคุณ  

เราขอแนะนำให้คุณเลือกรายการเอนทิตีที่มีการตั้งค่าคอนฟิกไว้ใน Sandbox ของคุณทั่วทั้งโครงการ หลังจากนั้นทดสอบกระบวนการตัดและการย้ายแพคเกจข้อมูลใดๆ ที่จำเป็นสำหรับการเริ่มใช้งานจริง คุณต้องย้ายแพคเกจข้อมูลใดๆ เข้าไปในสภาพแวดล้อมการผลิตด้วยตนเองเมื่อคุณพร้อมที่จะไปใช้งานจริง 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>ฉันควรทำอย่างไรถ้าสภาพแวดล้อมการผลิตของฉันหยุดทำงาน 

เมื่อต้องการรายงานการหยุดทำงานการผลิต ให้ทำตามขั้นตอนที่อธิบายไว้ใน  [รายงานการหยุดทำงานของการผลิต](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage) 

 ## <a name="see-also"></a>ดูเพิ่มเติมที่

 [จัดเตรียมสำหรับการเริ่มใช้งานจริง](hr-admin-go-live-prepare.md)
