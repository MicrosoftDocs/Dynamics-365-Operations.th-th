---
title: ตัวเลือกในการรายงาน
description: หัวข้อนี้อธิบายวิธีการเลือกกำหนดรายงาน Microsoft Dynamics 365 Human Resources หรือสร้างรายงานใหม่
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 706e901e89fa618540067d68546be1cef1ee7148
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413393"
---
# <a name="reporting-options"></a>ตัวเลือกในการรายงาน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**รายละเอียดสภาพแวดล้อม**

ปัญหานี้ใช้กับสภาพแวดล้อมทั้งหมด

**อาการ**

ลูกค้าต้องการกำหนดค่ารายงาน Microsoft Dynamics 365 Human Resources หรือสร้างรายงานใหม่

**ออก**

ผู้ใช้ไม่สามารถกำหนดค่ารายงาน Microsoft Power BI ที่ฝังอยู่ได้

**โซลูชัน**

- ข้อมูลทรัพยากรบุคคลที่ไหลไปยัง Dataverse สามารถถูกรายงานได้ผ่านตัวเชื่อมต่อ Power Apps Dataverse ไปยัง Power BI Desktop โปรดทราบว่า Dataverse ประกอบด้วยชุดย่อยของข้อมูลทรัพยากรบุคคล สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI และแดชบอร์ด ดู [สร้างรายงานและแดชบอร์ด Power BI ด้วย Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi)
- การรายงานทางอิเล็กทรอนิกส์ (ER) พร้อมใช้งานสำหรับรายงานบางรายงานในทรัพยากรบุคคล สามารถทำการกำหนดค่าที่ควบคุมโดยลูกค้าได้โดยใช้ตัวเลือกการตั้งค่าคอนฟิก ER
- ข้อมูลถูกส่งออกไปยัง Microsoft Excel หรือ Microsoft Word โดยใช้เอนทิตีข้อมูลต่าง ๆ ที่ทรัพยากรบุคคลให้ ผ่านทางการรวม Microsoft Office

**วิธีแก้ปัญหาระยะยาว**

ตัวเลือก Power BI เพิ่มเติมจะพร้อมใช้งาน และข้อมูลและเอนทิตีเพิ่มเติมจะเป็นส่วนหนึ่งของ Dataverse


[!INCLUDE[footer-include](../includes/footer-banner.md)]
