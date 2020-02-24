---
title: ไซต์และคลังสินค้าแบบรวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลไซต์และคลังสินค้าระหว่าง Finance and Operations และ Common Data Service
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 0f5ed58ad50df49250aa4c001401ff52d460dfa6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020035"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="3bfb4-103">ไซต์และคลังสินค้าแบบรวม</span><span class="sxs-lookup"><span data-stu-id="3bfb4-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="3bfb4-104">หัวข้อนี้อธิบายการรวมของข้อมูลไซต์และคลังสินค้าระหว่าง Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3bfb4-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="3bfb4-105">ไซต์และคลังสินค้าการดำเนินงานเป็นแนวคิดทั่วไปในแอพลิเคชัน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3bfb4-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="3bfb4-106">มีการใช้เพื่อจำลองห่วงโซ่อุปทานของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="3bfb4-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="3bfb4-107">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="3bfb4-107">Templates</span></span>

<span data-ttu-id="3bfb4-108">ด้วยการรวมกับ Common Data Service แนวคิดเหล่านี้และข้อมูลที่เกี่ยวข้องทั้งหมดจะพร้อมใช้งานใน Common Data Service โดยใช้ไซต์และเอนทิตีข้อมูลคลังสินค้าในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3bfb4-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="3bfb4-109">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3bfb4-109">Finance and Operations apps</span></span> | <span data-ttu-id="3bfb4-110">แอปพลิเคชันอื่น ๆ ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3bfb4-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="3bfb4-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3bfb4-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="3bfb4-112">ไซต์</span><span class="sxs-lookup"><span data-stu-id="3bfb4-112">Sites</span></span> | <span data-ttu-id="3bfb4-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="3bfb4-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="3bfb4-114">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="3bfb4-114">Warehouses</span></span> | <span data-ttu-id="3bfb4-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="3bfb4-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

