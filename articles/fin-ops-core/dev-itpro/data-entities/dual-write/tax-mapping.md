---
title: ภาษีที่รวม
description: บทความนี้อธิบายการรวมของข้อมูลภาษีระหว่างแอปการเงินและการดำเนินงานกับ Dataverse
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288808"
---
# <a name="integrated-tax"></a>ภาษีที่รวม

[!include [banner](../../includes/banner.md)]



ข้อมูลการตั้งค่าภาษีกำหนดการตั้งค่าสำหรับทั้งภาษีทางอ้อม (VAT, GST, ภาษีขาย) และภาษีหัก ณ ที่จ่าย อธิบายกฎการคำนวณภาษี อัตราภาษี บัญชีภาษี การชำระเงิน และแนวคิดอื่นๆ

## <a name="templates"></a>เทมเพลต

ข้อมูลภาษีรวมชุดของแผนผังตารางทำงาน ที่ร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้

| แอปการเงินและการดำเนินงาน | แอปการมีส่วนร่วมของลูกค้า | คำอธิบาย |
|-----------------------------|-----------------------------------|-------------|
[กลุ่มภาษีขายตามประเภทสินค้า](mapping-reference.md#196) | msdyn_taxitemgroups | |
[หน่วยงานจัดเก็บภาษีขาย](mapping-reference.md#193) | msdyn_taxauthorities | |
[เอนทิตี้รหัสยกเว้นภาษีขายสำหรับ CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[กลุ่มภาษีขาย](mapping-reference.md#195) | msdyn_taxgroups | |
[กลุ่มการลงรายการบัญชีแยกประเภทของภาษีขาย V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[รหัสภาษีหัก ณ ที่จ่าย](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[กลุ่มภาษีหัก ณ ที่จ่าย](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

