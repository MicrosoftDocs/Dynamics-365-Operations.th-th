---
title: หน้าและโมดูลการจัดการบัญชี
description: หัวข้อนี้จะครอบคลุมหน้าการจัดการบัญชีและโมดูลใน Microsoft Dynamics 365 Commerce
author: v-chgri
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885820"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="40d13-103">หน้าและโมดูลการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40d13-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="40d13-104">หัวข้อนี้จะครอบคลุมหน้าการจัดการบัญชีและโมดูลใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="40d13-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="40d13-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="40d13-105">Overview</span></span>

<span data-ttu-id="40d13-106">การจัดการบัญชีอ้างอิงถึงกลุ่มของหน้า ที่ใช้ในการจัดการข้อมูลบัญชีผู้ใช้–ที่เกี่ยวข้องใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="40d13-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="40d13-107">หน้าการจัดการบัญชีจะรวมหน้าเริ่มต้นของการจัดการบัญชี หน้าโพรไฟล์ผู้ใช้ หน้าที่อยู่ของผู้ใช้ หน้าประวัติคำสั่งซื้อ หน้ารายละเอียดของคำสั่งซื้อ หน้าความภักดี และหน้ารายการสิ่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="40d13-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="40d13-108">หน้าเริ่มต้นของการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40d13-108">Account management landing page</span></span>

<span data-ttu-id="40d13-109">หน้าเริ่มต้นของการจัดการบัญชีใช้โมดูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="40d13-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="40d13-110">**การจัดวางเนื้อหา** –โมดูลนี้เป็นคอนเทนเนอร์ที่จัดเก็บโมดูลทั้งหมดบนหน้าเริ่มต้นของการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40d13-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="40d13-111">**รายการต้อนรับบัญชี** –โมดูลนี้ใช้เพื่อให้ข้อความต้อนรับบนหน้าการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40d13-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="40d13-112">รวมถึงคุณสมบัติสำหรับหัวข้อและขนาดของไทล์</span><span class="sxs-lookup"><span data-stu-id="40d13-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="40d13-113">คุณสมบัติ **ขนาดของไทล์** กำหนดความกว้างของโมดูลในโมดูลการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="40d13-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="40d13-114">ค่าช่วงตั้งแต่ **1** ถึง **12** โดยที่ **12** แสดงความกว้างของคอนเทนเนอร์การจัดวางเนื้อหาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="40d13-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="40d13-115">**รายการการจัดวางคำสั่งซื้อของบัญชี** –โมดูลนี้ใช้เพื่อให้สรุปจำนวนของคำสั่งซื้อที่วางโดยบัญชีผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="40d13-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="40d13-116">รวมถึงคุณสมบัติสำหรับหัวข้อ ขนาดของไทล์ และลิงก์ "ดูรายละเีอียด"</span><span class="sxs-lookup"><span data-stu-id="40d13-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="40d13-117">ลิงค์ "ดูรายละเอียด" ควรถูกตั้งค่าให้เปลี่ยนเส้นทางไปยังหน้าประวัติการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="40d13-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="40d13-118">**รายการการจัดวางโพรไฟล์บัญชี** –โมดูลนี้ใช้เพื่อให้แสดงสรุปของโพรไฟล์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="40d13-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="40d13-119">รวมถึงคุณสมบัติสำหรับหัวข้อ ขนาดของไทล์ และลิงก์ "ดูรายละเีอียด"</span><span class="sxs-lookup"><span data-stu-id="40d13-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="40d13-120">ลิงค์ "ดูรายละเอียด" ควรถูกตั้งค่าให้เปลี่ยนเส้นทางไปยังหน้าโพรไฟล์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="40d13-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="40d13-121">**รายการสิ่งที่ต้องการของบัญชี** –โมดูลนี้ใช้เพื่อให้แสดงสรุปของสินค้าในรายการสิ่งที่ต้องการของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="40d13-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="40d13-122">ตัวอย่าง เช่น อาจระบุสถานะ "คุณมีสินค้าในรายการสิ่งที่ต้องการของคุณ 10 รายการ"</span><span class="sxs-lookup"><span data-stu-id="40d13-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="40d13-123">รวมถึงคุณสมบัติสำหรับหัวข้อ ขนาดของไทล์ และลิงก์ "ดูรายละเีอียด"</span><span class="sxs-lookup"><span data-stu-id="40d13-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="40d13-124">ลิงค์ "ดูรายละเอียด" ควรถูกตั้งค่าให้เปลี่ยนเส้นทางไปยังหน้ารายการสิ่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="40d13-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="40d13-125">**รายการที่อยู่ของบัญชี** –โมดูลนี้ใช้เพื่อให้แสดงสรุปของที่อยู่ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="40d13-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="40d13-126">ตัวอย่าง เช่น อาจระบุสถานะ "คุณมีที่อยู่ที่เพิ่มเข้าในบัญชีของคุณ 2 รายการ"</span><span class="sxs-lookup"><span data-stu-id="40d13-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="40d13-127">รวมถึงคุณสมบัติสำหรับหัวข้อ ขนาดของไทล์ และลิงก์ "ดูรายละเีอียด"</span><span class="sxs-lookup"><span data-stu-id="40d13-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="40d13-128">ลิงค์ "ดูรายละเอียด" ควรถูกตั้งค่าให้เปลี่ยนเส้นทางไปยังหน้าที่อยู่ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="40d13-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="40d13-129">**รายการสำหรับสมาชิกที่ใช้ในบัญชี** –โมดูลใช้นี้เพื่อแสดง และลิงค์ไปยังข้อมูลโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="40d13-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="40d13-130">รวมถึงคุณสมบัติสำหรับหัวข้อ ขนาดของไทล์ ลิงก์ "ดูรายละเีอียด" และลิงก์ "เข้าร่วมเป็นสมาชิก"</span><span class="sxs-lookup"><span data-stu-id="40d13-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="40d13-131">ลิงค์ "ดูรายละเอียด" ควรถูกตั้งค่าให้เปลี่ยนเส้นทางไปยังหน้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="40d13-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="40d13-132">ลิงค์ "เข้าร่วมเป็นสมาชิก" ควรถูกตั้งค่าให้เปลี่ยนเส้นทางไปยังหน้าซึ่งผู้ใช้สามารถเข้าร่วมโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="40d13-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="40d13-133">หน้าประวัติคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="40d13-133">Order history page</span></span>

<span data-ttu-id="40d13-134">หน้าประวัติคำสั่งซื้อใช้โมดูลประวัติคำสั่งซื้อ เพื่อแสดงคำสั่งซื้อล่าสุดทั้งหมดที่ผู้ใช้ได้วางไว้</span><span class="sxs-lookup"><span data-stu-id="40d13-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="40d13-135">หน้ารายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="40d13-135">Order details page</span></span>

<span data-ttu-id="40d13-136">หน้ารายละเอียดของคำสั่งซื้อให้ข้อมูลรายละเอียดสำหรับแต่ละคำสั่งซื้อ และเข้าถึงได้จากหน้าประวัติการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="40d13-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="40d13-137">ใช้โมดูลรายละเอียดคำสั่งซื้อ ซึ่งจำเป็นต้องใช้รหัสการขายหรือรหัสธุรกรรมเพื่อดึงข้อมูลรายละเอียดของคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="40d13-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="40d13-138">หน้าโพรไฟล์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="40d13-138">User profile page</span></span>

<span data-ttu-id="40d13-139">หน้าโพรไฟล์ผู้ใช้จะแสดงรายละเอียดบัญชีผู้ใช้ เช่น ชื่อและที่อยู่อีเมลของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="40d13-139">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="40d13-140">ใช้โมดูลโพรไฟล์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="40d13-140">It uses the user profile module.</span></span> <span data-ttu-id="40d13-141">แม้ว่าจะไม่สามารถลบที่อยู่อีเมล์ได้ แต่คุณสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="40d13-141">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="40d13-142">หน้าโปรไฟล์ผู้ใช้ยังแสดงการกำหนดลักษณะผู้ใช้ที่ช่วยให้ผู้ใช้สามารถเข้าร่วมหรือเลือกไม่รับจากคุณลักษณะบางอย่าง เช่น การตั้งค่าส่วนบุคคลของรายการแนะนำ</span><span class="sxs-lookup"><span data-stu-id="40d13-142">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="40d13-143">หน้าที่อยู่ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="40d13-143">User address page</span></span>

<span data-ttu-id="40d13-144">หน้าที่อยู่ของผู้ใช้แสดงรายการของที่อยู่ที่เชื่อมโยงกับบัญชีผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="40d13-144">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="40d13-145">ผู้ใช้ให้ที่อยู่เหล่านี้ในระหว่างการชำระเงินหรือเพิ่มในหน้านี้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="40d13-145">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="40d13-146">โมดูลที่อยู่ของผู้ใช้ ใช้เพิ่มและแก้ไขที่อยู่ ตั้งค่าที่อยู่หลัก และแสดงที่อยู่ที่มีอยู่บนหน้า</span><span class="sxs-lookup"><span data-stu-id="40d13-146">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="40d13-147">หน้ารายการสิ่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="40d13-147">Wish list page</span></span>

<span data-ttu-id="40d13-148">หน้ารายการสิ่งที่ต้องการแสดงรายการที่มีการเพิ่มลงในรายการสิ่งที่ต้องการของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="40d13-148">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="40d13-149">ใช้โมดูรายการสิ่งที่ต้องการเพื่อแสดงรายการสินค้าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="40d13-149">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="40d13-150">หน้าการตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="40d13-150">Loyalty page</span></span>

<span data-ttu-id="40d13-151">หน้าสมาิชิก ให้ลูกค้าเข้าร่วมโปรแกรมตอบแทนลูกค้าสมาชิก หรือถ้าเป็นสมาชิกของโปรแกรมลูกค้าสมาชิกอยู่แล้ว ให้ดูรายละเอียดของโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="40d13-151">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="40d13-152">นอกจากนี้ยังสามารถดูคะแนนที่ได้รับ และแลกคะแนนในธุรกรรมล่าสุด</span><span class="sxs-lookup"><span data-stu-id="40d13-152">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40d13-153">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="40d13-153">Additional resources</span></span>

[<span data-ttu-id="40d13-154">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="40d13-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="40d13-155">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="40d13-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="40d13-156">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="40d13-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="40d13-157">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="40d13-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="40d13-158">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="40d13-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="40d13-159">โมดูลใบยืนยันคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="40d13-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="40d13-160">โมดูหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="40d13-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="40d13-161">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="40d13-161">Footer module</span></span>](author-footer-module.md)
