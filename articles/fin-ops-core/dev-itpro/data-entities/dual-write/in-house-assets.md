---
title: สินทรัพย์ภายในองค์กรสำหรับการให้บริการ
description: หัวข้อนี้จะอธิบายถึงวิธีการที่คุณสามารถใช้ Microsoft Dtnamics 365 Field Service เพื่อให้บริการทั้งสินทรัพย์ของลูกค้าและสินทรัพย์ภายในองค์กร
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 1e423199d0639db5e403e280880036b590149095
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172957"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="29bb8-103">สินทรัพย์ภายในองค์กรสำหรับการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="29bb8-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="29bb8-104">Microsoft Dynamics 365 Field Service ได้รับการออกแบบมาเพื่อให้บริการสินทรัพย์ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="29bb8-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="29bb8-105">การจัดการสินทรัพย์สำหรับ Dynamics 365 Supply Chain Management ได้รับการออกแบบเพื่อรักษาสินทรัพย์ภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="29bb8-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="29bb8-106">การรวมกันของแอปทั้งสองนี้จะช่วยให้คุณสามารถใช้ Field Service เพื่อให้บริการทั้งสินทรัพย์ของลูกค้าและสินทรัพย์ภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="29bb8-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="29bb8-107">นอกจากนี้ คุณยังสามารถจัดประเภทสินทรัพย์ได้ตามตำแหน่งที่ทำงานหรือลำดับชั้น และติดตามการให้บริการในระดับที่ละเอียด</span><span class="sxs-lookup"><span data-stu-id="29bb8-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="29bb8-108">สำหรับข้อมูลเพิ่มเติม ให้ดู [รวม Dynamics 365 Field Service และ Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration)</span><span class="sxs-lookup"><span data-stu-id="29bb8-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="29bb8-109">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="29bb8-109">Templates</span></span>

<span data-ttu-id="29bb8-110">สินทรัพย์ภายในองค์กรประกอบด้วยชุดของแผนผังเอนทิตีหลักที่ทำงานร่วมกันในระหว่างการโต้ตอบข้อมูล ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="29bb8-110">In-house-assets include a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="29bb8-111">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="29bb8-111">Finance and Operations apps</span></span> | <span data-ttu-id="29bb8-112">แอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="29bb8-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="29bb8-113">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="29bb8-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="29bb8-114">แบบจำลองวงจรการใช้งานของสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="29bb8-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="29bb8-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="29bb8-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="29bb8-116">สถานะของวงจรการใช้ของสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="29bb8-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="29bb8-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="29bb8-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="29bb8-118">สินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="29bb8-118">Asset management assets</span></span> | <span data-ttu-id="29bb8-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="29bb8-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="29bb8-120">ชนิดสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="29bb8-120">Asset management asset types</span></span> | <span data-ttu-id="29bb8-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="29bb8-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="29bb8-122">แบบจำลองวงจรการใช้งานของตำแหน่งที่ทำงานในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="29bb8-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="29bb8-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="29bb8-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="29bb8-124">สถานะของวงจรการใช้ของตำแหน่งที่ทำงานในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="29bb8-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="29bb8-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="29bb8-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="29bb8-126">ตำแหน่งที่ทำงานในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="29bb8-126">Asset management functional locations</span></span> | <span data-ttu-id="29bb8-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="29bb8-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="29bb8-128">ชนิดของตำแหน่งที่ทำงานในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="29bb8-128">Asset management functional location types</span></span> | <span data-ttu-id="29bb8-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="29bb8-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="29bb8-130">ผู้ผลิตของการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="29bb8-130">Asset management manufacturers</span></span> | <span data-ttu-id="29bb8-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="29bb8-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="29bb8-132">แบบจำลองการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="29bb8-132">Asset management models</span></span> | <span data-ttu-id="29bb8-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="29bb8-133">msdyn\_models</span></span> | |
| <span data-ttu-id="29bb8-134">การรับประกันของการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="29bb8-134">Asset management warranty</span></span> | <span data-ttu-id="29bb8-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="29bb8-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]
