---
title: การรวมข้อมูลกับภาพรวมของ Microsoft Dynamics 365 for Field Service
description: หัวข้อนี้แสดงภาพรวมของการรวมกับ Microsoft Dynamics 365 for Field Service
author: ChristianRytt
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 22abe83f06b7fc57c73fb82ccafc4b426667e7c6
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865219"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service-overview"></a><span data-ttu-id="3b8b8-103">การรวมข้อมูลกับภาพรวมของ Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="3b8b8-103">Integration with Microsoft Dynamics 365 for Field Service overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3b8b8-104">Microsoft Dynamics 365 for Finance and Operations เปิดใช้งานการซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="3b8b8-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="3b8b8-105">สถานการณ์จำลองการรวมถูกตั้งค่าคอนฟิกโดยใช้เท็มเพลตตัวรวมข้อมูลที่ขยายได้ และ Common Data Service (CDS) เพื่อเปิดใช้งานการซิงโครไนส์ของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3b8b8-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>
<span data-ttu-id="3b8b8-106">เท็มเพลตมาตรฐานสามารถใช้เพื่อสร้างโครงการที่มีการรวมแบบกำหนดเอง ที่ซึ่งฟิลด์มาตรฐานและแบบกำหนดเองเพิ่มเติมและเอนทิตี สามารถถูกแม็ปเพื่อปรับปรุงการรวม และให้ตรงตามความต้องการทางธุรกิจเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3b8b8-106">Standard templates can be used to create custom integration projects, where additional standard and custom fields and entities can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="3b8b8-107">สร้างการรวมบริการฟิลด์ด้านบนสุดฟังก์ชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3b8b8-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/field-service-integration.png)

<span data-ttu-id="3b8b8-109">เฟสแรกของการรวมระหว่าง Field Service และ Finance and Operations จะเน้นบนการเปิดใช้งานใบสั่งผลิตและข้อตกลงใน Field Service ให้ออกใบแจ้งหนี้ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3b8b8-109">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="3b8b8-110">ขั้นตอนที่ได้รับการสนับสนุนเริ่มต้นใน Field Service ที่ซึ่งมีการซิงโครไนส์ข้อมูลจากใบสั่งผลิตไปยัง Finance and Operations เป็นใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3b8b8-110">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="3b8b8-111">ใน Finance and Operations ใบสั่งขายออกใบแจ้งหนี้เพื่อสร้างเอกสารใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="3b8b8-111">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="3b8b8-112">นอกจากนี้ ข้อมูลจากใบแจ้งหนี้ของข้อตกลงของ Field Service จะซิงโครไนส์กับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3b8b8-112">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="3b8b8-113">ตัวรวมข้อมูล Microsoft Dynamics 365 ซิงโครไนส์ข้อมูลโดยใช้โครงการที่กำหนดเองได้</span><span class="sxs-lookup"><span data-stu-id="3b8b8-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="3b8b8-114">เท็มเพลตมาตรฐานสามารถใช้เพื่อสร้างโครงการที่มีการรวมแบบกำหนดเอง ที่ซึ่งฟิลด์มาตรฐานและแบบกำหนดเองเพิ่มเติม และรวมทั้งเอนทิตี สามารถถูกแม็ปเพื่อปรับปรุงการรวม และให้ตรงตามข้อกำหนดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3b8b8-114">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="3b8b8-115">เฟสแรกของการรวมระหว่าง Field Service และ Finance and Operations เปิดใช้งานการซิงโครไนส์ของรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3b8b8-115">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="3b8b8-116">ผลิตภัณฑ์ใน Finance and Operations ไปยังผลิตภัณฑ์ใน Field Service ที่รวมข้อมูลชนิดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3b8b8-116">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="3b8b8-117">ใบสั่งผลิตใน Field Service ไปยังใบสั่งขายใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3b8b8-117">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="3b8b8-118">ใบแจ้งหนี้ใน Field Service ไปยังใบแจ้งหนี้ข้อความอิสระใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3b8b8-118">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="3b8b8-119">เมื่อต้องการดูตัวอย่างของวิธีการที่คุณสามารถซิงโครไนส์ใบสั่งงานระหว่าง Field Service และ Finance and Operations ดูวิดีโอ YouTube แบบย่อ [วิธีการซิงโครไนส์ใบสั่งงานกับการรวม Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo)</span><span class="sxs-lookup"><span data-stu-id="3b8b8-119">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a><span data-ttu-id="3b8b8-120">การรวมกับ Microsoft Dynamics 365 for Field Service รวมถึงสินค้าคงคลังและข้อมูลโครงการ</span><span class="sxs-lookup"><span data-stu-id="3b8b8-120">Integration with Microsoft Dynamics 365 for Field Service, including inventory and project information</span></span>

<span data-ttu-id="3b8b8-121">ฟังก์ชันเพิ่มเติมในขั้นตอนที่สองนี้ มุ่งเน้นในการให้ข้อมูลเชิงลึกแก่ช่างเทคนิคภาคสนามเกี่ยวกับข้อมูลสินค้าคงคลังจาก Finance and Operations ซึ่งอนุญาตให้รายการเหล่านั้นปรับปรุงระดับสินค้าคงคลังและทำการโอนย้ายวัสดุ</span><span class="sxs-lookup"><span data-stu-id="3b8b8-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Finance and Operations, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="3b8b8-122">นอกจากนี้ บริษัทที่ติดตั้งหรือให้บริการซ่อมบำรุงสินค้าที่ขายไปแล้วจะได้รับประโยชน์จากการควบคุมที่ดีขึ้นและการมองเห็นการขายและกระบวนการบริการทั้งหมดพร้อมกับการรวมจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="3b8b8-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="3b8b8-123">ฟังก์ชันประกอบด้วยการรวมของ:</span><span class="sxs-lookup"><span data-stu-id="3b8b8-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="3b8b8-124">ข้อมูลคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="3b8b8-124">Warehouse information</span></span>
- <span data-ttu-id="3b8b8-125">ข้อมูลปริมาณสินค้าคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="3b8b8-125">On-hand inventory information</span></span>
- <span data-ttu-id="3b8b8-126">การโอนย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="3b8b8-126">Inventory transfers</span></span>
- <span data-ttu-id="3b8b8-127">การปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="3b8b8-127">Inventory adjustments</span></span>
- <span data-ttu-id="3b8b8-128">โครงการ Dynamics 365 for Finance and Operations ที่เชื่อมโยงกับใบสั่งงาน Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="3b8b8-128">Dynamics 365 for Finance and Operations projects connected with Dynamics 365 for Field Service work orders</span></span>
- <span data-ttu-id="3b8b8-129">ใบสั่งงาน Dynamics 365 for Field Service ที่มีลิงค์ไปยังโครงการ Dynamics 365 for Finance and Operations นำหมายเลขโครงการนี้ไปใช้กับใบสั่งขาย Dynamics 365 for Finance and Operations เพื่ออนุญาตให้มีการออกใบแจ้งหนี้จากโครงการ</span><span class="sxs-lookup"><span data-stu-id="3b8b8-129">Dynamics 365 for Field Service work orders with link to Dynamics 365 for Finance and Operations projects, apply this project number to the Dynamics 365 for Finance and Operations sales order to allow invoicing from the project.</span></span> 

![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="3b8b8-131">เฟสที่สองของการรวมระหว่าง Field Service และ Finance and Operations เปิดใช้งานการซิงโครไนส์ที่มีเท็มเพลตต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3b8b8-131">The second phase of the integration between Field Service and Finance and Operations enables synchronization with the following templates:</span></span>
- <span data-ttu-id="3b8b8-132">คลังสินค้า (Fin and Ops ไปยัง Field Service) - คลังสินค้าจาก Finance and Operations ไปยัง Field Service [การสอบถามขั้นสูง]</span><span class="sxs-lookup"><span data-stu-id="3b8b8-132">Warehouses (Fin and Ops to Field Service) - Warehouses from Finance and Operations to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="3b8b8-133">สินค้าคงคลังของผลิตภัณฑ์ (Fin and Ops ไปยัง Field Service) - ข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service [การสอบถามขั้นสูง]</span><span class="sxs-lookup"><span data-stu-id="3b8b8-133">Product Inventory (Fin and Ops to Field Service) - Inventory level information from Finance and Operations to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="3b8b8-134">การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Fin and Ops) - การปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Finance and Operations [การสอบถามขั้นสูง]</span><span class="sxs-lookup"><span data-stu-id="3b8b8-134">Inventory Adjustment (Field Service to Fin and Ops) - Inventory adjustments from Field Service to Finance and Operations [Advanced Query]</span></span> 
- <span data-ttu-id="3b8b8-135">การโอนย้ายสินค้าคงคลัง (Field Service ไปยัง Fin and Ops) - การโอนย้ายสินค้าคงคลังจาก Field Service ไปยัง Finance and Operations [การสอบถามขั้นสูง]</span><span class="sxs-lookup"><span data-stu-id="3b8b8-135">Inventory Transfers (Field Service to Fin and Ops) - Inventory transfers from Field Service to Finance and Operations [Advanced Query]</span></span> 
- <span data-ttu-id="3b8b8-136">โครงการ (Fin and Ops ไปยัง Field Service) - รายการโครงการจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="3b8b8-136">Projects (Fin and Ops to Field Service) - Project list from Finance and Operations to Field Service</span></span> 
- <span data-ttu-id="3b8b8-137">ใบสั่งงานพร้อมกับโครงการ (Field Service ไปยัง Fin and Ops) - ใบสั่งงานใน Field Service ไปยัง Sales orders ใน Finance and Operations ที่มีการสนับสนุนสำหรับโครงการ [การสอบถามขั้นสูง]</span><span class="sxs-lookup"><span data-stu-id="3b8b8-137">Work Orders with Project (Field Service to Fin and Ops) - Work orders in Field Service to Sales orders  in Finance and Operations, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="3b8b8-138">ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Fin and Ops ไปยัง Sales) - Finance and Operations 'ผลิตภัณฑ์ที่นำออกใช้ที่สามารถขายได้' ไปยัง 'ผลิตภัณฑ์' Sales สำหรับ Field Service ซึ่งรวมถึงหน่วยสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="3b8b8-138">Field Service Products with Inventory unit (Fin and Ops to Sales) - Finance and Operations 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements"></a><span data-ttu-id="3b8b8-139">ความต้องการของระบบ</span><span class="sxs-lookup"><span data-stu-id="3b8b8-139">System requirements</span></span>

### <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="3b8b8-140">ความต้องการของระบบสำหรับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3b8b8-140">System requirements for Finance and Operations</span></span>
<span data-ttu-id="3b8b8-141">การรวม Field Service สนับสนุนเวอร์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3b8b8-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="3b8b8-142">Dynamics 365 for Finance and Operations รุ่น 8.1.2 (ธันวาคม 2018) นำออกใช้ในเดือนธันวาคม 2018 และมีรุ่นของแอพลิเคชันหมายเลข 8.1.195 ที่มี Platform Update 22 (7.0.5095)</span><span class="sxs-lookup"><span data-stu-id="3b8b8-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2018) was released in December 2018 and has an application build number 8.1.195 with Platform Update 22 (7.0.5095).</span></span> 

### <a name="system-requirements-for-field-service"></a><span data-ttu-id="3b8b8-143">ข้อกำหนดของระบบสำหรับ Field Service</span><span class="sxs-lookup"><span data-stu-id="3b8b8-143">System requirements for Field Service</span></span>
<span data-ttu-id="3b8b8-144">เมื่อต้องการใช้โซลูชันการรวม Field Service คุณต้องติดตั้งส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3b8b8-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="3b8b8-145">Field Service for Dynamics 365 (รุ่น 8.2.0.286) หรือรุ่นที่ใหม่กว่าใน Dynamics 365 9.1.x - นำออกใช้ในเดือนพฤศจิกายน 2018</span><span class="sxs-lookup"><span data-stu-id="3b8b8-145">Field Service for Dynamics 365 (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="3b8b8-146">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด (P2C) สำหรับ Dynamics 365 รุ่น 1.15.0.1 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="3b8b8-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="3b8b8-147">โซลูชันนี้มีให้การดาวน์โหลดจาก [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)</span><span class="sxs-lookup"><span data-stu-id="3b8b8-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="3b8b8-148">โซลูชัน 'การรวม Field Service โครงการและสินค้าคงคลัง' สำหรับ Dynamics 365 รุ่น 2.0.0.0 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="3b8b8-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="3b8b8-149">โซลูชันนี้มีให้การดาวน์โหลดจาก [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2)</span><span class="sxs-lookup"><span data-stu-id="3b8b8-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>
