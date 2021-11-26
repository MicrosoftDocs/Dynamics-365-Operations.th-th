---
title: แอปทรัพยากรบุคคลใน Teams
description: หัวข้อนี้จะแนะนำแอป Microsoft Dynamics 365 Human Resources ใน Microsoft Teams
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5e44b9fa40971710d8316c055c4d2ac51f9ab266
ms.sourcegitcommit: 7e0e2a266d9a9473df72e207554d9bd150e17ce3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/05/2021
ms.locfileid: "7771518"
---
# <a name="human-resources-app-in-teams"></a>แอปทรัพยากรบุคคลใน Teams

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

แอป Microsoft Dynamics 365 Human Resources ใน Microsoft Teams จะช่วยให้พนักงานสามารถขอลาหยุดและดูข้อมูลการลาหยุดใน Microsoft Teams ได้ในทันที พนักงานสามารถโต้ตอบกับบอทเพื่อร้องขอข้อมูล แท็บ **การลาหยุด** แสดงข้อมูลเพิ่มเติมโดยละเอียด นอกจากนี้ พวหเขายังสามารถส่งข้อมูลเกี่ยวกับการลางานที่กำลังจะเกิดขึ้นของคุณในทีมและการสนทนาภายนอกแอปพลิเคชันทรัพยากรบุคคลได้

![บอทของแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot.png)

![แท็บการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![ใบร้องขอการลางานของทรัพยากรบุคคล](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>ติดตั้งและตั้งค่า

คุณสามารถค้นหาแอป Dynamics 365 Human Resources ในร้านค้า Teams สำหรับข้อมูลเกี่ยวกับการติดตั้งแอป Teams ให้ดูที่ [การจัดการคำร้องขอการลาหยุดใน Teams](hr-teams-leave-app.md)

สำหรับข้อมูลเกี่ยวกับการจัดการสิทธิ์การได้รับอนุญาตของแอปใน Teams ให้ดูที่ [การจัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies)

หากคุณต้องการให้ผู้ใช้ของคุณดูปฏิทินการลางานและการขาดงานในแอป คุณจะต้องเปิดใช้งาน **ปฏิทินการลางานและการขาดงานใน Teams** ในการจัดการคุณลักษณะ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานคุณลักษณะ ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>เปิดใช้งานการแจ้งเตือนสำหรับแอป Human Resources ใน Teams

ถ้าคุณต้องการให้ผู้ใช้ได้รับการแจ้งเตือนคำขอการลางานในแอป Teams คุณต้องเปิดใช้งานการแจ้งเตือนใน Dynamics 365 Human Resources

>[!NOTE]
>เฉพาะผู้ใช้ที่ลงชื่อเข้าใช้ Teams และใช้แอป Dynamics 365 Human Resources Teams เท่านั้นที่จะได้รับการแจ้งเตือน

1. ในทรัพยากรบุคคล เลือก **การจัดการระบบ**

2. เลือก **ลิงก์**

3. ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ระบบ**

4. บนแท็บ **ทั่วไป** ตั้งค่า **เปิดใช้งานการแจ้งเตือนสำหรับแอป Teams** เป็น **ใช่**

   ![เปิดใช้งานการแจ้งเตือนแอป Teams ในพารามิเตอร์ระบบ](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. เมื่อต้องการเปิดการแจ้งเตือนของ Teams สำหรับผู้ใช้ทั้งหมด ให้เลือก **ใช่** ที่พร้อมท์

   ![เปิดใช้งานการแจ้งเตือนของ Teams สำหรับผู้ใช้ทั้งหมด](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>เปิดหรือปิดการแจ้งเตือนของ Teams สำหรับผู้ใช้แต่ละราย

หลังจากที่คุณได้เปิดใช้งานการแจ้งเตือนสำหรับแอป Dynamics 365 Human Resources Teams แล้ว คุณสามารถเปิดหรือปิดการแจ้งเตือนสำหรับผู้ใช้แต่ละรายได้

1. ในทรัพยากรบุคคล เลือก **การจัดการระบบ**

2. เลือก **ลิงก์**

3. ภายใต้ **ผู้ใช้** ให้เลือก **ตัวเลือกผู้ใช้**

4. เลือกแท็บ **ลำดับงาน**

5. ตั้งค่า **เปิดใช้งานการแจ้งเตือนสำหรับแอป Teams** เป็น **ใช่** เพื่อเปิดใช้งานการแจ้งเตือนสำหรับผู้ใช้ หรือ **ไม่** เพื่อปิดใช้งานการแจ้งเตือนสำหรับผู้ใช้

   ![เปิดใช้งานการแจ้งเตือนของแอป Teams ในแท็บลำดับงานของตัวเลือกผู้ใช้](./media/hr-admin-teams-leave-app-notifications.png)

6. เลือก **บันทึก**

## <a name="supported-languages"></a>ภาษาที่สนับสนุน

แอป Dynamics 365 Human Resources ใน Teams สนับสนุนภาษาต่อไปนี้:

| รหัสภาษา | ภาษา |
| --- | --- |
| de-DE | ภาษาเยอรมัน (เยอรมนี) |
| es-ES | ภาษาสเปน (สเปน) |
| es-MX | ภาษาสเปน (เม็กซิโก) |
| fr-CA | ภาษาฝรั่งเศส (แคนาดา) |
| fr-FR | ภาษาฝรั่งเศส (ฝรั่งเศส) |
| it-IT | ภาษาอิตาลี (อิตาลี) |
| nl-NL | ภาษาดัตช์ (เนเธอร์แลนด์) |
| pt-BR | ภาษาโปรตุเกส (บราซิล) |
| tr-TR | ภาษาตุรกี (ตุรกี) |
| zh-CN | จีน (ประยุกต์) |

## <a name="notes"></a>บันทึกย่อ

รายการงานต่อไปนี้ถูกเลื่อนออกใช้ในอนาคต:

| รายการงาน | สถานะ |
| --- | --- |
| ยอดดุลไม่ถูกต้องเมื่อส่งเวลาสำหรับวันที่ในอนาคต | การคาดการณ์ยังไม่พร้อมใช้งาน ยอดดุลปัจจุบันแสดงสำหรับวันที่ปัจจุบัน |
| ไม่สามารถยกเลิกการร้องขอ **รอการตรวจทาน** ได้ | ฟังก์ชันนี้ไม่ได้รับการสนับสนุนในขณะนี้และจะถูกเพิ่มในรุ่นต่อๆ ไป |
| มีการคำนวณข้อมูลยอดดุล ณ วันที่วันนี้ | ระบบปัจจุบันไม่แสดงยอดดุล ณ วันที่ของรอบระยะเวลาการคงค้าง ถึงแม้ว่าจะมีการตั้งค่าคอนฟิกในหน้า **พารามิเตอร์การลางานและการขาดงาน** |

## <a name="troubleshooting"></a>การแก้ไขปัญหา

ถ้าผู้ใช้กำลังมีปัญหาในการเข้าสู่ระบบ หรือใช้แอป Human Resources Teams ให้ลองปฏิบัติตามคำแนะนำในการแก้ไขปัญหาเหล่านี้ ถ้าคุณยังคงมีปัญหาหลังการแก้ไขปัญหา โปรดติดต่อฝ่ายสนับสนุน สำหรับข้อมูลเพิ่มเติม ดู [รับการสนับสนุน](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>ไม่สามารถเข้าสู่ระบบแอป Human Resources ใน Teams

หากผู้ใช้ติดต่อคุณ เนื่องจากไม่สามารถเข้าสู่ระบบแอปได้ ให้ตรวจสอบว่าผู้ใช้มีเรกคอร์ดพนักงานที่เกี่ยวข้องใน Human Resources

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>เกิดข้อผิดพลาดขณะอนุมัติคำขอการลางานในแอป Human Resources ใน Teams

หากผู้ใช้ได้รับข้อผิดพลาดขณะพยายามอนุมัติคำขอการลางานในแอป Teams ให้ทำตามขั้นตอนการแก้ไขปัญหาต่อไปนี้:

1. ตรวจสอบว่าบัญชี Teams ของพวกเขาเป็นอันเดียวกับที่ใช้สำหรับการเข้าถึง Human Resources

2. ตรวจสอบว่าพวกเขาเป็นผู้อนุมัติที่ถูกต้องสำหรับคำขอดังกล่าว โดยตรวจสอบการตั้งค่าลำดับงานสำหรับการอนุมัติการลางาน สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลำดับงานคำขอลางาน ดูที่ [สร้างลำดับงานคำขอลางาน](hr-leave-and-absence-workflow.md)

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>ปล่อยให้ผู้อนุมัติไม่ได้รับข้อความสนทนาของ Teams ในการอนุมัติคำขอลางาน

1. ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการแจ้งเตือนสำหรับสภาพแวดล้อมและผู้ใช้ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เปิดใช้งานการแจ้งเตือนสำหรับแอป Human Resources ใน Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) และ [เปิดหรือปิดการแจ้งเตือน Teams สำหรับผู้ใช้แต่ละราย](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users)

2. ตรวจสอบให้แน่ใจว่าผู้ใช้ลงชื่อเข้าใช้แท็บ **การสนทนา** โดยใช้ข้อมูลส่วนบุคคลเดียวกับที่ผู้ใช้ใช้ในการอนุมัติคำขอลางาน ใช้ข้อความ "ลงชื่อออก" แล้ว "ลงชื่อเข้าใช้" เพื่อลงชื่อเข้าใช้ด้วยข้อมูลส่วนบุคคลที่ถูกต้อง

3. หากปัญหายังคงอยู่ ให้ตรวจสอบสถานะของชุดงาน **ระบบเหตุการณ์ทางธุรกิจ** ในฐานะผู้ดูแลระบบ ถ้าอยู่ในขั้นตอน **กำลังรอ** หรือ **กำลังปฏิบัติการ** ให้ตรวจสอบอีกครั้งในอีกสองสามนาที หากสถานะยังคงไม่เปลี่ยนแปลง ให้บันทึกตั๋วการสนับสนุน เพื่อให้ทีมงานของเราสามารถแก้ไขปัญหาได้

## <a name="privacy-notice"></a>ประกาศความเป็นส่วนตัว

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

ด้วยบอท Dynamics 365 Human Resources ใน Microsoft Teams การป้อนข้อความของผู้ใช้จะได้รับการวิเคราะห์เพื่อให้เข้าใจถึงการสอบถาม/เจตนาพื้นฐาน ข้อมูลป้อนเข้าของผู้ใช้ เช่น "ค้นหาบัญชี Contoso" จะถูกวางในหนึ่งในบริการของ Microsoft's Cognitive Service ที่เรียกว่า Language Understanding Intelligent Service (LUIS) อ่านเพิ่มเติมเกี่ยวกับ LUIS [ที่นี่](https://www.luis.ai/) บริการ LUIS เข้าใจหรือทำให้ความตั้งใจของข้อมูลป้อนเข้าของผู้ใช้ (ในกรณีนี้คือความตั้งใจจะค้นหาข้อมูล) และเอนทิตีเป้าหมาย (ในกรณีนี้เอนทิตีที่ตั้งใจคือบัญชีที่ชื่อ Contoso) กำกวมน้อยลง ข้อมูลนี้จะถูกส่งผ่านไปยัง [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) ของ Microsoft ซึ่งโต้ตอบกับข้อมูลจาก Dynamics 365 Human Resources และเรียกข้อมูลที่ต้องการสำหรับการสอบถามของผู้ใช้

โดยการติดตั้งและอนุญาตให้เข้าถึงการใช้บอท คุณตกลงที่จะอนุญาตให้บริการ LUIS และกรอบงานบอท Azure ประมวลผลเจตนาของการป้อนข้อมูลซึ่งส่งผลให้มีประสบการณ์ของผู้ใช้ในการสนทนาที่ดีขึ้น บริการ LUIS และกรอบงงานบอท Azure อาจมีระดับการปฏิบัติตามกฎระเบียบที่แตกต่างจาก Dynamics 365 Human Resources ขณะที่บริการ LUIS มีสิทธิ์เข้าถึงเฉพาะการสอบถามของผู้ใช้และไม่ได้รับการออกแบบมาเพื่อเชื่อมต่อกับข้อมูลหรือบัญชีของผู้ใช้ Dynamics 365 Human Resources ผู้ใช้ของบอท Dynamics 365 Human Resources อาจสมัครใจป้อนการสอบถามที่มีข้อมูลลูกค้า ข้อมูลส่วนบุคคล หรือข้อมูลอื่นๆ และเนื้อหาการสอบถามดังกล่าวอาจถูกส่งไปยังบริการ LUIS และ Azure Bot Framework 

เนื้อหาของการสอบถามและข้อความของผู้ใช้จะถูกเก็บรักษาไว้ในระบบ LUIS เป็นเวลาสูงสุด 30 วัน จะถูกเข้ารหัสในส่วนที่เหลือ และไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ อ่านข้อมูลเพิ่มเติมเกี่ยวกับบริการขององค์ความรู้ [ที่นี่](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) 

เมื่อต้องการจัดการการตั้งค่าผู้ดูแลระบบสำหรับแอปใน Microsoft Teams ให้ไปที่ [ศูนย์การจัดการ Microsoft Teams](https://admin.teams.microsoft.com/)

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, กริดเหตุการณ์ Azure และ Azure Cosmos DB

เมื่อใช้แอป Dynamics 365 Human Resources ใน Microsoft Teams ข้อมูลลูกค้าบางรายอาจส่งออกไปภายนอกพื้นที่ทางภูมิศาสตร์ที่ผู้เช่าของคุณมีการใช้บริการ Human Resources

Dynamics 365 Human Resources จะส่งคำขอการลางานของพนักงานและรายละเอียดงานของลำดับงานไปยัง Event Grid Microsoft Azure และ Microsoft Teams ข้อมูลนี้อาจจัดเก็บไว้ในกริดเหตุการณ์ Microsoft Azure นานถึง 24 ชั่วโมงและจะประมวลผลในสหรัฐอเมริกา โดยมีการเข้ารหัสลับในการส่งต่อและขณะจัดเก็บ และ Microsoft หรือผู้ประมวลผลย่อยไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)

ในขณะที่สนทนากับบอทแชทในแอปทรัพยากรบุคคล เนื้อหาการสนทนาอาจจัดเก็บไว้ใน Azure Cosmos DB และส่งผ่านไปยัง Microsoft Teams ข้อมูลนี้อาจจัดเก็บไว้ใน Azure Cosmos DB ได้สูงสุด24ชั่วโมงและอาจได้รับการประมวลผลภายนอกภูมิภาคทางภูมิศาสตร์ที่มีการปรับใช้บริการทรัพยากรบุคคลของผู้เช่าของคุณจะถูกเข้ารหัสในการส่งต่อและในส่วนที่เหลือและไม่ได้ใช้โดย Microsoft หรือผู้ประมวลผลย่อยสำหรับการฝึกอบรมหรือการให้ปรับปรุงการบริการ เมื่อต้องการเข้าใจว่าข้อมูลของคุณจัดเก็บอยู่ใน Teams อย่างไร โปรดดูที่: [ตำแหน่งของข้อมูลใน Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)
 
เมื่อต้องการจำกัดการเข้าถึงแอปพลิเคชันทรัพยากรบุคคลใน Microsoft Teams สำหรับองค์กรหรือผู้ใช้ภายในองค์กรของคุณ ให้ดูที่ [จัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies)

## <a name="see-also"></a>ดูเพิ่มเติมที่ 

[ดาวน์โหลดและติดตั้ง Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[ศูนย์ความช่วยเหลือ Microsoft Teams](https://support.office.com/teams)</br>
[จัดการคำขอลางานใน Teams](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
