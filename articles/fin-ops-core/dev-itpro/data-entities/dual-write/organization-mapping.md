---
title: ลำดับชั้นขององค์กรใน Common Data Service
description: ในหัวข้อนี้อธิบายการรวมข้อมูลองค์กรระหว่างแอป Finance and Operations กับ Common Data Service
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fbf7cc33d12fb54d2ff02acc46ba2e284b2a2b3f
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020038"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="7df86-103">ลำดับชั้นขององค์กรใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7df86-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="7df86-104">เนื่องจาก Dynamics 365 Finance เป็นระบบทางการเงิน *องค์กร* เป็นแนวคิดหลัก และการตั้งค่าระบบจะเริ่มต้นด้วยการตั้งค่าคอนฟิกของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="7df86-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="7df86-105">สามารถติดตามการเงินของธุรกิจได้ที่ระดับองค์กรและที่ระดับใดก็ได้ในลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="7df86-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="7df86-106">แม้ว่า Common Data Service จะไม่มีแนวคิดของลำดับชั้นขององค์กร แต่ก็มีแนวคิดคร่าวๆ สองสามรายการ เช่น รายได้จากการขายรวม</span><span class="sxs-lookup"><span data-stu-id="7df86-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="7df86-107">ในฐานะที่เป็นส่วนหนึ่งของการรวม Common Data Service โครงสร้างข้อมูลลำดับชั้นขององค์กรจะถูกเพิ่มไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7df86-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="7df86-108">โฟลว์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7df86-108">Data flow</span></span>

<span data-ttu-id="7df86-109">ระบบแวดล้อมทางธุรกิจที่ประกอบด้วยแอป Finance and Operations และ Common Data Service จะยังคงมีลำดับชั้นขององค์กรต่อไป</span><span class="sxs-lookup"><span data-stu-id="7df86-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="7df86-110">ลำดับชั้นขององค์กรนี้สร้างขึ้นบนแอป Finance and Operations แต่เปิดเผยใน Common Data Service เพื่อวัตถุประสงค์ในการให้ข้อมูลและการขยาย</span><span class="sxs-lookup"><span data-stu-id="7df86-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="7df86-111">ภาพประกอบต่อไปนี้แสดงข้อมูลลำดับชั้นขององค์กรที่เปิดเผยใน Common Data Service เป็นโฟลว์ข้อมูลทางเดียวจากแอป Finance and Operations ไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7df86-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![รูปภาพของสถาปัตยกรรม](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="7df86-113">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="7df86-113">Templates</span></span>

<span data-ttu-id="7df86-114">แผนผังเอนทิตีลำดับชั้นขององค์กรพร้อมใช้งานสำหรับการทำข้อมูลทางเดียวให้ตรงกันจากแอป Finance and Operations ไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7df86-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="7df86-115">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="7df86-115">Templates</span></span>

<span data-ttu-id="7df86-116">ข้อมูลผลิตภัณฑ์ ประกอบด้วยข้อมูลทั้งหมดที่เกี่ยวข้องกับผลิตภัณฑ์ และคำนิยามของผลิตภัณฑ์ เช่น มิติของผลิตภัณฑ์ หรือการติดตาม และมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="7df86-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="7df86-117">ดังที่ตารางต่อไปนี้แสดง ชุดข้อมูลของแผนผังเอนทิตี้ถูกสร้างเพื่อซิงค์ผลิตภัณฑ์และข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="7df86-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="7df86-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7df86-118">Finance and Operations</span></span> | <span data-ttu-id="7df86-119">แอปพลิเคชันอื่น ๆ ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7df86-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="7df86-120">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7df86-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="7df86-121">วัตถุประสงค์ลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="7df86-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="7df86-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="7df86-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="7df86-123">เท็มเพลตนี้มีการซิงโครไนส์แบบทางเดียวสำหรับเอนทิตีวัตถุประสงค์ของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="7df86-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="7df86-124">ชนิดลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="7df86-124">Organization hierarchy type</span></span> | <span data-ttu-id="7df86-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="7df86-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="7df86-126">เท็มเพลตนี้มีการซิงโครไนส์แบบทางเดียวสำหรับเอนทิตีชนิดของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="7df86-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="7df86-127">ลำดับชั้นขององค์กรที่เผยแพร่</span><span class="sxs-lookup"><span data-stu-id="7df86-127">Organization hierarchy - published</span></span> | <span data-ttu-id="7df86-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="7df86-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="7df86-129">เท็มเพลตนี้มีการซิงโครไนส์แบบทางเดียวสำหรับเอนทิตีที่เผยแพร่ของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="7df86-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="7df86-130">หน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="7df86-130">Operating unit</span></span> | <span data-ttu-id="7df86-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="7df86-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="7df86-132">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="7df86-132">Legal entities</span></span> | <span data-ttu-id="7df86-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="7df86-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="7df86-134">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="7df86-134">Legal entities</span></span> | <span data-ttu-id="7df86-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="7df86-135">cdm_companies</span></span> | <span data-ttu-id="7df86-136">มีการซิงโครไนส์ข้อมูลของนิติบุคคล (บริษัท) สองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="7df86-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="7df86-137">องค์กรภายใน</span><span class="sxs-lookup"><span data-stu-id="7df86-137">Internal Organization</span></span>

<span data-ttu-id="7df86-138">ข้อมูลองค์กรภายในใน Common Data Service มาจากเอนทิตีสองรายการ **หน่วยปฏิบัติงาน** และ **นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="7df86-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

