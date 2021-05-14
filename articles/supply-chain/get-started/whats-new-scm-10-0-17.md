---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Supply Chain Management 10.0.17 (เมษายน 2021)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่ หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Supply Chain Management 10.0.17
author: kamaybac
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: fd8c306dd6c3aeb7ef41b4eb3f6f8bad040035c2
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935616"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10017-april-2021"></a><span data-ttu-id="47149-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Supply Chain Management 10.0.17 (เมษายน 2021)</span><span class="sxs-lookup"><span data-stu-id="47149-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.17 (April 2021)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47149-104">หัวข้อนี้แสดงรายการคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลงอย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Supply Chain Management รุ่น 10.0.17</span><span class="sxs-lookup"><span data-stu-id="47149-104">This topic lists features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management version 10.0.17.</span></span> <span data-ttu-id="47149-105">รุ่นนี้มีหมายเลขการสร้างเป็น 10.0.761 และพร้อมใช้งานดังนี้:</span><span class="sxs-lookup"><span data-stu-id="47149-105">This version has a build number of 10.0.761 and is available as follows:</span></span>

- <span data-ttu-id="47149-106">**ตัวอย่างการนำออกใช้:** กุมภาพันธ์ 2021</span><span class="sxs-lookup"><span data-stu-id="47149-106">**Preview of release:** February 2021</span></span>
- <span data-ttu-id="47149-107">**ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตเอง):** มีนาคม 2021</span><span class="sxs-lookup"><span data-stu-id="47149-107">**General availability of release (self-update):** March 2021</span></span>
- <span data-ttu-id="47149-108">**ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตอัตโนมัติ):** เมษายน 2021</span><span class="sxs-lookup"><span data-stu-id="47149-108">**General availability of release (auto-update):** April 2021</span></span>

## <a name="features-included-in-this-release"></a><span data-ttu-id="47149-109">คุณลักษณะที่รวมอยู่ในการนำออกใช้นี้</span><span class="sxs-lookup"><span data-stu-id="47149-109">Features included in this release</span></span>

<span data-ttu-id="47149-110">คุณลักษณะต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้</span><span class="sxs-lookup"><span data-stu-id="47149-110">The following features are included in this release.</span></span>  <span data-ttu-id="47149-111">ไปตามลิงก์ [แผนนำออกใช้](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) เพื่อดูวันที่นำออกใช้อย่างเป็นทางการสำหรับแต่ละคุณลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="47149-111">Follow the links to the [release plan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) to see the official release dates for each feature.</span></span>

<span data-ttu-id="47149-112">คุณลักษณะเหล่านี้ส่วนใหญ่ต้องถูกเปิดใช้งานโดยใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ก่อนที่คุณจะสามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="47149-112">Most of these features must be enabled using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) before you can use them.</span></span>

### <a name="asset-management"></a><span data-ttu-id="47149-113">การจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="47149-113">Asset management</span></span>

- [<span data-ttu-id="47149-114">ใช้กฎสำหรับการจัดกลุ่มใบสั่งงาน ในขณะที่รันแผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="47149-114">Apply rules for grouping work orders while running a maintenance plan</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/apply-rules-grouping-work-orders-while-running-maintenance-plan)<br> <span data-ttu-id="47149-115">- สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสร้างใบสั่งบริการ ให้ดูที่ [การสร้างใบสั่งงาน](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md)</span><span class="sxs-lookup"><span data-stu-id="47149-115">- For more information, see [Creating work orders](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md).</span></span>

- [<span data-ttu-id="47149-116">เรียกเก็บเงินจากลูกค้าเพื่องานการบํารุงรักษา</span><span class="sxs-lookup"><span data-stu-id="47149-116">Bill customers for maintenance work</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/bill-customers-maintenance-work)<br> <span data-ttu-id="47149-117">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ใบเรียกเก็บเงินการบํารุงรักษาสินทรัพย์ที่ลูกค้าเป็นเจ้าของ](../asset-management/integration-to-project-management-and-accounting/customer-billing.md)</span><span class="sxs-lookup"><span data-stu-id="47149-117">- For more information, see [Bill for maintenance on customer-owned assets](../asset-management/integration-to-project-management-and-accounting/customer-billing.md).</span></span>

- [<span data-ttu-id="47149-118">วางแผนการบํารุงรักษาตามค่าตัวนับสินทรัพย์สะสม</span><span class="sxs-lookup"><span data-stu-id="47149-118">Plan maintenance based on accumulated asset counter values</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/plan-maintenance-based-accumulated-asset-counter-values)<br> <span data-ttu-id="47149-119">- สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [แผนการบำรุงรักษา](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md)</span><span class="sxs-lookup"><span data-stu-id="47149-119">- For more information, see [Maintenance plans](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md).</span></span>

### <a name="inventory-and-logistics"></a><span data-ttu-id="47149-120">สินค้าคงคลังและลอจิสติกส์</span><span class="sxs-lookup"><span data-stu-id="47149-120">Inventory and logistics</span></span>

- [<span data-ttu-id="47149-121">กรอบงานการรวมเครื่องมือจัดการวัสดุเพื่อกระบวนการคลังสินค้าอัตโนมัติ (ก่อนหน้านี้คือ MHAX)</span><span class="sxs-lookup"><span data-stu-id="47149-121">Integration framework for material handling equipment for automated warehouse processes (previously MHAX)</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/integration-framework-material-handling-equipment-automated-warehouse-processes-previously-mhax)<br> <span data-ttu-id="47149-122">- สำหรับข้อมูลเพิ่มเติม ดูที่ [อินเทอร์เฟสเครื่องมือจัดการวัสดุ (MHAX)](../warehousing/mhax.md)</span><span class="sxs-lookup"><span data-stu-id="47149-122">- For more information, see [Material handling equipment interface (MHAX)](../warehousing/mhax.md).</span></span>

- [<span data-ttu-id="47149-123">ต้นทุนแฝง</span><span class="sxs-lookup"><span data-stu-id="47149-123">Landed cost</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/landed-cost)<br> <span data-ttu-id="47149-124">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โมดูลต้นทุนแฝง](../landed-cost/landed-cost-overview.md)</span><span class="sxs-lookup"><span data-stu-id="47149-124">- For more information, see [Landed cost module](../landed-cost/landed-cost-overview.md).</span></span>

- [<span data-ttu-id="47149-125">การจัดส่งเทียบกับมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="47149-125">Packing vs. storage dimensions</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/packing-vs.-storage-dimensions)<br> <span data-ttu-id="47149-126">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่ามิติต่าง ๆ ของการบรรจุและการจัดเก็บ](../warehousing/packing-vs-storage-dimensions.md)</span><span class="sxs-lookup"><span data-stu-id="47149-126">- For more information, see [Set different dimensions for packing and storage](../warehousing/packing-vs-storage-dimensions.md).</span></span>

- [<span data-ttu-id="47149-127">มุมมองที่บันทึกไว้ของสินค้าคงคลังและโลจิสติกส์</span><span class="sxs-lookup"><span data-stu-id="47149-127">Saved views for inventory and logistics</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-inventory-logistics)<br> <span data-ttu-id="47149-128">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [มุมมองที่บันทึกไว้แบบมาตรฐานของ Supply Chain Management](saved-views-scm.md)</span><span class="sxs-lookup"><span data-stu-id="47149-128">- For more information, see [Standard saved views for Supply Chain Management](saved-views-scm.md).</span></span>

- [<span data-ttu-id="47149-129">จัดกำหนดการการสร้างงานของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="47149-129">Schedule warehouse work creation</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-warehouse-work-creation)<br> <span data-ttu-id="47149-130">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [จัดกำหนดการการสร้างงานระหว่างเวฟ](../warehousing/configure-wave-schedule-work-creation.md)ฟ</span><span class="sxs-lookup"><span data-stu-id="47149-130">- For more information, see [Schedule work creation during wave](../warehousing/configure-wave-schedule-work-creation.md).</span></span>

- [<span data-ttu-id="47149-131">ตั้งค่ามิติทางการเงินเริ่มต้นในใบสำคัญการประเมินค่าต้นทุนแบบมาตรฐานใหม่ของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="47149-131">Set default financial dimensions for inventory standard cost revaluation vouchers</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/set-default-financial-dimensions-inventory-standard-cost-revaluation-vouchers)<br> <span data-ttu-id="47149-132">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [จัดการการอัปเดตต้นทุนมาตรฐาน](../cost-management/manage-standard-cost-updates.md)</span><span class="sxs-lookup"><span data-stu-id="47149-132">- For more information, see [Manage standard cost updates](../cost-management/manage-standard-cost-updates.md).</span></span>

- [<span data-ttu-id="47149-133">การจัดส่งพัสดุขนาดเล็ก (SPS)</span><span class="sxs-lookup"><span data-stu-id="47149-133">Small parcel shipping (SPS)</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/small-parcel-shipping-sps)<br> <span data-ttu-id="47149-134">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การจัดส่งพัสดุขนาดเล็ก](../warehousing/small-parcel-shipping.md)</span><span class="sxs-lookup"><span data-stu-id="47149-134">- For more information, see [Small parcel shipping](../warehousing/small-parcel-shipping.md).</span></span>

- [<span data-ttu-id="47149-135">การดำเนินการคลังสินค้าด้วยสเกลยูนิตในระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="47149-135">Warehouse execution with scale units in the cloud</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-scale-units-cloud)<br> <span data-ttu-id="47149-136">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ปริมาณงานการจัดการคลังสินค้าสำหรับสเกลยูนิตในระบบคลาวด์และ Edge](../cloud-edge/cloud-edge-workload-warehousing.md) และ [ใบสั่งคลังสินค้าสำหรับ scale unit ของระบบคลาวด์และ Edge](../cloud-edge/cloud-edge-warehouse-order.md)</span><span class="sxs-lookup"><span data-stu-id="47149-136">- For more information, see [Warehouse management workloads for cloud and edge scale units](../cloud-edge/cloud-edge-workload-warehousing.md) and [Warehouse orders for cloud and edge scale units](../cloud-edge/cloud-edge-warehouse-order.md).</span></span>

- [<span data-ttu-id="47149-137">แอปพลิเคชันการจัดการคลังสินค้าบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="47149-137">Warehouse management mobile application</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application)<br> <span data-ttu-id="47149-138">- สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การติดตั้งและเชื่อมต่อแอปการจัดการคลังสินค้า](../warehousing/install-configure-warehouse-management-app.md) และ [การตั้งค่าผู้ใช้อุปกรณ์เคลื่อนที่](../warehousing/mobile-device-user-settings.md)</span><span class="sxs-lookup"><span data-stu-id="47149-138">- For more information, see [Install and connect the Warehouse Management app](../warehousing/install-configure-warehouse-management-app.md) and [Mobile device user settings](../warehousing/mobile-device-user-settings.md).</span></span>

- <span data-ttu-id="47149-139">การแจ้งเตือนการดำเนินการเวฟ</span><span class="sxs-lookup"><span data-stu-id="47149-139">Wave execution notifications</span></span><br> <span data-ttu-id="47149-140">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การแจ้งเตือนการดำเนินการของเวฟ](../warehousing/wave-execution-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="47149-140">- For more information, see [Wave execution notifications](../warehousing/wave-execution-notifications.md)</span></span>

### <a name="manufacturing"></a><span data-ttu-id="47149-141">การผลิต</span><span class="sxs-lookup"><span data-stu-id="47149-141">Manufacturing</span></span>

- [<span data-ttu-id="47149-142">ความสามารถในการจัดการสินทรัพย์ในอินเทอร์เฟสการดำเนินการผลิต</span><span class="sxs-lookup"><span data-stu-id="47149-142">Asset management capabilities in the production floor execution interface</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/asset-management-capabilities-production-floor-execution-interface)<br> <span data-ttu-id="47149-143">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกอินเทอร์เฟสการดำเนินการผลิต](../production-control/production-floor-execution-configure.md)</span><span class="sxs-lookup"><span data-stu-id="47149-143">- For more information, see [Configure the production floor execution interface](../production-control/production-floor-execution-configure.md).</span></span>

- [<span data-ttu-id="47149-144">การดำเนินการผลิตด้วยสเกลยูนิตในระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="47149-144">Manufacturing execution with scale units in the cloud</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-scale-units-cloud)<br> <span data-ttu-id="47149-145">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ปริมาณงานในการจัดการการผลิตสำหรับสเกลยูนิตในระบบคลาวด์และ Edge](../cloud-edge/cloud-edge-workload-manufacturing.md)</span><span class="sxs-lookup"><span data-stu-id="47149-145">- For more information, see [Manufacturing execution workloads for cloud and edge scale units](../cloud-edge/cloud-edge-workload-manufacturing.md).</span></span>

- [<span data-ttu-id="47149-146">แทนที่หลักการสำรองเริ่มต้นสำหรับวัสดุในการผลิต</span><span class="sxs-lookup"><span data-stu-id="47149-146">Override the default reservation principle for materials in production</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/override-default-reservation-principle-materials-production)<br> <span data-ttu-id="47149-147">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [แทนที่หลักการจองเริ่มต้นของวัสดุในการผลิต](../production-control/override-default-reservation-principle.md)</span><span class="sxs-lookup"><span data-stu-id="47149-147">- For more information, see [Override the default reservation principle for materials in production](../production-control/override-default-reservation-principle.md).</span></span>

- [<span data-ttu-id="47149-148">มุมมองที่บันทึกไว้ของการควบคุมการผลิต</span><span class="sxs-lookup"><span data-stu-id="47149-148">Saved views for production control</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-production-control)<br> <span data-ttu-id="47149-149">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [มุมมองที่บันทึกไว้แบบมาตรฐานของ Supply Chain Management](saved-views-scm.md)</span><span class="sxs-lookup"><span data-stu-id="47149-149">- For more information, see [Standard saved views for Supply Chain Management](saved-views-scm.md).</span></span>

- <span data-ttu-id="47149-150">ลำดับหมายเลขแบบรวมสำหรับรหัสงาน</span><span class="sxs-lookup"><span data-stu-id="47149-150">Unified number sequence for job IDs</span></span><br> <span data-ttu-id="47149-151">- ดูข้อมูลเพิ่มเติมที่ ดูที่ [สำดับหมายเลขแบบรวมของรหัสงาน](../production-control/unified-job-ids.md)</span><span class="sxs-lookup"><span data-stu-id="47149-151">- For more information, see [Unified number sequence for job IDs](../production-control/unified-job-ids.md).</span></span>

### <a name="planning"></a><span data-ttu-id="47149-152">การวางแผน</span><span class="sxs-lookup"><span data-stu-id="47149-152">Planning</span></span>

- [<span data-ttu-id="47149-153">การสนับสนุนกรอบเวลาความครอบคลุมเพื่อการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="47149-153">Coverage time fence support for Planning Optimization</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/coverage-time-fence-support-planning-optimization)<br> <span data-ttu-id="47149-154">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [กรอบเวลาความครอบคลุม](../master-planning/planning-optimization/coverage-time-fence.md)</span><span class="sxs-lookup"><span data-stu-id="47149-154">- For more information, see [Coverage time fences](../master-planning/planning-optimization/coverage-time-fence.md).</span></span>

- [<span data-ttu-id="47149-155">การสนับสนุนแบบจำลองย่อยของการคาดการณ์เพื่อเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="47149-155">Forecast submodel support for Planning Optimization</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/forecast-submodel-support-planning-optimization)<br> <span data-ttu-id="47149-156">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การวางแผนหลักที่มีการคาดการณ์ความต้องการ](../master-planning/planning-optimization/demand-forecast.md)</span><span class="sxs-lookup"><span data-stu-id="47149-156">- For more information, see [Master planning with demand forecasts](../master-planning/planning-optimization/demand-forecast.md).</span></span>

- [<span data-ttu-id="47149-157">การสนับสนุนใบขอซื้อสำหรับการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="47149-157">Purchase requisition support for Planning Optimization</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/purchase-requisition-support-planning-optimization)<br> <span data-ttu-id="47149-158">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ใบขอซื้อ](../master-planning/planning-optimization/purchase-requisitions.md)</span><span class="sxs-lookup"><span data-stu-id="47149-158">- For more information, see [Purchase requisitions](../master-planning/planning-optimization/purchase-requisitions.md).</span></span>

- [<span data-ttu-id="47149-159">มุมมองที่บันทึกไว้สำหรับแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="47149-159">Saved views for planned orders</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-planned-orders)<br> <span data-ttu-id="47149-160">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [มุมมองที่บันทึกไว้แบบมาตรฐานของ Supply Chain Management](saved-views-scm.md)</span><span class="sxs-lookup"><span data-stu-id="47149-160">- For more information, see [Standard saved views for Supply Chain Management](saved-views-scm.md).</span></span>

### <a name="product-information-management"></a><span data-ttu-id="47149-161">การจัดการข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="47149-161">Product information management</span></span>

- [<span data-ttu-id="47149-162">เปิดใช้งานการจัดการการเปลี่ยนแปลงในผลิตภัณฑ์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="47149-162">Enable change management on existing products</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enable-change-management-existing-products)<br> <span data-ttu-id="47149-163">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เปิดใช้งานการจัดการการเปลี่ยนแปลงผลิตภัณฑ์ที่มีอยู่](../engineering-change-management/change-management-existing-products.md)</span><span class="sxs-lookup"><span data-stu-id="47149-163">- For more information, see [Enable change management on existing products](../engineering-change-management/change-management-existing-products.md).</span></span>

## <a name="new-and-updated-documentation-resources"></a><span data-ttu-id="47149-164">ทรัพยากรคู่มือใหม่และคู่มือที่มีการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="47149-164">New and updated documentation resources</span></span>

<span data-ttu-id="47149-165">เมื่อเร็ว ๆ นี้เรามีการเพิ่มหรืออัพเดตส่วนความช่วยเหลือต่อไปนี้อย่างมาก</span><span class="sxs-lookup"><span data-stu-id="47149-165">We have recently added or significantly updated the following help topics.</span></span> <span data-ttu-id="47149-166">ไม่จำเป็นต้องมีความเกี่ยวข้องกับลักษณะการทำงานใหม่ที่เพิ่มสำหรับรุ่นนี้ ตามที่แสดงรายการไว้ในส่วนก่อนหน้านี้ แต่อาจช่วยให้คุณสามารถเพิ่มเติมจากลักษณะการทำงานที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="47149-166">They aren't necessarily related to the new features added for this release, as listed in the previous section, but they may help you to get more out of existing features.</span></span>

### <a name="cost-management"></a><span data-ttu-id="47149-167">การจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="47149-167">Cost management</span></span>

- [<span data-ttu-id="47149-168">แก้ไขปัญหาการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="47149-168">Troubleshoot cost management</span></span>](../cost-management/troubleshoot-costmanagement.md)

### <a name="asset-management"></a><span data-ttu-id="47149-169">การจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="47149-169">Asset management</span></span>

- [<span data-ttu-id="47149-170">ตั้งค่าพื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="47149-170">Set up the Asset management mobile workspace</span></span>](../asset-management/set-up-asset-management-mobile.md)

### <a name="inventory-and-logistics"></a><span data-ttu-id="47149-171">สินค้าคงคลังและลอจิสติกส์</span><span class="sxs-lookup"><span data-stu-id="47149-171">Inventory and logistics</span></span>

- [<span data-ttu-id="47149-172">ตั้งค่าคอนฟิกตัวกรองผลิตภัณฑ์ในธุรกรรมคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="47149-172">Configure product filters for warehouse transactions</span></span>](../warehousing/filters-and-filter-codes.md)

- [<span data-ttu-id="47149-173">การตรวจนับตามรอบของสถานที่บางส่วน</span><span class="sxs-lookup"><span data-stu-id="47149-173">Partial location cycle counting</span></span>](../warehousing/partial-location-cycle-counting.md)

- [<span data-ttu-id="47149-174">การจัดกลุ่มรายการการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="47149-174">Pick line grouping</span></span>](../warehousing/pick-line-grouping.md)

- [<span data-ttu-id="47149-175">แก้ไขปัญหาการดําเนินการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="47149-175">Troubleshoot inventory operations</span></span>](../inventory/troubleshoot-inventory-operations.md)

- [<span data-ttu-id="47149-176">การแบ่งช่วงเวลาของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="47149-176">Warehouse slotting</span></span>](../warehousing/warehouse-slotting.md)

### <a name="manufacturing"></a><span data-ttu-id="47149-177">การผลิต</span><span class="sxs-lookup"><span data-stu-id="47149-177">Manufacturing</span></span>

- [<span data-ttu-id="47149-178">ออกแบบอินเทอร์เฟสการดำเนินการผลิต</span><span class="sxs-lookup"><span data-stu-id="47149-178">Design the production floor execution interface</span></span>](../production-control/production-floor-execution-tabs.md)

### <a name="planning"></a><span data-ttu-id="47149-179">การวางแผน</span><span class="sxs-lookup"><span data-stu-id="47149-179">Planning</span></span>

- [<span data-ttu-id="47149-180">การวางแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="47149-180">Intercompany planning</span></span>](../master-planning/planning-optimization/Intercompany-planning.md)

- [<span data-ttu-id="47149-181">การทำเครื่องหมายสินค้าคงคลังด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="47149-181">Inventory marking with Planning Optimization</span></span>](../master-planning/planning-optimization/marking.md)

- [<span data-ttu-id="47149-182">การวางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="47149-182">Production planning</span></span>](../master-planning/planning-optimization/production-planning.md)

- [<span data-ttu-id="47149-183">ใบขอซื้อในการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="47149-183">Purchase requisitions in master planning</span></span>](../master-planning/planning-optimization/purchase-requisitions.md)

## <a name="additional-resources"></a><span data-ttu-id="47149-184">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="47149-184">Additional resources</span></span>

### <a name="platform-updates-for-finance-and-operations-apps"></a><span data-ttu-id="47149-185">Platform update สำหรับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="47149-185">Platform updates for Finance and Operations apps</span></span>

<span data-ttu-id="47149-186">Microsoft Dynamics 365 Supply Chain Management 10.0.17 รวมถึง Platform update</span><span class="sxs-lookup"><span data-stu-id="47149-186">Microsoft Dynamics 365 Supply Chain Management 10.0.17 includes platform updates.</span></span> <span data-ttu-id="47149-187">เมื่อต้องการเรียนรู้เพิ่มเติม ให้ดูที่ [Platform update สำหรับรุ่น10.0.17 ของแอป Finance and Operations (เมษายน 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md)</span><span class="sxs-lookup"><span data-stu-id="47149-187">To learn more, see [Platform updates for version 10.0.17 of Finance and Operations apps (April 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md).</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="47149-188">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="47149-188">Bug fixes</span></span>

<span data-ttu-id="47149-189">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขบักที่รวมอยู่ในการอัปเดตแต่ละรายการที่เป็นส่วนหนึ่งของ 10.0.17 ให้ลงชื่อเข้าใช้ Lifecycle Services (LCS) และดู [บทความ KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=551039&dbType=3&qc=91219e7c3fc585acb17b810c915c3cbea499403538520c40e54de43a53aea6a8)</span><span class="sxs-lookup"><span data-stu-id="47149-189">For information about the bug fixes included in each of the updates that are part of 10.0.17, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=551039&dbType=3&qc=91219e7c3fc585acb17b810c915c3cbea499403538520c40e54de43a53aea6a8).</span></span>

### <a name="dynamics-365-2021-release-wave-1-plan"></a><span data-ttu-id="47149-190">Dynamics 365: 2021 แผนเวฟการนำออกใช้ 1</span><span class="sxs-lookup"><span data-stu-id="47149-190">Dynamics 365: 2021 release wave 1 plan</span></span>

<span data-ttu-id="47149-191">สงสัยเกี่ยวกับความสามารถที่กำลังจะเกิดขึ้นและที่เผยแพร่เมื่อเร็วๆ นี้ในแอปหรือแพลตฟอร์มทางธุรกิจใดๆ ของเราใช่ไหม</span><span class="sxs-lookup"><span data-stu-id="47149-191">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="47149-192">ตรวจสอบ [Dynamics 365: 2021 แผนเวฟการนำออกใช้ 1](/dynamics365-release-plan/2021wave1/)</span><span class="sxs-lookup"><span data-stu-id="47149-192">Check out the [Dynamics 365: 2021 release wave 1 plan](/dynamics365-release-plan/2021wave1/).</span></span> <span data-ttu-id="47149-193">เราได้บันทึกทุกรายละเอียดอย่างครอบคลุมตั้งแต่ต้นจนจบในเอกสารเดียวที่คุณสามารถใช้สำหรับการวางแผนได้</span><span class="sxs-lookup"><span data-stu-id="47149-193">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="47149-194">คุณลักษณะ Supply Chain Management ที่ถูกลบและที่ถูกยกเลิกการใช้</span><span class="sxs-lookup"><span data-stu-id="47149-194">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="47149-195">หัวข้อ [คุณลักษณะที่ถูกลบและที่ถูกยกเลิกการใช้ใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) จะอธิบายถึงคุณลักษณะที่ได้รับหรือถูกจัดกำหนดการให้ถูกลบหรือถูกยกเลิกการใช้สำหรับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="47149-195">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="47149-196">คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="47149-196">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="47149-197">คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต</span><span class="sxs-lookup"><span data-stu-id="47149-197">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="47149-198">ก่อนที่คุณลักษณะใดๆ จะถูกลบออกจากผลิตภัณฑ์ จะมีการประกาศการแจ้งเตือนการยกเลิกการใช้ในหัวข้อ [คุณลักษณะที่ถูกลบหรือที่ถูกเลิกใช้งานใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 เดือนก่อนการลบ</span><span class="sxs-lookup"><span data-stu-id="47149-198">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="47149-199">สำหรับการจำแนกการเปลี่ยนแปลงที่มีผลกระทบเฉพาะต่อเวลาการคอมไพล์ แต่เป็นไบนารีที่เข้ากันได้กับสภาพแวดล้อม sandbox และสภาพแวดล้อมการผลิต เวลาในการยกเลิกการใช้จะน้อยกว่า 12 เดือน</span><span class="sxs-lookup"><span data-stu-id="47149-199">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="47149-200">โดยทั่วไป รายการเหล่านี้คือการอัปเดตการทำงานที่จำเป็นต้องทำกับคอมไพเลอร์</span><span class="sxs-lookup"><span data-stu-id="47149-200">Typically, these are functional updates that need to be made to the compiler.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
