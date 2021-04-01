---
title: ซิงโครไนส์คลังสินค้าจาก Supply Chain Management ไปยัง Field Service
description: หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์คลังสินค้าจาก Dynamics 365 Supply Chain Management เป็น Dynamics 365 Field Service
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 051bbee28d45a6d4142beef40c5a173f2ca30a11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243044"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="991c8-103">ซิงโครไนส์คลังสินค้าจาก Supply Chain Management ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="991c8-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="991c8-104">หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์คลังสินค้าจาก Dynamics 365 Supply Chain Management เป็น Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="991c8-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="991c8-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="991c8-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="991c8-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="991c8-106">Templates and tasks</span></span>
<span data-ttu-id="991c8-107">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการเรียกใช้การซิงโครไนส์คลังสินค้าจาก Supply Chain Management ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="991c8-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="991c8-108">**เท็มเพลตในการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="991c8-108">**Template in Data integration**</span></span>
- <span data-ttu-id="991c8-109">คลังสินค้า (Supply Chain Management ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="991c8-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="991c8-110">**งานในโครงการการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="991c8-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="991c8-111">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="991c8-111">Warehouse</span></span>

## <a name="table-set"></a><span data-ttu-id="991c8-112">ชุดตาราง</span><span class="sxs-lookup"><span data-stu-id="991c8-112">Table set</span></span>
| <span data-ttu-id="991c8-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="991c8-113">Field Service</span></span>    | <span data-ttu-id="991c8-114">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="991c8-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="991c8-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="991c8-115">msdyn_warehouses</span></span> | <span data-ttu-id="991c8-116">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="991c8-116">Warehouses</span></span>                             |

## <a name="table-flow"></a><span data-ttu-id="991c8-117">โฟลว์ของตาราง</span><span class="sxs-lookup"><span data-stu-id="991c8-117">Table flow</span></span>
<span data-ttu-id="991c8-118">คลังสินค้าที่สร้างขึ้นและรักษาไว้ใน Supply Chain Management สามารถซิงโครไนส์กับ Field Service ได้ ผ่านทางโครงการรวมข้อมูล Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="991c8-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="991c8-119">อาจมีการควบคุมคลังสินค้าที่คุณต้องการที่ซิงโครไนส์กับ Field Service พร้อมกับแบบสอบถามขั้นสูง และการกรองข้อมูลในโครงการ</span><span class="sxs-lookup"><span data-stu-id="991c8-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="991c8-120">มีการสร้างคลังสินค้าที่ซิงโครไนส์จาก Supply Chain Management ใน Field Service กับคอลัมน์ **ได้รับการรักษาไว้ภายนอก** ถูกตั้งค่าเป็น **ใช่** และเรกคอร์ดเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="991c8-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** column set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="991c8-121">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="991c8-121">Field Service CRM solution</span></span>
<span data-ttu-id="991c8-122">เพื่อสนับสนุนการรวมระหว่าง Field Service และ Supply Chain Management ต้องมีฟังก์ชันเพิ่มเติมจากโซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="991c8-122">To support the integration between Field Service and Supply Chain Management, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="991c8-123">ในโซลูชัน คอลัมน์ **จะเก็บรักษาภายนอก** ได้ถูกเพิ่มไปยังตาราง **คลังสินค้า (msdyn_warehouses)**</span><span class="sxs-lookup"><span data-stu-id="991c8-123">In the solution, the **Is Maintained Externally** column has been added to the **Warehouse (msdyn_warehouses)** table.</span></span> <span data-ttu-id="991c8-124">คอลัมน์นี้ช่วยระบุว่ามีจัดการคลังสินค้าจาก Supply Chain Management หรือว่ามีอยู่เฉพาะใน Field Service</span><span class="sxs-lookup"><span data-stu-id="991c8-124">This column helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="991c8-125">การตั้งค่าสำหรับคอลัมน์นี้รวมถึง:</span><span class="sxs-lookup"><span data-stu-id="991c8-125">The settings for this column include:</span></span>
- <span data-ttu-id="991c8-126">**ใช่** – คลังสินค้าสร้างจาก Supply Chain Management และจะไม่สามารถแก้ไขได้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="991c8-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="991c8-127">**ไม่** – มีการป้อนคลังสินค้าโดยตรงใน Field Service และรักษาไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="991c8-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="991c8-128">คอลัมน์ **รักษาไว้สำหรับภายนอก** ช่วยควบคุมการซิงโครไนส์ของระดับสินค้าคงคลัง การปรับปรุง การโอนย้าย และการใช้บนใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="991c8-128">The **Is Externally Maintained** column helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="991c8-129">เฉพาะคลังสินค้าที่มี **รักษาไว้สำหรับภายนอก** ถูกตั้งค่าเป็น **ใช่** สามารถถูกซิงโครไนส์โดยตรงไปยังคลังสินค้าเดียวกันในระบบอื่นๆ ได้</span><span class="sxs-lookup"><span data-stu-id="991c8-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="991c8-130">คุณจะสามารถสร้างคลังสินค้าหลายแห่งใน Field Service ได้ (โดยที่ **ถูกรักษาไว้สำหรับภายนอก** = ไม่) แล้วแม็ปเข้ากับคลังสินค้าเดียว ซึ่งมีแบบสอบถามขั้นสูงและฟังก์ชันการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="991c8-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="991c8-131">จะมีการใช้ในสถานการณ์ที่คุณต้องการให้ Field service เป็นหลักของระดับสินค้าคงคลังโดยละเอียด และส่งเพียงการปรับปรุงไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="991c8-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Supply Chain Management.</span></span> <span data-ttu-id="991c8-132">ในกรณีนี้ Field service จะไม่ได้รับการปรับปรุงระดับสินค้าคงคลังจาก Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="991c8-132">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="991c8-133">สำหรับข้อมูลเพิ่มเติม ดู [ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) และ [ซิงโครไนส์ใบสั่งงานใน Field Service ไปยังใบสั่งขายที่เชื่อมโยงกับโครงการใน Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)</span><span class="sxs-lookup"><span data-stu-id="991c8-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="991c8-134">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="991c8-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="991c8-135">โครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="991c8-135">Data Integration project</span></span>
<span data-ttu-id="991c8-136">ก่อนการซิงโครไนส์คลังสินค้า ตรวจสอบว่าได้ปรับปรุงการสอบถามขั้นสูง และการกรองข้อมูลโครงการที่จะรวมเฉพาะคลังสินค้าที่คุณต้องการนำมาจาก Supply Chain Management ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="991c8-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="991c8-137">หมายเหตุว่า คุณจะต้องการคลังสินค้าที่ใน Field Service เพื่อใช้ในใบสั่งงาน การปรับปรุง และการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="991c8-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="991c8-138">เพื่อให้แน่ใจว่ามี **คีย์การรวม** อยู่ สำหรับ **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="991c8-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="991c8-139">ไปยังการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="991c8-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="991c8-140">เลือกแท็บ **การตั้งค่าการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="991c8-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="991c8-141">เลือกชุดของการเชื่อมต่อที่ใช้สำหรับการซิงโครไนส์ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="991c8-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="991c8-142">เลือกแท็บ **คีย์การรวม**</span><span class="sxs-lookup"><span data-stu-id="991c8-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="991c8-143">ค้นหา msdyn_workorders และยืนยันว่าคีย์ **msdyn_name (ชื่อ)** ถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="991c8-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="991c8-144">ถ้าไม่แสดงขึ้น ให้เพิ่มโดยการคลิก **เพิ่มคีย์** แล้วคลิก **บันทึก** ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="991c8-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="991c8-145">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="991c8-145">Template mapping in Data integration</span></span>

<span data-ttu-id="991c8-146">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="991c8-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="991c8-147">คลังสินค้า (Supply Chain Management ไปยัง Field Service): คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="991c8-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="991c8-148">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="991c8-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]