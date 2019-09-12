---
title: ส่งและอนุมัติงบประมาณโครงการ
description: กระบวนงานนี้แสดงวิธีการสร้างและส่งงบประมาณสำหรับโครงการ
author: mkirknel
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 798bbc68e625c58d56cdd769f48ba734ace1d028
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914872"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="d5c5e-103">ส่งและอนุมัติงบประมาณโครงการ</span><span class="sxs-lookup"><span data-stu-id="d5c5e-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5c5e-104">กระบวนงานนี้แสดงวิธีการสร้างและส่งงบประมาณสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="d5c5e-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="d5c5e-105">เมื่อคุณสร้างงบประมาณโครงการ คุณสามารถป้อนต้นทุนและรายได้ที่ประเมินสำหรับโครงการ และจากนั้น ใช้รายการเหล่านี้ในการควบคุมธุรกรรมโครงการที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="d5c5e-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="d5c5e-106">ในการจัดงบประมาณโครงการ ทุกงบประมาณเดิมและการปรับปรุงต้องส่งไปที่ลำดับงานโครงการสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="d5c5e-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="d5c5e-107">ลำดับงานช่วยให้คุณเพิ่มการควบคุมกระบวนการ และสร้างเรกคอร์ดประวัติการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="d5c5e-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="d5c5e-108">งานนี้ถูกสร้างขึ้นโดยใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="d5c5e-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="d5c5e-109">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > โครงการ > โครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="d5c5e-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d5c5e-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d5c5e-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d5c5e-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d5c5e-112">ใน **บานหน้าต่างการดำเนินการ** คลิก **วางแผน**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="d5c5e-113">คลิก **งบประมาณโครงการ**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="d5c5e-114">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d5c5e-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="d5c5e-115">ขยาย fastTab **ต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="d5c5e-116">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-116">Click **New**.</span></span>
9. <span data-ttu-id="d5c5e-117">ในฟิลด์ **ชนิดธุรกรรม** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d5c5e-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="d5c5e-118">ในฟิลด์ **ประเภท** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d5c5e-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="d5c5e-119">ในฟิลด์ **งบประมาณเดิม** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d5c5e-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="d5c5e-120">ขยาย fastTab **รายได้**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="d5c5e-121">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-121">Click **New**.</span></span>
14. <span data-ttu-id="d5c5e-122">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d5c5e-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="d5c5e-123">ในฟิลด์ **ชนิดธุรกรรม** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d5c5e-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="d5c5e-124">ในฟิลด์ **ประเภท** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d5c5e-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="d5c5e-125">ในฟิลด์ **งบประมาณเดิม** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d5c5e-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="d5c5e-126">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-126">Click **Save**.</span></span>
19. <span data-ttu-id="d5c5e-127">คลิก **ลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="d5c5e-128">คลิก **ส่ง** </span><span class="sxs-lookup"><span data-stu-id="d5c5e-128">Click **Submit**.</span></span>
21. <span data-ttu-id="d5c5e-129">ในฟิลด์ **ข้อคิดเห็น** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d5c5e-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="d5c5e-130">คลิก **ส่ง** </span><span class="sxs-lookup"><span data-stu-id="d5c5e-130">Click **Submit**.</span></span>

