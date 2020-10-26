---
title: ดูและส่งออกคำอธิบายฟิลด์
description: บทความนี้อธิบายวิธีการดูคำอธิบายฟิลด์และวิธีการใช้หน้าคำอธิบายฟิลด์เพื่อส่งออกคำอธิบาย
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 147dc55160de7d3cc01cc077095d2eb71f4d7861
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978189"
---
# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="9dbfb-103">ดูและส่งออกคำอธิบายฟิลด์</span><span class="sxs-lookup"><span data-stu-id="9dbfb-103">View and export field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9dbfb-104">บทความนี้อธิบายวิธีการดูคำอธิบายฟิลด์และวิธีการใช้หน้าคำอธิบายฟิลด์เพื่อส่งออกคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="9dbfb-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="9dbfb-105">ฟิลด์ที่ซับซ้อนมากขึ้นบางรายการมีคำอธิบายฟิลด์</span><span class="sxs-lookup"><span data-stu-id="9dbfb-105">Some of the more complex fields have field descriptions.</span></span> <span data-ttu-id="9dbfb-106">คำอธิบายเหล่านี้ปรากฏเมื่อคุณวางเมาส์เหนือฟิลด์</span><span class="sxs-lookup"><span data-stu-id="9dbfb-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="9dbfb-107">นอกจากนี้คุณสามารถดู และส่งออกคำอธิบายบนหน้า **ฟิลด์คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="9dbfb-107">You can also view and export descriptions on the **Field descriptions** page.</span></span>

<span data-ttu-id="9dbfb-108">ไม่ใช่ทุกหน้าที่มีคำอธิบายฟิลด์</span><span class="sxs-lookup"><span data-stu-id="9dbfb-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="9dbfb-109">เราเพียงต้องการแสดงคำอธิบายสำหรับฟิลด์ที่ซับซ้อนมากขึ้น ไม่ใช้ตำแหน่งที่มีการใช้ฟิลด์ที่ชัดเจน</span><span class="sxs-lookup"><span data-stu-id="9dbfb-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="9dbfb-110">ดังนั้นบางหน้าจะไม่มีคำอธิบายใดๆ บางหน้ามีคำอธิบายสองสามรายการ และบางหน้าที่ซับซ้อนมากขึ้น เช่น หน้าพารามิเตอร์ส่วนใหญ่ มีคำอธิบายหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="9dbfb-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span>

<span data-ttu-id="9dbfb-111">ถ้าคุณมีสิทธิเข้าถึงสภาพแวดล้อมการพัฒนา คุณสามารถเพิ่มคำอธิบายฟิลด์ใหม่และเลือกกำหนดคำอธิบายที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="9dbfb-111">If you have access to the development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="9dbfb-112">ตัวอย่างเช่น คุณสามารถเพิ่มข้อมูลเฉพาะบริษัทไปยังคำอธิบายฟิลด์ได้</span><span class="sxs-lookup"><span data-stu-id="9dbfb-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="9dbfb-113">สำหรับข้อมูลเพิ่มเติม โปรดดู [กำหนดคำอธิบายฟิลด์เอง](../../dev-itpro/user-interface/customize-field-help.md)</span><span class="sxs-lookup"><span data-stu-id="9dbfb-113">For more information, see [Customize field descriptions](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="9dbfb-114">ดูคำอธิบายฟิลด์ในอินเทอร์เฟสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9dbfb-114">See field descriptions in the user interface</span></span>

<span data-ttu-id="9dbfb-115">คุณสามารถดูคำอธิบายฟิลด์ได้โดยวางเมาส์เหนือฟิลด์</span><span class="sxs-lookup"><span data-stu-id="9dbfb-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="9dbfb-116">ถ้าไม่มีคำอธิบาย คุณจะเห็นชื่อฟิลด์เมื่อคุณวางเมาส์เหนือฟิลด์</span><span class="sxs-lookup"><span data-stu-id="9dbfb-116">If no description is available, you see the field name when you hover over the field.</span></span>

> [!NOTE]
> <span data-ttu-id="9dbfb-117">ใน In Dynamics AX 7.0 (กุมภาพันธ์ 2016) สามารถดูได้บนหน้า **Description ของฟิลด์** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9dbfb-117">In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.</span></span>

<span data-ttu-id="9dbfb-118">ภาพประกอบต่อไปนี้แสดงคำอธิบายฟิลด์ที่ปรากฏขึ้นเมื่อคุณวางเมาส์เหนือฟิลด์ **ล็อคสินค้าในระหว่างตรวจนับ**</span><span class="sxs-lookup"><span data-stu-id="9dbfb-118">The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span>

<span data-ttu-id="9dbfb-119">[![ตัวอย่างของคำอธิบายฟิลด์](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="9dbfb-119">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="9dbfb-120">ใช้หน้าคำอธิบายฟิลด์เพื่อดูและส่งออกวิธีใช้ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="9dbfb-120">Use the Field descriptions page to view and export field help</span></span>

<span data-ttu-id="9dbfb-121">หน้า **คำอธิบายฟิลด์** ทำให้คุณสามารถดูและส่งออกคำอธิบายฟิลด์ได้</span><span class="sxs-lookup"><span data-stu-id="9dbfb-121">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="9dbfb-122">คุณสามารถดูคำอธิบายที่ใช้งานได้สำหรับหน้าเดียวในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="9dbfb-122">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="9dbfb-123">ดูคำอธิบายสำหรับหน้า</span><span class="sxs-lookup"><span data-stu-id="9dbfb-123">View the descriptions for a page</span></span>

<span data-ttu-id="9dbfb-124">หากต้องการดูคำอธิบายสำหรับหน้า ให้ทำตามขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="9dbfb-124">To view the descriptions for a page, follow this step.</span></span>

- <span data-ttu-id="9dbfb-125">ในฟิลด์ **เลือกหน้า** ให้พิมพ์ชื่อของหน้า</span><span class="sxs-lookup"><span data-stu-id="9dbfb-125">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="9dbfb-126">อีกวิธีหนึ่งคือ คลิกลูกศรเพื่อเปิดรายการของหน้าทั้งหมด และจากนั้น เรียกดูหรือกรองข้อมูลรายการ</span><span class="sxs-lookup"><span data-stu-id="9dbfb-126">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="9dbfb-127">คุณสามารถใช้ชื่อของหน้าที่แสดงในอินเทอร์เฟสผู้ใช้ (UI) (ตัวอย่างเช่น **ลูกค้า**) หรือชื่อรหัส (ชื่อ AOT) ที่ใช้ได้เมื่อคุณคลิกขวาที่หน้า (ตัวอย่างเช่น **CustTable**)</span><span class="sxs-lookup"><span data-stu-id="9dbfb-127">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span>

<span data-ttu-id="9dbfb-128">สำหรับข้อมูลเกี่ยวกับวิธีการต่างๆ ในการกรองรายการของหน้า ดูส่วน "กำลังค้นหาหน้า" ในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="9dbfb-128">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span>

<span data-ttu-id="9dbfb-129">ถ้าคุณตั้งค่าตัวเลือก **รวมฟิลด์โดยไม่มีคำอธิบาย** เป็น **ใช่**ฟิลด์ทั้งหมดบนหน้าจะแสดงขึ้น ถึงแม้ว่าจะไม่มีคำอธิบายฟิลด์ก็ตาม</span><span class="sxs-lookup"><span data-stu-id="9dbfb-129">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="9dbfb-130">ส่งออกคำอธิบายสำหรับหน้า</span><span class="sxs-lookup"><span data-stu-id="9dbfb-130">Export the descriptions for a page</span></span>

<span data-ttu-id="9dbfb-131">หากต้องการส่งออกคำอธิบายสำหรับหน้า ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9dbfb-131">To export the descriptions for a page, follow these steps.</span></span>

1. <span data-ttu-id="9dbfb-132">ในฟิลด์ **เลือกหน้า** เลือกหน้า</span><span class="sxs-lookup"><span data-stu-id="9dbfb-132">In the **Select a page** field, select a page.</span></span>
2. <span data-ttu-id="9dbfb-133">คลิกปุ่ม **เปิดใน Microsoft Office** ที่มุมบนด้านขวา และจากนั้นคลิก **FieldDescriptionTmp**</span><span class="sxs-lookup"><span data-stu-id="9dbfb-133">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="9dbfb-134">กำลังค้นหาหน้า</span><span class="sxs-lookup"><span data-stu-id="9dbfb-134">Searching for a page</span></span>

<span data-ttu-id="9dbfb-135">มีหลายวิธีในการค้นหาหน้าในฟิลด์ **เลือกหน้า**</span><span class="sxs-lookup"><span data-stu-id="9dbfb-135">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="9dbfb-136">ในหลายกรณี คุณต้องคลิกลูกศรในฟิลด์ **เลือกหน้า** เพื่อเปิดรายการแบบหล่นลง และจากนั้น เลือกจากรายการของหน้าที่กรองแล้ว</span><span class="sxs-lookup"><span data-stu-id="9dbfb-136">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

- <span data-ttu-id="9dbfb-137">พิมพ์ชื่อบางส่วน แล้วเปิดรายการแบบหล่นลงเพื่อเลือกจากรายการของหน้าที่กรองแล้ว</span><span class="sxs-lookup"><span data-stu-id="9dbfb-137">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
- <span data-ttu-id="9dbfb-138">เปิดรายการแบบหล่นลง และจากนั้นคลิก **ชื่อหน้า** ที่เป็นหัวข้อที่ด้านบนของรายการหรือหัวข้อ **ชื่อ AOT หน้า**</span><span class="sxs-lookup"><span data-stu-id="9dbfb-138">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="9dbfb-139">กล่องโต้ตอบปรากฏขึ้นซึ่งคุณสามารถใช้ตัวเลือกการกรองขั้นสูง เช่น **ชื่อหน้าที่เริ่มต้นด้วย**</span><span class="sxs-lookup"><span data-stu-id="9dbfb-139">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
- <span data-ttu-id="9dbfb-140">พิมพ์ชื่อเต็มของหน้า</span><span class="sxs-lookup"><span data-stu-id="9dbfb-140">Type the full name of the page.</span></span> <span data-ttu-id="9dbfb-141">เมื่อคุณใช้ตัวเลือกนี้ วิธีที่ดีที่สุดคือการเปิดรายการแบบหล่นลง และดูว่ามีสิ่งอื่นใดที่อยู่ในรายการ แม้ว่าจะมีแสดงคำอธิบายฟิลด์</span><span class="sxs-lookup"><span data-stu-id="9dbfb-141">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>

    - <span data-ttu-id="9dbfb-142">ถ้ามีการตรงกันทุกประการกับชื่อเพียงหนึ่งรายการ คำอธิบายฟิลด์สำหรับหน้านั้นจะถูกแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="9dbfb-142">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    - <span data-ttu-id="9dbfb-143">ถ้ามีการตรงกันทุกประการมากกว่าหนี่งรายการ จะไม่มีคำอธิบายแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="9dbfb-143">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="9dbfb-144">คุณต้องเปิดรายการแบบหล่นลง และเลือกหน้าที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="9dbfb-144">You must open the drop-down list and select the page that you want.</span></span>
    - <span data-ttu-id="9dbfb-145">ถ้าชื่อที่คุณพิมพ์เป็นส่วนหนึ่งของชื่อของหน้าอื่น คุณจะสามารถดูคำอธิบายสำหรับหน้าของคุณได้</span><span class="sxs-lookup"><span data-stu-id="9dbfb-145">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="9dbfb-146">อย่างไรก็ตาม ถ้าคุณเปิดรายการแบบหล่นลง คุณจะเห็นหน้าเพิ่มเติมที่มีชื่อนั้น</span><span class="sxs-lookup"><span data-stu-id="9dbfb-146">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="9dbfb-147">ตัวอย่างเช่น ไม่มีคำอธิบายแสดงขึ้นเมื่อคุณพิมพ์ **การตรวจนับ** ในฟิลด์ **เลือกหน้า**</span><span class="sxs-lookup"><span data-stu-id="9dbfb-147">For example, no descriptions are shown when you type **Counting** in the **Select a page** field.</span></span> <span data-ttu-id="9dbfb-148">เมื่อคุณเปิดรายการแบบหล่นลง จะพบว่ามีสองหน้าที่มีชื่อ **การตรวจนับ** และหลายหน้าที่มีคำว่า "การตรวจนับ" ในชื่อ</span><span class="sxs-lookup"><span data-stu-id="9dbfb-148">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="9dbfb-149">ถ้าคุณเลือกหน้าที่มีชื่อ AOT **InventJournalCount** คำอธิบายฟิลด์จะแสดงขึ้นสำหรับหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="9dbfb-149">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="9dbfb-150">อย่างไรก็ตาม ถ้าคุณเปิดรายการแบบหล่นลงอีกครั้ง คุณจะพบว่าขณะนี้รายการมีหน้าทั้งหมดที่มี "InventJournalCount" เป็นส่วนหนึ่งของชื่อ AOT</span><span class="sxs-lookup"><span data-stu-id="9dbfb-150">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9dbfb-151">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="9dbfb-151">Troubleshooting</span></span>

<span data-ttu-id="9dbfb-152">ส่วนนี้ให้ข้อมูลที่ช่วยคุณในการแก้ไขปัญหาที่คุณอาจพบเมื่อใช้คำอธิบายฟิลด์</span><span class="sxs-lookup"><span data-stu-id="9dbfb-152">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="9dbfb-153">ฉันหาคำอธิบายฟิลด์ไม่พบ</span><span class="sxs-lookup"><span data-stu-id="9dbfb-153">I can't find a field description</span></span>

<span data-ttu-id="9dbfb-154">เรากำลังอยู่ในกระบวนการเพิ่มคำอธิบายสำหรับฟิลด์ที่ซับซ้อนมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="9dbfb-154">We're in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="9dbfb-155">ถ้าคุณต้องการความช่วยเหลือสำหรับฟิลด์เฉพาะใดๆ โปรดแจ้งให้เราทราบโดยการเพิ่มข้อคิดเห็นสำหรับหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="9dbfb-155">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="9dbfb-156">ไม่มีข้อมูลที่ต้องการในคำอธิบายฟิลด์</span><span class="sxs-lookup"><span data-stu-id="9dbfb-156">The field description isn't helpful</span></span>

<span data-ttu-id="9dbfb-157">โปรดแจ้งให้เราทราบโดยการเพิ่มข้อคิดเห็นสำหรับหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="9dbfb-157">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="9dbfb-158">อธิบายข้อมูลเพิ่มเติมที่คุณต้องการหากสามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="9dbfb-158">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="9dbfb-159">ฉันไม่พบฟิลด์ในหน้าคำอธิบายฟิลด์</span><span class="sxs-lookup"><span data-stu-id="9dbfb-159">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="9dbfb-160">เมื่อต้องการแสดงฟิลด์ทั้งหมดในหน้า ให้ตั้งค่าตัวเลือก **รวมฟิลด์ที่ไม่มีคำอธิบาย** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9dbfb-160">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="9dbfb-161">คลิกฟิลด์ **เลือกหน้า** เพื่อตรวจสอบว่าคุณเลือกหน้าที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9dbfb-161">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="9dbfb-162">ถ้าชื่อที่คุณพิมพ์เป็นส่วนหนึ่งของชื่อฟิลด์อื่น คุณอาจเลือกหน้าที่มีชื่อยาวกว่า</span><span class="sxs-lookup"><span data-stu-id="9dbfb-162">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="9dbfb-163">ฉันไม่พบหน้าในหน้าคำอธิบายฟิลด์</span><span class="sxs-lookup"><span data-stu-id="9dbfb-163">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="9dbfb-164">สำหรับข้อมูลเกี่ยวกับวิธีการต่างๆ ในการค้นหาหน้า ดูส่วน "กำลังค้นหาหน้า" ก่อนบทความนี้</span><span class="sxs-lookup"><span data-stu-id="9dbfb-164">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="9dbfb-165">ถ้าคุณพิมพ์ชื่อที่เหมือนกันของหน้า คำอธิบายฟิลด์อาจไม่แสดงถ้ามีหน้าที่มีชื่อเดียวกันมากกว่าหนึ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="9dbfb-165">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="9dbfb-166">คลิกที่ลูกศรในฟิลด์ **เลือกหน้า** เพื่อเปิดรายการของหน้าที่พร้อมใช้งานที่กรองแล้ว</span><span class="sxs-lookup"><span data-stu-id="9dbfb-166">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9dbfb-167">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9dbfb-167">Additional resources</span></span>

[<span data-ttu-id="9dbfb-168">กำหนดคำอธิบายฟิลด์เอง</span><span class="sxs-lookup"><span data-stu-id="9dbfb-168">Customize field descriptions</span></span>](../../dev-itpro/user-interface/customize-field-help.md)
