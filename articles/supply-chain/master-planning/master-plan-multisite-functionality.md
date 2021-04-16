---
title: ภาพรวมของการวางแผนหลักและฟังก์ชันหลายไซต์
description: การวางแผนหลักใช้การตั้งค่าไซต์และมิติสินค้าคงคลังของคลังสินค้ามาพิจารณา
author: roxanadiaconu
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e30bb8dfb790958b30cb3be807847ee737fb5026
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833580"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="30bc1-103">ภาพรวมของการวางแผนหลักและฟังก์ชันหลายไซต์</span><span class="sxs-lookup"><span data-stu-id="30bc1-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30bc1-104">การวางแผนหลักใช้การตั้งค่าไซต์และมิติสินค้าคงคลังของคลังสินค้ามาพิจารณา</span><span class="sxs-lookup"><span data-stu-id="30bc1-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="30bc1-105">มิติไซต์เป็นข้อมูลบังคับ และคุณสามารถตั้งค่ามิติคลังสินค้าให้เป็นข้อมูลบังคับได้</span><span class="sxs-lookup"><span data-stu-id="30bc1-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="30bc1-106">เมื่อมิติเป็นข้อมูลบังคับ คุณต้องป้อนค่ามิติบนธุรกรรมของสินค้าคงคลังทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="30bc1-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="30bc1-107">ดังนั้น ในระหว่างการวางแผนหลัก คุณต้องทราบไซต์และคลังสินค้าสำหรับความต้องการเริ่มแรก</span><span class="sxs-lookup"><span data-stu-id="30bc1-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="30bc1-108">มิติไซต์ยังต้องสอดคล้องในระหว่างการขยายความต้องการระดับล่าง ค่าไซต์ไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="30bc1-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="30bc1-109">เมื่อไม่ได้ตั้งค่าคลังสินค้าเป็นข้อมูลบังคับ จะไม่ทราบคลังสินค้าจากความต้องการเริ่มแรก</span><span class="sxs-lookup"><span data-stu-id="30bc1-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="30bc1-110">เครื่องวางแผนต้องกำหนดคลังสินค้าที่จะใช้ตามข้อมูลการตั้งค่าที่กำหนดสำหรับสินค้า คลังสินค้าแต่ละแห่ง และรายละเอียดของบรรทัดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="30bc1-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="30bc1-111">หัวข้อต่อไปนี้อธิบายวิธีการทำงานของเครื่องวางแผน เมื่อมีการกำหนดการตั้งค่าที่แตกต่างกันเพื่อกำหนดคลังสินค้าที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="30bc1-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="30bc1-112">การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า จำเป็นต้องมีคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="30bc1-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="30bc1-113">การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าบังคับ</span><span class="sxs-lookup"><span data-stu-id="30bc1-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="30bc1-114">การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า ไม่จำเป็นต้องมีคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="30bc1-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="30bc1-115">การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าไม่บังคับ</span><span class="sxs-lookup"><span data-stu-id="30bc1-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="30bc1-116">กำหนดเวอร์ชันสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="30bc1-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]