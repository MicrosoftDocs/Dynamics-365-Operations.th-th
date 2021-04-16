---
title: การตั้งค่าข้อมูลการจัดส่งสินค้า
description: หัวข้อนี้อธิบายวิธีการตั้งค่าข้อมูลการจัดส่งสำหรับโมดูลต้นทุนแฝง
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 74ac7e0eac545369eef1a48f0085c820a4728e75
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833700"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="6a698-103">การตั้งค่าข้อมูลการจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="6a698-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a698-104">หัวข้อนี้อธิบายวิธีการตั้งค่าข้อมูลการจัดส่งสำหรับโมดูล **ต้นทุนแฝง**</span><span class="sxs-lookup"><span data-stu-id="6a698-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="6a698-105">คำอธิบายเกี่ยวกับสินค้า</span><span class="sxs-lookup"><span data-stu-id="6a698-105">Description of goods</span></span>

<span data-ttu-id="6a698-106">คำอธิบายสินค้าจะช่วยระบุการเดินทาง คอนเทนเนอร์การจัดส่ง หรือใบแจ้งรายการ และสินค้าในนั้น</span><span class="sxs-lookup"><span data-stu-id="6a698-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="6a698-107">คุณสามารถเลือกรายละเอียดเกี่ยวกับสินค้าบนส่วนหน้าของคอนเทนเนอร์การจัดส่งหรือส่วนหน้าของใบแจ้งรายการ</span><span class="sxs-lookup"><span data-stu-id="6a698-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="6a698-108">เมื่อต้องการใช้งานอธิบายเกี่ยวกับสินค้า ให้ไปที่ **ต้นทุนแฝง \> การตั้งค่าข้อมูลการจัดส่ง \> คำอธิบายของสินค้า**</span><span class="sxs-lookup"><span data-stu-id="6a698-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="6a698-109">คุณสามารถดู เปิด สร้าง และลบเรกคอร์ดสำหรับคำอธิบายสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="6a698-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="6a698-110">ตารางต่อไปนี้อธิบายถึงฟิลด์ที่พร้อมใช้งานสำหรับเรกคอร์ดแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="6a698-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="6a698-111">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="6a698-111">Field</span></span> | <span data-ttu-id="6a698-112">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6a698-112">Description</span></span> |
|---|---|
| <span data-ttu-id="6a698-113">คำอธิบายเกี่ยวกับสินค้า</span><span class="sxs-lookup"><span data-stu-id="6a698-113">Description of goods</span></span> | <span data-ttu-id="6a698-114">ป้อนชื่อ/หมายเลขการระบุรหัสประจำตัวของชนิดสินค้าที่จะใช้อธิบายนี้</span><span class="sxs-lookup"><span data-stu-id="6a698-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="6a698-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6a698-115">Description</span></span> | <span data-ttu-id="6a698-116">ป้อนคำอธิบายเกี่ยวกับชนิดของสินค้าในประเภทนี้</span><span class="sxs-lookup"><span data-stu-id="6a698-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="6a698-117">เรือ</span><span class="sxs-lookup"><span data-stu-id="6a698-117">Vessels</span></span>

<span data-ttu-id="6a698-118">เรือคือชื่อเฉพาะของเรือหรือเรือที่บริษัทจัดส่งสินค้าหรือตัวแทนใช้</span><span class="sxs-lookup"><span data-stu-id="6a698-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="6a698-119">เมื่อคุณสร้างการเดินทาง คุณต้องเลือกหรือป้อนเรือให้เสมอ</span><span class="sxs-lookup"><span data-stu-id="6a698-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="6a698-120">ถ้าคุณมักใช้เรือเดียวกัน คุณสามารถช่วยให้การสร้างการเดินทางใหม่มีความรวดเร็วขึ้นและง่ายขึ้นด้วยการสร้างเรกคอร์ดเรือเพื่อแต่ละเรือ ของพวกเขา จึงอนุญาตให้ผู้ใช้เลือกเรือจากรายการ แทนที่จะป้อนชื่อหรือหมายเลขด้วยตนเองแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="6a698-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="6a698-121">เมื่อต้องการทำงานกับเรือ ให้ไปที่ **ต้นทุนแฝง \> การตั้งค่าข้อมูลการจัดส่ง \> เรือ**</span><span class="sxs-lookup"><span data-stu-id="6a698-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="6a698-122">คุณสามารถดู เปิด สร้าง และลบเรกคอร์ดสำหรับเรือได้</span><span class="sxs-lookup"><span data-stu-id="6a698-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="6a698-123">ตารางต่อไปนี้อธิบายถึงฟิลด์ที่พร้อมใช้งานสำหรับเรกคอร์ดแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="6a698-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="6a698-124">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="6a698-124">Field</span></span> | <span data-ttu-id="6a698-125">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6a698-125">Description</span></span> |
|---|---|
| <span data-ttu-id="6a698-126">เรือ</span><span class="sxs-lookup"><span data-stu-id="6a698-126">Vessel</span></span> | <span data-ttu-id="6a698-127">ป้อนชื่อ/หมายเลขการระบุรหัสประจำตัวของการจัดส่งที่จะใช้ในการขนส่งสินค้าบนการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="6a698-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="6a698-128">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6a698-128">Description</span></span> | <span data-ttu-id="6a698-129">ป้อนคำอธิบายเกี่ยวกับเรือ</span><span class="sxs-lookup"><span data-stu-id="6a698-129">Enter a description of the vessel.</span></span> <span data-ttu-id="6a698-130">โดยทั่วไป คำอธิบายนี้จะระบุชื่อของการจัดส่งและบริษัท/ตัวแทนจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="6a698-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="6a698-131">วิธีการนำส่ง</span><span class="sxs-lookup"><span data-stu-id="6a698-131">Mode of delivery</span></span> | <span data-ttu-id="6a698-132">เลือกวิธีการจัดส่งที่เรือใช้ (เช่น _ทางอากาศ_ _ทะเล_ หรือ _รถไฟ_)</span><span class="sxs-lookup"><span data-stu-id="6a698-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="6a698-133">ผู้ส่งออก</span><span class="sxs-lookup"><span data-stu-id="6a698-133">Exporters</span></span>

<span data-ttu-id="6a698-134">เรกคอร์ดผู้ส่งออกแต่ละเรกคอร์ดจะระบุผู้จัดจำหน่ายหรือผู้ส่งออกที่สามารถกําหนดเป็นผู้จัดจำหน่ายเพื่อการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="6a698-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="6a698-135">ผู้ส่งออกสามารถเชื่อมโยงกับการเดินทางและใช้ในการรายงานได้</span><span class="sxs-lookup"><span data-stu-id="6a698-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="6a698-136">เมื่อต้องการทำงานกับผู้ส่งออก ให้ไปที่ **ต้นทุนแฝง \> การตั้งค่าข้อมูลการจัดส่ง \> ผู้ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="6a698-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="6a698-137">คุณสามารถดู เปิด สร้าง และลบเรกคอร์ดสำหรับผู้ส่งออกได้</span><span class="sxs-lookup"><span data-stu-id="6a698-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="6a698-138">ตารางต่อไปนี้อธิบายถึงฟิลด์ที่พร้อมใช้งานสำหรับเรกคอร์ดแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="6a698-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="6a698-139">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="6a698-139">Field</span></span> | <span data-ttu-id="6a698-140">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6a698-140">Description</span></span> |
|---|---|
| <span data-ttu-id="6a698-141">ผู้ส่งออก</span><span class="sxs-lookup"><span data-stu-id="6a698-141">Exporter</span></span> | <span data-ttu-id="6a698-142">ป้อนชื่อ/หมายเลขการระบุรหัสประจำตัวของผู้ส่งออกสินค้าที่จะใช้ในการขนส่งบนการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="6a698-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="6a698-143">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6a698-143">Description</span></span> | <span data-ttu-id="6a698-144">ป้อนคำอธิบายเกี่ยวกับผู้ส่งออก</span><span class="sxs-lookup"><span data-stu-id="6a698-144">Enter a description of the exporter.</span></span> <span data-ttu-id="6a698-145">โดยทั่วไป คำอธิบายนี้จะระบุชื่อเต็มของบริษัท/ตัวแทนจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="6a698-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="6a698-146">รหัสโภคภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6a698-146">Commodity codes</span></span>

<span data-ttu-id="6a698-147">คุณใช้รหัสโภคภัณฑ์เพื่อช่วยในการระบุการระบุรหัสประจำตัวศุลกากรและการคํานวณอัตราภาษีของสินค้าบนการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="6a698-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="6a698-148">คุณสามารถเลือกรหัสโภคภัณฑ์ได้ในหน้า **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="6a698-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="6a698-149">เมื่อต้องการทำงานกับรหัสโภคภัณฑ์ ให้ไปที่ **ต้นทุนแฝง \> การตั้งค่าข้อมูลการจัดส่ง \> รหัสโภคภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="6a698-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="6a698-150">คุณสามารถดู เปิด สร้าง และลบเรกคอร์ดสำหรับรหัสโภคภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="6a698-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="6a698-151">ตารางต่อไปนี้อธิบายถึงฟิลด์ที่พร้อมใช้งานสำหรับเรกคอร์ดแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="6a698-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="6a698-152">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="6a698-152">Field</span></span> | <span data-ttu-id="6a698-153">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6a698-153">Description</span></span> |
|---|---|
| <span data-ttu-id="6a698-154">รหัสโภคภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6a698-154">Commodity code</span></span> | <span data-ttu-id="6a698-155">ป้อนรหัสเฉพาะของโภคภัณฑ์ชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="6a698-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="6a698-156">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6a698-156">Description</span></span> | <span data-ttu-id="6a698-157">ป้อนคำอธิบายเกี่ยวกับชนิดโภคภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6a698-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="6a698-158">คำอธิบายเกี่ยวกับศุลกากร</span><span class="sxs-lookup"><span data-stu-id="6a698-158">Customs description</span></span>

<span data-ttu-id="6a698-159">รายละเอียดศุลกากรจะช่วยระบุสินค้าเพื่อวัตถุประสงค์ทางด้านศุลกากร</span><span class="sxs-lookup"><span data-stu-id="6a698-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="6a698-160">คุณสามารถเลือกข้อความอธิบายศุลกากรในหน้า **ผลิตภัณฑ์ที่นำออกใช้** หรือบนรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="6a698-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="6a698-161">เมื่อต้องการใช้งานคำอธิบายศุลกากร ให้ไปที่ **ต้นทุนแฝง \> การตั้งค่าข้อมูลการจัดส่ง \> คำอธิบายของศุลกากร**</span><span class="sxs-lookup"><span data-stu-id="6a698-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="6a698-162">คุณสามารถดู เปิด สร้าง และลบเรกคอร์ดสำหรับคำอธิบายศุลกากรได้</span><span class="sxs-lookup"><span data-stu-id="6a698-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="6a698-163">ตารางต่อไปนี้อธิบายถึงฟิลด์ที่พร้อมใช้งานสำหรับเรกคอร์ดแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="6a698-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="6a698-164">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="6a698-164">Field</span></span> | <span data-ttu-id="6a698-165">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6a698-165">Description</span></span> |
|---|---|
| <span data-ttu-id="6a698-166">คำอธิบายเกี่ยวกับศุลกากร</span><span class="sxs-lookup"><span data-stu-id="6a698-166">Customs description</span></span> | <span data-ttu-id="6a698-167">ป้อนรหัสเฉพาะของการจัดประเภทศุลกากรชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="6a698-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="6a698-168">บ่อยครั้งที่รหัสนี้จะเป็นอธิบายที่เป็นทางการซึ่งจัดเตรียมให้โดยหน่วยงานศุลกากรเพื่ออธิบายและมูลค่าเชิงคุณภาพของสินค้า</span><span class="sxs-lookup"><span data-stu-id="6a698-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="6a698-169">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6a698-169">Description</span></span> | <span data-ttu-id="6a698-170">ป้อนคำอธิบายเกี่ยวกับการจัดประเภทศุลกากร</span><span class="sxs-lookup"><span data-stu-id="6a698-170">Enter a description of the customs classification.</span></span> |
