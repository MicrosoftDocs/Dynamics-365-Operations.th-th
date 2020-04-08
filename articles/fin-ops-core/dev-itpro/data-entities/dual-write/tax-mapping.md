---
title: ภาษีที่รวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลภาษีระหว่าง Finance and Operations และ Common Data Service
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
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173096"
---
# <a name="integrated-tax"></a><span data-ttu-id="e2873-103">ภาษีที่รวม</span><span class="sxs-lookup"><span data-stu-id="e2873-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e2873-104">ข้อมูลการตั้งค่าภาษีกำหนดการตั้งค่าสำหรับทั้งภาษีทางอ้อม (VAT, GST, ภาษีขาย) และภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="e2873-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="e2873-105">อธิบายกฎการคำนวณภาษี อัตราภาษี บัญชีภาษี การชำระเงิน และแนวคิดอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="e2873-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="e2873-106">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="e2873-106">Templates</span></span>

<span data-ttu-id="e2873-107">ข้อมูลภาษีรวมชุดของแผนผังเอนทิตีทำงาน ที่ร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e2873-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="e2873-108">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e2873-108">Finance and Operations apps</span></span> | <span data-ttu-id="e2873-109">แอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e2873-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="e2873-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e2873-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="e2873-111">รหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="e2873-111">Tax codes</span></span>                   | <span data-ttu-id="e2873-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="e2873-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="e2873-113">กลุ่มภาษี</span><span class="sxs-lookup"><span data-stu-id="e2873-113">Tax groups</span></span>                 | <span data-ttu-id="e2873-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="e2873-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="e2873-115">กลุ่มภาษีสินค้า</span><span class="sxs-lookup"><span data-stu-id="e2873-115">Tax item groups</span></span>             | <span data-ttu-id="e2873-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="e2873-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="e2873-117">ยกเว้นภาษี</span><span class="sxs-lookup"><span data-stu-id="e2873-117">Tax Exemptions</span></span>             | <span data-ttu-id="e2873-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="e2873-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="e2873-119">หน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="e2873-119">Tax Authorities</span></span>             | <span data-ttu-id="e2873-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="e2873-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="e2873-121">รหัสภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="e2873-121">Withholding tax codes</span></span>       | <span data-ttu-id="e2873-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="e2873-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="e2873-123">กลุ่มภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="e2873-123">Withholding tax groups</span></span>     | <span data-ttu-id="e2873-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="e2873-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="e2873-125">กลุ่มบัญชีแยกประเภทของภาษี</span><span class="sxs-lookup"><span data-stu-id="e2873-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="e2873-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="e2873-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

