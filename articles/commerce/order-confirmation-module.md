---
title: โมดูลการยืนยันใบสั่ง
description: หัวข้อนี้ครอบคลุมถึงโมดูลการยืนยันใบสั่งและอธิบายวิธีการใช้ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 407fc2724d4b589ef5f611974f9358e879dba7ed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257158"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="472ce-103">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="472ce-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="472ce-104">หัวข้อนี้ครอบคลุมถึงโมดูลการยืนยันใบสั่งและอธิบายวิธีการใช้ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="472ce-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="472ce-105">โมดูลการยืนยันใบสั่งใช้เพื่อแสดงรายละเอียดการยืนยันคำสั่งซื้อหลังจากที่มีการวางใบสั่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="472ce-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="472ce-106">เป็นการแสดงรหัสยืนยันใบสั่ง ข้อมูลการติดต่อเพื่อสั่งซื้อ และรายละเอียดการสั่งซื้ออื่น ๆ เช่นรายการที่ซื้อ ข้อมูลการชำระเงิน ตัวเลือกการเบิกสินค้า และวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="472ce-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="472ce-107">คุณลักษณะโมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="472ce-107">Order confirmation module properties</span></span>

| <span data-ttu-id="472ce-108">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="472ce-108">Property name</span></span>  | <span data-ttu-id="472ce-109">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="472ce-109">Values</span></span> | <span data-ttu-id="472ce-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="472ce-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="472ce-111">หัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="472ce-111">Heading</span></span>        | <span data-ttu-id="472ce-112">ข้อความหัวข้อ และแท็กหัวข้อ (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span><span class="sxs-lookup"><span data-stu-id="472ce-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="472ce-113">โมดูลการยืนยันใบสั่งสามารถมีหัวข้อได้</span><span class="sxs-lookup"><span data-stu-id="472ce-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="472ce-114">โดยค่าเริ่มต้น แท็กหัวเรื่อง **H2** จะใช้สำหรับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="472ce-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="472ce-115">อย่างไรก็ตาม คุณสามารถเปลี่ยนแท็กเพื่อให้ตรงกับความต้องการสำหรับการเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="472ce-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="472ce-116">หมายเลขผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="472ce-116">Contact number</span></span> | <span data-ttu-id="472ce-117">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="472ce-117">Text</span></span> | <span data-ttu-id="472ce-118">สามารถให้หมายเลขติดต่อสำหรับคำถามที่เกี่ยวข้องกับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="472ce-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="472ce-119">แสดงข้อมูลช่วงเวลาการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="472ce-119">Show pickup timeslot information</span></span> | <span data-ttu-id="472ce-120">จริงหรือเท็จ</span><span class="sxs-lookup"><span data-stu-id="472ce-120">True or False</span></span> | <span data-ttu-id="472ce-121">คุณสมบัตินี้มีอยู่ใน Dynamics 365 Commerce 10.0.15 และสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="472ce-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="472ce-122">เมื่อเป็นจริง จะมีการแสดงข้อมูลช่วงเวลาการเบิกสินค้าหากมีการระบุไว้สำหรับสินค้าที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="472ce-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="472ce-123">โมดูลที่สามารถใช้ในหน้าการยืนยันการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="472ce-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="472ce-124">เมื่อคุณสร้างหน้าการยืนยันการสั่งซื้อ คุณสามารถเพิ่มโมดูลที่เกี่ยวข้องอื่น ๆ นอกเหนือจากโมดูลการยืนยันการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="472ce-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="472ce-125">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="472ce-125">Here are some examples:</span></span>

- <span data-ttu-id="472ce-126">**โมดูลคำแนะนำ** – โมดูลคำแนะนำสามารถเพิ่มไปยังหน้าการยืนยันการสั่งซื้อเพื่อแนะนำผลิตภัณฑ์อื่น ๆ ให้กับลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="472ce-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="472ce-127">**โมดูลการตลาด** – โมดูลการตลาดใด ๆ ที่สามารถเพิ่มไปยังหน้าการยืนยันการสั่งซื้อเพื่อแสดงเนื้อหาการตลาด</span><span class="sxs-lookup"><span data-stu-id="472ce-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="472ce-128">เพิ่มโมดูลการยืนยันใบสั่งไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="472ce-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="472ce-129">ในการเพิ่มโมดูลการยืนยันใบสั่งไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="472ce-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="472ce-130">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="472ce-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="472ce-131">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อนชื่อ **แม่แบบการยืนยันใบสั่ง** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="472ce-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="472ce-132">ในช่อง **เนื้อหา** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="472ce-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="472ce-133">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **หน้าเริ่มต้น** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="472ce-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="472ce-134">ในช่อง **หลัก** ของโมดูล **หน้าเริ่มต้น** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="472ce-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="472ce-135">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **การยืนยันใบสั่ง** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="472ce-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="472ce-136">เลือก **บันทึก** และจากนั้น เลือก **พรีวิว** เพื่อพรีวิวเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="472ce-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="472ce-137">โมดูลการยืนยันใบสั่งจะไม่แสดงเนื่องจากจำเป็นต้องใช้บริบทของหมายเลขการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="472ce-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="472ce-138">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="472ce-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="472ce-139">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="472ce-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="472ce-140">ในกล่องโต้ตอบ **เลือกเท็มเพลต** ให้เลือก **แม่แบบการยืนยันใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="472ce-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="472ce-141">ภายใต้ **ชื่อของหน้า** ให้ป้อน **หน้าการยืนยันใบสั่ง** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="472ce-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="472ce-142">ในช่อง **หลัก** ของโมดูล **หน้าเริ่มต้น** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="472ce-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="472ce-143">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **การยืนยันใบสั่ง** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="472ce-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="472ce-144">ในบานหน้าต่างคุณสมบัติของโมดูลการยืนยันใบสั่ง ให้เลือก **ส่วนหัว** ถัดจากสัญลักษณ์ดินสอ</span><span class="sxs-lookup"><span data-stu-id="472ce-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="472ce-145">ในฟิลด์ **ข้อความส่วนหัว** ของกล่องโต้ตอบ **ส่วนหัว** ให้ป้อน **การยืนยันใบสั่ง** ของข้อความส่วนหัว และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="472ce-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="472ce-146">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="472ce-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="472ce-147">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="472ce-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="472ce-148">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="472ce-148">Additional resources</span></span>

[<span data-ttu-id="472ce-149">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="472ce-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="472ce-150">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="472ce-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="472ce-151">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="472ce-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="472ce-152">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="472ce-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="472ce-153">โมดูลที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="472ce-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="472ce-154">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="472ce-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="472ce-155">โมดูลข้อมูลการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="472ce-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="472ce-156">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="472ce-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]