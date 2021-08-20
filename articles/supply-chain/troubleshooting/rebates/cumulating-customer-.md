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
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760381"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>การรวมเงินคืนของลูกค้าล้มเหลว เมื่อมีการใช้กลุ่มเงินคืนของสินค้า

หมายเลข KB: 4611372

## <a name="symptoms"></a>อาการ

เมื่อคุณใช้ข้อตกลงเงินคืนของลูกค้า (ของชนิด *จำนวน*) โดยรวมกับกลุ่มเงินคืนของสินค้า เงินคืนจะถูกคํานวณ แต่การรวบรวมจะล้มเหลว

## <a name="resolution"></a>ความละเอียด

ระบบมีการทำงานตามที่ออกแบบ กลุ่มสินค้าจะจัดกลุ่มเฉพาะสินค้าที่มีเงื่อนไขขีดจำกัดเดียวกันเท่านั้น เงื่อนไขเงินคืน (ขีดจำกัด) ถูกตั้งค่าโดยเทียบกับยอดเงินสำหรับสินค้าแต่ละรายการ ไม่ใช่เทียบกับยอดเงินสะสมสำหรับสินค้าใดๆ ในกลุ่มสินค้า
