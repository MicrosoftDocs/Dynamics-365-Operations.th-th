---
title: หน้าและโมดูลการจัดการบัญชี
description: หัวข้อนี้จะครอบคลุมหน้าการจัดการบัญชีและโมดูลใน Microsoft Dynamics 365 Commerce
author: v-chgri
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8787a7b01ecf15752569d2a3a8d7804fe492e63d
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025735"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="121ba-103">หน้าและโมดูลการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="121ba-103">Account management pages and modules</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="121ba-104">หัวข้อนี้จะครอบคลุมหน้าการจัดการบัญชีและโมดูลใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="121ba-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="121ba-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="121ba-105">Overview</span></span>

<span data-ttu-id="121ba-106">การจัดการบัญชีอ้างอิงถึงกลุ่มของหน้า ที่ใช้ในการจัดการข้อมูลบัญชีผู้ใช้–ที่เกี่ยวข้องใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="121ba-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="121ba-107">หน้าการจัดการบัญชีจะรวมหน้าเริ่มต้นของการจัดการบัญชี หน้าโพรไฟล์ผู้ใช้ หน้าที่อยู่ของผู้ใช้ หน้าประวัติคำสั่งซื้อ หน้ารายละเอียดของคำสั่งซื้อ หน้าความภักดี และหน้ารายการสิ่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="121ba-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="121ba-108">หน้าเริ่มต้นของการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="121ba-108">Account management landing page</span></span>

<span data-ttu-id="121ba-109">หน้าเริ่มต้นของการจัดการบัญชีใช้โมดูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="121ba-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="121ba-110">**คอนเทนเนอร์** - เพจเริ่มต้นสำหรับโมดูลการจัดการบัญชีทั้งหมดควรอยู่ในคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="121ba-110">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="121ba-111">**ไทล์ต้อนรับบัญชี** – โมดูลนี้ใช้เพื่อระบุข้อความต้อนรับบนหน้าการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="121ba-111">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="121ba-112">นี่รวมถึงคุณสมบัติสำหรับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="121ba-112">It includes properties for the heading.</span></span>
- <span data-ttu-id="121ba-113">**ไทล์การใช้งานแบบทั่วไปของบัญชี** - โมดูลนี้สามารถใช้เพื่อระบุส่วนหัวและลิงก์ไปยังหน้าการจัดการบัญชี เช่น "ประวัติการสั่งซื้อ" หรือ "โปรไฟล์ของฉัน"</span><span class="sxs-lookup"><span data-stu-id="121ba-113">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="121ba-114">โมดูลไทล์ทั่วไปสามารถใช้เพื่อตั้งค่าคอนฟิกไทล์สำหรับหน้าใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="121ba-114">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="121ba-115">ใน Fabrikam โมดูลนี้ใช้สำหรับ "ประวัติการสั่งซื้อ" และลิงก์หน้า "โปรไฟล์ของฉัน" บนหน้าเพจเริ่มต้นของการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="121ba-115">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="121ba-116">**ไทล์สิ่งที่ต้องการของบัญชี** – โมดูลนี้ใช้เพื่อให้แสดงสรุปของสินค้าในรายการสิ่งที่ต้องการของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="121ba-116">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="121ba-117">ตัวอย่าง เช่น อาจระบุสถานะ "คุณมีสินค้าในรายการสิ่งที่ต้องการของคุณ 10 รายการ"</span><span class="sxs-lookup"><span data-stu-id="121ba-117">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="121ba-118">รวมถึงคุณสมบัติสำหรับหัวข้อ และลิงก์ "ดูรายละเอียด"</span><span class="sxs-lookup"><span data-stu-id="121ba-118">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="121ba-119">ลิงค์ "ดูรายละเอียด" ควรถูกตั้งค่าให้เปลี่ยนเส้นทางไปยังหน้ารายการสิ่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="121ba-119">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="121ba-120">**ไทล์ที่อยู่ของบัญชี** – โมดูลนี้ใช้เพื่อให้แสดงสรุปของที่อยู่ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="121ba-120">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="121ba-121">ตัวอย่าง เช่น อาจระบุสถานะ "คุณมีที่อยู่ที่เพิ่มเข้าในบัญชีของคุณ 2 รายการ"</span><span class="sxs-lookup"><span data-stu-id="121ba-121">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="121ba-122">รวมถึงคุณสมบัติสำหรับหัวข้อ และลิงก์ "ดูรายละเอียด"</span><span class="sxs-lookup"><span data-stu-id="121ba-122">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="121ba-123">ลิงค์ "ดูรายละเอียด" ควรถูกตั้งค่าให้เปลี่ยนเส้นทางไปยังหน้าที่อยู่ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="121ba-123">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="121ba-124">**ไทล์สำหรับสมาชิกที่ใช้ในบัญชี** – โมดูลใช้นี้เพื่อแสดง และลิงก์ไปยังข้อมูลโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="121ba-124">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="121ba-125">ไทล์นี้มีสองสถานะ: สถานะหนึ่งแสดงลิงก์เพื่อเข้าร่วมตลาดของสมาชิก ถ้าผู้ใช้ไม่ใช่สมาชิกอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="121ba-125">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="121ba-126">อีกสถานะหนึ่ง แสดงลิงก์เพื่อดูหน้ารายละเอียดของสมาชิก เมื่อผู้ใช้เป็นสมาชิกอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="121ba-126">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="121ba-127">คุณสมบัติรวมถึง ส่วนหัว ลิงก์ "การลงทะเบียน" และลิงก์ "ดูการตอบแทนลูกค้าสมาชิก"</span><span class="sxs-lookup"><span data-stu-id="121ba-127">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="121ba-128">ลิงค์ "ดูการตอบแทนลูกค้าสมาชิก" ควรถูกตั้งค่าให้เปลี่ยนเส้นทางไปยังหน้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="121ba-128">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="121ba-129">ลิงก์ "สมัครสมาชิก" ควรถูกตั้งค่าให้เปลี่ยนเส้นทางไปยังหน้าซึ่งผู้ใช้สามารถเข้าร่วมโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="121ba-129">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="121ba-130">หน้าประวัติคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="121ba-130">Order history page</span></span>

<span data-ttu-id="121ba-131">หน้าประวัติคำสั่งซื้อใช้โมดูลประวัติคำสั่งซื้อ เพื่อแสดงคำสั่งซื้อล่าสุดทั้งหมดที่ผู้ใช้ได้วางไว้</span><span class="sxs-lookup"><span data-stu-id="121ba-131">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="121ba-132">หน้ารายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="121ba-132">Order details page</span></span>

<span data-ttu-id="121ba-133">หน้ารายละเอียดของคำสั่งซื้อให้ข้อมูลรายละเอียดสำหรับแต่ละคำสั่งซื้อ และเข้าถึงได้จากหน้าประวัติการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="121ba-133">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="121ba-134">ใช้โมดูลรายละเอียดคำสั่งซื้อ ซึ่งจำเป็นต้องใช้รหัสการขายหรือรหัสธุรกรรมเพื่อดึงข้อมูลรายละเอียดของคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="121ba-134">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="121ba-135">หน้าโพรไฟล์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="121ba-135">User profile page</span></span>

<span data-ttu-id="121ba-136">หน้าโพรไฟล์ผู้ใช้จะแสดงรายละเอียดบัญชีผู้ใช้ เช่น ชื่อและที่อยู่อีเมลของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="121ba-136">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="121ba-137">ใช้รายละเอียดโพรไฟล์ผู้ใช้ และแก้ไขโพรไฟล์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="121ba-137">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="121ba-138">แม้ว่าจะไม่สามารถลบที่อยู่อีเมล์ได้ แต่คุณสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="121ba-138">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="121ba-139">หน้าโปรไฟล์ผู้ใช้ยังแสดงการกำหนดลักษณะผู้ใช้ ที่ช่วยให้ผู้ใช้สามารถเข้าร่วมหรือเลือกไม่รับจากคุณลักษณะบางอย่าง เช่น การตั้งค่าส่วนบุคคลของรายการแนะนำ</span><span class="sxs-lookup"><span data-stu-id="121ba-139">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="121ba-140">หน้าที่อยู่ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="121ba-140">User address page</span></span>

<span data-ttu-id="121ba-141">หน้าที่อยู่ของผู้ใช้แสดงรายการของที่อยู่ที่เชื่อมโยงกับบัญชีผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="121ba-141">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="121ba-142">ผู้ใช้ให้ที่อยู่เหล่านี้ในระหว่างการชำระเงินหรือเพิ่มในหน้านี้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="121ba-142">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="121ba-143">โมดูลที่อยู่ของผู้ใช้ ใช้เพิ่มและแก้ไขที่อยู่ ตั้งค่าที่อยู่หลัก และแสดงที่อยู่ที่มีอยู่บนหน้า</span><span class="sxs-lookup"><span data-stu-id="121ba-143">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="121ba-144">หน้ารายการสิ่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="121ba-144">Wish list page</span></span>

<span data-ttu-id="121ba-145">หน้ารายการสิ่งที่ต้องการแสดงรายการที่มีการเพิ่มลงในรายการสิ่งที่ต้องการของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="121ba-145">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="121ba-146">ใช้โมดูรายการสิ่งที่ต้องการเพื่อแสดงรายการสินค้าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="121ba-146">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="121ba-147">หน้าการตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="121ba-147">Loyalty page</span></span>

<span data-ttu-id="121ba-148">หน้าสมาชิก ให้ลูกค้าดูรายละเอียดการตอบแทนลูกค้าสมาชิก หรือถ้าเป็นสมาชิกของโปรแกรมลูกค้าสมาชิกอยู่แล้ว ให้ดูรายละเอียดของโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="121ba-148">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="121ba-149">นอกจากนี้ยังสามารถดูคะแนนที่ได้รับ และแลกคะแนนในธุรกรรมล่าสุด</span><span class="sxs-lookup"><span data-stu-id="121ba-149">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="121ba-150">หน้าใช้โมดูลสำหรับรายละเอียดของการตอบแทนลูกค้าสมาชิก เพื่อแสดงรายละเอียดของการตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="121ba-150">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="121ba-151">ในการเข้าร่วมโปรแกรมตอบแทนลูกค้าสมาชิก สามารถสร้างหน้าการตลาดกับโมดูลการลงทะเบียนการตอบแทนลูกค้าสมาชิก และเงื่อนไขสำหรับการตอบแทนลูกค้าสมาชิกได้</span><span class="sxs-lookup"><span data-stu-id="121ba-151">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="121ba-152">ถ้าผู้ใช้ไม่ได้เป็นสมาชิกของโปรแกรมตอบแทนลูกค้าสมาชิก โมดูลเหล่านี้จะเปิดให้ผู้ใช้สมัครใช้ได้</span><span class="sxs-lookup"><span data-stu-id="121ba-152">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="121ba-153">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="121ba-153">Additional resources</span></span>

[<span data-ttu-id="121ba-154">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="121ba-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="121ba-155">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="121ba-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="121ba-156">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="121ba-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="121ba-157">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="121ba-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="121ba-158">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="121ba-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="121ba-159">โมดูลใบยืนยันคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="121ba-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="121ba-160">โมดูหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="121ba-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="121ba-161">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="121ba-161">Footer module</span></span>](author-footer-module.md)
