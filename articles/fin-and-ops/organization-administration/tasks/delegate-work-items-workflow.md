--- 
title: "มอบหมายรายการงานในลำดับงาน"
description: "ถ้าคุณวางแผนที่จะไม่อยู่ในสำนักงานหรือไม่พร้อมที่จะดำเนินการกับรายการงาน คุณสามารถมอบหมายหรือกำหนดรายการงานของคุณอีกครั้งให้กับผู้ใช้รายอื่นได้"
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4765fec0cdce0e2f8859c979ff97d20aa6b20bfa
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="d4bcf-103">มอบหมายรายการงานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="d4bcf-103">Delegate work items in a workflow</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4bcf-104">ถ้าคุณวางแผนที่จะไม่อยู่ในสำนักงานหรือไม่พร้อมที่จะดำเนินการกับรายการงาน คุณสามารถมอบหมายหรือกำหนดรายการงานของคุณอีกครั้งให้กับผู้ใช้รายอื่นได้</span><span class="sxs-lookup"><span data-stu-id="d4bcf-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="d4bcf-105">กระบวนงานนี้ช่วยคุณในการตั้งค่าคอนฟิกระบบเพื่อให้มอบหมายรายการงานของคุณให้กับผู้ใช้รายอื่นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d4bcf-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="d4bcf-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="d4bcf-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="d4bcf-107">การตั้งค่าการมอบหมายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d4bcf-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="d4bcf-108">ไปที่ ทั่วไป > การตั้งค่า > ตัวเลือกผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="d4bcf-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="d4bcf-109">คลิกแท็บลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="d4bcf-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="d4bcf-110">ตรวจสอบให้แน่ใจว่ามีการขยายส่วน การมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="d4bcf-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="d4bcf-111">เมื่อต้องการตั้งค่าคอนฟิกระบบให้มอบหมายรายการงานของคุณให้กับผู้ใช้รายอื่นโดยอัตโนมัติ คุณจะต้องสร้างกฎการมอบหมาย ซึ่งจะระบุว่าควรมอบหมายรายการงานบางชนิดเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="d4bcf-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="d4bcf-112">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างกฎการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="d4bcf-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="d4bcf-113">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d4bcf-113">Click Add.</span></span>
4. <span data-ttu-id="d4bcf-114">ในฟิลด์ขอบเขต ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d4bcf-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="d4bcf-115">ทั้งหมด - มอบหมายรายการงานทั้งหมดที่กำหนดให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="d4bcf-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="d4bcf-116">โมดูล - มอบหมายเฉพาะรายการงานที่เกี่ยวข้องกับชนิดเฉพาะของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="d4bcf-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="d4bcf-117">ถ้าคุณเลือกตัวเลือกนี้ คุณจะต้องเลือกชนิดของลำดับงานในฟิลด์ชื่อ</span><span class="sxs-lookup"><span data-stu-id="d4bcf-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="d4bcf-118">ลำดับงาน - มอบหมายเฉพาะรายการงานที่เกี่ยวข้องกับลำดับงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="d4bcf-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="d4bcf-119">ถ้าคุณเลือกตัวเลือกนี้ คุณจะต้องเลือกลำดับงานในฟิลด์ชื่อ</span><span class="sxs-lookup"><span data-stu-id="d4bcf-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="d4bcf-120">ในฟิลด์การมอบหมาย เลือกผู้ใช้ที่จะมอบหมายรายการงานให้</span><span class="sxs-lookup"><span data-stu-id="d4bcf-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="d4bcf-121">ใช้ฟิลด์ วันที่/เวลาเริ่มต้นและวันที่/เวลาสิ้นสุด เพื่อระบุเวลาที่คุณต้องการให้รายการงานถูกมอบหมายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d4bcf-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="d4bcf-122">ในฟิลด์ วันที่/เวลาเริ่มต้น ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d4bcf-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="d4bcf-123">ในฟิลด์ วันที่/เวลาสิ้นสุด ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d4bcf-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="d4bcf-124">เลือกกล่องกาเครื่องหมาย เปิดใช้งาน เพื่อใช้กฎการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="d4bcf-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="d4bcf-125">ถ้าคุณเลือกโมดูลเป็นขอบเขต คุณจะต้องเลือกโมดูลในฟิลด์ชื่อ</span><span class="sxs-lookup"><span data-stu-id="d4bcf-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="d4bcf-126">ถ้าคุณเลือกลำดับงานเป็นขอบเขต คุณจะต้องเลือกลำดับงานเฉพาะที่จะมอบหมายในฟิลด์ชื่อ</span><span class="sxs-lookup"><span data-stu-id="d4bcf-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="d4bcf-127">ในฟิลด์ข้อคิดเห็น ป้อนข้อคิดเห็นที่อธิบายว่าเพราะเหตุใดคุณจึงกำลังจะมอบหมายรายการงาน</span><span class="sxs-lookup"><span data-stu-id="d4bcf-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>


