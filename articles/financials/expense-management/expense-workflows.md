---
title: "ตั้งค่าลำดับงานสำหรับค่าใช้จ่าย"
description: "คุณสามารถตั้งค่ากระบวนการลำดับงานที่ใช้ในการตรวจทานและอนุมัติเอกสารเดินทางและค่าใช้จ่าย"
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: ef60fbab0f75ff70206d954e3d098a3866c467b6
ms.contentlocale: th-th
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="2f8e8-103">ตั้งค่าลำดับงานสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2f8e8-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="2f8e8-104"> คุณสามารถตั้งค่ากระบวนการลำดับงานที่ใช้ในการตรวจทานและอนุมัติเอกสารเดินทางและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2f8e8-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="2f8e8-105">เอกสารที่คุณสามารถกำหนดลำดับงานให้ เช่น รายงานค่าใช้จ่าย ใบเบิกค่าเดินทาง และคำขอเบิกเงินทดรองจ่ายเงินสด</span><span class="sxs-lookup"><span data-stu-id="2f8e8-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="2f8e8-106">ลำดับงานแสดงถึงกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="2f8e8-106">A workflow represents a business process.</span></span> <span data-ttu-id="2f8e8-107">โดยจะกำหนดวิธีการที่เอกสารหมุนเวียนในระบบ และระบุว่าใครต้องทำงานให้เสร็จสมบูรณ์หรืออนุมัติเอกสาร</span><span class="sxs-lookup"><span data-stu-id="2f8e8-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="2f8e8-108">มีประโยชน์มากมายสำหรับการใช้ระบบลำดับงานในองค์กรของคุณดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2f8e8-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="2f8e8-109">**กระบวนการที่สอดคล้องกัน** — คุณสามารถกำหนดกระบวนการอนุมัติสำหรับเอกสารเฉพาะ เช่น ใบขอซื้อและรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2f8e8-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="2f8e8-110">การใช้ระบบลำดับงานช่วยให้แน่ใจว่าเอกสารจะได้รับการประมวลผลและอนุมัติในลักษณะที่สอดคล้องกันและมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="2f8e8-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="2f8e8-111">การติดตามกระบวนการ — คุณสามารถติดตามสถานะ ประวัติ และเมตริกประสิทธิภาพของอินสแตนซ์ลำดับงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2f8e8-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="2f8e8-112">ซึ่งจะช่วยคุณกำหนดว่าควรทำการเปลี่ยนแปลงกับลำดับงานเพื่อปรับปรุงประสิทธิภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2f8e8-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="2f8e8-113">รายการงานจากส่วนกลาง — ผู้ใช้สามารถดูรายการงานจากส่วนกลางเพื่อดูงานในลำดับงานและการอนุมัติที่กำหนดให้กับงานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="2f8e8-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="2f8e8-114">**ชนิดของลำดับงานที่คุณสามารถสร้าง**</span><span class="sxs-lookup"><span data-stu-id="2f8e8-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="2f8e8-115">ตารางต่อไปนี้แสดงชนิดของลำดับงานที่คุณสามารถสร้างใน **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="2f8e8-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="2f8e8-116">**ชนิด**</span><span class="sxs-lookup"><span data-stu-id="2f8e8-116">**Type**</span></span>                           | <span data-ttu-id="2f8e8-117">**ใช้ชนิดนี้กับ**</span><span class="sxs-lookup"><span data-stu-id="2f8e8-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="2f8e8-118">**รายงานค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="2f8e8-118">**Expense report**</span></span>                 | <span data-ttu-id="2f8e8-119">สร้างลำดับงานการอนุมัติสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2f8e8-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="2f8e8-120">**ลงรายการบัญชีรายงานค่าใช้จ่ายอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="2f8e8-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="2f8e8-121">สร้างลำดับงานการลงรายการบัญชีอัตโนมัติสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2f8e8-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="2f8e8-122">**สินค้าในรายการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="2f8e8-122">**Expense line item**</span></span>              | <span data-ttu-id="2f8e8-123">สร้างลำดับงานการอนุมัติสำหรับสินค้าในรายการในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2f8e8-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="2f8e8-124">**การลงรายการบัญชีสินค้าในรายการค่าใช้จ่ายอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="2f8e8-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="2f8e8-125">สร้างลำดับงานการลงรายการบัญชีอัตโนมัติสำหรับสินค้าในรายการในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2f8e8-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="2f8e8-126">**ใบเบิกค่าเดินทาง**</span><span class="sxs-lookup"><span data-stu-id="2f8e8-126">**Travel requisition**</span></span>             | <span data-ttu-id="2f8e8-127">สร้างลำดับงานการอนุมัติสำหรับใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="2f8e8-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="2f8e8-128">**คำขอเบิกเงินทดรองจ่าย**</span><span class="sxs-lookup"><span data-stu-id="2f8e8-128">**Cash advance request**</span></span>           | <span data-ttu-id="2f8e8-129">สร้างลำดับงานการอนุมัติสำหรับคำขอเบิกเงินทดรองจ่าย</span><span class="sxs-lookup"><span data-stu-id="2f8e8-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="2f8e8-130">**การขอคืนภาษี VAT**</span><span class="sxs-lookup"><span data-stu-id="2f8e8-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="2f8e8-131">สร้างลำดับงานการอนุมัติสำหรับการขอคืนภาษีมูลค่าเพิ่ม (VAT)</span><span class="sxs-lookup"><span data-stu-id="2f8e8-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

