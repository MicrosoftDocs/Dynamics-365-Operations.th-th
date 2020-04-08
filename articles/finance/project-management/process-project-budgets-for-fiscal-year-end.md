---
title: โอนย้ายงบประมาณโครงการเมื่อสิ้นสุดปีบัญชี
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการโอนย้ายยอดเงินงบประมาณคงเหลือไปที่ปีในอนาคต และสร้างรายละเอียดทะเบียนงบประมาณ
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
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
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172341"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="998b7-103">โอนย้ายงบประมาณโครงการเมื่อสิ้นสุดปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="998b7-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="998b7-104">เมื่อทำงานกับโครงการหลายปี คุณอาจมีงบประมาณคงเหลือเมื่อสิ้นปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="998b7-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="998b7-105">คุณสามารถโอนย้ายยอดเงินงบประมาณคงเหลือสำหรับปีในอนาคต และสร้างรายละเอียดการลงทะเบียนงบประมาณสำหรับยอดเงินในบัญชีแยกประเภททั่วไปที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="998b7-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="998b7-106">ก่อนที่คุณจะยกยอดยอดเงินคงเหลือไป ให้ตรวจสอบและวิเคราะห์ยอดเงินงบประมาณคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="998b7-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="998b7-107">ตรวจสอบและวิเคราะห์ยอดเงินงบประมาณคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="998b7-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="998b7-108">ให้ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อตรวจทานยอดเงินงบประมาณสิ้นปีสำหรับโครงการ แต่จะไม่ยกยอดเงินไป</span><span class="sxs-lookup"><span data-stu-id="998b7-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="998b7-109">ไปที่ **การจัดการและการบัญชีโครงการ** > **ประจำงวด** > **งบประมาณ** > **ยกยอดงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="998b7-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="998b7-110">บนหน้า **กระบวนการยกยอดงบประมาณโครงการ** บนแท็บ **ตัวเลือกสิ้นปี** ให้ตรวจสอบว่า **ยกยอดยอดเงินงบประมาณโครงการคงเหลือไป** ไม่ถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="998b7-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="998b7-111">บนแท็บ **พารามิเตอร์** ในฟิลด์ **ปีงบประมาณโครงการ** ให้เลือกปีบัญชีที่คุณต้องการดูยอดเงินงบประมาณคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="998b7-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="998b7-112">ในฟิลด์ **ปีบัญชีที่เปิด** ให้เลือกปีบัญชีที่คุณต้องการดูยอดเงินงบประมาณคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="998b7-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="998b7-113">ในฟิลด์ **จากแบบจำลองการคาดการณ์** เลือก **งบประมาณคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="998b7-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="998b7-114">ถ้าต้องการรวมโครงการที่ตรงกับเกณฑ์ที่คุณเลือกและไม่มีงบประมาณคงเหลือ ให้เลือก **แสดงค่าคงเหลือเป็นศูนย์**</span><span class="sxs-lookup"><span data-stu-id="998b7-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="998b7-115">บนแท็บ **เลือกงบประมาณ** ให้เลือก **ดึงข้อมูลงบประมาณทั้งหมด** เพื่อโหลดงบประมาณทั้งหมดที่ตรงกับเกณฑ์ที่เลือกของคุณ และจากนั้น เลือก **ประมวลผล**</span><span class="sxs-lookup"><span data-stu-id="998b7-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="998b7-116">เมื่อต้องการออกแบบการสอบถามฐานข้อมูลที่โหลดชุดเฉพาะของงบประมาณลงในบานหน้าต่าง ให้เลือก **ดึงข้อมูลงบประมาณที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="998b7-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="998b7-117">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการเฉพาะในบานหน้าต่าง ให้เลือกรายการ และจากนั้น เลือก **ดูรายละเอียดงบประมาณ** หรือ **ดูบัญชี**</span><span class="sxs-lookup"><span data-stu-id="998b7-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="998b7-118">ยกยอดยอดเงินงบประมาณคงเหลือไป</span><span class="sxs-lookup"><span data-stu-id="998b7-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="998b7-119">เมื่อคุณประมวลผลยอดเงินงบประมาณคงเหลือ คุณสามารถสร้างธุรกรรมในบัญชีแยกประเภททั่วไปสำหรับยอดเงินที่คุณยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="998b7-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="998b7-120">เมื่อต้องการสร้างธุรกรรมบัญชีแยกประเภททั่วไป ให้ดำเนินการขั้นตอนต่างๆ ให้เสร็จสมบูรณ์ในส่วน [ยกยอดเงินงบประมาณไป และสร้างธุรกรรมบัญชีแยกประเภททั่วไป](#carry-forward)</span><span class="sxs-lookup"><span data-stu-id="998b7-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="998b7-121">ยอดเงินงบประมาณที่ถูกยกยอดไปจะถูกโอนย้ายไปที่แบบจำลองการคาดการณ์ที่เลือกในหน้า **แบบจำลองการคาดการณ์** เป็นแบบจำลองการคาดการณ์การยกยอด</span><span class="sxs-lookup"><span data-stu-id="998b7-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="998b7-122">ยกยอดเงินงบประมาณไปและสร้างธุรกรรมบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="998b7-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="998b7-123">เลือก **การจัดการและการบัญชีโครงการ** > **ประจำงวด** > **งบประมาณ** > **ยกยอดงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="998b7-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="998b7-124">บนหน้า **กระบวนการยกยอดงบประมาณโครงการ** เลือก **สิ้นปี** และจากนั้น เปิดใช้งาน **ยกยอดเงินงบประมาณโครงการคงเหลือไป** และ **สร้างรายการทะเบียนงบประมาณในบัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="998b7-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="998b7-125">บนแท็บ **พารามิเตอร์** ในกลุ่มฟิลด์ **พารามิเตอร์โครงการ** ให้เลือกดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="998b7-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="998b7-126">**ปีงบประมาณโครงการ**: ให้เลือกจุดเริ่มต้นของปีบัญชีที่คุณต้องการดูยอดเงินงบประมาณคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="998b7-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="998b7-127">**กำไรและขาดทุน**: สร้างธุรกรรมกำไรและขาดทุนในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="998b7-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="998b7-128">**WIP**: สร้างธุรกรรมงานระหว่างทำ (WIP) ในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="998b7-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="998b7-129">**ค่าจ้าง**: สร้างธุรกรรมการปันส่วนค่าจ้างในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="998b7-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="998b7-130">ในกลุ่มฟิลด์ **บัญชีแยกประเภททั่วไป** แสดงข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="998b7-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="998b7-131">ในฟิลด์ **ปีบัญชีที่เปิด** ให้เลือกปีบัญชีที่คุณต้องการโอนย้ายยอดเงินงบประมาณคงเหลือไปสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="998b7-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="998b7-132">ค่าเริ่มต้นคือหนึ่งปีหลังจากค่าในฟิลด์ **ปีงบประมาณโครงการ**</span><span class="sxs-lookup"><span data-stu-id="998b7-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="998b7-133">ในฟิลด์ **ระยะเวลายกยอด** ให้เลือกระยะเวลาที่คุณต้องการสร้างรายละเอียดการลงทะเบียนงบประมาณในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="998b7-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="998b7-134">โดยทั่วไปจะเป็นรอบระยะเวลาแรกในปีบัญชีที่เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="998b7-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="998b7-135">ในกลุ่มฟิลด์ **คัดลอกจาก/ไปยัง** แสดงข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="998b7-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="998b7-136">ในฟิลด์ **จากแบบจำลองการคาดการณ์** ให้เลือกแบบจำลองการคาดการณ์งบประมาณโครงการที่เชื่อมโยงกับยอดเงินงบประมาณคงเหลือที่คุณต้องการโอนย้ายสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="998b7-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="998b7-137">ในฟิลด์ **ไปยังแบบจำลองงบประมาณบัญชีแยกประเภท** ให้เลือกแบบจำลองงบประมาณบัญชีแยกประเภทที่เชื่อมโยงกับยอดเงินงบประมาณที่คุณต้องการโอนย้ายไปยังบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="998b7-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="998b7-138">เลือก **โอนย้ายสกุลเงินการขาย** เมื่อต้องการใช้สกุลเงินการขายของโครงการสำหรับธุรกรรมบัญชีแยกประเภททั่วไปที่จะถูกสร้างขึ้น เมื่อคุณโอนย้ายยอดเงินงบประมาณสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="998b7-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="998b7-139">เมื่อไม่มีการเลือกตัวเลือก ธุรกรรมจะใช้สกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="998b7-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="998b7-140">เลือก **แสดงค่าคงเหลือเป็นศูนย์** เพื่อรวมโครงการที่ไม่มียอดเงินงบประมาณคงเหลือ แต่เป็นไปตามเกณฑ์อื่นที่คุณเลือกในโครงการที่แสดงขึ้นในบานหน้าต่างด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="998b7-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="998b7-141">บนแท็บ **เลือกงบประมาณ** ให้เลือก **ดึงข้อมูลงบประมาณทั้งหมด** เพื่อโหลดงบประมาณทั้งหมดที่ตรงกับเกณฑ์ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="998b7-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="998b7-142">ถ้าคุณต้องการออกแบบการสอบถามฐานข้อมูลที่โหลดชุดเฉพาะของงบประมาณโครงการลงในบานหน้าต่าง ให้เลือก **ดึงข้อมูลงบประมาณที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="998b7-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="998b7-143">สำหรับแต่ละโครงการที่คุณต้องการประมวลผล ให้เลือกตัวเลือกที่จุดเริ่มต้นของรายการสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="998b7-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="998b7-144">ถ้าต้องการเลือกโครงการทั้งหมดหรือเกือบทั้งหมด ให้เลือกเครื่องหมายถูกที่มุมซ้ายบน</span><span class="sxs-lookup"><span data-stu-id="998b7-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="998b7-145">ถ้าต้องการแยกการประมวลผลโครงการใดๆ ให้ยกเลิกการเลือกเครื่องหมายถูกสำหรับโครงการนั้น</span><span class="sxs-lookup"><span data-stu-id="998b7-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="998b7-146">เพื่อโอนย้ายยอดเงินงบประมาณคงเหลือสำหรับโครงการที่เลือกไปยังปีบัญชีที่เลือก และสร้างรายละเอียดการลงทะเบียนงบประมาณในบัญชีแยกประเภททั่วไป เลือก **ประมวลผล**</span><span class="sxs-lookup"><span data-stu-id="998b7-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="998b7-147">ยกยอดเงินงบประมาณไปโดยไม่มีการสร้างธุรกรรมบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="998b7-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="998b7-148">ไปที่ **การจัดการและการบัญชีโครงการ** > **ประจำงวด** > **งบประมาณ** > **ยกยอดงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="998b7-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="998b7-149">บนหน้า **กระบวนการยกยอดงบประมาณโครงการ** ในฟิลด์ **ตัวเลือกสิ้นปี** ให้เลือก **ยกยอดยอดเงินงบประมาณโครงการคงเหลือไป**</span><span class="sxs-lookup"><span data-stu-id="998b7-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="998b7-150">ในกลุ่ม **พารามิเตอร์** ในฟิลด์ **ปีงบประมาณโครงการ** ให้เลือกปีบัญชีที่คุณต้องการดูยอดเงินงบประมาณคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="998b7-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="998b7-151">ในกลุ่ม **คัดลอกจาก/ไปยัง** แสดงข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="998b7-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="998b7-152">ในฟิลด์ **จากแบบจำลองการคาดการณ์** ให้เลือกแบบจำลองการคาดการณ์งบประมาณโครงการที่เชื่อมโยงกับยอดเงินงบประมาณคงเหลือที่คุณต้องการโอนย้ายสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="998b7-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="998b7-153">ให้เลือก **แสดงค่าคงเหลือเป็นศูนย์** เพื่อรวมโครงการที่ไม่มีงบประมาณคงเหลือ แต่ตรงกับเกณฑ์ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="998b7-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="998b7-154">ในกลุ่ม **เลือกงบประมาณ** ให้เลือก **ดึงข้อมูลงบประมาณทั้งหมด** เพื่อโหลดงบประมาณทั้งหมดที่ตรงกับเกณฑ์ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="998b7-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="998b7-155">เมื่อต้องการออกแบบการสอบถามฐานข้อมูลที่โหลดชุดเฉพาะของงบประมาณโครงการลงในบานหน้าต่าง ให้เลือก **ดึงข้อมูลงบประมาณที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="998b7-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="998b7-156">สำหรับแต่ละโครงการที่คุณต้องการประมวลผล ให้เลือกตัวเลือกที่จุดเริ่มต้นของรายการสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="998b7-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="998b7-157">เลือก **ประมวลผล** เพื่อโอนย้ายยอดเงินงบประมาณคงเหลือสำหรับโครงการที่เลือกไปยังปีบัญชีที่เลือก</span><span class="sxs-lookup"><span data-stu-id="998b7-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

