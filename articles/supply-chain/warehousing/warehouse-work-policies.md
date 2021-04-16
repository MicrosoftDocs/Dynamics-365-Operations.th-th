---
title: นโยบายงาน
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่านโยบายงาน
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 39a9ba00763fac220eff16bdd42aa07cc8e35ba4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838141"
---
# <a name="work-policies"></a><span data-ttu-id="55072-103">นโยบายงาน</span><span class="sxs-lookup"><span data-stu-id="55072-103">Work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55072-104">หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าระบบและแอปการจัดการคลังสินค้าบนมือถือ เพื่อให้สนับสนุนนโยบายงาน</span><span class="sxs-lookup"><span data-stu-id="55072-104">This topic explains how to set up the system and the Warehouse Management mobile app so that they support work policies.</span></span> <span data-ttu-id="55072-105">คุณสามารถใช้ฟังก์ชันนี้เพื่อลงทะเบียนสินค้าคงคลังได้อย่างรวดเร็วโดยไม่ต้องสร้างงานการสำรองสินค้า เมื่อคุณได้รับใบสั่งซื้อหรือใบสั่งโอนย้าย หรือเมื่อคุณดำเนินกระบวนการผลิตเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="55072-105">You can use this functionality to quickly register inventory without creating putaway work when you receive purchase or transfer orders, or when you complete manufacturing processes.</span></span> <span data-ttu-id="55072-106">หัวข้อนี้ให้ข้อมูลทั่วไป</span><span class="sxs-lookup"><span data-stu-id="55072-106">This topic provides general information.</span></span> <span data-ttu-id="55072-107">สำหรับข้อมูลรายละเอียดที่เกี่ยวข้องกับการรับป้ายทะเบียน ให้ดูที่ [ป้ายทะเบียนที่ได้รับผ่านทางแอปการจัดการคลังสินค้าบนมือถือ](warehousing-mobile-device-app-license-plate-receiving.md)</span><span class="sxs-lookup"><span data-stu-id="55072-107">For detailed information that is related to license plate receiving, see [License plate receiving via the Warehouse Management mobile app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="55072-108">นโยบายงานจะควบคุมว่าจะสร้างงานของคลังสินค้าเมื่อมีการรายงานการเสร็จงานของสินค้าที่ผลิต หรือเมื่อได้รับสินค้าโดยใช้แอปการจัดการคลังสินค้าบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="55072-108">A work policy controls whether warehouse work is created when a manufactured item is reported as finished, or when goods are received by using the Warehouse Management mobile app.</span></span> <span data-ttu-id="55072-109">คุณตั้งค่านโยบายงานแต่ละรายการโดยการกำหนดเงื่อนไข ซึ่งจะใช้: ชนิดของใบสั่งงานและกระบวนการ สถานที่เก็บสินค้าคงคลัง และ (หรือ) ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="55072-109">You set up each work policy by defining the conditions where it applies: the work order types and processes, the inventory location, and (optionally) the products.</span></span> <span data-ttu-id="55072-110">ตัวอย่างเช่น ใบสั่งซื้อสำหรับผลิตภัณฑ์ *A0001* จะต้องได้รับในสถานที่ *RECV* ในคลังสินค้า *24*</span><span class="sxs-lookup"><span data-stu-id="55072-110">For example, a purchase order for product *A0001* must be received in location *RECV* in warehouse *24*.</span></span> <span data-ttu-id="55072-111">หลังจากนั้น ผลิตภัณฑ์จะถูกบริโภคในกระบวนการอื่นที่สถานที่ *RECV*</span><span class="sxs-lookup"><span data-stu-id="55072-111">Later, the product is consumed in another process at location *RECV*.</span></span> <span data-ttu-id="55072-112">ในกรณีนี้ คุณสามารถตั้งค่านโยบายงานเพื่อป้องกันไม่ให้มีการสร้างงานการสำรองสินค้า เมื่อผู้ปฏิบัติงานรายงานผลิตภัณฑ์ *A0001* เป็นได้รับในสถานที่ *RECV*</span><span class="sxs-lookup"><span data-stu-id="55072-112">In this case, you can set up a work policy to prevent putaway work from being created when a worker reports product *A0001* as received in location *RECV*.</span></span>

> [!NOTE]
> - <span data-ttu-id="55072-113">สำหรับนโยบายงานที่จะเปิดใช้งาน คุณต้องกำหนดสถานที่อย่างน้อยหนึ่งแห่งสำหรับนโยบายงานบนแท็บด่วน **สถานที่เก็บสินค้าคงคลัง** ของหน้า **นโยบายงาน**</span><span class="sxs-lookup"><span data-stu-id="55072-113">For a work policy to be active, you must define at least one location for it on the **Inventory locations** FastTab of the **Work policies** page.</span></span> 
> - <span data-ttu-id="55072-114">คุณไม่สามารถระบุสถานที่เดียวกันสำหรับนโยบายของงานหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="55072-114">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="55072-115">ตัวเลือก **พิมพ์ป้ายชื่อ** สำหรับรายการเมนูของอุปกรณ์เคลื่อนที่จะไม่พิมพ์ป้ายชื่อทะเบียนถ้าไม่มีการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="55072-115">The **Print label** option for mobile device menu items won't print a license plate label unless work was created.</span></span>

## <a name="activate-the-features-in-your-system"></a><span data-ttu-id="55072-116">เปิดใช้งานลักษณะการทำงานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="55072-116">Activate the features in your system</span></span>

<span data-ttu-id="55072-117">เมื่อต้องการทำให้ฟังก์ชันทั้งหมดที่อธิบายไว้ในหัวข้อนี้พร้อมใช้งานในระบบของคุณ ให้เปิดคุณลักษณะสองอย่างต่อไปนี้ใน [การจัดการลักษณะการทำงาน](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span><span class="sxs-lookup"><span data-stu-id="55072-117">To make all the functionality that is described in this topic available in your system, turn on the following two features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="55072-118">การปรับปรุงการรับป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="55072-118">License plate receiving enhancements</span></span>
- <span data-ttu-id="55072-119">การปรับปรุงนโยบายงานสำหรับงานขาเข้า</span><span class="sxs-lookup"><span data-stu-id="55072-119">Work policy enhancements for inbound work</span></span>

## <a name="the-work-policies-page"></a><span data-ttu-id="55072-120">หน้านโยบายงาน</span><span class="sxs-lookup"><span data-stu-id="55072-120">The Work policies page</span></span>

<span data-ttu-id="55072-121">เมื่อต้องการตั้งค่านโยบายงาน ให้ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> นโยบายงาน**</span><span class="sxs-lookup"><span data-stu-id="55072-121">To set up work policies, go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span> <span data-ttu-id="55072-122">จากนั้น บนแท็บด่วนแต่ละแท็บ ให้ตั้งค่าฟิลด์ตามที่อธิบายไว้ในส่วนย่อยต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="55072-122">Then, on each FastTab, set the fields as described in the following subsections.</span></span>

### <a name="the-work-order-types-fasttab"></a><span data-ttu-id="55072-123">แท็บด่วน ชนิดของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="55072-123">The Work order types FastTab</span></span>

<span data-ttu-id="55072-124">บนแท็บด่วน **ชนิดของใบสั่งงาน** ให้เพิ่มชนิดของใบสั่งงานทั้งหมด และกระบวนการทำงานที่เกี่ยวข้อง ที่นโยบายงานใช้</span><span class="sxs-lookup"><span data-stu-id="55072-124">On the **Work order types** FastTab, add all the work order types, and the related work processes, that the work policy applies to.</span></span> <span data-ttu-id="55072-125">ชนิดของใบสั่งงานและกระบวนการทำงานที่เกี่ยวข้องต่อไปนี้ได้รับการสนับสนุนสำหรับนโยบายงาน</span><span class="sxs-lookup"><span data-stu-id="55072-125">The following work order types and related work processes are supported for work policies.</span></span>

| <span data-ttu-id="55072-126">ชนิดใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="55072-126">Work order type</span></span> | <span data-ttu-id="55072-127">กระบวนการงาน</span><span class="sxs-lookup"><span data-stu-id="55072-127">Work process</span></span> |
|---|---|
| <span data-ttu-id="55072-128">การเบิกวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="55072-128">Raw material picking</span></span>| <span data-ttu-id="55072-129">กระบวนการที่เกี่ยวข้องทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="55072-129">All related processes</span></span> |
| <span data-ttu-id="55072-130">การสำรองผลิตภัณฑ์ร่วมและสินค้าพลอยได้</span><span class="sxs-lookup"><span data-stu-id="55072-130">Co-product and by-product put away</span></span> | <span data-ttu-id="55072-131">กระบวนการที่เกี่ยวข้องทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="55072-131">All related processes</span></span> |
| <span data-ttu-id="55072-132">การสำรองสินค้าที่สำเร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="55072-132">Finished goods putaway</span></span> | <span data-ttu-id="55072-133">กระบวนการที่เกี่ยวข้องทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="55072-133">All related processes</span></span> |
| <span data-ttu-id="55072-134">การรับสินค้าสินค้าโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="55072-134">Transfer receipt</span></span> | <span data-ttu-id="55072-135">การรับป้ายทะเบียน (และการสำรองสินค้า)</span><span class="sxs-lookup"><span data-stu-id="55072-135">License plate receiving (and putaway)</span></span> |
| <span data-ttu-id="55072-136">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="55072-136">Purchase orders</span></span> | <ul><li><span data-ttu-id="55072-137">การรับป้ายทะเบียน (และการสำรองสินค้า)</span><span class="sxs-lookup"><span data-stu-id="55072-137">License plate receiving (and putaway)</span></span></li><li><span data-ttu-id="55072-138">การรับสินค้าของจำนวนงานในศูนย์การผลิต (และการสำรองสินค้า)</span><span class="sxs-lookup"><span data-stu-id="55072-138">Load item receiving (and putaway)</span></span></li><li><span data-ttu-id="55072-139">การรับรายการใบสั่งซื้อ (และการสำรองสินค้า)</span><span class="sxs-lookup"><span data-stu-id="55072-139">Purchase order line receiving (and putaway)</span></span></li><li><span data-ttu-id="55072-140">การรับสินค้าตามใบสั่งซื้อ (และการสำรองสินค้า)</span><span class="sxs-lookup"><span data-stu-id="55072-140">Purchase order item receiving (and putaway)</span></span></li></ul> |

<span data-ttu-id="55072-141">เมื่อต้องการตั้งค่านโยบายงานเพื่อให้มีผลบังคับใช้กับกระบวนการงานต่างๆ ของชนิดใบสั่งงานเดียวกัน ให้เพิ่มบรรทัดแยกต่างหากสำหรับแต่ละกระบวนงานให้กับกริด</span><span class="sxs-lookup"><span data-stu-id="55072-141">To set up a work policy so that it applies to several work processes of the same work order type, add a separate line for each work process to the grid.</span></span>

<span data-ttu-id="55072-142">สำหรับแต่ละบรรทัดในกริด ให้กำหนดฟิลด์ **วิธีการสร้างงาน** เป็นค่าใดค่าหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="55072-142">For each line in the grid, set the **Work creation method** field to one of the following values:</span></span>

- <span data-ttu-id="55072-143">**ไม่เคย** – นโยบายงานจะป้องกันไม่ให้มีการสร้างงานของคลังสินค้าสำหรับชนิดลำดับงานที่เลือกและกระบวนการทำงานที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="55072-143">**Never** – The work policy will prevent warehouse work from being created for the selected work order type and related work process.</span></span>
- <span data-ttu-id="55072-144">**การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า** – นโยบายงานจะสร้างการสร้างงานการจัดส่งโดยใช้นโยบายที่คุณเลือกในฟิลด์ **ชื่อนโยบายการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า**</span><span class="sxs-lookup"><span data-stu-id="55072-144">**Cross docking** – The work policy will create cross-docking work by using the policy that you select in the **Cross docking policy name** field.</span></span>

### <a name="the-inventory-locations-fasttab"></a><span data-ttu-id="55072-145">แท็บด่วน สถานที่เก็บสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="55072-145">The Inventory locations FastTab</span></span>

<span data-ttu-id="55072-146">บนแท็บด่วน **สถานที่เก็บสินค้าคงคลัง** ให้เพิ่มสถานที่ทั้งหมดที่ควรใช้นโยบายงานนี้</span><span class="sxs-lookup"><span data-stu-id="55072-146">On the **Inventory locations** FastTab, add all the locations where this work policy should be applied.</span></span> <span data-ttu-id="55072-147">ถ้าไม่มีสถานที่ที่เชื่อมโยงกับนโยบายงาน นโยบายงานจะไม่ใช้กับกระบวนการใดๆ</span><span class="sxs-lookup"><span data-stu-id="55072-147">If no location is associated with a work policy, the work policy won't be applied to any process.</span></span>

<span data-ttu-id="55072-148">คุณไม่สามารถระบุสถานที่เดียวกันสำหรับนโยบายของงานหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="55072-148">You can't specify the same location for multiple work policies.</span></span>

<span data-ttu-id="55072-149">คุณสามารถใช้ที่ตั้งคลังสินค้าที่กำหนดให้กับโพรไฟล์สถานที่ได้ เมื่อปิดใช้งานตัวเลือก **ใช้การติดตามป้ายทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="55072-149">You can use a warehouse location that is assigned to a location profile where the **Use license plate tracking** option is turned off.</span></span> <span data-ttu-id="55072-150">ในกรณีนี้ ผู้ปฏิบัติงานจะลงทะเบียนปริมาณคงคลังคงเหลือโดยตรง</span><span class="sxs-lookup"><span data-stu-id="55072-150">In this case, workers will directly register the on-hand inventory.</span></span>

### <a name="the-products-fasttab"></a><span data-ttu-id="55072-151">แท็บด่วน ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="55072-151">The Products FastTab</span></span>

<span data-ttu-id="55072-152">บนแท็บ **ผลิตภัณฑ์** ให้ตั้งค่าฟิลด์ **การเลือกผลิตภัณฑ์** เพื่อควบคุมผลิตภัณฑ์ที่ควรใช้กับนโยบาย:</span><span class="sxs-lookup"><span data-stu-id="55072-152">On the **Products** tab, set the **Product selection** field to control which products the policy should apply to:</span></span>

- <span data-ttu-id="55072-153">**ทั้งหมด** – นโยบายควรใช้กับผลิตภัณฑ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="55072-153">**All** – The policy should apply to all products.</span></span>
- <span data-ttu-id="55072-154">**ที่เลือก** – นโยบายควรใช้กับผลิตภัณฑ์ที่มีอยู่ในกริดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="55072-154">**Selected** – The policy should apply only to products that are listed in the grid.</span></span> <span data-ttu-id="55072-155">ใช้แถบเครื่องมือบนแท็บด่วน **ผลิตภัณฑ์** เพื่อเพิ่มผลิตภัณฑ์ลงในกริดหรือลบผลิตภัณฑ์ออกจากกริด</span><span class="sxs-lookup"><span data-stu-id="55072-155">Use the toolbar on the **Products** FastTab to add products to the grid or remove them from the grid.</span></span>

## <a name="default-and-custom-to-locations"></a><span data-ttu-id="55072-156">สถานที่ "ปลายทาง" แบบเริ่มต้นและกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="55072-156">Default and custom "to" locations</span></span>

> [!NOTE]
> <span data-ttu-id="55072-157">เมื่อต้องการทำให้ฟังก์ชันที่อธิบายไว้ในส่วนนี้พร้อมใช้งานในระบบของคุณ คุณต้องเปิดใช้งานลักษณะการทำงาน *การปรับปรุงการรับป้ายทะเบียนสำหรับแอปคลังสินค้า* และ *การปรับปรุงนโยบายงานสำหรับงานขาเข้า* ใน [การจัดการลักษณะการทำงาน](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="55072-157">To make the functionality that is described in this section available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="55072-158">ก่อนหน้านี้ ระบบสนับสนุนการรับเฉพาะที่ที่ตั้งเริ่มต้นที่ถูกกำหนดไว้สำหรับคลังสินค้าแต่ละแห่งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="55072-158">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="55072-159">อย่างไรก็ตาม รายการเมนูบนอุปกรณ์เคลื่อนที่ที่ใช้กระบวนการสร้างงานต่อไปนี้จะให้ตัวเลือก **ใช้ข้อมูลเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="55072-159">However, mobile device menu items that use the following work creation processes now provide the **Use default data** option.</span></span> <span data-ttu-id="55072-160">ตัวเลือกนี้ช่วยให้คุณสามารถกำหนดสถานที่ "ปลายทาง" แบบกำหนดเองไปยังรายการเมนูอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="55072-160">This option lets you assign a custom "to" location to one or more menu items.</span></span> <span data-ttu-id="55072-161">(ตัวเลือกนี้พร้อมใช้งานอยู่แล้วสำหรับรายการเมนูชนิดอื่น)</span><span class="sxs-lookup"><span data-stu-id="55072-161">(This option was already available for some other types of menu items.)</span></span>

- <span data-ttu-id="55072-162">การรับป้ายทะเบียน (และการสำรองสินค้า)</span><span class="sxs-lookup"><span data-stu-id="55072-162">License plate receiving (and putaway)</span></span>
- <span data-ttu-id="55072-163">การรับสินค้าของจำนวนงานในศูนย์การผลิต (และการสำรองสินค้า)</span><span class="sxs-lookup"><span data-stu-id="55072-163">Load item receiving (and putaway)</span></span>
- <span data-ttu-id="55072-164">การรับรายการใบสั่งซื้อ (และการสำรองสินค้า)</span><span class="sxs-lookup"><span data-stu-id="55072-164">Purchase order line receiving (and putaway)</span></span>
- <span data-ttu-id="55072-165">การรับสินค้าตามใบสั่งซื้อ (และการสำรองสินค้า)</span><span class="sxs-lookup"><span data-stu-id="55072-165">Purchase order item receiving (and putaway)</span></span>

<span data-ttu-id="55072-166">การตั้งค่า **สถานที่ปลายทาง** สำหรับรายการเมนูจะแทนที่สถานที่รับสินค้าเริ่มต้นสำหรับคลังสินค้า สำหรับใบสั่งทั้งหมดที่ประมวลผลโดยใช้รายการเมนูดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="55072-166">The **To location** setting for a menu item overrides the default receiving location for the warehouse, for all orders that are processed by using that menu item.</span></span>

<span data-ttu-id="55072-167">เมื่อต้องการตั้งค่ารายการเมนูของอุปกรณ์เคลื่อนที่เพื่อสนับสนุนการรับสินค้าในสถานที่ที่กำหนดเอง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="55072-167">To set up a mobile device menu item to support receiving at a custom location, follow these steps.</span></span>

1. <span data-ttu-id="55072-168">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="55072-168">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="55072-169">เลือกหรือสร้างรายการเมนูที่ใช้กระบวนการสร้างงานอย่างใดอย่างหนึ่งซึ่งแสดงไว้ก่อนหน้านี้ในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="55072-169">Select or create a menu item that uses one of the work creation processes that are listed earlier in this section.</span></span>
1. <span data-ttu-id="55072-170">บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าตัวเลือก **ใช้ข้อมูลเริ่มต้น** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="55072-170">On the **General** FastTab, set the **Use default data** option to **Yes**.</span></span>
1. <span data-ttu-id="55072-171">ในบานหน้าต่างการดำเนินการ เลือก **ข้อมูลเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="55072-171">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="55072-172">บนหน้า **ข้อมูลเริ่มต้น** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="55072-172">On the **Default data** page, set the following values:</span></span>

    - <span data-ttu-id="55072-173">**ฟิลด์ข้อมูลเริ่มต้น:** ตั้งค่าฟิลด์นี้เป็น *สถานที่ปลายทาง*</span><span class="sxs-lookup"><span data-stu-id="55072-173">**Default data field:** Set this field to *To location*.</span></span>
    - <span data-ttu-id="55072-174">**คลังสินค้า:** เลือกคลังสินค้าปลายทางที่จะใช้กับรายการเมนูนี้</span><span class="sxs-lookup"><span data-stu-id="55072-174">**Warehouse:** Select the destination warehouse to use with this menu item.</span></span>
    - <span data-ttu-id="55072-175">**สถานที่:** ฟิลด์นี้แสดงรายการรหัสสถานที่ทั้งหมดที่พร้อมใช้งานสำหรับคลังสินค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="55072-175">**Location:** This field lists all the location IDs that are available for the selected warehouse.</span></span> <span data-ttu-id="55072-176">อย่างไรก็ตาม การตั้งค่าของฟิลด์นี้ไม่มีผลใดๆ</span><span class="sxs-lookup"><span data-stu-id="55072-176">However, the setting of this field doesn't actually have any effect.</span></span> <span data-ttu-id="55072-177">ดังนั้น คุณสามารถปล่อยให้ว่างได้</span><span class="sxs-lookup"><span data-stu-id="55072-177">Therefore, you can leave it blank.</span></span> <span data-ttu-id="55072-178">อย่างไรก็ตาม คุณสามารถใช้รายการเพื่อยืนยันรหัสที่คุณต้องป้อนในฟิลด์ **ค่าที่มีรหัสแบบตายตัว**</span><span class="sxs-lookup"><span data-stu-id="55072-178">Nevertheless, you can use the list to confirm the ID that you must enter in the **Hardcoded value** field.</span></span>
    - <span data-ttu-id="55072-179">**ค่าที่มีรหัสแบบตายตัว:** ป้อนรหัสสถานที่สำหรับสถานที่รับสินค้าที่ใช้กับรายการเมนูนี้</span><span class="sxs-lookup"><span data-stu-id="55072-179">**Hardcoded value:** Enter the location ID for the receiving location that applies to this menu item.</span></span>

> [!TIP]
> <span data-ttu-id="55072-180">คุณสามารถใช้นโยบายงานได้ก็ต่อเมื่อสถานที่รับสินค้าทั้งหมดแสดงอยู่ในการตั้งค่านโยบายงานที่เกี่ยวข้องเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="55072-180">A work policy can be applied only if all the receiving locations are listed in the relevant work policy setup.</span></span> <span data-ttu-id="55072-181">ข้อกำหนดนี้ใช้โดยไม่คำนึงว่าคุณกำลังใช้สถานที่รับสินค้าเริ่มต้นหรือสถานที่ "ปลายทาง" แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="55072-181">This requirement applies regardless of whether you're using the default warehouse receiving location or a custom "to" location.</span></span>

## <a name="example-scenario-warehouse-receiving"></a><span data-ttu-id="55072-182">ตัวอย่างสถานการณ์จำลอง: การรับของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="55072-182">Example scenario: Warehouse receiving</span></span>

<span data-ttu-id="55072-183">ผลิตภัณฑ์ทั้งหมดที่ได้รับโดยกระบวนการ *การรับสินค้าตามใบสั่งซื้อ (และการสำรองสินค้า)* ต้องลงทะเบียนในสถานที่ *FL-001* และต้องมีอยู่ในคลังสินค้า *24*</span><span class="sxs-lookup"><span data-stu-id="55072-183">All products that are received by the *Purchase order item receiving (and putaway)* process must be registered in location *FL-001*, and they must be available in warehouse *24*.</span></span> <span data-ttu-id="55072-184">อย่างไรก็ตาม งานไม่ควรถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="55072-184">However, work should not be created.</span></span> <span data-ttu-id="55072-185">ผลิตภัณฑ์ที่ได้รับโดยกระบวนการอื่นๆ (นั่นคือ โดยการใช้รายการเมนูของอุปกรณ์เคลื่อนที่อื่นๆ) ควรมีการลงทะเบียนที่สถานที่รับสินค้าเริ่มต้น (*RECV*) และควรสร้างงานตามปกติ</span><span class="sxs-lookup"><span data-stu-id="55072-185">Products that are received by any other process (that is, by using other mobile device menu items) should be registered at the default warehouse receiving location (*RECV*), and work should be created as usual.</span></span> <span data-ttu-id="55072-186">(สถานการณ์จำลองนี้ไม่แสดงการตั้งค่าการรับสินค้าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="55072-186">(This scenario doesn't show the default receiving setup.)</span></span>

<span data-ttu-id="55072-187">สถานการณ์จำลองนี้จำเป็นต้องมีองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="55072-187">This scenario requires the following elements:</span></span>

- <span data-ttu-id="55072-188">นโยบายงานสำหรับกระบวนการ *การรับสินค้าของใบสั่งซื้อ (และการสำรองสินค้า)* ในสถานที่ *FL-001* สำหรับผลิตภัณฑ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="55072-188">A work policy for the *Purchase order item receiving (and putaway)* process in location *FL-001*, for all products</span></span>
- <span data-ttu-id="55072-189">รายการเมนูของอุปกรณ์เคลื่อนที่ที่มีข้อมูลเริ่มต้น และตั้งค่าฟิลด์ **สถานที่ปลายทาง** เป็น *FL-001*</span><span class="sxs-lookup"><span data-stu-id="55072-189">A mobile device menu item that has default data, and that sets the **To location** field to *FL-001*</span></span>

### <a name="prerequisites"></a><span data-ttu-id="55072-190">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="55072-190">Prerequisites</span></span>

<span data-ttu-id="55072-191">เมื่อต้องการทำให้ฟังก์ชันที่อธิบายไว้ในสถานการณ์นี้พร้อมใช้งานในระบบของคุณ คุณต้องเปิดใช้งานลักษณะการทำงาน *การปรับปรุงการรับป้ายทะเบียนสำหรับแอปคลังสินค้า* และ *การปรับปรุงนโยบายงานสำหรับงานขาเข้า* ใน [การจัดการลักษณะการทำงาน](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="55072-191">To make the functionality that is described in this scenario available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="55072-192">สถานการณ์นี้ใช้ข้อมูลสาธิตมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="55072-192">This scenario uses the standard demo data.</span></span> <span data-ttu-id="55072-193">ดังนั้น หากคุณต้องการดำเนินการโดยใช้ค่าที่แสดงที่นี่ คุณต้องทำงานในระบบที่มีการติดตั้งข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="55072-193">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="55072-194">นอกจากนี้ คุณต้องเลือกนิติบุคคล **USMF**</span><span class="sxs-lookup"><span data-stu-id="55072-194">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-work-policy"></a><span data-ttu-id="55072-195">ตั้งค่านโยบายงาน</span><span class="sxs-lookup"><span data-stu-id="55072-195">Set up a work policy</span></span>

1. <span data-ttu-id="55072-196">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> นโยบายงาน**</span><span class="sxs-lookup"><span data-stu-id="55072-196">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="55072-197">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="55072-197">Select **New**.</span></span>
1. <span data-ttu-id="55072-198">ในฟิลด์ **ชื่อนโยบายงาน** ให้ป้อน *ไม่มีงานการสำรองสินค้าที่ซื้อ*</span><span class="sxs-lookup"><span data-stu-id="55072-198">In the **Work policy name** field, enter *No purchase item putaway work*.</span></span>
1. <span data-ttu-id="55072-199">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="55072-199">Select **Save**.</span></span>
1. <span data-ttu-id="55072-200">บนแท็บด่วน **ชนิดของใบสั่งงาน** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถวไปยังกริด แล้วตั้งค่าต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="55072-200">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="55072-201">**ชนิดของใบสั่งงาน:** *ใบสั่งซื้อ*</span><span class="sxs-lookup"><span data-stu-id="55072-201">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="55072-202">**กระบวนการของงาน:** *การรับสินค้าใบสั่งซื้อ (และการสำรองสินค้า)*</span><span class="sxs-lookup"><span data-stu-id="55072-202">**Work process:** *Purchase order item receiving (and putaway)*</span></span>
    - <span data-ttu-id="55072-203">**วิธีการสร้างงาน:** *ไม่ต้อง*</span><span class="sxs-lookup"><span data-stu-id="55072-203">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="55072-204">**ชื่อนโยบายการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="55072-204">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="55072-205">บนแท็บด่วน **สถานที่เก็บสินค้าคงคลัง** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถวไปยังกริด แล้วตั้งค่าต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="55072-205">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="55072-206">**คลังสินค้า:** *24*</span><span class="sxs-lookup"><span data-stu-id="55072-206">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="55072-207">**สถานที่:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="55072-207">**Location:** *FL-001*</span></span>

1. <span data-ttu-id="55072-208">บนแท็บด่วน **ผลิตภัณฑ์** ให้ตั้งค่าฟิลด์ **การเลือกผลิตภัณฑ์** เป็น *ทั้งหมด*</span><span class="sxs-lookup"><span data-stu-id="55072-208">On the **Products** FastTab, set the **Product selection** field to *All*.</span></span>
1. <span data-ttu-id="55072-209">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="55072-209">Select **Save**.</span></span>

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a><span data-ttu-id="55072-210">ตั้งค่ารายการเมนูของอุปกรณ์เคลื่อนที่เพื่อเปลี่ยนสถานที่รับสินค้า</span><span class="sxs-lookup"><span data-stu-id="55072-210">Set up a mobile device menu item to change the receiving location</span></span>

1. <span data-ttu-id="55072-211">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="55072-211">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="55072-212">ในบานหน้าต่างด้านซ้าย ให้เลือกรายการเมนู **รับสินค้า** ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="55072-212">In the left pane, select the existing **Purchase receive** menu item.</span></span>
1. <span data-ttu-id="55072-213">บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าตัวเลือก **ใช้ข้อมูลเริ่มต้น** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="55072-213">On the **General** FastTab, set the **Use default data** option to *Yes*.</span></span>
1. <span data-ttu-id="55072-214">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="55072-214">Select **Save**.</span></span>
1. <span data-ttu-id="55072-215">ในบานหน้าต่างการดำเนินการ เลือก **ข้อมูลเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="55072-215">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="55072-216">บนหน้า **ข้อมูลเริ่มต้น** บนบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด แล้วตั้งค่าต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="55072-216">On the **Default data** page, on the Action Pane, select **New** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="55072-217">**ฟิลด์ข้อมูลเริ่มต้น:** *สถานที่ปลายทาง*</span><span class="sxs-lookup"><span data-stu-id="55072-217">**Default data field:** *To location*</span></span>
    - <span data-ttu-id="55072-218">**คลังสินค้า:** *24*</span><span class="sxs-lookup"><span data-stu-id="55072-218">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="55072-219">**สถานที่:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="55072-219">**Location:** Leave this field blank.</span></span>
    - <span data-ttu-id="55072-220">**ค่าที่มีรหัสแบบตายตัว:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="55072-220">**Hardcoded value:** *FL-001*</span></span>

1. <span data-ttu-id="55072-221">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="55072-221">Select **Save**.</span></span>

### <a name="receive-a-purchase-order-without-creating-work"></a><span data-ttu-id="55072-222">รับใบสั่งซื้อโดยไม่มีการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="55072-222">Receive a purchase order without creating work</span></span>

<span data-ttu-id="55072-223">ตัวอย่างในส่วนนี้แสดงวิธีการรับสินค้าในใบสั่งซื้อ แต่ไม่มีการสร้างงาน ที่สถานที่แตกต่างจากสถานที่รับสินค้าเริ่มต้นที่ตั้งค่าไว้สำหรับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="55072-223">The example in this section shows how to receive a purchase order item, but without creating work, at a location that differs from the default receiving location that is set up for the warehouse.</span></span> <span data-ttu-id="55072-224">ตัวอย่างนี้ใช้นโยบายงานและสินค้าบนอุปกรณ์เคลื่อนที่ที่คุณสร้างไว้ก่อนหน้านี้ในสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="55072-224">This example uses the work policy and mobile device item that you created earlier in this scenario.</span></span>

#### <a name="create-a-purchase-order"></a><span data-ttu-id="55072-225">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="55072-225">Create a purchase order</span></span>

1. <span data-ttu-id="55072-226">ไปที่ **การจัดซื้อและการจัดหา \> ใบสั่งซื้อ \> ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="55072-226">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="55072-227">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="55072-227">Select **New**.</span></span>
1. <span data-ttu-id="55072-228">ในกล่องโต้ตอบ **สร้างใบสั่งซื้อ** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="55072-228">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="55072-229">**บัญชีผู้จัดจำหน่าย:** *US-101*</span><span class="sxs-lookup"><span data-stu-id="55072-229">**Vendor account:** *US-101*</span></span>
    - <span data-ttu-id="55072-230">**ไซต์:** *2*</span><span class="sxs-lookup"><span data-stu-id="55072-230">**Site:** *2*</span></span>
    - <span data-ttu-id="55072-231">**คลังสินค้า:** *24*</span><span class="sxs-lookup"><span data-stu-id="55072-231">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="55072-232">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบและเปิดใบสั่งซื้อใหม่</span><span class="sxs-lookup"><span data-stu-id="55072-232">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="55072-233">บนแท็บด่วน **บรรทัดใบสั่งซื้อ** ให้ตั้งค่าต่อไปนี้สำหรับแถวที่ว่างเปล่า:</span><span class="sxs-lookup"><span data-stu-id="55072-233">On the **Purchase order lines** FastTab, set the following values for the empty row:</span></span>

    - <span data-ttu-id="55072-234">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="55072-234">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="55072-235">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="55072-235">**Quantity:** *1*</span></span>

1. <span data-ttu-id="55072-236">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="55072-236">Select **Save**.</span></span>
1. <span data-ttu-id="55072-237">สร้างบันทึกย่อของหมายเลขใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="55072-237">Make a note of the purchase order number.</span></span>

#### <a name="receive-a-purchase-order"></a><span data-ttu-id="55072-238">รับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="55072-238">Receive a purchase order</span></span>

1. <span data-ttu-id="55072-239">บนอุปกรณ์เคลื่อนที่ ลงชื่อเข้าใช้คลังสินค้า *24* โดยใช้ *24* เป็นรหัสผู้ใช้ และ *1* เป็นรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="55072-239">On the mobile device, sign in to warehouse *24* by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="55072-240">เลือก **ขาเข้า**</span><span class="sxs-lookup"><span data-stu-id="55072-240">Select **Inbound**.</span></span>
1. <span data-ttu-id="55072-241">เลือก **รับการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="55072-241">Select **Purchase receive**.</span></span> <span data-ttu-id="55072-242">ฟิลด์ **สถานที่** ควรตั้งค่าเป็น *FL-001*</span><span class="sxs-lookup"><span data-stu-id="55072-242">The **Location** field should be set to *FL-001*.</span></span>
1. <span data-ttu-id="55072-243">ป้อนหมายเลขใบสั่งซื้อสำหรับใบสั่งซื้อที่คุณสร้างขึ้นในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="55072-243">Enter the purchase order number for the purchase order that you created in the previous procedure.</span></span>
1. <span data-ttu-id="55072-244">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อน *A0001*</span><span class="sxs-lookup"><span data-stu-id="55072-244">In the **Item number** field, enter *A0001*.</span></span>
1. <span data-ttu-id="55072-245">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="55072-245">Select **OK**.</span></span>
1. <span data-ttu-id="55072-246">ในฟิลด์ **ปริมาณ** ให้ป้อน *1*</span><span class="sxs-lookup"><span data-stu-id="55072-246">In the **Quantity** field, enter *1*.</span></span>
1. <span data-ttu-id="55072-247">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="55072-247">Select **OK**.</span></span>

<span data-ttu-id="55072-248">ตอนนี้ใบสั่งซื้อได้รับแล้ว แต่ไม่มีงานที่เชื่อมโยงอยู่</span><span class="sxs-lookup"><span data-stu-id="55072-248">The purchase order is now received, but no work is associated with it.</span></span> <span data-ttu-id="55072-249">ปริมาณคงคลังคงเหลือได้รับการปรับปรุงแล้ว และปริมาณ *1* รายการของสินค้า *A0001* พร้อมใช้งานที่สถานที่ *FL-001*</span><span class="sxs-lookup"><span data-stu-id="55072-249">The on-hand inventory has been updated, and a quantity of *1* of item *A0001* is now available at location *FL-001*.</span></span>

## <a name="example-scenario-manufacturing"></a><span data-ttu-id="55072-250">ตัวอย่างสถานการณ์จำลอง: การผลิต</span><span class="sxs-lookup"><span data-stu-id="55072-250">Example scenario: Manufacturing</span></span>

<span data-ttu-id="55072-251">ในตัวอย่างต่อไปนี้ มีใบสั่งผลิตสองรายการ คือ *PRD-001* และ *PRD-002*</span><span class="sxs-lookup"><span data-stu-id="55072-251">In the following example, there are two production orders, *PRD-001* and *PRD-002*.</span></span> <span data-ttu-id="55072-252">ใบสั่งผลิต *PRD-001* มีการดำเนินการที่มีชื่อว่า *การประกอบ* โดยที่ผลิตภัณฑ์ *SC1* ถูกรายงานเมื่อเสร็จสมบูรณ์ไปยังสถานที่ *001*</span><span class="sxs-lookup"><span data-stu-id="55072-252">Production order *PRD-001* has an operation that is named *Assembly*, where product *SC1* is being reported as finished to location *001*.</span></span> <span data-ttu-id="55072-253">ใบสั่งผลิต *PRD-002* มีการดำเนินการที่มีชื่อว่า *การทาสี* และใช้ผลิตภัณฑ์ *SC1* จากสถานที่ *001*</span><span class="sxs-lookup"><span data-stu-id="55072-253">Production order *PRD-002* has an operation that is named *Painting* and consumes product *SC1* from location *001*.</span></span> <span data-ttu-id="55072-254">นอกจากนี้ใบสั่งผลิต *PRD-002* ก็ใช้วัตถุดิบ *RM1* จากสถานที่ *001* เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="55072-254">Production order *PRD-002* also consumes raw material *RM1* from location *001*.</span></span> <span data-ttu-id="55072-255">วัตถุดิบ *RM1* ถูกจัดเก็บในสถานที่เก็บคลังสินค้า *BULK-001* และจะถูกเบิกสินค้าไปยังสถานที่ *001* โดยงานของคลังสินค้าสำหรับการเบิกสินค้าวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="55072-255">Raw material *RM1* is stored in warehouse location *BULK-001* and will be picked to location *001* by warehouse work for raw material picking.</span></span> <span data-ttu-id="55072-256">มีการสร้างงานการเบิกสินค้าเมื่อการผลิต *PRD-002* ถูกนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="55072-256">The picking work is generated when production *PRD-002* is released.</span></span>

<span data-ttu-id="55072-257">[![นโยบายงานของคลังสินค้า](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="55072-257">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span>

<span data-ttu-id="55072-258">เมื่อคุณกำลังวางแผนที่จะตั้งค่าคอนฟิกนโยบายงานของคลังสินค้าสำหรับสถานการณ์จำลองนี้ คุณควรพิจารณาประเด็นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="55072-258">When you're planning to configure a warehouse work policy for this scenario, you should consider the following points:</span></span>

- <span data-ttu-id="55072-259">งานของคลังสินค้าสำหรับการสำรองสินค้าที่สำเร็จแล้วไม่จำเป็นเมื่อคุณรายงานผลิตภัณฑ์ *SC1* เมื่อเสร็จสมบูรณ์จากใบสั่งผลิต *PRD-001* ไปยังสถานที่ *001*</span><span class="sxs-lookup"><span data-stu-id="55072-259">Warehouse work for putaway of finished goods isn't required when you report product *SC1* as finished from production order *PRD-001* to location *001*.</span></span> <span data-ttu-id="55072-260">เหตุผลที่การดำเนินงาน *การทาสี* สำหรับใบสั่งผลิต *PRD-002* ใช้ผลิตภัณฑ์ *SC1* ที่สถานที่เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="55072-260">The reason is that the *Painting* operation for production order *PRD-002* consumes product *SC1* at the same location.</span></span>
- <span data-ttu-id="55072-261">งานของคลังสินค้าสำหรับการเบิกสินค้าวัตถุดิบจำเป็นในการย้ายวัตถุดิบ *RM1* จากสถานที่เก็บคลังสินค้า *BULK-001* ไปยังสถานที่ *001*</span><span class="sxs-lookup"><span data-stu-id="55072-261">Warehouse work for raw material picking is required to move raw material *RM1* from warehouse location *BULK-001* to location *001*.</span></span>

<span data-ttu-id="55072-262">นี่คือตัวอย่างของนโยบายงานที่คุณสามารถตั้งค่าได้ตามข้อควรพิจารณาเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="55072-262">Here is an example of a work policy that you can set up, based on these considerations:</span></span>

- <span data-ttu-id="55072-263">**ชื่อนโยบายงาน:** *ไม่มีงานการสำรองสินค้า*</span><span class="sxs-lookup"><span data-stu-id="55072-263">**Work policy name:** *No putaway work*</span></span>
- <span data-ttu-id="55072-264">**ชนิดของใบสั่งงาน:** *การสำรองสินค้าที่สำเร็จแล้ว* และ *การสำรองผลิตภัณฑ์ร่วมและสินค้าพลอยได้*</span><span class="sxs-lookup"><span data-stu-id="55072-264">**Work order types:** *Finished goods put away* and *Co-product and by-product put away*</span></span>
- <span data-ttu-id="55072-265">**สถานที่เก็บสินค้าคงคลัง:** คลังสินค้า *51* และสถานที่ *001*</span><span class="sxs-lookup"><span data-stu-id="55072-265">**Inventory locations:** Warehouse *51* and location *001*</span></span>
- <span data-ttu-id="55072-266">**ผลิตภัณฑ์:** *SC1*</span><span class="sxs-lookup"><span data-stu-id="55072-266">**Products:** *SC1*</span></span>

<span data-ttu-id="55072-267">สถานการณ์ตัวอย่างต่อไปนี้ให้คำแนะนำทีละขั้นตอนสำหรับการตั้งค่านโยบายงานของคลังสินค้าสำหรับสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="55072-267">The following example scenario provides step-by-step instructions for setting up the warehouse work policy for this scenario.</span></span>

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="55072-268">สถานการณ์ตัวอย่าง: รายงานเมื่อเสร็จสมบูรณ์ไปยังสถานที่ที่ไม่มีการควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="55072-268">Example scenario: Report as finished to a location that isn't license plate–controlled</span></span>

<span data-ttu-id="55072-269">สถานการณ์นี้แสดงตัวอย่างการรายงานใบสั่งผลิตเมื่อเสร็จสมบูรณ์ไปยังสถานที่ที่ไม่มีป้ายทะเบียนที่มีการควบคุม</span><span class="sxs-lookup"><span data-stu-id="55072-269">This scenario shows an example where a production order is reported as finished to a location that isn't license plate–controlled.</span></span>

<span data-ttu-id="55072-270">สถานการณ์นี้ใช้ข้อมูลสาธิตมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="55072-270">This scenario uses the standard demo data.</span></span> <span data-ttu-id="55072-271">ดังนั้น หากคุณต้องการดำเนินการโดยใช้ค่าที่แสดงที่นี่ คุณต้องทำงานในระบบที่มีการติดตั้งข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="55072-271">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="55072-272">นอกจากนี้ คุณต้องเลือกนิติบุคคล **USMF**</span><span class="sxs-lookup"><span data-stu-id="55072-272">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="55072-273">ตั้งค่านโยบายงานของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="55072-273">Set up a warehouse work policy</span></span>

<span data-ttu-id="55072-274">กระบวนการคลังสินค้าไม่รวมงานคลังสินค้าเสมอไป</span><span class="sxs-lookup"><span data-stu-id="55072-274">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="55072-275">โดยการกำหนดนโยบายงาน คุณสามารถป้องกันการสร้างงานสำหรับการเบิกวัตถุดิบและการสำรองสินค้าสำเร็จรูป สำหรับชุดของผลิตภัณฑ์ที่ตำแหน่งเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="55072-275">By defining a work policy, you can prevent the creation of work for raw material picking and putaway of finished goods for a set of products at specific locations.</span></span>

1. <span data-ttu-id="55072-276">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> นโยบายงาน**</span><span class="sxs-lookup"><span data-stu-id="55072-276">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="55072-277">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="55072-277">Select **New**.</span></span>
1. <span data-ttu-id="55072-278">ในฟิลด์ **ชื่อนโยบายงาน** ให้ป้อน *ไม่มีงานการสำรองสินค้า*</span><span class="sxs-lookup"><span data-stu-id="55072-278">In the **Work policy name** field, enter *No putaway work*.</span></span>
1. <span data-ttu-id="55072-279">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="55072-279">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="55072-280">บนแท็บด่วน **ชนิดของใบสั่งงาน** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถวไปยังกริด แล้วตั้งค่าต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="55072-280">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="55072-281">**ชนิดใบสั่งงาน:** *การสำรองสินค้าที่สำเร็จแล้ว*</span><span class="sxs-lookup"><span data-stu-id="55072-281">**Work order type:** *Finished goods put away*</span></span>
    - <span data-ttu-id="55072-282">**กระบวนการทำงาน:** *กระบวนการทำงานที่เกี่ยวข้องทั้งหมด*</span><span class="sxs-lookup"><span data-stu-id="55072-282">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="55072-283">**วิธีการสร้างงาน:** *ไม่ต้อง*</span><span class="sxs-lookup"><span data-stu-id="55072-283">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="55072-284">**ชื่อนโยบายการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="55072-284">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="55072-285">เลือก **เพิ่ม** อีกครั้งเพื่อเพิ่มแถวที่สองไปยังกริด แล้วตั้งค่าต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="55072-285">Select **Add** again to add a second row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="55072-286">**ชนิดของใบสั่งงาน:** *การสำรองผลิตภัณฑ์ร่วมและสินค้าพลอยได้*</span><span class="sxs-lookup"><span data-stu-id="55072-286">**Work order type:** *Co-product and by-product put away*</span></span>
    - <span data-ttu-id="55072-287">**กระบวนการทำงาน:** *กระบวนการทำงานที่เกี่ยวข้องทั้งหมด*</span><span class="sxs-lookup"><span data-stu-id="55072-287">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="55072-288">**วิธีการสร้างงาน:** *ไม่ต้อง*</span><span class="sxs-lookup"><span data-stu-id="55072-288">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="55072-289">**ชื่อนโยบายการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="55072-289">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="55072-290">บนแท็บด่วน **สถานที่เก็บสินค้าคงคลัง** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถวไปยังกริด แล้วตั้งค่าต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="55072-290">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="55072-291">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="55072-291">**Warehouse:** *51*</span></span>
    - <span data-ttu-id="55072-292">**สถานที่:** *001*</span><span class="sxs-lookup"><span data-stu-id="55072-292">**Location:** *001*</span></span>

1. <span data-ttu-id="55072-293">บนแท็บด่วน **ผลิตภัณฑ์** ให้ตั้งค่าฟิลด์ **การเลือกผลิตภัณฑ์** เป็น *ที่เลือก*</span><span class="sxs-lookup"><span data-stu-id="55072-293">On the **Products** FastTab, set the **Product selection** field to *Selected*.</span></span>
1. <span data-ttu-id="55072-294">บนแท็บด่วน **ผลิตภัณฑ์** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="55072-294">On the **Products** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="55072-295">ในแถวใหม่ ตั้งค่าฟิลด์ **หมายเลขสินค้า** เป็น *L0101*</span><span class="sxs-lookup"><span data-stu-id="55072-295">In the new row, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="55072-296">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="55072-296">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-an-output-location"></a><span data-ttu-id="55072-297">ตั้งค่าที่ตั้งเอาท์พุท</span><span class="sxs-lookup"><span data-stu-id="55072-297">Set up an output location</span></span>

1. <span data-ttu-id="55072-298">ไปที่ **การจัดการองค์กร \> ทรัพยากร \> กลุ่มทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="55072-298">Go to **Organization administration \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="55072-299">ในบานหน้าต่างด้านซ้าย ให้เลือกกลุ่มทรัพยากร **5102**</span><span class="sxs-lookup"><span data-stu-id="55072-299">In the left pane, select resource group **5102**.</span></span>
1. <span data-ttu-id="55072-300">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="55072-300">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="55072-301">**คลังสินค้าเอาพุต:** *51*</span><span class="sxs-lookup"><span data-stu-id="55072-301">**Output warehouse:** *51*</span></span>
    - <span data-ttu-id="55072-302">**สถานที่เอาพุต:** *001*</span><span class="sxs-lookup"><span data-stu-id="55072-302">**Output location:** *001*</span></span>

1. <span data-ttu-id="55072-303">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="55072-303">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="55072-304">สถานที่ *001* ไม่ใช่สถานที่ที่มีการควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="55072-304">Location *001* isn't a license plate–controlled location.</span></span> <span data-ttu-id="55072-305">คุณสามารถตั้งค่าสถานที่เอาท์พุทที่ไม่ใช่ป้ายทะเบียนที่มีการควบคุม เฉพาะเมื่อนโยบายงานมีอยู่สำหรับสถานที่</span><span class="sxs-lookup"><span data-stu-id="55072-305">You can set up an output location that isn't license plate–controlled only if an applicable work policy exists for the location.</span></span>

### <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="55072-306">สร้างใบสั่งผลิตและรายงานเป็น เสร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="55072-306">Create a production order and report it as finished</span></span>

1. <span data-ttu-id="55072-307">ไปที่ **การควบคุมการผลิต \> ใบสั่งผลิต \> ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="55072-307">Go to **Production control \> Production orders \> All production orders**.</span></span>
1. <span data-ttu-id="55072-308">ในบานหน้าต่างการดำเนินการ เลือก **ใบสั่งผลิตใหม่**</span><span class="sxs-lookup"><span data-stu-id="55072-308">On the Action Pane, select **New production order**.</span></span>
1. <span data-ttu-id="55072-309">ในกล่องโต้ตอบ **สร้างใบสั่งผลิต** ให้ตั้งค่าฟิลด์ **หมายเลขสินค้า** เป็น *L0101*</span><span class="sxs-lookup"><span data-stu-id="55072-309">In the **Create production order** dialog box, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="55072-310">เลือก **สร้าง** เพื่อสร้างใบสั่ง และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="55072-310">Select **Create** to create the order and close the dialog box.</span></span>

    <span data-ttu-id="55072-311">ใบสั่งผลิตใหม่จะเพิ่มเข้าในกริดบนหน้า **ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="55072-311">A new production order is added to the grid on the **All production orders** page.</span></span>

    <span data-ttu-id="55072-312">เก็บใบสั่งผลิตใหม่ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="55072-312">Keep the new production order selected.</span></span>

1. <span data-ttu-id="55072-313">ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งผลิต** ในกลุ่ม **กระบวนการ** ให้เลือก **การประเมิน**</span><span class="sxs-lookup"><span data-stu-id="55072-313">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**.</span></span>
1. <span data-ttu-id="55072-314">ในกล่องโต้ตอบ **การประเมิน** อ่านการประเมิน แล้วเลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="55072-314">In the **Estimate** dialog box, read the estimate, and then select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="55072-315">ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งผลิต** ในกลุ่ม **กระบวนการ** ให้เลือก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="55072-315">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**.</span></span>
1. <span data-ttu-id="55072-316">ในกล่องโต้ตอบ **เริ่มต้น** บนแท็บ **ทั่วไป** ให้ตั้งค่าฟิลด์ **ปริมาณการใช้ BOM อัตโนมัติ** เป็น *ไม่ต้อง*</span><span class="sxs-lookup"><span data-stu-id="55072-316">In the **Start** dialog box, on the **General** tab, set the **Automatic BOM consumption** field to *Never*.</span></span>
1. <span data-ttu-id="55072-317">เลือก **ตกลง** เพื่อบันทึกการตั้งค่าของคุณ และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="55072-317">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="55072-318">ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งผลิต** ในกลุ่ม **กระบวนการ** ให้เลือก **รายงานการเสร็จงาน**</span><span class="sxs-lookup"><span data-stu-id="55072-318">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Report as finished**.</span></span>
1. <span data-ttu-id="55072-319">ในกล่องโต้ตอบ **รายงานการเสร็จงาน** บนแท็บ **ทั่วไป** ให้ตั้งค่าตัวเลือก **ยอมรับข้อผิดพลาด** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="55072-319">In the **Report as finished** dialog box, on the **General** tab, set the **Accept error** option to *Yes*.</span></span>
1. <span data-ttu-id="55072-320">เลือก **ตกลง** เพื่อบันทึกการตั้งค่าของคุณ และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="55072-320">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="55072-321">บนบานหน้าต่างการดำเนินการ ในแท็บ **คลังสินค้า** ในกลุ่ม **ทั่วไป** เลือก **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="55072-321">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span>

<span data-ttu-id="55072-322">เมื่อใบสั่งผลิตถูกรายงานเป็น เสร็จแล้ว จึงไม่มีการสร้างงานสำหรับการสำรอง</span><span class="sxs-lookup"><span data-stu-id="55072-322">When the production order is reported as finished, no work is generated for putaway.</span></span> <span data-ttu-id="55072-323">ลักษณะการทำงานนี้เกิดขึ้นเนื่องจากนโยบายงานถูกกำหนดให้ป้องกันงานจากการถูกสร้าง เมื่อผลิตภัณฑ์ *L0101* ถูกรายงานเป็น เสร็จแล้ว ไปยังสถานที่ *001*</span><span class="sxs-lookup"><span data-stu-id="55072-323">This behavior occurs because a work policy is defined that prevents work from being generated when product *L0101* is reported as finished to location *001*.</span></span>

## <a name="more-information"></a><span data-ttu-id="55072-324">ข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="55072-324">More information</span></span>

<span data-ttu-id="55072-325">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการเมนูบนอุปกรณ์เคลื่อนที่ ให้ดูที่ [ตั้งค่าอุปกรณ์เคลื่อนที่สำหรับงานของคลังสินค้า](configure-mobile-devices-warehouse.md)</span><span class="sxs-lookup"><span data-stu-id="55072-325">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="55072-326">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการรับป้ายทะเบียนและนโยบายงาน ให้ดูที่ [ป้ายทะเบียนที่ได้รับผ่านทางแอปการจัดการคลังสินค้าบนมือถือ](warehousing-mobile-device-app-license-plate-receiving.md)</span><span class="sxs-lookup"><span data-stu-id="55072-326">For more information about license plate receiving and work policies, see [License plate receiving via the Warehouse Management mobile app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="55072-327">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการจำนวนงานในศูนย์การผลิตขาเข้า ให้ดูที่ [การจัดการคลังสินค้าของจำนวนงานในศูนย์การผลิตขาเข้าสำหรับใบสั่งซื้อ](inbound-load-handling.md)</span><span class="sxs-lookup"><span data-stu-id="55072-327">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]