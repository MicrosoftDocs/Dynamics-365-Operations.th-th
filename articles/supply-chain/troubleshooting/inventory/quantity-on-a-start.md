---
title: ปริมาณในใบสั่งตรวจสอบสินค้าที่เริ่มต้นไม่มีการอัปเดตเมื่อแบ่งใบสั่ง
description: เมื่อคุณสร้างใบสั่งตรวจสอบสินค้าและพยายามแบ่ง ใบสั่งไม่มีการอัปเดตเป็นปริมาณคงเหลือที่แบ่ง
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026962"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>ปริมาณในใบสั่งตรวจสอบสินค้าที่เริ่มต้นไม่มีการอัปเดตเมื่อแบ่งใบสั่ง

หมายเลข KB: 4613113

## <a name="symptoms"></a>อาการ

เมื่อคุณสร้างใบสั่งตรวจสอบสินค้าและพยายามแบ่ง ใบสั่งไม่มีการอัปเดตเป็นปริมาณคงเหลือหลังการแบ่ง

## <a name="resolution"></a>ความละเอียด

ระบบจะไม่เปลี่ยนปริมาณเดิมจากใบสั่งตรวจสอบสินค้า เพื่อให้แน่ใจว่าคุณสามารถติดตามปริมาณเดิมที่สร้างไว้ให้กับใบสั่งตรวจสอบสินค้านั้น อย่างไรก็ตาม ระบบจะติดตามปริมาณที่แบ่งจากใบสั่งตรวจสอบสินค้า เมื่อต้องการติดตามนี้ จะใช้ฟิลด์ฐานข้อมูลที่ชื่อ `QuantityThatHasSplitIntoOtherQuarantineOrders` อย่างไรก็ตาม ฟิลด์นี้ไม่ปรากฏในอินเทอร์เฟสผู้ใช้ (UI)
