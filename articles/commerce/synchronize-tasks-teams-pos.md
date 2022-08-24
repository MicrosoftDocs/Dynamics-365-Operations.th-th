---
title: ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS
description: บทความนี้จะอธิบายวิธีการซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และการขายหน้าร้าน Dynamics 365 Commerce (POS)
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f7a26f1625ca9414a43f895ff37f697d573a36aa
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268286"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS

[!include [banner](includes/banner.md)]

บทความนี้จะอธิบายวิธีการซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และการขายหน้าร้าน Dynamics 365 Commerce (POS)

หนึ่งในวัตถุประสงค์หลักของการรวม Teams คือเพื่อเปิดใช้งานการซิงโครไนส์การจัดการงานระหว่างแอปพลิเคชัน POS และ Teams ด้วยวิธีนี้ พนักงานที่จัดเก็บสามารถใช้แอปพลิเคชัน POS หรือ Teams เพื่อจัดการงานและไม่ต้องสลับแอปพลิเคชัน

เนื่องจาก Planner ใช้เป็นที่เก็บภารกิจใน Teams จึงต้องมีการเชื่อมโยงระหว่าง Teams และ Dynamics 365 Commerce ลิงค์นี้จะสร้างขึ้นโดยใช้รหัสแผนเฉพาะสำหรับทีมงานร้านค้าที่กำหนด

ขั้นตอนต่อไปนี้แสดงวิธีการตั้งค่าการซิงโครไนส์การจัดการงานระหว่างแอปพลิเคชัน POS และ Teams

## <a name="publish-a-test-task-list-in-teams"></a>เผยแพร่รายการงานทดสอบใน Teams

ขั้นตอนต่อไปนี้สมมติว่าทีมงานร้านค้าของคุณใช้การรวมการจัดการงาน Microsoft Teams กับ Commerce เป็นครั้งแรก

หากต้องการเผยแพร่รายการงานทดสอบใน Teams ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้สู่ Teams ในฐานะผู้จัดการการสื่อสาร โดยทั่วไป ผู้จัดการการสื่อสารคือผู้ใช้ที่มีบทบาทเป็น **ผู้จัดการภูมิภาค** ใน Commerce
1. ในบานหน้าต่างนําทางด้านซ้าย ให้เลือก **งานตามผู้วางแผน**
1. บนแท็บ **รายการที่เผยแพร่** ให้เลือก **รายการใหม่** ที่ด้านล่างซ้าย และตั้งชื่อรายการงาน **รายการงานทดสอบ**
1. เลือก **สร้าง** รายการใหม่ปรากฎภายใต้ **แบบร่าง**
1. ภายใต้ **ชื่องาน** ให้ตั้งชื่องานแรก **การรวมการทดสอบ Teams** จากนั้นเลือก **ตกลง**
1. ในรายการ **แบบร่าง** ให้เลือกรายการงาน แล้วเลือก  **เผยแพร่** ในมุมด้านขวาบน
1. ในกล่องโต้ตอบ **เลือกว่าใครจะเผยแพร่** ให้เลือกทีมงานที่ควรได้รับรายการงานทดสอบ
1. เลือก **ถัดไป** เพื่อตรวจทานแผนการเผยแพร่ของคุณ ถ้าคุณต้องเปลี่ยนแปลง ให้เลือก  **ย้อนกลับ** 
1. เลือก **ยืนยันเพื่อดําเนินการต่อ** แล้วเลือก **เผยแพร่**
1. หลังจากที่การเผยแพร่เสร็จสมบูรณ์ ข้อความที่ด้านบนของแท็บ **รายการที่เผยแพร่** บ่งชี้ว่ามีการจัดส่งรายการงานของคุณเสร็จเรียบร้อยแล้วหรือไม่

สำหรับข้อมูลเพิ่มเติม ให้ดู [เผยแพร่รายการงานเพื่อสร้างและติดตามงานในองค์กรของคุณ](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df)

## <a name="link-pos-and-teams-for-task-management"></a>เชื่อมโยง POS และ Teams เพื่อการจัดการงาน

หากต้องการเชื่อมโยงแอปพลิเคชัน POS และ Microsoft Teams ของการจัดการงานใน Commerce headquarters ให้ปฏิบัติตามขั้นตอนต่อไปนี้

> [!NOTE]
> ก่อนที่คุณจะพยายามรวมการจัดการงานกับ Microsoft Teams ตรวจสอบให้แน่ใจว่าคุณได้เปิดใช้งาน [การรวม Dynamics 365 Commerce กับ Microsoft Teams](enable-teams-integration.md) 

1. ไปที่ **Retail และ Commerce \> การจัดการงาน \> การรวมงานด้วย Microsoft Teams**
1. บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**
1. ตั้งค่าตัวเลือก **เปิดใช้งานการรวมการจัดการงาน** เป็น **ใช่**
1. บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **การตั้งค่าการจัดการงาน** คุณควรได้รับการแจ้งเตือนที่บ่งชี้ว่าชุดงานที่ชื่อ **การเตรียมใช้งาน Teams** จะถูกสร้างขึ้น
1. ไปที่ **การจัดการระบบ \> การสอบถาม \> ชุดงาน** และค้นหางานล่าสุดที่มีคำอธิบาย **การเตรียมใช้งาน Teams** รอจนกว่างานนี้จะเสร็จสิ้นการรัน
1. รันงาน **CDX 1070** เพื่อเผยแพร่รหัสแผนและข้อมูลอ้างอิงร้านค้าไปยังเซิร์ฟเวอร์ Retail

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams](commerce-teams-integration.md)

[เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams](enable-teams-integration.md)

[สํารอง Microsoft Teams จาก Dynamics 365 Commerce](provision-teams-from-commerce.md)

[จัดการบทบาทผู้ใช้ใน Microsoft Teams](manage-user-roles-teams.md)

[แมปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams](map-stores-existing-teams.md)

[คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams](teams-integration-faq.md)
