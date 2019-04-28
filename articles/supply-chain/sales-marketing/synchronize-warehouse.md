---
title: ซิงโครไนส์คลังสินค้าจาก Finance and Operations ไปยัง Field Service
description: หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์คลังสินค้าจาก Microsoft Dynamics 365 for Finance and Operations เป็น Microsoft Dynamics 365 for Field Service
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 7e6d7626c00b9d7d98ce872652653c36ce7bc975
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/14/2019
ms.locfileid: "842544"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="cd886-103">ซิงโครไนส์คลังสินค้าจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="cd886-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cd886-104">หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์คลังสินค้าจาก Microsoft Dynamics 365 for Finance and Operations เป็น Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="cd886-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cd886-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="cd886-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cd886-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="cd886-106">Templates and tasks</span></span>
<span data-ttu-id="cd886-107">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการรันการซิงโครไนส์คลังสินค้าจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="cd886-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cd886-108">**เท็มเพลตในการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cd886-108">**Template in Data integration**</span></span>
- <span data-ttu-id="cd886-109">คลังสินค้า (Fin and Ops ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="cd886-109">Warehouses (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="cd886-110">**งานในโครงการการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cd886-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="cd886-111">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cd886-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="cd886-112">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="cd886-112">Entity set</span></span>
| <span data-ttu-id="cd886-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="cd886-113">Field Service</span></span>    | <span data-ttu-id="cd886-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cd886-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="cd886-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="cd886-115">msdyn_warehouses</span></span> | <span data-ttu-id="cd886-116">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cd886-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="cd886-117">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="cd886-117">Entity flow</span></span>
<span data-ttu-id="cd886-118">คลังสินค้าที่สร้างขึ้นและรักษาไว้ใน Finance and Operations สามารถซิงโครไนส์กับ Field Service ได้ ผ่านทางโครงการรวมข้อมูล Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="cd886-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="cd886-119">อาจมีการควบคุมคลังสินค้าที่คุณต้องการที่ซิงโครไนส์กับ Field Service พร้อมกับแบบสอบถามขั้นสูง และการกรองข้อมูลในโครงการ</span><span class="sxs-lookup"><span data-stu-id="cd886-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="cd886-120">มีการสร้างคลังสินค้าที่ซิงโครไนส์จาก Finance and Operations ใน Field Service กับฟิลด์ **ได้รับการรักษา** ถูกตั้งค่าเป็น **ใช่** ภายนอก และเรกคอร์ดถูกทำให้เป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="cd886-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="cd886-121">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="cd886-121">Field Service CRM solution</span></span>
<span data-ttu-id="cd886-122">เพื่อสนับสนุนการรวมระหว่าง Field Service และ Finance and Operations ต้องมีฟังก์ชันเพิ่มเติมจากโซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="cd886-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="cd886-123">ในโซลูชัน ฟิลด์ **จะเก็บรักษาภายนอก** ได้ถูกเพิ่มไปยังเอนทิตี **คลังสินค้า (msdyn_warehouses)**</span><span class="sxs-lookup"><span data-stu-id="cd886-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="cd886-124">ฟิลด์นี้ช่วยระบุว่ามีจัดการคลังสินค้าจาก Finance and Operations หรือมีเฉพาะใน Field Service</span><span class="sxs-lookup"><span data-stu-id="cd886-124">This field helps to identify if the warehouse is handled from Finance and Operations or if it only exists in Field Service.</span></span> <span data-ttu-id="cd886-125">การตั้งค่าสำหรับฟิลด์นี้รวมถึง:</span><span class="sxs-lookup"><span data-stu-id="cd886-125">The settings for this field include:</span></span>
- <span data-ttu-id="cd886-126">**ใช่** – คลังสินค้าที่สร้างจาก Finance and Operations และจะไม่สามารถแก้ไขได้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="cd886-126">**Yes** – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="cd886-127">**ไม่** – มีการป้อนคลังสินค้าโดยตรงใน Field Service และรักษาไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="cd886-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="cd886-128">ฟิลด์ **รักษาไว้สำหรับภายนอก** ช่วยควบคุมการซิงโครไนส์ของระดับสินค้าคงคลัง การปรับปรุง การโอนย้าย และการใช้บนใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="cd886-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="cd886-129">เฉพาะคลังสินค้าที่มี **รักษาไว้สำหรับภายนอก** ถูกตั้งค่าเป็น **ใช่** สามารถถูกซิงโครไนส์โดยตรงไปยังคลังสินค้าเดียวกันในระบบอื่นๆ ได้</span><span class="sxs-lookup"><span data-stu-id="cd886-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="cd886-130">คุณจะสามารถสร้างคลังสินค้าหลายแห่งใน Field Service ได้ ( **รักษาไว้สำหรับภายนอก = No**) แล้วแมปเข้ากับคลังสินค้าเดียวใน Finance and Operations แบบสอบถามขั้นสูง และการกรองข้อมูลฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="cd886-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="cd886-131">นี่จะถูกใช้ในสถานการณ์ที่คุณต้องการให้ Field service เป็นหลักของระดับสินค้าคงคลังโดยละเอียด และส่งการปรับปรุงไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cd886-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="cd886-132">ในกรณีนี้ Field service จะไม่ได้รับการปรับปรุงระดับสินค้าคงคลังจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cd886-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="cd886-133">สำหรับข้อมูลเพิ่มเติม ดู [ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) และ [ซิงโครไนส์ใบสั่งงานใน Field Service ไปยังใบสั่งขายที่เชื่อมโยงกับโครงการใน Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)</span><span class="sxs-lookup"><span data-stu-id="cd886-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="cd886-134">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="cd886-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="cd886-135">โครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cd886-135">Data Integration project</span></span>
<span data-ttu-id="cd886-136">ก่อนการซิงโครไนส์ของคลังสินค้า ตรวจสอบว่าได้ปรับปรุงการสอบถามขั้นสูง และการกรองข้อมูลโครงการที่จะรวมคลังสินค้าที่คุณต้องการนำมาจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="cd886-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="cd886-137">หมายเหตุว่า คุณจะต้องการคลังสินค้าที่ใน Field Service เพื่อใช้ในใบสั่งงาน การปรับปรุง และการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="cd886-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="cd886-138">เพื่อให้แน่ใจว่ามี **คีย์การรวม** อยู่ สำหรับ **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="cd886-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="cd886-139">ไปยังการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cd886-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="cd886-140">เลือกแท็บ **การตั้งค่าการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="cd886-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="cd886-141">เลือกชุดของการเชื่อมต่อที่ใช้สำหรับการซิงโครไนส์ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="cd886-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="cd886-142">เลือกแท็บ **คีย์การรวม**</span><span class="sxs-lookup"><span data-stu-id="cd886-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="cd886-143">ค้นหา msdyn_workorders และยืนยันว่าคีย์ **msdyn_name (ชื่อ)** ถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="cd886-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="cd886-144">ถ้าไม่แสดงขึ้น ให้เพิ่มโดยการคลิก **เพิ่มคีย์** แล้วคลิก **บันทึก** ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="cd886-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cd886-145">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cd886-145">Template mapping in Data integration</span></span>

<span data-ttu-id="cd886-146">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cd886-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a><span data-ttu-id="cd886-147">คลังสินค้า (Fin and Ops ไปยัง Field Service): คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cd886-147">Warehouses (Fin and Ops to Field Service): Warehouse</span></span>

<span data-ttu-id="cd886-148">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="cd886-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
