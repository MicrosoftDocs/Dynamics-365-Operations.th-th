---
title: ป้อนชุดบัญชีและชุดข้อมูลมิติ (การควบคุมรายการของเซ็กเมนต์)
description: บทความนี้อธิบายวิธีการป้อนบัญชี และชุดมิติ หรือบัญชีแยกประเภท รายการประสบการณ์มักหมายถึงตัวควบคุมรายการที่แบ่งเซ็กเมนต์
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: roschlom
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bed6a13a721269550fa72c495e7ecfddadf9d8b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260792"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="e0f12-104">ป้อนชุดบัญชีและชุดข้อมูลมิติ (การควบคุมรายการของเซ็กเมนต์)</span><span class="sxs-lookup"><span data-stu-id="e0f12-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0f12-105">บทความนี้อธิบายวิธีการป้อนบัญชี และชุดมิติ หรือบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="e0f12-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="e0f12-106">รายการประสบการณ์มักหมายถึงตัวควบคุมรายการที่แบ่งเซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="e0f12-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="e0f12-107">ผู้ใช้ป้อนชุดบัญชีและชุดมิติบนหน้าต่าง ๆ เช่นหน้าสำหรับสมุดรายวันทั่วไป การจัดงบประมาณ และ ข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="e0f12-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="e0f12-108">ชุดบัญชีที่และชุดมิติที่ถูกต้องขึ้นอยู่กับโครงสร้างทางบัญชีที่กำหนดให้กับบัญชีแยกประเภทและกฎขั้นสูงที่กำหนดให้กับโครงสร้างทางบัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="e0f12-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="e0f12-109">เมื่อผู้ใช้ป้อนชุดคำ พวกเขาสามารถพิมพ์ค่านั้นๆด้วยตนเอง หรือใช้ประโยชน์จากประสบการณ์การค้นหาหลากหลาย</span><span class="sxs-lookup"><span data-stu-id="e0f12-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="e0f12-110">เมื่อคุณป้อนฟิลด์ คุณสามารถเริ่มพิมพ์ และระบบจะค้นหาค่าและคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e0f12-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="e0f12-111">ตัวอย่างเช่น ถ้าคุณพิมพ์ 180 ระบบจะค้นหาค่าใดๆ ที่เริ่มต้นด้วยชุดหมายเลขนั้น</span><span class="sxs-lookup"><span data-stu-id="e0f12-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="e0f12-112">หรือคุณอาจพิมพ์ เงินสด ระบบจะค้นหาค่าใดๆ ที่มีคำอธิบายที่เริ่มต้นด้วย เงินสด</span><span class="sxs-lookup"><span data-stu-id="e0f12-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="e0f12-113">คุณยังสามารถใช้อักขระตัวแทน เช่น \*เงินสด หรือ \*180 เมื่อต้องการค้นหาค่าหรือคำอธิบายที่ประกอบด้วยเงื่อนไขการค้นหาได้</span><span class="sxs-lookup"><span data-stu-id="e0f12-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="e0f12-114">ตารางต่อไปนี้อธิบายแป้นพิมพ์ลัดที่สามารถใช้เมื่อปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="e0f12-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0f12-115">แป้นพิมพ์ลัด</span><span class="sxs-lookup"><span data-stu-id="e0f12-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="e0f12-116">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="e0f12-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0f12-117">Alt+เลื่อนลูกศรลง</span><span class="sxs-lookup"><span data-stu-id="e0f12-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="e0f12-118">เปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="e0f12-118">Open the lookup.</span></span> <span data-ttu-id="e0f12-119">ถ้าคุณกด Alt + ลูกศรลงอีกครั้ง โฟกัสจะย้ายเซ็กเมนต์ไปในเมนูพลายเอาท์</span><span class="sxs-lookup"><span data-stu-id="e0f12-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="e0f12-120">ป้อน และเลื่อน + Enter</span><span class="sxs-lookup"><span data-stu-id="e0f12-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="e0f12-121">ตัวกำหนดเขตผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="e0f12-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="e0f12-122">ลูกศรทางขวา และ ลูกศรทางซ้าย</span><span class="sxs-lookup"><span data-stu-id="e0f12-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="e0f12-123">ย้ายไปยังเซ็กเมนต์ถัดไปหรือก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="e0f12-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0f12-124">แท็บ</span><span class="sxs-lookup"><span data-stu-id="e0f12-124">Tab</span></span></td>
<td><span data-ttu-id="e0f12-125">ย้ายไปยังฟิลด์ถัดไปในกริด</span><span class="sxs-lookup"><span data-stu-id="e0f12-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e0f12-126">ตารางต่อไปนี้อธิบายแป้นพิมพ์ลัดที่สามารถใช้เมื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="e0f12-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0f12-127">แป้นพิมพ์ลัด</span><span class="sxs-lookup"><span data-stu-id="e0f12-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="e0f12-128">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="e0f12-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0f12-129">Esc</span><span class="sxs-lookup"><span data-stu-id="e0f12-129">Esc</span></span></td>
<td><span data-ttu-id="e0f12-130">ปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="e0f12-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="e0f12-131">ลูกศรขึ้น และ ลูกศรลง</span><span class="sxs-lookup"><span data-stu-id="e0f12-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="e0f12-132">เลื่อนหน้าขึ้น และ เลื่อนหน้าลง</span><span class="sxs-lookup"><span data-stu-id="e0f12-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="e0f12-133">โฮม และ สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="e0f12-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="e0f12-134">ย้ายไปยังค่าก่อนหน้าหรือถัดไปในรายการ ถึงกลุ่มก่อนหน้า หรือถัดไป ของค่าหรือไปยังองค์ประกอบแรก หรือสุดท้ายในการค้นหา</span><span class="sxs-lookup"><span data-stu-id="e0f12-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e0f12-135">ตัวกำหนดเขตผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="e0f12-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="e0f12-136">ลูกศรทางขวา และ ลูกศรทางซ้าย</span><span class="sxs-lookup"><span data-stu-id="e0f12-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="e0f12-137">ย้ายไปยังเซ็กเมนต์ถัดไปหรือก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="e0f12-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0f12-138">แท็บ</span><span class="sxs-lookup"><span data-stu-id="e0f12-138">Tab</span></span></td>
<td><span data-ttu-id="e0f12-139">ย้ายไปยังฟิลด์ถัดไปในกริด</span><span class="sxs-lookup"><span data-stu-id="e0f12-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0f12-140">Alt + W</span><span class="sxs-lookup"><span data-stu-id="e0f12-140">Alt+W</span></span></td>
<td><span data-ttu-id="e0f12-141">สลับไปมาระหว่างโหมด <strong>แสดงทั้งหมด</strong> และ <strong>แสดงสิ่งที่ใช้ได้</strong></span><span class="sxs-lookup"><span data-stu-id="e0f12-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]