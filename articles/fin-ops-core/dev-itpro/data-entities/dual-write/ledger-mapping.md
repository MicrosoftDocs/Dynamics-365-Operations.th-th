---
title: บัญชีแยกประเภทที่รวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลบัญชีแยกประเภทระหว่าง Finance and Operations และแอปพลิเคชัน Dynamics 365 โดยใช้ Dataverse
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.openlocfilehash: 18a95725af8014845d6fb39806917de7632ad56b92b75387cd916de927127b38
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723092"
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
