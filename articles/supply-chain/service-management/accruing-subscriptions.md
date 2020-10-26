---
title: การตั้งค้างรับการสั่งซื้อโดยบอกรับเป็นสมาชิก
description: ด้วยการสั่งซื้อโดยบอกรับเป็นสมาชิกการบริการ คุณจะรับรู้รายได้ในรอบเวลาที่ตามหลังวันที่เมื่อคุณออกใบแจ้งหนี้ธุรกรรมค่าธรรมเนียมได้ด้วยตัวเอง
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ebd65655db56ee1169f24dbc79fbfb5130f06a5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978832"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="f45fc-103">การตั้งค้างรับการสั่งซื้อโดยบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="f45fc-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f45fc-104">ด้วยการสั่งซื้อโดยบอกรับเป็นสมาชิกการบริการ คุณจะรับรู้รายได้ในรอบเวลาที่ตามหลังวันที่เมื่อคุณออกใบแจ้งหนี้ธุรกรรมค่าธรรมเนียมได้ด้วยตัวเอง</span><span class="sxs-lookup"><span data-stu-id="f45fc-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="f45fc-105">รอบระยะเวลาการรับรู้รายได้มีการสร้างขึ้นสำหรับรอบใบแจ้งหนี้ที่คุณตั้งค่าให้กับค่าธรรมเนียมการบอกรับเป็นสมาชิก และรอบระยะเวลาการรับรู้รายได้มีพื้นฐานตามรหัสช่วงเวลาของการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="f45fc-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="f45fc-106">คุณสามารถรับรู้รายได้และย้อนกลับรายได้ที่ค้างรับ</span><span class="sxs-lookup"><span data-stu-id="f45fc-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="f45fc-107">กลับรายการการรับรู้ของยอดเครดิต</span><span class="sxs-lookup"><span data-stu-id="f45fc-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="f45fc-108">ถ้าคุณให้เครดิตจำนวนเงินที่ออกใบแจ้งหนี้ คุณสามารถใช้วิธีได้สองวิธีในการย้อนกลับรายได้ที่รับรู้:</span><span class="sxs-lookup"><span data-stu-id="f45fc-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="f45fc-109">คุณสามารถกลับรายการธุรกรรมรายได้ค้างรับแต่ละธุรกรรมได้ ก่อนที่คุณจะสร้างข้อเสนอใบลดหนี้สำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="f45fc-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="f45fc-110">นี่เป็นวิธีแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="f45fc-110">This is the manual method.</span></span> <span data-ttu-id="f45fc-111">(แบบกำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="f45fc-111">(manual)</span></span>

  - <span data-ttu-id="f45fc-112">คุณสามารถย้อนกลับจำนวนเงินค้างรับในวันที่ที่มีการลงรายการบัญชีใบลดหนี้ หรือในวันที่ที่ลงรายการบัญชีเดิมของการรับรู้ได้</span><span class="sxs-lookup"><span data-stu-id="f45fc-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="f45fc-113">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [พารามิเตอร์การบอกรับเป็นสมาชิก (ฟอร์ม)](https://technet.microsoft.com/library/aa619615.aspx)</span><span class="sxs-lookup"><span data-stu-id="f45fc-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="f45fc-114">ตั้งค่าความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f45fc-114">Setup requirements</span></span>

<span data-ttu-id="f45fc-115">เมื่อต้องการรับรู้รายได้ ให้ตรวจสอบให้แน่ใจว่าข้อกำหนดข้อมูลต่อไปนี้ตรงกับเงื่อนไข:</span><span class="sxs-lookup"><span data-stu-id="f45fc-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="f45fc-116">การตั้งค่าบัญชี</span><span class="sxs-lookup"><span data-stu-id="f45fc-116">Account setup</span></span>

<span data-ttu-id="f45fc-117">**WIP - การบอกรับเป็นสมาชิก** และบัญชี **รายได้ค้างรับ - การบอกรับเป็นสมาชิก** ต้องถูกตั้งค่าในโมดูล **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="f45fc-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="f45fc-118">เมื่อคุณลงรายการบัญชีรายได้ค้างรับ บัญชี **WIP - การบอกรับเป็นสมาชิก** ถูกเดบิตด้วยยอดเงินคงค้าง และบัญชี **รายได้ค้างรับ - การบอกรับเป็นสมาชิก** จะถูกเครดิตด้วยยอดเงินคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f45fc-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="f45fc-119">การตั้งค่าบัญชีให้กับรายการคงค้างของการสั่งซื้อโดยบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="f45fc-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="f45fc-120">คลิก **การจัดการและการบัญชีโครงการ** \> **การตั้งค่า** \> **การลงรายการบัญชี** \> **การตั้งค่าการลงรายการบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="f45fc-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="f45fc-121">คลิกแท็บ **บัญชีรายได้** และเลือก **WIP - การบอกรับเป็นสมาชิก** หรือ **รายได้ค้างรับ - การบอกรับเป็นสมาชิก** เพื่อตั้งค่าบัญชี</span><span class="sxs-lookup"><span data-stu-id="f45fc-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="f45fc-122">การตั้งค่ากลุ่มการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="f45fc-122">Subscription group setup</span></span>

<span data-ttu-id="f45fc-123">เพื่อให้สามารถรับรู้รายได้สำหรับการบอกรับเป็นสมาชิก ต้องมีการเลือกกล่องกาเครื่องหมาย **รายได้ค้างรับ**</span><span class="sxs-lookup"><span data-stu-id="f45fc-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="f45fc-124">นี่จะพบในแบบฟอร์ม **กลุ่มการบอกรับเป็นสมาชิก** สำหรับกลุ่มที่ถูกแนบกับการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="f45fc-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="f45fc-125">คลิก **การจัดการงานบริการ** \> **การตั้งค่า** \> **การบอกรับเป็นสมาชิกการบริการ** \> **กลุ่มการบอกรับเป็นสมาชิก**</span><span class="sxs-lookup"><span data-stu-id="f45fc-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="f45fc-126">การเปิดใช้งานรายได้ค้างรับบนกลุ่มการบอกรับการสมัครสมาชิก</span><span class="sxs-lookup"><span data-stu-id="f45fc-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="f45fc-127">คลิก **การจัดการงานบริการ** \> **การตั้งค่า** \> **การบอกรับเป็นสมาชิกการบริการ** \> **กลุ่มการบอกรับเป็นสมาชิก**</span><span class="sxs-lookup"><span data-stu-id="f45fc-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="f45fc-128">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="f45fc-128">Periods</span></span>

<span data-ttu-id="f45fc-129">คุณต้องตั้งค่ารหัสช่วงเวลาการออกใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="f45fc-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="f45fc-130">นอกจากว่าคุณต้องการรับรู้รายได้ในช่วงเวลาเดียวกันกับที่คุณใช้สำหรับการออกใบแจ้งหนี้ คุณต้องตั้งค่าช่วงเวลาคงค้างด้วยเช่นเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="f45fc-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="f45fc-131">ตารางต่อไปนี้ให้ภาพรวมของช่วงเวลาคงค้างใดที่สามารถถูกตั้งค่าได้สำหรับช่วงเวลาในการออกใบแจ้งหนี้แต่ละช่วง:</span><span class="sxs-lookup"><span data-stu-id="f45fc-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f45fc-132">รอบระยะเวลาการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f45fc-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="f45fc-133">ช่วงเวลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f45fc-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f45fc-134"><strong>ปี</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="f45fc-135"><strong>ปี</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="f45fc-136"><strong>ไตรมาส</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="f45fc-137"><strong>เดือน</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="f45fc-138"><strong>วัน</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f45fc-139"><strong>ไตรมาส</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="f45fc-140"><strong>ไตรมาส</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="f45fc-141"><strong>เดือน</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="f45fc-142"><strong>วัน</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f45fc-143"><strong>เดือน</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="f45fc-144"><strong>เดือน</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="f45fc-145"><strong>วัน</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f45fc-146"><strong>สัปดาห์</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="f45fc-147"><strong>วัน</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f45fc-148"><strong>วัน</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="f45fc-149"><strong>วัน</strong></span><span class="sxs-lookup"><span data-stu-id="f45fc-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f45fc-150">การตั้งค่ารอบระยะเวลาการออกใบแจ้งหนี้เป็นส่วนบังคับในการตั้งค่ากลุ่มการบอกรับเป็นสมาชิกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f45fc-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="f45fc-151">คุณสามารถตัดสินใจได้ว่า จะตั้งค่าระยะเวลาค้างรับค้างจ่ายสำหรับกลุ่มการบอกรับเป็นสมาชิกด้วยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f45fc-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="f45fc-152">ถ้าคุณตั้งค่ารอบระยะเวลาคงค้างสำหรับกลุ่มการบอกรับสมาชิก รอบระยะเวลานี้ได้รับการแนะนำในฟิลด์ **รหัสรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="f45fc-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="f45fc-153">ฟิลด์นี้ถูกพบในแบบฟอร์ม **รับรู้รายได้การบอกรับเป็นสมาชิก** เมื่อคุณทำการรับรู้รายได้การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="f45fc-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="f45fc-154">แต่รอบระยะเวลาคงค้างเป็นข้อมูลที่เลือกได้เกี่ยวกับกลุ่มการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="f45fc-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f45fc-155">ใช้เส้นทางต่อไปนี้เพื่อเปิดแบบฟอร์ม <STRONG>รับรู้รายได้การบอกรับเป็นสมาชิก</STRONG></span><span class="sxs-lookup"><span data-stu-id="f45fc-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="f45fc-156">คลิก <STRONG>การจัดการงานบริการ</STRONG> &gt; <STRONG>งานประจำงวด</STRONG> &gt; <STRONG>การบอกรับเป็นสมาชิกการบริการ</STRONG> &gt; <STRONG>ตั้งรายการค้างรับของรายได้จากการบอกรับเป็นสมาชิก</STRONG></span><span class="sxs-lookup"><span data-stu-id="f45fc-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="f45fc-157">ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="f45fc-157">Transactions</span></span>

<span data-ttu-id="f45fc-158">คุณสามารถควบคุมจำนวนของธุรกรรมบัญชีแยกประเภทที่สร้างขึ้นได้ เมื่อคุณลงรายการบัญชีรายได้ค้างรับ</span><span class="sxs-lookup"><span data-stu-id="f45fc-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="f45fc-159">ในการบอกรับเป็นสมาชิก กำหนดว่าควรสร้างธุรกรรมบัญชีแยกประเภทเป็นยอดรวม หรือต่อรายการ</span><span class="sxs-lookup"><span data-stu-id="f45fc-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="f45fc-160">การระบุระดับรายละเอียดการลงรายการบัญชีเพื่อแสดงให้กับธุรกรรมคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f45fc-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="f45fc-161">คลิก **การจัดการและการบัญชีโครงการ** \> **การตั้งค่า** \> **พารามิเตอร์การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="f45fc-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="f45fc-162">บนแท็บ **การเงิน** ในฟิลด์ **ใบแจ้งหนี้** เลือก **ยอดรวม** หรือ **รายการ**</span><span class="sxs-lookup"><span data-stu-id="f45fc-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="f45fc-163">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="f45fc-163">See also</span></span>

[<span data-ttu-id="f45fc-164">ตั้งรายการค้างรับของรายได้จากการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="f45fc-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  


