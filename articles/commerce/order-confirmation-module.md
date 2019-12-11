---
title: โมดูลการยืนยันใบสั่ง
description: หัวข้อนี้ครอบคลุมถึงโมดูลการยืนยันใบสั่งและอธิบายวิธีการสร้างใน Microsoft Dynamics 365 Commerce
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698337"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="2ca9d-103">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2ca9d-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2ca9d-104">หัวข้อนี้ครอบคลุมถึงโมดูลการยืนยันใบสั่งและอธิบายวิธีการสร้างใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2ca9d-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2ca9d-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="2ca9d-105">Overview</span></span>

<span data-ttu-id="2ca9d-106">โมดูลการยืนยันใบสั่งใช้เพื่อแสดงข้อความยืนยันบนหน้าการยืนยันใบสั่งหลังจากที่มีการวางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2ca9d-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="2ca9d-107">โมดูลการยืนยันใบสั่งแสดงหมายเลขการยืนยันใบสั่งและที่อยู่อีเมล์ของลูกค้าที่ระบุไว้ในระหว่างการเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="2ca9d-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="2ca9d-108">เมื่อวางใบสั่งค้างไว้ระหว่างการเช็คเอาท์ หมายเลขการยืนยันใบสั่งและที่อยู่อีเมลของลูกค้าจะถูกส่งผ่านไปยังหน้าการยืนยันใบสั่งเป็นสตริงการสอบถามใน URL ของหน้า</span><span class="sxs-lookup"><span data-stu-id="2ca9d-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="2ca9d-109">โมดูลการยืนยันใบสั่งจะได้รับข้อมูลนี้และแสดงสถานะของใบสั่งบนหน้าการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2ca9d-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="2ca9d-110">โมดูลการยืนยันใบสั่งต้องใช้บริบทของหน้านี้เพื่อระบุสถานะของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2ca9d-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="2ca9d-111">คุณลักษณะโมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2ca9d-111">Order confirmation module properties</span></span>

| <span data-ttu-id="2ca9d-112">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="2ca9d-112">Property name</span></span> | <span data-ttu-id="2ca9d-113">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="2ca9d-113">Values</span></span> | <span data-ttu-id="2ca9d-114">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2ca9d-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="2ca9d-115">หัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="2ca9d-115">Heading</span></span>       | <span data-ttu-id="2ca9d-116">ข้อความหัวข้อ และแท็กหัวข้อ (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span><span class="sxs-lookup"><span data-stu-id="2ca9d-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="2ca9d-117">โมดูลการยืนยันใบสั่งสามารถมีหัวข้อได้</span><span class="sxs-lookup"><span data-stu-id="2ca9d-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="2ca9d-118">โดยค่าเริ่มต้น แท็กหัวเรื่อง **H2** จะใช้สำหรับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="2ca9d-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="2ca9d-119">อย่างไรก็ตาม คุณสามารถเปลี่ยนแท็กเพื่อให้ตรงกับความต้องการสำหรับการเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="2ca9d-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="2ca9d-120">โมดูลที่สามารถใช้ในโมดูลหน้าการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2ca9d-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="2ca9d-121">**คำแนะนำ** – สามารถใส่โมดูคำแนะนำบนหน้าการยืนยันใบสั่งเพื่อแนะนำผลิตภัณฑ์อื่นๆ ให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2ca9d-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="2ca9d-122">**การตลาด** – โมดูลการตลาดสามารถเพิ่มเนื้อหาทางการตลาดไปยังหน้าการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2ca9d-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="2ca9d-123">สร้างโมดูลหน้าการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2ca9d-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="2ca9d-124">สร้างเท็มเพลตของหน้าซึ่งมีชื่อว่า **เท็มเพลตการยืนยันใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="2ca9d-125">ในช่อง **หลัก** ของหน้าเริ่มต้น ให้เพิ่มโมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2ca9d-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="2ca9d-126">ในโมดูลการยืนยันใบสั่งให้เพิ่มโมดูคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="2ca9d-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="2ca9d-127">บันทึกและแสดงตัวอย่างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="2ca9d-127">Save and preview the template.</span></span> <span data-ttu-id="2ca9d-128">โมดูลการยืนยันใบสั่งไม่ควรแสดงเนื่องจากจำเป็นต้องใช้บริบทของหมายเลขการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2ca9d-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="2ca9d-129">เช็คอินแม่แบบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2ca9d-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="2ca9d-130">ใช้เท็มเพลตการยืนยันใบสั่งที่คุณเพิ่งสร้างขึ้น เพื่อสร้างหน้าที่ชื่อ **หน้าการยืนยันใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="2ca9d-131">เพิ่มหน้าเริ่มต้นลงในเค้าร่างของหน้า</span><span class="sxs-lookup"><span data-stu-id="2ca9d-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="2ca9d-132">ในช่อง **ส่วนหัว** ให้เพิ่มส่วนของส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="2ca9d-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="2ca9d-133">ในช่อง **ส่วนท้าย** ให้เพิ่มส่วนของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="2ca9d-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="2ca9d-134">ในช่อง **หลัก** ให้เพิ่มโมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2ca9d-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="2ca9d-135">ในบานหน้าต่างคุณสมบัติของโมดูลการยืนยันใบสั่ง ให้เพิ่มหัวข้อ **การยืนยันใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="2ca9d-136">ด้านล่างโมดูลการยืนยันใบสั่งให้เพิ่มโมดูคำแนะนำและตั้งค่าคอนฟิกเพื่อให้ใช้การตั้งค่า **การขายใหม่** และ **การขายที่ดีที่สุด**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="2ca9d-137">บันทึกและแสดงตัวอย่างหน้า ตรวจสอบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2ca9d-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ca9d-138">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2ca9d-138">Additional resources</span></span>

[<span data-ttu-id="2ca9d-139">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2ca9d-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2ca9d-140">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="2ca9d-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2ca9d-141">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="2ca9d-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2ca9d-142">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="2ca9d-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2ca9d-143">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="2ca9d-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2ca9d-144">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="2ca9d-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2ca9d-145">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="2ca9d-145">Footer module</span></span>](author-footer-module.md)
