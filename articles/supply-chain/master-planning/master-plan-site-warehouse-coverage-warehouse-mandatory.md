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
ms.openlocfilehash: c52fc9955afe2a7502d0e1f9e7cdfc5b89bbb31d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "365350"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="4d704-104">การจัดกำหนดการหลักสำหรับความครอบคลุมไซต์และคลังสินค้า ข้อมูลบังคับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4d704-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d704-105">หัวข้อนี้อธิบายวิธีการวางแผนไซต์ความครอบคลุมมิติสินค้าที่มีไซต์และคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4d704-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="4d704-106">มิติคลังสินค้าเป็นข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="4d704-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="4d704-107">สถานการณ์จำลองการวางแผนหลักนี้มีเงื่อนไขดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4d704-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="4d704-108">มิติไซต์มีการตั้งค่าเป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="4d704-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="4d704-109">มิติคลังสินค้ามีการตั้งค่าเป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="4d704-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="4d704-110">ตั้งค่าไซต์และมิติคลังสินค้าสำหรับการวางแผนความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="4d704-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="4d704-111">อาจมีการตั้งค่ามิติอื่นสำหรับการวางแผนความครอบคลุมด้วย</span><span class="sxs-lookup"><span data-stu-id="4d704-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="4d704-112">อย่างไรก็ตาม การตั้งค่าเหล่านั้นไม่ได้รับผลกระทบจากฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="4d704-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="4d704-113">รูปภาพต่อไปนี้แสดงวิธีการประมวลผลการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="4d704-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="4d704-114">พารามิเตอร์ที่มีการอ้างอิงในรูปภาพ และตำแหน่งของพารามิเตอร์เหล่านั้นมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4d704-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="4d704-115">คลังสินค้ามีการตั้งค่าเป็น **ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="4d704-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="4d704-116">คลิก **การบริหารสินค้าคงคลัง &gt; การตั้งค่า &gt; แบ่งสินค้าคงคลัง &gt; คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4d704-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="4d704-117">บนแท็บด่วน **การวางแผนหลัก** ดูฟิลด์ **กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="4d704-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="4d704-118">มีการกำหนดความครอบคลุมสินค้าสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4d704-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="4d704-119">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="4d704-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="4d704-120">เลือกสินค้า จากนั้น บน บานหน้าต่างการดำเนินการ บนแท็บ **แผน** คลิก **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4d704-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="4d704-121">มีการกำหนดความสัมพันธ์ในการเติมสินค้าสำหรับคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="4d704-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="4d704-122">คลิก **การบริหารสินค้าคงคลัง &gt; การตั้งค่า &gt; แบ่งสินค้าคงคลัง &gt; คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4d704-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="4d704-123">บนแท็บด่วน **การวางแผนหลัก** ดูกลุ่มฟิลด์ **คลังสินค้าหลัก**</span><span class="sxs-lookup"><span data-stu-id="4d704-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="4d704-124">ใบสั่งประเภทใบสั่งเริ่มต้นถูกตั้งค่าเป็นการผลิต ใบสั่งซื้อ หรือคัมบัง</span><span class="sxs-lookup"><span data-stu-id="4d704-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="4d704-125">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="4d704-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="4d704-126">เลือกสินค้า จากนั้น บน บานหน้าต่างการดำเนินการ บนแท็บ **แผน** คลิก **การตั้งค่าใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="4d704-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="4d704-127">ในฟอร์ม **การตั้งค่าใบสั่งเริ่มต้น** ดูฟิลด์ **ประเภทใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="4d704-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![ความต้องการความครอบคลุมไซต์และคลังสินค้าที่จำเป็นต้องมีคลังสินค้า](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="4d704-129">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4d704-129">Additional resources</span></span>
--------

[<span data-ttu-id="4d704-130">การวางแผนหลักและฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="4d704-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="4d704-131">การวางแผนหลัก - ความครอบคลุมไซต์ ข้อมูลบังคับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4d704-131">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="4d704-132">การวางแผนหลัก - ความครอบคลุมไซต์ คลังสินค้าไม่ใช่ข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="4d704-132">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="4d704-133">การวางแผนหลัก - ความครอบคลุมไซต์และคลังสินค้า คลังสินค้าไม่ใช่ข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="4d704-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="4d704-134">การวางแผนหลัก - วิธีการกำหนดเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="4d704-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



