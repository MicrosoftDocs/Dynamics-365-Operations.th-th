---
title: ซิงโครไนส์การโอนและการปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Supply Chain Management
description: หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ของการปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Dynamics 365 Supply Chain Management เป็น Dynamics 365 Field Service
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: d76adf10b9df48f5a7a5196e0469bb7cb1dbb34f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552244"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="fbb4f-103">ซิงโครไนส์การโอนและการปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fbb4f-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fbb4f-104">หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ของการปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Dynamics 365 Supply Chain Management เป็น Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="fbb4f-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="fbb4f-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="fbb4f-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="fbb4f-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="fbb4f-106">Templates and tasks</span></span>
<span data-ttu-id="fbb4f-107">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์การโอนย้ายและการปรับปรุงสินค้าคงคลังโดยตรงจาก Field Service ไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fbb4f-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="fbb4f-108">**เท็มเพลตในการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="fbb4f-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="fbb4f-109">การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="fbb4f-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="fbb4f-110">การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="fbb4f-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="fbb4f-111">**งานในโครงการการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="fbb4f-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="fbb4f-112">การปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fbb4f-112">Inventory Adjustments</span></span>
- <span data-ttu-id="fbb4f-113">การโอนย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fbb4f-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="fbb4f-114">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="fbb4f-114">Entity set</span></span>
| <span data-ttu-id="fbb4f-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="fbb4f-115">Field Service</span></span>                     | <span data-ttu-id="fbb4f-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fbb4f-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="fbb4f-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="fbb4f-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="fbb4f-118">ส่วนหัวและรายการสมุดรายวันการปรับปรุงสินค้าคงคลัง CDS</span><span class="sxs-lookup"><span data-stu-id="fbb4f-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="fbb4f-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="fbb4f-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="fbb4f-120">ส่วนหัวและรายการสมุดรายวันการโอนย้ายสินค้าคงคลัง CDS</span><span class="sxs-lookup"><span data-stu-id="fbb4f-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="fbb4f-121">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="fbb4f-121">Entity flow</span></span>
<span data-ttu-id="fbb4f-122">การปรับปรุงและการโอนย้ายสินค้าคงคลังที่ทำไว้ใน Field Service จะซิงโครไนซ์กับ Supply Chain Management หลังจากที่ **ลงรายการบัญชีสถานะ** ถูกเปลี่ยนจาก **สร้างแล้ว** เป็น **ลงรายการบัญชีแล้ว**</span><span class="sxs-lookup"><span data-stu-id="fbb4f-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="fbb4f-123">หากเป็นเช่นนั้น ใบสั่งโอนย้ายหรือการปรับปรุงจะถูกล็อค และกลายเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="fbb4f-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="fbb4f-124">ซึ่งหมายความว่า การปรับปรุงและการโอนย้ายสามารถลงรายการบัญชีใน Supply Chain Management แต่ไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="fbb4f-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="fbb4f-125">ใน Supply Chain Management คุณสามารถตั้งค่าชุดงานเพื่อลงรายการบัญชีการปรับปรุง และโอนย้ายสมุดรายวันสินค้าคงคลังที่สร้างขึ้นระหว่างการรวมโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="fbb4f-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="fbb4f-126">ดูข้อกำหนดเบื้องต้นต่อไปนี้สำหรับรายละเอียดเกี่ยวกับวิธีการเปิดใช้งานชุดงาน</span><span class="sxs-lookup"><span data-stu-id="fbb4f-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="fbb4f-127">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="fbb4f-127">Field Service CRM solution</span></span> 
<span data-ttu-id="fbb4f-128">มีการเพิ่มฟิลด์ **หน่วยสินค้าคงคลัง** ไปยังเอนทิตี **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="fbb4f-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="fbb4f-129">ฟิลด์นี้จำเป็นต้องใช้นับตั้งแต่หน่วยการขายและหน่วยสินค้าคงคลังไม่เหมือนกันเสมอใน Supply Chain Management และหน่วยสินค้าคงคลังจำเป็นสำหรับสินค้าคงคลังในคลังสินค้าใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fbb4f-129">This field is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="fbb4f-130">เมื่อคุณตั้งค่าผลิตภัณฑ์ในผลิตภัณฑ์การปรับปรุงสินค้าคงคลังสำหรับทั้งการปรับปรุงสินค้าคงคลังและการโอนย้ายสินค้าคงคลัง หน่วยจะถูกดึงมาจากค่าผลิตภัณฑ์ของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fbb4f-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="fbb4f-131">ถ้าค่าถูกพบ ฟิลด์ **หน่วย** จะถูกล็อคในผลิตภัณฑ์การปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fbb4f-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="fbb4f-132">มีการเพิ่มฟิลด์ **ลงรายการบัญชีสถานะ** ไปยังทั้งเอนทิตี **การปรับปรุงสินค้าคงคลัง** และเอนทิตี **การโอนย้ายสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="fbb4f-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="fbb4f-133">ฟิลด์นี้จะใช้เป็นตัวกรองสำหรับเวลาที่มีการส่งการปรับปรุงหรือการโอนย้ายไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fbb4f-133">This field is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="fbb4f-134">ค่าเริ่มต้นสำหรับฟิลด์นี้จะถูกสร้างขึ้น (1) แต่จะไม่ได้ถูกส่งไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fbb4f-134">The default for this field is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="fbb4f-135">เมื่อคุณปรับปรุงค่าที่จะลงรายการบัญชี (2) ค่านั้นจะถูกส่งไปยัง Supply Chain Management แต่หลังจากนั้นคุณจะไม่สามารถเปลี่ยนแปลงสิ่งใดได้ในการปรับปรุงหรือการโอนย้าย หรือเพิ่มรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="fbb4f-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="fbb4f-136">มีการเพิ่มฟิลด์ **ลำดับหมายเลข** ไปยังเอนทิตี **ผลิตภัณฑ์ของการปรับปรุงสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="fbb4f-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="fbb4f-137">ฟิลด์นี้ช่วยให้มั่นใจว่าการรวมมีหมายเลขเฉพาะ เพื่อให้การรวมสามารถสร้างและอัพเดตการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="fbb4f-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="fbb4f-138">เมื่อคุณสร้างผลิตภัณฑ์การปรับปรุงสินค้าคงคลังครั้งแรก จะมีการสร้างเรกคอร์ดใหม่ในเอนทิตี **P2C AutoNumber** เพื่อรักษาชุดหมายเลขและคำนำหน้าที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="fbb4f-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="fbb4f-139">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="fbb4f-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="fbb4f-140">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fbb4f-140">Supply Chain Management</span></span>
<span data-ttu-id="fbb4f-141">สามารถลงรายการบัญชีสมุดรายวันสินค้าคงคลังการรวมที่สร้างขึ้นโดยใช้ชุดงานโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="fbb4f-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="fbb4f-142">นี่จะถูกเปิดใช้งานจาก **การจัดการสินค้าคงคลัง > งานประจำงวด > การรวม CDS > ลงรายการบัญชีสมุดรายวันสินค้าคงคลังการรวม**</span><span class="sxs-lookup"><span data-stu-id="fbb4f-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fbb4f-143">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fbb4f-143">Template mapping in Data integration</span></span>

<span data-ttu-id="fbb4f-144">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fbb4f-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="fbb4f-145">การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Supply Chain Management): การปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fbb4f-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="fbb4f-146">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="fbb4f-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="fbb4f-147">การโอนย้ายสินค้าคงคลัง (Field Service ไปยัง Supply Chain Management): การโอนย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fbb4f-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="fbb4f-148">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="fbb4f-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
