---
title: สร้างงานการเบิกสินค้าทันทีเมื่อมีการนำโหลดออกใช้
description: ถ้าต้องสร้างงานทันทีเมื่อมีการนำโหลดออกใช้ คุณต้องตั้งค่าคอนฟิกแม่แบบเวฟตามต้องการ หน้านี้จะนำคุณไปสู่ขั้นตอนต่างๆ
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477758"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>งานการเบิกสินค้าไม่ถูกสร้างทันทีเมื่อมีการนำโหลดขาออกออกใช้

## <a name="symptoms"></a>อาการ

คุณสร้างสินค้าขาออกโดยใช้ใบสั่งขายหรือใบสั่งโอนย้าย และนำโหลดออกใช้ไปยังคลังสินค้า อย่างไรก็ตาม คุณสังเกตเห็นว่ายังไม่มีการสร้างงานการเบิกสินค้า

## <a name="resolution"></a>การแก้ปัญหา

ถ้าต้องสร้างงานทันทีเมื่อมีการนำโหลดออกใช้ คุณต้องตั้งค่าคอนฟิกแม่แบบเวฟตามต้องการ บนแม่แบบเวฟ ให้ตั้งค่าตัวเลือกต่อไปนี้เป็น *ใช่*:

- การสร้างเวฟอัตโนมัติ
- ประมวลผลเวฟเมื่อนำออกใช้ไปยังคลังสินค้า
- นำเวฟออกใช้อัตโนมัติ
