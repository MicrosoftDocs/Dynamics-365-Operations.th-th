---
title: ป้อนยอดดุลต้นงวดของค่าจ้าง
description: หัวข้ออธิบายขั้นตอนสำหรับการป้อนยอดดุลต้นงวดสำหรับรหัสรายได้ การหักลด สวัสดิการ และภาษี
author: andreabichsel
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9272828fe5d6e0bf131ea66353a0d5c3c7b1c4bd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752161"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="835f8-103">ป้อนยอดดุลต้นงวดของค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="835f8-103">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="835f8-104">หัวข้ออธิบายขั้นตอนสำหรับการป้อนยอดดุลต้นงวดสำหรับรหัสรายได้ การหักลด สวัสดิการ และภาษี</span><span class="sxs-lookup"><span data-stu-id="835f8-104">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="835f8-105">ข้อมูลนี้มีประโยชน์สำหรับคู่ค้า ผู้ซึ่งโอนย้ายข้อมูลสำหรับการใช้งานค่าจ้างใหม่จากระบบอื่น</span><span class="sxs-lookup"><span data-stu-id="835f8-105">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="835f8-106">ในการเตรียมป้อนยอดดุลค่าจ้างต้นงวด เราตรวจสอบข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="835f8-106">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="835f8-107">เรกคอร์ดพนักงานถูกป้อน และพร้อมใช้งานในระบบ</span><span class="sxs-lookup"><span data-stu-id="835f8-107">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="835f8-108">ข้อมูลต่อไปนี้ถูกตั้งค่า และมอบหมายให้แก่พนักงาน:</span><span class="sxs-lookup"><span data-stu-id="835f8-108">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="835f8-109">รอบการชำระค่าจ้างและรอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="835f8-109">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="835f8-110">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="835f8-110">Earning codes</span></span>
    - <span data-ttu-id="835f8-111">ภาษี</span><span class="sxs-lookup"><span data-stu-id="835f8-111">Taxes</span></span>
    - <span data-ttu-id="835f8-112">สวัสดิการและการหักลด</span><span class="sxs-lookup"><span data-stu-id="835f8-112">Benefits and deductions</span></span>

- <span data-ttu-id="835f8-113">บริษัทน่าจะเลือกวันซึ่งสามารถตั้งค่ายอดดุลต้นงวดเกี่ยวกับค่าจ้างได้</span><span class="sxs-lookup"><span data-stu-id="835f8-113">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="835f8-114">ข้อมูลถูกรวบรวมในรายได้ทั้งหมด สวัสดิการ/การหักเงิน การจัดสรรสวัสดิการ ภาษีพนักงาน และภาษีนายจ้าง และยอดเงิน YTD ของพวกเขาจากระบบดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="835f8-114">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="835f8-115">เมื่อคุณวางแผนที่จะป้อนยอดดุลต้นงวด พิจารณาว่าความละเอียดข้อมูลต้องเป็นระดับใด</span><span class="sxs-lookup"><span data-stu-id="835f8-115">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="835f8-116">ธุรกิจส่วนใหญ่ป้อนยอดเดี่ยวที่รวมบัญชีตั้งแต่ต้นปีจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="835f8-116">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="835f8-117">อย่างไรก็ตาม ถ้าต้องการข้อมูลเพิ่มเติม ยอดดุลคุณสามารถป้อนในส่วนเพิ่มรายไตรมาส</span><span class="sxs-lookup"><span data-stu-id="835f8-117">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="835f8-118">การตัดสินใจระดับของรายละเอียดที่จำเป็น จะกำหนดจำนวนใบแจ้งยอดการชำระเงินด้วยตนเองต้องถูกสร้างขึ้นสำหรับแต่ละผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="835f8-118">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="835f8-119">สำหรับยอดเงินเดี่ยวตั้งแต่ต้นปีจนถึงปัจจุบัน จำเป็นต้องมีรายงานการเงินแบบกำหนดเองหนึ่งรายการเท่านั้นสำหรับพนักงานแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="835f8-119">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="835f8-120">เพื่อทำเช่นนี้ ใช้ยอดเงินตั้งแต่ต้นปีจนถึงปัจจุบันจากใบแจ้งยอดการชำระเงินสุดท้ายจากระบบก่อนหน้านี้ ให้เป็นยอดเงินที่ป้อนในระบบค่าจ้างใหม่</span><span class="sxs-lookup"><span data-stu-id="835f8-120">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="835f8-121">ตัวอย่างต่อไปนี้แสดงวิธีที่คุณสามารถป้อนยอดดุลเริ่มต้นของค่าจ้างของพนักงาน ซึ่งรวมถึงรหัสรายได้ สวัสดิการ/การหักเงิน และภาษี</span><span class="sxs-lookup"><span data-stu-id="835f8-121">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="835f8-122">ในตัวอย่างของโลกแห่งความเป็นจริง คุณจะต้องมีสินค้าในรายการสำหรับแต่ละรหัสรายได้ การหักลดสวัสดิการ การจ่ายเงินสมทบของสวัสดิการ ภาษีพนักงาน และภาษีนายจ้าง ที่มียอดเงินที่ป้อนเป็นยอดตั้งแต่ปีจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="835f8-122">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="835f8-123">โดยใช้รายการของรหัสและยอดเงิน ทำตามขั้นตอนสำหรับการสร้างรายได้แบบธรรมดา และใบแจ้งยอดการชำระค่าจ้าง ที่มีการบัญชีที่ปิดใช้งานเพื่อนำยอดดุลต้นงวดมาใช้เพื่อวัตถุประสงค์ของค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="835f8-123">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="835f8-124">คุณปิดการใช้งานการบัญชี เนื่องจากคุณไม่ต้องลงรายการบัญชีใบแจ้งยอดการชำระของยอดดุลนี้ไปยังบัญชีแยกประเภททั่วไปของคุณ</span><span class="sxs-lookup"><span data-stu-id="835f8-124">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="835f8-125">ที่ทำในระบบดั้งเดิม และจะใช้กับเกินไปยังระบบใหม่เมื่อคุณกำหนดยอดดุลต้นงวดในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="835f8-125">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="835f8-126">A.</span><span class="sxs-lookup"><span data-stu-id="835f8-126">A.</span></span> <span data-ttu-id="835f8-127">วิธีการตั้งค่ารหัสรายได้ที่จะใช้ในยอดดุลต้นงวดของค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="835f8-127">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="835f8-128">เมื่อคุณป้อนยอดดุลต้นงวดของค่าจ้าง ให้แน่ใจว่ารหัสรายได้ที่คุณจะใช้ถูกตั้งค่าคอนฟิก ที่มีการเปิดใช้งานตัวเลือก "อนุญาตให้แก้ไขอัตราของใบแจ้งยอดรายได้"</span><span class="sxs-lookup"><span data-stu-id="835f8-128">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="835f8-129">ซึ่งจะทำให้คุณสามารถป้อนยอดเงินจากระบบเก่าด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="835f8-129">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="835f8-130">B.</span><span class="sxs-lookup"><span data-stu-id="835f8-130">B.</span></span> <span data-ttu-id="835f8-131">สร้างใบแจ้งยอดรายได้สำหรับพนักงานเพือให้มียอดดุลต้นงวด</span><span class="sxs-lookup"><span data-stu-id="835f8-131">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="835f8-132">ขั้นตอนนี้สร้างใบแจ้งยอดรายได้สำหรับผู้ปฏิบัติงานแต่ละรายด้วยตนเอง สำหรับรอบระยะเวลาการชำระค่าจ้างสุดท้ายของระบบเก่า ซึ่งสร้างรายการใบแจ้งยอดรายได้ในระบบค่าจ้างใหม่</span><span class="sxs-lookup"><span data-stu-id="835f8-132">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="835f8-133">ป้อนหนึ่งรายการสำหรับแต่ละรหัสรายได้ และยอดเงิน YTD และชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="835f8-133">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="835f8-134">ขั้นตอนตัวอย่างมีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="835f8-134">The sample steps are as follows:</span></span>

1. <span data-ttu-id="835f8-135">เปิดหน้า **ใบแจ้งยอดรายได้ทั้งหมด** และคลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="835f8-135">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="835f8-136">ป้อนข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="835f8-136">Enter the following:</span></span> 

    | <span data-ttu-id="835f8-137">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="835f8-137">Field</span></span>      | <span data-ttu-id="835f8-138">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="835f8-138">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="835f8-139">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="835f8-139">Worker</span></span>     | <span data-ttu-id="835f8-140">ไมเคิล เรดมอนด์</span><span class="sxs-lookup"><span data-stu-id="835f8-140">Michael Redmond</span></span>       |
    | <span data-ttu-id="835f8-141">รอบการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="835f8-141">Pay cycle</span></span>  | <span data-ttu-id="835f8-142">sm</span><span class="sxs-lookup"><span data-stu-id="835f8-142">sm</span></span>                    |
    | <span data-ttu-id="835f8-143">รอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="835f8-143">Pay period</span></span> | <span data-ttu-id="835f8-144">16/6/2560 - 30/6/2560</span><span class="sxs-lookup"><span data-stu-id="835f8-144">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="835f8-145">บนแท็บ **รายการใบแจ้งยอดรายได้** ให้ป้อนค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="835f8-145">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="835f8-146">รายการที่ 1: แท็บ **รายการของใบแจ้งยอดรายได้**</span><span class="sxs-lookup"><span data-stu-id="835f8-146">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="835f8-147">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="835f8-147">Field</span></span>            | <span data-ttu-id="835f8-148">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="835f8-148">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="835f8-149">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="835f8-149">Earnings code</span></span>    | <span data-ttu-id="835f8-150">การจ่ายค่าจ้างประจำ</span><span class="sxs-lookup"><span data-stu-id="835f8-150">Regular pay</span></span> |
    | <span data-ttu-id="835f8-151">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="835f8-151">Quantity</span></span>         | <span data-ttu-id="835f8-152">1.00</span><span class="sxs-lookup"><span data-stu-id="835f8-152">1.00</span></span>        |
    | <span data-ttu-id="835f8-153">อัตรา</span><span class="sxs-lookup"><span data-stu-id="835f8-153">Rate</span></span>             | <span data-ttu-id="835f8-154">30,000</span><span class="sxs-lookup"><span data-stu-id="835f8-154">30,000</span></span>      |
    | <span data-ttu-id="835f8-155">แท็บรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="835f8-155">Line details tab</span></span> |             |
    | <span data-ttu-id="835f8-156">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="835f8-156">Manual</span></span>           | <span data-ttu-id="835f8-157">(ทำเครื่องหมาย)</span><span class="sxs-lookup"><span data-stu-id="835f8-157">(marked)</span></span>    |

    <span data-ttu-id="835f8-158">รายการที่ 2: แท็บ **รายการของใบแจ้งยอดรายได้**</span><span class="sxs-lookup"><span data-stu-id="835f8-158">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="835f8-159">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="835f8-159">Field</span></span>            | <span data-ttu-id="835f8-160">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="835f8-160">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="835f8-161">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="835f8-161">Earnings code</span></span>    | <span data-ttu-id="835f8-162">โบนัส</span><span class="sxs-lookup"><span data-stu-id="835f8-162">Bonus</span></span>    |
    | <span data-ttu-id="835f8-163">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="835f8-163">Quantity</span></span>         | <span data-ttu-id="835f8-164">1.0000</span><span class="sxs-lookup"><span data-stu-id="835f8-164">1.0000</span></span>   |
    | <span data-ttu-id="835f8-165">อัตรา</span><span class="sxs-lookup"><span data-stu-id="835f8-165">Rate</span></span>             | <span data-ttu-id="835f8-166">4250.00</span><span class="sxs-lookup"><span data-stu-id="835f8-166">4250.00</span></span>  |
    | <span data-ttu-id="835f8-167">แท็บรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="835f8-167">Line details tab</span></span> |          |
    | <span data-ttu-id="835f8-168">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="835f8-168">Manual</span></span>           | <span data-ttu-id="835f8-169">(ทำเครื่องหมาย)</span><span class="sxs-lookup"><span data-stu-id="835f8-169">(marked)</span></span> |

    <span data-ttu-id="835f8-170">รายการที่ 3: แท็บ **รายการของใบแจ้งยอดรายได้**</span><span class="sxs-lookup"><span data-stu-id="835f8-170">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="835f8-171">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="835f8-171">Field</span></span>           | <span data-ttu-id="835f8-172">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="835f8-172">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="835f8-173">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="835f8-173">Earnings code</span></span>   | <span data-ttu-id="835f8-174">ค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="835f8-174">Commission</span></span> |
    | <span data-ttu-id="835f8-175">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="835f8-175">Quantity</span></span>        | <span data-ttu-id="835f8-176">1.0000</span><span class="sxs-lookup"><span data-stu-id="835f8-176">1.0000</span></span>     |
    | <span data-ttu-id="835f8-177">อัตรา</span><span class="sxs-lookup"><span data-stu-id="835f8-177">Rate</span></span>            | <span data-ttu-id="835f8-178">!,299.00</span><span class="sxs-lookup"><span data-stu-id="835f8-178">!,299.00</span></span>   |
    | <span data-ttu-id="835f8-179">อัตรา</span><span class="sxs-lookup"><span data-stu-id="835f8-179">Rate</span></span>            | <span data-ttu-id="835f8-180">1,299.00</span><span class="sxs-lookup"><span data-stu-id="835f8-180">1,299.00</span></span>   |
    | <span data-ttu-id="835f8-181">แท็บรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="835f8-181">Line detail tab</span></span> |            |
    | <span data-ttu-id="835f8-182">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="835f8-182">Manual</span></span>          | <span data-ttu-id="835f8-183">(ทำเครื่องหมาย)</span><span class="sxs-lookup"><span data-stu-id="835f8-183">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="835f8-184">การตั้งค่าแถบเลื่อน **ด้วยตนเอง** เป็น **ใช่** บนแท็บ **รายละเอียดรายการ** สำหรับรายการใบแจ้งยอดรายได้แต่ละรายการ เป็นกุญแจในการทำให้ยอดดุลต้นงวดของค่าจ้างถูกป้อนสำหรับผู้ปฏิบัติงานแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="835f8-184">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="835f8-185">ในบานหน้าต่าง **การดำเนินการ** คลิก **นำใบแจ้งยอดรายได้ออก** USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="835f8-185">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="835f8-186">ในคลิกบานหน้าต่าง **การดำเนินการ** คลิก **ใบแจ้งยอดการชำระ** เพื่อเปิดหน้า **สร้างใบแจ้งยอดการชำระ** และตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="835f8-186">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="835f8-187">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="835f8-187">Field</span></span>              | <span data-ttu-id="835f8-188">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="835f8-188">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="835f8-189">วันที่ชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="835f8-189">Payment date</span></span>       | <span data-ttu-id="835f8-190">วันที่ 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="835f8-190">6/30/2017</span></span> |
    | <span data-ttu-id="835f8-191">ชนิดการดำเนินการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="835f8-191">Payment run type</span></span>   | <span data-ttu-id="835f8-192">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="835f8-192">Manual</span></span>    |
    | <span data-ttu-id="835f8-193">ปิดใช้งานการบัญชี</span><span class="sxs-lookup"><span data-stu-id="835f8-193">Disable accounting</span></span> |   <span data-ttu-id="835f8-194">ใช่</span><span class="sxs-lookup"><span data-stu-id="835f8-194">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="835f8-195">นี่พร้อมใช้งานเฉพาะเมื่อชนิดการดำเนินการชำระเงินเป็นแบบกำหนดเอง และที่ซึ่งผู้ใช้ต้องการปิดใช้งานการบัญชีในการดำเนินการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="835f8-195">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="835f8-196">คลิก **ตกลง** และปิด **Infolog**</span><span class="sxs-lookup"><span data-stu-id="835f8-196">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="835f8-197">ทำไมแถบเลื่อนการปิดใช้งานการบัญชีจำเป็นต้องถูกตั้งค่าเป็นใช่ เมื่อสร้างใบแจ้งยอดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="835f8-197">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="835f8-198">การตั้งค่าแถบเลื่อนเป็น **ใช่** ป้องกันไม่ให้รายการใด ๆ ในใบแจ้งยอดการชำระเงินจากการถูกกระจายไปที่บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="835f8-198">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="835f8-199">ยอดเงินบัญชีแยกประเภททั่วไปถูกอัพเดตก่อนหน้านั้นเมื่อการมีป้อนยอดดุลบัญชีจากระบบดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="835f8-199">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="835f8-200">การป้อนยอดดุลต้นงวดสำหรับค่าจ้างช่วยให้คุณสามารถสร้างรายงานที่รวมข้อมูลจากปีก่อนหน้า รวมทั้งเพื่อการระบุขีดจำกัดสำหรับวัตถุประสงค์ด้านสวัสดิการและภาษี</span><span class="sxs-lookup"><span data-stu-id="835f8-200">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="835f8-201">C.</span><span class="sxs-lookup"><span data-stu-id="835f8-201">C.</span></span> <span data-ttu-id="835f8-202">สร้างใบแจ้งยอดชำระเงินสำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="835f8-202">Create pay statements for employees</span></span>

<span data-ttu-id="835f8-203">หลังจากที่คุณสร้างใบแจ้งยอดการชำระเงินที่มียอดดุลต้นงวด คุณต้องตรวจสอบว่าใบแจ้งยอดการชำระเงินสะท้อนถึงข้อมูลค่าจ้างได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="835f8-203">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="835f8-204">คุณต้องอัพเดตข้อมูลสวัสดิการและภาษีให้ตรงกับค่าในระบบค่าจ้างก่อนหน้านี้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="835f8-204">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="835f8-205">หลังจากที่คุณตรวจสอบว่า จำนวนเงินจากระบบค่าจ้างก่อนหน้าตรงกับยอดเงินในใบแจ้งยอดการชำระเงินปัจจุบันแล้ว คุณต้องสรุปใบแจ้งยอดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="835f8-205">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="835f8-206">เปิดหน้า **ใบแจ้งยอดการชำระเงินทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="835f8-206">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="835f8-207">เน้นใบแจ้งยอดการชำระเงินที่สร้างขึ้นล่าสุดสำหรับไมเคิล เรดมอนด์</span><span class="sxs-lookup"><span data-stu-id="835f8-207">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="835f8-208">คลิก **แก้ไข** เพื่อเปิดหน้า **ใบแจ้งยอดการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="835f8-208">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="835f8-209">เปิดแท็บ **การหักลดสวัสดิการ** และป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="835f8-209">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="835f8-210">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="835f8-210">Field</span></span>             | <span data-ttu-id="835f8-211">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="835f8-211">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="835f8-212">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="835f8-212">Benefit</span></span>           | <span data-ttu-id="835f8-213">ยอดการหักลด</span><span class="sxs-lookup"><span data-stu-id="835f8-213">Deduction amount</span></span> |
    | <span data-ttu-id="835f8-214">401K</span><span class="sxs-lookup"><span data-stu-id="835f8-214">401K</span></span>              | <span data-ttu-id="835f8-215">เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="835f8-215">Participate</span></span>      |
    | <span data-ttu-id="835f8-216">ทันตกรรม</span><span class="sxs-lookup"><span data-stu-id="835f8-216">Dental</span></span>            | <span data-ttu-id="835f8-217">SubSp</span><span class="sxs-lookup"><span data-stu-id="835f8-217">SubSp</span></span>            |
    | <span data-ttu-id="835f8-218">การใช้จ่ายในดูแลเชิงลึก</span><span class="sxs-lookup"><span data-stu-id="835f8-218">Dep care spending</span></span> | <span data-ttu-id="835f8-219">เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="835f8-219">Participate</span></span>      |
    | <span data-ttu-id="835f8-220">ระยะการมองเห็น</span><span class="sxs-lookup"><span data-stu-id="835f8-220">Vision</span></span>            | <span data-ttu-id="835f8-221">SupSp</span><span class="sxs-lookup"><span data-stu-id="835f8-221">SupSp</span></span>            |

5. <span data-ttu-id="835f8-222">ในแท็บ **การจ่ายเงินสมทบของสวัสดิการ** และป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="835f8-222">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="835f8-223">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="835f8-223">Field</span></span>   | <span data-ttu-id="835f8-224">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="835f8-224">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="835f8-225">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="835f8-225">Benefit</span></span> | <span data-ttu-id="835f8-226">ยอดการจ่ายเงินสมทบ</span><span class="sxs-lookup"><span data-stu-id="835f8-226">Contribution amount</span></span> |
    | <span data-ttu-id="835f8-227">401K</span><span class="sxs-lookup"><span data-stu-id="835f8-227">401K</span></span>    | <span data-ttu-id="835f8-228">เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="835f8-228">Participate</span></span>         |
    | <span data-ttu-id="835f8-229">ทันตกรรม</span><span class="sxs-lookup"><span data-stu-id="835f8-229">Dental</span></span>  | <span data-ttu-id="835f8-230">SubSp</span><span class="sxs-lookup"><span data-stu-id="835f8-230">SubSp</span></span>               |
    | <span data-ttu-id="835f8-231">ระยะการมองเห็น</span><span class="sxs-lookup"><span data-stu-id="835f8-231">Vision</span></span>  | <span data-ttu-id="835f8-232">SubSp</span><span class="sxs-lookup"><span data-stu-id="835f8-232">SubSp</span></span>               |

6. <span data-ttu-id="835f8-233">ในแท็บ **การหักลดภาษี** ป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="835f8-233">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="835f8-234">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="835f8-234">Field</span></span>           | <span data-ttu-id="835f8-235">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="835f8-235">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="835f8-236">รหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="835f8-236">Tax code</span></span>        | <span data-ttu-id="835f8-237">ยอดการหักลด</span><span class="sxs-lookup"><span data-stu-id="835f8-237">Deduction amount</span></span> |
    | <span data-ttu-id="835f8-238">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="835f8-238">USA-FED-ER-FICA</span></span> | <span data-ttu-id="835f8-239">1600.00</span><span class="sxs-lookup"><span data-stu-id="835f8-239">1600.00</span></span>          |
    | <span data-ttu-id="835f8-240">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="835f8-240">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="835f8-241">825.75</span><span class="sxs-lookup"><span data-stu-id="835f8-241">825.75</span></span>           |

7. <span data-ttu-id="835f8-242">ในแท็บ **การจ่ายเงินสมทบภาษี** ป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="835f8-242">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="835f8-243">คลิก **คำนวณ**</span><span class="sxs-lookup"><span data-stu-id="835f8-243">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="835f8-244">ตรวจสอบผลรวมของใบแจ้งยอดค่าจ้างว่าตรงกับ YTD ของระบบแบบดั้งเดิมสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="835f8-244">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="835f8-245">คุณอาจต้องรอการดำเนินการขั้นสุดท้ายในขั้นตอนถัดไป เพื่อทำการตรวจสอบบางอย่างโดยรวมของใบแจ้งยอดการชำระค่าจ้างทั้งหมดในการรวม</span><span class="sxs-lookup"><span data-stu-id="835f8-245">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="835f8-246">เมื่อตรวจสอบแล้ว รันใบแจ้งยอดการชำระค่าจ้างทั้งหมด และดำเนินการขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="835f8-246">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="835f8-247">กระบวนการเดิมสามารถทำได้ในการเพิ่มรายไตรมาส ถ้าจำเป็นสำหรับไตรมาสก่อนหน้านี้ทั้งหมดในแต่ละปี</span><span class="sxs-lookup"><span data-stu-id="835f8-247">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="835f8-248">สิ่งนี้จำเป็นก็ต่อเมื่อลูกค้าต้องการดูข้อมูลตามไตรมาสโดยไม่กลับไปยังระบบแบบดั้งเดิมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="835f8-248">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="835f8-249">ถ้าคุณทำผิดพลาดในการป้อนยอดดุลต้นงวดสำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="835f8-249">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="835f8-250">สามารถย้อนกลับ และป้อนธุรกรรมใหม่อีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="835f8-250">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="835f8-251">เพื่อย้อนกลับรายการธุรกรรม คุณเพียงต้องดำเนินการตามขั้นตอนในหน้า **ใบแจ้งยอดการชำระค่าจ้างทั้งหมด** ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="835f8-251">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="835f8-252">คลิก **ย้อนกลับ**</span><span class="sxs-lookup"><span data-stu-id="835f8-252">Click **Reverse**.</span></span>
2. <span data-ttu-id="835f8-253">คลิก **ใช่** เมื่อข้อความ "เมื่อคุณกลับรายการใบแจ้งยอดการชำระเงินนี้ ใบแจ้งยอดการชำระเงินกลับบัญชีจะถูกสร้างเพื่อออฟเซ็ตใบแจ้งยอดการชำระค่าจ้างนี้</span><span class="sxs-lookup"><span data-stu-id="835f8-253">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="835f8-254">ใบแจ้งยอดค่าจ้างไม่สามารถถูกแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="835f8-254">Neither pay statement can be edited.</span></span> <span data-ttu-id="835f8-255">คุณต้องการกลับรายการใบแจ้งยอดการชำระค่าจ้างนี้หรือไม่"</span><span class="sxs-lookup"><span data-stu-id="835f8-255">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="835f8-256">การแสดง</span><span class="sxs-lookup"><span data-stu-id="835f8-256">displays.</span></span> 

<span data-ttu-id="835f8-257">หลังจากที่คุณกลับรายการใบแจ้งยอดค่าจ้าง คุณสามารถสร้างใบแจ้งยอดการชำระค่าจ้างใหม่สำหรับผู้ปฏิบัติงานจากใบแจ้งยอดรายได้ที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="835f8-257">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="835f8-258">ตรวจสอบให้แน่ใจว่าได้ทำการแก้ไขบรรทัดที่ไม่ถูกต้องในใบแจ้งยอดรายได้ก่อนที่คุณจะสร้างใบแจ้งยอดค่าจ้างใหม่ จากนั้นให้สร้างใบแจ้งยอดค่าจ้างใหม่ที่มียอดเงินที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="835f8-258">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]