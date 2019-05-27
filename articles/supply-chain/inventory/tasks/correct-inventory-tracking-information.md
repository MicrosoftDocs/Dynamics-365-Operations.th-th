---
title: รวบรวมข้อมูลการติดตามสินค้าคงคลัง
description: 'ขั้นตอนนี้นำคุณผ่านกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการโอนสินค้าคงคลังในใบสั่งไปยังทะเบียนการเคลื่อนย้ายของสินค้าจากสถานที่หนึ่งในคลังสินค้าอื่น '
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cfe0f6995598757dcea824e1bb4f7ef8ab54a67b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549943"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="7bb97-103">รวบรวมข้อมูลการติดตามสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7bb97-103">Correct inventory tracking information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7bb97-104">ขั้นตอนนี้นำคุณผ่านกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการโอนสินค้าคงคลังในใบสั่งไปยังทะเบียนการเคลื่อนย้ายของสินค้าจากสถานที่หนึ่งในคลังสินค้าอื่น </span><span class="sxs-lookup"><span data-stu-id="7bb97-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="7bb97-105">ในตัวอย่างนี้ เราจะปรับปรุงข้อมูลของสินค้าที่ถูกควบคุมด้วยชุดงาน โดยการเปลี่ยนชุดงานการลงทะเบียนที่ไม่ถูกต้องไปยังชุดงานอื่น</span><span class="sxs-lookup"><span data-stu-id="7bb97-105">In this example, we’ll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="7bb97-106">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USPI หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="7bb97-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="7bb97-107">ถ้าคุณใช้ข้อมูลของคุณเอง คุณจำเป็นต้องมีสินค้าที่มีการเปิดใช้งานชุดงาน และจะต้องไม่มีการควบคุมที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="7bb97-107">If you use your own data, you need to have an item that’s batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="7bb97-108">คุณยังจำเป็นต้องมีการตั้งค่าชื่อสมุดรายวันสินค้าคงคลังสำหรับการโอนย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7bb97-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="7bb97-109">งานเหล่านี้จะปกติจะดำเนินการโดยพนักงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7bb97-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="7bb97-110">สร้างสมุดรายวันการโอนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7bb97-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="7bb97-111">ไปที่ โอน</span><span class="sxs-lookup"><span data-stu-id="7bb97-111">Go to Transfer.</span></span>
2. <span data-ttu-id="7bb97-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7bb97-112">Click New.</span></span>
3. <span data-ttu-id="7bb97-113">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7bb97-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="7bb97-114">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7bb97-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="7bb97-115">สร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7bb97-115">Create journal lines</span></span>
1. <span data-ttu-id="7bb97-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7bb97-116">Click New.</span></span>
2. <span data-ttu-id="7bb97-117">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7bb97-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="7bb97-118">ถ้าคุณใช้USPI ให้เลือกราการ 'M5003'</span><span class="sxs-lookup"><span data-stu-id="7bb97-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="7bb97-119">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7bb97-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="7bb97-120">คลิก แท็บมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7bb97-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="7bb97-121">ในฟิลด์หมายเลขชุดงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7bb97-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="7bb97-122">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7bb97-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="7bb97-123">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7bb97-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="7bb97-124">ในฟิลด์หมายเลขชุดงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7bb97-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="7bb97-125">ลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7bb97-125">Post the journal</span></span>
1. <span data-ttu-id="7bb97-126">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="7bb97-126">Click Post.</span></span>
2. <span data-ttu-id="7bb97-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7bb97-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="7bb97-128">ตรวจสอบข้อมูลการติดตาม</span><span class="sxs-lookup"><span data-stu-id="7bb97-128">Check tracing information</span></span>
1. <span data-ttu-id="7bb97-129">คลิกสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7bb97-129">Click Inventory.</span></span>
2. <span data-ttu-id="7bb97-130">คลิกการติดตาม</span><span class="sxs-lookup"><span data-stu-id="7bb97-130">Click Trace.</span></span>
3. <span data-ttu-id="7bb97-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7bb97-131">Click OK.</span></span>
    * <span data-ttu-id="7bb97-132">การใช้ข้อมูการติดตามนี้ คุณสามารถสำรองการติดตามซึ่งชุดงานสินค้าคงคลังจากที่แก้ไข </span><span class="sxs-lookup"><span data-stu-id="7bb97-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="7bb97-133">คุณยังสามารถใช้หน้าการติดตามสินค้านี้เพื่อดูข้อมูลได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="7bb97-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="7bb97-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7bb97-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="7bb97-135">ติดตามรายการความเคลื่อนไหวของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7bb97-135">Check inventory transactions</span></span>
1. <span data-ttu-id="7bb97-136">คลิกสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7bb97-136">Click Inventory.</span></span>
2. <span data-ttu-id="7bb97-137">คลิกธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="7bb97-137">Click Transactions.</span></span>
    * <span data-ttu-id="7bb97-138">คุณสามารถดูธุรกรรมที่ถูกสร้างขึ้นเมื่อคุณลงรายการบัญชีสมุดรายวันของคุณ</span><span class="sxs-lookup"><span data-stu-id="7bb97-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

