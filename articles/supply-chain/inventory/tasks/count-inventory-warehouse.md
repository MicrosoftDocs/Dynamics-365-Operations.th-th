---
title: นับจำนวนสินค้าคงคลังในคลังสินค้า
description: หัวข้อนี้อธิบายกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการตรวจนับสินค้าคงคลัง เพื่อนับสินค้าเฉพาะที่สถานที่ในคลังสินค้า
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a7f85cb91f36004a6bd6da714e7baa460a83a66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000116"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="581d0-103">นับจำนวนสินค้าคงคลังในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="581d0-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="581d0-104">หัวข้อนี้อธิบายกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการตรวจนับสินค้าคงคลัง เพื่อนับสินค้าเฉพาะที่สถานที่ในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="581d0-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="581d0-105">กระบวนงานดังกล่าวใช้กับฟังก์ชัน "คลังสินค้าพื้นฐาน" ซึ่งพร้อมใช้งานในโมดูลการจัดการสินค้าคงคลัง และไม่ใช้กับฟังก์ชันคลังสินค้าที่พร้อมใช้งานในโมดูลการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="581d0-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="581d0-106">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="581d0-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="581d0-107">ถ้าคุณกำลังใช้ข้อมูลของคุณเอง โปรดตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าผลิตภัณฑ์และสถานที่แล้ว และคุณได้สร้างชื่อสมุดรายวันสินค้าคงคลังสำหรับสมุดรายวันการตรวจนับแล้ว</span><span class="sxs-lookup"><span data-stu-id="581d0-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="581d0-108">การนับสินค้าคงคลังจะดำเนินการปกติโดยพนักงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="581d0-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="581d0-109">สร้างสมุดรายวันการตรวจนับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="581d0-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="581d0-110">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการสินค้าคงคลัง > รายการสมุดรายวัน > การนับสินค้า > การนับ**</span><span class="sxs-lookup"><span data-stu-id="581d0-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="581d0-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="581d0-111">Select **New**.</span></span>
3. <span data-ttu-id="581d0-112">ในฟิลด์ **ชื่อ** ให้เลือกชื่อสมุดรายวันการตรวจนับสินค้าคงคลังที่คุณต้องการใช้จากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="581d0-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="581d0-113">บางฟิลด์อื่นๆ จะถูกเติมข้อมูลตามการตั้งค่าของชื่อสมุดรายวันการตรวจนับสินค้าคงคลังที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="581d0-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="581d0-114">ในฟิลด์ **ผู้ปฏิบัติงาน** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="581d0-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="581d0-115">ในรายการ **เลือก** ผู้ปฏิบัติงานที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="581d0-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="581d0-116">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="581d0-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="581d0-117">สร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="581d0-117">Create journal lines</span></span>
1. <span data-ttu-id="581d0-118">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="581d0-118">Select **New**.</span></span>
2. <span data-ttu-id="581d0-119">ในฟิลด์ **หมายเลขสินค้า** ให้เลือกเรกคอร์ดที่ต้องการจากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="581d0-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="581d0-120">ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USMF เลือก **A0001**</span><span class="sxs-lookup"><span data-stu-id="581d0-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="581d0-121">ในฟิลด์ **ไซต์** ให้เลือกเรกคอร์ดที่ต้องการจากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="581d0-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="581d0-122">ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USMF เลือกไซต์ **2**</span><span class="sxs-lookup"><span data-stu-id="581d0-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="581d0-123">ในฟิลด์ **คลังสินค้า** ให้เลือกเรกคอร์ดที่ต้องการจากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="581d0-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="581d0-124">ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USMF เลือกคลังสินค้า **24**</span><span class="sxs-lookup"><span data-stu-id="581d0-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="581d0-125">ในฟิลด์ **สถานที่** ให้เลือกเรกคอร์ดที่ต้องการจากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="581d0-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="581d0-126">ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USMF เลือกสถานที่ **BULK-001**</span><span class="sxs-lookup"><span data-stu-id="581d0-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="581d0-127">ในฟิลด์ตรวจนับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="581d0-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="581d0-128">ถ้าคุณป้อนจำนวนที่ตรวจนับที่แตกต่างกับจำนวนที่แสดงในฟิลด์ **คงคลังคงเหลือ** ฟิลด์ **ปริมาณ** จะถูกปรับปรุงเพื่อแสดงความขัดแย้ง</span><span class="sxs-lookup"><span data-stu-id="581d0-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="581d0-129">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="581d0-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="581d0-130">ลงรายการบัญชีสมุดรายวันการตรวจนับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="581d0-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="581d0-131">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="581d0-131">Select **Post**.</span></span> <span data-ttu-id="581d0-132">เมื่อคุณลงรายการบัญชีสมุดรายวันการตรวจนับสินค้าคงคลัง ถ้าจำนวนที่ตรวจนับแตกต่างจากจำนวนที่รายงานในฟิลด์ **คงคลังคงเหลือ** การรับสินค้าสินค้าคงคลัง หรือการตัดสินค้าจากคลังจะลงถูกรายการบัญชี ระดับสินค้าคงคลังและค่าจะถูกเปลี่ยน และธุรกรรมบัญชีแยกประเภทจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="581d0-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="581d0-133">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="581d0-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="581d0-134">ดูธุรกรรมสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="581d0-134">View inventory transactions</span></span>
1. <span data-ttu-id="581d0-135">เลือก **สินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="581d0-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="581d0-136">เลือก **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="581d0-136">Select **Transactions**.</span></span> <span data-ttu-id="581d0-137">ที่นี่คุณสามารถดูธุรกรรมที่เกี่ยวข้องใดๆ ซึ่งจะถูกสร้างเมื่อคุณลงรายการบัญชีในสมุดรายวันการตรวจนับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="581d0-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

