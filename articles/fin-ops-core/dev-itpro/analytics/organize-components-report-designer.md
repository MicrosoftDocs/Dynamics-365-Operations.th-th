---
title: ส่วนประกอบรายงานองค์กรในผู้ออกแบบรายงาน
description: หัวข้อนี้อธิบายถึงวิธีการจัดระเบียบรายงานที่มีอยู่ บล็อคส่วนประกอบ และออบเจ็กต์ในตัวออกแบบรายงาน
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d348993422b24776098657dcef25a088ba2f826b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564554"
---
# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="8d296-103">ส่วนประกอบรายงานองค์กรในผู้ออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-103">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d296-104">หลังจากที่คุณได้ออกแบบบล็อคส่วนประกอบและสร้างรายงานแล้ว คุณควรจัดเรียงออบเจ็กต์เหล่านี้เพื่อให้ผู้ใช้สามารถค้นหาได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="8d296-104">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="8d296-105">บทความนี้อธิบายถึงวิธีการจัดระเบียบรายงานที่มีอยู่ บล็อคส่วนประกอบ และออบเจ็กต์ในตัวออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-105">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="8d296-106">คุณสามารถเปลี่ยนชื่อโฟลเดอร์ รายงาน บล็อคส่วนประกอบ และออบเจ็กต์อื่นๆ ในผู้ออกแบบรายงานเพื่อช่วยในการจัดระเบียบแฟ้มต่างๆของคุณ</span><span class="sxs-lookup"><span data-stu-id="8d296-106">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="8d296-107">ขึ้นอยู่กับชนิดขอออบเจ็กต์ที่คุณเปลี่ยนชื่อ คุณอาจต้องอัพเดตการเชื่อมโยงกับออบเจ็กต์นั้น</span><span class="sxs-lookup"><span data-stu-id="8d296-107">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="8d296-108">เปลี่ยนชื่อโฟลเดอร์หรือบล็อคส่วนประกอบใน Report Designer</span><span class="sxs-lookup"><span data-stu-id="8d296-108">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="8d296-109">คุณจะสามารถเปลี่ยนชื่อโฟลเดอร์ ข้อกำหนดของรายงาน คำนิยามแถว คำนิยามคอลัมน์ และคำนิยามลำดับการรายงานใน Report Designer</span><span class="sxs-lookup"><span data-stu-id="8d296-109">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="8d296-110">การเปลี่ยนชื่อโฟลเดอร์หรือบล็อคส่วนประกอบใน Report Designer</span><span class="sxs-lookup"><span data-stu-id="8d296-110">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="8d296-111">ใน Report Designer ใช้บานหน้าต่างนำทางเพื่อค้นหาโฟลเดอร์หรือออบเจ็กต์ที่ต้องการเปลี่ยนชื่อ</span><span class="sxs-lookup"><span data-stu-id="8d296-111">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="8d296-112">คลิกขวาโฟลเดอร์หรือออบเจ็กต์ และจากนั้น คลิก **เปลี่ยนชื่อ**</span><span class="sxs-lookup"><span data-stu-id="8d296-112">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="8d296-113">ฟิลด์ **ชื่อ** ในบานหน้าต่างนำทางกลายเป็นพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8d296-113">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="8d296-114">พิมพ์ชื่อใหม่ และกด ป้อน</span><span class="sxs-lookup"><span data-stu-id="8d296-114">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="8d296-115">ถ้าบล็อคส่วนประกอบเป็นคำนิยามแถว คำนิยามคอลัมน์ หรือคำนิยามแผนภูมิรายงาน คุณต้องปรับปรุงส่วนประกอบอื่น ๆ ที่เกี่ยวข้องกับสินค้า</span><span class="sxs-lookup"><span data-stu-id="8d296-115">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="8d296-116">คลิกขวาบล็อคส่วนประกอบที่คุณเปลี่ยนชื่อใหม่ในขั้นตอนที่ 3 เลือก **สมาคม**, แล้ว เลือกสินค้าในรายการเพื่อปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="8d296-116">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="8d296-117">ทำซ้ำขั้นตอนที่ 4 จนกว่าสินค้าที่เกี่ยวข้องทั้งหมดจะถูกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="8d296-117">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="8d296-118">รายงานสร้างและจัดการกลุ่มรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-118">Create and manage report groups</span></span>
<span data-ttu-id="8d296-119">คุณสามารถจัดกลุ่มข้อกำหนดของรายงานเพื่อสร้างรายงานหลายรายการพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="8d296-119">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="8d296-120">เมื่อต้องการสร้าง ปรับเปลี่ยน ลบ และสร้างกลุ่มการรายงาน คุณต้องมีบทบาทเป็นผู้ออกแบบหรือผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="8d296-120">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="8d296-121">ผู้ใช้ที่ มีบทบาทของผู้สร้างซึ่งสามารถสร้างกลุ่มการรายงาน และยังสามารถปรับเปลี่ยนข้อกำหนดของรายงานผู้ใช้ในการตั้งค่าสำหรับกลุ่มการรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-121">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="8d296-122">การสร้างกลุ่มรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-122">Create a report group</span></span>

1. <span data-ttu-id="8d296-123">ใน Report Designer ในบานหน้าต่างนำทาง คลิก **กลุ่มรายงาน**</span><span class="sxs-lookup"><span data-stu-id="8d296-123">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="8d296-124">บนเมนู **ไฟล์** คลิก **ใหม่** &gt; **คำนิยามกลุ่มรายงาน** เพื่อเปิดกลุ่มรายงานใหม่ในหน้าต่างตัวแสดง</span><span class="sxs-lookup"><span data-stu-id="8d296-124">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="8d296-125">หรือคลิกปุ่ม **กลุ่มรายงาน** ![กลุ่มรายงาน](media/report-group.gif "กลุ่มรายงาน") บนแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="8d296-125">Alternatively, click the **Report Group** button ![Report Group](media/report-group.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="8d296-126">คลิกแท็บ **กลุ่มรายงาน** เมื่อต้องการแทนข้อมูลในรายงานแต่ละคำนิยามสำหรับการสร้างรายงานนี้ เลือกกล่องกาเครื่องหมาย **แทนที่บริษัท รายละเอียด และการตั้งค่าวันที่จากแต่ละข้อกำหนดของรายงาน**</span><span class="sxs-lookup"><span data-stu-id="8d296-126">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="8d296-127">ชื่อบริษัท ระดับรายละเอียด การตั้งค่าสำรอง และข้อมูลวันที่จะถูกป้อนโดยอัตโนมัติ แต่คุณยังคงสามารถทำการอัพเดตได้</span><span class="sxs-lookup"><span data-stu-id="8d296-127">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="8d296-128">เมื่อต้องการสร้างรายงานหลายฉบับที่แสดงสกุลเงินรายงาน เลือกกล่องกาเครื่องหมาย **รวมสกุลเงินรายงานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="8d296-128">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="8d296-129">จากนั้นคุณสามารถเข้าถึงมุมมองต่าง ๆ โดยการคลิกปุ่ม **สกุลเงิน** ในตัวแสดงเว็บเมื่อคุณดูรายงานนั้น</span><span class="sxs-lookup"><span data-stu-id="8d296-129">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="8d296-130">ในการ **รายงานในฟิลด์กลุ่ม** คลิก **เพิ่ม** เพื่อเลือกรายงานเพื่อรวมไว้ในกลุ่มการรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-130">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="8d296-131">เมื่อต้องการเลือกรายงานหลายฉบับในกล่องโต้ตอบ **เพิ่ม** ให้กดคีย์ Ctrl ขณะที่คุณเลือกรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-131">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="8d296-132">เมื่อคุณเสร็จสิ้นการเลือกรายงาน คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8d296-132">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="8d296-133">คลิก **ไฟล์** &gt; **บันทึก** เพื่อบันทึกกลุ่มรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="8d296-133">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="8d296-134">ปรับเปลี่ยนกลุ่มรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-134">Modify a report group</span></span>

1. <span data-ttu-id="8d296-135">ใน Report Designer ในบานหน้าต่างนำทาง คลิก **กลุ่มรายงาน**</span><span class="sxs-lookup"><span data-stu-id="8d296-135">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="8d296-136">ดับเบิลคลินกลุ่มรายงานนั้นเพื่อปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="8d296-136">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="8d296-137">บนแท็บ **กลุ่มรายงาน** ทำการเปลี่ยนแปลงที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="8d296-137">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="8d296-138">ในเมนู **ไฟล์** คลิก **บันทึก** หรือหากต้องการบันทึกกลุ่มรายงานที่ปรับเปลี่ยน ให้คลิกปุ่ม **บันทึก** ![บันทึก](media/save.gif "บันทึก") บนแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="8d296-138">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](media/save.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="8d296-139">[หมายเหตุ] ถ้าคุณได้จัดกำหนดการรายงานเพื่อให้มีการสร้างขึ้นขณะตั้งค่าช่วง คุณสามารถแทนการตั้งค่าเหล่านี้ และสร้างรายงานได้ทันที</span><span class="sxs-lookup"><span data-stu-id="8d296-139">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="8d296-140">สร้างรายงานกลุ่มการรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-140">Generate a report group report</span></span>

1. <span data-ttu-id="8d296-141">ใน Report Designer ในบานหน้าต่างนำทาง คลิก **กลุ่มรายงาน**</span><span class="sxs-lookup"><span data-stu-id="8d296-141">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="8d296-142">เปิดกลุ่มรายงานเพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-142">Open the report group to generate.</span></span>
3. <span data-ttu-id="8d296-143">คลิกปุ่ม **สร้างรายงาน** ![สร้างรายงาน](media/generate-report.gif "สร้างรายงาน") เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-143">Click the **Generate Report** button ![Generate Report](media/generate-report.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="8d296-144">ลบกลุ่มรายงานออก</span><span class="sxs-lookup"><span data-stu-id="8d296-144">Delete a report group</span></span>

1. <span data-ttu-id="8d296-145">ใน Report Designer ในบานหน้าต่างนำทาง คลิก **กลุ่มรายงาน**</span><span class="sxs-lookup"><span data-stu-id="8d296-145">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="8d296-146">คลิกขวากลุ่มรายงานเพื่อลบ จากนั้นเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="8d296-146">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="8d296-147">เมื่อข้อความยืนยันปรากฏขึ้น คลิก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="8d296-147">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="8d296-148">ตัวควบคุมแท็บกลุ่มรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-148">Report Group tab controls</span></span>
<span data-ttu-id="8d296-149">ตารางต่อไปนี้จะให้คำอธิบายเกี่ยวกับตัวควบคุมบนแท็บ **กลุ่มรายงาน**</span><span class="sxs-lookup"><span data-stu-id="8d296-149">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8d296-150">การควบคุม</span><span class="sxs-lookup"><span data-stu-id="8d296-150">Control</span></span></th>
<th><span data-ttu-id="8d296-151">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="8d296-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8d296-152">แทนที่บริษัท รายละเอียด และวันที่การตั้งค่าจากแต่ละข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-152">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="8d296-153">เลือกกล่องกาเครื่องหมายนี้เพื่อแทนข้อกำหนดการรายงานแต่ละรายงานในกลุ่มการรายงานนี้สำหรับการสร้างรายงานเหล่านี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8d296-153">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d296-154">ชื่อบริษัท</span><span class="sxs-lookup"><span data-stu-id="8d296-154">Company name</span></span></td>
<td><span data-ttu-id="8d296-155">เลือกบริษัทที่จะใช้สำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-155">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d296-156">ระดับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="8d296-156">Detail level</span></span></td>
<td><span data-ttu-id="8d296-157">ระบุระดับของรายละเอียดที่มีอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-157">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="8d296-158"><strong>รายงานทางการเงิน</strong>− สรุปข้อมูลระดับสูง</span><span class="sxs-lookup"><span data-stu-id="8d296-158"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="8d296-159">คุณไม่&#39;สามารถดูรายละเอียดแนวลึกไปในบัญชีและมิติ ยกเว้นสำหรับบัญชีและมิติเหล่านั้นที่ได้ถูกเพิ่มผ่านแผนภูมิการรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-159">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="8d296-160"><strong>การเงิน &amp; บัญชี</strong>− รายงานที่ประกอบด้วยข้อมูลสรุปและรายละเอียดทางบัญชีระดับสูง</span><span class="sxs-lookup"><span data-stu-id="8d296-160"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="8d296-161"><strong>การเงิน บัญชี &amp; ธุรกรรม</strong> − รายงานที่ประกอบด้วยข้อมูลสรุปและธุรกรรมทางบัญชีระดับสูง</span><span class="sxs-lookup"><span data-stu-id="8d296-161"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="8d296-162">ส่วนสำรอง</span><span class="sxs-lookup"><span data-stu-id="8d296-162">Provisional</span></span></td>
<td><span data-ttu-id="8d296-163">ระบุชนิดของกิจกรรมที่มีอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-163">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="8d296-164"><strong>เฉพาะกิจกรรมที่ได้ลงรายการบัญชี</strong>−รวมเฉพาะธุรกรรมและยอดดุลที่จะลงรายการบัญชีข้อมูลทางการเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="8d296-164"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="8d296-165"><strong>กิจกรรมที่ลงรายการบัญชีและที่ยังไม่ได้ลงรายการบัญชี</strong>−รวมธุรกรรมและยอดดุลทั้งหมดที่จะป้อน และลงรายการบัญชีในข้อมูลทางการเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="8d296-165"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="8d296-166"><strong>เฉพาะกิจกรรมที่ยังไม่ได้ลงรายการบัญชี</strong>−รวมเฉพาะธุรกรรมและยอดดุลที่จะลงรายการบัญชีข้อมูลทางการเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="8d296-166"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="8d296-167">รวมการรายงานสกุลเงินทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8d296-167">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="8d296-168">สกุลเงินการรายงานเพิ่มเติมใดๆ ที่ถูกตั้งค่าคอนฟิกในระบบ Microsoft Dynamics ERP ของคุณถูกแสดงรายการที่นี่</span><span class="sxs-lookup"><span data-stu-id="8d296-168">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="8d296-169">เลือกกล่องกาเครื่องหมายนี้เพื่อสร้างรายงานเพิ่มเติมในสกุลเงินที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="8d296-169">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="8d296-170">เพื่อดูรายงานเหล่านี้ใน Web Viewer คลิกปุ่ม <strong>สกุลเงิน</strong> และจากนั้นเลือกสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="8d296-170">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d296-171">ข้อมูลวันที่ที่ไม่ได้รับการบันทึก ด้วยข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-171">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="8d296-172">รอบระยะเวลาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="8d296-172">Base period</span></span></li>
<li><span data-ttu-id="8d296-173">ปีพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="8d296-173">Base year</span></span></li>
<li><span data-ttu-id="8d296-174">รอบระยะเวลาที่ครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="8d296-174">Period covered</span></span></li>
</ul>
<span data-ttu-id="8d296-175">เฉพาะการตั้งค่าการเริ่มต้นรอบระยะเวลาฐานถูกบันทึก ด้วยข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-175">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8d296-176">ข้อมูลวันที่ที่ได้รับการบันทึก ด้วยข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-176">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="8d296-177">วันที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-177">Report date</span></span></li>
<li><span data-ttu-id="8d296-178">รอบระยะเวลาฐานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8d296-178">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="8d296-179">รายงานต่างๆในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="8d296-179">Reports in group</span></span></td>
<td><span data-ttu-id="8d296-180">เพิ่ม ลบ และสั่งรายงานต่างๆอีกครั้ง ในกลุ่มการรายงาน</span><span class="sxs-lookup"><span data-stu-id="8d296-180">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="8d296-181">เมื่อต้องการเพิ่มข้อกำหนดของรายงานให้กับกลุ่มรายงาน ดับเบิลคลิกลุ่มรายงาน จะเปิด แล้ว คลิก <strong>เพิ่ม</strong></span><span class="sxs-lookup"><span data-stu-id="8d296-181">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="8d296-182">เลือกรายงานเพื่อรวมในกลุ่มรายงาน จากนั้นคลิก <strong>ตกลง</strong></span><span class="sxs-lookup"><span data-stu-id="8d296-182">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="8d296-183">เมื่อต้องการลบรายงานออกจากกลุ่มการรายงาน เลือกเมื่อต้องการ แล้วคลิก <strong>ลบ</strong></span><span class="sxs-lookup"><span data-stu-id="8d296-183">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="8d296-184">เพื่อปรับเปลี่ยนใบสั่งที่สร้างรายงาน เลือกรายงานในรายการนั้น และคลิก <strong>เลื่อนขึ้น</strong> หรือ <strong>เลื่อนลง</strong></span><span class="sxs-lookup"><span data-stu-id="8d296-184">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="8d296-185">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8d296-185">Additional resources</span></span>

[<span data-ttu-id="8d296-186">การรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8d296-186">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]