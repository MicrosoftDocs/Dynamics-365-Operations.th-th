---
title: ภาพรวมการบริหารคลังสินค้า
description: 'ใช้การบริหารคลังสินค้าเพื่อตรวจสอบและดำเนินกระบวนการคลังสินค้าแบบอัตโนมัติ '
author: ShylaThompson
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters, WHSWorkPool
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad0659a86e75dc4a5a204ebc05405f62abf2ca1e
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4438862"
---
# <a name="warehouse-management-overview"></a><span data-ttu-id="414dd-103">ภาพรวมของการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="414dd-103">Warehouse management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="414dd-104">โมดูลการบริหารคลังสินค้าช่วยให้คุณสามารถจัดการกระบวนการคลังสินค้าในการผลิต การกระจาย และบริษัทขายปลีก</span><span class="sxs-lookup"><span data-stu-id="414dd-104">The Warehouse management module lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="414dd-105">โมดูลนี้มีลักษณะการทำงานที่หลากหลายเพื่อรองรับสถานที่ตั้งคลังสินค้าในระดับที่ดีที่สุดได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="414dd-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="414dd-106">การจัดการคลังสินค้าถูกรวมเข้ากับกระบวนการทางธุรกิจอื่นๆ ทั้งหมด เช่น ค่าขนส่ง การผลิต การควบคุมคุณภาพ การซื้อ การโอนย้าย การขาย และการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="414dd-106">Warehouse management is fully integrated with other business processes such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="414dd-107">เริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="414dd-107">Get started</span></span>
<span data-ttu-id="414dd-108">เมื่อต้องการเริ่มการทำงานกับการจัดการคลังสินค้า คุณต้องดำเนินการตั้งค่าพารามิเตอร์คลังสินค้าทั่วไปเพื่อสนับสนุนกระบวนการทางธุรกิจของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="414dd-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of your company.</span></span>

- <span data-ttu-id="414dd-109">ไปที่หน้า **พารามิเตอร์การจัดการคลังสินค้า** ภายใต้ **การจัดการคลังสินค้า** > **ตั้งค่า** เพื่อตั้งค่าพารามิเตอร์คลังสินค้าทั่วไป</span><span class="sxs-lookup"><span data-stu-id="414dd-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="414dd-110">คุณต้องตั้งค่าคอนฟิกส่วนประกอบสำหรับลำดับงานของกระบวนการคลังสินค้าขาเข้าและขาออกตามความต้องการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="414dd-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="414dd-111">ส่วนประกอบสำคัญที่สุดที่คุณต้องตั้งค่าคอนฟิกคือ เท็มเพลตเวฟ เท็มเพลตงาน กลุ่มงาน และคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="414dd-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="414dd-112">ภาพรวมของการตั้งค่าคอนฟิกคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="414dd-112">Warehouse configuration overview</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="414dd-113">ควบคุมงานคลังสินค้าโดยเท็มเพลตงานและคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="414dd-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="414dd-114">ตั้งค่าอุปกรณ์เคลื่อนที่สำหรับงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="414dd-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="414dd-115">ตั้งค่าคำสั่งสถานที่สำหรับการสำรองใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="414dd-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="414dd-116">ตั้งค่าเท็มเพลตงานสำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="414dd-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="414dd-117">กระบวนการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="414dd-117">Warehouse management processes</span></span>
- <span data-ttu-id="414dd-118">การสนับสนุนแบบรวมสำหรับเอกสารต้นทางสำหรับใบสั่งขาย การส่งคืนสินค้า ใบสั่งโอนย้าย ใบสั่งผลิต และคัมบัง</span><span class="sxs-lookup"><span data-stu-id="414dd-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="414dd-119">การสนับสนุนลำดับงานวัสดุที่ยืดหยุ่นทั้งขาเข้าและขาออกที่ยึดตามแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="414dd-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="414dd-120">การรวมทั้งหมดกับข้อเสนอการผลิตและการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="414dd-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="414dd-121">การควบคุมทั้งหมดของขีดจำกัดการเก็บสต็อกในสถานที่และปริมาตรของสถานที่</span><span class="sxs-lookup"><span data-stu-id="414dd-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="414dd-122">คุณสมบัติของสินค้าคงคลังตามสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="414dd-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="414dd-123">ชุดงานทั้งหมดและการสนับสนุนของชุดสินค้า</span><span class="sxs-lookup"><span data-stu-id="414dd-123">Full batch and serial item support</span></span>
- <span data-ttu-id="414dd-124">ความสามารถในการรับสินค้าต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="414dd-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="414dd-125">กลยุทธ์การเบิกสินค้าหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="414dd-125">Multiple picking strategies</span></span>
- <span data-ttu-id="414dd-126">การสนับสนุนแบบนอกกรอบสำหรับบาร์โค้ดสแกนเนอร์บาร์โค้ดรุ่นถัดไป</span><span class="sxs-lookup"><span data-stu-id="414dd-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="414dd-127">ชนิดแท่นวางสินค้า/คอนเทนเนอร์สำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="414dd-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="414dd-128">ความสามารถในการตรวจนับขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="414dd-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="414dd-129">การพิมพ์ป้ายชื่อและการกำหนดเส้นทางป้ายชื่อด้วยการสนับสนุน Zebra ZPL</span><span class="sxs-lookup"><span data-stu-id="414dd-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="414dd-130">การรวม Business Intelligence ลงใน Power BI</span><span class="sxs-lookup"><span data-stu-id="414dd-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="414dd-131">ความเคลื่อนไหวของสินค้าคงคลังแบบด้วยตนเองและโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="414dd-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="414dd-132">การควบคุมคุณภาพแบบรวมทั้งหมด (QMS)</span><span class="sxs-lookup"><span data-stu-id="414dd-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="414dd-133">ความสามารถในการติดตามของการจัดการวัสดุของผู้ปฏิบัติงานแบบเต็มรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="414dd-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="414dd-134">การประมวลผลเวฟขาออก</span><span class="sxs-lookup"><span data-stu-id="414dd-134">Outbound wave processing</span></span>
- <span data-ttu-id="414dd-135">การสนับสนุนการบรรจุแบบทำด้วยตนเองและการบรรจุลงตู้บรรจุสินค้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="414dd-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="414dd-136">การเบิกสินค้าคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="414dd-136">Cluster picking</span></span>
- <span data-ttu-id="414dd-137">การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าแบบง่าย</span><span class="sxs-lookup"><span data-stu-id="414dd-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="414dd-138">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="414dd-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="414dd-139">มีอะไรใหม่และอะไรที่กำลังพัฒนา</span><span class="sxs-lookup"><span data-stu-id="414dd-139">What's new and in development</span></span>
<span data-ttu-id="414dd-140">ไปที่ [แผนการทำงาน Microsoft Dynamics 365](https://roadmap.dynamics.com/) เพื่อดูว่ามีการนำคุณลักษณะใหม่ใดออกใช้ และมีคุณลักษณะใหม่ใดบ้างที่กำลังพัฒนา</span><span class="sxs-lookup"><span data-stu-id="414dd-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="414dd-141">บล็อก</span><span class="sxs-lookup"><span data-stu-id="414dd-141">Blogs</span></span>
<span data-ttu-id="414dd-142">คุณสามารถค้นหาความคิดเห็น ข่าว หรือข้อมูลอื่นๆ เกี่ยวกับการจัดการคลังสินค้าและโซลูชันอื่นใน [บล็อก Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog)</span><span class="sxs-lookup"><span data-stu-id="414dd-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 

