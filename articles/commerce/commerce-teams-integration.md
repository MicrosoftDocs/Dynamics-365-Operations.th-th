---
title: ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams
description: บทความนี้แสดงภาพรวมของการรวม Microsoft Dynamics 365 Commerce และ Microsoft Teams
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 928322c6a391510621bfebbb57d3930f91e69e24
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282915"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams

[!include [banner](includes/banner.md)]

บทความนี้แสดงภาพรวมของการรวม Microsoft Dynamics 365 Commerce และ Microsoft Teams

Dynamics 365 Commerce รวมเข้ากับ Teams เพื่อช่วยลูกค้าและปรับปรุงประสิทธิภาพของพนักงานด้วยการซิงโครไนส์การจัดการงานระหว่างแอปพลิเคชันสองตัวนั้น การจัดการงานที่ต่อเนื่องซึ่งการรวม Commerce และ Teams ช่วยให้ผู้จัดการร้านค้าและพนักงานสามารถสร้างรายการงาน กําหนดงานให้กับร้านค้าหลายร้าน และติดตามสถานะของงานในร้านค้าต่างๆ จากแอปพลิเคชันได้

การรวม Commerce และ Teams มีให้ใช้งานตั้งแต่การปล่อย Commerce รุ่น 10.0.18

## <a name="key-features"></a>คุณลักษณะสำคัญ

ต่อไปนี้เป็นคุณลักษณะการล็อคบางอย่างของคีย์ที่การรวม Commerce และ Microsoft Teams มีดังต่อไปนี้:

- เตรียมใช้งาน Teams โดยใช้ประโยชน์จากข้อมูลที่กําหนดไว้อย่างชัดเจนจาก Commerce เช่น โครงสร้างองค์กรและข้อมูลเกี่ยวกับร้านค้า ผู้ปฏิบัติงาน สิทธิการได้รับอนุญาต และบริบททางธุรกิจ
- ซิงโครไนส์การเปลี่ยนแปลงที่ต่อเนื่องได้อย่างง่ายดาย (ตัวอย่างเช่น การเพิ่มร้านค้าใหม่หรือการจ้างงานพนักงานใหม่) ระหว่าง Commerce และ Teams แต่เก็บ Commerce เป็นแหล่งข้อมูลหลักของโครงสร้างองค์กร
- รวมการจัดการงานระหว่าง Commerce และ Teams เพื่อช่วยจัดเก็บผู้ปฏิบัติงาน ผู้จัดการร้านค้า ผู้จัดการภูมิภาค และผู้จัดการฝ่ายการสื่อสารจะจัดการงานจากแอปพลิเคชันตัวใดตัวหนึ่ง

## <a name="prerequisites-for-using-integration-features"></a>เงื่อนไขเบื้องต้นของการใช้คุณลักษณะการรวม

ข้อเบื้องต้นต่อไปนี้ต้องอยู่ก่อนคุณจึงจะสามารถเริ่มใช้คุณลักษณะการรวม Microsoft Teams ได้:

- สิทธิการใช้งาน Microsoft 365 Business Standard (สิทธิการใช้นี้งานรวม Teams)
- บัญชี Azure Active Directory (Azure AD) ให้กับผู้จัดการร้านค้าและผู้ปฏิบัติงานทั้งหมด
- ระบบการขายหน้าร้าน (POS) ที่ตั้งค่าคอนฟิกด้วยการรับรองความถูกต้อง Azure AD

## <a name="conceptual-architecture"></a>สถาปัตยกรรมแนวคิด

ภาพประกอบต่อไปนี้จะแสดงสถาปัตยกรรมตามแนวคิดของการรวม Dynamics 365 Commerce และ Microsoft Teams โดยใช้ร้านค้าซานฟรานซิสโกเป็นตัวอย่าง ทั้งทีมงานและแอปพลิเคชัน Commerce POS จะใช้ Microsoft Planner เป็นที่เก็บเพื่อให้งานที่เผยแพร่จากทีมงานปรากฏในแอปพลิเคชัน POS และงานเฉพาะเฉพาะเรื่องที่สร้างขึ้นโดยผู้จัดการร้านค้าในแอปพลิเคชัน POS ปรากฏในทีมงาน ซึ่งส่งผลให้เกิดประสบการณ์การจัดการงานที่ต่อเนื่องระหว่างแอปพลิเคชันต่างๆ    

![สถาปัตยกรรมของการรวม Commerce และ Teams](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams](enable-teams-integration.md)

[สํารอง Microsoft Teams จาก Dynamics 365 Commerce](provision-teams-from-commerce.md)

[ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[จัดการบทบาทผู้ใช้ใน Microsoft Teams](manage-user-roles-teams.md)

[แมปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams](map-stores-existing-teams.md)

[คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams](teams-integration-faq.md)
