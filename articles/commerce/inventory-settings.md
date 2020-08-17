---
title: ใช้การตั้งค่าสินค้าคงคลัง
description: หัวข้อนี้จะครอบคลุมการตั้งค่าสินค้าคงคลัง และอธิบายวิธีการใช้การตั้งค่าสินค้าคงคลังใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 737e71dc73750bf151629fd904081924ac15b91e
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621232"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="257bd-103">ใช้การตั้งค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="257bd-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="257bd-104">หัวข้อนี้จะครอบคลุมการตั้งค่าสินค้าคงคลัง และอธิบายวิธีการใช้การตั้งค่าสินค้าคงคลังใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="257bd-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="257bd-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="257bd-105">Overview</span></span>

<span data-ttu-id="257bd-106">การตั้งค่าสินค้าคงคลังระบุว่าสินค้าคงคลังควรมีการตรวจสอบก่อนที่จะเพิ่มผลิตภัณฑ์ไปยังรถเข็นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="257bd-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="257bd-107">นอกจากนี้ยังมีการกำหนดข้อความการจัดซื้อสินค้าที่เกี่ยวข้องกับสินค้าคงคลัง เช่น "ในสต็อก" และ "เหลือเพียงไม่กี่รายการเท่านั้น"</span><span class="sxs-lookup"><span data-stu-id="257bd-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="257bd-108">การตั้งค่าเหล่านี้ทำให้แน่ใจว่าผลิตภัณฑ์ไม่สามารถซื้อได้ หากไม่มีสินค้าในสต็อก</span><span class="sxs-lookup"><span data-stu-id="257bd-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="257bd-109">Dynamics 365 Commerce แสดงการประเมินความพร้อมของสินค้าคงคลังคงเหลือสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="257bd-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="257bd-110">สำหรับข้อมูลเกี่ยวกับวิธีการคำนวณความพร้อมของสินค้าคงคลังคงเหลือ ดูที่ [การคำนวณความพร้อมของสินค้าคงคลังสำหรับช่องทางการขายปลีก](calculated-inventory-retail-channels.md)</span><span class="sxs-lookup"><span data-stu-id="257bd-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="257bd-111">ในโปรแกรมสร้างไซต์ Commerce ขีดจำกัดและช่วงของสินค้าคงคลังจะสามารถกำหนดสำหรับผลิตภัณฑ์หรือประเภทได้</span><span class="sxs-lookup"><span data-stu-id="257bd-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="257bd-112">โดยจะกำหนดว่าสินค้าคงคลังสามารถจัดประเภทเป็น มีในสต็อก สินค้าในสต็อกต่ำ หรือไม่มีสินค้าในสต็อก</span><span class="sxs-lookup"><span data-stu-id="257bd-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="257bd-113">สำหรับรายละเอียด ดูที่ [ตั้งค่าคอนฟิกบัฟเฟอร์สินค้าคงคลังและระดับสินค้าคงคลัง](inventory-buffers-levels.md)</span><span class="sxs-lookup"><span data-stu-id="257bd-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="257bd-114">การตั้งค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="257bd-114">Inventory settings</span></span>

<span data-ttu-id="257bd-115">ใน Commerce การตั้งค่าสินค้าคงคลังจะถูกกำหนดใน **การตั้งค่าไซต์ \> ส่วนขยาย \> การจัดการสินค้าคงคลัง** ในโปรแกรมสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="257bd-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="257bd-116">การตั้งค่าสินค้าคงคลังมีสี่รายการ ซึ่งล้าสมัย (ไม่ได้รับการสนับสนุน):</span><span class="sxs-lookup"><span data-stu-id="257bd-116">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="257bd-117">**เปิดใช้งานการตรวจสอบสินค้าคงคลังในแอป** – การตั้งค่านี้จะเปิดใช้งานการตรวจสอบสินค้าคงคลังของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="257bd-117">**Enable inventory check on app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="257bd-118">กล่องซื้อ รถเข็น และการเบิกสินค้าในโมดูลร้านค้าจะตรวจสอบสินค้าคงคลังของผลิตภัณฑ์ และจะสามารถเพิ่มผลิตภัณฑ์ลงในรถเข็นได้ เมื่อสินค้าคงคลังมีอยู่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="257bd-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="257bd-119">**ระดับสินค้าคงคลังตาม** – การตั้งค่านี้จะกำหนดวิธีการคำนวณระดับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="257bd-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="257bd-120">ค่าที่พร้อมใช้งานคือ **ที่มีทั้งหมด** **ที่มีตามจริง** และ **ขีดจำกัดการไม่มีสินค้าในสต็อก**</span><span class="sxs-lookup"><span data-stu-id="257bd-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="257bd-121">ใน Commerce ขีดจำกัดและช่วงของสินค้าคงคลังจะสามารถกำหนดสำหรับแต่ละผลิตภัณฑ์และประเภทได้</span><span class="sxs-lookup"><span data-stu-id="257bd-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="257bd-122">API ของสินค้าคงคลังของส่งคืนข้อมูลสินค้าคงคลังของผลิตภัณฑ์สำหรับทั้งคุณสมบัติที่ **มีอยู่ทั้งหมด** และคุณสมบัติที่ **มีอยู่จริง**</span><span class="sxs-lookup"><span data-stu-id="257bd-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="257bd-123">ผู้ค้าปลีกจะตัดสินใจว่าค่า **ที่มีอยู่ทั้งหมด** หรือ **ที่มีอยู่จริง** ควรใช้เพื่อกำหนดการตรวจนับสินค้าคงคลัง และช่วงที่สอดคล้องกันสำหรับสถานะมีสินค้าในสต็อก และไม่มีสินค้าในสต็อก</span><span class="sxs-lookup"><span data-stu-id="257bd-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="257bd-124">ค่า **ขีดจำกัดของการไม่มีสินค้าในสต็อก** ของการตั้งค่า **ระดับสินค้าคงคลังตาม** เป็นค่าเก่า (ดั้งเดิม) ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="257bd-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="257bd-125">เมื่อเลือกแล้ว การตรวจนับสินค้าคงคลังจะได้รับการกำหนดจากผลลัพธ์ของค่า **ที่มีอยู่ทั้งหมด** แต่มีการกำหนดขีดจำกัดโดยการตั้งค่าตัวเลข **ขีดจำกัดของการไม่มีสินค้าในสต็อก** ที่จะอธิบายในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="257bd-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="257bd-126">การตั้งค่าขีดจำกัดนี้จะนำไปใช้กับผลิตภัณฑ์ทั้งหมดระหว่างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="257bd-126">This threshold setting applies to all products across an e-Commerce site.</span></span> <span data-ttu-id="257bd-127">ถ้าสินค้าคงคลังต่ำกว่าตัวเลขขีดจำกัด ผลิตภัณฑ์จะมีการพิจารณาเป็น ไม่มีสินค้าในสต็อก</span><span class="sxs-lookup"><span data-stu-id="257bd-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="257bd-128">อย่างไรก็ตาม จะถือว่ามีในสต็อกสินค้า</span><span class="sxs-lookup"><span data-stu-id="257bd-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="257bd-129">ความสามารถของค่า **ขีดจำกัดของการไม่มีสินค้าในสต็อก** จำกัด และเราไม่แนะนำให้คุณใช้รุ่น 10.0.12 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="257bd-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="257bd-130">**ช่วงของสินค้าคงคลัง** - การตั้งค่านี้จะกำหนดช่วงของสินค้าคงคลังที่มีการแสดงข้อความบนโมดูลไซต์</span><span class="sxs-lookup"><span data-stu-id="257bd-130">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="257bd-131">มีผลบังคับใช้เมื่อมีการเลือกค่า **ที่มีอยู่ทั้งหมด** หรือ **ที่มีอยู่จริง** สำหรับการตั้งค่า **ระดับสินค้าคงคลังตาม**</span><span class="sxs-lookup"><span data-stu-id="257bd-131">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="257bd-132">ค่าที่พร้อมใช้งานมี **ทั้งหมด** **สินค้าในสต็อกต่ำและไม่มีสินค้าในสต็อก** และ **ไม่มีสินค้าในสต็อก**</span><span class="sxs-lookup"><span data-stu-id="257bd-132">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="257bd-133">เมื่อ **ทั้งหมด** ถูกเลือก ข้อความสำหรับช่วงของสินค้าคงคลังทั้งหมด จากในสต็อก (ข้อความ "มีอยู่") ไปยังไม่มีสินค้าในสต็อก (ข้อความ "ไม่มีสินค้าในสต็อก") จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="257bd-133">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="257bd-134">เมื่อ **สินค้าในสต็อกต่ำและไม่มีสินค้าในสต็อก** ถูกเลือก ข้อความสำหรับช่วงของสินค้าคงคลังทั้งหมดยกเว้นในสต็อก (ข้อความ "มีอยู่") จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="257bd-134">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="257bd-135">เมื่อ **ไม่มีสินค้าในสต็อก** ถูกเลือก เฉพาะข้อความ "ไม่มีสินค้าในสต็อก" จะแสดงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="257bd-135">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="257bd-136">**ขีดจำกัดของการไม่มีสินค้าในสต็อ** - การตั้งค่าที่เป็นตัวเลขเก่านี้จะมีผลเฉพาะเมื่อค่า **ขีดจำกัดของการไม่มีสินค้าในสต็อ** ถูกเลือกสำหรับการตั้งค่า **ระดับสินค้าคงคลังตาม** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="257bd-136">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="257bd-137">โมดูลที่ใช้การตั้งค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="257bd-137">Modules that use inventory settings</span></span>

<span data-ttu-id="257bd-138">โมดูลกล่องการซื้อ รายการโปรด ตัวเลือกร้านค้า รถเข็น และไอคอนรถเข็นใช้การตั้งค่าสินค้าคงคลัง เพื่อแสดงช่วงของสินค้าคงคลังและข้อความ</span><span class="sxs-lookup"><span data-stu-id="257bd-138">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="257bd-139">รูปภาพต่อไปนี้แสดงตัวอย่างของหน้ารายละเอียดผลิตภัณฑ์ (PDP) ซึ่งแสดงข้อความสินค้าในสต็อก ("มีอยู่")</span><span class="sxs-lookup"><span data-stu-id="257bd-139">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![ตัวอย่างของโมดูล PDP ที่ที่มีข้อความในสต็อก](./media/pdp-InStock.png)

<span data-ttu-id="257bd-141">รูปภาพต่อไปนี้แสดงตัวอย่างของ PDP ซึ่งแสดงข้อความ "ไม่มีสินค้าในสต็อก"</span><span class="sxs-lookup"><span data-stu-id="257bd-141">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![ตัวอย่างของโมดูล PDP ที่ที่มีข้อความ ไม่มีสินค้าในสต็อก](./media/pdp-outofstock.png)

<span data-ttu-id="257bd-143">รูปภาพต่อไปนี้แสดงตัวอย่างของรถเข็น ซึ่งแสดงข้อความสินค้าในสต็อก ("มีอยู่")</span><span class="sxs-lookup"><span data-stu-id="257bd-143">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![ตัวอย่างของโมดูลรถเข็น ที่มีข้อความในสต็อก](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="257bd-145">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="257bd-145">Additional resources</span></span>

[<span data-ttu-id="257bd-146">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="257bd-146">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="257bd-147">ตั้งค่าคอนฟิกบัฟเฟอร์สินค้าคงคลังและระดับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="257bd-147">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="257bd-148">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="257bd-148">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="257bd-149">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="257bd-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="257bd-150">หน้าและโมดูลการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="257bd-150">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="257bd-151">โมดูลตัวเลือกการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="257bd-151">Store selector module</span></span>](store-selector.md)
