---
title: การรวมข้อมูลกับภาพรวมของ Microsoft Dynamics 365 for Field Service
description: หัวข้อนี้แสดงภาพรวมของการรวมกับ Microsoft Dynamics 365 for Field Service
author: ChristianRytt
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 22abe83f06b7fc57c73fb82ccafc4b426667e7c6
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865219"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service-overview"></a>การรวมข้อมูลกับภาพรวมของ Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations เปิดใช้งานการซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Microsoft Dynamics 365 for Field Service สถานการณ์จำลองการรวมถูกตั้งค่าคอนฟิกโดยใช้เท็มเพลตตัวรวมข้อมูลที่ขยายได้ และ Common Data Service (CDS) เพื่อเปิดใช้งานการซิงโครไนส์ของกระบวนการทางธุรกิจ
เท็มเพลตมาตรฐานสามารถใช้เพื่อสร้างโครงการที่มีการรวมแบบกำหนดเอง ที่ซึ่งฟิลด์มาตรฐานและแบบกำหนดเองเพิ่มเติมและเอนทิตี สามารถถูกแม็ปเพื่อปรับปรุงการรวม และให้ตรงตามความต้องการทางธุรกิจเฉพาะ 

สร้างการรวมบริการฟิลด์ด้านบนสุดฟังก์ชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่มีอยู่

![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/field-service-integration.png)

เฟสแรกของการรวมระหว่าง Field Service และ Finance and Operations จะเน้นบนการเปิดใช้งานใบสั่งผลิตและข้อตกลงใน Field Service ให้ออกใบแจ้งหนี้ใน Finance and Operations ขั้นตอนที่ได้รับการสนับสนุนเริ่มต้นใน Field Service ที่ซึ่งมีการซิงโครไนส์ข้อมูลจากใบสั่งผลิตไปยัง Finance and Operations เป็นใบสั่งขาย ใน Finance and Operations ใบสั่งขายออกใบแจ้งหนี้เพื่อสร้างเอกสารใบแจ้งหนี้ นอกจากนี้ ข้อมูลจากใบแจ้งหนี้ของข้อตกลงของ Field Service จะซิงโครไนส์กับ Finance and Operations ตัวรวมข้อมูล Microsoft Dynamics 365 ซิงโครไนส์ข้อมูลโดยใช้โครงการที่กำหนดเองได้ เท็มเพลตมาตรฐานสามารถใช้เพื่อสร้างโครงการที่มีการรวมแบบกำหนดเอง ที่ซึ่งฟิลด์มาตรฐานและแบบกำหนดเองเพิ่มเติม และรวมทั้งเอนทิตี สามารถถูกแม็ปเพื่อปรับปรุงการรวม และให้ตรงตามข้อกำหนดเฉพาะ

เฟสแรกของการรวมระหว่าง Field Service และ Finance and Operations เปิดใช้งานการซิงโครไนส์ของรายการต่อไปนี้:

- [ผลิตภัณฑ์ใน Finance and Operations ไปยังผลิตภัณฑ์ใน Field Service ที่รวมข้อมูลชนิดผลิตภัณฑ์](field-service-product.md)
- [ใบสั่งผลิตใน Field Service ไปยังใบสั่งขายใน Finance and Operations](field-service-work-order.md)
- [ใบแจ้งหนี้ใน Field Service ไปยังใบแจ้งหนี้ข้อความอิสระใน Finance and Operations](field-service-invoice.md)

เมื่อต้องการดูตัวอย่างของวิธีการที่คุณสามารถซิงโครไนส์ใบสั่งงานระหว่าง Field Service และ Finance and Operations ดูวิดีโอ YouTube แบบย่อ [วิธีการซิงโครไนส์ใบสั่งงานกับการรวม Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo)

## <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>การรวมกับ Microsoft Dynamics 365 for Field Service รวมถึงสินค้าคงคลังและข้อมูลโครงการ

ฟังก์ชันเพิ่มเติมในขั้นตอนที่สองนี้ มุ่งเน้นในการให้ข้อมูลเชิงลึกแก่ช่างเทคนิคภาคสนามเกี่ยวกับข้อมูลสินค้าคงคลังจาก Finance and Operations ซึ่งอนุญาตให้รายการเหล่านั้นปรับปรุงระดับสินค้าคงคลังและทำการโอนย้ายวัสดุ นอกจากนี้ บริษัทที่ติดตั้งหรือให้บริการซ่อมบำรุงสินค้าที่ขายไปแล้วจะได้รับประโยชน์จากการควบคุมที่ดีขึ้นและการมองเห็นการขายและกระบวนการบริการทั้งหมดพร้อมกับการรวมจากโครงการ

### <a name="functionality-includes-integration-of"></a>ฟังก์ชันประกอบด้วยการรวมของ:
- ข้อมูลคลังสินค้า
- ข้อมูลปริมาณสินค้าคงคลังคงเหลือ
- การโอนย้ายสินค้าคงคลัง
- การปรับปรุงสินค้าคงคลัง
- โครงการ Dynamics 365 for Finance and Operations ที่เชื่อมโยงกับใบสั่งงาน Dynamics 365 for Field Service
- ใบสั่งงาน Dynamics 365 for Field Service ที่มีลิงค์ไปยังโครงการ Dynamics 365 for Finance and Operations นำหมายเลขโครงการนี้ไปใช้กับใบสั่งขาย Dynamics 365 for Finance and Operations เพื่ออนุญาตให้มีการออกใบแจ้งหนี้จากโครงการ 

![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>เฟสที่สองของการรวมระหว่าง Field Service และ Finance and Operations เปิดใช้งานการซิงโครไนส์ที่มีเท็มเพลตต่อไปนี้:
- คลังสินค้า (Fin and Ops ไปยัง Field Service) - คลังสินค้าจาก Finance and Operations ไปยัง Field Service [การสอบถามขั้นสูง] 
- สินค้าคงคลังของผลิตภัณฑ์ (Fin and Ops ไปยัง Field Service) - ข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service [การสอบถามขั้นสูง] 
- การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Fin and Ops) - การปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Finance and Operations [การสอบถามขั้นสูง] 
- การโอนย้ายสินค้าคงคลัง (Field Service ไปยัง Fin and Ops) - การโอนย้ายสินค้าคงคลังจาก Field Service ไปยัง Finance and Operations [การสอบถามขั้นสูง] 
- โครงการ (Fin and Ops ไปยัง Field Service) - รายการโครงการจาก Finance and Operations ไปยัง Field Service 
- ใบสั่งงานพร้อมกับโครงการ (Field Service ไปยัง Fin and Ops) - ใบสั่งงานใน Field Service ไปยัง Sales orders ใน Finance and Operations ที่มีการสนับสนุนสำหรับโครงการ [การสอบถามขั้นสูง] 
- ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Fin and Ops ไปยัง Sales) - Finance and Operations 'ผลิตภัณฑ์ที่นำออกใช้ที่สามารถขายได้' ไปยัง 'ผลิตภัณฑ์' Sales สำหรับ Field Service ซึ่งรวมถึงหน่วยสินค้าคงคลัง 

## <a name="system-requirements"></a>ความต้องการของระบบ

### <a name="system-requirements-for-finance-and-operations"></a>ความต้องการของระบบสำหรับ Finance and Operations
การรวม Field Service สนับสนุนเวอร์ชันต่อไปนี้:

- Dynamics 365 for Finance and Operations รุ่น 8.1.2 (ธันวาคม 2018) นำออกใช้ในเดือนธันวาคม 2018 และมีรุ่นของแอพลิเคชันหมายเลข 8.1.195 ที่มี Platform Update 22 (7.0.5095) 

### <a name="system-requirements-for-field-service"></a>ข้อกำหนดของระบบสำหรับ Field Service
เมื่อต้องการใช้โซลูชันการรวม Field Service คุณต้องติดตั้งส่วนประกอบต่อไปนี้:

- Field Service for Dynamics 365 (รุ่น 8.2.0.286) หรือรุ่นที่ใหม่กว่าใน Dynamics 365 9.1.x - นำออกใช้ในเดือนพฤศจิกายน 2018
- โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด (P2C) สำหรับ Dynamics 365 รุ่น 1.15.0.1 หรือรุ่นที่ใหม่กว่า โซลูชันนี้มีให้การดาวน์โหลดจาก [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)
- โซลูชัน 'การรวม Field Service โครงการและสินค้าคงคลัง' สำหรับ Dynamics 365 รุ่น 2.0.0.0 หรือรุ่นที่ใหม่กว่า โซลูชันนี้มีให้การดาวน์โหลดจาก [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2)
