---
title: ข้อผิดพลาดเกี่ยวกับพาธใบรับรอง เมื่ออัพเกรดหรือย้ายเป็น WMS
description: หากแอปแสดงข้อผิดพลาด "ไม่พบจุดยึดความเชื่อถือสำหรับพาธใบรับรอง" เมื่ออัพเกรดหรือย้ายไปที่ WMS หน้านี้จะให้ข้อมูลเกี่ยวกับวิธีการแก้ไขปัญหา
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477714"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>ไม่พบจุดยึดความเชื่อถือสำหรับพาธใบรับรอง เมื่ออัพเดตหรือย้ายไปที่ WMS

## <a name="symptoms"></a>อาการ

เมื่ออัพเกรดหรือย้ายไปที่ Warehouse Management (WMS) ขั้นสูง แอป Warehouse Management อาจแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:

> java.security.cert.certPathValidatorException: ไม่พบจุดยึดความเชื่อถือสำหรับพาธใบรับรอง

## <a name="cause"></a>สาเหตุ

นี่เกิดขึ้นเนื่องจากใบรับรองที่ลงชื่อด้วยตนเองไม่ได้รับความไว้วางใจใน Android 8+ ในสภาพแวดล้อมในสถานที่

## <a name="resolution"></a>การแก้ปัญหา

ใช้หน่วยงานรับรองภายนอก (สาธารณะ) (CA) การแก้ไขสำหรับปัญหานี้จะพร้อมใช้งานในรุ่น 1.9.0.0 ของแอป Warehouse Management สำหรับข้อมูลเพิ่มเติมเกี่ยวกับปัญหานี้และวิธีการแก้ไข โปรดดูที่ [ไม่พบจุดยึดความเชื่อถือสำหรับพาธใบรับรอง เมื่อตั้งค่าการเชื่อมต่อแอป](certification-path-app-connection-error.md)
