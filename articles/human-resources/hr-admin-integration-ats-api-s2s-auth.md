---
title: การรับรองความถูกต้องระหว่างเซิร์ฟเวอร์ของ API การรวม ATS
description: บทความนี้จะอธิบายวิธีการตั้งค่าการรับรองความถูกต้องระหว่างเซิร์ฟเวอร์เพื่อการรวมกับ API การรวมระบบการติดตามผู้สมัคร (ATS) ของ Dynamics 365 Human Resources
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: de3dc29c5366996276c02576eba27f7e831e4ccf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879379"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>การรับรองความถูกต้องระหว่างเซิร์ฟเวอร์ของ API การรวม ATS


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้จะอธิบายวิธีการตั้งค่าการรับรองความถูกต้องระหว่างเซิร์ฟเวอร์เพื่อการรวมใบสมัครกับ API การรวมระบบการติดตามผู้สมัคร (ATS) ของ Dynamics 365 Human Resources มีชั้นความปลอดภัยสองสามชั้นที่ต้องมีการจัดการสำหรับผู้ใช้งานบริการเพื่อเข้าถึงตารางเสมือน Microsoft Dataverse และข้อมูลที่เกี่ยวข้อง ผู้ใช้ต้องได้รับอนุญาตให้เข้าถึงตารางเสมือน Dataverse ใน Microsoft Power Platform และเข้าถึงข้อมูลใน Dynamics 365 Human Resources

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>เปิดใช้งานการเข้าถึงตารางเสมือน Dataverse ใน Power Platform

ขั้นตอนแรกที่เปิดใช้งานการเข้าถึงตารางเสมือน Dataverse ใน Power Platform คือการตั้งค่าใบสมัครของคุณใน Power Platform เพื่อการรับรองความถูกต้องกับปลายทางของตารางเสมือน Dataverse ขั้นตอนในการทำกล่าวไว้ใน [คู่มือนักพัฒนา Microsoft Dataverse](/powerapps/developer/data-platform)

  - หากต้องการลงทะเบียนแอปผู้เช่าคนเดียว: [ใช้การรับรองความถูกต้องระหว่างเซิร์ฟเวอร์ระหว่างเซิร์ฟเวอร์ของผู้เช่าเดียว](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - หากต้องการลงทะเบียนแอปผู้เช่าหลายคน: [ใช้การรับรองความถูกต้องระหว่างเซิร์ฟเวอร์ระหว่างเซิร์ฟเวอร์ของผู้เช่าหลายคน](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>การสร้างบทบาทความปลอดภัยให้กับการรวม ATS

ขั้นตอนหนึ่งหลังจากการสร้างผู้ใช้แอปพลิเคชันคือ กําหนดผู้ใช้ให้กับบทบาทความปลอดภัยที่กําหนดการเข้าถึงแอปพลิเคชันจะมีให้กับปลายทาง นี่คือขั้นตอนที่ 7 ใน [การสร้างผู้ใช้แอปพลิเคชัน](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) สำหรับการลงทะเบียนแอปผู้เช่าคนเดียว และ [สร้างบทบาทความปลอดภัยสำหรับผู้ใช้แอปพลิเคชัน](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user) สำหรับการลงทะเบียนแอปผู้เช่าหลายคน 

บทบาทที่คุณกําหนดผู้ใช้แอปพลิเคชันควรมีสิทธิ์เข้าถึงเอนทิตีข้อมูลที่ใช้เพื่อการรวม ATS ของคุณ สิ่งนี้ไม่มีอยู่สำเร็จรูป ดังนั้นจึงต้องสร้างบทบาทความปลอดภัยใหม่ บทบาทใหม่สามารถสร้างได้ตามขั้นตอนที่อธิบายไว้ใน [สร้างบทบาทความปลอดภัย](/power-platform/admin/create-edit-security-role#create-a-security-role)

สำหรับบทบาทใหม่ การเข้าถึงที่เหมาะสมต้องกําหนดให้กับเอนทิตีต่อไปนี้บนแท็บ **เอนทิตีแบบกำหนดเอง** ของบทบาทใหม่เป็นอย่างน้อย โปรดทราบว่าอาจมีเอนทิตีเพิ่มเติมที่คุณอาจต้องเพิ่ม ถ้าการรวมใช้ข้อมูลใบสมัครที่จำนวนมากขึ้น หลังจากสร้างบทบาทใหม่แล้ว จะสามารถมอบหมายบทบาทนี้ให้กับผู้ใช้แอปพลิเคชันได้

  - ผู้ปฏิบัติงานพื้นฐาน (mshr)
  - ผู้สมัครที่จะจ้างงาน (mshr)
  - ความสามารถด้านประกาศนียบัตร (mshr)
  - ชนิดของประกาศนียบัตร (mshr)
  - บริษัท
  - ฟังก์ชันงานค่าตอบแทน (mshr)
  - ชนิดงานค่าตอบแทน (mshr)
  - ประเทศ/ภูมิภาค (mshr)
  - แผนก (mshr)
  - ความสามารถด้านการศึกษา (mshr)
  - ระดับการศึกษา (mshr)
  - สาขาวิชาการศึกษา (mshr)
  - ข้อกำหนดด้านการศึกษา (mshr)
  - รหัส (mshr)
  - ชนิดข้อมูลประจำตัว (mshr)
  - สถาบัน (mshr)
  - หน่วยงานที่ออก (mshr)
  - ค่าตอบแทนงาน (mshr)
  - งาน (mshr)
  - ระดับการศึกษา (mshr)
  - ผู้ติดต่อของฝ่าย (mshr)
  - บุคคล (mshr)
  - ที่อยู่บุคคล (mshr)
  - การคัดเลือกบุคคล (mshr)
  - ชนิดของตำแหน่ง (mshr)
  - ตำแหน่ง V2 (mshr)
  - ความสามารถด้านประสบการณ์การอาชีพ (mshr)
  - ระดับการประเมิน (mshr)
  - แบบจำลองการประเมิน (mshr)
  - รหัสเหตุผล (mshr)
  - คำขอสรรหาบุคลากร (mshr)
  - ที่ตั้งของคำขอสรรหาบุคลากร (mshr)
  - ตำแหน่งของคำขอสรรหาบุคลากร (mshr)
  - ทักษะของคำขอสรรหาบุคลากร (mshr)
  - ชนิดการคัดเลือก (mshr)
  - ความสามารถด้านทักษะ (mshr)
  - ทักษะ (mshr)
  - ชื่อ (mshr)
  - สถานะทหารผ่านศึก (mshr)
  - ผู้ปฏิบัติงาน (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>การมอบสิทธิ์แอปพลิเคชันให้กับข้อมูลทรัพยากรบุคคล

ขั้นตอนที่สองคือการตรวจสอบให้แน่ใจว่าใบสมัครได้รับสิทธิที่เหมาะสมกับข้อมูลในทรัพยากรบุคคล ด้วยการเชื่อมโยงใบสมัครนั้นกับผู้ใช้ในแอปพลิเคชันทรัพยากรบุคคล สำหรับผู้ใช้แอปพลิเคชัน การเรียกใช้ระหว่างเซิร์ฟเวอร์ผ่านตารางเสมือน Dataverse จะเสร็จสิ้นในบริบทของข้อมูลเฉพาะตัวของผู้ใช้ (แอป) ใน Dataverse ที่เรียกการดำเนินการ จากนั้นบริการตัวปรับต่อตารางเสมือนจะค้นหาผู้ใช้ที่เกี่ยวข้องในทรัพยากรบุคคล และเรียกใช้การสอบถามในบริบทของผู้ใช้นั้น ซึ่งหมายความว่าต้องสร้างผู้ใช้ในทรัพยากรบุคคลด้วยบทบาทที่ถูกต้องซึ่งได้รับการมอบหมายเพื่อให้สามารถเข้าถึงข้อมูลที่การรวมใบสมัครต้องการ

นอกจากนี้ ผู้ใช้ทรัพยากรบุคคลจะต้องได้รับการมอบหมายสิทธิที่ถูกต้องให้กับข้อมูลในทรัพยากรบุคคลด้วย บทบาท **ใบสมัครการสรรหาบุคลากร** (HcmRecruitingIntegrator) จะพร้อมใช้งานพร้อมด้วยสิทธิ์ให้กับเอนทิตีหลักที่เปิดใช้งานเพื่อรวมกับข้อมูลการสรรหาบุคลากร บทบาทนี้สามารถได้รับการมอบหมายให้กับผู้ใช้แอปพลิเคชันในหน้า **ผู้ใช้** เพื่อให้สิทธิ์เข้าถึงข้อมูลที่เหมาะสม หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับบทบาทความปลอดภัยของทรัพยากรบุคคล โปรดดูที่ [ความปลอดภัยตามบทบาท](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security)

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>ตั้งค่าผู้ใช้ใหม่ที่มีสิทธิ์ที่เหมาะสม

หากต้องการตั้งค่าผู้ใช้ใหม่ที่มีสิทธิ์ที่เหมาะสม ให้ทำตามขั้นตอนต่อไปนี้

  1. เปิดหน้า **ผู้ใช้** ในทรัพยากรบุคคล และเลือก **สร้าง**
  2. ป้อน **รหัสผู้ใช้** และ **ชื่อผู้ใช้** ให้กับผู้ใช้แอปพลิเคชันใหม่ ตัวอย่างเช่น คุณสามารถป้อน "RecruitingIntegration"

      > [!NOTE]
      > หากแอปไม่มีบัญชีผู้ใช้หรือที่อยู่อีเมลของ Microsoft Azure Active Directory (Azure AD) คุณสามารถใส่บางอย่างเช่น "RecruitingApp" ในฟิลด์ที่อยู่อีเมลและผู้ให้บริการของผู้ใช้

  3. บนแท็บด่วน **บทบาทของผู้ใช้** ให้เลือกการดำเนินการ **กำหนดบทบาท**
  4. ในบานหน้าต่าง **กําหนดบทบาทให้กับผู้ใช้** ให้เลือก **ใบสมัครการสรรหาบุคลากร** และเลือก **ตกลง**
  5. บันทึกเรกคอร์ดผู้ใช้ใหม่

### <a name="link-the-new-human-resources-user-to-the-application"></a>เชื่อมโยงผู้ใช้ทรัพยากรบุคคลใหม่กับใบสมัคร

เมื่อสร้างผู้ใช้แล้ว ต้องสร้างเรกคอร์ดให้กับใบสมัครในฟอร์ม **ใบสมัคร Azure Active Directory** เพื่อเชื่อมโยงแอปนั้นกับผู้ใช้ทรัพยากรบุคคล

  1. เปิดฟอร์ม **ใบสมัคร Azure Active Directory** และเลือก **สร้าง**
  2. ในฟิลด์ **รหัสไคลเอนต์** ให้ป้อนรหัสไคลเอนต์ของผู้ใช้แอปพลิเคชันที่สร้างไว้ของใบสมัคร
  3. ในฟิลด์ **ชื่อ** ให้ป้อนชื่อของใบสมัครที่รวม
  4. ในฟิลด์ **รหัสผู้ใช้** ให้เลือกผู้ใช้ทรัพยากรบุคคลใหม่ที่สร้างขึ้นเพื่อการรวมการสรรหาบุคลากร
  5. บันทึกเรกคอร์ดใหม่

จากนั้นใบสมัครจะสามารถเข้าถึงข้อมูลทรัพยากรบุคคลได้ จํากัดเฉพาะข้อมูลที่เป็นข้อมูลเฉพาะที่ต้องใช้ในการรวมใบสมัครการสรรหาบุคลากรเท่านั้น

## <a name="see-also"></a>ดูเพิ่มเติมที่

[สรรหาผู้สมัครงาน](hr-personnel-recruit.md)<br>
[Microsoft Dataverse คืออะไร](/powerapps/maker/data-platform/data-platform-intro)<br>
[ใช้ Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)<br>
[สร้างและอัปเดตชุดตัวเลือกโดยใช้ Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
