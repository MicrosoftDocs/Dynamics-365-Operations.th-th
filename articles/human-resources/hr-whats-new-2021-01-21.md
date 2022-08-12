---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources 21 มกราคม 2021
description: บทความนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 21 มกราคม 2021
author: marcelbf
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f1daf630d3a9354012db9b5b487d8a5ed11e0ed
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066714"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources 21 มกราคม 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายถึงคุณลักษณะใหม่ ที่มีการเปลี่ยนแปลง หรือที่กำลังจะมาถึงเร็วๆ นี้ ใน Dynamics 365 Human Resources

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการอัปเดตและกำหนดการของพวกเรา ให้ดูที่ [กระบวนการอัปเดต](hr-admin-setup-update-process.md)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลักษณะการทำงานใหม่ และวันที่ที่พร้อมใช้งานทั่วไปที่คาดไว้ ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2020 เวฟ 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)


## <a name="in-this-release"></a>ในการเผยแพร่นี้

รุ่นนี้ประกอบด้วยลักษณะการทำงานและการแก้ไขปัญหาบักใหม่ๆ ดังต่อไปนี้ การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3866

### <a name="new-features"></a>ลักษณะการทำงานใหม่ๆ

โดยทั่วไปลักษณะการทำงานต่อไปนี้จะพร้อมใช้งานกับรุ่นนี้

| ลักษณะการทำงาน | แผนการรีลีส | การจัดทำเอกสาร |
| --- | --- | --- |
| Platform Update 10.0.16(40) | -- | [การอัปเดตแพลตฟอร์มสำหรับรุ่น 10.0.16 ของแอปการเงินและการดำเนินงาน (กุมภาพันธ์ 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16.md) |
| คำขอและการอนุมัติลำดับงานที่ดีขึ้น | [การปรับปรุงประสบการณ์ของลำดับงานการจัดการองค์กรและบุคลากร](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [ตัวเลือกการตั้งค่าคอนฟิกเพื่อกำหนดตำแหน่งรายการงานที่กำหนดให้กับฉัน](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| การอัพเดตการปฏิบัติตามกฎระเบียบของ Affordable Care Act (ACA) ของแบบฟอร์ม 1095-C แบบฟอร์ม 1095-B และการรายงานทางอิเล็กทรอนิกส์ในสวัสดิการดั้งเดิม | -- | -- | 
| ตอนนี้ การจัดการสวัสดิการสนับสนุนการรายงานการปฏิบัติตามกฎระเบียบ ACA ของนิติบุคคลตามสหรัฐอเมริกา | -- | [สร้างรายงาน ACA ในการจัดการสวัสดิการ](hr-benefits-management-aca-reports.md) |
| ขณะนี้ การจัดการสวัสดิการมีระดับอัตราสวัสดิการและเอนทิตีสองระดับของอัตราสวัสดิการที่เปิด  | -- | -- |

### <a name="bug-fixes"></a>การแก้ไขปัญหา

การแก้ไขปัญหาต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้

> [!NOTE]
> เป้าหมายของเราคือการส่งข้อมูลนี้ให้คุณโดยเร็วที่สุดเท่าที่จะเป็นไปได้ พวกเราอาจมีการอัปเดตในบทความนี้ เพื่อรวมการแก้ไขข้อผิดพลาดที่ทำให้เกิดข้อผิดพลาดในการสร้างหลังจากที่มีการเผยแพร่บทความนี้ในครั้งแรก

| หมายเลขปัญหา | ปัญหา |  คำอธิบาย |
| --- | --- | --- |
| 533079 | ข้อผิดพลาดการนําทาง "แบบฟอร์มถูกเรียกอย่างไม่ถูกต้อง" เมื่อเราพยายามดูการหัก | ข้อผิดพลาดคงที่ขณะดูการหักลดสวัสดิการที่มีมุมมอง **ณ วันที่** |
| 543641 | รหัสไปรษณีย์ที่ไม่ได้เติมข้อมูลในการรายงานทางอิเล็กทรอนิกส์  | แก้ไขบักภายในในรหัสไปรษณีย์ที่ไม่ปรากฏในรายงานอิเล็กทรอนิกส์ ACA เพื่อการจัดการสวัสดิการเมื่อรหัสความคุ้มครองเป็น M ถึง Q |
| 542815 | หน้าจอผู้ติดต่อส่วนบุคคลในระบบพนักงานบริการตนเองช่วยให้พนักงานสามารถดูผู้ติดต่อส่วนบุคคลของผู้อื่นได้ | ข้อผิดพลาดคงที่ที่แบบฟอร์ม **แก้ไข** ผู้ติดต่อส่วนบุคคลของระบบพนักงานบริการตนเองไม่สามารถจํากัดการสอบถามได้เพียงพอที่จะรับประกันว่ามีเพียงผู้ติดต่อส่วนบุคคลคนเดียวเท่านั้นที่จะถูกดึงข้อมูล เพื่ออนุญาตให้ผู้ใช้สามารถใช้แป้นพิมพ์ลัดเพื่อดูผู้ติดต่อของบุคคลอื่นได้ |
| 536157 | ไม่สามารถเปิดหน้า **การรวม Microsoft Dataverse** ในการดูแลระบบเนื่องจากการเรียก IsVirtualEntityPackageInled() | ปัญหาป้องกันไม่ให้ **การรวม Microsoft Dataverse** โหลดหน้าการรวมในทรัพยากรบุคคล |
| 533079 | ข้อผิดพลาดการนําทาง "แบบฟอร์มถูกเรียกอย่างไม่ถูกต้อง" เมื่อเราพยายามดูการหัก | เกิดข้อผิดพลาดคงที่ขณะอยู่ในแบบฟอร์ม **การหัก** ของสวัสดิการเมื่อดู **ณ วันที่** |
| 537264 | แท็บด่วน **ข้อมูลส่วนบุคคล** ขาดหายไปจากเรกคอร์ดผู้สมัคร | ขณะนี้ข้อมูลส่วนบุคคลของผู้สมัครจะพร้อมใช้งานในเรกคอร์ดผู้สมัคร |
| 537267 | **ประสบการณ์การทำงาน** ไม่แสดงบนเรกคอร์ดผู้สมัครภายใน | ตอนนี้แท็บด่วน **ประสบการณ์การทำงาน** แสดงบนเรกคอร์ดผู้สมัครภายใน ก่อนหน้านี้ ถ้าผู้สมัครเป็นพนักงานภายใน **ประสบการณ์การทำงาน** ถูกแทนที่ด้วย **ประวัติการจ้างงาน** ซึ่งเป็นประวัติการจ้างงานของผู้สมัครภายในองค์กร ทั้งเป็นผู้ที่เกี่ยวข้องและต้องแสดงต่อผู้สมัครภายใน |
| 537067 | **อนุญาตให้ติดต่อนายจ้าง** ไม่ได้แสดงขึ้น | การควบคุม **อนุญาตให้ติดต่อนายจ้าง** เพิ่มไปยังบานหน้าต่าง **แก้ไขประสบการณ์การทำงาน** ของเรกคอร์ดผู้สมัคร |
| 525957 | **สถานะของผู้สมัคร** ไม่ได้อัพเดตในผู้สมัครภายในเมื่อการโอนย้ายเสร็จสมบูรณ์ | เมื่อการโอนย้ายเสร็จสมบูรณ์ (มีการเลือกปุ่ม **เปลี่ยนตําแหน่ง** หรือ **ต่อเนื่อง** บนหน้า **โอนย้ายผู้ปฏิบัติงานไปที่หน้าการมอบหมายตําแหน่งงานใหม่**) **สถานะ** ของเรกคอร์ดผู้สมัครต้องเปลี่ยนเป็น **จ้างงาน** |
| 537051 | สัญลักษณ์สกุลเงินของรูปีอินเดียและไลราตุรกีไม่ได้ซิงค์ Dataverse อย่างถูกต้อง | สัญลักษณ์ของรูปีอินเดียและไลราตุรกีตอนนี้ซิงค์ Dataverse อย่างถูกต้อง |
| 534846 | ต้องเปิดใช้งานตารางการสรรหาบุคลากรเพื่อการจัดการข้อมูล | ขณะนี้ ตารางใหม่ที่สร้างไว้เพื่อคำขอการสรรหาบุคลากรและผู้สมัคร ขณะนี้เปิดใช้งานการจัดการข้อมูล อนุญาตให้เปิดใช้งานการติดตามการเปลี่ยนแปลงเป็นตาราง เปิดใช้งานการติดตามการเปลี่ยนแปลง OData ในตารางเสมือน Dataverse |
| 533474 | แก้ไขการอ้างอิงถึง Microsoft.SqlServer.X1vent.dll ขาดหายไป | ข้อยกเว้นของการโหลดแอสเซมบลีที่ Microsoft.SqlServer.XAvent.dll บล็อคตารางเสมือน Dataverse ไม่ให้ตั้งค่าในบางสภาพแวดล้อม |
| 481122 | พื้นที่ทำงาน **บุคคล** ที่แสดงตําแหน่งที่ถอน | ตําแหน่งที่ถอนแล้วถูกแสดงเป็นตําแหน่งที่เปิดในพื้นที่ทำงาน **บุคคล** ตําแหน่งที่ถอนแล้วไม่แสดงอีกต่อไป | 
| 541978 | เพิ่มที่อยู่อีเมลหลักในเอนทิตี BaseWorker | การเปลี่ยนแปลงนี้เพิ่มที่อยู่อีเมลหลักของผู้ปฏิบัติงานลงใน HcmWorkerBaseEntity |

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

ลักษณะการทำงานใหม่ต่อไปนี้อยู่ในการแสดงตัวอย่าง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดและปิดคุณลักษณะ ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)

| ลักษณะการทำงาน | แผนการรีลีส | การจัดทำเอกสาร |
| --- | --- | --- |
| แอป Human Resources ใน Microsoft Teams | [ประสบการณ์การลางานและการขาดงานของพนักงานใน Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [แอป Human Resources ใน Teams](./hr-admin-teams-leave-app.md)<br>[จัดการคำขอลางานใน Teams](hr-teams-leave-app.md) |
| การรวมกับ LinkedIn Talent Hub | [การรวมกับ LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [รวมกับ LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
| มุมมองข้ามบริษัทของการลางานสำหรับผู้จัดการ | [มุมมองข้ามบริษัทของการลางานของพนักงานสำหรับผู้จัดการ](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน](./hr-leave-and-absence-parameters.md) |
|ให้ข้อมูลเชิงลึกเพิ่มเติมในยอดดุลการลางาน| [ให้ข้อมูลเชิงลึกเพิ่มเติมในยอดดุลการลางาน](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [จัดการการลางานของพนักงาน](./hr-leave-and-absence-manage-employee-leave.md) |
| ผู้จัดการสามารถส่งคำขอสรรหาบุคลากรสำหรับตำแหน่งงาน | [ผู้จัดการสามารถส่งคำขอสรรหาบุคลากรสำหรับตำแหน่งงานที่เปิด](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [เพิ่มคำขอสรรหาบุคลากร](./hr-personnel-recruit.md#add-a-recruiting-request) |
| โพรไฟล์ผู้สมัครที่เพิ่มขึ้นในการจัดการบุคลากร | [โพรไฟล์ผู้สมัครที่เพิ่มขึ้นในการจัดการบุคลากร](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [เพิ่มหรือแก้ไขโพรไฟล์ผู้สมัคร](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| เปิดใช้งานการรวมอย่างง่ายด้วยผู้ให้การสรรหาบุคลากร | [เปิดใช้งานการรวมอย่างง่ายด้วยผู้ให้การสรรหาบุคลากร](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [สรรหาผู้สมัครงาน](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>เร็วๆ นี้
| ลักษณะการทำงาน | รายละเอียด |
| --- | --- |
| การยืนยันอีเมลการลงทะเบียนสวัสดิการ | เมื่อมีการเปิดใช้งานคุณลักษณะนี้จะมีการส่งอีเมลการยืนยันให้กับพนักงาน เมื่อพวกเขาตรวจดูจากประสบการณ์ในการลงทะเบียนสวัสดิการในการบริการตนเองของพนักงาน สำหรับข้อมูลเพิ่มเติม ให้ดู [ตั้งค่าคอนฟิกพารามิเตอร์การจัดการสวัสดิการต่อบริษัท](hr-benefits-setup-parameters-per-company.md) |
| ทักษะที่ป้อนโดยผู้จัดการของพนักงานสามารถอนุมัติโดยอัตโนมัติโดยลำดับงานได้ | เร็วๆ นี้ |

สำหรับรายการของลักษณะการทำงานที่วางแผนไว้ทั้งหมดและการเผยแพร่ตามกำหนดการของพวกเขา ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2020 เวฟ 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)

## <a name="terminology-updates-for-microsoft-dataverse"></a>การอัปเดตศัพท์ Microsoft Dataverse

มีผลบังคับใช้ พฤศจิกายน 2020 Common Data Service เปลี่ยนชื่อเป็น [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro) ดู [ประกาศอย่างเป็นทางการ](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) ของบล็อก Power Apps ในการเรียนรู้เพิ่มเติม พร้อมกับการเปลี่ยนแปลงชื่อนี้ มีการอัปเดตศัพท์ Dataverse บางอย่างแล้ว ตัวอย่างเช่น *เอนทิตี้* ตอนนี้เป็น *ตาราง* และ *ฟิลด์* ตอนนี้เป็น *คอลัมน์* สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การอัปเดตคำศัพท์](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)

ในการเผยแพร่นี้ ศัพท์ที่เกี่ยวข้องกับการรวม Dynamics 365 Human Resources ได้ถูก Dataverse อัปเดตตลอดทั้งแอปพลิเคชันเพื่อสะท้อนถึงการเปลี่ยนแปลงเหล่านี้ ตัวอย่างเช่น ขณะนี้ฟอร์ม **การรวม Common Data Service** เป็น **การรวม Microsoft Dataverse**

หากต้องการทราบเกี่ยวกับการรวม Dynamics 365 Human Resources ให้ดูที่ Microsoft Dataverse [การตั้งค่าคอนฟิกการรวม Microsoft Dataverse](./hr-admin-integration-common-data-service.md) และ [การตั้งค่าคอนฟิกตารางเสมือน Microsoft Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2020 ปล่อยเวฟ 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
