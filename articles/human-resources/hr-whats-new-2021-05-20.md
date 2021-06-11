---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources 20 พฤษภาคม 2021
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 20 พฤษภาคม 2021
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: afa64474e8eaf4c7b73e4f76d85e379f77b570a7
ms.sourcegitcommit: eff3da7ea98758f100d44ff7feec17157afc2e80
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111578"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources 20 พฤษภาคม 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่ ที่มีการเปลี่ยนแปลง หรือกำลังจะมาถึงในไม่ช้าใน Dynamics 365 Human Resources

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการอัปเดตและกำหนดการของพวกเรา ให้ดูที่ [กระบวนการอัปเดต](hr-admin-setup-update-process.md)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลักษณะการทำงานใหม่ และวันที่ที่พร้อมใช้งานทั่วไปที่คาดไว้ ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2021 เวฟ 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)

## <a name="in-this-release"></a>ในการเผยแพร่นี้

รุ่นนี้ประกอบด้วยลักษณะการทำงานและการแก้ไขปัญหาบักใหม่ๆ ดังต่อไปนี้ การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.4189

### <a name="new-features"></a>ลักษณะการทำงานใหม่ๆ

โดยทั่วไปลักษณะการทำงานต่อไปนี้จะพร้อมใช้งานกับรุ่นนี้

| ลักษณะการทำงาน | แผนการรีลีส | คู่มือ |
| --- | --- | --- |
| Platform Update 10.0.18 (42) | -- | [แพลตฟอร์มที่อัปเดตสำหรับรุ่น10.0.18 ของแอป Finance and Operations (พฤษภาคม 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| ขณะนี้แอปทรัพยากรบุคคลสำหรับ Microsoft Teams สนับสนุนการนิยามครึ่งวันและความสามารถแบบแบ่งวัน | -- | [จัดการคำขอลางานใน Teams](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>การแก้ไขปัญหา

การแก้ไขปัญหาต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้

> [!NOTE]
> เป้าหมายของเราคือการส่งข้อมูลนี้ให้คุณโดยเร็วที่สุดเท่าที่จะเป็นไปได้ พวกเราอาจมีการอัปเดตในหัวข้อนี้เพื่อรวมการแก้ไขข้อผิดพลาดที่ทำให้เกิดข้อผิดพลาดในการสร้างหลังจากที่มีการเผยแพร่หัวข้อนี้ในครั้งแรก

| หมายเลขปัญหา | ปัญหา |  คำอธิบาย |
| --- | --- | --- |
| 583776 | การลงทะเบียนโดยรวมของพนักงานเข้าในแผนการลางานทําให้เกิดข้อผิดพลาดของเรกคอร์ดซ้ำ | บักนี้ได้รับการแก้ไขด้วยการนำออกใช้ล่าสุดและควรประมวลผลการลงทะเบียนแผนการลางานโดยรวมเสร็จเรียบร้อยแล้ว |
| 582263 | ไม่สามารถรันการประมวลผลเหตุการณ์ตามอายุการใช้งานของผู้ปฏิบัติงานทั้งหมดในคราวเดียว | เมื่อฟิลด์ **ผู้ปฏิบัติงาน** ถูกปล่อยว่างไว้เพื่อการประมวลผลเหตุการณ์ตามอายุการใช้งาน ผู้ปฏิบัติงานทั้งหมดจะได้รับการประมวลผล |
| 558383 | ไม่ได้เลือกผู้รับผลประโยชน์หลักเป็น 100% ถ้าไม่ได้เลือกผู้ออกแบบเริ่มต้น | บักได้รับการแก้ไขแล้วเพื่อให้ผู้ใช้ต้องเลือกสลับผู้รับผลประโยชน์หลักเท่านั้น|
| 509404 | การวิเคราะห์พนักงานของแผนกไม่ได้พิจารณาการเคลื่อนย้ายของพนักงานระหว่างแผนก |การวิเคราะห์ได้รับการอัปเดตเพื่อรวมการโอนย้ายของพนักงานระหว่างแผนกต่างๆ|
| 579420 | คุณลักษณะคอลัมน์ที่ตรึงไว้ในกริดยังไม่พร้อมใช้งาน | คุณลักษณะ **คอลัมน์ที่ตรึงไว้ในกริด** ซึ่งไม่พร้อมใช้งานในทรัพยากรบุคคล แสดงรายการอยู่ในการจัดการคุณลักษณะ คุณลักษณะถูกลบออกจากรายการคุณลักษณะที่จะเปิดใช้งานแล้ว |

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

ลักษณะการทำงานใหม่ต่อไปนี้อยู่ในการแสดงตัวอย่าง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดและปิดคุณลักษณะ ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)

| ลักษณะการทำงาน | แผนการรีลีส | คู่มือ |
| --- | --- | --- |
| การสนับสนุนฟิลด์ที่กำหนดเองในกฎการมีคุณสมบัติเหมาะสมของการจัดการสวัสดิการ | [การสนับสนุนฟิลด์ที่กำหนดเองสำหรับการประมวลการมีคุณสมบัติเหมาะสม](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[การกำหนดค่ากฎการมีคุณสมบัติเหมาะสม](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| พื้นที่ทำงานการจัดการสวัสดิการ | [พื้นที่ทำงานการจัดการสวัสดิการ(พรีวิว)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [พื้นที่ทำงานการจัดการสวัสดิการ](hr-benefits-management-workspace.md) |
| การปรับปรุงประสบการณ์ลำดับงานของการลางานและการขาดงาน | [การปรับปรุงประสบการณ์ลำดับงานของการลางานและการขาดงาน](https://go.microsoft.com/fwlink/?linkid=2147528) | [ร้องขอการหยุดพัก](hr-employee-self-service-request-time-off.md)|
| เปิดใช้งานการรวมค่าจ้างแบบง่าย (API การรวมค่าจ้าง) | [เปิดใช้งานการรวมอย่างง่ายด้วยผู้ให้บริการระบบค่าจ้าง](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)|
| การตรวจสอบธุรกรรมการยกยอดวันลางาน | - | [การตรวจสอบธุรกรรมการยกยอดวันลางาน](hr-leave-and-absence-accrue.md#preview-leave-accrual-transaction-auditing)|

## <a name="coming-soon"></a>เร็วๆ นี้

| ลักษณะการทำงาน | รายละเอียด |
| --- | --- |
|  เปิดใช้งานผู้จัดการฝ่ายการขาดงานเพื่อจัดการการลางาน | [เปิดใช้งานผู้จัดการฝ่ายการขาดงานเพื่อจัดการการลางาน](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

สำหรับรายการของลักษณะการทำงานที่วางแผนไว้ทั้งหมดและการเผยแพร่ตามกำหนดการของพวกเขา ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2021 เวฟ 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2021 ปล่อยเวฟ 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
