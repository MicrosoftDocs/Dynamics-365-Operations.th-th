---
title: การรับป้ายทะเบียนแบบผสมไม่ทำงานสำหรับรหัสการโอนการครอบครองทั้งหมด
description: เมื่อฟิลด์ การดำเนินการ สำหรับรหัสการโอนการครอบครองถูกตั้งค่าเป็น เครดิต หรือ เสีย คุณสามารถใช้ได้เฉพาะ รายการเมนูการรับป้ายทะเบียนแบบผสม เพื่อประมวลผลสินค้าที่ส่งคืนเท่านั้น
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b762255bc5ef6a1e15688a9c635940e92e67db3c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477765"
---
# <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-but-credit"></a>การรับป้ายทะเบียนแบบผสมไม่ทำงานสำหรับรหัสการโอนการครอบครองใด ๆ ยกเว้นเครดิต

## <a name="symptoms"></a>อาการ

เมื่อฟิลด์ **การดำเนินการ** สำหรับรหัสการโอนการครอบครองถูกตั้งค่าเป็น *เครดิต* หรือ *เสีย* คุณสามารถใช้ได้เฉพาะ [รายการเมนูการรับป้ายทะเบียนแบบผสม](/dynamics365/supply-chain/warehousing/mixed-license-plate-receiving) เพื่อประมวลผลสินค้าที่ส่งคืนเท่านั้น

## <a name="resolution"></a>การแก้ปัญหา

Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน ปัจจุบัน เฉพาะ [รหัสการโอนการครอบครอง](/dynamics365/supply-chain/service-management/set-up-disposition-codes) ที่มีฟิลด์ **การดำเนินการ** ตั้งค่าเป็น *เครดิต* หรือ *เสีย* ได้รับการสนับสนุนสำหรับการรับป้ายทะเบียนแบบผสม
