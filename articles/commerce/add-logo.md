---
title: เพิ่มโลโก้
description: หัวข้อนี้อธิบายวิธีการเพิ่มโลโก้ไปยังไซต์ของคุณใน Microsoft Dynamics 365 Commerce
author: bicyclingfool
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 073c3d6f8d5ee88d51efb41f6b9c1a204b82fa12
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980318"
---
# <a name="add-a-logo"></a>เพิ่มโลโก้

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีการเพิ่มโลโก้ไปยังไซต์ของคุณใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

เมื่อคุณสร้างเว็บไซต์หนึ่ง สิ่งแรกที่คุณอาจจะทำคือการเพิ่มบริษัทหรือโลโก้แบรนด์ของคุณลงในส่วนหัวของเว็บไซต์ ไลบรารีโมดูลออนไลน์ Dynamics 365 Commerce มีโมดูลที่ทำให้งานนี้ง่ายขึ้น

คุณสามารถเพิ่มโลโก้ลงในเท็มเพลต เค้าโครง หรือหน้าได้โดยตรง ด้วยวิธีนี้คุณสามารถเปลี่ยนโลโก้ที่ปรากฏบนหน้าเว็บหรือกลุ่มของหน้าเว็บที่เฉพาะเจาะจงได้อย่างง่ายดาย อย่างไรก็ตามหัวข้อนี้ครอบคลุมสถานการณ์ที่พบบ่อยที่สุดที่คุณเพิ่มโลโก้ของคุณไปยังส่วนหัวที่สามารถนำมาใช้ในทุกหน้าของเว็บไซต์ของคุณ

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะสามารถเพิ่มโลโก้ลงในหน้าเว็บทั้งหมดของไซต์ คุณจะต้องทำงานเหล่านี้ให้เสร็จสมบูรณ์

1. อัพโหลดโลโก้ของคุณไปยังไลบรารีสื่อ
1. สร้างส่วนหัวข้อ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสร้างกลุ่มดังกล่าวและใช้หัวข้อ โปรดดู [ทำงานกับส่วน](work-with-fragments.md)
1. รวมส่วนหัวในเท็มเพลตที่หน้าของไซต์ของคุณใช้สำหรับเค้าโครงและตัวเลือกโมดูล หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับเท็มเพลต โปรดดูที่ [ทำงานกับเท็มเพลต](work-with-templates.md)

## <a name="add-a-logo-to-a-header-fragment"></a>เพิ่มโลโก้ให้กับส่วนหัว

หากต้องการเพิ่มโลโก้ให้กับส่วนหัวของเว็บไซต์ ให้ทำตามขั้นตอนเหล่านี้

1. ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ส่วนต่างๆ**
1. เลือกส่วนของส่วนหัวที่คุณสร้างไว้ก่อนหน้านี้ แล้วเลือก **แก้ไข**
1. ขยายโมดูลส่วนหัว
1. ในบานหน้าต่างคุณสมบัติสำหรับโมดูลส่วนหัว ให้ระบุรูปภาพและลิงก์สำหรับโลโก้ 
1. บันทึกส่วนของส่วนหัว แก้ไขให้เสร็จสิ้น และเผยแพร่

หลังจากที่คุณเผยแพร่ส่วนหัวที่อัปเดต หน้าไซต์ทั้งหมดที่ใช้เท็มเพลตที่ประกอบด้วยส่วนหัวจะแสดงโลโก้ของคุณ

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[เลือกธีมของไซต์](select-site-theme.md)

[ทำงานกับไฟล์การแก้ไข CSS](css-override-files.md)

[เพิ่มไอคอนประจำไซต์](add-favicon.md)

[เพิ่มข้อความต้อนรับ](add-welcome-message.md)

[เพิ่มข้อความสงวนลิขสิทธิ์](add-copyright-notice.md)

[เพิ่มภาษาลงในไซต์ของคุณ](add-languages-to-site.md)

[เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล](add-telemetry.md)

