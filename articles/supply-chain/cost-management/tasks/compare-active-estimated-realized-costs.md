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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed9fac210ba19795cd1d7608b582965564decc2e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "347019"
---
# <a name="compare-active-estimated-and-realized-costs-on-a-production-order"></a><span data-ttu-id="39a35-103">เปรียบเทียบต้นทุนที่ใช้งานอยู่ ต้นทุนโดยประมาณ และต้นทุนที่เกิดขึ้นจริงในใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="39a35-103">Compare active, estimated, and realized costs on a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39a35-104">กระบวนงานนี้แสดงวิธีการดูสาเหตุของผลต่างของการผลิตระดับสูงสำหรับใบสั่งผลิต </span><span class="sxs-lookup"><span data-stu-id="39a35-104">This procedure shows how to view reasons for high production variance for a production order.</span></span> <span data-ttu-id="39a35-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="39a35-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="39a35-106">กระบวนการนี้มีไว้สำหรับผู้ควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="39a35-106">This procedure is intended for the cost controller.</span></span>

1. <span data-ttu-id="39a35-107">คลิกการบริหารต้นทุน</span><span class="sxs-lookup"><span data-stu-id="39a35-107">Click Cost administration.</span></span>
2. <span data-ttu-id="39a35-108">ในฟิลด์วันที่ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="39a35-108">In the Date field, enter or select a value.</span></span>
    * <span data-ttu-id="39a35-109">กระบวนงานนี้ใช้ปีบัญชี 2012</span><span class="sxs-lookup"><span data-stu-id="39a35-109">This procedure uses the fiscal year 2012.</span></span> <span data-ttu-id="39a35-110">คุณสามารถตั้งค่าวันที่เริ่มต้นเป็นวันที่ 1 มกราคม 2012 และวันที่สิ้นสุดเป็นวันที่ 31 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="39a35-110">You can set From date to January 1, 2012 and To date to December 31, 2012.</span></span>  
3. <span data-ttu-id="39a35-111">คลิกแท็บผลต่างของการผลิตระดับสูง</span><span class="sxs-lookup"><span data-stu-id="39a35-111">Click the High production variances tab.</span></span>
4. <span data-ttu-id="39a35-112">คลิกเพื่อติดตามลิงค์ในฟิลด์การผลิต</span><span class="sxs-lookup"><span data-stu-id="39a35-112">Click to follow the link in the Production field.</span></span>
    * <span data-ttu-id="39a35-113">คลิก P000116 เพื่อติดตามลิงค์ในฟิลด์การผลิต</span><span class="sxs-lookup"><span data-stu-id="39a35-113">Click P000116 to follow the link in the Production field.</span></span>  
5. <span data-ttu-id="39a35-114">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="39a35-114">On the Action Pane, click Manage costs.</span></span>
6. <span data-ttu-id="39a35-115">คลิกดูการเปรียบเทียบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="39a35-115">Click View cost comparison.</span></span>
7. <span data-ttu-id="39a35-116">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="39a35-116">Click Close.</span></span>

