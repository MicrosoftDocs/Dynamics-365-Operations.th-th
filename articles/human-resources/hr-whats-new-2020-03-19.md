---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (19 มีนาคม 2020)
description: บทความนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 19 มีนาคม 2020
author: andreabichsel
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f88a3a83794cc46f670143bdb97c9624cff8dd0
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694775"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-19-2020"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (19 มีนาคม 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3014 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุน Lifecycle Services (LCS) สำหรับการอ้างอิง

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>ขณะนี้ข้อจำกัดของสภาพแวดล้อมของ Human Resources จะขึ้นอยู่กับการให้สิทธิ์ใช้งานที่ปรับปรุง (394595)

ขีดจำกัดในจำนวนของสภาพแวดล้อมต่อโครงการใน Lifecycle Services (LCS) มีการเปลี่ยนแปลง ขีดจำกัดก่อนหน้านี้มีสภาพแวดล้อมสองรายการ ขีดจำกัดในจำนวนของสภาพแวดล้อมการผลิตและ sandbox ที่คุณสามารถสร้างสำหรับ Human Resources ใน LCS ในขณะนี้ขึ้นอยู่กับการให้สิทธิ์ใช้งานที่ปรับปรุง ขณะนี้คุณสามารถสร้างสภาพแวดล้อมได้มากเท่าที่จำเป็นสำหรับโครงการ LCS แต่ละโครงการ โดยขึ้นอยู่กับจำนวนของสิทธิ์การใช้งานที่ซื้อ การให้สิทธิ์การใช้งานใหม่ ที่ปรับปรุงในวันที่ 1 กุมภาพันธ์ 2020 ช่วยให้ลูกค้าสามารถซื้อสภาพแวดล้อมเพิ่มเติมได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับข้อกำหนดการให้สิทธิ์การใช้งานสำหรับสภาพแวดล้อมเพิ่มเติม ให้ดูที่ [คู่มือการใช้สิทธิ์ของ Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources)

## <a name="provide-cross-company-viewing-of-compensation-data-for-employees-and-managers-403904"></a>ให้การดูข้อมูลค่าตอบแทนระหว่างบริษัทสำหรับพนักงานและผู้จัดการ (403904)

เปิดใช้งานคุณลักษณะนี้ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** สำหรับข้อมูลเพิ่มเติม ดูที่ [เปิดใช้งานหรือปิดใช้งานคุณลักษณะการแสดงตัวอย่าง](hr-admin-manage-features.md#enable-or-disable-preview-features)

เมื่อคุณเปิดใช้งานคุณลักษณะนี้ ผู้จัดการสามารถดูค่าตอบแทนของรายงานโดยตรงและแบบขยายได้โดยไม่ต้องลงชื่อเข้าใช้ในบริษัทของการจ้างงาน ประวัติค่าตอบแทนแบบเต็มจะพร้อมใช้งานจากบริษัทที่ลงชื่อเข้าใช้ใดๆ ซึ่งผู้จัดการสามารถเข้าถึงได้ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของระบบบริการตนเองของพนักงานและผู้จัดการ](hr-employee-manager-self-service-overview.md)

## <a name="enable-global-address-book-merge-functionality-427189"></a>เปิดใช้งานฟังก์ชันผนวกของสมุดที่อยู่สากล (427189)

ขณะนี้คุณสามารถผนวกรายการสมุดที่อยู่ที่ซ้ำกันได้ โดยการเลือกเรกคอร์ดที่ซ้ำกันและการเลือก **ผนวก** จากหน้า **สมุดที่อยู่สากล**

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-the-multiple-leave-type-feature-on-419635"></a>ไม่สามารถปรับปรุงยอดดุลการลางานสำหรับแผนที่ไม่มีการค้างรับค้างจ่ายที่สร้างขึ้นโดยใช้คุณลักษณะชนิดการลางานหลายรายการบน (419635)

ขณะนี้คุณสามารถปรับปรุงยอดดุลสำหรับแผนการลางานที่สร้างขึ้นด้วยคุณลักษณะการแสดงตัวอย่าง **ชนิดของการลางานหลายรายการ** ที่ถูกเปิดใช้งานในการจัดการคุณลักษณะ

## <a name="primary-position-field-in-the-workerpositionassignmententity-when-an-employee-is-terminated-420774"></a>ฟิลด์ตำแหน่งหลักใน WorkerPositionAssignmentEntity เมื่อพนักงานถูกเลิกจ้าง (420774)

สำหรับพนักงานที่มีการจ้างงานที่สิ้นสุด ตำแหน่งหลักที่ใช้งานอยู่ในขณะที่การยกเลิกแสดงขึ้นอยู่ในเอนทิตี้ สำหรับการรวม เรกคอร์ดที่ซ้ำกันจะไม่ถูกสร้างขึ้นสำหรับการกำหนดตำแหน่งผู้ปฏิบัติงานของพนักงานอีกต่อไป 

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>ขณะนี้โซลูชัน Dataverse พร้อมใช้งาน โดยมีการเปลี่ยนแปลงต่อไปนี้:

| คำอธิบาย | เงินทอน |
| --- | --- |
| เอนทิตี **งาน/ตำแหน่ง** เปลี่ยนแปลง | <ul><li>**ภูมิภาคของค่าตอบแทน** ที่เพิ่ม</li>|
| เพิ่มเอนทิตี **มิติของตำแหน่งงาน** แล้ว | <ul><li>**มิติทางการเงิน** ที่เพิ่ม</li>
| เอนทิตี **ผู้ปฏิบัติงาน** เปลี่ยนแปลง | <ul><li>**ลำดับชื่อ** ที่เพิ่ม</li><li>เพิ่ม **การทำงานจากที่บ้าน** แล้ว</li><li>**ภาษา** ที่เพิ่ม</li><li>**วันที่ของอายุงาน** ที่เพิ่ม</li><li>**วันที่ครบรอบปี** ที่เพิ่ม</li><li>เพิ่ม **วันที่จ้างงานเดิม** แล้ว</li></ul> |
| เอนทิตี **การจ้างงาน** เปลี่ยนแปลง | <ul><li>**มิติทางการเงิน** ที่เพิ่ม</li><li>**เหตุผลการสิ้นสุดการจ้างงาน** ที่เพิ่ม</li><li>**วันที่สิ้นสุดการจ้างงาน** เปลี่ยนชื่อจาก **วันที่เปลี่ยนแปลง**</li><li>**วันที่ทดลองงาน** ที่เพิ่ม</li></ul> |
| เอนทิตี **ที่อยู่ผู้ปฏิบัติงาน** เปลี่ยนแปลง | <ul><li>**ที่อยู่ถนน** ที่เพิ่ม</li><li>**บรรทัดที่อยู่ 1** **บรรทัดที่อยู่ 2** และ **บรรทัดที่อยู่ 3** ที่ทำเครื่องหมายสำหรับค่าเสื่อมราคา</li></ul> |
| เอนทิตีการตั้งค่าค่าตอบแทนผันแปรใหม่ | <ul><li>**ชนิดแผนตัวแปรค่าตอบแทน**</li><li>**แผนค่าตอบแทนผันแปร**</li><li>**กฎสิทธิพึงได้**</li><li>**ระดับแผนตัวแปรค่าตอบแทน**</li></ul> |
| เอนทตี **การจ้างงานในปฏิทินของผู้ปฏิบัติงาน** ใหม่ | <ul><li>เพิ่ม **เอนทิตีปฏิทินงาน** แล้ว</li></ul> |
| เอนทตี **รายละเอียดตำแหน่งที่มีค่าจ้าง** ใหม่ | <ul><li>เพิ่ม **รายละเอียดตำแหน่งที่มีค่าจ้าง** แล้ว</li></ul> |
| เอนทิตี้ **ชื่อ** ใหม่ | <ul><li>เพิ่ม **ชื่อเรื่อง** แล้ว</li></ul>เอนทิตี **ชื่อเรื่อง** ใหม่จะรวมอยู่ใน Dataverse แต่ไม่ได้อ้างอิงจากเอนทิตี **ตำแหน่งงาน** หรือ **งาน** ในขณะนี้ |

> [!NOTE]
> มิติทางการเงินสำหรับทั้งตำแหน่งและการจ้างงานจะมีการรวมทิศทางเดียวสำหรับการอัปเดตจากทรัพยากรบุคคลเป็น Dataverse การอัปเดตมิติทางการเงินไม่ได้ซิงโครไนส์จาก Dataverse กับทรัพยากรบุคคลในขณะนี้

ในช่วงสองถึงสามสัปดาห์ข้างหน้า การเปลี่ยนแปลงเอนทิตีเหล่านี้จะพร้อมใช้งานในสภาพแวดล้อมทั้งหมด เมื่อต้องการติดตั้งโซลูชัน Dataverse ล่าสุดสำหรับทรัพยากรบุคคลด้วยตนเอง:

1.  ไปยัง [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)

2.  เลือก **สภาพแวดล้อม**

3.  ค้นหาสภาพแวดล้อมที่คุณต้องการอัพเกรด สภาพแวดล้อมควรตรงกับ **ชื่อสภาพแวดล้อม** ในส่วน **ข้อมูล Common Data Service** ในฟอร์ม **เกี่ยวกับ** ในทรัพยากรบุคคล

4.  เลือกสภาพแวดล้อมเพื่อดูรายละเอียดของสภาพแวดล้อม

5.  ในแถบการดำเนินการที่ส่วนบนสุด เลือก **จัดการโซลูชัน** หน้าต่างเบราเซอร์ใหม่จะเปิดขึ้นและนำทางไปยัง **ศูนย์การจัดการ Dynamics 365** ในบริบทของสภาพแวดล้อมของคุณ

6.  ในรายการ **โซลูชัน** ให้เลือก **จุดยึด Dynamics 365 Human Resources**

7.  เลือก **อัพเกรด** เพื่อใช้โซลูชันล่าสุด

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>การแสดงตัวอย่าง SharePoint ไม่ทำงานในสภาพแวดล้อมบางอย่าง

ถ้าการแสดงตัวอย่างเอกสารสำหรับเอกสารที่จัดเก็บไว้ใน SharePoint ไม่ทำงาน ให้ลองกระบวนงานต่อไปนี้:

1. ตรวจสอบความถูกต้องว่าบัญชีผู้ใช้ของผู้ดูแลระบบมีอีเมลที่เชื่อมโยงกับเรกคอร์ดผู้ใช้ คุณสามารถดูข้อมูลนี้ได้ในหน้า **ผู้ใช้** ถ้าไม่ได้ตั้งค่าอีเมล คุณจำเป็นต้องเพิ่มอีเมลและผู้ให้บริการที่มี add-in ของ OData Excel โดยค่าเริ่มต้น ที่อยู่อีเมลไม่มีอยู่ในการออกแบบ Excel คุณต้องแก้ไขการออกแบบ Excel เพิ่มฟิลด์ทั้งหมด นำไปใช้ และรีเฟรช หลังจากที่คุณดำเนินการขั้นตอนดังกล่าวเสร็จเรียบร้อยแล้ว คุณจะสามารถปรับปรุงบัญชีผู้ดูแลระบบได้

2. หลังจากที่บัญชีผู้ดูแลระบบมีบัญชีอีเมลที่เชื่อมโยง ให้ลงชื่อเข้าใช้ใน Human Resources โดยใช้ข้อมูลประจำตัวของผู้ดูแลระบบ

3. เข้าถึงเอกสารแนบใน SharePoint เพื่อเริ่มต้นการแสดงตัวอย่างเอกสาร

4. ลงชื่อเข้าใช้ด้วยบัญชีผู้ใช้อื่นที่มีสิทธิ์เข้าถึงเอกสารแนบ และตรวจสอบว่ามีการทำงานของการแสดงตัวอย่างตามที่คาดไว้

## <a name="coming-soon"></a>เร็วๆ นี้

### <a name="platform-update-33"></a>แพลตฟอร์ม update 33

- แอปแบบเต็มหน้า (การแสดงตัวอย่าง) - คุณลักษณะการแสดงตัวอย่างนี้ ซึ่งกำหนดให้คุณสามารถเปิดใช้งานคุณลักษณะมุมมองที่บันทึกไว้ จะอนุญาตให้ Power Apps และแอปของบุคคลที่สามถูกเพิ่มเป็นประสบการณ์แบบเต็มหน้าผ่านแดชบอร์ด

- มุมมองที่บันทึกไว้ (การแสดงตัวอย่าง) - คุณลักษณะการแสดงตัวอย่างนี้เปิดใช้งานมุมมองที่บันทึกไว้ ซึ่งให้การปรับปรุงที่สำคัญแก่ระบบย่อยของการตั้งค่าส่วนบุคคล คุณลักษณะนี้อนุญาตให้ผู้ใช้สามารถมีชุดที่มีการตั้งชื่อหลายชุดของการตั้งค่าส่วนบุคคลต่อหน้า นอกจากนี้ คุณยังสามารถเผยแพร่มุมมองไปยังบทบาทความปลอดภัยได้ด้วย

- ประสบการณ์การกรองข้อมูล "เป็นหนึ่งใน" ที่มีประสิทธิภาพสูงสุด - คุณลักษณะนี้เปิดใช้งานประสบการณ์การกรองข้อมูล "เป็นหนึ่งใน" ที่มีประสิทธิภาพสูงสุดที่ช่วยให้สามารถป้อนค่าตัวกรองข้อมูลหลายค่าได้ง่ายขึ้น มีกลไกที่เรียบง่ายมากขึ้นในการลบค่าตัวกรองข้อมูลแต่ละรายการหรือทั้งหมด และมีการแสดงค่าตัวกรองที่ใช้งานง่ายและขนาดกะทัดรัดมากขึ้น

- ฟิลด์ที่แนะนำ - ผู้ใช้มักต้องเพิ่มฟิลด์ในกริดหรือหน้า นี่อาจเป็นเรื่องยากโดยมีฟิลด์ที่พร้อมใช้งานจำนวนมาก แทนที่จะมีการค้นหาผ่านรายการขนาดใหญ่ คุณลักษณะนี้จะเปิดใช้งานระบบเพื่อแสดงชุดของฟิลด์ที่แนะนำ โดยขึ้นอยู่กับสิ่งที่ผู้ใช้รายอื่นเพิ่มเข้าไปมากที่สุดในสถานการณ์ที่คล้ายกัน

- การดำเนินการเริ่มต้นที่มีปัญหาในกริด - คุณลักษณะนี้ช่วยให้มั่นใจว่าการดำเนินการเริ่มต้นในกริดเชื่อมโยงกับคอลัมน์ที่ระบุในกริด โดยไม่คำนึงว่าคอลัมน์นั้นจะถูกย้ายหรือถูกซ่อนอยู่หรือไม่

## <a name="new-production-release-cadence"></a>ระยะความถี่การนำออกใช้ของการผลิตใหม่

โดยเริ่มต้นในเดือนเมษายน ระยะความถี่การนำออกใช้สำหรับ Human Resources จะเลื่อนจากการปรับปรุงรายสัปดาห์เป็นการปรับปรุงรายสองสัปดาห์ การทำเช่นนี้จะช่วยให้มั่นใจในแนวทางปฏิบัติในการใช้งานที่ปลอดภัยโดยสัมพันธ์กัน และรักษามาตรฐานระดับสูงของความมั่นคงและความน่าเชื่อถือในบริการ เรากำลังวางการทดสอบเพิ่มเติมและการตรวจสอบที่เหมาะสม เพื่อตรวจสอบการใช้งานที่สำเร็จในแต่ละขั้นตอนของกระบวนการ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับระยะความถี่การนำออกใช้ ให้ดูที่ [กระบวนการปรับปรุง](hr-admin-setup-update-process.md)

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

ตัวอย่างคุณลักษณะต่อไปนี้จะพร้อมใช้งานในวันที่ 3 กุมภาพันธ์ 2020:

- **ตัวอย่างคุณลักษณะการลางานและขาดงาน** - สำหรับข้อมูลเพิ่มเติมโปรดดู [ตัวอย่างคุณลักษณะการลางานและขาดงาน](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **ตัวอย่างคุณลักษณะการจัดการสวัสดิการ** - สำหรับข้อมูลเพิ่มเติมรวมทั้งปัญหาที่ทราบโปรดดู [ภาพรวมการจัดการสวัสดิการ](hr-benefits-management-overview.md)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]