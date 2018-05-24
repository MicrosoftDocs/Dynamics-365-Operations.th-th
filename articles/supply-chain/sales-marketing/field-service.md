---
title: "การรวมกับ Microsoft Dynamics 365 for Field Service"
description: "หัวข้อนี้แสดงภาพรวมของการรวมกับ Microsoft Dynamics 365 for Field Service"
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 03a932652cdd93b2a5917d0fca72809d1648b678
ms.openlocfilehash: b1acf0b64914a3199fcf44f8377e32b26f0af99e
ms.contentlocale: th-th
ms.lasthandoff: 04/25/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>การรวมกับ Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations เปิดใช้งานการซิงโครไนส์กระบวนการทางธุรกิจระหว่าง Finance and Operations และ Microsoft Dynamics 365 for Field Service สถานการณ์จำลองการรวมถูกตั้งค่าคอนฟิกโดยใช้เท็มเพลตตัวรวมข้อมูลที่ขยายได้ และ Common Data Service (CDS) เพื่อเปิดใช้งานการซิงโครไนส์ของกระบวนการทางธุรกิจ

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

เฟสแรกของการรวมระหว่าง Field Service และ Finance and Operations จะเน้นบนการเปิดใช้งานใบสั่งผลิตและข้อตกลงใน Field Service ให้ออกใบแจ้งหนี้ใน Finance and Operations ขั้นตอนที่ได้รับการสนับสนุนเริ่มต้นใน Field Service ที่ซึ่งมีการซิงโครไนส์ข้อมูลจากใบสั่งผลิตไปยัง Finance and Operations เป็นใบสั่งขาย ใน Finance and Operations ใบสั่งขายออกใบแจ้งหนี้เพื่อสร้างเอกสารใบแจ้งหนี้ นอกจากนี้ ข้อมูลจากใบแจ้งหนี้ของข้อตกลงของ Field Service จะซิงโครไนส์กับ Finance and Operations ตัวรวมข้อมูล Microsoft Dynamics 365 ซิงโครไนส์ข้อมูลโดยใช้โครงการที่กำหนดเองได้ เท็มเพลตมาตรฐานสามารถใช้เพื่อสร้างโครงการที่มีการรวมแบบกำหนดเอง ที่ซึ่งฟิลด์มาตรฐานและแบบกำหนดเองเพิ่มเติม และรวมทั้งเอนทิตี สามารถถูกแม็ปเพื่อปรับปรุงการรวม และให้ตรงตามข้อกำหนดเฉพาะ

เฟสแรกของการรวมระหว่าง Field Service และ Finance and Operations เปิดใช้งานการซิงโครไนส์ของรายการต่อไปนี้:

- [ผลิตภัณฑ์ใน Finance and Operations ไปยังผลิตภัณฑ์ใน Field Service ที่รวมข้อมูลชนิดผลิตภัณฑ์](field-service-product.md)
- [ใบสั่งผลิตใน Field Service ไปยังใบสั่งขายใน Finance and Operations](field-service-work-order.md)
- [ใบแจ้งหนี้ใน Field Service ไปยังใบแจ้งหนี้ข้อความอิสระใน Finance and Operations](field-service-invoice.md)

เมื่อต้องการดูตัวอย่างของวิธีที่คุณสามารถซิงโครไนส์ใบสั่งงานระหว่าง Field Service และ Finance and Operations โปรดดูวิดีโอ YouTube แบบย่อ:

> [!Video https://www.youtube.com/embed/hAB4TDVMjxU]

[ซิงโครไนส์ใบสั่งงานระหว่าง Field Service กับ Finance and Operations (วิดีโอ YouTube)](https://youtu.be/hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a>ความต้องการของระบบสำหรับ Finance and Operations
การรวม Field Service สนับสนุนเวอร์ชันต่อไปนี้:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations รุ่น 8.0 (เมษายน 2018) หรือรุ่นที่ใหม่กว่า

- Dynamics 365 for Finance and Operations รุ่น 8.0 (เมษายน 2018) ถูกนำออกใช้ในเดือนเมษายน 2018 และได้สร้างแอพลิเคชันหมายเลข 8.0.30.8020 ที่มีการอัพเดแพลตฟอร์ม 15 (7.0.4841.35234) 

## <a name="system-requirements-for-field-service"></a>ข้อกำหนดของระบบสำหรับ Field Service
เมื่อต้องการใช้โซลูชันการรวม Field Service คุณต้องติดตั้งส่วนประกอบต่อไปนี้:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 สำหรับ Field Service 9.0 หรือรุ่นที่ใหม่กว่า

- Dynamics 365 for Field Service รุ่น 1612 (9.0.1.733) (DB 9.0.1.733) ออนไลน์ หรือรุ่นที่ใหม่กว่า
- โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด (P2C) สำหรับ Dynamics 365 รุ่น 1.15.0.1 หรือรุ่นที่ใหม่กว่า โซลูชันนี้จะพร้อมใช้งานสำหรับการดาวน์โหลดจาก [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)
- โซลูชันการรวม Field Service สำหรับ Dynamics 365 รุ่น 1.0.0.0 หรือรุ่นที่ใหม่กว่า โซลูชันนี้จะพร้อมใช้งานสำหรับการดาวน์โหลดจาก [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration)

