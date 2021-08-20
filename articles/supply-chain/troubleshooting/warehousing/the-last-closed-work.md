---
title: รายการงานที่ปิดครั้งสุดท้ายต้องเป็นส่งสินค้า
description: รายการงานที่ปิดครั้งสุดท้ายต้องเป็นส่งสินค้า
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bbc5797df2b7465b36ec5ea546a67441626daeb1c72f82dfca4eb7db3503b713
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760285"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>รายการงานที่ปิดครั้งสุดท้ายต้องเป็นส่งสินค้า

รหัสข้อผิดพลาด: WAX1285

## <a name="symptoms"></a>อาการ

ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:

> รายการงานที่ปิดครั้งสุดท้ายต้องเป็นส่งสินค้า

## <a name="cause"></a>สาเหตุ

ไม่สามารถยกเลิกงานในสถานะปัจจุบันได้

บนรายการงานล่าสุด ฟิลด์ **สถานะของงาน** ได้รับการตั้งค่าเป็น *ปิด* แต่ไม่ได้ตั้งค่าฟิลด์ **ชนิดงาน** เป็น *ส่ง*

## <a name="resolution"></a>ความละเอียด

หากต้องการยกเลิกงาน ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> การล้าง \> ยกเลิกงาน**
1. ในฟิลด์ **รหัสงาน** ให้ระบุรหัสงานที่คุณต้องการยกเลิก
1. เลือก **ตกลง**
1. เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยกเลิกงาน

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยกเลิกงานของคลังสินค้าสำหรับการจัดการข้อยกเว้น](../../warehousing/cancel-warehouse-work.md)
