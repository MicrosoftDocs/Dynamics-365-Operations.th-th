---
title: ค่าเผื่อความปลอดภัย
description: หัวข้อนี้จะอธิบายวิธีการใช้ค่าเผื่อความปลอดภัยกับ Add-in การเพิ่มประสิทธิภาพการวางแผนสำหรับ Microsoft Dynamics 365 Supply Chain Management
author: ChristianRytt
manager: tfehr
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4a15b1c3df5de1dc5a55cfaa08686ee85ed50ba3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236038"
---
# <a name="safety-margins"></a><span data-ttu-id="77f68-103">ค่าเผื่อความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="77f68-103">Safety margins</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77f68-104">หัวข้อนี้จะอธิบายวิธีการใช้ค่าเผื่อความปลอดภัยกับ Add-in การเพิ่มประสิทธิภาพการวางแผนสำหรับ Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="77f68-104">This topic describes how safety margins can be used with the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="safety-margins-overview"></a><span data-ttu-id="77f68-105">ภาพรวมค่าเผื่อความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="77f68-105">Safety margins overview</span></span>

<span data-ttu-id="77f68-106">วัตถุประสงค์ของค่าเผื่อความปลอดภัยคือเพื่อเปิดใช้งานการตั้งค่าที่ให้เวลาเผื่อบางส่วนนอกเหนือจากระยะเวลารอคอยสินค้าปกติ</span><span class="sxs-lookup"><span data-stu-id="77f68-106">The purpose of safety margins is to enable a setup that provides some buffer time beyond the normal lead time.</span></span> <span data-ttu-id="77f68-107">ตัวอย่างเช่น เมื่อต้องแกะหีบห่อหรือตรวจสอบวัสดุหลังมาถึงจากผู้จัดจำหน่าย คุณจะไม่สามารถเพิ่มเวลาพิเศษให้กับระยะเวลารอคอยสินค้าในการซื้อได้ เนื่องจากวิธีการนี้จะให้เวลาเผื่อเพิ่มเติมแก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="77f68-107">For example, when material must be unpacked or inspected after it arrives from the vendor, you can't just add the extra time to the purchase lead time, because this approach will give the additional buffer time to the supplier.</span></span> <span data-ttu-id="77f68-108">ในตัวอย่างนี้ ค่าเผื่อในการรับสินค้าสามารถใช้เพื่อให้มั่นใจว่าผู้จัดหาจะจัดส่งสินค้าก่อนเวลานี้</span><span class="sxs-lookup"><span data-stu-id="77f68-108">In this example, the receipt margin can be used to ensure that the supplier delivers earlier.</span></span> <span data-ttu-id="77f68-109">วิธีการนี้ให้เวลาเผื่อเพื่อให้สามารถจัดการสินค้าภายในได้</span><span class="sxs-lookup"><span data-stu-id="77f68-109">This approach provides buffer time so that the goods can be handled internally.</span></span>

<span data-ttu-id="77f68-110">มีค่าเผื่อความปลอดภัยอยู่สามชนิด:</span><span class="sxs-lookup"><span data-stu-id="77f68-110">There are three types of safety margins:</span></span>

- <span data-ttu-id="77f68-111">**ค่าเผื่อในการสั่งใหม่** – เวลาเผื่อสำหรับการวางใบสั่งการจัดหา</span><span class="sxs-lookup"><span data-stu-id="77f68-111">**Reorder margin** – The buffer time for placing the supply order</span></span>
- <span data-ttu-id="77f68-112">**ค่าเผื่อการรับสินค้า** - เวลาเผื่อสำหรับการจัดการกับการจัดหาสินค้าขาเข้า</span><span class="sxs-lookup"><span data-stu-id="77f68-112">**Receipt margin** – The buffer time for handling incoming supply</span></span>
- <span data-ttu-id="77f68-113">**ค่าเผื่อการออก** – เวลาเผื่อสำหรับการจัดการกับการจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="77f68-113">**Issue margin** – The buffer time for handling shipments</span></span>

<span data-ttu-id="77f68-114">ภาพประกอบต่อไปนี้แสดงวิธีการใช้ค่าเผื่อความปลอดภัยเหล่านี้เมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="77f68-114">The following illustration shows how these safety margins apply over time.</span></span>

![ค่าเผื่อความปลอดภัย](media/safety-margins-1.png)

<span data-ttu-id="77f68-116">มีการกำหนดค่าเผื่อทั้งหมดเป็นจำนวนวัน</span><span class="sxs-lookup"><span data-stu-id="77f68-116">All margins are defined in days.</span></span> <span data-ttu-id="77f68-117">ค่าเริ่มต้น *0* (ศูนย์) บ่งชี้ว่าไม่มีการใช้ค่าเผื่อ</span><span class="sxs-lookup"><span data-stu-id="77f68-117">The default value, *0* (zero), indicates that no margin is applied.</span></span> <span data-ttu-id="77f68-118">ถ้าคุณตั้งค่าค่าเผื่อหลายค่า ค่าทั้งหมดจะเพิ่มเข้าไปในเวลารวมจาก *วันที่ในใบสั่ง* การจัดหาถึง *วันที่ที่ต้องการ* อุปสงค์</span><span class="sxs-lookup"><span data-stu-id="77f68-118">If you set up multiple margins, they all add to the total time from the supply *order date* to the demand *requirement date*.</span></span> <span data-ttu-id="77f68-119">ตัวอย่างเช่น การตั้งค่าไม่มีระยะเวลารอคอยสินค้าและมีการตั้งค่าชนิดของค่าเผื่อทั้งสามชนิดเป็นหนึ่งวัน</span><span class="sxs-lookup"><span data-stu-id="77f68-119">For example, a setup has no lead time, and all three margin types are set to one day.</span></span> <span data-ttu-id="77f68-120">ในกรณีนี้ จะมีเวลาสามวันระหว่างวันที่ในใบสั่งการจัดหาและวันที่ที่ต้องการอุปสงค์ ดังนั้นถ้าวันที่ในใบสั่งเป็นวันที่ 1 กรกฎาคม วันที่ของความต้องการจะเป็นวันที่ 4 กรกฎาคม</span><span class="sxs-lookup"><span data-stu-id="77f68-120">In this case, there will be three days between the supply order date and the demand requirement date, so if the order date is July 1, the requirement date would be July 4.</span></span>

### <a name="receipt-margin"></a><span data-ttu-id="77f68-121">ค่าเผื่อในการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="77f68-121">Receipt margin</span></span>

<span data-ttu-id="77f68-122">ค่าเผื่อในการรับสินค้าอาจมีการใช้ค่าเผื่อความปลอดภัยสามวันมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="77f68-122">The receipt margin is probably the most used of the three safety margins.</span></span> <span data-ttu-id="77f68-123">ซึ่งใช้กับ *วันที่นำส่ง* และย้อนหลังจาก *วันที่ที่ต้องการ*</span><span class="sxs-lookup"><span data-stu-id="77f68-123">It's applied to the *delivery date* and backward from the *requirement date*.</span></span> <span data-ttu-id="77f68-124">กล่าวอีกอย่างหนึ่งคือ ผลิตภัณฑ์ควรได้รับค่าเผื่อจำนวนวันในการรับสินค้าที่ระบุไว้ก่อนที่จะต้องใช้</span><span class="sxs-lookup"><span data-stu-id="77f68-124">In other words, the products should be received the specified number of receipt margin days before they are required.</span></span>

<span data-ttu-id="77f68-125">ภาพประกอบต่อไปนี้เน้นค่าเผื่อในการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="77f68-125">The following illustration highlights the receipt margin.</span></span>

![ค่าเผื่อในการรับสินค้า](media/safety-margins-2.png)

<span data-ttu-id="77f68-127">โดยทั่วไป ค่าเผื่อในการรับสินค้าจะถูกใช้เป็นบัฟเฟอร์เพื่อให้มั่นใจถึงเวลาสำหรับการลงทะเบียนคลังสินค้าหรือกระบวนการที่ต้องใช้เวลานานอื่นๆ ที่ไม่ได้รับการบันทึกเป็นส่วนหนึ่งของระยะเวลารอคอยสินค้าทั่วไปในระบบ</span><span class="sxs-lookup"><span data-stu-id="77f68-127">The receipt margin is typically used as a buffer to ensure time for warehouse registration or other time-consuming processes that aren't captured as part of the general lead time in the system.</span></span> <span data-ttu-id="77f68-128">สำหรับการซื้อ ประโยชน์อย่างหนึ่งคือ *วันที่นำส่ง* ของใบสั่งซื้อจะถูกเลื่อนไปข้างหน้าตามนั้น</span><span class="sxs-lookup"><span data-stu-id="77f68-128">For purchases, one benefit is that the *delivery date* of the purchase order is moved forward accordingly.</span></span> <span data-ttu-id="77f68-129">ถ้าคุณเพิ่มระยะเวลารอคอยสินค้าแทนที่จะใช้ค่าเผื่อความปลอดภัย ผู้จัดจำหน่ายจะยังคงถูกขอให้นำส่งในนาทีสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="77f68-129">If you  increase the lead time instead of using a safety margin, the vendor will still be asked to deliver at the last minute.</span></span>

<span data-ttu-id="77f68-130">สังเกตว่าค่าเผื่อในการรับสินค้าไม่เปลี่ยนแปลง *วันที่ที่ต้องการ* ในการจัดหา</span><span class="sxs-lookup"><span data-stu-id="77f68-130">Notice that the receipt margin doesn't change the *requirement date* of the supply.</span></span> <span data-ttu-id="77f68-131">ดังนั้น ค่าเผื่อในการรับสินค้าจึงไม่สามารถมองเห็นได้โดยตรงเมื่อมีการเปรียบเทียบวันที่ที่ต้องการสำหรับอุปสงค์และการจัดหา (ตัวอย่างเช่น บนหน้า **ความต้องการสุทธิ**)</span><span class="sxs-lookup"><span data-stu-id="77f68-131">Therefore, the receipt margin isn't directly visible when requirement dates for demand and supply are compared (for example, on the **Net requirements** page).</span></span> <span data-ttu-id="77f68-132">ตัวอย่างเช่น ถ้าค่าเผื่อในการรับมีการตั้งค่าเป็นสี่วัน และวางแผนรายการใบสั่งซื้อสำหรับการรับสินค้าในวันที่สิบห้าของเดือน การวางแผนหลักจะคำนวณวันที่รับสินค้าที่ปรับปรุงเป็นวันที่สิบเก้าของเดือน</span><span class="sxs-lookup"><span data-stu-id="77f68-132">For example, if the receipt margin is set to four days, and a purchase order line is planned for receipt on the fifteenth of the month, master planning calculates the adjusted receipt date as the nineteenth of the month.</span></span>

<span data-ttu-id="77f68-133">โปรดทราบว่าไม่มีการใช้ค่าเผื่อในการรับสินค้าเมื่อมีการใช้ปริมาณสินค้าคงคลังคงเหลือเป็นการจัดหา</span><span class="sxs-lookup"><span data-stu-id="77f68-133">Note that a receipt margin isn't applied when on-hand inventory is used as the supply.</span></span> <span data-ttu-id="77f68-134">ปริมาณสินค้าคงคลังคงเหลือทั้งหมดจะถูกสันนิษฐานให้พร้อมใช้งานทันที โดยไม่คำนึงถึงเวลาที่ได้รับสินค้าจริง</span><span class="sxs-lookup"><span data-stu-id="77f68-134">All on-hand inventory is assumed to be available immediately, regardless of when it was actually received.</span></span>

### <a name="reorder-margin"></a><span data-ttu-id="77f68-135">ค่าเผื่อในการสั่งใหม่</span><span class="sxs-lookup"><span data-stu-id="77f68-135">Reorder margin</span></span>

> [!NOTE]
> <span data-ttu-id="77f68-136">**เร็วๆ นี้:** คุณลักษณะนี้ยังไม่ได้รับการสนับสนุนสำหรับการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="77f68-136">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="77f68-137">จนกว่าจะมีการสนับสนุน ค่าทั้งหมดที่ป้อนไว้สำหรับ **ค่าเผื่อในการสั่งใหม่ที่เพิ่มในระยะเวลารอคอยสินค้า** จะถือเป็น *0* (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="77f68-137">Until it's supported, all values that are entered for **Reorder margin added to item lead time** will be treated as *0* (zero).</span></span>

<span data-ttu-id="77f68-138">ภาพประกอบต่อไปนี้เน้นค่าเผื่อในการสั่งใหม่</span><span class="sxs-lookup"><span data-stu-id="77f68-138">The following illustration highlights the reorder margin.</span></span>

![ค่าเผื่อในการสั่งใหม่](media/safety-margins-3.png)

<span data-ttu-id="77f68-140">ค่าเผื่อในการสั่งใหม่นี้จะถูกเพิ่มก่อนระยะเวลารอคอยสินค้าสำหรับแผนการใบสั่งทั้งหมดในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="77f68-140">The reorder margin is added before the item lead time for all planned orders during master planning.</span></span> <span data-ttu-id="77f68-141">ดังนั้น จึงทำให้มั่นใจว่าจะมีเวลาเพิ่มในการวางใบสั่งการจัดหา</span><span class="sxs-lookup"><span data-stu-id="77f68-141">Therefore, it ensures additional time for a supply order to be placed.</span></span> <span data-ttu-id="77f68-142">โดยทั่วไปค่าเผื่อนี้จะใช้เป็นบัฟเฟอร์เพื่อให้มั่นใจถึงเวลาสำหรับกระบวนการอนุมัติหรือกระบวนการภายในอื่นๆ ที่จำเป็นในระหว่างการสร้างใบสั่งการจัดหา</span><span class="sxs-lookup"><span data-stu-id="77f68-142">This margin is typically used as a buffer to ensure time for approval processes or other internal processes that are required during the creation of supply orders.</span></span> <span data-ttu-id="77f68-143">ค่าเผื่อในการสั่งใหม่จะถูกกำหนดระหว่าง *วันที่ในใบสั่ง* การจัดหาและ *วันที่เริ่มต้น*</span><span class="sxs-lookup"><span data-stu-id="77f68-143">The reorder margin is put between the supply *order date* and *start date*.</span></span>

### <a name="issue-margin"></a><span data-ttu-id="77f68-144">ค่าเผื่อสำหรับการตัดสินค้าจากคลัง</span><span class="sxs-lookup"><span data-stu-id="77f68-144">Issue margin</span></span>

> [!NOTE]
> <span data-ttu-id="77f68-145">**เร็วๆ นี้:** คุณลักษณะนี้ยังไม่ได้รับการสนับสนุนสำหรับการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="77f68-145">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="77f68-146">จนกว่าจะมีการสนับสนุน ค่าทั้งหมดที่ป้อนไว้สำหรับ **ค่าเผื่อสำหรับการตัดสินค้าจากคลังที่ถูกหักออกจากวันที่ที่ต้องการ** จะถือเป็น *0* (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="77f68-146">Until it's supported, all values that are entered for **Issue margin deducted from requirement date** will be treated as *0* (zero).</span></span>

<span data-ttu-id="77f68-147">ภาพประกอบต่อไปนี้เน้นค่าเผื่อสำหรับการตัดสินค้าจากคลัง</span><span class="sxs-lookup"><span data-stu-id="77f68-147">The following illustration highlights the issue margin.</span></span>

![ค่าเผื่อสำหรับการตัดสินค้าจากคลัง](media/safety-margins-4.png)

<span data-ttu-id="77f68-149">ค่าเผื่อสำหรับการตัดสินค้าจากคลังจะถูกหักออกจากวันที่ที่ต้องการอุปสงค์ในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="77f68-149">The issue margin is deducted from the demand requirement date during master planning.</span></span> <span data-ttu-id="77f68-150">การทำเช่นนี้จะช่วยให้มั่นใจว่าคุณมีเวลาในการตอบสนองและส่งใบสั่งความต้องการที่เข้ามา</span><span class="sxs-lookup"><span data-stu-id="77f68-150">It helps ensure that you have time to react to and ship incoming demand orders.</span></span> <span data-ttu-id="77f68-151">โดยทั่วไปจะใช้ค่าเผื่อนี้เป็นบัฟเฟอร์เพื่อให้มั่นใจถึงเวลาสำหรับการจัดส่งและกระบวนการคลังสินค้าขาออกที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="77f68-151">This margin is typically used as a buffer to ensure time for shipment and related outbound warehouse processes.</span></span>

<span data-ttu-id="77f68-152">สังเกตว่าเมื่อมีการใช้ค่าเผื่อสำหรับการตัดสินค้าจากคลัง วันที่ที่ต้องการในการจัดหาและอุปสงค์ไม่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="77f68-152">Notice that when an issue margin is applied, related supply and demand requirement dates don't match.</span></span> <span data-ttu-id="77f68-153">แต่จะแตกต่างกันไปตามค่าเผื่อสำหรับการตัดสินค้าจากคลัง เนื่องจากมีการเพิ่มค่าเผื่อสำหรับการตัดสินค้าจากคลังระหว่าง *วันที่ที่ต้องการ* ในการจัดหาและ *วันที่ที่ต้องการ* อุปสงค์</span><span class="sxs-lookup"><span data-stu-id="77f68-153">Instead, they differ by the issue margin, because the issue margin is added between the supply *requirement date* and the demand *requirement date*.</span></span>

## <a name="set-up-safety-margins"></a><span data-ttu-id="77f68-154">ตั้งค่าค่าเผื่อความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="77f68-154">Set up safety margins</span></span>

### <a name="turn-on-safety-margins-in-feature-management"></a><span data-ttu-id="77f68-155">เปิดค่าเผื่อความปลอดภัยในการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="77f68-155">Turn on safety margins in Feature management</span></span>

<span data-ttu-id="77f68-156">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้กับการการเพิ่มประสิทธิภาพการวางแผน คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="77f68-156">Before you can use this feature with Planning Optimization, it must be turned on in your system.</span></span> <span data-ttu-id="77f68-157">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="77f68-157">Admins can use the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="77f68-158">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="77f68-158">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="77f68-159">**โมดูล:** _การวางแผนหลัก_</span><span class="sxs-lookup"><span data-stu-id="77f68-159">**Module:** _Master planning_</span></span>
- <span data-ttu-id="77f68-160">**ชื่อคุณลักษณะ:** _ค่าเผื่อสำหรับการเพิ่มประสิทธิภาพการวางแผน_</span><span class="sxs-lookup"><span data-stu-id="77f68-160">**Feature name:** _Margins for Planning Optimization_</span></span>

### <a name="define-safety-margins"></a><span data-ttu-id="77f68-161">กำหนดค่าเผื่อความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="77f68-161">Define safety margins</span></span>

<span data-ttu-id="77f68-162">ค่าเผื่อความปลอดภัยมีการตั้งค่าแบบยืดหยุ่น</span><span class="sxs-lookup"><span data-stu-id="77f68-162">Safety margins have a flexible setup.</span></span> <span data-ttu-id="77f68-163">เวลาดังกล่าวสามารถตั้งค่าได้ทั้ง *กลุ่มความครอบคลุม* และ *แผนหลัก*</span><span class="sxs-lookup"><span data-stu-id="77f68-163">They can be set on both the *coverage group* and the *master plan*.</span></span> <span data-ttu-id="77f68-164">คุณควรทำความเข้าใจว่ามีการเพิ่มค่าเผื่อที่ด้านบนของกันและกัน</span><span class="sxs-lookup"><span data-stu-id="77f68-164">It's important that you understand that the margins are added on top of each other.</span></span> <span data-ttu-id="77f68-165">ตัวอย่างเช่น ค่าเผื่อในการรับสินค้าสองวันในกลุ่มความครอบคลุมและสามวันในแผนหลักจะสร้างค่าเผื่อในการรับสินค้าที่มีผลบังคับใช้ห้าวัน</span><span class="sxs-lookup"><span data-stu-id="77f68-165">For example, a receipt margin of two days on the coverage group and three days on the master plan will produce an effective receipt margin of five days.</span></span>

<span data-ttu-id="77f68-166">ความสามารถในการกำหนดค่าเผื่อในแผนหลักจะมีประโยชน์เมื่อคุณต้องการจำลองระยะเวลารอคอยสินค้าหรือความไม่แน่นอนสำหรับแผนเฉพาะนานขึ้นแต่ไม่มีผลกระทบต่อการวางแผนรายวัน</span><span class="sxs-lookup"><span data-stu-id="77f68-166">The ability to set the margin on the master plan can be useful when you want to simulate longer lead times or uncertainty for a specific plan, but without affecting the daily planning.</span></span>

#### <a name="coverage-group-safety-margins"></a><span data-ttu-id="77f68-167">ค่าเผื่อความปลอดภัยของกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="77f68-167">Coverage group safety margins</span></span>

<span data-ttu-id="77f68-168">เมื่อต้องการใช้ค่าเผื่อความปลอดภัยกับกลุ่มความครอบคลุม ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="77f68-168">To apply a safety margin to a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="77f68-169">ไปยัง **การวางแผนหลัก \> การตั้งค่า \> กลุ่มความครอบคลุม**</span><span class="sxs-lookup"><span data-stu-id="77f68-169">Go to **Master planning \> Setup \> Coverage groups**.</span></span>
1. <span data-ttu-id="77f68-170">ในบานหน้าต่างรายการ ให้เลือกกลุ่มความครอบคลุมที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="77f68-170">In the list pane, select the desired coverage group.</span></span>
1. <span data-ttu-id="77f68-171">บนแท็บด่วน **อื่นๆ** ในส่วน **ค่าเผื่อความปลอดภัยเป็นวัน** ให้ใช้ฟิลด์ต่อไปนี้เพื่อตั้งค่าค่าเผื่อความปลอดภัยที่จำเป็น (ในหน่วยวัน)</span><span class="sxs-lookup"><span data-stu-id="77f68-171">On the **Other** FastTab, in the **Safety margins in days** section, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="77f68-172">ค่าเผื่อในการรับที่เพิ่มไปยังวันที่ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="77f68-172">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="77f68-173">ออกกำไรที่หักออกจากวันที่ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="77f68-173">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="77f68-174">จัดลำดับกำไรที่เพิ่มไปยังระยะเวลารอสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="77f68-174">Reorder margin added to item lead time</span></span>

#### <a name="master-plan-safety-margins"></a><span data-ttu-id="77f68-175">ค่าเผื่อความปลอดภัยของแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="77f68-175">Master plan safety margins</span></span>

<span data-ttu-id="77f68-176">เมื่อต้องการใช้ค่าเผื่อความปลอดภัยกับแผนหลัก ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="77f68-176">To apply a safety margin to a master plan, follow these steps.</span></span>

1. <span data-ttu-id="77f68-177">ไปที่ **การวางแผนหลัก \> การตั้งค่า \> แผน \> แผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="77f68-177">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="77f68-178">ในบานหน้าต่างรายการ ให้เลือกแผนหลักที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="77f68-178">In the list pane, select the desired master plan.</span></span>
1. <span data-ttu-id="77f68-179">บนแท็บด่วน **ค่าเผื่อความปลอดภัยเป็นวัน** ให้ใช้ฟิลด์ต่อไปนี้เพื่อตั้งค่าค่าเผื่อความปลอดภัยที่จำเป็น (ในหน่วยวัน)</span><span class="sxs-lookup"><span data-stu-id="77f68-179">On the **Safety margins in days** FastTab, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="77f68-180">ค่าเผื่อในการรับที่เพิ่มไปยังวันที่ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="77f68-180">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="77f68-181">ออกกำไรที่หักออกจากวันที่ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="77f68-181">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="77f68-182">จัดลำดับกำไรที่เพิ่มไปยังระยะเวลารอสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="77f68-182">Reorder margin added to item lead time</span></span>

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a><span data-ttu-id="77f68-183">กำหนดว่าการคำนวณจะเป็นไปตามวันที่ในปฏิทินหรือวันทำงาน</span><span class="sxs-lookup"><span data-stu-id="77f68-183">Define whether calculations are based on calendar days or work days</span></span>

<span data-ttu-id="77f68-184">คุณสามารถตั้งค่าค่าเผื่อความปลอดภัยทั้งหมดเพื่อให้คำนวณค่าเผื่อความปลอดภัยตามวันในปฏิทินหรือวันทำงานอย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="77f68-184">You can set all safety margins so that they are calculated based on either calendar days or work days.</span></span>

1. <span data-ttu-id="77f68-185">ไปที่ **การวางแผนหลัก \> การตั้งค่า \> พารามิเตอร์การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="77f68-185">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
1. <span data-ttu-id="77f68-186">บนแท็บ **ทั่วไป** ใน **ค่าเผื่อความปลอดภัยในหน่วยวัน** ให้ตั้งค่าตัวเลือก **วันทำงาน** เป็น *ใช่* เพื่อคำนวณค่าเผื่อตามวันทำงาน</span><span class="sxs-lookup"><span data-stu-id="77f68-186">On the **General** tab, in the **Safety margins in days** section, set the **Working days** option to *Yes* to calculate margins based on working days.</span></span> <span data-ttu-id="77f68-187">ตั้งค่าตัวเลือกเป็น *ไม่* เพื่อคำนวณค่าเผื่อตามวันในปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="77f68-187">Set the option to *No* to calculate margins based on calendar days.</span></span>

<span data-ttu-id="77f68-188">ตัวอย่างเช่น ปฏิทินเปิดตั้งแต่วันจันทร์ถึงวันศุกร์ และปิดวันเสาร์ถึงวันอาทิตย์</span><span class="sxs-lookup"><span data-stu-id="77f68-188">For example, a calendar is open from Monday through Friday and closed from Saturday through Sunday.</span></span> <span data-ttu-id="77f68-189">ถ้ามีค่าเผื่อในการรับสินค้าหนึ่งวัน วันที่ที่ต้องการในวันจันทร์จะสร้างวันที่นำส่งในวันศุกร์ก่อนหน้า เนื่องจากวันเสาร์และวันอาทิตย์ไม่ใช่วันทำงาน</span><span class="sxs-lookup"><span data-stu-id="77f68-189">If there is a receipt margin of one day, a requirement date on a Monday produces a delivery date on the previous Friday, because Saturday and Sunday aren't working days.</span></span>

<span data-ttu-id="77f68-190">ปฏิทินที่ใช้ในการกำหนดวันทำงานขึ้นอยู่กับการตั้งค่าและชนิดของการจัดหา</span><span class="sxs-lookup"><span data-stu-id="77f68-190">The calendar that is used to determine the working days depends on the setup and the supply type.</span></span> <span data-ttu-id="77f68-191">ซึ่งสามารถควบคุมโดยปฏิทินของกลุ่มความครอบคลุม คลังสินค้า และผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="77f68-191">It can be controlled by the calendars of the coverage group, the warehouse, and the vendor.</span></span>

> [!NOTE]
> <span data-ttu-id="77f68-192">ถ้า *คลังสินค้า* ไม่ได้เป็นส่วนหนึ่งของมิติความครอบคลุม (กล่าวคือ การวางแผนจะขึ้นอยู่กับ *ไซต์* เท่านั้น) ไม่ได้ใช้ปฏิทินคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="77f68-192">If *warehouse* isn't part of the coverage dimension (in other words, planning is based only on *site*), the warehouse calendar isn't used.</span></span>

<span data-ttu-id="77f68-193">ระบบสามารถจัดการการตั้งค่าที่มีการกำหนดปฏิทินหนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="77f68-193">The system can handle a setup where one or more calendars are defined.</span></span> <span data-ttu-id="77f68-194">ส่วนย่อยต่อไปนี้จะอธิบายชุดข้อมูลที่สามารถใช้เพื่อควบคุมผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="77f68-194">The following subsections describe the possible combinations that can be used to control the result.</span></span>

#### <a name="calendar-that-is-used-for-the-duration"></a><span data-ttu-id="77f68-195">ปฏิทินที่ใช้สำหรับระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="77f68-195">Calendar that is used for the duration</span></span>

<span data-ttu-id="77f68-196">ปฏิทินที่กำหนดจะควบคุมระยะเวลารอคอยสินค้ารวมตามจริงในวันของปฏิทิน ตั้งแต่วันที่ในใบสั่งการจัดหาไปจนถึงวันที่ที่ต้องการอุปสงค์</span><span class="sxs-lookup"><span data-stu-id="77f68-196">The defined calendars control the actual total lead time in calendar days, from the supply order date to the demand requirement date.</span></span> <span data-ttu-id="77f68-197">มีการใช้ระดับความสำคัญของปฏิทินต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="77f68-197">The following calendar prioritization is used:</span></span>

- <span data-ttu-id="77f68-198">**ระยะเวลารอคอยสินค้าในการซื้อ** – มีการพิจารณาเฉพาะปฏิทินของกลุ่มความครอบคลุมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="77f68-198">**Purchase lead time** – Only the coverage group calendar is considered.</span></span>
- <span data-ttu-id="77f68-199">**ค่าเผื่อในการรับสินค้า** - ใช้ปฏิทินกลุ่มความครอบคลุม ถ้ากำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="77f68-199">**Receipt margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="77f68-200">หรือต้องใช้ปฏิทินคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="77f68-200">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="77f68-201">**ค่าเผื่อสำหรับการตัดสินค้าจากคลัง** - ใช้ปฏิทินกลุ่มความครอบคลุม ถ้ากำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="77f68-201">**Issue margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="77f68-202">หรือต้องใช้ปฏิทินคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="77f68-202">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="77f68-203">**ค่าเผื่อในการสั่ง** – มีการพิจารณาเฉพาะปฏิทินของกลุ่มความครอบคลุมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="77f68-203">**Order margin** – Only the coverage group calendar is considered.</span></span>

#### <a name="calendar-that-is-used-for-the-final-date"></a><span data-ttu-id="77f68-204">ปฏิทินที่ใช้สำหรับวันที่สุดท้าย</span><span class="sxs-lookup"><span data-stu-id="77f68-204">Calendar that is used for the final date</span></span>

<span data-ttu-id="77f68-205">กฎต่อไปนี้จะใช้ในการกำหนดว่ากลไกจัดการการวางแผนสามารถใช้วันที่ที่กำหนดสำหรับชนิดวันที่ที่กำหนดหรือไม่:</span><span class="sxs-lookup"><span data-stu-id="77f68-205">The following rules are applied to determine whether the planning engine can use a given date for a given date type:</span></span>

- <span data-ttu-id="77f68-206">**วันที่ในการรับสินค้าที่ซื้อ** – ใช้ปฏิทินของผู้จัดจำหน่าย ถ้ากำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="77f68-206">**Purchase receipt date** – The vendor calendar is used, if it's defined.</span></span> <span data-ttu-id="77f68-207">หรือใช้ปฏิทินกลุ่มความครอบคลุม ถ้ากำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="77f68-207">Otherwise, the coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="77f68-208">ถ้าไม่ได้กำหนดปฏิทินเหล่านั้นไว้ จะมีการใช้ปฏิทินคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="77f68-208">If neither of those calendars is defined, the warehouse calendar is used.</span></span>
- <span data-ttu-id="77f68-209">**วันที่รับสินค้าสำหรับโอนย้าย** - ใช้ปฏิทินกลุ่มความครอบคลุม ถ้ากำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="77f68-209">**Transfer receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="77f68-210">หรือต้องใช้ปฏิทินคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="77f68-210">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="77f68-211">**วันที่รับสินค้าสำหรับการผลิต** - ใช้ปฏิทินกลุ่มความครอบคลุม ถ้ากำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="77f68-211">**Production receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="77f68-212">หรือต้องใช้ปฏิทินคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="77f68-212">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="77f68-213">**วันที่เปิดการตัดสินค้าจากคลังตามความต้องการ** - ใช้ปฏิทินคลังสินค้า ถ้ากำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="77f68-213">**Demand issue open day** – The warehouse calendar is used, if it's defined.</span></span> <span data-ttu-id="77f68-214">หรือใช้ปฏิทินกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="77f68-214">Otherwise, the coverage group calendar is used.</span></span>
- <span data-ttu-id="77f68-215">**วันที่เปิดของใบสั่ง** – ใช้ชุดข้อมูล (ร่วม) ของปฏิทินกลุ่มความครอบคลุมและปฏิทินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="77f68-215">**Order open day** – A combination (intersection) of the coverage group calendar and the vendor calendar is used.</span></span> <span data-ttu-id="77f68-216">ต้องเปิดทั้งสองปฏิทินเพื่อใช้วันที่</span><span class="sxs-lookup"><span data-stu-id="77f68-216">Both calendars must be open to use the date.</span></span> <span data-ttu-id="77f68-217">ถ้ามีการกำหนดปฏิทินเดียว จะมีการใช้ปฏิทินนั้น</span><span class="sxs-lookup"><span data-stu-id="77f68-217">If only one of the calendars is defined, that calendar is used alone.</span></span>

#### <a name="calendar-setup-overview-matrix"></a><span data-ttu-id="77f68-218">เมทริกซ์ภาพรวมของการตั้งค่าปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="77f68-218">Calendar setup overview matrix</span></span>

<span data-ttu-id="77f68-219">ภาพประกอบต่อไปนี้แสดงเมทริกซ์ที่สรุปว่าใช้ปฏิทินใดเมื่อมีการคำนวณค่าเผื่อความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="77f68-219">The following illustration presents a matrix that summarizes which calendars apply when safety margins are calculated.</span></span> <span data-ttu-id="77f68-220">(เลือกรูปเพื่อเปิดเวอร์ชันความละเอียดสูง) มีการใช้คำย่อและสีต่อไปนี้เพื่อบ่งชี้ว่ามีการระบุชนิดของปฏิทินแต่ละชนิดอย่างไร:</span><span class="sxs-lookup"><span data-stu-id="77f68-220">(Select the image to open a high-resolution version of it.) The following abbreviations and colors are used to indicate where each type of calendar is specified:</span></span>

- <span data-ttu-id="77f68-221">**กลุ่มความครอบคลุม (CG):** สีเขียว</span><span class="sxs-lookup"><span data-stu-id="77f68-221">**Coverage group (CG):** Green</span></span>
- <span data-ttu-id="77f68-222">**คลังสินค้า (WH):** สีเหลือง</span><span class="sxs-lookup"><span data-stu-id="77f68-222">**Warehouse (WH):** Yellow</span></span>
- <span data-ttu-id="77f68-223">**ผู้จัดจำหน่าย (V):** สีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="77f68-223">**Vendor (V):** Blue</span></span>

<span data-ttu-id="77f68-224">[![เมทริกซ์ภาพรวมของการตั้งค่าปฏิทิน](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span><span class="sxs-lookup"><span data-stu-id="77f68-224">[![Calendar setup overview matrix](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span></span>

## <a name="calculating-delays"></a><span data-ttu-id="77f68-225">การล่าช้าที่คำนวณ</span><span class="sxs-lookup"><span data-stu-id="77f68-225">Calculating delays</span></span>

<span data-ttu-id="77f68-226">มีการรวมค่าเผื่อความปลอดภัยทั้งสามชนิดเมื่อระบบกำหนดว่าใบสั่งมีความล่าช้าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="77f68-226">All three types of safety margins are included when the system determines whether an order is delayed.</span></span>

<span data-ttu-id="77f68-227">ตัวอย่างเช่น สินค้ามีระยะเวลารอคอยสินค้าเป็นเวลาหนึ่งวันและระยะเวลาการรับสินค้าสามวัน</span><span class="sxs-lookup"><span data-stu-id="77f68-227">For example, an item has lead time of one day and a receipt margin of three days.</span></span> <span data-ttu-id="77f68-228">ใบสั่งขายสำหรับสินค้านี้ได้รับการตั้งค่าเป็นจำเป็นในวันนี้</span><span class="sxs-lookup"><span data-stu-id="77f68-228">A sales order for this item is set as required today.</span></span> <span data-ttu-id="77f68-229">ในกรณีนี้ จะมีการคำนวณการล่าช้าเป็น *ระยะเวลารอคอยสินค้า* + *ค่าเผื่อในการรับสินค้า* = สี่วัน</span><span class="sxs-lookup"><span data-stu-id="77f68-229">In this case, the delay is calculated as *lead time* + *receipt margin* = four days.</span></span> <span data-ttu-id="77f68-230">ดังนั้น ถ้าวันนี้คือวันที่ 14 สิงหาคม การล่าช้าเป็นเวลาสี่วันจะทำให้มีการจัดส่งสินค้าในวันที่ 18 สิงหาคม</span><span class="sxs-lookup"><span data-stu-id="77f68-230">Therefore, if today is August 14, the four days of delay produces a delivery on August 18.</span></span> <span data-ttu-id="77f68-231">ในแผนภาพต่อไปนี้แสดงตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="77f68-231">The following illustration shows this example.</span></span>

![ตัวอย่างการคำนวณการล่าช้า](media/safety-margins-delays.png)

## <a name="additional-resources"></a><span data-ttu-id="77f68-233">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="77f68-233">Additional resources</span></span>

[<span data-ttu-id="77f68-234">เริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="77f68-234">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="77f68-235">การวิเคราะห์ความเหมาะสมของการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="77f68-235">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]