---
title: ตัวเลือกการรายงานใน Talent
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งลูกค้าต้องการกำหนดค่ารายงาน Microsoft Dynamics 365 for Talent หรือสร้างรายงานใหม่
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7e00a6e4fc01f72e1ef2347e08754997135215ed
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/12/2019
ms.locfileid: "950070"
---
# <a name="reporting-options-in-talent"></a>ตัวเลือกการรายงานใน Talent

[!include [banner](includes/banner.md)]

**รายละเอียดสภาพแวดล้อม**

ปัญหานี้ใช้กับสภาพแวดล้อมทั้งหมด

**อาการ**

ลูกค้าต้องการกำหนดค่ารายงาน Microsoft Dynamics 365 for Talent หรือสร้างรายงานใหม่

**ออกใช้**

ผู้ใช้ไม่สามารถกำหนดค่ารายงาน Microsoft Power BI ที่ฝังอยู่ได้

**โซลูชัน**

- ข้อมูล Core HR ที่ไหลไปยัง Common Data Service สามารถถูกรายงานได้ ผ่านตัวเชื่อมต่อ PowerApps Common Data Service ไปยัง Power BI Desktop โปรดทราบว่า Common Data Service ประกอบด้วยชุดย่อยของข้อมูล Core HR สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI และแดชบอร์ด ดู [สร้างรายงานและแดชบอร์ด Power BI ด้วย PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi)
- การรายงานทางอิเล็กทรอนิกส์ (ER) พร้อมใช้งานสำหรับรายงานบางรายงานใน Talent สามารถทำการกำหนดค่าที่ควบคุมโดยลูกค้าได้โดยใช้ตัวเลือกการตั้งค่าคอนฟิก ER
- ข้อมูลถูกส่งออกไปยัง Microsoft Excel หรือ Microsoft Word โดยใช้เอนทิตีข้อมูลต่างๆ ที่ Talent ให้ ผ่านทางการรวม Microsoft Office

**วิธีแก้ปัญหาระยะยาว**

ตัวเลือก Power BI เพิ่มเติมจะพร้อมใช้งาน และข้อมูลและเอนทิตีเพิ่มเติมจะเป็นส่วนหนึ่งของ Common Data Service
