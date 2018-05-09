---
title: "ปิดบัญชีแยกประเภททั่วไปรอบระยะเวลาเมื่อสิ้นสุด"
description: "หัวข้อนี้อธิบายถึงงานที่โดยทั่วไปจะเสร็จสมบูรณ์เมื่อทำการปิดรอบระยะเวลาสำหรับบัญชีแยกประเภททั่วไป"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 723e7306a0ffd0fd1a396a7852d9e7aa76f381fb
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="e4c62-103">ปิดบัญชีแยกประเภททั่วไปรอบระยะเวลาเมื่อสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="e4c62-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4c62-104">หัวข้อนี้อธิบายถึงงานที่โดยทั่วไปจะเสร็จสมบูรณ์เมื่อทำการปิดรอบระยะเวลาสำหรับบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="e4c62-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="e4c62-105">ในบัญชีแยกประเภททั่วไป คุณสามารถใช้ขั้นตอนการปิดเมื่อสิ้นสุดรอบระยะเวลา หรือ ปีหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="e4c62-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="e4c62-106">กระบวนการปิดบัญชีจัดเตรียมระบบสำหรับรอบระยะเวลาใหม่</span><span class="sxs-lookup"><span data-stu-id="e4c62-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="e4c62-107">เมื่อต้องการจัดเตรียมระบบสำหรับปีใหม่ คุณต้องดำเนินกระบวนการปิดบัญชีสิ้นปี</span><span class="sxs-lookup"><span data-stu-id="e4c62-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="e4c62-108">แต่ละองค์กรมีกระบวนการต่าง ๆ และขั้นตอนที่ทำงานสำหรับการสิ้นสุดของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="e4c62-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="e4c62-109">นี่คือขั้นตอนบางขั้นตอนที่จำเป็นต้องระบุสำหรับรอบระยะเวลาสิ้นสุด:</span><span class="sxs-lookup"><span data-stu-id="e4c62-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="e4c62-110">ดำเนินงานทั้งหมดสำหรับโมดูลอื่น ๆ ทั้งหมด เช่น บัญชีลูกหนี้, บัญชีเจ้าหนี้, และ สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e4c62-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="e4c62-111">ตรวจสอบว่า มีการลงรายการบัญชีสมุดรายวันทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e4c62-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="e4c62-112">ดำเนินการประเมินค่าสกุลเงินต่างประเทศเพื่อสร้างยอดเงินกำไรหรือขาดทุนใด ๆที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="e4c62-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="e4c62-113">จัดตั้งธุรกรรมสำหรับบัญชีแยกประเภทแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="e4c62-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="e4c62-114">การดำเนินการขอปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e4c62-114">Process any required allocations.</span></span>
-   <span data-ttu-id="e4c62-115">ลงรายการบัญชีการปรับปรุงสิ้นสุดรอบระยะเวลาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="e4c62-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="e4c62-116">รายการธุรกรรม และตรวจทานการ **รายงานสมุดรายวันบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="e4c62-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="e4c62-117">ดำเนินการรวมบัญชี โดยใช้บริษัทที่รวมบัญชีหรือการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e4c62-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="e4c62-118">สร้างงบการเงินสิ้นงวด โดยใช้การรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e4c62-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="e4c62-119">ตั้งค่ารอบระยะเวลาบัญชีแยกประเภทเป็น **คงค้าง**, เพื่อให้ไม่มีการ ลงรายการบัญชีอื่นใดเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="e4c62-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="e4c62-120">คุณสามารถจำกัดรอบระยะเวลาให้กับกลุ่มผู้ใช้เฉพาะขณะสิ้นสุดรอบระยะเวลากิจกรรมใดๆที่จะเกิด เพื่อการควบคุมที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="e4c62-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="e4c62-121">ไม่แนะนำให้กำหนดรอบระยะเวลาไปยัง **ปิดอย่างถาวร** เนื่องจากคุณจะไม่สามารถเปิดรอบระยะเวลาที่ปิดแล้วได้อีก</span><span class="sxs-lookup"><span data-stu-id="e4c62-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="e4c62-122">สามารถใช้พื้นที่ทำงานการปิดรอบระยะเวลาทางการเงินในการจัดระเบียบและติดตามงานที่จำเป็นสำหรับการประมวลผลสิ้นสุดรอบระยะเวลาต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="e4c62-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="e4c62-123">สำหรับข้อมูลเพิ่มเติม ให้ดูข้อมูลต่อไปนี้สำหรับข้อมูลเพิ่มเติม:</span><span class="sxs-lookup"><span data-stu-id="e4c62-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="e4c62-124">พื้นที่ทำงานการปิดรอบระยะเวลาทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e4c62-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="e4c62-125">การปิดบัญชีสิ้นปี</span><span class="sxs-lookup"><span data-stu-id="e4c62-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="e4c62-126">การปิดรอบระยะเวลาทางการเงินโดยรวม</span><span class="sxs-lookup"><span data-stu-id="e4c62-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)





