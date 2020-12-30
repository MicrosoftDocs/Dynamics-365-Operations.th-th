---
title: ดำเนินการกับการปันส่วน
description: บทความนี้ให้ข้อมูลเกี่ยวกับการปันส่วน ตัวเลือกสำหรับการประมวลผลใน Microsoft Dynamics 365 Finance และวิธีการใช้งานในการวางแผนงบประมาณ การปันส่วนจะถูกใช้เพื่อกระจายปริมาณระหว่างชุดข้อมูลบัญชีแยกประเภทหลายรายการ โดยจะช่วยให้แน่ใจได้ว่าค่าใช้จ่ายหรือรายได้ต่างๆจะถูกคิดในออบเจ็กต์ที่ถูกต้องในการลงบัญชี
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c8216ebdd1f26601743e6b35849be0813d06b4a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448418"
---
# <a name="process-allocations"></a><span data-ttu-id="502fc-105">ดำเนินการกับการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="502fc-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="502fc-106">บทความนี้ให้ข้อมูลเกี่ยวกับการปันส่วน ตัวเลือกสำหรับการประมวลผลและวิธีการใช้งานในการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="502fc-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="502fc-107">การปันส่วนจะถูกใช้เพื่อกระจายปริมาณระหว่างชุดข้อมูลบัญชีแยกประเภทหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="502fc-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="502fc-108">โดยจะช่วยให้แน่ใจได้ว่าค่าใช้จ่ายหรือรายได้ต่างๆจะถูกคิดในออบเจ็กต์ที่ถูกต้องในการลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="502fc-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="502fc-109">ความสามารถต่อไปนี้สนับสนุนกระบวนการนี้:</span><span class="sxs-lookup"><span data-stu-id="502fc-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="502fc-110">ปันส่วนยอดเงินธุรกรรมด้วยตนเอง โดยใช้การดำเนินการแบ่งในการกระจายการลงบัญชี หรือ โดยใช้เท็มเพลตเริ่มต้นของมิติทางการเงินกับเอกสาร</span><span class="sxs-lookup"><span data-stu-id="502fc-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="502fc-111">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การกระจายการลงบัญชี](../accounts-payable/accounting-distributions.md)</span><span class="sxs-lookup"><span data-stu-id="502fc-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="502fc-112">จำนวนธุรกรรมการปันส่วนอัตโนมัติขึ้นอยู่กับเงื่อนไขการปันส่วนที่กำหนดไว้ในบัญชีหลักแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="502fc-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="502fc-113">รายการบัญชีปันส่วนจะถูกสร้างขึ้นสำหรับแต่ละสมุดรายวันขึ้นอยู่กับเปอร์เซ็นต์และบัญชีแยกประเภทปลายทางเมื่อใดก็ตามที่รายการบัญชีเป็นไปตามเงื่อนไขซึ่งกำหนดไว้เป็นบัญชีแยกประเภทต้นทาง</span><span class="sxs-lookup"><span data-stu-id="502fc-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="502fc-114">สำหรับข้อมูลเพิ่มเติม โปรดดู [เงื่อนไขในการปันส่วนของบัญชีหลัก](../general-ledger/main-account-allocation-terms.md)</span><span class="sxs-lookup"><span data-stu-id="502fc-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="502fc-115">ยอดดุลบัญชีแยกประเภทหรือยอดเงินคงที่ปันส่วนโดยอัตโนมัติขึ้นอยู่กับกฎการปันส่วนของบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="502fc-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="502fc-116">กฎการปันส่วนบัญชีแยกประเภทต่างๆจะดำเนิการตามพื้นฐานของช่วงระยะการใช้สมุดรายวันการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="502fc-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="502fc-117">สำหรับข้อมูลเพิ่มเติม ดูที่ [กฎการปันส่วน](../general-ledger/ledger-allocation-rules.md)</span><span class="sxs-lookup"><span data-stu-id="502fc-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="502fc-118">การปันส่วนขั้นการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="502fc-118">Allocations in budget planning</span></span>

<span data-ttu-id="502fc-119">สามารถใช้กฎการปันส่วนบัญชีแยกประเภทสำหรับแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="502fc-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="502fc-120">เมื่อคุณใช้กฎการปันส่วนบัญชีแยกประเภทในแผนงบประมาณ, ของกฎการปันส่วนทำงานวิธีเดียวกันกับบัญชีแยกประเภท, เพียงแต่ข้อมูลต้นทางและข้อมูลปลายทางนั้นมาจากแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="502fc-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="502fc-121">คุณสามารถเลือกกฎการปันส่วนบัญชีแยกประเภทที่จะใช้สำหรับแผนงบประมาณด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="502fc-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="502fc-122">อีกทางหนึ่งคือ คุณสามารถใช้กำหนดการการปันส่วนที่รันในฐานะส่วนหนึ่งของกระบวนการลำดับงาน </span><span class="sxs-lookup"><span data-stu-id="502fc-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="502fc-123">คุณไม่สามารถใช้กฎการปันส่วนบัญชีแยกประเภทระหว่างบริษัทสำหรับการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="502fc-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>

