---
title: จัดการคำขอลาหยุดใน Teams
description: หัวข้อนี้จะแสดงวิธีการขอลาหยุดในแอป Dynamics 365 Human Resources ใน Microsoft Teams
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b3daa76385518ad4c7150fa93ce33be0351bfd57
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428839"
---
# <a name="manage-leave-requests-in-teams"></a>จัดการคำขอลาหยุดใน Teams

[!include [banner](includes/preview-feature.md)]

แอปพลิเคชัน Microsoft Dynamics 365 Human Resources ใน Microsoft Teams ช่วยให้คุณสามารถขอลาหยุดและดูข้อมูลยอดการลาหยุดของคุณได้ใน Microsoft Teams ในทันที คุณสามารถโต้ตอบกับบอทเพื่อร้องขอข้อมูล แท็บ **การลาหยุด** แสดงข้อมูลเพิ่มเติมโดยละเอียด

## <a name="install-the-app"></a>ติดตั้งแอป

คุณสามารถค้นหาแอปพลิเคชันทรัพยากรบุคคลในร้านค้า Teams

1. ใน Microsoft Teams ให้เลือกจุดไข่ปลา

   ![จุดไข่ปลาของแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. ค้นหา Dynamics 365 Human Resources และเลือกไทล์ **ทรัพยากรบุคคล**

   ![ไทล์ HR แอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. เลือก **เพิ่ม** เพื่อติดตั้งแอป

   ![ติดตั้งแอปการลาหยุดใน Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

ถ้าแอปนั้นไม่ได้ลงชื่อเข้าใช้คุณโดยอัตโนมัติ ให้เลือกแท็บ **การตั้งค่า** เพื่อลงชื่อเข้าใช้

![แท็บการตั้งค่าแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> ถ้าคุณไม่เห็นกล่องโต้ตอบลงชื่อเข้าใช้ ให้ตรวจสอบการตั้งค่าเบราว์เซอร์ของคุณเพื่ออนุญาตป๊อปอัพ 

ถ้าคุณมีสิทธิ์เข้าถึงอินสแตนซ์ของทรัพยากรบุคคลมากกว่าหนึ่งอินสแตนซ์ คุณสามารถเลือกสภาพแวดล้อมที่คุณต้องการเชื่อมต่อในแท็บ **การตั้งค่า** ได้

> [!WARNING]
> ขณะนี้แอปพลิเคชันไม่สนับสนุนบทบาทความปลอดภัยของผู้ดูแลระบบ และจะแสดงข้อความแสดงข้อผิดพลาดถ้าคุณลงชื่อเข้าใช้ด้วยบัญชีผู้ดูแลระบบ เมื่อต้องการลงชื่อเข้าใช้ด้วยบัญชีอื่น บนแท็บ **การตั้งค่า** ให้เลือกปุ่ม **สลับบัญชี** แล้วลงชื่อเข้าใช้ด้วยบัญชีผู้ใช้ที่ไม่มีสิทธิ์ของผู้ดูแลระบบ
 
## <a name="use-the-bot"></a>ใช้บอท

หลังจากที่ติดตั้งแอปแล้ว ข้อความต้อนรับจะปรากฏขึ้นให้คุณทราบชนิดของการดำเนินการที่บอทสามารถใช้ในนามของคุณได้

![ข้อความต้อนรับของบอทในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> เมื่อมีการโต้ตอบกับบอทครั้งแรก คุณอาจจำเป็นต้องลงชื่อเข้าใช้ ถ้าคุณไม่เห็นกล่องโต้ตอบลงชื่อเข้าใช้ ให้ตรวจสอบการตั้งค่าเบราว์เซอร์ของคุณเพื่ออนุญาตป๊อปอัพ

คุณสามารถขอให้บอทไปที่:

- แสดงข้อมูลยอดการลาหยุดสำหรับชนิดการลางานแต่ละชนิดที่คุณลงทะเบียนไว้

   ![แสดงยอดดุลในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- แสดงรายละเอียดเพิ่มเติมเกี่ยวกับชนิดการลางานที่เฉพาะเจาะจง

   ![แสดงรายละเอียดแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- เริ่มต้นการร้องขอการลาหยุดสำหรับคุณ

   ![การขอลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
หลังจากที่คุณเริ่มต้นการร้องขอการลางานแล้ว คุณสามารถปรับวันที่ที่ต้องการภายในบัตรได้ หรือคุณสามารถเลือก **แก้ไขรายละเอียด** เพื่อเพิ่มข้อมูลเพิ่มเติมไปยังคำขอของคุณ

![แก้ไขคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้พิมพ์ **ส่ง** เพื่อขอการอนุมัติ นอกจากนี้คุณยังสามารถพิมพ์ **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง

![ส่งคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>จัดการคำขอลางานของคุณใน Teams

แท็บ **การลาหยุด** จะช่วยให้คุณสามารถดูสิ่งต่อไปนี้:

- ข้อมูลยอดการลาหยุดสำหรับชนิดการลางานแต่ละชนิดที่คุณลงทะเบียนไว้

- คำขอการลางานที่กำลังจะมาถึง

- คำขอลาหยุด

- ร่างคำขอลางาน

![แท็บการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>สร้างคำขอใหม่

1. หากต้องการสร้างคำขอลางานใหม่ ให้เลือก **สร้างคำขอ**

   ![สร้างคำขอในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. ป้อนวันหรือวันที่ที่คุณต้องการลางาน แล้วเลือก **เพิ่ม**

   ![เพิ่มการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. ถ้าใช้ได้ ให้ป้อนรหัสเหตุผล ป้อนข้อคิดเห็นและเพิ่มไฟล์แนบใดๆ ด้วย

4. เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้พิมพ์ **ส่ง** เพื่อขอการอนุมัติ นอกจากนี้คุณยังสามารถพิมพ์ **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง

### <a name="manage-draft-requests"></a>จัดการคำขอที่ร่าง

1. เลือกแท็บ **แบบร่าง**

   ![แท็บแบบร่างในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. เลือกดินสอเพื่อแก้ไขคำขอ หรือเลือกถังขยะเพื่อลบคำขอ

3. ทำการเปลี่ยนแปลงที่จำเป็น เมื่อคุณป้อนข้อมูลเสร็จเรียบร้อยแล้ว ให้พิมพ์ **ส่ง** เพื่อขอการอนุมัติ นอกจากนี้คุณยังสามารถเลือก **บันทึกเป็นแบบร่าง** เพื่อย้อนกลับไปได้ในภายหลัง

   ![แก้ไขแบบร่างในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a>ประกาศความเป็นส่วนตัว

ด้วยบอท Dynamics 365 Human Resources ใน Microsoft Teams การป้อนข้อความของผู้ใช้จะได้รับการวิเคราะห์เพื่อให้เข้าใจถึงการสอบถาม/เจตนาพื้นฐาน ข้อมูลป้อนเข้าของผู้ใช้ เช่น "ค้นหาบัญชี Contoso" ถูกกำหนดเส้นทางไปยังบริการด้านความรู้ของ Microsoft อย่างใดอย่างหนึ่งที่เรียกว่า Language Understanding Intelligent Service (LUIS) อ่านเพิ่มเติมเกี่ยวกับ LUIS [ที่นี่](https://www.luis.ai/) บริการ LUIS เข้าใจหรือทำให้ความตั้งใจของข้อมูลป้อนเข้าของผู้ใช้ (ในกรณีนี้คือความตั้งใจจะค้นหาข้อมูล) และเอนทิตีเป้าหมาย (ในกรณีนี้เอนทิตีที่ตั้งใจคือบัญชีที่ชื่อ Contoso) กำกวมน้อยลง ข้อมูลนี้จะถูกส่งผ่านไปยัง [กรอบงานบอท Azure](https://azure.microsoft.com/services/bot-service/) ของ Microsoft ซึ่งโต้ตอบกับข้อมูลจาก Dynamics 365 Human Resources และเรียกข้อมูลที่ต้องการสำหรับการสอบถามของผู้ใช้ 

โดยการติดตั้งและอนุญาตให้เข้าถึงการใช้บอท คุณตกลงที่จะอนุญาตให้บริการ LUIS และกรอบงานบอท Azure ประมวลผลเจตนาของการป้อนข้อมูลซึ่งส่งผลให้มีประสบการณ์ของผู้ใช้ในการสนทนาที่ดีขึ้น บริการ LUIS และกรอบงงานบอท Azure อาจมีระดับการปฏิบัติตามกฎระเบียบที่แตกต่างจาก Dynamics 365 Human Resources ในขณะที่บริการ LUIS มีสิทธิ์เข้าถึงเฉพาะการสอบถามของผู้ใช้และไม่ได้รับการออกแบบมาเพื่อเชื่อมต่อกับข้อมูลหรือบัญชีของผู้ใช้ Dynamics 365 Human Resources ผู้ใช้ของบอท Dynamics 365 Human Resources อาจสมัครใจป้อนการสอบถามที่มีข้อมูลลูกค้า ข้อมูลส่วนบุคคล หรือข้อมูลอื่นๆ และเนื้อหาการสอบถามดังกล่าวอาจถูกส่งไปยังบริการ LUIS และกรอบงานบอท Azure 

เนื้อหาของการสอบถามและข้อความของผู้ใช้จะถูกเก็บรักษาไว้ในระบบ LUIS เป็นเวลาสูงสุด 30 วัน จะถูกเข้ารหัสในส่วนที่เหลือ และไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ อ่านข้อมูลเพิ่มเติมเกี่ยวกับบริการขององค์ความรู้ [ที่นี่](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) 

เมื่อต้องการจัดการการตั้งค่าผู้ดูแลระบบสำหรับแอปใน Microsoft Teams ให้ไปที่ [ศูนย์การจัดการ Microsoft Teams](https://admin.teams.microsoft.com/) 

## <a name="see-also"></a>ดูเพิ่มเติมที่

[ดาวน์โหลดและติดตั้ง Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[ศูนย์ความช่วยเหลือ Microsoft Teams](https://support.office.com/teams)</br>
[แอป Human Resources ใน Teams](hr-admin-teams-leave-app.md)
