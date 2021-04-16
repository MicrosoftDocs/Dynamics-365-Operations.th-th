---
title: ความถี่ในการคัดกรอง
description: หัวข้อนี้อธิบายชุดตัวเลือกความถี่ของคัดกรองสำหรับ Dynamics 365 Human Resources
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba1fba598bca088e67d8cb2865d1ea9baa97f19e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801274"
---
# <a name="screening-frequency"></a>ความถี่ในการคัดกรอง

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายชุดตัวเลือกความถี่ของคัดกรองสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmfrequencyunit

การแจงหมายเลขนี้จะให้ชุดตัวเลือกของค่าสำหรับความถี่ในการคัดกรอง 

| มูลค่า | ป้ายชื่อ | คำอธิบาย |
| --- | --- | --- |
| 200000000 ครั้งเดียวเท่านั้น | ต้องมีคัดกรองเพียงครั้งเดียว |
| 200000001 รายวัน | ความถี่ของคัดกรองจะคํานวณเป็นวัน |
| 200000002 รายสัปดาห์ | ความถี่ของคัดกรองจะคํานวณเป็นสัปดาห์ |
| 200000003 รายเดือน | ความถี่ของคัดกรองจะคํานวณเป็นเดือน |
| 200000004 รายปี | ความถี่ของคัดกรองจะคํานวณเป็นปี |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]