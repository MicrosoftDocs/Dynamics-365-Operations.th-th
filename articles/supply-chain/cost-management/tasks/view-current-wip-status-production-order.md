---
title: ดูสถานะปัจจุบันของ WIP ในใบสั่งผลิต
description: 'กระบวนงานนี้แสดงวิธีการดูรายงานWIPบนใบสั่งผลิต '
author: AndersGirke
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, CostAdminWorkspace, CostLastInventoryCloseCard, CostLastBackflushCostingCard, CostStatementCacheCard, CostReleasedProductsMissingCostingDataFormPart, CostCalculationPeriodTopVariancesChartFormPart, ProdTable, CostStatement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b35f8927082c70b53702c7ac7c866c05cfc1fde
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563077"
---
# <a name="view-current-wip-status-on-a-production-order"></a><span data-ttu-id="b4cb1-103">ดูสถานะปัจจุบันของ WIP ในใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="b4cb1-103">View current WIP status on a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4cb1-104">กระบวนงานนี้แสดงวิธีการดูรายงานWIPบนใบสั่งผลิต </span><span class="sxs-lookup"><span data-stu-id="b4cb1-104">This procedure shows how to view WIP statement on a production order.</span></span> <span data-ttu-id="b4cb1-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="b4cb1-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b4cb1-106">กระบวนการนี้มีไว้สำหรับผู้ควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="b4cb1-106">This procedure is intended for the cost controller.</span></span>

1. <span data-ttu-id="b4cb1-107">คลิกการบริหารต้นทุน</span><span class="sxs-lookup"><span data-stu-id="b4cb1-107">Click Cost administration.</span></span>
2. <span data-ttu-id="b4cb1-108">คลิกใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="b4cb1-108">Click Production orders.</span></span>
3. <span data-ttu-id="b4cb1-109">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์การผลิต ด้วยค่า 'p000153'</span><span class="sxs-lookup"><span data-stu-id="b4cb1-109">Use the Quick Filter to filter on the Production field with a value of 'p000153'.</span></span>
4. <span data-ttu-id="b4cb1-110">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="b4cb1-110">On the Action Pane, click Manage costs.</span></span>
5. <span data-ttu-id="b4cb1-111">คลิกรายงาน WIP สำหรับการผลิต</span><span class="sxs-lookup"><span data-stu-id="b4cb1-111">Click Production WIP statement.</span></span>
6. <span data-ttu-id="b4cb1-112">ในฟิลด์วันที่เริ่มต้น ตั้งค่าวันที่เป็น ' 2012-12-01'</span><span class="sxs-lookup"><span data-stu-id="b4cb1-112">In the From date field, set the date to '2012-12-01'.</span></span>
7. <span data-ttu-id="b4cb1-113">ในฟิลด์วันที่สิ้นสุด ตั้งค่าวันที่เป็น ' 2012-12-31'</span><span class="sxs-lookup"><span data-stu-id="b4cb1-113">In the To date field, set the date to '2012-12-31'.</span></span>

