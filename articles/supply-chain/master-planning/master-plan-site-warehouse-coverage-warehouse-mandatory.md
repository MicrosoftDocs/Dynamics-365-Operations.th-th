---
title: การจัดกำหนดการหลักสำหรับความครอบคลุมไซต์และคลังสินค้า ข้อมูลบังคับคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการวางแผนไซต์ความครอบคลุมมิติสินค้าที่มีไซต์และคลังสินค้า มิติคลังสินค้าเป็นข้อมูลบังคับ
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
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11720b70697112085ac612fc9eded8292a68ab2d
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815099"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="12b29-104">การจัดกำหนดการหลักสำหรับความครอบคลุมไซต์และคลังสินค้า ข้อมูลบังคับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="12b29-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12b29-105">หัวข้อนี้อธิบายวิธีการวางแผนไซต์ความครอบคลุมมิติสินค้าที่มีไซต์และคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="12b29-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="12b29-106">มิติคลังสินค้าเป็นข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="12b29-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="12b29-107">สถานการณ์จำลองการวางแผนหลักนี้มีเงื่อนไขดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="12b29-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="12b29-108">มิติไซต์มีการตั้งค่าเป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="12b29-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="12b29-109">มิติคลังสินค้ามีการตั้งค่าเป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="12b29-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="12b29-110">ตั้งค่าไซต์และมิติคลังสินค้าสำหรับการวางแผนความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="12b29-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="12b29-111">อาจมีการตั้งค่ามิติอื่นสำหรับการวางแผนความครอบคลุมด้วย</span><span class="sxs-lookup"><span data-stu-id="12b29-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="12b29-112">อย่างไรก็ตาม การตั้งค่าเหล่านั้นไม่ได้รับผลกระทบจากฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="12b29-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="12b29-113">รูปภาพต่อไปนี้แสดงวิธีการประมวลผลการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="12b29-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="12b29-114">พารามิเตอร์ที่มีการอ้างอิงในรูปภาพ และตำแหน่งของพารามิเตอร์เหล่านั้นมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="12b29-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="12b29-115">คลังสินค้ามีการตั้งค่าเป็น **ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="12b29-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="12b29-116">คลิก **การบริหารสินค้าคงคลัง &gt; การตั้งค่า &gt; แบ่งสินค้าคงคลัง &gt; คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="12b29-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="12b29-117">บนแท็บด่วน **การวางแผนหลัก** ดูฟิลด์ **กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="12b29-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="12b29-118">มีการกำหนดความครอบคลุมสินค้าสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="12b29-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="12b29-119">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="12b29-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="12b29-120">เลือกสินค้า จากนั้น บน บานหน้าต่างการดำเนินการ บนแท็บ **แผน** คลิก **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="12b29-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="12b29-121">มีการกำหนดความสัมพันธ์ในการเติมสินค้าสำหรับคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="12b29-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="12b29-122">คลิก **การบริหารสินค้าคงคลัง &gt; การตั้งค่า &gt; แบ่งสินค้าคงคลัง &gt; คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="12b29-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="12b29-123">บนแท็บด่วน **การวางแผนหลัก** ดูกลุ่มฟิลด์ **คลังสินค้าหลัก**</span><span class="sxs-lookup"><span data-stu-id="12b29-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="12b29-124">ใบสั่งประเภทใบสั่งเริ่มต้นถูกตั้งค่าเป็นการผลิต ใบสั่งซื้อ หรือคัมบัง</span><span class="sxs-lookup"><span data-stu-id="12b29-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="12b29-125">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="12b29-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="12b29-126">เลือกสินค้า จากนั้น บน บานหน้าต่างการดำเนินการ บนแท็บ **แผน** คลิก **การตั้งค่าใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="12b29-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="12b29-127">ในฟอร์ม **การตั้งค่าใบสั่งเริ่มต้น** ดูฟิลด์ **ประเภทใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="12b29-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![ความต้องการความครอบคลุมไซต์และคลังสินค้าที่จำเป็นต้องมีคลังสินค้า](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="12b29-129">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="12b29-129">Additional resources</span></span>
--------

[<span data-ttu-id="12b29-130">ภาพรวมของการวางแผนหลักและฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="12b29-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="12b29-131">การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าบังคับ</span><span class="sxs-lookup"><span data-stu-id="12b29-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="12b29-132">การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าไม่บังคับ</span><span class="sxs-lookup"><span data-stu-id="12b29-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="12b29-133">การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า ไม่จำเป็นต้องมีคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="12b29-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="12b29-134">กำหนดเวอร์ชันสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="12b29-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



