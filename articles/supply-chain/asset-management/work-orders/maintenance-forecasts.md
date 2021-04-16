---
title: การคาดการณ์ในการบำรุงรักษา
description: หัวข้อนี้อธิบายถึงการคาดการณ์ในการบำรุงรักษาในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dd652af3100f8de59e06490443baeebca58a4dd3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838549"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="1830f-103">การคาดการณ์ในการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1830f-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="1830f-104">เมื่อคุณสร้างใบสั่งงาน คุณสร้างงานใบสั่งงานที่มีสินทรัพย์และชนิดงานบำรุงรักษาที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="1830f-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="1830f-105">เมื่อคุณเลือกชนิดงานบำรุงรักษาที่มีการคาดการณ์ในการบำรุงรักษา การคาดการณ์จะถูกคัดลอกไปยังใบสั่งงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="1830f-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="1830f-106">คุณอาจเพิ่มรายการการคาดการณ์ไปยังใบสั่งงานหรือลบบรรทัดเหล่านั้นออกจากใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1830f-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="1830f-107">การตั้งค่าสถานะของวงจรการใช้ของใบสั่งงาน ชนิดโครงการที่เกี่ยวข้อง และกฎขั้นที่เกี่ยวข้องกับชนิดโครงการ จะเป็นตัวกำหนดว่าคุณสามารถเพิ่มหรือแก้ไขรายการการคาดการณ์ได้</span><span class="sxs-lookup"><span data-stu-id="1830f-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="1830f-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสถานะของวงจรการใช้ของใบสั่งงานและขั้นโครงการที่เกี่ยวข้อง ดู [การคาดการณ์ ใบสั่งงาน และโครงการ](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md)</span><span class="sxs-lookup"><span data-stu-id="1830f-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="1830f-109">เลือก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="1830f-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="1830f-110">เลือกใบสั่งงานในรายการ และจากนั้น บนบานหน้าต่างการดำเนินการ > แท็บ **ใบสั่งงาน** > กลุ่ม **โครงการ** ให้เลือก **การคาดการณ์**</span><span class="sxs-lookup"><span data-stu-id="1830f-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="1830f-111">หน้า **การคาดการณ์ในการบำรุงรักษาของใบสั่งงาน** แสดงรายการการคาดการณ์จากชนิดงานการบำรุงรักษาที่ถูกเลือกในงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1830f-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="1830f-112">เพิ่มการคาดการณ์ชั่วโมงไปที่ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1830f-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="1830f-113">บนหน้า **การคาดการณ์ในการบำรุงรักษาของใบสั่งงาน** เลือกงานใบสั่งงานเพื่อเพิ่มการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="1830f-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="1830f-114">บน FastTab **ชั่วโมง** เลือก **เพิ่ม** เพื่อสร้างรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="1830f-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="1830f-115">ในฟิลด์ **ประเภท** เลือกประเภท</span><span class="sxs-lookup"><span data-stu-id="1830f-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="1830f-116">ในฟิลด์ **ชั่วโมง** ป้อนจำนวนของชั่วโมงที่คาดการณ์</span><span class="sxs-lookup"><span data-stu-id="1830f-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="1830f-117">ในฟิลด์ **คุณสมบัติของรายการ** ให้เลือกชนิดของค่าธรรมเนียมที่ควรจะใช้ในรายการ</span><span class="sxs-lookup"><span data-stu-id="1830f-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="1830f-118">เพิ่มการคาดการณ์สินค้าไปที่ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1830f-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="1830f-119">มีสามวิธีในการเพิ่มสินค้าลงในการคาดการณ์การบำรุงรักษาของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1830f-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="1830f-120">คุณสามารถสร้างรายการสำหรับสินค้า (อะไหล่สำรอง) ที่ไม่ได้รวมอยู่ในรายการอะไหล่สำรองหรือสูตรการผลิตของสินทรัพย์ (BOM) คุณสามารถเลือกอะไหล่สำรองจากรายการอะไหล่สำรองที่ได้รับอนุมัติ หรือคุณสามารถเลือกสินค้าจาก BOM สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1830f-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="1830f-121">บนหน้า **การคาดการณ์ในการบำรุงรักษาของใบสั่งงาน** เลือกงานใบสั่งงานเพื่อเพิ่มการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="1830f-121">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

- <span data-ttu-id="1830f-122">บน FastTab **สินค้า** ให้เพิ่มสินค้าลงในการคาดการณ์ในการบำรุงรักษาโดยใช้วิธีการที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="1830f-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="1830f-123">เพื่อสร้างรายการใหม่สำหรับอะไหล่สำรองที่ไม่ได้อยู่ในรายการอะไหล่สำรองหรือBOM สินทรัพย์ ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1830f-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="1830f-124">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="1830f-124">Select **Add**.</span></span>
2. <span data-ttu-id="1830f-125">ในฟิลด์ **หมายเลขสินค้า** เลือกสินค้า</span><span class="sxs-lookup"><span data-stu-id="1830f-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="1830f-126">ในฟิลด์ **ปริมาณการขาย** ป้อนปริมาณ</span><span class="sxs-lookup"><span data-stu-id="1830f-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="1830f-127">ในฟิลด์ **หน่วย** เลือกหน่วยวัดสำหรับปริมาณ</span><span class="sxs-lookup"><span data-stu-id="1830f-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="1830f-128">ในฟิลด์ **ราคาต้นทุน** และฟิลด์ **สกุลเงิน** ป้อนค่าที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="1830f-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="1830f-129">ในฟิลด์ **ลักษณะของรายการ** ให้เลือกลักษณะของรายการ</span><span class="sxs-lookup"><span data-stu-id="1830f-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="1830f-130">ถ้าคุณต้องการเปลี่ยนรายการของมิติที่แสดงบนรายการสินค้า ให้เลือก **สินค้าคงคลัง** > **แสดงมิติ** เลือกมิติ และจากนั้น ตั้งค่าตัวเลือก **บันทึกการตั้งค่า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="1830f-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="1830f-131">เมื่อต้องการเพิ่มอะไหล่สำรองจากรายการอะไหล่ที่อนุมัติ ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1830f-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="1830f-132">เลือก **เพิ่มอะไหล่สำรอง**</span><span class="sxs-lookup"><span data-stu-id="1830f-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="1830f-133">เลือกอะไหล่สำรอง และแก้ไขข้อมูลที่เกี่ยวข้องตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1830f-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="1830f-134">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1830f-134">Select **OK**.</span></span>

<span data-ttu-id="1830f-135">เมื่อต้องการเพิ่มสินค้าจาก BOM สินทรัพย์ ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1830f-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="1830f-136">เลือก **เพิ่มสินค้า BOM**</span><span class="sxs-lookup"><span data-stu-id="1830f-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="1830f-137">เลือกสินค้า และแก้ไขข้อมูลที่เกี่ยวข้องตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1830f-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="1830f-138">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1830f-138">Select **OK**.</span></span>

<span data-ttu-id="1830f-139">การเรียกดูภาพรวมที่แสดงตำแหน่งในรายการที่เลือกถูกใช้โดยสัมพันธ์กับสินทรัพย์ ค่าเริ่มต้นของชนิดงานบำรุงรักษา อะไหล่สำรอง และใบสั่งงานในการจัดการสินทรัพย์ เลือก **สินค้าที่ใช้**</span><span class="sxs-lookup"><span data-stu-id="1830f-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="1830f-140">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับภาพรวมนี้ โปรดดู [สินค้าที่ใช้](../controlling-and-reporting/item-where-used.md)</span><span class="sxs-lookup"><span data-stu-id="1830f-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="1830f-141">เพิ่มการคาดการณ์ค่าใช้จ่ายไปที่ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1830f-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="1830f-142">บนหน้า **การคาดการณ์ในการบำรุงรักษาของใบสั่งงาน** เลือกงานใบสั่งงานเพื่อเพิ่มการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="1830f-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="1830f-143">บน FastTab **ค่าใช้จ่าย** เลือก **เพิ่ม** เพื่อสร้างรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="1830f-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="1830f-144">ในฟิลด์ **ประเภท** เลือกประเภท</span><span class="sxs-lookup"><span data-stu-id="1830f-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="1830f-145">ในฟิลด์ **ปริมาณ** ป้อนปริมาณ</span><span class="sxs-lookup"><span data-stu-id="1830f-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="1830f-146">ในฟิลด์ **ราคาต้นทุน** **สกุลเงินการขาย** และ **ราคาขาย** ป้อนค่าที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="1830f-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="1830f-147">ในฟิลด์ **คุณสมบัติของรายการ** ให้เลือกชนิดของค่าธรรมเนียมที่ควรจะใช้ในรายการ</span><span class="sxs-lookup"><span data-stu-id="1830f-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="1830f-148">บน FastTab **ผลรวมการคาดการณ์ในการบำรุงรักษา** แสดงภาพรวมของจำนวนรายการที่ได้ถูกสร้างขึ้น สำหรับงานใบสั่งงานที่เลือกและสำหรับใบสั่งงานบน FastTab แต่ละแท็บ</span><span class="sxs-lookup"><span data-stu-id="1830f-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="1830f-149">นอกจากนี้ ยังแสดงผลรวมของชั่วโมงการทำงานที่คาดการณ์ไว้สำหรับงานใบสั่งงานและใบสั่งงานด้วย</span><span class="sxs-lookup"><span data-stu-id="1830f-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="1830f-150">ภาพประกอบด้านล่างแสดงตัวอย่างของหน้า **การคาดการณ์ในการบำรุงรักษาของใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="1830f-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![รูปที่ 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="1830f-152">การอัพเดตอัตโนมัติของการคาดการณ์ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1830f-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="1830f-153">ถ้าต้นทุนชั่วโมง ต้นทุนสินค้า และค่าใช้จ่ายถูกอัพเดตในโมดูลอื่นๆ ใน Microsoft Dynamics 365 for Finance and Operations จะสามารถอัพเดตการคาดการณ์ใบสั่งงานในการจัดการสินทรัพย์ให้สะท้อนถึงการเปลี่ยนแปลงเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="1830f-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="1830f-154">ความสามารถนี้ช่วยรับประกันว่ามีการใช้ราคาต้นทุนล่าสุดอยู่เสมอในการคาดการณ์ใบสั่งงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="1830f-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="1830f-155">นอกจากนี้ คุณยังสามารถทำการอัพเดตที่คล้ายกันสำหรับ [การคาดการณ์ชนิดงานบำรุงรักษา](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="1830f-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="1830f-156">เลือก **การจัดการสินทรัพย์** > **ประจำงวด** > **การคาดการณ์** > **อัพเดตการคาดการณ์ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="1830f-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="1830f-157">ในกล่องโต้ตอบ **อัพเดตการคาดการณ์ใบสั่งงาน** บน FastTab **เรกคอร์ดที่จะรวม** คุณสามารถเพิ่มการเลือกที่เกี่ยวข้องกับใบสั่งงานหรืองานใบสั่งงานเฉพาะได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1830f-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="1830f-158">คลิก **ตัวกรอง** เพื่อทำการเลือกที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="1830f-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="1830f-159">บน FastTab **รันในเบื้องหลัง** คุณสามารถตั้งค่าการปรับปรุงอัตโนมัติเป็นชุดงานได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1830f-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="1830f-160">เลือก **ตกลง** เพื่อเริ่มต้นการปรับปรุงการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="1830f-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="1830f-161">ภาพประกอบด้านล่างแสดงตัวอย่างของกล่องโต้ตอบ **อัพเดตการคาดการณ์ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="1830f-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![รูปที่ 2](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]