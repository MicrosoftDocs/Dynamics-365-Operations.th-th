---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources 22 ตุลาคม 2020
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Human Resources
author: jcart1106
manager: tfehr
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e5c66d8695ee0ff41e81c699a5d5a37075470059
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107547"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources 22 ตุลาคม 2020

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่ ที่มีการเปลี่ยนแปลง หรือกำลังจะมาถึงในไม่ช้าใน Dynamics 365 Human Resources สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการอัปเดตและกำหนดการของพวกเรา ให้ดูที่ [กระบวนการอัปเดต](hr-admin-setup-update-process.md)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลักษณะการทำงานใหม่ และวันที่ที่พร้อมใช้งานทั่วไปที่คาดไว้ ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2020 เวฟ 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)

## <a name="in-this-release"></a>ในการเผยแพร่นี้

รุ่นนี้ประกอบด้วยลักษณะการทำงานและการแก้ไขปัญหาบักใหม่ๆ ดังต่อไปนี้ การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3680

### <a name="new-features"></a>ลักษณะการทำงานใหม่ๆ

โดยทั่วไปลักษณะการทำงานต่อไปนี้จะพร้อมใช้งานกับรุ่นนี้

| ลักษณะการทำงาน | แผนการรีลีส | การจัดทำเอกสาร |
| --- | --- | --- |
| Platform Update 10.0.14(38) | -- | [แพลตฟอร์มที่อัพเดตสำหรับรุ่น10.0.14 ของแอป Finance and Operations (พฤศจิกายน 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14) |
| การปรับปรุงประสบการณ์ของลำดับงานการจัดการองค์กรและบุคลากร | [การปรับปรุงประสบการณ์ของลำดับงานการจัดการองค์กรและบุคลากร](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [ตัวเลือกการตั้งค่าคอนฟิกเพื่อกำหนดตำแหน่งรายการงานที่กำหนดให้กับฉัน](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>การแก้ไขปัญหา

การแก้ไขปัญหาต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้

> [!NOTE]
> เป้าหมายของเราคือการส่งข้อมูลนี้ให้คุณโดยเร็วที่สุดเท่าที่จะเป็นไปได้ พวกเราอาจมีการอัปเดตในหัวข้อนี้เพื่อรวมการแก้ไขข้อผิดพลาดที่ทำให้เกิดข้อผิดพลาดในการสร้างหลังจากที่มีการเผยแพร่หัวข้อนี้ในครั้งแรก

| หมายเลขปัญหา| ออก  | คำอธิบาย|
| --- | --- | --- |
| 437922 | การนำเข้าชั่วโมง FMLA โดยใช้เอนทิตี DMF จะทำให้เกิดข้อผิดพลาดในการอ่านอย่างเดียว | การใช้เอนทิตีชั่วโมง FMLA เพื่อนำเข้าชั่วโมงที่เชื่อมโยงกับกรณี FMLA ล้มเหลว เราได้เพิ่มตรรกะเพื่อให้แน่ใจว่าชั่วโมงที่นำเข้าไม่เกินชั่วโมงที่เหลืออยู่สำหรับกรณี |
| 512019 | ยอดเงิน **ยกยอดไปล่าสุด** ที่ไม่ถูกต้อง | ในหน้า **เวลาหยุดพัก** ให้เปลี่ยน **ณ วันที่** เป็นวันแรกของรอบระยะเวลาทางบัญชีถัดไปซึ่งแสดงยอดเงิน **ยกยอดไป** ที่ไม่ถูกต้องสำหรับชนิด **การลางานประจำปี** ขณะนี้แสดงยอดเงินที่ถูกต้อง |
| 458639 | เอนทิตี **ผู้ติดต่อของผู้ปฏิบัติงาน** ไม่สนับสนุนโหมดการติดตามการเปลี่ยนแปลง | เราปรับปรุงเอนทิตี **ผู้ติดต่อของผู้ปฏิบัติงาน** เพื่อให้คุณสามารถใช้สถานการณ์การใช้ฐานข้อมูลของคุณเอง (BYOD)|
| 505347 | ผู้จัดการฝ่ายฝึกอบรมสามารถส่งคำขอการลางานสำหรับพนักงานเมื่อมีการเปิดใช้งานลักษณะการทำงานของผู้ปฏิบัติงานที่มีประสิทธิภาพ | บทบาทอื่นๆ นอกเหนือจากผู้ช่วยฝ่ายทรัพยากรบุคคลหรือผู้จัดการฝ่ายทรัพยากรบุคคลไม่ได้รับอนุญาตให้ส่งคำขอ time0off สำหรับพนักงาน |
| 513490 | การบันทึกการจัดการสวัสดิการ: เพิ่มการบันทึกสำหรับแผนโดยไม่มีตัวเลือกความครอบคลุม | เราเปิดใช้งานการบันทึกผลลัพธ์สำหรับ **แผนโดยไม่มีตัวเลือกความครอบคลุม** ขณะนี้แสดงอยู่ในตาราง **ผลลัพธ์ของกระบวนการ** และเรียงลำดับอย่างถูกต้องเพื่อแสดงที่ด้านบนสุด |
| 517021 | ไม่สามารถเลือกหลายแผนที่มีรหัส **ชนิดของแผน** เดียวกันได้ถ้า **ชนิดของแผน** มีการลงทะเบียนหนึ่งรายการสำหรับแต่ละชนิด | เราเปลี่ยนข้อจำกัดสำหรับการเลือกแผนที่ซึ่งอนุญาตให้มีการลงทะเบียนได้เพียงรายการเดียวเท่านั้น ขณะนี้ข้อจำกัดอยู่ในระดับ **รหัสชนิดของแผน** แทนที่จะเป็น **ชนิดของแผน** การเปลี่ยนแปลงนี้จะทำให้แผน เช่น HSA และ FSA ซึ่งเป็นชนิดเดียวกัน แต่คุณสามารถกำหนด **รหัสชนิดของแผน** แยกต่างหากได้ วิธีการนี้จะทำให้คุณสามารถเลือกทั้งสองอย่างสำหรับรอบระยะเวลาการลงทะเบียนเดียวกันได้ |
| 444791 | ไม่สามารถดูค่าตอบแทนในบริการตนเองของพนักงานเมื่อ **จำกัดการเข้าถึง** เปิดอยู่ในแผนค่าตอบแทน | ในบัตร **ค่าตอบแทน** ของพนักงานบริการตนเอง ยอดเงินค่าตอบแทนปัจจุบันและเปอร์เซ็นต์การขึ้นค่าตอบแทนที่แสดง "0" ถ้ามีการลงทะเบียนพนักงานในแผนที่มี **การจำกัดการเข้าถึง** และกำหนดให้กับบทบาทเฉพาะ เราแก้ไขปัญหานี้เพื่อให้พนักงานและผู้จัดการสามารถดูรายละเอียดค่าตอบแทนสำหรับตนเองและรายงานโดยตรงได้เสมอ |
| 457542 | การอัปเดตรายละเอียดหลักสูตรหลังจากที่ปิดหลักสูตรยังไม่ได้อัปเดตข้อมูลเดียวกันสำหรับพนักงานที่ใช้หลักสูตร | ข้อมูลพนักงานจะอัปเดตโดยทันที เมื่อคุณเปลี่ยนรายละเอียดหลักสูตรหลังจากปิดและเปิดหลักสูตรอีกครั้ง |
| 515342 | ไม่สามารถแทรกข้อมูลโดยใช้ **CDSLeaveRequestDetailEntity** ไม่พบบริษัทหรือไม่มีอยู่ | ตอนนี้คุณสามารถใช้ **CDSLeaveRequestDetailEntity** เพื่อแทรกข้อมูล |
| 514743 | เกิดข้อผิดพลาดในฟอร์ม **พารามิเตอร์อีเมล** เมื่อใช้ Microsoft Exchange | ข้อความ "ไม่สามารถโหลดไฟล์หรือแอสเซมบลี..." แสดงอยู่ในหน้า **พารามิเตอร์อีเมล** เมื่อผู้ให้บริการอีเมลถูกตั้งค่าเป็น **แลกเปลี่ยน** การแก้ไขนี้จะช่วยให้หน้า **พารามิเตอร์อีเมล** โหลดและบันทึกตามที่คาดไว้ |


## <a name="in-preview"></a>ในการแสดงตัวอย่าง

ลักษณะการทำงานใหม่ต่อไปนี้อยู่ในการแสดงตัวอย่าง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดและปิดคุณลักษณะ ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)

| ลักษณะการทำงาน | แผนการรีลีส | การจัดทำเอกสาร |
| --- | --- | --- |
| แอป Human Resources ใน Microsoft Teams | [ประสบการณ์การลางานและการขาดงานของพนักงานใน Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [แอป Human Resources ใน Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[จัดการคำขอลางานใน Teams](hr-teams-leave-app.md) |
| คำขอและการอนุมัติลำดับงานที่ดีขึ้น | [การปรับปรุงประสบการณ์ของลำดับงานการจัดการองค์กรและบุคลากร](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [ตัวเลือกการตั้งค่าคอนฟิกเพื่อกำหนดตำแหน่งรายการงานที่กำหนดให้กับฉัน](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| เอนทิตีเสมือนใน Common Data Service สำหรับทรัพยากรบุคคล | [ขยายข้อมูลหลัก Dynamics 365 Human Resources ใน Common Data Service](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [ตั้งค่าคอนฟิกเอนทิตีเสมือน Common Data Service](hr-admin-integration-common-data-service-virtual-entities.md) |
| การรวมกับ LinkedIn Talent Hub | [การรวมกับ LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [รวมกับ LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| ลิงก์แบบกำหนดเองในระบบบริการตนเองของผู้จัดการ | [ลิงก์แบบกำหนดเองในระบบบริการตนเองของผู้จัดการ](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [ลิงก์แบบกำหนดเองในระบบบริการตนเองของผู้จัดการ](https://aka.ms/MSSCustomLinks) |

## <a name="coming-soon"></a>เร็วๆ นี้

สำหรับรายการของลักษณะการทำงานที่วางแผนไว้ทั้งหมดและการเผยแพร่ตามกำหนดการของพวกเขา ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2020 เวฟ 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)


## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2020 ปล่อยเวฟ 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)
