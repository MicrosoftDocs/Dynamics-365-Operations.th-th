---
title: โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่าย
description: โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่ายควบคุมการลงรายการบัญชีของธุรกรรมผู้จัดจำหน่ายที่บัญชีแยกประเภททั่วไป
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43450c5f7ab8295b896b591880da9d0bddd955cf
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835357"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="bf051-103">โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="bf051-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf051-104">โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่ายควบคุมการลงรายการบัญชีของธุรกรรมผู้จัดจำหน่ายที่บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="bf051-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="bf051-105">โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="bf051-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="bf051-106">โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่ายช่วยให้คุณสามารถกำหนดบัญชีแยกประเภททั่วไปและการตั้งค่าเอกสารให้กับผู้จัดจำหน่ายทั้งหมด กลุ่มผู้จัดจำหน่าย หรือผู้จัดจำหน่ายรายเดียวได้</span><span class="sxs-lookup"><span data-stu-id="bf051-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors, or a single vendor.</span></span> <span data-ttu-id="bf051-107">การตั้งค่าเหล่านี้จะถูกใช้เมื่อคุณสร้างใบสั่งซื้อ ใบแจ้งหนี้ของผู้จัดจำหน่าย และการชำระเงินสด</span><span class="sxs-lookup"><span data-stu-id="bf051-107">These settings will be used when you create purchase orders, vendor invoices, and cash payments.</span></span> <span data-ttu-id="bf051-108">สำหรับบางธุรกรรม คุณสามารถเลือกโพรไฟล์การลงรายการบัญชีที่แตกต่าง และมีระดับความสำคัญเหนือกว่าโพรไฟล์การลงรายการบัญชีที่ตั้งค่าไว้สำหรับธุรกรรมในหน้านี้</span><span class="sxs-lookup"><span data-stu-id="bf051-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions on this page.</span></span> <span data-ttu-id="bf051-109">โพรไฟล์การลงรายการบัญชีเริ่มต้นจะถูกกำหนดไว้ใน FastTab **บัญชีแยกประเภทและภาษีขาย** บนหน้า **พารามิเตอร์บัญชีเจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="bf051-109">The default posting profile is defined on the **Ledger and Sales Tax** FastTab on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="bf051-110">จากนั้น โพรไฟล์การลงรายการบัญชีเริ่มต้นจะถูกรวมอยู่ในส่วนหัวของเอกสารใหม่โดยอัตโนมัติ ที่ซึ่งคุณสามารถเปลี่ยนเป็นโพรไฟล์การลงรายการบัญชีอื่นได้ หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="bf051-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile, if needed.</span></span>

<span data-ttu-id="bf051-111">นอกจากนี้ คุณยังสามารถเชื่อมโยงข้อกำหนดการลงรายการบัญชีกับชนิดการลงรายการบัญชีธุรกรรมในหน้า **ข้อกำหนดการลงรายการบัญชีของธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="bf051-111">You can also associate posting definitions with transaction posting types on the **Transaction posting definitions** page.</span></span> <span data-ttu-id="bf051-112">ข้อกำหนดการลงรายการบัญชีจะควบคุมการลงรายการบัญชีขอธุรกรรมผู้จัดจำหน่ายไปยังบัญชีแยกประเภททั่วไปแทนข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="bf051-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="bf051-113">การสร้างการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="bf051-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="bf051-114">**การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="bf051-114">**Setup**</span></span>

<span data-ttu-id="bf051-115">ระบุบัญชีแยกประเภทที่จะใช้ในการลงรายการบัญชีธุรกรรมที่มีโพรไฟล์การลงบัญชีที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="bf051-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="bf051-116">เลือกรหัสบัญชี และหากเป็นไปได้ เลือกหมายเลขบัญชีหรือหมายเลขกลุ่มสำหรับโพรไฟล์การลงบัญชีที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="bf051-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="bf051-117">ในกระบวนการลงรายการบัญชี ข้อมูลโพรไฟล์การลงรายการบัญชีที่เหมาะสมที่สุดสำหรับธุรกรรมแต่ละรายการจะถูกระบุโดยการค้นหารหัสบัญชี หมายเลขบัญชี หรือส่วนผสมระหว่างกลุ่มและหมายเลขที่เจาะจงที่สุด ตามระดับความสำคัญดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bf051-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority.</span></span>

| <span data-ttu-id="bf051-118">ค่าฟิลด์ **รหัสบัญชี**</span><span class="sxs-lookup"><span data-stu-id="bf051-118">**Account code** field value</span></span> | <span data-ttu-id="bf051-119">ค่าฟิลด์ **หมายเลขบัญชี/กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="bf051-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="bf051-120">ระดับความสำคัญของการค้นหา</span><span class="sxs-lookup"><span data-stu-id="bf051-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="bf051-121">**ตาราง**</span><span class="sxs-lookup"><span data-stu-id="bf051-121">**Table**</span></span>                    | <span data-ttu-id="bf051-122">บัญชีผู้จัดจำหน่ายที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="bf051-122">Specific vendor account</span></span>                     | <span data-ttu-id="bf051-123">1</span><span class="sxs-lookup"><span data-stu-id="bf051-123">1</span></span>               |
| <span data-ttu-id="bf051-124">**กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="bf051-124">**Group**</span></span>                    | <span data-ttu-id="bf051-125">กลุ่มผู้จัดจำหน่ายที่ถูกกำหนดให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="bf051-125">Vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="bf051-126">2</span><span class="sxs-lookup"><span data-stu-id="bf051-126">2</span></span>               |
| <span data-ttu-id="bf051-127">**ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="bf051-127">**All**</span></span>                      | <span data-ttu-id="bf051-128">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="bf051-128">Blank</span></span>                                       | <span data-ttu-id="bf051-129">3</span><span class="sxs-lookup"><span data-stu-id="bf051-129">3</span></span>               |

<span data-ttu-id="bf051-130">ถ้าคุณต้องการให้ธุรกรรมของผู้จัดจำหน่ายทั้งหมดมีโพรไฟล์การลงรายการบัญชีเหมือนกัน ให้ตั้งค่าโพรไฟล์การลงรายการบัญชีเพียงหนึ่งรายการด้วย **ทั้งหมด** ในฟิลด์ **รหัสบัญชี**</span><span class="sxs-lookup"><span data-stu-id="bf051-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with **All** in the **Account code** field.</span></span> <span data-ttu-id="bf051-131">ระบุค่าต่อไปนี้เพื่อตั้งค่าโพรไฟล์การลงรายการบัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="bf051-131">Specify the following values to set up your posting profile.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bf051-132">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="bf051-132">Field</span></span></th>
<th><span data-ttu-id="bf051-133">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bf051-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf051-134"><strong>โพรไฟล์การลงรายการบัญชี</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="bf051-135">ป้อนรหัสสำหรับโพรไฟล์การลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="bf051-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="bf051-136">ตัวอย่างเช่น คุณสามารถสร้างโพรไฟล์การลงบัญชี 2 โพรไฟล์ เพื่อให้มีหนึ่งบัญชีสำหรับยอดดุลผู้จัดจำหน่ายในสกุลเงินในประเทศ และอีกบัญชีหนึ่งสำหรับยอดดุลผู้จัดจำหน่ายในสกุลเงินต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="bf051-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="bf051-137">คุณสามารถเรียกบัญชีหนึ่งว่าในประเทศ และอีกบัญชีหนึ่งว่าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="bf051-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf051-138"><strong>คำอธิบาย</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="bf051-139">ป้อนคำอธิบายเกี่ยวโพรไฟล์การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="bf051-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf051-140"><strong>รหัสบัญชี</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="bf051-141">ระบุว่าจะใช้โพรไฟล์การลงบัญชีกับผู้จัดจำหน่ายเฉพาะราย กลุ่มของผู้จัดจำหน่าย หรือผู้จัดจำหน่ายทั้งหมด:</span><span class="sxs-lookup"><span data-stu-id="bf051-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="bf051-142"><strong>ตาราง</strong> – กฎการลงรายการบัญชีที่ใช้กับผู้จัดจำหน่ายรายเดียว</span><span class="sxs-lookup"><span data-stu-id="bf051-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="bf051-143">เลือกบัญชีผู้จัดจำหน่ายในฟิลด์ <strong>หมายเลขบัญชี/กลุ่ม</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-143">Select the vendor account in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="bf051-144"><strong>กลุ่ม</strong> – กฎการลงรายการบัญชีที่ใช้กับกลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="bf051-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="bf051-145">เลือกกลุ่มผู้จัดจำหน่ายในฟิลด์ <strong>หมายเลขบัญชี/กลุ่ม</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-145">Select the vendor group in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="bf051-146"><strong>ทั้งหมด</strong> – กฎการลงรายการบัญชีที่ใช้กับผู้จัดจำหน่ายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="bf051-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="bf051-147">ปล่อยฟิลด์ <strong>หมายเลขบัญชี/กลุ่ม</strong> ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="bf051-147">Leave the <strong>Account/Group number</strong> field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf051-148"><strong>หมายเลขบัญชี/กลุ่ม</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="bf051-149">ถ้ามีการเลือก <strong>ตาราง</strong> ในฟิลด์ <strong>รหัสบัญชี</strong> ให้เลือกหมายเลขบัญชีของผู้จัดจำหน่ายที่เชื่อมโยงกับโพรไฟล์การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="bf051-149">If <strong>Table</strong> is selected in the <strong>Account code</strong> field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="bf051-150">ถ้ามีการเลือก <strong>กลุ่ม</strong> ให้เลือกกลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="bf051-150">If <strong>Group</strong> is selected, select a vendor group.</span></span> <span data-ttu-id="bf051-151">ถ้ามีการเลือก <strong>ทั้งหมด</strong> ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="bf051-151">If <strong>All</strong> is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf051-152"><strong>บัญชีสรุป</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="bf051-153">เลือกรหัสบัญชีที่จะใช้เป็นบัญชีสรุปสำหรับผู้จัดจำหน่ายที่เกี่ยวข้องกับโพรไฟล์การลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="bf051-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span> <span data-ttu-id="bf051-154">จะมีการทำเครื่องหมายพารามิเตอร์ <strong>ไม่อนุญาตให้มีการป้อนข้อมูลด้วยตนเอง</strong> สำหรับบัญชีหลักนี้</span><span class="sxs-lookup"><span data-stu-id="bf051-154">The <strong>Do not allow manual entry</strong> parameter for this main account will be marked.</span></span> <span data-ttu-id="bf051-155">ถ้าคุณลบบัญชีนี้ออกจากโพรไฟล์การลงรายการบัญชีในเวลาต่อมา ให้ตรวจสอบความถูกต้องการตั้งค่า <strong>ไม่อนุญาตให้มีการตั้งค่าการป้อนข้อมูลด้วยตนเอง</strong> บนหน้า <strong>บัญชีหลัก</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-155">If you subsequently remove this account from the posting profile, validate the <strong>Do not allow manual entry</strong> setting on the <strong>Main accounts</strong> page.</span></span> 
<p><span data-ttu-id="bf051-156"><strong>หมายเหตุ:</strong> ถ้าตัวเลือก <strong>ใช้ข้อกำหนดการลงรายการบัญชี</strong> ถูกเลือกในหน้า <strong>พารามิเตอร์บัญชีแยกประเภททั่วไป</strong> ข้อกำหนดการลงรายการบัญชีธุรกรรมสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายจะถูกใช้แทนบัญชีสรุป</span><span class="sxs-lookup"><span data-stu-id="bf051-156"><strong>Note:</strong> If the <strong>Use posting definitions</strong> option is selected on the <strong>General ledger parameters</strong> page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf051-157"><strong>ตัดรายการบัญชี</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="bf051-158">เลือกบัญชีแยกประเภทที่มีสภาพคล่องที่ใช้สำหรับการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="bf051-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="bf051-159">ฟิลด์นี้จะพร้อมใช้งานเฉพาะเมื่อการคาดการณ์กระแสเงินสดถูกเปิดใช้งานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="bf051-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf051-160"><strong>การชำระภาษีขายล่วงหน้า</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="bf051-161">เลือกหมายเลขบัญชีสำหรับการชำระภาษีขายที่ได้รับล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="bf051-161">Select the account for sales tax payments that are received in advance.</span></span>
<p><span data-ttu-id="bf051-162"><strong>หมายเหตุ:</strong> โพรไฟล์การลงรายการบัญชีที่ใช้งานเมื่อมีการทำเครื่องหมายการชำระเงินเป็นการชำระเงินล่วงหน้า จะถูกเลือกในโพรไฟล์ <strong>การลงรายการบัญชี</strong> ที่มีฟิลด์ <strong>ใบสำคัญสมุดรายวันการชำระเงินล่วงหน้า</strong> ในพื้นที่ <strong>บัญชีแยกประเภทและภาษีขาย</strong> ในหน้า <strong>พารามิเตอร์บัญชีเจ้าหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-162"><strong>Note:</strong> The posting profile that is used when the payment is marked as a prepayment is selected in the <strong>Posting</strong> profile with <strong>Prepayment journal voucher</strong> field in the <strong>Ledger and sales tax</strong> area on the <strong>Accounts payable parameters</strong> page.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf051-163"><strong>บัญชีขาเข้า</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-163"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="bf051-164">เลือกรหัสบัญชีที่ลงรายการบัญชีข้อมูลเกี่ยวกับใบแจ้งหนี้ของผู้จัดจำหน่ายที่ยังไม่ได้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="bf051-164">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="bf051-165">ข้อมูลจะถูกป้อนในสมุดรายวันทะเบียนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="bf051-165">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="bf051-166">ตัวอย่างเช่น ผู้ใช้ป้อนข้อมูลพื้นฐานเกี่ยวกับใบแจ้งหนี้ของผู้จัดจำหน่ายเมื่อได้รับในทะเบียนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="bf051-166">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="bf051-167">เมื่อลงรายการบัญชีทะเบียนใบแจ้งหนี้แล้ว ธุรกรรมจะถูกลงรายการบัญชีในบัญชีที่ป้อนไว้ที่นี่ และในฟิลด์ <strong>บัญชีตรงข้าม</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-167">When the invoice register is posted, the transactions are posted to the account that is entered here and in the <strong>Offset account</strong> field.</span></span> <span data-ttu-id="bf051-168">เมื่อมีการอนุมัติใบแจ้งหนี้แล้ว หนี้สินจะถูกโอนย้ายจากบัญชีการมาถึงไปยังบัญชีสรุปผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="bf051-168">When the invoices are approved, the debt is transferred from the arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf051-169"><strong>บัญชีตรงข้าม</strong></span><span class="sxs-lookup"><span data-stu-id="bf051-169"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="bf051-170">เลือกรหัสบัญชีที่ใช้สำหรับการออฟเซ็ตใบแจ้งหนี้ของผู้จัดจำหน่ายที่ยังไม่ได้อนุมัติ ซึ่งจะอัพเดตโดยใช้ทะเบียนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="bf051-170">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="bf051-171">บัญชีตรงข้ามทำหน้าที่เป็นบัญชีตรงข้ามสำหรับธุรกรรมที่ลงรายการบัญชีในบัญชีการมาถึง</span><span class="sxs-lookup"><span data-stu-id="bf051-171">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="bf051-172">ดังนั้น บัญชีประกอบด้วยการสั่งซื้อของผู้จัดจำหน่ายที่ยังไม่ได้รับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="bf051-172">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="bf051-173">**ข้อจำกัด**</span><span class="sxs-lookup"><span data-stu-id="bf051-173">**Table restrictions**</span></span>

<span data-ttu-id="bf051-174">สำหรับธุรกรรมที่มีโพรไฟล์การลงบัญชีที่เลือกไว้ ให้ระบุว่าธุรกรรมจะได้รับชำระเงินโดยอัตโนมัติ จะมีการคำนวณดอกเบี้ย และจะออกจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="bf051-174">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="bf051-175">คุณยังสามารถเลือกบัญชีที่จะใช้เมื่อธุรกรรมที่มีโพรไฟล์การลงบัญชีที่เลือกไว้ปิดลง</span><span class="sxs-lookup"><span data-stu-id="bf051-175">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="bf051-176">ระบุค่าต่อไปนี้เพื่อตั้งค่าโพรไฟล์การลงรายการบัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="bf051-176">Specify the following values to set up your posting profile</span></span>

| <span data-ttu-id="bf051-177">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="bf051-177">Field</span></span>          | <span data-ttu-id="bf051-178">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bf051-178">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf051-179">**ชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="bf051-179">**Settlement**</span></span> | <span data-ttu-id="bf051-180">เลือกตัวเลือกนี้เพื่อเปิดใช้งานการชำระเงินของธุรกรรมที่มีโพรไฟล์การลงรายการบัญชีนี้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bf051-180">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="bf051-181">ถ้าไม่ได้เลือกตัวเลือกนี้ คุณต้องชำระธุรกรรมด้วยตนเองโดยใช้หน้า **ชำระธุรกรรมที่เปิดอยู่**</span><span class="sxs-lookup"><span data-stu-id="bf051-181">If this option is cleared, you must manually settle transactions by using the **Settle open transactions** page.</span></span> |
| <span data-ttu-id="bf051-182">**ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="bf051-182">**Cancel**</span></span>     | <span data-ttu-id="bf051-183">เลือกตัวเลือกนี้ ถ้าคุณต้องการที่จะสามารถยกเลิกธุรกรรมที่มีโพรไฟล์การลงรายการบัญชีนี้ได้</span><span class="sxs-lookup"><span data-stu-id="bf051-183">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="bf051-184">**ปิดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="bf051-184">**Close**</span></span>      | <span data-ttu-id="bf051-185">เลือกโพรไฟล์การลงรายการบัญชีที่จะเปลี่ยนเมื่อธุรกรรมที่มีโพรไฟล์การลงรายการบัญชีนี้ปิดบัญชีแล้ว</span><span class="sxs-lookup"><span data-stu-id="bf051-185">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="bf051-186">ธุรกรรมถือว่าปิดบัญชีแล้วเมื่อมีการชำระเต็มจำนวน</span><span class="sxs-lookup"><span data-stu-id="bf051-186">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |
