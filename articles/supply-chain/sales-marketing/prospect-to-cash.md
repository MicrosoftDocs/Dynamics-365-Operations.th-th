---
title: "ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด"
description: "หัวข้อแสดงภาพรวมของโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดระหว่าง Dynamics 365 for Finance and Operations, Enterprise edition และ Dynamics 365 for Sales"
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a>ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด  

[!include[banner](../includes/banner.md)]

โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดใช้ [การรวมข้อมูล](/common-data-service/entity-reference/dynamics-365-integration) ในการซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition และ Dynamics 365 for Sales ผ่าน Common Data Service (CDS) เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูลจะเปิดใช้งานขั้นตอนของข้อมูลบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales ขณะที่มีการถ่ายโอนข้อมูลระหว่าง Finance and Operations และ Sales คุณสามารถดำเนินกิจกรรมการขายและการตลาดใน Dynamics 365 สำหรับการขาย และจัดการกระบวนการเติมสินค้าตามใบสั่งใน Finance and Operations ได้ 

โซลูชันนี้มีการรวมในพื้นที่ต่อไปนี้: 

-   [รักษาบัญชีใน Sales และซิงโครไนส์กับ Finance and Operations](accounts-template-mapping.md)
-   [รักษาผู้ติดต่อใน Sales และซิงโครไนส์กับ Finance and Operations](contacts-template-mapping.md)
-   [รักษาผลิตภัณฑ์ใน Finance and Operations และซิงโครไนส์กับ Sales](products-template-mapping.md)
-   [สร้างใบเสนอราคาขายใน Sales และซิงโครไนส์กับ Finance and Operations](sales-quotation-template-mapping.md)
-   [สร้างใบสั่งขายใน Finance and Operations และซิงโครไนส์กับ Sales](sales-order-template-mapping.md)
-   [สร้างใบแจ้งหนี้การขายใน Finance and Operations และซิงโครไนส์กับ Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>ความต้องการของระบบสำหรับ Dynamics 365 for Finance and Operations, Enterprise Edition

เมื่อต้องการใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องติดตั้งสิ่งต่อไปนี้:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (กรกฎาคม 2017) พร้อมกับการอัพเดตแพลตฟอร์ม 8 (แอพลิเคชัน 7.2.11792.56024 พร้อมกับแพลตฟอร์ม 7.0.4565.16212)

- โปรแกรมแก้ไขด่วนสองรายการสำหรับ Dynamics 365 for Finance and Operations, Enterprise edition (กรกฎาคม 2017)

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) -โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์บรรทัดใบสั่งขายกับคุณลักษณะการรวมข้อมูลจาก Finance and Operations ไปยัง Sales
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) -โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์บรรทัดใบสั่งขายกับคุณลักษณะการรวมข้อมูลจาก Finance and Operations ไปยัง Sales
    
**หมายเหตุ**: คุณเพียงต้องติดตั้ง KB4036524 เนื่องจากการติดตั้งมีการเปลี่ยนแปลงจาก KB4036461
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>ข้อกำหนดของระบบสำหรับ Dynamics 365 for Sales

เมื่อต้องการใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องติดตั้งสิ่งต่อไปนี้:

- Dynamics 365 for Sales เวอร์ชัน 1612 (8.2.1.207) (DB 8.2.1.207) ออนไลน์ หรือใหม่กว่า
- โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Dynamics 365 for Sales เวอร์ชัน 1.14.0.0 (v14) หรือใหม่กว่า

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>ติดตั้งโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales

- ดาวน์โหลด [ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับไฟล์ Zip ของแพคเกจโซลูชัน Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) ใน CustomerSource

- ตรวจสอบว่าไฟล์ Zip ไม่ถูกบล็อคเพื่อที่คุณจะได้ไม่ได้รับข้อความแสดงข้อผิดพลาด "ไม่พบแพคเกจการนำเข้า" เมื่อคุณติดตั้งแพคเกจโซลูชัน เมื่อต้องการยกเลิกการบล็อคไฟล์ ให้ทำสิ่งต่อไปนี้:

    -  คลิกขวาที่ไฟล์ Zip
    -  เลือก **คุณสมบัติ** แล้วเลือก **ยกเลิกการบล็อค** 

- Unzip และรัน PackageDeployer.exe

- ติดตั้งโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดในอินสแตนซ์ Sales ของคุณ

    - เลือกชนิดการปรับใช้ **Office 365**
    - เลือก **แสดงขั้นสูง**
    - สำหรับการติดตั้งด่วน เลือก **ภูมิภาค** ถ้าคุณเลือก **ไม่ทราบ** ระบบจะค้นหาทุกภูมิภาค และจะใช้เวลานานในการติดตั้ง
    - ป้อน **ชื่อผู้ใช้** และ **รหัสผ่าน** สำหรับผู้ดูแลที่มีสิทธิ์ของผู้ใช้ในการติดตั้ง

