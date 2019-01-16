---
title: "ซิงโครไนส์การโอนและการปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Finance and Operations"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์การปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service"
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: th-th
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="17244-103">ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17244-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="17244-104">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์การปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="17244-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="17244-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="17244-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="17244-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="17244-106">Templates and tasks</span></span>
<span data-ttu-id="17244-107">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการรันการซิงโครไนส์ของการปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Microsoft Dynamics 365 for Field Service ไปยัง Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17244-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="17244-108">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="17244-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="17244-109">การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="17244-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="17244-110">การโอนย้ายสินค้าคงคลัง (Field Service ไปยัง Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="17244-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="17244-111">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="17244-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="17244-112">การปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="17244-112">Inventory Adjustments</span></span>
- <span data-ttu-id="17244-113">การโอนย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="17244-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="17244-114">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="17244-114">Entity set</span></span>
| <span data-ttu-id="17244-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="17244-115">Field Service</span></span>                     | <span data-ttu-id="17244-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17244-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="17244-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="17244-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="17244-118">ส่วนหัวและรายการสมุดรายวันการปรับปรุงสินค้าคงคลัง CDS</span><span class="sxs-lookup"><span data-stu-id="17244-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="17244-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="17244-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="17244-120">ส่วนหัวและรายการสมุดรายวันการโอนย้ายสินค้าคงคลัง CDS</span><span class="sxs-lookup"><span data-stu-id="17244-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="17244-121">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="17244-121">Entity flow</span></span>
<span data-ttu-id="17244-122">การปรับปรุงและการโอนย้ายสินค้าคงคลังที่ทำไว้ใน Field Service จะซิงโครไนซ์กับ Finance and Operations เมื่อ **ลงรายการบัญชีสถานะ** ถูกเปลี่ยนจาก สร้างแล้ว เป็นลงรายการบัญชีแล้ว</span><span class="sxs-lookup"><span data-stu-id="17244-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="17244-123">เมื่อสิ่งนี้เกิดขึ้น ใบสั่งการปรับปรุงหรือการโอนย้ายจะถูกล็อค และกลายเป็นแบบอ่านอย่างเดียว เนื่องจากการปรับปรุงและการโอนย้ายอาจถูกลงรายการบัญชีใน Finance and Operations และดังนั้นจึงไม่สามารถปรับเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="17244-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="17244-124">ใน Finance and Operations คุณสามารถตั้งค่าชุดงานเพื่อลงรายการบัญชีการปรับปรุง และโอนย้ายสมุดรายวันสินค้าคงคลังที่สร้างขึ้นด้วยการรวมโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="17244-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="17244-125">ดูข้อกำหนดเบื้องต้นด้านล่างนี้สำหรับรายละเอียดเกี่ยวกับวิธีการเปิดใช้งานชุดงาน</span><span class="sxs-lookup"><span data-stu-id="17244-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="17244-126">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="17244-126">Field Service CRM solution</span></span> 
<span data-ttu-id="17244-127">มีการเพิ่มฟิลด์หน่วยสินค้าคงคลังไปยังเอนทิตีผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="17244-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="17244-128">ฟิลด์นี้จำเป็นต้องใช้นับตั้งแต่หน่วยการขายและหน่วยสินค้าคงคลังไม่เหมือนกันเสมอใน Operations และสำหรับสินค้าคงคลังในคลังสินค้าใน operations เราต้องการหน่วยสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="17244-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="17244-129">เมื่อคุณตั้งค่าผลิตภัณฑ์ในผลิตภัณฑ์การปรับปรุงสินค้าคงคลังสำหรับทั้งการปรับปรุงสินค้าคงคลังและการโอนย้ายสินค้าคงคลัง หน่วยจะถูกดึงมาจากค่าผลิตภัณฑ์ของสินค้าคงคลังของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="17244-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="17244-130">ถ้าค่าถูกพบ ฟิลด์หน่วยจะถูกล็อคในผลิตภัณฑ์การปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="17244-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="17244-131">มีการเพิ่มฟิลด์การลงรายการบัญชีสถานะไปยังทั้งเอนทิตีการปรับปรุงสินค้าคงคลังและเอนทิตีการโอนย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="17244-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="17244-132">ฟิลด์นี้จะใช้เป็นตัวกรองสำหรับเวลาที่มีการส่งการปรับปรุงหรือการโอนย้ายไปยังการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="17244-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="17244-133">ฟิลด์นี้ถูกตั้งค่าเริ่มต้นเป็น สร้างแล้ว (1) และจากนั้น จะไม่ถูกไปยังการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="17244-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="17244-134">รายการที่คุณเปลี่ยนคือ ลงรายการบัญชีแล้ว (2) ซึ่งจะถูกส่งไปยังการดำเนินงาน แต่คุณจะไม่สามารถเปลี่ยนแปลงสิ่งใดได้ในการปรับปรุงหรือการโอนย้าย หรือเพิ่มรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="17244-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="17244-135">มีการเพิ่มฟิลด์ลำดับหมายเลขไปยังเอนทิตีผลิตภัณฑ์ของการปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="17244-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="17244-136">ฟิลด์นี้ช่วยให้การรวมมีหมายเลขเฉพาะ ดังนั้นการรวมจะทราบว่าจะทำการสร้าง และจะทำการปรับปรุงเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="17244-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="17244-137">เมื่อคุณสร้างผลิตภัณฑ์การปรับปรุงสินค้าคงคลังครั้งแรก จะมีการสร้างเรกคอร์ดใหม่ในเอนทิตี P2C AutoNumber เพื่อรักษาชุดหมายเลขและคำนำหน้าที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="17244-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="17244-138">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="17244-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="17244-139">ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17244-139">In Finance and Operations</span></span>
<span data-ttu-id="17244-140">สามารถลงรายการบัญชีสมุดรายวันสินค้าคงคลังการรวมที่สร้างขึ้นโดยการรวมกับชุดงานโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="17244-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="17244-141">นี่จะถูกเปิดใช้งานจาก: การจัดการสินค้าคงคลัง > งานประจำงวด > การรวม CDS > ลงรายการบัญชีสมุดรายวันสินค้าคงคลังการรวม</span><span class="sxs-lookup"><span data-stu-id="17244-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="17244-142">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="17244-142">Template mapping in Data integration</span></span>

<span data-ttu-id="17244-143">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="17244-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="17244-144">การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Finance and Operations): การปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="17244-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="17244-145">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="17244-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="17244-146">การโอนย้ายสินค้าคงคลัง (Field Service ไปยัง Finance and Operations): การโอนย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="17244-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="17244-147">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="17244-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

