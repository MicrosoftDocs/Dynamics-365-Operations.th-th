---
title: ใบสั่งซื้อที่ถูกยกเลิกจะปรากฏในรายการแบบร่างในพื้นที่ทำงาน
description: ใบสั่งซื้อที่ถูกยกเลิกจะปรากฏในรายการแบบร่างในพื้นที่ทำงานการจัดเตรียมใบสั่งซื้อ
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477762"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>ใบสั่งซื้อที่ถูกยกเลิกจะปรากฏในรายการแบบร่างในพื้นที่ทำงาน

## <a name="symptoms"></a>อาการ

หลังจากที่คุณยกเลิกใบสั่งซื้อที่อยู่ในสถานะ *ยืนยันแล้ว* ใบสั่งซื้อที่ถูกยกเลิกยังคงแสดงอยู่ในรายการของใบสั่งซื้อฉบับร่างในพื้นที่ทำงาน **การจัดเตรียมใบสั่งซื้อ**

## <a name="resolution"></a>การแก้ปัญหา

ปัญหานี้เกิดขึ้นเฉพาะสำหรับใบสั่งซื้อที่อาจมีการเปลี่ยนแปลงการจัดการเท่านั้น เกิดขึ้นเนื่องจากการยกเลิกจะถือว่ามีการเปลี่ยนแปลงที่ต้องได้รับการอนุมัติ โดยระบบจะดำเนินการอนุมัติโดยอัตโนมัติ ดังนั้นกระบวนการคือการส่งใบสั่งซื้อที่ถูกยกเลิกไปที่ลำดับงานการอนุมัติเพื่อให้สามารถเปลี่ยนเป็นสถานะ *ที่อนุมัติแล้ว* ในจุดนั้น ใบสั่งซื้อจะไม่ปรากฏในรายการใบสั่งซื้อฉบับร่างในพื้นที่ทำงาน **การจัดเตรียมใบสั่งซื้อ** อีกต่อไป
