---
title: การรวมข้อมูลกับภาพรวมของ Microsoft Dynamics 365 Field Service
description: บทความนี้แสดงภาพรวมของการรวมกับ Microsoft Dynamics 365 Field Service
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 12a9c57e2587150914c6087c041d63af9783c1f3
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103715"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>การรวมข้อมูลกับภาพรวมของ Microsoft Dynamics 365 Field Service

[!include[banner](../includes/banner.md)]



Supply Chain Management ทำให้เกิดการซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Dynamics 365 Supply Chain Management และ Dynamics 365 Field Service สถานการณ์จำลองของการรวมถูกตั้งค่าคอนฟิกโดยใช้เทมเพลตตัวรวมข้อมูลที่ขยายได้ และ Microsoft Dataverse เพื่อเปิดใช้งานการซิงโครไนส์ของกระบวนการทางธุรกิจ
เทมเพลตมาตรฐานสามารถใช้เพื่อสร้างโครงการที่มีการรวมแบบกำหนดเอง ที่ซึ่งคอลัมน์มาตรฐานและแบบกำหนดเองเพิ่มเติมและตาราง สามารถถูกแมปเพื่อปรับปรุงการรวม และให้ตรงตามความต้องการทางธุรกิจเฉพาะ 

สร้างการรวมบริการฟิลด์ด้านบนสุดฟังก์ชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่มีอยู่

![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/field-service-integration.png)

เฟสแรกของการรวมระหว่าง Field Service และ Supply Chain Management จะเน้นบนการเปิดใช้งานใบสั่งผลิตและข้อตกลงใน Field Service ที่จะถูกจัดทำใน Supply Chain Management ขั้นตอนที่ได้รับการสนับสนุนเริ่มต้นใน Field Service ซึ่งข้อมูลจากใบสั่งผลิตจะถูกซิงโครไนส์ไปยัง Supply Chain Management ในรูปแบบของใบสั่งขาย ใน Supply Chain Management ใบสั่งขายจะถูกจัดทำขึ้นเพื่อสร้างเอกสารใบแจ้งหนี้ นอกจากนี้ ข้อมูลในใบแจ้งหนี้ตามข้อตกลงของ Field Service จะซิงโครไนส์ไปยัง Supply Chain Management ตัวรวมข้อมูล Microsoft Dynamics 365 ซิงโครไนส์ข้อมูลโดยใช้โครงการที่กำหนดเองได้ เทมเพลตมาตรฐานสามารถใช้เพื่อสร้างโครงการที่มีการรวมแบบกำหนดเอง ที่ซึ่งคอลัมน์มาตรฐานและแบบกำหนดเองเพิ่มเติม และรวมทั้งตาราง สามารถถูกแมปเพื่อปรับปรุงการรวม และให้ตรงตามข้อกำหนดเฉพาะ

เฟสแรกของการรวมระหว่าง Field Service และ Supply Chain Management ทำให้สามารถซิงโครไนส์รายการดังต่อไปนี้:

- [การซิงโครไนส์ผลิตภัณฑ์จาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Field Service](field-service-product.md)
- [ซิงโครไนส์ใบสั่งงานใน Field Service กับใบสั่งขายเข้าด้วยกันใน Supply Chain Management](field-service-work-order.md)
- [การซิงโครไนส์ข้อตกลงของใบแจ้งหนี้ใน Field Service ไปยังใบแจ้งหนี้ข้อความอิสระใน Supply Chain Management](field-service-invoice.md)

เพื่อดูตัวอย่างของวิธีการซิงโครไนส์ใบสั่งงานระหว่าง Field Service และ Supply Chain Management ดูวิดีโอ YouTube แบบย่อ [วิธีการซิงโครไนส์ใบสั่งงานกับการรวม Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo)

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>การรวมกับ Field Service รวมถึงสินค้าคงคลังและข้อมูลโครงการ

ฟังก์ชันเพิ่มเติมในเฟสที่สองนี้ เน้นไปที่การให้ข้อมูลเชิงลึกแก่ช่างเทคนิคภาคสนามเกี่ยวกับข้อมูลสินค้าคงคลังจาก Supply Chain Management โดยยินยอมให้ช่างเทคนิคทำการปรับปรุงระดับสินค้าคงคลังและทำการโอนย้ายวัสดุได้ นอกจากนี้ บริษัทที่ติดตั้งหรือให้บริการซ่อมบำรุงสินค้าที่ขายไปแล้วจะได้รับประโยชน์จากการควบคุมที่ดีขึ้นและการมองเห็นการขายและกระบวนการบริการทั้งหมดพร้อมกับการรวมจากโครงการ

### <a name="functionality-includes-integration-of"></a>ฟังก์ชันประกอบด้วยการรวมของ:
- ข้อมูลคลังสินค้า
- ข้อมูลปริมาณสินค้าคงคลังคงเหลือ
- การโอนย้ายสินค้าคงคลัง
- การปรับปรุงสินค้าคงคลัง
- Supply Chain Management ที่เชื่อมโยงกับใบสั่งงานของ Dynamics 365 Field Service
- ใบสั่งงานของ Dynamics 365 Field Service ที่มีลิงก์ไปยังโครงการ Supply Chain Management นำหมายเลขโครงการนี้ไปใช้กับใบสั่งขาย เพื่ออนุญาตให้มีการจัดทำใบแจ้งหนี้จากโครงการ 

![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service ซึ่งรวมถึงข้อมูลสินค้าคงคลังและโครงการ](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>เฟสที่สองของการรวมระหว่าง Field Service และ Supply Chain Management สามารถซิงโครไนส์กับเทมเพลตดังต่อไปนี้:
- คลังสินค้า (Supply Chain Management to Field Service) - คลังสินค้าจาก Supply Chain Management to Field Service [การจัดการขั้นสูง] 
- คลังสินค้า (Supply Chain Management to Field Service) - ข้อมูลปริมาณคลังสินค้าจาก Supply Chain Management to Field Service [การจัดการขั้นสูง] 
- การปรับปรุงคลังสินค้า (Supply Chain Management to Field Service) - การปรับปรุงคลังสินค้าจาก Field Service to Supply Chain Management [การจัดการขั้นสูง] 
- การปรับปรุงคลังสินค้า (Supply Chain Management to Field Service) - การปรับปรุงคลังสินค้าจาก Field Service to Supply Chain Management [การจัดการขั้นสูง] 
- คลังสินค้า (Supply Chain Management to Field Service) - รายชื่อโครงการจาก Supply Chain Management to Field Service [การจัดการขั้นสูง] 
- ใบสั่งงานพร้อมกับโครงการ (Field Service ไปยัง Supply Chain Management) - ใบสั่งงานใน Field Service ไปยังใบสั่งขาย ใน Supply Chain Management ที่มีการสนับสนุนสำหรับโครงการ [การจัดการขั้นสูง] 
- ผลิตภัณฑ์ของ Field Service ที่มีหน่วยสินค้าคงคลัง (Supply Chain Management ไปยัง Sales) - รายการ 'ผลิตภัณฑ์ที่สามารถนำออกไปขายได้' ใน Supply Chain Management ไปยัง รายการ 'ผลิตภัณฑ์' ที่จะขายใน Field Service รวมถึงหน่วยสินค้าคงคลัง 

## <a name="system-requirements"></a>ความต้องการของระบบ

### <a name="system-requirements-for-supply-chain-management"></a>ระบบต้องใช้กับ Supply Chain Management
การรวม Field Service สนับสนุนเวอร์ชันต่อไปนี้:

- Dynamics 365 การเงินและการดำเนินงาน รุ่น 8.1.2 (ธันวาคม 2018) ถูกนำออกใช้ในเดือนธันวาคม 2018 และมีการสร้างแอพลิเคชันหมายเลข 8.1.195 ที่มีการอัพเดแพลตฟอร์ม 22 (7.0.5095) 

### <a name="system-requirements-for-field-service"></a>ข้อกำหนดของระบบสำหรับ Field Service
เมื่อต้องการใช้โซลูชันการรวม Field Service คุณต้องติดตั้งส่วนประกอบต่อไปนี้:

- Field Service (รุ่น 8.2.0.286) หรือรุ่นที่ใหม่กว่าใน Dynamics 365 9.1.x - ที่เริ่มใช้ในเดือนพฤศจิกายน 2018
- โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด (P2C) สำหรับ Dynamics 365 รุ่น 1.15.0.1 หรือรุ่นที่ใหม่กว่า โซลูชันนี้มีให้การดาวน์โหลดจาก [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)
- โซลูชัน 'การรวม Field Service โครงการและสินค้าคงคลัง' สำหรับ Dynamics 365 รุ่น 2.0.0.0 หรือรุ่นที่ใหม่กว่า โซลูชันนี้มีให้การดาวน์โหลดจาก [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
