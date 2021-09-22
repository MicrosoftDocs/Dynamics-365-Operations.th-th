---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources 23 สิงหาคม 2021
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 23 สิงหาคม 2021
author: marcelbf
ms.date: 08/23/2021
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
ms.search.validFrom: 2021-08-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 21c9ee0206bd77a8a2ec42501d64e83077baef09
ms.sourcegitcommit: 696796ca5635863850ae9ef16fc1fb0fc46ce8f0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/28/2021
ms.locfileid: "7441686"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-23-2021"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources 23 สิงหาคม 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่ ที่มีการเปลี่ยนแปลง หรือกำลังจะมาถึงในไม่ช้าใน Microsoft Dynamics 365 Human Resources

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการอัปเดตและกำหนดการของพวกเรา ให้ดูที่ [กระบวนการอัปเดต](hr-admin-setup-update-process.md)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลักษณะการทำงานใหม่ และวันที่ที่พร้อมใช้งานทั่วไปที่คาดไว้ ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2021 เวฟ 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)

## <a name="in-this-release"></a>ในการเผยแพร่นี้

รุ่นนี้ประกอบด้วยลักษณะการทำงานและการแก้ไขปัญหาบักใหม่ๆ ดังต่อไปนี้ การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.4419

### <a name="bug-fixes"></a>การแก้ไขปัญหา

การแก้ไขปัญหาต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้

> [!NOTE]
> เป้าหมายของเราคือการส่งข้อมูลนี้ให้คุณโดยเร็วที่สุดเท่าที่จะเป็นไปได้ พวกเราอาจมีการอัปเดตในหัวข้อนี้เพื่อรวมการแก้ไขข้อผิดพลาดที่ทำให้เกิดข้อผิดพลาดในการสร้างหลังจากที่มีการเผยแพร่หัวข้อนี้ในครั้งแรก

| หมายเลขปัญหา | ปัญหา | คำอธิบาย |
| --- | --- | --- |
| 594066 | ไม่สามารถลบข้อมูลผู้ติดต่อ | เมื่อเลือกเพื่อลบเรกคอร์ดข้อมูลการติดต่อของพนักงาน เรกคอร์ดข้อมูลการติดต่ออื่นที่ไม่ใช่เรกคอร์ดที่เลือกจะถูกลบแทน |
| 611339 | การเพิ่มการตั้งค่าส่วนบุคคลจะส่งผลให้บัญชีธนาคารละเว้นตัวกรองข้อมูลและดึงข้อมูลเรกคอร์ดแรกมาใช้ | การเพิ่มการตั้งค่าส่วนบุคคลทำให้รายการบัญชีธนาคารทำงานการสอบถามการตั้งค่าส่วนบุคคลหลังจากการสอบถามแหล่งข้อมูลทำงาน ซึ่งส่งผลให้การสอบถามดึงข้อมูลเรกคอร์ดสูงสุดโดยไม่พิจารณาว่ากำลังดูรายละเอียดของผู้ปฏิบัติงานใด |
| 591806 | งานวันครบกำหนดการเตรียมความพร้อมถูกคํานวณอย่างไม่ถูกต้อง | วันครบกําหนดถูกคํานวณอย่างไม่ถูกต้องเมื่อมีเงื่อนไขต่อไปนี้: รายการตรวจสอบที่สร้างโดยใช้ปฏิทินที่ใช้ช่วงเวลาแบบขยาย (ตัวอย่างเช่น 2005 ถึง 2050) และการกําหนดลักษณะของผู้ใช้ใช้โซนเวลาอื่นที่ไม่ใช่เวลามาตรฐานกลาง |   
| 592749 | ยอดดุลการลางานไม่ถูกต้องใน **ระบบพนักงานบริการตนเอง** | ถ้าพนักงานมีการจ้างงานในนิติบุคคลมากกว่าหนึ่งแห่ง และมีการเปิดใช้งานมุมมองการลางานระหว่างบริษัท ยอดดุลการลางานอาจไม่ถูกต้อง |
| 603133 | คําเตือนที่ไม่คาดคิดเมื่อส่งคำขอการลาหยุด | เมื่อส่งคำขอการลาหยุด กรอกข้อมูลในฟิลด์ **ครึ่งวัน** ก่อนที่ฟิลด์ **จำนวน** จะทําให้เกิดคําเตือนที่ไม่คาดคิด |
| 606546 | เลือกฟิลด์ที่ไม่ปรากฏในการลาหยุดที่อนุมัติ | กล่องกาเครื่องหมายเพื่อเลือกคำขอลางานที่อนุมัติหลายรายการมองไม่เห็น |
| 597059 | ผู้ปฏิบัติงานที่ไม่สามารถมองเห็นได้ใน **ปฏิทินบริษัทของการลางานและการขาดงาน** | ผู้ปฏิบัติงานจะไม่ปรากฏใน **ปฏิทินบริษัทของการลางานและการขาดงาน** ถ้าช่วงวันที่ใช้รวมวันใดๆ ที่พวกเขาถูกปฏิเสธคำขอลางาน |


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
| Platform Update 10.0.21 (45) | การเริ่มต้น Platform update 10.0.21 ถูกจัดกำหนดการให้เริ่มด้วยการนำออกใช้บริการในวันที่ 4 ตุลาคม 2021 เมื่อต้องการเรียนรู้เพิ่มเติม ให้ดูที่ [Platform update สำหรับรุ่น10.0.21 ของแอป Finance and Operations (ตุลาคม 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2021 ปล่อยเวฟ 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
