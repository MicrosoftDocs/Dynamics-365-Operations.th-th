---
title: น้ำหนักโหลดสามารถมีตัวเลขค่าบวกเท่านั้น
description: เมื่อประมวลผลงานระหว่างสถานที่ คุณอาจได้รับข้อผิดพลาดเกี่ยวกับน้ำหนักโหลดและการอัปเดตของคุณที่ถูกยกเลิก ให้ทำตามขั้นตอนต่อไปนี้เพื่อแก้ไขปัญหานี้
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477728"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>ข้อผิดพลาดน้ำหนักโหลดและการอัปเดตที่ถูกยกเลิกเมื่อประมวลผลงานระหว่างสถานที่

## <a name="symptoms"></a>อาการ

ถ้ามีการเปิดงานเมื่อคุณดำเนินงานจากสถานที่จัดส่งไปยังสถานที่การแบ่งระยะ หรือจากสถานที่การแบ่งระยะไปยังสถานที่เก็บสินค้า คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:

> ฟิลด์ 'น้ำหนักโหลด'(=-%1) สามารถมีตัวเลขค่าบวกเท่านั้น การอัพเดตถูกยกเลิก

## <a name="resolution"></a>การแก้ปัญหา

เมื่อต้องการแก้ไขปัญหานี้ ให้ไปที่ **การจัดการระบบ \> งานประจำงวด \> ฐานข้อมูล \> การตรวจสอบความสอดคล้องกันของข้อมูล** และรันกระบวนการสำหรับ **การตรวจสอบความสอดคล้องของน้ำหนักบรรทุกของคลังสินค้า**
