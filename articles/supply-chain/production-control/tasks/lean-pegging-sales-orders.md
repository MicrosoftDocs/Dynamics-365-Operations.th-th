---
title: การจำแนกประเภทแบบ Lean จากใบสั่งขาย
description: กระบวนงานนี้เน้นไปที่ การตรวจสอบความถูกต้องของแผนภูมิการเชื่อมโยงความต้องการกับการจัดซื้อจากรายการขายที่ซึ่งสินค้าถูกผลิตด้วยคัมบัง
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457e7128bed2232a3e092b31136f768940482741
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994190"
---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="252d9-103">การจำแนกประเภทแบบ Lean จากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="252d9-103">Lean pegging from sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="252d9-104">กระบวนงานนี้เน้นไปที่ การตรวจสอบความถูกต้องของแผนภูมิการเชื่อมโยงความต้องการกับการจัดซื้อจากรายการขายที่ซึ่งสินค้าถูกผลิตด้วยคัมบัง </span><span class="sxs-lookup"><span data-stu-id="252d9-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="252d9-105">หลังจากการตรวจสอบความถูกต้องของแผนภูมิการเชื่อมโยงความต้องการกับการจัดซื้อ งานคัมบังทั้งหมดจะถูกวางแผน </span><span class="sxs-lookup"><span data-stu-id="252d9-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="252d9-106">สิ่งนี้เป็นประโยชน์สำหรับสถานการณ์จำลองของใบสั่งที่เป็นผู้รับใบสั่งต้องแน่ใจว่า การผลิตจะสามารถเริ่มได้ทันที </span><span class="sxs-lookup"><span data-stu-id="252d9-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="252d9-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="252d9-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="252d9-108">กระบวนงานนี้มีไว้สำหรับผู้รับใบสั่งขั้นสูงที่ทำงานในบริษัทแบบ Lean</span><span class="sxs-lookup"><span data-stu-id="252d9-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="252d9-109">สร้างใบสั่งขายสำหรับสินค้าที่มีคัมบังควบคุม</span><span class="sxs-lookup"><span data-stu-id="252d9-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="252d9-110">ไปที่ใบสั่งขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="252d9-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="252d9-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="252d9-111">Click New.</span></span>
3. <span data-ttu-id="252d9-112">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="252d9-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="252d9-113">ใช้ สหรัฐอเมริกา-001</span><span class="sxs-lookup"><span data-stu-id="252d9-113">Use US-001.</span></span>  
4. <span data-ttu-id="252d9-114">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="252d9-114">Click OK.</span></span>
5. <span data-ttu-id="252d9-115">ในฟิลด์ หมายเลขสินค้า ให้พิมพ์ 'L0001'</span><span class="sxs-lookup"><span data-stu-id="252d9-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="252d9-116">กำหนดปริมาณเป็น '30'</span><span class="sxs-lookup"><span data-stu-id="252d9-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="252d9-117">เป็นเรื่องสำคัญที่ว่า ปริมาณมีค่าสูงกว่า 24 เพื่อทริกเกอร์กฎคัมบังของเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="252d9-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="252d9-118">เปิดแผนภูมิการเชื่อมโยงความต้องการกับการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="252d9-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="252d9-119">คลิกที่ผลิตภัณฑ์และการจัดหาวัสดุ</span><span class="sxs-lookup"><span data-stu-id="252d9-119">Click Product and supply.</span></span>
2. <span data-ttu-id="252d9-120">คลิกดูแผนภูมิการเชื่อมโยงความต้องการกับการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="252d9-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="252d9-121">โปรดสังเกตว่า แผนภูมิการเชื่อมโยงความต้องการกับการจัดซื้อแสดงระดับทั้งหมดของการเชื่อมโยงความต้องการกับการจัดซื้อที่จำเป็นสำหรับรายการใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="252d9-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="252d9-122">ในกรณีนี้ มีคัมบังสองระดับและส่วนประกอบที่จำเป็นทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="252d9-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="252d9-123">วางแผนแผนภูมิการเชื่อมโยงความต้องการกับการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="252d9-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="252d9-124">ในแผนภูมิ ให้เลือก ' รายการขาย 000832\Kanban 000558'</span><span class="sxs-lookup"><span data-stu-id="252d9-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="252d9-125">ขยายส่วนงานคัมบัง</span><span class="sxs-lookup"><span data-stu-id="252d9-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="252d9-126">โปรดสังเกตว่า สถานะงานสำหรับงานคัมบังคือ ไม่ได้วางแผน</span><span class="sxs-lookup"><span data-stu-id="252d9-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="252d9-127">คลิกการวางแผนแผนภูมิการเชื่อมโยงความต้องการกับการจัดซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="252d9-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="252d9-128">นี่จะเป็นการวางแผนงานคัมบังทั้งหมดในแผนภูมิการเชื่อมโยงความต้องการกับการจัดซื้อ ซึ่งเปลี่ยนสถานะงานจาก ไม่ได้วางแผน เป็น วางแผนแล้ว</span><span class="sxs-lookup"><span data-stu-id="252d9-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="252d9-129">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="252d9-129">Refresh the page.</span></span>
    * <span data-ttu-id="252d9-130">โปรดสังเกตว่า สถานะของงานคัมบังได้เปลี่ยนแปลงจาก ไม่ได้วางแผน เป็น วางแผนแล้ว</span><span class="sxs-lookup"><span data-stu-id="252d9-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="252d9-131">ในแผนภูมิ ให้เลือก 'รายการขาย 000832\Kanban 000558\Issue สำหรับ L0001\Kanban 000559'</span><span class="sxs-lookup"><span data-stu-id="252d9-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="252d9-132">งานสำหรับคัมบังที่สองมีการวางแผนแล้วเช่นกัน เนื่องจากมีการวางแผนภูมิการเชื่อมโยงความต้องการกับการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="252d9-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="252d9-133">สังเกตว่าสถานะของงานคัมบังจะเปลี่ยนจาก ไม่ได้วางแผน เป็น วางแผนแล้ว</span><span class="sxs-lookup"><span data-stu-id="252d9-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  

