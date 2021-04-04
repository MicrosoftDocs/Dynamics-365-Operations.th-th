---
title: มอบหมายรายการงานในลำดับงาน
description: ถ้าคุณวางแผนที่จะไม่อยู่ในสำนักงานหรือไม่พร้อมที่จะดำเนินการกับรายการงาน คุณสามารถมอบหมายหรือกำหนดรายการงานของคุณอีกครั้งให้กับผู้ใช้รายอื่นได้
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 054e183374d2b24f38b0f90ff90acfeeca013861
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560566"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="783dc-103">มอบหมายรายการงานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="783dc-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="783dc-104">มอบหมายรายการงานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="783dc-104">Manually delegate a work item</span></span>

<span data-ttu-id="783dc-105">เมื่อต้องการมอบหมายรายการงานแต่ละรายการ เลือกตัวเลือก **มอบหมาย** ในเมนู **ลำดับงาน** แล้วป้อนผู้ใช้ที่จะมอบหมายให้กับข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="783dc-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="783dc-106">ขั้นตอนนี้จะเป็นการมอบหมายรายการงานให้กับผู้ใช้นั้นๆ เพื่อให้ผู้ใช้ดังกล่าวสามารถทำให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="783dc-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="783dc-107">การมอบหมายรายการงานหลายรายการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="783dc-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="783dc-108">สามารถมอบหมายรายการงานจำนวนมากพร้อมกันจากหน้า **รายการงานที่กำหนดให้กับฉัน**</span><span class="sxs-lookup"><span data-stu-id="783dc-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="783dc-109">ชนิดลำดับงานต่อไปนี้มีสิทธิ์สำหรับการมอบหมายโดยรวม: ลำดับงานการอนุมัติตามข้อตกลงการซื้อ ลำดับงานใบสั่งซื้อ การตรวจทานใบขอซื้อ และลำดับงานใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="783dc-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="783dc-110">มีการปิดใช้งานคุณลักษณะ **มอบหมายงานหลายรายการ** โดยค่าเริ่มต้นและสามารถเปิดใช้งานได้ใน **พื้นที่ทำงาน > การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="783dc-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="783dc-111">โปรดติดต่อผู้ดูแลระบบของคุณเพื่อขอความช่วยเหลือในการเปิดใช้งานคุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="783dc-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="783dc-112">ไปที่ **ทั่วไป > ทั่วไป > รายการงาน > รายการงานที่กำหนดให้กับฉัน**</span><span class="sxs-lookup"><span data-stu-id="783dc-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="783dc-113">เลือกรายการงานที่จะมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="783dc-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="783dc-114">คลิกที่เมนู **มอบหมายรายการงาน**</span><span class="sxs-lookup"><span data-stu-id="783dc-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="783dc-115">ในฟิลด์ **ผู้ใช้** เลือกผู้ใช้ที่จะมอบหมายรายการงานให้</span><span class="sxs-lookup"><span data-stu-id="783dc-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="783dc-116">ในฟิลด์ **ข้อคิดเห็น** ป้อนข้อคิดเห็นที่อธิบายว่าเพราะเหตุใดคุณจึงจะมอบหมายรายการงาน</span><span class="sxs-lookup"><span data-stu-id="783dc-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="783dc-117">คลิกปุ่ม **มอบหมายรายการงาน** เพื่อดำเนินการการมอบหมายรายการงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="783dc-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="783dc-118">มอบหมายรายการงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="783dc-118">Automatically delegate work items</span></span>

<span data-ttu-id="783dc-119">ถ้าคุณวางแผนที่จะไม่อยู่ที่สำนักงาน หรือไม่พร้อมที่จะดำเนินการกับรายการงานเป็นระยะเวลาหนึ่ง คุณสามารถมอบหมายรายการงานใหม่ให้กับผู้ใช้รายอื่นโดยอัตโนมัติได้โดยใช้หน้า **ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="783dc-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="783dc-120">การตั้งค่าการมอบหมายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="783dc-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="783dc-121">ไปที่ **ทั่วไป > การตั้งค่า > ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="783dc-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="783dc-122">คลิกแท็บ **ลำดับงาน** ตรวจสอบให้แน่ใจว่ามีการขยายส่วนของการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="783dc-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="783dc-123">เมื่อต้องการตั้งค่าคอนฟิกระบบให้มอบหมายรายการงานของคุณให้กับผู้ใช้รายอื่นโดยอัตโนมัติ คุณจะต้องสร้างกฎการมอบหมาย ซึ่งจะระบุว่าควรมอบหมายรายการงานบางชนิดเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="783dc-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="783dc-124">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างกฎการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="783dc-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="783dc-125">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="783dc-125">Click **Add**.</span></span>
4. <span data-ttu-id="783dc-126">ในฟิลด์ **ขอบเขต** ให้เลือกหนึ่งตัวเลือก:</span><span class="sxs-lookup"><span data-stu-id="783dc-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="783dc-127">ทั้งหมด - มอบหมายรายการงานทั้งหมดที่กำหนดให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="783dc-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="783dc-128">โมดูล - มอบหมายเฉพาะรายการงานที่เกี่ยวข้องกับชนิดเฉพาะของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="783dc-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="783dc-129">ถ้าคุณเลือกตัวเลือกนี้ คุณจะต้องเลือกชนิดของลำดับงานในฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="783dc-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="783dc-130">ลำดับงาน - มอบหมายเฉพาะรายการงานที่เกี่ยวข้องกับลำดับงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="783dc-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="783dc-131">ถ้าคุณเลือกตัวเลือกนี้ คุณจะต้องเลือกลำดับงานในฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="783dc-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="783dc-132">ในฟิลด์ **ชื่อ**:</span><span class="sxs-lookup"><span data-stu-id="783dc-132">In the **Name** field:</span></span>
    - <span data-ttu-id="783dc-133">สำหรับขอบเขต **โมดูล** ให้เลือกโมดูลเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="783dc-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="783dc-134">สำหรับขอบเขต **ลำดับงาน** ให้เลือกลำดับงานเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="783dc-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="783dc-135">ในฟิลด์ **การมอบหมาย** เลือกผู้ใช้ที่จะมอบหมายรายการงานให้</span><span class="sxs-lookup"><span data-stu-id="783dc-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="783dc-136">ใช้ฟิลด์ **วันที่/เวลาเริ่มต้น** และ **วันที่/เวลาสิ้นสุด** เพื่อระบุเวลาที่คุณต้องการให้รายการงานถูกมอบหมายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="783dc-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="783dc-137">ในฟิลด์ **วันที่/เวลาเริ่มต้น** ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="783dc-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="783dc-138">ในฟิลด์ **วันที่/เวลาสิ้นสุด** ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="783dc-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="783dc-139">เลือกกล่องกาเครื่องหมาย **เปิดใช้งาน** เพื่อใช้กฎการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="783dc-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="783dc-140">ในฟิลด์ **ข้อคิดเห็น** ป้อนข้อคิดเห็นที่อธิบายว่าเพราะเหตุใดคุณจึงจะมอบหมายรายการงาน</span><span class="sxs-lookup"><span data-stu-id="783dc-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]