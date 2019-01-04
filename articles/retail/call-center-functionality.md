---
title: "ฟังก์ชัน Sales ของศูนย์บริการ"
description: "หัวข้อนี้แสดงภาพรวมฟังก์ชันการขายของศูนย์บริการใน Microsoft Dynamics 365 for Retail"
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 8b78762ce70b318e1f77e1e49ffaa7b72f01667f
ms.contentlocale: th-th
ms.lasthandoff: 01/04/2019

---

# <a name="call-center-sales-functionality"></a><span data-ttu-id="aba15-103">ฟังก์ชัน Sales ของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="aba15-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aba15-104">ใน Dynamics 365 for Retail ศูนย์บริการคือ ชนิดของช่องทางการขายปลีกที่สามารถถูกกำหนดได้ในแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="aba15-104">In Dynamics 365 for Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="aba15-105">การกำหนดช่องทางเฉพาะสำหรับเอนทิตีศูนย์บริการของคุณ ช่วยให้ระบบสามารถผูกค่าเริ่มต้นของข้อมูลที่เฉพาะเจาะจงและค่าเริ่มต้นของการประมวลผลใบสั่งกับใบสั่งขาย ที่สร้างขึ้นโดยผู้ใช้ของช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="aba15-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="aba15-106">คุณลักษณะของศูนย์บริการประกอบด้วย ราคาขายปลีกขั้นสูงและการส่งเสริมการขาย แค็ตตาล็อก บัตรของขวัญ โปรแกรมตอบแทนลูกค้าสมาชิก และคูปอง</span><span class="sxs-lookup"><span data-stu-id="aba15-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="aba15-107">ใบสั่งของศูนย์บริการยังเพิ่มขึ้นโดยแอพลิเคชันการขายหน้าร้าน (POS) เพื่อสนับสนุนสถานการณ์จำลองการเติมช่องสัญญาณระหว่างใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="aba15-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="aba15-108">จำเป็นต้องทราบว่า ขณะที่สามารถใช้โมดูลศูนย์บริการโดยอุตสาหกรรมอื่นๆ นอกจากการขายปลีก การนำออกใช้ปัจจุบันของแอพลิเคชันศูนย์บริการ Dynamics 365 for Retail ยังไม่มีการปรับให้เหมาะสมสำหรับการใช้ในสถานการณ์จำลองการประมวลผลใบสั่งแบบระหว่างธุรกิจ (B2B) หรือสถานการณ์จำลองที่ใบสั่งมีรายการขายจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="aba15-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Dynamics 365 for Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="aba15-109">ขอแนะนำว่า ผู้ใช้ที่ต้องการใช้คุณลักษณะของศูนย์บริการสำหรับการประมวลผลใบสั่ง ภายนอกการประมวลผลธุรกรรมแบบโดยตรงต่อผู้บริโภคทั่วไป ใช้เวลาที่เพียงพอในการทดสอบ และตรวจสอบว่าการเปิดใช้งานฟังก์ชันศูนย์บริการจะสอดคล้องกับความต้องการด้านประสิทธิภาพและด้านการทำงาน</span><span class="sxs-lookup"><span data-stu-id="aba15-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="aba15-110">นอกเหนือจากการสนับสนุนการสร้างใบสั่ง โมดูลศูนย์บริการยังให้แอพลิเคชันบริการลูกค้าที่เข้าใจง่าย ซึ่งทำให้ง่ายขึ้นสำหรับผู้ใช้ในการค้นหาบัญชีลูกค้าและในการตรวจทานข้อมูลใบสั่งของลูกค้าที่เกี่ยวข้องและแอททริบิวต์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="aba15-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="aba15-111">หน้าจอบริการลูกค้าถูกออกแบบมาเพื่อเปิดใช้งานผู้ใช้ให้สามารถเข้าถึงข้อมูลที่เกี่ยวข้องกับใบสั่งได้อย่างรวดเร็ว ซึ่งจะอนุญาตให้ตอบคำถามทั่วไปที่เกี่ยวกับใบสั่งส่วนมากที่ได้รับจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="aba15-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="aba15-112">หน้านี้แสดงลิงค์ไปยังเอกสารที่เกี่ยวข้องซึ่งเกี่ยวข้องกับการตั้งค่า การตั้งค่าคอนฟิก และการใช้ด้านการทำงานของคุณลักษณะศูนย์บริการใน Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="aba15-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Dynamics 365 for Retail.</span></span>

## <a name="configure-the-call-center"></a><span data-ttu-id="aba15-113">ตั้งค่าคอนฟิกศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="aba15-113">Configure the call center</span></span>

[<span data-ttu-id="aba15-114">ตั้งค่าตัวเลือกการประมวลผลใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="aba15-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="aba15-115">ตั้งค่าคอนฟิกการประมวลผลใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="aba15-115">Configure order processing</span></span>

[<span data-ttu-id="aba15-116">ตั้งค่าการแจ้งเตือนการตรวจสอบการฉ้อโกง</span><span class="sxs-lookup"><span data-stu-id="aba15-116">Set up fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="aba15-117">ระงับใบสั่งด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="aba15-117">Manual Order Holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="aba15-118">ตั้งค่าคอนฟิกการประมวลผลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="aba15-118">Configure payment processing</span></span>

[<span data-ttu-id="aba15-119">วิธีการชำระเงินในศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="aba15-119">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="aba15-120">ตั้งค่าคอนฟิกโหมดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="aba15-120">Configure delivery modes</span></span>

[<span data-ttu-id="aba15-121">ตั้งค่าคอนฟิกศูนย์บริการ โหมดการจัดส่ง และค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="aba15-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="aba15-122">ตั้งค่าคอนฟิกการตลาดโดยตรง</span><span class="sxs-lookup"><span data-stu-id="aba15-122">Configure direct marketing</span></span>

[<span data-ttu-id="aba15-123">แค็ตตาล็อกของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="aba15-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="aba15-124">ตั้งค่าการวิเคราะห์ RFM</span><span class="sxs-lookup"><span data-stu-id="aba15-124">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="aba15-125">ตั้งค่าคอนฟิกโปรแกรมความต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="aba15-125">Configure continuity programs</span></span>

[<span data-ttu-id="aba15-126">ตั้งค่าโปรแกรมความต่อเนื่องสำหรับศูนย์บริการทางโทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="aba15-126">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)

