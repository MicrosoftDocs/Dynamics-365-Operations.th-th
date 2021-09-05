---
title: กรองใบสั่งระหว่างบริษัท เพื่อหลีกเลี่ยงการซิงโครไนส์ใบสั่งและรายการใบสั่ง
description: หัวข้อนี้อธิบายวิธีการกรองใบสั่งระหว่างบริษัท เพื่อให้เอนทิตี้ ใบสั่ง และ รายการใบสั่ง ไม่ได้ซิงค์
author: negudava
ms.date: 11/09/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: negudava
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e09f2037645609d5b5b5d05f27bc5f094287ef03
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416964"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>กรองใบสั่งระหว่างบริษัท เพื่อหลีกเลี่ยงการซิงโครไนส์ใบสั่งและรายการใบสั่ง

[!include [banner](../../includes/banner.md)]

คุณสามารถกรองใบสั่งระหว่างบริษัท เพื่อให้ตาราง **ใบสั่ง** และ **รายการใบสั่ง** ไม่ได้ซิงค์ ในบางสถานการณ์ รายละเอียดของใบสั่งระหว่างบริษัทไม่จำเป็น ในแอปการมีส่วนร่วมของลูกค้า

แต่ละตาราง Dataverse มาตรฐานจะถูกขยายโดยมีการอ้างอิงไปยังคอลัมน์ **IntercompanyOrder** และแผนผังแบบการรวมแบบสองทิศทางได้รับการแก้ไข เพื่อให้อ้างอิงถึงฟิลด์เพิ่มเติมในตัวกรองข้อมูล ดังนั้น ใบสั่งระหว่างบริษัทจึงไม่ซิงค์อีกต่อไป กระบวนการนี้จะช่วยป้องกันข้อมูลที่ไม่จำเป็นในแอปการมีส่วนร่วมของลูกค้า

1. ขยายตาราง **ส่วนหัวของใบสั่งขาย CDS** โดยเพิ่มการอ้างอิงลงในคอลัมน์ **IntercompanyOrder** คอลัมน์นี้จะมีการเติมข้อมูลเฉพาะในใบสั่งระหว่างบริษัทเท่านั้น คอลัมน์ **IntercompanyOrder** มีอยู่ในตาราง **SalesTable**

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="แม็ปการจัดเตรียมไปยังหน้าเป้าหมายให้กับส่วนหัวของใบสั่งขาย CDS":::

2. หลังจากที่ **ส่วนหัวข้อของใบสั่งขาย CDS** ถูกขยายแล้ว คอลัมน์ **IntercompanyOrder** จะพร้อมใช้งานในการแม็ป ใช้ตัวกรองที่มี `INTERCOMPANYORDER == ""` เป็นสตริงการสอบถาม

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="แก้ไขกล่องโต้ตอบการสอบถามเกี่ยวกับส่วนหัวของใบสั่งขาย CDS":::

3. ขยายตาราง **บรรทัดของใบสั่งขาย CDS** โดยเพิ่มการอ้างอิงลงในคอลัมน์ **IntercompanyInventTransId** คอลัมน์นี้จะมีการเติมข้อมูลเฉพาะในใบสั่งระหว่างบริษัทเท่านั้น คอลัมน์ **InterCompanyInventTransId** มีอยู่ในตาราง **SalesLine**

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="แม็ปการจัดเตรียมไปยังหน้าเป้าหมายให้กับบรรทัดของใบสั่งขาย CDS":::

4. หลังจากที่ **รายการใบสั่งขายของ CDS** ถูกขยายแล้ว คอลัมน์ **IntercompanyInventTransId** จะพร้อมใช้งานในการแม็ป ใช้ตัวกรองที่มี `INTERCOMPANYINVENTTRANSID == ""` เป็นสตริงการสอบถาม

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="แก้ไขกล่องโต้ตอบการสอบถามเกี่ยวกับรายการของใบสั่งขาย CDS":::

5. ทําซ้ําขั้นตอนที่ 1 และ 2 เพื่อขยายตาราง **ส่วนหัวของใบแจ้งหนี้การขาย V2** และเพิ่มการสอบถามตัวกรอง ในกรณีนี้ ให้ใช้ `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` เป็นสตริงการสอบถามของตัวกรอง

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="แม็ปการจัดเตรียมไปยังหน้าเป้าหมายให้กับส่วนหัวของใบแจ้งหนี้ V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="แก้ไขกล่องโต้ตอบการสอบถามเกี่ยวกับส่วนหัวของใบแจ้งหนี้การขาย V2":::

6. ทําซ้ําขั้นตอนที่ 3 และ 4 เพื่อขยายตาราง **บรรทัดของใบแจ้งหนี้การขาย V2** และเพิ่มการสอบถามตัวกรอง ในกรณีนี้ ให้ใช้ `INTERCOMPANYINVENTTRANSID == ""` เป็นสตริงการสอบถามของตัวกรอง

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="แก้ไขกล่องโต้ตอบการสอบถามเกี่ยวกับรายการของใบแจ้งหนี้การขาย V2":::

7. ตาราง **ใบเสนอราคา** ไม่มีความสัมพันธ์ระหว่างบริษัท ถ้ามีบุคคลสร้างใบเสนอราคาสำหรับลูกค้าระหว่างบริษัทอย่างใดอย่างหนึ่ง คุณสามารถใช้คอลัมน์ **CustGroup** เพื่อวางลูกค้าทั้งหมดเหล่านั้นลงในกลุ่มลูกค้าหนึ่งกลุ่ม คุณสามารถขยายส่วนหัวและรายการโดยเพิ่มคอลัมน์ **CustGroup** แล้วกรองข้อมูล เพื่อให้กลุ่มนั้นไม่รวมอยู่ในกลุ่ม

    :::image type="content" source="media/filter-cust-group.png" alt-text="แม็ปการจัดเตรียมไปยังหน้าเป้าหมายให้กับส่วนหัวของใบเสนอราคาการขาย CDS":::

8. หลังจากที่ขยาย **ใบเสนอราคา** แล้ว ให้ใช้ตัวกรองที่มี `CUSTGROUP != "<company>"` เป็นสตริงการสอบถาม

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="แก้ไขกล่องโต้ตอบการสอบถามเกี่ยวกับส่วนหัวของใบเสนอราคาการขาย CDS":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]