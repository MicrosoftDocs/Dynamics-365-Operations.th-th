---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources 9 สิงหาคม 2021
description: บทความนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 9 สิงหาคม 2021
author: marcelbf
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad1397084dd3eb210065fe6d8c20c5b8253cd206
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882879"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources 9 สิงหาคม 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายถึงคุณลักษณะที่ใหม่ ที่มีการเปลี่ยนแปลง หรือที่กำลังจะมาถึงเร็วๆ นี้ ใน Microsoft Dynamics 365 Human Resources

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการอัปเดตและกำหนดการของพวกเรา ให้ดูที่ [กระบวนการอัปเดต](hr-admin-setup-update-process.md)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลักษณะการทำงานใหม่ และวันที่ที่พร้อมใช้งานทั่วไปที่คาดไว้ ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2021 เวฟ 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)

## <a name="in-this-release"></a>ในการเผยแพร่นี้

รุ่นนี้ประกอบด้วยลักษณะการทำงานและการแก้ไขปัญหาบักใหม่ๆ ดังต่อไปนี้ การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.4393

### <a name="bug-fixes"></a>การแก้ไขปัญหา

การแก้ไขปัญหาต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้

> [!NOTE]
> เป้าหมายของเราคือการส่งข้อมูลนี้ให้คุณโดยเร็วที่สุดเท่าที่จะเป็นไปได้ พวกเราอาจมีการอัปเดตในบทความนี้ เพื่อรวมการแก้ไขข้อผิดพลาดที่ทำให้เกิดข้อผิดพลาดในการสร้างหลังจากที่มีการเผยแพร่บทความนี้ในครั้งแรก

| หมายเลขปัญหา | ปัญหา | คำอธิบาย |
| --- | --- | --- |
| 558385 | ผู้ถูกกำหนดเริ่มต้นไม่ถูกเลือกไว้เมื่อตัวเลือก **เลือกผู้ถูกกำหนดอัตโนมัติ** เปิดอยู่สำหรับผู้ถูกกำหนดเริ่มต้น | ขณะนี้ปัญหานี้ได้รับการแก้ไขแล้ว ผู้ถูกกำหนดเริ่มต้นหลายรายจะถูกเลือกโดยอัตโนมัติในแผนที่มีสิทธิ์ เมื่อตัวเลือก **เลือกผู้ถูกกำหนดอัตโนมัติ** บนหน้า **พารามิเตอร์ที่ใช้ร่วมกันของฝ่ายทรัพยากรบุคคล** เปิดอยู่ |
| 589617 | ในหน้า **หมดเวลา** ยอดดุลที่ **พร้อมใช้ในการซื้อ** และ **พร้อมใช้ในการขาย** จะว่างเปล่าเมื่อการเข้าถึงจํากัดไว้เฉพาะบริษัทเท่านั้น | ขณะนี้ปัญหานี้ได้รับการแก้ไขแล้ว หน้า **หมดเวลา** แสดงยอดดุลที่ **พร้อมใช้ในการซื้อ** และ **พร้อมใช้ในการขาย** ที่ถูกต้องเมื่อผู้ใช้ถูกจํากัดไว้เฉพาะบริษัทเท่านั้น |

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

ลักษณะการทำงานใหม่ต่อไปนี้อยู่ในการแสดงตัวอย่าง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเปิดหรือปิดคุณลักษณะ ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)

| ลักษณะการทำงาน | แผนการรีลีส | การจัดทำเอกสาร |
| --- | --- | --- |
| พื้นที่ทำงานการจัดการสวัสดิการ | [พื้นที่ทำงานการจัดการสวัสดิการ(พรีวิว)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [พื้นที่ทำงานการจัดการสวัสดิการ](hr-benefits-management-workspace.md) |
| เปิดใช้งานการรวมค่าจ้างแบบง่าย (API การรวมค่าจ้าง) | [เปิดใช้งานการรวมอย่างง่ายด้วยผู้ให้บริการระบบค่าจ้าง](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)|
| เปิดใช้งานผู้จัดการฝ่ายการขาดงานเพื่อจัดการการลางาน | [เปิดใช้งานผู้จัดการฝ่ายการขาดงานเพื่อจัดการการลางาน](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | ด้วยรุ่นนี้ เราจะอัปเดตมุมมองพื้นที่ทำงานของผู้จัดด้านการลางาน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกบทบาทผู้จัดการด้านการลางาน](https://go.microsoft.com/fwlink/?linkid=2168107) |
| ตั้งค่าคอนฟิกข้อกำหนดเอกสารแนบต่อชนิดการลางาน | [ตั้งค่าคอนฟิกข้อกำหนดเอกสารแนบต่อชนิดการลางาน](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](https://go.microsoft.com/fwlink/?linkid=2168108)|
| ตั้งค่าคอนฟิกหน่วยการลางานต่อชนิดการลางาน | [ตั้งค่าคอนฟิกหน่วยการลางานต่อชนิดการลางาน](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](https://go.microsoft.com/fwlink/?linkid=2168215)|
| เปิดใช้งานพนักงานที่จะเลือกเป็นพร้อมจะชําระเงิน | [เปิดใช้งานพนักงานที่จะเลือกเป็นพร้อมจะชําระเงิน](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [พร้อมที่จะจ่าย](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>เร็วๆ นี้

สำหรับรายการของลักษณะการทำงานที่วางแผนไว้ทั้งหมดและการเผยแพร่ตามกำหนดการของพวกเขา ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2021 เวฟ 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)

| ลักษณะการทำงาน | รายละเอียด |
| --- | --- |
| Platform Update 10.0.21 (45) | การเริ่มต้น Platform update 10.0.21 ถูกจัดกำหนดการให้เริ่มด้วยการนำออกใช้บริการในวันที่ 4 ตุลาคม 2021 สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การอัปเดตแพลตฟอร์มสำหรับรุ่น 10.0.21 ของแอปการเงินและการดำเนินงาน (ตุลาคม 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2021 ปล่อยเวฟ 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
