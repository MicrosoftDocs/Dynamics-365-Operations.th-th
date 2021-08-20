---
title: ใบสั่งที่ยืนยันที่ได้รับมาโดยตรงจะถูกประมวลผลโดยลำดับงานในระหว่างการตรวจทาน
description: ใบสั่งที่ยืนยันที่ได้รับมาโดยตรงจะถูกประมวลผลโดยลำดับงานที่มีสถานะระหว่างการตรวจทาน
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d20f1c1d6e8fc83dd996b04bf0321a41f7b39290f306d1ac9f4fcd17514832e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721186"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>ใบสั่งที่ยืนยันที่ได้รับมาโดยตรงจะถูกประมวลผลโดยลำดับงานในระหว่างการตรวจทาน

หมายเลข KB: 4612450

## <a name="symptoms"></a>อาการ

ใบสั่งที่ยืนยันที่ได้รับมาโดยตรงจะถูกประมวลผลโดยลำดับงานที่มีสถานะ *ระหว่างการตรวจทาน*

## <a name="resolution"></a>ความละเอียด

เมื่อการติดตามการเปลี่ยนแปลงกรณีเปิดใช้งาน สถานะ *ระหว่างการตรวจทาน* จะกำหนดให้ใบสั่งที่ได้รับมาซึ่งยืนยันแล้ว (ใบสั่งซื้อของผู้รับเหมารายย่อย) ดังนั้นถ้าใบสั่งซื้อได้รับมา (ใบสั่งซื้อของผู้รับเหมารายย่อย) ใบสั่งซื้อนั้นจะถูกส่งไปยังลำดับงานเท่านั้น ถ้าใบสั่งซื้อเป็นแผนการใบสั่งซื้อที่ยืนยันแล้ว ใบสั่งซื้อจะได้รับการอนุมัติโดยอัตโนมัติเพื่อให้แน่ใจว่ากลไกจัดการวางแผนจะไม่สร้างแผนการใบสั่งใหม่ในขณะที่ใบสั่งซื้อยังคงอยู่ในสถานะ *ร่าง*
