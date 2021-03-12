---
title: การแปลงหน่วยวัดต่อผลิตภัณฑ์ย่อย
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการแปลงหน่วยวัดสำหรับผลิตภัณฑ์ย่อย ซึ่งรวมตัวอย่างของการตั้งค่า
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 5f327d1d0b38ad724da6a302cefc115262317812
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001710"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="01fd5-104">การแปลงหน่วยวัดต่อผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="01fd5-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01fd5-105">หัวข้อนี้อธิบายวิธีการตั้งค่าการแปลงหน่วยวัดสำหรับผลิตภัณฑ์ย่อยต่างๆ</span><span class="sxs-lookup"><span data-stu-id="01fd5-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="01fd5-106">แทนที่จะสร้างผลิตภัณฑ์แต่ละรายการหลายรายการที่ต้องมีการบำรุงรักษา คุณสามารถใช้ผลิตภัณฑ์ย่อยเพื่อสร้างการเปลี่ยนแปลงของผลิตภัณฑ์เดียว</span><span class="sxs-lookup"><span data-stu-id="01fd5-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="01fd5-107">ตัวอย่างเช่น ผลิตภัณฑ์ย่อยอาจเป็นเสื้อยืดของขนาดและสีที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="01fd5-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="01fd5-108">ก่อนหน้านี้ อาจตั้งค่าการแปลงหน่วยได้เฉพาะในผลิตภัณฑ์หลักเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="01fd5-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="01fd5-109">ดังนั้นผลิตภัณฑ์ย่อยทั้งหมดมีกฎการแปลงหน่วยเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="01fd5-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="01fd5-110">อย่างไรก็ตาม เมื่อมีการเปิดใช้งานคุณลักษณะ *การแปลงหน่วยวัดสำหรับผลิตภัณฑ์ย่อย* ถ้าเสื้อยืดของคุณมีการขายในกล่องและจำนวนของเสื้อยืดที่สามารถบรรจุไว้ในกล่องจะขึ้นอยู่กับขนาดของเสื้อยืด คุณสามารถตั้งค่าการแปลงหน่วยระหว่างขนาดเสื้อผ้าต่างๆ และกล่องที่ใช้สำหรับบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="01fd5-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="01fd5-111">เปิดใช้งานคุณลักษณะการทำงานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="01fd5-111">Turn on the feature in your system</span></span>

<span data-ttu-id="01fd5-112">หากคุณยังไม่เห็นคุณลักษณะนี้ในระบบของคุณ ให้ไปที่ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) แล้วเปิดใช้งานคุณลักษณะ *การแปลงหน่วยวัดสำหรับผลิตภัณฑ์ย่อย*</span><span class="sxs-lookup"><span data-stu-id="01fd5-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="01fd5-113">ตั้งค่าผลิตภัณฑ์สำหรับการแปลงหน่วยสำหรับแต่ละผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="01fd5-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="01fd5-114">คุณสามารถสร้างผลิตภัณฑ์ย่อยสำหรับผลิตภัณฑ์ที่เป็นผลิตภัณฑ์หลักเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="01fd5-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="01fd5-115">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างผลิตภัณฑ์หลัก](tasks/create-product-master.md)</span><span class="sxs-lookup"><span data-stu-id="01fd5-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="01fd5-116">คุณลักษณะ *การแปลงหน่วยวัดสำหรับผลิตภัณฑ์ย่อย* ไม่พร้อมใช้งานสำหรับผลิตภัณฑ์ที่ตั้งค่าไว้สำหรับกระบวนการที่มีน้ำหนักจริง</span><span class="sxs-lookup"><span data-stu-id="01fd5-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="01fd5-117">เมื่อต้องการตั้งค่าคอนฟิกข้อมูลของผลิตภัณฑ์หลักเพื่อสนับสนุนการแปลงหน่วยสำหรับแต่ละตัวแปร ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="01fd5-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="01fd5-118">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="01fd5-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="01fd5-119">สร้างหรือเปิดผลิตภัณฑ์หลักเพื่อให้ไปที่หน้า **รายละเอียดผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="01fd5-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="01fd5-120">ตั้งค่าตัวเลือก **เปิดใช้งานการแปลงหน่วยวัด** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="01fd5-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="01fd5-121">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผลิตภัณฑ์** ในกลุ่ม **การตั้งค่า** ให้เลือก **การแปลงหน่วย**</span><span class="sxs-lookup"><span data-stu-id="01fd5-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="01fd5-122">หน้า **การแปลงหน่วย** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="01fd5-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="01fd5-123">เลือกแท็บใดแท็บหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="01fd5-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="01fd5-124">**การแปลงในระดับ Intra** – เลือกแท็บนี้เพื่อแปลงระหว่างหน่วยที่อยู่ในประเภทของหน่วยเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="01fd5-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="01fd5-125">**การแปลงในระดับ Inter** – เลือกแท็บนี้เพื่อแปลงระหว่างหน่วยที่อยู่ในประเภทของหน่วยต่างกัน</span><span class="sxs-lookup"><span data-stu-id="01fd5-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="01fd5-126">เลือก **สร้าง** เพื่อเพิ่มการแปลงหน่วยใหม่</span><span class="sxs-lookup"><span data-stu-id="01fd5-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="01fd5-127">ตั้งค่าฟิลด์ **สร้างการแปลงสำหรับ** เป็นหนึ่งในค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="01fd5-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="01fd5-128">**ผลิตภัณฑ์** – ถ้าคุณเลือกค่านี้ คุณสามารถตั้งค่าการแปลงหน่วยสำหรับผลิตภัณฑ์หลักได้</span><span class="sxs-lookup"><span data-stu-id="01fd5-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="01fd5-129">การแปลงหน่วยที่จะใช้สำรองสำหรับผลิตภัณฑ์ย่อยทั้งหมดที่ไม่ได้กำหนดให้มีการแปลงหน่วย</span><span class="sxs-lookup"><span data-stu-id="01fd5-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="01fd5-130">**ผลิตภัณฑ์ย่อย** – ถ้าคุณเลือกค่านี้ คุณสามารถตั้งค่าการแปลงหน่วยสำหรับผลิตภัณฑ์ย่อยที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="01fd5-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="01fd5-131">ใช้ฟิลด์ **ผลิตภัณฑ์ย่อย** เพื่อเลือกตัวแปร</span><span class="sxs-lookup"><span data-stu-id="01fd5-131">Use the **Product variant** field to select the variant.</span></span>

    <span data-ttu-id="01fd5-132">![การเพิ่มการแปลงหน่วยใหม่](media/uom-new-conversion.png "การเพิ่มการแปลงหน่วยใหม่")</span><span class="sxs-lookup"><span data-stu-id="01fd5-132">![Adding a new unit conversion](media/uom-new-conversion.png "Adding a new unit conversion")</span></span>

1. <span data-ttu-id="01fd5-133">ใช้ฟิลด์อื่นๆ ที่จะกำหนดให้มีการตั้งค่าการแปลงหน่วยของคุณ</span><span class="sxs-lookup"><span data-stu-id="01fd5-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="01fd5-134">เลือก **ตกลง** เพื่อบันทึกการแปลงหน่วยใหม่</span><span class="sxs-lookup"><span data-stu-id="01fd5-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="01fd5-135">คุณสามารถเปิดหน้า **การแปลงหน่วย** สำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยจากหน้าใดๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="01fd5-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="01fd5-136">รายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="01fd5-136">Product details</span></span>
> - <span data-ttu-id="01fd5-137">รายละเอียดผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="01fd5-137">Released products details</span></span>
> - <span data-ttu-id="01fd5-138">ผลิตภัณฑ์ย่อยที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="01fd5-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="01fd5-139">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="01fd5-139">Example scenario</span></span>

<span data-ttu-id="01fd5-140">ในสถานการณ์จำลองนี้ บริษัทขายเสื้อยืดขนาดเล็ก ขนาดกลาง ขนาดใหญ่ และขนาดใหญ่พิเศษ</span><span class="sxs-lookup"><span data-stu-id="01fd5-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="01fd5-141">เสื้อยืดถูกกำหนดให้เป็นผลิตภัณฑ์ และขนาดที่แตกต่างกันจะถูกกำหนดเป็นผลิตภัณฑ์ย่อยของผลิตภัณฑ์นั้น</span><span class="sxs-lookup"><span data-stu-id="01fd5-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="01fd5-142">เสื้อถูกบรรจุลงในกล่อง</span><span class="sxs-lookup"><span data-stu-id="01fd5-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="01fd5-143">สำหรับขนาดเล็ก ขนาดกลาง และขนาดใหญ่ อาจมีเสื้อห้าตัวในแต่ละกล่อง</span><span class="sxs-lookup"><span data-stu-id="01fd5-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="01fd5-144">อย่างไรก็ตามสำหรับขนาดใหญ่พิเศษ มีพื้นที่สำหรับเสื้อเพียงสี่ตัวเท่านั้นในแต่ละกล่อง</span><span class="sxs-lookup"><span data-stu-id="01fd5-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="01fd5-145">บริษัทต้องการติดตามผลิตภัณฑ์ย่อยที่แตกต่างกันในหน่วย *ชิ้น* แต่ขายในหน่วย *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="01fd5-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="01fd5-146">สำหรับขนาดเล็ก ขนาดกลาง และขนาดใหญ่ การแปลงระหว่างหน่วยสินค้าคงคลังและหน่วยการขายคือ 1 กล่อง = 5 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="01fd5-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="01fd5-147">สำหรับขนาดใหญ่พิเศษมีการแปลง 1 กล่อง = 4 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="01fd5-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="01fd5-148">จากหน้า **รายละเอียดผลิตภัณฑ์** สำหรับผลิตภัณฑ์ **เสื้อยืด** ให้เปิดหน้า **การแปลงหน่วย**</span><span class="sxs-lookup"><span data-stu-id="01fd5-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="01fd5-149">ในหน้า **การแปลงหน่วย** ตั้งค่าการแปลงหน่วยต่อไปนี้สำหรับผลิตภัณฑ์ย่อย **ขนาดใหญ่พิเศษ** ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="01fd5-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="01fd5-150">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="01fd5-150">Field</span></span>                 | <span data-ttu-id="01fd5-151">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="01fd5-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="01fd5-152">สร้างการแปลงสำหรับ</span><span class="sxs-lookup"><span data-stu-id="01fd5-152">Create conversion for</span></span> | <span data-ttu-id="01fd5-153">ผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="01fd5-153">Product variant</span></span>         |
    | <span data-ttu-id="01fd5-154">ผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="01fd5-154">Product variant</span></span>       | <span data-ttu-id="01fd5-155">เสื้อยืด : : ใหญ่พิเศษ : :</span><span class="sxs-lookup"><span data-stu-id="01fd5-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="01fd5-156">หน่วยเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="01fd5-156">From unit</span></span>             | <span data-ttu-id="01fd5-157">กล่อง</span><span class="sxs-lookup"><span data-stu-id="01fd5-157">Boxes</span></span>                   |
    | <span data-ttu-id="01fd5-158">แฟคเตอร์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="01fd5-158">Factor</span></span>                | <span data-ttu-id="01fd5-159">4</span><span class="sxs-lookup"><span data-stu-id="01fd5-159">4</span></span>                       |
    | <span data-ttu-id="01fd5-160">หน่วยเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="01fd5-160">To Unit</span></span>               | <span data-ttu-id="01fd5-161">ชิ้น</span><span class="sxs-lookup"><span data-stu-id="01fd5-161">Pieces</span></span>                  |

1. <span data-ttu-id="01fd5-162">เนื่องจากผลิตภัณฑ์ย่อย **ขนาดเล็ก** **กลาง** และ **ใหญ่** มีหน่วยการแปลงเดียวกันระหว่างหน่วย *กล่อง* และ *ชิ้น*  คุณสามารถกำหนดการแปลงหน่วยต่อไปนี้สำหรับผลิตภัณฑ์ย่อยในผลิตภัณฑ์หลักได้</span><span class="sxs-lookup"><span data-stu-id="01fd5-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="01fd5-163">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="01fd5-163">Field</span></span>                 | <span data-ttu-id="01fd5-164">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="01fd5-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="01fd5-165">สร้างการแปลงสำหรับ</span><span class="sxs-lookup"><span data-stu-id="01fd5-165">Create conversion for</span></span> | <span data-ttu-id="01fd5-166">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="01fd5-166">Product</span></span> |
    | <span data-ttu-id="01fd5-167">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="01fd5-167">Product</span></span>               | <span data-ttu-id="01fd5-168">เสื้อยืด</span><span class="sxs-lookup"><span data-stu-id="01fd5-168">T-Shirt</span></span> |
    | <span data-ttu-id="01fd5-169">หน่วยเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="01fd5-169">From unit</span></span>             | <span data-ttu-id="01fd5-170">กล่อง</span><span class="sxs-lookup"><span data-stu-id="01fd5-170">Boxes</span></span>   |
    | <span data-ttu-id="01fd5-171">แฟคเตอร์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="01fd5-171">Factor</span></span>                | <span data-ttu-id="01fd5-172">5</span><span class="sxs-lookup"><span data-stu-id="01fd5-172">5</span></span>       |
    | <span data-ttu-id="01fd5-173">หน่วยเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="01fd5-173">To Unit</span></span>               | <span data-ttu-id="01fd5-174">ชิ้น</span><span class="sxs-lookup"><span data-stu-id="01fd5-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="01fd5-175">การใช้ Excel เพื่ออัพเดตการแปลงหน่วย</span><span class="sxs-lookup"><span data-stu-id="01fd5-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="01fd5-176">ถ้าผลิตภัณฑ์มีผลิตภัณฑ์ย่อยมากมายที่มีการแปลงหน่วยที่แตกต่างกัน คุณควรส่งออกการแปลงหน่วยไปยังสมุดงาน Microsoft Excel อัปเดตข้อมูลดังกล่าว แล้วเผยแพร่อีกครั้งไปยัง Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="01fd5-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="01fd5-177">เมื่อต้องการส่งออกการแปลงหน่วยไปยัง Excel บนหน้า **การแปลงหน่วย** บนบานหน้าต่างการดำเนินการ ให้เลือก **เปิดใน Microsoft Office**</span><span class="sxs-lookup"><span data-stu-id="01fd5-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01fd5-178">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="01fd5-178">Additional resources</span></span>

[<span data-ttu-id="01fd5-179">จัดการหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="01fd5-179">Manage unit of measure</span></span>](tasks/manage-unit-measure.md)
