---
title: การลงทะเบียนพนักงานในแผนค่าตอบแทนคงที่
description: 'ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการสามารถกำหนดพนักงานไปยังแผนค่าตอบแทนคงที่เพื่อจัดการค่าจ้างพื้นฐานของพวกเขา '
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d611f2631a59fbe1e131e82ca9937a5adaaf2ebd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688754"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>การลงทะเบียนพนักงานในแผนค่าตอบแทนคงที่


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการสามารถกำหนดพนักงานไปยังแผนค่าตอบแทนคงที่เพื่อจัดการค่าจ้างพื้นฐานของพวกเขา  ขั้นตอนนี้ถือว่าแผนถาวรถูกสร้างขึ้นแล้วและกำลังเปิดใช้งานอยู่ และถือว่าได้ตั้งกฎการมีสิทธิ์สำหรับแผนไว้แล้ว  บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF หากจะเริ่มต้นกระบวนการ ให้ไปที่ **ทรัพยากรบุคคล** > **ผู้ปฏิบัติงาน** > **พนักงาน** > **ค่าตอบแทน** > **แผนคงที่**

1. คลิก **สร้าง**
2. ในฟิลด์ **การดำเนินการ** เลือกการดำเนินการค่าตอบแทนคงที่ของ **การจ้างงาน/จ้างงานใหม่** เพื่ออธิบายการเปลี่ยนแปลงในค่าตอบแทนของพนักงาน
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
4. ในฟิลด์ **ตำแหน่ง** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
5. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
    * ระดับที่ถูกแสดงนั้นมาจากแท็บด่วน **ค่าตอบแทน** > **ระดับ** จาก **งาน** ที่กำหนดให้กับ **ตำแหน่ง** ระดับต้องถูกตั้งค่าบนงานก่อนที่คุณจะสามารถกำหนดค่าตอบแทนให้กับพนักงาน  
6. ในฟิลด์ **แผน** เลือกแผนค่าตอบแทนคงที่สำหรับพนักงาน การค้นหา **แผนn** จะถูกกรองเพื่อแสดงเฉพาะแผนที่พนักงานมีสิทธิตาม **กฎการมีสิทธิ์**
7. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * วันที่ **มีผลบังคับใช้** และ **หมดอายุ** สำหรับค่าตอบแทนจะตั้งต้นจากวันเริ่มต้นและวันสิ้นสุดสำหรับการมอบหมายตำแหน่งงานของผู้ปฏิบัติงาน คุณสามารถปรับเปลี่ยนวันเหล่านี้ตามความจำเป็น  
    * ถ้าแผนค่าตอบแทนคงที่เป็นแผนขั้นตอน เลือกขั้นตอนที่ประกอบด้วยอัตราค่าจ้างที่ถูกต้องสำหรับพนักงาน  ถ้าแผนค่าตอบแทนคงที่เป็นแผนระดับหรือแถบ ให้ป้อนอัตราค่าจ้างสำหรับพนักงาน  อัตราค่าจ้างจะถูกตรวจสอบโดยเทียบกับการตั้งค่าค่าเผื่อสำหรับแผน และจุดอ้างอิงค่าต่ำสุดและสูงสุดสำหรับระดับค่าตอบแทนของงาน  
8. คลิก **ตกลง**



[!INCLUDE[footer-include](../includes/footer-banner.md)]
