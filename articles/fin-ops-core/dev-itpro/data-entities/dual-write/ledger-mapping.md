---
title: บัญชีแยกประเภทแบบรวม
description: บทความนี้อธิบายการรวมของข้อมูลบัญชีแยกประเภทระหว่างแอปการเงินและการดำเนินงานและแอปพลิเคชัน Dynamics 365 โดยใช้ Dataverse
author: RamaKrishnamoorthy
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 728c131c260586e7f1f787f22ccf02ed81c94c01
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289162"
---
# <a name="integrated-ledger"></a>บัญชีแยกประเภทแบบรวม

[!include [banner](../../includes/banner.md)]



ในแอปพลิเคชันธุรกิจ ข้อมูลบัญชีแยกประเภทจะกำหนดหลักที่ตั้งค่าไว้สำหรับวิธีการดำเนินธุรกิจของบริษัท ตัวอย่างเช่น ข้อมูลบัญชีแยกประเภทจะอธิบายถึงปีบัญชีที่บริษัทดำเนินตาม สกุลเงินที่ใช้ทำธุรกรรม และบัญชีที่ใช้ บทความนี้จะอธิบายการรวมของข้อมูลทางการเงินหลักนี้

## <a name="templates"></a>เท็มเพลต

ข้อมูลบัญชีแยกประเภทรวมชุดของแผนผังตารางทางการเงินหลัก ที่ร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้

แอปการเงินและการดำเนินงาน | แอปการมีส่วนร่วมของลูกค้า     | คำอธิบาย
---------------------------------|----------------------------------|------------
[อัตราแลกเปลี่ยน CDS](mapping-reference.md#123) | msdyn_currencyexchangerates |
[ผังบัญชี](mapping-reference.md#121) | msdyn_chartofaccountses |
[สกุลเงิน](mapping-reference.md#218) | transactioncurrencies |
[คู่สกุลเงินของอัตราแลกเปลี่ยน](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[ชนิดอัตราแลกเปลี่ยน](mapping-reference.md#129) | msdyn_exchangeratetypes |
[รูปแบบมิติทางการเงิน](mapping-reference.md#130) | msdyn_financialdimensionformats |
[มิติทางการเงิน](mapping-reference.md#128) | msdyn_dimensionattributes |
[เอนทิตี้การรวมปฏิทินทางการเงิน](mapping-reference.md#132) | msdyn_fiscalcalendars |
[รอบระยะเวลาปฏิทินทางการเงิน](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[เอนทิตี้การรวมปีปฏิทินทางการเงิน](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[Ledger](mapping-reference.md#148) | msdyn_ledgers |
[บัญชีหลัก](mapping-reference.md#152) | msdyn_mainaccounts |
[ประเภทบัญชีหลัก](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

