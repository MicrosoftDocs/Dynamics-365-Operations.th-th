---
title: "สัญญาโครงการ"
description: "บทความนี้อธิบายและแสดงตัวอย่างของสัญญาโครงการที่คุณสามารถสร้างสำหรับโครงการและแหล่งเงินทุนชนิดต่างๆ และวิธีการจัดการสัญญาและการออกใบแจ้งหนี้แก่ลูกค้าโครงการใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition"
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 0d7d3b64b0d6a662246074b12e3a3fe105dfae47
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2017

---

# <a name="project-contracts"></a><span data-ttu-id="fc9a8-103">สัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-103">Project contracts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fc9a8-104">บทความนี้อธิบายและแสดงตัวอย่างของสัญญาโครงการที่คุณสามารถสร้างสำหรับโครงการและแหล่งเงินทุนชนิดต่างๆ และวิธีการจัดการสัญญาและการออกใบแจ้งหนี้แก่ลูกค้าโครงการใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="fc9a8-104">This article describes and provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="fc9a8-105">ชนิดของโครงการที่คุณสร้างขึ้นสำหรับสัญญาโครงการ จะเป็นตัวกำหนดวิธีการที่ใช้ในการออกใบแจ้งหนี้แก่ลูกค้าโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="fc9a8-106">คุณสามารถแก้ไขสัญญาโครงการและโครงการที่เกี่ยวข้อง แต่คุณไม่สามารถเปลี่ยนชนิดของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="fc9a8-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="fc9a8-107">โดยการใช้สัญญาโครงการ คุณสามารถออกใบแจ้งหนี้หนึ่งโครงการขึ้นไปในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="fc9a8-108">สัญญาโครงการยังช่วยรับประกันความสอดคล้องกันของกระบวนการออกใบแจ้งหนี้ สำหรับทุกโครงการย่อยในโครงสร้างโครงการการค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="fc9a8-109">ทุกโครงการที่จะออกใบแจ้งหนี้ต้องเชื่อมโยงกับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="fc9a8-110">การตั้งค่าสำหรับสัญญาโครงการจะใช้กับโครงการและโครงการย่อยทั้งหมดที่เกี่ยวข้องกับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="fc9a8-111">สัญญาโครงการสามารถระบุอย่างน้อยหนึ่งแหล่งเงินทุน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="fc9a8-112">ดังนั้น คุณสามารถแบ่งการเรียกเก็บเงินระหว่างบรรดาผู้ให้ทุนหลายราย ตั้งค่าวงเงินทุนเพื่อที่จะไม่เรียกเก็บแหล่งเงินทุนเงินเกินกว่ายอดเงินที่ระบุ และตั้งค่าคอนฟิกกฎการจัดหาเงินทุนสำหรับรายจ่ายที่คิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="fc9a8-113">แหล่งเงินทุนสำหรับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-113">Funding for project contracts</span></span>
<span data-ttu-id="fc9a8-114">บางรายสัญญาโครงการระบุว่า หลายฝ่ายร่วมกันรับผิดชอบด้านเงินทุนต้นทุนโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="fc9a8-115">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="fc9a8-115">Here are some examples:</span></span>

-   <span data-ttu-id="fc9a8-116">ลูกค้ารายใหญ่ที่มีหลายส่วนร้องขอให้จัดหาเงินทุนของโครงการโดยแบ่งตามส่วน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="fc9a8-117">บริษัทของคุณใช้ต้นทุนของโครงการขนาดใหญ่ร่วมกับกับองค์กรภายนอก</span><span class="sxs-lookup"><span data-stu-id="fc9a8-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="fc9a8-118">โครงการถนนได้รับเงินทุนร่วมจากสองอำเภอ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="fc9a8-119">โครงการสะพานได้รับเงินทุนโครงการโดยรัฐบาลเงินมอบช่วยเหลือและจากบริษัทเอกชน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="fc9a8-120">ใน Finance and Operations คุณสามารถแบ่งการเรียกเก็บเงินสำหรับธุรกรรมเดียวหรือทั้งโครงการระหว่างลูกค้าหลายราย เงินช่วยเหลือ หรือองค์กร</span><span class="sxs-lookup"><span data-stu-id="fc9a8-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="fc9a8-121">ในโครงการที่มีผู้ให้ทุนหลายราย ทุกฝ่ายที่เกี่ยวข้องกับการจัดหาเงินทุนของโครงการจัดหาเงินทุนขั้นสูง จะเรียกว่าแหล่งเงินทุน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="fc9a8-122">หลังจากลูกค้า องค์กร หรือเงินช่วยเหลือถูกกำหนดเป็นแหล่งเงินทุน จึงจะสามารถกำหนดไปยังอย่างน้อยหนึ่งกฎการจัดหาเงินทุน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="fc9a8-123">กฎการจัดหาเงินทุนประกอบด้วยเกณฑ์ที่กำหนดวิธีการปันส่วนค่าธรรมเนียมกับแหล่งเงินทุนหลายแหล่งสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="fc9a8-124">เนื่องจากสินค้าที่เก็บในคลังสินค้า เช่นที่ปรากฏบนใบขอซื้อและใบสั่งซื้อ ไม่สามารถแบ่งได้ ยอดต้นทุนไม่สามารถแบ่งระหว่างแหล่งเงินทุนหลายแหล่งเมื่อมีการกระจายสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc9a8-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="fc9a8-125">ดังนั้น ค่าแหล่งเงินทุนยังคงเป็น 0 (ศูนย์) จนกว่าจะมีการลงรายการบัญชีการตัดสินค้าจากคลัง</span><span class="sxs-lookup"><span data-stu-id="fc9a8-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="fc9a8-126">เมื่อลงรายการบัญชีการตัดสินค้าจากคลังของสินค้าคงคลังแล้ว ยอดต้นทุนจะถูกกระจายตามกฎการกระจายบัญชีสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="fc9a8-127">นี่คือบางขั้นตอนที่คุณสามารถกระทำได้เพื่อให้การแบ่งการเรียกเก็บเงินระหว่างแหล่งเงินทุนหลายแหล่งทำได้ง่ายขึ้น:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="fc9a8-128">ระบุว่า ธุรกรรมทั้งหมดที่ป้อนสำหรับโครงการ ใช้สกุลเงินการขายเดียวกับในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="fc9a8-129">ตั้งค่าวงเงินทุนเพื่อให้แหล่งเงินทุนไม่ได้ถูกออกใบแจ้งหนี้เกินกว่ายอดเงินที่ระบุในโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="fc9a8-130">การตั้งค่าคอนฟิกกฎการจัดหาเงินทุนและวงเงินทุนสำหรับแต่ละผู้ปฏิบัติงาน สินค้า ประเภท กลุ่มประเภท และชนิดของธุรกรรม (หรือสำหรับชนิดของธุรกรรมทั้งหมด)</span><span class="sxs-lookup"><span data-stu-id="fc9a8-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="fc9a8-131">เลือกระบุวันเริ่มต้นและสิ้นสุดที่ไม่จำเป็นต้องระบุ เพื่อกำหนดรอบระยะเวลาที่แต่ละกฎการจัดหาเงินทุนมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="fc9a8-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="fc9a8-132">ระบุเปอร์เซ็นต์ที่แต่ละแหล่งเงินทุนรับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="fc9a8-133">ระบุแหล่งเงินทุนที่รับผิดชอบสำหรับการปัดเศษผลต่างที่เกิดจากการคำนวณการปันส่วนการจัดหาเงินทุน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="fc9a8-134">ตั้งค่ากฎที่กำหนดวิธีการที่ต้นทุนโครงการจะออกใบแจ้งหนี้ให้แก่ลูกค้าภายนอก และคิดค่าธรรมเนียมกับองค์กรภายใน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="fc9a8-135">บันทึกธุรกกรมในบัญชีแหล่งเงินทุนที่ระงับ จนกว่าจะสามารถรับเงินทุนเพิ่มเติม หรือจนกว่าคุณจะตัดสินใจที่จะรับผิดชอบต้นทุนเป็นการภายใน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="fc9a8-136">ในการกำหนดกลุ่มภาษีที่จะเชื่อมโยงกับธุรกรรม โครงการจะถูกค้นหาสำหรับการกำหนดกลุ่มภาษี</span><span class="sxs-lookup"><span data-stu-id="fc9a8-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="fc9a8-137">ถ้าไม่มีการกำหนดกลุ่มภาษีการไว้ในระดับโครงการ จะค้นหาในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="fc9a8-138">ตัวอย่าง: หลายแหล่งเงินทุน (ปกติ)</span><span class="sxs-lookup"><span data-stu-id="fc9a8-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="fc9a8-139">ตารางต่อไปนี้แสดงสถานการณ์จำลองสำหรับการจัดการการปันส่วนการจัดหาเงินทุนระหว่างแหล่งเงินทุนหลายแหล่ง</span><span class="sxs-lookup"><span data-stu-id="fc9a8-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="fc9a8-140">สถานการณ์เหล่านี้ ขึ้นอยู่กับสมมติฐานดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="fc9a8-141">การตั้งค่าระดับความสำคัญเป็นปัจจัยในการปันส่วนจำนวนเงินก่อนที่จะใช้เงื่อนไขกฎการจัดหาเงินทุนอื่น</span><span class="sxs-lookup"><span data-stu-id="fc9a8-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="fc9a8-142">จะไม่มีการระบุช่วงวันที่เพื่อกำหนดรอบระยะเวลา เมื่อกฎการจัดหาเงินทุนมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="fc9a8-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc9a8-143"><strong>สถานการณ์จำลอง</strong></span><span class="sxs-lookup"><span data-stu-id="fc9a8-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="fc9a8-144"><strong>แหล่งเงินทุน </strong></span><span class="sxs-lookup"><span data-stu-id="fc9a8-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="fc9a8-145"><strong>เปอร์เซ็นต์การปันส่วน </strong></span><span class="sxs-lookup"><span data-stu-id="fc9a8-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="fc9a8-146"><strong>ระดับความสำคัญของการปันส่วนการจัดหาเงินทุน </strong></span><span class="sxs-lookup"><span data-stu-id="fc9a8-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc9a8-147">คุณต้องการปันส่วนต้นทุนกับแหล่งเงินทุนหนึ่งจนกว่าเงินทุนจะหมดลง ปันส่วนต้นทุนไปยังแหล่งเงินทุนที่สองจนกว่าเงินทุนจะหมดลง และสุดท้าย ปันส่วนต้นทุนคงเหลือไปยังแหล่งเงินทุนที่สาม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="fc9a8-148">แหล่งเงินทุน 1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="fc9a8-149">แหล่งเงินทุน 2</span><span class="sxs-lookup"><span data-stu-id="fc9a8-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="fc9a8-150">แหล่งเงินทุน 3</span><span class="sxs-lookup"><span data-stu-id="fc9a8-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fc9a8-151">100%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-151">100%</span></span></li>
<li><span data-ttu-id="fc9a8-152">100%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-152">100%</span></span></li>
<li><span data-ttu-id="fc9a8-153">100%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fc9a8-154">1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-154">1</span></span></li>
<li><span data-ttu-id="fc9a8-155">2</span><span class="sxs-lookup"><span data-stu-id="fc9a8-155">2</span></span></li>
<li><span data-ttu-id="fc9a8-156">3</span><span class="sxs-lookup"><span data-stu-id="fc9a8-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc9a8-157">คุณต้องการปันส่วน 75 เปอร์เซ็นต์ของต้นทุนไปยังแหล่งเงินทุนหนึ่ง และ 25 เปอร์เซ็นต์ไปยังแหล่งเงินทุนที่สอง</span><span class="sxs-lookup"><span data-stu-id="fc9a8-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="fc9a8-158">เมื่อแหล่งเงินทุนเหล่านี้ทั้งหมดแล้ว คุณต้องการชำระต้นทุนที่เหลือจากแหล่งเงินทุนที่สาม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="fc9a8-159">แหล่งเงินทุน 1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="fc9a8-160">แหล่งเงินทุน 2</span><span class="sxs-lookup"><span data-stu-id="fc9a8-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="fc9a8-161">แหล่งเงินทุน 3</span><span class="sxs-lookup"><span data-stu-id="fc9a8-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fc9a8-162">75%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-162">75%</span></span></li>
<li><span data-ttu-id="fc9a8-163">25%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-163">25%</span></span></li>
<li><span data-ttu-id="fc9a8-164">100%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fc9a8-165">1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-165">1</span></span></li>
<li><span data-ttu-id="fc9a8-166">1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-166">1</span></span></li>
<li><span data-ttu-id="fc9a8-167">2</span><span class="sxs-lookup"><span data-stu-id="fc9a8-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc9a8-168">คุณต้องการปันส่วน 75 เปอร์เซ็นต์ของต้นทุนไปยังแหล่งเงินทุนหนึ่ง และ 25 เปอร์เซ็นต์ไปยังแหล่งเงินทุนที่สอง</span><span class="sxs-lookup"><span data-stu-id="fc9a8-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="fc9a8-169">เมื่อแหล่งเงินทุนเหล่านี้ทั้งหมดแล้ว คุณต้องการแบ่งชำระต้นทุนที่เหลือระหว่างจากแหล่งเงินทุนที่สามอละแหล่งเงินทุนที่สี่</span><span class="sxs-lookup"><span data-stu-id="fc9a8-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="fc9a8-170">แหล่งเงินทุน 1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="fc9a8-171">แหล่งเงินทุน 2</span><span class="sxs-lookup"><span data-stu-id="fc9a8-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="fc9a8-172">แหล่งเงินทุน 3</span><span class="sxs-lookup"><span data-stu-id="fc9a8-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="fc9a8-173">แหล่งเงินทุน 4</span><span class="sxs-lookup"><span data-stu-id="fc9a8-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fc9a8-174">75%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-174">75%</span></span></li>
<li><span data-ttu-id="fc9a8-175">25%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-175">25%</span></span></li>
<li><span data-ttu-id="fc9a8-176">50%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-176">50%</span></span></li>
<li><span data-ttu-id="fc9a8-177">50%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fc9a8-178">1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-178">1</span></span></li>
<li><span data-ttu-id="fc9a8-179">1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-179">1</span></span></li>
<li><span data-ttu-id="fc9a8-180">2</span><span class="sxs-lookup"><span data-stu-id="fc9a8-180">2</span></span></li>
<li><span data-ttu-id="fc9a8-181">2</span><span class="sxs-lookup"><span data-stu-id="fc9a8-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc9a8-182">คุณต้องการปันส่วน 25 เปอร์เซ็นต์แรกของต้นทุนไปยังแหล่งเงินทุนหนึ่ง และที่เหลือไปยังแหล่งเงินทุนที่สอง</span><span class="sxs-lookup"><span data-stu-id="fc9a8-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="fc9a8-183">แหล่งเงินทุน 1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="fc9a8-184">แหล่งเงินทุน 2</span><span class="sxs-lookup"><span data-stu-id="fc9a8-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fc9a8-185">25%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-185">25%</span></span></li>
<li><span data-ttu-id="fc9a8-186">100%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fc9a8-187">1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-187">1</span></span></li>
<li><span data-ttu-id="fc9a8-188">2</span><span class="sxs-lookup"><span data-stu-id="fc9a8-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="fc9a8-189">ตัวอย่าง: หลายแหล่งเงินทุน (ซับซ้อน)</span><span class="sxs-lookup"><span data-stu-id="fc9a8-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="fc9a8-190">คุณมีสามแหล่งเงินทุนที่คุณต้องการใช้ตามลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="fc9a8-191">ใช้แหล่งเงินทุน 2 และแหล่งเงินทุน 3 เท่า ๆ กันจนกระทั่งแหล่งเงินทุน 2 หมดลง</span><span class="sxs-lookup"><span data-stu-id="fc9a8-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="fc9a8-192">ใช้แหล่งเงินทุน 3 ต่อจนกว่าจะหมด</span><span class="sxs-lookup"><span data-stu-id="fc9a8-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="fc9a8-193">ใช้แหล่งเงินทุน 1 หลังจากแหล่งเงินทุน 3 หมดลง</span><span class="sxs-lookup"><span data-stu-id="fc9a8-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="fc9a8-194">เพื่อให้บรรลุเป้าหมายนี้ คุณต้องดำเนินการดังนี้:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="fc9a8-195">ตั้งค่าขีดจำกัดสำหรับแหล่งเงินทุน 2 และแหล่งเงินทุน 3 ตามลำดับยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="fc9a8-196">สร้างกฎการจัดหาเงินทุนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="fc9a8-197">กฎที่ 1 (ระดับความสำคัญ 1): ปันส่วน 50 เปอร์เซ็นต์ของธุรกรรมไปยังแหล่งเงินทุน 2 และ 50 เปอร์เซ็นต์ไปยังแหล่งเงินทุน 3</span><span class="sxs-lookup"><span data-stu-id="fc9a8-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="fc9a8-198">กฎที่ 2 (ระดับความสำคัญ 2): ปันส่วน 100 เปอร์เซ็นต์ของธุรกรรมไปยังแหล่งเงินทุน 3</span><span class="sxs-lookup"><span data-stu-id="fc9a8-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="fc9a8-199">กฎที่ 3 (ระดับความสำคัญ 3): ปันส่วน 100 เปอร์เซ็นต์ของธุรกรรมไปยังแหล่งเงินทุน 1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="fc9a8-200">การตั้งค่านี้สามารถทำได้เนื่องจากมีการตรวจสอบธุรกรรมเทียบกับกฎและข้อจำกัดในการกำหนดว่า สามารถใช้กับธุรกรรมได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="fc9a8-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="fc9a8-201">ถ้าไม่มีกฎเฉพาะหรือขีดจำกัดเพื่อใช้กับธุรกรรม กฎรวมของธุรกรรมทั้งหมดจะถูกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="fc9a8-202">กฎธุรกรรมทั้งหมดจะต้องตรงกับธุรกรรมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fc9a8-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="fc9a8-203">ถ้าพบว่ากฎตรงกับธุรกรรม จะใช้เปอร์เซ็นต์ที่มีการปันส่วนในกฎเป็นอันดับแรก แต่หลังจากที่การตรงกันนี้ถูกตรวจสอบโดยเทียบกับขีดจำกัดที่ตั้งค่าไว้แล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fc9a8-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="fc9a8-204">ถ้าตรงตามขีดจำกัด และเงินของแหล่งเงินทุนได้หมดลงแล้ว จะละเว้นกฎการจัดหาเงินทุนที่เกี่ยวข้องกับวงเงินทุน และโปรแกรมตรวจสอบกฎถัดไปที่สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="fc9a8-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="fc9a8-205">ในบางกรณี เฉพาะบางส่วนของธุรกรรมสามารถปันส่วนภายใต้กฎ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="fc9a8-206">สิ่งนี้อาจเกิดขึ้นได้เนื่องจากถึงขีดจำกัดเมื่อมีการปันส่วนธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="fc9a8-207">ในกรณีนี้ มีเพียงยอดเงินจำนวนหนึ่งที่จะปันส่วนตามกฎนั้น เช่น 50 เปอร์เซ็นต์ต่อแต่ละแหล่งเงินทุน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="fc9a8-208">นี่คือกรณีในกฎ 1 ซึ่งได้อธิบายไว้ก่อนหน้าในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="fc9a8-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="fc9a8-209">ยอดคงเหลือจะปันส่วนตามกฎการถัดไปตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="fc9a8-210">ตารางต่อไปนี้จะตรวจสอบสถานการณ์นี้โดยละเอียดขึ้น</span><span class="sxs-lookup"><span data-stu-id="fc9a8-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc9a8-211"><strong>โฟกัส </strong></span><span class="sxs-lookup"><span data-stu-id="fc9a8-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="fc9a8-212"><strong>รายละเอียด</strong></span><span class="sxs-lookup"><span data-stu-id="fc9a8-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc9a8-213">กฎการจัดหาเงินทุน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="fc9a8-214">กฎข้อ 1 (ระดับความสำคัญ 1): ธุรกรรมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fc9a8-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="fc9a8-215">การปันส่วนแหล่งเงินทุน 2 ที่ 50% และแหล่งเงินทุน 3 ที่ 50%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="fc9a8-216">กฎข้อ 2 (ระดับความสำคัญ 2): ธุรกรรมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fc9a8-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="fc9a8-217">ปันส่วนแหล่งเงินทุน 3 ที่ 100%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="fc9a8-218">กฎข้อ 3 (ระดับความสำคัญ 2): ธุรกรรมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fc9a8-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="fc9a8-219">ปันส่วนแหล่งเงินทุน 1 ที่ 100%</span><span class="sxs-lookup"><span data-stu-id="fc9a8-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc9a8-220">วงเงินทุน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="fc9a8-221">ขีดจำกัดแหล่งเงินทุน 1 = 10,000.00</span><span class="sxs-lookup"><span data-stu-id="fc9a8-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="fc9a8-222">ขีดจำกัดแหล่งเงินทุน 2 = 500.00</span><span class="sxs-lookup"><span data-stu-id="fc9a8-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="fc9a8-223">ขีดจำกัดแหล่งเงินทุน 3 = 750.00</span><span class="sxs-lookup"><span data-stu-id="fc9a8-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc9a8-224">ธุรกรรม 1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-224">Transaction 1</span></span></td>
<td><span data-ttu-id="fc9a8-225"><strong>ยอดเงินธุรกรรม:</strong> 100.00<strong>เงินทุน:</strong> ธุรกรรมจะถูกชำระตามกฎข้อ 1 เท่านั้น เนื่องจากธุรกรรมที่จะถูกชำระทั้งหมดหลังจากมีการบังคับใช้กฎข้อ 1</span><span class="sxs-lookup"><span data-stu-id="fc9a8-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="fc9a8-226">ธุรกรรมจะได้รับเงินทุนเท่า ๆ กันระหว่างแหล่งเงินทุน 2 และแหล่งเงินทุน 3</span><span class="sxs-lookup"><span data-stu-id="fc9a8-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="fc9a8-227">ที่มาของแหล่งเงินทุน 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="fc9a8-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="fc9a8-228">ที่มาของแหล่งเงินทุน 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="fc9a8-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc9a8-229">ธุรกรรม 2</span><span class="sxs-lookup"><span data-stu-id="fc9a8-229">Transaction 2</span></span></td>
<td><span data-ttu-id="fc9a8-230"><strong>ยอดเงินธุรกรรม:</strong> 5,000.00<strong>เงินทุน:</strong> ธุรกรรมจะถูกชำระตามกฎทั้งหมดสามข้อ<strong>Rule 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="fc9a8-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.<strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="fc9a8-231">แหล่งเงินทุน 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="fc9a8-231">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="fc9a8-232">ที่มาของแหล่งเงินทุน 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="fc9a8-232">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="fc9a8-233">
<strong>กฎ 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="fc9a8-233">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="fc9a8-234">ที่มาของแหล่งเงินทุน 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="fc9a8-234">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="fc9a8-235">
<strong>กฎ 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="fc9a8-235">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="fc9a8-236">ที่มาของแหล่งเงินทุน 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="fc9a8-236">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc9a8-237">เงินทุนรวมที่จะแจกจ่ายไปยังแต่ละแหล่งเงินทุน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-237">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="fc9a8-238">ที่มาของแหล่งเงินทุน 1: 3,850.00</span><span class="sxs-lookup"><span data-stu-id="fc9a8-238">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="fc9a8-239">ที่มาของแหล่งเงินทุน 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="fc9a8-239">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="fc9a8-240">ที่มาของแหล่งเงินทุน 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="fc9a8-240">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="fc9a8-241">กฎการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-241">Billing rules</span></span>
<span data-ttu-id="fc9a8-242">เมื่อคุณเจรจาสัญญาโครงการกับลูกค้า คุณสามารถกำหนดว่าจะออกอินวอยซ์ลูกค้าสำหรับงานในโครงการอย่างไรและเมื่อไร</span><span class="sxs-lookup"><span data-stu-id="fc9a8-242">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="fc9a8-243">หลังจากที่คุณตั้งค่าสัญญาโครงการและโครงการ คุณสามารถตั้งค่ากฏการเรียกเก็บเงินสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-243">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="fc9a8-244">กฎการเรียกเก็บเงินจะขึ้นอยู่กับเงื่อนไขของโครงการที่ระบุไว้ในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-244">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="fc9a8-245">กฎการเรียกเก็บเงินที่คุณสามารถสร้างได้ขึ้นอยู่กับเงื่อนในสัญญาโครงการและชนิดของโครงการ เช่น เวลาและวัสดุ หรือราคาคงที่ ตามที่คุณเชื่อมโยงกับกฎการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-245">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="fc9a8-246">คุณสามารถสร้างกฎการเรียกเก็บเงินมากกว่าหนึ่งกฎสำหรับหนึ่งสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-246">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="fc9a8-247">นอกจากนี้ คุณยังสามารถกำหนดกฎการเรียกเก็บเงินกับโครงการหลายโครงการที่สัมพันธ์กับสัญญาโครงการเดียวกัน และมีเงื่อนไขการเรียกเก็บเงินที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-247">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="fc9a8-248">คุณสามารถตั้งค่าชนิดของกฎการเรียกเก็บเงินต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-248">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="fc9a8-249">**หน่วยของการจัดส่ง** – ออกใบแจ้งหนี้แก่ลูกค้าเมื่อหน่วยการจัดส่งเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="fc9a8-249">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="fc9a8-250">คุณสามารถกำหนดหน่วยของการจัดส่งไว้ในสัญญา</span><span class="sxs-lookup"><span data-stu-id="fc9a8-250">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="fc9a8-251">**ความคืบหน้า**– ออกใบแจ้งหนี้แก่ลูกค้าเมื่อหน่วยการจัดส่งเสร็จสมบูรณ์เป็นเปอร์เซ็นต์ตามที่ระบุไว้ในโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-251">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="fc9a8-252">คุณสามารถตั้งค่ากฎการเรียกเก็บเงินเพื่อคำนวณเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์โดยอัตโนมัติ หรือคุณสามารถคำนวณเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์แล้วด้วยตนเอง และออกใบแจ้งหนี้ตามยอดเงินนั้นแก่ลูกค้าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="fc9a8-252">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="fc9a8-253">**เหตุการณ์สำคัญ** – สร้างใบแจ้งหนี้สำหรับยอดเงินทั้งหมดของเหตุการณ์สำคัญของโครงการ เมื่อถึงเหตุการณ์สำคัญนั้น</span><span class="sxs-lookup"><span data-stu-id="fc9a8-253">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="fc9a8-254">**ค่าธรรเนียม** – ออกใบแจ้งหนี้แก่ลูกค้าสำหรับบริการของคุณรวมทั้งค่าธรรมเนียมการจัดการ โดยทั่วไปจะเป็นเปอร์เซ็นต์ของต้นทุนการบริการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-254">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="fc9a8-255">**เวลาและวัสดุ** – ออกใบแจ้งหนี้แก่ลูกค้าสำหรับมูลค่าของเวลาและวัสดุที่ใช้ในโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-255">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="fc9a8-256">สำหรับกฎการเรียกเก็บเงินทุกชนิด คุณสามารถระบุเปอร์เซ็นต์เงินประกันผลงานที่จะหักออกจากใบแจ้งหนี้ของลูกค้าจนกว่าโครงการจะถึงขั้นตอนที่ตกลงกันไว้</span><span class="sxs-lookup"><span data-stu-id="fc9a8-256">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="fc9a8-257">การชำระเงินเงินประกันผลงานเป็นเปอร์เซ็นต์จะระบุเอาไว้ในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-257">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="fc9a8-258">ยอดเงินจะถูกคำนวณตาม และหักลบออกจากมูลค่ารวมของรายการในใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="fc9a8-258">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="fc9a8-259">สำหรับกฎการเรียกเก็บเงิน **เวลาและวัสดุ** และ **ความคืบหน้า** คุณสามารถกำหนดประเภทที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fc9a8-259">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="fc9a8-260">ประเภทที่คิดค่าธรรมเนียมได้บ่งชี้ไปยังธุรกรรมที่ควรจะรวมอยู่ในใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="fc9a8-260">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="fc9a8-261">เมื่อคุณพร้อมที่จะออกใบแจ้งหนี้ลูกค้า ยอดเงินที่จะออกใบแจ้งหนี้สำหรับโครงการจะคำนวณตามกฎการเรียกเก็บเงิน และสร้างข้อเสนอใบแจ้งหนี้โครงการขึ้น</span><span class="sxs-lookup"><span data-stu-id="fc9a8-261">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="fc9a8-262">ส่วนต่อไปนี้แสดงตัวอย่างซึ่งแสดงวิธีตั้งค่าและจัดการกฎการเรียกเก็บเงินสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-262">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="fc9a8-263">ตัวอย่าง: สร้างกฎการเรียกเก็บเงินตามจำนวนของหน่วยที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fc9a8-263">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="fc9a8-264">องค์กรของคุณเข้าสู่ข้อตกลงเพื่อระบุผลรวมของรอบเวลาการฝึกอบรมจำนวนห้ารอบแก่พนักงานของลูกค้า ที่ต้นทุน 10000 สำหรับแต่ละรอบเวลาการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-264">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="fc9a8-265">คุณออกใบแจ้งหนี้แก่ลูกค้าตามหลังแต่ละเซสชันการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-265">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="fc9a8-266">เมื่อคุณตั้งค่ากฎการเรียกเก็บเงินสำหรับสัญญา คุณจะใช้ค่าดังอไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-266">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="fc9a8-267">หน่วยของการจัดส่งคือหนึ่งรอบเวลาการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-267">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="fc9a8-268">ราคาต่อหน่วยคือ 10,000 ต่อหนึ่งรอบเวลาการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-268">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="fc9a8-269">จำนวนรวมของหน่วยเป็นห้ารอบเวลาการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-269">The total number of units is five training sessions.</span></span>

<span data-ttu-id="fc9a8-270">เมื่อเสร็จสิ้นรอบเวลาการฝึกอบรมหนึ่ง คุณสามารถสร้างใบแจ้งหนี้ 10,000 สำหรับหน่วยแรกที่จัดส่งแล้ว และส่งใบแจ้งหนี้ไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="fc9a8-270">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="fc9a8-271">ตัวอย่าง: สร้างกฎการเรียกเก็บเงินที่อิงตามเปอร์เซ็นต์ที่ระบุของการเสร็จสมบูรณ์โครงการ (คำนวณด้วยตนเอง)</span><span class="sxs-lookup"><span data-stu-id="fc9a8-271">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="fc9a8-272">องค์กรของคุณเป็นบริษัทที่ปรึกษาด้านซอฟต์แวร์ เข้าสู่ข้อตกลงกับลูกค้าเพื่อพัฒนาส่วนของผลิตภัณฑ์ที่ลูกค้ากำลังพัฒนาอยู่</span><span class="sxs-lookup"><span data-stu-id="fc9a8-272">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="fc9a8-273">องค์กรของคุณตกลงที่จะจัดส่งรหัสซอฟต์แวร์รอบระยะเวลาหกเดือน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-273">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="fc9a8-274">ลูกค้าตกลงที่จะชำระเงินให้แก่องค์กรของคุณเป็นจำนวนทั้งหมด 100000 สำหรับการทำงาน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-274">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="fc9a8-275">คุณสร้างกฎการเรียกเก็บเงินเพื่ออกใบแจ้งหนี้แก่ลูกค้าตามเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์ในโครงการ ตามที่ระบุในสัญญา</span><span class="sxs-lookup"><span data-stu-id="fc9a8-275">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="fc9a8-276">สิ้นเดือนแรก คุณพบกับลูกค้าเพื่อกำหนดเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="fc9a8-276">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="fc9a8-277">หลังจากคุณและลูกค้าตรวจทานโครงการ คุณตัดสินใจว่า โครงการเสร็จสมบูรณ์ไป 15 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="fc9a8-277">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="fc9a8-278">คุณสร้างใบแจ้งหนี้จำนวน 15000 (15 เปอร์เซ็นต์ของ 100000) และส่งไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="fc9a8-278">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="fc9a8-279">ตัวอย่าง: สร้างกฎการเรียกเก็บเงินที่อิงตามเปอร์เซ็นต์ที่ระบุของการเสร็จสมบูรณ์โครงการ (คำนวณโดยอัตโนมัติ)</span><span class="sxs-lookup"><span data-stu-id="fc9a8-279">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="fc9a8-280">องค์กรของคุณคือบริษัทพัฒนาซอฟต์แวร์ ตกลงที่จะพัฒนาแพคเกจการลงบัญชีค่าจ้างให้ลูกค้าเป็นมูลค่า 30000</span><span class="sxs-lookup"><span data-stu-id="fc9a8-280">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="fc9a8-281">ลูกค้าตกลงที่จะชำระเงินให้แก่องค์กรของคุณตามเปอร์เซ็นต์งานที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fc9a8-281">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="fc9a8-282">คุณคาดคะเนว่า ต้นทุนของโครงการเป็น 20000</span><span class="sxs-lookup"><span data-stu-id="fc9a8-282">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="fc9a8-283">สัญญาโครงการระบุประเภทของงานที่คุณใช้ในกระบวนการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-283">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="fc9a8-284">คุณตั้งค่ากฎการเรียกเก็บเงินว่าจะคำนวณยอดเงินใบแจ้งหนี้ตามเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์สำหรับแต่ละประเภท การเรียกเก็บเงินโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-284">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="fc9a8-285">คุณตั้งค่างบประมาณสำหรับแต่ละประเภท:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-285">You set up a budget for each category:</span></span>

-   <span data-ttu-id="fc9a8-286">**การพัฒนา** – ต้นทุน 15,000 และรายได้ 20,000</span><span class="sxs-lookup"><span data-stu-id="fc9a8-286">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="fc9a8-287">**การติดตั้ง** – ต้นทุน 5,000 และรายได้ 10,000</span><span class="sxs-lookup"><span data-stu-id="fc9a8-287">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="fc9a8-288">เมื่อคุณสร้างใบแจ้งหนี้ของลูกค้าเป็นครั้งแรก ยอดเงินใบแจ้งหนี้จะคำนวณโดยอัตโนมัติตามข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-288">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="fc9a8-289">หนึ่งเดือนผ่านไป ผู้ปฏิบัติงานในโครงการส่งแผ่นเวลาสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-289">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="fc9a8-290">ต้นทุนของชั่วโมงที่ผู้ปฏิบัติงานคือ 5000 สำหรับการพัฒนา และ 1000 สำหรับการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="fc9a8-290">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="fc9a8-291">งานพัฒนาเสร็จนสมบูรณ์แล้ว 33 เปอร์เซ็นต์ (ต้นทุนจริง 5,000/ต้นทุนงบประมาณ 15,000) และงานการติดตั้งเสร็จนสมบูรณ์แล้ว 20 เปอร์เซ็นต์ (ต้นทุนจริง 1,000/ต้นทุนงบประมาณ 5,000)</span><span class="sxs-lookup"><span data-stu-id="fc9a8-291">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="fc9a8-292">ยอดเงินใบแจ้งหนี้ 8,667 จะถูกคำนวณโดยอัตมัติ (33 เปอร์เซ็นต์ของ 20,000 บวก 20 เปอร์เซ็นต์ของ 10,000)</span><span class="sxs-lookup"><span data-stu-id="fc9a8-292">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="fc9a8-293">คุณสร้างใบแจ้งหนี้จำนวน 8,667 และส่งไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="fc9a8-293">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="fc9a8-294">ตัวอย่าง: สร้างกฎการเรียกเก็บเงินตามเหตุการณ์สำคัญที่ตกลงไว้</span><span class="sxs-lookup"><span data-stu-id="fc9a8-294">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="fc9a8-295">องค์กรของคุณเป็นบริษัทให้คำปรึกษาด้านการจัดการ ตกลงที่จะดำเนินการวิจัยตลาดเกี่ยวกับสินค้าบริโภคที่ลูกค้าวางแผนจะขาย</span><span class="sxs-lookup"><span data-stu-id="fc9a8-295">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="fc9a8-296">ลูกค้าตกลงที่จะใช้บริการของคุณสำหรับรอบระยะเวลาสามเดือน เริ่มต้นในเดือนมีนาคม และตกลงที่จะชำระเงินแก่องค์กรของคุณ 50000</span><span class="sxs-lookup"><span data-stu-id="fc9a8-296">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="fc9a8-297">โครงการมีเหตุการณ์สำคัญสามอย่าง:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-297">The project has three milestones:</span></span>

-   <span data-ttu-id="fc9a8-298">เหตุการณ์สำคัญ 1: รวบรวมข้อมูลผู้บริโภค – 31 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-298">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="fc9a8-299">เหตุการณ์สำคัญ 2: วิเคราะห์ข้อมูลผู้บริโภค – 30 เมษายน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-299">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="fc9a8-300">เหตุการณ์สำคัญ 3: นำเสนอข้อเสนอความอยู่รอดของผลิตภัณฑ์ – 31 พฤษภาคม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-300">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="fc9a8-301">ลูกค้าตกลงที่จะชำระเงินองค์กรของคุณ 10,000 สำหรับเหตุการณ์สำคัญแรก 20,000 สำหรับเหตุการณ์สำคัญที่สอง และ 20,000 สำหรับเหตุการณ์สำคัญที่สาม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-301">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="fc9a8-302">เมื่อคุณตั้งค่าสัญญาโครงการ คุณตกลงที่จะเรียกเก็บเงินจากลูกค้าตามเหตุการณ์สำคัญที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fc9a8-302">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="fc9a8-303">การตั้งค่ากฎการเรียกเก็บเงินประกอบด้วยขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-303">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="fc9a8-304">กำหนดเหตุการณ์สำคัญของโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-304">Define the project milestones.</span></span>
-   <span data-ttu-id="fc9a8-305">กำหนดยอดเงินที่จะออกใบแจ้งหนี้ลูกค้า เมื่อแต่ละเหตุการณ์สำคัญเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fc9a8-305">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="fc9a8-306">เมื่อเหตุการณ์สำคัญแรกเสร็จสมบูรณ์ในวันที่ 31 มีนาคม คุณทำเครื่องหมายเหตุการณ์สำคัญเสร็จสมบูรณ์แล้ว และจากนั้นสร้างใบแจ้งหนี้ยอด 10,000 และส่งไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="fc9a8-306">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="fc9a8-307">คุณไม่สามารถสร้างใบแจ้งหนี้สำหรับเหตุการณ์สำคัญได้จนกว่าคุณได้ทำเครื่องหมายว่าเหตุการณ์สำคัญเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="fc9a8-307">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="fc9a8-308">ตัวอย่าง: สร้างกฎการเรียกเก็บเงินตามค่าบริการบวกค่าธรรมเนียมการจัดการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-308">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="fc9a8-309">องค์กรของคุณเป็นบริษัทให้คำปรึกษาด้านการจัดการ ตกลงที่จะดำเนินการวิจัยตลาดเพื่อประเมินความอยู่รอดของผลิตภัณฑ์ที่ลูกค้า บริษัทขายปลีกกำลังพัฒนา</span><span class="sxs-lookup"><span data-stu-id="fc9a8-309">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="fc9a8-310">เงื่อนไขของข้อตกลงระบุว่า คุณจะให้บริการของบริษัทให้คำปรึกษาด้านการจัดการสามอันดับแรกของคุณ ที่จะทำการวิจัยตามพื้นฐานของเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-310">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="fc9a8-311">ลูกค้าตกลงที่จะชำระ 100 ต่อชั่วโมง บวกค่าธรรมเนียมการจัดการ 10 เปอร์เซ็นต์สำหรับชั่วโมงให้คำปรึกษาที่เรียกเก็บไปยังโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-311">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="fc9a8-312">เมื่อคุณตั้งค่าสัญญาโครงการ สร้างกฎการเรียกเก็บเงินเพื่อเพิ่มค่าธรรมเนียมการจัดการ 10 เปอร์เซ็นต์สำหรับชั่วโมงการให้คำปรึกษาที่เรียกเก็บไปยังโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-312">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="fc9a8-313">เมื่อคุณสร้างใบแจ้งหนี้สำหรับลูกค้า ลูกค้าจะถูกเรียกเก็บเงินค่าธรรมเนียมการจัดการ 10 เปอร์เซ็นต์ บวกราคาชั่วโมงให้คำปรึกษา</span><span class="sxs-lookup"><span data-stu-id="fc9a8-313">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="fc9a8-314">ตัวอย่างเช่น ถ้าที่ปรึกษาสามรายทำงานรวม 200 ชั่วโมงในโครงการ ใบแจ้งหนี้จำนวน 22,000 ถูกสร้างขึ้นตามการคำนวณต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-314">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="fc9a8-315">200 ชั่วโมงที่ 100 ต่อชั่วโมง = 20,000</span><span class="sxs-lookup"><span data-stu-id="fc9a8-315">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="fc9a8-316">ค่าธรรมเนียมการจัดการ 10 เปอร์เซ็นต์ = 2,000</span><span class="sxs-lookup"><span data-stu-id="fc9a8-316">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="fc9a8-317">รวมยอดเงินใบแจ้งหนี้ = 22,000</span><span class="sxs-lookup"><span data-stu-id="fc9a8-317">Total invoice amount = 22,000</span></span>

<span data-ttu-id="fc9a8-318">หากค่าธรรมเนียมคิดภาษีให้กับลูกค้า และคุณเลือกกลุ่มภาษีขายในสัญญาโครงการ กลุ่มภาษีขายจะป้อนโดยอัตโนมัติในกฎการเรียกเก็บเงินสำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="fc9a8-318">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="fc9a8-319">ตัวอย่าง: สร้างกฎการเรียกเก็บเงินสำหรับค่าของเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-319">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="fc9a8-320">องค์กรของคุณเป็นบริษัทที่ปรึกษาด้านซอฟต์แวร์ ตกลงที่จะจัดหาที่ปรึกษาทางเทคนิคห้ารายให้ทำงานในโครงการพัฒนาซอฟต์แวร์ให้ลูกค้าสำหรับหกเดือนข้างหน้า</span><span class="sxs-lookup"><span data-stu-id="fc9a8-320">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="fc9a8-321">ลูกค้าตกลงที่จะชำระเงิน 150 ต่อแต่ละชั่วโมงให้คำปรึกษา บวกต้นทุนของวัสดุสำนักงาน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-321">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="fc9a8-322">องค์กรของคุณส่งใบแจ้งหนี้ให้กับลูกค้าเมื่อสิ้นสุดแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-322">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="fc9a8-323">เมื่อคุณตั้งค่าสัญญาโครงการ คุณตกลงที่จะเรียกเก็บเงินจากลูกค้าแต่ละเดือนสำหรับเวลาและวัสดุในโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-323">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="fc9a8-324">คุณสร้างกฎการเรียกเก็บเงินที่รวมถึงข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc9a8-324">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="fc9a8-325">สัญญารอบระยะเวลาเป็นหกเดือน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-325">The contract period is six months.</span></span>
-   <span data-ttu-id="fc9a8-326">เวลาให้คำปรึกษาคำนวณที่อัตรา 150 ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="fc9a8-326">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="fc9a8-327">ค่าใช้จ่ายวัสดุสำนักงานจะออกใบแจ้งหนี้ตามราคา และราคาทั้งหมดไม่เกิน 10,000 สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-327">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="fc9a8-328">คุณสร้างใบแจ้งหนี้ของลูกค้าที่สิ้นสุดแต่ละเดือนปฏิทินในระหว่างโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-328">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="fc9a8-329">ในระหว่างเดือนแรก ทั้งหมด 800 ชั่วโมงถูกบันทึกไว้โดยที่ปรึกษาในโครงการ</span><span class="sxs-lookup"><span data-stu-id="fc9a8-329">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="fc9a8-330">ต้นทุนของวัสดุสำนักงานที่คิดกับโครงการคือ 2000</span><span class="sxs-lookup"><span data-stu-id="fc9a8-330">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="fc9a8-331">ดังนั้น เมื่อสิ้นสุดเดือน คุณสร้างใบแจ้งหนี้สำหรับ 122,000 ซึ่งจะคำนวณจาก 800 ชั่วโมง เมื่อคิด 150 ต่อชั่วโมง บวกด้วย 2000 สำหรับวัสดุสำนักงาน</span><span class="sxs-lookup"><span data-stu-id="fc9a8-331">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>




