---
title: ไม่สามารถนำโหลดที่จัดส่งแล้วบางส่วนไปใช้กับคลังสินค้าอีกครั้งได้
description: ในเวอร์ชันก่อนหน้านี้ คุณไม่สามารถนำโหลดที่จัดส่งแล้วบางส่วนไปใช้อีกครั้งได้ เมื่อใช้ฟังก์ชันบางอย่างที่มีการจองที่ไม่สมบูรณ์ นี่ได้รับการแก้ไขแล้ว
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477757"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>ไม่สามารถนำโหลดที่จัดส่งแล้วบางส่วนไปใช้กับคลังสินค้าอีกครั้งได้

## <a name="symptoms"></a>อาการ

คุณไม่สามารถนำโหลดบางอย่างไปใช้กับคลังสินค้าได้ เมื่อคุณทำการนำออกใช้ไปยังคลังสินค้า ข้อความ "การดำเนินการเสร็จสมบูรณ์" จะปรากฏขึ้น แต่ไม่มีอะไรเกิดขึ้น และไม่มีการสร้างงานสำหรับปริมาณคงเหลือ ปัญหานี้เกิดขึ้นเมื่อคุณใช้ฟังก์ชันโหลดการขนส่งและไม่มีการจองสินค้าที่ไม่สมบูรณ์

## <a name="resolution"></a>การแก้ปัญหา

[ปัญหา KB 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("โหลดที่จัดส่งบางส่วนอาจเวฟและประมวลผลใหม่") เป็นแบบคงที่ใน [รุ่น 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15)
