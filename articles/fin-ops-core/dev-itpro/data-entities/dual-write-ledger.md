---
title: บัญชีแยกประเภทที่รวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลบัญชีแยกประเภทระหว่าง Finance and Operations และ Customer Engagement โดยใช้ Common Data Service
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 43819e23b167663a51095546cab307e7d7c79a38
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771059"
---
## <a name="integrated-ledger"></a><span data-ttu-id="12819-103">บัญชีแยกประเภทที่รวม</span><span class="sxs-lookup"><span data-stu-id="12819-103">Integrated ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12819-104">ในแอปพลิเคชันธุรกิจ ข้อมูลบัญชีแยกประเภทจะกำหนดหลักที่ตั้งค่าไว้สำหรับวิธีการดำเนินธุรกิจของบริษัท</span><span class="sxs-lookup"><span data-stu-id="12819-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="12819-105">ตัวอย่างเช่น ข้อมูลบัญชีแยกประเภทจะอธิบายถึงปีบัญชีที่บริษัทดำเนินตาม สกุลเงินที่ใช้ทำธุรกรรม และบัญชีที่ใช้</span><span class="sxs-lookup"><span data-stu-id="12819-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="12819-106">หัวข้อนี้จะอธิบายการรวมของข้อมูลทางการเงินหลักนี้</span><span class="sxs-lookup"><span data-stu-id="12819-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="12819-107">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="12819-107">Templates</span></span>

<span data-ttu-id="12819-108">ข้อมูลบัญชีแยกประเภทรวมชุดของแผนผังเอนทิตีทางการเงินหลัก ที่ร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="12819-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="12819-109">แอพ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="12819-109">Finance and Operations apps</span></span>      | <span data-ttu-id="12819-110">แอปพลิเคชันอื่น ๆ ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="12819-110">Other Dynamics 365 apps</span></span>
---------------------------------|---------------------------------
<span data-ttu-id="12819-111">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="12819-111">Currencies</span></span>                       | <span data-ttu-id="12819-112">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="12819-112">transactioncurrencies</span></span>
<span data-ttu-id="12819-113">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="12819-113">FiscalCalendar</span></span>                   | <span data-ttu-id="12819-114">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="12819-114">msdyn\_fiscalcalendars</span></span>
<span data-ttu-id="12819-115">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="12819-115">FiscalCalendarYear</span></span>               | <span data-ttu-id="12819-116">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="12819-116">msdyn\_fiscalcalendaryears</span></span>
<span data-ttu-id="12819-117">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="12819-117">ExchRateType</span></span>                     | <span data-ttu-id="12819-118">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="12819-118">msdyn\_exchangeratetypes</span></span>
<span data-ttu-id="12819-119">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="12819-119">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="12819-120">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="12819-120">msdyn\_currencyexchangeratepairs</span></span>
<span data-ttu-id="12819-121">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="12819-121">FiscalPeriodEntity</span></span>               | <span data-ttu-id="12819-122">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="12819-122">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="12819-123">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="12819-123">MainAccountCategory</span></span>              | <span data-ttu-id="12819-124">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="12819-124">msdyn\_mainaccountcategory</span></span>
<span data-ttu-id="12819-125">MainAccount</span><span class="sxs-lookup"><span data-stu-id="12819-125">MainAccount</span></span>                      | <span data-ttu-id="12819-126">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="12819-126">msdyn\_mainaccounts</span></span>
<span data-ttu-id="12819-127">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="12819-127">Ledger</span></span>                           | <span data-ttu-id="12819-128">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="12819-128">msdyn\_ledgers</span></span>
<span data-ttu-id="12819-129">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="12819-129">ExchangeRates</span></span>                    | <span data-ttu-id="12819-130">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="12819-130">msdyn\_currencyexchangerates</span></span>
<span data-ttu-id="12819-131">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="12819-131">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="12819-132">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="12819-132">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="12819-133">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="12819-133">DimensionAttributeEntity</span></span>         | <span data-ttu-id="12819-134">msdyn\_dimensionattributes.md</span><span class="sxs-lookup"><span data-stu-id="12819-134">msdyn\_dimensionattributes.md</span></span>
<span data-ttu-id="12819-135">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="12819-135">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="12819-136">msdyn\_financialdimensionformats.md</span><span class="sxs-lookup"><span data-stu-id="12819-136">msdyn\_financialdimensionformats.md</span></span>
<span data-ttu-id="12819-137">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="12819-137">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="12819-138">msdyn\_chartofaccounts.md</span><span class="sxs-lookup"><span data-stu-id="12819-138">msdyn\_chartofaccounts.md</span></span>


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Currency](dual-write/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](dual-write/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](dual-write/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](dual-write/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](dual-write/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](dual-write/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](dual-write/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](dual-write/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](dual-write/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](dual-write/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](dual-write/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](dual-write/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




