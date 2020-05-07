---
title: สร้างสัญญาขั้นสูงสำหรับการเรียกเก็บเงินตามความคืบหน้า
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างสัญญาโครงการ เพื่อให้คุณสามารถสร้างใบแจ้งหนี้สำหรับลูกค้า โดยยึดตามเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282851"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="02408-103">สร้างสัญญาขั้นสูงสำหรับการเรียกเก็บเงินตามความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="02408-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="02408-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างสัญญาโครงการ เพื่อให้คุณสามารถสร้างใบแจ้งหนี้สำหรับลูกค้า โดยยึดตามเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="02408-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="02408-105">ยอดเงินในใบแจ้งหนี้จะถูกคำนวณโดยอัตโนมัติสำหรับประเภทงบประมาณของงานที่คุณตั้งค่าสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="02408-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="02408-106">มีการตั้งค่าช่วงเวลาของใบแจ้งหนี้ เมื่อคุณเจรจาสัญญาโครงการกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="02408-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="02408-107">ใช้กระบวนงานในหัวข้อนี้เพื่อตั้งค่าสัญญา โครงการที่เกี่ยวข้อง และกฎการเรียกเก็บเงิน ที่คำนวณยอดเงินในใบแจ้งหนี้สำหรับประเภทงบประมาณของงานที่คุณตั้งค่าสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="02408-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="02408-108">หลังจากที่คุณได้สร้างสัญญาและโครงการแล้ว คุณสามารถตั้งค่ารายละเอียดของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="02408-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="02408-109">ตัวอย่างเช่น คุณสามารถกำหนดกิจกรรมและกำหนดผู้ปฏิบัติงานให้แก่โครงการได้</span><span class="sxs-lookup"><span data-stu-id="02408-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="02408-110">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="02408-110">Example</span></span>

<span data-ttu-id="02408-111">องค์กรของคุณเป็นบริษัทพัฒนาซอฟต์แวร์</span><span class="sxs-lookup"><span data-stu-id="02408-111">Your organization is a software development firm.</span></span> <span data-ttu-id="02408-112">คุณตกลงที่จะพัฒนาแพ็คเกจการบัญชีค่าจ้างสำหรับลูกค้าสำหรับค่าธรรมเนียมรวม 20,000 ดอลลาร์สหรัฐ (USD)</span><span class="sxs-lookup"><span data-stu-id="02408-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="02408-113">องค์กรของคุณตกลงที่จะออกใบแจ้งหนี้ไปให้ลูกค้า เมื่อคุณดำเนินการเปอร์เซ็นต์ที่ระบุของโครงการแล้วเสร็จ</span><span class="sxs-lookup"><span data-stu-id="02408-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="02408-114">คุณตั้งค่าประเภทโครงการต่อไปนี้สำหรับงาน เพื่อให้คุณสามารถใช้ในกระบวนการเรียกเก็บเงินได้:</span><span class="sxs-lookup"><span data-stu-id="02408-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="02408-115">การให้คำปรึกษา</span><span class="sxs-lookup"><span data-stu-id="02408-115">Consulting</span></span>
- <span data-ttu-id="02408-116">ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="02408-116">Design</span></span>
- <span data-ttu-id="02408-117">การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="02408-117">Installation</span></span>

<span data-ttu-id="02408-118">นอกจากนี้ คุณยังตั้งค่ากฎการเรียกเก็บเงินที่จะคำนวณยอดเงินใบแจ้งหนี้โดยอัตโนมัติ สำหรับเปอร์เซ็นต์ของงานในโครงการที่เสร็จสมบูรณ์ในแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="02408-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="02408-119">ผู้จัดการงบประมาณสร้างงบประมาณสำหรับประเภทโครงการ</span><span class="sxs-lookup"><span data-stu-id="02408-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="02408-120">ปริมาณของงานที่เสร็จสมบูรณ์จะถูกคำนวณเป็นเปอร์เซ็นต์ของงานที่เกิดขึ้นจริงเปรียบเทียบกับยอดเงินที่จัดงบประมาณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="02408-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="02408-121">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="02408-121">Prerequisites</span></span>

<span data-ttu-id="02408-122">ก่อนที่คุณจะสร้างโครงการที่ใช้กฎการเรียกเก็บเงิน คุณต้องตั้งค่าลำดับหมายเลขสำหรับกฎการเรียกเก็บเงินและสมุดรายวันค่าธรรมเนียมที่ใช้ในการลงรายการบัญชีการเรียกเก็บเงินตามความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="02408-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="02408-123">ไปที่ **การจัดการและการบัญชีโครงการ** \> **การตั้งค่า** \> **พารามิเตอร์การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="02408-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="02408-124">บนหน้า **พารามิเตอร์การจัดการและการบัญชีโครงการ** บนแท็บ **ลำดับหมายเลข** ให้ตั้งค่าลำดับหมายเลขที่คุณต้องการใช้ เมื่อมีการสร้างกฎการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="02408-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="02408-125">ไปยัง **การจัดการและการบัญชีโครงการ** \> **สมุดรายวัน** \> **ค่าธรรมเนียม**</span><span class="sxs-lookup"><span data-stu-id="02408-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="02408-126">บนหน้า **สมุดรายวันค่าธรรมเนียม** เลือก **สร้าง** แล้วป้อนชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="02408-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="02408-127">สร้างสัญญาสำหรับการเรียกเก็บเงินตามความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="02408-127">Create a contract for progress billings</span></span>

<span data-ttu-id="02408-128">ใช้กระบวนงานนี้เพื่อสร้างสัญญาโครงการสำหรับโครงการที่มีราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="02408-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="02408-129">คุณสร้างใบแจ้งหนี้โครงการ เมื่องานที่เสร็จสมบูรณ์ในโครงการไปถึงเปอร์เซ็นต์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="02408-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="02408-130">ไปที่ **การจัดการและการบัญชีโครงการ** \> **โครงการ** \> **สัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="02408-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="02408-131">ในหน้า **สัญญาโครงการ** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="02408-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="02408-132">ในกล่องโต้ตอบ **สัญญาโครงการใหม่** ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="02408-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="02408-133">**ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="02408-133">**Name**</span></span>
    - <span data-ttu-id="02408-134">**ชนิดของการจัดหาเงินทุน**</span><span class="sxs-lookup"><span data-stu-id="02408-134">**Funding type**</span></span>
    - <span data-ttu-id="02408-135">**แหล่งเงินทุน**</span><span class="sxs-lookup"><span data-stu-id="02408-135">**Funding source**</span></span>
    - <span data-ttu-id="02408-136">**สกุลเงินที่ใช้ในการขาย** – โดยค่าเริ่มต้น สกุลเงินนี้จะใช้สำหรับใบแจ้งหนี้ของลูกค้าที่เชื่อมโยงกับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="02408-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="02408-137">อย่างไรก็ตาม คุณสามารถเปลี่ยนสกุลเงินที่ใช้ในการขายในใบแจ้งหนี้ของลูกค้าที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="02408-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="02408-138">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="02408-138">Select **OK**.</span></span> <span data-ttu-id="02408-139">ข้อมูลจะถูกคัดลอกไปยังส่วนหัวของหน้า **สัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="02408-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="02408-140">บนหน้า **สัญญาโครงการ** ให้กรอกข้อมูลที่จำเป็นส่วนที่เหลือสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="02408-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="02408-141">สร้างโครงการสำหรับการเรียกเก็บเงินตามความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="02408-141">Create a project for progress billings</span></span>

<span data-ttu-id="02408-142">ทำตามขั้นตอนเหล่านี้เพื่อสร้างโครงการและโครงการย่อยใดๆ ที่เชื่อมโยงกับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="02408-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="02408-143">ไปที่ **การจัดการและการบัญชีโครงการ** \> **โครงการ** \> **โครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="02408-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="02408-144">ในหน้า **โครงการทั้งหมด** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="02408-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="02408-145">ในกล่องโต้ตอบ **โครงการใหม่** ในฟิลด์ **ชนิดโครงการ** ให้เลือก **เวลาและวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="02408-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="02408-146">เลือกกลุ่มโครงการ</span><span class="sxs-lookup"><span data-stu-id="02408-146">Select a project group.</span></span> <span data-ttu-id="02408-147">กลุ่มโครงการกำหนดข้อมูลการลงรายการบัญชีสำหรับโครงการที่ถูกกำหนดให้กับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="02408-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="02408-148">เลือก **สร้างโครงการ**</span><span class="sxs-lookup"><span data-stu-id="02408-148">Select **Create project**.</span></span>
6. <span data-ttu-id="02408-149">หลังจากที่มีการสร้างโครงการแล้ว ให้ตั้งค่าขั้นตอนของโครงการเป็น **อยู่ระหว่างดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="02408-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="02408-150">สร้างงบประมาณสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="02408-150">Create a budget for a project</span></span>

<span data-ttu-id="02408-151">ประเภทงบประมาณถูกใช้ในการคำนวณยอดเงินใบแจ้งหนี้สำหรับเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์สำหรับแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="02408-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="02408-152">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างประเภทงบประมาณสำหรับต้นทุนที่ประเมิน</span><span class="sxs-lookup"><span data-stu-id="02408-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="02408-153">ไปที่ **การจัดการและการบัญชีโครงการ** \> **โครงการ** \> **โครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="02408-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="02408-154">บนหน้า **โครงการทั้งหมด** ให้เลือกและเปิดโครงการที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="02408-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="02408-155">บนหน้า **โครงการ** บนบานหน้าต่างการดำเนินการ บนแท็บ **แผน** ในกลุ่ม **งบประมาณ** ให้เลือก **งบประมาณโครงการ**</span><span class="sxs-lookup"><span data-stu-id="02408-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="02408-156">บนหน้า **งบประมาณโครงการ** ให้ป้อนต้นทุนที่ประเมินสำหรับประเภทแต่ละประเภทในโครงการ</span><span class="sxs-lookup"><span data-stu-id="02408-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="02408-157">สร้างกฎการเรียกเก็บเงินสำหรับการเรียกเก็บเงินตามความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="02408-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="02408-158">ไปที่ **การจัดการและการบัญชีโครงการ** \> **โครงการ** \> **สัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="02408-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="02408-159">บนหน้า **สัญญาโครงการ** ให้เลือกและเปิดสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="02408-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="02408-160">บนหน้าสัญญาโครงการ บนแท็บ FastTab **กฎการเรียกเก็บเงิน** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="02408-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="02408-161">บนหน้า **กฎการเรียกเก็บเงิน** ในฟิลด์ **ชนิดรายการ** เลือก **ความก้าวหน้า**</span><span class="sxs-lookup"><span data-stu-id="02408-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="02408-162">บน FastTab **รายละเอียดของรายการกฎการเรียกเก็บเงิน** ในฟิลด์ **มูลค่าตามสัญญา** ให้ป้อนมูลค่ารวมของสัญญา</span><span class="sxs-lookup"><span data-stu-id="02408-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="02408-163">ในฟิลด์ **ประเภท** ให้เลือกประเภทที่จะลงรายการบัญชีธุรกรรมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="02408-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="02408-164">ในฟิลด์ **โครงการ** ให้เลือกโครงการที่ใช้กฎการเรียกเก็บเงินนี้</span><span class="sxs-lookup"><span data-stu-id="02408-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="02408-165">ไม่จำเป็น: กำหนดกฎการเรียกเก็บเงินให้แก่โครงการเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="02408-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="02408-166">บน FastTab **โครงการ** ในส่วน **โครงการที่พร้อมใช้งาน** ให้เลือกโครงการ แล้วเลือกปุ่มลูกศรขวาเพื่อเพิ่มโครงการในส่วน **โครงการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="02408-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="02408-167">ไม่จำเป็น: คำนวณยอดเงินเปอร์เซ็นต์ที่ลูกค้าหักจากเงินที่ชำระในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="02408-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="02408-168">บน FastTab **เงื่อนไขเงินประกันผลงานสำหรับการชำระเงิน** ให้เลือกแหล่งเงินทุน และจากนั้นในฟิลด์ **เปอร์เซ็นต์เงินวางประกัน** ให้ป้อนเปอร์เซ็นต์ของเงินวางประกัน</span><span class="sxs-lookup"><span data-stu-id="02408-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="02408-169">ทำซ้ำขั้นตอนเหล่านี้เพื่อสร้างกฎการเรียกเก็บเงินเพิ่มเติมสำหรับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="02408-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
