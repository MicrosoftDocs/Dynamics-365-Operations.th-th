---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent (16 กรกฎาคม 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 for Talent
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ac0990a72224395cf109c7eb42cbb48ece2a0b4f
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795207"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-july-16-2019"></a>มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent (16 กรกฎาคม 2019)

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 for Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract
รุ่นนี้มีการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract

### <a name="coming-soon-in-attract"></a>เร็วๆ นี้ใน Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>การอนุมัติงานปรากฏในโฮมเพจ

การอนุมัติจะปรากฏในส่วน **การอนุมัติ** บนแดชบอร์ด ผู้อนุมัติสามารถตรวจทานการอนุมัติของตนภายใต้ **กำหนดให้กับคุณ** ซึ่งแสดงรหัสงาน หัวข้องาน ผู้อนุมัติอื่นๆ และวันที่ที่กำหนดงาน ผู้ใช้ที่ส่งงานให้กับการอนุมัติสามารถตรวจทานงานของตนได้ภายใต้ **ร้องขอโดยคุณ** ซึ่งแสดงผู้อนุมัติซึ่งยังคงต้องอนุมัติงานที่ส่ง

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม
รุ่นนี้มีการแก้ไขบักรองสำหรับ Dynamics 365 Talent: การเตรียมความพร้อม

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR
การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2390

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>เอนทิตี Common Data Service ที่สนับสนุนฟิลด์ที่กำหนดเองในขณะนี้

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>ไม่สามารถดูเป้าหมายและบทวิจารณ์ในระบบบริการตนเองของผู้จัดการ

การเปลี่ยนแปลงของสัปดาห์นี้ทำให้สามารถแสดงและแก้ไขเป้าหมายและบทวิจารณ์สำหรับผู้จัดการข้ามระดับในระบบบริการตนเองของผู้จัดการ

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>ไม่สามารถปิดฟอร์มเป้าหมาย หลังจากที่ผู้ใช้แก้ไขฟิลด์เป้าหมายใดๆ

รุ่นนี้แก้ไขปัญหาที่ซึ่งฟอร์มเป้าหมายไม่ได้ปิดเมื่อเลือก **ปิด**

### <a name="creating-new-goals-and-saving-displays-error"></a>การสร้างเป้าหมายใหม่และการบันทึกข้อผิดพลาดของการแสดงผล

รุ่นนี้แก้ไขปัญหา เมื่อบันทึกเป้าหมายในระบบบริการตนเองของพนักงานและผู้จัดการ

### <a name="unable-to-add-a-field-to-position-details"></a>ไม่สามารถเพิ่มฟิลด์ให้กับรายละเอียดตำแหน่ง 

ด้วยรุ่นนี้ ขณะนี้มีการสนับสนุนฟิลด์ที่กำหนดเองในรายละเอียดตำแหน่ง
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>ไม่สามารถตั้งค่าวันที่หมดอายุบนรหัสรายได้โดยใช้การจัดการข้อมูล

ขณะนี้การเปลี่ยนแปลงช่วยให้คุณสามารถกำหนดวันหมดอายุในรหัสรายได้ในการจัดการข้อมูลได้

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>ฟิลด์ที่กำหนดเองใหม่ไม่ซิงค์อย่างรวดเร็วเพียงพอ

ประสิทธิภาพของการซิงโครไนส์ฟิลด์ที่กำหนดเองไปยัง Common Data Service ได้รับการปรับปรุงด้วยการนำออกใช้ของสัปดาห์นี้

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>การส่งออกเอนทิตีไปยังงานฐานข้อมูลล้มเหลวโดยมีข้อความแสดงข้อผิดพลาด: "รูปแบบของสตริงการเริ่มต้นไม่สอดคล้องกับข้อกำหนดที่เริ่มต้นที่ดัชนี 0"

รุ่นนี้แก้ไขปัญหาที่ซึ่งชุดงานฐานข้อมูลล้มเหลว เพื่อปรับปรุงด้วยตนเอง:

1. ไปยัง **การจัดการข้อมูล**
2. เลือก **ตั้งค่าคอนฟิกการส่งออกเอนทิตีไปยังฐานข้อมูล**
3. ป้อนสตริงการเชื่อมต่อไปยังฐานข้อมูลเป้าหมายอีกครั้ง และเลือก **บันทึก**

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>การตั้งค่าคอนฟิกอีเมล SMTP ล้มเหลวโดยทันทีโดยมีข้อความแสดงข้อผิดพลาด: "เซิร์ฟเวอร์ SMTP ต้องมีการเชื่อมต่อที่ปลอดภัย หรือไคลเอนต์ไม่มีการพิสูจน์ตัวจริง"

รุ่นนี้แก้ไขการตั้งค่าคอนฟิกอีเมล SMTP ที่ล้มเหลวโดยทันที เพื่อปรับปรุงด้วยตนเอง:

1. ไปยัง **การจัดการระบบ**
2. เลือก **พารามิเตอร์อีเมล**
3. เลือก **การตั้งค่า SMTP** 
4. ป้อนชื่อผู้ใช้และรหัสผ่านที่ใช้สำหรับเซิร์ฟเวอร์ SMTP อีกครั้ง และเลือก **บันทึก**

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>มีการเปิดใช้งานคุณลักษณะการแสดงตัวอย่างเฉพาะในอินสแตนซ์ sandbox

เมื่อคุณจัดเตรียมอินสแตนซ์ใหม่ของ Talent คุณสามารถระบุได้ว่าชนิดของอินสแตนซ์เป็น **การผลิต** หรือ **Sandbox** ชนิดของอินสแตนซ์ **Sandbox** อนุญาตให้มีการทดสอบของคุณลักษณะใหม่ก่อนเวลา อินสแตนซ์ Talent ที่มีอยู่ทั้งหมดจะได้รับการปรับปรุงเป็นชนิดอินสแตนซ์ **การผลิต** ถ้าคุณต้องการให้หนึ่งในอินสแตนซ์ที่มีอยู่ของคุณได้รับการปรับปรุงเป็นชนิดของอินสแตนซ์ **Sandbox** ติดต่อ [ฝ่ายสนับสนุน](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) เพื่อเริ่มต้นการร้องขอการเปลี่ยนแปลง

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเผยแพร่การเปลี่ยนแปลง โปรดดู [เตรียมใช้งาน Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)

### <a name="restrict-leave-types-in-time-off-requests"></a>จำกัดชนิดการลางานในการร้องขอเวลาหยุดพัก

องค์กรสามารถให้ชนิดของการลางานที่แตกต่างกันหลายชนิดแก่พนักงาน อย่างไรก็ตาม อาจไม่เหมาะสมสำหรับพนักงานที่จะส่งการร้องขอเวลาหยุดพักสำหรับชนิดการลางานบางชนิด ชนิดการลางานเหล่านั้นอาจถูกจัดการโดย HR แทน ในการนำออกใช้นี้ คุณสามารถตั้งค่าคอนฟิกได้ว่าชนิดของการลางานใดที่พนักงานสามารถส่งการร้องขอเวลาหยุดพักได้ 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>ดูข้อมูลประสิทธิภาพสำหรับรายงานแบบตรงและแบบขยายในการบริการตนเองของผู้จัดการ

ตัวเลือกใหม่จะช่วยให้ผู้จัดการสามารถดูประสิทธิภาพของทั้งรายงานโดยตรงและรายงานที่ขยายของตนได้ ในปัจจุบัน ผู้จัดการรายการสามารถกำหนดและปรับปรุงเป้าหมายผลการปฏิบัติงานและออกการตรวจทานใหม่ นอกจากนี้ ผู้จัดการโดยตรงและพนักงานสามารถรักษาและปรับปรุงสมุดรายวันประสิทธิภาพ เพื่อให้มั่นใจว่ากระบวนการตรวจทานประสิทธิภาพจะทำงานได้อย่างราบรื่น เมื่อมีการใช้การเปลี่ยนแปลงนี้ ผู้จัดการจะสามารถดูและรักษาข้อมูลที่เกี่ยวข้องกับประสิทธิภาพสำหรับรายงานแบบขยายของพวกเขา นอกเหนือจากรายงานโดยตรงของพวกเขา
