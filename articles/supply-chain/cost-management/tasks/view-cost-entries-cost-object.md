--- 
title: "ดูรายการข้อมูลต้นทุนสำหรับออบเจ็กต์ต้นทุน"
description: "กระบวนการนี้แสดงวิธีการดูรายการต้นทุนสำหรับราคาทุนของสิ่งของ "
author: AndersGirke
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, CostAdminWorkspace, CostLastInventoryCloseCard, CostLastBackflushCostingCard, CostStatementCacheCard, CostReleasedProductsMissingCostingDataFormPart, CostCalculationPeriodTopVariancesChartFormPart, EcoResProductDetailsExtended, InventCostOnhandItem, InventValueTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 9c67ac7dd06219b9521e4832b18204bcf8662a81
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="view-cost-entries-for-a-cost-object"></a><span data-ttu-id="e5f9b-103">ดูรายการข้อมูลต้นทุนสำหรับออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e5f9b-103">View cost entries for a cost object</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5f9b-104">กระบวนการนี้แสดงวิธีการดูรายการต้นทุนสำหรับราคาทุนของสิ่งของ </span><span class="sxs-lookup"><span data-stu-id="e5f9b-104">This procedure shows how to view cost entries for a cost object.</span></span> <span data-ttu-id="e5f9b-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="e5f9b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e5f9b-106">กระบวนการนี้มีไว้สำหรับผู้ควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e5f9b-106">This procedure is intended for the cost controller.</span></span>

1. <span data-ttu-id="e5f9b-107">คลิกการบริหารต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e5f9b-107">Click Cost administration.</span></span>
2. <span data-ttu-id="e5f9b-108">คลิกผลิตภัณฑ์ต่างๆที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="e5f9b-108">Click Released products.</span></span>
3. <span data-ttu-id="e5f9b-109">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="e5f9b-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e5f9b-110">ตัวอย่างเช่น ใช้ตัวกรองฟิลด์หมายเลขสินค้าด้วยค่า 'm0004'</span><span class="sxs-lookup"><span data-stu-id="e5f9b-110">For example, filter on the Item number field with a value of 'm0004'.</span></span>
4. <span data-ttu-id="e5f9b-111">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e5f9b-111">On the Action Pane, click Manage costs.</span></span>
5. <span data-ttu-id="e5f9b-112">คลิกวัตถุต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e5f9b-112">Click Cost objects.</span></span>
6. <span data-ttu-id="e5f9b-113">คลิกรายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e5f9b-113">Click Cost entries.</span></span>
7. <span data-ttu-id="e5f9b-114">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์หมายเลขด้วยค่า 'p000031'</span><span class="sxs-lookup"><span data-stu-id="e5f9b-114">Use the Quick Filter to filter on the Number field with a value of 'p000031'.</span></span>
    * <span data-ttu-id="e5f9b-115">ถ้าหากรายการต้นทุนไม่ปรากฏ ตั้งค่าวันเริ่มต้นวันที่ 31 มกราคม 2012 และวันที่สิ้นสุดเป็นวันที่ 31 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="e5f9b-115">If cost entries are blank, set From date to January 31, 2012 and To date to December 31, 2012.</span></span>  


