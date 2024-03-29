---
title: ภาพรวมของเอนทิตี้ต้นทุนแฝง
description: ในบทความนี้จะแสดงภาพรวมของเอนทิตีข้อมูลของต้นทุนแฝง ซึ่งเปิดใช้งานแหล่งข้อมูลภายนอกเพื่อสร้างการเดินทางและต้นทุน และอัปเดตเรกคอร์ดการติดตามคอนเทนเนอร์
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 03d05bf5dee5c6bcf322f5be9dd69c23234d52fd
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166685"
---
# <a name="landed-cost-entities-overview"></a>ภาพรวมของเอนทิตีต้นทุนแฝง

[!include [banner](../includes/banner.md)]

**โมดูลต้นทุนแฝง** ช่วยให้ธุรกิจสามารถลดขั้นตอนการดำเนินการจัดส่งสินค้าขาเข้าได้ โดยการให้การควบคุมทางการเงินและลอจิสติกส์การขนส่งที่นําเข้า จากผู้ผลิตไปยังคลังสินค้าได้ เอนทิตีข้อมูลธุรกรรมของต้นทุนแฝง ซึ่งเปิดใช้งานแหล่งข้อมูลภายนอก (เช่น บริการผู้ขนส่งสินค้า) เพื่อสร้างการเดินทางและต้นทุน และอัปเดตเรกคอร์ดการติดตามคอนเทนเนอร์

นี่คือบางส่วนของการดำเนินการที่รองรับ:

- สร้างและอัปเดตการเดินทาง คอนเทนเนอร์ขนส่ง และเรกคอร์ดใบแจ้งรายการที่มีอยู่ของใบสั่งขาเข้า
- สร้างและอัปเดตต้นทุนที่ประเมินต่อพื้นที่ต้นทุนแต่ละพื้นที่
- สร้างและอัพเปตเรกคอร์ดกิจกรรมคอนเทนเนอร์ขนส่งเพื่อบันทึกวันที่เริ่มต้น วันที่สิ้นสุดที่ประเมิน และวันที่สิ้นสุดจริงให้กับแต่ละขาของการเดินทางของคอนเทนเนอร์
- สร้างการปันส่วนใบแจ้งหนี้ต้นทุนผู้จัดจำหน่าย
