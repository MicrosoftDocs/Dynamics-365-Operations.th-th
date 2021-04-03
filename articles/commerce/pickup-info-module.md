---
title: โมดูลข้อมูลการเบิกสินค้า
description: หัวข้อนี้ครอบคลุมถึงโมดูลข้อมูลการเบิกสินค้าและอธิบายวิธีการเพิ่มลงในหน้าเช็คเอาท์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 222e8ad79b30e5197f7140958309d442b284f286
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263191"
---
# <a name="pickup-information-module"></a><span data-ttu-id="85608-103">โมดูลข้อมูลการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="85608-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="85608-104">หัวข้อนี้ครอบคลุมถึงโมดูลข้อมูลการเบิกสินค้าและอธิบายวิธีการเพิ่มลงในหน้าเช็คเอาท์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="85608-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="85608-105">โมดูลการเบิกสินค้าสามารถใช้ในโมดูลการเช็คเอาท์เพื่อแสดงข้อมูลการเบิกสินค้าตามใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="85608-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="85608-106">ลูกค้าสามารถดูวันที่และช่องเวลาที่มีการเบิกสินค้าที่พร้อมใช้งาน แล้วเลือกเวลาที่เหมาะสมเพื่อเบิกสินค้าตามใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="85608-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="85608-107">ตัวอย่างเช่น ลูกค้าสามารถเลือกที่จะเบิกสินค้าในเวลา 15 น. เมื่อวันที่ 21 มีนาคมจากร้านค้าของซานฟรานซิสโก</span><span class="sxs-lookup"><span data-stu-id="85608-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="85608-108">ต้องตั้งค่าคอนฟิกช่องเวลาการเบิกสินค้าสำหรับร้านค้าที่เหมาะสมในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="85608-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="85608-109">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างและการอัพเดตช่องเวลาสำหรับการเบิกสินค้าของลูกค้า](dev-itpro/pickup-timeslots.md)</span><span class="sxs-lookup"><span data-stu-id="85608-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="85608-110">ถ้ามีการสร้างโมดูลการเบิกสินค้าไว้ในหน้าเช็คเอาท์ แต่ไม่มีการกำหนดช่องเวลาไว้สำหรับร้านค้าที่เลือกไว้สำหรับการเบิกสินค้า โมดูลจะแสดงข้อมูล แต่ผู้ใช้จะไม่สามารถเลือกช่องเวลาใด ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="85608-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="85608-111">ช่องเวลาไม่จำเป็นต้องระบุและไม่จำเป็นต้องใช้เพื่อวางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="85608-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="85608-112">ถ้ามีการเลือกหลายรายการสำหรับการเบิกสินค้าระหว่างร้านค้าหลายแห่ง โมดูลการเบิกสินค้าจะช่วยให้ผู้ใช้สามารถเลือกช่องเวลาสำหรับร้านค้าแต่ละร้าน โดยมีช่องเวลาดังกล่าวพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="85608-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="85608-113">การสนับสนุนสำหรับช่องเวลาและโมดูลข้อมูลการเบิกสินค้าสำหรับการชำระเงินจะพร้อมใช้งานใน Dynamics 365 Commerce รุ่น 10.0.15 และรุ่นใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="85608-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="85608-114">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการเลือกช่องเวลาโดยผ่านโมดูลข้อมูลการเบิกสินค้าบนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="85608-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![ตัวอย่างของโมดูลข้อมูลการเบิกสินค้าที่อยู่จัดส่งบนหน้าเช็คเอาท์](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="85608-116">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="85608-116">Module properties</span></span>

- <span data-ttu-id="85608-117">**หัวข้อ** – ป้อนหัวข้อเฉพาะสำหรับโมดูล</span><span class="sxs-lookup"><span data-stu-id="85608-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="85608-118">แสดงข้อมูลช่วงเวลาหลังจากวางใบสั่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="85608-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="85608-119">หลังจากวางใบสั่งแล้ว ข้อมูลเกี่ยวกับช่องเวลาที่เลือกสามารถดูได้ใน [โมดูลการยืนยันใบสั่ง](order-confirmation-module.md) และ [โมดูลรายละเอียดใบสั่ง](account-management.md#order-details-page)</span><span class="sxs-lookup"><span data-stu-id="85608-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="85608-120">ทั้งโมดูลเหล่านี้มีคุณสมบัติ **แสดงข้อมูลช่วงเวลา**</span><span class="sxs-lookup"><span data-stu-id="85608-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="85608-121">ก่อนที่จะสามารถแสดงช่องเวลาที่เลือกในระหว่างกระบวนการใบสั่ง คุณสมบัตินี้ต้องถูกตั้งค่าเป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="85608-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="85608-122">เพิ่มงโมดูลข้อมูลการเบิกสินค้าเช็คเอาท์ที่อยู่บนหน้า</span><span class="sxs-lookup"><span data-stu-id="85608-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="85608-123">สำหรับคำแนะนำเกี่ยวกับวิธีการเพิ่มโมดูลข้อมูลการเบิกสินค้าลงในหน้าเช็คเอาท์และตั้งค่าคุณสมบัติที่จำเป็น ให้ดูที่ [โมดูลเช็คเอาท์](add-checkout-module.md)</span><span class="sxs-lookup"><span data-stu-id="85608-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="85608-124">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้าการเช็คเอาท์อีคอมเมิร์ซ ซึ่งรวมถึงช่องเวลาสำหรับสินค้าในรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="85608-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![ตัวอย่างของหน้าการเช็คเอาท์อีคอมเมิร์ซ ซึ่งรวมถึงช่องเวลาสำหรับสินค้าในรายการเบิกสินค้า](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="85608-126">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="85608-126">Additional resources</span></span>

[<span data-ttu-id="85608-127">สร้างและอัพเดตที่ช่วงเวลาสำหรับการเบิกสินค้าของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="85608-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="85608-128">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="85608-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="85608-129">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="85608-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="85608-130">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="85608-130">Order details module</span></span>](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]