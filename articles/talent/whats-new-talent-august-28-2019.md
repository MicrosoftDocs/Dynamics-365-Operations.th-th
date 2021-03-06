---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 for Talent (27 สิงหาคม 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 for Talent
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8965636e539345be5ef0ad591f7017938efd322d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529815"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 for Talent (27 สิงหาคม 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 for Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR

การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2447 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>มีการเปิดใช้งานคุณลักษณะการแสดงตัวอย่างเฉพาะในอินสแตนซ์ sandbox

เมื่อคุณจัดเตรียมอินสแตนซ์ใหม่ของ Talent คุณสามารถระบุได้ว่าชนิดของอินสแตนซ์เป็น การผลิต หรือ Sandbox ชนิดของอินสแตนซ์ Sandbox อนุญาตให้มีการทดสอบของคุณลักษณะใหม่ก่อนเวลา อินสแตนซ์ Talent ที่มีอยู่ทั้งหมดจะได้รับการปรับปรุงเป็นชนิดอินสแตนซ์ การผลิต ถ้าคุณต้องการให้หนึ่งในอินสแตนซ์ที่มีอยู่ของคุณได้รับการปรับปรุงเป็นชนิดของอินสแตนซ์ Sandbox ติดต่อ ฝ่ายสนับสนุน เพื่อเริ่มต้นการร้องขอการเปลี่ยนแปลง

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเผยแพร่การเปลี่ยนแปลง โปรดดู [เตรียมใช้งาน Talent](./provisioning-talent.md)

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>ดูข้อมูลที่ขยายสำหรับประสิทธิภาพในการบริการตนเองของผู้จัดการ

ตัวเลือกใหม่จะช่วยให้ผู้จัดการสามารถดูประสิทธิภาพของทั้งรายงานโดยตรงและรายงานที่ขยายของตนได้ ในปัจจุบัน ผู้จัดการรายการสามารถกำหนดและปรับปรุงเป้าหมายผลการปฏิบัติงานและออกการตรวจทานใหม่ นอกจากนี้ ผู้จัดการโดยตรงและพนักงานสามารถรักษาและปรับปรุงสมุดรายวันประสิทธิภาพ เพื่อให้มั่นใจว่ากระบวนการตรวจทานประสิทธิภาพจะทำงานได้อย่างราบรื่น เมื่อมีการใช้การเปลี่ยนแปลงนี้ ผู้จัดการจะสามารถดูและรักษาข้อมูลที่เกี่ยวข้องกับประสิทธิภาพสำหรับรายงานแบบขยายของพวกเขา นอกเหนือจากรายงานโดยตรงของพวกเขา

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>การลบนิติบุคคลไม่ได้รับอนุญาตถ้ามีพนักงานอยู่ภายในบริษัท (339849)

ด้วยการเปลี่ยนแปลงนี้ คุณไม่สามารถลบบริษัทได้ ถ้ามีพนักงานและข้อมูลที่เกี่ยวข้องอื่นๆอยู่สำหรับนิติบุคคล

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>การวิเคราะห์ข่าวกรองธุรกิจการจัดการค่าตอบแทนไม่ตรงกับพื้นที่ทำงานค่าตอบแทน (322493)

ในรุ่นนี้ การวิเคราะห์ค่าตอบแทนได้รับการการปรับปรุงเพื่อให้สะท้อนถึงแผนที่กำหนดให้กับพนักงานอย่างถูกต้อง

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>ตัวยึดลำดับงาน %บริษัท% จะแสดง DAT เมื่อมีการจ้างงานพนักงานโดยใช้ลำดับงาน (343905)

ในรุ่นนี้ ตัวยึดของบริษัทจะแสดงนิติบุคคลที่สัมพันธ์กับการจ้างงานของพนักงานใหม่

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>เอนทิตี้ CDSJobPosition แสดงข้อผิดพลาดเมื่อมีการตั้งค่าวันที่สิ้นสุดการมีผลบังคับใช้ (349387)

ในรุ่นนี้ **รายละเอียดตำแหน่ง** และแหล่งข้อมูล **ช่วงเวลาของตำแหน่ง** บนเอนทิตี้ **CDSJobPosition** อนุญาตให้มีการแก้ไขจาก Common Data Service ไปที่ฟิลด์ **วันที่มีผลบังคับใช้** 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>สำหรับการเลิกจ้างพนักงาน วันสุดท้ายที่ทำงานจะมีการเติมบนวันที่สิ้นสุดการมอบหมาย (332496)

การเปลี่ยนแปลงนี้ในขณะนี้จะเริ่มต้น **วันที่สิ้นสุดการมอบหมาย** ตำแหน่งไปยัง **วันที่สิ้นสุดการจ้างงาน** คุณสามารถเปลี่ยนค่าเริ่มต้นเหล่านี้ได้ในขณะที่ป้อนข้อมูล

### <a name="legal-entities-arent-limited-with-hire-338871"></a>นิติบุคคลไม่มีข้อจำกัดในการจ้างงาน (338871)
 
การเปลี่ยนแปลงนี้จำกัดกระบวนการจ้างงานเพื่อแสดงเฉพาะนิติบุคคลเหล่านั้นที่ผู้ใช้มีสิทธิ์เข้าถึงเท่านั้น  

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

### <a name="streamlined-employee-entry-and-navigation"></a>การป้อนข้อมูลและการนำทางของพนักงานที่มีประสิทธิภาพ

ขณะนี้ฟังก์ชันนี้พร้อมใช้งานในสภาพแวดล้อมการทดลองและ Sandbox เมื่อต้องการเปิดใช้งานคุณลักษณะนี้ นำทางไปที่ **การจัดการระบบ > ลิงค์ > การตั้งค่า > พารามิเตอร์ระบบ > คุณลักษณะการแสดงตัวอย่าง** เลือก **ฟอร์มผู้ปฏิบัติงานที่มีการปรับปรุงและการนำทาง** การทำเช่นนี้เปิดใช้งานการเปลี่ยนแปลงเหล่านี้สำหรับผู้ใช้ทั้งหมด คุณสามารถปิดตัวเลือกนี้ได้ตลอดเวลา

สำหรับข้อมูลเพิ่มเติม ให้ดู [การป้อนข้อมูลและการนำทางของพนักงานที่มีประสิทธิภาพ](./streamlined-employee-entry.md)

## <a name="coming-soon"></a>เร็วๆ นี้

### <a name="platform-update-29"></a>แพลตฟอร์ม update 29

สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับการปรับปรุงแพลตฟอร์ม 29 ดูที่ [คุณลักษณะการแสดงตัวอย่างในการปรับปรุงแพลตฟอร์ม Dynamics 365 for Finance and Operations 29 (ตุลาคม 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29)


[!INCLUDE[footer-include](../includes/footer-banner.md)]