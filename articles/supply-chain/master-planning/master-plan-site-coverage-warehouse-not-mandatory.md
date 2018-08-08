---
title: "การวางแผนหลักสำหรับความครอบคลุมไซต์ที่ไม่จำเป็นต้องมีคลังสินค้า"
description: "หัวข้อนี้อธิบายวิธีการวางแผนสินค้าที่มีไซต์เป็นชุดมิติความครอบคลุม"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 9475a7fbe40d7feb60c23e0d7164222469dffa75
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="afc54-103">การวางแผนหลักสำหรับความครอบคลุมไซต์ที่ไม่จำเป็นต้องมีคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="afc54-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afc54-104">หัวข้อนี้อธิบายวิธีการวางแผนสินค้าที่มีไซต์เป็นชุดมิติความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="afc54-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="afc54-105">สถานการณ์จำลองการวางแผนหลักนี้มีเงื่อนไขดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="afc54-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="afc54-106">มิติไซต์มีการตั้งค่าเป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="afc54-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="afc54-107">ไม่ได้ตั้งค่ามิติคลังสินค้าเป็นข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="afc54-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="afc54-108">คุณอาจจะทราบคลังสินค้า แต่มันไม่ได้ใช้ในการคำนวณการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="afc54-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="afc54-109">มิติไซต์ตั้งค่าสำหรับการวางแผนความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="afc54-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="afc54-110">มิติคลังสินค้าไม่ได้ตั้งค่าสำหรับการวางแผนความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="afc54-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="afc54-111">ดังนั้น การจัดหาวัสดุและความต้องการถูกรวมโดยไซต์ และอาจรวมถึงมิติความครอบคลุมที่วางแผนอื่นด้วย</span><span class="sxs-lookup"><span data-stu-id="afc54-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="afc54-112">รูปภาพต่อไปนี้แสดงวิธีการประมวลผลการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="afc54-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="afc54-113">พารามิเตอร์ที่มีการอ้างอิงในรูปภาพ และตำแหน่งของพารามิเตอร์เหล่านั้นมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="afc54-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="afc54-114">มีการกำหนดความครอบคลุมสินค้าสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="afc54-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="afc54-115">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="afc54-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="afc54-116">เลือกสินค้า และคลิก **วางแผน &gt; ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="afc54-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="afc54-117">มีการกำหนดความสัมพันธ์ในการเติมสินค้าสำหรับคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="afc54-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="afc54-118">คลิก **การบริหารสินค้าคงคลัง &gt; การตั้งค่า &gt; แบ่งสินค้าคงคลัง &gt; คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="afc54-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="afc54-119">บนแท็บ **การวางแผนหลัก** ดูกลุ่มฟิลด์ **คลังสินค้าหลัก**</span><span class="sxs-lookup"><span data-stu-id="afc54-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="afc54-120">ใบสั่งประเภทใบสั่งเริ่มต้นที่ถูกตั้งค่าเป็นการผลิต ใบสั่งซื้อหรือคัมบัง</span><span class="sxs-lookup"><span data-stu-id="afc54-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="afc54-121">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="afc54-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="afc54-122">เลือกสินค้า และคลิก **วางแผน &gt; การตั้งค่าใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="afc54-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="afc54-123">ในฟอร์ม **การตั้งค่าใบสั่งเริ่มต้น** ดูฟิลด์ **ประเภทใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="afc54-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![ความต้องการความครอบคลุมไซต์ที่ไม่จำเป็นต้องมีคลังสินค้า](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="afc54-125">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="afc54-125">Additional resources</span></span>
--------

[<span data-ttu-id="afc54-126">การวางแผนหลักและฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="afc54-126">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="afc54-127">การวางแผนหลัก - ความครอบคลุมไซต์ ข้อมูลบังคับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="afc54-127">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="afc54-128">การวางแผนหลัก - ความครอบคลุมไซต์และคลังสินค้า คลังสินค้าไม่ใช่ข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="afc54-128">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="afc54-129">การวางแผนหลัก- ความครอบคลุมไซต์และคลังสินค้า ข้อมูลบังคับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="afc54-129">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="afc54-130">การวางแผนหลัก - วิธีการกำหนดเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="afc54-130">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




