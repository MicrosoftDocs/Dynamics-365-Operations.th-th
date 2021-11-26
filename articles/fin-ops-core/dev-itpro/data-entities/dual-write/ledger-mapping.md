---
title: บัญชีแยกประเภทที่รวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลบัญชีแยกประเภทระหว่าง Finance and Operations และแอปพลิเคชัน Dynamics 365 โดยใช้ Dataverse
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e41d600464d707d01a0e319dd3cd343b04aa26b7
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782391"
---
# <a name="integrated-ledger"></a>บัญชีแยกประเภทแบบรวม

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

ในแอปพลิเคชันธุรกิจ ข้อมูลบัญชีแยกประเภทจะกำหนดหลักที่ตั้งค่าไว้สำหรับวิธีการดำเนินธุรกิจของบริษัท ตัวอย่างเช่น ข้อมูลบัญชีแยกประเภทจะอธิบายถึงปีบัญชีที่บริษัทดำเนินตาม สกุลเงินที่ใช้ทำธุรกรรม และบัญชีที่ใช้ หัวข้อนี้จะอธิบายการรวมของข้อมูลทางการเงินหลักนี้

## <a name="templates"></a>เท็มเพลต

ข้อมูลบัญชีแยกประเภทรวมชุดของแผนผังตารางทางการเงินหลัก ที่ร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้

แอป Finance and Operations | แอป Customer Engagement     | คำอธิบาย
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
