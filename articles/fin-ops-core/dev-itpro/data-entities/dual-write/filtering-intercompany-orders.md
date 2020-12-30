---
title: กรองใบสั่งระหว่างบริษัทเพื่อหลีกเลี่ยงการซิงโครไนส์ใบสั่งและรายการใบสั่ง
description: หัวจ้อนี้อธบายวิธีการกรองใบสั่งระหว่างบริษัทเพื่อหลีกเลี่ยงการซิงโครไนส์ใบสั่งและรายการใบสั่ง
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701044"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>กรองใบสั่งระหว่างบริษัทเพื่อหลีกเลี่ยงการซิงโครไนส์ใบสั่งและรายการใบสั่ง

[!include [banner](../../includes/banner.md)]

คุณสามารถกรองใบสั่งระหว่างบริษัทเพื่อหลีกเลี่ยงการซิงโครไนส์เอนทิตี **ใบสั่ง** และ **รายการใบสั่ง** ในบางสถานการณ์ รายละเอียดของใบสั่งระหว่างบริษัทไม่จำเป็นในแอปการมีส่วนร่วมของลูกค้า

แต่ละเอนทิตี Common Data Service มาตรฐานจะถูกขยายโดยมีการอ้างอิงไปยังฟิลด์ **IntercompanyOrder** และแผนผังแบบการรวมแบบสองทิศทางได้รับการแก้ไขเพื่ออ้างอิงถึงฟิลด์เพิ่มเติมในตัวกรองข้อมูล ผลลัพธ์คือใบสั่งระหว่างบริษัทจะไม่มีการซิงโครไนส์อีกต่อไป กระบวนการนี้จะหลีกเลี่ยงข้อมูลที่ไม่จำเป็นในแอปการมีส่วนร่วมของลูกค้า

1. เพิ่มการอ้างอิงถึง **IntercompanyOrder** ลงใน **หัวข้อของใบสั่งขาย CDS** มีการเติมข้อมูลในใบสั่งระหว่างบริษัทเท่านั้น ฟิลด์ **IntercompanyOrder** มีอยู่ใน **SalesTable**

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="แม็ปการแบ่งระยะไปยังเป้าหมาย SalesOrderHeader":::
    
2. หลังจากที่ **หัวข้อของใบสั่งขายของ CDS** ถูกขยายแล้ว ฟิลด์ **IntercompanyOrder** จะพร้อมใช้งานในการแม็ป ใช้ตัวกรองข้อมูลกับ `INTERCOMPANYORDER == ""` เป็นสตริงการสอบถาม

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="หัวข้อของใบสั่งขาย แก้ไขการสอบถาม":::

3. เพิ่มการอ้างอิงให้ **IntercompanyInventTransId** กับ **บรรทัดใบสั่งขาย CDS**  มีการเติมข้อมูลในใบสั่งระหว่างบริษัทเท่านั้น ฟิลด์ **InterCompanyInventTransID** มีอยู่ใน **SalesLine**

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="แม็ปการแบ่งระยะไปยังเป้าหมาย SalesOrderLine":::

4. หลังจากที่ **รายการใบสั่งขายของ CDS** ถูกขยายแล้ว ฟิลด์ **IntercompanyInventTransId** จะพร้อมใช้งานในการแม็ป ใช้ตัวกรองข้อมูลกับ `INTERCOMPANYINVENTTRANSID == ""` เป็นสตริงการสอบถาม

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="รายการใบสั่งขาย แก้ไขการสอบถาม":::

5. ขยาย **หัวข้อของใบแจ้งหนี้การขาย V2** และ **บรรทัดใบแจ้งหนี้การขาย V2** ในลักษณะเดียวกับที่คุณขยายเอนทิตี Common Data Service ในขั้นตอนที่ 1 และ 2 เพิ่มการสอบถามตัวกรอง สตริงตัวกรองสำหรับ **หัวข้อของใบแจ้งหนี้การขาย V2** คือ `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` สตริงตัวกรองสำหรับ **รายการใบแจ้งหนี้การขาย V2** คือ `INTERCOMPANYINVENTTRANSID == ""`

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="แม็ปการแบ่งระยะไปยังเป้าหมาย หัวข้อของใบแจ้งหนี้การขาย":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="หัวข้อของใบแจ้งหนี้การขาย แก้ไขการสอบถาม":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="รายการของใบแจ้งหนี้การขาย แก้ไขการสอบถาม":::

6. เอนทิตี **ใบเสนอราคา** ไม่มีความสัมพันธ์ระหว่างบริษัท ถ้ามีบุคคลสร้างใบเสนอราคาสำหรับลูกค้าระหว่างบริษัทอย่างใดอย่างหนึ่ง คุณสามารถกำหนดลูกค้าเหล่านี้ทั้งหมดในกลุ่มลูกค้าหนึ่งกลุ่มโดยใช้ฟิลด์ **CustGroup**  หัวข้อและบรรทัดสามารถขยายเพื่อเพิ่มฟิลด์ **CustGroup** แล้วกรองเพื่อไม่รวมกลุ่มนี้

    :::image type="content" source="media/filter-cust-group.png" alt-text="แม็ปการแบ่งระยะไปยังเป้าหมาย หัวข้อของใบเสนอราคาการขาย":::

7. หลังจากที่คุณขยายใช้เอนทิตี **ใบเสนอราคา** แล้ว ให้ใช้ตัวกรองข้อมูลกับ `CUSTGROUP !=  "<company>"` เป็นสตริงการสอบถาม

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="หัวข้อของใบเสนอราคาขาย แก้ไขการสอบถาม":::
