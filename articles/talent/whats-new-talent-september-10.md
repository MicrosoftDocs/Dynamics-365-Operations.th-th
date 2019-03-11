---
title: มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (10 กันยายน 2018)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
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
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306474"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a>มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (10 กันยายน 2018)

[!include [banner](includes/banner.md)]

**สร้าง 8.1.138.0**

หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>อนุญาตเวลาที่เฉพาะเจาะจงของวันในคำร้องขอเวลาหยุดพัก (ครึ่งวัน)

หากการลางานและการขาดงานถูกตั้งค่า เพื่อให้เวลาหยุดพักถูกส่งในหน่วยวัน ขณะนี้ คุณยังสามารถเปิดใช้งานคำนิยามครึ่งวันอีกด้วย จากนั้น เมื่อผู้ใช้ส่งคำขอของเวลาหยุดพัก พวกเขาสามารถระบุได้ว่า พวกเขาร้องขอวันหยุดครึ่งวันแรก หรือครึ่งวันหลัง

โดยค่าเริ่มต้น ตัวเลือกนี้จะถูกปิดไว้ สำหรับพนักงานที่จะร้องขอวันหยุดครึ่งวันแรกหรือครึ่งวันหลัง คุณต้องเปิดใช้งานตัวเลือกนี้ในพื้นที่ **การลางานและการขาดงาน** ของพารามิเตอร์ทรัพยากรบุคคล

สิทธิ์ความปลอดภัยสำหรับคุณลักษณะนี้คือ รักษาพารามิเตอร์ทรัพยากรบุคคล

## <a name="validation-of-leave-and-absence-entries"></a>การตรวจสอบของรายการการขาดงานและการลางาน

โดยขึ้นอยู่กับวิธีการตั้งค่าคอนฟิกการลางาน พนักงานที่พยายามส่งคำขอเวลาหยุดพักที่ยาวเกินกว่าจำนวนวันทำงานของพวกเขา จะได้รับข้อความแจ้งเตือน กล่าวคือ รายการเหล่านั้นจะได้รับการเตือน ถ้าพวกเขาใช้เวลามากกว่าหนึ่งวันเต็มๆ ในวันที่ใด ๆ ที่ระบุ

การตรวจสอบนี้ถูกเปิดอยู่เสมอ เวลาใดๆ ที่พนักงานเกินขีดจำกัดวันที่กำหนดไว้ พวกเขาจะได้รับคำเตือนในคำขอเวลาหยุดพักของพวกเขา

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>ฟิลด์เพิ่มเติมสำหรับการกำหนดเงื่อนไขในลำดับงาน

มีการเพิ่มฟิลด์เพิ่มเติมไปยังการกำหนดเงื่อนไขและตัวยึดตำแหน่งสำหรับลำดับงานหลายรายการใน Core HR

ระบบได้เพิ่มฟิลด์ต่อไปนี้ ไปยังค่าตอบแทน การสิ้นสุดการจ้างงาน และลำดับงานการโอนย้าย:

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
- TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- ตำแหน่ง
- สหภาพ
- แผนก
- PositionType
- CompLocation
- ชื่อตำแหน่ง
- งาน
- JobType
- JobFamily
- JobFunction

ระบบได้เพิ่มฟิลด์ต่อไปนี้ลงในเวิร์กโฟลว์ตำแหน่ง:

- ตำแหน่ง
- สหภาพ
- แผนก
- PositionType
- CompLocation
- ชื่อตำแหน่ง
- งาน
- JobType
- JobFamily
- JobFunction

ฟิลด์ในคำสั่งแบบมีเงื่อนไขและตัวยึดตำแหน่ง จะพร้อมใช้งานสำหรับผู้ใช้ทั้งหมดที่สามารถเข้าถึงการตั้งค่าคอนฟิกลำดับงานที่กล่าวไว้ก่อนหน้านี้

## <a name="navigation-to-attract-from-personnel-management"></a>การนำทางไปยัง Attract จากการจัดการบุคลากร

ในการจัดการบุคลากร ถ้า Attract ยังไม่ได้ถูกตั้งค่า ส่วน **ผู้สมัครที่จะจ้าง** กำหนดให้ผู้ใช้เริ่มต้นด้วย Attract แทนที่จะแสดงข้อความ "เราไม่พบสิ่งที่จะแสดงไว้ที่นี่"

## <a name="other-changes"></a>การเปลี่ยนแปลงอื่นๆ

รุ่นนี้ประกอบด้วยการแก้ไขบักเพิ่มเติมหลายรายการ:

- เมื่อมีการว่าจ้างผู้รับจ้าง แท็บ **ค่าตอบแทน** ไม่ควรพร้อมใช้งานบนหน้าคำขอ/การดำเนินการ
- ในระหว่างกระบวนการร้องขอการเลิกจ้าง คุณไม่สามารถทำต่อไปได้ จนกว่าฟิลด์ที่จำเป็นทั้งหมดประกอบด้วยข้อมูล
- เรียงปัญหาในการเรียงลำดับและการแสดงวันที่ในการจัดการบุคลากร ได้ถูกระบุ
