---
title: "ซิงโครไนส์คลังสินค้าจาก Finance and Operations ไปยัง Field Service"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์คลังสินค้าจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service"
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: th-th
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="11d37-103">ซิงโครไนส์คลังสินค้าจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="11d37-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="11d37-104">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์คลังสินค้าจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="11d37-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="11d37-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="11d37-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="11d37-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="11d37-106">Templates and tasks</span></span>
<span data-ttu-id="11d37-107">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการรันการซิงโครไนส์ของคลังสินค้าจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="11d37-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="11d37-108">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="11d37-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="11d37-109">คลังสินค้า (Finance and Operations ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="11d37-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="11d37-110">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="11d37-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="11d37-111">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="11d37-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="11d37-112">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="11d37-112">Entity set</span></span>
| <span data-ttu-id="11d37-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="11d37-113">Field Service</span></span>    | <span data-ttu-id="11d37-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11d37-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="11d37-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="11d37-115">msdyn_warehouses</span></span> | <span data-ttu-id="11d37-116">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="11d37-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="11d37-117">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="11d37-117">Entity flow</span></span>
<span data-ttu-id="11d37-118">คลังสินค้าที่สร้างขึ้นและรักษาไว้ใน Finance and Operations สามารถซิงโครไนส์กับ Field Service ได้ ผ่านทางโครงการรวมข้อมูล Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="11d37-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="11d37-119">อาจมีการควบคุมคลังสินค้าที่ต้องการที่ซิงโครไนส์กับ Field Service พร้อมกับแบบสอบถามขั้นสูง และการกรองข้อมูลในโครงการ</span><span class="sxs-lookup"><span data-stu-id="11d37-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="11d37-120">มีการสร้างคลังสินค้าที่ซิงโครไนส์จาก Finance and Operations ใน Field Service กับฟิลด์ ได้รับการรักษา ถูกตั้งค่าเป็น ใช่ ภายนอก และเรกคอร์ดถูกทำให้เป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="11d37-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="11d37-121">โซลูชัน CRM ของ Field Service เพื่อสนับสนุนการรวมระหว่าง Field Service และ Finance and Operations ต้องมีฟังก์ชันเพิ่มเติมจากโซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="11d37-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="11d37-122">โซลูชันมีการเปลี่ยนแปลงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="11d37-122">The solution includes the following changes.</span></span>
<span data-ttu-id="11d37-123">ฟิลด์ **จะเก็บรักษาภายนอก** ได้ถูกเพิ่มไปยังเอนทิตี **คลังสินค้า (msdyn_warehouses)**</span><span class="sxs-lookup"><span data-stu-id="11d37-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="11d37-124">ฟิลด์นี้ช่วยระบุว่ามีจัดการคลังสินค้าจาก Operations หรือมีเฉพาะใน Field Service</span><span class="sxs-lookup"><span data-stu-id="11d37-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="11d37-125">ใช่ – คลังสินค้าที่สร้างจาก Finance and Operations และจะไม่สามารถแก้ไขได้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="11d37-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="11d37-126">ไม่ – มีการป้อนคลังสินค้าโดยตรงใน Field Service และรักษาไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="11d37-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="11d37-127">ฟิลด์ **ถูกรักษาไว้ภายนอก** ช่วยควบคุมการซิงโครไนส์ของระดับสินค้าคงคลัง การปรับปรุง การโอนย้าย และการใช้บนใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="11d37-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="11d37-128">เฉพาะคลังสินค้าที่มี **ถูกรักษาไว้จากภายนอก** = สามารถใช้ ใช่ เพื่อซิงโครไนส์โดยตรงไปยังคลังสินค้าเดียวกันในระบบอื่นๆ ได้</span><span class="sxs-lookup"><span data-stu-id="11d37-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="11d37-129">หมายเหตุ: คุณจะสามารถสร้างคลังสินค้าหลายแห่งใน Field Services ได้ ( **ถูกรักษาไว้ภายนอก** = No) แล้วแมปเข้ากับคลังสินค้าเดียวใน Finance and Operations แบบสอบถามขั้นสูง และการกรองข้อมูลฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="11d37-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="11d37-130">นี่จะถูกใช้ในสถานการณ์ที่คุณต้องการให้ Field service เป็นหลักของระดับสินค้าคงคลังโดยละเอียด และส่งการปรับปรุงไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11d37-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="11d37-131">ในกรณีนี้ Field service จะไม่ได้รับการปรับปรุงระดับสินค้าคงคลังจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11d37-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="11d37-132">ดูข้อมูลเพิ่มเติมในการซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service to Finance and Operations และซิงโครไนส์ใบสั่งงานใน Field Service ไปยังใบสั่งขายที่เชื่อมโยงกับโครงการใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11d37-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="11d37-133">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="11d37-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="11d37-134">ในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="11d37-134">In the Data Integration project</span></span>
<span data-ttu-id="11d37-135">ก่อนการซิงโครไนส์ของคลังสินค้า ตรวจสอบว่าได้ปรับปรุงการสอบถามขั้นสูง และการกรองข้อมูลโครงการที่จะรวมคลังสินค้าที่คุณต้องการนำมาจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="11d37-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="11d37-136">หมายเหตุว่า คุณจะต้องการคลังสินค้าที่ใน Field Service เพื่อใช้ในใบสั่งงาน การปรับปรุง และการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="11d37-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="11d37-137">ให้แน่ใจว่ามี **คีย์การรวม** อยู่ สำหรับ **msdyn_warehouses**</span><span class="sxs-lookup"><span data-stu-id="11d37-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="11d37-138">ไปยังการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="11d37-138">Go to Data Integration</span></span>
2. <span data-ttu-id="11d37-139">เลือกแท็บ **การตั้งค่าการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="11d37-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="11d37-140">เลือกชุดของการเชื่อมต่อที่ใช้สำหรับการซิงโครไนส์ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="11d37-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="11d37-141">เลือกแท็บ **คีย์การรวม**</span><span class="sxs-lookup"><span data-stu-id="11d37-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="11d37-142">ค้นหา msdyn_workorders และตรวจสอบว่าคีย์ **msdyn_name (ชื่อ)** ถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="11d37-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="11d37-143">ถ้าไม่แสดงขึ้น ให้เพิ่มโดยการคลิก **เพิ่มคีย์** และคลิก **บันทึก** ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="11d37-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="11d37-144">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="11d37-144">Template mapping in Data integration</span></span>

<span data-ttu-id="11d37-145">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="11d37-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="11d37-146">คลังสินค้าจาก (Finance and Operations ไปยัง Field Service): คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="11d37-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="11d37-147">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="11d37-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

