---
title: "โพรไฟล์การลงรายการบัญชีลูกค้า"
description: "โพรไฟล์การลงบัญชีของลูกค้าควบคุมการลงรายการบัญชีของธุรกรรมลูกค้าให้บัญชีแยกประเภททั่วไป"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f246780a320f9a5e25ca423a099669a4f7e57bab
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="customer-posting-profiles"></a><span data-ttu-id="1f8dd-103">โพรไฟล์การลงรายการบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="1f8dd-103">Customer posting profiles</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="1f8dd-104">โพรไฟล์การลงบัญชีของลูกค้าควบคุมการลงรายการบัญชีของธุรกรรมลูกค้าให้บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="1f8dd-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="1f8dd-105">โพรไฟล์การลงรายการบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="1f8dd-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="1f8dd-106">โพรไฟล์การลงรายการบัญชีลูกค้าช่วยให้คุณสามารถกำหนดบัญชีแยกประเภททั่วไปและการตั้งค่าเอกสารให้กับลูกค้าทั้งหมด กลุ่มลูกค้า หรือลูกค้ารายเดียวได้</span><span class="sxs-lookup"><span data-stu-id="1f8dd-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="1f8dd-107">การตั้งค่าเหล่านี้จะใช้เมื่อคุณสร้างใบสั่งขาย ใบแจ้งหนี้ข้อความอิสระ การชำระเงินสด จดหมายเรียกเก็บเงิน และดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="1f8dd-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="1f8dd-108">สำหรับบางธุรกรรม คุณสามารถเลือกโพรไฟล์การลงบัญชีที่แตกต่าง และมีระดับความสำคัญเหนือกว่า โพรไฟล์การลงบัญชีที่ตั้งค่าไว้แล้วสำหรับธุรกรรมในหน้านี้</span><span class="sxs-lookup"><span data-stu-id="1f8dd-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="1f8dd-109">มีกำหนดค่าเริ่มต้นโพรไฟล์การลงรายการบัญชีในแท็บด่วนบัญชีแยกประเภทและภาษี บนหน้าพารามิเตอร์บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="1f8dd-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="1f8dd-110">ค่าเริ่มต้นโพรไฟล์การลงรายการบัญชีจะรวมอยู่ในส่วนหัวของเอกสารใหม่โดยอัตโนมัติ ซึ่งคุณสามารถเปลี่ยนเป็นโพรไฟล์การลงรายการบัญชีอื่นหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="1f8dd-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="1f8dd-111">คุณยังสามารถเชื่อมโยงข้อกำหนดการลงรายการบัญชีกับชนิดการลงรายการบัญชีธุรกรรม ในหน้าข้อกำหนดการลงรายการบัญชีของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="1f8dd-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="1f8dd-112">ข้อกำหนดการลงรายการบัญชีจะควบคุมการลงรายการบัญชีของธุรกรรมลูกค้าไปยังบัญชีแยกประเภททั่วไปแทนข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="1f8dd-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="1f8dd-113">การสร้างการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="1f8dd-113">Creating a posting profile</span></span>
<span data-ttu-id="1f8dd-114">ระบุบัญชีแยกประเภทที่จะใช้ในการลงรายการบัญชีธุรกรรมที่มีโพรไฟล์การลงบัญชีที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="1f8dd-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="1f8dd-115">เลือกรหัสบัญชี และหากเป็นไปได้ เลือกหมายเลขบัญชีหรือหมายเลขกลุ่มสำหรับโพรไฟล์การลงบัญชีที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="1f8dd-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="1f8dd-116">ในกระบวนการลงรายการบัญชี ข้อมูลโพรไฟล์การลงบัญชีที่เหมาะสมที่สุดสำหรับแต่ละธุรกรรมจะถูกระบุโดยการค้นหาชุดรหัสบัญชี หมายเลขบัญชี หรือส่วนผสมระหว่างกลุ่มและหมายเลขที่เจาะจงที่สุดตามระดับความสำคัญดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1f8dd-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="1f8dd-117">ค่าฟิลด์ **รหัสบัญชี**</span><span class="sxs-lookup"><span data-stu-id="1f8dd-117">**Account code** field value</span></span> | <span data-ttu-id="1f8dd-118">ค่าฟิลด์ **หมายเลขบัญชี/กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="1f8dd-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="1f8dd-119">ระดับความสำคัญของการค้นหา</span><span class="sxs-lookup"><span data-stu-id="1f8dd-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="1f8dd-120">**ตาราง**</span><span class="sxs-lookup"><span data-stu-id="1f8dd-120">**Table**</span></span>                    | <span data-ttu-id="1f8dd-121">บัญชีลูกค้าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1f8dd-121">Specific customer account</span></span>                       | <span data-ttu-id="1f8dd-122">1</span><span class="sxs-lookup"><span data-stu-id="1f8dd-122">1</span></span>               |
| <span data-ttu-id="1f8dd-123">**กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="1f8dd-123">**Group**</span></span>                    | <span data-ttu-id="1f8dd-124">กลุ่มลูกค้าที่ถูกกำหนดให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="1f8dd-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="1f8dd-125">2</span><span class="sxs-lookup"><span data-stu-id="1f8dd-125">2</span></span>               |
| <span data-ttu-id="1f8dd-126">**ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="1f8dd-126">**All**</span></span>                      | <span data-ttu-id="1f8dd-127">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="1f8dd-127">Blank</span></span>                                           | <span data-ttu-id="1f8dd-128">3</span><span class="sxs-lookup"><span data-stu-id="1f8dd-128">3</span></span>               |

<span data-ttu-id="1f8dd-129">ถ้าคุณต้องการให้ธุรกรรมลูกค้าทั้งหมดมีโพรไฟล์การลงบัญชีเหมือนกัน ให้ตั้งค่าเพียงหนึ่งโพรไฟล์การลงบัญชีในฟิลด์รหัสบัญชี</span><span class="sxs-lookup"><span data-stu-id="1f8dd-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="1f8dd-130">ระบุค่าต่อไปนี้เพื่อตั้งค่าโพรไฟล์การลงรายการบัญชีของคุณ:</span><span class="sxs-lookup"><span data-stu-id="1f8dd-130">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1f8dd-131">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="1f8dd-131">Field</span></span></th>
<th><span data-ttu-id="1f8dd-132">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1f8dd-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f8dd-133"><strong>โพรไฟล์การลงรายการบัญชี</strong></span><span class="sxs-lookup"><span data-stu-id="1f8dd-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="1f8dd-134">ป้อนรหัสสำหรับโพรไฟล์การลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="1f8dd-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="1f8dd-135">ตัวอย่างเช่น คุณสามารถสร้างโพรไฟล์การลงบัญชี 2 โพรไฟล์ เพื่อให้มีหนึ่งบัญชีสำหรับยอดดุลลูกค้าในสกุลเงินในประเทศ และอีกบัญชีหนึ่งสำหรับยอดดุลลูกค้าในสกุลเงินต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="1f8dd-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="1f8dd-136">คุณสามารถเรียกบัญชีหนึ่งว่าในประเทศ และอีกบัญชีหนึ่งว่าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="1f8dd-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8dd-137"><strong>คำอธิบาย</strong></span><span class="sxs-lookup"><span data-stu-id="1f8dd-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="1f8dd-138">ป้อนคำอธิบายเกี่ยวโพรไฟล์การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="1f8dd-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="1f8dd-139">ซึ่งจะใช้เพื่อให้ระบุโพรไฟล์การลงรายการบัญชีได้ดีขึ้นเมื่อคุณดูในหน้านี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1f8dd-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8dd-140"><strong>รหัสบัญชี</strong></span><span class="sxs-lookup"><span data-stu-id="1f8dd-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="1f8dd-141">ระบุว่าการตั้งค่าโพรไฟล์การลงรายการบัญชีใช้กับลูกค้ารายเดียว กลุ่มลูกค้า หรือลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1f8dd-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="1f8dd-142"><strong>ตาราง</strong> – กฎการลงรายการบัญชีที่ใช้กับลูกค้ารายเดียว</span><span class="sxs-lookup"><span data-stu-id="1f8dd-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="1f8dd-143">เลือกบัญชีลูกค้าในฟิลด์หมายเลขบัญชี/กลุ่ม</span><span class="sxs-lookup"><span data-stu-id="1f8dd-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="1f8dd-144"><strong>กลุ่ม</strong> – กฎการลงรายการบัญชีที่ใช้กับกลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="1f8dd-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="1f8dd-145">เลือกกลุ่มลูกค้าในฟิลด์หมายเลขบัญชี/กลุ่ม</span><span class="sxs-lookup"><span data-stu-id="1f8dd-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="1f8dd-146"><strong>ทั้งหมด</strong> – กฎการลงรายการบัญชีที่ใช้กับลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1f8dd-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="1f8dd-147">ปล่อยฟิลด์หมายเลขบัญชี/กลุ่มว่างไว้</span><span class="sxs-lookup"><span data-stu-id="1f8dd-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8dd-148"><strong>หมายเลขบัญชี/กลุ่ม</strong></span><span class="sxs-lookup"><span data-stu-id="1f8dd-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="1f8dd-149">ถ้าในฟิลด์รหัสบัญชีเลือกตารางไว้ ให้เลือกหมายเลขบัญชีของลูกค้าที่เชื่อมโยงกับโพรไฟล์การลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="1f8dd-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="1f8dd-150">ถ้าเลือกกลุ่ม ให้เลือกกลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="1f8dd-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="1f8dd-151">ถ้าเลือกทั้งหมด ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="1f8dd-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8dd-152"><strong>บัญชีสรุป</strong></span><span class="sxs-lookup"><span data-stu-id="1f8dd-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="1f8dd-153">เลือกบัญชีแยกประเภทที่จะใช้เป็นบัญชีสรุปลูกค้า สำหรับลูกค้าที่สัมพันธ์กับโพรไฟล์การลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="1f8dd-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8dd-154"><strong>ตัดรายการบัญชี</strong></span><span class="sxs-lookup"><span data-stu-id="1f8dd-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="1f8dd-155">เลือกบัญชีแยกประเภทที่มีสภาพคล่องที่ใช้สำหรับการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="1f8dd-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="1f8dd-156">ฟิลด์นี้จะปรากฏขึ้นมื่อมีการเปิดใช้งานการคาดการณ์กระแสเงินสดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1f8dd-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8dd-157"><strong>การชำระภาษีขายล่วงหน้า</strong></span><span class="sxs-lookup"><span data-stu-id="1f8dd-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="1f8dd-158">เลือกหมายเลขบัญชีสำหรับภาษีขายสำหรับการชำระเงินที่ได้รับล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="1f8dd-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="บันทึก" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="1f8dd-160"><strong>บันทึก</strong></span><span class="sxs-lookup"><span data-stu-id="1f8dd-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f8dd-161">ใช้หน้าพารามิเตอร์บัญชีลูกหนี้บัญชีเพื่อระบุโพรไฟล์การลงรายการบัญชีที่จะใช้เมื่อการชำระเงินถูกทำเครื่องหมายเป็นการชำระเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="1f8dd-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8dd-162"><strong>หนี้สินสำหรับบัญชีส่วนลด</strong></span><span class="sxs-lookup"><span data-stu-id="1f8dd-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="1f8dd-163">เลือกบัญชีแยกประเภทสำหรับหนี้สินที่เป็นส่วนลด</span><span class="sxs-lookup"><span data-stu-id="1f8dd-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8dd-164"><strong>ลำดับจดหมายเรียกเก็บเงิน</strong></span><span class="sxs-lookup"><span data-stu-id="1f8dd-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="1f8dd-165">เลือกตัวระบุของลำดับจดหมายเรียกเก็บเงินเพื่อใช้สำหรับลูกค้าที่มีการกำหนดโพรไฟล์การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="1f8dd-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8dd-166"><strong>รหัสดอกเบี้ย</strong></span><span class="sxs-lookup"><span data-stu-id="1f8dd-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="1f8dd-167">เลือกรหัสดอกเบี้ยเพื่อใช้สำหรับการคำนวณดอกเบี้ยสำหรับลูกค้าที่มีการกำหนดโพรไฟล์การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="1f8dd-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="1f8dd-168">**ข้อจำกัด**</span><span class="sxs-lookup"><span data-stu-id="1f8dd-168">**Table restrictions**</span></span>

<span data-ttu-id="1f8dd-169">สำหรับธุรกรรมที่มีโพรไฟล์การลงบัญชีที่เลือกไว้ ให้ระบุว่าธุรกรรมจะได้รับชำระเงินโดยอัตโนมัติ จะมีการคำนวณดอกเบี้ย และจะออกจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="1f8dd-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="1f8dd-170">คุณยังสามารถเลือกบัญชีที่จะใช้เมื่อธุรกรรมที่มีโพรไฟล์การลงบัญชีที่เลือกไว้ปิดลง</span><span class="sxs-lookup"><span data-stu-id="1f8dd-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="1f8dd-171">ระบุค่าต่อไปนี้เพื่อตั้งค่าโพรไฟล์การลงรายการบัญชีของคุณ:</span><span class="sxs-lookup"><span data-stu-id="1f8dd-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="1f8dd-172">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="1f8dd-172">Field</span></span>                 | <span data-ttu-id="1f8dd-173">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1f8dd-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f8dd-174">**การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="1f8dd-174">**Settlement**</span></span>        | <span data-ttu-id="1f8dd-175">เลือกการสลับนี้เพื่อเปิดใช้งานการชำระเงินธุรกรรมที่มีโพรไฟล์การลงรายการบัญชีนี้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="1f8dd-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="1f8dd-176">ถ้าไม่ได้เลือกการสลับนี้ คุณต้องชำระธุรกรรมด้วยตนเองโดยใช้หน้าชำระธุรกรรมที่ค้างอยู่ หรือหน้าป้อนการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="1f8dd-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="1f8dd-177">**ความสนใจ**</span><span class="sxs-lookup"><span data-stu-id="1f8dd-177">**Interest**</span></span>          | <span data-ttu-id="1f8dd-178">เลือกการสลับนี้ถ้าควรคำนวณดอกเบี้ยตามยอดดุลค้างชำระของลูกค้า สำหรับบัญชีลูกค้าที่ใช้โพรไฟล์นี้</span><span class="sxs-lookup"><span data-stu-id="1f8dd-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="1f8dd-179">ถ้าไม่ได้เลือกการสลับนี้ จะไม่มีการคำนวณค่าธรรมเนียมดอกเบี้ยสำหรับลูกค้ารายนี้</span><span class="sxs-lookup"><span data-stu-id="1f8dd-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="1f8dd-180">**จดหมายเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="1f8dd-180">**Collection letter**</span></span> | <span data-ttu-id="1f8dd-181">เลือกการสลับนี้ถ้าควรสร้างจดหมายเรียกเก็บเงินสำหรับบัญชีลูกค้าที่ใช้โพรไฟล์นี้</span><span class="sxs-lookup"><span data-stu-id="1f8dd-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="1f8dd-182">ถ้าไม่ได้เลือกการสลับนี้ จะไม่มีการสร้างจดหมายเรียกเก็บเงินสำหรับลูกค้ารายนี้</span><span class="sxs-lookup"><span data-stu-id="1f8dd-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="1f8dd-183">**ปิดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="1f8dd-183">**Close**</span></span>             | <span data-ttu-id="1f8dd-184">เลือกโพรไฟล์การลงรายการบัญชีที่จะเปลี่ยนเมื่อธุรกรรมที่มีโพรไฟล์การลงรายการบัญชีนี้ปิดบัญชีแล้ว</span><span class="sxs-lookup"><span data-stu-id="1f8dd-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="1f8dd-185">ธุรกรรมนี้จะถือว่าเป็นปิดบัญชีแล้ว เมื่อมีการจับคู่ครบถ้วนแล้ว</span><span class="sxs-lookup"><span data-stu-id="1f8dd-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="1f8dd-186">สำหรับข้อมูลเพิ่มเติม โปรดดู [ภาพรวมการชำระเงินของลูกค้า](../cash-bank-management/tasks/customer-payment-overview.md)</span><span class="sxs-lookup"><span data-stu-id="1f8dd-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>


