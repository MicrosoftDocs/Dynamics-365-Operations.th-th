---
title: "ปรับปรุงระดับปริมาณสินค้าคงคลังในคลังสินค้า (คลังสินค้าพื้นฐาน)"
description: "กระบวนงานนี้นำคุณผ่านกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการปรับปรุงสินค้าคงคลังเพื่อปรับปรุงระดับสินค้าคงคลังของผลิตภัณฑ์ในคลังสินค้า "
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 0694ba1c69697e745f75db856bdc5b38454a68dc
ms.contentlocale: th-th
ms.lasthandoff: 01/17/2018

---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="b7663-103">ปรับปรุงระดับปริมาณสินค้าคงคลังในคลังสินค้า (คลังสินค้าพื้นฐาน)</span><span class="sxs-lookup"><span data-stu-id="b7663-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b7663-104">กระบวนงานนี้นำคุณผ่านกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการปรับปรุงสินค้าคงคลังเพื่อปรับปรุงระดับสินค้าคงคลังของผลิตภัณฑ์ในคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="b7663-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="b7663-105">คุณจำเป็นต้องมีชื่อสมุดรายวันสินค้าคงคลังที่ตั้งค่าสำหรับการปรับปรุงสินค้าคงคลัง ก่อนที่คุณจะเริ่มต้นนี้ </span><span class="sxs-lookup"><span data-stu-id="b7663-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="b7663-106">คุณสามารถดำเนินการขั้นตอนนี้ได้ในข้อมูลสาธิตของบริษัท USMF หรือการใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="b7663-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="b7663-107">งานเหล่านี้จะปกติจะดำเนินการโดยพนักงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="b7663-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="b7663-108">สร้างสมุดรายวันการปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b7663-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="b7663-109">ไปที่ การบริหารสินค้าคงคลัง > รายการสมุดบันทึกรายวัน > สินค้า > การปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b7663-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="b7663-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b7663-110">Click New.</span></span>
3. <span data-ttu-id="b7663-111">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b7663-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b7663-112">ในรายการ คลิก ชื่อสมุดรายวันการปรับปรุงสินค้าคงคลังที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="b7663-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="b7663-113">บางฟิลด์อื่นๆ จะถูกเติมข้อมูลตามการตั้งค่าของชื่อสมุดรายวันการปรับปรุงสินค้าคงคลังที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="b7663-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="b7663-114">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b7663-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="b7663-115">สร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="b7663-115">Create journal lines</span></span>
1. <span data-ttu-id="b7663-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b7663-116">Click New.</span></span>
2. <span data-ttu-id="b7663-117">ในรายการ ทำเครื่องหมายที่ฟิลด์หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="b7663-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="b7663-118">ในฟิลด์หมายเลขสินค้า เลือกสินค้า </span><span class="sxs-lookup"><span data-stu-id="b7663-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="b7663-119">ถ้าคุณกำลังใช้ข้อมูลสาธิตของบริษัท USMF ชนิด 'D0001'</span><span class="sxs-lookup"><span data-stu-id="b7663-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="b7663-120">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b7663-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b7663-121">ในรายการ เลือก ไซต์</span><span class="sxs-lookup"><span data-stu-id="b7663-121">In the list, select a site.</span></span>
6. <span data-ttu-id="b7663-122">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b7663-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b7663-123">ในรายการ เลือก คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="b7663-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="b7663-124">ถ้าคุณได้เลือกสินค้าทีมีตำแหน่งที่ตั้งเป็นมิติบังคับ คุณจะต้องระบุตำแหน่งที่ตั้งที่นี่</span><span class="sxs-lookup"><span data-stu-id="b7663-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="b7663-125">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b7663-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b7663-126">ฟิลด์ราคาต้นทุนระบุต้นทุนต่อหน่วยสำหรับการรับสต็อก </span><span class="sxs-lookup"><span data-stu-id="b7663-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="b7663-127">ถ้าไม่ระบุต้นทุนสำหรับหมายเลขสินค้า หรือถ้าคุณต้องการเปลี่ยนแปลงต้นทุนด้วยตนเอง คุณควรทำ ณ ที่นี่</span><span class="sxs-lookup"><span data-stu-id="b7663-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="b7663-128">ตรวจสอบความถูกต้องและลงรายการบัญชีสมุดการปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b7663-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="b7663-129">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b7663-129">Click Validate.</span></span>
2. <span data-ttu-id="b7663-130">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b7663-130">Click OK.</span></span>
3. <span data-ttu-id="b7663-131">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="b7663-131">Click Post.</span></span>
    * <span data-ttu-id="b7663-132">เมื่อคุณลงรายการบัญชีสมุดรายวันชนิดนี้ การรับสินค้าคงคลังหรือการตัดสินค้าจากคลังจะถูกลงรายการบัญชี มีการเปลี่ยนแปลงระดับและมูลค่าสินค้าคงคลัง และมีการสร้างธุรกรรมบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="b7663-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="b7663-133">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b7663-133">Click OK.</span></span>
5. <span data-ttu-id="b7663-134">ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="b7663-134">Close the form.</span></span>
6. <span data-ttu-id="b7663-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b7663-135">Close the page.</span></span>

