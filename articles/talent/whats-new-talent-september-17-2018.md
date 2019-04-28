---
title: มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (17 กันยายน 2018)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 213324f9074f88d9fdc8efdfa46bc3ed7817d1e8
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/19/2019
ms.locfileid: "856818"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-17-2018"></a>มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (17 กันยายน 2018)

[!include [banner](includes/banner.md)]

**สร้าง 8.1.154.0**

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a>การลางานและการขาดงาน – เวลาค้างรับค้างจ่ายตามชั่วโมงที่ทำงาน

มีการเพิ่มชนิดการรับรู้ใหม่ไปยังแผนการลางาน ขณะนี้ กำหนดการคงค้างสามารถทำได้ตามเดือนของการบริการหรือชั่วโมงที่ทำงาน สำหรับข้อมูลเพิ่มเติม ดู [เวลาหยุดพักคงค้างตามชั่วโมงที่ทำงาน](leave-accrue-hours-worked.md)

## <a name="platform-update-18"></a>แพลตฟอร์ม update 18

การปรับปรุงแพลตฟอร์ม 18 เป็นส่วนหนึ่งของการนำออกใช้ Talent ในขณะนี้ 

-   คุณจะสามารถซ่อนฟิลด์บังคับและอื่นๆ ได้โดยผ่านการตั้งค่าส่วนบุคคล ซึ่งช่วยให้ผู้ใช้สามารถสร้างประสบการณ์แบบง่าย ที่ซึ่งฟิลด์บังคับที่เริ่มโดยตรรกะทางธุรกิจ จะไม่แสดงขึ้น นอกจากนี้ ฟิลด์บังคับที่ซ่อนไว้จะทำให้มองเห็นได้แบบชั่วคราวว่า มีข้อมูลเมื่อมีการพยายามทำการบันทึกหรือไม่

-   ในการปรับปรุงแพลตฟอร์ม 18 ขณะนี้ ไคลเอนต์เว็บ Talent จัดเรียงภาพให้ตรงกับ Microsoft Fluent Design

    -   เมื่อฟิลด์อยู่ใน "โหมดอ่าน" คุณสามารถเลือกตัวเลือกการแก้ไขในฟิลด์ได้โดยง่าย เพื่อสลับแบบฟอร์มเพื่อแก้ไข

    -   การเปลี่ยนแปลงในวิธีที่ฟิลด์แสดงเมื่ออยู่ในโหมดอ่าน

    -   หัวข้อในพื้นที่ทำงานและหน้าเป็นตัวหนา

-   ลักษณะการทำงานของการค้นหาแบบไม่แทนที่ ได้รับการปรับปรุง สำหรับข้อมูลเพิ่มเติม ดู [ลักษณะการทำงานที่ปรับปรุงแล้วสำหรับการค้นหาแบบไม่แทนที่](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0)

## <a name="bug-fixes"></a>การแก้ไขปัญหา

รุ่นนี้ประกอบด้วยการแก้ไขบักเพิ่มเติมหลายรายการ ซึ่งรวมทั้งการอ้างอิงถึง ACA ADA และ I9 จะถูกเปิดใช้งานในบริษัทในสหรัฐอเมริกาในขณะนี้
