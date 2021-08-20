---
title: คุณไม่สามารถยกเลิกงานที่อยู่บนผู้ใช้ได้
description: คุณไม่สามารถยกเลิกงานที่อยู่บนผู้ใช้ได้
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
ms.openlocfilehash: 1d7b0140d0c2724234a549ca4dfb23109012654abe0e60fcea1f98e8f17c153a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748702"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>คุณไม่สามารถยกเลิกงานที่อยู่บนผู้ใช้ได้

รหัสข้อผิดพลาด: WAX708

## <a name="symptoms"></a>อาการ

ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:

> คุณไม่สามารถยกเลิกงานที่อยู่กับผู้ใช้ได้

## <a name="cause"></a>สาเหตุ

งานถูกล็อคโดยผู้ใช้ไม่สามารถยกเลิกได้ เมื่อต้องการยืนยันสิ่งนี้ ให้เปิดรหัสงานแล้วเปิดแท็บ **ทั่วไป** ถ้างานถูกล็อคไว้ ฟิลด์ **สถานะของงาน** จะถูกตั้งค่าเป็น *อยู่ระหว่างการดำเนินการ* และฟิลด์ **ล็อคโดย** จะตั้งค่าเป็นรหัสผู้ใช้

## <a name="resolution"></a>ความละเอียด

หากต้องการยกเลิกงาน ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> การล้าง \> ยกเลิกงาน**
1. ในฟิลด์ **รหัสงาน** ให้ระบุรหัสงานที่คุณต้องการยกเลิก
1. เลือก **ตกลง**
1. เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยกเลิกงาน

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยกเลิกงานของคลังสินค้าสำหรับการจัดการข้อยกเว้น](../../warehousing/cancel-warehouse-work.md)
