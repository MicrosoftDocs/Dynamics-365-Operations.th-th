---
title: รวบรวมข้อมูลการติดตามสินค้าคงคลัง
description: 'ขั้นตอนนี้นำคุณผ่านกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการโอนสินค้าคงคลังในใบสั่งไปยังทะเบียนการเคลื่อนย้ายของสินค้าจากสถานที่หนึ่งในคลังสินค้าอื่น '
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76e73f10df5bb520b6d0d787eda08053a5e33c81
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223421"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="21476-103">รวบรวมข้อมูลการติดตามสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="21476-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21476-104">ขั้นตอนนี้นำคุณผ่านกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการโอนสินค้าคงคลังในใบสั่งไปยังทะเบียนการเคลื่อนย้ายของสินค้าจากสถานที่หนึ่งในคลังสินค้าอื่น </span><span class="sxs-lookup"><span data-stu-id="21476-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="21476-105">ในตัวอย่างนี้ เราจะปรับปรุงข้อมูลของสินค้าที่ถูกควบคุมด้วยชุดงาน โดยการเปลี่ยนชุดงานที่ลงทะเบียนอย่างไม่ถูกต้องไปยังชุดงานอื่น</span><span class="sxs-lookup"><span data-stu-id="21476-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="21476-106">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USPI หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="21476-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="21476-107">ถ้าคุณใช้ข้อมูลของคุณเอง คุณจำเป็นต้องมีสินค้าที่มีการเปิดใช้งานชุดงาน และจะต้องไม่มีการควบคุมสถานที่</span><span class="sxs-lookup"><span data-stu-id="21476-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="21476-108">คุณยังจำเป็นต้องมีการตั้งค่าชื่อสมุดรายวันสินค้าคงคลังสำหรับการโอนย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="21476-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="21476-109">งานเหล่านี้จะปกติจะดำเนินการโดยพนักงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="21476-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="21476-110">สร้างสมุดรายวันการโอนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="21476-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="21476-111">ไปที่ โอน</span><span class="sxs-lookup"><span data-stu-id="21476-111">Go to Transfer.</span></span>
2. <span data-ttu-id="21476-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="21476-112">Click New.</span></span>
3. <span data-ttu-id="21476-113">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="21476-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="21476-114">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="21476-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="21476-115">สร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="21476-115">Create journal lines</span></span>
1. <span data-ttu-id="21476-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="21476-116">Click New.</span></span>
2. <span data-ttu-id="21476-117">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="21476-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="21476-118">ถ้าคุณใช้USPI ให้เลือกราการ 'M5003'</span><span class="sxs-lookup"><span data-stu-id="21476-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="21476-119">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="21476-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="21476-120">คลิก แท็บมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="21476-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="21476-121">ในฟิลด์หมายเลขชุดงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="21476-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="21476-122">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="21476-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="21476-123">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="21476-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="21476-124">ในฟิลด์หมายเลขชุดงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="21476-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="21476-125">ลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="21476-125">Post the journal</span></span>
1. <span data-ttu-id="21476-126">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="21476-126">Click Post.</span></span>
2. <span data-ttu-id="21476-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="21476-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="21476-128">ตรวจสอบข้อมูลการติดตาม</span><span class="sxs-lookup"><span data-stu-id="21476-128">Check tracing information</span></span>
1. <span data-ttu-id="21476-129">คลิกสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="21476-129">Click Inventory.</span></span>
2. <span data-ttu-id="21476-130">คลิกการติดตาม</span><span class="sxs-lookup"><span data-stu-id="21476-130">Click Trace.</span></span>
3. <span data-ttu-id="21476-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="21476-131">Click OK.</span></span>
    * <span data-ttu-id="21476-132">การใช้ข้อมูการติดตามนี้ คุณสามารถสำรองการติดตามซึ่งชุดงานสินค้าคงคลังจากที่แก้ไข </span><span class="sxs-lookup"><span data-stu-id="21476-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="21476-133">คุณยังสามารถใช้หน้าการติดตามสินค้านี้เพื่อดูข้อมูลได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="21476-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="21476-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="21476-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="21476-135">ติดตามรายการความเคลื่อนไหวของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="21476-135">Check inventory transactions</span></span>
1. <span data-ttu-id="21476-136">คลิกสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="21476-136">Click Inventory.</span></span>
2. <span data-ttu-id="21476-137">คลิกธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="21476-137">Click Transactions.</span></span>
    * <span data-ttu-id="21476-138">คุณสามารถดูธุรกรรมที่ถูกสร้างขึ้นเมื่อคุณลงรายการบัญชีสมุดรายวันของคุณ</span><span class="sxs-lookup"><span data-stu-id="21476-138">Here you can see the transactions that were created when you posted your journal.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]