---
title: ภาษีที่รวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลภาษีระหว่าง Finance and Operations และ Dataverse
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
ms.openlocfilehash: a7992520b57b4c19b6dc8e13bd8e9ffc87b40f5a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750653"
---
# <a name="integrated-tax"></a><span data-ttu-id="4cf0d-103">ภาษีที่รวม</span><span class="sxs-lookup"><span data-stu-id="4cf0d-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="4cf0d-104">ข้อมูลการตั้งค่าภาษีกำหนดการตั้งค่าสำหรับทั้งภาษีทางอ้อม (VAT, GST, ภาษีขาย) และภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="4cf0d-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="4cf0d-105">อธิบายกฎการคำนวณภาษี อัตราภาษี บัญชีภาษี การชำระเงิน และแนวคิดอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="4cf0d-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="4cf0d-106">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="4cf0d-106">Templates</span></span>

<span data-ttu-id="4cf0d-107">ข้อมูลภาษีรวมชุดของแผนผังตารางทำงาน ที่ร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4cf0d-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="4cf0d-108">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4cf0d-108">Finance and Operations apps</span></span> | <span data-ttu-id="4cf0d-109">แอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4cf0d-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="4cf0d-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4cf0d-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="4cf0d-111">กลุ่มภาษีขายตามประเภทสินค้า</span><span class="sxs-lookup"><span data-stu-id="4cf0d-111">Item sales tax group</span></span> | <span data-ttu-id="4cf0d-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="4cf0d-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="4cf0d-113">หน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="4cf0d-113">Sales tax authorities</span></span> | <span data-ttu-id="4cf0d-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="4cf0d-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="4cf0d-115">เอนทิตี้รหัสยกเว้นภาษีขายสำหรับ CDS</span><span class="sxs-lookup"><span data-stu-id="4cf0d-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="4cf0d-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="4cf0d-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="4cf0d-117">กลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="4cf0d-117">Sales tax groups</span></span> | <span data-ttu-id="4cf0d-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="4cf0d-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="4cf0d-119">กลุ่มการลงรายการบัญชีแยกประเภทของภาษีขาย V2</span><span class="sxs-lookup"><span data-stu-id="4cf0d-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="4cf0d-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="4cf0d-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="4cf0d-121">รหัสภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="4cf0d-121">Withholding tax codes</span></span> | <span data-ttu-id="4cf0d-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="4cf0d-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="4cf0d-123">กลุ่มภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="4cf0d-123">Withholding tax groups</span></span> | <span data-ttu-id="4cf0d-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="4cf0d-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]