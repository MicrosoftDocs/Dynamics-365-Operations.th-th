---
title: ลำดับชั้นขององค์กรใน Dataverse
description: ในหัวข้อนี้อธิบายการรวมข้อมูลองค์กรระหว่างแอป Finance and Operations กับ Dataverse
author: RamaKrishnamoorthy
ms.date: 07/15/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8b147c27b9309b1b3597f1194c415fbb2e2b7ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750823"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="92ca1-103">ลำดับชั้นขององค์กรใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="92ca1-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="92ca1-104">เนื่องจาก Dynamics 365 Finance เป็นระบบทางการเงิน *องค์กร* เป็นแนวคิดหลัก และการตั้งค่าระบบจะเริ่มต้นด้วยการตั้งค่าคอนฟิกของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="92ca1-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="92ca1-105">สามารถติดตามการเงินของธุรกิจได้ที่ระดับองค์กรและที่ระดับใดก็ได้ในลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="92ca1-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="92ca1-106">แม้ว่า Dataverse จะไม่มีแนวคิดของลำดับชั้นขององค์กร แต่ก็มีแนวคิดคร่าวๆ สองสามรายการ เช่น รายได้จากการขายรวม</span><span class="sxs-lookup"><span data-stu-id="92ca1-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="92ca1-107">ในฐานะที่เป็นส่วนหนึ่งของการรวม Dataverse โครงสร้างข้อมูลลำดับชั้นขององค์กรจะถูกเพิ่มไปยัง Dataverse</span><span class="sxs-lookup"><span data-stu-id="92ca1-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="92ca1-108">โฟลว์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92ca1-108">Data flow</span></span>

<span data-ttu-id="92ca1-109">ระบบแวดล้อมทางธุรกิจที่ประกอบด้วยแอป Finance and Operations และ Dataverse จะยังคงมีลำดับชั้นขององค์กรต่อไป</span><span class="sxs-lookup"><span data-stu-id="92ca1-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="92ca1-110">ลำดับชั้นขององค์กรนี้สร้างขึ้นบนแอป Finance and Operations แต่เปิดเผยใน Dataverse เพื่อวัตถุประสงค์ในการให้ข้อมูลและการขยาย</span><span class="sxs-lookup"><span data-stu-id="92ca1-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="92ca1-111">ภาพประกอบต่อไปนี้แสดงข้อมูลลำดับชั้นขององค์กรที่เปิดเผยใน Dataverse เป็นโฟลว์ข้อมูลทางเดียวจากแอป Finance and Operations ไปยัง Dataverse</span><span class="sxs-lookup"><span data-stu-id="92ca1-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![รูปภาพของสถาปัตยกรรม](media/dual-write-data-flow.png)

<span data-ttu-id="92ca1-113">แผนผังตารางลำดับชั้นขององค์กรพร้อมใช้งานสำหรับการทำข้อมูลทางเดียวให้ตรงกันจากแอป Finance and Operations ไปยัง Dataverse</span><span class="sxs-lookup"><span data-stu-id="92ca1-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="92ca1-114">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="92ca1-114">Templates</span></span>

<span data-ttu-id="92ca1-115">ข้อมูลผลิตภัณฑ์ ประกอบด้วยข้อมูลทั้งหมดที่เกี่ยวข้องกับผลิตภัณฑ์ และคำนิยามของผลิตภัณฑ์ เช่น มิติของผลิตภัณฑ์ หรือการติดตาม และมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="92ca1-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="92ca1-116">ดังที่ตารางต่อไปนี้แสดง ชุดข้อมูลของแผนผังตารางถูกสร้างเพื่อซิงค์ผลิตภัณฑ์และข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="92ca1-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="92ca1-117">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="92ca1-117">Finance and Operations apps</span></span> | <span data-ttu-id="92ca1-118">แอปพลิเคชันอื่น ๆ ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="92ca1-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="92ca1-119">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="92ca1-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="92ca1-120">วัตถุประสงค์ลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="92ca1-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="92ca1-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="92ca1-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="92ca1-122">แม่แบบนี้มีการซิงโครไนส์แบบทางเดียวสำหรับตารางวัตถุประสงค์ของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="92ca1-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="92ca1-123">ชนิดลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="92ca1-123">Organization hierarchy type</span></span> | <span data-ttu-id="92ca1-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="92ca1-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="92ca1-125">แม่แบบนี้มีการซิงโครไนส์แบบทางเดียวสำหรับตารางชนิดของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="92ca1-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="92ca1-126">ลำดับชั้นขององค์กร - เผยแพร่</span><span class="sxs-lookup"><span data-stu-id="92ca1-126">Organization hierarchy - published</span></span> | <span data-ttu-id="92ca1-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="92ca1-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="92ca1-128">แม่แบบนี้มีการซิงโครไนส์แบบทางเดียวสำหรับตารางที่เผยแพร่ของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="92ca1-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="92ca1-129">หน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="92ca1-129">Operating unit</span></span> | <span data-ttu-id="92ca1-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="92ca1-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="92ca1-131">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="92ca1-131">Legal entities</span></span> | <span data-ttu-id="92ca1-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="92ca1-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="92ca1-133">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="92ca1-133">Legal entities</span></span> | <span data-ttu-id="92ca1-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="92ca1-134">cdm_companies</span></span> | <span data-ttu-id="92ca1-135">มีการซิงโครไนส์ข้อมูลของนิติบุคคล (บริษัท) สองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="92ca1-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="92ca1-136">องค์กรภายใน</span><span class="sxs-lookup"><span data-stu-id="92ca1-136">Internal Organization</span></span>

<span data-ttu-id="92ca1-137">ข้อมูลองค์กรภายในใน Dataverse มาจากตารางสองรายการ **หน่วยปฏิบัติงาน** และ **นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="92ca1-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]