---
title: นับจำนวนสินค้าคงคลังในคลังสินค้า
description: 'ขั้นตอนนี้นำคุณไปสู่กระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการตรวจนับสินค้าคงคลังในใบสั่งที่นับสินค้าเฉพาะที่สถานที่ในคลังสินค้า '
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549931"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="a81f2-103">นับจำนวนสินค้าคงคลังในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a81f2-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a81f2-104">ขั้นตอนนี้นำคุณไปสู่กระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการตรวจนับสินค้าคงคลังในใบสั่งที่นับสินค้าเฉพาะที่สถานที่ในคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="a81f2-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="a81f2-105">กระบวนงานดังกล่าวใช้กับฟังก์ชัน "คลังสินค้าพื้นฐาน" ซึ่งอยู่ในโมดูลการจัดการสินค้าคงคลัง และไม่ใช้กับฟังก์ชันคลังสินค้าที่อยู่ในโมดูลการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a81f2-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="a81f2-106">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="a81f2-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="a81f2-107">ถ้าคุณกำลังใช้ข้อมูลของคุณเอง โปรดตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าผลิตภัณฑ์และสถานที่แล้ว และคุณได้สร้างชื่อสมุดรายวันสินค้าคงคลังสำหรับสมุดรายวันการตรวจนับแล้ว</span><span class="sxs-lookup"><span data-stu-id="a81f2-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="a81f2-108">การนับสินค้าคงคลังจะดำเนินการปกติโดยพนักงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a81f2-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="a81f2-109">สร้างสมุดรายวันการตรวจนับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a81f2-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="a81f2-110">ไปที่ การบริหารสินค้าคงคลัง > รายการสมุดรายวัน > การนับสินค้า > การนับ</span><span class="sxs-lookup"><span data-stu-id="a81f2-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="a81f2-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="a81f2-111">Click New.</span></span>
3. <span data-ttu-id="a81f2-112">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a81f2-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a81f2-113">ในรายการ คลิกชื่อสมุดรายวันการตรวจนับสินค้าคงคลังที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="a81f2-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="a81f2-114">บางฟิลด์อื่นๆ จะถูกเติมข้อมูลตามการตั้งค่าของชื่อสมุดรายวันการตรวจนับสินค้าคงคลังที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="a81f2-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="a81f2-115">ในฟิลด์ผู้ปฏิบัติงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a81f2-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a81f2-116">ในรายการ ให้เลือกผู้ปฏิบัติงานที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="a81f2-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="a81f2-117">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="a81f2-117">Click Select.</span></span>
8. <span data-ttu-id="a81f2-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="a81f2-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="a81f2-119">สร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a81f2-119">Create journal lines</span></span>
1. <span data-ttu-id="a81f2-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="a81f2-120">Click New.</span></span>
2. <span data-ttu-id="a81f2-121">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a81f2-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a81f2-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a81f2-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a81f2-123">ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USMF เลือก 'A0001'</span><span class="sxs-lookup"><span data-stu-id="a81f2-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="a81f2-124">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a81f2-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a81f2-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a81f2-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a81f2-126">ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USMF เลือกไซต์ '2'</span><span class="sxs-lookup"><span data-stu-id="a81f2-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="a81f2-127">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a81f2-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a81f2-128">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a81f2-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a81f2-129">ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USMF เลือกคลังสินค้า '24'</span><span class="sxs-lookup"><span data-stu-id="a81f2-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="a81f2-130">ในฟิลด์ตำแหน่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a81f2-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a81f2-131">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a81f2-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a81f2-132">ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USMF เลือกสถานที่ 'BULK-001'</span><span class="sxs-lookup"><span data-stu-id="a81f2-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="a81f2-133">ในฟิลด์ตรวจนับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="a81f2-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="a81f2-134">ถ้าคุณป้อนหมายเลขการตรวจนับที่แตกต่างกับหมายเลขที่แสดงในฟิลด์คงคลังคงเหลือ ฟิลด์ปริมาณจะถูกอัพเดทเพื่อแสดงความขัดแย้ง</span><span class="sxs-lookup"><span data-stu-id="a81f2-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="a81f2-135">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="a81f2-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="a81f2-136">ลงรายการบัญชีสมุดรายวันการตรวจนับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a81f2-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="a81f2-137">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="a81f2-137">Click Post.</span></span>
    * <span data-ttu-id="a81f2-138">เมื่อคุณลงรายการบัญชีสมุดรายวันการตรวจนับสินค้าคงคลัง ถ้าจำนวนที่ตรวจนับแล้วแตกต่างจากจำนวนที่รายงานในฟิลด์สินค้าคงคลังคงเหลือการรับสินค้าสินค้าคงคลัง หรือตัดสินค้าจากคลังได้ลงถูกรายการบัญชี ระดับสินค้าคงคลังและค่าจะถูกเปลี่ยน และบัญชีแยกประเภทธุรกรรมจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a81f2-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="a81f2-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="a81f2-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="a81f2-140">ดูธุรกรรมสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a81f2-140">View inventory transactions</span></span>
1. <span data-ttu-id="a81f2-141">คลิกสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a81f2-141">Click Inventory.</span></span>
2. <span data-ttu-id="a81f2-142">คลิกธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="a81f2-142">Click Transactions.</span></span>
    * <span data-ttu-id="a81f2-143">ที่นี่คุณสามารถดูธุรกรรมที่เกี่ยวข้องใดๆ ซึ่งจะถูกสร้างเมื่อคุณลงรายการบัญชีในสมุดรายวันการตรวจนับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a81f2-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

