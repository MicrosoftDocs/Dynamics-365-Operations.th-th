---
title: ต้องระบุป้ายทะเบียนสำหรับสถานที่นี้
description: ถ้าคุณได้รับข้อผิดพลาดนี้หลังจากสร้างใบสั่งโอนย้ายให้กับคลังสินค้าที่เปิดใช้งาน WMS สถานที่รับสินค้าเริ่มต้นจะว่างเปล่าสำหรับคลังสินค้าส่งต่อ
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477707"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>ข้อผิดพลาดเกี่ยวกับข้อมูลจำเพาะป้ายทะเบียนเมื่อยืนยันการจัดส่งของใบสั่งโอนย้าย

## <a name="symptoms"></a>อาการ

หากคุณสร้างใบสั่งโอนย้ายโดยใช้คลังสินค้าที่เปิดใช้งานสำหรับการจัดการคลังสินค้าขั้นสูง (WMS) แล้ว จากนั้นพยายามยืนยันการจัดส่งหลังจากงานเสร็จสมบูรณ์แล้ว คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:

> ต้องระบุป้ายทะเบียนสำหรับสถานที่นี้

## <a name="cause"></a>สาเหตุ

ทั้งนี้เนื่องจากฟิลด์ **สถานที่รับสินค้าเริ่มต้น** จะว่างเปล่าสำหรับคลังสินค้าส่งต่อของคลังสินค้า "เริ่มต้น"

## <a name="resolution"></a>การแก้ปัญหา

เมื่อต้องการแก้ไขปัญหานี้ ให้ระบุสถานที่รับสินค้าเริ่มต้นในคลังสินค้าส่งต่อ ตรวจสอบให้แน่ใจว่าที่ตั้งนี้เป็นป้ายทะเบียนที่ควบคุม
