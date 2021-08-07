---
title: ภาษีที่รวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลภาษีระหว่าง Finance and Operations และ Dataverse
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e1b5d62e56dd1f87dbfedc6a8ca7379587481ff4
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542330"
---
# <a name="integrated-tax"></a>ภาษีที่รวม

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

ข้อมูลการตั้งค่าภาษีกำหนดการตั้งค่าสำหรับทั้งภาษีทางอ้อม (VAT, GST, ภาษีขาย) และภาษีหัก ณ ที่จ่าย อธิบายกฎการคำนวณภาษี อัตราภาษี บัญชีภาษี การชำระเงิน และแนวคิดอื่นๆ

## <a name="templates"></a>เท็มเพลต

ข้อมูลภาษีรวมชุดของแผนผังตารางทำงาน ที่ร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้

| แอป Finance and Operations | แอป Customer Engagement | คำอธิบาย |
|-----------------------------|-----------------------------------|-------------|
[กลุ่มภาษีขายตามประเภทสินค้า](mapping-reference.md#196) | msdyn_taxitemgroups | |
[หน่วยงานจัดเก็บภาษีขาย](mapping-reference.md#193) | msdyn_taxauthorities | |
[เอนทิตี้รหัสยกเว้นภาษีขายสำหรับ CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[กลุ่มภาษีขาย](mapping-reference.md#195) | msdyn_taxgroups | |
[กลุ่มการลงรายการบัญชีแยกประเภทของภาษีขาย V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[รหัสภาษีหัก ณ ที่จ่าย](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[กลุ่มภาษีหัก ณ ที่จ่าย](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
