---
title: ดูประวัติลำดับงาน
description: หัวข้อนี้อธิบายขั้นตอนในการดูสถานะของเอกสารที่ถูกส่งให้กับระบบลำดับงานเพื่อการประมวลผลและการอนุมัติ
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 325478ed89b9c650899001dd08d1c98550fce520
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798991"
---
# <a name="view-workflow-history"></a><span data-ttu-id="78210-103">ดูประวัติลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="78210-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78210-104">หัวข้อนี้อธิบายขั้นตอนในการดูสถานะของเอกสารที่ถูกส่งให้กับระบบลำดับงานเพื่อการประมวลผลและการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="78210-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="78210-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="78210-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="78210-106">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การสอบถาม > > ลำดับงาน > ประวัติลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="78210-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="78210-107">ใช้แบบฟอร์มนี้เพื่อดูสถานะของเอกสารที่ส่งให้กับระบบลำดับงานเพื่อการประมวลผลและการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="78210-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="78210-108">**รหัสอินสแตนซ์** คือรหัสการระบุรหัสประจำตัวของอินสแตนซ์ลำดับงานที่กำลังประมวลผล หรือได้ประมวลผลเอกสารแล้ว</span><span class="sxs-lookup"><span data-stu-id="78210-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="78210-109">**สถานะ** คือสถานะลำดับงานของเอกสาร</span><span class="sxs-lookup"><span data-stu-id="78210-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="78210-110">**รหัสลำดับงาน** คือรหัสการระบุรหัสประจำตัวของลำดับงานที่กำลังประมวลผล หรือได้ประมวลผลเอกสารแล้ว</span><span class="sxs-lookup"><span data-stu-id="78210-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="78210-111">**เอกสาร** คือรหัสการระบุรหัสประจำตัวของเอกสาร</span><span class="sxs-lookup"><span data-stu-id="78210-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="78210-112">**ชนิดเอกสาร** คือชนิดของเอกสารที่ถูกส่งสำหรับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="78210-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="78210-113">**ลำดับงาน** คือชื่อของลำดับงานที่กำลังประมวลผล หรือได้ประมวลผลเอกสารแล้ว</span><span class="sxs-lookup"><span data-stu-id="78210-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="78210-114">**รุ่น** คือหมายเลขรุ่นของลำดับงานที่กำลังประมวลผล หรือได้ประมวลผลเอกสารแล้ว</span><span class="sxs-lookup"><span data-stu-id="78210-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="78210-115">**วันที่และเวลาที่สร้าง** คือวันที่และเวลาที่ส่งเอกสาร</span><span class="sxs-lookup"><span data-stu-id="78210-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="78210-116">**เวลาที่เลยกำหนด** คือเวลาที่ผ่านไปนับตั้งแต่ส่งเอกสาร</span><span class="sxs-lookup"><span data-stu-id="78210-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="78210-117">ปุ่ม **ดำเนินการต่อ** ช่วยให้คุณสามารถดำเนินกระบวนการลำดับงานสำหรับเอกสารที่เลือกต่อได้</span><span class="sxs-lookup"><span data-stu-id="78210-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="78210-118">ปุ่ม **เรียกคืน** ช่วยให้คุณสามารถเรียกคืนเอกสารที่เลือกเพื่อที่จะไม่ให้มีการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="78210-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="78210-119">ในรายการ ให้เลือกลิงค์ในแถวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="78210-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="78210-120">ตรวจสอบให้แน่ใจว่ามีการขยายส่วน **รายการงาน**</span><span class="sxs-lookup"><span data-stu-id="78210-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="78210-121">ในส่วนนี้ คุณสามารถดูรายการงานที่เกี่ยวข้องกับเอกสารที่เลือก</span><span class="sxs-lookup"><span data-stu-id="78210-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="78210-122">ตัวอย่างเช่น งานอาจจำเป็นต้องเสร็จสมบูรณ์ หรือเอกสารอาจจำเป็นต้องได้รับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="78210-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="78210-123">ปุ่ม **กำหนดใหม่** จะเปิดกล่องโต้ตอบซึ่งคุณสามารถกำหนดงานอีกครั้งให้กับผู้ใช้รายอื่น</span><span class="sxs-lookup"><span data-stu-id="78210-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="78210-124">ตรวจสอบให้แน่ใจว่ามีการขยายส่วน **รายละเอียดการติดตาม**</span><span class="sxs-lookup"><span data-stu-id="78210-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="78210-125">ในส่วนนี้ คุณสามารถดูประวัติลำดับงานของเอกสารที่เลือกได้</span><span class="sxs-lookup"><span data-stu-id="78210-125">In this section you can view the workflow history of the selected document.</span></span>  

