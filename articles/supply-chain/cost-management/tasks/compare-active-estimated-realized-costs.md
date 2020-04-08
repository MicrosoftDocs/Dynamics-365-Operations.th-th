---
title: เปรียบเทียบต้นทุนที่ใช้งานอยู่ ต้นทุนโดยประมาณ และต้นทุนที่เกิดขึ้นจริงในใบสั่งผลิต
description: 'กระบวนงานนี้แสดงวิธีการดูสาเหตุของผลต่างของการผลิตระดับสูงสำหรับใบสั่งผลิต '
author: AndersGirke
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, CostAdminWorkspace, CostLastInventoryCloseCard, CostLastBackflushCostingCard, CostStatementCacheCard, CostReleasedProductsMissingCostingDataFormPart, CostCalculationPeriodTopVariancesChartFormPart, CostSelectPeriodDialogForm, CostCalculationPeriodTopVariancesListFormPart, ProdTable, CostCalculationCompareDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47c87f47e200c06d750a713b1adafe18955478db
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150498"
---
# <a name="compare-active-estimated-and-realized-costs-on-a-production-order"></a>เปรียบเทียบต้นทุนที่ใช้งานอยู่ ต้นทุนโดยประมาณ และต้นทุนที่เกิดขึ้นจริงในใบสั่งผลิต

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการดูสาเหตุของผลต่างของการผลิตระดับสูงสำหรับใบสั่งผลิต  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF กระบวนการนี้มีไว้สำหรับผู้ควบคุมต้นทุน

1. คลิกการบริหารต้นทุน
2. ในฟิลด์วันที่ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * กระบวนงานนี้ใช้ปีบัญชี 2012 คุณสามารถตั้งค่าวันที่เริ่มต้นเป็นวันที่ 1 มกราคม 2012 และวันที่สิ้นสุดเป็นวันที่ 31 ธันวาคม 2012  
3. คลิกแท็บผลต่างของการผลิตระดับสูง
4. คลิกเพื่อติดตามลิงค์ในฟิลด์การผลิต
    * คลิก P000116 เพื่อติดตามลิงค์ในฟิลด์การผลิต  
5. ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน
6. คลิกดูการเปรียบเทียบต้นทุน
7. คลิก ปิด

