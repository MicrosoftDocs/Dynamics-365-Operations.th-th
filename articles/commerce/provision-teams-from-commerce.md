---
title: เตรียมใช้งาน Microsoft Teams จาก Dynamics 365 Commerce
description: หัวข้อนี้จะอธิบายวิธีการเตรียมใช้งาน Microsoft Teams โดยใช้ข้อมูลองค์กรจาก Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 96382c072e03506294d72899072a358091bda8ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842757"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>เตรียมใช้งาน Microsoft Teams จาก Dynamics 365 Commerce

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

หัวข้อนี้จะอธิบายวิธีการเตรียมใช้งาน Microsoft Teams โดยใช้ข้อมูลองค์กรจาก Dynamics 365 Commerce

Dynamics 365 Commerce เสนอวิธีที่ง่ายในการเตรียมใช้งาน Teams ถ้าคุณยังไม่ได้ตั้งค่า Teams ให้กับร้านค้าปลีกของคุณที่นั่น โดยการใช้ข้อมูลที่กําหนดไว้อย่างชัดเจนจาก Commerce ที่คุณต้องการใช้ใน Teams คุณสามารถช่วยให้พนักงานร้านค้าของคุณสามารถเริ่มต้นใช้งานใน Teams ได้ ข้อมูลนี้ประกอบด้วยลำดับชั้นขององค์กร ชื่อร้านค้า ข้อมูลพนักงาน และบัญชี Azure Active Directory (Azure AD) 

กระบวนการเตรียมใช้งาน Teams มีสองขั้นตอนหลักดังนี้

1. ใน Teams ให้สร้างทีมงานให้กับร้านค้าปลีกแต่ละร้าน และเพิ่มผู้ปฏิบัติงานของร้านค้าเป็นสมาชิกของทีมงานที่เหมาะสม ถ้าพนักงานเชื่อมโยงกับร้านค้าปลีกมากกว่าหนึ่งร้าน การเป็นสมาชิกทีมงานจะสะท้อนถึงข้อเท็จจริงนั้น ทีมการสื่อสารที่มีผู้จัดการภูมิภาคเป็นสมาชิกจะถูกสร้างขึ้นเพื่อช่วยเผยแพร่งานจาก Teams
1. อัพโหลดลำดับชั้นองค์กรของคุณจาก Commerce ไปที่ Teams

## <a name="provision-teams-in-commerce-headquarters"></a>เตรียมใช้งาน Teams ในศูนย์ควบคุม Commerce

ก่อนที่คุณจะเตรียมใช้งาน Microsoft Teams ให้จัดเตรียมงานเหล่านี้ให้เสร็จสมบูรณ์

- ยืนยันว่าผู้จัดการส่วนภูมิภาคทั้งหมดได้ยืนยันให้ผู้จัดการฝ่ายสื่อสารแล้ว
- ยืนยันว่าบัญชี Azure ของผู้จัดการร้านค้าทุกแห่งและผู้ปฏิบัติงานได้รับการเชื่อมโยงกับเรกคอร์ดผู้ปฏิบัติงานของผู้จัดการหรือผู้ปฏิบัติงานในศูนย์ควบคุม Commerce หรือไม่

เมื่อต้องการเตรียมใช้งาน Teams ในศูนย์ควบคุม Commerce ให้ทําตามขั้นตอนต่อไปนี้

1. ไปที่ **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่าคอนฟิกการรวม Microsoft Teams**
1. บนบานหน้าต่างการดำเนินการ เลือก **เตรียมใช้งาน Teams** ชุดงานที่มีชื่อว่า **การเตรียมใช้งาน Teams** จะถูกสร้างขึ้น
1. ไปที่ **การจัดการระบบ \> การสอบถาม \> ชุดงาน** และค้นหางานล่าสุดที่มีคำอธิบาย **การเตรียมใช้งาน Teams** รอจนกว่างานนี้จะเสร็จสิ้นการรัน

> [!TIP]
> หากไม่มีผู้จัดการระดับภูมิภาค ผู้จัดการร้านค้า และผู้ปฏิบัติงานร้านค้าใดเกี่ยวข้องกับลิขสิทธิ์ของ Teams คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ล้มเหลวในการดึงข้อมูลประเภท Sku ที่รับผิดชอบของผู้ใช้" เมื่อต้องการแก้ปัญหา ให้เลือก **ซิงค์ Teams และสมาชิก** ในบานหน้าต่างการการดำเนินการ

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>ตรวจสอบความถูกต้องของการเตรียมใช้งาน Teams ในศูนย์การจัดการ Teams

หากต้องการตรวจสอบความถูกต้องของการเตรียมใช้งาน Microsoft Teams ในศูนย์การจัดการ Microsoft Teams ให้ปฏิบัติตามขั้นตอนต่อไปนี้
    
1. ไปที่ [ศูนย์การจัดการ Teams](https://admin.teams.microsoft.com/)และเข้าสู่ระบบในฐานะผู้ดูแลระบบของผู้เช่า e-commerce ของคุณ
1. ในบานหน้าต่างนําทางด้านซ้าย ให้เลือก **Teams** เพื่อขยาย แล้วเลือก **จัดการ Teams**
1. ยืนยันว่ามีการสร้างทีมงานหนึ่งทีมขึ้นแล้วในร้านค้าปลีก Commerce แต่ละร้าน
1. เลือกทีมงาน และยืนยันว่ามีการเพิ่มผู้ปฏิบัติงานของร้านค้าเป็นสมาชิกแล้ว
1. ในบานหน้าต่างนําทางด้านซ้าย ให้เลือก **ผู้ใช้** และยืนยันว่าพนักงานในร้านค้าทั้งหมดในร้านค้าทั้งหมดได้เพิ่มเป็นผู้ใช้แล้ว

ตัวอย่างต่อไปนี้จะแสดงตัวอย่างของหน้า **จัดการ Teams** ในศูนย์การจัดการ Teams

![ตัวอย่างของหน้าการจัดการทีมงานในศูนย์การจัดการ Teams](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>อัพโหลดลำดับชั้นองค์กร Commerce ไปที่ Teams
    
ลำดับชั้นองค์กรของ Commerce สามารถใช้ใน Microsoft Teams เพื่อเผยแพร่งานไปยังร้านค้าทั้งหมดหรือร้านค้าที่เลือกที่ใช้โครงสร้างลำดับชั้นเดียวกัน

หากต้องการอัพโหลดลำดับชั้นองค์กรของ Commerce ไปยัง Teams ให้ทำตามขั้นตอนเหล่านี้
    
1. ในศูนย์ควบคุม Commerce ไปที่ **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่าคอนฟิกการรวม Microsoft Teams**
1. เลือก **ดาวน์โหลดลำดับชั้นเป้าหมาย** แล้วเลือก **ร้านค้าปลีกตามภูมิภาค** เพื่อดาวน์โหลดไฟล์ค่าที่แบ่งด้วยเครื่องหมายจุลภาค (CSV) ของลำดับชั้นขององค์กร
1. ติดตั้งโมดูล Microsoft Teams PowerShell โดยปฏิบัติตามขั้นตอนต่อไปนี้ใน [ติดตั้ง Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install)
1. เมื่อคุณเห็นพร้อมต์ในหน้าต่าง Teams PowerShell เข้าสู่ระบบโดยใช้บัญชีผู้ดูแลระบบของผู้เช่า Azure AD ของคุณ
1. ปฏิบัติตามขั้นตอนใน [ตั้งค่าลำดับชั้นของเป้าหมายทีมงาน](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) ของคุณเพื่ออัพโหลดไฟล์ CSV ไปยังลำดับชั้นเป้าหมาย

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>ตรวจสอบว่าอัพโหลดลำดับชั้นขององค์กรไปยัง Teamsแล้ว

หากต้องการตรวจสอบว่าอัพโหลดลำดับชั้นขององค์กรไปยัง Microsoft Teams แล้ว ให้ทำตามขั้นตอนต่อไปนี้

1. ลงชื่อเข้าใช้สู่ Teams ในฐานะผู้จัดการการสื่อสาร
1. ในบานหน้าต่างนําทางด้านซ้าย ให้เลือก **งานตามผู้วางแผน**
1. บนแท็บ **รายการที่เผยแพร่** ให้สร้างรายการใหม่ที่มีงานดัมมี
1. เลือก **เผยแพร่** ลำดับชั้นขององค์กรควรแสดงในกล่องโต้ตอบ **เลือกว่าใครจะเผยแพร่** ดังที่แสดงในตัวอย่างต่อไปนี้

![ตัวอย่างของลำดับชั้นขององค์กรในกล่องโต้ตอบ เลือกผู้ที่จะเผยแพร่ไปยัง](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams](commerce-teams-integration.md)

[เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams](enable-teams-integration.md)

[ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[จัดการบทบาทผู้ใช้ใน Microsoft Teams](manage-user-roles-teams.md)

[แม็ปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams](map-stores-existing-teams.md)

[คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams](teams-integration-faq.md)
