---
title: "การวางแผนหลักและฟังก์ชันหลายไซต์"
description: "การวางแผนหลักใช้การตั้งค่าไซต์และมิติสินค้าคงคลังของคลังสินค้ามาพิจารณา"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 10981e0fe201566c83fd28c792000865bc533cd3
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="master-planning-and-multisite-functionality"></a><span data-ttu-id="38185-103">การวางแผนหลักและฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="38185-103">Master planning and multisite functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38185-104">การวางแผนหลักใช้การตั้งค่าไซต์และมิติสินค้าคงคลังของคลังสินค้ามาพิจารณา</span><span class="sxs-lookup"><span data-stu-id="38185-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="38185-105">มิติไซต์เป็นข้อมูลบังคับ และคุณสามารถตั้งค่ามิติคลังสินค้าให้เป็นข้อมูลบังคับได้</span><span class="sxs-lookup"><span data-stu-id="38185-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="38185-106">เมื่อมิติเป็นข้อมูลบังคับ คุณต้องป้อนค่ามิติบนธุรกรรมของสินค้าคงคลังทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="38185-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="38185-107">ดังนั้น ในระหว่างการวางแผนหลัก คุณต้องทราบไซต์และคลังสินค้าสำหรับความต้องการเริ่มแรก</span><span class="sxs-lookup"><span data-stu-id="38185-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="38185-108">มิติไซต์ยังต้องสอดคล้องในระหว่างการขยายความต้องการระดับล่าง ค่าไซต์ไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="38185-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="38185-109">เมื่อไม่ได้ตั้งค่าคลังสินค้าเป็นข้อมูลบังคับ จะไม่ทราบคลังสินค้าจากความต้องการเริ่มแรก</span><span class="sxs-lookup"><span data-stu-id="38185-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="38185-110">เครื่องวางแผนต้องกำหนดคลังสินค้าที่จะใช้ตามข้อมูลการตั้งค่าที่กำหนดสำหรับสินค้า คลังสินค้าแต่ละแห่ง และรายละเอียดของบรรทัดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="38185-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="38185-111">หัวข้อต่อไปนี้อธิบายวิธีการทำงานของเครื่องวางแผน เมื่อมีการกำหนดการตั้งค่าที่แตกต่างกันเพื่อกำหนดคลังสินค้าที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="38185-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="38185-112">การวางแผนหลัก- ความครอบคลุมไซต์และคลังสินค้า ข้อมูลบังคับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="38185-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="38185-113">การวางแผนหลัก - ความครอบคลุมไซต์ ข้อมูลบังคับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="38185-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="38185-114">การวางแผนหลัก - ความครอบคลุมไซต์และคลังสินค้า คลังสินค้าไม่ใช่ข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="38185-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="38185-115">การวางแผนหลัก - ความครอบคลุมไซต์ คลังสินค้าไม่ใช่ข้อมูลบังคับ</span><span class="sxs-lookup"><span data-stu-id="38185-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="38185-116">การวางแผนหลัก - วิธีการกำหนดเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="38185-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




