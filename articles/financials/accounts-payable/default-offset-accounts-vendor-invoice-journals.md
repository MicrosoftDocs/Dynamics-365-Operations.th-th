---
title: "บัญชีตรงข้ามเริ่มต้นสำหรับสมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่ายและสมุดรายวันการอนุมัติใบแจ้งหนี้"
description: "หัวข้อนี้จะช่วยคุณในการกำหนดตำแหน่งที่คุณควรจะมอบหมายบัญชีเริ่มต้นสำหรับสมุดรายวันใบแจ้งหนี้"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 90b24e8e00a78c122e0f7c712a694c9c62bd4824
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="c0aa5-103">บัญชีตรงข้ามเริ่มต้นสำหรับสมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่ายและสมุดรายวันการอนุมัติใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c0aa5-103">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="c0aa5-104">บัญชีตรงข้ามเริ่มต้นถูกใช้ในหน้าสมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่ายต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c0aa5-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="c0aa5-105">สมุดรายวันใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c0aa5-105">Invoice journal</span></span>
-   <span data-ttu-id="c0aa5-106">สมุดรายวันการอนุมัติใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c0aa5-106">Invoice approval journal</span></span>

<span data-ttu-id="c0aa5-107">ใช้ตารางต่อไปนี้เพื่อช่วยให้คุณกำหนดตำแหน่งที่ควรจะมอบหมายบัญชีเริ่มต้นสำหรับสมุดรายวันใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c0aa5-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0aa5-108">ตั้งค่าบัญชีเริ่มต้นที่นี่</span><span class="sxs-lookup"><span data-stu-id="c0aa5-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="c0aa5-109">ที่มีค่าบัญชีเริ่มต้นมาให้</span><span class="sxs-lookup"><span data-stu-id="c0aa5-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="c0aa5-110">ตัวเลือกนี้มีผลกระทบต่อการประมวลผลอย่างไร</span><span class="sxs-lookup"><span data-stu-id="c0aa5-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="c0aa5-111">เมื่อคุณควรใช้ตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="c0aa5-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0aa5-112"><strong>กลุ่มผู้จัดจำหน่าย</strong>– ตั้งค่าบัญชีตรงข้ามเริ่มต้นสำหรับกลุ่มผู้จัดจำหน่ายในหน้า <strong>การตั้งค่าบัญชีเริ่มต้น</strong> ซึ่งคุณสามารถเปิดจากหน้า <strong>กลุ่มผู้จัดจำหน่าย</strong></span><span class="sxs-lookup"><span data-stu-id="c0aa5-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="c0aa5-113">บัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c0aa5-113">Vendor account</span></span></li>
<li><span data-ttu-id="c0aa5-114">รายการสมุดรายวันสำหรับบัญชีผู้จัดจำหน่ายในกลุ่มผู้จัดจำหน่าย ถ้าไม่ได้ระบุบัญชีเริ่มต้นสำหรับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c0aa5-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="c0aa5-115">แสดงบัญชีตรงข้ามเริ่มต้นสำหรับกลุ่มผู้จัดจำหน่ายเป็นบัญชีตรงข้ามเริ่มต้นสำหรับผู้จัดจำหน่ายในหน้า <strong>การตั้งค่าบัญชีเริ่มต้น</strong></span><span class="sxs-lookup"><span data-stu-id="c0aa5-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="c0aa5-116">คุณสามารถเปิดหน้านี้จากหน้า <strong>รายการผู้จัดจำหน่ายทั้งหมด</strong></span><span class="sxs-lookup"><span data-stu-id="c0aa5-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="c0aa5-117">ใช้ตัวเลือกนี้ถ้าโดยทั่วไปคุณชำระค่าจ้างสำหรับชนิดของสิ่งเดียวกันจากกลุ่มผู้จัดจำหน่ายเดียวกันตามช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="c0aa5-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0aa5-118"><strong>บัญชีผู้จัดจำหน่าย</strong> – ตั้งค่าบัญชีตรงข้ามเริ่มต้นสำหรับกลุ่มผู้จัดจำหน่ายในหน้า <strong>การตั้งค่าบัญชีเริ่มต้น</strong> ซึ่งคุณสามารถเปิดจากหน้า <strong>กลุ่มผู้จัดจำหน่าย</strong></span><span class="sxs-lookup"><span data-stu-id="c0aa5-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="c0aa5-119">รายการสมุดรายวันสำหรับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c0aa5-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="c0aa5-120">บัญชีตรงข้ามเริ่มต้นสำหรับบัญชีผู้จัดจำหน่ายจะแสดงเป็นบัญชีตรงข้ามเริ่มต้นสำหรับรายการสมุดรายวันสำหรับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c0aa5-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="c0aa5-121">ใช้ตัวเลือกนี้ถ้าโดยทั่วไปคุณชำระค่าจ้างสำหรับชนิดของสิ่งเดียวกันจากผู้จัดจำหน่ายเดียวกันตามช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="c0aa5-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0aa5-122"><strong>ชื่อสมุดรายวัน</strong> – ตั้งค่าบัญชีตรงข้ามเริ่มต้นสำหรับสมุดรายวันในหน้า <strong>ชื่อสมุดรายวัน</strong></span><span class="sxs-lookup"><span data-stu-id="c0aa5-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="c0aa5-123">เลือกตัวเลือก <strong>บัญชีตรงข้ามคงที่</strong></span><span class="sxs-lookup"><span data-stu-id="c0aa5-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="c0aa5-124">โปรดทราบว่า คุณไม่สามารถ&#39;ระบุบัญชีตรงข้ามเริ่มต้นในชื่อสมุดรายวันได้ ถ้าชนิดสมุดรายวันของชื่อสมุดรายวันเป็น <strong>ทะเบียนใบแจ้งหนี้</strong> หรือ <strong>การอนุมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="c0aa5-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="c0aa5-125">หัวข้อสมุดรายวันที่ใช้ชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0aa5-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="c0aa5-126">รายการสมุดรายวันในสมุดรายวันที่ใช้ชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0aa5-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="c0aa5-127">ถ้าตัวเลือก <strong>บัญชีตรงข้ามคงที่</strong> ในหน้า <strong>ชื่อสมุดรายวัน</strong> ถูกเลือก บัญชีตรงข้ามสำหรับชื่อสมุดรายวันจะแทนที่บัญชีตรงข้ามเริ่มต้นสำหรับผู้จัดจำหน่ายหรือกลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c0aa5-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="c0aa5-128">ใช้ตัวเลือกนี้เพื่อตั้งค่าสมุดรายวันสำหรับต้นทุนและค่าใช้จ่ายเฉพาะที่จะถูกเรียกเก็บไปยังบัญชีเฉพาะ โดยไม่คำนึงว่าผู้จัดจำหน่ายนั้นเป็นของผู้จัดจำหน่ายหรือกลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c0aa5-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0aa5-129"><strong>ชื่อสมุดรายวัน</strong> – ตั้งค่าบัญชีตรงข้ามเริ่มต้นสำหรับสมุดรายวันในหน้า <strong>ชื่อสมุดรายวัน</strong></span><span class="sxs-lookup"><span data-stu-id="c0aa5-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="c0aa5-130">ยกเลิกการเลือกตัวเลือก <strong>บัญชีตรงข้ามคงที่</strong></span><span class="sxs-lookup"><span data-stu-id="c0aa5-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="c0aa5-131">โปรดทราบว่า คุณไม่สามารถ&#39;ระบุบัญชีตรงข้ามเริ่มต้นในชื่อสมุดรายวันได้ ถ้าชนิดสมุดรายวันของชื่อสมุดรายวันเป็น <strong>ทะเบียนใบแจ้งหนี้</strong> หรือ <strong>การอนุมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="c0aa5-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="c0aa5-132">ส่วนหัวของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0aa5-132">Journal header</span></span></li>
<li><span data-ttu-id="c0aa5-133">รายการสมุดรายวันในสมุดรายวันที่ใช้ชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0aa5-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="c0aa5-134">รายการเริ่มต้นเหล่านี้จะใช้ในหน้าหัวข้อของสมุดรายวันและบัญชีตรงข้ามในแบบฟอร์มหัวข้อของสมุดรายวัน ซึ่งใช้เป็นรายการเริ่มต้นในหน้าใบสำคัญสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0aa5-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="c0aa5-135">บัญชีเริ่มต้นจากหน้า <strong>ชื่อสมุดรายวัน </strong>จะใช้เฉพาะเมื่อไม่ได้ตั้งค่าบัญชีเริ่มต้นสำหรับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c0aa5-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="c0aa5-136">ใช้ตัวเลือกนี้เพื่อตั้งค่าบัญชีเริ่มต้นที่จะใช้ เมื่อไม่มี&#39;การกำหนดบัญชีตรงข้ามของผู้จัดจำหน่ายเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0aa5-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0aa5-137"><strong>หัวข้อสมุดรายวัน</strong> – ตั้งค่าบัญชีตรงข้ามเริ่มต้นสำหรับสมุดรายวันเพื่อใช้เป็นรายการเริ่มต้นในหน้าใบสำคัญสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0aa5-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="c0aa5-138">โปรดทราบว่า คุณไม่สามารถ&#39;ระบุบัญชีตรงข้ามเริ่มต้นในหัวข้อสมุดรายวันได้ ถ้าชนิดสมุดรายวันของชื่อสมุดรายวันเป็น <strong>ทะเบียนใบแจ้งหนี้</strong> หรือ <strong>การอนุมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="c0aa5-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="c0aa5-139">รายการสมุดรายวันในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0aa5-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="c0aa5-140">บัญชีตรงข้ามเริ่มต้นสำหรับสมุดรายวันจะถูกใช้เป็นรายการเริ่มต้นในหน้าใบสำคัญสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0aa5-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="c0aa5-141">ใช้ตัวเลือกนี้เพื่อช่วยป้อนข้อมูลให้เร็วขึ้น ถ้ารายการส่วนใหญ่ในสมุดรายวันมีบัญชีตรงข้ามเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c0aa5-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






