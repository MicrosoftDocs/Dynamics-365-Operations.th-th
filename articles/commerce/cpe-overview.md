---
title: ภาพรวมของสภาพแวดล้อมการประเมิน Dynamics 365 Commerce
description: หัวข้อนี้จะแสดงภาพรวมของสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bdd634a04b6bbcf50d04cae8d670367268e57f1e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795894"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a>ภาพรวมของสภาพแวดล้อมการประเมิน Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

หัวข้อนี้จะแสดงภาพรวมของสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce

> [!NOTE]
> สภาพแวดล้อมการประเมิน Commerce โดยทั่วไปไม่พร้อมใช้งาน และจะถูกกำหนดให้กับคู่ค้าและลูกค้าในแต่ละคำขอ สำหรับข้อมูลเพิ่มเติม ติดต่อคู่ค้า Microsoft ของคุณ

สภาพแวดล้อมการประเมินของ Commerce คือสภาพแวดล้อมที่ครอบคลุมที่ไม่จำเป็นต้องระบุของ Dynamics 365 Commerce ที่อนุญาตให้คู่ค้าและผู้ที่มีแนวโน้มจะเป็นลูกค้าทดลองใช้ผลิตภัณฑ์ Commerce ได้

สภาพแวดล้อมการประเมินมีการตั้งค่าคอนฟิกไว้ล่วงหน้าเพียงบางส่วนเพื่อลดขั้นตอนหลังการเตรียมใช้งานที่จำเป็น

นอกเหนือจากข้อจำกัดเล็กน้อยบางอย่างผลิตภัณฑ์ที่ไม่มีผลต่อคุณลักษณะหรือฟังก์ชัน สภาพแวดล้อมการประเมินของ Commerce จะมอบประสบการณ์ Commerce ที่สมบูรณ์ และสามารถนำมาใช้โดยลูกค้าและคู่ค้าที่ดำเนินการเพื่อประเมินผลิตภัณฑ์ ให้ความคิดเห็น และทำการวิเคราะห์ความเหมาะสม/ช่องว่าง

## <a name="limitations-of-the-commerce-evaluation-environment"></a>ข้อจำกัดของสภาพแวดล้อมการประเมินของ Commerce

ถึงแม้ว่าสภาพแวดล้อมการประเมินของ Commerce จะให้ชุดของคุณลักษณะและการทำงานของ Commerce อย่างเต็มรูปแบบ แต่ก็มีข้อจำกัดเล็กน้อยบางอย่าง:

- ถึงแม้ว่าสภาพแวดล้อมการประเมินของ Commerce จะไม่มีข้อจำกัดทางภูมิศาสตร์ ส่วนประกอบของสภาพแวดล้อม เช่น Retail Cloud Scale Unit (RCSU) และแอปพลิเคชันอีคอมเมิร์ซ ควรถูกเตรียมใช้งานเฉพาะในสหรัฐอเมริกาเท่านั้น
- การใช้สภาพแวดล้อมการประเมินของ Commerce ถูกจำกัดที่ 30 วัน นับจากวันที่มีการเตรียมใช้งานอีคอมเมิร์ซ
- สามารถปรับใช้สภาพแวดล้อมการประเมินของ Commerce ได้สำเร็จแล้ว และเริ่มต้นเฉพาะในสภาพแวดล้อมที่ใช้โทโพโลยีสาธิต ที่ซึ่งส่วนประกอบทั้งหมดของสภาพแวดล้อมถูกปรับใช้ในเครื่องเสมือน (VM) ที่โฮสต์บนระบบคลาวด์เดียว ข้อจำกัดหลักของโทโพโลยีนี้คือ จำนวนของผู้ใช้พร้อมกันที่สภาพแวดล้อมสามารถรองรับได้

## <a name="get-started"></a>เริ่มต้น

เมื่อต้องการเตรียมใช้งานสภาพแวดล้อมการประเมินของ Commerce โปรดดูที่ [เตรียมใช้งานสภาพแวดล้อมการประเมินของ Commerce](provisioning-guide.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[เตรียมใช้งานสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](provisioning-guide.md)

[ตั้งค่าคอนฟิกภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-post-provisioning.md)

[ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-bopis.md)

[ตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-optional-features.md)

[FAQ เกี่ยวกับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
