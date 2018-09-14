--- 
title: "ติดตามสินค้าหรือวัตถุดิบ"
description: "ขั้นตอนนี้แสดงถึงวิธีใช้การติดตามสินค้าเพื่อระบุบสถานที่ของสินค้า หรือวัตถุดิบที่ถูกใช้ หรือกำลังใช้ "
author: pjacobse
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 897a777b3f4ce05fe995aa98a72feb99d82837ef
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="20061-103">ติดตามสินค้าหรือวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="20061-103">Trace an item or raw material</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20061-104">ขั้นตอนนี้แสดงถึงวิธีใช้การติดตามสินค้าเพื่อระบุบสถานที่ของสินค้า หรือวัตถุดิบที่ถูกใช้ หรือกำลังใช้ </span><span class="sxs-lookup"><span data-stu-id="20061-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="20061-105">ด้วยกระบวนงานนี้ คุณสามารถระบุสินค้า ติดตามสินค้ากลับไปยังแหล่งที่มา แล้วติดตามการผลิตไปข้างหน้าผ่านการผลิตและการขายผลิตภัณฑ์สำเร็จรูป </span><span class="sxs-lookup"><span data-stu-id="20061-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="20061-106">ขั้นตอนนี้สามารถนำมาใช้ในการตรวจสอบผลกระทบของลูกค้า ใบสั่งขายที่ได้รับผลกระทบ และอีกมากมาย </span><span class="sxs-lookup"><span data-stu-id="20061-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="20061-107">ขั้นตอนนี้จะใช้ข้อมูลสาธิตบริษัท USP2</span><span class="sxs-lookup"><span data-stu-id="20061-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="20061-108">ติดตามสินค้ากลับมาโดยใช้หมายเลขชุดงานที่รู้จัก</span><span class="sxs-lookup"><span data-stu-id="20061-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="20061-109">ไปที่การบริหารสินค้าคงคลัง > การสอบถามและรายงาน > มิติการติดตาม > การติดตามสินค้า</span><span class="sxs-lookup"><span data-stu-id="20061-109">Go to Inventory management > Inquiries and reports > Tracking dimensions > Item tracing.</span></span>
2. <span data-ttu-id="20061-110">ในฟิลด์หมายเลขสินค้า ให้เลือก 'P9100'</span><span class="sxs-lookup"><span data-stu-id="20061-110">In the Item number field, select P9100.</span></span>
3. <span data-ttu-id="20061-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="20061-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="20061-112">ในฟิลด์ไปข้างหน้า หรือฟิลด์ย้อนหลัง เลือก 'ย้อนหลัง'</span><span class="sxs-lookup"><span data-stu-id="20061-112">In the Forward or backward field, select 'Backward'.</span></span>
5. <span data-ttu-id="20061-113">ในฟิลด์หมายเลขชุดงาน เลือก เป็น-12-344-01</span><span class="sxs-lookup"><span data-stu-id="20061-113">In the Batch number field, select as-12-344-01.</span></span>
6. <span data-ttu-id="20061-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="20061-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="20061-115">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="20061-115">Click OK.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="20061-116">ระบุสินค้า ติดตามไปข้างหน้า และทำการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="20061-116">Identify an item, trace it forward, and make an analysis</span></span>
    * <span data-ttu-id="20061-117">โหนดบนสุดของแผนภูมิแสดงถึงปริมาณคงคลังของสินค้าและชุดงานที่ถูกเลือก </span><span class="sxs-lookup"><span data-stu-id="20061-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="20061-118">คุณต้องขยายโหนดของแผนภูมิ เพื่อค้นหาสินค้าที่มีควรจะมีดำเนินการการติดตามแบบไปข้างหน้า</span><span class="sxs-lookup"><span data-stu-id="20061-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="20061-119">ในแผนภูมิ ให้ขยาย 'โหนดที่อธิบายด้านล่าง แล้วเลือกโหนดสุดท้าย'</span><span class="sxs-lookup"><span data-stu-id="20061-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    * <span data-ttu-id="20061-120">ขยาย: 'P9100 / 1 / 10 / เป็น-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● เบิกสินค้าแล้ว ● ใบสั่งขาย 000072 ● 22 ธันวาคม 2015 ● -1 keg ● -4.00 gal ● ไซต์=1 คลังสินค้า=10 หมายเลขชุดงาน=เป็น-12-344-01  \P9100 ● การผลิต B-000050 ● 9 ธันวาคม 2015● 7 keg ● 27.00 gal ● ไซต์=1 คลังสินค้า=10 หมายเลขชุดงาน=as-12-344-01 ● ผลิตภัณฑ์ร่วม: P9101' แล้วเลือกโหนดนั้น</span><span class="sxs-lookup"><span data-stu-id="20061-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="20061-121">ในแผนภูมิ ให้ขยาย 'โหนดที่อธิบายด้านล่าง แล้วเลือกโหนดนั้น'</span><span class="sxs-lookup"><span data-stu-id="20061-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    * <span data-ttu-id="20061-122">เริ่มต้นจากโหนดที่คุณเพิ่งเลือก ขยาย M9103 ● สายการผลิต 'B-000050 ● 9 ธันวาคม 2015 ● -160.00 ปอนด์ ● ขนาด=70, สี=ตกลง, ไซต์=1, คลังสินค้า=10, หมายเลขชุดงาน=App01' และจากนั้นให้เลือกโหนดนั้น</span><span class="sxs-lookup"><span data-stu-id="20061-122">Starting from the node that you’ve just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="20061-123">คลิก ติดตามจากโหนด</span><span class="sxs-lookup"><span data-stu-id="20061-123">Click Trace from node.</span></span>
4. <span data-ttu-id="20061-124">คลิก ไปข้างหน้า</span><span class="sxs-lookup"><span data-stu-id="20061-124">Click Forward.</span></span>
5. <span data-ttu-id="20061-125">บนบานหน้าต่างการดำเนินการ คลิกการติดตาม</span><span class="sxs-lookup"><span data-stu-id="20061-125">On the Action Pane, click Tracing.</span></span>
    * <span data-ttu-id="20061-126">มีตัวเลือกการติดตามหลายตัวเลือก ที่ให้ข้อมูลเกี่ยวกับลูกค้าที่ได้รับผลกระทบจากสินค้าที่คุณกำลังติดตาม และใบสั่งขายที่เกี่ยวข้องกับสินค้าที่ได้จัดส่งแล้วและยังไม่มีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="20061-126">There are several tracing options which provide information about the customers impacted by the item that you’re tracing, and the sales orders related to the item which have and haven’t been shipped.</span></span>   
6. <span data-ttu-id="20061-127">คลิก ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="20061-127">Click Customers.</span></span>
7. <span data-ttu-id="20061-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="20061-128">Close the page.</span></span>
8. <span data-ttu-id="20061-129">บนบานหน้าต่างการดำเนินการ คลิกการติดตาม</span><span class="sxs-lookup"><span data-stu-id="20061-129">On the Action Pane, click Tracing.</span></span>
9. <span data-ttu-id="20061-130">คลิก ใบสั่งขายที่จัดส่งสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="20061-130">Click Shipped sales orders.</span></span>
10. <span data-ttu-id="20061-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="20061-131">Close the page.</span></span>


