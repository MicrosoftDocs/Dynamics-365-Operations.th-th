---
title: เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams
description: หัวข้อนี้อธิบายวิธีการเปิดใช้งานการรวม Microsoft Dynamics 365 Commerce และ Microsoft Teams
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dfada577ab97fdb9912c22d2399529f934b25d54
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695745"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีการเปิดใช้งานการรวม Microsoft Dynamics 365 Commerce และ Microsoft Teams

เมื่อต้องการเตรียมใช้งาน Teams ด้วยข้อมูลจาก Dynamics 365 Commerce และซิงโครไนส์ลักษณะการงานการจัดการงานระหว่าง Teams และแอปพลิเคชันการขายหน้าร้าน (POS) คุณต้องเปิดใช้งานคุณลักษณะการรวมในศูนย์ควบคุม Commerce

> [!NOTE]
> เมื่อคุณเปิดใช้งานการรวม Teams คุณยินยอมให้แบ่งปันข้อมูลของคุณกับ Teams ข้อมูลที่ใช้ร่วมกันกับ Teams อาจอยู่ในประเทศอื่นที่แตกต่างจากข้อมูล Commerce ของคุณ และอาจขึ้นอยู่กับมาตรฐานการปฏิบัติตามกฎระเบียบที่แตกต่างกัน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ศูนย์ความเชื่อถือของ Microsoft](https://www.microsoft.com/trust-center) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับนโยบายสิทธิส่วนบุคคลของ Microsoft โปรดดูที่ [รายงานสิทธิส่วนบุคคลของ Microsoft](https://aka.ms/privacy)

## <a name="enable-teams-integration"></a>เปิดใช้งานการรวม Teams

ก่อนที่คุณจะสามารถเปิดใช้งานการรวม Microsoft Teams กับ Commerce ได้ คุณต้องลงทะเบียนแอปพลิเคชัน Teams กับผู้เช่าของคุณในพอร์ทัล Azure ก่อน

หากต้องการลงทะเบียนแอปพลิเคชัน Teams กับผู้เช่าในพอร์ทัล Azure ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ปฏิบัติตามขั้นตอนใน [เริ่มต้นใช้งานด่วน: ลงทะเบียนแอปในแพลตฟอร์มเอกลักษณ์ Microsoft](/azure/active-directory/develop/quickstart-register-app) เพื่อลงทะเบียนแอปพลิเคชัน Teams กับผู้เช่าในพอร์ทัล Azure
1. บนแท็บ **การลงทะเบียนแอป** ให้เลือกแอปที่คุณสร้างไว้ในขั้นตอนก่อนหน้านี้ จากนั้นบนแท็บ การ **การรับรองความถูกต้อง** ให้เลือก **เพิ่มแพลตฟอร์ม**
1. ในกล่องโต้ตอบ ให้เลือก **เว็บ** จากนั้นในฟิลด์ **URL การเปลี่ยนเส้นทาง** ให้ป้อน URL ในรูปแบบ **\<HQUrl\>/oauth** แทนที่ **\<HQUrl\>** ด้วย URL ศูนย์ควบคุม Commerce ของคุณ (ตัวอย่างเช่น `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`)
1. ในหน้า **ภาพรวม** ของแอปที่ลงทะเบียน คัดลอกค่า **รหัสแอปพลิเคชัน (ไคลเอ็นต์)** คุณจะต้องระบุค่านี้เปิดใช้งานการรวม Teams ในศูนย์ควบคุม Commerce ในส่วนถัดไป
1. ทำตามคำแนะนำใน [เพิ่มข้อมูลลับของไคลเอ็นต์](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) เพื่อเพิ่มข้อมูลลับของไคลเอ็นต์ แล้วคัดลอก **ค่าข้อมูลลับ** ของไคลเอนต์ คุณจะต้องระบุค่านี้เปิดใช้งานการรวม Teams ในศูนย์ควบคุม Commerce ในส่วนถัดไป
1. เลือก **สิทธิ์ของ API** แล้วเลือก **เพิ่มสิทธิ์**
1. ในกล่องโต้ตอบ **ขอสิทธิ์ API** เลือก **Microsoft Graph** เลือก **สิทธิ์ที่ได้รับมอบ** ขยาย **กลุ่ม** เลือก **Group.ReadWrite.All** แล้วเลือก **เพิ่มสิทธิ์**
1. ในกล่องโต้ตอบ **ขอสิทธิ์ API** เลือก **เพิ่มสิทธิ์** เลือก **Microsoft Graph** เลือก **สิทธิ์ของแอปพลิเคชัน** ขยาย **กลุ่ม** เลือก **Group.ReadWrite.All** แล้วเลือก **เพิ่มสิทธิ์**
1. ในกล่องโต้ตอบ **ขอสิทธิ์ API** เลือก **เพิ่มสิทธิ์** บนแท็บ **API ที่องค์กรของฉันใช้** ค้นหา **Microsoft Teams Retail Service** แล้วเลือก
1. เลือก **สิทธิ์ที่ได้รับมอบ** ขยาย **TaskPublishing** เลือก **TaskPublishing.ReadWrite.All** แล้วเลือก **เพิ่มสิทธิ์** สำหรับข้อมูลเพิ่มเติม ดูที่ [ตั้งค่าคอนฟิกแอปพลิเคชันไคลเอ็นต์เพื่อเข้าถึง Web API](/azure/active-directory/develop/quickstart-configure-app-access-web-apis)

เมื่อต้องการเปิดใช้งานการรวม Teams ในศูนย์ควบคุม Commerce ให้ทําตามขั้นตอนต่อไปนี้

1. ไปที่ **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่าคอนฟิกการรวม Microsoft Teams**
1. บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**
1. ตั้งค่าตัวเลือก **เปิดใช้งานการรวม Microsoft Teams** เป็น **ใช่**
1. ในฟิลด์ **รหัสแอปพลิเคชัน** ป้อนค่า **รหัสแอปพลิเคชัน (ไคลเอ็นต์)** ที่คุณได้รับมาตอนลงทะเบียนแอปพลิเคชัน Teams ในพอร์ทัล Azure
1. ในฟิลด์ **คีย์แอปพลิเคชัน** ป้อนค่า **ค่าข้อมูลลับ** ที่คุณได้รับมาตอนเพิ่มข้อมูลลับของไคลเอ็นต์ในพอร์ทัล Azure
1. บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**

ภาพต่อไปนี้แสดงตัวอย่างการตั้งค่าคอนฟิกการรวม Teams ในศูนย์ควบคุม Commerce

![การตั้งค่าคอนฟิกการรวม Teams ในศูนย์ควบคุม Commerce](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>ปิดใช้งานการรวม Teams

เมื่อต้องการปิดใช้งานการรวม Microsoft Teams ในศูนย์ควบคุม Commerce ให้ทําตามขั้นตอนต่อไปนี้

1. ไปที่ **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่าคอนฟิกการรวม Microsoft Teams**
1. บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**
3. ตั้งค่าตัวเลือก **เปิดใช้งานการรวม Microsoft Teams** เป็น **ไม่**
4. ล้างข้อมูลค่าออกจากฟิลด์ **รหัสแอปพลิเคชัน** และ **คีย์แอปพลิเคชัน**
1. บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**

> [!NOTE]
> หลังจากที่คุณปิดใช้งานการรวม Teams กับ Commerce แล้ว เทอร์มินัล POS จะไม่แสดงงานที่เผยแพร่จากแอปพลิเคชัน Teams อีกต่อไป

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams](commerce-teams-integration.md)

[สํารอง Microsoft Teams จาก Dynamics 365 Commerce](provision-teams-from-commerce.md)

[ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[จัดการบทบาทผู้ใช้ใน Microsoft Teams](manage-user-roles-teams.md)

[แมปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams](map-stores-existing-teams.md)

[คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams](teams-integration-faq.md)
