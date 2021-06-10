---
title: กําหนดไอคอนและชื่อขั้นตอนสำหรับแอป Warehouse Management บนมือถือ
description: หัวข้อนี้อธิบายวิธีการกําหนดไอคอนและชื่อขั้นตอนให้กับโฟลว์งานใหม่หรือที่กําหนดเองสำหรับแอป Warehouse Management บนมือถือ
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049375"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="36e19-103">กําหนดไอคอนและชื่อขั้นตอนสำหรับแอป Warehouse Management บนมือถือ</span><span class="sxs-lookup"><span data-stu-id="36e19-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36e19-104">หัวข้อนี้อธิบายวิธีการกําหนดไอคอนขั้นตอนและชื่อขั้นตอนให้กับโฟลว์งานใหม่หรือที่กําหนดเองสำหรับแอป Warehouse Management บนมือถือ</span><span class="sxs-lookup"><span data-stu-id="36e19-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="36e19-105">ภาพประกอบต่อไปนี้จะแสดงวิธีที่ไอคอนและชื่อขั้นตอนปรากฏในแอป Warehouse Management บนมือถือ</span><span class="sxs-lookup"><span data-stu-id="36e19-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="36e19-106">![ตัวอย่างของไอคอนขั้นตอนและชื่อขั้นตอนในแอป Warehouse Management บนมือถือ](media/step-icon-example.png "ตัวอย่างของไอคอนขั้นตอนและชื่อขั้นตอนในแอป Warehouse Management บนมือถือ")</span><span class="sxs-lookup"><span data-stu-id="36e19-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="36e19-107">เปิดใช้งานคุณลักษณะการทำงานนี้ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="36e19-107">Turn on this feature in your system</span></span>

<span data-ttu-id="36e19-108">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="36e19-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="36e19-109">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="36e19-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="36e19-110">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="36e19-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="36e19-111">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="36e19-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="36e19-112">**ชื่อคุณลักษณะ:** *การตั้งค่าผู้ใช้ ไอคอน และชื่อขั้นตอน ของแอปคลังสินค้าใหม่*</span><span class="sxs-lookup"><span data-stu-id="36e19-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="36e19-113">รหัส คลาส และไอคอนขั้นตอนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="36e19-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="36e19-114">แต่ละขั้นตอนในโฟลว์งานจะถูกระบุโดยรหัสขั้นตอน และแต่ละรหัสขั้นตอนมีคลาสขั้นตอนที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="36e19-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="36e19-115">ไอคอนขั้นตอนและชื่อจะระบุอยู่ในแต่ละคลาสขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="36e19-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="36e19-116">รหัสขั้นตอนและคลาสขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="36e19-116">Step IDs and step classes</span></span>

<span data-ttu-id="36e19-117">ตารางต่อไปนี้แสดงรายการรหัสขั้นตอนทุกรหัสที่พร้อมใช้งานในปัจจุบัน และคลาสขั้นตอนที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="36e19-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="36e19-118">ชื่อตัวควบคุมของฟิลด์ป้อนข้อมูลหลักถูกใช้เป็นรหัสขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="36e19-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="36e19-119">สำหรับตัวอย่างที่แสดงว่ามีการใช้รหัสขั้นตอนและคลาสเหล่านี้อย่างไร โปรดดูที่การใช้งานของวิธีการ `WHSMobileAppStepInfoBuilder.stepId()` ใน [ตัวอย่าง: กําหนดไอคอนขั้นตอนและชื่อให้กับส่วนโฟลว์ที่กําหนดเอง](#example) ในภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="36e19-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="36e19-120">รหัสขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="36e19-120">Step ID</span></span> | <span data-ttu-id="36e19-121">คลาสขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="36e19-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="36e19-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="36e19-122">BatchDisposition</span></span> | <span data-ttu-id="36e19-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="36e19-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="36e19-124">ผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="36e19-124">Carrier</span></span> | <span data-ttu-id="36e19-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="36e19-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="36e19-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-126">CatchWeight</span></span> | <span data-ttu-id="36e19-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="36e19-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="36e19-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="36e19-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="36e19-130">CatchWeightTag</span></span> | <span data-ttu-id="36e19-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="36e19-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="36e19-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="36e19-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="36e19-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="36e19-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="36e19-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="36e19-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="36e19-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="36e19-136">CheckDigit</span></span> | <span data-ttu-id="36e19-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="36e19-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="36e19-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="36e19-138">ClusterId</span></span> | <span data-ttu-id="36e19-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="36e19-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="36e19-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="36e19-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="36e19-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="36e19-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="36e19-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="36e19-142">ClusterPosition</span></span> | <span data-ttu-id="36e19-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="36e19-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="36e19-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="36e19-144">ConfigId</span></span> | <span data-ttu-id="36e19-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="36e19-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="36e19-146">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="36e19-146">Confirmation</span></span> | <span data-ttu-id="36e19-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="36e19-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="36e19-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="36e19-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="36e19-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="36e19-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="36e19-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="36e19-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="36e19-154">ContainerType</span></span> | <span data-ttu-id="36e19-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="36e19-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="36e19-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="36e19-156">CountingReasonCode</span></span> | <span data-ttu-id="36e19-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="36e19-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="36e19-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="36e19-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="36e19-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="36e19-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="36e19-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="36e19-160">CycleCountQty1</span></span> | <span data-ttu-id="36e19-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="36e19-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="36e19-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="36e19-162">CycleCountQty2</span></span> | <span data-ttu-id="36e19-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="36e19-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="36e19-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="36e19-164">CycleCountQty3</span></span> | <span data-ttu-id="36e19-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="36e19-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="36e19-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="36e19-166">CycleCountQty4</span></span> | <span data-ttu-id="36e19-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="36e19-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="36e19-168">Disposition</span><span class="sxs-lookup"><span data-stu-id="36e19-168">Disposition</span></span> | <span data-ttu-id="36e19-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="36e19-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="36e19-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="36e19-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="36e19-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="36e19-172">DriverCheckInId</span></span> | <span data-ttu-id="36e19-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="36e19-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="36e19-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="36e19-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="36e19-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="36e19-176">DriverCheckOutId</span></span> | <span data-ttu-id="36e19-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="36e19-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="36e19-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="36e19-178">ExpDate</span></span> | <span data-ttu-id="36e19-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="36e19-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="36e19-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="36e19-180">FromBatchDisposition</span></span> | <span data-ttu-id="36e19-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="36e19-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="36e19-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="36e19-182">FromInventoryStatus</span></span> | <span data-ttu-id="36e19-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="36e19-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="36e19-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="36e19-184">FullQty</span></span> | <span data-ttu-id="36e19-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="36e19-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="36e19-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="36e19-186">InboundPut</span></span> | <span data-ttu-id="36e19-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="36e19-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="36e19-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="36e19-188">InventBatchId</span></span> | <span data-ttu-id="36e19-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="36e19-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="36e19-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="36e19-190">InventColorId</span></span> | <span data-ttu-id="36e19-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="36e19-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="36e19-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="36e19-192">InventLocation</span></span> | <span data-ttu-id="36e19-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="36e19-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="36e19-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="36e19-194">InventLocationId</span></span> | <span data-ttu-id="36e19-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="36e19-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="36e19-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="36e19-196">InventSerialId</span></span> | <span data-ttu-id="36e19-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="36e19-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="36e19-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="36e19-198">InventSizeId</span></span> | <span data-ttu-id="36e19-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="36e19-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="36e19-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="36e19-200">InventStatusId</span></span> | <span data-ttu-id="36e19-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="36e19-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="36e19-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="36e19-202">InventStyleId</span></span> | <span data-ttu-id="36e19-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="36e19-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="36e19-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="36e19-204">InventVersionId</span></span> | <span data-ttu-id="36e19-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="36e19-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="36e19-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="36e19-206">ItemId</span></span> | <span data-ttu-id="36e19-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="36e19-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="36e19-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="36e19-208">ITMContainerID</span></span> | <span data-ttu-id="36e19-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="36e19-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="36e19-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="36e19-210">ITMShipmentID</span></span> | <span data-ttu-id="36e19-211">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="36e19-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="36e19-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="36e19-212">KanbanCardId</span></span> | <span data-ttu-id="36e19-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="36e19-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="36e19-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="36e19-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="36e19-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="36e19-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="36e19-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="36e19-216">KanbanOrCardId</span></span> | <span data-ttu-id="36e19-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="36e19-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="36e19-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-218">LicensePlateId</span></span> | <span data-ttu-id="36e19-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="36e19-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="36e19-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="36e19-220">LoadId</span></span> | <span data-ttu-id="36e19-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="36e19-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="36e19-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="36e19-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="36e19-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="36e19-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="36e19-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="36e19-224">LocOrLP</span></span> | <span data-ttu-id="36e19-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="36e19-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="36e19-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="36e19-226">LocOrLP_From</span></span> | <span data-ttu-id="36e19-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="36e19-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="36e19-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="36e19-228">LocOrLP_To</span></span> | <span data-ttu-id="36e19-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="36e19-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="36e19-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="36e19-230">LocOrLPCheck</span></span> | <span data-ttu-id="36e19-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="36e19-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="36e19-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="36e19-232">LocVerification</span></span> | <span data-ttu-id="36e19-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="36e19-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="36e19-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="36e19-234">LPAdjustIn</span></span> | <span data-ttu-id="36e19-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="36e19-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="36e19-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="36e19-236">LPBreakChildLP</span></span> | <span data-ttu-id="36e19-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="36e19-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="36e19-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="36e19-238">LPBreakParentLP</span></span> | <span data-ttu-id="36e19-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="36e19-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="36e19-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="36e19-240">LPBuildChildLP</span></span> | <span data-ttu-id="36e19-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="36e19-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="36e19-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="36e19-242">LPBuildParentLP</span></span> | <span data-ttu-id="36e19-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="36e19-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="36e19-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="36e19-244">LPVerification</span></span> | <span data-ttu-id="36e19-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="36e19-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="36e19-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="36e19-246">MergeContainerId</span></span> | <span data-ttu-id="36e19-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="36e19-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="36e19-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="36e19-248">MixedLPLineNum</span></span> | <span data-ttu-id="36e19-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="36e19-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="36e19-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="36e19-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="36e19-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="36e19-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="36e19-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="36e19-252">MovementConfirmCancel</span></span> | <span data-ttu-id="36e19-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="36e19-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="36e19-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-254">NewCaptureWeight</span></span> | <span data-ttu-id="36e19-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="36e19-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="36e19-256">NewQty</span></span> | <span data-ttu-id="36e19-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="36e19-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="36e19-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="36e19-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="36e19-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="36e19-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="36e19-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="36e19-260">OutboundPut</span></span> | <span data-ttu-id="36e19-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="36e19-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="36e19-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-262">OutboundWeight</span></span> | <span data-ttu-id="36e19-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="36e19-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="36e19-264">OverridePutNewLocation</span></span> | <span data-ttu-id="36e19-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="36e19-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="36e19-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="36e19-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="36e19-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="36e19-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="36e19-268">POLineNum</span></span> | <span data-ttu-id="36e19-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="36e19-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="36e19-270">หมายเลขใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="36e19-270">PONum</span></span> | <span data-ttu-id="36e19-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="36e19-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="36e19-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="36e19-272">PositionFull</span></span> | <span data-ttu-id="36e19-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="36e19-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="36e19-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="36e19-274">PositionFullQty</span></span> | <span data-ttu-id="36e19-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="36e19-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="36e19-276">ความแข็งแรง</span><span class="sxs-lookup"><span data-stu-id="36e19-276">Potency</span></span> | <span data-ttu-id="36e19-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="36e19-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="36e19-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="36e19-278">PrinterName</span></span> | <span data-ttu-id="36e19-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="36e19-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="36e19-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="36e19-280">ProdId</span></span> | <span data-ttu-id="36e19-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="36e19-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="36e19-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="36e19-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="36e19-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-284">ProductConfirmation</span></span> | <span data-ttu-id="36e19-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="36e19-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="36e19-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="36e19-288">ส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="36e19-288">Put</span></span> | <span data-ttu-id="36e19-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="36e19-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="36e19-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="36e19-290">PutawayClusterId</span></span> | <span data-ttu-id="36e19-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="36e19-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="36e19-292">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="36e19-292">Qty</span></span> | <span data-ttu-id="36e19-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="36e19-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="36e19-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="36e19-294">QtyAdjust</span></span> | <span data-ttu-id="36e19-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="36e19-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="36e19-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="36e19-296">QtyShort</span></span> | <span data-ttu-id="36e19-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="36e19-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="36e19-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="36e19-298">QtyToConsume</span></span> | <span data-ttu-id="36e19-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="36e19-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="36e19-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="36e19-300">QtyToPick</span></span> | <span data-ttu-id="36e19-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="36e19-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="36e19-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="36e19-302">QtyToPut</span></span> | <span data-ttu-id="36e19-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="36e19-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="36e19-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="36e19-304">QtyToScrap</span></span> | <span data-ttu-id="36e19-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="36e19-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="36e19-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="36e19-306">QtyVerification</span></span> | <span data-ttu-id="36e19-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="36e19-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="36e19-308">QtyWithscanningLimit</span><span class="sxs-lookup"><span data-stu-id="36e19-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="36e19-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="36e19-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="36e19-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="36e19-310">ReasonString</span></span> | <span data-ttu-id="36e19-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="36e19-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="36e19-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="36e19-312">RecvLocationId</span></span> | <span data-ttu-id="36e19-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="36e19-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="36e19-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="36e19-314">RemoveContainerId</span></span> | <span data-ttu-id="36e19-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="36e19-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="36e19-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="36e19-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="36e19-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="36e19-318">RMANum</span></span> | <span data-ttu-id="36e19-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="36e19-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="36e19-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="36e19-320">ShortPickReason</span></span> | <span data-ttu-id="36e19-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="36e19-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="36e19-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="36e19-322">SortConOrLP</span></span> | <span data-ttu-id="36e19-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="36e19-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="36e19-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-324">SortLicensePlateId</span></span> | <span data-ttu-id="36e19-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="36e19-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="36e19-326">SortPositionId</span></span> | <span data-ttu-id="36e19-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="36e19-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="36e19-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="36e19-328">SortVerification</span></span> | <span data-ttu-id="36e19-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="36e19-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="36e19-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="36e19-330">StartLocationId</span></span> | <span data-ttu-id="36e19-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="36e19-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="36e19-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="36e19-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="36e19-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-334">TargetLicensePlateId</span></span> | <span data-ttu-id="36e19-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="36e19-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="36e19-336">TOLineNum</span></span> | <span data-ttu-id="36e19-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="36e19-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="36e19-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="36e19-338">ToLocation</span></span> | <span data-ttu-id="36e19-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="36e19-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="36e19-340">TONum</span><span class="sxs-lookup"><span data-stu-id="36e19-340">TONum</span></span> | <span data-ttu-id="36e19-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="36e19-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="36e19-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="36e19-342">ToWarehouse</span></span> | <span data-ttu-id="36e19-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="36e19-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="36e19-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="36e19-344">TransportLoadId</span></span> | <span data-ttu-id="36e19-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="36e19-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="36e19-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="36e19-346">WaveLabelId</span></span> | <span data-ttu-id="36e19-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="36e19-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="36e19-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="36e19-348">WaveLblQty</span></span> | <span data-ttu-id="36e19-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="36e19-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="36e19-350">น้ำหนัก</span><span class="sxs-lookup"><span data-stu-id="36e19-350">Weight</span></span> | <span data-ttu-id="36e19-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="36e19-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="36e19-352">WeightToConsume</span></span> | <span data-ttu-id="36e19-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="36e19-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="36e19-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="36e19-354">WHSAdjustmentType</span></span> | <span data-ttu-id="36e19-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="36e19-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="36e19-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="36e19-356">WHSReceivingException</span></span> | <span data-ttu-id="36e19-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="36e19-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="36e19-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="36e19-358">WHSWorkException</span></span> | <span data-ttu-id="36e19-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="36e19-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="36e19-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="36e19-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="36e19-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="36e19-362">WMSLocationId</span></span> | <span data-ttu-id="36e19-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="36e19-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="36e19-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="36e19-364">WorkId</span></span> | <span data-ttu-id="36e19-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="36e19-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="36e19-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="36e19-366">WorkIdToCancel</span></span> | <span data-ttu-id="36e19-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="36e19-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="36e19-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="36e19-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="36e19-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="36e19-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="36e19-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="36e19-370">WorkPoolId</span></span> | <span data-ttu-id="36e19-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="36e19-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="36e19-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="36e19-372">ZoneId</span></span> | <span data-ttu-id="36e19-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="36e19-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="36e19-374">ไอคอนขั้นตอนที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="36e19-374">Available step icons</span></span>

<span data-ttu-id="36e19-375">ระบบมีคอลเลกชันไอคอนขั้นตอนมาตรฐานที่คุณสามารถใช้กับขั้นตอนที่กำหนดเองของคุณ</span><span class="sxs-lookup"><span data-stu-id="36e19-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="36e19-376">ขณะนี้คุณไม่สามารถอัปโหลดไอคอนขั้นตอนที่กำหนดเองได้</span><span class="sxs-lookup"><span data-stu-id="36e19-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="36e19-377">ดังนั้นคุณจึงต้องเลือกหนึ่งในไอคอนขั้นตอนมาตรฐานเสมอ</span><span class="sxs-lookup"><span data-stu-id="36e19-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="36e19-378">ตารางต่อไปนี้จะแสดงไอคอนขั้นตอนมาตรฐานทุกไอคอนที่พร้อมใช้งานในปัจจุบันและชื่อขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="36e19-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="เกี่ยวกับไอคอนขั้นตอน"><br><span data-ttu-id="36e19-380">เกี่ยวกับ</span><span class="sxs-lookup"><span data-stu-id="36e19-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="เพิ่มไอคอนป้ายทะเบียนหรือขั้นตอนสินค้า"><br><span data-ttu-id="36e19-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="36e19-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="ไอคอนขั้นตอนการโอนการครอบครองชุดงาน"><br><span data-ttu-id="36e19-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="36e19-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="ไอคอนขั้นตอนของผู้ขนส่ง"><br><span data-ttu-id="36e19-386">ผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="36e19-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="ไอคอนขั้นตอนแท็กน้ำหนักจริง"><br><span data-ttu-id="36e19-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="36e19-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="ไอคอนขั้นตอนน้ำหนักของแท็กน้ำหนักจริง"><br><span data-ttu-id="36e19-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="ไอคอนขั้นตอนตัวเลขการตรวจสอบ"><br><span data-ttu-id="36e19-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="36e19-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="ไอคอนขั้นตอนรหัสเช็คอินหรือเช็คเอาท์"><br><span data-ttu-id="36e19-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="36e19-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="ไอคอนขั้นตอนป้ายทะเบียนรอง"><br><span data-ttu-id="36e19-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="36e19-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="ไอคอนขั้นตอนรหัสคลัสเตอร์"><br><span data-ttu-id="36e19-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="36e19-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="ไอคอนขั้นตอนตําแหน่งคลัสเตอร์"><br><span data-ttu-id="36e19-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="36e19-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="ไอคอนขั้นตอนรหัสการกำหนด"><br><span data-ttu-id="36e19-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="36e19-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="ไอคอนขั้นตอนของฟิลด์ที่กำหนดค่า"><br><span data-ttu-id="36e19-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="36e19-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="ไอคอนขั้นตอนที่กำหนดค่าหรือป้ายทะเบียน"><br><span data-ttu-id="36e19-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="36e19-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="ไอคอนขั้นตอนการรวมจากรหัสป้ายทะเบียนรวม"><br><span data-ttu-id="36e19-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="36e19-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="ไอคอนขั้นตอนการรวมเป็นรหัสป้ายทะเบียนรวม"><br><span data-ttu-id="36e19-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="36e19-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="ไอคอนขั้นตอนชนิดคอนเทนเนอร์"><br><span data-ttu-id="36e19-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="36e19-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="ไอคอนขั้นตอนการตรวจนับ"><br><span data-ttu-id="36e19-414">การตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="36e19-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="ไอคอนขั้นตอนรหัสเหตุผลการตรวจนับ"><br><span data-ttu-id="36e19-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="36e19-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="ไอคอนขั้นตอนรหัสประเทศผู้ผลิต"><br><span data-ttu-id="36e19-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="36e19-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="ไอคอนขั้นตอนการโอนการครอบครอง"><br><span data-ttu-id="36e19-420">Disposition</span><span class="sxs-lookup"><span data-stu-id="36e19-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="ไอคอนขั้นตอนเสร็จสิ้น"><br><span data-ttu-id="36e19-422">ทำแล้ว</span><span class="sxs-lookup"><span data-stu-id="36e19-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="ไอคอนขั้นตอนการยืนยันการเช็คอินของพนักงานขนส่ง"><br><span data-ttu-id="36e19-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="ไอคอนขั้นตอนรหัสการเช็คอินของพนักงานขนส่ง"><br><span data-ttu-id="36e19-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="36e19-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="ไอคอนขั้นตอนรหัสการเช็คเอาท์ของพนักงานขนส่ง"><br><span data-ttu-id="36e19-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="36e19-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="ไอคอนขั้นตอนวันหมดอายุ"><br><span data-ttu-id="36e19-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="36e19-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="ไอคอนขั้นตอนของฟิลด์"><br><span data-ttu-id="36e19-432">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="36e19-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="ไอคอนขั้นตอนจากการโอนการครอบครองชุดงาน"><br><span data-ttu-id="36e19-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="36e19-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="ไอคอนขั้นตอนสถานะสินค้าคงคลังเริ่มต้น"><br><span data-ttu-id="36e19-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="36e19-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="ไอคอนขั้นตอนแอททริบิวต์รหัส"><br><span data-ttu-id="36e19-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="36e19-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="ไอคอนขั้นตอนรหัสชุดงานสินค้าคงคลัง"><br><span data-ttu-id="36e19-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="36e19-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="ไอคอนขั้นตอนรหัสสีสินค้าคงคลัง"><br><span data-ttu-id="36e19-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="36e19-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="ไอคอนขั้นตอนที่ตั้งสินค้าคงคลัง"><br><span data-ttu-id="36e19-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="36e19-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="ไอคอนขั้นตอนรหัสลำดับประจำสินค้าคงคลัง"><br><span data-ttu-id="36e19-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="36e19-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="ไอคอนขั้นตอนรหัสขนาดสินค้าคงคลัง"><br><span data-ttu-id="36e19-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="36e19-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="ไอคอนขั้นตอนรหัสสถานะสินค้าคงคลัง"><br><span data-ttu-id="36e19-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="36e19-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="ไอคอนขั้นตอนรหัสลักษณะสินค้าคงคลัง"><br><span data-ttu-id="36e19-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="36e19-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="ไอคอนขั้นตอนรหัสรุ่นสินค้าคงคลัง"><br><span data-ttu-id="36e19-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="36e19-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="ไอคอนขั้นตอนรหัสสินค้า"><br><span data-ttu-id="36e19-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="36e19-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ไอคอนขั้นตอนรหัสคอนเทนเนอร์ ITM"><br><span data-ttu-id="36e19-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="36e19-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ไอคอนขั้นตอนรหัสการจัดส่ง ITM"><br><span data-ttu-id="36e19-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="36e19-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="ไอคอนขั้นตอนรหัสบัตรคัมบัง"><br><span data-ttu-id="36e19-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="36e19-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="ไอคอนขั้นตอนรหัสบัตรหรือคัมบัง"><br><span data-ttu-id="36e19-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="36e19-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="ไอคอนขั้นตอนรหัสของป้ายทะเบียน"><br><span data-ttu-id="36e19-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="36e19-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="ไอคอนขั้นตอนรหัสสินค้า"><br><span data-ttu-id="36e19-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="36e19-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="ไอคอนขั้นตอนการกำหนดตำแหน่งป้ายทะเบียนตามสถานที่"><br><span data-ttu-id="36e19-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="36e19-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="ไอคอนขั้นตอนป้ายทะเบียนหรือที่ตั้ง"><br><span data-ttu-id="36e19-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="36e19-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="ไอคอนขั้นตอนการตรวจสอบป้ายทะเบียนหรือที่ตั้ง"><br><span data-ttu-id="36e19-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="36e19-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="ป้ายทะเบียนหรือที่ตั้งจากไอคอนขั้นตอน"><br><span data-ttu-id="36e19-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="36e19-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="ป้ายทะเบียนหรือที่ตั้งเป็นไอคอนขั้นตอน"><br><span data-ttu-id="36e19-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="36e19-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="ไอคอนขั้นตอนของกระบวนการที่เสร็จสมบูรณ์แบบยาว"><br><span data-ttu-id="36e19-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="36e19-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="ไอคอนขั้นตอน LP หลักของการแบ่ง LP"><br><span data-ttu-id="36e19-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="36e19-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="ไอคอนขั้นตอนรหัสคอนเทนเนอร์การรวม"><br><span data-ttu-id="36e19-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="36e19-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="ไอคอนขั้นตอนหมายเลขรายการป้ายทะเบียนแบบผสม"><br><span data-ttu-id="36e19-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="36e19-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="ไอคอนขั้นตอนน้ำหนักของสินค้าขาออก"><br><span data-ttu-id="36e19-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="36e19-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="ไอคอนขั้นตอนของเจ้าของ"><br><span data-ttu-id="36e19-490">เจ้าของ</span><span class="sxs-lookup"><span data-stu-id="36e19-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="ไอคอนขั้นตอนป้ายทะเบียนหลัก"><br><span data-ttu-id="36e19-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="36e19-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="โปรดยืนยันไอคอนขั้นตอน"><br><span data-ttu-id="36e19-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="36e19-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="ไอคอนขั้นตอนหมายเลขรายการใบสั่งซื้อ"><br><span data-ttu-id="36e19-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="36e19-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="ไอคอนขั้นตอนหมายเลขใบสั่งซื้อ"><br><span data-ttu-id="36e19-498">หมายเลขใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="36e19-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="ไอคอนขั้นตอนตำแหน่งแบบเต็ม"><br><span data-ttu-id="36e19-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="36e19-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="ไอคอนขั้นตอนความแข็งแรง"><br><span data-ttu-id="36e19-502">ความแข็งแรง</span><span class="sxs-lookup"><span data-stu-id="36e19-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="ไอคอนขั้นตอนชื่อเครื่องพิมพ์"><br><span data-ttu-id="36e19-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="36e19-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="ไอคอนขั้นตอนรหัส Prod"><br><span data-ttu-id="36e19-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="36e19-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="ไอคอนขั้นตอนการยืนยันผลิตภัณฑ์"><br><span data-ttu-id="36e19-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="ไอคอนขั้นตอนการส่งสินค้า"><br><span data-ttu-id="36e19-510">ส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="36e19-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="ไอคอนขั้นตอนรหัสคลัสเตอร์การสำรองสินค้า"><br><span data-ttu-id="36e19-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="36e19-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="ไอคอนขั้นตอนของปริมาณ"><br><span data-ttu-id="36e19-514">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="36e19-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="การปรับปรุงปริมาณในไอคอนขั้นตอน"><br><span data-ttu-id="36e19-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="36e19-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="ไอคอนขั้นตอนแบบสั้นของปริมาณ"><br><span data-ttu-id="36e19-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="36e19-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="ไอคอนขั้นตอนปริมาณที่จะใช้"><br><span data-ttu-id="36e19-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="36e19-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="ไอคอนขั้นตอนปริมาณที่จะส่ง"><br><span data-ttu-id="36e19-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="36e19-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="ไอคอนขั้นตอนปริมาณที่จะขัดเกลา"><br><span data-ttu-id="36e19-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="36e19-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="ไอคอนขั้นตอนการยืนยันปริมาณ"><br><span data-ttu-id="36e19-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="36e19-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="ไอคอนขั้นตอนของงานสิ้นสุดการรายงานเมื่อเสร็จสมบูรณ์"><br><span data-ttu-id="36e19-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="36e19-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="ไอคอนขั้นตอนรหัสสถานที่รับ"><br><span data-ttu-id="36e19-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="36e19-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="ไอคอนขั้นตอนรหัสคอนเทนเนอร์การนำออก"><br><span data-ttu-id="36e19-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="36e19-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="ไอคอนขั้นตอนหมายเลข RMA"><br><span data-ttu-id="36e19-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="36e19-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="ไอคอนขั้นตอนของใบสั่งที่เลือก"><br><span data-ttu-id="36e19-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="36e19-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="ไอคอนขั้นตอนเหตุผลการเบิกสินค้าระยะสั้น"><br><span data-ttu-id="36e19-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="36e19-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="ไอคอนขั้นตอนรหัสตําแหน่งเรียงลำดับ"><br><span data-ttu-id="36e19-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="36e19-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="ไอคอนขั้นตอนรหัสของป้ายทะเบียนเป้าหมาย"><br><span data-ttu-id="36e19-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="ไอคอนขั้นตอนหมายเลขรายการสุดท้าย"><br><span data-ttu-id="36e19-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="36e19-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="ไอคอนขั้นตอนที่ตั้งสุดท้าย"><br><span data-ttu-id="36e19-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="36e19-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="ไอคอนขั้นตอนหมายเลขสุดท้าย"><br><span data-ttu-id="36e19-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="36e19-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="ไอคอนขั้นตอนคลังสินค้าสุดท้าย"><br><span data-ttu-id="36e19-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="36e19-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="ไอคอนขั้นตอนรหัสการบรรทุกเพื่อขนส่ง"><br><span data-ttu-id="36e19-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="36e19-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="ไอคอนขั้นตอนรหัสชุดงานผู้จัดจำหน่าย"><br><span data-ttu-id="36e19-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="36e19-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="ไอคอนขั้นตอนรหัสป้ายชื่อเวฟ"><br><span data-ttu-id="36e19-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="36e19-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="ไอคอนขั้นตอนปริมาณป้ายชื่อเวฟ"><br><span data-ttu-id="36e19-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="36e19-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="ไอคอนขั้นตอนน้ำหนัก"><br><span data-ttu-id="36e19-560">น้ำหนัก</span><span class="sxs-lookup"><span data-stu-id="36e19-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="ไอคอนขั้นตอนน้ำหนักที่จะใช้"><br><span data-ttu-id="36e19-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="36e19-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="ไอคอนขั้นตอนชนิดการปรับปรุง WHS"><br><span data-ttu-id="36e19-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="36e19-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="ไอคอนขั้นตอนข้อยกเว้นการรับ WHS"><br><span data-ttu-id="36e19-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="36e19-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="ไอคอนขั้นตอนรหัสที่ตั้ง WMS"><br><span data-ttu-id="36e19-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="36e19-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="ไอคอนขั้นตอนรหัสงาน"><br><span data-ttu-id="36e19-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="36e19-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="ไอคอนขั้นตอนรหัสงานที่จะยกเลิก"><br><span data-ttu-id="36e19-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="36e19-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="ไอคอนขั้นตอนรหัสของป้ายทะเบียนงาน"><br><span data-ttu-id="36e19-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36e19-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="ไอคอนขั้นตอนคลัสเตอร์ของการสำรองสินค้าของรหัสของป้ายทะเบียนงาน"><br><span data-ttu-id="36e19-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="36e19-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="ไอคอนขั้นตอนรหัสกลุ่มงาน"><br><span data-ttu-id="36e19-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="36e19-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="ไอคอนขั้นตอนรหัสโซน"><br><span data-ttu-id="36e19-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="36e19-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="36e19-581">ตัวอย่าง: กําหนดไอคอนขั้นตอนและชื่อให้กับโฟลว์ที่กําหนดเอง</span><span class="sxs-lookup"><span data-stu-id="36e19-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="36e19-582">ตัวอย่างนี้อธิบายวิธีการตั้งค่าไอคอนขั้นตอนและชื่อขั้นตอนของโฟลว์งานที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="36e19-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="36e19-583">สถานการณ์ดังกล่าวสร้างขึ้นจากตัวอย่างของโฟลว์งานที่กำหนดเอง ซึ่งนําเสนอและสำรวจไปในรายละเอียดเพิ่มเติมในประกาศบล็อกต่อไปนี้: [การกำหนดค่า Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app)</span><span class="sxs-lookup"><span data-stu-id="36e19-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="36e19-584">โฟลว์งานจะใช้ได้กับวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="36e19-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="36e19-585">แอปจะแสดงหน้าที่ขอให้ผู้ปฏิบัติงานระบุรหัสคอนเทนเนอร์ (ตัวอย่างเช่น โดยการสแกนบาร์โค้ด)</span><span class="sxs-lookup"><span data-stu-id="36e19-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="36e19-586">หากรหัสคอนเทนเนอร์ถูกต้อง แอปจะเปิดขึ้นหน้าใหม่ที่เตือนผู้ปฏิบัติงานเกี่ยวกับน้ําหนัก</span><span class="sxs-lookup"><span data-stu-id="36e19-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="36e19-587">(หากรหัสคอนเทนเนอร์ไม่ถูกต้อง ผู้ปฏิบัติงานจะถูกส่งกลับไปที่หน้าแรก)</span><span class="sxs-lookup"><span data-stu-id="36e19-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="36e19-588">เมื่อผู้ปฏิบัติงานป้อนน้ําหนักที่ถูกต้อง ระบบจะจัดเก็บน้ําหนักและส่งคืนผู้ปฏิบัติงานไปที่หน้าแรก</span><span class="sxs-lookup"><span data-stu-id="36e19-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="36e19-589">ในแผนภาพต่อไปนี้แสดงโฟลว์งานนี้</span><span class="sxs-lookup"><span data-stu-id="36e19-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="36e19-590">![แผนภาพของโฟลว์งาน](media/step-icons-example-task-flow.png "แผนภาพของโฟลว์งาน")</span><span class="sxs-lookup"><span data-stu-id="36e19-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="36e19-591">สร้างคลาสขั้นตอนเกี่ยวกับหน้าข้อมูลป้อนเข้าคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="36e19-591">Create a step class for the container input page</span></span>

<span data-ttu-id="36e19-592">หน้าข้อมูลป้อนเข้าคอนเทนเนอร์ช่วยให้ผู้ปฏิบัติงานสแกนหรือป้อนรหัสคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="36e19-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="36e19-593">![หน้าข้อมูลป้อนเข้าคอนเทนเนอร์](media/step-icons-example-container-input.png "หน้าข้อมูลป้อนเข้าคอนเทนเนอร์")</span><span class="sxs-lookup"><span data-stu-id="36e19-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="36e19-594">ในหน้าข้อมูลป้อนเข้าคอนเทนเนอร์ ชื่อตัวควบคุมของฟิลด์ป้อนข้อมูลคือ `ContainerId`</span><span class="sxs-lookup"><span data-stu-id="36e19-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="36e19-595">เนื่องจากชื่อตัวควบคุมนี้ไม่อยู่ใน [รายการรหัสขั้นตอน](#step-ids-classes) คุณจึงไม่พบขั้นตอนที่มีอยู่ซึ่งอิงตามรหัสขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="36e19-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="36e19-596">ดังนั้น คุณต้องสร้างคลาสขั้นตอนที่แสดงถึงขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="36e19-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="36e19-597">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="36e19-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="36e19-598">รหัสของไอคอนขั้นตอนจัดเก็บอยู่ในสมาชิกคลาส `defaultStepIcon` และชื่อขั้นตอนจัดเก็บอยู่ในสมาชิกคลาส `defaultStepTitle`</span><span class="sxs-lookup"><span data-stu-id="36e19-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="36e19-599">เมื่อต้องการกําหนดไอคอนขั้นตอน ให้ตั้งค่า `defaultStepIcon` เป็นหนึ่งในรหัสไอคอนที่แสดงรายการในส่วน [ไอคอนขั้นตอนที่พร้อมใช้งาน](#step-icons) ก่อนหน้าในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="36e19-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="36e19-600">ใช้ไอคอนขั้นตอนและชื่อมาตรฐานหรือที่กำหนดเองสำหรับอินพุทน้ำหนัก</span><span class="sxs-lookup"><span data-stu-id="36e19-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="36e19-601">หน้าอินพุทน้ําหนักให้ผู้ปฏิบัติงานป้อนน้ําหนัก</span><span class="sxs-lookup"><span data-stu-id="36e19-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="36e19-602">![หน้าอินพุทน้ําหนัก](media/step-icons-example-weight-input.png "หน้าอินพุทน้ําหนัก")</span><span class="sxs-lookup"><span data-stu-id="36e19-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="36e19-603">ในหน้าอินพุทน้ําหนัก ชื่อตัวควบคุมของฟิลด์ป้อนเข้าคือ `Weight` ซึ่งอยู่ใน [รายการของรหัสขั้นตอน](#step-ids-classes)</span><span class="sxs-lookup"><span data-stu-id="36e19-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="36e19-604">ดังนั้นถ้าไอคอนขั้นตอนและชื่อที่กําหนดไว้ในคลาส `WHSMobileAppStepWeight` เป็นที่ยอมรับให้คุณ คุณจะไม่ต้องเปลี่ยนสิ่งใดในขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="36e19-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="36e19-605">อย่างไรก็ตาม หากคุณต้องการใช้ไอคอนหรือชื่ออื่นของขั้นตอนนี้ คุณสามารถแทนที่วิธีการ `stepId()` หรือวิธีการ `stepInfo()` ในคลาสโปรแกรมสร้าง</span><span class="sxs-lookup"><span data-stu-id="36e19-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="36e19-606">แต่ละโฟลว์งานจะมีโปรแกรมสร้างข้อมูลขั้นตอนของตนเอง</span><span class="sxs-lookup"><span data-stu-id="36e19-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="36e19-607">การแทนที่วิธีการ stepId()</span><span class="sxs-lookup"><span data-stu-id="36e19-607">Override the stepId() method</span></span>

<span data-ttu-id="36e19-608">ตัวอย่างต่อไปนี้แสดงวิธีการหนึ่งที่คุณสามารถปรับเปลี่ยนคลาสของโปรแกรมสร้างด้วยการแทนที่วิธีการ `stepId()`</span><span class="sxs-lookup"><span data-stu-id="36e19-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="36e19-609">จากนั้นให้คุณสร้างคลาสขั้นตอนในขั้นตอน `NewWeight`</span><span class="sxs-lookup"><span data-stu-id="36e19-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="36e19-610">รหัสควรคล้ายกับรหัสสำหรับตัวอย่าง `ContainerId` ที่แสดงไว้ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="36e19-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="36e19-611">การแทนที่วิธีการ stepInfo()</span><span class="sxs-lookup"><span data-stu-id="36e19-611">Override the stepInfo() method</span></span>

<span data-ttu-id="36e19-612">ตัวอย่างต่อไปนี้แสดงวิธีการหนึ่งที่คุณสามารถปรับเปลี่ยนคลาสของโปรแกรมสร้างด้วยการแทนที่วิธีการ `stepInfo()`</span><span class="sxs-lookup"><span data-stu-id="36e19-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="36e19-613">จากนั้นให้คุณสร้างออบเจ็กต์ `WHSMobileAppStepInfo` และตั้งไอคอนและ/หรือชื่อโดยตรง</span><span class="sxs-lookup"><span data-stu-id="36e19-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36e19-614">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="36e19-614">Additional resources</span></span>

- [<span data-ttu-id="36e19-615">ติดตั้งและเชื่อมต่อแอปการบริหารคลังสินค้าบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="36e19-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="36e19-616">การตั้งค่าผู้ใช้ของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="36e19-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
