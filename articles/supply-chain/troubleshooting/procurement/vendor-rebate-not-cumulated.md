---
title: เงินคืนของผู้จัดจำหน่ายไม่ได้รับการสะสมตามใบแจ้งหนี้
description: เงินคืนของผู้จัดจำหน่ายไม่ได้รับการสะสมตามใบแจ้งหนี้
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9d4596a7351969bf181982a24ea1dcc6f5732831
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477783"
---
# <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>เงินคืนของผู้จัดจำหน่ายไม่ได้รับการสะสมตามใบแจ้งหนี้

## <a name="symptoms"></a>อาการ

ถ้าใบแจ้งหนี้ที่ลงรายการบัญชีมีวันที่ครบกำหนดแตกต่างกัน ใบแจ้งหนี้เหล่านั้นจะไม่มีผลในเงินคืนของผู้จัดจำหน่ายที่สร้างขึ้นจากใบแจ้งหนี้ดังกล่าว

## <a name="resolution"></a>การแก้ปัญหา

ไม่มีการคำนึงถึงวันที่ครบกำหนด เมื่อมีการคำนวณเงินคืนของผู้จัดจำหน่าย ให้พิจารณาการเลือกกำหนดระบบด้วยตนเองเพื่อให้วันที่ครบกำหนดและความสัมพันธ์กับใบแจ้งหนี้มีความเกี่ยวข้องกับเงินคืนของผู้จัดจำหน่ายจริงมากขึ้น
