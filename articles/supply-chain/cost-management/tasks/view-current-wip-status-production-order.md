---
title: ดูสถานะปัจจุบันของ WIP ในใบสั่งผลิต
description: 'กระบวนงานนี้แสดงวิธีการดูรายงานWIPบนใบสั่งผลิต '
author: AndersGirke
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, CostAdminWorkspace, CostLastInventoryCloseCard, CostLastBackflushCostingCard, CostStatementCacheCard, CostReleasedProductsMissingCostingDataFormPart, CostCalculationPeriodTopVariancesChartFormPart, ProdTable, CostStatement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21f86508da647d2527132cf96371ba996f453523
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260706"
---
# <a name="view-current-wip-status-on-a-production-order"></a><span data-ttu-id="3a693-103">ดูสถานะปัจจุบันของ WIP ในใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="3a693-103">View current WIP status on a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a693-104">กระบวนงานนี้แสดงวิธีการดูรายงานWIPบนใบสั่งผลิต </span><span class="sxs-lookup"><span data-stu-id="3a693-104">This procedure shows how to view WIP statement on a production order.</span></span> <span data-ttu-id="3a693-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="3a693-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3a693-106">กระบวนการนี้มีไว้สำหรับผู้ควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3a693-106">This procedure is intended for the cost controller.</span></span>

1. <span data-ttu-id="3a693-107">คลิกการบริหารต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3a693-107">Click Cost administration.</span></span>
2. <span data-ttu-id="3a693-108">คลิกใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="3a693-108">Click Production orders.</span></span>
3. <span data-ttu-id="3a693-109">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์การผลิต ด้วยค่า 'p000153'</span><span class="sxs-lookup"><span data-stu-id="3a693-109">Use the Quick Filter to filter on the Production field with a value of 'p000153'.</span></span>
4. <span data-ttu-id="3a693-110">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3a693-110">On the Action Pane, click Manage costs.</span></span>
5. <span data-ttu-id="3a693-111">คลิกรายงาน WIP สำหรับการผลิต</span><span class="sxs-lookup"><span data-stu-id="3a693-111">Click Production WIP statement.</span></span>
6. <span data-ttu-id="3a693-112">ในฟิลด์วันที่เริ่มต้น ตั้งค่าวันที่เป็น ' 2012-12-01'</span><span class="sxs-lookup"><span data-stu-id="3a693-112">In the From date field, set the date to '2012-12-01'.</span></span>
7. <span data-ttu-id="3a693-113">ในฟิลด์วันที่สิ้นสุด ตั้งค่าวันที่เป็น ' 2012-12-31'</span><span class="sxs-lookup"><span data-stu-id="3a693-113">In the To date field, set the date to '2012-12-31'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]