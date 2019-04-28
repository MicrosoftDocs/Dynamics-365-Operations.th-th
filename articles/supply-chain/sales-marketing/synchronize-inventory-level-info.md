---
title: ซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service
description: หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations เป็น Microsoft Dynamics 365 for Field Service
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
ms.openlocfilehash: 6b2bdf1ca6f6ae43cd85c8a1353ee8305052761d
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/14/2019
ms.locfileid: "842567"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="14459-103">ซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="14459-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="14459-104">หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations เป็น Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="14459-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="14459-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="14459-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="14459-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="14459-106">Templates and tasks</span></span>
<span data-ttu-id="14459-107">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการซิงโครไนส์ระดับปริมาณคงคลังคงเหลือจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="14459-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="14459-108">**เท็มเพลตในการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="14459-108">**Template in Data integration**</span></span>
- <span data-ttu-id="14459-109">สินค้าคงคลังของผลิตภัณฑ์ (Fin and Ops ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="14459-109">Product Inventory (Fin and Ops to Field Service)</span></span>
  
<span data-ttu-id="14459-110">**งานในโครงการการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="14459-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="14459-111">สินค้าคงคลังของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="14459-111">Product inventory</span></span>

<span data-ttu-id="14459-112">จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ของระดับสินค้าคงคลังจะเกิดขึ้นได้:</span><span class="sxs-lookup"><span data-stu-id="14459-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="14459-113">คลังสินค้า (Fin and Ops ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="14459-113">Warehouses (Fin and Ops to Field Service)</span></span> 
- <span data-ttu-id="14459-114">ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Fin and Ops ไปยัง Sales)</span><span class="sxs-lookup"><span data-stu-id="14459-114">Field Service products with Inventory unit (Fin and Ops to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="14459-115">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="14459-115">Entity set</span></span>

| <span data-ttu-id="14459-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="14459-116">Field Service</span></span>                      | <span data-ttu-id="14459-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14459-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="14459-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="14459-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="14459-119">สินค้าคงคลังคงเหลือ CDS ตามคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="14459-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="14459-120">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="14459-120">Entity flow</span></span>
<span data-ttu-id="14459-121">ข้อมูลระดับสินค้าคงคลังจาก Finance and Operation ถูกส่งไปยัง Field Service สำหรับผลิตภัณฑ์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="14459-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="14459-122">ข้อมูลระดับสินค้าคงคลังรวม:</span><span class="sxs-lookup"><span data-stu-id="14459-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="14459-123">ปริมาณคงคลังคงเหลือ (ปริมาณทางกายภาพที่บันทึกในปัจจุบันที่อยู่ในคลังสินค้า)</span><span class="sxs-lookup"><span data-stu-id="14459-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="14459-124">ปริมาณที่อยู่ระหว่างการสั่ง (ปริมาณรวมที่บันทึกไว้ในใบสั่ง เช่น ใบสั่งขาย)</span><span class="sxs-lookup"><span data-stu-id="14459-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="14459-125">ปริมาณที่สั่ง (ปริมาณรวมที่สั่งที่บันทึกไว้ เช่น ใบสั่งซื้อ)</span><span class="sxs-lookup"><span data-stu-id="14459-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="14459-126">ข้อมูลนี้จะถูกรวบรวมสำหรับแต่ละผลิตภัณฑ์ที่นำออกใช้สำหรับคลังสินค้าแต่ละรายการ และซิงโครไนส์ตามการติดตามการเปลี่ยนแปลง เมื่อระดับสินค้าคงคลังมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="14459-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="14459-127">ใน Field Service โซลูชันการรวมสร้างสมุดรายวันสินค้าคงคลังสำหรับผลต่าง เพื่อเรียกระดับใน Field Service เพื่อให้ตรงกับระดับใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14459-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="14459-128">Finance and Operations จะทำหน้าที่เป็นต้นแบบสำหรับระดับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="14459-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="14459-129">ดังนั้น จึงจำเป็นต้องตั้งค่าการรวมสำหรับใบสั่งงาน การโอนย้าย และการปรับปรุงจาก Field Service ไปยัง Finance and Operations ถ้ามีการใช้ฟังก์ชันนี้ใน Field Service ร่วมกับการซิงโครไนส์ของระดับสินค้าคงคลังจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14459-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="14459-130">ผลิตภัณฑ์และคลังสินค้าที่ซึ่งระดับสินค้าคงคลังเป็นต้นฉบับจาก Finance and Operations และสามารถควบคุมได้ด้วยการสอบถามและการกรองขั้นสูง (Power Query)</span><span class="sxs-lookup"><span data-stu-id="14459-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="14459-131">คุณจะสามารถสร้างคลังสินค้าหลายแห่งใน Field Services ได้ ( **ถูกรักษาไว้ภายนอก = No**) แล้วแมปเข้ากับคลังสินค้าเดียวใน Finance and Operations แบบสอบถามขั้นสูง และการกรองข้อมูลฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="14459-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="14459-132">นี่จะถูกใช้ในสถานการณ์ที่คุณต้องการให้ Field service เป็นหลักของระดับสินค้าคงคลังโดยละเอียด และส่งการปรับปรุงไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14459-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="14459-133">ในกรณีนี้ Field service จะไม่ได้รับการปรับปรุงระดับสินค้าคงคลังจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14459-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="14459-134">สำหรับข้อมูลเพิ่มเติม ดู [ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) และ [ซิงโครไนส์ใบสั่งงานใน Field Service ไปยังใบสั่งขายที่เชื่อมโยงกับโครงการใน Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)</span><span class="sxs-lookup"><span data-stu-id="14459-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="14459-135">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="14459-135">Field Service CRM solution</span></span>
<span data-ttu-id="14459-136">เอนทิตี **สินค้าคงคลังของผลิตภัณฑ์ภายนอก** ถูกใช้สำหรับ backend ในการรวมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="14459-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="14459-137">เอนทิตีนี้รับค่าระดับสินค้าคงคลังจาก Finance and Operations ในการรวม และจากนั้น แปลงค่าเหล่านั้นเป็นสมุดรายวันสินค้าคงคลัง Manuel ซึ่งจากนั้น เปลี่ยนแปลงผลิตภัณฑ์สินค้าคงคลังในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="14459-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="14459-138">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="14459-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration-project"></a><span data-ttu-id="14459-139">โครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="14459-139">Data integration project</span></span>
<span data-ttu-id="14459-140">คุณสามารถใช้ตัวกรองข้อมูลกับการสอบถามและการกรองขั้นสูงในการควบคุมว่า เฉพาะผลิตภัณฑ์และคลังสินค้าที่ต้องการที่ส่งข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="14459-140">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="14459-141">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="14459-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a><span data-ttu-id="14459-142">สินค้าคงคลังของผลิตภัณฑ์ (Fin and Ops ไปยัง Field Service): สินค้าคงคลังของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="14459-142">Product inventory (Fin and Ops to Field Service): Product inventory</span></span>

<span data-ttu-id="14459-143">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="14459-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
