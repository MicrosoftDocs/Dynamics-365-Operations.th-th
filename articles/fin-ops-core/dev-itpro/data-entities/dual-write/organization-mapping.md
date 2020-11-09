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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f502519ba419cb8fa322eb1d22f06d2b805f5f05
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000745"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="e96b3-103">ลำดับชั้นขององค์กรใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e96b3-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e96b3-104">เนื่องจาก Dynamics 365 Finance เป็นระบบทางการเงิน *องค์กร* เป็นแนวคิดหลัก และการตั้งค่าระบบจะเริ่มต้นด้วยการตั้งค่าคอนฟิกของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="e96b3-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="e96b3-105">สามารถติดตามการเงินของธุรกิจได้ที่ระดับองค์กรและที่ระดับใดก็ได้ในลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="e96b3-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="e96b3-106">แม้ว่า Common Data Service จะไม่มีแนวคิดของลำดับชั้นขององค์กร แต่ก็มีแนวคิดคร่าวๆ สองสามรายการ เช่น รายได้จากการขายรวม</span><span class="sxs-lookup"><span data-stu-id="e96b3-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="e96b3-107">ในฐานะที่เป็นส่วนหนึ่งของการรวม Common Data Service โครงสร้างข้อมูลลำดับชั้นขององค์กรจะถูกเพิ่มไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e96b3-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="e96b3-108">โฟลว์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e96b3-108">Data flow</span></span>

<span data-ttu-id="e96b3-109">ระบบแวดล้อมทางธุรกิจที่ประกอบด้วยแอป Finance and Operations และ Common Data Service จะยังคงมีลำดับชั้นขององค์กรต่อไป</span><span class="sxs-lookup"><span data-stu-id="e96b3-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="e96b3-110">ลำดับชั้นขององค์กรนี้สร้างขึ้นบนแอป Finance and Operations แต่เปิดเผยใน Common Data Service เพื่อวัตถุประสงค์ในการให้ข้อมูลและการขยาย</span><span class="sxs-lookup"><span data-stu-id="e96b3-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="e96b3-111">ภาพประกอบต่อไปนี้แสดงข้อมูลลำดับชั้นขององค์กรที่เปิดเผยใน Common Data Service เป็นโฟลว์ข้อมูลทางเดียวจากแอป Finance and Operations ไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e96b3-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![รูปภาพของสถาปัตยกรรม](media/dual-write-data-flow.png)

<span data-ttu-id="e96b3-113">แผนผังเอนทิตีลำดับชั้นขององค์กรพร้อมใช้งานสำหรับการทำข้อมูลทางเดียวให้ตรงกันจากแอป Finance and Operations ไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e96b3-113">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="e96b3-114">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="e96b3-114">Templates</span></span>

<span data-ttu-id="e96b3-115">ข้อมูลผลิตภัณฑ์ ประกอบด้วยข้อมูลทั้งหมดที่เกี่ยวข้องกับผลิตภัณฑ์ และคำนิยามของผลิตภัณฑ์ เช่น มิติของผลิตภัณฑ์ หรือการติดตาม และมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="e96b3-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="e96b3-116">ดังที่ตารางต่อไปนี้แสดง ชุดข้อมูลของแผนผังเอนทิตี้ถูกสร้างเพื่อซิงค์ผลิตภัณฑ์และข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="e96b3-116">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="e96b3-117">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e96b3-117">Finance and Operations apps</span></span> | <span data-ttu-id="e96b3-118">แอปพลิเคชันอื่น ๆ ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e96b3-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="e96b3-119">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e96b3-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="e96b3-120">วัตถุประสงค์ลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="e96b3-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="e96b3-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="e96b3-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="e96b3-122">เท็มเพลตนี้มีการซิงโครไนส์แบบทางเดียวสำหรับเอนทิตีวัตถุประสงค์ของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="e96b3-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="e96b3-123">ชนิดลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="e96b3-123">Organization hierarchy type</span></span> | <span data-ttu-id="e96b3-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="e96b3-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="e96b3-125">เท็มเพลตนี้มีการซิงโครไนส์แบบทางเดียวสำหรับเอนทิตีชนิดของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="e96b3-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="e96b3-126">ลำดับชั้นขององค์กรที่เผยแพร่</span><span class="sxs-lookup"><span data-stu-id="e96b3-126">Organization hierarchy - published</span></span> | <span data-ttu-id="e96b3-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="e96b3-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="e96b3-128">เท็มเพลตนี้มีการซิงโครไนส์แบบทางเดียวสำหรับเอนทิตีที่เผยแพร่ของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="e96b3-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="e96b3-129">หน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="e96b3-129">Operating unit</span></span> | <span data-ttu-id="e96b3-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="e96b3-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="e96b3-131">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="e96b3-131">Legal entities</span></span> | <span data-ttu-id="e96b3-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="e96b3-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="e96b3-133">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="e96b3-133">Legal entities</span></span> | <span data-ttu-id="e96b3-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="e96b3-134">cdm_companies</span></span> | <span data-ttu-id="e96b3-135">มีการซิงโครไนส์ข้อมูลของนิติบุคคล (บริษัท) สองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="e96b3-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="e96b3-136">องค์กรภายใน</span><span class="sxs-lookup"><span data-stu-id="e96b3-136">Internal Organization</span></span>

<span data-ttu-id="e96b3-137">ข้อมูลองค์กรภายในใน Common Data Service มาจากเอนทิตีสองรายการ **หน่วยปฏิบัติงาน** และ **นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="e96b3-137">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
