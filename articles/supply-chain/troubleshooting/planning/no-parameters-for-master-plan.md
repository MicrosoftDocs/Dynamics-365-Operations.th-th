---
title: ไม่มีพารามิเตอร์ของแผนหลักอยู่
description: เมื่อคุณพยายามยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่าไม่มีพารามิเตอร์อยู่
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
ms.openlocfilehash: d039b79684f87e7791fb9dae7cbdc6ced220bc092d9a0ab624616c1c345986da
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756786"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a>ไม่มีพารามิเตอร์ของแผนหลักอยู่

รหัสข้อผิดพลาด: SYS25368

## <a name="symptoms"></a>อาการ

เมื่อคุณพยายามยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:

> ไม่มีพารามิเตอร์สำหรับแผนหลัก %1 อยู่

## <a name="cause"></a>สาเหตุ

เนื่องจากปัญหาการตั้งค่าคอนฟิก ระบบไม่พบการตั้งค่าของแผนที่ระบุ

## <a name="resolution"></a>การแก้ปัญหา

- ไปที่ **การวางแผนหลัก \> การตั้งค่า \> แผน \> แผนหลัก** และตรวจสอบให้แน่ใจว่ามีแผนที่มีชื่อที่ระบุอยู่
