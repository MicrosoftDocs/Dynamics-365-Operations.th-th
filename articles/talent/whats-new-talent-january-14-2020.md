---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (14 มกราคม 2020)
description: บทความนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 01/14/2020
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
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c885602f99995d536d8ff3be43e67578abcda3fc
ms.sourcegitcommit: a2f9dce06322dada6b5f1c82051ef2359f8c0f12
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/24/2020
ms.locfileid: "3081829"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-14-2020"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (14 มกราคม 2020)

[!include [banner](includes/banner.md)]

บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR

การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2709 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

### <a name="system-unable-to-generate-calendar-days-when-importing-through-data-management-framework-381195"></a>ระบบไม่สามารถสร้างวันปฏิทิน เมื่อนำเข้าโดยผ่านกรอบงานการจัดการข้อมูล (381195)

การเปลี่ยนแปลงนี้แก้ไขปัญหาที่การนำเข้าวันปฏิทินสร้างข้อผิดพลาด **รูปแบบวันที่ที่ไม่ถูกต้อง** ข้อผิดพลาดนี้จะป้องกันไม่ให้มีการสร้างรายการวันที่ของปฏิทินงาน

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
