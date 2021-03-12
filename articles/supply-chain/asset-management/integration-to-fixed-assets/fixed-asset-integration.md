---
title: รวมการจัดการสินทรัพย์กับสินทรัพย์ถาวร
description: หัวข้อนี้จะอธิบายถึงวิธีการรวมการบริหารสินทรัพย์และโมดูลบัญชีสินทรัพย์ถาวร เพื่อให้คุณสามารถเชื่อมโยงสินทรัพย์ถาวรกับสินทรัพย์ที่บำรุงรักษาได้
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 879950b9aeb345fcd59dfe73d3963a44607c7ac2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994240"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="2b1ce-103">รวมการจัดการสินทรัพย์กับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="2b1ce-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b1ce-104">โดยการรวมโมดูล **การบริหารสินทรัพย์** และ **บัญชีสินทรัพย์ถาวร** คุณสามารถเชื่อมโยงสินทรัพย์ถาวรกับสินทรัพย์ที่บำรุงรักษาได้</span><span class="sxs-lookup"><span data-stu-id="2b1ce-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="2b1ce-105">ผู้ใช้สินทรัพย์ถาวรสามารถสร้างสินทรัพย์ที่บำรุงรักษาจากสินทรัพย์ถาวรใหม่หรือสินทรัพย์ถาวรที่มีอยู่ และผู้ใช้ในการจัดการสินทรัพย์สามารถเชื่อมโยงสินทรัพย์ที่บำรุงรักษากับสินทรัพย์ถาวรที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="2b1ce-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="2b1ce-106">นอกจากนี้ คุณลักษณะนี้ยังช่วยให้ผู้ใช้สินทรัพย์ถาวรสามารถดูต้นทุนที่มีการลงรายการบัญชีจากใบสั่งงานได้ง่าย สำหรับสินทรัพย์ที่บำรุงรักษาที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="2b1ce-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="2b1ce-107">ในหัวข้อนี้ *สินทรัพย์ที่บำรุงรักษา* อ้างอิงถึงสินทรัพย์จากโมดูล **การจัดการสินทรัพย์** และ *สินทรัพย์ถาวร* อ้างอิงถึงสินทรัพย์จากโมดูล **สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="2b1ce-108">ตั้งค่าสถานที่เริ่มต้นสำหรับสินทรัพย์ที่บำรุงรักษาใหม่ที่สร้างขึ้นจากสินทรัพย์ถาวร (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="2b1ce-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="2b1ce-109">การตั้งค่าคอนฟิกที่เลือกกำหนดได้นี้อนุญาตให้คุณตั้งค่าตำแหน่งที่ทำงานเริ่มต้นสำหรับสินทรัพย์ที่บำรุงรักษาใหม่ที่สร้างขึ้นจากสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="2b1ce-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="2b1ce-110">โดยทั่วไป คุณจะทำการตั้งค่าคอนฟิกนี้ให้เสร็จสมบูรณ์เพียงครั้งเดียว ถ้าคุณดำเนินการให้เสร็จสมบูรณ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2b1ce-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="2b1ce-111">เพื่อให้การตั้งค่าคอนฟิกเสร็จสมบูรณ์ ให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="2b1ce-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="2b1ce-112">ไปที่ **การจัดการสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การจัดการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="2b1ce-113">บนแท็บ **สินทรัพย์ถาวร** ในฟิลด์ **ตำแหน่งที่ทำงาน** เลือกสถานที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2b1ce-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="2b1ce-114">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="2b1ce-115">การทำงานกับสินทรัพย์ที่บำรุงรักษาและสินทรัพย์ถาวรแบบรวม</span><span class="sxs-lookup"><span data-stu-id="2b1ce-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="2b1ce-116">ส่วนนี้จะให้ชุดของกระบวนงานต่างๆ ที่แสดงวิธีต่างๆ ที่คุณสามารถทำงานกับคุณลักษณะการจัดการสินทรัพย์และสินทรัพย์ถาวรแบบรวม</span><span class="sxs-lookup"><span data-stu-id="2b1ce-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="2b1ce-117">เชื่อมโยงสินทรัพย์ที่บำรุงรักษาที่มีอยู่กับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="2b1ce-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="2b1ce-118">เพื่อเชื่อมโยงสินทรัพย์ที่บำรุงรักษาที่มีอยู่กับสินทรัพย์ถาวร ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2b1ce-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="2b1ce-119">ไปยัง **การจัดการสินทรัพย์ \> สินทรัพย์ \> สินทรัพย์ทั้งหมด** (หรือ **สินทรัพย์ที่ใช้งานอยู่**)</span><span class="sxs-lookup"><span data-stu-id="2b1ce-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="2b1ce-120">เลือกสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2b1ce-120">Select an asset.</span></span>
1. <span data-ttu-id="2b1ce-121">บน FastTab **สินทรัพย์ถาวร** ในฟิลด์ **หมายเลขสินทรัพย์ถาวร** ให้เลือกสินทรัพย์ถาวรที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="2b1ce-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="2b1ce-122">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="2b1ce-123">ดูสินทรัพย์ถาวรที่สัมพันธ์กับสินทรัพย์ที่บำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2b1ce-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="2b1ce-124">เพื่อดูสินทรัพย์ถาวรที่สัมพันธ์กับสินทรัพย์ที่บำรุงรักษาที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2b1ce-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="2b1ce-125">ไปยัง **การจัดการสินทรัพย์ \> สินทรัพย์ \> สินทรัพย์ทั้งหมด** (หรือ **สินทรัพย์ที่ใช้งานอยู่**)</span><span class="sxs-lookup"><span data-stu-id="2b1ce-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="2b1ce-126">เลือกสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2b1ce-126">Select an asset.</span></span>
1. <span data-ttu-id="2b1ce-127">บน FastTab **สินทรัพย์ถาวร** ในฟิลด์ **หมายเลขสินทรัพย์ถาวร** ให้เลือกการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="2b1ce-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="2b1ce-128">หน้า **สินทรัพย์ถาวร** สำหรับสินทรัพย์ที่เลือกถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="2b1ce-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="2b1ce-129">(โดยทั่วไป จะพบหน้านี้ที่ **สินทรัพย์ถาวร \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร**)</span><span class="sxs-lookup"><span data-stu-id="2b1ce-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="2b1ce-130">ดูสินทรัพย์ที่บำรุงรักษาที่สัมพันธ์กับสินทรัพย์ถาวรที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2b1ce-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="2b1ce-131">เพื่อดูสินทรัพย์ที่บำรุงรักษาที่สัมพันธ์กับสินทรัพย์ถาวรที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2b1ce-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="2b1ce-132">ไปที่ **สินทรัพย์ถาวร \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="2b1ce-133">เลือกสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2b1ce-133">Select an asset.</span></span>
1. <span data-ttu-id="2b1ce-134">บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดการสินทรัพย์** ในกลุ่ม **มุมมอง** ให้เลือก **สินทรัพย์ที่บำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="2b1ce-135">หน้า **สินทรัพย์ที่บำรุงรักษา** สำหรับสินทรัพย์ที่สัมพันธ์กับสินทรัพย์ถาวรที่เลือกจะถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="2b1ce-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="2b1ce-136">(โดยทั่วไป จะพบหน้านี้ที่ **การจัดการสินทรัพย์ \> สินทรัพย์ \> สินทรัพย์ทั้งหมด**)</span><span class="sxs-lookup"><span data-stu-id="2b1ce-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="2b1ce-137">ดูต้นทุนการบำรุงรักษาที่สัมพันธ์กับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="2b1ce-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="2b1ce-138">คุณสามารถลงรายการบัญชีใบสั่งงานการจัดการสินทรัพย์สำหรับสินทรัพย์บำรุงรักษาได้ และโดยทั่วไปใบสั่งงานแต่ละใบจะมีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2b1ce-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="2b1ce-139">เมื่อสินทรัพย์ถาวรเชื่อมโยงกับสินทรัพย์ของการบำรุงรักษา คุณสามารถไปจากสินทรัพย์ถาวรได้โดยตรงเพื่อดูต้นทุนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="2b1ce-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="2b1ce-140">เพื่อดูต้นทุนการบำรุงรักษาที่สัมพันธ์กับสินทรัพย์ถาวร ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2b1ce-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="2b1ce-141">ไปที่ **สินทรัพย์ถาวร \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="2b1ce-142">เลือกสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2b1ce-142">Select an asset.</span></span>
1. <span data-ttu-id="2b1ce-143">บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดการสินทรัพย์** ในกลุ่ม **มุมมอง** ให้เลือก **ต้นทุนการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="2b1ce-144">หน้า **ต้นทุนการบำรุงรักษา** เปิดอยู่ และแสดงต้นทุนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="2b1ce-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="2b1ce-145">สร้างสินทรัพย์ที่บำรุงรักษาใหม่สำหรับสินทรัพย์ถาวรที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="2b1ce-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="2b1ce-146">เพื่อสร้างสินทรัพย์ที่บำรุงรักษาใหม่สำหรับสินทรัพย์ถาวรที่มีอยู่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2b1ce-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="2b1ce-147">ไปที่ **สินทรัพย์ถาวร \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="2b1ce-148">เลือกสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2b1ce-148">Select an asset.</span></span>
1. <span data-ttu-id="2b1ce-149">บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดการสินทรัพย์** ในกลุ่ม **ใหม่** ให้เลือก **สร้างสินทรัพย์ที่บำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="2b1ce-150">(ถ้าตัวเลือกนี้ไม่พร้อมใช้งาน สินทรัพย์ที่บำรุงรักษาอาจเชื่อมโยงกับสินทรัพย์ถาวรที่เลือกอยู่แล้ว)</span><span class="sxs-lookup"><span data-stu-id="2b1ce-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="2b1ce-151">เสร็จสิ้นการสร้างสินทรัพย์ตามที่อธิบายไว้ใน [สร้างสินทรัพย์](../objects/create-an-object.md)</span><span class="sxs-lookup"><span data-stu-id="2b1ce-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="2b1ce-152">สร้างสินทรัพย์ถาวรใหม่และเพิ่มสินทรัพย์ที่บำรุงรักษาใหม่</span><span class="sxs-lookup"><span data-stu-id="2b1ce-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="2b1ce-153">เพื่อสร้างสินทรัพย์ถาวรใหม่และเพิ่มสินทรัพย์ที่บำรุงรักษาใหม่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2b1ce-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="2b1ce-154">ไปที่ **สินทรัพย์ถาวร \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="2b1ce-155">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2b1ce-156">เสร็จสิ้นการสร้างสินทรัพย์ถาวรตามที่อธิบายไว้ใน [สร้างสินทรัพย์ถาวร](../../../finance/fixed-assets/tasks/create-fixed-asset.md)</span><span class="sxs-lookup"><span data-stu-id="2b1ce-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="2b1ce-157">บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดการสินทรัพย์** ในกลุ่ม **ใหม่** ให้เลือก **สร้างสินทรัพย์ที่บำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="2b1ce-158">เสร็จสิ้นการสร้างสินทรัพย์ตามที่อธิบายไว้ใน [สร้างสินทรัพย์](../objects/create-an-object.md)</span><span class="sxs-lookup"><span data-stu-id="2b1ce-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="2b1ce-159">ลบการเชื่อมโยงระหว่างสินทรัพย์สองรายการ</span><span class="sxs-lookup"><span data-stu-id="2b1ce-159">Remove the association between two assets</span></span>

<span data-ttu-id="2b1ce-160">ในบางกรณี คุณอาจต้องยกเลิกการเชื่อมโยงสินทรัพย์ที่บำรุงรักษาจากสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="2b1ce-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="2b1ce-161">ตัวอย่างเช่น ถ้าคุณต้องการ [สร้างสินทรัพย์ที่บำรุงรักษาใหม่](#new-maintenance-from-fixed) จากสินทรัพย์ถาวร ก่อนอื่นคุณต้องลบการเชื่อมโยงที่มีอยู่ใดๆ</span><span class="sxs-lookup"><span data-stu-id="2b1ce-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="2b1ce-162">เมื่อต้องการลบการเชื่อมโยงที่มีอยู่ระหว่างสินทรัพย์ที่บำรุงรักษาและสินทรัพย์ถาวร ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2b1ce-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="2b1ce-163">ไปยัง **การจัดการสินทรัพย์ \> สินทรัพย์ \> สินทรัพย์ทั้งหมด** (หรือ **สินทรัพย์ที่ใช้งานอยู่**)</span><span class="sxs-lookup"><span data-stu-id="2b1ce-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="2b1ce-164">ค้นหาและเปิดสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="2b1ce-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="2b1ce-165">บน FastTab **สินทรัพย์ถาวร** ให้ล้างค่าจากฟิลด์ **ตำแหน่งที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="2b1ce-166">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2b1ce-166">On the Action Pane, select **Save**.</span></span>
