---
title: ตั้งค่าพื้นฐานของผลิตภัณฑ์หลักที่นำออกใช้ให้ครบถ้วน
description: หัวข้อนี้แสดงวิธีดำเนินการตั้งค่าอย่างน้อยที่สุดที่จำเป็นให้เสร็จสมบูรณ์ก่อนที่ผลิตภัณฑ์หลักจะถูกใช้ในรุ่น BOM
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b8fde67699270906b893eee06600b8acf4c681e9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208328"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="4ef6e-103">ตั้งค่าพื้นฐานของผลิตภัณฑ์หลักที่นำออกใช้ให้ครบถ้วน</span><span class="sxs-lookup"><span data-stu-id="4ef6e-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4ef6e-104">หัวข้อนี้แสดงวิธีดำเนินการตั้งค่าอย่างน้อยที่สุดที่จำเป็นให้เสร็จสมบูรณ์ก่อนที่ผลิตภัณฑ์หลักจะถูกใช้ในรุ่น BOM</span><span class="sxs-lookup"><span data-stu-id="4ef6e-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="4ef6e-105">นี่คือกระบวนงานที่สามจากแปดกระบวนงานที่อธิบายถึงวิธีการสร้างชุดงานสำหรับการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="4ef6e-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="4ef6e-106">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="4ef6e-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="4ef6e-107">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="4ef6e-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="4ef6e-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4ef6e-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="4ef6e-109">เลือกผลิตภัณฑ์หลักที่คุณได้นำออกใช้ในขั้นตอนที่สอง </span><span class="sxs-lookup"><span data-stu-id="4ef6e-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="4ef6e-110">ผลิตภัณฑ์หลักนี้ถูกสร้างขึ้นด้วยเทคโนโลยีการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="4ef6e-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="4ef6e-111">ในบานหน้าต่างการดำเนินการ เลือก **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="4ef6e-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="4ef6e-112">เลือก **กลุ่มมิติ** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="4ef6e-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="4ef6e-113">ในฟิลด์ **กลุ่มมิติการจัดเก็บ** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4ef6e-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4ef6e-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4ef6e-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="4ef6e-115">กลุ่มมิติการจัดเก็บจะกำหนดว่ามิติการจัดเก็บใดที่จะใช้สำหรับธุรกรรมผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="4ef6e-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="4ef6e-116">เลือก **ไซต์** สำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="4ef6e-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="4ef6e-117">ในฟิลด์ **กลุ่มมิติการติดตาม** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4ef6e-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="4ef6e-118">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4ef6e-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="4ef6e-119">กลุ่มมิติการติดตามจะกำหนดว่ามิติการติดตามใดที่จะใช้สำหรับธุรกรรมผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="4ef6e-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="4ef6e-120">เลือก **ไม่มี** สำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="4ef6e-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="4ef6e-121">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4ef6e-121">Click **OK**.</span></span>
10. <span data-ttu-id="4ef6e-122">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="4ef6e-122">Click **Edit**.</span></span>
11. <span data-ttu-id="4ef6e-123">ในฟิลด์ **กลุ่มแบบจำลองสินค้า** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4ef6e-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="4ef6e-124">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4ef6e-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="4ef6e-125">กลุ่มแบบจำลองสินค้าประกอบด้วยการตั้งค่าที่กำหนดวิธีควบคุมและจัดการกับการรับสินค้าและการตัดสินค้าจากคลัง</span><span class="sxs-lookup"><span data-stu-id="4ef6e-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="4ef6e-126">นอกจากนี้ ยังกำหนดวิธีการคำนวณการใช้สินค้าด้วย </span><span class="sxs-lookup"><span data-stu-id="4ef6e-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="4ef6e-127">เลือก **FIFO** สำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="4ef6e-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="4ef6e-128">ขยายส่วน **จัดการต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="4ef6e-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="4ef6e-129">ในฟิลด์ **กลุ่มสินค้า** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4ef6e-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="4ef6e-130">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4ef6e-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="4ef6e-131">กลุ่มสินค้าจะใช้ในการจัดการสินค้าคงคลังโดยการแบ่งสินค้าคงคลังออกเป็นกลุ่ม </span><span class="sxs-lookup"><span data-stu-id="4ef6e-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="4ef6e-132">เลือก **CarAudio** สำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="4ef6e-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="4ef6e-133">บนบานหน้าต่างการดำเนินการ เลือก **วางแผน**</span><span class="sxs-lookup"><span data-stu-id="4ef6e-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="4ef6e-134">เลือก **การตั้งค่าใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="4ef6e-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="4ef6e-135">ใน **ฟิลด์ชนิดใบสั่งเริ่มต้น** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="4ef6e-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="4ef6e-136">เลือก **การผลิต** เพื่อระบุว่าตัวเลือกค่าเริ่มต้นในการจัดหาวัสดุสำหรับผลิตภัณฑ์หลักนี้คือ เพื่อทำการผลิต</span><span class="sxs-lookup"><span data-stu-id="4ef6e-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="4ef6e-137">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4ef6e-137">Select **Save**.</span></span>
20. <span data-ttu-id="4ef6e-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4ef6e-138">Close the page.</span></span>
21. <span data-ttu-id="4ef6e-139">ปิดฟอร์ม **รายละเอียดผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="4ef6e-139">Close the **Released product details** form.</span></span>

