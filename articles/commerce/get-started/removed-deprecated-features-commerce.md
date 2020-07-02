---
title: คุณลักษณะที่เอาออกหรือเลิกสนับสนุนใน Dynamics 365 Commerce
description: หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่ถูกวางแผนไว้สำหรับการลบจาก Dynamics 365 Commerce
author: josaw
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443929"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="70028-103">คุณลักษณะที่เอาออกหรือเลิกสนับสนุนใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="70028-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70028-104">หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่ถูกวางแผนไว้สำหรับการลบจาก Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="70028-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="70028-105">คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="70028-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="70028-106">คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต</span><span class="sxs-lookup"><span data-stu-id="70028-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="70028-107">รายการนี้มีไว้เพื่อช่วยคุณพิจารณาการลบออกและการยกเลิกการใช้งานเหล่านี้สำหรับการวางแผนของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="70028-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="70028-108">ข้อมูลโดยละเอียดเกี่ยวกับออบเจ็กต์ต่างๆ ในแอป Finance and Operations พบได้ใน [รายงานอ้างอิงทางเทคนิค](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)</span><span class="sxs-lookup"><span data-stu-id="70028-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="70028-109">คุณสามารถเปรียบเทียบเวอร์ชันต่างๆ ของรายงานเหล่านี้ เพื่อเรียนรู้เกี่ยวกับออบเจ็กต์ที่เปลี่ยนแปลงหรือถูกลบออกในแต่ละรุ่นของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70028-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a><span data-ttu-id="70028-110">คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Commerce 10.0.11</span><span class="sxs-lookup"><span data-stu-id="70028-110">Features removed or deprecated in the Commerce 10.0.11 release</span></span>
### <a name="data-action-hooks"></a><span data-ttu-id="70028-111">จุดเชื่อมต่อการดำเนินการกับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="70028-111">Data action hooks</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="70028-112">**เหตุผลสำหรับการยกเลิกการใช้/การลบ**</span><span class="sxs-lookup"><span data-stu-id="70028-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="70028-113">จุดเชื่อมต่อการดำเนินการกับข้อมูลไม่ได้รับการสนับสนุน เนื่องจากปัญหาประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="70028-113">The data action hooks feature has been deprecated due to performance issues.</span></span> |
| <span data-ttu-id="70028-114">**แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="70028-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="70028-115">ขอแนะนำให้ใช้ [การแทนที่การดำเนินการกับข้อมูล](../e-commerce-extensibility/data-action-overrides.md) แทน เพื่อแก้ไขตรรกะทางธุรกิจในเลเยอร์การดำเนินการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="70028-115">It is recommended to instead use [data action overrides](../e-commerce-extensibility/data-action-overrides.md) to modify business logic in the data action layer.</span></span>|
| <span data-ttu-id="70028-116">**พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**</span><span class="sxs-lookup"><span data-stu-id="70028-116">**Product areas affected**</span></span>         | <span data-ttu-id="70028-117">การดำเนินการข้อมูลเกี่ยวกับความสามารถในการเพิ่มฟังก์ชันของอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="70028-117">E-Commerce extensibility data actions</span></span> |
| <span data-ttu-id="70028-118">**ตัวเลือกการปรับใช้**</span><span class="sxs-lookup"><span data-stu-id="70028-118">**Deployment option**</span></span>              | <span data-ttu-id="70028-119">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="70028-119">All</span></span> |
| <span data-ttu-id="70028-120">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="70028-120">**Status**</span></span>                         | <span data-ttu-id="70028-121">ไม่สนับสนุน: ณ วันที่ของการนำออกใช้ 10.0.11</span><span class="sxs-lookup"><span data-stu-id="70028-121">Deprecated: As of release 10.0.11</span></span> |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="70028-122">คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Commerce 10.0.10</span><span class="sxs-lookup"><span data-stu-id="70028-122">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="70028-123">การดำเนินการ POS 803 - การเบิกสินค้าและการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="70028-123">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="70028-124">**เหตุผลสำหรับการยกเลิกการใช้/การลบ**</span><span class="sxs-lookup"><span data-stu-id="70028-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="70028-125">การดำเนินการเบิกสินค้าและการรับสินค้าจะถูกยกเลิกการใช้งานเนื่องจากการออกแบบการดำเนินงานใหม่</span><span class="sxs-lookup"><span data-stu-id="70028-125">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="70028-126">**แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="70028-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="70028-127">ใช่</span><span class="sxs-lookup"><span data-stu-id="70028-127">Yes.</span></span> <span data-ttu-id="70028-128">จะถูกแทนที่ด้วยสองการดำเนินงาน POS ใหม่: การดำเนินงานขาเข้า (804) และการดำเนินงานขาออก (805)</span><span class="sxs-lookup"><span data-stu-id="70028-128">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="70028-129">**พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**</span><span class="sxs-lookup"><span data-stu-id="70028-129">**Product areas affected**</span></span>         | <span data-ttu-id="70028-130">ใบสมัครสำหรับการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="70028-130">Point of sale (POS) application</span></span> |
| <span data-ttu-id="70028-131">**ตัวเลือกการปรับใช้**</span><span class="sxs-lookup"><span data-stu-id="70028-131">**Deployment option**</span></span>              | <span data-ttu-id="70028-132">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="70028-132">All</span></span> |
| <span data-ttu-id="70028-133">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="70028-133">**Status**</span></span>                         | <span data-ttu-id="70028-134">ไม่สนับสนุน: เมื่อนำรุ่น 10.0.10 ออกใช้ การดำเนินการเบิกสินค้าและการรับสินค้าจะไม่ได้รับการอัพเดทใดๆ ใหม่อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="70028-134">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="70028-135">การแก้ไขข้อผิดพลาดที่สำคัญเท่านั้นที่จะดำเนินการสำหรับการดำเนินงานนี้ในรุ่นต่อๆ ไป</span><span class="sxs-lookup"><span data-stu-id="70028-135">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="70028-136">ลูกค้าทั้งหมดจะได้รับการสนับสนุนให้ย้ายไปที่ [การดำเนินงานขาเข้าใหม่](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) และ [การดำเนินงานขาออก](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) ซึ่งจะยังคงเป็นส่วนหนึ่งของแผนงานผลิตภัณฑ์ระยะยาวของเรา</span><span class="sxs-lookup"><span data-stu-id="70028-136">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="70028-137">คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Commerce 10.0.7</span><span class="sxs-lookup"><span data-stu-id="70028-137">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="70028-138">API ของ Commerce GetProductAvailabilities และ GetAvailableInventoryNearby</span><span class="sxs-lookup"><span data-stu-id="70028-138">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="70028-139">**เหตุผลสำหรับการยกเลิกการใช้/การลบ**</span><span class="sxs-lookup"><span data-stu-id="70028-139">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="70028-140">API ที่ปรับให้เหมาะสมใหม่ถูกสร้างเพื่อแทนที่ API ของ GetProductAvailabilities และ GetAvailableInventoryNearby</span><span class="sxs-lookup"><span data-stu-id="70028-140">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="70028-141">**แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="70028-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="70028-142">ใช่: ถูกแทนที่ด้วย API ของ GetEstimatedAvailability และ GetEstimatedProductWarehouseAvailability</span><span class="sxs-lookup"><span data-stu-id="70028-142">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="70028-143">**พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**</span><span class="sxs-lookup"><span data-stu-id="70028-143">**Product areas affected**</span></span>         | <span data-ttu-id="70028-144">SDK แอปพลิเคชันอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="70028-144">e-Commerce application SDK</span></span> |
| <span data-ttu-id="70028-145">**ตัวเลือกการปรับใช้**</span><span class="sxs-lookup"><span data-stu-id="70028-145">**Deployment option**</span></span>              | <span data-ttu-id="70028-146">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="70028-146">All</span></span> |
| <span data-ttu-id="70028-147">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="70028-147">**Status**</span></span>                         | <span data-ttu-id="70028-148">ไม่ได้รับการสนับสนุน: รุ่น 10.0.7 ที่นำออกใช้จะไม่มีการลงทุนทางวิศวกรรมที่ทำสำหรับ GetProductAvailabilities และ GetAvailableInventoryNearby</span><span class="sxs-lookup"><span data-stu-id="70028-148">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="70028-149">องค์กรที่ใช้ API เหล่านี้ในการปรับใช้อีคอมเมิร์ซของตนควรแปลงเป็น API ของ GetEstimatedAvailability และ GetEstimatedProductWarehouseAvailability ใหม่ และเปิดใช้งาน [คุณลักษณะการทำงานการคำนวณความพร้อมใช้งานของผลิตภัณฑ์ที่เหมาะสม](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels)</span><span class="sxs-lookup"><span data-stu-id="70028-149">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="70028-150">ประกาศก่อนหน้านี้เกี่ยวกับคุณลักษณะที่ถูกลบหรือเลิกสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="70028-150">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="70028-151">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้ ให้ดูที่ [คุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json)</span><span class="sxs-lookup"><span data-stu-id="70028-151">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
