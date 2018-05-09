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
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1944053a2f52648f4e70d40a2b515c69d462ee26
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="a3fe4-103">ตั้งค่าลำดับงานสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a3fe4-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3fe4-104"> คุณสามารถตั้งค่ากระบวนการลำดับงานที่ใช้ในการตรวจทานและอนุมัติเอกสารเดินทางและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a3fe4-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="a3fe4-105">เอกสารที่คุณสามารถกำหนดลำดับงานให้ เช่น รายงานค่าใช้จ่าย ใบเบิกค่าเดินทาง และคำขอเบิกเงินทดรองจ่ายเงินสด</span><span class="sxs-lookup"><span data-stu-id="a3fe4-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="a3fe4-106">ลำดับงานแสดงถึงกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="a3fe4-106">A workflow represents a business process.</span></span> <span data-ttu-id="a3fe4-107">โดยจะกำหนดวิธีการที่เอกสารหมุนเวียนในระบบ และระบุว่าใครต้องทำงานให้เสร็จสมบูรณ์หรืออนุมัติเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a3fe4-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="a3fe4-108">มีประโยชน์มากมายสำหรับการใช้ระบบลำดับงานในองค์กรของคุณดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a3fe4-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="a3fe4-109">**กระบวนการที่สอดคล้องกัน** — คุณสามารถกำหนดกระบวนการอนุมัติสำหรับเอกสารเฉพาะ เช่น ใบขอซื้อและรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a3fe4-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="a3fe4-110">การใช้ระบบลำดับงานช่วยให้แน่ใจว่าเอกสารจะได้รับการประมวลผลและอนุมัติในลักษณะที่สอดคล้องกันและมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a3fe4-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="a3fe4-111">การติดตามกระบวนการ — คุณสามารถติดตามสถานะ ประวัติ และเมตริกประสิทธิภาพของอินสแตนซ์ลำดับงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="a3fe4-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="a3fe4-112">ซึ่งจะช่วยคุณกำหนดว่าควรทำการเปลี่ยนแปลงกับลำดับงานเพื่อปรับปรุงประสิทธิภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a3fe4-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="a3fe4-113">รายการงานจากส่วนกลาง — ผู้ใช้สามารถดูรายการงานจากส่วนกลางเพื่อดูงานในลำดับงานและการอนุมัติที่กำหนดให้กับงานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="a3fe4-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="a3fe4-114">**ชนิดของลำดับงานที่คุณสามารถสร้าง**</span><span class="sxs-lookup"><span data-stu-id="a3fe4-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="a3fe4-115">ตารางต่อไปนี้แสดงชนิดของลำดับงานที่คุณสามารถสร้างใน **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="a3fe4-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="a3fe4-116"><strong>ชนิด</strong></span><span class="sxs-lookup"><span data-stu-id="a3fe4-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="a3fe4-117"><strong>ใช้ชนิดนี้กับ</strong></span><span class="sxs-lookup"><span data-stu-id="a3fe4-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="a3fe4-118"><strong>รายงานค่าใช้จ่าย</strong></span><span class="sxs-lookup"><span data-stu-id="a3fe4-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="a3fe4-119">สร้างลำดับงานการอนุมัติสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a3fe4-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="a3fe4-120"><strong>ลงรายการบัญชีรายงานค่าใช้จ่ายอัตโนมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="a3fe4-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="a3fe4-121">สร้างลำดับงานการลงรายการบัญชีอัตโนมัติสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a3fe4-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="a3fe4-122"><strong>สินค้าในรายการค่าใช้จ่าย</strong></span><span class="sxs-lookup"><span data-stu-id="a3fe4-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="a3fe4-123">สร้างลำดับงานการอนุมัติสำหรับสินค้าในรายการในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a3fe4-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="a3fe4-124"><strong>การลงรายการบัญชีสินค้าในรายการค่าใช้จ่ายอัตโนมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="a3fe4-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="a3fe4-125">สร้างลำดับงานการลงรายการบัญชีอัตโนมัติสำหรับสินค้าในรายการในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a3fe4-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="a3fe4-126"><strong>ใบเบิกค่าเดินทาง</strong></span><span class="sxs-lookup"><span data-stu-id="a3fe4-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="a3fe4-127">สร้างลำดับงานการอนุมัติสำหรับใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="a3fe4-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="a3fe4-128"><strong>คำขอเบิกเงินทดรองจ่าย</strong></span><span class="sxs-lookup"><span data-stu-id="a3fe4-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="a3fe4-129">สร้างลำดับงานการอนุมัติสำหรับคำขอเบิกเงินทดรองจ่าย</span><span class="sxs-lookup"><span data-stu-id="a3fe4-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="a3fe4-130"><strong>การขอคืนภาษี VAT</strong></span><span class="sxs-lookup"><span data-stu-id="a3fe4-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="a3fe4-131">สร้างลำดับงานการอนุมัติสำหรับการขอคืนภาษีมูลค่าเพิ่ม (VAT)</span><span class="sxs-lookup"><span data-stu-id="a3fe4-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


