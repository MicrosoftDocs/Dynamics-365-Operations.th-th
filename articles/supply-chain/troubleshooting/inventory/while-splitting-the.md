---
title: เมื่อปริมาณตามน้ําหนักจริงถูกแบ่ง ระบบจะใช้ปริมาณต่ำสุดแทนปริมาณที่ระบุ
description: เมื่อปริมาณตามน้ําหนักจริงถูกแบ่งออกเป็นชุด ฟิลด์ปริมาณการเบิกสินค้าจะใช้ปริมาณต่ำสุดที่ตั้งค่าไว้ของสินค้า ไม่ใช่ปริมาณที่ระบุ
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026958"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>เมื่อปริมาณตามน้ําหนักจริงถูกแบ่ง ระบบจะใช้ปริมาณต่ำสุดแทนปริมาณที่ระบุ

หมายเลข KB: 4612073

## <a name="symptoms"></a>อาการ

เมื่อปริมาณตามน้ําหนักจริงถูกแบ่งออกเป็นชุด ฟิลด์ **ปริมาณการเบิกสินค้า** จะใช้ปริมาณต่ำสุดที่ตั้งค่าไว้ของสินค้า ไม่ใช่ปริมาณที่ระบุ

## <a name="resolution"></a>ความละเอียด

ระบบมีการทำงานตามที่ออกแบบ ระบบใช้การตั้งค่าปริมาณต่ำสุดของสินค้าแต่ละรายการในการเบิกสินค้า
