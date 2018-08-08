---
title: "มิติองค์ประกอบต้นทุน"
description: "หนึ่งในหลักของการลงบัญชีต้นทุนคือมิติองค์ประกอบต้นทุนจะถูกใช้ในการจัดประเภทและติดตามขั้นตอนของต้นทุน"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: c703d1a9ae36d4342dc652d70dd82379187057c1
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="cost-element-dimensions"></a><span data-ttu-id="ebce8-103">มิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ebce8-103">Cost element dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebce8-104">หนึ่งในหลักของการลงบัญชีต้นทุนคือมิติองค์ประกอบต้นทุนจะถูกใช้ในการจัดประเภทและติดตามขั้นตอนของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ebce8-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="ebce8-105">องค์ประกอบต้นทุนสอดคล้องกับรายการต้นทุนที่เกี่ยวข้องในผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="ebce8-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="ebce8-106">โดยทั่วไป สามารถเป็นชนิดขององค์ประกอบใดๆ ในระดับต่ำสุดในธุรกิจที่สามารถส่งต้นทุนไปได้</span><span class="sxs-lookup"><span data-stu-id="ebce8-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="ebce8-107">องค์ประกอบต้นทุนที่เป็นแนวคิดมีตั้งแต่บัญชีแยกประเภทจนถึงทรัพยากรต้นทุนที่เกี่ยวข้องทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="ebce8-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="ebce8-108">ปัจจุบัน การลงบัญชีต้นทุนสนับสนุนบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="ebce8-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="ebce8-109">องค์ประกอบต้นทุนสองชนิด</span><span class="sxs-lookup"><span data-stu-id="ebce8-109">Two types of cost elements</span></span>
<span data-ttu-id="ebce8-110">องค์ประกอบต้นทุนมีสองชนิด: องค์ประกอบต้นทุนหลักและองค์ประกอบต้นทุนรอง</span><span class="sxs-lookup"><span data-stu-id="ebce8-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="ebce8-111">ตารางต่อไปนี้อธิบายความแตกต่างระหว่างสองชนิดดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="ebce8-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ebce8-112"><strong>องค์ประกอบต้นทุนหลัก</strong></span><span class="sxs-lookup"><span data-stu-id="ebce8-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="ebce8-113"><strong>องค์ประกอบต้นทุนรอง</strong></span><span class="sxs-lookup"><span data-stu-id="ebce8-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebce8-114">องค์ประกอบต้นทุนหลักแสดงถึงขั้นตอนของต้นทุนจากการลงบัญชีทางการเงินถึงการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ebce8-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="ebce8-115">โครงสร้างองค์ประกอบต้นทุนสอดคล้องกับโครงสร้างทางบัญชีกำไรขาดทุนในบัญชีแยกประเภททั่วไป ซึ่งองค์ประกอบต้นทุนอาจสอดคล้องกับบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="ebce8-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="ebce8-116">ไม่ใช่บัญชีหลักทั้งหมดที่จำเป็นต้องแสดงเป็นองค์ประกอบต้นทุนตามความต้องการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="ebce8-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="ebce8-117">ตัวอย่างขององค์ประกอบต้นทุนหลักรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="ebce8-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="ebce8-118">ต้นทุนขาย (COG)</span><span class="sxs-lookup"><span data-stu-id="ebce8-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="ebce8-119">ต้นทุนวัสดุทางอ้อม</span><span class="sxs-lookup"><span data-stu-id="ebce8-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="ebce8-120">ต้นทุนบุคลากร</span><span class="sxs-lookup"><span data-stu-id="ebce8-120">Personnel costs</span></span></li>
<li><span data-ttu-id="ebce8-121">ต้นทุนพลังงาน</span><span class="sxs-lookup"><span data-stu-id="ebce8-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="ebce8-122">องค์ประกอบต้นทุนรองแสดงถึงขั้นตอนของต้นทุนภายในเนื่องจากมีการสร้างและใช้ต้นทุนเหล่านี้ในการลงบัญชีต้นทุนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ebce8-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="ebce8-123">และนำเพื่อรักษาความปลอดภัยที่สามารถติดตามแหล่งที่มาของต้นทุนได้</span><span class="sxs-lookup"><span data-stu-id="ebce8-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="ebce8-124">องค์ประกอบต้นทุนเหล่านี้จะใช้ในการปันส่วนต้นทุนและการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="ebce8-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="ebce8-125">ตัวอย่างขององค์ประกอบต้นทุนรองรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="ebce8-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="ebce8-126">ต้นทุนการผลิต</span><span class="sxs-lookup"><span data-stu-id="ebce8-126">Production costs</span></span></li>
<li><span data-ttu-id="ebce8-127">ค่าโสหุ้ยการผลิต วัสดุ และการตลาด</span><span class="sxs-lookup"><span data-stu-id="ebce8-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="ebce8-128">มิติองค์ประกอบต้นทุนและสมาชิกมิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ebce8-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="ebce8-129">องค์ประกอบต้นทุนถูกอ้างอิงเป็น *มิติองค์ประกอบต้นทุน*</span><span class="sxs-lookup"><span data-stu-id="ebce8-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="ebce8-130">ค่ามิติแต่ละรายการจะถูกเรียกว่า *สมาชิกของมิติองค์ประกอบต้นทุน*</span><span class="sxs-lookup"><span data-stu-id="ebce8-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="ebce8-131">ตัวอย่างเช่น คุณสามารถมีโครงสร้างผังบัญชี (COA) ของสหรัฐอเมริกาที่เป็นพื้นฐานสำหรับการรายงานตามกฎหมายของคุณ</span><span class="sxs-lookup"><span data-stu-id="ebce8-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="ebce8-132">COA นี้จะใช้เป็นมิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ebce8-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="ebce8-133">บัญชีซึ่งเป็นองค์ประกอบต้นทุนหลักจะถูกแสดงเป็นสมาชิกมิติองค์ประกอบต้นทุนในการลงบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ebce8-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="ebce8-134">ภาพหน้าจอต่อไปนี้แสดงตัวอย่างของบัญชีหลักเป็นมิติองค์ประกอบต้นทุนที่มีบัญชีหลักจริงเป็นสมาชิกมิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ebce8-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="ebce8-135">[![มิติองค์ประกอบต้นทุน](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="ebce8-135">[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="ebce8-136">นำเข้าสมาชิกมิติองค์ประกอบต้นทุนผ่านตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ebce8-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="ebce8-137">เพื่อช่วยให้การตั้งค่าสมาชิกมิติองค์ประกอบต้นทุนในการลงบัญชีต้นทุนง่ายขึ้น คุณสามารถใช้ตัวเชื่อมต่อข้อมูลที่อาจสร้างขึ้นไว้ล่วงหน้าหรือสร้างแบบกำหนดเองของคุณในการดึงข้อมูลองค์ประกอบต้นทุนหลักจากระบบต้นทางอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="ebce8-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="ebce8-138">ข้อควรพิจารณาการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ebce8-138">Implementation considerations</span></span>
<span data-ttu-id="ebce8-139">เนื่องจากองค์ประกอบต้นทุนแสดงถึงระดับต่ำสุดของรายละเอียดต้นทุน คุณควรตรวจสอบให้แน่ใจว่ามีการรวมองค์ประกอบต้นทุนทั้งหมดที่จำเป็นในการสร้างการรายงานการจัดการเมื่อคุณใช้งานโครงสร้างองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ebce8-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="ebce8-140">การค้นหาจำนวนองค์ประกอบต้นทุนที่เหมาะสมสำหรับการควบคุมต้นทุนอาจทำได้ยาก</span><span class="sxs-lookup"><span data-stu-id="ebce8-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="ebce8-141">การมีองค์ประกอบต้นทุนนับพันรายการอาจทำให้การควบคุมแต่ละองค์ประกอบต้นทุนทำได้ยาก</span><span class="sxs-lookup"><span data-stu-id="ebce8-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="ebce8-142">อีกวิธีหนึ่งคือ คุณสามารถจัดกลุ่มองค์ประกอบต้นทุนและจัดการการควบคุมต้นทุนในระดับรวม</span><span class="sxs-lookup"><span data-stu-id="ebce8-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>




