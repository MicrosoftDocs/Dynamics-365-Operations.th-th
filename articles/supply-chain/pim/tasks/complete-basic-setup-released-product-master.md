---
title: ตั้งค่าพื้นฐานของผลิตภัณฑ์หลักที่นำออกใช้ให้ครบถ้วน
description: 'ขั้นตอนนี้แสดงวิธีการการตั้งค่าอย่างน้อยที่สุดที่ต้องระบุก่อนที่ผลิตภัณฑ์หลักจะถูกใช้ในเวอร์ชันสูตร BOM '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3a91977c38c0ce0f9fe114bec943c7cb32a5d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "354793"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="4301a-103">ตั้งค่าพื้นฐานของผลิตภัณฑ์หลักที่นำออกใช้ให้ครบถ้วน</span><span class="sxs-lookup"><span data-stu-id="4301a-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4301a-104">ขั้นตอนนี้แสดงวิธีการการตั้งค่าอย่างน้อยที่สุดที่ต้องระบุก่อนที่ผลิตภัณฑ์หลักจะถูกใช้ในเวอร์ชันสูตร BOM </span><span class="sxs-lookup"><span data-stu-id="4301a-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="4301a-105">นี่คือกระบวนงานที่สามจากแปดกระบวนงานที่อธิบายถึงวิธีการสร้างชุดงานสำหรับการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="4301a-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="4301a-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="4301a-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="4301a-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="4301a-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="4301a-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4301a-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4301a-109">เลือกผลิตภัณฑ์หลักที่คุณได้นำออกใช้ในขั้นตอนที่สอง </span><span class="sxs-lookup"><span data-stu-id="4301a-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="4301a-110">ผลิตภัณฑ์หลักนี้ถูกสร้างขึ้นด้วยเทคโนโลยีการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="4301a-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="4301a-111">ในบานหน้าต่างการดำเนินการ คลิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4301a-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="4301a-112">คลิกกลุ่มมิติเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="4301a-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="4301a-113">ในฟิลด์กลุ่มมิติการจัดเก็บ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="4301a-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4301a-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4301a-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4301a-115">กลุ่มมิติการจัดเก็บจะกำหนดว่ามิติการจัดเก็บใดที่จะใช้สำหรับธุรกรรมผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="4301a-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="4301a-116">เลือกไซต์สำหรับขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="4301a-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="4301a-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4301a-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4301a-118">ในฟิลก์กลุ่มมิติการติดตาม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="4301a-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4301a-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4301a-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4301a-120">กลุ่มมิติการติดตามจะกำหนดว่ามิติการติดตามใดที่จะใช้สำหรับธุรกรรมผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="4301a-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="4301a-121">เลือกไซต์สำหรับขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="4301a-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="4301a-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4301a-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="4301a-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4301a-123">Click OK.</span></span>
12. <span data-ttu-id="4301a-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4301a-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="4301a-125">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="4301a-125">Click Edit.</span></span>
    * <span data-ttu-id="4301a-126">เปิดฟอร์มรายละเอียดผลิตภัณฑ์ที่นำออกใช้เพื่อดำเนินการงานการตั้งค่าต่อ</span><span class="sxs-lookup"><span data-stu-id="4301a-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="4301a-127">ในฟิลด์กลุ่มแบบจำลองสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="4301a-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="4301a-128">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4301a-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4301a-129">กลุ่มแบบจำลองสินค้าประกอบด้วยการตั้งค่าที่กำหนดวิธีควบคุมและจัดการกับการรับสินค้าและการตัดสินค้าจากคลัง</span><span class="sxs-lookup"><span data-stu-id="4301a-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="4301a-130">นอกจากนี้ ยังกำหนดวิธีการคำนวณการใช้สินค้าด้วย </span><span class="sxs-lookup"><span data-stu-id="4301a-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="4301a-131">เลือก FIFO สำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="4301a-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="4301a-132">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4301a-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="4301a-133">ขยายหรือยุบส่วนการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="4301a-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="4301a-134">ในฟิลด์กลุ่มสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="4301a-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="4301a-135">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4301a-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4301a-136">กลุ่มสินค้าจะใช้ในการจัดการสินค้าคงคลังโดยการแบ่งสินค้าคงคลังออกเป็นกลุ่ม </span><span class="sxs-lookup"><span data-stu-id="4301a-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="4301a-137">เลือก CarAudio สำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="4301a-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="4301a-138">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4301a-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="4301a-139">ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน</span><span class="sxs-lookup"><span data-stu-id="4301a-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="4301a-140">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4301a-140">Click Default order settings.</span></span>
23. <span data-ttu-id="4301a-141">ในฟิลด์ชนิดใบสั่งเริ่มต้น ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="4301a-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="4301a-142">เลือกการผลิตเพื่อระบุว่าตัวเลือกค่าเริ่มต้นในการจัดหาวัสดุสำหรับผลิตภัณฑ์หลักเพื่อทำการผลิต</span><span class="sxs-lookup"><span data-stu-id="4301a-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="4301a-143">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4301a-143">Close the page.</span></span>
25. <span data-ttu-id="4301a-144">ปิดแบบฟอร์มรายละเอียดผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="4301a-144">Close the Released product details form.</span></span>

