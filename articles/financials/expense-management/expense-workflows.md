---
title: ตั้งค่าลำดับงานสำหรับค่าใช้จ่าย
description: คุณสามารถตั้งค่ากระบวนการลำดับงานที่ใช้ในการตรวจทานและอนุมัติเอกสารเดินทางและค่าใช้จ่าย
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86cadf7277fbb7e08dad4b5dc2a46e1c6ce5a888
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840972"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="a4532-103">ตั้งค่าลำดับงานสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a4532-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4532-104"> คุณสามารถตั้งค่ากระบวนการลำดับงานที่ใช้ในการตรวจทานและอนุมัติเอกสารเดินทางและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a4532-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="a4532-105">เอกสารที่คุณสามารถกำหนดลำดับงานให้ เช่น รายงานค่าใช้จ่าย ใบเบิกค่าเดินทาง และคำขอเบิกเงินทดรองจ่ายเงินสด</span><span class="sxs-lookup"><span data-stu-id="a4532-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="a4532-106">ลำดับงานแสดงถึงกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="a4532-106">A workflow represents a business process.</span></span> <span data-ttu-id="a4532-107">โดยจะกำหนดวิธีการที่เอกสารหมุนเวียนในระบบ และระบุว่าใครต้องทำงานให้เสร็จสมบูรณ์หรืออนุมัติเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a4532-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="a4532-108">มีประโยชน์มากมายสำหรับการใช้ระบบลำดับงานในองค์กรของคุณดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a4532-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="a4532-109">**กระบวนการที่สอดคล้องกัน** — คุณสามารถกำหนดกระบวนการอนุมัติสำหรับเอกสารเฉพาะ เช่น ใบขอซื้อและรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a4532-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="a4532-110">การใช้ระบบลำดับงานช่วยให้แน่ใจว่าเอกสารจะได้รับการประมวลผลและอนุมัติในลักษณะที่สอดคล้องกันและมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a4532-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="a4532-111">การติดตามกระบวนการ — คุณสามารถติดตามสถานะ ประวัติ และเมตริกประสิทธิภาพของอินสแตนซ์ลำดับงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="a4532-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="a4532-112">ซึ่งจะช่วยคุณกำหนดว่าควรทำการเปลี่ยนแปลงกับลำดับงานเพื่อปรับปรุงประสิทธิภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4532-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="a4532-113">รายการงานจากส่วนกลาง — ผู้ใช้สามารถดูรายการงานจากส่วนกลางเพื่อดูงานในลำดับงานและการอนุมัติที่กำหนดให้กับงานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="a4532-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="a4532-114">**ชนิดของลำดับงานที่คุณสามารถสร้าง**</span><span class="sxs-lookup"><span data-stu-id="a4532-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="a4532-115">ตารางต่อไปนี้แสดงชนิดของลำดับงานที่คุณสามารถสร้างใน **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="a4532-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="a4532-116"><strong>ชนิด</strong></span><span class="sxs-lookup"><span data-stu-id="a4532-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="a4532-117"><strong>ใช้ชนิดนี้กับ</strong></span><span class="sxs-lookup"><span data-stu-id="a4532-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="a4532-118"><strong>รายงานค่าใช้จ่าย</strong></span><span class="sxs-lookup"><span data-stu-id="a4532-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="a4532-119">สร้างลำดับงานการอนุมัติสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a4532-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="a4532-120"><strong>ลงรายการบัญชีรายงานค่าใช้จ่ายอัตโนมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="a4532-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="a4532-121">สร้างลำดับงานการลงรายการบัญชีอัตโนมัติสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a4532-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="a4532-122"><strong>สินค้าในรายการค่าใช้จ่าย</strong></span><span class="sxs-lookup"><span data-stu-id="a4532-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="a4532-123">สร้างลำดับงานการอนุมัติสำหรับสินค้าในรายการในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a4532-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="a4532-124"><strong>การลงรายการบัญชีสินค้าในรายการค่าใช้จ่ายอัตโนมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="a4532-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="a4532-125">สร้างลำดับงานการลงรายการบัญชีอัตโนมัติสำหรับสินค้าในรายการในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a4532-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="a4532-126"><strong>ใบเบิกค่าเดินทาง</strong></span><span class="sxs-lookup"><span data-stu-id="a4532-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="a4532-127">สร้างลำดับงานการอนุมัติสำหรับใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="a4532-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="a4532-128"><strong>คำขอเบิกเงินทดรองจ่าย</strong></span><span class="sxs-lookup"><span data-stu-id="a4532-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="a4532-129">สร้างลำดับงานการอนุมัติสำหรับคำขอเบิกเงินทดรองจ่าย</span><span class="sxs-lookup"><span data-stu-id="a4532-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="a4532-130"><strong>การขอคืนภาษี VAT</strong></span><span class="sxs-lookup"><span data-stu-id="a4532-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="a4532-131">สร้างลำดับงานการอนุมัติสำหรับการขอคืนภาษีมูลค่าเพิ่ม (VAT)</span><span class="sxs-lookup"><span data-stu-id="a4532-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

