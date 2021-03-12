---
title: สร้างการจัดวางพื้นที่คลังสินค้าใหม่
description: หัวข้อนี้อธิบายวิธีการตั้งค่าข้อมูลเกี่ยวกับสถานที่เก็บในคลังสินค้า
author: perlynne
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f07fee1787cc2719bafbe2bb6d54849edda14018
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000045"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="ccd63-103">สร้างการจัดวางพื้นที่คลังสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="ccd63-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ccd63-104">หัวข้อนี้อธิบายวิธีการตั้งค่าข้อมูลเกี่ยวกับสถานที่เก็บในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="ccd63-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="ccd63-105">ใช้ได้เฉพาะกับคลังสินค้าที่สร้างขึ้นโดยใช้ "คลังสินค้าพื้นฐาน" ในโมดูลการบริหารสินค้าคงคลัง ไม่ใช่คลังสินค้าที่สร้างขึ้นในโมดูลการบริหารคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="ccd63-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="ccd63-106">คุณสามารถใช้กระบวนงานนี้ในข้อมูลสาธิตของบริษัท USMF หรือข้อมูลของคุณเอง ขั้นตอนนี้มีไว้สำหรับผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="ccd63-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="ccd63-107">ตั้งค่าความจุสถานที่ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ccd63-107">Set the default location capacity</span></span>
1. <span data-ttu-id="ccd63-108">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการสินค้าคงคลัง > การตั้งค่า > พารามิเตอร์สินค้าคงคลังและการจัดการคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ccd63-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="ccd63-109">เลือกแท็บ **สถานที่**</span><span class="sxs-lookup"><span data-stu-id="ccd63-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="ccd63-110">ในฟิลด์ **ความกว้างพื้นฐาน** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ccd63-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="ccd63-111">ในฟิลด์ **ความลึกพื้นฐาน** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ccd63-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="ccd63-112">ในฟิลด์ **ความสูงพื้นฐาน** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ccd63-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="ccd63-113">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ccd63-113">Select **Save**.</span></span>
7. <span data-ttu-id="ccd63-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ccd63-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="ccd63-115">กำหนดรูปแบบของชื่อสถานที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="ccd63-115">Define the location name format</span></span>
1. <span data-ttu-id="ccd63-116">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการสินค้าคงคลัง > การตั้งค่า > การแบ่งสินค้าคงคลัง > คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ccd63-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="ccd63-117">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ccd63-117">Select **New**.</span></span>
3. <span data-ttu-id="ccd63-118">ในฟิลด์ **คลังสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ccd63-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="ccd63-119">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ccd63-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ccd63-120">ในฟิลด์ **ไซต์** ให้เลือกเรกคอร์ดที่ต้องการในการค้นหา</span><span class="sxs-lookup"><span data-stu-id="ccd63-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="ccd63-121">สลับการขยายของส่วน **ชื่อสถานที่**</span><span class="sxs-lookup"><span data-stu-id="ccd63-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="ccd63-122">ตัวเลือกในส่วนนี้กำหนดรูปแบบเริ่มต้นสำหรับชื่อสถานที่เก็บ </span><span class="sxs-lookup"><span data-stu-id="ccd63-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="ccd63-123">ในตัวอย่างของเรา จะรวมถึงหมายเลขที่เก็บ หมายเลขชั้นเก็บสินค้า และหมายเลขชั้นวาง</span><span class="sxs-lookup"><span data-stu-id="ccd63-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="ccd63-124">ตั้งค่าตัวเลือก **รวมที่เก็บสินค้า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ccd63-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="ccd63-125">ตั้งค่าตัวเลือก **รวมชั้นเก็บสินค้า** ให้เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ccd63-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="ccd63-126">ในฟิลด์ **รูปแบบ** สำหรับชั้นเก็บสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ccd63-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="ccd63-127">ตั้งค่าตัวเลือก **วมชั้นวางสินค้า** ให้เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ccd63-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="ccd63-128">ในฟิลด์ **รูปแบบ** สำหรับชั้นวางสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ccd63-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="ccd63-129">กำหนดที่ตั้งของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="ccd63-129">Define warehouse locations</span></span>
1. <span data-ttu-id="ccd63-130">บนบานหน้าต่างการดำเนินการ เลือก **คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ccd63-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="ccd63-131">เลือก **วิซาร์ดที่ตั้ง**</span><span class="sxs-lookup"><span data-stu-id="ccd63-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="ccd63-132">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="ccd63-132">Select **Next**.</span></span>
4. <span data-ttu-id="ccd63-133">ยกเลิกการเลือกตัวเลือก **ท่าสินค้าขาออก**</span><span class="sxs-lookup"><span data-stu-id="ccd63-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="ccd63-134">ยกเลิกการเลือกตัวเลือก **สถานที่เก็บสินค้าจำนวนมาก**</span><span class="sxs-lookup"><span data-stu-id="ccd63-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="ccd63-135">เลือก **ถัดไป** จนกว่าคุณจะมาถึงตัวเลือกเพื่อเลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="ccd63-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="ccd63-136">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ccd63-136">Close the page.</span></span>
8. <span data-ttu-id="ccd63-137">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="ccd63-137">Refresh the page.</span></span>

