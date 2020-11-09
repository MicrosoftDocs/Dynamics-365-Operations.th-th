---
title: โมดูลรถเข็น
description: หัวข้อนี้ครอบคลุมถึงโมดูลรถเข็น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: 39026ec56ebf25342410330f2ba3e2e7773dfd6a
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055438"
---
# <a name="cart-module"></a><span data-ttu-id="3bcd6-103">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="3bcd6-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3bcd6-104">หัวข้อนี้ครอบคลุมถึงโมดูลรถเข็น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3bcd6-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3bcd6-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="3bcd6-105">Overview</span></span>

<span data-ttu-id="3bcd6-106">โมดูลรถเข็นแสดงสินค้าที่มีการเพิ่มลงในรถเข็น ก่อนที่ลูกค้าจะดำเนินการเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="3bcd6-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="3bcd6-107">นอกจากนี้ โมดูลยังแสดงสรุปใบสั่งและอนุญาตให้ลูกค้าสามารถใช้หรือลบรหัสโปรโมชันได้</span><span class="sxs-lookup"><span data-stu-id="3bcd6-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="3bcd6-108">โมดูลรถเข็นสนับสนุนการชำระเงินของผู้ที่ลงชื่อเข้าใช้ และการชำระเงินของผู้เยี่ยมชม</span><span class="sxs-lookup"><span data-stu-id="3bcd6-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="3bcd6-109">นอกจากนี้ยังสนับสนุนลิงก์ **กลับไปยังการช้อปปิ้ง**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="3bcd6-110">คุณสามารถตั้งค่าคอนฟิกเส้นทางสำหรับลิงก์นี้ได้ที่ **การตั้งค่าไซต์ \> ส่วนขยาย \> เส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="3bcd6-111">โมดูลรถเข็นแสดงข้อมูลตามรหัสรถเข็น ซึ่งเป็นคุ้กกี้ของเบราว์เซอร์ที่มีอยู่ทั่วทั้งไซต์</span><span class="sxs-lookup"><span data-stu-id="3bcd6-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="3bcd6-112">รูปภาพต่อไปนี้แสดงตัวอย่างของหน้ารถเข็นบนไซต์ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="3bcd6-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![ตัวอย่างของโมดูลรถเข็นบนไซต์ Fabrikam](./media/cart2.PNG)

<span data-ttu-id="3bcd6-114">รูปภาพต่อไปนี้แสดงตัวอย่างของหน้ารถเข็นบนไซต์ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="3bcd6-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="3bcd6-115">ในตัวอย่างนี้ มีค่าธรรมเนียมการดำเนินการสำหรับสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="3bcd6-115">In this example, there is a handling fee for a line item.</span></span>

![ตัวอย่างของโมดูรถเข็นที่มีค่าธรรมเนียมการจัดการสำหรับสินค้าในรายการ](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="3bcd6-117">คุณสมบัติของโมดูลรถเข็นและช่อง</span><span class="sxs-lookup"><span data-stu-id="3bcd6-117">Cart module properties and slots</span></span>

| <span data-ttu-id="3bcd6-118">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="3bcd6-118">Property</span></span> | <span data-ttu-id="3bcd6-119">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="3bcd6-119">Values</span></span> | <span data-ttu-id="3bcd6-120">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3bcd6-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="3bcd6-121">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="3bcd6-121">Heading</span></span> | <span data-ttu-id="3bcd6-122">ข้อความหัวเรื่องและแท็กหัวเรื่อง ( **H1** , **H2** , **H3** , **H4** , **H5** หรือ **H6** )</span><span class="sxs-lookup"><span data-stu-id="3bcd6-122">Heading text and a heading tag ( **H1** , **H2** , **H3** , **H4** , **H5** , or **H6** )</span></span> | <span data-ttu-id="3bcd6-123">หัวเรื่องสำหรับรถเข็น เช่น "ถุงช้อปปิ้ง" หรือ "สินค้าในรถเข็นของคุณ"</span><span class="sxs-lookup"><span data-stu-id="3bcd6-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="3bcd6-124">แสดงข้อผิดพลาดเกี่ยวกับสินค้าคงคลังหมด</span><span class="sxs-lookup"><span data-stu-id="3bcd6-124">Show out of stock errors</span></span> | <span data-ttu-id="3bcd6-125">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-125">**True** or **False**</span></span> | <span data-ttu-id="3bcd6-126">ถ้าคุณสมบัตินี้ตั้งค่าเป็น **จริง** หน้ารถเข็นจะแสดงข้อผิดพลาดที่เกี่ยวข้องกับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="3bcd6-126">If this property is set to **True** , the cart page will show stock-related errors.</span></span> <span data-ttu-id="3bcd6-127">เราขอแนะนำให้คุณตั้งค่าคุณสมบัตินี้เป็น **จริง** ถ้ามีการใช้การตรวจสอบสินค้าคงคลังบนไซต์</span><span class="sxs-lookup"><span data-stu-id="3bcd6-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="3bcd6-128">แสดงค่าธรรมเนียมการขนส่งสำหรับสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="3bcd6-128">Show shipping charges for line items</span></span> | <span data-ttu-id="3bcd6-129">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-129">**True** or **False**</span></span> | <span data-ttu-id="3bcd6-130">ถ้ามีการตั้งค่าคุณสมบัตินี้เป็น **จริง** สินค้าในรายการของรถเข็นจะแสดงค่าธรรมเนียมการจัดส่ง ถ้ามีข้อมูลนี้อยู่</span><span class="sxs-lookup"><span data-stu-id="3bcd6-130">If this property is set to **True** , cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="3bcd6-131">คุณลักษณะนี้ไม่ได้รับการสนับสนุนในชุดรูปแบบ Fabrikam เนื่องจากผู้ใช้เลือกการจัดส่งเฉพาะในขั้นตอนเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="3bcd6-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="3bcd6-132">อย่างไรก็ตาม คุณสามารถเปิดใช้งานคุณลักษณะนี้ในลำดับงานอื่นๆ ได้ถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3bcd6-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="3bcd6-133">โมดูลที่สามารถใช้ในโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="3bcd6-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="3bcd6-134">**บล็อคข้อความ** –โมดูลนี้สนับสนุนการส่งข้อความแบบกำหนดเองในโมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="3bcd6-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="3bcd6-135">ข้อความจะถูกขับเคลื่อนโดยระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="3bcd6-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="3bcd6-136">คุณสามารถเพิ่มข้อความใดก็ได้ เช่น "สำหรับปัญหาในการสั่งซื้อของคุณ โปรดติดต่อ 1-800-Fabrikam"</span><span class="sxs-lookup"><span data-stu-id="3bcd6-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="3bcd6-137">**ตัวเลือกร้านค้า** –โมดูลนี้แสดงรายการของร้านค้าใกล้เคียง ที่มีสินค้าพร้อมสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="3bcd6-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="3bcd6-138">ซึ่งช่วยให้ผู้ใช้ป้อนสถานที่ เพื่อค้นหาร้านค้าที่อยู่ใกล้เคียง</span><span class="sxs-lookup"><span data-stu-id="3bcd6-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="3bcd6-139">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลตัวเลือกร้านค้า](store-selector.md)</span><span class="sxs-lookup"><span data-stu-id="3bcd6-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="3bcd6-140">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="3bcd6-140">Module properties</span></span>

<span data-ttu-id="3bcd6-141">โมดูลกล่องรถเข็นต่อไปนี้สามารถตั้งค่าคอนฟิกได้ที่ **การตั้งค่าไซต์ \> ส่วนขยาย** :</span><span class="sxs-lookup"><span data-stu-id="3bcd6-141">The following cart module settings can be configured at **Site Settings \> Extensions** :</span></span>

- <span data-ttu-id="3bcd6-142">**ปริมาณสูงสุด** - คุณสมบัตินี้ใช้เพื่อระบุจำนวนสูงสุดของสินค้าแต่ละรายการที่สามารถเพิ่มเข้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="3bcd6-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="3bcd6-143">ตัวอย่างเช่น ผู้ค้าปลีกอาจตั้งให้สามารถขายผลิตภัณฑ์แต่ละอย่างได้เพียง 10 ชุด ในหนึ่งธุรกรรมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3bcd6-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="3bcd6-144">**สินค้าคงคลัง** – สำหรับข้อมูลเกี่ยวกับวิธีการใช้การตั้งค่าสินค้าคงคลัง ให้ดูที่ [ใช้การตั้งค่าสินค้าคงคลัง](inventory-settings.md)</span><span class="sxs-lookup"><span data-stu-id="3bcd6-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="3bcd6-145">**กลับไปยังการช้อปปิ้ง** – คุณสมบัตินี้ใช้เพื่อระบุเส้นทางสำหรับลิงก์ **กลับไปยังการช้อปปิ้ง**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="3bcd6-146">คุณสามารถตั้งค่าคอนฟิกกระบวนการผลิตที่ระดับไซต์ ซึ่งช่วยให้ร้านค้าปลีกสามารถนำลูกค้ากลับไปยังโฮมเพจหรือหน้าอื่นๆ บนไซต์ได้</span><span class="sxs-lookup"><span data-stu-id="3bcd6-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3bcd6-147">ใน Dynamics 365 Commerce รุ่น 10.0.14 และรุ่นที่ใหม่กว่า สินค้าในรถเข็นจะรวมกันตามการตั้งค่าที่กำหนดไว้ในโพรไฟล์การทำงานแบบออนไลน์สำหรับร้านค้าออนไลน์ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="3bcd6-147">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="3bcd6-148">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างโพรไฟล์การทำงานแบบออนไลน์และตั้งค่าคุณสมบัติที่จำเป็นสำหรับการรวม โปรดดู [สร้างโพรไฟล์การทำงานแบบออนไลน์](online-functionality-profile.md)</span><span class="sxs-lookup"><span data-stu-id="3bcd6-148">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="3bcd6-149">การโต้ตอบ Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="3bcd6-149">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="3bcd6-150">โมดูลของรถเข็นจะดึงข้อมูลผลิตภัณฑ์โดยใช้ Commerce Scale Unit APIs</span><span class="sxs-lookup"><span data-stu-id="3bcd6-150">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="3bcd6-151">รหัสรถเข็นจากคุกกี้ของเบราว์เซอร์ใช้เพื่อดึงข้อมูลผลิตภัณฑ์ทั้งหมดจาก Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="3bcd6-151">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="3bcd6-152">เพิ่มโมดูลรถเข็นไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="3bcd6-152">Add a cart module to a page</span></span>

<span data-ttu-id="3bcd6-153">การเพิ่มโมดูลรถเข็นไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3bcd6-153">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3bcd6-154">ไปที่ **ส่วนย่อย** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="3bcd6-154">Go to **Fragments** , and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="3bcd6-155">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือกโมดูล **รถเข็น**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-155">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="3bcd6-156">ภายใต้ **ชื่อส่วนย่อย** ให้ป้อนชื่อสำหรับ **ส่วนย่อยรถเข็น** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-156">Under **Fragment name** , enter the name **Cart fragment** , and then select **OK**.</span></span>
1. <span data-ttu-id="3bcd6-157">เลือกช่อง **รถเข็น**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-157">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="3bcd6-158">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือกสัญลักษณ์ดินสอ ป้อนข้อความหัวข้อในฟิลด์ แล้วเลือกสัญลักษณ์เครื่องหมายถูก</span><span class="sxs-lookup"><span data-stu-id="3bcd6-158">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="3bcd6-159">ในช่อง **รถเข็น** เลือกจุดไข่ปลา ( **...** ) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-159">In the **Cart** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3bcd6-160">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ตัวเลือกร้านค้า** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-160">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3bcd6-161">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วน และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="3bcd6-161">Select **Save** , select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="3bcd6-162">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="3bcd6-162">Go to **Templates** , and select **New** to create a new template.</span></span>
1. <span data-ttu-id="3bcd6-163">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อนชื่อของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="3bcd6-163">In the **New Template** dialog box, under **Template name** , enter a name for the template.</span></span>
1. <span data-ttu-id="3bcd6-164">ในแผนภูมิเค้าร่าง ให้เลือกช่อง **เนื้อหา** เลือกปุ่มจุดไข่ปลา ( **...** ) จากนั้นเลือก **เพิ่มส่วนย่อย**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-164">In the outline tree, select the **Body** slot, select the ellipsis ( **...** ), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="3bcd6-165">ในกล่องโต้ตอบ **เลือกส่วนย่อย** ให้เลือกส่วนย่อย **ส่วนย่อยรถเข็น** ที่คุณสร้างไว้ก่อนหน้า แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-165">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="3bcd6-166">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="3bcd6-166">Select **Save** , select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="3bcd6-167">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="3bcd6-167">Go to **Pages** , and select **New** to create a new page.</span></span>
1. <span data-ttu-id="3bcd6-168">ในกล่องโต้ตอบ **เลือกเท็มเพลต** ให้เลือกเท็มเพลตที่คุณสร้างไว้ ป้อนชื่อหน้า แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3bcd6-168">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="3bcd6-169">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="3bcd6-169">Select **Save** , and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="3bcd6-170">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="3bcd6-170">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3bcd6-171">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3bcd6-171">Additional resources</span></span>

[<span data-ttu-id="3bcd6-172">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="3bcd6-172">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="3bcd6-173">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="3bcd6-173">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3bcd6-174">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="3bcd6-174">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="3bcd6-175">โมดูลที่อยู่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="3bcd6-175">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="3bcd6-176">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="3bcd6-176">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="3bcd6-177">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3bcd6-177">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3bcd6-178">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="3bcd6-178">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="3bcd6-179">คำนวณความพร้อมของสินค้าคงคลังสำหรับช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="3bcd6-179">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="3bcd6-180">สร้างโพรไฟล์ฟังก์ชันการทำงานออนไลน์</span><span class="sxs-lookup"><span data-stu-id="3bcd6-180">Create an online functionality profile</span></span>](online-functionality-profile.md)
