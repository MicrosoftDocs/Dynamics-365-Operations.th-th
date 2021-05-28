---
title: การปิดบัญชีสิ้นปีขาดยอดดุลยกมา
description: หัวข้อนี้อธิบายเหตุผลว่าเพราะเหตุใดยอดดุลยกมาจึงอาจขาดหายไปเมื่อคุณปิดบัญชีสิ้นปี และวิธีสร้างยอดดุลนั้นใหม่หากยอดดุลเหล่านั้นขาดหายไป
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028589"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="2ed24-103">การปิดบัญชีสิ้นปีขาดยอดดุลยกมา</span><span class="sxs-lookup"><span data-stu-id="2ed24-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ed24-104">หัวข้อนี้อธิบายเหตุผลว่าเพราะเหตุใดยอดดุลยกมาจึงอาจขาดหายไปเมื่อคุณปิดบัญชีสิ้นปี และวิธีสร้างยอดดุลนั้นใหม่หากยอดดุลเหล่านั้นขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="2ed24-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="2ed24-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="2ed24-105">Symptom</span></span>

<span data-ttu-id="2ed24-106">เพราเหตุใดจึงไม่มียอดดุลต้นงวดหลังจากรันการปิดบัญชีแยกประเภททั่วไปตอนสิ้นปี</span><span class="sxs-lookup"><span data-stu-id="2ed24-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="2ed24-107">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="2ed24-107">Resolution</span></span>

<span data-ttu-id="2ed24-108">ต่อไปนี้เป็นสิ่งที่ต้องตรวจสอบว่าคุณได้ปิดบัญชีสิ้นปีในบัญชีแยกประเภททั่วไปแล้วหรือไม่ และสร้างงบทดลองที่จะไม่แสดงยอดดุลยกมาสำหรับปีบัญชีถัดไปหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2ed24-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="2ed24-109">ถ้าการเลือกฟิลด์ **ยกเลิกการปิดก่อนหน้านี้** ตั้งค่าเป็น **ใช่** จะมีการกลับรายการปิดบัญชีสิ้นปีก่อนหน้าสำหรับปีบัญชีเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="2ed24-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="2ed24-110">เมื่อรันกระบวนการเพื่อกลับรายการปิดบัญชีสิ้นปี การป้อนรายการทั้งหมดสำหรับยอดดุลการปิดบัญชีและรายการยอดดุลยกมาทั้งหมดจะถูกลบออกเหมือนกับว่ายังไม่ได้มีการปิดบัญชีสิ้นปี</span><span class="sxs-lookup"><span data-stu-id="2ed24-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="2ed24-111">ระบบจะลบใบสำคัญออกด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="2ed24-111">The vouchers are also deleted.</span></span> <span data-ttu-id="2ed24-112">กระบวนการปิดบัญชีสิ้นปีจะไม่รันอีกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2ed24-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="2ed24-113">คุณต้องเริ่มกระบวนการอีกครั้ง โดยครั้งนี้ให้อัพเดตตัวเลือก **ยกเลิกการปิดก่อนหน้านี้** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="2ed24-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="2ed24-114">สถานการณ์นี้จะครอบคลุมอยู่ในหัวข้อคำถามที่ถามบ่อยเกี่ยวกับการปิดบัญชีสิ้นปี</span><span class="sxs-lookup"><span data-stu-id="2ed24-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="2ed24-115">ดูข้อมูลเพิ่มเติมที่ [คำถามที่ถามบ่อยเกี่ยวกับกิจกรรมตอนสิ้นปี](faq-year-end-activities.md)</span><span class="sxs-lookup"><span data-stu-id="2ed24-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="2ed24-116">อาการ</span><span class="sxs-lookup"><span data-stu-id="2ed24-116">Symptom</span></span>

<span data-ttu-id="2ed24-117">ฉันรันการปิดบัญชีสิ้นปีโดยตั้งค่าตัวเลือก **ยกเลิกการปิดก่อนหน้านี้** เป็น **ไม่** และฉันยังคงไม่มียอดดุลยกมาสำหรับปีบัญชีของฉัน</span><span class="sxs-lookup"><span data-stu-id="2ed24-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="2ed24-118">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="2ed24-118">Resolution</span></span>

<span data-ttu-id="2ed24-119">อันดับแรกให้ตรวจสอบสถานะของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2ed24-119">First check the status of the batch job.</span></span> <span data-ttu-id="2ed24-120">การปิดบัญชีสิ้นปีประกอบด้วยงานที่แยกต่างหากหลายงาน แต่ขั้นตอนที่สำคัญที่สุดคืองานในชุดงานที่มีคำอธิบายภารกิจ **ขั้นตอน 5.0.0**</span><span class="sxs-lookup"><span data-stu-id="2ed24-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="2ed24-121">การลงรายการบัญชีธุรกรรมเปิดปีและธุรกรรมปิดปีไปยังบัญชีแยกประเภททั่วไปจะเกิดขึ้นในระหว่างขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="2ed24-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="2ed24-122">[![รายการประวัติชุดงาน](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="2ed24-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="2ed24-123">ถ้าขั้นตอนนี้สิ้นสุดเสร็จเรียบร้อยแล้ว แต่คุณไม่เห็นยอดดุลยกมาในหน้า **การสอบถามงบทดลอง** (**บัญชีแยกประเภททั่วไป > การสอบถามและรายงาน > งบทดลอง**) ตรวจสอบผลลัพธ์ของชุดงานที่ปิดบัญชีเมื่อสิ้นปีเพื่อดูว่าขั้นตอนการสร้างยอดดุลอีกครั้งเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="2ed24-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="2ed24-124">[![ผลลัพธ์ของชุดงานที่ปิดบัญชีสิ้นปี](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="2ed24-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="2ed24-125">ถ้าขั้นตอนนี้ล้มเหลวด้วยเหตุผลใดก็ตาม ธุรกรรมเปิดปี (และธุรกรรมปิดปี) อาจมีแนวโน้มที่จะลงรายการบัญชีเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="2ed24-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="2ed24-126">คุณสามารถตรวจสอบว่ามีการลงรายการบัญชีธุรกรรมบัญชีแยกประเภททั่วไปเสร็จเรียบร้อยแล้วหรือไม่โดยใช้หน้า **การสอบถามธุรกรรมใบสำคัญ** ด้วยการระบุหมายเลขและวันที่ของใบสำคัญที่ระบุไว้ในกล่องโต้ตอบการปิดบัญชีสิ้นปีของปีที่คุณปิดบัญชี (**บัญชีแยกประเภททั่วไป > การสอบถามและรายงาน > ธุรกรรมใบสำคัญ**)</span><span class="sxs-lookup"><span data-stu-id="2ed24-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="2ed24-127">[![การสอบถามธุรกรรมใบสำคัญ](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="2ed24-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="2ed24-128">ถ้ามีใบสำคัญที่เปิดปี (และปิดปี) อยู่ คุณจะไม่ต้องรันการปิดบัญชีสิ้นปีอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="2ed24-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="2ed24-129">แต่ให้ดูส่วนถัดไปเพื่อทราบข้อมูลเกี่ยวกับวิธีดำเนินการต่อไปแทน</span><span class="sxs-lookup"><span data-stu-id="2ed24-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="2ed24-130">อาการ</span><span class="sxs-lookup"><span data-stu-id="2ed24-130">Symptom</span></span>

<span data-ttu-id="2ed24-131">ขั้นตอน "การสร้างยอดดุลอีกครั้ง" ในการปิดบัญชีสิ้นปีล้มเหลว ฉันต้องรันกระบวนการปิดบัญชีสิ้นปีทั้งหมดใหม่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="2ed24-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="2ed24-132">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="2ed24-132">Resolution</span></span>

<span data-ttu-id="2ed24-133">ขั้นตอนการสร้างยอดดุลอีกครั้งจะอัพเดตยอดดุลบัญชีแยกประเภททั่วไปที่ใช้เมื่อสร้างการสอบถามงบทดลอง</span><span class="sxs-lookup"><span data-stu-id="2ed24-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="2ed24-134">ซึ่งเป็นขั้นตอนสุดท้ายในกระบวนการปิดบัญชีสิ้นปี</span><span class="sxs-lookup"><span data-stu-id="2ed24-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="2ed24-135">ถ้าขั้นตอนนี้เป็นเพียงขั้นตอนเดียวที่ล้มเหลว ธุรกรรมบัญชีแยกประเภททั่วไปได้ลงรายการบัญชีเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="2ed24-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="2ed24-136">คุณไม่จำเป็นต้องรันการปิดบัญชีสิ้นปีอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="2ed24-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="2ed24-137">คุณสามารถรันกระบวนการเพื่อสร้างยอดดุลใหม่ด้วยตนเองได้โดยใช้หน้า **ชุดมิติทางการเงิน** (**บัญชีแยกประเภททั่วไป > ผังบัญชี > มิติ > ชุดมิติทางการเงิน**)</span><span class="sxs-lookup"><span data-stu-id="2ed24-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="2ed24-138">[![ปุ่มสร้างยอดดุลอีกครั้งในหน้าชุดมิติทางการเงิน](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="2ed24-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="2ed24-139">ถ้าขั้นตอนนี้ต้องใช้เวลานานในการประมวลผล เราขอแนะนำว่าควรทบทวนแนวทางปฏิบัติสำหรับชุดมิติทางการเงินตามที่อธิบายไว้ใน [แนวทางปฏิบัติสำหรับการอัพเดตชุดมิติทางการเงิน](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets)</span><span class="sxs-lookup"><span data-stu-id="2ed24-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

