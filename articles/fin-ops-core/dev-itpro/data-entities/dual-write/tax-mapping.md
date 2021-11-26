---
title: ภาษีที่รวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลภาษีระหว่าง Finance and Operations และ Dataverse
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: d1e74bbbeba019ca48dd823b58251643e96edd0c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782221"
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
