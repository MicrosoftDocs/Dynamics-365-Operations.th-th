---
title: ยืนยันการจัดส่งขาออกจากชุดงาน
description: บทความนี้จะอธิบายวิธีการตั้งค่าชุดงานที่ยืนยันการจัดส่งสินค้าตามใบสั่งโอนย้ายขาออกโดยอัตโนมัติสำหรับโหลดงานที่พร้อมในการจัดส่ง
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 00749a69b17b0064290d7b41ccb2171386716302
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875114"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>ยืนยันการจัดส่งขาออกจากชุดงาน

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการตั้งค่าชุดงานที่ยืนยันการจัดส่งสินค้าตามใบสั่งโอนย้ายขาออกโดยอัตโนมัติสำหรับโหลดงานที่พร้อมในการจัดส่ง ชุดงานที่อธิบายไว้ที่นี่ใช้กับการจัดส่งตามใบสั่งโอนย้ายเท่านั้น ไม่ใช่สำหรับใบสั่งขาย

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>เปิดหรือปิดคุณลักษณะยืนยันการจัดส่งขาออกจากชุดงาน

หากต้องการใช้ฟังก์ชันที่อธิบายไว้ในบทความนี้ คุณต้องเปิดคุณลักษณะ *ยืนยันการจัดส่งขาออกจากชุดงาน* ให้กับระบบของคุณ (เริ่มจาก Supply Chain Management เวอร์ชัน 10.0.21 คุณลักษณะนี้จะเปิดตามค่าเริ่มต้น) เริ่มจาก Supply Chain Management รุ่น 10.0.25 คุณลักษณะนี้เป็นแบบบังคับและไม่สามารถปิดได้ ถ้าคุณเรียกใช้รุ่นที่เก่ากว่า 10.0.25 ผู้ดูแลระบบสามารถเปิดหรือปิดฟังก์ชันนี้ได้โดยค้นหาคุณลักษณะ *ยืนยันการจัดส่งขาออกจากชุดงาน* ในพื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

## <a name="process-outbound-shipments"></a>ประมวลผลการจัดส่งขาออก

เมื่อต้องการตั้งค่าชุดงานที่จัดกำหนดการไว้เพื่อรันการยืนยันการจัดส่งขาออกสำหรับการโหลดงานที่พร้อมในการจัดส่ง:

1. ไปที่งานประจำงวด **การจัดการคลังสินค้า \> \>ประมวลผลการจัดส่งขาออก**
1. กล่องโต้ตอบ **ยืนยันการจัดส่ง** จะเปิดขึ้น บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรองข้อมูล**
1. กล่องโต้ตอบตัวแก้ไขการสอบถามจะเปิดขึ้น บนแท็บ **ช่วง** เพิ่มแถวที่มีค่าต่อไปนี้:
    - **ตาราง** - *โหลด*
    - **ตารางสืบทอด** - *โหลด*
    - **ฟิลด์** - *สถานะการโหลด*
    - **เงื่อนไข** - *โหลด*
1. เลือก **ตกลง** เพื่อกลับไปที่กล่องโต้ตอบ **การยืนยันการจัดส่ง**
1. บนแท็บด่วน **การรันในส่วนเบื้องหลัง** ให้ตั้งค่า **การประมวลผลชุดงาน** เป็น **ใช่**
1. บนแท็บด่วน **การรันในส่วนเบื้องหลัง** เลือก **การเกิดซ้ำ**
1. กล่องโต้ตอบ **กำหนดการเกิดซ้ำ** จะเปิดขึ้น ตั้งค่ากำหนดการรันตามที่จำเป็นสำหรับธุรกิจของคุณ
1. เลือก **ตกลง** เพื่อกลับไปที่กล่องโต้ตอบ **การยืนยันการจัดส่ง**
1. เลือก **ตกลง** บนกล่องโต้ตอบ **ยืนยันการจัดส่ง** เพื่อเพิ่มชุดงานเข้าในคิวชุดงาน

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของการประมวลผลชุดงาน](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]