---
title: ราคาต่อหน่วยในใบสั่งซื้อไม่ได้คำนวณตามการแปลงหน่วย
description: ราคาต่อหน่วยในใบสั่งซื้อไม่ได้คำนวณตามการแปลงหน่วย
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477735"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>ราคาต่อหน่วยในใบสั่งซื้อไม่ได้คำนวณตามการแปลงหน่วย

## <a name="symptoms"></a>อาการ

เมื่อมีการเปลี่ยนหน่วยในใบสั่งซื้อ ราคาข้อตกลงทางการค้าจะไม่มีการคำนวณใหม่ตามข้อกำหนดของการแปลงหน่วย

## <a name="cause"></a>สาเหตุ

ราคาจะได้รับจากข้อตกลงทางการค้าเสมอ (หรือการตั้งค่าราคาอื่นๆ ในระบบ เช่น ข้อตกลงการขาย หรือราคาสินค้า) และตั้งค่าไว้สำหรับหนึ่งหน่วย

ถ้ามีการเปลี่ยนหน่วยในบรรทัดใบสั่ง ระบบจะค้นหาราคาสำหรับหน่วยใหม่และใช้ราคาดังกล่าว ถ้าไม่พบราคาสำหรับหน่วยนั้น ระบบจะไม่มีการใช้ราคา ไม่สามารถใช้การแปลงหน่วยเพื่อคำนวณราคาใหม่เป็นหน่วยอื่นได้ ในทางทฤษฎี ราคาสำหรับหนึ่งกล่องในสิบกล่องอาจไม่เท่ากับราคาสิบเท่าของกล่องเดียว

## <a name="workaround"></a>วิธีการแก้ไข

วิธีการหนึ่งในการหลีกเลี่ยงปัญหานี้คือตรวจสอบให้แน่ใจว่ามีข้อตกลงทางการค้าสำหรับหน่วยที่คุณคาดว่าจะใช้ในบรรทัดใบสั่งสำหรับสินค้า
