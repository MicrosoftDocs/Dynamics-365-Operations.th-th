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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924412"
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
