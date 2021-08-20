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
ms.openlocfilehash: cf307964a07c2b69eb5e4ef2cf9dc094482736d0970e333e84f674c9be6331c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740538"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>มีการพิมพ์ป้ายชื่อเพียงป้ายชื่อเดียวหลายหัวข้อบนใบรับสินค้าเดียว

หมายเลข KB: 4614667

## <a name="symptoms"></a>อาการ

ส่วนหัวของงานหลายหัวข้อสร้างขึ้นเพื่อป้ายทะเบียนเป้าหมายเดียวกันโดยเป็นส่วนหนึ่งของเหตุการณ์การรับสินค้าตามแอปคลังสินค้าเดียว แต่จะมีการพิมพ์ป้ายชื่อทะเบียนเพียงป้ายชื่อเดียวเมื่อได้รับผลิตภัณฑ์

## <a name="resolution"></a>ความละเอียด

ระบบมีการทำงานตามที่ออกแบบ

ในการออกแบบปัจจุบัน จะมีการสร้างป้ายชื่อทะเบียนเดียวเสมอ ไม่ว่าจํานวนของหัวข้องานและชุดรายการงานที่มีอยู่จะเป็นอย่างไรก็ตาม ป้ายชื่อที่สร้างมีข้อมูลเพียงชุดเดียว

เมื่อต้องการแก้ไขปัญหานี้ ให้ตรวจสอบให้แน่ใจว่าการสร้างหัวข้อของงานได้รับการแม็ปกับป้ายทะเบียนเป้าหมายเพียงป้ายเดียวเสมอ
