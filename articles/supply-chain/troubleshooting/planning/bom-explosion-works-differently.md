---
title: การกระจาย BOM แตกต่างจากการกระจายของใบสั่งผลิตที่ยืนยันและประเมินไว้
description: การกระจายสูตรการผลิตจะทำงานแตกต่างกันสำหรับใบสั่งผลิตที่ยืนยัน และสำหรับใบสั่งผลิตที่ประเมินไว้สำหรับงานที่สร้างขึ้นด้วยตนเอง
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477737"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>การกระจาย BOM แตกต่างจากการกระจายของใบสั่งผลิตที่ยืนยันและประเมินไว้

## <a name="symptoms"></a>อาการ

เมื่อยืนยันใบสั่งผลิตสินค้า จะไม่มีการกระจายเมื่อคุณกระจายสูตรการผลิต (BOM) อย่างไรก็ตาม เมื่อคุณสร้างใบสั่งงานด้วยตนเองแล้วประเมินใบสั่งผลิต จะมีการกระจายสินค้า

### <a name="resolution"></a>การแก้ปัญหา

การกระจายที่เกิดขึ้นเมื่อยืนยันใบสั่งผลิตจะชี้ไปยังแผนการใบสั่ง แต่ไม่ได้แสดงว่าแผนการใบสั่งจะถูกยืนยันในกรณีนี้ในขณะนี้ อย่างไรก็ตาม ถ้ามีการประเมินใบสั่งผลิตไว้ การกระจายจะถูกทริกเกอร์จากใบสั่งผลิตที่นำออกใช้ซึ่งไม่มีแผนการใบสั่งอยู่
