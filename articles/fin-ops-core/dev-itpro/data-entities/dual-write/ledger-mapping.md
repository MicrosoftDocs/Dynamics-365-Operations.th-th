---
title: บัญชีแยกประเภทแบบรวม
description: บทความนี้อธิบายการรวมของข้อมูลบัญชีแยกประเภทระหว่างแอปการเงินและการดำเนินงานและแอปพลิเคชัน Dynamics 365 โดยใช้ Dataverse
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e83d66f3f8c8927b9baaf99838a4e242e7e011dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847202"
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
