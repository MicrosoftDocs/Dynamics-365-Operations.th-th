---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources 2 ธันวาคม 2020
description: บทความนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 2 ธันวาคม 2020
author: marcelbf
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cecef6d2e73b42126b1be100dca52ebd8d9270fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848120"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources 2 ธันวาคม 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายถึงคุณลักษณะใหม่ ที่มีการเปลี่ยนแปลง หรือที่กำลังจะมาถึงเร็วๆ นี้ ใน Dynamics 365 Human Resources

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการอัปเดตและกำหนดการของพวกเรา ให้ดูที่ [กระบวนการอัปเดต](hr-admin-setup-update-process.md)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลักษณะการทำงานใหม่ และวันที่ที่พร้อมใช้งานทั่วไปที่คาดไว้ ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2020 เวฟ 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)

## <a name="in-this-release"></a>ในการเผยแพร่นี้

รุ่นนี้ประกอบด้วยลักษณะการทำงานและการแก้ไขปัญหาบักใหม่ๆ ดังต่อไปนี้ การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3788

### <a name="new-features"></a>ลักษณะการทำงานใหม่ๆ

โดยทั่วไปลักษณะการทำงานต่อไปนี้จะพร้อมใช้งานกับรุ่นนี้

| ลักษณะการทำงาน | แผนการรีลีส | การจัดทำเอกสาร |
| --- | --- | --- |
| ผู้จัดการสามารถส่งคำขอสรรหาบุคลากรสำหรับตำแหน่งงาน | [ผู้จัดการสามารถส่งคำขอสรรหาบุคลากรสำหรับตำแหน่งงานที่เปิด](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [เพิ่มคำขอสรรหาบุคลากร](./hr-personnel-recruit.md#add-a-recruiting-request) |
| โพรไฟล์ผู้สมัครที่เพิ่มขึ้นในการจัดการบุคลากร | [โพรไฟล์ผู้สมัครที่เพิ่มขึ้นในการจัดการบุคลากร](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [เพิ่มหรือแก้ไขโพรไฟล์ผู้สมัคร](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| เปิดใช้งานการรวมอย่างง่ายด้วยผู้ให้การสรรหาบุคลากร | [เปิดใช้งานการรวมอย่างง่ายด้วยผู้ให้การสรรหาบุคลากร](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [สรรหาผู้สมัครงาน](./hr-personnel-recruit.md) |
| ลิงก์แบบกำหนดเองในระบบบริการตนเองของผู้จัดการ | [ลิงก์แบบกำหนดเองในระบบบริการตนเองของผู้จัดการ](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [ลิงก์แบบกำหนดเองในระบบบริการตนเองของผู้จัดการ](./hr-employee-manager-self-service-custom-links.md) |


### <a name="bug-fixes"></a>การแก้ไขปัญหา

การแก้ไขปัญหาต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้

> [!NOTE]
> เป้าหมายของเราคือการส่งข้อมูลนี้ให้คุณโดยเร็วที่สุดเท่าที่จะเป็นไปได้ พวกเราอาจมีการอัปเดตในบทความนี้ เพื่อรวมการแก้ไขข้อผิดพลาดที่ทำให้เกิดข้อผิดพลาดในการสร้างหลังจากที่มีการเผยแพร่บทความนี้ในครั้งแรก

| หมายเลขปัญหา | ปัญหา | คำอธิบาย |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult ควรรวม datetime ที่ใช้ในการประมวลผล | ขณะนี้ผลการประมวลผล BenefitEligibity มี datetimestamp สำหรับการประมวลผลครั้งล่าสุด ซึ่งขาดหายไปก่อนหน้านี้ |
| 526903 | การลงทะเบียนสวัสดิการล้มเหลวสำหรับแผนที่มีผู้อยู่ในอุปการะ เมื่อ **เลือกผู้ถูกกำหนดอัตโนมัติ** ถูกเปิดอยู่ใน **พารามิเตอร์ที่ใช้ร่วมกันของฝ่ายทรัพยากรบุคคล** | แก้ไขปัญหาที่ซึ่งการลงทะเบียนสวัสดิการมีความล้มเหลวสำหรับผู้อยู่ในอุปการะ เมื่อเปิดใช้งานตัวเลือก **เลือกผู้ถูกกำหนดอัตโนมัติ** ถูกเปิดอยู่สำหรับผู้ถูกกำหนดเริ่มต้น |
| 521922 | พารามิเตอร์ **แสดงข้อมูลการขาดงานโดยไม่มีรายละเอียด** แสดงรายละเอียดของคำขอเวลาหยุดพักในปฏิทินการขาดงานของทีมงาน | ชนิดการลางาน สีของชนิดการลางาน และรายละเอียดวัน ที่แสดงอยู่ในปฏิทินการขาดงานของทีมงาน เมื่อ **แสดงการขาดงานโดยไม่มีรายละเอียด** ถูกกำหนดเป็น **ใช่** ใน **พารามิเตอร์การลางานและการขาดงาน** นี่ได้รับการแก้ไขแล้ว และขณะนี้ชนิดการลางานจะไม่แสดงขึ้นและมีการใช้สีของชนิดการลางานเริ่มต้น (สีน้ำเงินเข้ม) สำหรับชนิดการลางานทั้งหมดในปฏิทินการขาดงานของทีมงาน |
| 527316 | การเปลี่ยนแปลงชื่อเรื่องสำหรับการแจ้งเตือนงาน ตำแหน่ง และผู้ปฏิบัติงาน ไม่ได้ซิงค์กัน | ความสัมพันธ์ของชื่อเรื่องถูกเพิ่มเข้าไปในเอนทิตีงาน ตำแหน่ง และผู้ปฏิบัติงาน ก่อนหน้านี้ การซิงค์สำหรับความสัมพันธ์นี้ใช้ได้สำหรับการซิงค์จากทรัพยากรบุคคลไปยัง Dataverse แต่ใช้ไม่ได้สำหรับการแจ้งเตือนจาก Dataverse นี่ได้รับการแก้ไขแล้ว |
| 512275 | ลบตัวเลือกสีออกจาก **พารามิเตอร์การลางานและการขาดงาน** | หลังจากที่มีการกำหนดสีในชนิดการลางานแล้ว ตัวเลือกสีจะไม่จำเป็นใน **พารามิเตอร์การลางานและการขาดงาน** อีกต่อไป ดังนั้นจึงถูกลบออก |
| 437112 | ข้อความแสดงข้อผิดพลาดที่ทำให้เข้าใจผิดพลาดในระหว่างการกำหนดตำแหน่งพนักงาน | ปรับปรุงข้อความแสดงข้อผิดพลาด เมื่อจ้างผู้ปฏิบัติงานและพยายามกำหนดผู้ปฏิบัติงานให้กับตำแหน่งที่ไม่ได้ใช้งานอยู่ ข้อความที่ปรับปรุง **ตำแหน่งที่ระบุไม่ได้ใช้งานอยู่ ณ วันที่เริ่มต้นการจ้างงาน โปรดตรวจสอบระยะเวลาของตำแหน่งนี้** |
| 527816 | ปัญหาประสิทธิภาพการทำงานกับหน้า **เวลาหยุดพัก** | มีการปรับปรุงประสิทธิภาพการทำงานในหน้า **เวลาหยุดพัก** |
| 523158 | BenefitPeriodMigrationUpgrade และ BenefitPlanMigrationUpgrade ไม่ได้ดำเนินการ | แก้ไขปัญหาด้วยการย้ายสวัสดิการที่เกี่ยวข้องกับ **รอบระยะเวลา** และ **แผน** ที่ดำเนินงานไม่ถูกต้อง |

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

ลักษณะการทำงานใหม่ต่อไปนี้อยู่ในการแสดงตัวอย่าง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดและปิดคุณลักษณะ ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)

| ลักษณะการทำงาน | แผนการรีลีส | การจัดทำเอกสาร |
| --- | --- | --- |
| แอป Human Resources ใน Microsoft Teams | [ประสบการณ์การลางานและการขาดงานของพนักงานใน Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [แอป Human Resources ใน Teams](./hr-admin-teams-leave-app.md)<br>[จัดการคำขอลางานใน Teams](hr-teams-leave-app.md) |
| คำขอและการอนุมัติลำดับงานที่ดีขึ้น | [การปรับปรุงประสบการณ์ของลำดับงานการจัดการองค์กรและบุคลากร](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [ตัวเลือกการตั้งค่าคอนฟิกเพื่อกำหนดตำแหน่งรายการงานที่กำหนดให้กับฉัน](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| การรวมกับ LinkedIn Talent Hub | [การรวมกับ LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [รวมกับ LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
|มุมมองข้ามบริษัทของการลางานสำหรับผู้จัดการ | [มุมมองข้ามบริษัทของการลางานของพนักงานสำหรับผู้จัดการ](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน](./hr-leave-and-absence-parameters.md) |
|ให้ข้อมูลเชิงลึกเพิ่มเติมในยอดดุลการลางาน| [ให้ข้อมูลเชิงลึกเพิ่มเติมในยอดดุลการลางาน](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [จัดการการลางานของพนักงาน](./hr-leave-and-absence-manage-employee-leave.md) |
| ผู้จัดการสามารถส่งคำขอสรรหาบุคลากรสำหรับตำแหน่งงาน | [ผู้จัดการสามารถส่งคำขอสรรหาบุคลากรสำหรับตำแหน่งงานที่เปิด](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [เพิ่มคำขอสรรหาบุคลากร](./hr-personnel-recruit.md#add-a-recruiting-request) |
| โพรไฟล์ผู้สมัครที่เพิ่มขึ้นในการจัดการบุคลากร | [โพรไฟล์ผู้สมัครที่เพิ่มขึ้นในการจัดการบุคลากร](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [เพิ่มหรือแก้ไขโพรไฟล์ผู้สมัคร](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| เปิดใช้งานการรวมอย่างง่ายด้วยผู้ให้การสรรหาบุคลากร | [เปิดใช้งานการรวมอย่างง่ายด้วยผู้ให้การสรรหาบุคลากร](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [สรรหาผู้สมัครงาน](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>เร็วๆ นี้

สำหรับรายการของลักษณะการทำงานที่วางแผนไว้ทั้งหมดและการเผยแพร่ตามกำหนดการของพวกเขา ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2020 เวฟ 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2020 ปล่อยเวฟ 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]