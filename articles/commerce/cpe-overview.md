---
title: ภาพรวมของสภาพแวดล้อมการแสดงตัวอย่างของ Commerce
description: หัวข้อนี้จะแสดงภาพรวมของการค้นหาที่ขับเคลื่อนโดยระบบคลาวด์ใน Microsoft Dynamics 365 Commerce
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906081"
---
# <a name="commerce-preview-environment-overview"></a>ภาพรวมของสภาพแวดล้อมการแสดงตัวอย่างของ Commerce

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

หัวข้อนี้จะแสดงภาพรวมของการค้นหาที่ขับเคลื่อนโดยระบบคลาวด์ใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

สภาพแวดล้อมการแสดงตัวอย่างของ Commerce คือสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce แบบ end-to-end ที่เป็นทางเลือกของลูกค้าที่มีศักยภาพในการทดลองใช้ผลิตภัณฑ์ Commerce ก่อนที่จะเปิดตัวทั่วไปในสาธารณชน

นอกเหนือจากข้อจำกัดเล็กน้อยที่ไม่มีผลต่อคุณลักษณะหรือฟังก์ชัน การทำงานของระบบการแสดงตัวอย่างของ Commerce จะมอบประสบการณ์ทางการค้าที่สมบูรณ์ และสามารถนำมาใช้โดยลูกค้าและคู่ค้าที่ดำเนินการเพื่อประเมินผลิตภัณฑ์ให้ความคิดเห็นและทำการวิเคราะห์ที่พอดี/ช่องว่าง

## <a name="limitations-of-the-commerce-preview-environment"></a>ข้อจำกัดของสภาพแวดล้อมการแสดงตัวอย่าง Commerce

ถึงแม้ว่าสภาพแวดล้อมการแสดงตัวอย่าง Commerce จะให้ชุดคุณลักษณะและการทำงานของ Commerce อย่างเต็มรูปแบบ แต่ก็มีข้อจำกัดเล็กน้อย:

- ถึงแม้ว่าสภาพแวดล้อมการแสดงตัวอย่างของ Commerce จะไม่มีข้อจำกัดทางภูมิศาสตร์ ส่วนประกอบของสภาพแวดล้อม Retail Cloud Scale Unit เช่น (RCSU) และแอปพลิเคชันอีคอมเมิร์ซ สามารถเตรียมใช้งานได้เฉพาะในสหรัฐอเมริกาเท่านั้น
- การใช้สภาพแวดล้อมการแสดงตัวอย่าง Commerce มีการจำกัดเวลา 30 วัน นับจากวันที่จัดสรรอีคอมเมิร์ซ
- สภาพแวดล้อมการแสดงตัวอย่าง Commerce สามารถปรับใช้เรียบร้อยแล้วและเริ่มต้นเฉพาะในสภาพแวดล้อมที่ใช้โทโพโลยีสาธิตที่ส่วนประกอบทั้งหมดของสภาพแวดล้อมที่มีการปรับใช้ในเครื่องเสมือน (VM) เดียว ข้อจำกัดหลักของโทโพโลยี OneBox VM นี้คือจำนวนของผู้ใช้พร้อมกันที่สภาพแวดล้อมการแสดงตัวอย่างสามารถสนับสนุน
- สภาพแวดล้อมการแสดงตัวอย่าง Commerce สามารถประเมินได้จนกว่าความพร้อมใช้งานทั่วไป (GA) ของผลิตภัณฑ์ Commerce เท่านั้น สภาพแวดล้อมการสาธิตใหม่จะพร้อมใช้งานหลังจาก GA

## <a name="get-started"></a>เริ่มต้นใช้งาน

ในการจัดสรรสภาพแวดล้อมการแสดงตัวอย่าง Commerce โปรดดูที่ [การจัดสรรสภาพแวดล้อมการแสดงตัวอย่างของ Commerce](provisioning-guide.md)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[เตรียมใช้งานสภาพแวดล้อมการแสดงตัวอย่างของ Commerce](provisioning-guide.md)

[กำหนดค่าสภาพแวดล้อมการแสดงตัวอย่างของ Commerce](cpe-post-provisioning.md)

[กำหนดค่าคุณลักษณะเสริมสำหรับสภาพแวดล้อมการแสดงตัวอย่างของ Commerce](cpe-optional-features.md)

[FAQ เกี่ยวกับสภาพแวดล้อมการแสดงตัวอย่างของ Commerce](cpe-faq.md)
