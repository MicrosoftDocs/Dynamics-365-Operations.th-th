---
title: แผนการใบสั่งผลิตต้องจัดตารางการผลิตก่อนที่จะสามารถยืนยันได้
description: เมื่อคุณพยายามยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่าต้องจัดตารางการผลิตใบสั่งก่อนที่จะสามารถยืนยันได้
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294195"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>แผนการใบสั่งผลิตต้องจัดตารางการผลิตก่อนที่จะสามารถยืนยันได้

รหัสข้อผิดพลาด: SYS309802

## <a name="symptoms"></a>อาการ

เมื่อคุณพยายามยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:

> ต้องจัดกำหนดการแผนการใบสั่งผลิตก่อนที่จะสามารถยืนยันได้

## <a name="cause"></a>สาเหตุ

วันที่เริ่มต้นและวันที่สิ้นสุดตามการจัดตารางการผลิตต้องไม่ว่างเปล่า

## <a name="resolution"></a>การแก้ปัญหา

หากต้องการระบุวันที่เริ่มต้นและวันที่สิ้นสุดของแผนการใบสั่ง ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **การวางแผนหลัก \> การวางแผนหลัก \> แผนการใบสั่ง**
1. เปิดแผนการใบสั่งที่เกี่ยวข้อง
1. บนแท็บด่วน **ทั่วไป** ในส่วน **ที่จัดตารางการผลิต** ให้ระบุวันที่ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด**
