---
title: "ป้อนชุดบัญชีและชุดข้อมูลมิติ (การควบคุมรายการของเซ็กเมนต์)"
description: "บทความนี้อธิบายวิธีการป้อนบัญชี และชุดมิติ หรือบัญชีแยกประเภท รายการประสบการณ์มักหมายถึงตัวควบคุมรายการที่แบ่งเซ็กเมนต์"
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 610b21069d9f13a511f8017d0069fda0371abf10
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="30b6c-104">ป้อนชุดบัญชีและชุดข้อมูลมิติ (การควบคุมรายการของเซ็กเมนต์)</span><span class="sxs-lookup"><span data-stu-id="30b6c-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="30b6c-105">บทความนี้อธิบายวิธีการป้อนบัญชี และชุดมิติ หรือบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="30b6c-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="30b6c-106">รายการประสบการณ์มักหมายถึงตัวควบคุมรายการที่แบ่งเซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="30b6c-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="30b6c-107">ผู้ใช้ป้อนชุดบัญชีและชุดมิติบนหน้าต่าง ๆ เช่นหน้าสำหรับสมุดรายวันทั่วไป การจัดงบประมาณ และ ข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="30b6c-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="30b6c-108">ชุดบัญชีที่และชุดมิติที่ถูกต้องขึ้นอยู่กับโครงสร้างทางบัญชีที่กำหนดให้กับบัญชีแยกประเภทและกฎขั้นสูงที่กำหนดให้กับโครงสร้างทางบัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="30b6c-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="30b6c-109">เมื่อผู้ใช้ป้อนชุดคำ พวกเขาสามารถพิมพ์ค่านั้นๆด้วยตนเอง หรือใช้ประโยชน์จากประสบการณ์การค้นหาหลากหลาย</span><span class="sxs-lookup"><span data-stu-id="30b6c-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="30b6c-110">เมื่อคุณป้อนฟิลด์ คุณสามารถเริ่มพิมพ์ และระบบจะค้นหาค่าและคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="30b6c-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="30b6c-111">ตัวอย่างเช่น ถ้าคุณพิมพ์ 180 ระบบจะค้นหาค่าใดๆ ที่เริ่มต้นด้วยชุดหมายเลขนั้น</span><span class="sxs-lookup"><span data-stu-id="30b6c-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="30b6c-112">หรือคุณอาจพิมพ์ เงินสด ระบบจะค้นหาค่าใดๆ ที่มีคำอธิบายที่เริ่มต้นด้วย เงินสด</span><span class="sxs-lookup"><span data-stu-id="30b6c-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="30b6c-113">คุณยังสามารถใช้อักขระตัวแทน เช่น \*เงินสด หรือ \*180 เมื่อต้องการค้นหาค่าหรือคำอธิบายที่ประกอบด้วยเงื่อนไขการค้นหาได้</span><span class="sxs-lookup"><span data-stu-id="30b6c-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="30b6c-114">ตารางต่อไปนี้อธิบายแป้นพิมพ์ลัดที่สามารถใช้เมื่อปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="30b6c-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30b6c-115">แป้นพิมพ์ลัด</span><span class="sxs-lookup"><span data-stu-id="30b6c-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="30b6c-116">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="30b6c-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30b6c-117">Alt+เลื่อนลูกศรลง</span><span class="sxs-lookup"><span data-stu-id="30b6c-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="30b6c-118">เปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="30b6c-118">Open the lookup.</span></span> <span data-ttu-id="30b6c-119">ถ้าคุณกด Alt + ลูกศรลงอีกครั้ง โฟกัสจะย้ายเซ็กเมนต์ไปในเมนูพลายเอาท์</span><span class="sxs-lookup"><span data-stu-id="30b6c-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="30b6c-120">ป้อน และเลื่อน + Enter</span><span class="sxs-lookup"><span data-stu-id="30b6c-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="30b6c-121">ตัวกำหนดเขตผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="30b6c-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="30b6c-122">ลูกศรทางขวา และ ลูกศรทางซ้าย</span><span class="sxs-lookup"><span data-stu-id="30b6c-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="30b6c-123">ย้ายไปยังเซ็กเมนต์ถัดไปหรือก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="30b6c-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30b6c-124">แท็บ</span><span class="sxs-lookup"><span data-stu-id="30b6c-124">Tab</span></span></td>
<td><span data-ttu-id="30b6c-125">ย้ายไปยังฟิลด์ถัดไปในกริด</span><span class="sxs-lookup"><span data-stu-id="30b6c-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="30b6c-126">ตารางต่อไปนี้อธิบายแป้นพิมพ์ลัดที่สามารถใช้เมื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="30b6c-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30b6c-127">แป้นพิมพ์ลัด</span><span class="sxs-lookup"><span data-stu-id="30b6c-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="30b6c-128">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="30b6c-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30b6c-129">Esc</span><span class="sxs-lookup"><span data-stu-id="30b6c-129">Esc</span></span></td>
<td><span data-ttu-id="30b6c-130">ปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="30b6c-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="30b6c-131">ลูกศรขึ้น และ ลูกศรลง</span><span class="sxs-lookup"><span data-stu-id="30b6c-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="30b6c-132">เลื่อนหน้าขึ้น และ เลื่อนหน้าลง</span><span class="sxs-lookup"><span data-stu-id="30b6c-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="30b6c-133">โฮม และ สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="30b6c-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="30b6c-134">ย้ายไปยังค่าก่อนหน้าหรือถัดไปในรายการ ถึงกลุ่มก่อนหน้า หรือถัดไป ของค่าหรือไปยังองค์ประกอบแรก หรือสุดท้ายในการค้นหา</span><span class="sxs-lookup"><span data-stu-id="30b6c-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="30b6c-135">ตัวกำหนดเขตผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="30b6c-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="30b6c-136">ลูกศรทางขวา และ ลูกศรทางซ้าย</span><span class="sxs-lookup"><span data-stu-id="30b6c-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="30b6c-137">ย้ายไปยังเซ็กเมนต์ถัดไปหรือก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="30b6c-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30b6c-138">แท็บ</span><span class="sxs-lookup"><span data-stu-id="30b6c-138">Tab</span></span></td>
<td><span data-ttu-id="30b6c-139">ย้ายไปยังฟิลด์ถัดไปในกริด</span><span class="sxs-lookup"><span data-stu-id="30b6c-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30b6c-140">Alt + W</span><span class="sxs-lookup"><span data-stu-id="30b6c-140">Alt+W</span></span></td>
<td><span data-ttu-id="30b6c-141">สลับไปมาระหว่างโหมด <strong>แสดงทั้งหมด</strong> และ <strong>แสดงสิ่งที่ใช้ได้</strong></span><span class="sxs-lookup"><span data-stu-id="30b6c-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>

 




