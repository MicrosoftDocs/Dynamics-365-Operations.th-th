---
title: ฟิลด์วันที่ทดสอบล่าสุดไม่มีการอัเดตเมื่อสร้างใบสั่งตรวจสอบคุณภาพหลายใบ
description: ฟิลด์วันที่ทดสอบล่าสุดไม่มีการอัเดตเมื่อสร้างใบสั่งตรวจสอบคุณภาพหลายใบ
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742039"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>ฟิลด์วันที่ทดสอบล่าสุดไม่มีการอัเดตเมื่อสร้างใบสั่งตรวจสอบคุณภาพหลายใบ

หมายเลข KB: 4612803

## <a name="symptoms"></a>อาการ

ฟิลด์ **วันที่ทดสอบล่าสุด** ไม่มีการอัเดตเมื่อสร้างใบสั่งตรวจสอบคุณภาพหลายใบ

## <a name="resolution"></a>ความละเอียด

ระบบมีการทำงานตามที่ออกแบบ วันที่ทดสอบล่าสุดไม่เกี่ยวข้องกับใบสั่งตรวจสอบคุณภาพ โดยจะจัดเก็บวันที่ที่สินค้าเสร็จสมบูรณ์ที่ซื้อหรือผลิตครั้งแรก วันที่นี้จะใช้ในการคํานวณวันที่แนะนําอายุการเก็บสินค้า
