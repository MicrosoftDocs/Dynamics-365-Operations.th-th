---
title: แก้ไขปัญหาที่เกี่ยวข้องกับการรับรู้โซลูชัน
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับการแก้ไขปัญหาซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการรับรู้โซลูชัน
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 013e37269ec3df2bede15b28cffcc175967de9a3
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172632"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>แก้ไขปัญหาที่เกี่ยวข้องกับการรับรู้โซลูชัน

[!include [banner](../../includes/banner.md)]



หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Common Data Service กล่าวคือ จะให้ข้อมูลซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการรับรู้โซลูชัน

> [!IMPORTANT]
> ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD) ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่

## <a name="error-on-the-dual-write-page"></a>ข้อผิดพลาดในหน้าการรวมแบบสองทิศทาง

บนหน้า **การรวมแบบสองทิศทาง** คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้:

*ไม่พบเอนทิตี้ที่มีชื่อว่า 'msdyn\_dualwriteentitymap' with namemapping='Logical' ใน MetadataCache*

เมื่อต้องการแก้ไขปัญหานี้ โปรดตรวจสอบให้แน่ใจว่าได้ติดตั้งโซลูชันหลักของการรวมแบบสองทิศทางแล้วใน Common Data Service โซลูชันหลักของการรวมแบบสองทิศทางเป็นข้อกำหนดเบื้องต้นสำหรับการรับรู้โซลูชัน
