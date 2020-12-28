---
title: ภาพรวมของการรวมเข้ากับ Microsoft Dynamics 365 Field Service
description: หัวข้อนี้แสดงภาพรวมของการรวมกับ Microsoft Dynamics 365 Field Service
author: ChristianRytt
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 18eef310470cafd9d59bb1c848bbaeb8bf5b9fa1
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528910"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a><span data-ttu-id="7f5b2-103">ภาพรวมของการรวมเข้ากับ Microsoft Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="7f5b2-103">Integration with Microsoft Dynamics 365 Field Service overview</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7f5b2-104">Supply Chain Management ทำให้เกิดการซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Dynamics 365 Supply Chain Management และ Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="7f5b2-104">Supply Chain Management enables synchronization of business processes between Dynamics 365 Supply Chain Management and Dynamics 365 Field Service.</span></span> <span data-ttu-id="7f5b2-105">สถานการณ์จำลองของการรวมถูกตั้งค่าคอนฟิกโดยใช้เท็มเพลตตัวรวมข้อมูลที่ขยายได้ และ Common Data Service เพื่อเปิดใช้งานการซิงโครไนส์ของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="7f5b2-105">The integration scenarios are configured by using extensible Data integrator templates and Common Data Service to enable the synchronization of business processes.</span></span>
<span data-ttu-id="7f5b2-106">เท็มเพลตมาตรฐานสามารถใช้เพื่อสร้างโครงการที่มีการรวมแบบกำหนดเอง ที่ซึ่งฟิลด์มาตรฐานและแบบกำหนดเองเพิ่มเติมและเอนทิตี สามารถถูกแม็ปเพื่อปรับปรุงการรวม และให้ตรงตามความต้องการทางธุรกิจเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="7f5b2-106">Standard templates can be used to create custom integration projects, where additional standard and custom fields and entities can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="7f5b2-107">สร้างการรวมบริการฟิลด์ด้านบนสุดฟังก์ชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="7f5b2-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/field-service-integration.png)

<span data-ttu-id="7f5b2-109">เฟสแรกของการรวมระหว่าง Field Service และ Supply Chain Management จะเน้นบนการเปิดใช้งานใบสั่งผลิตและข้อตกลงใน Field Service ที่จะถูกจัดทำใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7f5b2-109">The first phase  of the integration between Field Service and Supply Chain Management is focused on enabling work orders and agreements in Field Service to be invoiced in Supply Chain Management.</span></span> <span data-ttu-id="7f5b2-110">ขั้นตอนที่ได้รับการสนับสนุนเริ่มต้นใน Field Service ซึ่งข้อมูลจากใบสั่งผลิตจะถูกซิงโครไนส์ไปยัง Supply Chain Management ในรูปแบบของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7f5b2-110">The supported flow starts in Field Service, where information from work orders is synchronized to Supply Chain Management as sales orders.</span></span> <span data-ttu-id="7f5b2-111">ใน Supply Chain Management ใบสั่งขายจะถูกจัดทำขึ้นเพื่อสร้างเอกสารใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="7f5b2-111">In Supply Chain Management, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="7f5b2-112">นอกจากนี้ ข้อมูลในใบแจ้งหนี้ตามข้อตกลงของ Field Service จะซิงโครไนส์ไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7f5b2-112">In addition, the information from Field Service agreement invoices is synchronized to Supply Chain Management.</span></span> <span data-ttu-id="7f5b2-113">ตัวรวมข้อมูล Microsoft Dynamics 365 ซิงโครไนส์ข้อมูลโดยใช้โครงการที่กำหนดเองได้</span><span class="sxs-lookup"><span data-stu-id="7f5b2-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="7f5b2-114">เท็มเพลตมาตรฐานสามารถใช้เพื่อสร้างโครงการที่มีการรวมแบบกำหนดเอง ที่ซึ่งฟิลด์มาตรฐานและแบบกำหนดเองเพิ่มเติม และรวมทั้งเอนทิตี สามารถถูกแม็ปเพื่อปรับปรุงการรวม และให้ตรงตามข้อกำหนดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="7f5b2-114">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="7f5b2-115">เฟสแรกของการรวมระหว่าง Field Service และ Supply Chain Management ทำให้สามารถซิงโครไนส์รายการดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f5b2-115">The first phase of the integration between Field Service and Supply Chain Management enables synchronization of the following items:</span></span>

- [<span data-ttu-id="7f5b2-116">การซิงโครไนส์ผลิตภัณฑ์จาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Field Service</span><span class="sxs-lookup"><span data-stu-id="7f5b2-116">Synchronize products in Supply Chain Management to products in Field Service</span></span>](field-service-product.md)
- [<span data-ttu-id="7f5b2-117">ซิงโครไนส์ใบสั่งงานใน Field Service กับใบสั่งขายเข้าด้วยกันใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7f5b2-117">Synchronize work orders in Field Service to sales orders in Supply Chain Management</span></span>](field-service-work-order.md)
- [<span data-ttu-id="7f5b2-118">การซิงโครไนส์ข้อตกลงของใบแจ้งหนี้ใน Field Service ไปยังใบแจ้งหนี้ข้อความอิสระใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7f5b2-118">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>](field-service-invoice.md)

<span data-ttu-id="7f5b2-119">เพื่อดูตัวอย่างของวิธีการซิงโครไนส์ใบสั่งงานระหว่าง Field Service และ Supply Chain Management ดูวิดีโอ YouTube แบบย่อ [วิธีการซิงโครไนส์ใบสั่งงานกับการรวม Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo)</span><span class="sxs-lookup"><span data-stu-id="7f5b2-119">To see an example of how you can synchronize a work order between Field Service and Supply Chain Management, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="integration-with-field-service-including-inventory-and-project-information"></a><span data-ttu-id="7f5b2-120">การรวมกับ Field Service รวมถึงสินค้าคงคลังและข้อมูลโครงการ</span><span class="sxs-lookup"><span data-stu-id="7f5b2-120">Integration with Field Service, including inventory and project information</span></span>

<span data-ttu-id="7f5b2-121">ฟังก์ชันเพิ่มเติมในเฟสที่สองนี้ เน้นไปที่การให้ข้อมูลเชิงลึกแก่ช่างเทคนิคภาคสนามเกี่ยวกับข้อมูลสินค้าคงคลังจาก Supply Chain Management โดยยินยอมให้ช่างเทคนิคทำการปรับปรุงระดับสินค้าคงคลังและทำการโอนย้ายวัสดุได้</span><span class="sxs-lookup"><span data-stu-id="7f5b2-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Supply Chain Management, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="7f5b2-122">นอกจากนี้ บริษัทที่ติดตั้งหรือให้บริการซ่อมบำรุงสินค้าที่ขายไปแล้วจะได้รับประโยชน์จากการควบคุมที่ดีขึ้นและการมองเห็นการขายและกระบวนการบริการทั้งหมดพร้อมกับการรวมจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="7f5b2-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="7f5b2-123">ฟังก์ชันประกอบด้วยการรวมของ:</span><span class="sxs-lookup"><span data-stu-id="7f5b2-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="7f5b2-124">ข้อมูลคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7f5b2-124">Warehouse information</span></span>
- <span data-ttu-id="7f5b2-125">ข้อมูลปริมาณสินค้าคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="7f5b2-125">On-hand inventory information</span></span>
- <span data-ttu-id="7f5b2-126">การโอนย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7f5b2-126">Inventory transfers</span></span>
- <span data-ttu-id="7f5b2-127">การปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7f5b2-127">Inventory adjustments</span></span>
- <span data-ttu-id="7f5b2-128">Supply Chain Management ที่เชื่อมโยงกับใบสั่งงานของ Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="7f5b2-128">Supply Chain Management projects connected with Dynamics 365 Field Service work orders</span></span>
- <span data-ttu-id="7f5b2-129">ใบสั่งงานของ Dynamics 365 Field Service ที่มีลิงค์ไปยังโครงการ Supply Chain Management นำหมายเลขโครงการนี้ไปใช้กับใบสั่งขาย เพื่ออนุญาตให้มีการจัดทำใบแจ้งหนี้จากโครงการ</span><span class="sxs-lookup"><span data-stu-id="7f5b2-129">Dynamics 365 Field Service work orders with link to Supply Chain Management projects, apply this project number to the sales order to allow invoicing from the project.</span></span> 

![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="7f5b2-131">เฟสที่สองของการรวมระหว่าง Field Service และ Supply Chain Management สามารถซิงโครไนส์กับเท็มเพลตดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f5b2-131">The second phase of the integration between Field Service and Supply Chain Management enables synchronization with the following templates:</span></span>
- <span data-ttu-id="7f5b2-132">คลังสินค้า (Supply Chain Management ไปยัง Field Service) - คลังสินค้าจาก Supply Chain Management ไปยัง Field Service [การสอบถามขั้นสูง]</span><span class="sxs-lookup"><span data-stu-id="7f5b2-132">Warehouses (Supply Chain Management to Field Service) - Warehouses from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="7f5b2-133">สินค้าคงคลังของผลิตภัณฑ์ (Supply Chain Management ไปยัง Field Service) - ข้อมูลระดับสินค้าคงคลังจาก Supply Chain Management ไปยัง Field Service [การสอบถามขั้นสูง]</span><span class="sxs-lookup"><span data-stu-id="7f5b2-133">Product Inventory (Supply Chain Management to Field Service) - Inventory level information from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="7f5b2-134">การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Supply Chain Management) - การปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Supply Chain Management  [การสอบถามขั้นสูง]</span><span class="sxs-lookup"><span data-stu-id="7f5b2-134">Inventory Adjustment (Field Service to Supply Chain Management) - Inventory adjustments from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="7f5b2-135">การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Supply Chain Management) - การปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Supply Chain Management [การสอบถามขั้นสูง]</span><span class="sxs-lookup"><span data-stu-id="7f5b2-135">Inventory Transfers (Field Service to Supply Chain Management) - Inventory transfers from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="7f5b2-136">คลังสินค้า (Supply Chain Management to Field Service) - รายชื่อโครงการจาก Supply Chain Management to Field Service [การจัดการขั้นสูง]</span><span class="sxs-lookup"><span data-stu-id="7f5b2-136">Projects (Supply Chain Management to Field Service) - Project list from Supply Chain Management to Field Service</span></span> 
- <span data-ttu-id="7f5b2-137">ใบสั่งงานพร้อมกับโครงการ (Field Service ไปยัง Supply Chain Management) - ใบสั่งงานใน Field Service ไปยังใบสั่งขายใน Supply Chain Management ที่มีการสนับสนุนสำหรับโครงการ [การสอบถามขั้นสูง]</span><span class="sxs-lookup"><span data-stu-id="7f5b2-137">Work Orders with Project (Field Service to Supply Chain Management) - Work orders in Field Service to Sales orders  in Supply Chain Management, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="7f5b2-138">ผลิตภัณฑ์ของ Field Service ที่มีหน่วยสินค้าคงคลัง (Supply Chain Management ไปยัง Sales) - รายการ 'ผลิตภัณฑ์ที่สามารถนำออกไปขายได้' ใน Supply Chain Management ไปยัง รายการ 'ผลิตภัณฑ์' ที่จะขายใน Field Service รวมถึงหน่วยสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7f5b2-138">Field Service Products with Inventory unit (Supply Chain Management to Sales) - Supply Chain Management 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements"></a><span data-ttu-id="7f5b2-139">ความต้องการของระบบ</span><span class="sxs-lookup"><span data-stu-id="7f5b2-139">System requirements</span></span>

### <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="7f5b2-140">ระบบต้องใช้กับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7f5b2-140">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="7f5b2-141">การรวม Field Service สนับสนุนเวอร์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f5b2-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="7f5b2-142">Dynamics 365 for Finance and Operations รุ่น 8.1.2 (ธันวาคม 2018) ที่เริ่มใช้ในเดือนธันวาคม 2018 และมีหมายเลขผลิตของแอพพลิเคชัน 8.1.195 ที่มี Platform Update 22 (7.0.5095)</span><span class="sxs-lookup"><span data-stu-id="7f5b2-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2018) was released in December 2018 and has an application build number 8.1.195 with Platform update 22 (7.0.5095).</span></span> 

### <a name="system-requirements-for-field-service"></a><span data-ttu-id="7f5b2-143">ข้อกำหนดของระบบสำหรับ Field Service</span><span class="sxs-lookup"><span data-stu-id="7f5b2-143">System requirements for Field Service</span></span>
<span data-ttu-id="7f5b2-144">เมื่อต้องการใช้โซลูชันการรวม Field Service คุณต้องติดตั้งส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f5b2-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="7f5b2-145">Field Service (รุ่น 8.2.0.286) หรือรุ่นที่ใหม่กว่าใน Dynamics 365 9.1.x - ที่เริ่มใช้ในเดือนพฤศจิกายน 2018</span><span class="sxs-lookup"><span data-stu-id="7f5b2-145">Field Service (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="7f5b2-146">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด (P2C) สำหรับ Dynamics 365 รุ่น 1.15.0.1 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="7f5b2-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="7f5b2-147">โซลูชันนี้มีให้การดาวน์โหลดจาก [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)</span><span class="sxs-lookup"><span data-stu-id="7f5b2-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="7f5b2-148">โซลูชัน 'การรวม Field Service โครงการและสินค้าคงคลัง' สำหรับ Dynamics 365 รุ่น 2.0.0.0 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="7f5b2-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="7f5b2-149">โซลูชันนี้มีให้การดาวน์โหลดจาก [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2)</span><span class="sxs-lookup"><span data-stu-id="7f5b2-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>
