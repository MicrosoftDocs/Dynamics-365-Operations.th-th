--- 
title: "ตั้งค่าพื้นฐานของผลิตภัณฑ์หลักที่นำออกใช้ให้ครบถ้วน"
description: "ขั้นตอนนี้แสดงวิธีการการตั้งค่าอย่างน้อยที่สุดที่ต้องระบุก่อนที่ผลิตภัณฑ์หลักจะถูกใช้ในเวอร์ชันสูตร BOM "
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 8e08fbd53657bcf31a12166cf06b614ce3e3f131
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="ad0ef-103">ตั้งค่าพื้นฐานของผลิตภัณฑ์หลักที่นำออกใช้ให้ครบถ้วน</span><span class="sxs-lookup"><span data-stu-id="ad0ef-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad0ef-104">ขั้นตอนนี้แสดงวิธีการการตั้งค่าอย่างน้อยที่สุดที่ต้องระบุก่อนที่ผลิตภัณฑ์หลักจะถูกใช้ในเวอร์ชันสูตร BOM </span><span class="sxs-lookup"><span data-stu-id="ad0ef-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="ad0ef-105">นี่คือกระบวนงานที่สามจากแปดกระบวนงานที่อธิบายถึงวิธีการสร้างชุดงานสำหรับการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="ad0ef-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="ad0ef-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="ad0ef-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="ad0ef-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="ad0ef-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ad0ef-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ad0ef-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ad0ef-109">เลือกผลิตภัณฑ์หลักที่คุณได้นำออกใช้ในขั้นตอนที่สอง </span><span class="sxs-lookup"><span data-stu-id="ad0ef-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="ad0ef-110">ผลิตภัณฑ์หลักนี้ถูกสร้างขึ้นด้วยเทคโนโลยีการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="ad0ef-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="ad0ef-111">ในบานหน้าต่างการดำเนินการ คลิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ad0ef-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="ad0ef-112">คลิกกลุ่มมิติเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="ad0ef-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="ad0ef-113">ในฟิลด์กลุ่มมิติการจัดเก็บ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="ad0ef-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ad0ef-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ad0ef-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ad0ef-115">กลุ่มมิติการจัดเก็บจะกำหนดว่ามิติการจัดเก็บใดที่จะใช้สำหรับธุรกรรมผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="ad0ef-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="ad0ef-116">เลือกไซต์สำหรับขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="ad0ef-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="ad0ef-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ad0ef-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ad0ef-118">ในฟิลก์กลุ่มมิติการติดตาม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="ad0ef-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ad0ef-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ad0ef-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ad0ef-120">กลุ่มมิติการติดตามจะกำหนดว่ามิติการติดตามใดที่จะใช้สำหรับธุรกรรมผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="ad0ef-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="ad0ef-121">เลือกไซต์สำหรับขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="ad0ef-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="ad0ef-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ad0ef-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="ad0ef-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ad0ef-123">Click OK.</span></span>
12. <span data-ttu-id="ad0ef-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ad0ef-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="ad0ef-125">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="ad0ef-125">Click Edit.</span></span>
    * <span data-ttu-id="ad0ef-126">เปิดฟอร์มรายละเอียดผลิตภัณฑ์ที่นำออกใช้เพื่อดำเนินการงานการตั้งค่าต่อ</span><span class="sxs-lookup"><span data-stu-id="ad0ef-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="ad0ef-127">ในฟิลด์กลุ่มแบบจำลองสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="ad0ef-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="ad0ef-128">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ad0ef-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ad0ef-129">กลุ่มแบบจำลองสินค้าประกอบด้วยการตั้งค่าที่กำหนดวิธีควบคุมและจัดการกับการรับสินค้าและการตัดสินค้าจากคลัง</span><span class="sxs-lookup"><span data-stu-id="ad0ef-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="ad0ef-130">นอกจากนี้ ยังกำหนดวิธีการคำนวณการใช้สินค้าด้วย </span><span class="sxs-lookup"><span data-stu-id="ad0ef-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="ad0ef-131">เลือก FIFO สำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="ad0ef-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="ad0ef-132">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ad0ef-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="ad0ef-133">ขยายหรือยุบส่วนการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ad0ef-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="ad0ef-134">ในฟิลด์กลุ่มสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="ad0ef-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="ad0ef-135">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ad0ef-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ad0ef-136">กลุ่มสินค้าจะใช้ในการจัดการสินค้าคงคลังโดยการแบ่งสินค้าคงคลังออกเป็นกลุ่ม </span><span class="sxs-lookup"><span data-stu-id="ad0ef-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="ad0ef-137">เลือก CarAudio สำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="ad0ef-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="ad0ef-138">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ad0ef-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="ad0ef-139">ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน</span><span class="sxs-lookup"><span data-stu-id="ad0ef-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="ad0ef-140">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ad0ef-140">Click Default order settings.</span></span>
23. <span data-ttu-id="ad0ef-141">ในฟิลด์ชนิดใบสั่งเริ่มต้น ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ad0ef-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="ad0ef-142">เลือกการผลิตเพื่อระบุว่าตัวเลือกค่าเริ่มต้นในการจัดหาวัสดุสำหรับผลิตภัณฑ์หลักเพื่อทำการผลิต</span><span class="sxs-lookup"><span data-stu-id="ad0ef-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="ad0ef-143">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ad0ef-143">Close the page.</span></span>
25. <span data-ttu-id="ad0ef-144">ปิดแบบฟอร์มรายละเอียดผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="ad0ef-144">Close the Released product details form.</span></span>


