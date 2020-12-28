---
title: การแก้ไขปัญหาการรวม LinkedIn กับ Microsoft Dynamics 365 Talent - Attract
description: หัวข้อนี้อธิบายถึงวิธีการแก้ไขปัญหาเมื่อคุณพยายามลงประกาศงานไปยัง LinkedIn จาก Microsoft Dynamics 365 Talent - Attract
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: ec095642f556b8d0087dd22f35097671a30047a6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462674"
---
# <a name="troubleshoot-integration-with-linkedin-and-attract"></a>การแก้ไขปัญหาการรวมกับ LinkedIn และ Attract

[!include [banner](includes/banner.md)]

ใช้ข้อมูลต่อไปนี้เพื่อช่วยแก้ไขปัญหาที่คุณอาจมี เมื่อคุณพยายามลงประกาศงานไปยัง LinkedIn จาก Microsoft Dynamics 365 Talent: Attract

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a>คุณไม่สามารถลงชื่อเข้าใช้ LinkedIn จาก Attract

หากคุณกำลังประสบปัญหาในการลงชื่อเข้าใช้ LinkedIn จาก Attract ให้ลองทำตามขั้นตอนต่อไปนี้

1. ตรวจสอบว่าข้อมูลประจำตัวของ LinkedIn ที่คุณป้อนใน Attract ใช้ได้และถูกต้อง
2. ถ้าข้อมูลประจำตัวใช้ได้และถูกต้อง ติดต่อ [ฝ่ายสนับสนุนของ LinkedIn](https://www.linkedin.com/help/linkedin)
3. ถ้าปัญหายังคงอยู่ ติดต่อ [ฝ่ายสนับสนุนของ Microsoft](./talent-support.md)

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a>ประกาศงานจาก Attract ไม่ปรากฏบน LinkedIn

ถ้างานของคุณไม่ปรากฏบน LinkedIn หลังจาก 24 ชั่วโมง ให้ลองทำตามขั้นตอนต่อไปนี้

1. ตรวจสอบให้แน่ใจว่ารหัสของบริษัท LinkedIn ของคุณแม็ปไปยังหน้าของบริษัท LinkedIn ของคุณ และป้อนไว้อย่างถูกต้องในศูนย์การจัดการ Attract สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเปลี่ยนการตั้งค่า LinkedIn ในศูนย์การจัดการ ให้ดูที่ [ตั้งค่าการรวมกับ LinkedIn สำหรับ Microsoft Dynamics 365 Talent - Attract](attract-admin-linkedin.md) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสบริษัท LinkedIn โปรดดูที่ [การเชื่อมโยงรหัสบริษัท Linkedin กับบอร์ดงาน Linkedin - คำถามที่ถามบ่อย](https://www.linkedin.com/help/linkedin/answer/98972)
2. ตรวจสอบรายละเอียดงานบน LinkedIn เพื่อให้แน่ใจว่าที่อยู่เสร็จสมบูรณ์แล้ว เมื่อต้องการลงประกาศงานให้สมบูรณ์ LinkedIn ต้องการอย่างน้อยเมืองและประเทศหรือภูมิภาคของงาน
3. ตรวจสอบให้แน่ใจว่างานไม่ซ้ำกับงานอื่นที่มีการลงประกาศแล้วใน LinkedIn LinkedIn จะไม่ลงประกาศงานที่ซ้ำกับช่องงานพิเศษของ LinkedIn หรือรายการที่จำกัดจากแหล่งที่มาอื่น ตรวจสอบว่าบุคคลอื่นในบริษัทของคุณยังไม่ได้ลงประกาศงานด้วยตนเอง

## <a name="see-also"></a>ดูเพิ่มเติมที่

[การรวม Attract กับ FAQ เกี่ยวกับ LinkedIn](./attract-linkedin-faq.md)

[ลงประกาศงานใน LinkedIn จาก Microsoft Dynamics 365 Talent - Attract](./attract-post-jobs-to-linkedin.md)

[จัดหาผู้สมัครด้วย LinkedIn Recruiter ใน Microsoft Dynamics 365 Talent - Attract](./attract-linkedin-recruiter.md)

[สร้าง อนุมัติ และลงรายการบัญชีงานใน Attract](./creating-jobs-attract.md)

[การแก้ไขปัญหาการรวม LinkedIn และ Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md)
