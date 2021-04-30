---
title: ซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Supply Chain Management ไปยัง Field Service
description: หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Dynamics 365 Supply Chain Management เป็น Dynamics 365 Field Service
author: ChristianRytt
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 15466699b94c284208330d50b840c874534b879c
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910291"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="fb90c-103">ซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Supply Chain Management ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="fb90c-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="fb90c-104">หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Dynamics 365 Supply Chain Management เป็น Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="fb90c-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="fb90c-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="fb90c-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="fb90c-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="fb90c-106">Templates and tasks</span></span>
<span data-ttu-id="fb90c-107">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ระดับปริมาณคงคลังคงเหลือโดยตรงจาก Supply Chain Management ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="fb90c-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="fb90c-108">**เท็มเพลตในการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="fb90c-108">**Template in Data integration**</span></span>
- <span data-ttu-id="fb90c-109">สินค้าคงคลัง (Supply Chain Management ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="fb90c-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="fb90c-110">**งานในโครงการการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="fb90c-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="fb90c-111">สินค้าคงคลังของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="fb90c-111">Product inventory</span></span>

<span data-ttu-id="fb90c-112">จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ของระดับสินค้าคงคลังจะเกิดขึ้นได้:</span><span class="sxs-lookup"><span data-stu-id="fb90c-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="fb90c-113">คลังสินค้า (Supply Chain Management ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="fb90c-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="fb90c-114">ผลิตภัณฑ์ Field Service ที่มากับหน่วยสินค้าคงคลัง (Supply Chain Management ไปยัง Sales)</span><span class="sxs-lookup"><span data-stu-id="fb90c-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="fb90c-115">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="fb90c-115">Entity set</span></span>

| <span data-ttu-id="fb90c-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="fb90c-116">Field Service</span></span>                      | <span data-ttu-id="fb90c-117">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fb90c-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="fb90c-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="fb90c-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="fb90c-119">สินค้าคงคลังคงเหลือ Dataverse ตามคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="fb90c-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="fb90c-120">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="fb90c-120">Entity flow</span></span>
<span data-ttu-id="fb90c-121">ข้อมูลระดับสินค้าคงคลังจาก Finance and Operation ถูกส่งไปยัง Field Service สำหรับผลิตภัณฑ์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fb90c-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="fb90c-122">ข้อมูลระดับสินค้าคงคลังรวม:</span><span class="sxs-lookup"><span data-stu-id="fb90c-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="fb90c-123">ปริมาณคงคลังคงเหลือ (ปริมาณทางกายภาพที่บันทึกในปัจจุบันที่อยู่ในคลังสินค้า)</span><span class="sxs-lookup"><span data-stu-id="fb90c-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="fb90c-124">ปริมาณที่อยู่ระหว่างการสั่ง (ปริมาณรวมที่บันทึกไว้ในใบสั่ง เช่น ใบสั่งขาย)</span><span class="sxs-lookup"><span data-stu-id="fb90c-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="fb90c-125">ปริมาณที่สั่ง (ปริมาณรวมที่สั่งที่บันทึกไว้ เช่น ใบสั่งซื้อ)</span><span class="sxs-lookup"><span data-stu-id="fb90c-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="fb90c-126">ข้อมูลนี้จะถูกรวบรวมสำหรับแต่ละผลิตภัณฑ์ที่นำออกใช้สำหรับคลังสินค้าแต่ละรายการ และซิงโครไนส์ตามการติดตามการเปลี่ยนแปลง เมื่อระดับสินค้าคงคลังมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="fb90c-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="fb90c-127">ใน Field Service โซลูชันการรวมสร้างสมุดรายวันสินค้าคงคลังสำหรับผลต่าง เพื่อเรียกระดับใน Field Service เพื่อให้ตรงกับระดับใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fb90c-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="fb90c-128">Supply Chain Management จะทำหน้าที่เป็นต้นแบบสำหรับระดับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fb90c-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="fb90c-129">ดังนั้น จึงจำเป็นต้องตั้งค่าการรวมสำหรับใบสั่งงาน การโอนย้าย และการปรับปรุงจาก Field Service ไปยัง Supply Chain Management ถ้ามีการใช้ฟังก์ชันนี้ใน Field Service ร่วมกับการซิงโครไนส์ของระดับสินค้าคงคลังจาก Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fb90c-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="fb90c-130">ผลิตภัณฑ์และคลังสินค้าที่ซึ่งระดับสินค้าคงคลังเป็นต้นฉบับจาก Supply Chain Management และสามารถควบคุมได้ด้วยการสอบถามและการกรองขั้นสูง (Power Query)</span><span class="sxs-lookup"><span data-stu-id="fb90c-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="fb90c-131">คุณจะสามารถสร้างคลังสินค้าหลายแห่งใน Field Services ได้ ( **ถูกรักษาไว้ภายนอก = No**) แล้วแมปเข้ากับคลังสินค้าเดียวใน Supply Chain Management แบบสอบถามขั้นสูง และการกรองข้อมูลฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="fb90c-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="fb90c-132">นี่จะถูกใช้ในสถานการณ์ที่คุณต้องการให้ Field service เป็นหลักของระดับสินค้าคงคลังโดยละเอียด และส่งการปรับปรุงไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fb90c-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="fb90c-133">ในกรณีนี้ Field service จะไม่ได้รับการปรับปรุงระดับสินค้าคงคลังจาก Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fb90c-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="fb90c-134">สำหรับข้อมูลเพิ่มเติม ดู [ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service to Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) และ [ซิงโครไนส์ใบสั่งงานใน Field Service ไปยังใบสั่งขายที่เชื่อมโยงกับโครงการใน Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)</span><span class="sxs-lookup"><span data-stu-id="fb90c-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="fb90c-135">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="fb90c-135">Field Service CRM solution</span></span>
<span data-ttu-id="fb90c-136">เอนทิตี **สินค้าคงคลังของผลิตภัณฑ์ภายนอก** ถูกใช้สำหรับ backend ในการรวมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fb90c-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="fb90c-137">เอนทิตีนี้รับค่าระดับสินค้าคงคลังจาก Supply Chain Management ในการรวม และจากนั้น แปลงค่าเหล่านั้นเป็นสมุดรายวันสินค้าคงคลัง Manuel ซึ่งจากนั้น เปลี่ยนแปลงผลิตภัณฑ์สินค้าคงคลังในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="fb90c-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="fb90c-138">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="fb90c-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="fb90c-139">การรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fb90c-139">Data integration</span></span>
<span data-ttu-id="fb90c-140">สำหรับโครงการที่จะทำงาน คุณต้องตรวจสอบให้แน่ใจว่ามีการอัพเดตคีย์การรวมสำหรับ msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="fb90c-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="fb90c-141">ไปที่ **การรวมข้อมูล > ชุดการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="fb90c-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="fb90c-142">เลือกชุดการเชื่อมต่อที่ใช้</span><span class="sxs-lookup"><span data-stu-id="fb90c-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="fb90c-143">บนแท็บ **คีย์การรวม** ตรวจสอบให้แน่ใจว่ามีการเพิ่มคีย์ต่อไปนี้ลงใน msdynce_externalproductinventories:</span><span class="sxs-lookup"><span data-stu-id="fb90c-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="fb90c-144">msdynce_productnumber (หมายเลขผลิตภัณฑ์)</span><span class="sxs-lookup"><span data-stu-id="fb90c-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="fb90c-145">msdynce_warehouseid (รหัสคลังสินค้า)</span><span class="sxs-lookup"><span data-stu-id="fb90c-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="fb90c-146">โครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fb90c-146">Data integration project</span></span>
<span data-ttu-id="fb90c-147">คุณสามารถใช้ตัวกรองข้อมูลกับการสอบถามและการกรองขั้นสูงในการควบคุมว่า เฉพาะผลิตภัณฑ์และคลังสินค้าที่ต้องการที่ส่งข้อมูลระดับสินค้าคงคลังจาก Supply Chain Management ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="fb90c-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fb90c-148">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fb90c-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="fb90c-149">สินค้าคงคลัง (Supply Chain Management ไปยัง Field Service): สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fb90c-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="fb90c-150">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="fb90c-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]