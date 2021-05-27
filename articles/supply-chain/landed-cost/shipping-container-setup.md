---
title: คอนเทนเนอร์การจัดส่ง
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนเทนเนอร์การจัดส่งสำหรับโมดูลต้นทุนแฝง
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 8f86f3603b64093214bb7cf7d165ba0fc2229ca3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021551"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="30a22-103">การตั้งค่าคอนเทนเนอร์การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30a22-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนเทนเนอร์การจัดส่งสำหรับโมดูล **ต้นทุนแฝง**</span><span class="sxs-lookup"><span data-stu-id="30a22-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="30a22-105">ตั้งค่าชนิดคอนเทนเนอร์การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-105">Set up shipping container types</span></span>

<span data-ttu-id="30a22-106">ชนิดคอนเทนเนอร์การจัดส่งจะกําหนดชนิดของคอนเทนเนอร์การจัดส่งที่พร้อมใช้งานในระหว่างการเดินทางและการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="30a22-107">เมื่อต้องการใช้งานชนิดคอนเทนเนอร์การจัดส่ง ให้ไปที่ชนิด **ต้นทุนแฝง \> การตั้งค่าคอนเทนเนอร์ \> ชนิดคอนเทนเนอร์การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="30a22-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="30a22-108">ที่นั่น คุณสามารถดู เพิ่ม และลบเรกคอร์ดสำหรับชนิดคอนเทนเนอร์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="30a22-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="30a22-109">ตารางต่อไปนี้อธิบายถึงฟิลด์ที่พร้อมใช้งานสำหรับเรกคอร์ดแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="30a22-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="30a22-110">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="30a22-110">Field</span></span> | <span data-ttu-id="30a22-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="30a22-111">Description</span></span> |
|---|---|
| <span data-ttu-id="30a22-112">ชนิดคอนเทนเนอร์การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-112">Shipping container type</span></span> | <span data-ttu-id="30a22-113">ป้อนหมายเลขประจำตัว/ชื่อเฉพาะสำหรับชนิดคอนเทนเนอร์การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="30a22-114">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="30a22-114">Description</span></span> | <span data-ttu-id="30a22-115">ป้อนคำอธิบายของชนิดคอนเทนเนอร์การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="30a22-116">ปริมาตร</span><span class="sxs-lookup"><span data-stu-id="30a22-116">Volume</span></span> | <span data-ttu-id="30a22-117">ป้อนปริมาตรสูงสุดที่อนุญาตในคอนเทนเนอร์การจัดส่งชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="30a22-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="30a22-118">น้ำหนัก</span><span class="sxs-lookup"><span data-stu-id="30a22-118">Weight</span></span> | <span data-ttu-id="30a22-119">ป้อนน้ำหนักสูงสุดที่อนุญาตในคอนเทนเนอร์การจัดส่งชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="30a22-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="30a22-120">ส่งคืนได้</span><span class="sxs-lookup"><span data-stu-id="30a22-120">Returnable</span></span> | <span data-ttu-id="30a22-121">ระบุว่าสามารถส่งคืนคอนเทนเนอร์การจัดส่งชนิดนี้ไปยังผู้จัดจำหน่ายหลังจากใช้ระหว่างการเดินทางหรือไม่</span><span class="sxs-lookup"><span data-stu-id="30a22-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="30a22-122">ถ้าตั้งค่าตัวเลือกนี้เป็น *ใช่* อาจมีต้นทุนเพิ่มเติมที่จะใช้ในการส่งคืนคอนเทนเนอร์การจัดส่งชนิดนี้ไปยังท่าเรือต้นทาง</span><span class="sxs-lookup"><span data-stu-id="30a22-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="30a22-123">ตั้งค่าคอนเทนเนอร์การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-123">Set up shipping containers</span></span>

<span data-ttu-id="30a22-124">คุณใช้เรกคอร์ดคอนเทนเนอร์การจัดส่งเพื่อระบุคอนเทนเนอร์แต่ละแห่งที่คุณใช้ระหว่างการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="30a22-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="30a22-125">เมื่อคุณสร้างการเดินทาง คุณสามารถเลือกเฉพาะคอนเทนเนอร์หนึ่ง ๆ ได้ในรายการเรกคอร์ดคอนเทนเนอร์การจัดส่งทั้งหมดที่คุณกําหนดไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="30a22-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="30a22-126">ลักษณะการเช่นนี้มีประโยชน์โดยเฉพาะอย่างยิ่งถ้าบริษัทของคุณเป็นเจ้าของคอนเทนเนอร์การจัดส่งของตนเอง</span><span class="sxs-lookup"><span data-stu-id="30a22-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="30a22-127">คุณไม่มีสิทธิ์ป้อนหมายเลขคอนเทนเนอร์การจัดส่งในคอนเทนเนอร์การจัดส่งที่จะใช้เป็นเวลาในการจัดส่งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="30a22-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="30a22-128">แต่คุณสามารถเพิ่มหมายเลขคอนเทนเนอร์เมื่อคุณสร้างการเดินทางได้</span><span class="sxs-lookup"><span data-stu-id="30a22-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="30a22-129">เรกคอร์ดคอนเทนเนอร์การจัดส่งจะใช้ในต้นทุนแฝงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="30a22-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="30a22-130">ไม่มีอยู่ในโมดูล **การจัดการการขนส่ง** มาตรฐาน (TMS)</span><span class="sxs-lookup"><span data-stu-id="30a22-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="30a22-131">เมื่อต้องการใช้งานคอนเทนเนอร์การจัดส่ง ให้ไปที่ชนิด **ต้นทุนแฝง \> การตั้งค่าคอนเทนเนอร์ \> คอนเทนเนอร์การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="30a22-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="30a22-132">ที่นั่น คุณสามารถดู เพิ่ม และลบเรกคอร์ดสำหรับคอนเทนเนอร์การจัดส่งของคุณได้</span><span class="sxs-lookup"><span data-stu-id="30a22-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="30a22-133">ตารางต่อไปนี้อธิบายถึงฟิลด์ที่พร้อมใช้งานสำหรับเรกคอร์ดแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="30a22-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="30a22-134">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="30a22-134">Field</span></span> | <span data-ttu-id="30a22-135">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="30a22-135">Description</span></span> |
|---|---|
| <span data-ttu-id="30a22-136">คอนเทนเนอร์การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-136">Shipping container</span></span> | <span data-ttu-id="30a22-137">ป้อนหมายเลขประจำตัว/ชื่อเฉพาะสำหรับคอนเทนเนอร์การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="30a22-138">ชนิดคอนเทนเนอร์การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-138">Shipping container type</span></span> | <span data-ttu-id="30a22-139">เลือกชนิดของคอนเทนเนอร์การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-139">Select the type of shipping container.</span></span> <span data-ttu-id="30a22-140">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [ตั้งค่าชนิดคอนเทนเนอร์การจัดส่ง](#shipping-container-types) ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="30a22-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="30a22-141">การตั้งค่าคอนเทนเนอร์การจัดส่งเป็นข้อมูลที่ไม่บังคับ</span><span class="sxs-lookup"><span data-stu-id="30a22-141">The shipping container setup is optional.</span></span> <span data-ttu-id="30a22-142">โดยทั่วไป คุณจะใช้คอนเทนเนอร์นั้นเฉพาะเมื่อบริษัทของคุณเป็นเจ้าของคอนเทนเนอร์การจัดส่งของตนเอง หรือมักใช้คอนเทนเนอร์การจัดส่งเดิมมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="30a22-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="30a22-143">ไม่มีการคํานวณตัวเลขการตรวจสอบกับหมายเลขคอนเทนเนอร์การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="30a22-144">ตั้งค่าชนิดของหน่วย</span><span class="sxs-lookup"><span data-stu-id="30a22-144">Set up unit types</span></span>

<span data-ttu-id="30a22-145">ชนิดของหน่วยจะกําหนดการจัดกลุ่มและวิธีการระบุเพิ่มเติมต่าง ๆ ในคอนเทนเนอร์การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="30a22-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="30a22-146">โดยทั่วไป ชนิดหน่วยจะใช้เพื่อระบุชนิดของคอนเทนเนอร์ที่บรรจุอยู่ในบรรจุภัณฑ์ เช่น แท่นวางสินค้าหรือดรัม</span><span class="sxs-lookup"><span data-stu-id="30a22-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="30a22-147">คุณสามารถเลือกชนิดของหน่วยเมื่อคุณตั้งค่าคอนเทนเนอร์ในหน้า **คอนเทนเนอร์การจัดส่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="30a22-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="30a22-148">ชนิดของหน่วยจะใช้ในต้นทุนแฝงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="30a22-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="30a22-149">ไม่พร้อมใช้งานใน TMS</span><span class="sxs-lookup"><span data-stu-id="30a22-149">They aren't available in TMS.</span></span>

<span data-ttu-id="30a22-150">เมื่อต้องการใช้งานชนิดของหน่วย ให้ไปที่ชนิด **ต้นทุนแฝง \> การตั้งค่าคอนเทนเนอร์ \> ชนิดของหน่วย**</span><span class="sxs-lookup"><span data-stu-id="30a22-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="30a22-151">ที่นั่น คุณสามารถดู เพิ่ม และลบเรกคอร์ดสำหรับชนิดของหน่วยของคุณได้</span><span class="sxs-lookup"><span data-stu-id="30a22-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="30a22-152">ตารางต่อไปนี้อธิบายถึงฟิลด์ที่พร้อมใช้งานสำหรับเรกคอร์ดแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="30a22-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="30a22-153">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="30a22-153">Field</span></span> | <span data-ttu-id="30a22-154">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="30a22-154">Description</span></span> |
|---|---|
| <span data-ttu-id="30a22-155">ชนิดของหน่วย</span><span class="sxs-lookup"><span data-stu-id="30a22-155">Unit type</span></span> | <span data-ttu-id="30a22-156">ป้อนหมายเลขประจำตัว/ชื่อเฉพาะสำหรับชนิดของหน่วย</span><span class="sxs-lookup"><span data-stu-id="30a22-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="30a22-157">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="30a22-157">Description</span></span> | <span data-ttu-id="30a22-158">ป้อนคำอธิบายของชนิดของหน่วย</span><span class="sxs-lookup"><span data-stu-id="30a22-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="30a22-159">ตั้งค่าชนิดห้องเย็น</span><span class="sxs-lookup"><span data-stu-id="30a22-159">Set up refrigeration types</span></span>

<span data-ttu-id="30a22-160">ชนิดของห้องเย็นจะกําหนดการจัดกลุ่มและวิธีการระบุเพิ่มเติมต่าง ๆ ในคอนเทนเนอร์การจัดส่ง (ปกติคอนเทนเนอร์ห้องเย็น)</span><span class="sxs-lookup"><span data-stu-id="30a22-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="30a22-161">คุณสามารถเลือกชนิดของห้องเย็นเมื่อคุณตั้งค่าคอนเทนเนอร์ในหน้า **คอนเทนเนอร์การจัดส่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="30a22-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="30a22-162">เมื่อต้องการใช้งานชนิดของห้องเย็น ให้ไปที่ชนิด **ต้นทุนแฝง \> การตั้งค่าคอนเทนเนอร์ \> ชนิดของห้องเย็น**</span><span class="sxs-lookup"><span data-stu-id="30a22-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="30a22-163">ที่นั่น คุณสามารถดู เพิ่ม และลบเรกคอร์ดสำหรับชนิดห้องเย็นของคุณได้</span><span class="sxs-lookup"><span data-stu-id="30a22-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="30a22-164">ตารางต่อไปนี้อธิบายถึงฟิลด์ที่พร้อมใช้งานสำหรับเรกคอร์ดแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="30a22-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="30a22-165">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="30a22-165">Field</span></span> | <span data-ttu-id="30a22-166">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="30a22-166">Description</span></span> |
|---|---|
| <span data-ttu-id="30a22-167">ชนิดการทำความเย็น</span><span class="sxs-lookup"><span data-stu-id="30a22-167">Refrigeration type</span></span> | <span data-ttu-id="30a22-168">ป้อนหมายเลขประจำตัว/ชื่อเฉพาะสำหรับชนิดของห้องเย็น</span><span class="sxs-lookup"><span data-stu-id="30a22-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="30a22-169">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="30a22-169">Description</span></span> | <span data-ttu-id="30a22-170">ป้อนคำอธิบายเกี่ยวกับชนิดของห้องเย็น</span><span class="sxs-lookup"><span data-stu-id="30a22-170">Enter a description of the refrigeration type.</span></span> |
