---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 for Talent (17 กันยายน 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 for Talent
author: Darinkramer
manager: AnnBe
ms.date: 9/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 97e55919309e3e95d21b4fdb14f913cf511280eb
ms.sourcegitcommit: f853c8d46ffc8e578387bac4cd48a948916983ef
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/19/2019
ms.locfileid: "2002584"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-17-2019"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 for Talent (17 กันยายน 2019)

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 for Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract
รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม
รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR
การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2492 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>คุณสามารถเปิดใช้งานคุณลักษณะตัวอย่างในสภาพแวดล้อมของ Sandbox และ Trail

เมื่อคุณจัดเตรียมอินสแตนซ์ใหม่ของ Talent คุณสามารถระบุได้ว่าชนิดของอินสแตนซ์เป็น การผลิต หรือ Sandbox อินสแตนซ์ของชนิด Sandbox อนุญาตให้มีการทดสอบของคุณลักษณะใหม่ได้ล่วงหน้า ถ้าคุณต้องการให้หนึ่งในอินสแตนซ์ที่มีอยู่ของคุณได้รับการปรับปรุงเป็นชนิดของอินสแตนซ์ Sandbox ติดต่อ ฝ่ายสนับสนุน เพื่อเริ่มต้นการร้องขอการเปลี่ยนแปลง

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเผยแพร่การเปลี่ยนแปลง โปรดดู [เตรียมใช้งาน Talent](./provisioning-talent.md)

### <a name="human-resources-staff-cant-see-performance-review-details-once-assigned-to-them-by-workflow-370308"></a>เจ้าหน้าที่ฝ่ายทรัพยากรบุคคลไม่สามารถดูรายละเอียดการตรวจทานประสิทธิภาพได้เมื่อมอบหมายลำดับงานให้กับพวกเขา (370308)

ด้วยการอัพเดตของสัปดาห์นี้ ผู้เชี่ยวชาญด้าน HR จะสามารถดูรายละเอียดการตรวจทานประสิทธิภาพที่มอบหมายให้กับพวกเขาโดยใช้การประมวลผลลำดับงาน เมื่อต้องการดูรีวิว ให้ไปยัง **การบริการตัวเองของพนักงาน > รายการงานที่มอบหมายให้ฉัน**

### <a name="job-family-field-missing-in-the-manage-changes-page-for-job-details-346031"></a>ฟิลด์ครอบครัวงานที่ขาดหายไปในหน้าจัดการการเปลี่ยนแปลงสำหรับรายละเอียดงาน (346031)

ในรุ่นนี้ ฟิลด์ครอบครัวงานได้ถูกเพิ่มเข้าไปในหน้า **จัดการการเปลี่ยนแปลง** สำหรับรายละเอียดงานแล้ว

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

### <a name="streamlined-employee-entry-and-navigation"></a>การป้อนข้อมูลและการนำทางของพนักงานที่มีประสิทธิภาพ

ขณะนี้ฟังก์ชันนี้พร้อมใช้งานในสภาพแวดล้อม sandbox เมื่อต้องการเปิดใช้งานคุณลักษณะนี้ นำทางไปที่ **การจัดการระบบ > ลิงค์ > การตั้งค่า > พารามิเตอร์ระบบ > คุณลักษณะการแสดงตัวอย่าง** เลือก **ฟอร์มผู้ปฏิบัติงานที่มีการปรับปรุงและการนำทาง** การทำเช่นนี้จะเปิดใช้งานการเปลี่ยนแปลงเหล่านี้สำหรับผู้ใช้ทั้งหมด คุณสามารถปิดตัวเลือกนี้ได้ตลอดเวลา

สำหรับข้อมูลเพิ่มเติม ให้ดู [การป้อนข้อมูลและการนำทางของพนักงานที่มีประสิทธิภาพ](./streamlined-employee-entry.md) เพื่อดูการเปลี่ยนแปลง ให้ดูวิดีโอที่ [Dynamics 365 for Talent 2019 ปล่อยภาพรวมของเวฟ 2](https://aka.ms/ROGT19RW2ROV)
