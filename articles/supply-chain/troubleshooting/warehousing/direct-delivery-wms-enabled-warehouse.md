---
title: การจัดส่งสินค้าโดยตรงไม่สามารถประมวลผลคลังสินค้าที่เปิดใช้งาน WMS ได้
description: ถ้าคลังสินค้ามีการเปิดใช้งาน WMS การจัดส่งสินค้าโดยตรงจะไม่ได้รับการสนับสนุน หากต้องการใช้การจัดส่งสินค้าโดยตรง คุณต้องเลือกสินค้าที่ไม่ใช่ WMS และคลังสินค้า
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477792"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>การจัดส่งสินค้าโดยตรงไม่สามารถประมวลผลคลังสินค้าที่เปิดใช้งาน WMS ได้

## <a name="symptoms"></a>อาการ

ถ้ามีการเพิ่มสินค้าในรายการขายเพื่อจัดส่งสินค้าโดยตรงจากคลังสินค้าที่เปิดใช้งาน Warehouse Management (WMS) คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้เมื่อรายการขายมีการอัปเดต:

> การจัดส่งสินค้าโดยตรงไม่สามารถดำเนินการสำหรับคลังสินค้า 1% เนื่องจากมีการเปิดใช้งานการจัดการคลังสินค้า โปรดระบุคลังสินค้าอื่นที่ไม่ได้เปิดใช้งานสำหรับการจัดการคลังสินค้า

## <a name="resolution"></a>การแก้ปัญหา

Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน ปัจจุบัน WMS ไม่สนับสนุนการจัดส่งสินค้าโดยตรง เมื่อต้องการใช้การจัดส่งสินค้าโดยตรง คุณต้องเลือกสินค้าที่ไม่ใช่ WMS และคลังสินค้า
