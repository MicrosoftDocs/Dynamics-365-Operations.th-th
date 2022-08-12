---
title: แก้ไขปัญหาที่เกี่ยวข้องกับการรับรู้โซลูชัน
description: บทความนี้จะให้ข้อมูลเกี่ยวกับการแก้ไขปัญหาซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการรับรู้โซลูชัน
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6866956efcc76a7da6c3aa5fb36058de78d5472e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111312"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>แก้ไขปัญหาที่เกี่ยวข้องกับการรับรู้โซลูชัน

[!include [banner](../../includes/banner.md)]





บทความนี้แสดงข้อมูลการแก้ไขปัญหาสำหรับการรวมข้อมูลด้วยการรวมแบบสองทิศทางระหว่างแอปการเงินและการดำเนินงานกับ Dataverse กล่าวคือ จะให้ข้อมูลซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการรับรู้โซลูชัน

> [!IMPORTANT]
> ปัญหาบางอย่างที่ที่อยู่ของบทความนี้ อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD) ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่

## <a name="error-on-the-dual-write-page"></a>ข้อผิดพลาดในหน้าการรวมแบบสองทิศทาง

บนหน้า **การรวมแบบสองทิศทาง** คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้:

*ไม่พบเอนทิตีที่มีชื่อว่า 'msdyn\_dualwriteentitymap' with namemapping='Logical' ใน MetadataCache*

เมื่อต้องการแก้ไขปัญหานี้ โปรดตรวจสอบให้แน่ใจว่าได้ติดตั้งโซลูชันหลักของการรวมแบบสองทิศทางแล้วใน Dataverse โซลูชันหลักของการรวมแบบสองทิศทางเป็นข้อกำหนดเบื้องต้นสำหรับการรับรู้โซลูชัน


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
