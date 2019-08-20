---
title: ลำดับชั้นขององค์กรใน Common Data Service
description: หัวข้อนี้อธิบายการรวมของข้อมูลเชิงองค์กรระหว่าง Finance and Operations และ Common Data Service
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
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789253"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="a3baf-103">ลำดับชั้นขององค์กรใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a3baf-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="a3baf-104">เนื่องจาก Microsoft Dynamics 365 for Finance and Operations เป็นระบบทางการเงิน *องค์กร* เป็นแนวคิดหลัก และการตั้งค่าระบบจะเริ่มต้นด้วยการตั้งค่าคอนฟิกของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="a3baf-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="a3baf-105">สามารถติดตามการเงินและการดำเนินงานของธุรกิจได้ที่ระดับองค์กรและที่ระดับใดก็ได้ในลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="a3baf-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="a3baf-106">แม้ว่า Common Data Service จะไม่มีแนวคิดของลำดับชั้นขององค์กร แต่ก็มีแนวคิดคร่าวๆ สองสามรายการ เช่น รายได้จากการขายรวม</span><span class="sxs-lookup"><span data-stu-id="a3baf-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="a3baf-107">ในฐานะที่เป็นส่วนหนึ่งของการรวม Common Data Service โครงสร้างข้อมูลลำดับชั้นขององค์กรจะถูกเพิ่มไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a3baf-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="a3baf-108">โฟลว์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a3baf-108">Data flow</span></span>

<span data-ttu-id="a3baf-109">ระบบนิเวศทางธุรกิจที่ประกอบด้วย Finance and Operations และ Common Data Service จะยังคงมีลำดับชั้นขององค์กรอยู่</span><span class="sxs-lookup"><span data-stu-id="a3baf-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="a3baf-110">ลำดับชั้นขององค์กรนี้ถูกสร้างขึ้นใน Finance and Operations แต่จะถูกเปิดเผยใน Common Data Service เพื่อวัตถุประสงค์ในการให้ข้อมูลและความสามารถในการเพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="a3baf-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="a3baf-111">ภาพประกอบต่อไปนี้แสดงข้อมูลลำดับชั้นขององค์กรที่ถูกเปิดเผยใน Common Data Service เป็นโฟลว์ข้อมูลทางเดียวจาก Finance and Operations ไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a3baf-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![รูปภาพของสถาปัตยกรรม](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="a3baf-113">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="a3baf-113">Templates</span></span>

<span data-ttu-id="a3baf-114">แผนผังเอนทิตีลำดับชั้นขององค์กรจะพร้อมใช้งานสำหรับการซิงโครไนส์ข้อมูลแบบทางเดียวจาก Finance and operations ไปยัง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a3baf-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="a3baf-115">วัตถุประสงค์ลำดับชั้นขององค์กรภายใน</span><span class="sxs-lookup"><span data-stu-id="a3baf-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="a3baf-116">เท็มเพลตนี้ให้การซิงโครไนส์แบบทางเดียวของเอนทิตีวัตถุประสงค์ลำดับชั้นขององค์กรจาก Finance and Operations ไปยัง Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="a3baf-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="a3baf-117">ฟิลด์ต้นทาง</span><span class="sxs-lookup"><span data-stu-id="a3baf-117">Source field</span></span> | <span data-ttu-id="a3baf-118">ชนิดของการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a3baf-118">Map type</span></span> | <span data-ttu-id="a3baf-119">ฟิลด์ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="a3baf-119">Destination field</span></span>
---|---|---
<span data-ttu-id="a3baf-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="a3baf-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="a3baf-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="a3baf-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="a3baf-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="a3baf-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="a3baf-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="a3baf-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="a3baf-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="a3baf-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="a3baf-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="a3baf-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="a3baf-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="a3baf-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="a3baf-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="a3baf-127">msdyn\_immutable</span></span>
<span data-ttu-id="a3baf-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="a3baf-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="a3baf-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="a3baf-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="a3baf-130">ชนิดลำดับชั้นขององค์กรภายใน</span><span class="sxs-lookup"><span data-stu-id="a3baf-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="a3baf-131">เท็มเพลตนี้ให้การซิงโครไนส์แบบทางเดียวของเอนทิตีชนิดลำดับชั้นขององค์กรจาก Finance and Operations ไปยัง Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="a3baf-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="a3baf-132">ฟิลด์ต้นทาง</span><span class="sxs-lookup"><span data-stu-id="a3baf-132">Source field</span></span> | <span data-ttu-id="a3baf-133">ชนิดของการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a3baf-133">Map type</span></span> | <span data-ttu-id="a3baf-134">ฟิลด์ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="a3baf-134">Destination field</span></span>
---|---|---
<span data-ttu-id="a3baf-135">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="a3baf-135">NAME</span></span> | \> | <span data-ttu-id="a3baf-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="a3baf-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="a3baf-137">ลำดับชั้นขององค์กรภายใน</span><span class="sxs-lookup"><span data-stu-id="a3baf-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="a3baf-138">เท็มเพลตนี้ให้การซิงโครไนส์แบบทางเดียวของเอนทิตีที่เผยแพร่ของลำดับชั้นขององค์กรจาก Finance and Operations ไปยัง Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="a3baf-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="a3baf-139">ฟิลด์ต้นทาง</span><span class="sxs-lookup"><span data-stu-id="a3baf-139">Source field</span></span> | <span data-ttu-id="a3baf-140">ชนิดของการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a3baf-140">Map type</span></span> | <span data-ttu-id="a3baf-141">ฟิลด์ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="a3baf-141">Destination field</span></span>
---|---|---
<span data-ttu-id="a3baf-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="a3baf-142">VALIDTO</span></span> | \> | <span data-ttu-id="a3baf-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="a3baf-143">msdyn\_validto</span></span>
<span data-ttu-id="a3baf-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="a3baf-144">VALIDFROM</span></span> | \> | <span data-ttu-id="a3baf-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="a3baf-145">msdyn\_validfrom</span></span>
<span data-ttu-id="a3baf-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="a3baf-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="a3baf-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="a3baf-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="a3baf-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="a3baf-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="a3baf-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="a3baf-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="a3baf-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="a3baf-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="a3baf-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="a3baf-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="a3baf-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="a3baf-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="a3baf-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="a3baf-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="a3baf-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="a3baf-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="a3baf-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="a3baf-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="a3baf-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="a3baf-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="a3baf-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="a3baf-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="a3baf-158">องค์กรภายใน</span><span class="sxs-lookup"><span data-stu-id="a3baf-158">Internal Organization</span></span>

<span data-ttu-id="a3baf-159">ข้อมูลองค์กรภายในใน Common Data Service มาจากเอนทิตี Finance and Operations สองรายการ **หน่วยปฏิบัติงาน** และ **นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="a3baf-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="a3baf-160">หน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="a3baf-160">Operating unit</span></span>

<span data-ttu-id="a3baf-161">ฟิลด์ต้นทาง</span><span class="sxs-lookup"><span data-stu-id="a3baf-161">Source field</span></span> | <span data-ttu-id="a3baf-162">ชนิดของการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a3baf-162">Map type</span></span> | <span data-ttu-id="a3baf-163">ฟิลด์ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="a3baf-163">Destination field</span></span>
---|---|---
<span data-ttu-id="a3baf-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="a3baf-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="a3baf-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="a3baf-165">msdyn\_languageid</span></span>
<span data-ttu-id="a3baf-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="a3baf-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="a3baf-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="a3baf-167">msdyn\_namealias</span></span>
<span data-ttu-id="a3baf-168">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="a3baf-168">NAME</span></span> | \> | <span data-ttu-id="a3baf-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="a3baf-169">msdyn\_name</span></span>
<span data-ttu-id="a3baf-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="a3baf-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="a3baf-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="a3baf-171">msdyn\_partynumber</span></span>
<span data-ttu-id="a3baf-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="a3baf-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="a3baf-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="a3baf-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="a3baf-174">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="a3baf-174">Legal entity</span></span>

<span data-ttu-id="a3baf-175">ฟิลด์ต้นทาง</span><span class="sxs-lookup"><span data-stu-id="a3baf-175">Source field</span></span> | <span data-ttu-id="a3baf-176">ชนิดของการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a3baf-176">Map type</span></span> | <span data-ttu-id="a3baf-177">ฟิลด์ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="a3baf-177">Destination field</span></span>
---|---|---
<span data-ttu-id="a3baf-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="a3baf-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="a3baf-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="a3baf-179">msdyn\_namealias</span></span>
<span data-ttu-id="a3baf-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="a3baf-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="a3baf-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="a3baf-181">msdyn\_languageid</span></span>
<span data-ttu-id="a3baf-182">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="a3baf-182">NAME</span></span> | \> | <span data-ttu-id="a3baf-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="a3baf-183">msdyn\_name</span></span>
<span data-ttu-id="a3baf-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="a3baf-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="a3baf-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="a3baf-185">msdyn\_partynumber</span></span>
<span data-ttu-id="a3baf-186">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="a3baf-186">none</span></span> | \>\> | <span data-ttu-id="a3baf-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="a3baf-187">msdyn\_type</span></span>
<span data-ttu-id="a3baf-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="a3baf-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="a3baf-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="a3baf-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="a3baf-190">บริษัท</span><span class="sxs-lookup"><span data-stu-id="a3baf-190">Company</span></span>

<span data-ttu-id="a3baf-191">นำเสนอข้อมูลการซิงโครไนส์แบบสองทิศทางของนิติบุคคล (บริษัท) ระหว่าง Finance and Operations และ Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="a3baf-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="a3baf-192">ฟิลด์ต้นทาง</span><span class="sxs-lookup"><span data-stu-id="a3baf-192">Source field</span></span> | <span data-ttu-id="a3baf-193">ชนิดของการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a3baf-193">Map type</span></span> | <span data-ttu-id="a3baf-194">ฟิลด์ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="a3baf-194">Destination field</span></span>
---|---|---
<span data-ttu-id="a3baf-195">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="a3baf-195">NAME</span></span> | = | <span data-ttu-id="a3baf-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="a3baf-196">cdm\_name</span></span>
<span data-ttu-id="a3baf-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="a3baf-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="a3baf-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="a3baf-198">cdm\_companycode</span></span>
