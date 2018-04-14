---
title: "โอนย้ายสินค้าคงคลังที่มีอยู่จริงภายในคลังสินค้า"
description: "ขั้นตอนนี้อธิบายเกี่ยวกับกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการโอนสินค้าคงคลังในใบสั่งไปยังทะเบียนการเคลื่อนย้ายของสินค้าจากสถานที่หนึ่งในคลังสินค้าอื่น "
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 442a608d2f7c7923ec50654d3d96cc429d205537
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="64dd2-103">โอนย้ายสินค้าคงคลังที่มีอยู่จริงภายในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="64dd2-103">Transfer physical inventory within the warehouse</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="64dd2-104">ขั้นตอนนี้อธิบายเกี่ยวกับกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการโอนสินค้าคงคลังในใบสั่งไปยังทะเบียนการเคลื่อนย้ายของสินค้าจากสถานที่หนึ่งในคลังสินค้าอื่น </span><span class="sxs-lookup"><span data-stu-id="64dd2-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="64dd2-105">คุณจำเป็นต้องมีชื่อสมุดรายวันสินค้าคงคลังที่มีการตั้งค่าสำหรับการโอนย้ายสินค้าคงคลังก่อนที่คุณจะเริ่มการทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="64dd2-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="64dd2-106">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF โดยใช้ค่าตัวอย่างที่แสดง หรือคุณสามารถใช้ข้อมูลของคุณเองได้ถ้าคุณได้ตั้งค่าผลิตภัณฑ์และสถานที่แล้ว</span><span class="sxs-lookup"><span data-stu-id="64dd2-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="64dd2-107">งานเหล่านี้จะปกติจะดำเนินการโดยพนักงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="64dd2-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="64dd2-108">สร้างสมุดรายวันการโอนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="64dd2-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="64dd2-109">ไปที่ โอน</span><span class="sxs-lookup"><span data-stu-id="64dd2-109">Go to Transfer.</span></span>
2. <span data-ttu-id="64dd2-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="64dd2-110">Click New.</span></span>
3. <span data-ttu-id="64dd2-111">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="64dd2-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="64dd2-112">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="64dd2-112">Click OK.</span></span>
    * <span data-ttu-id="64dd2-113">มีตัวเลือกในการระบุเป็น 'เริ่มต้น' และ 'สิ้นสุด' มิติสำหรับแต่ละรายการในสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="64dd2-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="64dd2-114">สิ่งเหล่านี้มีความจำเป็นสำหรับชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="64dd2-114">These are essential for this journal type.</span></span> <span data-ttu-id="64dd2-115">คุณสามารถโอนสิ้นค้าไปยังที่ตั้งที่ใช้กฎที่ต่างกัน</span><span class="sxs-lookup"><span data-stu-id="64dd2-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="64dd2-116">ตัวอย่างนี้พวกเราจะโอนสินค้าภายในคลังสินค้าเดียวกัน จากสถานที่ควบคุมป้ายทะเบียนไปยังสถานที่ที่ไม่ได้ควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="64dd2-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="64dd2-117">สร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="64dd2-117">Create journal lines</span></span>
1. <span data-ttu-id="64dd2-118">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="64dd2-118">Click New.</span></span>
2. <span data-ttu-id="64dd2-119">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="64dd2-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="64dd2-120">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก 'A0001'</span><span class="sxs-lookup"><span data-stu-id="64dd2-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="64dd2-121">ในฟิลด์จากไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="64dd2-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="64dd2-122">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก '2'</span><span class="sxs-lookup"><span data-stu-id="64dd2-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="64dd2-123">ในฟิลด์ไปยังไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="64dd2-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="64dd2-124">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก '2'</span><span class="sxs-lookup"><span data-stu-id="64dd2-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="64dd2-125">ในฟิลด์จากคลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="64dd2-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="64dd2-126">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก '24'</span><span class="sxs-lookup"><span data-stu-id="64dd2-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="64dd2-127">ในฟิลด์ไปยังคลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="64dd2-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="64dd2-128">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก '24'</span><span class="sxs-lookup"><span data-stu-id="64dd2-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="64dd2-129">ในฟิลด์จากที่ตั้ง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="64dd2-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="64dd2-130">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก 'FL-001'</span><span class="sxs-lookup"><span data-stu-id="64dd2-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="64dd2-131">ในฟิลด์ไปยังที่ตั้ง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="64dd2-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="64dd2-132">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือกสินค้า 'BULK-001'</span><span class="sxs-lookup"><span data-stu-id="64dd2-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="64dd2-133">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="64dd2-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="64dd2-134">คลิก แท็บมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="64dd2-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="64dd2-135">ในฟิลด์ป้ายทะเบียน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="64dd2-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="64dd2-136">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก '24'</span><span class="sxs-lookup"><span data-stu-id="64dd2-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="64dd2-137">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="64dd2-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="64dd2-138">ลงรายการบัญชีสมุดรายวันการโอนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="64dd2-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="64dd2-139">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="64dd2-139">Click Post.</span></span>
2. <span data-ttu-id="64dd2-140">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="64dd2-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="64dd2-141">ดูธุรกรรมสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="64dd2-141">View inventory transactions</span></span>
1. <span data-ttu-id="64dd2-142">คลิกสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="64dd2-142">Click Inventory.</span></span>
2. <span data-ttu-id="64dd2-143">คลิกธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="64dd2-143">Click Transactions.</span></span>
    * <span data-ttu-id="64dd2-144">คุณสามารถดูธุรกรรมที่ถูกสร้างขึ้นเมื่อคุณลงรายการบัญชีสมุดรายวันของคุณ</span><span class="sxs-lookup"><span data-stu-id="64dd2-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

