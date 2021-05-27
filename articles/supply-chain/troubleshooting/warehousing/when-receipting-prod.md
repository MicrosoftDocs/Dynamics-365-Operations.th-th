---
title: มีการพิมพ์ป้ายชื่อเพียงป้ายชื่อเดียวหลายหัวข้อบนใบรับสินค้าเดียว
description: มีการพิมพ์ป้ายชื่อเพียงป้ายชื่อเดียวหลายหัวข้อบนใบรับสินค้าเดียว
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026948"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>มีการพิมพ์ป้ายชื่อเพียงป้ายชื่อเดียวหลายหัวข้อบนใบรับสินค้าเดียว

หมายเลข KB: 4614667

## <a name="symptoms"></a>อาการ

ส่วนหัวของงานหลายหัวข้อสร้างขึ้นเพื่อป้ายทะเบียนเป้าหมายเดียวกันโดยเป็นส่วนหนึ่งของเหตุการณ์การรับสินค้าตามแอปคลังสินค้าเดียว แต่จะมีการพิมพ์ป้ายชื่อทะเบียนเพียงป้ายชื่อเดียวเมื่อได้รับผลิตภัณฑ์

## <a name="resolution"></a>ความละเอียด

ระบบมีการทำงานตามที่ออกแบบ

ในการออกแบบปัจจุบัน จะมีการสร้างป้ายชื่อทะเบียนเดียวเสมอ ไม่ว่าจํานวนของหัวข้องานและชุดรายการงานที่มีอยู่จะเป็นอย่างไรก็ตาม ป้ายชื่อที่สร้างมีข้อมูลเพียงชุดเดียว

เมื่อต้องการแก้ไขปัญหานี้ ให้ตรวจสอบให้แน่ใจว่าการสร้างหัวข้อของงานได้รับการแม็ปกับป้ายทะเบียนเป้าหมายเพียงป้ายเดียวเสมอ
