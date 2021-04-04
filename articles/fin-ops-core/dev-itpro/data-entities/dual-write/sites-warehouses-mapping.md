---
title: ไซต์และคลังสินค้าแบบรวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลไซต์และคลังสินค้าระหว่าง Finance and Operations และ Dataverse
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: b93e5f15e281c20f8688d496fc78f8b46b8aa996
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560372"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="1be6a-103">ไซต์และคลังสินค้าแบบรวม</span><span class="sxs-lookup"><span data-stu-id="1be6a-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="1be6a-104">หัวข้อนี้อธิบายการรวมของข้อมูลไซต์และคลังสินค้าระหว่าง Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="1be6a-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="1be6a-105">ไซต์และคลังสินค้าการดำเนินงานเป็นแนวคิดทั่วไปในแอพลิเคชัน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1be6a-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="1be6a-106">มีการใช้เพื่อจำลองห่วงโซ่อุปทานของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="1be6a-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="1be6a-107">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="1be6a-107">Templates</span></span>

<span data-ttu-id="1be6a-108">ด้วยการรวมกับ Dataverse แนวคิดเหล่านี้และข้อมูลที่เกี่ยวข้องทั้งหมดจะพร้อมใช้งานใน Dataverse โดยใช้ไซต์และตารางข้อมูลคลังสินค้าในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1be6a-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="1be6a-109">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1be6a-109">Finance and Operations apps</span></span> | <span data-ttu-id="1be6a-110">แอปพลิเคชันอื่น ๆ ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="1be6a-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="1be6a-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1be6a-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="1be6a-112">ไซต์</span><span class="sxs-lookup"><span data-stu-id="1be6a-112">Sites</span></span> | <span data-ttu-id="1be6a-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="1be6a-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="1be6a-114">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="1be6a-114">Warehouses</span></span> | <span data-ttu-id="1be6a-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="1be6a-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]