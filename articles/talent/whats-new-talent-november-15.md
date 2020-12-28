---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้าง Dynamics 365 Talent - Core HR (15 พฤศจิกายน 2018)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือถูกเปลี่ยนแปลงใน Microsoft Dynamics 365 Talent - Core HR
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a7598db1dc4c11864cf5f5a73d00672ceb66e8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462703"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้าง Dynamics 365 Talent - Core HR (15 พฤศจิกายน 2018)

**สร้าง 8.1.2045**

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR

## <a name="other-changesfixes"></a>การเปลี่ยนแปลง/การแก้ไขอื่นๆ

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>ไม่สามารถเปลี่ยนตำแหน่งปัจจุบันของพนักงานเป็นตำแหน่งที่เปิดในอนาคตได้

มีการเปลี่ยนแปลงเพื่อเปิดใช้งานการโอนย้ายตำแหน่ง เมื่อตำแหน่งพร้อมใช้งานเฉพาะในอนาคต 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>ตำแหน่งไม่แสดง เมื่อสร้างพนักงานใหม่

มีการทำการเปลี่ยนแปลงเพื่อแสดงตำแหน่งที่เปิดทั้งหมดที่พร้อมใช้งานสำหรับการกำหนด เมื่อจ้างพนักงานใหม่ใน Talent ซึ่งรวมถึงตำแหน่งในอดีต หรือถ้าตำแหน่งได้ถูกกำหนดวันที่ในอนาคต ขณะนี้ ตำแหน่งจะปรากฏอย่างถูกต้องตามวันที่เริ่มต้นการจ้างงาน 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>วันที่สิ้นสุดการจ้างงานกำลังแสดงตามการตั้งค่าผู้ใช้

มีการทำการเปลี่ยนแปลงไปยังรายการพนักงานในอดีตไปยังบัญชีสำหรับการออฟเซ็ตโซนเวลาใดๆ สำหรับโซนเวลาที่ต้องการของพนักงาน เมื่อดูวันที่สิ้นสุดการจ้างงาน

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>ลิงค์รายการงานที่กำหนดให้กับฉันไม่แสดงข้อมูลที่ถูกต้อง

ด้วยการเปลี่ยนแปลงนี้ การนำทางไปยังรายละเอียดของรายการงานแต่ละรายการในรายการ จะแสดงข้อมูลที่ถูกต้องสำหรับสินค้าที่เลือก ปัญหานี้เกิดขึ้นกับตัวเลือกความปลอดภัยขั้นสูงเท่านั้น


## <a name="known-issue"></a>ปัญหาที่ทราบ

- **ปัญหา**: เมื่อเพิ่มสิ่งที่แนบมาใหม่กับผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** จะกลายเป็นสีเทา 
- **วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่าก FactBoxes บนหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว ถ้า FactBoxes ถูกปิด เมื่อหน้า **ผู้ปฏิบัติงาน** ถูกโหลด ปุ่มเอกสารแนบจะถูกเปิดใช้งาน (ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)
