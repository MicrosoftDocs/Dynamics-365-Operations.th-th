---
title: โมดูลรถเข็น
description: หัวข้อนี้ครอบคลุมถึงโมดูลรถเข็น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f21268ed4cffed1d5c789f722796cdf05e965819
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621047"
---
# <a name="cart-module"></a><span data-ttu-id="13723-103">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="13723-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="13723-104">หัวข้อนี้ครอบคลุมถึงโมดูลรถเข็น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="13723-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="13723-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="13723-105">Overview</span></span>

<span data-ttu-id="13723-106">โมดูลรถเข็นแสดงสินค้าที่มีการเพิ่มลงในรถเข็น ก่อนที่ลูกค้าจะดำเนินการเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="13723-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="13723-107">นอกจากนี้ โมดูลยังแสดงสรุปใบสั่งและอนุญาตให้ลูกค้าสามารถใช้หรือลบรหัสโปรโมชันได้</span><span class="sxs-lookup"><span data-stu-id="13723-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="13723-108">โมดูลรถเข็นสนับสนุนการชำระเงินของผู้ที่ลงชื่อเข้าใช้ และการชำระเงินของผู้เยี่ยมชม</span><span class="sxs-lookup"><span data-stu-id="13723-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="13723-109">นอกจากนี้ยังสนับสนุนลิงก์ **กลับไปยังการช้อปปิ้ง**</span><span class="sxs-lookup"><span data-stu-id="13723-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="13723-110">คุณสามารถตั้งค่าคอนฟิกเส้นทางสำหรับลิงก์นี้ได้ที่ **การตั้งค่าไซต์ \> ส่วนขยาย \> เส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="13723-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="13723-111">โมดูลรถเข็นแสดงข้อมูลตามรหัสรถเข็น ซึ่งเป็นคุ้กกี้ของเบราว์เซอร์ที่มีอยู่ทั่วทั้งไซต์</span><span class="sxs-lookup"><span data-stu-id="13723-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="13723-112">รูปภาพต่อไปนี้แสดงตัวอย่างของหน้ารถเข็นบนไซต์ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="13723-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![ตัวอย่างของโมดูลรถเข็น](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="13723-114">คุณสมบัติของโมดูลรถเข็นและช่อง</span><span class="sxs-lookup"><span data-stu-id="13723-114">Cart module properties and slots</span></span>

<span data-ttu-id="13723-115">โมดูลรถเข็นมีคุณสมบัติ **หัวข้อ** ซึ่งสามารถตั้งค่าเป็นค่าต่าง ๆ เช่น **ถุงช้อปปิ้ง** และ **สินค้าในรถเข็นของคุณ**</span><span class="sxs-lookup"><span data-stu-id="13723-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="13723-116">โมดูลที่สามารถใช้ในโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="13723-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="13723-117">**บล็อคข้อความ** –โมดูลนี้สนับสนุนการส่งข้อความแบบกำหนดเองในโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="13723-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="13723-118">ข้อความจะถูกขับเคลื่อนโดยระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="13723-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="13723-119">คุณสามารถเพิ่มข้อความใดก็ได้ เช่น "สำหรับปัญหาในการสั่งซื้อของคุณ โปรดติดต่อ 1-800-Fabrikam"</span><span class="sxs-lookup"><span data-stu-id="13723-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="13723-120">**ตัวเลือกร้านค้า** –โมดูลนี้แสดงรายการของร้านค้าใกล้เคียง ที่มีสินค้าพร้อมสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="13723-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="13723-121">ซึ่งช่วยให้ผู้ใช้ป้อนสถานที่ เพื่อค้นหาร้านค้าที่อยู่ใกล้เคียง</span><span class="sxs-lookup"><span data-stu-id="13723-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="13723-122">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลตัวเลือกร้านค้า](store-selector.md)</span><span class="sxs-lookup"><span data-stu-id="13723-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="13723-123">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="13723-123">Module properties</span></span>

<span data-ttu-id="13723-124">โมดูลกล่องรถเข็นต่อไปนี้สามารถตั้งค่าคอนฟิกได้ที่ **การตั้งค่าไซต์ \> ส่วนขยาย**:</span><span class="sxs-lookup"><span data-stu-id="13723-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="13723-125">**ปริมาณสูงสุด** - คุณสมบัตินี้ใช้เพื่อระบุจำนวนสูงสุดของสินค้าแต่ละรายการที่สามารถเพิ่มเข้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="13723-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="13723-126">ตัวอย่างเช่น ผู้ค้าปลีกอาจตั้งให้สามารถขายผลิตภัณฑ์แต่ละอย่างได้เพียง 10 ชุด ในหนึ่งธุรกรรมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="13723-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="13723-127">**สินค้าคงคลัง** – สำหรับข้อมูลเกี่ยวกับวิธีการใช้การตั้งค่าสินค้าคงคลัง ให้ดูที่ [ใช้การตั้งค่าสินค้าคงคลัง](inventory-settings.md)</span><span class="sxs-lookup"><span data-stu-id="13723-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="13723-128">**กลับไปยังการช้อปปิ้ง** – คุณสมบัตินี้ใช้เพื่อระบุเส้นทางสำหรับลิงก์ **กลับไปยังการช้อปปิ้ง**</span><span class="sxs-lookup"><span data-stu-id="13723-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="13723-129">คุณสามารถตั้งค่าคอนฟิกกระบวนการผลิตที่ระดับไซต์ ซึ่งช่วยให้ร้านค้าปลีกสามารถนำลูกค้ากลับไปยังโฮมเพจหรือหน้าอื่นๆ บนไซต์ได้</span><span class="sxs-lookup"><span data-stu-id="13723-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="13723-130">การโต้ตอบ Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="13723-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="13723-131">โมดูลของรถเข็นจะดึงข้อมูลผลิตภัณฑ์โดยใช้ Commerce Scale Unit APIs</span><span class="sxs-lookup"><span data-stu-id="13723-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="13723-132">รหัสรถเข็นจากคุกกี้ของเบราว์เซอร์ใช้เพื่อดึงข้อมูลผลิตภัณฑ์ทั้งหมดจาก Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="13723-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="13723-133">เพิ่มโมดูลรถเข็นไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="13723-133">Add a cart module to a page</span></span>

<span data-ttu-id="13723-134">การเพิ่มโมดูลรถเข็นไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="13723-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="13723-135">ไปที่ **ส่วนของเพจ** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="13723-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="13723-136">ในกล่องโต้ตอบ **ส่วนย่อยของหน้าใหม่** ให้เลือกโมดูล **รถเข็น**</span><span class="sxs-lookup"><span data-stu-id="13723-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="13723-137">ภายใต้ **ชื่อส่วนย่อยของหน้า** ให้ป้อนชื่อสำหรับ **ส่วนย่อยรถเข็น** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="13723-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="13723-138">เลือกช่อง **รถเข็น**</span><span class="sxs-lookup"><span data-stu-id="13723-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="13723-139">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือกสัญลักษณ์ดินสอ ป้อนข้อความหัวข้อในฟิลด์ แล้วเลือกสัญลักษณ์เครื่องหมายถูก</span><span class="sxs-lookup"><span data-stu-id="13723-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="13723-140">ในช่อง **รถเข็น** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="13723-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="13723-141">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ตัวเลือกร้านค้า** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="13723-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="13723-142">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วน และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="13723-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="13723-143">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="13723-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="13723-144">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อนชื่อของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="13723-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="13723-145">ในแผนภูมิเค้าร่าง ให้เลือกช่อง **เนื้อหา** เลือกปุ่มจุดไข่ปลา (**...**) จากนั้นเลือก **เพิ่มส่วนย่อย**</span><span class="sxs-lookup"><span data-stu-id="13723-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="13723-146">ในกล่องโต้ตอบ **เลือกส่วนย่อยของหน้า** ให้เลือกส่วนย่อย **ส่วนย่อยรถเข็น** ที่คุณสร้างไว้ก่อนหน้า แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="13723-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="13723-147">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="13723-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="13723-148">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="13723-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="13723-149">ในกล่องโต้ตอบ **เลือกเท็มเพลต** ให้เลือกเท็มเพลตที่คุณสร้างไว้ ป้อนชื่อหน้า แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="13723-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="13723-150">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="13723-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="13723-151">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="13723-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13723-152">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="13723-152">Additional resources</span></span>

[<span data-ttu-id="13723-153">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="13723-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="13723-154">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="13723-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="13723-155">โมดูลตัวเลือกการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="13723-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="13723-156">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="13723-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="13723-157">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="13723-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="13723-158">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="13723-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="13723-159">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="13723-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="13723-160">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="13723-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="13723-161">โมดูลส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="13723-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="13723-162">คำนวณความพร้อมของสินค้าคงคลังสำหรับช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="13723-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
