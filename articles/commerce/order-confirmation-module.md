---
title: โมดูลรายละเอียดใบสั่ง
description: หัวข้อนี้ครอบคลุมถึงโมดูลรายละเอียดใบสั่งและอธิบายวิธีการใช้งานใน Microsoft Dynamics 365 Commerce
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026028"
---
# <a name="order-details-module"></a><span data-ttu-id="572c7-103">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="572c7-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="572c7-104">หัวข้อนี้ครอบคลุมถึงโมดูลรายละเอียดใบสั่งและอธิบายวิธีการใช้งานใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="572c7-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="572c7-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="572c7-105">Overview</span></span>

<span data-ttu-id="572c7-106">โมดูลรายละเอียดใบสั่ง ใช้เพื่อแสดงรายละเอียดการยืนยันคำสั่งซื้อหลังจากที่มีการวางใบสั่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="572c7-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="572c7-107">เป็นการแสดงรหัสยืนยันใบสั่ง ข้อมูลการติดต่อเพื่อสั่งซื้อ และรายละเอียดการสั่งซื้ออื่น ๆ เช่นรายการที่ซื้อ ข้อมูลการชำระเงิน และวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="572c7-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="572c7-108">คุณลักษณะโมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="572c7-108">Order confirmation module properties</span></span>

| <span data-ttu-id="572c7-109">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="572c7-109">Property name</span></span>  | <span data-ttu-id="572c7-110">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="572c7-110">Values</span></span> | <span data-ttu-id="572c7-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="572c7-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="572c7-112">หัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="572c7-112">Heading</span></span>        | <span data-ttu-id="572c7-113">ข้อความหัวข้อ และแท็กหัวข้อ (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span><span class="sxs-lookup"><span data-stu-id="572c7-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="572c7-114">โมดูลการยืนยันใบสั่งสามารถมีหัวข้อได้</span><span class="sxs-lookup"><span data-stu-id="572c7-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="572c7-115">โดยค่าเริ่มต้น แท็กหัวเรื่อง **H2** จะใช้สำหรับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="572c7-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="572c7-116">อย่างไรก็ตาม คุณสามารถเปลี่ยนแท็กเพื่อให้ตรงกับความต้องการสำหรับการเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="572c7-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="572c7-117">หมายเลขผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="572c7-117">Contact number</span></span> | <span data-ttu-id="572c7-118">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="572c7-118">Text</span></span> | <span data-ttu-id="572c7-119">สามารถให้หมายเลขติดต่อสำหรับคำถามที่เกี่ยวข้องกับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="572c7-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="572c7-120">โมดูลที่สามารถใช้ในหน้ารายละเอียดการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="572c7-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="572c7-121">เมื่อคุณสร้างหน้ารายละเอียดการสั่งซื้อ คุณสามารถเพิ่มโมดูลที่เกี่ยวข้องอื่น ๆ นอกเหนือจากโมดูลรายละเอียดการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="572c7-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="572c7-122">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="572c7-122">Here are some examples:</span></span>

- <span data-ttu-id="572c7-123">**โมดูลคำแนะนำ** – โมดูลคำแนะนำสามารถเพิ่มไปยังหน้ารายละเอียดการสั่งซื้อเพื่อแนะนำผลิตภัณฑ์อื่น ๆ ให้กับลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="572c7-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="572c7-124">**โมดูลการตลาด** – โมดูลการตลาดใด ๆ ที่สามารถเพิ่มไปยังหน้ารายละเอียดการสั่งซื้อเพื่อแสดงเนื้อหาการตลาด</span><span class="sxs-lookup"><span data-stu-id="572c7-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="572c7-125">สร้างโมดูลหน้ารายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="572c7-125">Create an order details page module</span></span>

1. <span data-ttu-id="572c7-126">สร้างแม่แบบหน้าที่มีชื่อว่า **แม่แบบรายละเอียดการสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="572c7-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="572c7-127">ในช่อง **หลัก** ของหน้าเริ่มต้น ให้เพิ่มโมดูลรายละเอียดคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="572c7-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="572c7-128">ในโมดูลรายละเอียดคำสั่งซื้อ เพิ่มโมดูลคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="572c7-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="572c7-129">บันทึกและแสดงตัวอย่างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="572c7-129">Save and preview the template.</span></span> <span data-ttu-id="572c7-130">โมดูลรายละเอียดการสั่งซื้อจะไม่ถูกแสดงผล เนื่องจากต้องใช้บริบทของหมายเลขยืนยันการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="572c7-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="572c7-131">แก้ไขแม่แบบให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="572c7-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="572c7-132">ใช้แม่แบบรายละเอียดการสั่งซื้อที่คุณเพิ่งสร้างเพื่อสร้างหน้าที่มีชื่อว่า **หน้ารายละเอียดการสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="572c7-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="572c7-133">เพิ่มหน้าเริ่มต้นลงในเค้าร่างของหน้า</span><span class="sxs-lookup"><span data-stu-id="572c7-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="572c7-134">ในช่อง **ส่วนหัว** ให้เพิ่มส่วนของส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="572c7-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="572c7-135">ในช่อง **ส่วนท้าย** ให้เพิ่มส่วนของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="572c7-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="572c7-136">ในช่อง **หลัก** ให้เพิ่มโมดูลรายละเอียดคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="572c7-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="572c7-137">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลรายละเอียดคำสั่งซื้อ ให้เพิ่มหัวเรื่อง **รายละเอียดคำสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="572c7-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="572c7-138">ใต้โมดูลรายละเอียดคำสั่งซื้อ เพิ่มโมดูลคำแนะนำและกำหนดค่าเพื่อให้ใช้การตั้งค่า **ใหม่** และ **ขายดีที่สุด**</span><span class="sxs-lookup"><span data-stu-id="572c7-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="572c7-139">บันทึกและแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="572c7-139">Save and preview the page.</span></span>
1. <span data-ttu-id="572c7-140">แก้ไขหน้าให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="572c7-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="572c7-141">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="572c7-141">Additional resources</span></span>

[<span data-ttu-id="572c7-142">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="572c7-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="572c7-143">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="572c7-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="572c7-144">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="572c7-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="572c7-145">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="572c7-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="572c7-146">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="572c7-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="572c7-147">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="572c7-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="572c7-148">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="572c7-148">Footer module</span></span>](author-footer-module.md)
