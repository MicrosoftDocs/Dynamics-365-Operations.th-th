---
title: รายละเอียดรายการงาน
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับหน้ารายละเอียดของรายการงาน ซึ่งแสดงรายการที่ครอบคลุม สามารถเรียงลำดับได้ และสามารถกรองได้ ของรายการงานแต่ละรายการในระบบของคุณ
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bcb340b21e06b294a40784bf3a1da71b0daf7655
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015906"
---
# <a name="work-line-details"></a><span data-ttu-id="bbcee-103">รายละเอียดรายการงาน</span><span class="sxs-lookup"><span data-stu-id="bbcee-103">Work line details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbcee-104">หน้า **รายละเอียดของรายการงาน** แสดงรายการที่ครอบคลุม สามารถเรียงลำดับได้ และสามารถกรองได้ ของรายการงานแต่ละรายการในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="bbcee-104">The **Work line details** page shows a comprehensive, sortable, and filterable list of the individual work lines in your system.</span></span> <span data-ttu-id="bbcee-105">ซึ่งแสดงภาพรวมที่สมบูรณ์ของงานที่กำลังวางแผนและดำเนินการในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="bbcee-105">It provides a complete overview of work that is being planned and executed in the warehouse.</span></span> <span data-ttu-id="bbcee-106">คุณสามารถสลับระหว่างการดูรายการงานทั้งหมดและการดูรายการงานที่เปิดอยู่ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="bbcee-106">You can easily switch between viewing all work lines and viewing only open work lines.</span></span> <span data-ttu-id="bbcee-107">รายละเอียดที่ระบุสำหรับแต่ละรายการประกอบด้วย สถานะของงาน หมายเลขสินค้า สถานที่ ปริมาณงาน รหัสโหลด และรหัสการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="bbcee-107">Details that are provided for each line include the work status, item number, location, work quantity, load ID, and shipment ID.</span></span>

## <a name="turn-on-the-work-line-details-feature"></a><span data-ttu-id="bbcee-108">เปิดคุณลักษณะรายละเอียดของรายการงาน</span><span class="sxs-lookup"><span data-stu-id="bbcee-108">Turn on the work line details feature</span></span>

<span data-ttu-id="bbcee-109">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="bbcee-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="bbcee-110">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="bbcee-110">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="bbcee-111">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bbcee-111">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="bbcee-112">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="bbcee-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="bbcee-113">**ชื่อคุณลักษณะ:** *รายละเอียดของรายการงาน*</span><span class="sxs-lookup"><span data-stu-id="bbcee-113">**Feature name:** *Work line details*</span></span>

## <a name="open-and-use-the-work-line-details-page"></a><span data-ttu-id="bbcee-114">เปิดและใช้หน้ารายละเอียดของรายการงาน</span><span class="sxs-lookup"><span data-stu-id="bbcee-114">Open and use the Work line details page</span></span>

<span data-ttu-id="bbcee-115">เมื่อต้องการดูรายการของรายละเอียดของรายการงาน ให้ไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดของรายการงาน**</span><span class="sxs-lookup"><span data-stu-id="bbcee-115">To view the list of work line details, go to **Warehouse management \> Work \> Work line details**.</span></span> <span data-ttu-id="bbcee-116">จากที่นี่ คุณสามารถทำการดำเนินการต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="bbcee-116">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="bbcee-117">ใช้ฟิลด์ **ตัวกรอง** เพื่อค้นหารายการที่มีค่าเฉพาะสำหรับพารามิเตอร์ใดๆ ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bbcee-117">Use the **Filter** field to search for lines that have a specific value for any available parameter.</span></span> <span data-ttu-id="bbcee-118">(พารามิเตอร์ที่พร้อมใช้งานจะรวมพารามิเตอร์มากมายที่ไม่ได้แสดงเป็นคอลัมน์ในกริด)</span><span class="sxs-lookup"><span data-stu-id="bbcee-118">(Available parameters include many parameters that aren't shown as columns in the grid.)</span></span>
- <span data-ttu-id="bbcee-119">ใช้กล่องกาเครื่องหมาย **แสดงที่ปิด** เพื่อแสดงหรือซ่อนรายการที่ปิด</span><span class="sxs-lookup"><span data-stu-id="bbcee-119">Use the **Show closed** check box to show or hide closed lines.</span></span>
- <span data-ttu-id="bbcee-120">เลือก **มิติการแสดงผล** เพื่อเปิดกล่องโต้ตอบ **การแสดงมิติ** ที่คุณสามารถเลือกที่จะแสดงหรือซ่อนคอลัมน์มิติต่างๆ ในกริด</span><span class="sxs-lookup"><span data-stu-id="bbcee-120">Select **Display dimensions** to open the **Dimensions display** dialog box, where you can choose to show or hide various dimension columns in the grid.</span></span>
- <span data-ttu-id="bbcee-121">เลือกส่วนหัวของคอลัมน์ใดๆ เพื่อเปิดเมนูซึ่งคุณสามารถเลือกที่จะเรียงลำดับหรือกรองรายการตามค่าในคอลัมน์ดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="bbcee-121">Select any column heading to open a menu where you can choose to sort or filter the list by values in that column.</span></span>
- <span data-ttu-id="bbcee-122">เลือกรายการงาน แล้วจากนั้น เลือก **เปลี่ยนสถานที่** เพื่อเปิดกล่องโต้ตอบซึ่งคุณสามารถเปลี่ยนสถานที่สำหรับรายการงานนั้นได้</span><span class="sxs-lookup"><span data-stu-id="bbcee-122">Select a work line, and then select **Change location** to open a dialog box where you can change the location for that work line.</span></span> <span data-ttu-id="bbcee-123">สถานที่ที่คุณระบุจะแทนที่การตั้งค่าของคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="bbcee-123">The location that you specify will override the setup of the location directive.</span></span>
- <span data-ttu-id="bbcee-124">เลือกรายการงาน แล้วจากนั้น เลือก **ยกเลิกรายการงาน** เพื่อเปิดกล่องโต้ตอบที่ซึ่งคุณสามารถลดปริมาณของรายการงานนั้นได้เพียงบางส่วนหรือทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="bbcee-124">Select a work line, and then select **Cancel work line** to open a dialog box where you can partially or fully reduce the quantity of that work line.</span></span>
- <span data-ttu-id="bbcee-125">ปรับปรุงปริมาณ</span><span class="sxs-lookup"><span data-stu-id="bbcee-125">Adjust quantities.</span></span>
- <span data-ttu-id="bbcee-126">ดูธุรกรรมที่อยู่เบื้องหลังรายการงานใดๆ</span><span class="sxs-lookup"><span data-stu-id="bbcee-126">View the transactions behind any work line.</span></span>

## <a name="try-out-the-feature"></a><span data-ttu-id="bbcee-127">ลองใช้คุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="bbcee-127">Try out the feature</span></span>

<span data-ttu-id="bbcee-128">ในส่วนนี้จะให้การสาธิตสามส่วนซึ่งแสดงวิธีการทำงานกับรายละเอียดรายการงาน</span><span class="sxs-lookup"><span data-stu-id="bbcee-128">This section provides a three-part demo that shows how to work with work line details.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="bbcee-129">ทำให้ข้อมูลตัวอย่างพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bbcee-129">Make sample data available</span></span>

<span data-ttu-id="bbcee-130">เมื่อต้องการดำเนินการสาธิตนี้โดยใช้เรกคอร์ดและค่าตัวอย่างที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="bbcee-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="bbcee-131">นอกจากนี้ คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bbcee-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="bbcee-132">นอกจากนี้ คุณยังสามารถใช้การสาธิตนี้เป็นคำแนะนำ เมื่อคุณทำงานในระบบการผลิต</span><span class="sxs-lookup"><span data-stu-id="bbcee-132">You can also use this demo as guidance when you work on a production system.</span></span> <span data-ttu-id="bbcee-133">อย่างไรก็ตาม คุณต้องแทนที่ค่าของคุณเอง และคุณอาจขาดเรกคอร์ดที่จำเป็นบางชนิดที่ข้อมูลสาธิตมาตรฐานมีให้</span><span class="sxs-lookup"><span data-stu-id="bbcee-133">However, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="bbcee-134">ตรวจสอบว่าการตั้งค่าสถานการณ์จำลองมีสินค้าคงคลังที่พร้อมใช้งานเพียงพอ</span><span class="sxs-lookup"><span data-stu-id="bbcee-134">Verify that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="bbcee-135">ถ้าคุณกำลังทำงานกับข้อมูลการสาธิต **USMF** ก่อนอื่นคุณควรตรวจสอบให้แน่ใจว่า ระบบของคุณได้รับการตั้งค่าไว้เพื่อให้สินค้าคงคลังพร้อมใช้งานเพียงพอที่สถานที่เบิกสินค้าที่เกี่ยวข้องแต่ละแห่ง</span><span class="sxs-lookup"><span data-stu-id="bbcee-135">If you're working with the **USMF** demo data, you should first make sure that your system is set up so that enough inventory is available at each relevant pick location.</span></span> <span data-ttu-id="bbcee-136">สำหรับการสาธิตนี้ ความคาดหวังคือว่า คุณมีสินค้าคงคลังต่อไปนี้ที่พร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="bbcee-136">For this demo, the expectation is that you have the following inventory available:</span></span>

- <span data-ttu-id="bbcee-137">**สินค้า M9200:** 45 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="bbcee-137">**Item M9200:** 45 ea.</span></span> <span data-ttu-id="bbcee-138">(หรือมากกว่านั้น)</span><span class="sxs-lookup"><span data-stu-id="bbcee-138">(or more)</span></span>
- <span data-ttu-id="bbcee-139">**สินค้า M9202:** 10 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="bbcee-139">**Item M9202:** 10 ea.</span></span> <span data-ttu-id="bbcee-140">(หรือมากกว่านั้น)</span><span class="sxs-lookup"><span data-stu-id="bbcee-140">(or more)</span></span>

<span data-ttu-id="bbcee-141">ทำตามขั้นตอนต่อไปนี้เพื่อตรวจสอบว่ามีสินค้าคงคลังที่เพียงพอพร้อมใช้งาน และเพื่อทำการปรับปรุงใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="bbcee-141">Follow these steps to verify that enough inventory is available and to make any adjustments that are required.</span></span>

1. <span data-ttu-id="bbcee-142">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่** และกำหนดสถานที่เบิกสินค้าที่จะใช้สำหรับการเบิกสินค้าตามใบสั่งขายที่คลังสินค้า 51</span><span class="sxs-lookup"><span data-stu-id="bbcee-142">Go to **Warehouse management \> Setup \> Location directives** , and determine which picking locations are used for sales order picking at warehouse 51.</span></span> <span data-ttu-id="bbcee-143">(สำหรับข้อมูลเพิ่มเติม ดู [ควบคุมงานคลังสินค้าโดยใช้เท็มเพลตงานและคำสั่งสถานที่](control-warehouse-location-directives.md))</span><span class="sxs-lookup"><span data-stu-id="bbcee-143">(For more information, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md).)</span></span>
1. <span data-ttu-id="bbcee-144">ตรวจสอบระดับสินค้าคงคลังที่สถานที่ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="bbcee-144">Check the inventory levels at the relevant locations.</span></span>
1. <span data-ttu-id="bbcee-145">ปรับปรุงสินค้าคงคลังตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="bbcee-145">Adjust inventory as required.</span></span> <span data-ttu-id="bbcee-146">คุณสามารถสร้างการเคลื่อนไหวด้วยตนเอง ใช้การเติมสินค้า หรือใช้โฟลว์อื่นใดๆ เพื่อปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="bbcee-146">You can create manual movements, use replenishment, or apply any other flow to adjust the inventory.</span></span>

### <a name="part-1-create-picking-work"></a><span data-ttu-id="bbcee-147">ส่วนที่ 1: สร้างงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="bbcee-147">Part 1: Create picking work</span></span>

<span data-ttu-id="bbcee-148">ก่อนที่คุณจะเริ่มสร้างงาน โปรดตรวจสอบให้แน่ใจว่าคลังสินค้าของคุณได้รับการตั้งค่าให้ตอบสนองต่อคำของานในลักษณะที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="bbcee-148">Before you start to create work, make sure that your warehouse is set up to respond to work requests in the expected manner.</span></span>

<span data-ttu-id="bbcee-149">ทำตามขั้นตอนเหล่านี้เพื่อสร้างงานการเบิกสินค้าบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="bbcee-149">Follow these steps to create some picking work.</span></span>

1. <span data-ttu-id="bbcee-150">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="bbcee-150">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="bbcee-151">เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบ **สร้างใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="bbcee-151">Select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="bbcee-152">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bbcee-152">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="bbcee-153">บน FastTab **ลูกค้า** ให้ตั้งค่าฟิลด์ **บัญชีลูกค้า** เป็น _US-001_</span><span class="sxs-lookup"><span data-stu-id="bbcee-153">On the **Customer** FastTab, set the **Customer account** field to _US-001_.</span></span>
    - <span data-ttu-id="bbcee-154">บน FastTab **ทั่วไป** ให้ตั้งค่าฟิลด์ **คลังสินค้า** เป็น _51_</span><span class="sxs-lookup"><span data-stu-id="bbcee-154">On the **General** FastTab, set the **Warehouse** field to _51_.</span></span>

1. <span data-ttu-id="bbcee-155">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="bbcee-155">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="bbcee-156">มีการเปิดใบสั่งขายใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="bbcee-156">Your new sales order is opened.</span></span> <span data-ttu-id="bbcee-157">ซึ่งมีแถวใหม่ที่ว่างเปล่าในกริด **รายการใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="bbcee-157">It includes a new, empty row in the **Sales order lines** grid.</span></span> <span data-ttu-id="bbcee-158">ในรายการใบสั่งนี้ ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bbcee-158">On this order line, set the following values:</span></span>

    - <span data-ttu-id="bbcee-159">**หมายเลขสินค้า:** _M9200_</span><span class="sxs-lookup"><span data-stu-id="bbcee-159">**Item number:** _M9200_</span></span>
    - <span data-ttu-id="bbcee-160">**ปริมาณ:** _20_</span><span class="sxs-lookup"><span data-stu-id="bbcee-160">**Quantity:** _20_</span></span>
    - <span data-ttu-id="bbcee-161">**หน่วย:** _ea_</span><span class="sxs-lookup"><span data-stu-id="bbcee-161">**Unit:** _ea_</span></span>

1. <span data-ttu-id="bbcee-162">เลือกรายการใบสั่งใหม่ และจากนั้น บนเมนู **สินค้าคงคลัง** เลือก **การจอง** เพื่อเปิดหน้า **การจอง**</span><span class="sxs-lookup"><span data-stu-id="bbcee-162">Select the new order line, and then, on the **Inventory** menu, select **Reservation** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="bbcee-163">บนหน้า **การจอง** ให้เลือก **สำรองล็อต** เพื่อจองปริมาณทั้งหมดของรายการที่เลือกในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="bbcee-163">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="bbcee-164">ปิดหน้า **การจอง** เพื่อส่งคืนไปยังใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="bbcee-164">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="bbcee-165">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="bbcee-165">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span> <span data-ttu-id="bbcee-166">ระบบจะสร้างการจัดส่ง จะเพิ่มไปยังจำนวนงานในศูนย์การผลิตใหม่ และสร้างงานที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="bbcee-166">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="bbcee-167">สร้างใบสั่งขายที่สองสำหรับบัญชีลูกค้าและคลังสินค้าเดียวกันกับที่คุณใช้สำหรับใบสั่งแรก</span><span class="sxs-lookup"><span data-stu-id="bbcee-167">Create a second sales order for the same customer account and warehouse that you used for the first order.</span></span> <span data-ttu-id="bbcee-168">เพิ่มรายการใบสั่งสองรายการต่อไปนี้ลงในใบสั่งนี้:</span><span class="sxs-lookup"><span data-stu-id="bbcee-168">Add the following two order lines to this order:</span></span>

    - <span data-ttu-id="bbcee-169">**รายการที่ 1:** ตั้งค่าฟิลด์ **หมายเลขสินค้า** เป็น _M9200_ ฟิลด์ **จำนวน** เป็น _25_ และฟิลด์ **หน่วย** เป็น _ชิ้น_</span><span class="sxs-lookup"><span data-stu-id="bbcee-169">**Line 1:** Set the **Item number** field to _M9200_ , the **Quantity** field to _25_ , and the **Unit** field to _ea_.</span></span>
    - <span data-ttu-id="bbcee-170">**รายการที่ 2:** ตั้งค่าฟิลด์ **หมายเลขสินค้า** เป็น _M9202_ ฟิลด์ **จำนวน** เป็น _10_ และฟิลด์ **หน่วย** เป็น _ชิ้น_</span><span class="sxs-lookup"><span data-stu-id="bbcee-170">**Line 2:** Set the **Item number** field to _M9202_ , the **Quantity** field to _10_ , and the **Unit** field to _ea_.</span></span>

1. <span data-ttu-id="bbcee-171">ทำซ้ำขั้นตอนที่ 6 ถึง 8 เพื่อจองสินค้าคงคลังสำหรับรายการใบสั่งแต่ละรายการ (หนึ่งรายการต่อครั้ง) แล้วจากนั้น ทำซ้ำขั้นตอนที่ 9 เพื่อนำใบสั่งออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="bbcee-171">Repeat steps 6 through 8 to reserve the inventory for each order line (one at a time), and then repeat step 9 to release the order to the warehouse.</span></span>

### <a name="part-2-change-the-location-for-a-work-line"></a><span data-ttu-id="bbcee-172">ส่วนที่ 2: เปลี่ยนสถานที่สำหรับรายการงาน</span><span class="sxs-lookup"><span data-stu-id="bbcee-172">Part 2: Change the location for a work line</span></span>

1. <span data-ttu-id="bbcee-173">ไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดของรายการงาน**</span><span class="sxs-lookup"><span data-stu-id="bbcee-173">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="bbcee-174">ค้นหาและเลือกหนึ่งในรายการงานที่คุณสร้างขึ้นสำหรับการสาธิตนี้</span><span class="sxs-lookup"><span data-stu-id="bbcee-174">Find and select one of the work lines that you created for this demo.</span></span>
1. <span data-ttu-id="bbcee-175">เลือก **เปลี่ยนสถานที่** เพื่อเปิดกล่องโต้ตอบ **เลือกสถานที่ใหม่**</span><span class="sxs-lookup"><span data-stu-id="bbcee-175">Select **Change location** to open the **Select new location** dialog box.</span></span>
1. <span data-ttu-id="bbcee-176">ในกล่องโต้ตอบ **เลือกสถานที่ใหม่** ในฟิลด์ **สถานที่** ให้เลือกสถานที่ใหม่สำหรับรายการงาน</span><span class="sxs-lookup"><span data-stu-id="bbcee-176">In the **Select new location** dialog box, in the **Location** field, select a new location for the work line.</span></span>
1. <span data-ttu-id="bbcee-177">เลือก **ตกลง** เพื่อใช้การเปลี่ยนแปลงของคุณ และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="bbcee-177">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bbcee-178">คุณสามารถส่งการเปลี่ยนแปลงสถานที่ได้เฉพาะเมื่อสถานที่ใหม่มีสินค้าคงคลังที่พร้อมใช้งานที่เพียงพอ (สำหรับการเบิกสินค้า) หรือเมื่อผ่านการตรวจสอบความถูกต้องของชนิดสถานที่ (สำหรับการส่งสินค้า)</span><span class="sxs-lookup"><span data-stu-id="bbcee-178">You can submit location changes only if the new location has enough inventory available (for a pick), or if it passes location-type validation (for a put).</span></span>

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a><span data-ttu-id="bbcee-179">ส่วนที่ 3: เปลี่ยนปริมาณของรายการงาน หรือยกเลิกรายการงาน</span><span class="sxs-lookup"><span data-stu-id="bbcee-179">Part 3: Change the quantity of a work line or cancel a work line</span></span>

1. <span data-ttu-id="bbcee-180">ไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดของรายการงาน**</span><span class="sxs-lookup"><span data-stu-id="bbcee-180">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="bbcee-181">ค้นหาและเลือกหนึ่งในรายการงานที่คุณสร้างขึ้นสำหรับการสาธิตนี้</span><span class="sxs-lookup"><span data-stu-id="bbcee-181">Find and select one of the work lines that you created for this demo.</span></span> <span data-ttu-id="bbcee-182">โปรดทราบว่าคุณสามารถยกเลิกหรือเปลี่ยนปริมาณได้เฉพาะสำหรับรายการงานที่มีชนิดงานเป็น _เบิกสินค้า_ เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="bbcee-182">Note that you can cancel or change quantities only for work lines where the work type is _pick_.</span></span>
1. <span data-ttu-id="bbcee-183">เลือก **ยกเลิกรายการงาน** เพื่อเปิดกล่องโต้ตอบ **ปริมาณที่จะยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="bbcee-183">Select **Cancel work line** to open the **Quantity to cancel** dialog box.</span></span>
1. <span data-ttu-id="bbcee-184">ในกล่องโต้ตอบ **ปริมาณที่จะยกเลิก** ให้เปลี่ยนค่าในฟิลด์ **ปริมาณ** เพื่อระบุปริมาณที่ควรถูก *ลบออกจาก* ปริมาณที่ระบุไว้สำหรับรายการนี้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="bbcee-184">In the **Quantity to cancel** dialog box, change the value in the **Quantity** field to specify the quantity that should be *subtracted from* the quantity that is currently specified for the line.</span></span> <span data-ttu-id="bbcee-185">โดยค่าเริ่มต้น ฟิลด์ **ปริมาณ** จะแสดงปริมาณทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="bbcee-185">By default, the **Quantity** field shows the full quantity.</span></span>

    - <span data-ttu-id="bbcee-186">ถ้าคุณยกเลิกปริมาณทั้งหมด จะมีการเปลี่ยนค่า **สถานะของงาน** เป็น _ยกเลิก_ แต่ฟิลด์ **ปริมาณงาน** จะยังคงแสดงค่าดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="bbcee-186">If you cancel the full quantity, the **Work status** value will be changed to _Canceled_ , but the **Work quantity** field will still show the original value.</span></span>
    - <span data-ttu-id="bbcee-187">ถ้าคุณยกเลิกเพียงส่วนหนึ่งของปริมาณทั้งหมด ฟิลด์ **ปริมาณงาน** จะถูกปรับปรุงเพื่อแสดงค่าใหม่ แต่ค่า **สถานะของงาน** จะไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="bbcee-187">If you cancel just part of the quantity, the **Work quantity** field will be updated to show the new value, but the **Work status** value won't change.</span></span>

1. <span data-ttu-id="bbcee-188">เลือก **ตกลง** เพื่อใช้การเปลี่ยนแปลงของคุณ และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="bbcee-188">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bbcee-189">ถ้าคุณยกเลิกเพียงบางส่วนของปริมาณสำหรับรายการงาน คุณต้องลบปริมาณที่ล้าสมัยออกจากรายการจำนวนงานในศูนย์การผลิตด้วย</span><span class="sxs-lookup"><span data-stu-id="bbcee-189">If you cancel just part of the quantity for a work line, you must also remove the obsolete quantity from the load line.</span></span> <span data-ttu-id="bbcee-190">มิฉะนั้น เว้นแต่จะมีการตั้งค่าขีดจำกัดการรับสินค้าต่ำกว่าปริมาณการสั่งอย่างถูกต้อง รายการจำนวนงานในศูนย์การผลิตจะไม่สามารถได้รับการยืนยันการจัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="bbcee-190">Otherwise, unless under-delivery is set up correctly, the load line can't be ship-confirmed.</span></span>
