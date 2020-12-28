---
title: การจัดกำหนดการใช้จำนวนงานในศูนย์การผลิต
description: หัวข้อนี้อธิบายวิธีการตั้งค่า และจัดกำหนดการโหลดสำหรับคลังสินค้า
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87455077c69834c9ace6409f4cc611ae6e14beb4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438274"
---
# <a name="schedule-load-utilization"></a><span data-ttu-id="f50b4-103">การจัดกำหนดการใช้จำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="f50b4-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f50b4-104">คุณสามารถจัดกำหนดการใช้จำนวนงานสำหรับชนิดสถานที่ที่เลือกได้ และคุณยังสามารถคาดการณ์การใช้จำนวนงานในปัจจุบันและอนาคตได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="f50b4-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="f50b4-105">คุณสามารถคาดการณ์การใช้จำนวนงานสำหรับอย่างน้อยหนึ่งไซต์ได้ สำหรับหน่วยจำนวนงาน (โซนหรือคลังสินค้า) หรือสำหรับชุดรวมของโซนและคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f50b4-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="f50b4-106">จัดกำหนดการ และดูจำนวนงานในศูนย์การผลิตสำหรับคลังสินค้าหรือไซต์</span><span class="sxs-lookup"><span data-stu-id="f50b4-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="f50b4-107">การจัดตารางจำนวนงานในศูนย์การผลิตสำหรับไซต์ คลังสินค้า หรือโซน คุณสามารถสร้างการตั้งค่าการใช้ประโยชน์พื้นที่ และเชื่อมโยงกับแผนหลักได้</span><span class="sxs-lookup"><span data-stu-id="f50b4-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="f50b4-108">ในการตั้งค่าการใช้พื้นที่ว่าง คุณใช้ชนิดของที่ตั้ง เช่น **สถานที่เก็บสินค้าจำนวนมาก** และ **สถานที่เบิกสินค้า** เพื่อระบุวิธีคาดการณ์การใช้พื้นที่</span><span class="sxs-lookup"><span data-stu-id="f50b4-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="f50b4-109">คุณยังสามารถระบุโหมดการวางสินค้าสำหรับการจัดเก็บได้ด้วย เช่น **โซน**</span><span class="sxs-lookup"><span data-stu-id="f50b4-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="f50b4-110">การนำเสนอการใช้ประโยชน์พื้นที่ในอนาคตจะขึ้นอยู่กับข้อมูลที่ได้รับการคำนวณแผนหลักที่เชื่อมโยง </span><span class="sxs-lookup"><span data-stu-id="f50b4-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="f50b4-111">แผนหลักจะการคาดการณ์การวางแผนทรัพยากรสำหรับใบสั่งขาเข้าและขาออกสำหรับการผลิตและการดำเนินงาน </span><span class="sxs-lookup"><span data-stu-id="f50b4-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="f50b4-112">การนำเสนอพื้นที่ที่พร้อมใช้งานจะขึ้นอยู่กับความสัมพันธ์ระหว่างการตั้งค่าการใช้ประโยชน์พื้นที่และแผนหลักที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f50b4-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="f50b4-113">ด้วยการใช้โหมดการวางสินค้าสำหรับการจัดเก็บที่คุณเลือกในการตั้งค่าการใช้ประโยชน์พื้นที่ คุณสามารถระบุได้ว่า ควรจะคาดการณ์จำนวนงานในศูนย์การผลิตสำหรับแต่ละคลังสินค้าหรือโซน หรือการคาดการณ์ควรมีข้อมูลเกี่ยวกับทั้งคลังสินค้าและโซน</span><span class="sxs-lookup"><span data-stu-id="f50b4-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="f50b4-114">คุณยังระบุอีกว่า ตำแหน่งที่ตั้งที่ถูกบล็อคควรถูกแยกออกจากการคำนวณการใช้จำนวนงานในศูนย์การผลิตหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f50b4-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="f50b4-115">คุณสามารถคาดการณ์การใช้ประโยชน์พื้นที่โดยการสร้างรายงาน **การใช้พื้นที่วางสินค้าในคลังสินค้า** ได้</span><span class="sxs-lookup"><span data-stu-id="f50b4-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="f50b4-116">เมื่อคุณสร้างรายงานนี้ คุณสามารถระบุได้ว่า ควรจะคาดการณ์การใช้จำนวนงานในศูนย์การผลิตสำหรับแต่ละไซต์ ระหว่างไซต์ หรือสำหรับหน่วยจำนวนงานในศูนย์การผลิตที่เลือก เช่น โซน หรือคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f50b4-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="f50b4-117">สร้างการตั้งค่าการใช้พื้นที่สำหรับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f50b4-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="f50b4-118">เลือก **การบริหารสินค้าคงคลัง** \> **ตั้งค่า** \> **การตรวจสอบคลังสินค้า** \> **การใช้พื้นที่**</span><span class="sxs-lookup"><span data-stu-id="f50b4-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="f50b4-119">เลือก **สร้าง** เพื่อสร้างการตั้งค่าการใช้พื้นที่</span><span class="sxs-lookup"><span data-stu-id="f50b4-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="f50b4-120">ระบุรหัสและชื่อสำหรับการตั้งค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="f50b4-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="f50b4-121">ในฟิลด์ **โหมดการวางสินค้าสำหรับการจัดเก็บ** ให้เลือกว่าภาพรวมของการใช้พื้นที่ควรแสดงข้อมูลตามคลังสินค้า โซน หรือคลังสินค้าและโซน</span><span class="sxs-lookup"><span data-stu-id="f50b4-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="f50b4-122">ตั้งค่าตัวเลือก **ไม่รวมสถานที่เก็บที่ถูกบล็อค** เป็น **ใช่** เพื่อแยกสถานที่เก็บสินค้าคงคลังที่ถูกบล็อคจากการคำนวณพื้นที่ว่างที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f50b4-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="f50b4-123">คุณสามารถบล็อคสถานที่เก็บสินค้าคงคลังสำหรับอินพุทและเอาท์พุทได้ โดยการระบุสาเหตุการบล็อคสำหรับสถานที่ในฟิลด์ **อินพุทถูกบล็อค** หรือ **เอาท์พุทถูกบล็อค** บน FastTab **อื่นๆ** ในหน้า **สถานที่เก็บสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="f50b4-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="f50b4-124">บน FastTab **ชนิดของที่ตั้ง** ให้เลือกชนิดที่ตั้งเพื่อรวมในการคำนวณการใช้พื้นที่</span><span class="sxs-lookup"><span data-stu-id="f50b4-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="f50b4-125">คุณต้องเลือกอย่างน้อยหนึ่งชนิดที่ตั้งสำหรับการเสนอ</span><span class="sxs-lookup"><span data-stu-id="f50b4-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="f50b4-126">เชื่อมโยงการตั้งค่าการใช้พื้นที่กับแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="f50b4-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="f50b4-127">เลือก **Iการบริหารสินค้าคงคลังt** \> **งานประจำงวด** \> **จัดกำหนดการใช้จำนวนงานในศูนย์การผลิต**</span><span class="sxs-lookup"><span data-stu-id="f50b4-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="f50b4-128">ในฟิลด์ **แผนหลัก** ให้เลือกแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="f50b4-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="f50b4-129">ในฟิลด์ **จำนวนวัน** ให้ระบุจำนวนวันที่จะรวมไว้ในการคาดการณ์ของปริมาณงานปัจจุบันและในอนาคต</span><span class="sxs-lookup"><span data-stu-id="f50b4-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="f50b4-130">ในฟิลด์ **การใช้พื้นที่** ให้เลือกการตั้งค่าการใช้พื้นที่เพื่อใช้ในการคาดการณ์ของปริมาณงานปัจจุบันและในอนาคต</span><span class="sxs-lookup"><span data-stu-id="f50b4-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="f50b4-131">ระบุการเสนอการใช้จำนวนงานในศูนย์การผลิตแล้วดูข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f50b4-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="f50b4-132">เลือก **การบริหารสินค้าคงคลัง** \> **การสอบถามและรายงาน** \> **รายงานสินค้าคงคลังทางกายภาพ** \> **การใช้พื้นที่วางสินค้าในคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f50b4-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="f50b4-133">ในฟิลด์ **แสดงตาม** ให้เลือกระดับของการคาดการณ์การใช้พื้นที่:</span><span class="sxs-lookup"><span data-stu-id="f50b4-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="f50b4-134">**ไซต์** – คาดการณ์การใช้พื้นที่สำหรับแต่ละไซต์</span><span class="sxs-lookup"><span data-stu-id="f50b4-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="f50b4-135">การเสนอนี้เป็นประโยชน์มาก ตัวอย่างเช่น ถ้าคุณต้องการดูคลังสินค้าทั้งหมดสำหรับไซต์เพื่อให้คุณสามารถปรับสมดุลการใช้พื้นที่ระหว่างคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f50b4-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="f50b4-136">**หน่วยการวางสินค้า** – คาดการณ์การใช้พื้นที่สำหรับโซนหรือคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f50b4-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="f50b4-137">จากนั้นพื้นที่ว่างที่พร้อมใช้งานจะถูกคาดการณ์ตามค่าที่คุณเลือกไว้ในฟิลด์ **โหมดการวางสินค้าสำหรับการจัดเก็บ** ในหน้า **การใช้พื้นที่** เมื่อคุณได้สร้างการตั้งค่าการใช้พื้นที่</span><span class="sxs-lookup"><span data-stu-id="f50b4-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="f50b4-138">ทำตามขั้นตอนเหล่านี้ โดยขึ้นอยู่กับค่าที่คุณเลือกไว้ในขั้นตอนก่อนหน้า:</span><span class="sxs-lookup"><span data-stu-id="f50b4-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="f50b4-139">หากคุณเลือก **ไซต์** ในฟิลด์ **แสดงตาม** ฟิลด์ **ไซต์** จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f50b4-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="f50b4-140">เลือกอย่างน้อยหนึ่งไซต์ที่จะรวมไว้ในการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="f50b4-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="f50b4-141">หากคุณเลือก **หน่วยการวางสินค้า** ในฟิลด์ **แสดงตาม** ฟิลด์ **หน่วยการวางสินค้า** จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f50b4-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="f50b4-142">เลือกหน่วยการวางสินค้า</span><span class="sxs-lookup"><span data-stu-id="f50b4-142">Select the load unit.</span></span>

4. <span data-ttu-id="f50b4-143">ในฟิลด์ **ชนิดการวางสินค้า** ให้เลือก **ปริมาตร** หรือ **น้ำหนัก** เพื่อระบุหน่วยปฏิบัติงานคลังสินค้าที่จะคาดการณ์พื้นที่ว่างให้</span><span class="sxs-lookup"><span data-stu-id="f50b4-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="f50b4-144">ในฟิลด์ **การตั้งค่าการใช้พื้นที่** ให้เลือกการตั้งค่าการใช้พื้นที่ที่คาดการณ์ควรยึดตาม</span><span class="sxs-lookup"><span data-stu-id="f50b4-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>
