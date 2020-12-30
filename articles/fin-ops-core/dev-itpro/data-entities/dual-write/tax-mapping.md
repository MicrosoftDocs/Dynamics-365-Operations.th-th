---
title: ภาษีที่รวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลภาษีระหว่าง Finance and Operations และ Dataverse
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
ms.openlocfilehash: 14c22dd6602b5fbf866c8dc6b057f6c8acb1f48f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679307"
---
# <a name="integrated-tax"></a><span data-ttu-id="3bf9a-103">ภาษีที่รวม</span><span class="sxs-lookup"><span data-stu-id="3bf9a-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="3bf9a-104">ข้อมูลการตั้งค่าภาษีกำหนดการตั้งค่าสำหรับทั้งภาษีทางอ้อม (VAT, GST, ภาษีขาย) และภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="3bf9a-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="3bf9a-105">อธิบายกฎการคำนวณภาษี อัตราภาษี บัญชีภาษี การชำระเงิน และแนวคิดอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="3bf9a-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="3bf9a-106">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="3bf9a-106">Templates</span></span>

<span data-ttu-id="3bf9a-107">ข้อมูลภาษีรวมชุดของแผนผังตารางทำงาน ที่ร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3bf9a-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="3bf9a-108">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3bf9a-108">Finance and Operations apps</span></span> | <span data-ttu-id="3bf9a-109">แอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3bf9a-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="3bf9a-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3bf9a-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="3bf9a-111">กลุ่มภาษีขายตามประเภทสินค้า</span><span class="sxs-lookup"><span data-stu-id="3bf9a-111">Item sales tax group</span></span> | <span data-ttu-id="3bf9a-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="3bf9a-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="3bf9a-113">หน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3bf9a-113">Sales tax authorities</span></span> | <span data-ttu-id="3bf9a-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="3bf9a-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="3bf9a-115">เอนทิตี้รหัสยกเว้นภาษีขายสำหรับ CDS</span><span class="sxs-lookup"><span data-stu-id="3bf9a-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="3bf9a-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="3bf9a-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="3bf9a-117">กลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3bf9a-117">Sales tax groups</span></span> | <span data-ttu-id="3bf9a-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="3bf9a-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="3bf9a-119">กลุ่มการลงรายการบัญชีแยกประเภทของภาษีขาย V2</span><span class="sxs-lookup"><span data-stu-id="3bf9a-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="3bf9a-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="3bf9a-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="3bf9a-121">รหัสภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="3bf9a-121">Withholding tax codes</span></span> | <span data-ttu-id="3bf9a-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="3bf9a-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="3bf9a-123">กลุ่มภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="3bf9a-123">Withholding tax groups</span></span> | <span data-ttu-id="3bf9a-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="3bf9a-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

