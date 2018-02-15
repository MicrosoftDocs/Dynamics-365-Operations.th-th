---
title: "ข้อกำหนดเบื้องต้นสำหรับต้นทุนมาตรฐาน"
description: "หัวข้อนี้อธิบายขั้นตอนพื้นฐานสำหรับการใช้ต้นทุนมาตรฐาน"
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e63f2b4289b640e601492425331ea8f3804d139a
ms.openlocfilehash: 4f505a2de89863d1a12d415795fdfb82b3557bc0
ms.contentlocale: th-th
ms.lasthandoff: 01/17/2018

---

# <a name="prerequisites-for-standard-costs"></a><span data-ttu-id="2e433-103">ข้อกำหนดเบื้องต้นสำหรับต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="2e433-103">Prerequisites for standard costs</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2e433-104">หัวข้อนี้อธิบายขั้นตอนพื้นฐานสำหรับการใช้ต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="2e433-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="2e433-105">ขั้นตอนในลำดับต่อมาขึ้นอยู่กับการดำเนินการของบริษัท</span><span class="sxs-lookup"><span data-stu-id="2e433-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="2e433-106">ตัวอย่างเช่น ขั้นตอนแตกต่างสำหรับสภาพแวดล้อมที่ไม่เกี่ยวกับการผลิต สภาพแวดล้อมการผลิตที่ไม่ใช้กระบวนการผลิต และสภาพแวดล้อมการผลิตที่ใช้กระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="2e433-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="2e433-107">หากต้องการตั้งค่าต้นทุนมาตรฐาน ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2e433-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="2e433-108">**1. สร้างกลุ่มแบบจำลองสินค้าสำหรับต้นทุนมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="2e433-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="2e433-109">ใช้หน้า **กลุ่มแบบจำลองสินค้า** เพื่อสร้างกลุ่มใหม่สำหรับต้นทุนมาตรฐาน และเพื่อกำหนดแบบจำลองสินค้าคงคลังของ **ต้นทุนมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="2e433-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="2e433-110">ตัวระบุสำหรับกลุ่มแบบจำลองสินค้าควรจะมีความหมาย เช่น **ต้นทุน Std**</span><span class="sxs-lookup"><span data-stu-id="2e433-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="2e433-111">เลือกกล่องกาเครื่องหมายเพื่อระบุว่า กลุ่มควรให้อนุญาตสินค้าคงคลังค่าลบทางการเงิน และควรลงรายการบัญชีสินค้าคงคลังตามจริง และสินค้าคงคลังทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="2e433-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="2e433-112">กลุ่มต้นทุนมาตรฐานจะถูกกำหนดให้กับสินค้า</span><span class="sxs-lookup"><span data-stu-id="2e433-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="2e433-113">**2. กำหนดบัญชีแยกประเภทที่เกี่ยวข้องกับผลต่างของต้นทุนมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="2e433-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="2e433-114">ใช้หน้า **ผังบัญชี** เพื่อกำหนดบัญชีแยกประเภทที่เกี่ยวข้องกับผลต่างของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="2e433-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="2e433-115">บัญชีแยกประเภทเหล่านี้ต้องได้รับการกำหนด ก่อนที่จะสามารถถูกกำหนดลงในหน้า **การลงรายการบัญชี** ได้</span><span class="sxs-lookup"><span data-stu-id="2e433-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="2e433-116">บัญชีแยกประเภทสามารถสะท้อนกลุ่มสินค้าและกลุ่มต้นทุนได้</span><span class="sxs-lookup"><span data-stu-id="2e433-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="2e433-117">**3. กำหนดบัญชีแยกประเภทให้กับการลงรายการบัญชีสินค้าที่เกี่ยวข้องกับผลต่างของต้นทุนมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="2e433-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="2e433-118">ใช้หน้า **การลงรายการบัญชี** เพื่อกำหนดบัญชีแยกประเภทที่เกี่ยวข้องกับผลต่างของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="2e433-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="2e433-119">คุณสามารถระบุบัญชีแยกประเภทของผลต่างตามสินค้า (หรือกลุ่มสินค้า) และตามกลุ่มต้นทุน (หรือชนิดกลุ่มต้นทุน) หรือคุณสามารถระบุว่าบัญชีแยกบัญชีจะใช้งานกับสินค้าทั้งหมดและกลุ่มต้นทุนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2e433-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="2e433-120">ตัวเลือกเหล่านี้ตรงกับความสัมพันธ์ของต้นทุนสำหรับตาราง กลุ่ม และทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2e433-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="2e433-121">ก่อนที่คุณจะกำหนดกฎการลงรายการบัญชีของสินค้า ใช้หน้า **การรวมของธุรกรรม** เพื่อเปิดใช้งานความสัมพันธ์ของต้นทุน (สำหรับตาราง กลุ่ม และทั้งหมด)</span><span class="sxs-lookup"><span data-stu-id="2e433-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="2e433-122">**4. กำหนดพารามิเตอร์สินค้าคงคลังที่เกี่ยวข้องกับต้นทุนมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="2e433-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="2e433-123">ใช้แท็บ **สูตรการผลิต** บนหน้า **พารามิเตอร์สินค้าคงคลัง** เพื่อกำหนดพารามิเตอร์การควบคุมต้นทุนสองตัวที่เกี่ยวข้องกับต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="2e433-123">Use the **Bills of materials** tab on the **Inventory parameters** page to define two cost control parameters that are related to standard costs.</span></span> 

    -  <span data-ttu-id="2e433-124">ใช้ฟิลด์ **การแบ่งต้นทุน** เลือก **ไม่มี** หรือ **บัญชีแยกประเภทย่อย**</span><span class="sxs-lookup"><span data-stu-id="2e433-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="2e433-125">ถ้าคุณเลือก **บัญชีแยกประเภทย่อย** การแบ่งต้นทุนจะเป็นการแบ่งต้นทุน *ที่ใช้งานอยู่*</span><span class="sxs-lookup"><span data-stu-id="2e433-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="2e433-126">การจำแนกต้นทุนที่ใช้งานอยู่เป็นสิ่งจำเป็นสำหรับการคำนวณ การเก็บรักษา และการดูการจัดเซกเมนต์กลุ่มต้นทุนในโครงสร้างผลิตภัณฑ์แบบหลายระดับของสินค้าต้นทุนมาตรฐาน </span><span class="sxs-lookup"><span data-stu-id="2e433-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="2e433-127">เมื่อใช้งานการแบ่งต้นทุน คุณสามารถรายงานและวิเคราะห์สินค้าคงคลัง งานระหว่างทำ (WIP) ต้นทุนสินค้าขาย (COGS) ต่อกลุ่มต้นทุนในระดับเดียว หลายระดับ หรือรูปแบบรวม</span><span class="sxs-lookup"><span data-stu-id="2e433-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="2e433-128">เมื่อใช้งานการแบ่งต้นทุน ถ้าคุณเปิดใช้งานต้นทุนของสินค้าที่ผลิต การแบ่งส่วนกลุ่มต้นทุนจะถูกเก็บไว้ในเรกคอร์ดต้นทุนของสินค้า</span><span class="sxs-lookup"><span data-stu-id="2e433-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="2e433-129">ถ้าคุณเลือก **ไม่มี** การแบ่งส่วนกลุ่มต้นทุนจะไม่ถูกเก็บรักษาไว้สำหรับสินค้าต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="2e433-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="2e433-130">กล่าวคือ ต้นทุนมาตรฐานของสินค้าที่ผลิตจะถูกคำนวณ และถูกเก็บรักษาเป็นยอดเดียว โดยไม่มีการแบ่งส่วนกลุ่มต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2e433-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="2e433-131">การจัดสรรต้นทุนของส่วนประกอบที่ผลิตจะถูกรวมเป็นยอดเดียว</span><span class="sxs-lookup"><span data-stu-id="2e433-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="2e433-132">ใช้ฟิลด์ **ผลต่างจากมาตรฐาน** เลือก **สรุป** หรือ **ต่อกลุ่มต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="2e433-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="2e433-133">ถ้าคุณเลือก **ต่อกลุ่มต้นทุน** คุณสามารถระบุผลต่างราคาซื้อและผลต่างการผลิตตามกลุ่มต้นทุนได้</span><span class="sxs-lookup"><span data-stu-id="2e433-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="2e433-134">นอกจากนี้คุณยังสามารถระบุผลต่างของการผลิตสี่ชนิดได้: ผลต่างของขนาดล็อต ปริมาณ ราคา และการแทนค่า</span><span class="sxs-lookup"><span data-stu-id="2e433-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="2e433-135">ถ้าคุณเลือก **สรุป** คุณจะไม่สามารถระบุผลต่างตามกลุ่มต้นทุนได้ และคุณจะไม่สามารถระบุผลต่างการผลิตสี่ชนิดได้</span><span class="sxs-lookup"><span data-stu-id="2e433-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="2e433-136">คุณสามารถดูผลต่างการผลิตที่ได้รับการสรุปได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2e433-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="2e433-137">นโยบายเกี่ยวกับผลต่างจากมาตรฐานทำงานอย่างเป็นอิสระจากนโยบายการจำแนกต้นทุน </span><span class="sxs-lookup"><span data-stu-id="2e433-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="2e433-138">กล่าวคือ คุณสามารถเลือกนโยบายการแบ่งต้นทุนได้เป็น **ไม่มี** และเลือกผลต่างต่อกลุ่มต้นทุน เพื่อให้ระบบจะยังคงรวบรวมผลต่างการผลิตตามกลุ่มต้นทุนอยู่</span><span class="sxs-lookup"><span data-stu-id="2e433-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="2e433-139">**5. สร้างเวอร์ชันการคิดต้นทุนสำหรับต้นทุนมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="2e433-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="2e433-140">ใช้หน้า **การตั้งค่าเวอร์ชันการคิดต้นทุน** เพื่อสร้างเวอร์ชันการคิดต้นทุนหนึ่งเวอร์ชันหรือมากกว่าสำหรับต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="2e433-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="2e433-141">เวอร์ชันการคำนวณต้นทุนแต่ละเวอร์ชันต้องได้รับการออกแบบโดยชนิดการคิดต้นทุนแบบ **ต้นทุนมาตรฐาน** และต้องอนุญาตให้รวมข้อมูลต้นทุนไว้ในเนื้อหาได้</span><span class="sxs-lookup"><span data-stu-id="2e433-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="2e433-142">**6. เตรียมลูกค้าที่มีอยู่เพื่อใช้ต้นทุนมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="2e433-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="2e433-143">ลูกค้าที่ต้องการเปลี่ยนสินค้าที่มีอยู่ของพวกเขาเป็นแบบจำลองสินค้าคงคลังของต้นทุนมาตรฐานจะต้องใช้หน้า **การแปลงต้นทุนมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="2e433-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="2e433-144">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="2e433-144">Related topics</span></span>
--------

[<span data-ttu-id="2e433-145">ภาพรวมของการแปลงต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="2e433-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)


