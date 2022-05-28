---
title: คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams
description: หัวข้อนี้มีข้อมูลเกี่ยวกับคำตอบสำหรับคำถามที่ถามบ่อยเกี่ยวกับการรวม Microsoft Dynamics 365 Commerce และ Microsoft Teams
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 16ad6cec0fb852d863039740e9f2c3406467e899
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692520"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams

[!include [banner](includes/banner.md)]

หัวข้อนี้มีข้อมูลเกี่ยวกับคำตอบสำหรับคำถามที่ถามบ่อยเกี่ยวกับการรวม Microsoft Dynamics 365 Commerce และ Microsoft Teams

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>ใครในร้านค้าจะกลายเป็นเจ้าของทีมงานขณะเตรียมใช้งาน Teams จาก Commerce 

ผู้จัดการร้านค้าทั้งหมดจะถูกเพิ่มเป็นเจ้าของกลุ่มทีมงานที่ตรงกันโดยอัตโนมัติ เพื่อให้สามารถดําเนินการได้ เช่น การเพิ่มช่องทางส่วนตัวและเพิ่มหรือลบสมาชิก 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>ฉันจะกําหนดบทบาท "ผู้จัดการฝ่ายสื่อสาร" ให้กับพนักงานในศูนย์ควบคุม Commerce อย่างไร 

ผู้จัดการฝ่ายการสื่อสาร Microsoft Teams สามารถสร้างและเผยแพร่รายการงานได้ พนักงานในองค์กรที่ต้องเป็นผู้จัดการการสื่อสารต้องมีบทบาทเป็น "ผู้จัดการฝ่ายงานขายปลีก" ที่มอบหมายให้กับพนักงานในศูนย์ควบคุม Commerce

เมื่อต้องการกําหนดบทบาทผู้จัดการงานขายปลีกให้กับพนักงานในศูนย์ควบคุม Commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปยัง **การขายปลีกและการค้า \> พนักงาน \> ผู้ใช้**
1. เลือกพนักงาน
1. บนแท็บด่วน **บทบาทของผู้ใช้** ให้เลือก **กำหนดบทบาท**
1. ในกล่องโต้ตอบ **กำหนดบทบาทให้กับผู้ใช้** ให้เลือกบทบาทของ **ผู้จัดการงานขายปลีก** แล้วเลือก **ตกลง**

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>ฉันจะสามารถอัพโหลดลำดับชั้นขององค์กรเป็นลำชั้นขององค์กรเฉพาะ Microsoft Teams ได้อย่างไร

ในศูนย์ควบคุม Commerce ลำดับชั้นขององค์กรทั้งหมดจะเชื่อมโยงกับวัตถุประสงค์หนึ่งวัตถุประสงค์หรือมากกว่า ตรวจสอบให้แน่ใจว่าลำดับชั้นที่คุณต้องการเตรียมใช้งาน Microsoft Teams มีวัตถุประสงค์ **การรายงานการขายปลีก** ที่เชื่อมโยงอยู่ด้วย ดังที่แสดงในรูปภาพตัวอย่างต่อไปนี้ 

![ตัวอย่างของวัตถุประสงค์ของลำดับชั้นขององค์กรในศูนย์ควบคุม Commerce](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>ฉันจะเปิดใช้งานผู้ปฏิบัติงานของร้านค้าปลีกเพื่อล็อกอินเข้าสู่การขายหน้าร้านของ Commerce (POS) โดยใช้ Azure Active Directory (Azure AD)?

หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีตั้งค่าคอนฟิกประสบการณ์การลงชื่อเข้าใช้ Commerce POS เพื่อใช้การรับรองความถูกต้อง Azure AD โปรดดูที่ [เปิดใช้งานการรับรองความถูกต้อง Azure Active Directory ของการลงชื่อเข้าใช้ POS](aad-pos-logon.md)

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>ฉันจะแม็ปร้านค้าและทีมงานที่สอดคล้องกันในศูนย์ควบคุม Commerce ได้อย่างไร ถ้าองค์กรได้สร้างทีมงานไว้แล้วใน Microsoft Teams

หากต้องการข้อมูลเกี่ยวกับวิธีการแม็ปร้านค้าและทีมงานหากมีทีมงานที่มีอยู่แล้ว โปรดดูที่ [แม็ปร้านค้าและทีมงานที่ตรงกันหากองค์กรของคุณมีทีมงานที่มีอยู่ก่อนอยู่แล้วใน Microsoft Teams](map-stores-existing-teams.md)

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>ฉันจะล้างข้อมูลโทเคน Microsoft Graph API ที่จัดเก็บไว้ในที่จัดเก็บรอบเวลาอย่างไร

ผู้ใช้ที่ลงชื่อเข้าใช้การขายหน้าร้าน (POS) ที่มีบัญชี Azure Active Directory (Azure AD) ควรลงชื่อออกจาก POS หรือปิดโปรแกรมประยุกต์เพื่อล้างข้อมูลการจัดเก็บรอบเวลา 

> [!TIP]
> แนวทางที่แนะนาคือต้องมีผู้ปฏิบัติงานของร้านค้าล็อคเทอร์มินัล POS หรือออกจากรอบเวลาเสมอเมื่อไม่ใช้เทอร์มินัล 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>เกิดอะไรขึ้นถ้าร้านค้าไม่มีผู้จัดการร้านค้า

หากร้านค้าไม่มีผู้จัดการ ระบบจะไม่สร้างกลุ่มทีมงานให้กับร้านค้าหรือใน Teams 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>เกิดอะไรขึ้นถ้าผู้จัดการร้านค้าลาออกจากบริษัท

ผู้ที่มีบทบาทเจ้าของสามารถเพิ่มผู้จัดการร้านค้าใหม่ในศูนย์ควบคุม Commerce และ Teams เตรียมใช้งานใหม่เพื่อให้ผู้จัดการใหม่มีสิทธิ์ที่จําเป็นใน Teams ของกลุ่ม 

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams](commerce-teams-integration.md)

[เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams](enable-teams-integration.md)

[สํารอง Microsoft Teams จาก Dynamics 365 Commerce](provision-teams-from-commerce.md)

[ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[จัดการบทบาทผู้ใช้ใน Microsoft Teams](manage-user-roles-teams.md)

[แม็ปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams](map-stores-existing-teams.md)
