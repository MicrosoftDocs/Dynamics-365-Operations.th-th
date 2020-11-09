---
title: บัญชีแยกประเภทที่รวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลบัญชีแยกประเภทระหว่าง Finance and Operations และแอปพลิเคชัน Dynamics 365 โดยใช้ Common Data Service
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7f5435a97776b817a4b99887cbab8283de25b692
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014869"
---
# <a name="integrated-ledger"></a>บัญชีแยกประเภทแบบรวม

[!include [banner](../../includes/banner.md)]



ในแอปพลิเคชันธุรกิจ ข้อมูลบัญชีแยกประเภทจะกำหนดหลักที่ตั้งค่าไว้สำหรับวิธีการดำเนินธุรกิจของบริษัท ตัวอย่างเช่น ข้อมูลบัญชีแยกประเภทจะอธิบายถึงปีบัญชีที่บริษัทดำเนินตาม สกุลเงินที่ใช้ทำธุรกรรม และบัญชีที่ใช้ หัวข้อนี้จะอธิบายการรวมของข้อมูลทางการเงินหลักนี้

## <a name="templates"></a>เท็มเพลต

ข้อมูลบัญชีแยกประเภทรวมชุดของแผนผังเอนทิตีทางการเงินหลัก ที่ร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้

แอป Finance and Operations      | แอปที่เป็นแบบโมเดลใน Dynamics 365 | คำอธิบาย
---------------------------------|----------------------------------|------------
สกุลเงิน                       | transactioncurrencies            |
FiscalCalendar                   | msdyn\_fiscalcalendars        |
FiscalCalendarYear               | msdyn\_fiscalcalendaryears        |
ExchRateType                     | msdyn\_exchangeratetypes        |
ExchangeRateCurrencyPair         | msdyn\_currencyexchangeratepairs        |
FiscalPeriodEntity               | msdyn\_fiscalcalendarperiods        |
MainAccountCategory              | msdyn\_mainaccountcategory        |
MainAccount                      | msdyn\_mainaccounts        |
บัญชีแยกประเภท                           | msdyn\_ledgers        |
ExchangeRates                    | msdyn\_currencyexchangerates        |
FinancialCalendarPeriod          | msdyn\_fiscalcalendarperiods        |
DimensionAttributeEntity         | msdyn\_dimensionattributes        |
DimensionIntegrationFormatEntity | msdyn\_financialdimensionformats        |
LedgerChartOfAccounts            | msdyn\_chartofaccounts        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




