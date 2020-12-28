---
title: รายงานการจัดเก็บมูลค่าสินค้าคงคลัง
description: หัวข้อนี้จะอธิบายถึงวิธีการรันรายงานการจัดเก็บมูลค่าสินค้าคงคลัง และทำให้ผลลัพธ์พร้อมใช้งานแบบดิจิตอล เป็นหน้าแบบโต้ตอบใน Microsoft Dynamics 365 Supply Chain Management หรือเป็นเอกสารที่ส่งออกในรูปแบบใดรูปแบบหนึ่ง
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f50318e0a955d8244ba854aa1fd73ad7532b9198
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438457"
---
# <a name="inventory-value-storage-report"></a><span data-ttu-id="7a68d-103">รายงานการจัดเก็บมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7a68d-103">Inventory value storage report</span></span>

<span data-ttu-id="7a68d-104">หัวข้อนี้จะอธิบายถึงวิธีการรันรายงาน **การจัดเก็บมูลค่าสินค้าคงคลัง** และทำให้ผลลัพธ์พร้อมใช้งานแบบดิจิตอล เป็นหน้าแบบโต้ตอบใน Microsoft Dynamics 365 Supply Chain Management หรือเป็นเอกสารที่ส่งออกในรูปแบบใดรูปแบบหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7a68d-104">This topic explains how to run an **Inventory value storage** report and make the output available digitally, either as an interactive page in Microsoft Dynamics 365 Supply Chain Management or as an exported document in any of several formats.</span></span>

<span data-ttu-id="7a68d-105">เมื่อคุณดูรายงานในเบราเซอร์ของคุณ คอลัมน์และยอดดุลรวมจะมีการปรับปรุงแบบไดนามิก โดยขึ้นอยู่กับโครงร่างที่คุณตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="7a68d-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on the layout that you've configured.</span></span> <span data-ttu-id="7a68d-106">คุณสามารถเรียงลำดับผลลัพธ์ กรองข้อมูล ดูรายละเอียดแนวลึกลงในข้อมูล และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="7a68d-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="7a68d-107">ผลลัพธ์ของรายงานจะถูกจัดเก็บไว้ในเอนทิตี้ข้อมูล **มูลค่าของสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="7a68d-107">Report results are stored in the **Inventory value** data entity.</span></span> <span data-ttu-id="7a68d-108">ดังนั้น คุณจึงสามารถกรองและส่งออกผลลัพธ์ไปยังรูปแบบต่างๆ เช่น ค่าที่แบ่งด้วยเครื่องหมายจุลภาค (CSV) หรือรูปแบบ Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="7a68d-108">Therefore, you can filter and export the results to a format such as comma-separated values (CSV) or Microsoft Excel format.</span></span>

<span data-ttu-id="7a68d-109">รายงาน **การจัดเก็บมูลค่าสินค้าคงคลัง** จะมีประโยชน์ เมื่อผลลัพธ์มีหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="7a68d-109">The **Inventory value storage** report is helpful when the output contains many lines.</span></span> <span data-ttu-id="7a68d-110">ตัวอย่างเช่น คุณมีสินค้า 50,000 รายการและมีการสร้างร้านค้า 300 แห่ง เป็นคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a68d-110">For example, you have 50,000 items, and 300 stores have been created as warehouses.</span></span> <span data-ttu-id="7a68d-111">ในกรณีนี้ ถ้าคุณร้องขอยอดดุลสิ้นงวดของสินค้าคงคลังโดยเรียงตามสินค้า ไซต์ และคลังสินค้า ผลลัพธ์จะประกอบด้วยหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="7a68d-111">In this case, if you request inventory ending balances by item, site, and warehouse, the output will contain many lines.</span></span>

> [!NOTE]
> <span data-ttu-id="7a68d-112">รายงานจะไม่มีผลรวมย่อยที่กำหนดไว้ในโครงร่างรายงาน</span><span class="sxs-lookup"><span data-stu-id="7a68d-112">The report won't include subtotals that are defined in the report layout.</span></span> <span data-ttu-id="7a68d-113">นอกจากนี้ จะไม่มีการรวมยอดดุลบัญชีแยกประเภททั่วไป แม้กระทั่งเวลาที่จะมีการกำหนดในโครงร่างรายงาน</span><span class="sxs-lookup"><span data-stu-id="7a68d-113">It also won't include general ledger balances, even when they are defined in the report layout.</span></span> <span data-ttu-id="7a68d-114">ต้องทำการกระทบยอดกับบัญชีแยกประเภททั่วไปโดยใช้ยอดดุลทดลอง</span><span class="sxs-lookup"><span data-stu-id="7a68d-114">Reconciliation to the general ledger must be done by using trial balances.</span></span>

## <a name="turn-on-the-inventory-value-storage-feature"></a><span data-ttu-id="7a68d-115">เปิดใช้งานคุณลักษณะการจัดเก็บมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7a68d-115">Turn on the Inventory value storage feature</span></span>

<span data-ttu-id="7a68d-116">ก่อนที่คุณจะสามารถสร้างรายงาน **การจัดเก็บมูลค่าสินค้าคงคลัง** คุณต้องเปิดใช้งานคุณลักษณะในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="7a68d-116">Before you can generate an **Inventory value storage** report, you must turn on the feature in your system.</span></span> <span data-ttu-id="7a68d-117">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="7a68d-117">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="7a68d-118">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7a68d-118">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7a68d-119">**โมดูล** – การจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7a68d-119">**Module** – Cost management</span></span>
- <span data-ttu-id="7a68d-120">**ชื่อคุณลักษณะ** – การจัดเก็บมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7a68d-120">**Feature name** – Inventory value storage</span></span>

## <a name="generate-an-inventory-value-storage-report"></a><span data-ttu-id="7a68d-121">สร้างรายงานการจัดเก็บมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7a68d-121">Generate an Inventory value storage report</span></span>

<span data-ttu-id="7a68d-122">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างและจัดเก็บรายงาน **การจัดเก็บมูลค่าสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="7a68d-122">Follow these steps to generate and store an **Inventory value storage** report.</span></span>

1. <span data-ttu-id="7a68d-123">ไปที่ **การจัดการต้นทุน \> การสอบถามและรายงาน \> การจัดเก็บรายงานมูลค่าสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="7a68d-123">Go to **Cost management \> Inquiries and reports \> Inventory value report storage**.</span></span>
1. <span data-ttu-id="7a68d-124">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="7a68d-124">Select **New**.</span></span>
1. <span data-ttu-id="7a68d-125">ในกล่องโต้ตอบ **มูลค่าสินค้าคงคลัง** ที่ปรากฏขึ้น ให้ตั้งค่าต่อไปนี้เพื่อกำหนดว่าจะรวมเรกคอร์ดใดในรายงานของคุณ:</span><span class="sxs-lookup"><span data-stu-id="7a68d-125">In the **Inventory value** dialog box that appears, set the following values to define which records are included in your report:</span></span>

    - <span data-ttu-id="7a68d-126">บน FastTab **พารามิเตอร์** ให้ป้อนชื่อที่ไม่ซ้ำกันสำหรับรายงาน และใช้ฟิลด์ในส่วน **ช่วงวันที่** เพื่อกำหนดว่าเรกคอร์ดใดจะถูกรวมอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="7a68d-126">On the **Parameters** FastTab, enter a unique name for the report, and use the fields in the **Date interval** section to define which records are included in the report.</span></span> <span data-ttu-id="7a68d-127">เมื่อต้องการกำหนดช่วงวันที่ คุณสามารถเลือกช่วงที่กำหนดไว้ล่วงหน้า (เทียบกับวันที่สร้างรายงาน) ในฟิลด์ **รหัสช่วงวันที่** หรือเลือกวันที่เฉพาะในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="7a68d-127">To define the date interval, you can either select a preset range (relative to the report generation date) in the **Date interval code** field, or select specific dates in the **From date** and **To date** fields.</span></span>
    - <span data-ttu-id="7a68d-128">บน FastTab **เรกคอร์ดที่จะรวม** ให้ตั้งค่าตัวกรองข้อมูลและข้อจำกัดเพื่อกำหนดข้อมูลที่จะถูกรวมไว้ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="7a68d-128">On the **Records to include** FastTab, set up filters and constraints to define which data is included in the report.</span></span>
    - <span data-ttu-id="7a68d-129">บน FastTab **รันในเบื้องหลัง** ให้ระบุว่าจะสร้างรายงานอย่างไร เมื่อใด และบ่อยครั้งเพียงใด</span><span class="sxs-lookup"><span data-stu-id="7a68d-129">On the **Run in the background** FastTab, specify how, when, and how often the report is generated.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7a68d-130">มีการรันรายงานนี้เสมอโดยเป็นส่วนหนึ่งของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="7a68d-130">This report is always run as part of a batch job.</span></span>

1. <span data-ttu-id="7a68d-131">เลือก **ตกลง** เพื่อใช้การตั้งค่าของคุณ และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="7a68d-131">Select **OK** to apply your settings and close the dialog box.</span></span>

<span data-ttu-id="7a68d-132">หลังจากชุดงานเสร็จสมบูรณ์ รายงานจะถูกแสดงรายการบนหน้า **การจัดเก็บรายงานมูลค่าสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="7a68d-132">After the batch job is completed, the report will be listed on the **Inventory value report storage** page.</span></span> <span data-ttu-id="7a68d-133">คุณอาจต้องรีเฟรชหน้าเพื่อดูรายงาน</span><span class="sxs-lookup"><span data-stu-id="7a68d-133">You might have to refresh the page to see the report.</span></span>

## <a name="explore-an-inventory-value-storage-report"></a><span data-ttu-id="7a68d-134">สำรวจรายงานการจัดเก็บมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7a68d-134">Explore an Inventory value storage report</span></span>

<span data-ttu-id="7a68d-135">หลังจากที่คุณสร้างรายงานแล้ว คุณสามารถดูและสำรวจได้ตลอดเวลาโดยทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7a68d-135">After you've generated a report, you can view and explore it at any time by following these steps.</span></span>

1. <span data-ttu-id="7a68d-136">ไปที่ **การจัดการต้นทุน \> การสอบถามและรายงาน \> การจัดเก็บรายงานมูลค่าสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="7a68d-136">Go to **Cost management \> Inquiries and reports \> Inventory value report storage**.</span></span>
1. <span data-ttu-id="7a68d-137">เลือกรายงานในรายการ</span><span class="sxs-lookup"><span data-stu-id="7a68d-137">Select a report in the list.</span></span>
1. <span data-ttu-id="7a68d-138">เลือก **ดูรายละเอียด** เพื่อแสดงเนื้อหารายงาน</span><span class="sxs-lookup"><span data-stu-id="7a68d-138">Select **View details** to show the report content.</span></span>
1. <span data-ttu-id="7a68d-139">สำรวจรายงานโดยปฏิบัติตามขั้นตอนใดๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7a68d-139">Explore the report by following any of these steps:</span></span>

    - <span data-ttu-id="7a68d-140">เช่นกันกับหน้ามาตรฐานส่วนใหญ่ใน Supply Chain Management คุณสามารถเลือกส่วนหัวของคอลัมน์ใดๆ ได้เกือบทั้งหมดเพื่อเรียงลำดับหรือกรองข้อมูลกริดตามค่าในคอลัมน์นั้น</span><span class="sxs-lookup"><span data-stu-id="7a68d-140">As for most standard pages in Supply Chain Management, you can select almost any column heading to sort or filter the grid by the values in that column.</span></span>
    - <span data-ttu-id="7a68d-141">ใช้ฟิลด์ **ตัวกรองข้อมูล** เพื่อกรองรายงานตามค่าใดๆ ในคอลัมน์ใดๆ ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7a68d-141">Use the **Filter** field to filter the report by any value in any of several available columns.</span></span>
    - <span data-ttu-id="7a68d-142">ใช้เมนูมุมมอง (เหนือฟิลด์ **ตัวกรองข้อมูล**) เพื่อบันทึกและโหลดชุดโปรดของตัวเลือกการเรียงลำดับและการกรองข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="7a68d-142">Use the view menu (above the **Filter** field) to save and load your favorite combinations of sort and filter options.</span></span>

## <a name="export-an-inventory-value-storage-report"></a><span data-ttu-id="7a68d-143">ส่งออกรายงานการจัดเก็บมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7a68d-143">Export an Inventory value storage report</span></span>

<span data-ttu-id="7a68d-144">รายงานทุกฉบับที่คุณสร้างจะถูกจัดเก็บไว้ในเอนทิตี้ข้อมูล **มูลค่าของสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="7a68d-144">Every report that you generate is stored in the **Inventory value** data entity.</span></span> <span data-ttu-id="7a68d-145">คุณสามารถใช้คุณลักษณะการจัดการข้อมูลมาตรฐานของ Supply Chain Management เพื่อส่งออกข้อมูลจากเอนทิตี้นี้ไปยังรูปแบบข้อมูลใดๆ ที่ได้รับการสนับสนุน เช่น รูปแบบ CSV หรือ Excel</span><span class="sxs-lookup"><span data-stu-id="7a68d-145">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, such as CSV or Excel format.</span></span>

<span data-ttu-id="7a68d-146">ตัวอย่างต่อไปนี้แสดงวิธีการส่งออกรายงาน **รายงานมูลค่าของสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="7a68d-146">The following example shows how to export an **Inventory value report** report.</span></span>

1. <span data-ttu-id="7a68d-147">ไปที่ **การจัดการระบบ \> พื้นที่ทำงาน \> การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="7a68d-147">Go to **System administration \> Workspaces \> Data management**.</span></span>
1. <span data-ttu-id="7a68d-148">ในส่วน **นำเข้า/ส่งออก** ให้เลือกไทล์ **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="7a68d-148">In the **Import / Export** section, select the **Export** tile.</span></span> 
1. <span data-ttu-id="7a68d-149">บนหน้า **ส่งออก** ที่ปรากฏขึ้น คุณจะตั้งค่างานการส่งออก</span><span class="sxs-lookup"><span data-stu-id="7a68d-149">On the **Export** page that appears, you will set up the export job.</span></span> <span data-ttu-id="7a68d-150">อันดับแรกให้ป้อนชื่อกลุ่มสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="7a68d-150">First enter a group name for the job.</span></span>
1. <span data-ttu-id="7a68d-151">ในส่วน **เอนทิตี้ที่เลือก** ให้เลือก **เพิ่มเอนทิตี้**</span><span class="sxs-lookup"><span data-stu-id="7a68d-151">In the **Selected entities** section, select **Add entity**.</span></span>
1. <span data-ttu-id="7a68d-152">ในกล่องโต้ตอบที่ปรากฏขึ้น ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7a68d-152">In the dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="7a68d-153">**ชื่อเอนทิตี้** – เลือก **มูลค่าของสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="7a68d-153">**Entity name** – Select **Inventory value**.</span></span>
    - <span data-ttu-id="7a68d-154">**รูปแบบข้อมูลเป้าหมาย** – เลือกรูปแบบที่จะส่งออกข้อมูลไป</span><span class="sxs-lookup"><span data-stu-id="7a68d-154">**Target data format** – Select the format to export data to.</span></span>

1. <span data-ttu-id="7a68d-155">เลือก **เพิ่ม** เพื่อเพิ่มแถวใหม่ แล้วเลือก **ปิด** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="7a68d-155">Select **Add** to add the new row, and then select **Close** to close the dialog box.</span></span>
1. <span data-ttu-id="7a68d-156">โดยปกติแล้วคุณจะส่งออกรายงานครั้งละหนึ่งฉบับ</span><span class="sxs-lookup"><span data-stu-id="7a68d-156">Usually, you will export one report at a time.</span></span> <span data-ttu-id="7a68d-157">เมื่อต้องการส่งออกรายงานเดียว ให้ตั้งค่าตัวกรองสำหรับแถวที่คุณเพิ่งเพิ่มลงในกล่องโต้ตอบ **การสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="7a68d-157">To export a single report, set up a filter for the row that you just added to the **Inquiry** dialog box.</span></span> <span data-ttu-id="7a68d-158">ด้วยวิธีนี้ คุณสามารถกำหนดรายงานจากเอนทิตี้ **มูลค่าของสินค้าคงคลัง** ที่จะรวมไว้ในการส่งออกของคุณได้</span><span class="sxs-lookup"><span data-stu-id="7a68d-158">In this way, you can define which report from the **Inventory value** entity is included in your export.</span></span> <span data-ttu-id="7a68d-159">ปฏิบัติตามขั้นตอนต่อไปนี้ในการตั้งค่าตัวเลือกตัวกรองต่อไปนี้เพื่อส่งออกรายงานฉบับเดียว:</span><span class="sxs-lookup"><span data-stu-id="7a68d-159">Follow these steps to set the following filter options to export a single report:</span></span>

    1. <span data-ttu-id="7a68d-160">บนแท็บ **ช่วง** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถว</span><span class="sxs-lookup"><span data-stu-id="7a68d-160">On the **Range** tab, select **Add** to add a row.</span></span>
    2. <span data-ttu-id="7a68d-161">ตั้งค่าฟิลด์ **ตาราง** เป็น **มูลค่าของสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="7a68d-161">Set the **Table** field to **Inventory value**.</span></span>
    3. <span data-ttu-id="7a68d-162">ตั้งค่าฟิลด์ **ตารางสืบทอด** เป็น **มูลค่าของสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="7a68d-162">Set the **Derived table** field to **Inventory value**.</span></span>
    4. <span data-ttu-id="7a68d-163">ตั้งค่าฟิลด์ **ฟิลด์** เป็นฟิลด์ที่คุณต้องการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7a68d-163">Set the **Field** field to the field that you want to filter by.</span></span> <span data-ttu-id="7a68d-164">โดยปกติแล้วคุณจะใช้ฟิลด์ **ชื่อการดำเนินการ** และ/หรือฟิลด์ **เวลาที่ใช้ในการดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="7a68d-164">Usually, you will use the **Execution name** field and/or the **Execution time** field.</span></span>
    5. <span data-ttu-id="7a68d-165">ตั้งค่าฟิลด์ **เงื่อนไข** เป็นค่าที่คุณต้องการค้นหาในฟิลด์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7a68d-165">Set the **Criteria** field to the value that you want to look for in the selected field.</span></span> <span data-ttu-id="7a68d-166">(ถ้าคุณเลือกฟิลด์ **ชื่อการดำเนินการ** ในขั้นตอนก่อนหน้านี้ ค่านี้จะเป็นชื่อของรายงาน</span><span class="sxs-lookup"><span data-stu-id="7a68d-166">(If you selected the **Execution name** field in the previous step, this value will be the name of the report.</span></span> <span data-ttu-id="7a68d-167">ถ้าคุณเลือกฟิลด์ **เวลาที่ใช้ในการดำเนินการ** จะเป็นเวลาที่มีการสร้างรายงาน)</span><span class="sxs-lookup"><span data-stu-id="7a68d-167">If you selected the **Execution time** field, it will be the time when the report was generated.)</span></span>
    6. <span data-ttu-id="7a68d-168">เพิ่มแถวเพิ่มเติมไปยังแท็บ **ช่วง** ตามที่คุณต้องการ จนกว่าคุณจะระบุรายงานที่คุณกำลังค้นหาโดยไม่ซ้ำ</span><span class="sxs-lookup"><span data-stu-id="7a68d-168">Add more rows to the **Range** tab as you require, until you've uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="7a68d-169">เลือก **ตกลง** เพื่อบันทึกการตั้งค่าของคุณ และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="7a68d-169">Select **OK** to save your settings and close the dialog box.</span></span>
1. <span data-ttu-id="7a68d-170">เลือก **บันทึก** เพื่อบันทึกการตั้งค่าการส่งออกของคุณ</span><span class="sxs-lookup"><span data-stu-id="7a68d-170">Select **Save** to save your export setup.</span></span>
1. <span data-ttu-id="7a68d-171">บนแท็บ **ตัวเลือกการส่งออก** และเลือก **ส่งออกเดี๋ยวนี้** เพื่อสร้างไฟล์การส่งออก</span><span class="sxs-lookup"><span data-stu-id="7a68d-171">On the **Export options** tab, select **Export now** to generate the export file.</span></span>
1. <span data-ttu-id="7a68d-172">บนหน้า **สรุปการดำเนินการ** ที่ปรากฏขึ้น คุณสามารถดูสถานะของงานการส่งออกของคุณและรายการของเอนทิตี้ที่มีการส่งออก</span><span class="sxs-lookup"><span data-stu-id="7a68d-172">On the **Execution summary** page that appears, you can view the status of your export job and a list of the entities that were exported.</span></span> <span data-ttu-id="7a68d-173">ในส่วน **สถานะการประมวลผลเอนทิตี้** เลือกเอนทิตี้ **มูลค่าของสินค้าคงคลัง** ในรายการ และจากนั้น เลือก **ดาวน์โหลดไฟล์** เพื่อดาวน์โหลดข้อมูลที่ถูกส่งออกจากเอนทิตี้นั้น</span><span class="sxs-lookup"><span data-stu-id="7a68d-173">In the **Entity processing status** section, select the **Inventory value** entity in the list, and then select **Download file** to download the data that was exported from that entity.</span></span>

<span data-ttu-id="7a68d-174">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้การจัดการข้อมูลเพื่อส่งออกข้อมูล โปรดดู [ภาพรวมของงานนำเข้าและส่งออกข้อมูล](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)</span><span class="sxs-lookup"><span data-stu-id="7a68d-174">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
