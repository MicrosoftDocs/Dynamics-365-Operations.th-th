---
title: ไม่สามารถยกเลิกงานได้เนื่องจากสถานะของงาน
description: ไม่สามารถยกเลิกงานได้เนื่องจากสถานะของงาน
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924266"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>ไม่สามารถยกเลิกงานได้เนื่องจากสถานะของงาน

รหัสข้อผิดพลาด: WAX2190

## <a name="symptoms"></a>อาการ

ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:

> คุณไม่สามารถยกเลิกงาน %1 เนื่องจากมีสถานะ %2

## <a name="cause"></a>สาเหตุ

ไม่สามารถยกเลิกงานในสถานะปัจจุบันได้

หัวข้องานหรือรายการงานไม่มีค่า **สถานะของงาน** ที่คาดไว้ ฟิลด์ **สถานะของงาน** ไม่ได้ตั้งค่าบนหัวข้องานเป็น *เปิด* หรือ *อยู่ระหว่างการดำเนินการ*

## <a name="resolution"></a>ความละเอียด

หากต้องการยกเลิกงาน ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> การล้าง \> ยกเลิกงาน**
1. ในฟิลด์ **รหัสงาน** ให้ระบุรหัสงานที่คุณต้องการยกเลิก
1. เลือก **ตกลง**
1. เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยกเลิกงาน

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยกเลิกงานของคลังสินค้าสำหรับการจัดการข้อยกเว้น](../../warehousing/cancel-warehouse-work.md)
