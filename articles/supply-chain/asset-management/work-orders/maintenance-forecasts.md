---
title: การคาดการณ์ในการบำรุงรักษา
description: หัวข้อนี้อธิบายถึงการคาดการณ์ในการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024510"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="08a21-103">การคาดการณ์ในการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="08a21-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="08a21-104">เมื่อคุณสร้างใบสั่งงาน คุณสร้างงานใบสั่งงานกับสินทรัพย์และชนิดงานบำรุงรักษาที่เกี่ยวข้องได้</span><span class="sxs-lookup"><span data-stu-id="08a21-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="08a21-105">เมื่อคุณเลือกชนิดงานบำรุงรักษาที่มีการคาดการณ์ในการบำรุงรักษา การคาดการณ์จะถูกคัดลอกไปยังใบสั่งงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="08a21-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="08a21-106">คุณสามารถเพิ่มหรือลบรายการการคาดการณ์บนใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="08a21-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="08a21-107">การตั้งค่าสถานะวงจรชีวิตของใบสั่งงานชนิดโครงการที่เกี่ยวข้องและกฎขั้นที่เกี่ยวข้องกับชนิดโครงการจะกำหนดว่าคุณสามารถเพิ่มหรือแก้ไขรายการการคาดการณ์ได้</span><span class="sxs-lookup"><span data-stu-id="08a21-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="08a21-108">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="08a21-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="08a21-109">เลือกใบสั่งงานในรายการ และคลิก **การคาดการณ์**</span><span class="sxs-lookup"><span data-stu-id="08a21-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="08a21-110">ใน **การคาดการณ์ในการบำรุงรักษาใบสั่งงาน** รายการการคาดการณ์จากชนิดงานการบำรุงรักษาที่เลือกในงานใบสั่งงานจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="08a21-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="08a21-111">เพิ่มการคาดการณ์ชั่วโมงไปที่ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="08a21-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="08a21-112">เลือกงานใบสั่งงานที่คุณต้องการเพิ่มการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="08a21-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="08a21-113">บนแท็บด่วน **ชั่วโมง** คลิก **เพิ่ม** เพื่อสร้างรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="08a21-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="08a21-114">เลือกประเภทในฟิลด์ **ประเภท**</span><span class="sxs-lookup"><span data-stu-id="08a21-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="08a21-115">แทรกจำนวนของชั่วโมงการคาดการณ์ในฟิลด์ **ชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="08a21-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="08a21-116">ในฟิลด์ **คุณสมบัติของรายการ** ให้เลือกชนิดค่าธรรมเนียมที่จะใช้ในรายการ</span><span class="sxs-lookup"><span data-stu-id="08a21-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="08a21-117">เพิ่มการคาดการณ์สินค้าไปที่ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="08a21-117">Add items forecast to a work order</span></span>

<span data-ttu-id="08a21-118">มีสามวิธีในการเพิ่มสินค้าลงในการคาดการณ์ในการบำรุงรักษาใบสั่งงาน: คุณสามารถสร้างรายการสำหรับสินค้า (อะไหล่สำรอง) ที่ไม่ได้รวมอยู่ในรายการอะไหล่หรือ BOM สินทรัพย์ คุณสามารถเลือกอะไหล่สำรองจากรายการอะไหล่สำรองที่ได้รับอนุมัติ และคุณสามารถเลือกสินค้าจาก BOM สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="08a21-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="08a21-119">เลือกงานใบสั่งงานที่คุณต้องการเพิ่มการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="08a21-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="08a21-120">เลือกแท็บด่วน **สินค้า**</span><span class="sxs-lookup"><span data-stu-id="08a21-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="08a21-121">คลิก **เพิ่ม** เพื่อสร้างรายการใหม่สำหรับอะไหล่สำรองที่ไม่ได้อยู่ในรายการอะไหล่สำรองหรือรายการ BOM สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="08a21-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="08a21-122">เลือกสินค้าในฟิลด์ **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="08a21-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="08a21-123">แทรกปริมาณในฟิลด์ **ปริมาณการขาย** และเลือกหน่วยปริมาณในฟิลด์ **หน่วย**</span><span class="sxs-lookup"><span data-stu-id="08a21-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="08a21-124">แทรกราคาต้นทุนและสกุลเงินในฟิลด์ที่เกี่ยวข้อง และเลือก **คุณสมบัติของรายการ**</span><span class="sxs-lookup"><span data-stu-id="08a21-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="08a21-125">ถ้าคุณต้องการเปลี่ยนรายการของมิติที่แสดงบนรายการสินค้า ให้คลิก **สินค้าคงคลัง** > **แสดงมิติ** เลือกมิติ และเลือก "ใช่" บนปุ่มสลับ **บันทึกการตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="08a21-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="08a21-126">ถ้าคุณต้องการเพิ่มอะไหล่สำรองที่ได้รับการอนุมัติให้กับการคาดการณ์ในการบำรุงรักษา คลิก **เพิ่มอะไหล่สำรอง** เลือกอะไหล่สำรอง แก้ไขข้อมูลที่เกี่ยวข้องถ้าจำเป็น และคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="08a21-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="08a21-127">ถ้าคุณต้องการเพิ่มสินค้า BOM สินทรัพย์ลงในการคาดการณ์ ให้คลิก **เพิ่มสินค้า BOM** เลือกสินค้า แก้ไขข้อมูลที่เกี่ยวข้องกับการถ้าจำเป็น และคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="08a21-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="08a21-128">คลิก **สินค้าที่ใช้** ถ้าต้องการดูภาพรวมของตำแหน่งที่สินค้าในรายการที่เลือกถูกใช้ในการจัดการสินทรัพย์โดยสัมพันธ์กับสินทรัพย์ ค่าเริ่มต้นของชนิดงานการบำรุงรักษา อะไหล่สำรอง และใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="08a21-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="08a21-129">เพิ่มการคาดการณ์ค่าใช้จ่ายไปที่ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="08a21-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="08a21-130">หัวข้อนี้อธิบายวิธีการเพิ่มการคาดการณ์ค่าใช้จ่ายไปที่ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="08a21-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="08a21-131">ในด้านซ้ายมือของฟอร์ม ให้เลือกงานใบสั่งงานที่คุณต้องการเพิ่มการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="08a21-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="08a21-132">เลือกแท็บด่วน **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="08a21-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="08a21-133">คลิก **เพิ่ม** เพื่อสร้างรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="08a21-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="08a21-134">เลือกประเภทในฟิลด์ **ประเภท**</span><span class="sxs-lookup"><span data-stu-id="08a21-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="08a21-135">แทรกปริมาณในฟิลด์ **ปริมาณ**</span><span class="sxs-lookup"><span data-stu-id="08a21-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="08a21-136">แทรกราคาต้นทุน สกุลเงินการขาย และราคาขายในฟิลด์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="08a21-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="08a21-137">ในฟิลด์ **คุณสมบัติของรายการ** ให้เลือกชนิดค่าธรรมเนียมที่จะใช้ในรายการ</span><span class="sxs-lookup"><span data-stu-id="08a21-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="08a21-138">บนแท็บด่วน **ผลรวมการคาดการณ์ในการบำรุงรักษา** คุณสามารถดูภาพรวมของจำนวนรายการที่สร้างขึ้นบนแต่ละแท็บ สำหรับงานใบสั่งงานที่เลือกและสำหรับใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="08a21-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="08a21-139">นอกจากนี้ คุณยังสามารถดูผลรวมของชั่วโมงการทำงานที่คาดการณ์ไว้สำหรับงานใบสั่งงานและสำหรับใบสั่งงานได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="08a21-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![รูปที่ 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="08a21-141">การอัพเดตอัตโนมัติของการคาดการณ์ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="08a21-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="08a21-142">ในการจัดการสินทรัพย์ คุณสามารถอัพเดตการเปลี่ยนแปลงใดๆได้โดยอัตโนมัติในการคาดการณ์ใบสั่งงานที่เกี่ยวข้องกับต้นทุนชั่วโมง ต้นทุนสินค้า และค่าใช้จ่าย ที่มีการอัพเดตในโมดูลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="08a21-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules.</span></span> <span data-ttu-id="08a21-143">การทำเช่นนี้ทำเพื่อให้แน่ใจว่ามีการใช้ราคาต้นทุนล่าสุดอยู่เสมอในการคาดการณ์ใบสั่งงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="08a21-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="08a21-144">นอกจากนี้คุณยังสามารถทำการอัพเดตที่คล้ายกันสำหรับ [การคาดการณ์ชนิดงานบำรุงรักษา](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)</span><span class="sxs-lookup"><span data-stu-id="08a21-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="08a21-145">คลิก **การจัดการสินทรัพย์** > **ประจำงวด** > **การคาดการณ์** > **อัพเดตการคาดการณ์ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="08a21-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="08a21-146">ในกล่องโต้ตอบรายการแบบหล่นลง **การอัพเดตการคาดการณ์ใบสั่งงาน** คุณสามารถเพิ่มการเลือกที่เกี่ยวข้องกับใบสั่งงานหรืองานใบสั่งงานเฉพาะได้ ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="08a21-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="08a21-147">คลิก **ตัวกรอง** เพื่อทำการเลือกดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="08a21-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="08a21-148">ถ้าจำเป็น คุณสามารถตั้งค่าการอัพเดตโดยอัตโนมัติเป็นชุดงานได้บนแท็บด่วน **รันในแบบเบื้องหลัง**</span><span class="sxs-lookup"><span data-stu-id="08a21-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="08a21-149">คลิก **ตกลง** เพื่อเริ่มต้นการอัพเดตการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="08a21-149">Click **OK** to start the forecast update.</span></span>


![รูปที่ 2](media/07-work-orders.png)

