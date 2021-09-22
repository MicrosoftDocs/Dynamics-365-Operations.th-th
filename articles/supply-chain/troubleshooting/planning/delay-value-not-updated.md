---
title: ค่าความล่าช้าจะไม่ได้รับการอัพเดตเมื่อคุณจัดกำหนดการแผนการใบสั่งใหม่
description: ค่าความล่าช้าจะไม่ได้รับการอัพเดตเมื่อคุณจัดกำหนดการแผนการใบสั่งใหม่
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 566702913774cf002ab38e367f690a479d968657
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477763"
---
# <a name="the-delay-value-isnt-updated-when-you-reschedule-a-planned-order"></a>ค่าความล่าช้าจะไม่ได้รับการอัพเดตเมื่อคุณจัดกำหนดการแผนการใบสั่งใหม่

## <a name="symptoms"></a>อาการ

ค่าความล่าช้าจะไม่ได้รับการอัพเดตเมื่อคุณจัดกำหนดการแผนการใบสั่งใหม่

## <a name="resolution"></a>การแก้ปัญหา

เมื่อต้องการอัพเดตการหน่วงเวลาสำหรับแผนการใบสั่ง ให้เปิดกล่องโต้ตอบ **การจัดกำหนดการใหม่** สำหรับใบสั่งที่วางแผน บนแท็บด่วน **การกระจาย** โปรดตรวจสอบให้แน่ใจว่า มีการตั้งค่าตัวเลือก **ประมวลผลการกระจายหลังจากจัดกำหนดการใหม่** เป็น *ใช่*
