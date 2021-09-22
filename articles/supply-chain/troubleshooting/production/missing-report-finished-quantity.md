---
title: การอัปเดตการรายงานเมื่อเสร็จสมบูรณ์จะล้มเหลวโดยมีข้อผิดพลาดเกี่ยวกับปริมาณที่ขาดหายไป
description: หากคุณพยายามจบใบสั่งผลิตในขณะที่รายงานปริมาณข้อผิดพลาด แต่ไม่ใช่ในขณะที่ฉันรายงานปริมาณเวลาหรือวัสดุ การอัปเดตการรายงานเมื่อเสร็จสมบูรณ์จะล้มเหลว
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7785549c47063727f2749749940c1a96a351e70f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477711"
---
# <a name="report-as-finished-update-fails-with-a-missing-quantity-error"></a>การอัปเดตการรายงานเมื่อเสร็จสมบูรณ์จะล้มเหลวโดยมีข้อผิดพลาดเกี่ยวกับปริมาณที่ขาดหายไป

## <a name="symptoms"></a>อาการ

คุณพยายามรายงานใบสั่งผลิตเมื่อเสร็จสมบูรณ์ในขณะที่รายงานปริมาณข้อผิดพลาด แต่ไม่ใช่ในขณะที่รายงานปริมาณเวลาหรือวัสดุ การอัปเดตการรายงานเมื่อเสร็จสมบูรณ์จะล้มเหลวเมื่อคุณพยายามจบใบสั่งผลิต และคุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:

> ปริมาณที่รายงานการเสร็จงานขาดหายไป

## <a name="resolution"></a>การแก้ปัญหา

หากคุณรายงานปริมาณของข้อผิดพลาดในใบสั่งผลิต คุณต้องรายงานปริมาณสินค้าที่ดี
