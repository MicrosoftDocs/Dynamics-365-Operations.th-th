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
ms.openlocfilehash: 4625570cb706199dca78f23b1864ca1d81cc66e896cf10d6d5f16cf1a9d1dc16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713505"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>ปริมาณในใบสั่งตรวจสอบสินค้าที่เริ่มต้นไม่มีการอัปเดตเมื่อแบ่งใบสั่ง

หมายเลข KB: 4613113

## <a name="symptoms"></a>อาการ

เมื่อคุณสร้างใบสั่งตรวจสอบสินค้าและพยายามแบ่ง ใบสั่งไม่มีการอัปเดตเป็นปริมาณคงเหลือหลังการแบ่ง

## <a name="resolution"></a>ความละเอียด

ระบบจะไม่เปลี่ยนปริมาณเดิมจากใบสั่งตรวจสอบสินค้า เพื่อให้แน่ใจว่าคุณสามารถติดตามปริมาณเดิมที่สร้างไว้ให้กับใบสั่งตรวจสอบสินค้านั้น อย่างไรก็ตาม ระบบจะติดตามปริมาณที่แบ่งจากใบสั่งตรวจสอบสินค้า เมื่อต้องการติดตามนี้ จะใช้ฟิลด์ฐานข้อมูลที่ชื่อ `QuantityThatHasSplitIntoOtherQuarantineOrders` อย่างไรก็ตาม ฟิลด์นี้ไม่ปรากฏในอินเทอร์เฟสผู้ใช้ (UI)
