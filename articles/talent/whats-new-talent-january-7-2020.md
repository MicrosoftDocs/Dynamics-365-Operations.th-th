---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (7 มกราคม 2020)
description: บทความนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
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
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462716"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (7 มกราคม 2020)

บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR

การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2697 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>ไม่สามารถลบผู้ปฏิบัติงานที่ไม่มีเรกคอร์ดการจ้างงานได้ - (386157)

การเปลี่ยนแปลงนี้จะเพิ่มตัวเลือกการลบในฟอร์ม **ผู้ปฏิบัติงานที่ไม่มีการจ้างงาน** ผู้ปฏิบัติงานจะปรากฏในฟอร์มนี้ เมื่อไม่มีจ้างงานในอดีต ในปัจจุบัน หรือในอนาคต สำหรับผู้ปฏิบัติงาน ในรุ่นนี้ การลบจะถูกเปิดใช้งานเฉพาะผู้ดูแลระบบเท่านั้น อย่างไรก็ตาม ในการนำออกใช้ของสัปดาห์ถัดไป จะมีการอัพเดตการรักษาความปลอดภัยเพื่ออนุญาตให้ผู้ใช้ทั้งหมดที่มีบทบาทผู้ช่วยของ HR สามารถลบพนักงานได้โดยไม่มีจ้างงาน นอกจากนี้ คุณยังสามารถทำการเปลี่ยนแปลงเหล่านี้ได้ด้วยตนเองโดยปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **การตั้งค่าคอนฟิกการรักษาความปลอดภัย**
2. ในแท็บ **สิทธิ์** ให้กรองรายการ **สิทธิ์** ไปยัง **รักษาผู้ปฏิบัติงาน**
3. ในคอลัมน์ **อ้างอิง** เลือก **รายการเมนูที่แสดง**
4. ใน **รายการเมนูที่แสดง** เลือก **HcmWOrkersWithoutEmployment**
5. ตั้งค่าสิทธิ์ **ลบ** เพื่อให้สิทธิ์
6. เลือกแท็บ **ออบเจ็กต์ที่ยังไม่ได้เผยแพร่**
7. เลือก **เผยแพร่ทั้งหมด**
