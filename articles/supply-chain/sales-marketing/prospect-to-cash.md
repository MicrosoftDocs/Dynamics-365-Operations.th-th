---
title: ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด
description: หัวข้อนี้แสดงภาพรวมของโซลูชันของผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสดระหว่าง Dynamics 365 Supply Chain Management และ Dynamics 365 Sales
author: ChristianRytt
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: bb928a14d231bef1255612194ec9fdeb9be8f611d26aa4dfbf3efaec8a8d3e9f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726692"
---
# <a name="prospect-to-cash"></a>ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสด

[!include [banner](../includes/banner.md)]

โซลูชั่นผู้ที่มีแนวโน้มจะเป็นลูกค้าเเงินสดให้การซิงโครไนส์โดยตรงระหว่าง Dynamics 365 Supply Chain Management และ Dynamics 365 Sales เท็มเพลตผู้ผู้ที่มีแนวโน้มจะเป็นลูกค้าเเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูลจะเปิดใช้งานโฟลว์ของข้อมูลสำหรับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขาย ในขณะที่มีการถ่ายโอนข้อมูล คุณสามารถดำเนินกิจกรรมส่งเสริมการขายและการตลาดใน Sales และคุณสามารถแฮนเดิลการเติมเต็มสินค้าตามใบสั่งโดยใช้การจัดการสินค้าคงคลังใน Supply Chain Management 

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ให้ดูวิดีโอ YouTube แบบย่อ [การรวมผู้ที่มีแนวโน้มจะเป็นลูกค้ากับเงินสด](https://www.youtube.com/watch?v=AVV9x5x-XCg)

ในเวอร์ชันปัจจุบัน โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดแสดงชนิดของการซิงโครไนส์โดยตรงต่อไปนี้:

- [ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังรายชื่อลูกค้าใน Supply Chain Management](accounts-template-mapping-direct.md)
- [ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Sales](products-template-mapping-direct.md)
- [ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อหรือรายชื่อลูกค้าใน Supply Chain Management](contacts-template-mapping-direct.md)
- [ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Sales ไปยัง Supply Chain Management](sales-quotation-template-mapping-sales-fin.md)
- [การซิงโครไนส์ใบสั่งขายโดยตรงระหว่าง Sales และ Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)
- [ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Supply Chain Management ไปยัง Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a>ระบบต้องใช้กับ Supply Chain Management
การรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดได้รับการสนับสนุนในรุ่นต่อไปนี้:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (ธันวาคม 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (ธันวาคม 2017) - รุ่นของแอพลิเคชัน 7.3.11971.56116 กับการอัพเดแพลตฟอร์ม 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise Edition (กรกฎาคม 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (กรกฎาคม 2017) - ที่มีการอัพเดตแพลตฟอร์ม 8 (รุ่นของแอพลิเคชัน 7.2.11792.56024 ที่มีบิลด์ของแพลตฟอร์ม 7.0.4565.16212)
- จำเป็นต้องมีโปรแกรมแก้ไขด่วนต่อไปนี้:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์ใบสั่งขายจาก Sales ไปยัง Supply Chain Management ผ่านทางคุณลักษณะการรวมข้อมูล ยังมีการปรับปรุงอื่นๆ อีกหลายส่วน
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์ใบสั่งขายจาก Supply Chain Management ไปยัง Sales ผ่านทางคุณลักษณะการรวมข้อมูล
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์ใบสั่งขายจาก Supply Chain Management ไปยัง Sales ผ่านทางคุณลักษณะการรวมข้อมูล

    > [!NOTE]
    > คุณเพียงต้องติดตั้ง KB4045570 เนื่องจากการติดตั้งรวมการเปลี่ยนแปลงจากของโปรแกรมแก้ไขด่วนอื่นๆ 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations รุ่น 1611 (พฤศจิกายน 2016)

- Dynamics 365 for Finance and Operations รุ่น 1611 (พฤศจิกายน 2016) ที่มีการอัพเดตแพลตฟอร์ม 8 หรือสูงกว่า

- จำเป็นต้องมีโปรแกรมแก้ไขด่วนต่อไปนี้:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - เปิดใช้งานการซิงโครไนส์ใบสั่งขายกับตัวรวมข้อมูลจาก Supply Chain Management ไปยัง Sales 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - เปิดใช้งานการซิงโครไนส์ส่วนหัวและรายการกับตัวรวมข้อมูลจาก Supply Chain Management ไปยัง Sales
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - จำเป็นต้องมีการสนับสนุนสำหรับการรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดผ่านทางเอนทิตีข้อมูล
    
    > [!NOTE]
    > หลังจากที่คุณติดตั้งโปรแกรมแก้ไขด่วน คุณต้องทริกเกอร์ชุดงานต่อไปนี้จากแบบฟอร์ม **SalesPopulateProspectToCash** แบบฟอร์มนี้ถูกซ่อนไว้ เนื่องจากคุณต้องการเพียงครั้งเดียว เพื่อเข้าถึงแบบฟอร์ม ให้ล็อกอินเข้าสู่สภาพแวดล้อม และเพิ่มรายการต่อไปนี้ไปยัง URL ในที่อยู่เบราเซอร์ของคุณ: *&mi=action:SalesPopulateProspectToCash* ตัวอย่างเช่น `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash` เมื่อแบบฟอร์มเปิดขึ้น คลิกตกลง การดำเนินการนี้จะเติมข้อมูลในฟิลด์ **LineCreationSequnceNumber** ใหม่ ในตาราง **SalesLine** **SalesQuotationLine** และ **CustInvoiceTrans** ด้วยค่าที่ไม่ซ้ำกัน และรีเฟรชรายการผลิตภัณฑ์ นี่เป็นสิ่งจำเป็นสำหรับการรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดกับการทำงาน


## <a name="system-requirements-for-sales"></a>ความต้องการของระบบสำหรับ Sales

เมื่อต้องการใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องติดตั้งส่วนประกอบต่อไปนี้:

- Dynamics 365 Sales รุ่น 1612 (8.2.1.207) (DB 8.2.1.207) ออนไลน์หรือรุ่นที่ใหม่กว่า
- โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสดสำหรับ Dynamics 365 Sales รุ่น 1.15.0.0 หรือรุ่นที่ใหม่กว่า โซลูชันนี้มีให้การดาวน์โหลดจาก AppSource [ดาวน์โหลด Dynamics 365 ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]