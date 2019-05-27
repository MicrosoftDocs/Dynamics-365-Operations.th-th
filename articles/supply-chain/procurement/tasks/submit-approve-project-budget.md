---
title: ส่งและอนุมัติงบประมาณโครงการ
description: กระบวนงานนี้แสดงวิธีการสร้างและส่งงบประมาณสำหรับโครงการ
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f727e19d3f8c424b1c59e52602b7e907151f4492
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569856"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="1dbc2-103">ส่งและอนุมัติงบประมาณโครงการ</span><span class="sxs-lookup"><span data-stu-id="1dbc2-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1dbc2-104">กระบวนงานนี้แสดงวิธีการสร้างและส่งงบประมาณสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="1dbc2-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="1dbc2-105">เมื่อคุณสร้างงบประมาณโครงการ คุณสามารถป้อนต้นทุนและรายได้ที่ประเมินสำหรับโครงการ และจากนั้น ใช้รายการเหล่านี้ในการควบคุมธุรกรรมโครงการที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="1dbc2-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="1dbc2-106">ในการจัดงบประมาณโครงการ ทุกงบประมาณเดิมและการปรับปรุงต้องส่งไปที่ลำดับงานโครงการสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="1dbc2-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="1dbc2-107">ลำดับงานช่วยให้คุณเพิ่มการควบคุมกระบวนการ และสร้างเรกคอร์ดประวัติการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="1dbc2-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="1dbc2-108">งานนี้ถูกสร้างขึ้นโดยใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="1dbc2-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="1dbc2-109">ไปที่การจัดการโครงการและการบัญชี > โครงการ > โครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1dbc2-109">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="1dbc2-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1dbc2-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1dbc2-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1dbc2-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1dbc2-112">ในบานหน้าต่างการดำเนินการ คลิกวางแผน</span><span class="sxs-lookup"><span data-stu-id="1dbc2-112">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="1dbc2-113">คลิก งบประมาณโครงการ</span><span class="sxs-lookup"><span data-stu-id="1dbc2-113">Click Project budget.</span></span>
6. <span data-ttu-id="1dbc2-114">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="1dbc2-114">In the Description field, type a value.</span></span>
7. <span data-ttu-id="1dbc2-115">ขยายส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="1dbc2-115">Expand the Cost section</span></span>
8. <span data-ttu-id="1dbc2-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="1dbc2-116">Click New.</span></span>
9. <span data-ttu-id="1dbc2-117">ในฟิลด์ชนิดธุรกรรม ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="1dbc2-117">In the Transaction type field, select an option.</span></span>
10. <span data-ttu-id="1dbc2-118">ในฟิลด์ประเภท ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1dbc2-118">In the Category field, enter or select a value.</span></span>
11. <span data-ttu-id="1dbc2-119">ในฟิลด์งบประมาณเดิม ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="1dbc2-119">In the Original budget field, enter a number.</span></span>
12. <span data-ttu-id="1dbc2-120">ขยายส่วนรายได้</span><span class="sxs-lookup"><span data-stu-id="1dbc2-120">Expand the Revenues section.</span></span>
13. <span data-ttu-id="1dbc2-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="1dbc2-121">Click New.</span></span>
14. <span data-ttu-id="1dbc2-122">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1dbc2-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="1dbc2-123">ในฟิลด์ชนิดธุรกรรม ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="1dbc2-123">In the Transaction type field, select an option.</span></span>
16. <span data-ttu-id="1dbc2-124">ในฟิลด์ประเภท ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1dbc2-124">In the Category field, enter or select a value.</span></span>
17. <span data-ttu-id="1dbc2-125">ในฟิลด์งบประมาณเดิม ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="1dbc2-125">In the Original budget field, enter a number.</span></span>
18. <span data-ttu-id="1dbc2-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="1dbc2-126">Click Save.</span></span>
19. <span data-ttu-id="1dbc2-127">คลิก ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="1dbc2-127">Click Workflow.</span></span>
20. <span data-ttu-id="1dbc2-128">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="1dbc2-128">Click Submit.</span></span>
21. <span data-ttu-id="1dbc2-129">ในฟิลด์ข้อคิดเห็น ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1dbc2-129">In the Comment field, type a value.</span></span>
22. <span data-ttu-id="1dbc2-130">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="1dbc2-130">Click Submit.</span></span>

