---
title: ปัญหาเกี่ยวกับการแปลงสกุลเงินข้อตกลงทางการค้า
description: จะไม่มีการคำนวณราคาข้อตกลงทางการค้าใหม่อีกครั้งตามสกุลเงิน เมื่อสกุลเงินแตกต่างกันในใบสั่งซื้อ
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
ms.openlocfilehash: 1b6dc36c5f5ee6b611eebd81f378399ce1748c63
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477704"
---
# <a name="trade-agreement-currency-conversion-issues"></a>ปัญหาเกี่ยวกับการแปลงสกุลเงินข้อตกลงทางการค้า

## <a name="symptoms"></a>อาการ

ราคาข้อตกลงทางการค้าจะไม่มีการคำนวณใหม่อีกครั้งตามสกุลเงิน เมื่อสกุลเงินแตกต่างกันในใบสั่งซื้อ

## <a name="resolution"></a>การแก้ปัญหา

ลักษณะการทำงานของ *สกุลเงินทั่วไป* ช่วยให้คุณสามารถกำหนดราคาและส่วนลดในสกุลเงินเดียวเท่านั้น คุณสามารถแปลงเป็นสกุลเงินอื่นได้ตามที่ต้องการ นอกจากนี้คุณยังสามารถใช้คุณลักษณะการปัดเศษแบบชาญฉลาดได้โดยอัตโนมัติเมื่อมีการแปลงเสร็จเรียบร้อยแล้ว
