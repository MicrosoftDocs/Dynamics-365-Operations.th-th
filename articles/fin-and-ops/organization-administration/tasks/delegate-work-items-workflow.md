---
title: มอบหมายรายการงานในลำดับงาน
description: ถ้าคุณวางแผนที่จะไม่อยู่ในสำนักงานหรือไม่พร้อมที่จะดำเนินการกับรายการงาน คุณสามารถมอบหมายหรือกำหนดรายการงานของคุณอีกครั้งให้กับผู้ใช้รายอื่นได้
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44dc747543e32b54729d12c89a401b0187e25a61
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916426"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="604e0-103">มอบหมายรายการงานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="604e0-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="604e0-104">มอบหมายรายการงานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="604e0-104">Manually delegate a work item</span></span>

<span data-ttu-id="604e0-105">เมื่อต้องการมอบหมายรายการงานแต่ละรายการ เลือกตัวเลือก **มอบหมาย** ในเมนู **ลำดับงาน** แล้วป้อนผู้ใช้ที่จะมอบหมายให้กับข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="604e0-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="604e0-106">ขั้นตอนนี้จะเป็นการมอบหมายรายการงานให้กับผู้ใช้นั้นๆ เพื่อให้ผู้ใช้ดังกล่าวสามารถทำให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="604e0-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="604e0-107">มอบหมายรายการงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="604e0-107">Automatically delegate work items</span></span>

<span data-ttu-id="604e0-108">ถ้าคุณวางแผนที่จะไม่อยู่ที่สำนักงาน หรือไม่พร้อมที่จะดำเนินการกับรายการงานเป็นระยะเวลาหนึ่ง คุณสามารถมอบหมายรายการงานใหม่ให้กับผู้ใช้รายอื่นโดยอัตโนมัติได้โดยใช้หน้า **ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="604e0-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="604e0-109">การตั้งค่าการมอบหมายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="604e0-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="604e0-110">ไปที่ **ทั่วไป > การตั้งค่า > ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="604e0-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="604e0-111">คลิกแท็บ **ลำดับงาน** ตรวจสอบให้แน่ใจว่ามีการขยายส่วนของการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="604e0-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="604e0-112">เมื่อต้องการตั้งค่าคอนฟิกระบบให้มอบหมายรายการงานของคุณให้กับผู้ใช้รายอื่นโดยอัตโนมัติ คุณจะต้องสร้างกฎการมอบหมาย ซึ่งจะระบุว่าควรมอบหมายรายการงานบางชนิดเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="604e0-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="604e0-113">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างกฎการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="604e0-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="604e0-114">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="604e0-114">Click **Add**.</span></span>
4. <span data-ttu-id="604e0-115">ในฟิลด์ **ขอบเขต** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="604e0-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="604e0-116">ทั้งหมด - มอบหมายรายการงานทั้งหมดที่กำหนดให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="604e0-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="604e0-117">โมดูล - มอบหมายเฉพาะรายการงานที่เกี่ยวข้องกับชนิดเฉพาะของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="604e0-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="604e0-118">ถ้าคุณเลือกตัวเลือกนี้ คุณจะต้องเลือกชนิดของลำดับงานในฟิลด์ชื่อ</span><span class="sxs-lookup"><span data-stu-id="604e0-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="604e0-119">ลำดับงาน - มอบหมายเฉพาะรายการงานที่เกี่ยวข้องกับลำดับงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="604e0-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="604e0-120">ถ้าคุณเลือกตัวเลือกนี้ คุณจะต้องเลือกลำดับงานในฟิลด์ชื่อ</span><span class="sxs-lookup"><span data-stu-id="604e0-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="604e0-121">ในฟิลด์ **การมอบหมาย** เลือกผู้ใช้ที่จะมอบหมายรายการงานให้</span><span class="sxs-lookup"><span data-stu-id="604e0-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="604e0-122">ใช้ฟิลด์ วันที่/เวลาเริ่มต้นและวันที่/เวลาสิ้นสุด เพื่อระบุเวลาที่คุณต้องการให้รายการงานถูกมอบหมายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="604e0-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="604e0-123">ในฟิลด์ **วันที่/เวลาเริ่มต้น** ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="604e0-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="604e0-124">ในฟิลด์ **วันที่/เวลาสิ้นสุด** ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="604e0-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="604e0-125">เลือกกล่องกาเครื่องหมาย **เปิดใช้งาน** เพื่อใช้กฎการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="604e0-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="604e0-126">ถ้าคุณเลือก **โมดูล** เป็นขอบเขต จากนั้น คุณจะต้องเลือกโมดูลในฟิลด์ชื่อ</span><span class="sxs-lookup"><span data-stu-id="604e0-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="604e0-127">ถ้าคุณเลือก **ลำดับงาน** เป็นขอบเขต จากนั้น คุณจะต้องเลือกลำดับงานเฉพาะที่จะมอบหมายในฟิลด์ชื่อ</span><span class="sxs-lookup"><span data-stu-id="604e0-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="604e0-128">ในฟิลด์ **ข้อคิดเห็น** ป้อนข้อคิดเห็นที่อธิบายว่าเพราะเหตุใดคุณจึงกำลังจะมอบหมายรายการงาน</span><span class="sxs-lookup"><span data-stu-id="604e0-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

