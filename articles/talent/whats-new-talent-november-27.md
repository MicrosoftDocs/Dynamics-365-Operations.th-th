---
title: มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (27 พฤศจิกายน 2018)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
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
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6bd049bfe4639136276ab2f14e6310e45d1254f2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306377"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a>มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (27 พฤศจิกายน 2018)

[!include [banner](includes/banner.md)]

**สร้าง 8.1.2064**

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR


## <a name="changes"></a>การเปลี่ยนแปลง

### <a name="unable-to-create-a-note-in-case-management"></a>ไม่สามารถสร้างบันทึกย่อในการจัดการกรณีได้

มีการทำการเปลี่ยนแปลงสำหรับปัญหา ขณะพยายามแก้ไขหรือสร้างบันทึกย่อในล็อกกรณีของการจัดการกรณี

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>คำที่สะกดผิดบนแท็บการวิเคราะห์ในพื้นที่ทำงานค่าตอบแทน 

มีการทำการเปลี่ยนแปลงเพื่อแก้ไขการสะกดของ 'เชื้อชาติ' ในแผนภูมิการวิเคราะห์ค่าตอบแทนในพื้นที่ทำงานค่าตอบแทน

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>พื้นที่ทำงานแบบบริการตนเองของพนักงานไม่ได้แสดง เมื่อผู้ใช้ไม่ได้ถูกกำหนดให้กับผู้ปฏิบัติงาน 

มีการทำการเปลี่ยนแปลง เมื่อพื้นที่ทำงาน **ระบบบริการตนเองของพนักงาน** ถูกเลือกเป็นเพจเริ่มต้นเมื่อเริ่มต้นสำหรับผู้ใช้ที่ไม่ได้ถูกกำหนดให้กับผู้ปฏิบัติงาน ในสถานการณ์นี้ แดชบอร์ดเริ่มต้นจะแสดงขึ้น

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>ข้อผิดพลาดการลางานและการขาดงาน: การอ้างอิงออบเจ็กต์ไม่ได้ถูกตั้งค่าให้กับอินสแตนซ์ของออบเจ็กต์

มีการทำการเปลี่ยนแปลงไปยังการลางานและการขาดงานเพื่อแก้ไขข้อผิดพลาดนี้ หลังจากการอนุมัติเรกคอร์ดการขาดงานและการลางานในรายการ **รายการงานที่กำหนดให้กับฉัน**

### <a name="unable-to-recall-an-image-workflow"></a>ไม่สามารถเรียกคืนลำดับงานที่มีรูปภาพ

หลังจากเรียกคืนลำดับงานที่มีรูปภาพ ลำดับงานจะถูกกำหนดเป็น "ยกเลิกแล้ว" และสามารถลบคำขอที่มีอยู่ในพื้นที่ทำงานการบริการตนเองของพนักงาน

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>พนักงานหรือผู้รับเหมาที่ถูกจ้างงานใหม่จะแสดงขึ้นหลายครั้ง หลังจากการสิ้นสุดการจ้างงาน 

ด้วยการอัพเดตนี้ พนักงานที่สิ้นสุดการจ้างงานที่ถูกจ้างงานใหม่จะแสดงขึ้นเพียงหนึ่งครั้งในรายการที่ออก 

## <a name="known-issue"></a>ปัญหาที่ทราบ

- **ปัญหา**: เมื่อเพิ่มสิ่งที่แนบมาใหม่กับผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** จะกลายเป็นสีเทา 
- **วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่าก FactBoxes บนหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว ถ้า FactBoxes ถูกปิด เมื่อหน้า **ผู้ปฏิบัติงาน** ถูกโหลด ปุ่มเอกสารแนบจะถูกเปิดใช้งาน (ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)
