---
title: การรวมเงินคืนของลูกค้าล้มเหลว เมื่อมีการใช้กลุ่มเงินคืนของสินค้า
description: เมื่อคุณใช้ข้อตกลงเงินคืนของลูกค้าโดยรวมกับกลุ่มเงินคืนของสินค้า เงินคืนจะถูกคํานวณ แต่การรวบรวมจะล้มเหลว
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026939"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>การรวมเงินคืนของลูกค้าล้มเหลว เมื่อมีการใช้กลุ่มเงินคืนของสินค้า

หมายเลข KB: 4611372

## <a name="symptoms"></a>อาการ

เมื่อคุณใช้ข้อตกลงเงินคืนของลูกค้า (ของชนิด *จำนวน*) โดยรวมกับกลุ่มเงินคืนของสินค้า เงินคืนจะถูกคํานวณ แต่การรวบรวมจะล้มเหลว

## <a name="resolution"></a>ความละเอียด

ระบบมีการทำงานตามที่ออกแบบ กลุ่มสินค้าจะจัดกลุ่มเฉพาะสินค้าที่มีเงื่อนไขขีดจำกัดเดียวกันเท่านั้น เงื่อนไขเงินคืน (ขีดจำกัด) ถูกตั้งค่าโดยเทียบกับยอดเงินสำหรับสินค้าแต่ละรายการ ไม่ใช่เทียบกับยอดเงินสะสมสำหรับสินค้าใดๆ ในกลุ่มสินค้า
