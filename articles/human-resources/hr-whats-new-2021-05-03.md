---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources 3 พฤษภาคม 2021
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 3 พฤษภาคม 2021
author: marcelbf
ms.date: 05/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 01babeae8ccb5af5e414cb78734ce05adf670277
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689788"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources 3 พฤษภาคม 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่ ที่มีการเปลี่ยนแปลง หรือกำลังจะมาถึงในไม่ช้าใน Dynamics 365 Human Resources

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการอัปเดตและกำหนดการของพวกเรา ให้ดูที่ [กระบวนการอัปเดต](hr-admin-setup-update-process.md)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลักษณะการทำงานใหม่ และวันที่ที่พร้อมใช้งานทั่วไปที่คาดไว้ ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2021 เวฟ 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)

## <a name="in-this-release"></a>ในการเผยแพร่นี้

รุ่นนี้ประกอบด้วยลักษณะการทำงานและการแก้ไขปัญหาบักใหม่ๆ ดังต่อไปนี้ การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.4140

### <a name="new-features"></a>ลักษณะการทำงานใหม่ๆ

โดยทั่วไปลักษณะการทำงานต่อไปนี้จะพร้อมใช้งานกับรุ่นนี้

| ลักษณะการทำงาน | แผนการรีลีส | คู่มือ |
| --- | --- | --- |
| เพิ่มแถบข้อมูลเมื่อสร้างเหตุการณ์ตามอายุการใช้งาน | - | เมื่อคุณสร้างเหตุการณ์ตามอายุการใช้งาน แถบข้อมูลจะแสดงข้อความที่ระบุชนิดของเหตุการณ์อายุการใช้งานที่สร้าง

### <a name="bug-fixes"></a>การแก้ไขปัญหา

การแก้ไขปัญหาต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้

> [!NOTE]
> เป้าหมายของเราคือการส่งข้อมูลนี้ให้คุณโดยเร็วที่สุดเท่าที่จะเป็นไปได้ พวกเราอาจมีการอัปเดตในหัวข้อนี้เพื่อรวมการแก้ไขข้อผิดพลาดที่ทำให้เกิดข้อผิดพลาดในการสร้างหลังจากที่มีการเผยแพร่หัวข้อนี้ในครั้งแรก

| หมายเลขปัญหา | ออก |  คำอธิบาย |
| --- | --- | --- |
| 559312 |  ระดับจะไม่แสดงเมื่อสร้างแผนค่าตอบแทนคงที่ของพนักงาน |  เมื่อมีโซนเวลาที่ไม่ตรงกันระหว่างโซนเวลาของผู้ใช้และโซนเวลาของบริษัท ระดับค่าตอบแทนในงานนั้นไม่สามารถอ่านได้ การสอบถามถูกอัปเดตเพื่อดึงข้อมูลตามเวลา UTC แล้ว |
| 573676  | ไม่สามารถเพิ่มรอบระยะเวลาใหม่ในฟอร์ม **แผนสวัสดิการ** | อัปเดตฟอร์มเพื่อให้เปิดใช้งานปุ่ม **สร้าง** ภายใต้แท็บด่วน **รอบระยะเวลา** ใน **แผนสวัสดิการ** |

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

ลักษณะการทำงานใหม่ต่อไปนี้อยู่ในการแสดงตัวอย่าง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดและปิดคุณลักษณะ ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)

| ลักษณะการทำงาน | แผนการรีลีส | การจัดทำเอกสาร |
| --- | --- | --- |
| พื้นที่ทำงานการจัดการสวัสดิการ | [พื้นที่ทำงานการจัดการสวัสดิการ(พรีวิว)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [พื้นที่ทำงานการจัดการสวัสดิการ](hr-benefits-management-workspace.md) |
| การปรับปรุงประสบการณ์ลำดับงานของการลางานและการขาดงาน | [การปรับปรุงประสบการณ์ลำดับงานของการลางานและการขาดงาน](https://go.microsoft.com/fwlink/?linkid=2147528) | [ร้องขอการหยุดพัก](hr-employee-self-service-request-time-off.md)|
| เปิดใช้งานการรวมค่าจ้างแบบง่าย (API การรวมค่าจ้าง) | [เปิดใช้งานการรวมอย่างง่ายด้วยผู้ให้บริการระบบค่าจ้าง](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)|
| การตรวจสอบธุรกรรมการยกยอดวันลางาน | - | [การตรวจสอบธุรกรรมการยกยอดวันลางาน](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>เร็วๆ นี้

| ลักษณะการทำงาน | รายละเอียด |
| --- | --- |
| Platform Update 10.0.18 (42) | Platform update 10.0.18 ถูกจัดกำหนดการให้เริ่มต้นด้วยการนำออกใช้บริการในวันที่ 17 พฤษภาคม 2021 สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การอัปเดตแพลตฟอร์มสำหรับรุ่น 10.0.18 ของแอปการเงินและการดำเนินงาน (พฤษภาคม 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| การสนับสนุนฟิลด์ที่กำหนดเองในกฎการมีคุณสมบัติเหมาะสมของการจัดการสวัสดิการ  | [การสนับสนุนฟิลด์ที่กำหนดเองสำหรับการประมวลการมีคุณสมบัติเหมาะสม](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

สำหรับรายการของลักษณะการทำงานที่วางแผนไว้ทั้งหมดและการเผยแพร่ตามกำหนดการของพวกเขา ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2021 เวฟ 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2021 ปล่อยเวฟ 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
