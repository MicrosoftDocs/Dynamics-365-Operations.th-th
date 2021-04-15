---
title: ภาพรวมของไลบรารีโมดูล
description: หัวข้อนี้แสดงภาพรวมของไลบรารีโมดูล Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76fd75c2ed9a3ba4728129b77a43b50267be3bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795344"
---
# <a name="module-library-overview"></a><span data-ttu-id="94881-103">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="94881-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="94881-104">หัวข้อนี้แสดงภาพรวมของไลบรารีโมดูล Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="94881-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="94881-105">ไลบรารีโมดูล Dynamics 365 Commerce เป็นชุดของโมดูลที่สามารถใช้ในการสร้างเว็บไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="94881-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="94881-106">โมดูลมีทั้งด้านอินเทอร์เฟสผู้ใช้ (UI) และลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="94881-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="94881-107">ชุดรูปแบบสามารถนำไปใช้กับโมดูลในไลบรารีโมดูล เพื่อเปลี่ยนลักษณะที่แสดง</span><span class="sxs-lookup"><span data-stu-id="94881-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="94881-108">ชุดรูปแบบใช้ Cascading Style Sheets (CSS)</span><span class="sxs-lookup"><span data-stu-id="94881-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="94881-109">ธีมสำหรับไซต์ e-Commerce แบบสมมติที่มีชื่อว่า "Fabrikam" ให้ไว้เป็นส่วนหนึ่งของไลบรารีโมดูล และสามารถใช้เป็นข้อมูลอ้างอิงได้</span><span class="sxs-lookup"><span data-stu-id="94881-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="94881-110">โมดูลไลบรารีของโมดูล</span><span class="sxs-lookup"><span data-stu-id="94881-110">Module library modules</span></span>

<span data-ttu-id="94881-111">ชนิดของโมดูลต่อไปนี้มีให้ในไลบรารีโมดูล:</span><span class="sxs-lookup"><span data-stu-id="94881-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="94881-112">**โมดูลคอนเทนเนอร์** – โมดูลคอนเทนเนอร์เป็นโมดูลที่เรียบง่ายที่ทำหน้าที่เป็นโฮสต์สำหรับโมดูลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="94881-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="94881-113">ซึ่งควบคุมโครงร่างของโมดูลที่อยู่ภายใน</span><span class="sxs-lookup"><span data-stu-id="94881-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="94881-114">**โมดูลการตลาด** – โมดูลการตลาด ได้แก่ บล็อคเนื้อหา บล็อคข้อความ เครื่องเล่นวิดีโอ และโมดูลแบบวงล้อ</span><span class="sxs-lookup"><span data-stu-id="94881-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="94881-115">โมดูลเหล่านี้ทั้งหมดสามารถใช้ในการแสดงเนื้อหาได้</span><span class="sxs-lookup"><span data-stu-id="94881-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="94881-116">ซึ่งสามารถนำไปใช้ที่หน้าไหนก็ได้ และจะถูกขับเคลื่อนด้วยข้อมูลจากระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="94881-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="94881-117">**โมดูลส่วนหัวและส่วนท้าย** – โมดูลส่วนหัวและส่วนท้ายจะปรากฏในส่วนหัวและส่วนท้ายของหน้าไซต์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="94881-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="94881-118">คุณสามารถตั้งค่าคอนฟิกโมดูลเหล่านี้ตามต้องการได้โดยใช้คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="94881-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="94881-119">**โมดูลค้นหา** – ผลิตภัณฑ์จะถูกพบได้โดยใช้โมดูลการค้นหาในส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="94881-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="94881-120">ผลการค้นหาจะปรากฏขึ้นบนหน้าผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="94881-120">Search results appear on the search results page.</span></span> <span data-ttu-id="94881-121">นอกจากนี้คุณยังสามารถค้นหาผลิตภัณฑ์ในหน้าประเภท ซึ่งเป็นหน้าเฉพาะสำหรับแต่ละประเภทที่ได้รับการสนับสนุน ในลำดับชั้นการนำทางของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="94881-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="94881-122">นอกจากนี้ คุณยังสามารถใช้โมดูลตัวคัดสรรในการกรองผลการค้นหาและหน้าประเภทได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="94881-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="94881-123">**โมดูลหน้ารายละเอียดผลิตภัณฑ์** – หน้ารายละเอียดของผลิตภัณฑ์ใช้หลายโมดูลเพื่อแสดงข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="94881-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="94881-124">โมดูลในกล่องการซื้อ ให้ลูกค้าสามารถดูผลิตภัณฑ์และเพิ่มสินค้าลงในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="94881-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="94881-125">โมดูลอื่นๆ เช่น โมดูลข้อมูลจำเพาะด้านเทคนิค แสดงรายละเอียดของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="94881-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="94881-126">โมดูลการจัดอันดับ และความคิดเห็นสามารถใช้เพื่อดูและให้ความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="94881-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="94881-127">**โมดูลซื้อออนไลน์ รับสินค้าที่ร้านค้า** – โมดูลซื้อออนไลน์ รับสินค้าที่ร้านค้าทำงานร่วมกับ Bing Maps</span><span class="sxs-lookup"><span data-stu-id="94881-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="94881-128">คุณสามารถใช้ในการค้นหาร้านค้าใกล้เคียง ที่ลูกค้าสามารถรับสินค้าที่ซื้อได้</span><span class="sxs-lookup"><span data-stu-id="94881-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="94881-129">**โมดูลการซื้อ** – โมดูลการซื้อรวมถึงโมดูลรถเข็น ซึ่งสามารถใช้เพื่อเพิ่มสินค้าลงในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="94881-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="94881-130">โมดูลการชำระเงินจะเก็บที่อยู่ในการจัดส่ง ตัวเลือกการจัดส่ง บัตรของขวัญ โปรแกรมสะสมคะแนน และข้อมูลบัตรเครดิตเพื่อให้สามารถประมวลผลใบสั่งซื้อได้</span><span class="sxs-lookup"><span data-stu-id="94881-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="94881-131">หลังจากวางใบสั่งซื้อแล้ว คุณสามารถใช้โมดูลการยืนยันใบสั่งเพื่อแสดงรายละเอียดการยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="94881-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="94881-132">**โมดูลการจัดการบัญชี** – โมดูลเข้าสู่ระบบของผู้ใช้ ให้ลูกค้าล็อกอินเข้าสู่บัญชีที่มีอยู่ และโมดูลการลงทะเบียนจะช่วยให้ผู้ใช้สามารถสร้างบัญชีใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="94881-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="94881-133">หลังจากที่สร้างบัญชีแล้ว คุณสามารถใช้โมดูลบัญชีของใบสั่งซื้อเพื่อดูใบสั่งซื้อล่าสุด และโมดูลรายละเอียดใบสั่งซื้อสามารถใช้เพื่อดูรายละเอียดของใบสั่งซื้อได้</span><span class="sxs-lookup"><span data-stu-id="94881-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="94881-134">**โมดูลคำแนะนำ** – ข้อแนะนำแสดงโดยใช้โมดูลการวางผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="94881-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="94881-135">โมดูลนี้สนับสนุนรายการอัลกอริทึม และรายการที่เลือกโดยบรรณาธิการ ที่สามารถแสดงในหน้าใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="94881-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94881-136">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="94881-136">Additional resources</span></span>

[<span data-ttu-id="94881-137">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="94881-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="94881-138">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="94881-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="94881-139">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="94881-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="94881-140">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="94881-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="94881-141">โมดูลใบยืนยันคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="94881-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="94881-142">โมดูหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="94881-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="94881-143">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="94881-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]