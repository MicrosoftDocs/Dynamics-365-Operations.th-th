---
title: ปริมาณไม่ถูกต้องในหน่วย %1 เมื่อปฏิบัติงานแบ่งการเบิกสินค้า
description: เมื่อแบ่งการเบิกสินค้าระหว่างชุดงานหลายชุด คุณอาจได้รับข้อผิดพลาดว่าปริมาณไม่ถูกต้องในหน่วย %1 หน้านี้ช่วยแก้ปัญหา
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4627db7400d6ccd81f25f100de4696058ce35c42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477697"
---
# <a name="quantity-is-not-valid-when-performing-a-split-pick-across-multiple-batches"></a>ปริมาณไม่ถูกต้องเมื่อปฏิบัติการแบ่งการเบิกสินค้าระหว่างชุดงานหลายชุด

## <a name="symptoms"></a>อาการ

เมื่อคุณพยายามดำเนินการ *แบ่งการเบิกสินค้า* ในหลายชุดงาน คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้:

> ปริมาณไม่ถูกต้องสำหรับหน่วย %1

## <a name="resolution"></a>การแก้ปัญหา

ผู้ปฏิบัติงานคลังสินค้าต้องใช้กระบวนการ *เบิกสินค้าแบบสั้น* ในแอป Warehouse Management บนมือถือ ถ้าคุณกำลังพยายามเลือกหลายชุดจากสถานที่เดียวกัน คุณยังสามารถใช้ตัวเลือก **แบบเต็ม** ในแอปได้ด้วย
