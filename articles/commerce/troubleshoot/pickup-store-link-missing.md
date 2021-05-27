---
title: ตัวเลือกการเบิกสินค้านี้จะไม่ปรากฏในหน้ารถเข็นหรือรายละเอียดผลิตภัณฑ์
description: หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อตัวเลือกสําหรับการเบิกสินค้าในร้านค้าไม่ปรากฏบนหน้ารถเข็นหรือหน้ารายละเอียดผลิตภัณฑ์
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f692d73bf1755422e9bfc8314c1156e043ccf761
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020828"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="ece23-103">ตัวเลือก "การเบิกสินค้านี้" จะไม่ปรากฏในหน้ารถเข็นหรือรายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ece23-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ece23-104">หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อตัวเลือกสําหรับการเบิกสินค้าในร้านค้าไม่ปรากฏบนหน้ารถเข็นหรือหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ece23-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="ece23-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="ece23-105">Description</span></span>

<span data-ttu-id="ece23-106">ปุ่ม **การเบิกสินค้านี้** จะไม่ปรากฏในหน้ารถเข็นหรือรายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ece23-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="ece23-107">รูปภาพประกอบต่อไปนี้จะแสดงตัวอย่างของหน้าที่มีปุ่ม **เบิกสินค้านี้**</span><span class="sxs-lookup"><span data-stu-id="ece23-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![ปุ่มเบิกสินค้านี้](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="ece23-109">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="ece23-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="ece23-110">เปิดใช้งานส่วนขยาย BOPIS ของโปรแกรมสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="ece23-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="ece23-111">หากต้องการเปิดใช้งานส่วนขยาย "ซื้อออนไลน์ ให้เบิกสินค้าในร้านค้า" (BOPIS) ของโปรแกรมสร้างไซต์ Commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ece23-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ece23-112">เลือกไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ece23-112">Select your site.</span></span>
1. <span data-ttu-id="ece23-113">เลือก **การตั้งค่าไซต์** แล้วจากนั้นเลือก **ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="ece23-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="ece23-114">ตรวจสอบให้แน่ใจว่ามีการล้างข้อมูลตัวเลือก **ปิดใช้งาน BOPIS**</span><span class="sxs-lookup"><span data-stu-id="ece23-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="ece23-115">ตั้งค่าคอนฟิกวิธีการจัดส่งในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="ece23-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="ece23-116">หากต้องการตั้งค่าคอนฟิกโหมดการจัดส่งในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ece23-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ece23-117">ไปที่ **การจัดซื้อและการจัดหา \>การตั้งค่า \> โหมดการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="ece23-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="ece23-118">ตรวจสอบให้แน่ใจว่ามีการสร้างโหมดการจัดส่ง **เบิกสินค้าของลูกค้า** และมีการมอบหมายผลิตภัณฑ์และที่อยู่ให้กับวิธีการเบิกสินค้านั้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="ece23-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="ece23-119">ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="ece23-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="ece23-120">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ใบสั่งของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="ece23-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="ece23-121">ตรวจสอบให้แน่ใจว่ามีการตั้งค่าคอนฟิก **โหมดการเบิกของสำหรับจัดส่ง** อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ece23-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="ece23-122">การตั้งค่าคอนฟิกการชำระเงินใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="ece23-122">Configure customer orders payments</span></span>

<span data-ttu-id="ece23-123">หากต้องการตั้งค่าคอนฟิกการชำระเงินใบสั่งของลูกค้าในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ece23-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ece23-124">ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="ece23-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="ece23-125">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ใบสั่งของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="ece23-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="ece23-126">บนแท็บด่วน **การชำระเงิน** โปรดตรวจสอบให้แน่ใจว่าได้ตั้งค่าฟิลด์ **เงื่อนไขการชำระเงิน** และ **วิธีการชำระเงิน** อย่างถูกต้องแล้ว</span><span class="sxs-lookup"><span data-stu-id="ece23-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ece23-127">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ece23-127">Additional resources</span></span>

[<span data-ttu-id="ece23-128">ตั้งค่าคอนฟิก BOPIS</span><span class="sxs-lookup"><span data-stu-id="ece23-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="ece23-129">เปิดใช้งานวิธีการจัดส่งหลายครั้งสำหรับใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="ece23-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="ece23-130">การชำระเงินใบสั่ง Commerce ผ่านช่องทาง Omni</span><span class="sxs-lookup"><span data-stu-id="ece23-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="ece23-131">โมดูลตัวเลือกการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="ece23-131">Store selector module</span></span>](../store-selector.md)
