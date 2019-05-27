---
title: โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่าย
description: โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่ายควบคุมการลงรายการบัญชีของธุรกรรมผู้จัดจำหน่ายที่บัญชีแยกประเภททั่วไป
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e81f8b472e7ac7578c184716dcb4e5f3d7aeb65d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512179"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="2a0ef-103">โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2a0ef-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a0ef-104">โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่ายควบคุมการลงรายการบัญชีของธุรกรรมผู้จัดจำหน่ายที่บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="2a0ef-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="2a0ef-105">โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2a0ef-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="2a0ef-106">โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่ายช่วยให้คุณสามารถกำหนดบัญชีแยกประเภททั่วไปและการตั้งค่าเอกสารให้กับผู้จัดจำหน่ายทั้งหมด กลุ่มผู้จัดจำหน่าย หรือผู้จัดจำหน่ายรายเดียวได้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors or a single vendor.</span></span> <span data-ttu-id="2a0ef-107">การตั้งค่าเหล่านี้จะใช้เมื่อคุณสร้างใบสั่งซื้อ ใบแจ้งหนี้ของผู้จัดจำหน่าย และการชำระเงินสด</span><span class="sxs-lookup"><span data-stu-id="2a0ef-107">These settings will be used when you create purchase orders, vendor invoices and cash payments.</span></span> <span data-ttu-id="2a0ef-108">สำหรับบางธุรกรรม คุณสามารถเลือกโพรไฟล์การลงบัญชีที่แตกต่าง และมีระดับความสำคัญเหนือกว่า โพรไฟล์การลงบัญชีที่ตั้งค่าไว้แล้วสำหรับธุรกรรมในหน้านี้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> <span data-ttu-id="2a0ef-109">ค่าเริ่มต้นโพรไฟล์การลงรายการบัญชีจะถูกกำหนดไว้ในแท็บด่วนบัญชีแยกประเภทและภาษี บนหน้าพารามิเตอร์บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts payable parameters page.</span></span> <span data-ttu-id="2a0ef-110">ค่าเริ่มต้นโพรไฟล์การลงรายการบัญชีจะรวมอยู่ในส่วนหัวของเอกสารใหม่โดยอัตโนมัติ ซึ่งคุณสามารถเปลี่ยนเป็นโพรไฟล์การลงรายการบัญชีอื่นได้หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="2a0ef-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="2a0ef-111">คุณยังสามารถเชื่อมโยงข้อกำหนดการลงรายการบัญชีกับชนิดการลงรายการบัญชีธุรกรรม ในหน้าข้อกำหนดการลงรายการบัญชีของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="2a0ef-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="2a0ef-112">ข้อกำหนดการลงรายการบัญชีจะควบคุมการลงรายการบัญชีขอธุรกรรมผู้จัดจำหน่ายไปยังบัญชีแยกประเภททั่วไปแทนข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a0ef-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="2a0ef-113">การสร้างการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a0ef-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="2a0ef-114">**การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="2a0ef-114">**Setup**</span></span>

<span data-ttu-id="2a0ef-115">ระบุบัญชีแยกประเภทที่จะใช้ในการลงรายการบัญชีธุรกรรมที่มีโพรไฟล์การลงบัญชีที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="2a0ef-116">เลือกรหัสบัญชี และหากเป็นไปได้ เลือกหมายเลขบัญชีหรือหมายเลขกลุ่มสำหรับโพรไฟล์การลงบัญชีที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="2a0ef-117">ในกระบวนการลงรายการบัญชี ข้อมูลโพรไฟล์การลงบัญชีที่เหมาะสมที่สุดสำหรับแต่ละธุรกรรมจะถูกระบุโดยการค้นหาชุดรหัสบัญชี หมายเลขบัญชี หรือส่วนผสมระหว่างกลุ่มและหมายเลขที่เจาะจงที่สุดตามระดับความสำคัญดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="2a0ef-118">ค่าฟิลด์ **รหัสบัญชี**</span><span class="sxs-lookup"><span data-stu-id="2a0ef-118">**Account code** field value</span></span> | <span data-ttu-id="2a0ef-119">ค่าฟิลด์ **หมายเลขบัญชี/กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="2a0ef-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="2a0ef-120">ระดับความสำคัญของการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2a0ef-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="2a0ef-121">**ตาราง**</span><span class="sxs-lookup"><span data-stu-id="2a0ef-121">**Table**</span></span>                    | <span data-ttu-id="2a0ef-122">บัญชีผู้จัดจำหน่ายที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="2a0ef-122">Specific vendor account</span></span>                     | <span data-ttu-id="2a0ef-123">1</span><span class="sxs-lookup"><span data-stu-id="2a0ef-123">1</span></span>               |
| <span data-ttu-id="2a0ef-124">**กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="2a0ef-124">**Group**</span></span>                    | <span data-ttu-id="2a0ef-125">กลุ่มผู้จัดจำหน่ายที่กำหนดให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2a0ef-125">vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="2a0ef-126">2</span><span class="sxs-lookup"><span data-stu-id="2a0ef-126">2</span></span>               |
| <span data-ttu-id="2a0ef-127">**ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="2a0ef-127">**All**</span></span>                      | <span data-ttu-id="2a0ef-128">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="2a0ef-128">Blank</span></span>                                       | <span data-ttu-id="2a0ef-129">3</span><span class="sxs-lookup"><span data-stu-id="2a0ef-129">3</span></span>               |

<span data-ttu-id="2a0ef-130">ถ้าคุณต้องการให้ธุรกรรมผู้จัดจำหน่ายทั้งหมดมีโพรไฟล์การลงบัญชีเหมือนกัน ให้ตั้งค่าเพียงหนึ่งโพรไฟล์การลงบัญชีในฟิลด์รหัสบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a0ef-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="2a0ef-131">ระบุค่าต่อไปนี้เพื่อตั้งค่าโพรไฟล์การลงรายการบัญชีของคุณ:</span><span class="sxs-lookup"><span data-stu-id="2a0ef-131">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a0ef-132">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="2a0ef-132">Field</span></span></th>
<th><span data-ttu-id="2a0ef-133">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2a0ef-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a0ef-134"><strong>โพรไฟล์การลงรายการบัญชี</strong></span><span class="sxs-lookup"><span data-stu-id="2a0ef-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="2a0ef-135">ป้อนรหัสสำหรับโพรไฟล์การลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a0ef-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="2a0ef-136">ตัวอย่างเช่น คุณสามารถสร้างโพรไฟล์การลงบัญชี 2 โพรไฟล์ เพื่อให้มีหนึ่งบัญชีสำหรับยอดดุลผู้จัดจำหน่ายในสกุลเงินในประเทศ และอีกบัญชีหนึ่งสำหรับยอดดุลผู้จัดจำหน่ายในสกุลเงินต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="2a0ef-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="2a0ef-137">คุณสามารถเรียกบัญชีหนึ่งว่าในประเทศ และอีกบัญชีหนึ่งว่าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="2a0ef-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a0ef-138"><strong>คำอธิบาย</strong></span><span class="sxs-lookup"><span data-stu-id="2a0ef-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="2a0ef-139">ป้อนคำอธิบายเกี่ยวโพรไฟล์การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a0ef-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a0ef-140"><strong>รหัสบัญชี</strong></span><span class="sxs-lookup"><span data-stu-id="2a0ef-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="2a0ef-141">ระบุว่าจะใช้โพรไฟล์การลงบัญชีกับผู้จัดจำหน่ายเฉพาะราย กลุ่มของผู้จัดจำหน่าย หรือผู้จัดจำหน่ายทั้งหมด:</span><span class="sxs-lookup"><span data-stu-id="2a0ef-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="2a0ef-142"><strong>ตาราง</strong> – กฎการลงรายการบัญชีที่ใช้กับผู้จัดจำหน่ายรายเดียว</span><span class="sxs-lookup"><span data-stu-id="2a0ef-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="2a0ef-143">เลือกบัญชีผู้จัดจำหน่ายในฟิลด์หมายเลขบัญชี/กลุ่ม</span><span class="sxs-lookup"><span data-stu-id="2a0ef-143">Select the vendor account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="2a0ef-144"><strong>กลุ่ม</strong> – กฎการลงรายการบัญชีที่ใช้กับกลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2a0ef-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="2a0ef-145">เลือกกลุ่มผู้จัดจำหน่ายในฟิลด์หมายเลขบัญชี/กลุ่ม</span><span class="sxs-lookup"><span data-stu-id="2a0ef-145">Select the vendor group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="2a0ef-146"><strong>ทั้งหมด</strong> – กฎการลงรายการบัญชีที่ใช้กับผู้จัดจำหน่ายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2a0ef-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="2a0ef-147">ปล่อยฟิลด์หมายเลขบัญชี/กลุ่มว่างไว้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a0ef-148"><strong>หมายเลขบัญชี/กลุ่ม</strong></span><span class="sxs-lookup"><span data-stu-id="2a0ef-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="2a0ef-149">ถ้าในฟิลด์รหัสบัญชีเลือกตารางไว้ ให้เลือกหมายเลขบัญชีของผู้จัดจำหน่ายที่เชื่อมโยงกับโพรไฟล์การลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a0ef-149">If Table is selected in the Account code field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="2a0ef-150">ถ้าเลือกกลุ่ม ให้เลือกกลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2a0ef-150">If Group is selected, select a vendor group.</span></span> <span data-ttu-id="2a0ef-151">ถ้าเลือกทั้งหมด ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a0ef-152"><strong>บัญชีสรุป</strong></span><span class="sxs-lookup"><span data-stu-id="2a0ef-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="2a0ef-153">เลือกรหัสบัญชีที่จะใช้เป็นบัญชีสรุปสำหรับผู้จัดจำหน่ายที่เกี่ยวข้องกับโพรไฟล์การลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a0ef-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="บันทึก" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="2a0ef-155"><strong>บันทึก</strong></span><span class="sxs-lookup"><span data-stu-id="2a0ef-155"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a0ef-156">ถ้าเลือกการสลับข้อกำหนดการลงรายการบัญชีในหน้าพารามิเตอร์บัญชีแยกประเภททั่วไป ข้อกำหนดการลงรายการบัญชีธุรกรรมของใบแจ้งหนี้ขอผู้จัดจำหน่ายจะถูกใช้แทนบัญชีสรุป</span><span class="sxs-lookup"><span data-stu-id="2a0ef-156">If the Use posting definitions toggle is selected in the General ledger parameters page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a0ef-157"><strong>ตัดรายการบัญชี</strong></span><span class="sxs-lookup"><span data-stu-id="2a0ef-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="2a0ef-158">เลือกบัญชีแยกประเภทที่มีสภาพคล่องที่ใช้สำหรับการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="2a0ef-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="2a0ef-159">ฟิลด์นี้จะพร้อมใช้งานเฉพาะเมื่อการคาดการณ์กระแสเงินสดถูกเปิดใช้งานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2a0ef-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a0ef-160"><strong>การชำระภาษีขายล่วงหน้า</strong></span><span class="sxs-lookup"><span data-stu-id="2a0ef-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="2a0ef-161">เลือกหมายเลขบัญชีสำหรับการชำระภาษีขายที่ได้รับล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="2a0ef-161">Select the account for sales tax payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="บันทึก" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="2a0ef-163"><strong>บันทึก</strong></span><span class="sxs-lookup"><span data-stu-id="2a0ef-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a0ef-164">โพรไฟล์การลงบัญชีที่ใช้งานเมื่อทำเครื่องหมายการชำระเงินเป็นการชำระเงินล่วงหน้า จะถูกเลื่อกในโพรไฟล์การลงรายการบัญชีกับฟิลด์ใบสำคัญสมุดรายวันการชำระเงินล่วงหน้า ในส่วนบัญชีแยกประเภทและภาษีขายของหน้าพารามิเตอร์บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-164">The posting profile that is used when the payment is marked as a prepayment is selected in the Posting profile with prepayment journal voucher field in the Ledger and sales tax area of the Accounts payable parameters page.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a0ef-165"><strong>บัญชีขาเข้า</strong></span><span class="sxs-lookup"><span data-stu-id="2a0ef-165"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="2a0ef-166">เลือกรหัสบัญชีที่ลงรายการบัญชีข้อมูลเกี่ยวกับใบแจ้งหนี้ของผู้จัดจำหน่ายที่ยังไม่ได้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="2a0ef-166">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="2a0ef-167">ข้อมูลจะถูกป้อนในสมุดรายวันทะเบียนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-167">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="2a0ef-168">ตัวอย่างเช่น ผู้ใช้ป้อนข้อมูลพื้นฐานเกี่ยวกับใบแจ้งหนี้ของผู้จัดจำหน่ายเมื่อได้รับในทะเบียนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-168">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="2a0ef-169">เมื่อลงรายการบัญชีทะเบียนใบแจ้งหนี้แล้ว ธุรกรรมที่ลงรายการบัญชีในบัญชีที่ป้อนไว้ที่นี่ และในฟิลด์บัญชีตรงข้าม</span><span class="sxs-lookup"><span data-stu-id="2a0ef-169">When the invoice register is posted, the transactions are posted to the account that is entered here and in the Offset account field.</span></span> <span data-ttu-id="2a0ef-170">เมื่อมีอนุมัติใบแจ้งหนี้แล้ว หนี้สินจะถูกโอนย้ายจากบัญชีการมาถึงไปยังบัญชีสรุปผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2a0ef-170">When the invoices are approved, the debt is transferred from the Arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a0ef-171"><strong>บัญชีตรงข้าม</strong></span><span class="sxs-lookup"><span data-stu-id="2a0ef-171"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="2a0ef-172">เลือกรหัสบัญชีที่ใช้สำหรับการออฟเซ็ตใบแจ้งหนี้ของผู้จัดจำหน่ายที่ยังไม่ได้อนุมัติ ซึ่งจะอัพเดตโดยใช้ทะเบียนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-172">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="2a0ef-173">บัญชีตรงข้ามทำหน้าที่เป็นบัญชีตรงข้ามสำหรับธุรกรรมที่ลงรายการบัญชีในบัญชีการมาถึง</span><span class="sxs-lookup"><span data-stu-id="2a0ef-173">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="2a0ef-174">ดังนั้น บัญชีประกอบด้วยการสั่งซื้อของผู้จัดจำหน่ายที่ยังไม่ได้รับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="2a0ef-174">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="2a0ef-175">**ข้อจำกัด**</span><span class="sxs-lookup"><span data-stu-id="2a0ef-175">**Table restrictions**</span></span>

<span data-ttu-id="2a0ef-176">สำหรับธุรกรรมที่มีโพรไฟล์การลงบัญชีที่เลือกไว้ ให้ระบุว่าธุรกรรมจะได้รับชำระเงินโดยอัตโนมัติ จะมีการคำนวณดอกเบี้ย และจะออกจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="2a0ef-176">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="2a0ef-177">คุณยังสามารถเลือกบัญชีที่จะใช้เมื่อธุรกรรมที่มีโพรไฟล์การลงบัญชีที่เลือกไว้ปิดลง</span><span class="sxs-lookup"><span data-stu-id="2a0ef-177">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="2a0ef-178">ระบุค่าต่อไปนี้เพื่อตั้งค่าโพรไฟล์การลงรายการบัญชีของคุณ:</span><span class="sxs-lookup"><span data-stu-id="2a0ef-178">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="2a0ef-179">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="2a0ef-179">Field</span></span>          | <span data-ttu-id="2a0ef-180">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2a0ef-180">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0ef-181">**การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="2a0ef-181">**Settlement**</span></span> | <span data-ttu-id="2a0ef-182">เลือกตัวเลือกนี้เพื่อเปิดใช้งานการชำระเงินของธุรกรรมที่มีโพรไฟล์การลงรายการบัญชีนี้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2a0ef-182">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="2a0ef-183">ถ้าไม่ได้เลือกตัวเลือกนี้ คุณต้องชำระธุรกรรมด้วยตนเองโดยใช้หน้าชำระธุรกรรมที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="2a0ef-183">If this option is cleared, you must manually settle transactions by using the Settle open transactions page.</span></span> |
| <span data-ttu-id="2a0ef-184">**ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="2a0ef-184">**Cancel**</span></span>     | <span data-ttu-id="2a0ef-185">เลือกตัวเลือกนี้ ถ้าคุณต้องการที่จะสามารถยกเลิกธุรกรรมที่มีโพรไฟล์การลงรายการบัญชีนี้ได้</span><span class="sxs-lookup"><span data-stu-id="2a0ef-185">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="2a0ef-186">**ปิดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="2a0ef-186">**Close**</span></span>      | <span data-ttu-id="2a0ef-187">เลือกโพรไฟล์การลงรายการบัญชีที่จะเปลี่ยนเมื่อธุรกรรมที่มีโพรไฟล์การลงรายการบัญชีนี้ปิดบัญชีแล้ว</span><span class="sxs-lookup"><span data-stu-id="2a0ef-187">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="2a0ef-188">ธุรกรรมถือว่าปิดบัญชีแล้วเมื่อมีการชำระเต็มจำนวน</span><span class="sxs-lookup"><span data-stu-id="2a0ef-188">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |





