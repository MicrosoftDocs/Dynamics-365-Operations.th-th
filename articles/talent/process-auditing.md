---
title: ติดตามการเปลี่ยนแปลงในข้อมูลการสรรหาบุคลากร
description: คุณลักษณะการตรวจสอบกระบวนการช่วยให้คุณสามารถติดตาม เมื่อผู้สมัคร งานที่เปิด หรือใบสมัครงาน เปลี่ยนแปลงสำหรับการรายงานหรือการปฏิบัติตามกฎระเบียบ
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 0b0be541416d2e4be78da223ec8e95c195d90bbc
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832668"
---
# <a name="track-changes-in-recruiting-data"></a>ติดตามการเปลี่ยนแปลงในข้อมูลการสรรหาบุคลากร

[!include [banner](includes/banner.md)]

คุณสามารถติดตามการเปลี่ยนแปลงที่ทำไปยังผู้สมัคร งานที่เปิด และใบสมัครงาน โดยใช้กระบวนการตรวจสอบ นี่เป็นประโยชน์สำหรับการรายงานหรือการปฏิบัติตามกฎระเบียบ

คุณสามารถดูข้อมูลที่ติดตามได้ใน Power BI โดยใช้ตัวเชื่อมต่อ OData สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เชื่อมต่อกับตัวดึงข้อมูล OData ใน Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-connect-odata)

## <a name="track-changes"></a>ติดตามการเปลี่ยนแปลง
เมื่อต้องการตั้งค่าการติดตามการเปลี่ยนแปลงในข้อมูลการสรรหาบุคลากร ให้ทำตามขั้นตอนเหล่านี้:

1. ใน [Power Apps](https://web.powerapps.com) ให้เลือกสภาพแวดล้อมที่เหมาะสม

2. เลือก **การตั้งค่า** (ไอคอนเกียร์) เลือก **การกำหนดค่าขั้นสูง** และจากนั้น เลือก **ทรัพยากร** ภายใต้ **ทรัพยากรนักพัฒนา** 

3. บนหน้า **ทรัพยากรของนักพัฒนา** ให้คัดลอกค่าในฟิลด์ **ค่า Web API ของอินสแตนซ์** ตัวอย่างเช่น ค่าอาจมีลักษณะเป็น: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/

4. จากนั้น คุณสามารถสอบถามข้อมูลจากหนึ่งในเอนทิตีต่อไปนี้:
  - ประวัติงานที่เปิด (msdyn_jobopeninghistories)
  - ประวัติของใบสมัครงาน (msdyn_jobapplicationhistories) 
  - ประวัติผู้สมัคร (msdyn_candidatehistories)

## <a name="data-reported"></a>รายงานข้อมูลแล้ว

ข้อมูลต่อไปนี้พร้อมใช้งานกับการตรวจสอบความถูกต้องของกระบวนการ

| รายงานข้อมูลแล้ว | คำอธิบาย |
| --- | --- |
| เปลี่ยนโดย (msdyn_ChangedbyId) | การอ้างอิงถึงผู้ใช้ |
| สร้างเมื่อ (createdon) |  วันที่และเวลาใน UTC เมื่อเกิดการเปลี่ยนแปลง |
| ชนิดของการเปลี่ยนแปลง (msdyn_changetype) | การเปลี่ยนแปลงใดที่เกิดขึ้น |
| ค่าทั่วไปสำหรับผู้สมัคร งานที่เปิด <br></br>และใบสมัครงาน | ที่สร้าง<br></br>อัพเดตแล้ว |
| ประวัติใบสมัครงาน | เพิ่มอาร์ทิแฟกต์แล้ว <br></br>ลบอาร์ทิแฟกต์แล้ว |
| ประวัติงานที่เปิด | TODO: เพิ่มการลงรายการบัญชีแล้ว <br></br>TODO: ลบการลงรายการบัญชีแล้ว <br></br>TODO: ปรับปรุงการลงรายการบัญชีแล้ว <br></br>TODO: เพิ่มผู้เข้าร่วมแล้ว <br></br>TODO: ลบผู้เข้าร่วมแล้ว |
| ประวัติผู้สมัคร | เพิ่มอาร์ทิแฟกต์แล้ว <br></br>ลบอาร์ทิแฟกต์แล้ว <br></br>เพิ่มประสบการณ์การทำงานแล้ว <br></br>ลบประสบการณ์การทำงานแล้ว <br></br>เพิ่มการศึกษาแล้ว <br></br>ลบการศึกษาแล้ว <br></br>เพิ่มทักษะแล้ว <br></br>ลบทักษะแล้ว <br></br>เพิ่มแท็กแล้ว <br></br>ลบแท็กแล้ว <br></br>เพิ่มเครือข่ายสังคมแล้ว <br></br>ลบเครือข่ายสังคมแล้ว <br></br>เพิ่มรายละเอียดส่วนบุคคลแล้ว <br></br>ปรับปรุงรายละเอียดส่วนบุคคลแล้ว<br></br> |
| ฟิลด์ที่เปลี่ยนแปลง (msdyn_changedfields) | ฟิลด์ที่เปลี่ยนแปลงซึ่งแสดงรายการออบเจ็กต์ JSON อาจไม่จัดเก็บค่าสำหรับฟิลด์ทั้งหมด<br></br><br></br>สำหรับการเปลี่ยนแปลง "สร้างแล้ว" และ "ปรับปรุงแล้ว" จะแสดงรายการฟิลด์บนเรกคอร์ดที่สร้างหรือปรับเปลี่ยน<br></br><br></br>สำหรับชนิดของการเปลี่ยนแปลง "เพิ่มแล้ว" จะแสดงรายการฟิลด์บนเรกคอร์ดรอง<br></br><br></br>**ตัวอย่าง:**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": true } <br></br>} |
|ประวัติใบสมัครงาน | ใบสมัครงาน (msdyn_JobapplicatonId)<br></br>สถานะ (msdyn_status) <br></br>คำอธิบายรายการของสถานะ (msdyn_statusreason) <br></br>เหตุผลการปฏิเสธ (msdyn_rejectionreason) |
| ประวัติงานที่เปิด | งานที่เปิด (msdyn_JobopeningId) <br></br>สถานะ (msdyn_jobopeningstatus) <br></br>คำอธิบายรายการของสถานะ (msdyn_jobopeningstatusreason) |
| ประวัติผู้สมัคร | ผู้สมัคร (msdyn_CandidateId) |
