---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources 26 กรกฎาคม 2021
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 26 กรกฏาคม 2021
author: marcelbf
ms.date: 07/12/2021
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
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 810511c42cd690579d8c8b6ebcc17b0cf7fcb9eb2b999822dc2226fabd127cc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771526"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources 26 กรกฎาคม 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่ ที่มีการเปลี่ยนแปลง หรือกำลังจะมาถึงในไม่ช้าใน Dynamics 365 Human Resources

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการอัปเดตและกำหนดการของพวกเรา ให้ดูที่ [กระบวนการอัปเดต](hr-admin-setup-update-process.md)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลักษณะการทำงานใหม่ และวันที่ที่พร้อมใช้งานทั่วไปที่คาดไว้ ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2021 เวฟ 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)

## <a name="in-this-release"></a>ในการเผยแพร่นี้

รุ่นนี้ประกอบด้วยลักษณะการทำงานและการแก้ไขปัญหาบักใหม่ๆ ดังต่อไปนี้ การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.4384

### <a name="new-features"></a>ลักษณะการทำงานใหม่ๆ

โดยทั่วไปลักษณะการทำงานต่อไปนี้จะพร้อมใช้งานกับรุ่นนี้

| ลักษณะการทำงาน | แผนการรีลีส | คู่มือ |
| --- | --- | --- |
| แพลตฟอร์ม update 10.0.20 | -- | [แพลตฟอร์มที่อัปเดตสำหรับรุ่น 10.0.20 ของแอป Finance and Operations (สิงหาคม 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>การแก้ไขปัญหา

การแก้ไขปัญหาต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้

> [!NOTE]
> เป้าหมายของเราคือการส่งข้อมูลนี้ให้คุณโดยเร็วที่สุดเท่าที่จะเป็นไปได้ พวกเราอาจมีการอัปเดตในหัวข้อนี้เพื่อรวมการแก้ไขข้อผิดพลาดที่ทำให้เกิดข้อผิดพลาดในการสร้างหลังจากที่มีการเผยแพร่หัวข้อนี้ในครั้งแรก

| หมายเลขปัญหา | ปัญหา |  คำอธิบาย |
| --- | --- | --- |
| 600422 | การตรวจสอบความถูกต้องของที่อยู่เงินเดือนไม่ผ่าน เพื่อให้พร้อมที่จะชำระ | มีการอัปเดตการตรวจสอบความถูกต้องเพื่อต้องการที่อยู่เพียงที่อยู่เดียวของชนิด 'ที่ตั้งถิ่นที่อยู่ในบัญชีเงินเดือน' และที่อยู่เพียงที่อยู่เดียวของชนิด 'สถานที่งานในบัญชีเงินเดือน' |
| 601226 | ปัญหาการรวมข้อมูล: โครงการส่งออกการรวมบัญชีเงินเดือน ไม่มีตัวเลือกในการส่งออกข้อมูลทั้งหมด | การรวมระบบค่าจ้างกับ Ceridian DayForce ถูกส่งส่วนเพิ่มแทนการส่งออกข้อมูลทั้งหมด Ceridian ต้องรีเฟรชแบบเต็มเสมอ ขณะนี้ปัญหานี้แก้ไขแล้ว เอนทิตี้ในโครงการส่งออกข้อมูลจะไม่พลิกไปผลักส่วนเพิ่มอีกต่อไป |
| 602272 | ขณะนี้ไม่มีไทล์ที่เพิ่มไปยังพื้นที่ทำงานระบบพนักงานบริการตนเองแล้ว และไม่สามารถเพิ่มไทล์ได้อีกต่อไป | เราแก้ไขปัญหาเกี่ยวกับการตั้งค่าส่วนบุคคลให้กับระบบบริการตนเองของพนักงาน ไทล์ใหม่สามารถเพิ่มให้กับมุมมองและการตั้งค่าส่วนบุคคลใดๆ ที่มีอยู่จะมองเห็นได้โดยผู้ใช้ |
| 600711 | ฟิลด์การเลือกคำนิยามครึ่งวันที่เปิดใช้งานไว้ของคำขอการลางานเต็มวัน | ปัญหานี้ได้รับการแก้ไขแล้ว และฟิลด์นิยามแบบคงที่และครึ่งวันจะเปิดใช้งานเฉพาะเมื่อพนักงานเลือกชนิดการลางานที่มีการเปิดใช้งานการเลือกคำนิยามครึ่งวัน และครึ่งวันตามค่าจำนวนที่เลือก |
| 602208 | หน่วยอัตราตามเกณฑ์คงค้างที่แสดงชั่วโมงแทนวัน | ขณะนี้ปัญหานี้ได้รับการแก้ไขแล้ว ฟอร์ม **การลาหยุด** จะแสดงหน่วยการลางานที่ถูกต้อง (ชั่วโมงหรือวัน) ของคอลัมน์ **อัตราตามเกณฑ์คงค้าง** |

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

ลักษณะการทำงานใหม่ต่อไปนี้อยู่ในการแสดงตัวอย่าง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดและปิดคุณลักษณะ ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)

| ลักษณะการทำงาน | แผนการรีลีส | การจัดทำเอกสาร |
| --- | --- | --- |
| พื้นที่ทำงานการจัดการสวัสดิการ | [พื้นที่ทำงานการจัดการสวัสดิการ(พรีวิว)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [พื้นที่ทำงานการจัดการสวัสดิการ](hr-benefits-management-workspace.md) |
| เปิดใช้งานการรวมค่าจ้างแบบง่าย (API การรวมค่าจ้าง) | [เปิดใช้งานการรวมอย่างง่ายด้วยผู้ให้บริการระบบค่าจ้าง](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)|
|  เปิดใช้งานผู้จัดการฝ่ายการขาดงานเพื่อจัดการการลางาน | [เปิดใช้งานผู้จัดการฝ่ายการขาดงานเพื่อจัดการการลางาน](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | ด้วยรุ่นนี้ เราจะอัปเดตมุมมองพื้นที่ทำงานของผู้จัดด้านการลางาน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกบทบาทผู้จัดการด้านการลางาน](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  ตั้งค่าคอนฟิกข้อกำหนดเอกสารแนบต่อชนิดการลางาน | [ตั้งค่าคอนฟิกข้อกำหนดเอกสารแนบต่อชนิดการลางาน](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  ตั้งค่าคอนฟิกหน่วยการลางานต่อชนิดการลางาน | [ตั้งค่าคอนฟิกหน่วยการลางานต่อชนิดการลางาน](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](https://go.microsoft.com/fwlink/?linkid=2168215)|
| เปิดใช้งานพนักงานที่จะเลือกเป็นพร้อมจะชําระเงิน | [เปิดใช้งานพนักงานที่จะเลือกเป็นพร้อมจะชําระเงิน](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [พร้อมที่จะจ่าย](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>เร็วๆ นี้

สำหรับรายการของลักษณะการทำงานที่วางแผนไว้ทั้งหมดและการเผยแพร่ตามกำหนดการของพวกเขา ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2021 เวฟ 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2021 ปล่อยเวฟ 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
