---
title: การเลิกใช้งานของแอป Dynamics 365 Talent - Attract และ Onboard
description: หัวข้อนี้จะอธิบายการเลิกใช้งานของแอป Dynamics 365 Talent - Attract และ Onboard
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e17b92621f05ad8483a7c578bfaece58a530df2d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692015"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>การเลิกใช้งานของแอป Dynamics 365 Talent: Attract และ Onboard


ในเดือนธันวาคม 2019 เราได้ประกาศว่าวันที่ 1 กุมภาพันธ์ 2022 จะมีการเลิกใช้งานของแอป Dynamics 365 Talent - Attract และ Onboard โดยให้เวลาแก่ลูกค้าสองปีในการวางแผน

หากต้องการข้อมูลเพิ่มเติมเกี่ยวกับการเลิกใช้งานของแอปเหล่านี้ โปรดดูที่:
 - [การเลิกใช้แอป Dynamics 365 Talent - Attract และ Dynamics 365 Talent: Onboard](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [การสร้างบุคลากรที่ประสบความสาเร็จมากขึ้นด้วย Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

เราจะให้การสนับสนุน Dynamics 365 Human Resources อย่างต่อเนื่อง ซึ่งจะช่วยให้ลูกค้าของเราได้รับข้อมูลเชิงลึกของบุคลากรเพื่อสร้างประสบการณ์ของพนักงานที่ขับเคลื่อนด้วยข้อมูลอยู่ในหลายด้าน เช่น

- ค่าตอบแทน
- สิทธิประโยชน์
- การลางานและการขาดงาน
- การปฏิบัติตาม
- Payroll
- คำติชมประสิทธิภาพการทำงาน
- การฝึกอบรมและการรับรอง
- โปรแกรมแบบบริการตนเอง

## <a name="dynamics-365-talent-apps-retirement-faq"></a>คำถามที่ถามบ่อยเกี่ยวกับการเลิกใช้งานแอป Dynamics 365 Talent

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>ประสบการณ์ของผู้ใช้สำหรับแอป Dynamics 365 Talent - Attract และ Onboard ตั้งแต่วันที่ 1 กุมภาพันธ์ 2022 จะเป็นอย่างไร

ผู้ใช้จะไม่สามารถใช้แอปพลิเคชันและระบบจะเปลี่ยนเส้นทางไปยังหน้าการเลิกใช้งาน

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>ลูกค้าสามารถส่งออกข้อมูลของแอป Dynamics 365 Talent - Attract และ Onboard ต่อหลังจากวันที่ 1 กุมภาพันธ์ 2022 ได้หรือไม่
  
ไม่มี การเลิกใช้งานมีการประกาศในเดือนธันวาคม 2019 และความสามารถในการส่งออกที่จำเป็นมีให้บริการจนถึงวันที่ 1 กุมภาพันธ์ 2022 เท่านั้น 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>ข้อมูลของลูกค้าที่เกี่ยวข้องกับทั้งแอป Dynamics 365 Talent - Attract และ Onboard และ Dataverse จะถูกลบหลังจากวันที่ 1 กุมภาพันธ์ 2022 ใช่หรือไม่

ไม่ เอนทิตี้ Dataverse จะยังคงอยู่ดังเดิมในสภาพแวดล้อม Microsoft Dataverse ของลูกค้าแม้หลังจากการเลิกใช้งาน เว้นแต่โซลูชัน Human Capital Management Talent เท่านั้นที่จะถูกลบหรือถอนการติดตั้ง

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>ฉันทราบชื่อของสภาพแวดล้อม Talent ฉันจะสามารถดูข้อมูล Attract และ Onboard ใน Dataverse ได้อย่างไร

1.  ลงชื่อเข้าใช้ Power Apps: https://make.powerapps.com
2.  เลือกสภาพแวดล้อมที่คุณต้องการดูข้อมูล Attract และ Onboard
3.  ไปที่ **Dataverse > ตาราง** 
4.  พิมพ์ “msdyn_” ใน **ค้นหา** ถ้าคุณเห็นรายการของตารางที่ขึ้นต้นด้วย "msdyn_" + ชื่อตาราง (ตัวอย่าง: msdyn_candidate) แสดงว่าคุณพบสภาพแวดล้อมที่มีข้อมูล Attract และ Onboard

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>ฉันไม่ทราบชื่อของสภาพแวดล้อม Talent ฉันจะสามารถค้นหาสภาพแวดล้อมที่มีข้อมูลแอปพลิเคชัน Dynamics 365 Talent: Attract และ Dynamics 365 Talent: Onboard ได้อย่างไร

1)  ลงชื่อเข้าใช้ศูนย์จัดการ Power Platform: https://admin.powerplatform.microsoft.com/
2)  เลือก **สภาพแวดล้อม**
3)  เลือกสภาพแวดล้อมเฉพาะที่จะประเมิน
4)  เลือก **ทรัพยากร > แอป Dynamics 365**
5)  ถ้าคุณเห็นโซลูชัน **HCM Talent** ติดตั้งอยู่ สภาพแวดล้อมนี้ควรมีข้อมูล Attract และ Onboard จัดเก็บไว้ภายใน 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> โซลูชัน **HCM Talent** ยังใช้งานใน Dynamics 365 Human Resources ได้ด้วย
