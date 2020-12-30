---
title: ตั้งค่าคอนฟิกพารามิเตอร์พื้นที่ทำงานการควบคุมต้นทุน
description: ใช้กระบวนงานนี้เพื่อตั้งค่าคอนฟิกพื้นที่ทำงานการควบคุมต้นทุนเพื่อให้ผู้จัดการระดับต่าง ๆ ในองค์กรสามารถรับความช่วยเหลือจากออบเจ็กต์ต้นทุน เช่น ศูนย์ต้นทุนและกลุ่มผลิตภัณฑ์
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca05f6174541a6e97ec94db209a99424a87550eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448559"
---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="1d7cd-103">ตั้งค่าคอนฟิกพารามิเตอร์พื้นที่ทำงานการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="1d7cd-103">Configure cost control workspace parameters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d7cd-104">ใช้กระบวนงานนี้เพื่อตั้งค่าคอนฟิกพื้นที่ทำงานการควบคุมต้นทุนเพื่อให้ผู้จัดการระดับต่าง ๆ ในองค์กรสามารถรับความช่วยเหลือจากออบเจ็กต์ต้นทุน เช่น ศูนย์ต้นทุนและกลุ่มผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="1d7cd-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="1d7cd-105">บริษัทสาธิต USP2 ถูกใช้ในการสร้างเรกคอร์ดนี้</span><span class="sxs-lookup"><span data-stu-id="1d7cd-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="1d7cd-106">ไปที่ บัญชีต้นทุน > การตั้งค่า > การตั้งค่าคอนฟิกพื้นที่ทำงานของการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="1d7cd-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="1d7cd-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="1d7cd-107">Click New.</span></span>
3. <span data-ttu-id="1d7cd-108">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="1d7cd-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1d7cd-109">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="1d7cd-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1d7cd-110">เลือก ใช่ ในฟิลด์ เผยแพร่แล้ว</span><span class="sxs-lookup"><span data-stu-id="1d7cd-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="1d7cd-111">ถ้าคุณตั้งค่าตัวเลือกนี้เป็น ใช่ ผู้ใช้ที่ได้รับการกำหนดบทบาทหนึ่งบทบาทใดในบทบาทเหล่านี้จะสามารถดูรายงานในพื้นที่ทำงานการควบคุมต้นทุน: ผู้จัดการการบัญชีต้นทุน นักบัญชีต้นทุน เสมียนบัญชีต้นทุน หรือตัวควบคุมออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="1d7cd-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="1d7cd-112">ถ้าคุณตั้งค่าตัวเลือกนี้เป็น ไม่ใช่ เฉพาะผู้ใช้ที่ได้รับการกำหนดบทบาทหนึ่งบทบาทใดในบทบาทเหล่านี้จะสามารถดูรายงานในพื้นที่ทำงานการควบคุมต้นทุน: ผู้จัดการการบัญชีต้นทุน นักบัญชีต้นทุน หรือเสมียนบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="1d7cd-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="1d7cd-113">ขยายส่วนการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1d7cd-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="1d7cd-114">ในฟิลด์หน่วยการควบคุมต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1d7cd-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="1d7cd-115">ในฟิลด์เวอร์ชันเดิมของงบประมาณ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1d7cd-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="1d7cd-116">ในฟิลด์ลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1d7cd-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="1d7cd-117">ในฟิลด์ลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1d7cd-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="1d7cd-118">ขยายส่วนกำหนดเรกคอร์ดการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="1d7cd-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="1d7cd-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="1d7cd-119">Click New.</span></span>
13. <span data-ttu-id="1d7cd-120">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1d7cd-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="1d7cd-121">ในฟิลด์รอบระยะเวลาปฏิทินทางการเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1d7cd-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="1d7cd-122">ในฟิลด์เวอร์ชันจริง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1d7cd-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="1d7cd-123">ขยายรอบระยะเวลาทางบัญชีสำหรับแต่ละส่วนของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="1d7cd-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="1d7cd-124">เลือก ใช่ ในฟิลด์ รอบระยะเวลาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="1d7cd-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="1d7cd-125">ขยายคอลัมน์เพื่อแสดงสำหรับส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="1d7cd-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="1d7cd-126">เลือก ใช่ ในฟิลด์ ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="1d7cd-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="1d7cd-127">เลือก ใช่ ในฟิลด์ ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="1d7cd-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="1d7cd-128">เลือก ใช่ ในฟิลด์ รวมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="1d7cd-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="1d7cd-129">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="1d7cd-129">Click Save.</span></span>
23. <span data-ttu-id="1d7cd-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1d7cd-130">Close the page.</span></span>
24. <span data-ttu-id="1d7cd-131">ไปที่ การบัญชีต้นทุน > พื้นที่ทำงาน > การควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="1d7cd-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="1d7cd-132">เลือกคำสั่งเพื่อดูต้นทุนคงที่ ต้นทุนผันแปร รวมต้นทุน และต้นทุนที่ไม่ได้จัดประเภทสำหรับรอบระยะเวลาทางบัญชีที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1d7cd-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="1d7cd-133">ในฟิลด์รอบระยะเวลาปฏิทินทางการเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1d7cd-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="1d7cd-134">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1d7cd-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="1d7cd-135">หลังจากที่คุณได้เลือกลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ขยายลำดับชั้นมิติองค์ประกอบต้นทุนเพื่อดูค่าต้นทุนที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1d7cd-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="1d7cd-136">ตัวอย่างเช่น คุณสามารถขยายลำดับชั้นเป็นค่าโสหุ้ยการผลิตเพื่อดูค่าได้</span><span class="sxs-lookup"><span data-stu-id="1d7cd-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  

