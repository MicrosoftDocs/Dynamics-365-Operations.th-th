---
title: "ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังลูกค้าใน Finance and Operations"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีจาก Microsoft Dynamics 365 for Sales ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition"
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 16bbca2d9eb8c3d9c33752404ebecbe4415517a2
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังลูกค้าใน Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> ก่อนที่คุณจะสามารถใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดได้ คุณควรทำความคุ้นเคยกับ [การรวมข้อมูล Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration)

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีโดยตรงจาก Microsoft Dynamics 365 for Sales ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition

## <a name="data-flow-in-prospect-to-cash"></a>โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด

โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Finance and Operations และ Sales  เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล จะเปิดใช้งานขั้นตอนของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Finance and Operations และ Sales

[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

เมื่อต้องการเข้าถึงเท็มเพลตที่พร้อมใช้งาน เปิด [ศูนย์การจัดการ PowerApps](https://preview.admin.powerapps.com/dataintegration) เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์บัญชีจาก Sales ไปยัง Finance and Operations:

- **ชื่อของเท็มเพลตในการรวมข้อมูล:** บัญชี (Sales ไปยัง Fin and Ops) - ตรง
- **ชื่อของงานในโครงการ:** บัญชี - ลูกค้า

ไม่มีงานในการซิงโครไนส์จำเป็นต้องใช้ ก่อนการซิงโครไนส์บัญชี/ลูกค้าจะสามารถเกิดขึ้นได้

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| ใบสั่งขาย    | Finance and Operations |
|----------|------------------------|
| บัญชี | ลูกค้า V2           |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

บัญชีจะถูกจัดการใน Sales และจะถูกซิงโครไนส์ไปยัง Finance and Operations ในฐานะลูกค้า คุณสมบัติ **ถูกรักษาไว้สำหรับภายนอก** ในลูกค้าเหล่านี้ถูกตั้งค่าเป็น **ใช่** เพื่อติดตามลูกค้าที่มีต้นกำเนิดมาจาก Sales ในระหว่างการออกใบแจ้งหนี้ ข้อมูลนี้จะถูกใช้เพื่อกรองข้อมูลใบแจ้งหนี้ที่ถูกซิงค์โครไนซ์ไปยัง Sales

## <a name="prospect-to-cash-solution-for-sales"></a>โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales

ฟิลด์ **หมายเลขบัญชี** จะพร้อมใช้งานบนหน้า **บัญชี** ซึ่งถูกทำให้เป็นคีย์เฉพาะและธรรมชาติ เพื่อสนับสนุนการรวม คุณลักษณะคีย์ธรรมชาติของโซลูชันการจัดการความสัมพันธ์กับลูกค้า (CRM) อาจส่งผลกระทบต่อลูกค้าที่ใช้ฟิลด์ **หมายเลขบัญชี** อยู่แล้ว แต่จะไม่ส่งผลกระทบต่อลูกค้าที่ไม่ได้ใช้ค่า **หมายเลขบัญชี** สำหรับแต่ละบัญชี ในปัจจุบัน โซลูชันการรวมไม่สนับสนุนกรณีนี้

เมื่อมีการสร้างบัญชีใหม่ ถ้าค่า **หมายเลขบัญชี** ไม่ได้มีอยู่แล้ว ระบบจะสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข ค่าประกอบด้วย **ACC** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้นแล้วจึงตามด้วยคำต่อท้ายหกอักขระ นี่คือตัวอย่าง: **ACC-01000-BVRCPS**

เมื่อมีการใช้โซลูชันการรวมสำหรับ Sales สคริปต์การอัพเกรดจะตั้งค่าฟิลด์ **หมายเลขบัญชี** สำหรับบัญชีที่มีอยู่ใน Sales ถ้าไม่มีค่า **หมายเลขบัญชี** ลำดับหมายเลขที่ได้กล่าวถึงก่อนหน้านี้จะถูกนำมาใช้

## <a name="preconditions-and-mapping-setup"></a>การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป

- การแม็ป **CustomerGroupId** จะต้องถูกอัพเดตเป็นค่าที่ถูกต้องใน Finance and Operations คุณสามารถระบุค่าเริ่มต้น หรือคุณสามารถตั้งค่าโดยใช้แผนผังค่า

    ค่าเท็มเพลตเริ่มต้นคือ **10**

- โดยการเพิ่มการแม็ปต่อไปนี้ คุณสามารถช่วยลดจำนวนการอัพเดตด้วยตนเองที่จำเป็นใน Finance and Operations ได้ คุณสามารถใช้ค่าเริ่มต้นค่าหรือแผนผังค่าจาก ตัวอย่างเช่น **ประเทศ/ภูมิภาค** หรือ **เมือง** ได้

    - **SiteId** – จำเป็นต้องมีไซต์เพื่อสร้างบรรทัดใบสั่งขายและใบเสนอราคาใน Finance and Operations สามารถนำไซต์เริ่มต้นจากผลิตภัณฑ์หรือจากลูกค้าอย่างใดอย่างหนึ่งจากส่วนหน้าของใบสั่งได้

        ค่าเท็มเพลตเริ่มต้นคือ **1**

    - **WarehouseId** – จำเป็นต้องมีคลังสินค้าเพื่อดำเนินการกับบรรทัดใบสั่งขายและใบเสนอราคาใน Finance and Operations สามารถนำคลังสินค้าเริ่มต้นจากผลิตภัณฑ์หรือจากลูกค้าอย่างใดอย่างหนึ่งจากส่วนหน้าของใบสั่งใน Finance and Operations ได้

        ค่าเท็มเพลตเริ่มต้นคือ **13**

    - **LanguageId** – จำเป็นต้องมีภาษาเพื่อสร้างใบเสนอราคาและใบสั่งขายใน Finance and Operations โดยค่าเริ่มต้น จะใช้ภาษาจากส่วนหน้าของใบสั่งจากลูกค้า

        ค่าเท็มเพลตเริ่มต้นคือ **en-us**

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

> [!NOTE]
> ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการจัดส่ง** และ **วิธีการจัดส่ง** ไม่ได้รวมอยู่ในการแม็ปเริ่มต้น หากต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่าง

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล 

> [!NOTE]
> การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Sales ไปยัง Finance and Operations

![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>หัวข้อที่เกี่ยวข้อง


[ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](prospect-to-cash.md)

[ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังลูกค้าใน Finance and Operations](accounts-template-mapping-direct.md)

[ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations](contacts-template-mapping-direct.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงจาก Finance and Operations ไปยัง Sales](sales-order-template-mapping-direct.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Finance and Operations ไปยัง Sales](sales-invoice-template-mapping-direct.md)


