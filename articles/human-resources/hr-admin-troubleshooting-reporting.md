---
title: ตัวเลือกในการรายงาน
description: บทความนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งลูกค้าต้องการกำหนดค่ารายงาน Microsoft Dynamics 365 Human Resources หรือสร้างรายงานใหม่
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 830c8c32128a8dfc1b009557afb272e48ae3a1ff
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114416"
---
# <a name="reporting-options"></a>ตัวเลือกในการรายงาน

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**รายละเอียดสภาพแวดล้อม**

ปัญหานี้ใช้กับสภาพแวดล้อมทั้งหมด

**อาการ**

ลูกค้าต้องการกำหนดค่ารายงาน Microsoft Dynamics 365 Human Resources หรือสร้างรายงานใหม่

**ออกใช้**

ผู้ใช้ไม่สามารถกำหนดค่ารายงาน Microsoft Power BI ที่ฝังอยู่ได้

**โซลูชัน**

- ข้อมูลทรัพยากรบุคคลที่ไหลไปยัง Dataverse สามารถถูกรายงานได้ผ่านตัวเชื่อมต่อ Power Apps Dataverse ไปยัง Power BI Desktop โปรดทราบว่า Dataverse ประกอบด้วยชุดย่อยของข้อมูลทรัพยากรบุคคล สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI และแดชบอร์ด ดู [สร้างรายงานและแดชบอร์ด Power BI ด้วย Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi)
- การรายงานทางอิเล็กทรอนิกส์ (ER) พร้อมใช้งานสำหรับรายงานบางรายงานในทรัพยากรบุคคล สามารถทำการกำหนดค่าที่ควบคุมโดยลูกค้าได้โดยใช้ตัวเลือกการตั้งค่าคอนฟิก ER
- ข้อมูลถูกส่งออกไปยัง Microsoft Excel หรือ Microsoft Word โดยใช้เอนทิตีข้อมูลต่าง ๆ ที่ทรัพยากรบุคคลให้ ผ่านทางการรวม Microsoft Office

**วิธีแก้ปัญหาระยะยาว**

ตัวเลือก Power BI เพิ่มเติมจะพร้อมใช้งาน และข้อมูลและเอนทิตีเพิ่มเติมจะเป็นส่วนหนึ่งของ Dataverse
