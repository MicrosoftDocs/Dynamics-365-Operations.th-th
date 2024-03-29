---
title: ตรวจสอบความขัดแย้งของราคาในใบสั่งระหว่างบริษัท
description: บทความนี้จะอธิบายถึงวิธีการตรวจสอบความขัดแย้งของราคาในใบสั่งระหว่างบริษัท
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ca27e86545ba8179c595e55487dbbf49cd9ec528
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890696"
---
# <a name="check-intercompany-order-price-discrepancies"></a>ตรวจสอบความขัดแย้งของราคาในใบสั่งระหว่างบริษัท

[!include [banner](../../includes/banner.md)]

คุณสามารถใช้กระบวนงานนี้เพื่อตรวจสอบความขัดแย้งของราคาในใบสั่งระหว่างบริษัท

1. ไปที่ **การจัดซื้อและการจัดหา \> ประจำงวด \> การล้าง \> การตรวจสอบความขัดแย้งของราคาในใบสั่งระหว่างบริษัท**
1. ตั้งค่าชุดงาน หากจำเป็น แล้วเลือก **ตกลง** เพื่อตรวจสอบราคาและส่วนลดสำหรับใบสั่งขายและใบสั่งซื้อระหว่างบริษัท หรือ เลือก **ยกเลิก** เพื่อปิดหน้าโดยไม่ดำเนินการตรวจสอบ

    > [!TIP]
    > ถ้ามีปัญหาใดๆ เกี่ยวกับการซิงโครไนส์หรือราคา ซึ่งมีอยู่ในข้อความแสดงข้อมูลที่จะแสดง คุณสามารถพิมพ์ข้อความแสดงข้อมูลเพื่อการอ้างอิงได้

1. ในข้อความแสดงข้อมูล ให้เลือกที่รายการที่เกี่ยวข้องเพื่อเปิดใบสั่งในนิติบุคคลปัจจุบัน เปิดใบสั่งในนิติบุคคลที่เกี่ยวข้องโดยเลือก **ระหว่างบริษัท** แล้วตามด้วย **ใบสั่งซื้อระหว่างบริษัท** หรือ **ใบสั่งขายระหว่างบริษัท**

    > [!NOTE]
    > ถ้าต้องการอนุญาตให้มีการอัพเดตใบสั่งระหว่างบริษัท:
    >
    > 1. ไปที่ **บัญชีลูกหนี้ \> ลูกค้า \> ลูกค้าทั้งหมด**
    > 1. บนบานหน้าต่างการดำเนินการ เลือกแท็บ **ทั่วไป** และจากนั้น เลือก **ระหว่างบริษัท**
    > 1. บนหน้า **ระหว่างบริษัท** ให้เลือก **นโยบายใบสั่งซื้อ** หรือ **นโยบายใบสั่งขาย**
    > 1. เลือก **อนุญาตให้แก้ไขราคา** และ **อนุญาตให้แก้ไขส่วนลด** ในทั้งสองพื้นที่ได้

1. เปิดใบสั่งระหว่างบริษัทที่เกี่ยวข้องที่คุณต้องการคงราคาไว้ 
1. สำหรับแต่ละบรรทัดใบสั่ง ให้เปลี่ยนฟิลด์ **ราคาต่อหน่วย** สำหรับรายการ แล้วเปลี่ยนกลับไปเป็นมูลค่าเดิม เปลี่ยนฟิลด์ **ส่วนลด** ต่อรายการสินค้ากลับไปกลับมา และเปลี่ยนฟิลด์ **ค่าธรรมเนียมของการซื้อ** หรือ **การซื้อหรือค่าธรรมเนียม** ที่เกี่ยวข้องการขายกลับไปกลับมา การเปลี่ยนมูลค่านี้กลับไปกลับมาจะทริกเกอร์การซิงโครไนส์ราคา ส่วนลด และค่าธรรมเนียมเบ็ดเตล็ด จากบรรทัดใบสั่งระหว่างบริษัทนี้ไปยังบรรทัดใบสั่งระหว่างบริษัทที่อ้างอิงถึง เพื่อให้สอดคล้องกันโดยอัตโนมัติ

    > [!NOTE]
    > การซิงโครไนส์นี้จะใช้ได้เฉพาะเมื่อ ใบสั่งขายระหว่างบริษัทยังไม่ได้ออกใบแจ้งหนี้เท่านั้น ถ้าใบสั่งขายระหว่างบริษัทมีการลงรายการบัญชีใบแจ้งหนี้แล้ว และสมุดรายวันใบแจ้งหนี้ลูกค้าถูกสร้างขึ้นแล้ว จะต้องทำการเปลี่ยนแปลงโดยตรงบนบรรทัดใบสั่งซื้อระหว่างบริษัท ด้วยการกำหนดราคา ส่วนลด และค่าธรรมเนียมให้เท่ากับราคา ส่วนลด และค่าธรรมเนียมเบ็ดเตล็ดในสมุดรายวันใบแจ้งหนี้ลูกค้าระหว่างบริษัท มิฉะนั้น ใบสั่งซื้อระหว่างบริษัทจะไม่สามาถลงรายการบัญชีใบแจ้งหนี้ได้ เนื่องจากมีความไม่สอดคล้องในยอดรวมของใบสั่ง

1. ทำซ้ำกระบวนงาน จนกว่าจะซิงโครไนส์ใบสั่งซื้อและใบสั่งขายระหว่างบริษัททั้งหมดแล้ว

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
