---
title: ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังรายชื่อลูกค้าใน Supply Chain Management
description: หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้ในการซิงโครไนส์บัญชีจาก Dynamics 365 Sales ไปยัง Supply Chain Management
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 0499f604049240a226b4002710817034598b1e66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977724"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังรายชื่อลูกค้าใน Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> ก่อนที่คุณจะสามารถใช้โซลูชันผู้มีแนวโน้มจะเป็นลูกค้าเงินสด คุณควรคุ้นเคยกับ [รวมข้อมูลลงใน Microsoft Dataverse สำหรับแอป](https://docs.microsoft.com/powerapps/administrator/data-integrator)

หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้ในการซิงโครไนส์บัญชีจาก Dynamics 365 Sales ไปยัง Dynamics 365 Supply Chain Management โดยตรง

## <a name="data-flow-in-prospect-to-cash"></a>โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด

โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Supply Chain Management และ Sales  แม่แบบของผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสดที่มีให้ใช้งานร่วมกันกับคุณลักษณะการรวมข้อมูล ช่วยให้เกิดกระแสของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Supply Chain Management และ Sales ภาพประกอบต่อไปนี้ แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Supply Chain Management และ Sales

[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

เมื่อต้องการเข้าถึงแม่แบบที่พร้อมใช้งาน ให้เปิด [Power Apps ศูนย์การจัดการ](https://preview.admin.powerapps.com/dataintegration) เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

แม่แบบและงานพื้นฐานต่อไปนี้ จะถูกใช้ในการซิงโครไนส์บัญชีจาก Sales ไปยัง Supply Chain Management:

- **ชื่อของเท็มเพลตในการรวมข้อมูล:** บัญชี (Sales ไปยัง Fin and Ops) - ตรง
- **ชื่อของงานในโครงการ:** บัญชี - ลูกค้า

ไม่มีงานในการซิงโครไนส์จำเป็นต้องใช้ ก่อนการซิงโครไนส์บัญชี/ลูกค้าจะสามารถเกิดขึ้นได้

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| ใบสั่งขาย    | Supply Chain Management |
|----------|------------------------|
| บัญชี | ลูกค้า V2           |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

บัญชีที่ได้รับการจัดการใน Sales จะถูกซิงโครไนส์ไปยัง Supply Chain Management ในฐานะลูกค้า คุณสมบัติ **ถูกรักษาไว้สำหรับภายนอก** ในลูกค้าเหล่านี้ถูกตั้งค่าเป็น **ใช่** เพื่อติดตามลูกค้าที่มีต้นกำเนิดมาจาก Sales ในระหว่างการออกใบแจ้งหนี้ ข้อมูลนี้จะถูกใช้เพื่อกรองข้อมูลใบแจ้งหนี้ที่ถูกซิงค์โครไนซ์ไปยัง Sales

## <a name="prospect-to-cash-solution-for-sales"></a>โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales

คอลัมน์ **หมายเลขบัญชี** จะพร้อมใช้งานบนหน้า **บัญชี** ซึ่งถูกทำให้เป็นคีย์เฉพาะและธรรมชาติ เพื่อสนับสนุนการรวม คุณลักษณะคีย์ธรรมชาติของโซลูชัน Customer Relationship Management (CRM) อาจส่งผลกระทบต่อลูกค้าที่ใช้คอลัมน์ **หมายเลขบัญชี** อยู่แล้ว แต่จะไม่ส่งผลกระทบต่อลูกค้าที่ไม่ได้ใช้ค่า **หมายเลขบัญชี** สำหรับแต่ละบัญชี ในปัจจุบัน โซลูชันการรวมไม่สนับสนุนกรณีนี้

เมื่อมีการสร้างบัญชีใหม่ ถ้าค่า **หมายเลขบัญชี** ไม่ได้มีอยู่แล้ว ระบบจะสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข ค่าประกอบด้วย **ACC** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้นแล้วจึงตามด้วยคำต่อท้ายหกอักขระ นี่คือตัวอย่าง: **ACC-01000-BVRCPS**

เมื่อมีการใช้โซลูชันการรวมสำหรับ Sales สคริปต์การอัพเกรดจะตั้งค่าคอลัมน์ **หมายเลขบัญชี** สำหรับบัญชีที่มีอยู่ใน Sales ถ้าไม่มีค่า **หมายเลขบัญชี** ลำดับหมายเลขที่ได้กล่าวถึงก่อนหน้านี้จะถูกนำมาใช้

## <a name="preconditions-and-mapping-setup"></a>การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป

- การแม็ป **CustomerGroupId** จะต้องถูกอัพเดตเพื่อให้เป็นค่าที่ถูกต้องใน Supply Chain Management คุณสามารถระบุค่าเริ่มต้น หรือคุณสามารถตั้งค่าโดยใช้แผนผังค่า

    ค่าเท็มเพลตเริ่มต้นคือ **10**

- โดยการเพิ่มการแม็ปต่อไปนี้ คุณสามารถช่วยลดจำนวนการอัพเดตที่จำเป็นด้วยตนเองใน Supply Chain Management ได้ คุณสามารถใช้ค่าเริ่มต้นค่าหรือแผนผังค่าจาก ตัวอย่างเช่น **ประเทศ/ภูมิภาค** หรือ **เมือง** ได้

    - **SiteId** – จำเป็นต้องมีไซต์เพื่อสร้างรายการใบเสนอราคาและใบสั่งขายใน Supply Chain Management สามารถนำไซต์เริ่มต้นจากผลิตภัณฑ์หรือจากลูกค้าอย่างใดอย่างหนึ่งจากส่วนหน้าของใบสั่งได้

        ค่าเท็มเพลตเริ่มต้นคือ **1**

    - **WarehouseId** – จำเป็นต้องมีคลังสินค้าเพื่อดำเนินการกับรายการใบเสนอราคาและใบสั่งขายใน Supply Chain Management สามารถนำคลังสินค้าเริ่มต้นจากผลิตภัณฑ์หรือจากลูกค้าอย่างใดอย่างหนึ่งจากส่วนหน้าของใบสั่งใน Supply Chain Management ได้

        ค่าเท็มเพลตเริ่มต้นคือ **13**

    - **LanguageId** – จำเป็นต้องมีภาษาเพื่อสร้างรายการใบเสนอราคาและใบสั่งขายใน Supply Chain Management โดยค่าเริ่มต้น จะใช้ภาษาจากส่วนหน้าของใบสั่งจากลูกค้า

        ค่าเท็มเพลตเริ่มต้นคือ **en-us**

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

> [!NOTE]
> คอลัมน์ **เงื่อนไขการชำระเงิน** **เงื่อนไขการขนส่ง** **เงื่อนไขการจัดส่ง** **วิธีการจัดส่ง** และ **โหมดการจัดส่ง** ไม่ได้รวมอยู่ในการแม็ปเริ่มต้น หากต้องการแม็ปคอลัมน์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เฉพาะเจาะจงสำหรับข้อมูลในองค์กรที่ตารางถูกซิงโครไนส์

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล 

> [!NOTE]
> การแม็ปจะช่วยแสดงให้เห็นว่า ข้อมูลคอลัมน์ใดที่จะถูกซิงโครไนส์จาก Sales ไปยัง Supply Chain Management

![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>หัวข้อที่เกี่ยวข้อง


[ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสด](prospect-to-cash.md)

[ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังรายชื่อลูกค้าใน Supply Chain Management](accounts-template-mapping-direct.md)

[ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อหรือรายชื่อลูกค้าใน Supply Chain Management](contacts-template-mapping-direct.md)

[การซิงโครไนส์ใบสั่งขายโดยตรงระหว่าง Sales และ Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Supply Chain Management ไปยัง Sales](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]