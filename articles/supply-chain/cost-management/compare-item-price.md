---
title: รายงานการเปรียบเทียบการจัดเก็บราคาสินค้า
description: เรียนรู้วิธีสร้างรายงานการเปรียบเทียบการจัดเก็บราคาสินค้า และจากนั้นเรียกดูและ/หรือส่งออกผลลัพธ์
author: AndersGirke
manager: AnnBe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 80e376db3616af27d94ee55480cd2f56441db93b
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/19/2020
ms.locfileid: "3072126"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="088a4-103">รายงานการเปรียบเทียบการจัดเก็บราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="088a4-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="088a4-104">หัวข้อนี้จะอธิบายถึงวิธีการรันรายงาน **การเปรียบเทียบการจัดเก็บราคาสินค้า** และทำให้ผลลัพธ์พร้อมใช้งานแบบดิจิตอล เป็นหน้าแบบโต้ตอบใน Dynamics 365 Supply Chain Management หรือเป็นเอกสารที่ส่งออกในรูปแบบใดรูปแบบหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="088a4-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="088a4-105">เมื่อคุณดูรายงานในเบราเซอร์ของคุณ คอลัมน์และยอดดุลรวมจะมีการปรับปรุงแบบไดนามิก โดยขึ้นอยู่กับโครงร่างที่มีการตั้งค่าคอนฟิกของคุณ</span><span class="sxs-lookup"><span data-stu-id="088a4-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="088a4-106">คุณสามารถเรียงลำดับผลลัพธ์ กรองข้อมูล ดูรายละเอียดแนวลึกลงในข้อมูล และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="088a4-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="088a4-107">ผลลัพธ์ของรายงานจะถูกจัดเก็บไว้ในเอนทิตี้ข้อมูล **การเปรียบเทียบราคาสินค้า** ซึ่งช่วยให้คุณสามารถกรองข้อมูลและส่งออกผลลัพธ์ไปยังรูปแบบต่างๆ เช่น CSV หรือ Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="088a4-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="088a4-108">รายงาน **การเปรียบเทียบการจัดเก็บราคาสินค้า** มีประโยชน์ในกรณีที่ผลลัพธ์มีหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="088a4-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="088a4-109">ตัวอย่างเช่น ผลลัพธ์จะประกอบด้วยหลายรายการ ถ้าคุณมีสินค้ามากกว่า 40,000 รายการที่มีราคาสินค้าที่ค้างอยู่ในรุ่นการคิดต้นทุน</span><span class="sxs-lookup"><span data-stu-id="088a4-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="088a4-110">เปิดใช้งานการเปรียบเทียบการจัดเก็บราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="088a4-110">Enable compare item prices storage</span></span>

<span data-ttu-id="088a4-111">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="088a4-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="088a4-112">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งานได้ ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="088a4-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="088a4-113">ต่อไปนี้มีการแสดงรายการคุณลักษณะเป็น:</span><span class="sxs-lookup"><span data-stu-id="088a4-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="088a4-114">**โมดูล** - การจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="088a4-114">**Module** - Cost management</span></span>
- <span data-ttu-id="088a4-115">**ชื่อคุณลักษณะ** - เปรียบเทียบการจัดเก็บราคาของสินค้า</span><span class="sxs-lookup"><span data-stu-id="088a4-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="088a4-116">สร้างรายงานการเปรียบเทียบการจัดเก็บราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="088a4-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="088a4-117">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างและจัดเก็บรายงาน **การเปรียบเทียบการจัดเก็บราคาสินค้า**:</span><span class="sxs-lookup"><span data-stu-id="088a4-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="088a4-118">ไปที่ **การจัดการต้นทุน > การสอบถามและรายงาน > รายงานต้นทุนที่กำหนดไว้ล่วงหน้า > เปรียบเทียบการจัดเก็บราคาสินค้า**</span><span class="sxs-lookup"><span data-stu-id="088a4-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="088a4-119">เลือก **สร้าง** เพื่อเปิดบานหน้าต่าง **เปรียบเทียบราคาสินค้า**</span><span class="sxs-lookup"><span data-stu-id="088a4-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="088a4-120">ตั้งค่าตัวเลือกต่อไปนี้เพื่อกำหนดราคาที่จะเปรียบเทียบในรายงานของคุณ:</span><span class="sxs-lookup"><span data-stu-id="088a4-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="088a4-121">บน FastTab **พารามิเตอร์** ให้รายงาน **ชื่อ** ที่ไม่ซ้ำกัน และใช้ฟิลด์ในส่วน **ราคาที่ค้างอยู่เพื่อเปรียบเทียบ** และ **ราคาที่ใช้สำหรับการเปรียบเทียบ** เพื่อกำหนดราคาและวันที่ที่จะเปรียบเทียบ</span><span class="sxs-lookup"><span data-stu-id="088a4-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="088a4-122">บน FastTab **เรกคอร์ดที่จะรวม** ให้ตั้งค่าตัวกรองข้อมูลและข้อจำกัดเพื่อกำหนดข้อมูลที่จะรวมไว้ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="088a4-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="088a4-123">บน FastTab **รันในพื้นหลัง** ให้ตั้งค่าวิธีการ เวลา และความถี่ที่คุณต้องการสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="088a4-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="088a4-124">มีการดำเนินการรายงานนี้เสมอโดยเป็นส่วนหนึ่งของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="088a4-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="088a4-125">เลือก **ตกลง** เพื่อใช้การตั้งค่าของคุณ และปิดบานหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="088a4-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="088a4-126">หลังจากชุดงานเสร็จสมบูรณ์แล้ว จะมีการแสดงรายการอยู่บนหน้า **การเปรียบเทียบการจัดเก็บราคาสินค้า**</span><span class="sxs-lookup"><span data-stu-id="088a4-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="088a4-127">คุณอาจจำเป็นต้องรีเฟรชหน้าเพื่อดูรายงาน</span><span class="sxs-lookup"><span data-stu-id="088a4-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="088a4-128">สำรวจรายงานการเปรียบเทียบการจัดเก็บราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="088a4-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="088a4-129">หลังจากที่คุณสร้างรายงานแล้ว คุณสามารถดูและสำรวจได้ตลอดเวลาดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="088a4-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="088a4-130">ไปที่ **การจัดการต้นทุน > การสอบถามและรายงาน > รายงานต้นทุนที่กำหนดไว้ล่วงหน้า > เปรียบเทียบการจัดเก็บราคาสินค้า**</span><span class="sxs-lookup"><span data-stu-id="088a4-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="088a4-131">เลือกรายงานจากรายการ</span><span class="sxs-lookup"><span data-stu-id="088a4-131">Select a report from the list.</span></span>

1. <span data-ttu-id="088a4-132">ดำเนินการตามข้อใดข้อหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="088a4-132">Do one of the following:</span></span>

    - <span data-ttu-id="088a4-133">เลือก **ภาพรวม** เพื่อดูภาพรวมของผลลัพธ์ของรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="088a4-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="088a4-134">เลือก **ดูรายละเอียด** เพื่อดูมุมมองโดยละเอียดเพิ่มเติมของรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="088a4-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="088a4-135">หลังจากที่มุมมองที่เลือกเปิดขึ้น คุณสามารถดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="088a4-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="088a4-136">เลือกส่วนหัวของคอลัมน์ใดๆ เกือบทั้งหมดเพื่อเรียงลำดับหรือกรองข้อมูลตารางตามค่าในคอลัมน์นั้น เช่นเดียวกับฟอร์มมาตรฐานส่วนใหญ่ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="088a4-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="088a4-137">โปรดทราบว่า คุณไม่สามารถเรียงลำดับหรือกรองข้อมูลคอลัมน์ **ราคาเปลี่ยนแปลงสุทธิ %** ได้ เนื่องจากฟิลด์นี้เป็นฟิลด์ที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="088a4-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="088a4-138">เลือก **การแสดงมิติ** เพื่อเปิดบานหน้าต่างที่ซึ่งคุณสามารถเลือกคอลัมน์มิติที่จะรวมไว้ในฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="088a4-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="088a4-139">ตั้งค่า **บันทึกการตั้งค่า** เป็น **ใช่** ถ้าคุณต้องการบันทึกการตั้งค่าเหล่านี้ ดังนั้นจะมีการเก็บรักษาไว้ในครั้งต่อไปที่คุณเปิดรายงาน</span><span class="sxs-lookup"><span data-stu-id="088a4-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="088a4-140">เลือก **ตกลง** เพื่อใช้การตั้งค่าของคุณและปิด</span><span class="sxs-lookup"><span data-stu-id="088a4-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="088a4-141">เลือกแถวใดก็ได้ในฟอร์ม แล้วเลือก **ดูรายละเอียด** เพื่อดูข้อมูลเพิ่มเติมเกี่ยวกับสินค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088a4-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="088a4-142">คุณจะสามารถดูรายละเอียดแนวลึกของข้อมูลจากที่นี่ได้</span><span class="sxs-lookup"><span data-stu-id="088a4-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="088a4-143">เลือกแถวใดก็ได้ในแบบฟอร์ม แล้วเลือก **ดูแผนภูมิเปรียบเทียบ** เพื่อดูการแสดงผลกราฟิกแบบโต้ตอบของผลลัพธ์ของคุณตามที่เกี่ยวข้องกับสินค้าที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="088a4-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="088a4-144">คุณสามารถสำรวจผลลัพธ์เหล่านี้ได้ด้วยการเลือกองค์ประกอบแบบกราฟิกต่างๆ ในแผนภูมิและสัญลักษณ์ของแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="088a4-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="088a4-145">เลือกแถวใดก็ได้ในฟอร์ม แล้วเลือก **ดูรายละเอียดการคำนวณ** เพื่อดูข้อมูลเพิ่มเติมเกี่ยวกับการคำนวณที่เกี่ยวข้องกับสินค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="088a4-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="088a4-146">คุณจะสามารถดูรายละเอียดแนวลึกของข้อมูลจากที่นี่ได้</span><span class="sxs-lookup"><span data-stu-id="088a4-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="088a4-147">ส่งออกรายงานการเปรียบเทียบการจัดเก็บราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="088a4-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="088a4-148">แต่ละรายงานที่คุณสร้างจะถูกจัดเก็บไว้ในเอนทิตี้ข้อมูล **การเปรียบเทียบราคาสินค้า**</span><span class="sxs-lookup"><span data-stu-id="088a4-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="088a4-149">คุณสามารถใช้คุณลักษณะการจัดการข้อมูลมาตรฐานของ Supply Chain Management เพื่อส่งออกข้อมูลจากเอนทิตี้นี้ไปยังรูปแบบข้อมูลใดๆ ที่ได้รับการสนับสนุน ซึ่งรวมถึง CSV หรือ Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="088a4-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="088a4-150">ต่อไปนี้เป็นตัวอย่างของวิธีการส่งออกรายงาน **การเปรียบเทียบการจัดเก็บราคาสินค้า**:</span><span class="sxs-lookup"><span data-stu-id="088a4-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="088a4-151">ไปที่ **การจัดการระบบ > พื้นที่ทำงาน > การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="088a4-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="088a4-152">เลือกปุ่ม **ส่งออก** ในส่วน **การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="088a4-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="088a4-153">หน้า **ส่งออก** จะเปิดขึ้น ซึ่งคุณจะใช้เพื่อตั้งค่างานการส่งออกของคุณ</span><span class="sxs-lookup"><span data-stu-id="088a4-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="088a4-154">เริ่มต้นด้วยการตั้ง **ชื่อกลุ่ม** ให้กับงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="088a4-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="088a4-155">ในส่วน **เอนทิตี้ที่เลือก** ให้เลือก **เพิ่มเอนทิตี้** เพื่อเปิดกล่องโต้ตอบที่ซึ่งคุณสามารถตั้งค่าตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="088a4-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="088a4-156">**ชื่อเอนทิตี้** - เลือก **การเปรียบเทียบราคาสินค้า**</span><span class="sxs-lookup"><span data-stu-id="088a4-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="088a4-157">**รูปแบบข้อมูลเป้าหมาย** - เลือกรูปแบบที่คุณต้องการส่งออกไป</span><span class="sxs-lookup"><span data-stu-id="088a4-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="088a4-158">เลือก **เพิ่ม** เพื่อเพิ่มแถวใหม่ แล้วเลือก **ปิด** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="088a4-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="088a4-159">โดยปกติแล้วคุณจะส่งออกรายงานครั้งละหนึ่งฉบับ</span><span class="sxs-lookup"><span data-stu-id="088a4-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="088a4-160">เมื่อต้องการทำเช่นนี้ ให้ตั้งค่า **ตัวกรอง** สำหรับแถวที่คุณเพิ่งเพิ่มไปยังบานหน้าต่าง **การสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="088a4-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="088a4-161">การทำเช่นนี้จะช่วยให้คุณสามารถกำหนดว่ารายงานใดจากเอนทิตี้ **การเปรียบเทียบราคาสินค้า** ที่คุณต้องการรวมไว้ในการส่งออกของคุณ</span><span class="sxs-lookup"><span data-stu-id="088a4-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="088a4-162">ตั้งค่าตัวเลือกตัวกรองต่อไปนี้เพื่อส่งออกรายงานฉบับเดียว:</span><span class="sxs-lookup"><span data-stu-id="088a4-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="088a4-163">บนแท็บ **ช่วง** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถวใหม่</span><span class="sxs-lookup"><span data-stu-id="088a4-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="088a4-164">ตั้งค่า **ตาราง** เป็น **การเปรียบเทียบราคาสินค้า**</span><span class="sxs-lookup"><span data-stu-id="088a4-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="088a4-165">ตั้งค่า **ตารางสืบทอด** เป็น **การเปรียบเทียบราคาสินค้า**</span><span class="sxs-lookup"><span data-stu-id="088a4-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="088a4-166">ตั้งค่า **ฟิลด์** เป็นฟิลด์ที่คุณต้องการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="088a4-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="088a4-167">โดยปกติแล้วคุณจะใช้ **ชื่อในการดำเนินการ** หรือ **เวลาในการดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="088a4-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="088a4-168">กำหนด **เงื่อนไข** ให้กับค่าจากฟิลด์ที่เลือกของคุณซึ่งคุณต้องการค้นหา (ชื่อของรายงาน หรือเวลาที่มีการสร้างรายงาน อย่างใดอย่างหนึ่ง)</span><span class="sxs-lookup"><span data-stu-id="088a4-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="088a4-169">ถ้าจำเป็น ให้เพิ่มแถวเพิ่มเติมในตาราง **ช่วง** จนกว่าคุณจะระบุรายงานที่คุณกำลังค้นหาโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="088a4-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="088a4-170">เลือก **ตกลง** เพื่อบันทึกการตั้งค่าของคุณและปิด</span><span class="sxs-lookup"><span data-stu-id="088a4-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="088a4-171">เลือก **บันทึก** เพื่อบันทึกการตั้งค่าการส่งออกของคุณ</span><span class="sxs-lookup"><span data-stu-id="088a4-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="088a4-172">เปิดแท็บ **ตัวเลือกการส่งออก** และเลือก **ส่งออกเดี๋ยวนี้** เพื่อสร้างไฟล์การส่งออก</span><span class="sxs-lookup"><span data-stu-id="088a4-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="088a4-173">หน้า **สรุปการดำเนินการ** จะเปิดขึ้น ซึ่งคุณสามารถดูสถานะของงานการส่งออกของคุณและรายการเอนทิตี้ที่มีการส่งออก</span><span class="sxs-lookup"><span data-stu-id="088a4-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="088a4-174">เลือกเอนทิตี้ **เปรียบเทียบราคาสินค้า** ที่แสดงรายการอยู่ในพื้นที่ **สถานะการประมวลผลเอนทิตี้** และจากนั้น เลือก **ดาวน์โหลดไฟล์** เพื่อดาวน์โหลดข้อมูลที่ส่งออกจากเอนทิตี้นั้น</span><span class="sxs-lookup"><span data-stu-id="088a4-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="088a4-175">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้การจัดการข้อมูลเพื่อส่งออกข้อมูล โปรดดู [ภาพรวมของงานนำเข้าและส่งออกข้อมูล](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)</span><span class="sxs-lookup"><span data-stu-id="088a4-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
