---
title: "ดำเนินการกับการปันส่วน"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับการปันส่วน ตัวเลือกสำหรับการประมวลผลใน Microsoft Dynamics 365 for Finance and Operations และวิธีที่ใช้ในการวางแผนงบประมาณ การปันส่วนจะถูกใช้เพื่อกระจายปริมาณระหว่างชุดข้อมูลบัญชีแยกประเภทหลายรายการ โดยจะช่วยรับประกันได้ว่าค่าใช้จ่ายหรือรายได้จะถูกคิดในออบเจ็กต์ที่ถูกต้องในการลงบัญชี"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 26e7f607e070ac6c09a92d7809d65bac34d51f0b
ms.contentlocale: th-th
ms.lasthandoff: 03/26/2018

---

# <a name="process-allocations"></a><span data-ttu-id="5b336-105">ดำเนินการกับการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="5b336-105">Process allocations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5b336-106">บทความนี้แสดงข้อมูลเกี่ยวกับการปันส่วน ตัวเลือกสำหรับการประมวลผลใน Microsoft Dynamics 365 for Finance and Operations และวิธีที่ใช้ในการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b336-106">This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Finance and Operations, and how they can be used in budget planning.</span></span> <span data-ttu-id="5b336-107">การปันส่วนจะถูกใช้เพื่อกระจายปริมาณระหว่างชุดข้อมูลบัญชีแยกประเภทหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="5b336-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="5b336-108">โดยจะช่วยรับประกันได้ว่าค่าใช้จ่ายหรือรายได้จะถูกคิดในออบเจ็กต์ที่ถูกต้องในการลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="5b336-108">They help guarantee that expenses or revenue is charged to the correct object in accounting.</span></span>

<span data-ttu-id="5b336-109">Microsoft Dynamics 365 for Finance and Operations มอบความสามารถดังต่อไปนี้ เพื่อสนับสนุนกระบวนการนี้:</span><span class="sxs-lookup"><span data-stu-id="5b336-109">Microsoft Dynamics 365 for Finance and Operations provides the following capabilities to support this process:</span></span>

-   <span data-ttu-id="5b336-110">ปันส่วนยอดเงินธุรกรรมด้วยตนเอง โดยใช้การดำเนินการแบ่งในการกระจายการลงบัญชี หรือ โดยใช้เท็มเพลตเริ่มต้นของมิติทางการเงินกับเอกสาร</span><span class="sxs-lookup"><span data-stu-id="5b336-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="5b336-111">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การกระจายการลงบัญชี](../accounts-payable/accounting-distributions.md)</span><span class="sxs-lookup"><span data-stu-id="5b336-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="5b336-112">จำนวนธุรกรรมการปันส่วนอัตโนมัติขึ้นอยู่กับเงื่อนไขการปันส่วนที่กำหนดไว้ในบัญชีหลักแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="5b336-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="5b336-113">รายการบัญชีปันส่วนจะถูกสร้างขึ้นสำหรับแต่ละสมุดรายวันขึ้นอยู่กับเปอร์เซ็นต์และบัญชีแยกประเภทปลายทางเมื่อใดก็ตามที่รายการบัญชีเป็นไปตามเงื่อนไขซึ่งกำหนดไว้เป็นบัญชีแยกประเภทต้นทาง</span><span class="sxs-lookup"><span data-stu-id="5b336-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="5b336-114">ยอดดุลบัญชีแยกประเภทหรือยอดเงินคงที่ปันส่วนโดยอัตโนมัติขึ้นอยู่กับกฎการปันส่วนของบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="5b336-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="5b336-115">กฎการปันส่วนบัญชีแยกประเภทต่างๆจะดำเนิการตามพื้นฐานของช่วงระยะการใช้สมุดรายวันการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="5b336-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="5b336-116">การปันส่วนขั้นการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b336-116">Allocations in budget planning</span></span>

<span data-ttu-id="5b336-117">สามารถใช้กฎการปันส่วนบัญชีแยกประเภทสำหรับแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b336-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="5b336-118">เมื่อคุณใช้กฎการปันส่วนบัญชีแยกประเภทในแผนงบประมาณ, ของกฎการปันส่วนทำงานวิธีเดียวกันกับบัญชีแยกประเภท, เพียงแต่ข้อมูลต้นทางและข้อมูลปลายทางนั้นมาจากแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b336-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="5b336-119">คุณสามารถเลือกกฎการปันส่วนบัญชีแยกประเภทที่จะใช้สำหรับแผนงบประมาณด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="5b336-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="5b336-120">อีกทางหนึ่งคือ คุณสามารถใช้กำหนดการการปันส่วนที่รันในฐานะส่วนหนึ่งของกระบวนการลำดับงาน </span><span class="sxs-lookup"><span data-stu-id="5b336-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="5b336-121">คุณไม่สามารถใช้กฎการปันส่วนบัญชีแยกประเภทระหว่างบริษัทสำหรับการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b336-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>






