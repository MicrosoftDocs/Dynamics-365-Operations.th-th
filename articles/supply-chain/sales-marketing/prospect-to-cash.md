---
title: "ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด"
description: "หัวข้อนี้แสดงภาพรวมของโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดระหว่าง Microsoft Dynamics 365 for Finance and Operations, Enterprise edition และ Microsoft Dynamics 365 for Sales"
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: th-th
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a>ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด

[!include[banner](../includes/banner.md)]

โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดให้การซิงโครไนส์โดยตรงระหว่าง Microsoft Dynamics 365 for Finance and Operations, Enterprise edition และ Microsoft Dynamics 365 for Sales เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล จะเปิดใช้งานโฟลว์ของข้อมูลสำหรับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales ขณะที่มีการถ่ายโอนข้อมูลระหว่าง Finance and Operations และ Sales คุณสามารถดำเนินกิจกรรมการขายและการตลาดใน Sales และคุณสามารถจัดการการเติมสินค้าตามใบสั่งโดยใช้การบริหารสินค้าคงคลัง Finance and Operations ได้

ในเวอร์ชันปัจจุบัน โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดแสดงชนิดของการซิงโครไนส์โดยตรงต่อไปนี้:

- [รักษาบัญชีใน Sales และซิงโครไนส์โดยตรงจาก Sales ไปยัง Finance and Operations](accounts-template-mapping-direct.md)
- [รักษาผลิตภัณฑ์ใน Finance and Operations และซิงโครไนส์โดยตรงกับ Sales](products-template-mapping-direct.md)
- [รักษาผู้ติดต่อใน Sales และซิงโครไนส์โดยตรงไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations](contacts-template-mapping-direct.md)
- [ซิงโครไนส์ใบเสนอราคาขายโดยตรงจาก Sales ไปยัง Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [ซิงโครไนส์ใบสั่งขายโดยตรงจาก Finance and Operations ไปยัง Sales](sales-order-template-mapping-direct.md)
- [ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงระหว่าง Sales และ Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
- [ซิงโครไนส์ใบแจ้งหนี้การขายโดยตรงจาก Finance and Operations ไปยัง Sales](sales-invoice-template-mapping-direct.md)

ในเวอร์ชันก่อนหน้า โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดแสดงชนิดของการซิงโครไนส์ที่ไม่ใช่โดยตรงต่อไปนี้:

- [รักษาบัญชีใน Sales และซิงโครไนส์กับ Finance and Operations](accounts-template-mapping.md)
- [รักษาผู้ติดต่อใน Sales และซิงโครไนส์กับ Finance and Operations](contacts-template-mapping.md)
- [รักษาผลิตภัณฑ์ใน Finance and Operations และซิงโครไนส์กับ Sales](products-template-mapping.md)
- [สร้างใบเสนอราคาขายใน Sales และซิงโครไนส์กับ Finance and Operations](sales-quotation-template-mapping.md)
- [สร้างใบสั่งขายใน Finance and Operations และซิงโครไนส์กับ Sales](sales-order-template-mapping.md)
- [สร้างใบแจ้งหนี้การขายใน Finance and Operations และซิงโครไนส์กับ Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>ความต้องการของระบบสำหรับ Finance and Operations

เมื่อต้องการใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องติดตั้งส่วนประกอบต่อไปนี้:

### <a name="july-2017"></a>กรกฎาคม 2017 

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (กรกฎาคม 2017) พร้อมกับการอัพเดตแพลตฟอร์ม 8 (การสร้างแอพลิเคชัน 7.2.11792.56024 พร้อมกับการสร้างแพลตฟอร์ม 7.0.4565.16212)
- โปรแกรมแก้ไขด่วนต่อไปนี้สำหรับ Finance and Operations:

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์ใบสั่งขายจาก Sales ไปยัง Finance and Operations ผ่านทางคุณลักษณะการรวมข้อมูล ยังมีการปรับปรุงอื่นๆ อีกหลายส่วน
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์รายการใบสั่งขายจาก Finance and Operations ไปยัง Sales ผ่านทางคุณลักษณะการรวมข้อมูล
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์ใบสั่งขายจาก Finance and Operations ไปยัง Sales ผ่านทางคุณลักษณะการรวมข้อมูล

    > [!NOTE]
    > คุณเพียงต้องติดตั้ง KB4045570 เนื่องจากการติดตั้งรวมการเปลี่ยนแปลงจากบทความ Microsoft Knowledge Base (KB) อื่นๆ

### <a name="november-2016-version-1611"></a>พฤศจิกายน 2016 (รุ่น 1611)

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (พฤศจิกายน 2016) การอัพเดตแพลตฟอร์ม 8 หรือสูงกว่า

- โปรแกรมแก้ไขด่วนต่อไปนี้สำหรับ Finance and Operations:

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - เปิดใช้งานการซิงโครไนส์ใบสั่งขายกับตัวรวมข้อมูลจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Sales 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - เปิดใช้งานการซิงโครไนส์ใบสั่งขายกับตัวรวมข้อมูลจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Sales
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - จำเป็นต้องมีการสนับสนุนสำหรับการรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดผ่านทางเอนทิตีข้อมูล
    
    > [!NOTE]
    > หลังจากติดตั้งโปรแกรมแก้ไขด่วน คุณต้องทริกเกอร์ชุดงานต่อไปนี้จากแบบฟอร์ม SalesPopulateProspectToCash แบบฟอร์มนี้ถูกซ่อนไว้ เนื่องจากคุณต้องการเพียงครั้งเดียว เพื่อเข้าถึงรายการนี้ ให้เพิ่มรายการต่อไปนี้ไปยังที่อยู่เบราเซอร์ของคุณ เมื่อมีการล็อกอินเข้าสู่สภาพแวดล้อม: &mi=action:SalesPopulateProspectToCash เช่น https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash ในแบบฟอร์มที่เปิด คลิกตกลง
    การดำเนินการนี้จะเติมข้อมูลในฟิลด์ "LineCreationSequnceNumber" ใหม่ ในตาราง "SalesLine" "SalesQuotationLine" และ "CustInvoiceTrans" ด้วยค่าที่ไม่ซ้ำกัน และรีเฟรชรายการผลิตภัณฑ์ ซึ่งจำเป็นสำหรับการรวม P2C กับงานบน 7.1


## <a name="system-requirements-for-sales"></a>ความต้องการของระบบสำหรับ Sales

เมื่อต้องการใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องติดตั้งส่วนประกอบต่อไปนี้:

- Microsoft Dynamics 365 for Sales รุ่น 1612 (8.2.1.207) (DB 8.2.1.207) ออนไลน์
- โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Microsoft Dynamics 365 for Sales รุ่น 1.15.0.0 (v15) 

   > [!NOTE]
   >
   > เท็มเพลตที่มีรุ่น 1.0.0.0 และ 1.0.0.1 ได้รับการสนับสนุนบนโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Microsoft Dynamics 365 for Sales รุ่น 1.14.1.0
   >
   > เท็มเพลตที่มีรุ่น 2.0.0.0 และ 2.1.0.0 ได้รับการสนับสนุนบนโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Microsoft Dynamics 365 for Sales รุ่น 1.15.0.0

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>ติดตั้งโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales

1. ดาวน์โหลด [ไฟล์ Zip ของแพคเกจโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) จาก CustomerSource
2. ต้องแน่ใจว่าไฟล์ Zip ไม่ถูกบล็อค มิฉะนั้น เมื่อคุณพยายามติดตั้งแพคเกจโซลูชัน คุณได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ไม่พบแพคเกจนำเข้า" เพื่อยกเลิกการบล็อคไฟล์ Zip คลิกขวา แล้วเลือก **คุณสมบัติ** จากนั้น เลือก **ยกเลิกการบล็อก**
3. Unzip และรัน **PackageDeployer.exe**
4. ติดตั้งโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดบนอินสแตนซ์ Sales ของคุณ

    1. เลือก **Office 365** เป็นชนิดการปรับใช้
    2. เลือก **แสดงขั้นสูง**
    3. สำหรับการติดตั้งด่วน เลือกภูมิภาค ถ้าคุณเลือก **ไม่ทราบ** ระบบจะค้นหาทุกภูมิภาค และจะใช้เวลานานมากขึ้นในการติดตั้ง
    4. ป้อนชื่อผู้ใช้และรหัสผ่านของผู้ใช้ที่เป็นผู้ดูแลระบบที่มีสิทธิ์ในการติดตั้ง

