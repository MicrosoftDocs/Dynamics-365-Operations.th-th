---
title: โอนย้ายสินค้าคงคลังที่มีอยู่จริงภายในคลังสินค้า
description: 'ขั้นตอนนี้อธิบายเกี่ยวกับกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการโอนสินค้าคงคลังในใบสั่งไปยังทะเบียนการเคลื่อนย้ายของสินค้าจากสถานที่หนึ่งในคลังสินค้าอื่น '
author: MarkusFogelberg
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 540ba2266ea74c36babce57670f84159c89018f1
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383445"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="cf8b3-103">โอนย้ายสินค้าคงคลังที่มีอยู่จริงภายในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cf8b3-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf8b3-104">ขั้นตอนนี้อธิบายเกี่ยวกับกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการโอนสินค้าคงคลังในใบสั่งไปยังทะเบียนการเคลื่อนย้ายของสินค้าจากสถานที่หนึ่งในคลังสินค้าอื่น </span><span class="sxs-lookup"><span data-stu-id="cf8b3-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="cf8b3-105">คุณจำเป็นต้องมีชื่อสมุดรายวันสินค้าคงคลังที่มีการตั้งค่าสำหรับการโอนย้ายสินค้าคงคลังก่อนที่คุณจะเริ่มการทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="cf8b3-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="cf8b3-106">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF โดยใช้ค่าตัวอย่างที่แสดง หรือคุณสามารถใช้ข้อมูลของคุณเองได้ถ้าคุณได้ตั้งค่าผลิตภัณฑ์และสถานที่แล้ว</span><span class="sxs-lookup"><span data-stu-id="cf8b3-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="cf8b3-107">งานเหล่านี้จะปกติจะดำเนินการโดยพนักงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cf8b3-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="cf8b3-108">สร้างสมุดรายวันการโอนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cf8b3-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="cf8b3-109">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **การบริหารสินค้าคงคลัง > รายการสมุดรายวัน > สินค้า > โอนย้าย**</span><span class="sxs-lookup"><span data-stu-id="cf8b3-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="cf8b3-110">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="cf8b3-110">Click **New**.</span></span>
3. <span data-ttu-id="cf8b3-111">ในฟิลด์ **ชื่อ** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="cf8b3-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="cf8b3-112">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cf8b3-112">Click **OK**.</span></span> <span data-ttu-id="cf8b3-113">มีตัวเลือกในการระบุเป็น 'เริ่มต้น' และ 'สิ้นสุด' มิติสำหรับแต่ละรายการในสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="cf8b3-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="cf8b3-114">สิ่งเหล่านี้มีความจำเป็นสำหรับชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="cf8b3-114">These are essential for this journal type.</span></span> <span data-ttu-id="cf8b3-115">คุณสามารถโอนสิ้นค้าไปยังที่ตั้งที่ใช้กฎที่ต่างกัน</span><span class="sxs-lookup"><span data-stu-id="cf8b3-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="cf8b3-116">ในตัวอย่างนี้ พวกเราจะโอนสินค้าภายในคลังสินค้าเดียวกัน จากสถานที่ที่ควบคุมป้ายทะเบียนไปยังสถานที่ที่ไม่ได้ควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cf8b3-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="cf8b3-117">สร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="cf8b3-117">Create journal lines</span></span>
1. <span data-ttu-id="cf8b3-118">**fastTab รายการสมุดรายวัน** คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="cf8b3-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="cf8b3-119">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cf8b3-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="cf8b3-120">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก 'A0001'</span><span class="sxs-lookup"><span data-stu-id="cf8b3-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="cf8b3-121">ในฟิลด์ **ไซต์ต้นทาง** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cf8b3-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="cf8b3-122">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก '2'</span><span class="sxs-lookup"><span data-stu-id="cf8b3-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="cf8b3-123">ในฟิลด์ **ไซต์ปลายทาง** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cf8b3-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="cf8b3-124">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก '2'</span><span class="sxs-lookup"><span data-stu-id="cf8b3-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="cf8b3-125">ในฟิลด์ **คลังสินค้าต้นทาง** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cf8b3-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="cf8b3-126">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก '24'</span><span class="sxs-lookup"><span data-stu-id="cf8b3-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="cf8b3-127">ในฟิลด์ **คลังสินค้าปลายทาง** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cf8b3-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="cf8b3-128">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก '24'</span><span class="sxs-lookup"><span data-stu-id="cf8b3-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="cf8b3-129">ในฟิลด์ **สถานที่ต้นทาง** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cf8b3-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="cf8b3-130">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก 'FL-001'</span><span class="sxs-lookup"><span data-stu-id="cf8b3-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="cf8b3-131">ในฟิลด์ **สถานที่ปลายทาง** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cf8b3-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="cf8b3-132">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือกสินค้า 'BULK-001'</span><span class="sxs-lookup"><span data-stu-id="cf8b3-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="cf8b3-133">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="cf8b3-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="cf8b3-134">ใน fastTab **รายละเอียดของรายการ** คลิกแท็บ **มิติสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="cf8b3-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="cf8b3-135">ใน **จากมิติสินค้าคงคลัง** ในฟิลด์ **ป้ายทะเบียน** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="cf8b3-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="cf8b3-136">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก '24'</span><span class="sxs-lookup"><span data-stu-id="cf8b3-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="cf8b3-137">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cf8b3-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="cf8b3-138">ลงรายการบัญชีสมุดรายวันการโอนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cf8b3-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="cf8b3-139">ใน **บานหน้าต่างการดำเนินการ** คลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="cf8b3-139">On the **Action Pane**, click **Post**.</span></span>
2. <span data-ttu-id="cf8b3-140">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cf8b3-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="cf8b3-141">ดูธุรกรรมสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cf8b3-141">View inventory transactions</span></span>
1. <span data-ttu-id="cf8b3-142">คลิก **สินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="cf8b3-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="cf8b3-143">คลิก **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="cf8b3-143">Click **Transactions**.</span></span> <span data-ttu-id="cf8b3-144">คุณสามารถดูธุรกรรมที่ถูกสร้างขึ้นเมื่อคุณลงรายการบัญชีสมุดรายวันของคุณ</span><span class="sxs-lookup"><span data-stu-id="cf8b3-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

