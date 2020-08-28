---
title: โมดูลรายละเอียดใบสั่ง
description: หัวข้อนี้ครอบคลุมถึงโมดูลรายละเอียดใบสั่งและอธิบายวิธีการใช้งานใน Microsoft Dynamics 365 Commerce
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5876b953a3b3d960c106acf37731fde13b93f8e7
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661183"
---
# <a name="order-details-module"></a><span data-ttu-id="015ac-103">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="015ac-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="015ac-104">หัวข้อนี้ครอบคลุมถึงโมดูลรายละเอียดใบสั่งและอธิบายวิธีการใช้งานใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="015ac-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="015ac-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="015ac-105">Overview</span></span>

<span data-ttu-id="015ac-106">โมดูลรายละเอียดใบสั่ง ใช้เพื่อแสดงรายละเอียดการยืนยันคำสั่งซื้อหลังจากที่มีการวางใบสั่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="015ac-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="015ac-107">เป็นการแสดงรหัสยืนยันใบสั่ง ข้อมูลการติดต่อเพื่อสั่งซื้อ และรายละเอียดการสั่งซื้ออื่น ๆ เช่นรายการที่ซื้อ ข้อมูลการชำระเงิน และวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="015ac-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="015ac-108">คุณลักษณะโมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="015ac-108">Order details module properties</span></span>

| <span data-ttu-id="015ac-109">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="015ac-109">Property name</span></span>  | <span data-ttu-id="015ac-110">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="015ac-110">Values</span></span> | <span data-ttu-id="015ac-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="015ac-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="015ac-112">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="015ac-112">Heading</span></span>        | <span data-ttu-id="015ac-113">ข้อความหัวข้อ และแท็กหัวข้อ (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span><span class="sxs-lookup"><span data-stu-id="015ac-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="015ac-114">โมดูลรายละเอียดใบสั่งสามารถมีส่วนหัวได้</span><span class="sxs-lookup"><span data-stu-id="015ac-114">The order details module can have a heading.</span></span> <span data-ttu-id="015ac-115">โดยค่าเริ่มต้น แท็กหัวเรื่อง **H2** จะใช้สำหรับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="015ac-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="015ac-116">อย่างไรก็ตาม คุณสามารถเปลี่ยนแท็กเพื่อให้ตรงกับความต้องการสำหรับการเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="015ac-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="015ac-117">หมายเลขผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="015ac-117">Contact number</span></span> | <span data-ttu-id="015ac-118">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="015ac-118">Text</span></span> | <span data-ttu-id="015ac-119">สามารถให้หมายเลขติดต่อสำหรับคำถามที่เกี่ยวข้องกับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="015ac-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="015ac-120">โมดูลที่สามารถใช้ในหน้ารายละเอียดการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="015ac-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="015ac-121">เมื่อคุณสร้างหน้ารายละเอียดการสั่งซื้อ คุณสามารถเพิ่มโมดูลที่เกี่ยวข้องอื่น ๆ นอกเหนือจากโมดูลรายละเอียดการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="015ac-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="015ac-122">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="015ac-122">Here are some examples:</span></span>

- <span data-ttu-id="015ac-123">**โมดูลคำแนะนำ** – โมดูลคำแนะนำสามารถเพิ่มไปยังหน้ารายละเอียดการสั่งซื้อเพื่อแนะนำผลิตภัณฑ์อื่น ๆ ให้กับลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="015ac-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="015ac-124">**โมดูลการตลาด** – โมดูลการตลาดใด ๆ ที่สามารถเพิ่มไปยังหน้ารายละเอียดการสั่งซื้อเพื่อแสดงเนื้อหาการตลาด</span><span class="sxs-lookup"><span data-stu-id="015ac-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="015ac-125">เพิ่มโมดูลรายละเอียดใบสั่งไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="015ac-125">Add an order details module to a page</span></span>

<span data-ttu-id="015ac-126">ในการเพิ่มโมดูลรายละเอียดใบสั่งไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="015ac-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="015ac-127">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="015ac-127">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="015ac-128">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อนชื่อ **เท็มเพลตรายละเอียดใบสั่ง** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="015ac-128">In the **New Template** dialog box, under **Template name**, enter the name **Order details template**, and then select **OK**.</span></span>
1. <span data-ttu-id="015ac-129">ในช่อง **เนื้อหา** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="015ac-129">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="015ac-130">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **หน้าเริ่มต้น** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="015ac-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="015ac-131">ในช่อง **หลัก** ของโมดูล **หน้าเริ่มต้น** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="015ac-131">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="015ac-132">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **รายละเอียดใบสั่ง** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="015ac-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="015ac-133">เลือก **บันทึก** และจากนั้น เลือก **พรีวิว** เพื่อพรีวิวเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="015ac-133">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="015ac-134">โมดูลรายละเอียดการสั่งซื้อจะไม่ถูกแสดงผล เนื่องจากต้องใช้บริบทของหมายเลขยืนยันการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="015ac-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="015ac-135">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="015ac-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="015ac-136">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="015ac-136">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="015ac-137">ในกล่องโต้ตอบ **เลือกเท็มเพลต** ให้เลือก **เท็มเพลตรายละเอียดใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="015ac-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="015ac-138">ภายใต้ **ชื่อของหน้า** ให้ป้อน **หน้ารายละเอียดใบสั่ง** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="015ac-138">Under **Page name**, enter **Order details page**, and then select **OK**.</span></span>
1. <span data-ttu-id="015ac-139">ในช่อง **หลัก** ของโมดูล **หน้าเริ่มต้น** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="015ac-139">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="015ac-140">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **รายละเอียดใบสั่ง** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="015ac-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="015ac-141">ในบานหน้าต่างคุณสมบัติของโมดูลรายละเอียดใบสั่ง ให้เลือก **ส่วนหัว** ถัดจากสัญลักษณ์ดินสอ</span><span class="sxs-lookup"><span data-stu-id="015ac-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="015ac-142">ในฟิลด์ **ข้อความส่วนหัว** ของกล่องโต้ตอบ **ส่วนหัว** ให้ป้อน **รายละเอียดใบสั่ง** ของข้อความส่วนหัว และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="015ac-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details**, and then select **OK**.</span></span>
1. <span data-ttu-id="015ac-143">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="015ac-143">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="015ac-144">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="015ac-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="015ac-145">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="015ac-145">Additional resources</span></span>

[<span data-ttu-id="015ac-146">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="015ac-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="015ac-147">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="015ac-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="015ac-148">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="015ac-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="015ac-149">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="015ac-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="015ac-150">โมดูลที่อยู่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="015ac-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="015ac-151">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="015ac-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="015ac-152">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="015ac-152">Gift card module</span></span>](add-giftcard.md)
