---
title: "บัญชีตรงข้ามเริ่มต้นสำหรับสมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่ายและสมุดรายวันการอนุมัติใบแจ้งหนี้"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2b62eafc71b5d1ad4eaaf252efd1dcbb97b86f3
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="17bf6-102">บัญชีตรงข้ามเริ่มต้นสำหรับสมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่ายและสมุดรายวันการอนุมัติใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="17bf6-102">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="17bf6-103">บัญชีตรงข้ามเริ่มต้นถูกใช้ในหน้าสมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่ายต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="17bf6-103">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="17bf6-104">สมุดรายวันใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="17bf6-104">Invoice journal</span></span>
-   <span data-ttu-id="17bf6-105">สมุดรายวันการอนุมัติใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="17bf6-105">Invoice approval journal</span></span>

<span data-ttu-id="17bf6-106">ใช้ตารางต่อไปนี้เพื่อช่วยให้คุณกำหนดตำแหน่งที่ควรจะมอบหมายบัญชีเริ่มต้นสำหรับสมุดรายวันใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="17bf6-106">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17bf6-107">ตั้งค่าบัญชีเริ่มต้นที่นี่</span><span class="sxs-lookup"><span data-stu-id="17bf6-107">Set up default accounts here</span></span></th>
<th><span data-ttu-id="17bf6-108">ที่มีค่าบัญชีเริ่มต้นมาให้</span><span class="sxs-lookup"><span data-stu-id="17bf6-108">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="17bf6-109">ตัวเลือกนี้มีผลกระทบต่อการประมวลผลอย่างไร</span><span class="sxs-lookup"><span data-stu-id="17bf6-109">How this option affects processing</span></span></th>
<th><span data-ttu-id="17bf6-110">เมื่อคุณควรใช้ตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="17bf6-110">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17bf6-111"><strong>กลุ่มผู้จัดจำหน่าย</strong>– ตั้งค่าบัญชีตรงข้ามเริ่มต้นสำหรับกลุ่มผู้จัดจำหน่ายในหน้า <strong>การตั้งค่าบัญชีเริ่มต้น</strong> ซึ่งคุณสามารถเปิดจากหน้า <strong>กลุ่มผู้จัดจำหน่าย</strong></span><span class="sxs-lookup"><span data-stu-id="17bf6-111"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="17bf6-112">บัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="17bf6-112">Vendor account</span></span></li>
<li><span data-ttu-id="17bf6-113">รายการสมุดรายวันสำหรับบัญชีผู้จัดจำหน่ายในกลุ่มผู้จัดจำหน่าย ถ้าไม่ได้ระบุบัญชีเริ่มต้นสำหรับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="17bf6-113">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="17bf6-114">แสดงบัญชีตรงข้ามเริ่มต้นสำหรับกลุ่มผู้จัดจำหน่ายเป็นบัญชีตรงข้ามเริ่มต้นสำหรับผู้จัดจำหน่ายในหน้า <strong>การตั้งค่าบัญชีเริ่มต้น</strong></span><span class="sxs-lookup"><span data-stu-id="17bf6-114">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="17bf6-115">คุณสามารถเปิดหน้านี้จากหน้า <strong>รายการผู้จัดจำหน่ายทั้งหมด</strong></span><span class="sxs-lookup"><span data-stu-id="17bf6-115">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="17bf6-116">ใช้ตัวเลือกนี้ถ้าโดยทั่วไปคุณชำระค่าจ้างสำหรับชนิดของสิ่งเดียวกันจากกลุ่มผู้จัดจำหน่ายเดียวกันตามช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="17bf6-116">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17bf6-117"><strong>บัญชีผู้จัดจำหน่าย</strong> – ตั้งค่าบัญชีตรงข้ามเริ่มต้นสำหรับกลุ่มผู้จัดจำหน่ายในหน้า <strong>การตั้งค่าบัญชีเริ่มต้น</strong> ซึ่งคุณสามารถเปิดจากหน้า <strong>กลุ่มผู้จัดจำหน่าย</strong></span><span class="sxs-lookup"><span data-stu-id="17bf6-117"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="17bf6-118">รายการสมุดรายวันสำหรับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="17bf6-118">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="17bf6-119">บัญชีตรงข้ามเริ่มต้นสำหรับบัญชีผู้จัดจำหน่ายจะแสดงเป็นบัญชีตรงข้ามเริ่มต้นสำหรับรายการสมุดรายวันสำหรับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="17bf6-119">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="17bf6-120">ใช้ตัวเลือกนี้ถ้าโดยทั่วไปคุณชำระค่าจ้างสำหรับชนิดของสิ่งเดียวกันจากผู้จัดจำหน่ายเดียวกันตามช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="17bf6-120">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17bf6-121"><strong>ชื่อสมุดรายวัน</strong> – ตั้งค่าบัญชีตรงข้ามเริ่มต้นสำหรับสมุดรายวันในหน้า <strong>ชื่อสมุดรายวัน</strong></span><span class="sxs-lookup"><span data-stu-id="17bf6-121"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="17bf6-122">เลือกตัวเลือก <strong>บัญชีตรงข้ามคงที่</strong></span><span class="sxs-lookup"><span data-stu-id="17bf6-122">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="17bf6-123">โปรดทราบว่า คุณไม่สามารถระบุบัญชีตรงข้ามเริ่มต้นในชื่อสมุดรายวัน ถ้าชนิดสมุดรายวันของชื่อสมุดรายวันเป็น <strong>ทะเบียนใบแจ้งหนี้</strong> หรือ <strong>การอนุมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="17bf6-123">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="17bf6-124">หัวข้อสมุดรายวันที่ใช้ชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="17bf6-124">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="17bf6-125">รายการสมุดรายวันในสมุดรายวันที่ใช้ชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="17bf6-125">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="17bf6-126">ถ้าตัวเลือก <strong>บัญชีตรงข้ามคงที่</strong> ในหน้า <strong>ชื่อสมุดรายวัน</strong> ถูกเลือก บัญชีตรงข้ามสำหรับชื่อสมุดรายวันจะแทนที่บัญชีตรงข้ามเริ่มต้นสำหรับผู้จัดจำหน่ายหรือกลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="17bf6-126">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="17bf6-127">ใช้ตัวเลือกนี้เพื่อตั้งค่าสมุดรายวันสำหรับต้นทุนและค่าใช้จ่ายเฉพาะที่จะถูกเรียกเก็บไปยังบัญชีเฉพาะ โดยไม่คำนึงว่าผู้จัดจำหน่ายนั้นเป็นของผู้จัดจำหน่ายหรือกลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="17bf6-127">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17bf6-128"><strong>ชื่อสมุดรายวัน</strong> – ตั้งค่าบัญชีตรงข้ามเริ่มต้นสำหรับสมุดรายวันในหน้า <strong>ชื่อสมุดรายวัน</strong></span><span class="sxs-lookup"><span data-stu-id="17bf6-128"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="17bf6-129">ยกเลิกการเลือกตัวเลือก <strong>บัญชีตรงข้ามคงที่</strong></span><span class="sxs-lookup"><span data-stu-id="17bf6-129">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="17bf6-130">โปรดทราบว่า คุณไม่สามารถระบุบัญชีตรงข้ามเริ่มต้นในชื่อสมุดรายวัน ถ้าชนิดสมุดรายวันของชื่อสมุดรายวันเป็น <strong>ทะเบียนใบแจ้งหนี้</strong> หรือ <strong>การอนุมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="17bf6-130">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="17bf6-131">ส่วนหัวของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="17bf6-131">Journal header</span></span></li>
<li><span data-ttu-id="17bf6-132">รายการสมุดรายวันในสมุดรายวันที่ใช้ชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="17bf6-132">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="17bf6-133">รายการเริ่มต้นเหล่านี้จะใช้ในหน้าหัวข้อของสมุดรายวันและบัญชีตรงข้ามในแบบฟอร์มหัวข้อของสมุดรายวัน ซึ่งใช้เป็นรายการเริ่มต้นในหน้าใบสำคัญสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="17bf6-133">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="17bf6-134">บัญชีเริ่มต้นจากหน้า <strong>ชื่อสมุดรายวัน </strong>จะใช้เฉพาะเมื่อไม่ได้ตั้งค่าบัญชีเริ่มต้นสำหรับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="17bf6-134">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="17bf6-135">ใช้ตัวเลือกนี้เพื่อตั้งค่าบัญชีเริ่มต้นที่จะใช้เมื่อไม่มีการกำหนดบัญชีตรงข้ามของผู้จัดจำหน่ายเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="17bf6-135">Use this option to set up default accounts that are used when a default vendor offset account isn't assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17bf6-136"><strong>หัวข้อสมุดรายวัน</strong> – ตั้งค่าบัญชีตรงข้ามเริ่มต้นสำหรับสมุดรายวันเพื่อใช้เป็นรายการเริ่มต้นในหน้าใบสำคัญสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="17bf6-136"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="17bf6-137">โปรดทราบว่า คุณไม่สามารถระบุบัญชีตรงข้ามเริ่มต้นในหัวข้อสมุดรายวัน ถ้าชนิดสมุดรายวันของชื่อสมุดรายวันเป็น <strong>ทะเบียนใบแจ้งหนี้</strong> หรือ <strong>การอนุมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="17bf6-137">Note that you can't specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="17bf6-138">รายการสมุดรายวันในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="17bf6-138">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="17bf6-139">บัญชีตรงข้ามเริ่มต้นสำหรับสมุดรายวันจะถูกใช้เป็นรายการเริ่มต้นในหน้าใบสำคัญสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="17bf6-139">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="17bf6-140">ใช้ตัวเลือกนี้เพื่อช่วยป้อนข้อมูลให้เร็วขึ้น ถ้ารายการส่วนใหญ่ในสมุดรายวันมีบัญชีตรงข้ามเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="17bf6-140">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






