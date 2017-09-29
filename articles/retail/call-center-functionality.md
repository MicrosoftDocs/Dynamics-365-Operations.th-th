---
title: "ฟังก์ชันข้อมูลศูนย์บริการ"
description: "บทความนี้แสดงภาพรวมฟังก์ชันการขายของศูนย์บริการใน Microsoft Dynamics 365 for Retail"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 00d24e9933d087f150ec5270da94ad911423824d
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---

# <a name="call-center-functionality"></a><span data-ttu-id="cb2f0-103">ฟังก์ชันข้อมูลศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="cb2f0-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="cb2f0-104">บทความนี้แสดงภาพรวมฟังก์ชันการขายของศูนย์บริการใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="cb2f0-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="cb2f0-105">นอกจากนี้ Dynamics 365 for Retail ยังสนับสนุนศูนย์บริการเป็นชนิดของช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="cb2f0-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="cb2f0-106">ในศูนย์บริการ ผู้ปฏิบัติงานจะรับใบสั่งจากลูกค้าผ่านทางโทรศัพท์ และสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="cb2f0-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="cb2f0-107">ฟังก์ชันของศูนย์บริการรวมถึงคุณลักษณะที่ออกแบบมาเพื่อทำให้การรับใบสั่งทางโทรศัพท์เป็นเรื่องที่ง่ายขึ้น และจัดการกับการบริการลูกค้าตลอดทั้งกระบวนการเติมสินค้าตามใบสั่ง </span><span class="sxs-lookup"><span data-stu-id="cb2f0-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="cb2f0-108">ตัวอย่างเช่น ผู้ปฏิบัติงานของศูนย์บริการสามารถป้อนข้อมูลการชำระเงินได้โดยตรงลงในใบสั่งขาย และสามารถดูสรุปรายละเอียดของค่าธรรมเนียมและการชำระเงินก่อนที่จะส่งใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cb2f0-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="cb2f0-109">ผู้ปฏิบัติงานที่ยังมีตัวเลือกสำหรับการควบคุมการกำหนดราคา และสามารถเข้าถึงข้อมูลต่างๆ เกี่ยวกับลูกค้า ผลิตภัณฑ์ และราคาจากหน้า **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="cb2f0-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="cb2f0-110">นอกจากนี้ ศูนย์บริการมีสนับสนุนฟังก์ชันการติดตามประวัติและสถานะใบสั่งของลูกค้าอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="cb2f0-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="cb2f0-111">แต่ละศูนย์บริการสามารถมีผู้ใช้ของตนเอง วิธีการชำระเงิน กลุ่มราคา มิติทางการเงิน และวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="cb2f0-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="cb2f0-112">คุณสามารถกำหนดค่าตัวเลือกเหล่านี้เมื่อคุณสร้างศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="cb2f0-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="cb2f0-113">นอกจากนี้ คุณสามารถใช้หน้า **ศูนย์บริการ** เพื่อเปิดใช้งานหรือปิดใช้งานกลุ่มต่าง ๆ ของคุณลักษณะที่ไม่ซ้ำกันกับศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="cb2f0-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="cb2f0-114">**การดำเนินการใบสั่งให้เสร็จสมบูรณ์** – กลุ่มนี้รวมถึงคุณลักษณะที่เกี่ยวข้องกับการชำระเงินและการดำเนินการใบสั่งให้เสร็จสมบูรณ์ในแบบหน้า **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="cb2f0-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="cb2f0-115">**การขายที่สั่งการ** – กลุ่มนี้รวมถึงคุณลักษณะที่เกี่ยวข้องกับรหัสต้นทาง สคริปต์ และคำขอแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="cb2f0-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="cb2f0-116">หลังจากที่คุณเปิดใช้งานคุณลักษณะเหล่านี้ในการตั้งค่าศูนย์บริการ จะพร้อมใช้งานในหน้า **ใบสั่งขาย** สำหรับผู้ใช้ที่เชื่อมโยงกับศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="cb2f0-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="cb2f0-117">ลักษณะการทำงานเหล่านี้ส่วนใหญ่จำเป็นต้องตั้งค่าเพิ่มเติมก่อนที่จะสามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="cb2f0-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="cb2f0-118">ก่อนที่ผู้ใช้สามารถสร้างใบสั่งที่ศูนย์บริการได้ คุณต้องเพิ่มผู้ใช้เหล่านั้นที่ศูนย์บริการเป็นผู้ใช้ศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="cb2f0-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="cb2f0-119">ขั้นตอนนี้เปิดใช้งานการตั้งค่าคอนฟิกเฉพาะช่องทางศูนย์บริการและฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="cb2f0-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="cb2f0-120">ต่อไปนี้เป็นตัวอย่างของฟังก์ชันบางอย่างที่จะสามารถใช้งานได้:</span><span class="sxs-lookup"><span data-stu-id="cb2f0-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="cb2f0-121">การขายที่แนะนำให้ตั้งค่าคอนฟิกตัวเลือกสำหรับโทรศัพท์สคริปต์และรูปภาพผลิตภัณฑ์จะช่วยเหลือและแนะนำให้เจ้าหน้าที่ฝ่ายขายขณะใช้ใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cb2f0-121">Guided selling provides configuration options for telesales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="cb2f0-122">ใบสั่งจะไม่เสร็จสมบูรณ์จนกว่าพนักงานฝ่ายขายจะรวมวิธีการชำระเงินอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="cb2f0-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="cb2f0-123">สามารถกำหนดกฎการเพิ่มการขายหรือการขายสินค้าในพร้อมต์ให้พนักงานฝ่ายขายส่งเสริมผลิตภัณฑ์เฉพาะให้กับลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="cb2f0-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="cb2f0-124">พนักงานฝ่ายขายสามารถรวบรวมข้อมูลแหล่งที่มาของรหัสสำหรับแค็ตตาล็อกที่ลูกค้าจะสั่งซื้อได้</span><span class="sxs-lookup"><span data-stu-id="cb2f0-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="cb2f0-125">พนักงานฝ่ายขายสามารถเพิ่มคูปองผู้ค้าปลีกได้ที่ใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cb2f0-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="cb2f0-126">พนักงานฝ่ายขายสามารถขายโปรแกรมความต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="cb2f0-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="cb2f0-127">ใบสั่งสามารถถูกตั้งค่าสถานะระงับด้วยตนเองหรือโดยอัตโนมัติ เพื่อบ่งชี้ว่าจำเป็นต้องมีการตรวจสอบเพิ่มเติมก่อนที่จะสามารถประมวลผลใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cb2f0-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





