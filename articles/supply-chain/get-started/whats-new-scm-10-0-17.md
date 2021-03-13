---
title: ตัวอย่าง Dynamics 365 Supply Chain Management 10.0.17 (เมษายน 2021)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่ หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Supply Chain Management 10.0.17
author: kamaybac
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-11-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: bfa6e04f8d7ae192d0acd88fb3f1d7e2ce6cc576
ms.sourcegitcommit: b9c6ad79d05feb858f818b37ce5c344f90cc6eb7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/08/2021
ms.locfileid: "5137939"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10017-april-2021"></a><span data-ttu-id="2d1ee-103">ตัวอย่าง Dynamics 365 Supply Chain Management 10.0.17 (เมษายน 2021)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-103">Preview of Dynamics 365 Supply Chain Management 10.0.17 (April 2021)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="2d1ee-104">หัวข้อนี้แสดงรายการคุณลักษณะที่ใหม่ หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ในพรีวิว Microsoft Dynamics 365 Supply Chain Management ของรุ่น 10.0.17</span><span class="sxs-lookup"><span data-stu-id="2d1ee-104">This topic lists features that are either new or changed in the Microsoft Dynamics 365 Supply Chain Management preview of version 10.0.17.</span></span> <span data-ttu-id="2d1ee-105">รุ่นนี้มีหมายเลขการสร้างเป็น 10.0.761 และพร้อมใช้งานดังนี้:</span><span class="sxs-lookup"><span data-stu-id="2d1ee-105">This version has a build number of 10.0.761 and is available as follows:</span></span>

- <span data-ttu-id="2d1ee-106">**ตัวอย่างการนำออกใช้:** กุมภาพันธ์ 2021</span><span class="sxs-lookup"><span data-stu-id="2d1ee-106">**Preview of release:** February 2021</span></span>
- <span data-ttu-id="2d1ee-107">**ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตเอง):** มีนาคม 2021</span><span class="sxs-lookup"><span data-stu-id="2d1ee-107">**General availability of release (self-update):** March 2021</span></span>
- <span data-ttu-id="2d1ee-108">**ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตอัตโนมัติ):** เมษายน 2021</span><span class="sxs-lookup"><span data-stu-id="2d1ee-108">**General availability of release (auto-update):** April 2021</span></span>

## <a name="features-included-in-this-release"></a><span data-ttu-id="2d1ee-109">คุณลักษณะที่รวมอยู่ในการนำออกใช้นี้</span><span class="sxs-lookup"><span data-stu-id="2d1ee-109">Features included in this release</span></span>

<span data-ttu-id="2d1ee-110">คุณลักษณะต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้</span><span class="sxs-lookup"><span data-stu-id="2d1ee-110">The following features are included in this release.</span></span> <span data-ttu-id="2d1ee-111">คุณลักษณะที่แสดงรายการบางอย่างยังคงอยู่ในพรีวิว ในขณะที่บางรายการอาจพร้อมใช้งานโดยทั่วไปอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="2d1ee-111">Some of the listed features are still in preview, while others may already be generally available.</span></span> <span data-ttu-id="2d1ee-112">ไปตามลิงก์ [แผนนำออกใช้](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) เพื่อดูวันที่นำออกใช้อย่างเป็นทางการสำหรับแต่ละคุณลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="2d1ee-112">Follow the links to the [release plan](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) to see the official release dates for each feature.</span></span>

- [<span data-ttu-id="2d1ee-113">ใช้กฎสำหรับการจัดกลุ่มใบสั่งงาน ในขณะที่รันแผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="2d1ee-113">Apply rules for grouping work orders while running a maintenance plan</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/apply-rules-grouping-work-orders-while-running-maintenance-plan)<br> <span data-ttu-id="2d1ee-114">- สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสร้างใบสั่งบริการ ให้ดูที่ [การสร้างใบสั่งงาน](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-114">- For more information, see [Creating work orders](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md).</span></span>

<!-- KFM: Blocked for now. Dana will followup.
- [Approve and save vendor-submitted bank details](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) 
-->

- <span data-ttu-id="2d1ee-115">ความสามารถในการจัดการสินทรัพย์ในอินเทอร์เฟสการดำเนินการผลิต</span><span class="sxs-lookup"><span data-stu-id="2d1ee-115">Asset management capabilities in the production floor execution interface</span></span><br> <span data-ttu-id="2d1ee-116">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ผู้ปฏิบัติงานจะใช้อินเทอร์เฟสการดำเนินการผลิตอย่างไร](../production-control/production-floor-execution-use.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-116">- For more information, see [How workers use the production floor execution interface](../production-control/production-floor-execution-use.md).</span></span>  <!-- KFM: Not yet published on release plan, but is ready. Should be in the next publish. -->

- [<span data-ttu-id="2d1ee-117">เรียกเก็บเงินจากลูกค้าเพื่องานการบํารุงรักษา</span><span class="sxs-lookup"><span data-stu-id="2d1ee-117">Bill customers for maintenance work</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/bill-customers-maintenance-work)<br> <span data-ttu-id="2d1ee-118">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ใบเรียกเก็บเงินการบํารุงรักษาสินทรัพย์ที่ลูกค้าเป็นเจ้าของ](../asset-management/integration-to-project-management-and-accounting/customer-billing.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-118">- For more information, see [Bill for maintenance on customer-owned assets](../asset-management/integration-to-project-management-and-accounting/customer-billing.md).</span></span>

- [<span data-ttu-id="2d1ee-119">การสนับสนุนกรอบเวลาความครอบคลุมเพื่อการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="2d1ee-119">Coverage time fence support for Planning Optimization</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/coverage-time-fence-support-planning-optimization)<br> <span data-ttu-id="2d1ee-120">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [กรอบเวลาความครอบคลุม](../master-planning/planning-optimization/coverage-time-fence.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-120">- For more information, see [Coverage time fences](../master-planning/planning-optimization/coverage-time-fence.md).</span></span>

- [<span data-ttu-id="2d1ee-121">เปิดใช้งานการจัดการการเปลี่ยนแปลงในผลิตภัณฑ์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="2d1ee-121">Enable change management on existing products</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enable-change-management-existing-products)

<!-- KFM: Add this when the feature appears in release plan at next update:
- Enterprise-scale inventory performance improvements and archiving  -->

- [<span data-ttu-id="2d1ee-122">ต้นทุนแฝง</span><span class="sxs-lookup"><span data-stu-id="2d1ee-122">Landed cost</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/landed-cost)

- [<span data-ttu-id="2d1ee-123">การดำเนินการผลิตด้วยสเกลยูนิตในระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="2d1ee-123">Manufacturing execution with scale units in the cloud</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-scale-units-cloud)<br> <span data-ttu-id="2d1ee-124">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ปริมาณงานในการจัดการการผลิตสำหรับสเกลยูนิตในระบบคลาวด์และ Edge](../cloud-edge/cloud-edge-workload-manufacturing.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-124">- For more information, see [Manufacturing execution workloads for cloud and edge scale units](../cloud-edge/cloud-edge-workload-manufacturing.md).</span></span>

- [<span data-ttu-id="2d1ee-125">การจัดการวัสดุ/ Warehouse Automation</span><span class="sxs-lookup"><span data-stu-id="2d1ee-125">Material handling/warehouse automation</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/material-handlingwarehouse-automation) <!-- KFM: Update RP link when the new one goes live -->

- [<span data-ttu-id="2d1ee-126">การจัดส่งเทียบกับมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="2d1ee-126">Packing vs. storage dimensions</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/packing-vs.-storage-dimensions)<br> <span data-ttu-id="2d1ee-127">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่ามิติต่าง ๆ ของการบรรจุและการจัดเก็บ](../warehousing/packing-vs-storage-dimensions.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-127">- For more information, see [Set different dimensions for packing and storage](../warehousing/packing-vs-storage-dimensions.md)</span></span>

- <span data-ttu-id="2d1ee-128">แทนที่หลักการจองเริ่มต้นของวัสดุในการผลิต</span><span class="sxs-lookup"><span data-stu-id="2d1ee-128">Override the default reservation principle for materials in production</span></span><br> <span data-ttu-id="2d1ee-129">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [แทนที่หลักการจองเริ่มต้นของวัสดุในการผลิต](../production-control/override-default-reservation-principle.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-129">- For more information, see [Override the default reservation principle for materials in production](../production-control/override-default-reservation-principle.md).</span></span> <!-- KFM: Not yet published on release plan, but is ready. Should be in the next publish. -->

- [<span data-ttu-id="2d1ee-130">วางแผนการบํารุงรักษาตามค่าตัวนับสินทรัพย์สะสม</span><span class="sxs-lookup"><span data-stu-id="2d1ee-130">Plan maintenance based on accumulated asset counter values</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/plan-maintenance-based-accumulated-asset-counter-values)<br> <span data-ttu-id="2d1ee-131">- สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [แผนการบำรุงรักษา](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-131">- For more information, see [Maintenance plans](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md).</span></span>

- [<span data-ttu-id="2d1ee-132">การสนับสนุนใบขอซื้อสำหรับการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="2d1ee-132">Purchase requisition support for Planning Optimization</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/purchase-requisition-support-planning-optimization)<br> <span data-ttu-id="2d1ee-133">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ใบขอซื้อ](../master-planning/planning-optimization/purchase-requisitions.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-133">- For more information, see [Purchase requisitions](../master-planning/planning-optimization/purchase-requisitions.md).</span></span>

- [<span data-ttu-id="2d1ee-134">มุมมองที่บันทึกไว้ของสินค้าคงคลังและโลจิสติกส์</span><span class="sxs-lookup"><span data-stu-id="2d1ee-134">Saved views for inventory and logistics</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-inventory-logistics)<br> <span data-ttu-id="2d1ee-135">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [มุมมองที่บันทึกไว้แบบมาตรฐานของ Supply Chain Management](saved-views-scm.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-135">- For more information, see [Standard saved views for Supply Chain Management](saved-views-scm.md).</span></span>

- [<span data-ttu-id="2d1ee-136">มุมมองที่บันทึกไว้สำหรับแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2d1ee-136">Saved views for planned orders</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-planned-orders)<br> <span data-ttu-id="2d1ee-137">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [มุมมองที่บันทึกไว้แบบมาตรฐานของ Supply Chain Management](saved-views-scm.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-137">- For more information, see [Standard saved views for Supply Chain Management](saved-views-scm.md).</span></span>

- [<span data-ttu-id="2d1ee-138">มุมมองที่บันทึกไว้ของการควบคุมการผลิต</span><span class="sxs-lookup"><span data-stu-id="2d1ee-138">Saved views for production control</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-production-control)<br> <span data-ttu-id="2d1ee-139">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [มุมมองที่บันทึกไว้แบบมาตรฐานของ Supply Chain Management](saved-views-scm.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-139">- For more information, see [Standard saved views for Supply Chain Management](saved-views-scm.md).</span></span>

- [<span data-ttu-id="2d1ee-140">จัดกำหนดการการสร้างงานของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="2d1ee-140">Schedule warehouse work creation</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-warehouse-work-creation)<br> <span data-ttu-id="2d1ee-141">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [จัดกำหนดการการสร้างงานระหว่างเวฟ](../warehousing/configure-wave-schedule-work-creation.md)ฟ</span><span class="sxs-lookup"><span data-stu-id="2d1ee-141">- For more information, see [Schedule work creation during wave](../warehousing/configure-wave-schedule-work-creation.md).</span></span>

- [<span data-ttu-id="2d1ee-142">ตั้งค่ามิติทางการเงินเริ่มต้นในใบสำคัญการประเมินค่าต้นทุนแบบมาตรฐานใหม่ของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2d1ee-142">Set default financial dimensions for inventory standard cost revaluation vouchers</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/set-default-financial-dimensions-inventory-standard-cost-revaluation-vouchers)<br> <span data-ttu-id="2d1ee-143">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [จัดการการอัปเดตต้นทุนมาตรฐาน](../cost-management/manage-standard-cost-updates.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-143">- For more information, see [Manage standard cost updates](../cost-management/manage-standard-cost-updates.md).</span></span>

- [<span data-ttu-id="2d1ee-144">การจัดส่งพัสดุขนาดเล็ก (SPS)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-144">Small parcel shipping (SPS)</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/small-package-shipping-sps)<br> <span data-ttu-id="2d1ee-145">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การจัดส่งพัสดุขนาดเล็ก](../warehousing/small-parcel-shipping.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-145">- For more information, see [Small parcel shipping](../warehousing/small-parcel-shipping.md).</span></span> <!-- KFM: Update RP link when the new one goes live -->

- [<span data-ttu-id="2d1ee-146">การดำเนินการคลังสินค้าด้วยสเกลยูนิตในระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="2d1ee-146">Warehouse execution with scale units in the cloud</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-scale-units-cloud)<br> <span data-ttu-id="2d1ee-147">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ปริมาณงานการจัดการคลังสินค้าสำหรับสเกลยูนิตในระบบคลาวด์และ Edge](../cloud-edge/cloud-edge-workload-warehousing.md) และ [ใบสั่งคลังสินค้าสำหรับ scale unit ของระบบคลาวด์และ Edge](../cloud-edge/cloud-edge-warehouse-order.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-147">- For more information, see [Warehouse management workloads for cloud and edge scale units](../cloud-edge/cloud-edge-workload-warehousing.md) and [Warehouse orders for cloud and edge scale units](../cloud-edge/cloud-edge-warehouse-order.md).</span></span>

- [<span data-ttu-id="2d1ee-148">แอปพลิเคชันการจัดการคลังสินค้าบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="2d1ee-148">Warehouse management mobile application</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application)<br> <span data-ttu-id="2d1ee-149">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ติดตั้งและเชื่อมต่อแอปการจัดการคลังสินค้า](../warehousing/install-configure-warehouse-management-app.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-149">- For more information, see [Install and connect the Warehouse Management app](../warehousing/install-configure-warehouse-management-app.md).</span></span>

<span data-ttu-id="2d1ee-150">คุณลักษณะเหล่านี้ส่วนใหญ่ต้องถูกเปิดใช้งานโดยใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ก่อนที่คุณจะสามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="2d1ee-150">Most of these features must be enabled using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) before you can use them.</span></span>

## <a name="new-and-updated-documentation-resources"></a><span data-ttu-id="2d1ee-151">ทรัพยากรคู่มือใหม่และคู่มือที่มีการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="2d1ee-151">New and updated documentation resources</span></span>

<span data-ttu-id="2d1ee-152">เมื่อเร็ว ๆ นี้เรามีการเพิ่มหรืออัพเดตส่วนความช่วยเหลือต่อไปนี้อย่างมาก</span><span class="sxs-lookup"><span data-stu-id="2d1ee-152">We have recently added or significantly updated the following help topics.</span></span> <span data-ttu-id="2d1ee-153">ไม่จำเป็นต้องมีความเกี่ยวข้องกับลักษณะการทำงานใหม่ที่เพิ่มสำหรับรุ่นนี้ ตามที่แสดงรายการไว้ในส่วนก่อนหน้านี้ แต่อาจช่วยให้คุณสามารถเพิ่มเติมจากลักษณะการทำงานที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="2d1ee-153">They aren't necessarily related to the new features added for this release, as listed in the previous section, but they may help you to get more out of existing features.</span></span>

- [<span data-ttu-id="2d1ee-154">ตั้งค่าคอนฟิกตัวกรองผลิตภัณฑ์ในธุรกรรมคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="2d1ee-154">Configure product filters for warehouse transactions</span></span>](../warehousing/filters-and-filter-codes.md)

- [<span data-ttu-id="2d1ee-155">ออกแบบอินเทอร์เฟสการดำเนินการผลิต</span><span class="sxs-lookup"><span data-stu-id="2d1ee-155">Design the production floor execution interface</span></span>](../production-control/production-floor-execution-tabs.md)

- [<span data-ttu-id="2d1ee-156">การวางแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="2d1ee-156">Intercompany planning</span></span>](../master-planning/planning-optimization/Intercompany-planning.md)

- [<span data-ttu-id="2d1ee-157">การทำเครื่องหมายสินค้าคงคลังด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="2d1ee-157">Inventory marking with Planning Optimization</span></span>](../master-planning/planning-optimization/marking.md)

- [<span data-ttu-id="2d1ee-158">การวางแผนหลักที่มีการคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="2d1ee-158">Master planning with demand forecasts</span></span>](../master-planning/planning-optimization/demand-forecast.md)

- [<span data-ttu-id="2d1ee-159">การตรวจนับตามรอบของสถานที่บางส่วน</span><span class="sxs-lookup"><span data-stu-id="2d1ee-159">Partial location cycle counting</span></span>](../warehousing/partial-location-cycle-counting.md)

- [<span data-ttu-id="2d1ee-160">การจัดกลุ่มรายการการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2d1ee-160">Pick line grouping</span></span>](../warehousing/pick-line-grouping.md)

- [<span data-ttu-id="2d1ee-161">การวางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="2d1ee-161">Production planning</span></span>](../master-planning/planning-optimization/production-planning.md) <!--KFM: Remember to add YouTube link to this topic -->

- [<span data-ttu-id="2d1ee-162">ใบขอซื้อในการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="2d1ee-162">Purchase requisitions in master planning</span></span>](../master-planning/planning-optimization/purchase-requisitions.md)

- [<span data-ttu-id="2d1ee-163">ตั้งค่าพื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="2d1ee-163">Set up the Asset management mobile workspace</span></span>](../asset-management/set-up-asset-management-mobile.md)

- [<span data-ttu-id="2d1ee-164">แก้ไขปัญหาการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2d1ee-164">Troubleshoot cost management</span></span>](../cost-management/troubleshoot-costmanagement.md)

- [<span data-ttu-id="2d1ee-165">แก้ไขปัญหาการดําเนินงานสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2d1ee-165">Troubleshoot inventory operations</span></span>](../inventory/troubleshoot-inventory-operations.md)

- [<span data-ttu-id="2d1ee-166">การแบ่งช่วงเวลาของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="2d1ee-166">Warehouse slotting</span></span>](../warehousing/warehouse-slotting.md)

## <a name="additional-resources"></a><span data-ttu-id="2d1ee-167">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2d1ee-167">Additional resources</span></span>

### <a name="platform-updates-for-finance-and-operations-apps"></a><span data-ttu-id="2d1ee-168">Platform update สำหรับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2d1ee-168">Platform updates for Finance and Operations apps</span></span>

<span data-ttu-id="2d1ee-169">Microsoft Dynamics 365 Supply Chain Management 10.0.17 รวมถึง Platform update</span><span class="sxs-lookup"><span data-stu-id="2d1ee-169">Microsoft Dynamics 365 Supply Chain Management 10.0.17 includes platform updates.</span></span> <span data-ttu-id="2d1ee-170">เมื่อต้องการเรียนรู้เพิ่มเติม ให้ดูที่ [Platform update สำหรับรุ่น10.0.17 ของแอป Finance and Operations (เมษายน 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-170">To learn more, see [Platform updates for version 10.0.17 of Finance and Operations apps (April 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md).</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2d1ee-171">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="2d1ee-171">Bug fixes</span></span>

<span data-ttu-id="2d1ee-172">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขบักที่รวมอยู่ในการอัปเดตแต่ละรายการที่เป็นส่วนหนึ่งของ 10.0.17 ให้ลงชื่อเข้าใช้ Lifecycle Services (LCS) และดู [บทความ KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=551039&dbType=3&qc=91219e7c3fc585acb17b810c915c3cbea499403538520c40e54de43a53aea6a8)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-172">For information about the bug fixes included in each of the updates that are part of 10.0.17, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=551039&dbType=3&qc=91219e7c3fc585acb17b810c915c3cbea499403538520c40e54de43a53aea6a8).</span></span>

### <a name="dynamics-365-2021-release-wave-1-plan"></a><span data-ttu-id="2d1ee-173">Dynamics 365: 2021 แผนเวฟการนำออกใช้ 1</span><span class="sxs-lookup"><span data-stu-id="2d1ee-173">Dynamics 365: 2021 release wave 1 plan</span></span>

<span data-ttu-id="2d1ee-174">สงสัยเกี่ยวกับความสามารถที่กำลังจะเกิดขึ้นและที่เผยแพร่เมื่อเร็วๆ นี้ในแอปหรือแพลตฟอร์มทางธุรกิจใดๆ ของเราใช่ไหม</span><span class="sxs-lookup"><span data-stu-id="2d1ee-174">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="2d1ee-175">ตรวจสอบ [Dynamics 365: 2021 แผนเวฟการนำออกใช้ 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/)</span><span class="sxs-lookup"><span data-stu-id="2d1ee-175">Check out the [Dynamics 365: 2021 release wave 1 plan](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/).</span></span> <span data-ttu-id="2d1ee-176">เราได้บันทึกทุกรายละเอียดอย่างครอบคลุมตั้งแต่ต้นจนจบในเอกสารเดียวที่คุณสามารถใช้สำหรับการวางแผนได้</span><span class="sxs-lookup"><span data-stu-id="2d1ee-176">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="2d1ee-177">คุณลักษณะ Supply Chain Management ที่ถูกลบและที่ถูกยกเลิกการใช้</span><span class="sxs-lookup"><span data-stu-id="2d1ee-177">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="2d1ee-178">หัวข้อ [คุณลักษณะที่ถูกลบและที่ถูกยกเลิกการใช้ใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) จะอธิบายถึงคุณลักษณะที่ได้รับหรือถูกจัดกำหนดการให้ถูกลบหรือถูกยกเลิกการใช้สำหรับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2d1ee-178">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="2d1ee-179">คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="2d1ee-179">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="2d1ee-180">คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต</span><span class="sxs-lookup"><span data-stu-id="2d1ee-180">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="2d1ee-181">ก่อนที่คุณลักษณะใดๆ จะถูกลบออกจากผลิตภัณฑ์ จะมีการประกาศการแจ้งเตือนการยกเลิกการใช้ในหัวข้อ [คุณลักษณะที่ถูกลบหรือที่ถูกเลิกใช้งานใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 เดือนก่อนการลบ</span><span class="sxs-lookup"><span data-stu-id="2d1ee-181">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="2d1ee-182">สำหรับการจำแนกการเปลี่ยนแปลงที่มีผลกระทบเฉพาะต่อเวลาการคอมไพล์ แต่เป็นไบนารีที่เข้ากันได้กับสภาพแวดล้อม sandbox และสภาพแวดล้อมการผลิต เวลาในการยกเลิกการใช้จะน้อยกว่า 12 เดือน</span><span class="sxs-lookup"><span data-stu-id="2d1ee-182">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="2d1ee-183">โดยทั่วไป รายการเหล่านี้คือการอัปเดตการทำงานที่จำเป็นต้องทำกับคอมไพเลอร์</span><span class="sxs-lookup"><span data-stu-id="2d1ee-183">Typically, these are functional updates that need to be made to the compiler.</span></span>
