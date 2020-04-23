---
title: การแปลงหน่วยวัดต่อผลิตภัณฑ์ย่อย
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการแปลงหน่วยวัดในผลิตภัณฑ์ย่อย
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: e50be7fa6fa686a90b2dd5c5200c881e4629f019
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204504"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="b901d-103">การแปลงหน่วยวัดต่อผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="b901d-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b901d-104">หัวข้อนี้อธิบายวิธีการตั้งค่าการแปลงหน่วยวัดในผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="b901d-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="b901d-105">ซึ่งรวมตัวอย่างของการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="b901d-105">It includes an example of the setup.</span></span>

<span data-ttu-id="b901d-106">คุณลักษณะนี้ช่วยให้บริษัทสามารถกำหนดการแปลงหน่วยที่แตกต่างกันระหว่างผลิตภัณฑ์ย่อยของผลิตภัณฑ์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="b901d-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="b901d-107">ตัวอย่างต่อไปนี้จะใช้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="b901d-107">The following example is used in this topic.</span></span> <span data-ttu-id="b901d-108">บริษัทขายเสื้อยืดขนาดเล็ก ขนาดกลาง ขนาดใหญ่ และขนาดใหญ่พิเศษ</span><span class="sxs-lookup"><span data-stu-id="b901d-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="b901d-109">เสื้อยืดถูกกำหนดให้เป็นผลิตภัณฑ์ และขนาดที่แตกต่างกันจะถูกกำหนดเป็นผลิตภัณฑ์ย่อยของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b901d-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="b901d-110">เสื้อยืดถูกบรรจุในกล่อง และอาจมีเสื้อยืดห้าตัวในกล่อง ยกเว้นขนาดใหญ่พิเศษที่มีพื้นที่สำหรับเสื้อยืดสี่ตัวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b901d-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="b901d-111">บริษัทต้องการติดตามผลิตภัณฑ์ย่อยที่แตกต่างกันของเสื้อยืดในหน่วย **ชิ้น** แต่ขายเสื้อยืดในหน่วย **กล่อง**</span><span class="sxs-lookup"><span data-stu-id="b901d-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="b901d-112">การแปลงระหว่างหน่วยสินค้าคงคลังและหน่วยการขายคือ 1 กล่อง = 5 ชิ้น ยกเว้นขนาดใหญ่พิเศษของผลิตภัณฑ์ย่อยที่การแปลงเป็น 1 กล่อง = 4 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="b901d-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="b901d-113">ตั้งค่าผลิตภัณฑ์สำหรับการแปลงหน่วยสำหรับแต่ละผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="b901d-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="b901d-114">คุณสามารถสร้างได้เฉพาะผลิตภัณฑ์ย่อยสำหรับผลิตภัณฑ์ของ **ชนิดย่อยของผลิตภัณฑ์**: **ผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="b901d-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="b901d-115">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างผลิตภัณฑ์หลัก](tasks/create-product-master.md)</span><span class="sxs-lookup"><span data-stu-id="b901d-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="b901d-116">ไม่มีการเปิดใช้งานคุณลักษณะสำหรับผลิตภัณฑ์ที่มีตั้งค่าสำหรับกระบวนการตามน้ำหนักจริง</span><span class="sxs-lookup"><span data-stu-id="b901d-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="b901d-117">เมื่อมีการสร้างผลิตภัณฑ์หลักที่มีผลิตภัณฑ์ย่อยที่นำออกใช้ การแปลงหน่วยสำหรับแต่ละผลิตภัณฑ์ย่อยจะสามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="b901d-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="b901d-118">คุณสามารถค้นหารายการเมนูสำหรับการเปิดหน้าการแปลงหน่วยได้ ในบริบทของผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยในหน้าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b901d-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="b901d-119">หน้า **รายละเอียดผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="b901d-119">**Product details** page</span></span>
-   <span data-ttu-id="b901d-120">หน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="b901d-120">**Released products details** page</span></span>
-   <span data-ttu-id="b901d-121">หน้า **ผลิตภัณฑ์ย่อยที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="b901d-121">**Released product variants** page</span></span>

<span data-ttu-id="b901d-122">เมื่อคุณเปิดหน้า **การแปลงหน่วย** ในบริบทของผลิตภัณฑ์หลักหรือผลิตภัณฑ์ย่อยที่นำออกใช้ คุณสามารถเลือกว่าคุณต้องการตั้งค่าการแปลงหน่วยสำหรับผลิตภัณฑ์ หรือสำหรับผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="b901d-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="b901d-123">คุณทำเช่นนั้นโดยเลือก **ผลิตภัณฑ์ย่อย** หรือ **ผลิตภัณฑ์** ในฟิลด์ **สร้างการแปลงสำหรับ**</span><span class="sxs-lookup"><span data-stu-id="b901d-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="b901d-124">ผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="b901d-124">Product variant</span></span>

<span data-ttu-id="b901d-125">ถ้าคุณเลือก **ผลิตภัณฑ์ย่อย** จากนั้นคุณสามารถเลือกตัวแปรที่คุณต้องการตั้งค่าการแปลงหน่วยในฟิลด์ **ผลิตภัณฑ์ย่อย**</span><span class="sxs-lookup"><span data-stu-id="b901d-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="b901d-126">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b901d-126">Product</span></span>

<span data-ttu-id="b901d-127">ถ้าคุณเลือก **ผลิตภัณฑ์** จากนั้นคุณสามารถตั้งค่าการแปลงหน่วยสำหรับผลิตภัณฑ์หลักได้</span><span class="sxs-lookup"><span data-stu-id="b901d-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="b901d-128">การแปลงหน่วยนี้จะใช้สำหรับผลิตภัณฑ์ย่อยทั้งหมดโดยไม่มีการแปลงหน่วยที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="b901d-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="b901d-129">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b901d-129">Example</span></span>

<span data-ttu-id="b901d-130">ผลิตภัณฑ์หลัก **เสื้อยืด** มีผลิตภัณฑ์ย่อยที่นำออกใช้สี่ขนาด เล็ก กลาง ใหญ่ และใหญ่พิเศษ</span><span class="sxs-lookup"><span data-stu-id="b901d-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="b901d-131">เสื้อยืดถูกบรรจุในกล่อง และอาจมีเสื้อยืดห้าตัวในกล่อง ยกเว้นขนาดใหญ่พิเศษที่มีพื้นที่สำหรับเสื้อยืดสี่ตัวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b901d-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="b901d-132">อันดับแรก เปิดหน้า **การแปลงหน่วย** จากหน้ารายละเอียดผลิตภัณฑ์ที่นำออกใช้สำหรับ **เสื้อยืด**</span><span class="sxs-lookup"><span data-stu-id="b901d-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="b901d-133">ในหน้า **การแปลงหน่วย** ตั้งค่าการแปลงหน่วยสำหรับผลิตภัณฑ์ย่อยขนาดใหญ่พิเศษที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="b901d-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="b901d-134">**ฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="b901d-134">**Field**</span></span>             | <span data-ttu-id="b901d-135">**การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="b901d-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="b901d-136">สร้างการแปลงสำหรับ</span><span class="sxs-lookup"><span data-stu-id="b901d-136">Create conversion for</span></span> | <span data-ttu-id="b901d-137">ผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="b901d-137">Product variant</span></span>         |
| <span data-ttu-id="b901d-138">ผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="b901d-138">Product variant</span></span>       | <span data-ttu-id="b901d-139">เสื้อยืด : : ใหญ่พิเศษ : :</span><span class="sxs-lookup"><span data-stu-id="b901d-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="b901d-140">หน่วยเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b901d-140">From unit</span></span>             | <span data-ttu-id="b901d-141">กล่อง</span><span class="sxs-lookup"><span data-stu-id="b901d-141">Boxes</span></span>                   |
| <span data-ttu-id="b901d-142">แฟคเตอร์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="b901d-142">Factor</span></span>                | <span data-ttu-id="b901d-143">4</span><span class="sxs-lookup"><span data-stu-id="b901d-143">4</span></span>                       |
| <span data-ttu-id="b901d-144">หน่วยเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b901d-144">To Unit</span></span>               | <span data-ttu-id="b901d-145">ชิ้น</span><span class="sxs-lookup"><span data-stu-id="b901d-145">Pieces</span></span>                  |

<span data-ttu-id="b901d-146">ผลิตภัณฑ์ย่อยที่นำออกใช้ขนาดเล็ก กลาง และใหญ่ มีหน่วยการแปลงเดียวกันระหว่างหน่วยกล่องและชิ้น ซึ่งหมายความว่า คุณสามารถกำหนดการแปลงหน่วยสำหรับผลิตภัณฑ์ย่อยเหล่านี้ในผลิตภัณฑ์หลักได้</span><span class="sxs-lookup"><span data-stu-id="b901d-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="b901d-147">**ฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="b901d-147">**Field**</span></span>             | <span data-ttu-id="b901d-148">**การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="b901d-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b901d-149">สร้างการแปลงสำหรับ</span><span class="sxs-lookup"><span data-stu-id="b901d-149">Create conversion for</span></span> | <span data-ttu-id="b901d-150">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b901d-150">Product</span></span>     |
| <span data-ttu-id="b901d-151">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b901d-151">Product</span></span>               | <span data-ttu-id="b901d-152">เสื้อยืด</span><span class="sxs-lookup"><span data-stu-id="b901d-152">T-Shirt</span></span>     |
| <span data-ttu-id="b901d-153">หน่วยเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b901d-153">From unit</span></span>             | <span data-ttu-id="b901d-154">กล่อง</span><span class="sxs-lookup"><span data-stu-id="b901d-154">Boxes</span></span>       |
| <span data-ttu-id="b901d-155">แฟคเตอร์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="b901d-155">Factor</span></span>                | <span data-ttu-id="b901d-156">5</span><span class="sxs-lookup"><span data-stu-id="b901d-156">5</span></span>           |
| <span data-ttu-id="b901d-157">หน่วยเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b901d-157">To Unit</span></span>               | <span data-ttu-id="b901d-158">ชิ้น</span><span class="sxs-lookup"><span data-stu-id="b901d-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="b901d-159">การใช้ Excel เพื่ออัพเดตการแปลงหน่วย</span><span class="sxs-lookup"><span data-stu-id="b901d-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="b901d-160">ถ้าผลิตภัณฑ์มีหลายผลิตภัณฑ์ย่อยที่มีการแปลงหน่วยที่แตกต่างกัน เป็นความคิดที่ดีในการส่งออกการแปลงหน่วยจากหน้า **การแปลงหน่วย** ไปยังแผ่นตาราง Excel อัพเดตการแปลง และจากนั้นเผยแพร่กลับไปยัง Supply Chain Mangement</span><span class="sxs-lookup"><span data-stu-id="b901d-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="b901d-161">มีการเปิดใช้งานตัวเลือกที่จะส่งออกไปยัง Excel และเผยแพร่การแก้ไขกลับไปยัง Supply Chain Mangement จากรายการเมนู **เปิดใน Microsoft office** บนบานหน้าต่างการดำเนินการบนหน้า **การแปลงหน่วย**</span><span class="sxs-lookup"><span data-stu-id="b901d-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
