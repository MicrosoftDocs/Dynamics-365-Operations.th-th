---
title: ตั้งค่าคอนฟิกวิธีการชำระเงินด้วยบัญชีลูกค้าสำหรับไซต์อีคอมเมิร์ซของ B2B
description: ในหัวข้อนี้จะอธิบายวิธีตั้งค่าคอนฟิกวิธีการชำระเงินของบัญชีลูกค้าให้กับไซต์อีคอมเมิร์ซระหว่างธุรกิจ (B2B)
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 82dfd6ac7e97d838ef442fd6ded4a4f165fc795b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211212"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="73742-103">ตั้งค่าคอนฟิกวิธีการชำระเงินด้วยบัญชีลูกค้าสำหรับไซต์อีคอมเมิร์ซของ B2B</span><span class="sxs-lookup"><span data-stu-id="73742-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73742-104">ในหัวข้อนี้จะอธิบายวิธีตั้งค่าคอนฟิกวิธีการชำระเงินของบัญชีลูกค้าให้กับไซต์อีคอมเมิร์ซระหว่างธุรกิจ (B2B)</span><span class="sxs-lookup"><span data-stu-id="73742-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="73742-105">ผู้ค้าปลีกสามารถยอมรับการชำระเงินที่หลากหลายในซื้อสินค้าและบริการที่ผู้ค้าปลีกจำหน่ายในช่องทางอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="73742-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="73742-106">ชนิดการชำระเงินแต่ละชนิดที่ผู้ขายปลีกยอมรับ ต้องตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce เมื่อมีการตั้งค่าระบบ</span><span class="sxs-lookup"><span data-stu-id="73742-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="73742-107">ต้องสนับสนุนการชำระเงินบัญชีลูกค้า (หรือ "ในบัญชี") บนไซต์อีคอมเมิร์ซของ B2B</span><span class="sxs-lookup"><span data-stu-id="73742-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="73742-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="73742-108">Prerequisites</span></span>

1. <span data-ttu-id="73742-109">เพิ่มวิธีการชำระเงินของบัญชีลูกค้าในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="73742-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="73742-110">เชื่อมโยงวิธีการชำระเงินของบัญชีลูกค้ากับช่องทางอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="73742-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="73742-111">ตรวจสอบให้แน่ใจว่าเปิดใช้งาน **อนุญาตในบัญชี** กับลูกค้ารายนั้นที่ **Retail และ Commerce \> ลูกค้า \> ลูกค้าทั้งหมด \> ค่าเริ่มต้นของการชำระเงิน** ในศูนย์ควบคุม Commerce ได้</span><span class="sxs-lookup"><span data-stu-id="73742-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="73742-112">ตรวจสอบให้แน่ใจว่าพารามิเตอร์ **วงเงินสินเชื่อ** ได้รับการตั้งค่าอย่างเหมาะสมที่ **Retail และ Commerce \> ลูกค้า \> ลูกค้าทั้งหมด \> ค่าเริ่มต้นของการชำระเงิน** ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="73742-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="73742-113">เปิดใช้งานวิธีการชำระเงินด้วยบัญชีลูกค้าในตัวสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="73742-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="73742-114">หากต้องการเปิดใช้งานวิธีการชำระเงินด้วยบัญชีลูกค้าในตัวสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="73742-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="73742-115">ไปที่ **การตั้งค่าไซต์ \> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="73742-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="73742-116">ตั้งค่าคุณสมบัติ **เปิดใช้งานการชำระเงินด้วยบัญชีลูกค้า** เป็น **เปิดใช้งานแล้วสำหรับลูกค้า B2B**</span><span class="sxs-lookup"><span data-stu-id="73742-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="73742-117">เลือก **บันทึกและเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="73742-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="73742-118">การตั้งค่าโปรแกรมสร้างไซต์ใหม่จะมีผลเฉพาะหลังจากที่อัปเดตไฟล์ app.settings.json แล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="73742-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="73742-119">สำหรับข้อมูลเพิ่มเติม โปรดดู [SDK และอัปเดตไลบรารีโมดูล](../e-commerce-extensibility/sdk-updates.md)</span><span class="sxs-lookup"><span data-stu-id="73742-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="73742-120">เปิดใช้งานวิธีการชำระเงินของบัญชีลูกค้าในหน้าเช็คเอาท์ของไซต์อีคอมเมิร์ซของ B2B</span><span class="sxs-lookup"><span data-stu-id="73742-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="73742-121">หากต้องการเปิดใช้งานวิธีการชำระเงินของบัญชีลูกค้าในหน้าเช็คเอาท์ของไซต์อีคอมเมิร์ซของ B2B ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="73742-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="73742-122">ในตัวสร้างไซต์ Commerce ให้ค้นหาและแก้ไขหน้าเช็คเอาท์หรือบางส่วนของหน้าเช็คเอาท์ที่มีโมดูลเช็คเอาท์ของไซต์อีคอมเมิร์ซของ B2B</span><span class="sxs-lookup"><span data-stu-id="73742-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="73742-123">ในช่อง **คอนเทนเนอร์ส่วนเช็คเอาท์** ให้เลือก **เพิ่มโมดูล** แล้วเพิ่มโมดูล **การชำระเงินของบัญชีลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="73742-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="73742-124">จัดตําแหน่ง **การชำระเงินของบัญชีลูกค้า** โดยการเลือกจุดไข่ปลา (**...**) แล้วเลือก **เลื่อนขึ้น** หรือ **เลื่อนลง** ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="73742-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="73742-125">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="73742-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="73742-126">ยืนยันว่าวิธีการจ่ายเงินของบัญชีลูกค้าเปิดใช้งานและเผยแพร่แล้ว</span><span class="sxs-lookup"><span data-stu-id="73742-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="73742-127">หากต้องการยืนยันว่าวิธีการจ่ายเงินของบัญชีลูกค้าเปิดใช้งานแล้ว ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="73742-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="73742-128">ลงชื่อเข้าใช้ไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="73742-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="73742-129">เพิ่มผลิตภัณฑ์ลงในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="73742-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="73742-130">ไปที่หน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="73742-130">Go to the checkout page.</span></span> <span data-ttu-id="73742-131">คุณควรเห็นวิธีการชำระเงิน **บัญชีลูกค้า** ใหม่</span><span class="sxs-lookup"><span data-stu-id="73742-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73742-132">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="73742-132">Additional resources</span></span>

[<span data-ttu-id="73742-133">ตั้งค่าไซต์อีคอมเมิร์ซ B2B</span><span class="sxs-lookup"><span data-stu-id="73742-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="73742-134">สร้างลำดับชั้นการจำลององค์กรขององค์กร B2B</span><span class="sxs-lookup"><span data-stu-id="73742-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="73742-135">จัดการผู้ใช้คู่ค้าทางธุรกิจบนไซต์อีคอมเมิร์ซของ B2B</span><span class="sxs-lookup"><span data-stu-id="73742-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="73742-136">ตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์เกี่ยวกับไซต์อีคอมเมิร์ซของ B2B</span><span class="sxs-lookup"><span data-stu-id="73742-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="73742-137">การอัปเดต SDK และไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="73742-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]