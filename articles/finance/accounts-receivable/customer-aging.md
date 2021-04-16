---
title: รายงานอายุหนี้ของลูกค้า
description: รายงานอายุหนี้ของลูกค้าแสดงยอดดุลที่ครบกำหนดชำระจากลูกค้า เรียงลำดับตามช่วงวันที่ หรือรอบระยะเวลาอายุหนี้
author: JodiChristiansen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b80345513d355115a182c108bf3843963e9a59d9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840352"
---
# <a name="customer-aging-report"></a><span data-ttu-id="2cabe-103">รายงานอายุหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2cabe-103">Customer aging report</span></span> 

<span data-ttu-id="2cabe-104">รายงาน **อายุหนี้ของลูกค้า** แสดงยอดดุลที่ครบกำหนดชำระจากลูกค้า เรียงลำดับตามช่วงวันที่ หรือรอบระยะเวลาอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="2cabe-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="2cabe-105">เมื่อคุณสร้างรายงานนี้ พารามิเตอร์เริ่มต้นต่อไปนี้จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="2cabe-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="2cabe-106">คุณสามารถใช้พารามิเตอร์เหล่านี้เพื่อกรองข้อมูลที่จะแสดงขึ้นในรายงาน</span><span class="sxs-lookup"><span data-stu-id="2cabe-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="2cabe-107">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าการเรียกเก็บเงิน](set-up-collections.md)</span><span class="sxs-lookup"><span data-stu-id="2cabe-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2cabe-108">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="2cabe-108">Field</span></span></p></th>
<th><p><span data-ttu-id="2cabe-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2cabe-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cabe-110"><strong>การจัดประเภทการเรียกเก็บเงิน</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-111">เลือกการจัดประเภทการเรียกเก็บเงินอย่างน้อยหนึ่งรายการเพื่อรวมไว้ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="2cabe-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="2cabe-112">**หมายเหตุ:** ตัวควบคุมนี้สามารถใช้ได้ก็ต่อเมื่อมีการเลือกคีย์การตั้งค่าคอนฟิก <STRONG>ภาครัฐ</STRONG> ไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2cabe-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cabe-113"><strong>รวมธุรกรรมที่ไม่มีการจัดประเภทการเรียกเก็บเงิน</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-114">ถ้าเลือกกล่องกาเครื่องหมายนี้ ธุรกรรมทั้งหมดที่ไม่มีการจัดประเภทการเรียกเก็บเงินที่กำหนดให้กับรายการจะแสดงอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="2cabe-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="2cabe-115">**หมายเหตุ:** ตัวควบคุมนี้สามารถใช้ได้ก็ต่อเมื่อมีการเลือกคีย์การตั้งค่าคอนฟิก <STRONG>ภาครัฐ</STRONG> ไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2cabe-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cabe-116"><strong>อายุหนี้ ณ วันที่</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-117">ป้อนวันที่ที่ใช้ในกลุ่มอายุหนี้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2cabe-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cabe-118"><strong>ยอดดุล ณ วันที่</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-119">ป้อนวันที่เพื่อดูยอดดุลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2cabe-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="2cabe-120">การทำเช่นนี้เรียกอีกอย่างหนึ่งว่า วันที่ตัดยอดสำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="2cabe-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cabe-121"><strong>วันที่เริ่มต้น</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-122">ป้อนวันที่ที่อยู่ภายในช่วงรอบระยะเวลาแรกหรือรอบระยะเวลาอายุหนี้ที่จะรวมไว้ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="2cabe-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cabe-123"><strong>เกณฑ์</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-124">เลือกชนิดของวันที่ที่จะใช้เป็นพื้นฐานของรายงาน</span><span class="sxs-lookup"><span data-stu-id="2cabe-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="2cabe-125"><strong>วันที่ธุรกรรม</strong> – วันที่ลงรายการบัญชีธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="2cabe-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="2cabe-126">ตัวอย่างเช่น ข้อมูลนี้อาจเป็นวันที่ใบแจ้งหนี้ ซึ่งเป็นข้อมูลพื้นฐานสำหรับการคำนวณวันที่ครบกำหนดชำระ</span><span class="sxs-lookup"><span data-stu-id="2cabe-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="2cabe-127"><strong>วันที่ครบกำหนด</strong> – วันที่ครบกำหนดของธุรกรรม ตามเงื่อนไขการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2cabe-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="2cabe-128"><strong>วันที่ในเอกสาร</strong> – วันที่ในเอกสารที่กำหนดโดยผู้ใช้ที่เป็นพื้นฐานสำหรับการคำนวณวันที่ครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="2cabe-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cabe-129"><strong>ข้อกำหนดรอบระยะเวลาอายุหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-130">เลือกข้อกำหนดรอบระยะเวลาอายุหนี้ </span><span class="sxs-lookup"><span data-stu-id="2cabe-130">Select an aging period definition.</span></span> <span data-ttu-id="2cabe-131">จะไม่มีการใช้ฟิลด์ <strong>ช่วงเวลา</strong> ถ้าคุณเลือกข้อกำหนดรอบระยะเวลาอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="2cabe-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="2cabe-132">คุณไม่สามารถใช้ข้อกำหนดรอบระยะเวลาอายุหนี้ที่มีมากกว่าหกรอบระยะเวลาอายุหนี้ในรายงานที่พิมพ์ได้</span><span class="sxs-lookup"><span data-stu-id="2cabe-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="2cabe-133">**หมายเหตุ:** คุณสามารถตั้งค่ารอบระยะเวลาอายุหนี้ในหน้า <STRONG>ข้อกำหนดรอบระยะเวลาอายุหนี้</STRONG></span><span class="sxs-lookup"><span data-stu-id="2cabe-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cabe-134"><strong>พิมพ์คำอธิบายรอบระยะเวลาอายุหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-135">เลือก <strong>ใช่</strong> เพื่อรวมคำอธิบายรอบระยะเวลาอายุหนี้ไว้ที่ด้านบนของคอลัมรอบระยะเวลาอายุหนี้แต่ละคอลัมน์ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="2cabe-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="2cabe-136">เลือก <strong>หมายเลข</strong> เพื่อพิมพ์รายงานโดยไม่มีหัวข้อคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="2cabe-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cabe-137"><strong>ช่วงเวลา</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-138">กำหนดรอบระยะเวลาที่จะใช้โดยการป้อนจำนวนหน่วยของวันหรือเดือนในแต่ละรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="2cabe-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="2cabe-139">ตัวอย่างเช่น ถ้าต้องการดูข้อมูลอายุหนี้ตามสัปดาห์ ป้อน 7 ในฟิลด์นี้และเลือก <strong>วัน</strong> ในฟิลด์ <strong>วัน/เดือน</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="2cabe-140">**หมายเหตุ:** ข้อมูลที่คุณป้อนในฟิลด์นี้จะมีการใช้เฉพาะเมื่อคุณไม่ได้เลือกข้อกำหนดรอบระยะเวลาอายุหนี้ไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2cabe-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="2cabe-141">มิฉะนั้น ทิศทางการพิมพ์จะถูกกำหนดในข้อกำหนดรอบระยะเวลาอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="2cabe-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cabe-142"><strong>วัน/เดือน</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-143">เลือกหน่วยซึ่งอาจเป็น <strong>วัน</strong> หรือ <strong>เดือน</strong> ที่จะใช้ในการกำหนดรอบระยะเวลาในฟิลด์ <strong>ช่วงเวลา</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cabe-144"><strong>คำสั่งการพิมพ์</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-145">เลือกว่าจะคำนวณยอดดุลและพิมพ์รายงานอายุหนี้สำหรับรอบระยะเวลาในอดีตหรือในอนาคตหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2cabe-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="2cabe-146">วันที่จะถูกประเมินโดยสัมพันธ์กับวันที่ที่เลือกในฟิลด์ <strong>ยอดดุล ณ วันที่</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="2cabe-147">โดยสัมพันธ์กับวันที่เลือกไว้ในฟิลด์ เลือก <strong>ย้อนหลัง</strong> เพื่อแสดงข้อมูลสำหรับรอบระยะเวลาในอดีต</span><span class="sxs-lookup"><span data-stu-id="2cabe-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="2cabe-148">เลือก <strong>ไปข้างหน้า</strong> เพื่อแสดงข้อมูลสำหรับรอบระยะเวลาในอนาคต</span><span class="sxs-lookup"><span data-stu-id="2cabe-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>
<div class="alert"><span data-ttu-id="2cabe-149">
  
<STRONG>หมายเหตุ:</STRONG> ข้อมูลที่คุณป้อนในฟิลด์นี้จะมีการใช้เฉพาะเมื่อคุณไม่ได้เลือกข้อกำหนดรอบระยะเวลาอายุหนี้ไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2cabe-149">
  
<STRONG>Note:</STRONG> The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cabe-150"><strong>รายละเอียด</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-151">เลือกรายการธุรกรรมที่รวมอยู่ในยอดดุลซึ่งปรากฏอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="2cabe-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cabe-152"><strong>รวมยอดเงินในสกุลเงินของธุรกรรม</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-153">เลือกเพื่อรวมยอดเงินในสกุลเงินของธุรกรรม นอกเหนือจากยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="2cabe-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="2cabe-154">ถ้าไม่ได้เลือกกล่องกาเครื่องหมายนี้ ยอดเงินในรายงานจะแสดงอยู่ในสกุลเงินทางบัญชีเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2cabe-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cabe-155"><strong>ยอดดุลติดลบ</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-156">เลือกเพื่อรวมบัญชีลูกค้าที่มียอดดุลติดลบ</span><span class="sxs-lookup"><span data-stu-id="2cabe-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cabe-157"><strong>ไม่รวมบัญชีที่มียอดดุลเป็นศูนย์</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-158">เลือกเพื่อแยกบัญชีลูกค้าที่มียอดดุลเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="2cabe-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cabe-159"><strong>การกำหนดตำแหน่งการชำระเงิน</strong></span><span class="sxs-lookup"><span data-stu-id="2cabe-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="2cabe-160">เลือกเพื่อแสดงการชำระเงินที่ยังไม่ได้ชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2cabe-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="2cabe-161">เหล่านี้จะแสดงในคอลัมน์แรกของรายงาน</span><span class="sxs-lookup"><span data-stu-id="2cabe-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]