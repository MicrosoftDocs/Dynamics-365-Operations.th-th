---
title: ใช้การตั้งค่าสินค้าคงคลัง
description: หัวข้อนี้จะครอบคลุมการตั้งค่าสินค้าคงคลัง และอธิบายวิธีการใช้การตั้งค่าสินค้าคงคลังใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3da447c298993794afa49a0fbaddb1c21cf6231a
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271316"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="a1d37-103">ใช้การตั้งค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a1d37-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a1d37-104">หัวข้อนี้จะครอบคลุมการตั้งค่าสินค้าคงคลัง และอธิบายวิธีการใช้การตั้งค่าสินค้าคงคลังใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a1d37-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a1d37-105">การตั้งค่าสินค้าคงคลังระบุว่าสินค้าคงคลังควรมีการตรวจสอบก่อนที่จะเพิ่มผลิตภัณฑ์ไปยังรถเข็นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a1d37-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="a1d37-106">นอกจากนี้ยังมีการกำหนดข้อความการจัดซื้อสินค้าที่เกี่ยวข้องกับสินค้าคงคลัง เช่น "ในสต็อก" และ "เหลือเพียงไม่กี่รายการเท่านั้น"</span><span class="sxs-lookup"><span data-stu-id="a1d37-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="a1d37-107">การตั้งค่าเหล่านี้ทำให้แน่ใจว่าผลิตภัณฑ์ไม่สามารถซื้อได้ หากไม่มีสินค้าในสต็อก</span><span class="sxs-lookup"><span data-stu-id="a1d37-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="a1d37-108">Dynamics 365 Commerce แสดงการประเมินความพร้อมของสินค้าคงคลังคงเหลือสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a1d37-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="a1d37-109">สำหรับข้อมูลเกี่ยวกับวิธีการคำนวณความพร้อมของสินค้าคงคลังคงเหลือ ดูที่ [การคำนวณความพร้อมของสินค้าคงคลังสำหรับช่องทางการขายปลีก](calculated-inventory-retail-channels.md)</span><span class="sxs-lookup"><span data-stu-id="a1d37-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="a1d37-110">ในโปรแกรมสร้างไซต์ Commerce ขีดจำกัดและช่วงของสินค้าคงคลังจะสามารถกำหนดสำหรับผลิตภัณฑ์หรือประเภทได้</span><span class="sxs-lookup"><span data-stu-id="a1d37-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="a1d37-111">โดยจะกำหนดว่าสินค้าคงคลังสามารถจัดประเภทเป็น มีในสต็อก สินค้าในสต็อกต่ำ หรือไม่มีสินค้าในสต็อก</span><span class="sxs-lookup"><span data-stu-id="a1d37-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="a1d37-112">สำหรับรายละเอียด ดูที่ [ตั้งค่าคอนฟิกบัฟเฟอร์สินค้าคงคลังและระดับสินค้าคงคลัง](inventory-buffers-levels.md)</span><span class="sxs-lookup"><span data-stu-id="a1d37-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a1d37-113">การสนับสนุนสำหรับขีดจำกัดของสินค้าคงคลังและช่วงมีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.12</span><span class="sxs-lookup"><span data-stu-id="a1d37-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="a1d37-114">การตั้งค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a1d37-114">Inventory settings</span></span>

<span data-ttu-id="a1d37-115">ใน Commerce การตั้งค่าสินค้าคงคลังจะถูกกำหนดใน **การตั้งค่าไซต์ \> ส่วนขยาย \> การจัดการสินค้าคงคลัง** ในโปรแกรมสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="a1d37-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="a1d37-116">การตั้งค่าสินค้าคงคลังมีห้ารายการ ซึ่งล้าสมัย (ไม่ได้รับการสนับสนุน):</span><span class="sxs-lookup"><span data-stu-id="a1d37-116">There are five inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="a1d37-117">**เปิดใช้งานการตรวจสอบสินค้าคงคลังในแอป** – การตั้งค่านี้จะเปิดใช้งานการตรวจสอบสินค้าคงคลังของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a1d37-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="a1d37-118">กล่องซื้อ รถเข็น และการเบิกสินค้าในโมดูลร้านค้าจะตรวจสอบสินค้าคงคลังของผลิตภัณฑ์ และจะสามารถเพิ่มผลิตภัณฑ์ลงในรถเข็นได้ เมื่อสินค้าคงคลังมีอยู่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a1d37-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="a1d37-119">**ระดับสินค้าคงคลังตาม** – การตั้งค่านี้จะกำหนดวิธีการคำนวณระดับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a1d37-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="a1d37-120">ค่าที่พร้อมใช้งานคือ **ที่มีทั้งหมด** **ที่มีตามจริง** และ **ขีดจำกัดการไม่มีสินค้าในสต็อก**</span><span class="sxs-lookup"><span data-stu-id="a1d37-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="a1d37-121">ใน Commerce ขีดจำกัดและช่วงของสินค้าคงคลังจะสามารถกำหนดสำหรับแต่ละผลิตภัณฑ์และประเภทได้</span><span class="sxs-lookup"><span data-stu-id="a1d37-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="a1d37-122">API ของสินค้าคงคลังของส่งคืนข้อมูลสินค้าคงคลังของผลิตภัณฑ์สำหรับทั้งคุณสมบัติที่ **มีอยู่ทั้งหมด** และคุณสมบัติที่ **มีอยู่จริง**</span><span class="sxs-lookup"><span data-stu-id="a1d37-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="a1d37-123">ผู้ค้าปลีกจะตัดสินใจว่าค่า **ที่มีอยู่ทั้งหมด** หรือ **ที่มีอยู่จริง** ควรใช้เพื่อกำหนดการตรวจนับสินค้าคงคลัง และช่วงที่สอดคล้องกันสำหรับสถานะมีสินค้าในสต็อก และไม่มีสินค้าในสต็อก</span><span class="sxs-lookup"><span data-stu-id="a1d37-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="a1d37-124">ค่า **ขีดจำกัดของการไม่มีสินค้าในสต็อก** ของการตั้งค่า **ระดับสินค้าคงคลังตาม** เป็นค่าเก่า (ดั้งเดิม) ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="a1d37-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="a1d37-125">เมื่อเลือกแล้ว การตรวจนับสินค้าคงคลังจะได้รับการกำหนดจากผลลัพธ์ของค่า **ที่มีอยู่ทั้งหมด** แต่มีการกำหนดขีดจำกัดโดยการตั้งค่าตัวเลข **ขีดจำกัดของการไม่มีสินค้าในสต็อก** ที่จะอธิบายในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="a1d37-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="a1d37-126">การตั้งค่าขีดจำกัดนี้จะนำไปใช้กับผลิตภัณฑ์ทั้งหมดระหว่างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="a1d37-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="a1d37-127">ถ้าสินค้าคงคลังต่ำกว่าตัวเลขขีดจำกัด ผลิตภัณฑ์จะมีการพิจารณาเป็น ไม่มีสินค้าในสต็อก</span><span class="sxs-lookup"><span data-stu-id="a1d37-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="a1d37-128">อย่างไรก็ตาม จะถือว่ามีในสต็อกสินค้า</span><span class="sxs-lookup"><span data-stu-id="a1d37-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="a1d37-129">ความสามารถของค่า **ขีดจำกัดของการไม่มีสินค้าในสต็อก** จำกัด และเราไม่แนะนำให้คุณใช้รุ่น 10.0.12 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="a1d37-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="a1d37-130">**ระดับสินค้าคงคลังในคลังสินค้าหลายแห่ง** – การตั้งค่านี้ช่วยให้สามารถคํานวณระดับสินค้าคงคลังกับคลังสินค้าเริ่มต้นหรือคลังสินค้าหลายแห่งได้</span><span class="sxs-lookup"><span data-stu-id="a1d37-130">**Inventory level for multiple warehouses** – This setting enables the inventory level to be calculated against the default warehouse or multiple warehouses.</span></span> <span data-ttu-id="a1d37-131">ตัวเลือก **ขึ้นอยู่กับคลังสินค้า** แต่ละตัวจะคํานวณระดับสินค้าคงคลังตามคลังสินค้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a1d37-131">The **Based on individual warehouse** option will calculate inventory levels based on the default warehouse.</span></span> <span data-ttu-id="a1d37-132">หรือไซต์อีคอมเมิร์ซอาจชี้ไปยังคลังสินค้าต่าง ๆ เพื่อช่วยในการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a1d37-132">Alternatively, an e-commerce site can point to multiple warehouses to facilitate fulfillment.</span></span> <span data-ttu-id="a1d37-133">ในกรณีดังกล่าว ตัวเลือก **ตามการรวมคลังสินค้าการจัดส่งและการเบิกสินค้า** จะใช้เพื่อบ่งชี้ความพร้อมใช้งานของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a1d37-133">In that case, the **Based on aggregate for Shipping and Pickup warehouses** option is used to indicate stock availability.</span></span> <span data-ttu-id="a1d37-134">ตัวอย่างเช่น เมื่อลูกค้าซื้อสินค้าและเลือก "การจัดส่งสินค้า" เป็นวิธีการจัดส่ง สินค้าสามารถจัดส่งจากคลังสินค้าใด ๆ ในกลุ่มการเติมสินค้าที่มีสินค้าคงคลังที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a1d37-134">For example, when a customer purchases an item and selects "shipping" as the delivery mode, the item can be shipped from any warehouse in the fulfillment group that has available inventory.</span></span> <span data-ttu-id="a1d37-135">หน้ารายละเอียดผลิตภัณฑ์ (PDP) จะแสดงข้อความ "ในสินค้าคงคลัง" เพื่อจัดส่ง หากคลังสินค้าจัดส่งที่พร้อมใช้งานในกลุ่มการเติมสินค้ามีสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a1d37-135">The product details page (PDP) will show an "In stock" message for shipping if any available shipping warehouse in the fulfillment group has inventory.</span></span> 

> [!IMPORTANT] 
> <span data-ttu-id="a1d37-136">การตั้งค่า **ระดับสินค้าคงคลังหลายคลังสินค้าสามารถใช้** พร้อมใช้งานตั้งแต่ Commerce รุ่น 10.0.19</span><span class="sxs-lookup"><span data-stu-id="a1d37-136">The **Inventory level for multiple warehouses** setting is available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="a1d37-137">ถ้าคุณกำลังอัพปเดตจากเวอร์ชันที่เก่ากว่าของ Commerce คุณต้องอัปเดตไฟล์ appsettings.json ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a1d37-137">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="a1d37-138">สำหรับคำแนะนำ โปรดดู [SDK และอัปเดตไลบรารีโมดูล](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)</span><span class="sxs-lookup"><span data-stu-id="a1d37-138">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

- <span data-ttu-id="a1d37-139">**ช่วงของสินค้าคงคลัง** - การตั้งค่านี้จะกำหนดช่วงของสินค้าคงคลังที่มีการแสดงข้อความบนโมดูลไซต์</span><span class="sxs-lookup"><span data-stu-id="a1d37-139">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="a1d37-140">มีผลบังคับใช้เมื่อมีการเลือกค่า **ที่มีอยู่ทั้งหมด** หรือ **ที่มีอยู่จริง** สำหรับการตั้งค่า **ระดับสินค้าคงคลังตาม**</span><span class="sxs-lookup"><span data-stu-id="a1d37-140">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="a1d37-141">ค่าที่พร้อมใช้งานมี **ทั้งหมด** **สินค้าในสต็อกต่ำและไม่มีสินค้าในสต็อก** และ **ไม่มีสินค้าในสต็อก**</span><span class="sxs-lookup"><span data-stu-id="a1d37-141">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="a1d37-142">เมื่อ **ทั้งหมด** ถูกเลือก ข้อความสำหรับช่วงของสินค้าคงคลังทั้งหมด จากในสต็อก (ข้อความ "มีอยู่") ไปยังไม่มีสินค้าในสต็อก (ข้อความ "ไม่มีสินค้าในสต็อก") จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="a1d37-142">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="a1d37-143">เมื่อ **สินค้าในสต็อกต่ำและไม่มีสินค้าในสต็อก** ถูกเลือก ข้อความสำหรับช่วงของสินค้าคงคลังทั้งหมดยกเว้นในสต็อก (ข้อความ "มีอยู่") จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="a1d37-143">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="a1d37-144">เมื่อ **ไม่มีสินค้าในสต็อก** ถูกเลือก เฉพาะข้อความ "ไม่มีสินค้าในสต็อก" จะแสดงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a1d37-144">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="a1d37-145">**ขีดจำกัดของการไม่มีสินค้าในสต็อ** - การตั้งค่าที่เป็นตัวเลขเก่านี้จะมีผลเฉพาะเมื่อค่า **ขีดจำกัดของการไม่มีสินค้าในสต็อ** ถูกเลือกสำหรับการตั้งค่า **ระดับสินค้าคงคลังตาม** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a1d37-145">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="a1d37-146">การตั้งค่าเหล่านี้มีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.12</span><span class="sxs-lookup"><span data-stu-id="a1d37-146">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="a1d37-147">ถ้าคุณกำลังอัพปเดตจากเวอร์ชันที่เก่ากว่าของ Dynamics 365 Commerce คุณต้องอัปเดตไฟล์ appsettings.json ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a1d37-147">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="a1d37-148">สำหรับคำแนะนำเกี่ยวกับการอัปเดตไฟล์ appsettings.json ให้ดูที่ [อัปเดต SDK และไลบรารีโมดูล](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)</span><span class="sxs-lookup"><span data-stu-id="a1d37-148">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="a1d37-149">โมดูลที่ใช้การตั้งค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a1d37-149">Modules that use inventory settings</span></span>

<span data-ttu-id="a1d37-150">โมดูลกล่องการซื้อ รายการโปรด ตัวเลือกร้านค้า รถเข็น และไอคอนรถเข็นใช้การตั้งค่าสินค้าคงคลัง เพื่อแสดงช่วงของสินค้าคงคลังและข้อความ</span><span class="sxs-lookup"><span data-stu-id="a1d37-150">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="a1d37-151">ในตัวอย่างในภาพประกอบต่อไปนี้ จะมีข้อความ PDP แสดงอยู่ในสินค้าคงคลัง ("พร้อมใช้งาน")</span><span class="sxs-lookup"><span data-stu-id="a1d37-151">In the example in the following illustration, a PDP is showing an in-stock ("Available") message.</span></span>

![ตัวอย่างของโมดูล PDP ที่ที่มีข้อความในสต็อก](./media/pdp-InStock.png)

<span data-ttu-id="a1d37-153">ในตัวอย่างในภาพประกอบต่อไปนี้ PDP แสดงข้อความ "ไม่มีสินค้าในสต็อก"</span><span class="sxs-lookup"><span data-stu-id="a1d37-153">In the example in the following illustration, a PDP is showing an "Out of stock" message.</span></span>

![ตัวอย่างของโมดูล PDP ที่ที่มีข้อความ ไม่มีสินค้าในสต็อก](./media/pdp-outofstock.png)

<span data-ttu-id="a1d37-155&quot;>ในตัวอย่างในภาพประกอบต่อไปนี้ รถเข็นแสดงอยู่ในสินค้าคงคลัง (&quot;พร้อมใช้งาน")</span><span class="sxs-lookup"><span data-stu-id="a1d37-155">In the example in the following illustration, a cart is showing an in-stock ("Available") message.</span></span>

![ตัวอย่างของโมดูลรถเข็น ที่มีข้อความในสต็อก](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="a1d37-157">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a1d37-157">Additional resources</span></span>

[<span data-ttu-id="a1d37-158">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="a1d37-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a1d37-159">ตั้งค่าคอนฟิกสินค้าคงคลังสำรองและระดับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a1d37-159">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="a1d37-160">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="a1d37-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a1d37-161">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="a1d37-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a1d37-162">หน้าและโมดูลการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="a1d37-162">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="a1d37-163">โมดูลตัวเลือกการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="a1d37-163">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="a1d37-164">การอัปเดต SDK และไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="a1d37-164">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
