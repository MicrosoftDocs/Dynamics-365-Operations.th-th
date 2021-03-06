---
title: เปิดใช้งานการรับรองความถูกต้อง Azure Active Directory สำหรับการลงชื่อเข้าใช้ POS
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกประสบการณ์ในการลงชื่อเข้าใช้สำหรับการขายหน้าร้าน (POS) ของ Microsoft Dynamics 365 Commerce เพื่อให้ใช้การรับรองความถูกต้อง Azure Active Directory
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d6073a04814adf8237b4caa952b31b011f4b34bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982751"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>เปิดใช้งานการรับรองความถูกต้อง Azure Active Directory สำหรับการลงชื่อเข้าใช้ POS
[!include [banner](includes/banner.md)]


ลูกค้าหลายรายที่ใช้ Microsoft Dynamics 365 Commerce ยังใช้ Microsoft Cloud Service อื่นๆ และพวกเขาอาจใช้ Azure Active Directory (Azure AD) เพื่อจัดการข้อมูลประจำตัวของผู้ใช้สำหรับบริการเหล่านั้น ในกรณีดังกล่าว ลูกค้าอาจต้องการใช้บัญชี Azure AD เดียวกันระหว่างแอพลิเคชัน หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกประสบการณ์ในการลงชื่อเข้าใช้สำหรับการขายหน้าร้าน (POS) ของ Commerce เพื่อให้ใช้การรับรองความถูกต้อง Azure AD

## <a name="configure-azure-ad-authentication"></a>ตั้งค่าคอนฟิกการรับรองความถูกต้อง Azure AD

เมื่อต้องการทำให้ Azure AD พร้อมใช้งานเป็นวิธีการรับรองความถูกต้องสำหรับการลงชื่อเข้าใช้ POS สำหรับร้านค้า คุณต้องตั้งค่าคอนฟิกการตั้งค่าของโพรไฟล์ฟังก์ชันของร้านค้า แล้วใช้การตั้งค่าเหล่านั้นกับไคลเอนต์ POS

เมื่อต้องการตั้งค่าคอนฟิกโพรไฟล์ฟังก์ชัน ให้ทำตามขั้นตอนเหล่านี้

1. ไปยัง **การขายปลีกและการค้า** \> **การตั้งค่าช่องทาง** \> **การตั้งค่า POS** \> **โปรไฟล์ POS** \> **โปรไฟล์ฟังก์ชัน**
1. เลือกโพรไฟล์ฟังก์ชันที่จะเปลี่ยน
1. บน FastTab **ฟังก์ชัน** ในส่วน **การเข้าสู่ระบบของพนักงาน POS** ให้เปลี่ยนค่าของฟิลด์ **วิธีการรับรองความถูกต้องของการเข้าสู่ระบบ** จาก **รหัสบุคลากรและรหัสผ่าน** เป็น **Azure Active Directory**

โดยค่าเริ่มต้น โพรไฟล์ฟังก์ชันทั้งหมดจะใช้ **รหัสบุคลากรและรหัสผ่าน** เป็นวิธีการรับรองความถูกต้องของ POS ดังนั้น คุณต้องเปลี่ยนค่าของฟิลด์ **วิธีการรับรองความถูกต้องของการเข้าสู่ระบบ** ถ้าคุณต้องการใช้ตรรกะ Azure AD ร้านค้าปลีกทั้งหมดที่เชื่อมโยงกับโพรไฟล์ฟังก์ชันที่เลือกจะได้รับผลกระทบจากการเปลี่ยนแปลงนี้

เมื่อต้องการใช้การตั้งค่ากับไคลเอนต์ POS ให้ทำตามขั้นตอนต่อไปนี้

1. ไปยัง **การขายปลีกและการค้า** \> **การขายปลีกและไอทีเชิงพาณิชย์** \> **กำหนดการการจัดจำหน่าย**
1. รันงาน **1070** (**การตั้งค่าคอนฟิกช่องทาง**) กำหนดการการกระจาย

> [!NOTE]
> การตรวจสอบความถูกต้อง Azure AD ต้องใช้การเชื่อมต่ออินเทอร์เน็ต การดำเนินการนี้จะไม่ทำงานเมื่อ POS อยู่ในโหมดออฟไลน์
> 
> ในขณะนี้ฟังก์ชัน **การแทนที่ผู้จัดการ** ไม่สนับสนุน Azure AD เป็นวิธีการรับรองความถูกต้อง ต้องระบุรหัสผู้ปฏิบัติการและรหัสผ่านแม้ว่า Azure AD จะมีการตั้งค่าคอนฟิกเป็นวิธีการรับรองความถูกต้องสำหรับการลงชื่อเข้าใช้ POS

## <a name="associate-an-azure-ad-account-with-a-worker"></a>เชื่อมโยงบัญชี Azure AD กับผู้ปฏิบัติงาน

ก่อนที่ผู้ปฏิบัติงานร้านค้าจะสามารถใช้บัญชี Azure AD เพื่อลงชื่อเข้าใช้ไปยังแอพลิเคชัน POS ได้ บัญชี Azure AD ต้องเชื่อมโยงกับผู้ปฏิบัติงานนั้น

เมื่อต้องการเชื่อมโยงบัญชี Azure AD กับผู้ปฏิบัติงาน ให้ทำตามขั้นตอนต่อไปนี้

1. ไปยัง **Retail และ Commerce** \> **พนักงาน** \> **ผู้ปฏิบัติงาน**
1. เปิดหน้ารายละเอียดสำหรับผู้ปฏิบัติงาน
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **Commerce** ในกลุ่ม **ข้อมูลเฉพาะตัวภายนอก** ให้เลือก **เชื่อมโยงข้อมูลเฉพาะตัวที่มีอยู่**
1. ในกล่องโต้ตอบ **ใช้ข้อมูลเฉพาะตัวภายนอกที่มีอยู่** ให้เลือก **ค้นหาโดยใช้อีเมล** ป้อนที่อยู่อีเมล Azure AD แล้วเลือก **ค้นหา**
1. เลือกบัญชี Azure AD ที่จะส่งคืน แล้วเลือก **ตกลง**

ฟิลด์ **นามแฝง** **UPN** และ **ตัวระบุย่อยภายนอก** บนแท็บ **Commerce** ของหน้ารายละเอียดของผู้ปฏิบัติงานจะถูกกรอกข้อมูล

> [!NOTE]
> หลังจากที่มีการอัพเดตเรกคอร์ดผู้ปฏิบัติงานแล้ว ตัวอย่างเช่น หากมีการเชื่อมโยง Azure AD กับบัญชีใหม่ รหัสผ่านมีการเปลี่ยนแปลงหรือมีการอัพเดตสมุดที่อยู่ของพนักงาน ขอแนะนำให้คุณรันกำหนดการกระจาย **1060** (**พนักงาน**) เพื่อซิงโครไนส์ข้อมูลพนักงานล่าสุดไปยังช่องทาง ด้วยวิธีนี้ แอปพลิเคชัน POS สามารถดึงข้อมูลที่ถูกต้องสำหรับการตรวจสอบความถูกต้องของผู้ใช้และการตรวจสอบสิทธิ์

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าฟังก์ชันการล็อกออนแบบขยายสำหรับ MPOS และ POS ระบบคลาวด์](extended-logon.md)

[สร้างโพรไฟล์ฟังก์ชันการขายปลีก](retail-functionality-profile.md)

[ ตั้งค่าคอนฟิกผู้ปฏิบัติงาน](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
