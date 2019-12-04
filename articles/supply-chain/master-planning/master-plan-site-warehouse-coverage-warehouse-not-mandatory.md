---
title: การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า คลังสินค้าไม่ใช่ข้อมูลบังคับ
description: หัวข้อนี้อธิบายวิธีการวางแผนไซต์ความครอบคลุมมิติสินค้าที่มีไซต์และคลังสินค้า มิติคลังสินค้าไม่ได้เป็นข้อมูลบังคับ
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cea228e04632bd61f60771b09481241df5d16bd3
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813718"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="f0701-104">การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า คลังสินค้าไม่ใช่ข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="f0701-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0701-105">หัวข้อนี้อธิบายวิธีการวางแผนไซต์ความครอบคลุมมิติสินค้าที่มีไซต์และคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0701-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="f0701-106">มิติคลังสินค้าไม่ได้เป็นข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="f0701-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="f0701-107">สถานการณ์จำลองการวางแผนหลักนี้มีเงื่อนไขดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f0701-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="f0701-108">มิติไซต์มีการตั้งค่าเป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f0701-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="f0701-109">การตั้งค่านี้ไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="f0701-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="f0701-110">ไม่ได้ตั้งค่ามิติคลังสินค้าเป็นข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="f0701-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="f0701-111">คุณอาจจะทราบคลังสินค้า แต่มันไม่ได้ใช้ในการคำนวณการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="f0701-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="f0701-112">ตั้งค่าไซต์และมิติคลังสินค้าสำหรับการวางแผนความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="f0701-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="f0701-113">อาจมีการตั้งค่ามิติอื่นสำหรับการวางแผนความครอบคลุมด้วย</span><span class="sxs-lookup"><span data-stu-id="f0701-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="f0701-114">อย่างไรก็ตาม การตั้งค่าเหล่านั้นไม่ได้รับผลกระทบจากฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="f0701-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="f0701-115">รูปภาพต่อไปนี้แสดงวิธีการประมวลผลการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="f0701-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="f0701-116">พารามิเตอร์ที่มีการอ้างอิงในรูปภาพ และตำแหน่งของพารามิเตอร์เหล่านั้นมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f0701-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="f0701-117">คลังสินค้ามีการตั้งค่าเป็น ด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="f0701-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="f0701-118">คลิก **การบริหารสินค้าคงคลัง &gt; การตั้งค่า &gt; แบ่งสินค้าคงคลัง &gt; คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f0701-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="f0701-119">บนแท็บด่วน **การวางแผนหลัก** ดูฟิลด์ **กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="f0701-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="f0701-120">มีการกำหนดความครอบคลุมสินค้าสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0701-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="f0701-121">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="f0701-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="f0701-122">เลือกสินค้า จากนั้น บน บานหน้าต่างการดำเนินการ บนแท็บ **แผน** คลิก **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f0701-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="f0701-123">มีการกำหนดความสัมพันธ์ในการเติมสินค้าสำหรับคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="f0701-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="f0701-124">คลิก **การบริหารสินค้าคงคลัง &gt; การตั้งค่า &gt; แบ่งสินค้าคงคลัง &gt; คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f0701-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="f0701-125">บนแท็บด่วน **การวางแผนหลัก** ดูกลุ่มฟิลด์ **คลังสินค้าหลัก**</span><span class="sxs-lookup"><span data-stu-id="f0701-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="f0701-126">ใบสั่งประเภทใบสั่งเริ่มต้นถูกตั้งค่าเป็นการผลิต ใบสั่งซื้อ หรือคัมบัง</span><span class="sxs-lookup"><span data-stu-id="f0701-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="f0701-127">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="f0701-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="f0701-128">เลือกสินค้า จากนั้น บน บานหน้าต่างการดำเนินการ บนแท็บ **แผน** คลิก **การตั้งค่าใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="f0701-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="f0701-129">ในฟอร์ม **การตั้งค่าใบสั่งเริ่มต้น** ดูฟิลด์ **ประเภทใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="f0701-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![ความต้องการสำหรับไซต์และคลังสินค้าที่ไม่จำเป็นต้องมีคลังสินค้า](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="f0701-131">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f0701-131">Additional resources</span></span>
--------

[<span data-ttu-id="f0701-132">ภาพรวมของการวางแผนหลักและฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="f0701-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="f0701-133">การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าบังคับ</span><span class="sxs-lookup"><span data-stu-id="f0701-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="f0701-134">การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า จำเป็นต้องมีคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0701-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="f0701-135">การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า ไม่จำเป็นต้องมีคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0701-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="f0701-136">กำหนดเวอร์ชันสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="f0701-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



