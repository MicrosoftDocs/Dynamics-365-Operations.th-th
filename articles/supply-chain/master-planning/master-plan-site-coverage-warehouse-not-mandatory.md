---
title: การวางแผนหลักสำหรับความครอบคลุมไซต์ที่ไม่จำเป็นต้องมีคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการวางแผนสินค้าที่มีไซต์เป็นชุดมิติความครอบคลุม
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f4cde5c570148ca58c4ea583a8f538a72d4957d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987057"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="f264a-103">การวางแผนหลักสำหรับความครอบคลุมไซต์ที่ไม่จำเป็นต้องมีคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f264a-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f264a-104">หัวข้อนี้อธิบายวิธีการวางแผนสินค้าที่มีไซต์เป็นชุดมิติความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="f264a-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="f264a-105">สถานการณ์จำลองการวางแผนหลักนี้มีเงื่อนไขดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f264a-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="f264a-106">มิติไซต์มีการตั้งค่าเป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f264a-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="f264a-107">ไม่ได้ตั้งค่ามิติคลังสินค้าเป็นข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="f264a-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="f264a-108">คุณอาจจะทราบคลังสินค้า แต่มันไม่ได้ใช้ในการคำนวณการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="f264a-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="f264a-109">มิติไซต์ตั้งค่าสำหรับการวางแผนความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="f264a-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="f264a-110">มิติคลังสินค้าไม่ได้ตั้งค่าสำหรับการวางแผนความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="f264a-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="f264a-111">ดังนั้น การจัดหาวัสดุและความต้องการถูกรวมโดยไซต์ และอาจรวมถึงมิติความครอบคลุมที่วางแผนอื่นด้วย</span><span class="sxs-lookup"><span data-stu-id="f264a-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="f264a-112">รูปภาพต่อไปนี้แสดงวิธีการประมวลผลการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="f264a-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="f264a-113">พารามิเตอร์ที่มีการอ้างอิงในรูปภาพ และตำแหน่งของพารามิเตอร์เหล่านั้นมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f264a-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="f264a-114">มีการกำหนดความครอบคลุมสินค้าสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="f264a-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="f264a-115">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="f264a-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="f264a-116">เลือกสินค้า และคลิก **วางแผน &gt; ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f264a-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="f264a-117">มีการกำหนดความสัมพันธ์ในการเติมสินค้าสำหรับคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="f264a-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="f264a-118">คลิก **การบริหารสินค้าคงคลัง &gt; การตั้งค่า &gt; แบ่งสินค้าคงคลัง &gt; คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f264a-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="f264a-119">บนแท็บ **การวางแผนหลัก** ดูกลุ่มฟิลด์ **คลังสินค้าหลัก**</span><span class="sxs-lookup"><span data-stu-id="f264a-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="f264a-120">ใบสั่งประเภทใบสั่งเริ่มต้นที่ถูกตั้งค่าเป็นการผลิต ใบสั่งซื้อหรือคัมบัง</span><span class="sxs-lookup"><span data-stu-id="f264a-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="f264a-121">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="f264a-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="f264a-122">เลือกสินค้า และคลิก **วางแผน &gt; การตั้งค่าใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="f264a-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="f264a-123">ในฟอร์ม **การตั้งค่าใบสั่งเริ่มต้น** ดูฟิลด์ **ประเภทใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="f264a-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![ความต้องการความครอบคลุมไซต์ที่ไม่จำเป็นต้องมีคลังสินค้า](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="f264a-125">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f264a-125">Additional resources</span></span>
--------

[<span data-ttu-id="f264a-126">ภาพรวมของการวางแผนหลักและฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="f264a-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="f264a-127">การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า จำเป็นต้องมีคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f264a-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="f264a-128">การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าบังคับ</span><span class="sxs-lookup"><span data-stu-id="f264a-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="f264a-129">การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าไม่บังคับ</span><span class="sxs-lookup"><span data-stu-id="f264a-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="f264a-130">กำหนดเวอร์ชันสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="f264a-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



