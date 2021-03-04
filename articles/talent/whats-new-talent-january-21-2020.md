---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (21 มกราคม 2020)
description: บทความนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
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
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528134"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (21 มกราคม 2020)

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract เราได้เพิ่มฟังก์ชันไปยัง Attract เพื่อสนับสนุนประกาศล่าสุดของเรา [การสร้างบุคลากรที่ประสบความสำเร็จมากขึ้นด้วย Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/)

### <a name="download-environment-data"></a>ดาวน์โหลดข้อมูลสภาพแวดล้อม

ผู้ดูแลระบบสามารถดาวน์โหลดข้อมูลของสภาพแวดล้อมของตนเองได้ มีการส่งออกข้อมูลในรูปแบบ JSON มาตรฐานที่มีงาน ผู้สมัคร และการตั้งค่าคอนฟิกทั้งหมดที่ส่งออกในไฟล์ซิป สำหรับข้อมูลเพิ่มเติม ดู [ส่งออกข้อมูลจาก Attract และ Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data)

### <a name="restricting-access-to-environments-for-non-admin-users"></a>การจำกัดการเข้าถึงสภาพแวดล้อมสำหรับผู้ใช้ที่ไม่ใช่ผู้ดูแลระบบ

ขณะนี้ผู้ดูแลระบบสามารถจำกัดการเข้าถึงสภาพแวดล้อมสำหรับผู้ใช้ที่ไม่ใช่ผู้ดูแลระบบ การดำเนินการนี้ไม่สามารถยกเลิกได้ สำหรับข้อมูลเพิ่มเติม โปรดดู [จำกัดการเข้าถึง Attract](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract)

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard

### <a name="exporting-onboarding-guides"></a>การส่งออก Guides การเตรียมความพร้อม

ขณะนี้ผู้ใช้สามารถส่งออก Guides การเตรียมความพร้อมและเท็มเพลตการเตรียมความพร้อมทั้งหมดของพวกเขาได้ในรูปแบบเอกสาร Word สำหรับข้อมูลเพิ่มเติม ดู [ส่งออกข้อมูลจาก Attract และ Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data)

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR

การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2726 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>ฟิลด์ค่าตอบแทนรายปีล่าสุดในฟอร์มตรวจสอบการจ้างงานไม่สอดคล้องกัน (392092)

การนำออกใช้นี้มีการเปลี่ยนแปลงที่จะแสดงสกุลเงินล่าสุดอย่างสม่ำเสมอ โดยใช้ตัวเลือกบริษัทบนฟอร์ม **ตรวจสอบการจ้างงาน**

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>เรียกว่า ฟิลด์ที่เพิ่มลงในการค้นหาผู้รับผลป้อนกลับ (407789)

เมื่อให้ผลป้อนกลับเกี่ยวกับประสิทธิภาพ การค้นหาสำหรับผู้ปฏิบัติงานจึงไม่มีข้อมูลเพียงพอที่จะตรวจสอบว่าผลป้อนกลับไปยังบุคคลที่ถูกต้องหรือไม่ เราได้เพิ่มคอลัมน์ **เรียกว่า** เพื่อช่วยระบุชื่อเฉพาะของพนักงาน
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>มีการสร้างเรกคอร์ด HcmWorkerPayrollInfo โดยไม่มีการเชื่อมโยงกับผู้ปฏิบัติงาน (394526)

การนำออกใช้นี้รวมถึงการเปลี่ยนแปลงเป็น ไม่เขียนเรกคอดร์ด HCMWorkerPayrollInfo โดยไม่มีการอ้างอิงถึงพนักงาน

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>สามารถแก้ไขแผนกได้ เมื่อนำทางจากลำดับชั้นของตำแหน่ง (341001)

เมื่อมีการตั้งค่าการรักษาความปลอดภัยเพื่อปฏิเสธการเข้าถึงการแก้ไขแผนก การแก้ไขจะถูกปิดใช้งาน เมื่อนำทางไปยังฟอร์ม **แผนก** ในสถานการณ์จำลองทั้งหมด

## <a name="coming-soon"></a>เร็วๆ นี้

โซลูชัน Common Data Service ใหม่จะพร้อมใช้งานเร็วๆ นี้ โดยมีการเปลี่ยนแปลงต่อไปนี้:

| คำอธิบาย | เปลี่ยน |
| --- | --- |
| เอนทิตี **งาน/ตำแหน่ง** เปลี่ยนแปลง | <ul><li>**ภูมิภาคของค่าตอบแทน** ที่เพิ่ม</li><li>**มิติทางการเงิน** ที่เพิ่ม</li></ul> |
| เอนทิตี **ผู้ปฏิบัติงาน** เปลี่ยนแปลง | <ul><li>**ลำดับชื่อ** ที่เพิ่ม</li><li>เพิ่ม **การทำงานจากที่บ้าน** แล้ว</li><li>**ภาษา** ที่เพิ่ม</li><li>**วันที่ของอายุงาน** ที่เพิ่ม</li><li>**วันที่ครบรอบปี** ที่เพิ่ม</li><li>เพิ่ม **วันที่จ้างงานเดิม** แล้ว</li></ul> |
| เอนทิตี **การจ้างงาน** เปลี่ยนแปลง | <ul><li>**มิติทางการเงิน** ที่เพิ่ม</li><li>**เหตุผลการสิ้นสุดการจ้างงาน** ที่เพิ่ม</li><li>**วันที่สิ้นสุดการจ้างงาน** เปลี่ยนชื่อจาก **วันที่เปลี่ยนแปลง**</li><li>**วันที่ทดลองงาน** ที่เพิ่ม</li></ul> |
| เอนทิตี **ที่อยู่ผู้ปฏิบัติงาน** เปลี่ยนแปลง | <ul><li>**ที่อยู่ถนน** ที่เพิ่ม</li><li>**บรรทัดที่อยู่ 1** **บรรทัดที่อยู่ 2** และ **บรรทัดที่อยู่ 3** ที่ทำเครื่องหมายสำหรับค่าเสื่อมราคา</li></ul> |
| เอนทิตีการตั้งค่าค่าตอบแทนผันแปรใหม่ | <ul><li>**ชนิดแผนตัวแปรค่าตอบแทน**</li><li>**แผนค่าตอบแทนผันแปร**</li><li>**กฎสิทธิพึงได้**</li><li>**ระดับแผนตัวแปรค่าตอบแทน**</li></ul> |
| เอนทตี **การจ้างงานในปฏิทินของผู้ปฏิบัติงาน** ใหม่ | <ul><li>เพิ่ม **เอนทิตีปฏิทินงาน** แล้ว</li></ul> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]