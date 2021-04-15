---
title: บัญชีแยกประเภทที่รวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลบัญชีแยกประเภทระหว่าง Finance and Operations และแอปพลิเคชัน Dynamics 365 โดยใช้ Dataverse
author: robinarh
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5fedcbcd8db2692214ea66b2fbab9f7381e0a622
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748528"
---
# <a name="integrated-ledger"></a><span data-ttu-id="7bf97-103">บัญชีแยกประเภทแบบรวม</span><span class="sxs-lookup"><span data-stu-id="7bf97-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="7bf97-104">ในแอปพลิเคชันธุรกิจ ข้อมูลบัญชีแยกประเภทจะกำหนดหลักที่ตั้งค่าไว้สำหรับวิธีการดำเนินธุรกิจของบริษัท</span><span class="sxs-lookup"><span data-stu-id="7bf97-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="7bf97-105">ตัวอย่างเช่น ข้อมูลบัญชีแยกประเภทจะอธิบายถึงปีบัญชีที่บริษัทดำเนินตาม สกุลเงินที่ใช้ทำธุรกรรม และบัญชีที่ใช้</span><span class="sxs-lookup"><span data-stu-id="7bf97-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="7bf97-106">หัวข้อนี้จะอธิบายการรวมของข้อมูลทางการเงินหลักนี้</span><span class="sxs-lookup"><span data-stu-id="7bf97-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="7bf97-107">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="7bf97-107">Templates</span></span>

<span data-ttu-id="7bf97-108">ข้อมูลบัญชีแยกประเภทรวมชุดของแผนผังตารางทางการเงินหลัก ที่ร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7bf97-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="7bf97-109">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7bf97-109">Finance and Operations apps</span></span>      | <span data-ttu-id="7bf97-110">แอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7bf97-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="7bf97-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7bf97-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="7bf97-112">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="7bf97-112">Currencies</span></span>                       | <span data-ttu-id="7bf97-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="7bf97-113">transactioncurrencies</span></span>            |
<span data-ttu-id="7bf97-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="7bf97-114">FiscalCalendar</span></span>                   | <span data-ttu-id="7bf97-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="7bf97-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="7bf97-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="7bf97-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="7bf97-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="7bf97-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="7bf97-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="7bf97-118">ExchRateType</span></span>                     | <span data-ttu-id="7bf97-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="7bf97-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="7bf97-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="7bf97-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="7bf97-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="7bf97-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="7bf97-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="7bf97-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="7bf97-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="7bf97-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="7bf97-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="7bf97-124">MainAccountCategory</span></span>              | <span data-ttu-id="7bf97-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="7bf97-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="7bf97-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="7bf97-126">MainAccount</span></span>                      | <span data-ttu-id="7bf97-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="7bf97-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="7bf97-128">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="7bf97-128">Ledger</span></span>                           | <span data-ttu-id="7bf97-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="7bf97-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="7bf97-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="7bf97-130">ExchangeRates</span></span>                    | <span data-ttu-id="7bf97-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="7bf97-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="7bf97-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="7bf97-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="7bf97-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="7bf97-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="7bf97-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="7bf97-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="7bf97-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="7bf97-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="7bf97-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="7bf97-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="7bf97-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="7bf97-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="7bf97-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="7bf97-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="7bf97-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="7bf97-139">msdyn\_chartofaccounts</span></span>        |


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






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]