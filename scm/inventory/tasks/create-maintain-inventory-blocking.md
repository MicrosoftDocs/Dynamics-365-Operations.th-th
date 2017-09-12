---
title: "สร้างและรักษาการบล็อคสินค้าคงคลัง"
description: "ขั้นตอนนี้แสดงวิธีการป้องกันสินค้าคงคลังคงเหลือทางกายภาพจากการสำรองไว้โดยเอกสารต้นทางขาออกอื่น ๆ โดยใช้การบล็อคสินค้าคงคลัง "
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: th-th
ms.lasthandoff: 09/12/2017

---
# <a name="create-and-maintain-inventory-blocking"></a><span data-ttu-id="b63ce-103">สร้างและรักษาการบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b63ce-103">Create and maintain inventory blocking</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b63ce-104">ขั้นตอนนี้แสดงวิธีการป้องกันสินค้าคงคลังคงเหลือทางกายภาพจากการสำรองไว้โดยเอกสารต้นทางขาออกอื่น ๆ โดยใช้การบล็อคสินค้าคงคลัง </span><span class="sxs-lookup"><span data-stu-id="b63ce-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="b63ce-105">คุณสามารถรันกระบวนการในข้อมูลสาธิตบริษัท USMF โดยใช้ค่าตัวอย่างที่จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="b63ce-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="b63ce-106">คุณต้องมีสินค้าคงคลังคงเหลือทางกายภาพพร้อมใช้งานก่อนที่คุณเริ่มกระบวนการนี้</span><span class="sxs-lookup"><span data-stu-id="b63ce-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="b63ce-107">สร้างการบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b63ce-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="b63ce-108">ไปยังการบริหารสินค้าคงคลัง > งานประจำงวด > การบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b63ce-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="b63ce-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b63ce-109">Click New.</span></span>
3. <span data-ttu-id="b63ce-110">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b63ce-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b63ce-111">ในรายการ ให้เลือกสินค้าที่คุณต้องการเลือก</span><span class="sxs-lookup"><span data-stu-id="b63ce-111">In the list, select the item you want to choose.</span></span>
    * <span data-ttu-id="b63ce-112">เลือกหมายเลขสินค้ากับสินค้าคงคลังคงเหลือที่มีอยู่จริงที่คุณต้องการบล็อค </span><span class="sxs-lookup"><span data-stu-id="b63ce-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="b63ce-113">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือกสินค้า M9201</span><span class="sxs-lookup"><span data-stu-id="b63ce-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="b63ce-114">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b63ce-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b63ce-115">ถ้าคุณกำลังใช้สินค้า M9201 คุณต้องเลือกน้อยกว่า 200</span><span class="sxs-lookup"><span data-stu-id="b63ce-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="b63ce-116">สลับการขยายของส่วนมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b63ce-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="b63ce-117">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b63ce-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b63ce-118">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b63ce-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b63ce-119">ถ้าคุณกำลังใช้สินค้า M9201 คุณสามารถเลือกคลังสินค้า 51 ได้</span><span class="sxs-lookup"><span data-stu-id="b63ce-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="b63ce-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b63ce-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="b63ce-121">ปรับปรุงเงื่อนไขของการบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b63ce-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="b63ce-122">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b63ce-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b63ce-123">อัพเดตฟิลด์ปริมาณสินค้าคงคลังเพื่อสะท้อนปริมาณการบล็อค</span><span class="sxs-lookup"><span data-stu-id="b63ce-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="b63ce-124">ในฟิลด์วันที่คาดหวังไว้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="b63ce-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="b63ce-125">คุณอาจต้องการที่จะระบุเมื่อสินค้าคงคลังที่ถูกบล็อคถูกคาดว่าจะพร้อมใช้งานสำหรับการจอง โดยการกำหนดวันที่คาดไว้ </span><span class="sxs-lookup"><span data-stu-id="b63ce-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="b63ce-126">ถ้าตัวเลือกใบเสร็จรับเงินที่คาดไว้ถูกเลือกสำหรับสินค้าคงคลังการที่ถูกบล็อค ซึ่งเป็นตามค่าเริ่มต้นเมื่อคุณสร้างการบล็อค วันที่วันนี้จะปรากฏบนธุรกรรมที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="b63ce-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="b63ce-127">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b63ce-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="b63ce-128">ลบการบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b63ce-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="b63ce-129">คลิก ลบ</span><span class="sxs-lookup"><span data-stu-id="b63ce-129">Click Delete.</span></span>
2. <span data-ttu-id="b63ce-130">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="b63ce-130">Click Yes.</span></span>
3. <span data-ttu-id="b63ce-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b63ce-131">Close the page.</span></span>

