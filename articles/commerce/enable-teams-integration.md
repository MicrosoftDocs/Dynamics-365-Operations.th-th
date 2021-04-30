---
title: เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams
description: หัวข้อนี้อธิบายวิธีการเปิดใช้งานการรวม Microsoft Dynamics 365 Commerce และ Microsoft Teams
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
ms.openlocfilehash: c4d596f27ffe15a97dc04e2ce7e85d21f8e7161f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908406"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีการเปิดใช้งานการรวม Microsoft Dynamics 365 Commerce และ Microsoft Teams

เมื่อต้องการเตรียมใช้งาน Teams ด้วยข้อมูลจาก Dynamics 365 Commerce และซิงโครไนส์ลักษณะการงานการจัดการงานระหว่าง Teams และโปรแกรมประยุกต์การขายหน้าร้าน (POS) คุณต้องเปิดใช้งานคุณลักษณะการรวมในศูนย์ควบคุม Commerce

> [!NOTE]
> เมื่อคุณเปิดใช้งานการรวม Teams คุณยินยอมให้แบ่งปันข้อมูลของคุณกับ Teams ข้อมูลที่ใช้ร่วมกันกับ Teams อาจอยู่ในประเทศอื่นที่แตกต่างจากข้อมูล Commerce ของคุณ และอาจขึ้นอยู่กับมาตรฐานการปฏิบัติตามกฎระเบียบที่แตกต่างกัน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ศูนย์ความเชื่อถือของ Microsoft](https://www.microsoft.com/trust-center) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับนโยบายสิทธิส่วนบุคคลของ Microsoft โปรดดูที่ [รายงานสิทธิส่วนบุคคลของ Microsoft](https://aka.ms/privacy)

## <a name="enable-teams-integration"></a>เปิดใช้งานการรวม Teams

ก่อนที่คุณจะสามารถเปิดใช้งานการรวม Microsoft Teams กับ Commerce ได้ คุณต้องลงทะเบียนโปรแกรมประยุกต์ Teams กับผู้เช่าของคุณในพอร์ทัล Azure ก่อน

หากต้องการลงทะเบียนโปรแกรมประยุกต์ Teams กับผู้เช่าในพอร์ทัล Azure ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ปฏิบัติตามขั้นตอนใน [เริ่มต้นใช้งานด่วน: ลงทะเบียนแอปในแพลตฟอร์มเอกลักษณ์ Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) เพื่อลงทะเบียนโปรแกรมประยุกต์ Teams กับผู้เช่าในพอร์ทัล Azure
1. คัดลอก **ค่ารหัสโปรแกรมประยุกต์ (ไคลเอนต์)** จากหน้า **ภาพรวม** ของแอปที่ลงทะเบียน คุณจะใช้ค่านี้เปิดใช้งานการรวม Teams ในศูนย์ควบคุม Commerce
1. คัดลอกค่าใบรับรองที่ป้อนเมื่อคุณ [เพิ่มใบรับรอง](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) ในขั้นตอนที่ 1 ใบรับรองเรียกอีกอย่างว่าคีย์สาธารณะหรือคีย์โปรแกรมประยุกต์ คุณจะใช้ค่านี้เปิดใช้งานการรวม Teams ในศูนย์ควบคุม Commerce

เมื่อต้องการเปิดใช้งานการรวม Teams ในศูนย์ควบคุม Commerce ให้ทําตามขั้นตอนต่อไปนี้

1. ไปที่ **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่าคอนฟิกการรวม Microsoft Teams**
1. บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**
1. ตั้งค่าตัวเลือก **เปิดใช้งานการรวม Microsoft Teams** เป็น **ใช่**
1. ในฟิลด์ **รหัสโปรแกรมประยุกต์** และ **คีย์โปรแกรมประยุกต์** ให้ป้อนค่าที่คุณได้รับเมื่อคุณลงทะเบียนโปรแกรมประยุกต์ Teams ในพอร์ทัล Azure
1. บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**

ภาพต่อไปนี้แสดงตัวอย่างการตั้งค่าคอนฟิกการรวม Teams ในศูนย์ควบคุม Commerce

![การตั้งค่าคอนฟิกการรวม Teams ในศูนย์ควบคุม Commerce](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>ปิดใช้งานการรวม Teams

เมื่อต้องการปิดใช้งานการรวม Microsoft Teams ในศูนย์ควบคุม Commerce ให้ทําตามขั้นตอนต่อไปนี้

1. ไปที่ **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่าคอนฟิกการรวม Microsoft Teams**
1. บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**
3. ตั้งค่าตัวเลือก **เปิดใช้งานการรวม Microsoft Teams** เป็น **ไม่**
4. ล้างข้อมูลค่าออกจากฟิลด์ **รหัสโปรแกรมประยุกต์** และ **คีย์โปรแกรมประยุกต์**
1. บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**

> [!NOTE]
> หลังจากที่คุณปิดใช้งานการรวม Teams กับ Commerce แล้ว เทอร์มินัล POS จะไม่แสดงงานที่เผยแพร่จากโปรแกรมประยุกต์ Teams อีกต่อไป

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams](commerce-teams-integration.md)

[สํารอง Microsoft Teams จาก Dynamics 365 Commerce](provision-teams-from-commerce.md)

[ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[จัดการบทบาทผู้ใช้ใน Microsoft Teams](manage-user-roles-teams.md)

[แม็ปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams](map-stores-existing-teams.md)

[คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams](teams-integration-faq.md)
