---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources 28 มกราคม 2021
description: บทความนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 28 มกราคม 2021
author: marcelbf
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 46bbda21c3eb2b32030b93afc2a40785c22b124e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909772"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources 28 มกราคม 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายถึงคุณลักษณะใหม่ ที่มีการเปลี่ยนแปลง หรือที่กำลังจะมาถึงเร็วๆ นี้ ใน Dynamics 365 Human Resources

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการอัปเดตและกำหนดการของพวกเรา ให้ดูที่ [กระบวนการอัปเดต](hr-admin-setup-update-process.md)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลักษณะการทำงานใหม่ และวันที่ที่พร้อมใช้งานทั่วไปที่คาดไว้ ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2021 เวฟ 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)

## <a name="in-this-release"></a>ในการเผยแพร่นี้

รุ่นนี้ประกอบด้วยลักษณะการทำงานและการแก้ไขปัญหาบักใหม่ๆ ดังต่อไปนี้ การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3906

### <a name="new-features"></a>ลักษณะการทำงานใหม่ๆ

โดยทั่วไปลักษณะการทำงานต่อไปนี้จะพร้อมใช้งานกับรุ่นนี้

| ลักษณะการทำงาน | แผนการรีลีส | การจัดทำเอกสาร |
| --- | --- | --- |
| รวมรหัสเหตุผลของสวัสดิการไว้ในพื้นที่ทำงาน **การจัดการบุคลากร** | -- | [ตั้งค่ารหัสเหตุผล](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>การแก้ไขปัญหา

การแก้ไขปัญหาต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้

> [!NOTE]
> เป้าหมายของเราคือการส่งข้อมูลนี้ให้คุณโดยเร็วที่สุดเท่าที่จะเป็นไปได้ พวกเราอาจมีการอัปเดตในบทความนี้ เพื่อรวมการแก้ไขข้อผิดพลาดที่ทำให้เกิดข้อผิดพลาดในการสร้างหลังจากที่มีการเผยแพร่บทความนี้ในครั้งแรก


| หมายเลขปัญหา | ปัญหา |  คำอธิบาย |
| --- | --- | --- |
| 539456 | ปฏิทินแสดงชนิดการลางานของข้อความหนึ่ง ๆ เมื่อพารามิเตอร์ **แสดงเฉพาะการขาดงานที่ไม่มีรายละเอียด** เท่านั้นที่เปิดใช้งาน | เมื่อตัวเลือก **แสดงเฉพาะการขาดงานที่ไม่มีรายละเอียด** เปิดใช้งานวันที่ของคำขอขณะนี้แสดงขึ้นบนจอภาพ |
| 528907 | การให้สิทธิ์เข้าถึงนิติบุคคลในบทบาทพนักงานส่งผลให้ผู้จัดการไม่สามารถดูกิจกรรมยอดดุลการลางานของพนักงานในพื้นที่ **ทีมของฉัน** ของระบบพนักงานบริการตนเอง |ขณะนี้การตั้งค่าตัวเลือกนี้ช่วยให้ผู้จัดการสามารถยังคงดูดูกิจกรรมยอดดุลการลางานต่อไปได้ |
| 526280 | ข้อผิดพลาดเกี่ยวกับสิทธิ์ใน HcmWorkerEntity, HcmEmployeeEntity และ HcmContractorEntity | ผู้ใช้ในบทบาทที่ไม่ใช่ผู้ดูแลระบบไม่สามารถส่งออกเอนทิตีที่แสดงรายการเนื่องจากข้อผิดพลาดเกี่ยวกับสิทธิ์ในฟิลด์ NationalityCountryRegion ผู้ใช้จะยังคงต้องการสิทธิ์ต่อไปนี้เพื่อส่งออกข้อมูลนี้: HcmWorkerEntityMaintain, HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain และ HCMContractorEntityView |
| 542147 | ฟิลด์ **หมายเลขบัญชีธนาคาร** และ **หมายเลขการกำหนดเส้นทาง** เมื่อเพิ่มบัญชีธนาคารผ่านระบบพนักงานบริการตนเอง | เราได้แก้ไขข้อผิดพลาดที่พนักงานต้องป้อนฟิลด์ **หมายเลขบัญชีธนาคาร** และ **หมายเลขการกำหนดเส้นทาง** ขณะเพิ่มรายละเอียดบัญชีธนาคาร ฟิลด์เหล่านี้จะไม่บังคับอีกต่อไปในขณะที่บันทึกข้อมูลบัญชีธนาคารใหม่ |
| 543641 | รหัสไปรษณีย์ที่ไม่ได้เติมข้อมูลในการรายงานทางอิเล็กทรอนิกส์ | แก้ไขบักที่รหัสไปรษณีย์ไม่ได้เติมข้อมูลในรายงาน ACA เป็นรหัสความคุ้มครอง L ถึง Q |
| 545402 | เพิ่มการเปลี่ยนแปลงการเส้นทางของไฟล์ UserB csving.js เพื่อลบข้อผิดพลาด 404 | ผู้ใช้ไม่ควรเห็นข้อผิดพลาด 404 ในคอนโซลอีกต่อไป |

## <a name="in-preview"></a>ในการแสดงตัวอย่าง   

ลักษณะการทำงานใหม่ต่อไปนี้อยู่ในการแสดงตัวอย่าง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดและปิดคุณลักษณะ ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)

| ลักษณะการทำงาน | แผนการรีลีส | การจัดทำเอกสาร |
| --- | --- | --- |
| แอป Human Resources ใน Microsoft Teams | [ประสบการณ์การลางานและการขาดงานของพนักงานใน Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [แอป Human Resources ใน Teams](./hr-admin-teams-leave-app.md)<br>[จัดการคำขอลางานใน Teams](hr-teams-leave-app.md) |
| มุมมองข้ามบริษัทของการลางานสำหรับผู้จัดการ | [มุมมองข้ามบริษัทของการลางานของพนักงานสำหรับผู้จัดการ](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน](./hr-leave-and-absence-parameters.md) |

## <a name="coming-soon"></a>เร็วๆ นี้

| ลักษณะการทำงาน | รายละเอียด |
| --- | --- |
| การยืนยันอีเมลการลงทะเบียนสวัสดิการ | เมื่อมีการเปิดใช้งานคุณลักษณะนี้จะมีการส่งอีเมลการยืนยันให้กับพนักงาน เมื่อพวกเขาตรวจดูจากประสบการณ์ในการลงทะเบียนสวัสดิการในการบริการตนเองของพนักงาน คุณลักษณะนี้จะมีพร้อมใช้งานในวันที่ 1 กุมภาพันธ์ สำหรับข้อมูลเพิ่มเติม ให้ดู [ตั้งค่าคอนฟิกพารามิเตอร์การจัดการสวัสดิการต่อบริษัท](hr-benefits-setup-parameters-per-company.md) |
| ทักษะที่ป้อนโดยผู้จัดการของพนักงานสามารถอนุมัติโดยอัตโนมัติโดยลำดับงานได้ | เร็วๆ นี้ |

สำหรับรายการของลักษณะการทำงานที่วางแผนไว้ทั้งหมดและการเผยแพร่ตามกำหนดการของพวกเขา ให้ดูที่ [ภาพรวมของ Dynamics 365 Human Resources รุ่น 2021 เวฟ 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)

## <a name="terminology-updates-for-microsoft-dataverse"></a>การอัปเดตศัพท์ Microsoft Dataverse

มีผลบังคับใช้ พฤศจิกายน 2020 Common Data Service เปลี่ยนชื่อเป็น [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro) ดู [ประกาศอย่างเป็นทางการ](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) ของบล็อก Power Apps ในการเรียนรู้เพิ่มเติม พร้อมกับการเปลี่ยนแปลงชื่อนี้ มีการอัปเดตศัพท์ Dataverse บางอย่างแล้ว ตัวอย่างเช่น *เอนทิตี้* ตอนนี้เป็น *ตาราง* และ *ฟิลด์* ตอนนี้เป็น *คอลัมน์* สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การอัปเดตคำศัพท์](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)

ในการเผยแพร่นี้ ศัพท์ที่เกี่ยวข้องกับการรวม Dynamics 365 Human Resources ได้ถูก Dataverse อัปเดตตลอดทั้งแอปพลิเคชันเพื่อสะท้อนถึงการเปลี่ยนแปลงเหล่านี้ ตัวอย่างเช่น ขณะนี้ฟอร์ม **การรวม Common Data Service** เป็น **การรวม Microsoft Dataverse**

หากต้องการทราบเกี่ยวกับการรวม Dynamics 365 Human Resources ให้ดูที่ Microsoft Dataverse [การตั้งค่าคอนฟิกการรวม Microsoft Dataverse](./hr-admin-integration-common-data-service.md) และ [การตั้งค่าคอนฟิกตารางเสมือน Microsoft Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2021 ปล่อยเวฟ 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]