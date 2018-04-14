--- 
title: "สร้างกฎขั้นสูงสำหรับสมุดรายวัน"
description: "กระบวนงานนี้ดำเนินการสร้างกฎขั้นสูงสำหรับสมุดรายวัน "
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 36f4edd6fa9711022e291ea5ceffbcc9ef55b2a9
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="2d024-103">สร้างกฎขั้นสูงสำหรับสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="2d024-103">Create advanced rules for journals</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d024-104">กระบวนงานนี้ดำเนินการสร้างกฎขั้นสูงสำหรับสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="2d024-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="2d024-105">ซึ่งรวมถึงการตั้งค่าการควบคุมสมุดรายวันและข้อจำกัดในการลงรายการบัญชีของผู้ใช้ </span><span class="sxs-lookup"><span data-stu-id="2d024-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="2d024-106">กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="2d024-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="2d024-107">ตั้งค่าการควบคุมสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="2d024-107">Set up journal control</span></span>
1. <span data-ttu-id="2d024-108">ไปที่บัญชีแยกประเภททั่วไป > การตั้งค่าสมุดรายวัน > ชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="2d024-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="2d024-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2d024-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2d024-110">คลิกการควบคุมสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="2d024-110">Click Journal control.</span></span>
4. <span data-ttu-id="2d024-111">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="2d024-111">Click Add.</span></span>
5. <span data-ttu-id="2d024-112">ในฟิลด์บัญชีบริษัท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2d024-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2d024-113">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2d024-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2d024-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2d024-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2d024-115">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="2d024-115">Click Add.</span></span>
9. <span data-ttu-id="2d024-116">ในฟิลด์โครงสร้างทางบัญชี ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2d024-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="2d024-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2d024-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="2d024-118">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2d024-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="2d024-119">ในฟิลด์เซ็กเมนต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2d024-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="2d024-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2d024-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="2d024-121">ในฟิลด์จากค่า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2d024-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="2d024-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2d024-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="2d024-123">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2d024-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="2d024-124">ในฟิลด์ไปที่ค่า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2d024-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="2d024-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2d024-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="2d024-126">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2d024-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="2d024-127">การตั้งค่าข้อจำกัดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2d024-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="2d024-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2d024-128">Close the page.</span></span>
2. <span data-ttu-id="2d024-129">คลิกข้อจำกัดในการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2d024-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="2d024-130">ใน คุณต้องการตั้งค่าข้อจำกัดในการลงรายการบัญชีอย่างไร ให้เลือก โดยกลุ่มผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2d024-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="2d024-131">ในแผนภูมิ ให้ตรวจสอบ 'กลุ่มที่คุณต้องการอนุญาตให้มีการลงรายการบัญชีสำหรับชื่อสมุดรายวัน'</span><span class="sxs-lookup"><span data-stu-id="2d024-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="2d024-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2d024-132">Click OK.</span></span>


