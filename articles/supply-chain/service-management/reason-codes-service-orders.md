---
title: รหัสเหตุผลสำหรับใบสั่งบริการ
description: ใช้รหัสเหตุผลเพื่อช่วยอธิบายสถานะของใบสั่งบริการ เมื่อมีการอัพเดตขั้นตอนของใบสั่งบริการ
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAStageTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdade89d07fec6a01926015a8c73bacce015fd7a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563844"
---
# <a name="reason-codes-for-service-orders"></a>รหัสเหตุผลสำหรับใบสั่งบริการ   

[!include [banner](../includes/banner.md)]


คุณสามารถใช้รหัสเหตุผลเพื่อช่วยอธิบายสถานะของใบสั่งบริการได้ เมื่อมีการอัพเดตขั้นตอนของใบสั่งบริการ ตัวอย่างเช่น ถ้าคุณยกเลิกใบสั่งบริการ คุณสามารถเลือกรหัสเหตุผลสำหรับการยกเลิก

หากต้องการดูข้อมูลเกี่ยวกับรหัสเหตุผลที่ใช้โดยติดตามความคืบหน้าของใบสั่งบริการ ให้รันรายงานความคืบหน้าของใบสั่งบริการ  รายงานนี้จะแสดงรายการใบสั่งบริการทั้งหมด และรหัสเหตุผลใดที่ระบุเมื่อมีการอัพเดตขั้นใบสั่งบริการ ไม่ว่าจะเป็นขั้นใดก็ตาม

## <a name="turn-reason-codes-on-or-off"></a>เปิดหรือปิดรหัสเหตุผล

ไม่จำเป็นต้องระบุรหัสเหตุผล  คุณสามารถตัดสินใจว่าต้องมีรหัสเหตุผล เมื่อคุณอัพเดตใบสั่งบริการไปยังขั้นบริการเฉพาะหรือไม่

1.  คลิก **การจัดการงานบริการ** \> **ตั้งค่า** \> **ใบสั่งบริการ** \> **ขั้นตอนการบริการ**

2.  ในแบบฟอร์ม **ขั้นตอนการบริการ** เลือกขั้นตอนการบริการ และจากนั้น เลือกกล่องกาเครื่องหมาย **เหตุผล** สำหรับขั้นตอนการบริการ

3.  ปิดแบบฟอร์มเพื่อบันทึกการเปลี่ยนแปลงของคุณ

## <a name="see-also"></a>ดูเพิ่มเติมที่

[ตั้งค่าระยะใบสั่งบริการ](set-up-service-order-stages.md)



