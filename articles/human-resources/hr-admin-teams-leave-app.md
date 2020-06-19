---
title: แอปทรัพยากรบุคคลใน Teams
description: หัวข้อนี้จะแนะนำแอป Microsoft Dynamics 365 Human Resources ใน Microsoft Teams
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.openlocfilehash: 36684710e39c27840cc4aaa259a85579104fd8d6
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431141"
---
# <a name="human-resources-app-in-teams"></a>แอปทรัพยากรบุคคลใน Teams

[!include [banner](includes/preview-feature.md)]

แอป Microsoft Dynamics 365 Human Resources ใน Microsoft Teams ช่วยให้พนักงานสามารถขอลาหยุดและดูข้อมูลยอดการลาหยุดได้ใน Microsoft Teams ในทันที พนักงานสามารถโต้ตอบกับบอทเพื่อร้องขอข้อมูล แท็บ **การลาหยุด** แสดงข้อมูลเพิ่มเติมโดยละเอียด

![บอทของแอปการลาหยุด Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![แท็บการลาหยุดในแอปการลาหยุด Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>ติดตั้งและตั้งค่า

คุณสามารถค้นหาแอปพลิเคชันทรัพยากรบุคคลในร้านค้า Teams สำหรับข้อมูลเกี่ยวกับการติดตั้งแอป Teams ให้ดูที่ [การจัดการคำร้องขอการลาหยุดใน Teams](hr-teams-leave-app.md)

สำหรับข้อมูลเกี่ยวกับการจัดการสิทธิ์การได้รับอนุญาตของแอปใน Teams ให้ดูที่ [การจัดการนโยบายสิทธิ์ของแอปใน Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)

## <a name="known-issues"></a>ปัญหาที่ทราบ

| ออก | สถานะ |
| --- | --- |
| ข้อผิดพลาด: มีปัญหาในการค้นหาสภาพแวดล้อมที่จะเชื่อมต่อ | คุณอาจได้รับข้อผิดพลาดนี้ แม้ว่าคุณจะได้ตรวจสอบความถูกต้องว่าผู้ใช้สามารถเข้าถึงสภาพแวดล้อมของทรัพยากรบุคคลอย่างน้อยหนึ่งรายการ นอกจากนี้ คุณอาจไม่เห็นสภาพแวดล้อมทั้งหมดที่คุณคาดไว้ จนกว่าเราจะแก้ไขปัญหานี้ ให้ลบผู้ใช้ และจากนั้น นำเข้าอีกครั้งเพื่อแก้ไขปัญหา |
| ยอดดุลไม่ถูกต้องเมื่อส่งเวลาสำหรับวันที่ในอนาคต | การคาดการณ์ยังไม่พร้อมใช้งาน ยอดดุลปัจจุบันแสดงสำหรับวันที่ปัจจุบัน |
| เมื่อลดจำนวนชั่วโมงที่ใช้ในการร้องขอที่มีอยู่ **ยอดดุลคงเหลือจะถูก** จะลดลงแทนที่จะเพิ่มขึ้น | เราจะจัดการปัญหาที่ทราบนี้ในอนาคต การแสดงผลไม่ถูกต้องแต่มีการปรับปรุงยอดที่ถูกต้องเมื่อทำการส่ง |
| บัตร **การลาหยุดที่กำลังจะมาถึง** 2 ใบแสดงวันที่เดียวกัน | บัตรแสดงถึงการส่งทีละรายการ เราจะนำคำติชมไปใช้แและทำการปรับปรุงต่อไป |
| ไม่สามารถยกเลิกการร้องขอ **รอการตรวจทาน** ได้ | ฟังก์ชันนี้ไม่ได้รับการสนับสนุนในขณะนี้และจะถูกเพิ่มในรุ่นต่อๆ ไป |
| มีการคำนวณข้อมูลยอดดุล ณ วันที่วันนี้ | ระบบปัจจุบันไม่แสดงยอดดุล ณ วันที่ของรอบระยะเวลาการคงค้าง ถึงแม้ว่าจะมีการตั้งค่าคอนฟิกในพารามิเตอร์การลางานและการขาดงาน |

## <a name="privacy-notice"></a>ประกาศความเป็นส่วนตัว

ด้วยบอท Dynamics 365 Human Resources ใน Microsoft Teams การป้อนข้อความของผู้ใช้จะได้รับการวิเคราะห์เพื่อให้เข้าใจถึงการสอบถาม/เจตนาพื้นฐาน ข้อมูลป้อนเข้าของผู้ใช้ เช่น "ค้นหาบัญชี Contoso" ถูกกำหนดเส้นทางไปยังบริการด้านความรู้ของ Microsoft อย่างใดอย่างหนึ่งที่เรียกว่า Language Understanding Intelligent Service (LUIS) อ่านเพิ่มเติมเกี่ยวกับ LUIS [ที่นี่](https://www.luis.ai/) บริการ LUIS เข้าใจหรือทำให้ความตั้งใจของข้อมูลป้อนเข้าของผู้ใช้ (ในกรณีนี้คือความตั้งใจจะค้นหาข้อมูล) และเอนทิตีเป้าหมาย (ในกรณีนี้เอนทิตีที่ตั้งใจคือบัญชีที่ชื่อ Contoso) กำกวมน้อยลง ข้อมูลนี้จะถูกส่งผ่านไปยัง [กรอบงานบอท Azure](https://azure.microsoft.com/services/bot-service/) ของ Microsoft ซึ่งโต้ตอบกับข้อมูลจาก Dynamics 365 Human Resources และเรียกข้อมูลที่ต้องการสำหรับการสอบถามของผู้ใช้ 

โดยการติดตั้งและอนุญาตให้เข้าถึงการใช้บอท คุณตกลงที่จะอนุญาตให้บริการ LUIS และกรอบงานบอท Azure ประมวลผลเจตนาของการป้อนข้อมูลซึ่งส่งผลให้มีประสบการณ์ของผู้ใช้ในการสนทนาที่ดีขึ้น บริการ LUIS และกรอบงงานบอท Azure อาจมีระดับการปฏิบัติตามกฎระเบียบที่แตกต่างจาก Dynamics 365 Human Resources ในขณะที่บริการ LUIS มีสิทธิ์เข้าถึงเฉพาะการสอบถามของผู้ใช้และไม่ได้รับการออกแบบมาเพื่อเชื่อมต่อกับข้อมูลหรือบัญชีของผู้ใช้ Dynamics 365 Human Resources ผู้ใช้ของบอท Dynamics 365 Human Resources อาจสมัครใจป้อนการสอบถามที่มีข้อมูลลูกค้า ข้อมูลส่วนบุคคล หรือข้อมูลอื่นๆ และเนื้อหาการสอบถามดังกล่าวอาจถูกส่งไปยังบริการ LUIS และกรอบงานบอท Azure 

เนื้อหาของการสอบถามและข้อความของผู้ใช้จะถูกเก็บรักษาไว้ในระบบ LUIS เป็นเวลาสูงสุด 30 วัน จะถูกเข้ารหัสในส่วนที่เหลือ และไม่ได้ใช้สำหรับการฝึกอบรมหรือการปรับปรุงบริการ อ่านข้อมูลเพิ่มเติมเกี่ยวกับบริการขององค์ความรู้ [ที่นี่](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) 

เมื่อต้องการจัดการการตั้งค่าผู้ดูแลระบบสำหรับแอปใน Microsoft Teams ให้ไปที่ [ศูนย์การจัดการ Microsoft Teams](https://admin.teams.microsoft.com/) 

## <a name="see-also"></a>ดูเพิ่มเติมที่ 

[ดาวน์โหลดและติดตั้ง Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[ศูนย์ความช่วยเหลือ Microsoft Teams](https://support.office.com/teams)</br>
[จัดการคำขอลางานใน Teams](hr-teams-leave-app.md)

