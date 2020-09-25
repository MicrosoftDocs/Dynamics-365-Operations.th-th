---
title: แอปทรัพยากรบุคคลใน Teams
description: หัวข้อนี้จะแนะนำแอป Microsoft Dynamics 365 Human Resources ใน Microsoft Teams
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776319"
---
# <a name="human-resources-app-in-teams"></a>แอปทรัพยากรบุคคลใน Teams

[!include [banner](includes/preview-feature.md)]

แอป Microsoft Dynamics 365 Human Resources ใน Microsoft Teams ช่วยให้พนักงานสามารถขอลาหยุดและดูข้อมูลยอดการลาหยุดได้ใน Microsoft Teams ในทันที พนักงานสามารถโต้ตอบกับบอทเพื่อร้องขอข้อมูล แท็บ **การลาหยุด** แสดงข้อมูลเพิ่มเติมโดยละเอียด

![บอทของแอปการลาหยุด Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![แท็บการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>ติดตั้งและตั้งค่า

คุณสามารถค้นหาแอปพลิเคชันทรัพยากรบุคคลในร้านค้า Teams สำหรับข้อมูลเกี่ยวกับการติดตั้งแอป Teams ให้ดูที่ [การจัดการคำร้องขอการลาหยุดใน Teams](hr-teams-leave-app.md)

สำหรับข้อมูลเกี่ยวกับการจัดการสิทธิ์การได้รับอนุญาตของแอปใน Teams ให้ดูที่ [การจัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>เปิดใช้งานการแจ้งเตือนสำหรับแอป Human Resources ใน Teams

ถ้าคุณต้องการให้ผู้ใช้ได้รับการแจ้งเตือนคำขอการลางานในแอป Teams คุณต้องเปิดใช้งานการแจ้งเตือนใน Human Resources

>[!NOTE]
>เฉพาะผู้ใช้ที่ลงชื่อเข้าใช้ Teams และใช้แอป Human Resources Teams เท่านั้นที่จะได้รับการแจ้งเตือน

1. ในทรัพยากรบุคคล เลือก **การจัดการระบบ**

2. เลือก **ลิงก์**

3. ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ระบบ**

4. บนแท็บ **ทั่วไป** ตั้งค่า **เปิดใช้งานการแจ้งเตือนสำหรับแอป Teams** เป็น **ใช่**

   ![เปิดใช้งานการแจ้งเตือนแอป Teams ในพารามิเตอร์ระบบ](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. เมื่อต้องการเปิดการแจ้งเตือนของ Teams สำหรับผู้ใช้ทั้งหมด ให้เลือก **ใช่** ที่พร้อมท์

   ![เปิดใช้งานการแจ้งเตือนของ Teams สำหรับผู้ใช้ทั้งหมด](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>เปิดหรือปิดการแจ้งเตือนของ Teams สำหรับผู้ใช้แต่ละราย

หลังจากที่คุณได้เปิดใช้งานการแจ้งเตือนสำหรับแอป Human Resources Teams แล้ว คุณสามารถเปิดหรือปิดการแจ้งเตือนสำหรับผู้ใช้แต่ละรายได้

1. ในทรัพยากรบุคคล เลือก **การจัดการระบบ**

2. เลือก **ลิงก์**

3. ภายใต้ **ผู้ใช้** ให้เลือก **ตัวเลือกผู้ใช้**

4. เลือกแท็บ **ลำดับงาน**

5. ตั้งค่า **เปิดใช้งานการแจ้งเตือนสำหรับแอป Teams** เป็น **ใช่** เพื่อเปิดใช้งานการแจ้งเตือนสำหรับผู้ใช้ หรือ **ไม่** เพื่อปิดใช้งานการแจ้งเตือนสำหรับผู้ใช้

   ![เปิดใช้งานการแจ้งเตือนของแอป Teams ในแท็บลำดับงานของตัวเลือกผู้ใช้](./media/hr-admin-teams-leave-app-notifications.png)

6. เลือก **บันทึก**

## <a name="known-issues"></a>ปัญหาที่ทราบ

| ออก | สถานะ |
| --- | --- |
| การเลื่อนแนวนอนไม่ทำงานบนโทรศัพท์ Android | การเลื่อนแนวนอนไม่ใช่ปัญหาบนอุปกรณ์ iOS หรือเดสก์ท็อป เรากำลังดำเนินการแก้ไขสำหรับ Android |
| ข้อผิดพลาด: มีปัญหาในการค้นหาสภาพแวดล้อมที่จะเชื่อมต่อ | คุณอาจได้รับข้อผิดพลาดนี้ แม้ว่าคุณจะได้ตรวจสอบความถูกต้องว่าผู้ใช้สามารถเข้าถึงสภาพแวดล้อมของทรัพยากรบุคคลอย่างน้อยหนึ่งรายการ นอกจากนี้ คุณอาจไม่เห็นสภาพแวดล้อมทั้งหมดที่คุณคาดไว้ จนกว่าเราจะแก้ไขปัญหานี้ ให้ลบผู้ใช้ และจากนั้น นำเข้าอีกครั้งเพื่อแก้ไขปัญหา |
| ยอดดุลไม่ถูกต้องเมื่อส่งเวลาสำหรับวันที่ในอนาคต | การคาดการณ์ยังไม่พร้อมใช้งาน ยอดดุลปัจจุบันแสดงสำหรับวันที่ปัจจุบัน |
| ไม่สามารถยกเลิกการร้องขอ **รอการตรวจทาน** ได้ | ฟังก์ชันนี้ไม่ได้รับการสนับสนุนในขณะนี้และจะถูกเพิ่มในรุ่นต่อๆ ไป |
| มีการคำนวณข้อมูลยอดดุล ณ วันที่วันนี้ | ระบบปัจจุบันไม่แสดงยอดดุล ณ วันที่ของรอบระยะเวลาการคงค้าง ถึงแม้ว่าจะมีการตั้งค่าคอนฟิกในพารามิเตอร์การลางานและการขาดงาน |

## <a name="privacy-notice"></a>ประกาศความเป็นส่วนตัว

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

ด้วยบอท Dynamics 365 Human Resources ใน Microsoft Teams การป้อนข้อความของผู้ใช้จะได้รับการวิเคราะห์เพื่อให้เข้าใจถึงการสอบถาม/เจตนาพื้นฐาน ข้อมูลป้อนเข้าของผู้ใช้ เช่น "ค้นหาบัญชี Contoso" ถูกกำหนดเส้นทางไปยังบริการด้านความรู้ของ Microsoft อย่างใดอย่างหนึ่งที่เรียกว่า Language Understanding Intelligent Service (LUIS) อ่านเพิ่มเติมเกี่ยวกับ LUIS [ที่นี่](https://www.luis.ai/) บริการ LUIS เข้าใจหรือทำให้ความตั้งใจของข้อมูลป้อนเข้าของผู้ใช้ (ในกรณีนี้คือความตั้งใจจะค้นหาข้อมูล) และเอนทิตีเป้าหมาย (ในกรณีนี้เอนทิตีที่ตั้งใจคือบัญชีที่ชื่อ Contoso) กำกวมน้อยลง ข้อมูลนี้จะถูกส่งผ่านไปยัง [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) ของ Microsoft ซึ่งโต้ตอบกับข้อมูลจาก Dynamics 365 Human Resources และเรียกข้อมูลที่ต้องการสำหรับการสอบถามของผู้ใช้ 

โดยการติดตั้งและอนุญาตให้เข้าถึงการใช้บอท คุณตกลงที่จะอนุญาตให้บริการ LUIS และกรอบงานบอท Azure ประมวลผลเจตนาของการป้อนข้อมูลซึ่งส่งผลให้มีประสบการณ์ของผู้ใช้ในการสนทนาที่ดีขึ้น บริการ LUIS และกรอบงงานบอท Azure อาจมีระดับการปฏิบัติตามกฎระเบียบที่แตกต่างจาก Dynamics 365 Human Resources ในขณะที่บริการ LUIS มีสิทธิ์เข้าถึงเฉพาะการสอบถามของผู้ใช้และไม่ได้รับการออกแบบมาเพื่อเชื่อมต่อกับข้อมูลหรือบัญชีของผู้ใช้ Dynamics 365 Human Resources ผู้ใช้ของบอท Dynamics 365 Human Resources อาจสมัครใจป้อนการสอบถามที่มีข้อมูลลูกค้า ข้อมูลส่วนบุคคล หรือข้อมูลอื่นๆ และเนื้อหาการสอบถามดังกล่าวอาจถูกส่งไปยังบริการ LUIS และกรอบงานบอท Azure 

เนื้อหาของการสอบถามและข้อความของผู้ใช้จะถูกเก็บรักษาไว้ในระบบ LUIS เป็นเวลาสูงสุด 30 วัน จะถูกเข้ารหัสในส่วนที่เหลือ และไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ อ่านข้อมูลเพิ่มเติมเกี่ยวกับบริการขององค์ความรู้ [ที่นี่](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) 

เมื่อต้องการจัดการการตั้งค่าผู้ดูแลระบบสำหรับแอปใน Microsoft Teams ให้ไปที่ [ศูนย์การจัดการ Microsoft Teams](https://admin.teams.microsoft.com/)

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a>กริดเหตุการณ์ Microsoft Azure และ Microsoft Teams

เมื่อใช้คุณลักษณะการแจ้งเตือนสำหรับแอป Dynamics 365 Human Resources ใน Teams ข้อมูลลูกค้าบางรายจะมีการส่งออกไปภายนอกพื้นที่ทางภูมิศาสตร์ที่มีการใช้บริการ Human Resources ของผู้เช่าของคุณ Dynamics 365 Human Resources ส่งคำขอการลางานของพนักงานและรายละเอียดงานของลำดับงานไปยังกริดเหตุการณ์ Microsoft Azure และ Microsoft Teams ข้อมูลนี้อาจจัดเก็บไว้นานถึง 24 ชั่วโมงและประมวลผลในสหรัฐอเมริกา โดยมีการเข้ารหัสลับในการส่งต่อและขณะจัดเก็บ และ Microsoft หรือผู้ประมวลผลย่อยไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ

## <a name="see-also"></a>ดูเพิ่มเติมที่ 

[ดาวน์โหลดและติดตั้ง Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[ศูนย์ความช่วยเหลือ Microsoft Teams](https://support.office.com/teams)</br>
[จัดการคำขอลางานใน Teams](hr-teams-leave-app.md)

