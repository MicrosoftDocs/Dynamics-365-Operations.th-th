---
title: โมดูลรถเข็น
description: หัวข้อนี้ครอบคลุมโมดูลบรรทุกและอธิบายวิธีการเพิ่มไปยังหน้าไซต์ใน Microsoft Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5b0ce69f57e6ba691803752280466b41ced7c521
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206498"
---
# <a name="cart-module"></a><span data-ttu-id="f7f12-103">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="f7f12-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f7f12-104">หัวข้อนี้ครอบคลุมโมดูลบรรทุกและอธิบายวิธีการเพิ่มไปยังหน้าไซต์ใน Microsoft Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f7f12-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f7f12-105">โมดูลรถเข็นแสดงสินค้าที่มีการเพิ่มลงในรถเข็น ก่อนที่ลูกค้าจะดำเนินการเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="f7f12-105">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="f7f12-106">นอกจากนี้ โมดูลยังแสดงสรุปใบสั่งและอนุญาตให้ลูกค้าสามารถใช้หรือลบรหัสโปรโมชันได้</span><span class="sxs-lookup"><span data-stu-id="f7f12-106">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="f7f12-107">โมดูลรถเข็นสนับสนุนการชำระเงินของผู้ที่ลงชื่อเข้าใช้ และการชำระเงินของผู้เยี่ยมชม</span><span class="sxs-lookup"><span data-stu-id="f7f12-107">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="f7f12-108">นอกจากนี้ยังสนับสนุนลิงก์ **กลับไปยังการช้อปปิ้ง**</span><span class="sxs-lookup"><span data-stu-id="f7f12-108">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="f7f12-109">คุณสามารถตั้งค่าคอนฟิกเส้นทางสำหรับลิงก์นี้ได้ที่ **การตั้งค่าไซต์ \> ส่วนขยาย \> เส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="f7f12-109">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="f7f12-110">โมดูลรถเข็นแสดงข้อมูลตามรหัสรถเข็น ซึ่งเป็นคุ้กกี้ของเบราว์เซอร์ที่มีอยู่ทั่วทั้งไซต์</span><span class="sxs-lookup"><span data-stu-id="f7f12-110">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="f7f12-111">รูปภาพต่อไปนี้แสดงตัวอย่างของหน้ารถเข็นบนไซต์ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="f7f12-111">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![ตัวอย่างของโมดูลรถเข็นบนไซต์ Fabrikam](./media/cart2.PNG)

<span data-ttu-id="f7f12-113">รูปภาพต่อไปนี้แสดงตัวอย่างของหน้ารถเข็นบนไซต์ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="f7f12-113">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="f7f12-114">ในตัวอย่างนี้ มีค่าธรรมเนียมการดำเนินการสำหรับสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="f7f12-114">In this example, there is a handling fee for a line item.</span></span>

![ตัวอย่างของโมดูรถเข็นที่มีค่าธรรมเนียมการจัดการสำหรับสินค้าในรายการ](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="f7f12-116">คุณสมบัติของโมดูลรถเข็นและช่อง</span><span class="sxs-lookup"><span data-stu-id="f7f12-116">Cart module properties and slots</span></span>

| <span data-ttu-id="f7f12-117">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="f7f12-117">Property</span></span> | <span data-ttu-id="f7f12-118">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="f7f12-118">Values</span></span> | <span data-ttu-id="f7f12-119">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f7f12-119">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="f7f12-120">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="f7f12-120">Heading</span></span> | <span data-ttu-id="f7f12-121">ข้อความหัวเรื่องและแท็กหัวเรื่อง (**H1**, **H2**, **H3**, **H4**, **H5** หรือ **H6**)</span><span class="sxs-lookup"><span data-stu-id="f7f12-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="f7f12-122">หัวเรื่องสำหรับรถเข็น เช่น "ถุงช้อปปิ้ง" หรือ "สินค้าในรถเข็นของคุณ"</span><span class="sxs-lookup"><span data-stu-id="f7f12-122">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="f7f12-123">แสดงข้อผิดพลาดเกี่ยวกับสินค้าคงคลังหมด</span><span class="sxs-lookup"><span data-stu-id="f7f12-123">Show out of stock errors</span></span> | <span data-ttu-id="f7f12-124">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="f7f12-124">**True** or **False**</span></span> | <span data-ttu-id="f7f12-125">ถ้าคุณสมบัตินี้ตั้งค่าเป็น **จริง** หน้ารถเข็นจะแสดงข้อผิดพลาดที่เกี่ยวข้องกับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="f7f12-125">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="f7f12-126">เราขอแนะนำให้คุณตั้งค่าคุณสมบัตินี้เป็น **จริง** ถ้ามีการใช้การตรวจสอบสินค้าคงคลังบนไซต์</span><span class="sxs-lookup"><span data-stu-id="f7f12-126">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="f7f12-127">แสดงค่าธรรมเนียมการขนส่งสำหรับสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="f7f12-127">Show shipping charges for line items</span></span> | <span data-ttu-id="f7f12-128">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="f7f12-128">**True** or **False**</span></span> | <span data-ttu-id="f7f12-129">ถ้ามีการตั้งค่าคุณสมบัตินี้เป็น **จริง** สินค้าในรายการของรถเข็นจะแสดงค่าธรรมเนียมการจัดส่ง ถ้ามีข้อมูลนี้อยู่</span><span class="sxs-lookup"><span data-stu-id="f7f12-129">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="f7f12-130">คุณลักษณะนี้ไม่ได้รับการสนับสนุนในชุดรูปแบบ Fabrikam เนื่องจากผู้ใช้เลือกการจัดส่งเฉพาะในขั้นตอนเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="f7f12-130">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="f7f12-131">อย่างไรก็ตาม คุณสามารถเปิดใช้งานคุณลักษณะนี้ในลำดับงานอื่นๆ ได้ถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f7f12-131">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="f7f12-132">แสดงโปรโมชันที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="f7f12-132">Show available promotions</span></span>| <span data-ttu-id="f7f12-133">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="f7f12-133">**True** or **False**</span></span> | <span data-ttu-id="f7f12-134">หากคุณสมบัตินี้ถูกตั้งค่าเป็น **จริง** รถเข็นจะแสดงโปรโมชันที่พร้อมใช้งานตามสินค้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="f7f12-134">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="f7f12-135">ความสามารถนี้พร้อมใช้งานในรุ่น Dynamics 365 Commerce 10.0.16</span><span class="sxs-lookup"><span data-stu-id="f7f12-135">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="f7f12-136">โมดูลที่สามารถใช้ในโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="f7f12-136">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="f7f12-137">**บล็อคข้อความ** –โมดูลนี้สนับสนุนการส่งข้อความแบบกำหนดเองในโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="f7f12-137">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="f7f12-138">ข้อความจะถูกขับเคลื่อนโดยระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="f7f12-138">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="f7f12-139">คุณสามารถเพิ่มข้อความใดก็ได้ เช่น "สำหรับปัญหาในการสั่งซื้อของคุณ โปรดติดต่อ 1-800-Fabrikam"</span><span class="sxs-lookup"><span data-stu-id="f7f12-139">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="f7f12-140">**ตัวเลือกร้านค้า** –โมดูลนี้แสดงรายการของร้านค้าใกล้เคียง ที่มีสินค้าพร้อมสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="f7f12-140">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="f7f12-141">ซึ่งช่วยให้ผู้ใช้ป้อนสถานที่ เพื่อค้นหาร้านค้าที่อยู่ใกล้เคียง</span><span class="sxs-lookup"><span data-stu-id="f7f12-141">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="f7f12-142">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลตัวเลือกร้านค้า](store-selector.md)</span><span class="sxs-lookup"><span data-stu-id="f7f12-142">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="f7f12-143">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="f7f12-143">Module properties</span></span>

<span data-ttu-id="f7f12-144">โมดูลกล่องรถเข็นต่อไปนี้สามารถตั้งค่าคอนฟิกได้ที่ **การตั้งค่าไซต์ \> ส่วนขยาย**:</span><span class="sxs-lookup"><span data-stu-id="f7f12-144">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="f7f12-145">**ปริมาณสูงสุด** - คุณสมบัตินี้ใช้เพื่อระบุจำนวนสูงสุดของสินค้าแต่ละรายการที่สามารถเพิ่มเข้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="f7f12-145">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="f7f12-146">ตัวอย่างเช่น ผู้ค้าปลีกอาจตั้งให้สามารถขายผลิตภัณฑ์แต่ละอย่างได้เพียง 10 ชุด ในหนึ่งธุรกรรมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f7f12-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="f7f12-147">**สินค้าคงคลัง** – สำหรับข้อมูลเกี่ยวกับวิธีการใช้การตั้งค่าสินค้าคงคลัง ให้ดูที่ [ใช้การตั้งค่าสินค้าคงคลัง](inventory-settings.md)</span><span class="sxs-lookup"><span data-stu-id="f7f12-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="f7f12-148">**กลับไปยังการช้อปปิ้ง** – คุณสมบัตินี้ใช้เพื่อระบุเส้นทางสำหรับลิงก์ **กลับไปยังการช้อปปิ้ง**</span><span class="sxs-lookup"><span data-stu-id="f7f12-148">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="f7f12-149">คุณสามารถตั้งค่าคอนฟิกกระบวนการผลิตที่ระดับไซต์ ซึ่งช่วยให้ร้านค้าปลีกสามารถนำลูกค้ากลับไปยังโฮมเพจหรือหน้าอื่นๆ บนไซต์ได้</span><span class="sxs-lookup"><span data-stu-id="f7f12-149">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7f12-150">ใน Dynamics 365 Commerce รุ่น 10.0.14 และรุ่นที่ใหม่กว่า สินค้าในรถเข็นจะรวมกันตามการตั้งค่าที่กำหนดไว้ในโพรไฟล์การทำงานแบบออนไลน์สำหรับร้านค้าออนไลน์ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="f7f12-150">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="f7f12-151">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างโพรไฟล์การทำงานแบบออนไลน์และตั้งค่าคุณสมบัติที่จำเป็นสำหรับการรวม โปรดดู [สร้างโพรไฟล์การทำงานแบบออนไลน์](online-functionality-profile.md)</span><span class="sxs-lookup"><span data-stu-id="f7f12-151">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="f7f12-152">การโต้ตอบ Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="f7f12-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="f7f12-153">โมดูลของรถเข็นจะดึงข้อมูลผลิตภัณฑ์โดยใช้ Commerce Scale Unit APIs</span><span class="sxs-lookup"><span data-stu-id="f7f12-153">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="f7f12-154">รหัสรถเข็นจากคุกกี้ของเบราว์เซอร์ใช้เพื่อดึงข้อมูลผลิตภัณฑ์ทั้งหมดจาก Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="f7f12-154">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="f7f12-155">เพิ่มโมดูลรถเข็นไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="f7f12-155">Add a cart module to a page</span></span>

<span data-ttu-id="f7f12-156">การเพิ่มโมดูลรถเข็นไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7f12-156">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f7f12-157">ไปที่ **ส่วนย่อย** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="f7f12-157">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="f7f12-158">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือกโมดูล **รถเข็น**</span><span class="sxs-lookup"><span data-stu-id="f7f12-158">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="f7f12-159">ภายใต้ **ชื่อส่วนย่อย** ให้ป้อนชื่อสำหรับ **ส่วนย่อยรถเข็น** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f7f12-159">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="f7f12-160">เลือกช่อง **รถเข็น**</span><span class="sxs-lookup"><span data-stu-id="f7f12-160">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="f7f12-161">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือกสัญลักษณ์ดินสอ ป้อนข้อความหัวข้อในฟิลด์ แล้วเลือกสัญลักษณ์เครื่องหมายถูก</span><span class="sxs-lookup"><span data-stu-id="f7f12-161">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="f7f12-162">ในช่อง **รถเข็น** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="f7f12-162">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f7f12-163">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ตัวเลือกร้านค้า** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f7f12-163">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f7f12-164">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วน และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f7f12-164">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f7f12-165">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="f7f12-165">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f7f12-166">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อนชื่อของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f7f12-166">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="f7f12-167">ในแผนภูมิเค้าร่าง ให้เลือกช่อง **เนื้อหา** เลือกปุ่มจุดไข่ปลา (**...**) จากนั้นเลือก **เพิ่มส่วนย่อย**</span><span class="sxs-lookup"><span data-stu-id="f7f12-167">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="f7f12-168">ในกล่องโต้ตอบ **เลือกส่วนย่อย** ให้เลือกส่วนย่อย **ส่วนย่อยรถเข็น** ที่คุณสร้างไว้ก่อนหน้า แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f7f12-168">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="f7f12-169">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f7f12-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f7f12-170">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="f7f12-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="f7f12-171">ในกล่องโต้ตอบ **เลือกเท็มเพลต** ให้เลือกเท็มเพลตที่คุณสร้างไว้ ป้อนชื่อหน้า แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f7f12-171">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="f7f12-172">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="f7f12-172">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="f7f12-173">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f7f12-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7f12-174">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f7f12-174">Additional resources</span></span>

[<span data-ttu-id="f7f12-175">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="f7f12-175">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f7f12-176">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="f7f12-176">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f7f12-177">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f7f12-177">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="f7f12-178">โมดูลที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f7f12-178">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="f7f12-179">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f7f12-179">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="f7f12-180">โมดูลข้อมูลการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="f7f12-180">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="f7f12-181">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="f7f12-181">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f7f12-182">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="f7f12-182">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="f7f12-183">คำนวณความพร้อมของสินค้าคงคลังสำหรับช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="f7f12-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="f7f12-184">สร้างโพรไฟล์ฟังก์ชันการทำงานออนไลน์</span><span class="sxs-lookup"><span data-stu-id="f7f12-184">Create an online functionality profile</span></span>](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]