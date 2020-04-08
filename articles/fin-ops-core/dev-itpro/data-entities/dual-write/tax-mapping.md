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
# <a name="integrated-tax"></a>ภาษีที่รวม

[!include [banner](../../includes/banner.md)]



ข้อมูลการตั้งค่าภาษีกำหนดการตั้งค่าสำหรับทั้งภาษีทางอ้อม (VAT, GST, ภาษีขาย) และภาษีหัก ณ ที่จ่าย อธิบายกฎการคำนวณภาษี อัตราภาษี บัญชีภาษี การชำระเงิน และแนวคิดอื่นๆ

## <a name="templates"></a>เท็มเพลต

ข้อมูลภาษีรวมชุดของแผนผังเอนทิตีทำงาน ที่ร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้

| แอป Finance and Operations | แอปที่เป็นแบบโมเดลใน Dynamics 365 | คำอธิบาย |
-------------------------|---------------------------------
รหัสภาษี                   | msdyn\_taxcodes.md | 
กลุ่มภาษี                 | msdyn\_taxgroups.md | 
กลุ่มภาษีสินค้า             | msdyn\_taxitemgroups.md | 
ยกเว้นภาษี             | msdyn\_taxexemptcodes.md | 
หน่วยงานจัดเก็บภาษี             | msdyn\_taxauthorities.md | 
รหัสภาษีหัก ณ ที่จ่าย       | msdyn\_withholdingtaxcodes.md | 
กลุ่มภาษีหัก ณ ที่จ่าย     | msdyn\_withholdingtaxgroups.md | 
กลุ่มบัญชีแยกประเภทของภาษี | msdyn\_taxpostinggroups     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

