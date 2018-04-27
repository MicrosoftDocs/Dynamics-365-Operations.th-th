---
title: "ป้อนยอดดุลต้นงวดของค่าจ้าง"
description: "หัวข้ออธิบายขั้นตอนสำหรับการป้อนยอดดุลต้นงวดสำหรับรหัสรายได้ การหักลด สวัสดิการ และภาษี ข้อมูลนี้มีประโยชน์สำหรับคู่ค้าเพื่อย้ายหรือโอนย้ายข้อมูลสำหรับการใช้งานค่าจ้างใหม่จากระบบอื่น"
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 93333757995c874c2cf03514acff28a54ae7f787
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="58687-104">ป้อนยอดดุลต้นงวดของค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="58687-104">Enter payroll beginning balances</span></span>

[!INCLUDE [banner](../../includes/banner.md)]

<span data-ttu-id="58687-105">หัวข้ออธิบายขั้นตอนสำหรับการป้อนยอดดุลต้นงวดสำหรับรหัสรายได้ การหักลด สวัสดิการ และภาษี</span><span class="sxs-lookup"><span data-stu-id="58687-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="58687-106">ข้อมูลนี้มีประโยชน์สำหรับคู่ค้า ผู้ซึ่งโอนย้ายข้อมูลสำหรับการใช้งานค่าจ้างใหม่จากระบบอื่น</span><span class="sxs-lookup"><span data-stu-id="58687-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="58687-107">ในการเตรียมป้อนยอดดุลค่าจ้างต้นงวด เราตรวจสอบข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="58687-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

> * <span data-ttu-id="58687-108">เรกคอร์ดพนักงานถูกป้อน และพร้อมใช้งานในระบบ</span><span class="sxs-lookup"><span data-stu-id="58687-108">Employee records are entered and available in the system</span></span>
> * <span data-ttu-id="58687-109">ข้อมูลต่อไปนี้ถูกตั้งค่า และมอบหมายให้แก่พนักงาน:</span><span class="sxs-lookup"><span data-stu-id="58687-109">The following data is set up and assigned to employees:</span></span>
> 
> > * <span data-ttu-id="58687-110">รอบการชำระค่าจ้างและรอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="58687-110">Pay cycles and pay periods</span></span>
> > * <span data-ttu-id="58687-111">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="58687-111">Earning codes</span></span>
> > * <span data-ttu-id="58687-112">ภาษี</span><span class="sxs-lookup"><span data-stu-id="58687-112">Taxes</span></span>
> > * <span data-ttu-id="58687-113">สวัสดิการและการหักลด</span><span class="sxs-lookup"><span data-stu-id="58687-113">Benefits and deductions</span></span>
> 
> * <span data-ttu-id="58687-114">บริษัทน่าจะเลือกวันซึ่งสามารถตั้งค่ายอดดุลต้นงวดเกี่ยวกับค่าจ้างได้</span><span class="sxs-lookup"><span data-stu-id="58687-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
> 
> * <span data-ttu-id="58687-115">ข้อมูลถูกรวบรวมในรายได้ทั้งหมด สวัสดิการ/การหักเงิน การจัดสรรสวัสดิการ ภาษีพนักงาน และภาษีนายจ้าง และยอดเงิน YTD ของพวกเขาจากระบบดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="58687-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="58687-116">เมื่อคุณวางแผนที่จะป้อนยอดดุลต้นงวด พิจารณาว่าความละเอียดข้อมูลต้องเป็นระดับใด</span><span class="sxs-lookup"><span data-stu-id="58687-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="58687-117">ธุรกิจส่วนใหญ่ป้อนยอดเดี่ยวที่รวมบัญชีตั้งแต่ต้นปีจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="58687-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="58687-118">อย่างไรก็ตาม ถ้าต้องการข้อมูลเพิ่มเติม ยอดดุลคุณสามารถป้อนในส่วนเพิ่มรายไตรมาส</span><span class="sxs-lookup"><span data-stu-id="58687-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="58687-119">การตัดสินใจระดับของรายละเอียดที่จำเป็น จะกำหนดจำนวนใบแจ้งยอดการชำระเงินด้วยตนเองต้องถูกสร้างขึ้นสำหรับแต่ละผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="58687-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="58687-120">สำหรับยอดเงินเดี่ยวตั้งแต่ต้นปีจนถึงปัจจุบัน จำเป็นต้องมีรายงานการเงินแบบกำหนดเองหนึ่งรายการเท่านั้นสำหรับพนักงานแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="58687-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="58687-121">เพื่อทำเช่นนี้ ใช้ยอดเงินตั้งแต่ต้นปีจนถึงปัจจุบันจากใบแจ้งยอดการชำระเงินสุดท้ายจากระบบก่อนหน้านี้ ให้เป็นยอดเงินที่ป้อนในระบบค่าจ้างใหม่</span><span class="sxs-lookup"><span data-stu-id="58687-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="58687-122">ตัวอย่างต่อไปนี้แสดงวิธีที่คุณสามารถป้อนยอดดุลเริ่มต้นของค่าจ้างของพนักงาน ซึ่งรวมถึงรหัสรายได้ สวัสดิการ/การหักเงิน และภาษี</span><span class="sxs-lookup"><span data-stu-id="58687-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="58687-123">ในตัวอย่างของโลกแห่งความเป็นจริง คุณจะต้องมีสินค้าในรายการสำหรับแต่ละรหัสรายได้ การหักลดสวัสดิการ การจ่ายเงินสมทบของสวัสดิการ ภาษีพนักงาน และภาษีนายจ้าง ที่มียอดเงินที่ป้อนเป็นยอดตั้งแต่ปีจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="58687-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="58687-124">โดยใช้รายการของรหัสและยอดเงิน ทำตามขั้นตอนสำหรับการสร้างรายได้แบบธรรมดา และใบแจ้งยอดการชำระค่าจ้าง ที่มีการบัญชีที่ปิดใช้งานเพื่อนำยอดดุลต้นงวดมาใช้เพื่อวัตถุประสงค์ของค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="58687-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span>  <span data-ttu-id="58687-125">คุณปิดการใช้งานการบัญชี เนื่องจากคุณไม่ต้องลงรายการบัญชีใบแจ้งยอดการชำระของยอดดุลนี้ไปยังบัญชีแยกประเภททั่วไปของคุณ</span><span class="sxs-lookup"><span data-stu-id="58687-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="58687-126">ที่ทำในระบบดั้งเดิม และจะใช้กับเกินไปยังระบบใหม่เมื่อคุณกำหนดยอดดุลต้นงวดในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="58687-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="58687-127">A.</span><span class="sxs-lookup"><span data-stu-id="58687-127">A.</span></span> <span data-ttu-id="58687-128">วิธีการตั้งค่ารหัสรายได้ที่จะใช้ในยอดดุลต้นงวดของค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="58687-128">How to set up earnings codes to be used on payroll beginning balances</span></span>
<span data-ttu-id="58687-129">เมื่อคุณป้อนยอดดุลต้นงวดของค่าจ้าง ให้แน่ใจว่ารหัสรายได้ที่คุณจะใช้ถูกตั้งค่าคอนฟิก ที่มีการเปิดใช้งานตัวเลือก "อนุญาตให้แก้ไขอัตราของใบแจ้งยอดรายได้"</span><span class="sxs-lookup"><span data-stu-id="58687-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="58687-130">ซึ่งจะทำให้คุณสามารถป้อนยอดเงินจากระบบเก่าด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="58687-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="58687-131">B.</span><span class="sxs-lookup"><span data-stu-id="58687-131">B.</span></span> <span data-ttu-id="58687-132">สร้างใบแจ้งยอดรายได้สำหรับพนักงานเพือให้มียอดดุลต้นงวด</span><span class="sxs-lookup"><span data-stu-id="58687-132">Create earnings statement for an employee to have a beginning balance</span></span>
<span data-ttu-id="58687-133">ขั้นตอนนี้สร้างใบแจ้งยอดรายได้สำหรับผู้ปฏิบัติงานแต่ละรายด้วยตนเอง สำหรับรอบระยะเวลาการชำระค่าจ้างสุดท้ายของระบบเก่า ซึ่งสร้างรายการใบแจ้งยอดรายได้ในระบบค่าจ้างใหม่</span><span class="sxs-lookup"><span data-stu-id="58687-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="58687-134">ป้อนหนึ่งรายการสำหรับแต่ละรหัสรายได้ และยอดเงิน YTD และชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="58687-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="58687-135">ขั้นตอนตัวอย่างมีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="58687-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="58687-136">เปิดหน้า **ใบแจ้งยอดรายได้ทั้งหมด** และคลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="58687-136">Open the **All earnings statements** page and click **New**.</span></span>  

<span data-ttu-id="58687-137">ป้อนข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="58687-137">Enter the following:</span></span> 

| <span data-ttu-id="58687-138">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="58687-138">Field</span></span>      | <span data-ttu-id="58687-139">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="58687-139">Value</span></span>                 |
|------------|-----------------------|
| <span data-ttu-id="58687-140">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="58687-140">Worker</span></span>     | <span data-ttu-id="58687-141">ไมเคิล เรดมอนด์</span><span class="sxs-lookup"><span data-stu-id="58687-141">Michael Redmond</span></span>       |
| <span data-ttu-id="58687-142">รอบการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="58687-142">Pay cycle</span></span>  | <span data-ttu-id="58687-143">sm</span><span class="sxs-lookup"><span data-stu-id="58687-143">sm</span></span>                    |
| <span data-ttu-id="58687-144">รอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="58687-144">Pay period</span></span> | <span data-ttu-id="58687-145">16/6/2560 - 30/6/2560</span><span class="sxs-lookup"><span data-stu-id="58687-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="58687-146">บนแท็บ **รายการใบแจ้งยอดรายได้** ให้ป้อนค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="58687-146">In the **Earnings statement line** tab, enter the following:</span></span>

<span data-ttu-id="58687-147">รายการที่ 1: แท็บ **รายการของใบแจ้งยอดรายได้**</span><span class="sxs-lookup"><span data-stu-id="58687-147">Line 1: **Earning statement line** tab</span></span>

| <span data-ttu-id="58687-148">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="58687-148">Field</span></span>            | <span data-ttu-id="58687-149">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="58687-149">Value</span></span>       |
|------------------|-------------|
| <span data-ttu-id="58687-150">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="58687-150">Earnings code</span></span>    | <span data-ttu-id="58687-151">การจ่ายค่าจ้างประจำ</span><span class="sxs-lookup"><span data-stu-id="58687-151">Regular pay</span></span> |
| <span data-ttu-id="58687-152">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="58687-152">Quantity</span></span>         | <span data-ttu-id="58687-153">1.00</span><span class="sxs-lookup"><span data-stu-id="58687-153">1.00</span></span>        |
| <span data-ttu-id="58687-154">เรจ</span><span class="sxs-lookup"><span data-stu-id="58687-154">Rage</span></span>             | <span data-ttu-id="58687-155">30,000</span><span class="sxs-lookup"><span data-stu-id="58687-155">30,000</span></span>      |
| <span data-ttu-id="58687-156">แท็บรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="58687-156">Line details tab</span></span> |             |
| <span data-ttu-id="58687-157">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="58687-157">Manual</span></span>           | <span data-ttu-id="58687-158">(ทำเครื่องหมาย)</span><span class="sxs-lookup"><span data-stu-id="58687-158">(marked)</span></span>    |

<span data-ttu-id="58687-159">รายการที่ 2: แท็บ **รายการของใบแจ้งยอดรายได้**</span><span class="sxs-lookup"><span data-stu-id="58687-159">Line 2: **Earning statement line** tab</span></span>

| <span data-ttu-id="58687-160">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="58687-160">Field</span></span>            | <span data-ttu-id="58687-161">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="58687-161">Value</span></span>    |
|------------------|----------|
| <span data-ttu-id="58687-162">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="58687-162">Earnings code</span></span>    | <span data-ttu-id="58687-163">โบนัส</span><span class="sxs-lookup"><span data-stu-id="58687-163">Bonus</span></span>    |
| <span data-ttu-id="58687-164">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="58687-164">Quantity</span></span>         | <span data-ttu-id="58687-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="58687-165">1.0000</span></span>   |
| <span data-ttu-id="58687-166">อัตรา</span><span class="sxs-lookup"><span data-stu-id="58687-166">Rate</span></span>             | <span data-ttu-id="58687-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="58687-167">4250.00</span></span>  |
| <span data-ttu-id="58687-168">แท็บรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="58687-168">Line details tab</span></span> |          |
| <span data-ttu-id="58687-169">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="58687-169">Manual</span></span>           | <span data-ttu-id="58687-170">(ทำเครื่องหมาย)</span><span class="sxs-lookup"><span data-stu-id="58687-170">(marked)</span></span> |

<span data-ttu-id="58687-171">รายการที่ 3: แท็บ **รายการของใบแจ้งยอดรายได้**</span><span class="sxs-lookup"><span data-stu-id="58687-171">Line 3: **Earning statement line** tab</span></span>

| <span data-ttu-id="58687-172">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="58687-172">Field</span></span>           | <span data-ttu-id="58687-173">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="58687-173">Value</span></span>      |
|-----------------|------------|
| <span data-ttu-id="58687-174">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="58687-174">Earnings code</span></span>   | <span data-ttu-id="58687-175">ค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="58687-175">Commission</span></span> |
| <span data-ttu-id="58687-176">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="58687-176">Quantity</span></span>        | <span data-ttu-id="58687-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="58687-177">1.0000</span></span>     |
| <span data-ttu-id="58687-178">อัตรา</span><span class="sxs-lookup"><span data-stu-id="58687-178">Rate</span></span>            | <span data-ttu-id="58687-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="58687-179">!,299.00</span></span>   |
| <span data-ttu-id="58687-180">อัตรา</span><span class="sxs-lookup"><span data-stu-id="58687-180">Rate</span></span>            | <span data-ttu-id="58687-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="58687-181">1,299.00</span></span>   |
| <span data-ttu-id="58687-182">แท็บรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="58687-182">Line detail tab</span></span> |            |
| <span data-ttu-id="58687-183">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="58687-183">Manual</span></span>          | <span data-ttu-id="58687-184">(ทำเครื่องหมาย)</span><span class="sxs-lookup"><span data-stu-id="58687-184">(Marked)</span></span>   |

> [!NOTE]
> <span data-ttu-id="58687-185">การตั้งค่าแถบเลื่อน **ด้วยตนเอง** เป็น **ใช่** บนแท็บ **รายละเอียดรายการ** สำหรับรายการใบแจ้งยอดรายได้แต่ละรายการ เป็นกุญแจในการทำให้ยอดดุลต้นงวดของค่าจ้างถูกป้อนสำหรับผู้ปฏิบัติงานแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="58687-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="58687-186">ในบานหน้าต่าง **การดำเนินการ** คลิก **นำใบแจ้งยอดรายได้ออก** USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="58687-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>

4. <span data-ttu-id="58687-187">ในคลิกบานหน้าต่าง **การดำเนินการ** คลิก **ใบแจ้งยอดการชำระ** เพื่อเปิดหน้า **สร้างใบแจ้งยอดการชำระ** และตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="58687-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

| <span data-ttu-id="58687-188">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="58687-188">Field</span></span>              | <span data-ttu-id="58687-189">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="58687-189">Value</span></span>     |
|--------------------|-----------|
| <span data-ttu-id="58687-190">วันที่ชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="58687-190">Payment date</span></span>       | <span data-ttu-id="58687-191">วันที่ 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="58687-191">6/30/2017</span></span> |
| <span data-ttu-id="58687-192">ชนิดการดำเนินการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="58687-192">Payment run type</span></span>   | <span data-ttu-id="58687-193">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="58687-193">Manual</span></span>    |
| <span data-ttu-id="58687-194">ปิดใช้งานการบัญชี</span><span class="sxs-lookup"><span data-stu-id="58687-194">Disable accounting</span></span> |   <span data-ttu-id="58687-195">ใช่</span><span class="sxs-lookup"><span data-stu-id="58687-195">Yes</span></span>     |

> [!NOTE] 
> <span data-ttu-id="58687-196">นี่พร้อมใช้งานเฉพาะเมื่อชนิดการดำเนินการชำระเงินเป็นแบบกำหนดเอง และที่ซึ่งผู้ใช้ต้องการปิดใช้งานการบัญชีในการดำเนินการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="58687-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

<span data-ttu-id="58687-197">คลิก **ตกลง** และปิด **Infolog**</span><span class="sxs-lookup"><span data-stu-id="58687-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="58687-198">ทำไมแถบเลื่อนการปิดใช้งานการบัญชีจำเป็นต้องถูกตั้งค่าเป็นใช่ เมื่อสร้างใบแจ้งยอดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="58687-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>
<span data-ttu-id="58687-199">การตั้งค่าแถบเลื่อนเป็น **ใช่** ป้องกันไม่ให้รายการใด ๆ ในใบแจ้งยอดการชำระเงินจากการถูกกระจายไปที่บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="58687-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="58687-200">ยอดเงินบัญชีแยกประเภททั่วไปถูกอัพเดตก่อนหน้านั้นเมื่อการมีป้อนยอดดุลบัญชีจากระบบดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="58687-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="58687-201">การป้อนยอดดุลต้นงวดสำหรับค่าจ้างช่วยให้คุณสามารถสร้างรายงานที่รวมข้อมูลจากปีก่อนหน้า รวมทั้งเพื่อการระบุขีดจำกัดสำหรับวัตถุประสงค์ด้านสวัสดิการและภาษี</span><span class="sxs-lookup"><span data-stu-id="58687-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>   

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="58687-202">C.</span><span class="sxs-lookup"><span data-stu-id="58687-202">C.</span></span> <span data-ttu-id="58687-203">สร้างใบแจ้งยอดชำระเงินสำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="58687-203">Create pay statements for employees</span></span>
<span data-ttu-id="58687-204">หลังจากที่คุณสร้างใบแจ้งยอดการชำระเงินที่มียอดดุลต้นงวด คุณต้องตรวจสอบว่าใบแจ้งยอดการชำระเงินสะท้อนถึงข้อมูลค่าจ้างได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="58687-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="58687-205">คุณต้องอัพเดตข้อมูลสวัสดิการและภาษีให้ตรงกับค่าในระบบค่าจ้างก่อนหน้านี้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="58687-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="58687-206">หลังจากที่คุณตรวจสอบว่า จำนวนเงินจากระบบค่าจ้างก่อนหน้าตรงกับยอดเงินในใบแจ้งยอดการชำระเงินปัจจุบันแล้ว คุณต้องสรุปใบแจ้งยอดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="58687-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="58687-207">เปิดหน้า **ใบแจ้งยอดการชำระเงินทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="58687-207">Open the **All pay statements** page.</span></span>

2. <span data-ttu-id="58687-208">เน้นใบแจ้งยอดการชำระเงินที่สร้างขึ้นล่าสุดสำหรับไมเคิล เรดมอนด์</span><span class="sxs-lookup"><span data-stu-id="58687-208">Highlight the last generated pay statement for Michael Redmond</span></span>

3. <span data-ttu-id="58687-209">คลิก **แก้ไข** เพื่อเปิดหน้า **ใบแจ้งยอดการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="58687-209">Click **Edit** to open the **Pay statement** page.</span></span>

4. <span data-ttu-id="58687-210">เปิดแท็บ **การหักลดสวัสดิการ** และป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="58687-210">Open the **Benefit deductions** tab and enter the following:</span></span>

|       <span data-ttu-id="58687-211">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="58687-211">Field</span></span>       |      <span data-ttu-id="58687-212">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="58687-212">Value</span></span>       |
|-------------------|------------------|
|      <span data-ttu-id="58687-213">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="58687-213">Benefit</span></span>      | <span data-ttu-id="58687-214">ยอดการหักลด</span><span class="sxs-lookup"><span data-stu-id="58687-214">Deduction amount</span></span> |
|       <span data-ttu-id="58687-215">401K</span><span class="sxs-lookup"><span data-stu-id="58687-215">401K</span></span>        |   <span data-ttu-id="58687-216">เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="58687-216">Participate</span></span>    |
|      <span data-ttu-id="58687-217">ทันตกรรม</span><span class="sxs-lookup"><span data-stu-id="58687-217">Dental</span></span>       |      <span data-ttu-id="58687-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="58687-218">SubSp</span></span>       |
| <span data-ttu-id="58687-219">การใช้จ่ายในดูแลเชิงลึก</span><span class="sxs-lookup"><span data-stu-id="58687-219">Dep care spending</span></span> |   <span data-ttu-id="58687-220">เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="58687-220">Participate</span></span>    |
|      <span data-ttu-id="58687-221">ระยะการมองเห็น</span><span class="sxs-lookup"><span data-stu-id="58687-221">Vision</span></span>       |      <span data-ttu-id="58687-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="58687-222">SupSp</span></span>       |

5. <span data-ttu-id="58687-223">ในแท็บ **การจ่ายเงินสมทบของสวัสดิการ** และป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="58687-223">In the **Benefit contributions** tab and enter the following:</span></span>

|  <span data-ttu-id="58687-224">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="58687-224">Field</span></span>  |        <span data-ttu-id="58687-225">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="58687-225">Value</span></span>        |
|---------|---------------------|
| <span data-ttu-id="58687-226">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="58687-226">Benefit</span></span> | <span data-ttu-id="58687-227">ยอดการจ่ายเงินสมทบ</span><span class="sxs-lookup"><span data-stu-id="58687-227">Contribution amount</span></span> |
|  <span data-ttu-id="58687-228">401K</span><span class="sxs-lookup"><span data-stu-id="58687-228">401K</span></span>   |     <span data-ttu-id="58687-229">เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="58687-229">Participate</span></span>     |
| <span data-ttu-id="58687-230">ทันตกรรม</span><span class="sxs-lookup"><span data-stu-id="58687-230">Dental</span></span>  |        <span data-ttu-id="58687-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="58687-231">SubSp</span></span>        |
| <span data-ttu-id="58687-232">ระยะการมองเห็น</span><span class="sxs-lookup"><span data-stu-id="58687-232">Vision</span></span>  |        <span data-ttu-id="58687-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="58687-233">SubSp</span></span>        |

6. <span data-ttu-id="58687-234">ในแท็บ **การหักลดภาษี** ป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="58687-234">In the **Tax deductions** tab, enter the following:</span></span>

| <span data-ttu-id="58687-235">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="58687-235">Field</span></span>           | <span data-ttu-id="58687-236">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="58687-236">Value</span></span>            |
|-----------------|------------------|
| <span data-ttu-id="58687-237">รหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="58687-237">Tax code</span></span>        | <span data-ttu-id="58687-238">ยอดการหักลด</span><span class="sxs-lookup"><span data-stu-id="58687-238">Deduction amount</span></span> |
| <span data-ttu-id="58687-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="58687-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="58687-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="58687-240">1600.00</span></span>          |
| <span data-ttu-id="58687-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="58687-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="58687-242">825.75</span><span class="sxs-lookup"><span data-stu-id="58687-242">825.75</span></span>           |

7. <span data-ttu-id="58687-243">ในแท็บ **การจ่ายเงินสมทบภาษี** ป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="58687-243">In the **Tax contributions** tab enter the following:</span></span>

8. <span data-ttu-id="58687-244">คลิก **คำนวณ**</span><span class="sxs-lookup"><span data-stu-id="58687-244">Click **Calculate**.</span></span>
   > [!IMPORTANT] 
   > <span data-ttu-id="58687-245">ตรวจสอบผลรวมของใบแจ้งยอดค่าจ้างว่าตรงกับ YTD ของระบบแบบดั้งเดิมสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="58687-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="58687-246">คุณอาจต้องรอการดำเนินการขั้นสุดท้ายในขั้นตอนถัดไป เพื่อทำการตรวจสอบบางอย่างโดยรวมของใบแจ้งยอดการชำระค่าจ้างทั้งหมดในการรวม</span><span class="sxs-lookup"><span data-stu-id="58687-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="58687-247">เมื่อตรวจสอบแล้ว รันใบแจ้งยอดการชำระค่าจ้างทั้งหมด และดำเนินการขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="58687-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="58687-248">กระบวนการเดิมสามารถทำได้ในการเพิ่มรายไตรมาส ถ้าจำเป็นสำหรับไตรมาสก่อนหน้านี้ทั้งหมดในแต่ละปี</span><span class="sxs-lookup"><span data-stu-id="58687-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="58687-249">สิ่งนี้จำเป็นก็ต่อเมื่อลูกค้าต้องการดูข้อมูลตามไตรมาสโดยไม่กลับไปยังระบบแบบดั้งเดิมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="58687-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="58687-250">ถ้าคุณทำผิดพลาดในการป้อนยอดดุลต้นงวดสำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="58687-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>
<span data-ttu-id="58687-251">สามารถย้อนกลับ และป้อนธุรกรรมใหม่อีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="58687-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="58687-252">เพื่อย้อนกลับรายการธุรกรรม คุณเพียงต้องดำเนินการตามขั้นตอนในหน้า **ใบแจ้งยอดการชำระค่าจ้างทั้งหมด** ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="58687-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="58687-253">คลิก **ย้อนกลับ**</span><span class="sxs-lookup"><span data-stu-id="58687-253">Click **Reverse**.</span></span>

2. <span data-ttu-id="58687-254">คลิก **ใช่** เมื่อข้อความ "เมื่อคุณกลับรายการใบแจ้งยอดการชำระเงินนี้ ใบแจ้งยอดการชำระเงินกลับบัญชีจะถูกสร้างเพื่อออฟเซ็ตใบแจ้งยอดการชำระค่าจ้างนี้</span><span class="sxs-lookup"><span data-stu-id="58687-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="58687-255">ใบแจ้งยอดค่าจ้างไม่สามารถถูกแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="58687-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="58687-256">คุณต้องการกลับรายการใบแจ้งยอดการชำระค่าจ้างนี้หรือไม่"</span><span class="sxs-lookup"><span data-stu-id="58687-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="58687-257">การแสดง</span><span class="sxs-lookup"><span data-stu-id="58687-257">displays.</span></span> 

<span data-ttu-id="58687-258">หลังจากที่คุณกลับรายการใบแจ้งยอดค่าจ้าง คุณสามารถสร้างใบแจ้งยอดการชำระค่าจ้างใหม่สำหรับผู้ปฏิบัติงานจากใบแจ้งยอดรายได้ที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="58687-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="58687-259">ตรวจสอบให้แน่ใจว่าได้ทำการแก้ไขบรรทัดที่ไม่ถูกต้องในใบแจ้งยอดรายได้ก่อนที่คุณจะสร้างใบแจ้งยอดค่าจ้างใหม่ จากนั้นให้สร้างใบแจ้งยอดค่าจ้างใหม่ที่มียอดเงินที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="58687-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 

