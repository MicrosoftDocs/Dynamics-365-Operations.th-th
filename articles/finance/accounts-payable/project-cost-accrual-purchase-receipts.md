---
title: การค้างรับค้างจ่ายต้นทุนโครงการในใบรับสินค้าซื้อ
description: หัวข้อนี้อธิบายวิธีการติดตามต้นทุนโครงการค้างรับจากใบรับสินค้าของการซื้อใน Microsoft Dynamics 365 Finance
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c2b92f1f5caf34bf798b86380b73c2dcc7de17b3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231651"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="4d4c9-103">การค้างรับค้างจ่ายต้นทุนโครงการในใบรับสินค้าซื้อ</span><span class="sxs-lookup"><span data-stu-id="4d4c9-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d4c9-104">หัวข้อนี้อธิบายวิธีการติดตามต้นทุนโครงการค้างรับจากใบรับสินค้าของการซื้อใน Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="4d4c9-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 Finance.</span></span> 

<span data-ttu-id="4d4c9-105">ใบแจ้งหนี้สำหรับโครงการมักจะมาถึงช้ากว่าสินค้าและบริการที่จัดส่ง ซึ่งอาจมีผลกระทบอย่างมากต่อตัวบ่งชี้ประสิทธิภาพการทำงานหลัก (KPI) ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d4c9-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="4d4c9-106">การสามารถติดตามธุรกรรมเหล่านี้ได้ทั้งในรายงานทางการเงินและรายงานของโครงการเป็นสิ่งสำคัญ</span><span class="sxs-lookup"><span data-stu-id="4d4c9-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="4d4c9-107">สถานการณ์ตัวอย่างต่อไปนี้จะแสดงสิ่งนี้</span><span class="sxs-lookup"><span data-stu-id="4d4c9-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="4d4c9-108">การให้คำปรึกษา Contoso ได้เริ่มต้นโครงการการปรับใช้ระบบคลาวด์ใหม่</span><span class="sxs-lookup"><span data-stu-id="4d4c9-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="4d4c9-109">มีการสร้างใบสั่งซื้อเพื่อซื้อเครื่องคอมพิวเตอร์สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d4c9-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="4d4c9-110">คอมพิวเตอร์จะมีต้นทุนเท่ากับ $1500 และบริการการติดตั้งจะมีต้นทุนเท่ากับ $150</span><span class="sxs-lookup"><span data-stu-id="4d4c9-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="4d4c9-111">ผู้จัดจำหน่ายได้จัดส่งและติดตั้งเครื่องคอมพิวเตอร์แล้ว แต่ใบแจ้งหนี้ยังมาไม่ถึงการให้คำปรึกษา Contoso</span><span class="sxs-lookup"><span data-stu-id="4d4c9-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="4d4c9-112">ผู้จัดการโครงการอยากเห็นการรับรู้ต้นทุนของโครงการที่ $1650 ก่อนที่จะจัดส่งใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="4d4c9-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="4d4c9-113">ต้นทุนนี้ควรจะสะท้อนให้เห็นในงบการเงินสิ้นเดือนของของบริษัทด้วย</span><span class="sxs-lookup"><span data-stu-id="4d4c9-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="4d4c9-114">ค่าใช้จ่ายค้างจ่ายจะต้องถูกบันทึกบนระดับทางการเงินและระดับโครงการเพื่อวัตถุประสงค์ในการรายงาน</span><span class="sxs-lookup"><span data-stu-id="4d4c9-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="4d4c9-115">การอัพเดตทางการเงินของใบรับสินค้าสามารถติดตามสำหรับประเภทสินค้าและการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="4d4c9-115">The financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="4d4c9-116">สำหรับสินค้า บนหน้า **พารามิเตอร์บัญชีเจ้าหนี้** เลือกตัวเลือก **ลงรายการบัญชีใบรับสินค้าในบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="4d4c9-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="4d4c9-117">[![หน้าพารามิเตอร์บัญชีเจ้าหนี้](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="4d4c9-117">[![Accounts payable parameters page](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="4d4c9-118">สำหรับประเภทการจัดซื้อ บนหน้า **กฎนโยบายประเภท** เลือกนโยบาย **การซื้อ** จากนั้นเลือก **บันทึกค่าใช้จ่ายการซื้อค้างจ่ายเมื่อรับสินค้า** สำหรับประเภทการจัดซื้อแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="4d4c9-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="4d4c9-119">[![หน้ากฎนโยบายประเภท](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="4d4c9-119">[![Category policy rule page](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="4d4c9-120">บัญชี **รายจ่ายการซื้อ ยังไม่ได้ออกใบแจ้งหนี้** และ **รายการคงค้างของการซื้อ** ใน **การตั้งค่าการลงรายการบัญชี** จะใช้เมื่อมีการลงรายการบัญชีใบสำคัญที่เกี่ยวข้องกับใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4d4c9-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>

<span data-ttu-id="4d4c9-121">ลองดูว่าการลงรายการบัญชีใบรับสินค้าจะส่งผลกระทบต่อบัญชีแยกประเภททั่วไปและข้อมูลโครงการอย่างไรโดยใช้สถานการณ์เดียวกันนี้</span><span class="sxs-lookup"><span data-stu-id="4d4c9-121">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="4d4c9-122">**ขั้นตอนที่ 1:** สร้างและยืนยันใบสั่งซื้อใหม่สำหรับโครงการเพื่อบันทึกการซื้อเครื่องคอมพิวเตอร์เป็นจำนวนเงิน $1500 และสำหรับการบริการติดตั้งเป็นจำนวนเงิน $150</span><span class="sxs-lookup"><span data-stu-id="4d4c9-122">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="4d4c9-123">[![สร้างใบสั่งซื้อใหม่](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="4d4c9-123">[![Create new purchase order](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="4d4c9-124">เมื่อมีการยืนยันใบสั่งซื้อ ธุรกรรมสำหรับต้นทุนผูกมัดจะถูกสร้างขึ้นสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d4c9-124">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="4d4c9-125">[![ธุรกรรมที่สร้างขึ้น](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="4d4c9-125">[![Transactions created](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="4d4c9-126">ธุรกรรมสำหรับต้นทุนผูกมัดจะมีการตั้งค่าฟิลด์ **จุดเริ่มต้นของธุรกรรม** เป็น **ใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="4d4c9-126">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="4d4c9-127">การสร้างและการยืนยันใบสั่งซื้อไม่ได้เป็นการสร้างธุรกรรมสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d4c9-127">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="4d4c9-128">**ขั้นตอนที่ 2:** สินค้าและบริการได้รับการจัดส่งและมีการลงทะเบียนใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4d4c9-128">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="4d4c9-129">การลงรายการบัญชีใบรับสินค้าจะสร้างและลงรายการบัญชีใบสำคัญในบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="4d4c9-129">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="4d4c9-130">ใบสำคัญจะการหักบัญชีเงินฝากรายจ่ายการซื้อ บัญชีที่ยังไม่ได้ออกใบแจ้งหนี้ และบัญชีค้างรับค้างจ่ายการซื้อเครดิต</span><span class="sxs-lookup"><span data-stu-id="4d4c9-130">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="4d4c9-131">[![ธุรกรรมใบสำคัญ](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="4d4c9-131">[![Voucher transactions](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="4d4c9-132">การลงรายการบัญชีใบรับสินค้าจะใช้การตั้งค่าการลงรายการบัญชีสำหรับประเภทการจัดซื้อ และผลิตภัณฑ์ ไม่ใช่การตั้งค่าการลงรายการบัญชีสำหรับประเภทโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d4c9-132">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="4d4c9-133">เพื่อให้สะท้อนถึงผลกระทบทางการเงินของรายการคงค้างของการซื้อได้อย่างถูกต้อง การตั้งค่านี้จะต้องถูกจัดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="4d4c9-133">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="4d4c9-134">สามารถแม็ปประเภทการจัดซื้อกับประเภทโครงการบนหน้า **ประเภทการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="4d4c9-134">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="4d4c9-135">[![หน้าประเภทการจัดซื้อ](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="4d4c9-135">[![Procurement category page](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="4d4c9-136">**ขั้นตอนที่ 3:** สร้างใบแจ้งหนี้ของผู้จัดจำหน่ายฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="4d4c9-136">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="4d4c9-137">การลงรายการบัญชีใบรับสินค้าไม่มีผลกระทบต่อข้อมูลโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d4c9-137">Posting a product receipt does not impact project information.</span></span> <span data-ttu-id="4d4c9-138">วิธีการแก้ไขปัญหาคือคุณสามารถสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายฉบับร่างได้หลังจากที่ลงรายการบัญชีการรับสินค้าซื้อโดยทันที</span><span class="sxs-lookup"><span data-stu-id="4d4c9-138">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="4d4c9-139">ไปที่หน้า **ใบสั่งซื้อ** &gt; **แท็บใบแจ้งหนี้** &gt; **สร้าง** &gt; **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="4d4c9-139">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="4d4c9-140">วิธีนี้เป็นการสร้างเอกสารใบแจ้งหนี้ที่ค้างอยู่ที่อัพเดตข้อมูลโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d4c9-140">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="4d4c9-141">การสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายฉบับร่างจะสร้างธุรกรรมโครงการที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="4d4c9-141">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="4d4c9-142">[![ธุรกรรมโครงการที่ค้างอยู่](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="4d4c9-142">[![Pending project transactions](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="4d4c9-143">ในหน้า **ต้นทุนผูกมัด** เรกคอร์ดที่สร้างขึ้นในขั้นตอนที่ 1 จะถูกปิด และจะมีการสร้างเรกคอร์ดใหม่เพื่อให้สะท้อนถึงต้นทุนผูกมัดที่มาจากใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="4d4c9-143">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="4d4c9-144">ฟิลด์ **จุดเริ่มต้นของธุรกรรม** สำหรับต้นทุนผูกมัดจะถูกกำหนดเป็น **ใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="4d4c9-144">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="4d4c9-145">[![หน้าต้นทุนผูกมัด](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="4d4c9-145">[![Commited costs page](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="4d4c9-146">ใบแจ้งหนี้ของผู้จัดจำหน่ายจะยังคงอยู่ในสถานะที่ค้างอยู่จนกว่าใบแจ้งหนี้ของผู้จัดจำหน่ายจริงจะมาถึง</span><span class="sxs-lookup"><span data-stu-id="4d4c9-146">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]