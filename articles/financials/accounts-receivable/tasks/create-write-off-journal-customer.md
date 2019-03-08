---
title: สร้างสมุดรายวันการตัดจ่ายสำหรับลูกค้า
description: 'คู่มือการทำงานนี้จะแสดงวิธีการตั้งค่าพารามิเตอร์สำหรับการตัดจ่าย และตัดธุรกรรมจากหน้าการเรียกเก็บเงิน หน้าใบแจ้งหนี้ของลูกค้าเปิดและหน้าของลูกค้า '
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cd576458bab1e4654d21773b581a5b0f726c928
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "339820"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="7a16d-103">สร้างสมุดรายวันการตัดจ่ายสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a16d-104">คู่มือการทำงานนี้จะแสดงวิธีการตั้งค่าพารามิเตอร์สำหรับการตัดจ่าย และตัดธุรกรรมจากหน้าการเรียกเก็บเงิน หน้าใบแจ้งหนี้ของลูกค้าเปิดและหน้าของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="7a16d-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="7a16d-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="7a16d-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="7a16d-106">ตั้งค่าพารามิเตอร์การตัดจ่าย</span><span class="sxs-lookup"><span data-stu-id="7a16d-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="7a16d-107">ไปที่สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > พารามิเตอร์บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="7a16d-107">Go to Credit and collections > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="7a16d-108">คลิก แท็บการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7a16d-108">Click the Collections tab.</span></span>
3. <span data-ttu-id="7a16d-109">ขยายหรือยุบส่วนตัดจ่าย</span><span class="sxs-lookup"><span data-stu-id="7a16d-109">Expand or collapse the Write-off section.</span></span>
    * <span data-ttu-id="7a16d-110">สมุดรายวันการตัดจ่ายคือสมุดรายวันทั่วไปที่จะเก็บธุรกรรมการตัดจ่ายที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="7a16d-110">The Write-off journal is the general journal that will hold the write-off transactions that you create.</span></span>  
    * <span data-ttu-id="7a16d-111">คุณสามารถแนบรหัสเหตุผลสำหรับการตัดจ่ายได้ทุกครั้ง </span><span class="sxs-lookup"><span data-stu-id="7a16d-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="7a16d-112">คุณสามารถแทนค่าเริ่มต้นนี้ในขณะการตัดจ่ายได้</span><span class="sxs-lookup"><span data-stu-id="7a16d-112">You can override this default at the time of the write-off.</span></span>  
    * <span data-ttu-id="7a16d-113">ตั้งค่าตัวนี้เป็น ใช่ ถ้าคุณต้องการแยกภาษีขายออกจากธุรกรรมดั้งเดิมในการตัดจ่าย</span><span class="sxs-lookup"><span data-stu-id="7a16d-113">Set this to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="7a16d-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-114">Close the page.</span></span>
5. <span data-ttu-id="7a16d-115">ไปที่สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > โพรไฟล์การลงรายการบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-115">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
    * <span data-ttu-id="7a16d-116">บัญชีตัดจ่ายจะถูกใช้เป็นบัญชีค่าใช้จ่าย หรือจองการปรับปรุงในสมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="7a16d-116">The write-off account will be used as the expense account or reserve adjustment in the general journal</span></span>   
6. <span data-ttu-id="7a16d-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="7a16d-118">ตัดจ่ายยอดดุลของลูกค้าจากหน้ายอดดุลตามอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="7a16d-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="7a16d-119">ไปที่สินเชื่อและการเรียกเก็บเงิน > การเรียกเก็บเงิน > ยอดดุลตามอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="7a16d-119">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="7a16d-120">ทำเครื่องหมายที่แถวสำหรับลูกค้าที่คุณต้องการตัดจ่าย </span><span class="sxs-lookup"><span data-stu-id="7a16d-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="7a16d-121">ตัวอย่างเช่น ทำเครื่องหมายบรรทัดรายการที่มี บริษัท Birch อยู่</span><span class="sxs-lookup"><span data-stu-id="7a16d-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="7a16d-122">ในแผงการดำเนินการ คลิก รวบรวม</span><span class="sxs-lookup"><span data-stu-id="7a16d-122">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="7a16d-123">คลิก ตัดจ่าย</span><span class="sxs-lookup"><span data-stu-id="7a16d-123">Click Write off.</span></span>
5. <span data-ttu-id="7a16d-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7a16d-124">Click OK.</span></span>
6. <span data-ttu-id="7a16d-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-125">Close the page.</span></span>
7. <span data-ttu-id="7a16d-126">ไปที่บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="7a16d-126">Go to General ledger > Journal entries > General journals.</span></span>
8. <span data-ttu-id="7a16d-127">เลือกหมายเลขชุดงานสมุดรายวันสำหรับสมุดรายวันที่มีการตัดจ่ายของคุณอยู่</span><span class="sxs-lookup"><span data-stu-id="7a16d-127">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="7a16d-128">หนึ่งบรรทัดจะถูกสร้างขึ้นมาเพื่อกลับรายการยอดดุลลูกค้า </span><span class="sxs-lookup"><span data-stu-id="7a16d-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="7a16d-129">อีกอย่างน้อยหนึ่งบรรทัดจะถูกสร้างขึ้นเพื่อลงรายการการตัดจ่ายไปยังบัญชีตัดจ่าย</span><span class="sxs-lookup"><span data-stu-id="7a16d-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="7a16d-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-130">Close the page.</span></span>
10. <span data-ttu-id="7a16d-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="7a16d-132">ตัดจ่ายธุรกรรมจากแบบฟอร์มการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7a16d-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="7a16d-133">ไปที่สินเชื่อและการเรียกเก็บเงิน > การเรียกเก็บเงิน > ยอดดุลตามอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="7a16d-133">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="7a16d-134">เลือกชื่อของลูกค้าที่มีธุรกรรมที่คุณต้องการตัดจ่าย </span><span class="sxs-lookup"><span data-stu-id="7a16d-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="7a16d-135">ตัวอย่างเช่น เลือก Cave Wholesales (สหรัฐอเมริกา-004)</span><span class="sxs-lookup"><span data-stu-id="7a16d-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="7a16d-136">ทำเครื่องหมายบนแถวธุรกรรมที่หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7a16d-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="7a16d-137">ทำเครื่องหมายบนแถวธุรกรรมที่สอง</span><span class="sxs-lookup"><span data-stu-id="7a16d-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="7a16d-138">คลิก ตัดจ่าย</span><span class="sxs-lookup"><span data-stu-id="7a16d-138">Click Write off.</span></span>
6. <span data-ttu-id="7a16d-139">ในฟิลด์ข้อคิดเห็นเกี่ยวกับเหตุผล พิมพ์ 'Bad debts'</span><span class="sxs-lookup"><span data-stu-id="7a16d-139">In the Reason comment field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="7a16d-140">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7a16d-140">Click OK.</span></span>
8. <span data-ttu-id="7a16d-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-141">Close the page.</span></span>
9. <span data-ttu-id="7a16d-142">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-142">Close the page.</span></span>
10. <span data-ttu-id="7a16d-143">ไปที่บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="7a16d-143">Go to General ledger > Journal entries > General journals.</span></span>
11. <span data-ttu-id="7a16d-144">เลือกหมายเลขชุดงานสมุดรายวันสำหรับสมุดรายวันที่มีการตัดจ่ายของคุณอยู่</span><span class="sxs-lookup"><span data-stu-id="7a16d-144">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="7a16d-145">หนึ่งบรรทัดจะถูกสร้างขึ้นมาเพื่อกลับรายการยอดดุลลูกค้า </span><span class="sxs-lookup"><span data-stu-id="7a16d-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="7a16d-146">อีกอย่างน้อยหนึ่งบรรทัดจะถูกสร้างขึ้นเพื่อลงรายการการตัดจ่ายไปยังบัญชีตัดจ่าย</span><span class="sxs-lookup"><span data-stu-id="7a16d-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="7a16d-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-147">Close the page.</span></span>
13. <span data-ttu-id="7a16d-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="7a16d-149">ตัดจ่ายใบแจ้งหนี้จากหน้าใบแจ้งหนี้ของลูกค้าที่เปิดไว้</span><span class="sxs-lookup"><span data-stu-id="7a16d-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="7a16d-150">ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > เปิดใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-150">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="7a16d-151">ทำเครื่องหมายบรรทัดรายการสำหรับใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="7a16d-151">Mark the line for an invoice.</span></span> <span data-ttu-id="7a16d-152">ตัวอย่างเช่น ทำเครื่องหมายในรายการสำหรับ CIV-000667</span><span class="sxs-lookup"><span data-stu-id="7a16d-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="7a16d-153">ในบานหน้าต่างการดำเนินการ คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="7a16d-153">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="7a16d-154">คลิก ตัดจ่าย</span><span class="sxs-lookup"><span data-stu-id="7a16d-154">Click Write off.</span></span>
5. <span data-ttu-id="7a16d-155">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7a16d-155">Click OK.</span></span>
6. <span data-ttu-id="7a16d-156">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="7a16d-157">ตัดจ่ายยอดดุลของลูกค้าจากหน้าเพจของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="7a16d-158">ไปที่บัญชีลูกหนี้ > ลูกค้า > ลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7a16d-158">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="7a16d-159">เลือกรหัสลูกค้า </span><span class="sxs-lookup"><span data-stu-id="7a16d-159">Select a customer account.</span></span> <span data-ttu-id="7a16d-160">ตัวอย่างเช่น เลือก สหรัฐอเมริกา-001 (Contoso Retail Diego San)</span><span class="sxs-lookup"><span data-stu-id="7a16d-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="7a16d-161">ในแผงการดำเนินการ คลิก รวบรวม</span><span class="sxs-lookup"><span data-stu-id="7a16d-161">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="7a16d-162">คลิก ตัดจ่าย</span><span class="sxs-lookup"><span data-stu-id="7a16d-162">Click Write off.</span></span>
5. <span data-ttu-id="7a16d-163">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7a16d-163">Click OK.</span></span>
6. <span data-ttu-id="7a16d-164">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a16d-164">Close the page.</span></span>

