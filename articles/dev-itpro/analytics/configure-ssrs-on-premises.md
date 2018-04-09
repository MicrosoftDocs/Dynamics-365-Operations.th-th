---
title: "ตั้งค่าคอนฟิก SQL Server Reporting Services สำหรับการปรับใช้ในองค์กร"
description: "หัวข้อนี้แสดงข้อมูลเกี่ยวกับการตั้งค่าคอนฟิกบริการรายงาน SQL Server (SSRS) สำหรับการปรับใช้ในองค์กร"
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 2ecfb759a59292ddbce484b3ae20368c486fedd9
ms.contentlocale: th-th
ms.lasthandoff: 03/26/2018

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a>ตั้งค่าคอนฟิก SQL Server Reporting Services สำหรับการปรับใช้ในองค์กร

[!include[banner](../includes/banner.md)]

ใช้ขั้นตอนในหัวข้อนี้ในการตั้งค่าคอนฟิกบริการรายงาน SQL Server (SSRS) สำหรับการปรับใช้ Microsoft Dynamics 365 for Finance and Operations (ในองค์กร) ของคุณ

1. เปิดแอพลิเคชัน Reporting Services Configuration Manager
2. ทิ้ง **ชื่อเซิร์ฟเวอร์** เริ่มต้น ซึ่งควรเป็นชื่อของเครื่องปัจจุบัน และ **อินสแตนซ์ของเซิร์ฟเวอร์รายงาน** **MSSQLSERVER** 
3. คลิก **เชื่อมต่อ**
   
   [![การเชื่อมต่อการตั้งค่าคอนฟิกเซิร์ฟเวอร์การรายงาน](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)
   
4. คลิกแท็บ **บัญชีบริการ** และตรวจสอบว่าการตั้งค่าตรงกับภาพต่อไปนี้หรือไม่

    [![แท็บบัญชีบริการ](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)
    
5. คลิกแท็บ **URL ของเว็บเซอร์วิส** และตรวจสอบว่าการตั้งค่าตรงกับภาพต่อไปนี้หรือไม่ 

    [![แท็บ URL ของบริการเว็บ](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png) 
    
6. คลิกแท็บ **ฐานข้อมูล** และตรวจสอบว่า **ชื่อฐานข้อมูล** และ **การตั้งค่าข้อมูลประจำตัว** ตรงกับภาพต่อไปนี้หรือไม่ **หมายเหตุ:** คุณจะต้องสร้างฐานข้อมูลใหม่ เมื่อต้องการทำเช่นนี้ ให้คลิก **เปลี่ยนแปลงฐานข้อมูล** แล้วตรวจสอบว่าชื่อฐานข้อมูลใหม่คือ: **DynamicsAxReportServer**

    [![แท็บฐานข้อมูล](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)
    
7. คลิกแท็บ **URL ของเว็บพอร์ทัล** และตรวจสอบว่าการตั้งค่าตรงกับภาพต่อไปนี้หรือไม่ **หมายเหตุ:** คุณต้องคลิก **ใช้** เพื่อสร้างและตั้งค่าคอนฟิกพอร์ทัลให้ถูกต้อง

    [![แท็บ URL ของเว็บพอร์ทัล](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)
    
  หลังจากที่มีการตั้งค่าคอนฟิกพอร์ทัล แท็บ **เว็บพอร์ทัล** จะตรงกับรูปภาพต่อไปนี้
    [![แท็บเว็บพอร์ทัล](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)
    
8. คลิก URL รายงานเพื่อดูเว็บพอร์ทัลบริการรายงาน SQL Server 
9.  เมื่อคุณอยู่ในพอร์ทัล ให้สร้างโฟลเดอร์ใหม่ที่ชื่อว่า **Dynamics**

    [![โฟลเดอร์ Dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)
    
10. ใน **Reporting Services Configuration Manager** คลิกแท็บ **การตั้งค่าอีเมล** และตรวจสอบว่าการตั้งค่าตรงกับภาพต่อไปนี้

    [![แท็บการตั้งค่าอีเมล](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)
    
11. คลิกแท็บ **บัญชีการดำเนินการ** และตรวจสอบว่าการตั้งค่าตรงกับภาพต่อไปนี้หรือไม่

    [![แท็บบัญชีการดำเนินการ](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)
    
  อย่าเปลี่ยนการตั้งค่าเริ่มต้นในแท็บ **คีย์การเข้ารหัส** [![แท็บคีย์การเข้ารหัส](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)
    
12. คลิกแท็บ **การตั้งค่าการบอกรับเป็นสมาชิก** และตรวจสอบว่าการตั้งค่าตรงกับภาพต่อไปนี้หรือไม่

    [![แท็บการตั้งค่าการบอกรับเป็นสมาชิก](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)
    
  อย่าเปลี่ยนการตั้งค่าเริ่มต้นในแท็บ **การปรับใช้ Scale-out** [![แท็บการปรับใช้ Scale-out](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)
    
  อย่าเปลี่ยนการตั้งค่าเริ่มต้นในแท็บ **การรวม Power BI** [![แท็บการรวม Power BI](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png) 
    
13. คลิก **ออก** เพื่อปิด **Reporting Services Configuration Manager**

    [![ปิด Reporting Services Configuration Manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
    


