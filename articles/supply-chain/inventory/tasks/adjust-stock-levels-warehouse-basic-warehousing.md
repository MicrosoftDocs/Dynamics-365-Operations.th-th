---
title: ปรับปรุงระดับปริมาณสินค้าคงคลังในคลังสินค้า (คลังสินค้าพื้นฐาน)
description: 'กระบวนงานนี้นำคุณผ่านกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการปรับปรุงสินค้าคงคลังเพื่อปรับปรุงระดับสินค้าคงคลังของผลิตภัณฑ์ในคลังสินค้า '
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9678dffd84e9e4032510811731a67da953b40431
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204274"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="9f348-103">ปรับปรุงระดับปริมาณสินค้าคงคลังในคลังสินค้า (คลังสินค้าพื้นฐาน)</span><span class="sxs-lookup"><span data-stu-id="9f348-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f348-104">กระบวนงานนี้นำคุณผ่านกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการปรับปรุงสินค้าคงคลังเพื่อปรับปรุงระดับสินค้าคงคลังของผลิตภัณฑ์ในคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="9f348-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="9f348-105">คุณจำเป็นต้องมีชื่อสมุดรายวันสินค้าคงคลังที่ตั้งค่าสำหรับการปรับปรุงสินค้าคงคลัง ก่อนที่คุณจะเริ่มต้นนี้ </span><span class="sxs-lookup"><span data-stu-id="9f348-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="9f348-106">คุณสามารถดำเนินการขั้นตอนนี้ได้ในข้อมูลสาธิตของบริษัท USMF หรือการใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="9f348-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="9f348-107">งานเหล่านี้จะปกติจะดำเนินการโดยพนักงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="9f348-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="9f348-108">สร้างสมุดรายวันการปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="9f348-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="9f348-109">ไปที่ การบริหารสินค้าคงคลัง > รายการสมุดบันทึกรายวัน > สินค้า > การปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="9f348-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="9f348-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9f348-110">Click New.</span></span>
3. <span data-ttu-id="9f348-111">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="9f348-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9f348-112">ในรายการ คลิก ชื่อสมุดรายวันการปรับปรุงสินค้าคงคลังที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="9f348-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="9f348-113">บางฟิลด์อื่นๆ จะถูกเติมข้อมูลตามการตั้งค่าของชื่อสมุดรายวันการปรับปรุงสินค้าคงคลังที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="9f348-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="9f348-114">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9f348-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="9f348-115">สร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="9f348-115">Create journal lines</span></span>
1. <span data-ttu-id="9f348-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9f348-116">Click New.</span></span>
2. <span data-ttu-id="9f348-117">ในรายการ ทำเครื่องหมายที่ฟิลด์หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="9f348-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="9f348-118">ในฟิลด์หมายเลขสินค้า เลือกสินค้า </span><span class="sxs-lookup"><span data-stu-id="9f348-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="9f348-119">ถ้าคุณกำลังใช้ข้อมูลสาธิตของบริษัท USMF ชนิด 'D0001'</span><span class="sxs-lookup"><span data-stu-id="9f348-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="9f348-120">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="9f348-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9f348-121">ในรายการ เลือก ไซต์</span><span class="sxs-lookup"><span data-stu-id="9f348-121">In the list, select a site.</span></span>
6. <span data-ttu-id="9f348-122">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="9f348-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9f348-123">ในรายการ เลือก คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="9f348-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="9f348-124">ถ้าคุณได้เลือกสินค้าทีมีตำแหน่งที่ตั้งเป็นมิติบังคับ คุณจะต้องระบุตำแหน่งที่ตั้งที่นี่</span><span class="sxs-lookup"><span data-stu-id="9f348-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="9f348-125">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="9f348-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9f348-126">ฟิลด์ราคาต้นทุนระบุต้นทุนต่อหน่วยสำหรับการรับสต็อก </span><span class="sxs-lookup"><span data-stu-id="9f348-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="9f348-127">ถ้าไม่ระบุต้นทุนสำหรับหมายเลขสินค้า หรือถ้าคุณต้องการเปลี่ยนแปลงต้นทุนด้วยตนเอง คุณควรทำ ณ ที่นี่</span><span class="sxs-lookup"><span data-stu-id="9f348-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="9f348-128">ตรวจสอบความถูกต้องและลงรายการบัญชีสมุดการปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="9f348-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="9f348-129">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9f348-129">Click Validate.</span></span>
2. <span data-ttu-id="9f348-130">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9f348-130">Click OK.</span></span>
3. <span data-ttu-id="9f348-131">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="9f348-131">Click Post.</span></span>
    * <span data-ttu-id="9f348-132">เมื่อคุณลงรายการบัญชีสมุดรายวันชนิดนี้ การรับสินค้าคงคลังหรือการตัดสินค้าจากคลังจะถูกลงรายการบัญชี มีการเปลี่ยนแปลงระดับและมูลค่าสินค้าคงคลัง และมีการสร้างธุรกรรมบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="9f348-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="9f348-133">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9f348-133">Click OK.</span></span>
5. <span data-ttu-id="9f348-134">ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="9f348-134">Close the form.</span></span>
6. <span data-ttu-id="9f348-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9f348-135">Close the page.</span></span>

