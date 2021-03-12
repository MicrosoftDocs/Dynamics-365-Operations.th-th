---
title: การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าบังคับ
description: หัวข้อนี้อธิบายวิธีการวางแผนสินค้าที่มีไซต์เป็นมิติความครอบคลุม คลังสินค้าเป็นมิติบังคับ
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
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72240e7db8ec914220cb8f8f1185a91a304ff66b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977974"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="145e5-104">การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าบังคับ</span><span class="sxs-lookup"><span data-stu-id="145e5-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="145e5-105">หัวข้อนี้อธิบายวิธีการวางแผนสินค้าที่มีไซต์เป็นมิติความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="145e5-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="145e5-106">คลังสินค้าเป็นมิติบังคับ</span><span class="sxs-lookup"><span data-stu-id="145e5-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="145e5-107">สถานการณ์จำลองการวางแผนหลักนี้มีเงื่อนไขดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="145e5-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="145e5-108">มิติไซต์มีการตั้งค่าเป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="145e5-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="145e5-109">การตั้งค่านี้ไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="145e5-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="145e5-110">มิติคลังสินค้ามีการตั้งค่าเป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="145e5-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="145e5-111">มิติไซต์ตั้งค่าสำหรับการวางแผนความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="145e5-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="145e5-112">อาจมีการตั้งค่ามิติอื่นสำหรับการวางแผนความครอบคลุมด้วย</span><span class="sxs-lookup"><span data-stu-id="145e5-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="145e5-113">อย่างไรก็ตาม การตั้งค่าเหล่านั้นไม่ได้รับผลกระทบจากฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="145e5-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="145e5-114">มิติคลังสินค้าไม่ได้ตั้งค่าสำหรับการวางแผนความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="145e5-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="145e5-115">ดังนั้น การจัดหาวัสดุและความต้องการถูกรวมโดยไซต์ และอาจรวมถึงมิติความครอบคลุมที่วางแผนอื่นด้วย</span><span class="sxs-lookup"><span data-stu-id="145e5-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="145e5-116">รูปภาพต่อไปนี้แสดงวิธีการประมวลผลการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="145e5-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="145e5-117">พารามิเตอร์ที่มีการอ้างอิงในรูปภาพ และตำแหน่งของพารามิเตอร์เหล่านั้นมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="145e5-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="145e5-118">มีการกำหนดความครอบคลุมสินค้าสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="145e5-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="145e5-119">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="145e5-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="145e5-120">เลือกสินค้า และคลิก **วางแผน &gt; ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="145e5-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="145e5-121">มีการกำหนดความสัมพันธ์ในการเติมสินค้าสำหรับคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="145e5-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="145e5-122">คลิก **การบริหารสินค้าคงคลัง &gt; การตั้งค่า &gt; แบ่งสินค้าคงคลัง &gt; คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="145e5-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="145e5-123">บนแท็บ **การวางแผนหลัก** ดูกลุ่มฟิลด์ **คลังสินค้าหลัก**</span><span class="sxs-lookup"><span data-stu-id="145e5-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="145e5-124">ใบสั่งประเภทใบสั่งเริ่มต้นถูกตั้งค่าเป็นการผลิต ใบสั่งซื้อ หรือคัมบัง</span><span class="sxs-lookup"><span data-stu-id="145e5-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="145e5-125">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="145e5-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="145e5-126">เลือกสินค้า และคลิก **วางแผน &gt; การตั้งค่าใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="145e5-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="145e5-127">ในฟอร์ม **การตั้งค่าใบสั่งเริ่มต้น** ดูฟิลด์ **ประเภทใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="145e5-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![ความต้องการความครอบคลุมไซต์ที่จำเป็นต้องมีคลังสินค้า](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="145e5-129">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="145e5-129">Additional resources</span></span>
--------

[<span data-ttu-id="145e5-130">ภาพรวมของการวางแผนหลักและฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="145e5-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="145e5-131">การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า จำเป็นต้องมีคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="145e5-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="145e5-132">การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าบังคับ</span><span class="sxs-lookup"><span data-stu-id="145e5-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="145e5-133">การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า ไม่จำเป็นต้องมีคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="145e5-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="145e5-134">กำหนดเวอร์ชันสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="145e5-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



