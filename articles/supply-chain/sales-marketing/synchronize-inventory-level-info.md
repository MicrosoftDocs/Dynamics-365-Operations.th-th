---
title: "ซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: th-th
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="6b411-103">ซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="6b411-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6b411-104">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="6b411-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="6b411-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="6b411-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="6b411-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="6b411-106">Templates and tasks</span></span>
<span data-ttu-id="6b411-107">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการรันการซิงโครไนส์ของระดับปริมาณคงคลังคงเหลือจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="6b411-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="6b411-108">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="6b411-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="6b411-109">สินค้าคงคลังของผลิตภัณฑ์ (Finance and Operations ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="6b411-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="6b411-110">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="6b411-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="6b411-111">สินค้าคงคลังของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6b411-111">Product inventory</span></span>

<span data-ttu-id="6b411-112">จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ของระดับสินค้าคงคลังจะเกิดขึ้นได้:</span><span class="sxs-lookup"><span data-stu-id="6b411-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="6b411-113">คลังสินค้า (Finance and Operations ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="6b411-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="6b411-114">ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Sales)</span><span class="sxs-lookup"><span data-stu-id="6b411-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="6b411-115">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="6b411-115">Entity set</span></span>

| <span data-ttu-id="6b411-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="6b411-116">Field Service</span></span>                      | <span data-ttu-id="6b411-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6b411-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="6b411-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="6b411-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="6b411-119">สินค้าคงคลังคงเหลือ CDS ตามคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6b411-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="6b411-120">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="6b411-120">Entity flow</span></span>
<span data-ttu-id="6b411-121">ข้อมูลระดับสินค้าคงคลังจาก Finance and Operation ถูกส่งไปยัง Field Service สำหรับผลิตภัณฑ์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6b411-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="6b411-122">ข้อมูลระดับสินค้าคงคลังรวม:</span><span class="sxs-lookup"><span data-stu-id="6b411-122">The inventory level information include:</span></span> 
- <span data-ttu-id="6b411-123">ปริมาณคงคลังคงเหลือ (ปริมาณทางกายภาพที่บันทึกในปัจจุบันที่อยู่ในคลังสินค้า)</span><span class="sxs-lookup"><span data-stu-id="6b411-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="6b411-124">ปริมาณที่อยู่ระหว่างการสั่ง (ปริมาณรวมที่บันทึกไว้ในใบสั่ง - เช่น ใบสั่งขาย)</span><span class="sxs-lookup"><span data-stu-id="6b411-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="6b411-125">ปริมาณที่สั่ง (ปริมาณรวมที่สั่งที่บันทึกไว้ - เช่น ใบสั่งซื้อ)</span><span class="sxs-lookup"><span data-stu-id="6b411-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="6b411-126">ข้อมูลนี้จะถูกรวบรวมสำหรับแต่ละผลิตภัณฑ์ที่นำออกใช้สำหรับคลังสินค้าแต่ละรายการ และซิงโครไนส์ตามการติดตามการเปลี่ยนแปลง เมื่อระดับสินค้าคงคลังมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="6b411-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="6b411-127">ใน Field Service โซลูชันการรวมสร้างสมุดรายวันสินค้าคงคลังสำหรับผลต่าง เพื่อเรียกระดับใน Field Service เพื่อให้ตรงกับระดับใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6b411-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="6b411-128">Finance and Operations จะทำหน้าที่เป็นต้นแบบสำหรับระดับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="6b411-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="6b411-129">ดังนั้น จึงจำเป็นต้องตั้งค่าการรวมสำหรับใบสั่งงาน การโอนย้าย และการปรับปรุงจาก Field Service ไปยัง Finance and Operations ถ้ามีการใช้ฟังก์ชันนี้ใน Field Service ร่วมกับการซิงโครไนส์ของระดับสินค้าคงคลังจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6b411-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="6b411-130">ผลิตภัณฑ์และคลังสินค้าที่ซึ่งระดับสินค้าคงคลังเป็นต้นฉบับจาก Finance and Operations และสามารถควบคุมได้ด้วยการสอบถามและการกรองขั้นสูง (Power Query)</span><span class="sxs-lookup"><span data-stu-id="6b411-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="6b411-131">หมายเหตุ: คุณจะสามารถสร้างคลังสินค้าหลายแห่งใน Field Services ได้ (ด้วย ถูกรักษาไว้ภายนอก = ไม่) แล้วจากนั้นแม็ปเข้ากับคลังสินค้าเดียวใน Finance and Operations ด้วยแบบสอบถามขั้นสูงและการกรองข้อมูลฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="6b411-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="6b411-132">นี่จะถูกใช้ในสถานการณ์ที่คุณต้องการให้ Field service เป็นหลักของระดับสินค้าคงคลังโดยละเอียด และส่งการปรับปรุงไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6b411-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="6b411-133">ในกรณีนี้ Field service จะไม่ได้รับการปรับปรุงระดับสินค้าคงคลังจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6b411-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="6b411-134">ดูข้อมูลเพิ่มเติมในการซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service to Finance and Operations และซิงโครไนส์ใบสั่งงานใน Field Service ไปยังใบสั่งขายที่เชื่อมโยงกับโครงการใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6b411-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="6b411-135">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="6b411-135">Field Service CRM solution</span></span>
<span data-ttu-id="6b411-136">เอนทิตีสินค้าคงคลังของผลิตภัณฑ์ภายนอกเป็นเอนทิตีใหม่ที่จะใช้สำหรับ backend ในการรวมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6b411-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="6b411-137">ซึ่งรับค่าระดับสินค้าคงคลังจาก Finance and Operations ในการรวม และจากนั้น แปลงค่าเหล่านั้นเป็นสมุดรายวันสินค้าคงคลัง Manuel ซึ่งจากนั้น เปลี่ยนแปลงผลิตภัณฑ์สินค้าคงคลังในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6b411-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="6b411-138">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="6b411-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="6b411-139">ในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6b411-139">In the Data Integration project</span></span>
<span data-ttu-id="6b411-140">ใช้ตัวกรองข้อมูลกับการสอบถามและการกรองขั้นสูงในการควบคุมว่า เฉพาะผลิตภัณฑ์และคลังสินค้าที่ต้องการที่ส่งข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="6b411-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6b411-141">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6b411-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="6b411-142">สินค้าคงคลังของผลิตภัณฑ์ (Finance and Operations ไปยัง Field Service): สินค้าคงคลังของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6b411-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="6b411-143">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="6b411-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

