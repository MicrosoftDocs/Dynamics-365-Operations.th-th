---
title: " ออกแบบความสัมพันธ์ระหว่างหน่วยงานขององค์กร"
description: 'กระบวนงานนี้แนะนำเกี่ยวกับวิธีการออกแบบความสัมพันธ์ระหว่างหน่วยงาน '
author: mugunthanm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner, OMNodeSelection,  HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c6502a05d3cc53d8031b9f8e365454556513c3c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416169"
---
# <a name="design-the-relationships-between-organizational-units"></a><span data-ttu-id="2db6b-103"> ออกแบบความสัมพันธ์ระหว่างหน่วยงานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="2db6b-103">Design the relationships between organizational units</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2db6b-104">กระบวนงานนี้แนะนำเกี่ยวกับวิธีการออกแบบความสัมพันธ์ระหว่างหน่วยงาน </span><span class="sxs-lookup"><span data-stu-id="2db6b-104">This procedure walks through how to design the relationship between organizational units.</span></span> <span data-ttu-id="2db6b-105">คุณต้องสร้างวัตถุประสงค์ใหม่ขององค์กรก่อนการกำหนดความสัมพันธ์ หรือคุณสามารถใช้ในวัตถุประสงค์องค์กรที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="2db6b-105">You must create a new organization purpose before defining the relationship, or you can use the existing organization purpose.</span></span> <span data-ttu-id="2db6b-106">ข้อมูลบริษัทสาธิตที่ใช้ในการปฏิบัติตามขั้นตอนนี้คือ USRT </span><span class="sxs-lookup"><span data-stu-id="2db6b-106">The demo data company used to complete this procedure is USRT.</span></span> <span data-ttu-id="2db6b-107">งานนี้มีไว้สำหรับบทบาทผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="2db6b-107">This task is intended for the administrator role.</span></span>

1. <span data-ttu-id="2db6b-108">ไปที่การจัดการองค์กร > องค์กร > ลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="2db6b-108">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="2db6b-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2db6b-109">Click New.</span></span>
3. <span data-ttu-id="2db6b-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="2db6b-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2db6b-111">คลิกที่กำหนดวัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="2db6b-111">Click Assign purpose.</span></span>
5. <span data-ttu-id="2db6b-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2db6b-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="2db6b-113">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="2db6b-113">Click Add.</span></span>
7. <span data-ttu-id="2db6b-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2db6b-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="2db6b-115">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2db6b-115">Click OK.</span></span>
    * <span data-ttu-id="2db6b-116">คุณสามารถเลือกวัตถุประสงค์ขององค์กรได้มากตามความจำเป็นสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="2db6b-116">You can select as many organization purposes as required for your organization.</span></span>  
9. <span data-ttu-id="2db6b-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2db6b-117">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="2db6b-118">คลิกที่กำหนดเป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2db6b-118">Click Set as default.</span></span>
11. <span data-ttu-id="2db6b-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2db6b-119">Close the page.</span></span>
12. <span data-ttu-id="2db6b-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2db6b-120">Click Save.</span></span>
13. <span data-ttu-id="2db6b-121">คลิกที่มุมมอง</span><span class="sxs-lookup"><span data-stu-id="2db6b-121">Click View.</span></span>
14. <span data-ttu-id="2db6b-122">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="2db6b-122">Click Edit.</span></span>
15. <span data-ttu-id="2db6b-123">คลิก แทรก</span><span class="sxs-lookup"><span data-stu-id="2db6b-123">Click Insert.</span></span>
16. <span data-ttu-id="2db6b-124">คลิกที่หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="2db6b-124">Click Business unit.</span></span>
17. <span data-ttu-id="2db6b-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2db6b-125">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="2db6b-126">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2db6b-126">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="2db6b-127">คลิก แทรก</span><span class="sxs-lookup"><span data-stu-id="2db6b-127">Click Insert.</span></span>
20. <span data-ttu-id="2db6b-128">เลือกช่องทางการค้า</span><span class="sxs-lookup"><span data-stu-id="2db6b-128">Click Commerce channel.</span></span>
21. <span data-ttu-id="2db6b-129">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2db6b-129">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="2db6b-130">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2db6b-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2db6b-131">คุณสามารถเพิ่มหน่วยงานได้มากเท่าที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="2db6b-131">You can add as many organization units as is required.</span></span>  
23. <span data-ttu-id="2db6b-132">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2db6b-132">Click Save.</span></span>
24. <span data-ttu-id="2db6b-133">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="2db6b-133">Click Close.</span></span>
25. <span data-ttu-id="2db6b-134">คลิกที่เผยแพร่เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="2db6b-134">Click Publish to open the drop dialog.</span></span>
26. <span data-ttu-id="2db6b-135">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="2db6b-135">In the Effective date field, enter a date and time.</span></span>
27. <span data-ttu-id="2db6b-136">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="2db6b-136">In the Effective date field, enter a date and time.</span></span>
28. <span data-ttu-id="2db6b-137">ในฟิลด์อธิบายการเปลี่ยนแปลง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2db6b-137">In the Describe changes field, type a value.</span></span>
29. <span data-ttu-id="2db6b-138">คลิกที่เผยแพร่ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2db6b-138">Click Publish.</span></span>
30. <span data-ttu-id="2db6b-139">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="2db6b-139">Click Close.</span></span>

