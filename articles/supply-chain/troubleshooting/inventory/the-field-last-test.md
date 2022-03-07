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
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026960"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>ฟิลด์วันที่ทดสอบล่าสุดไม่มีการอัเดตเมื่อสร้างใบสั่งตรวจสอบคุณภาพหลายใบ

หมายเลข KB: 4612803

## <a name="symptoms"></a>อาการ

ฟิลด์ **วันที่ทดสอบล่าสุด** ไม่มีการอัเดตเมื่อสร้างใบสั่งตรวจสอบคุณภาพหลายใบ

## <a name="resolution"></a>ความละเอียด

ระบบมีการทำงานตามที่ออกแบบ วันที่ทดสอบล่าสุดไม่เกี่ยวข้องกับใบสั่งตรวจสอบคุณภาพ โดยจะจัดเก็บวันที่ที่สินค้าเสร็จสมบูรณ์ที่ซื้อหรือผลิตครั้งแรก วันที่นี้จะใช้ในการคํานวณวันที่แนะนําอายุการเก็บสินค้า
