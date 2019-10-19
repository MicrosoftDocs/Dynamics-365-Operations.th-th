---
title: ปิดปีบัญชี
description: กระบวนงานนี้ระบุกระบวนการปิดบัญชีสิ้นปีที่โอนย้ายยอดดุลไปยังปีบัญชีใหม่
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c12f0842f6e8edf3b51d12d0e008eb09acf8c374
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180098"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="fd5b6-103">ปิดปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="fd5b6-103">Close the fiscal year</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd5b6-104">กระบวนงานนี้ระบุกระบวนการปิดบัญชีสิ้นปีที่โอนย้ายยอดดุลไปยังปีบัญชีใหม่</span><span class="sxs-lookup"><span data-stu-id="fd5b6-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="fd5b6-105">ตรวจสอบพารามิเตอร์การปิดบัญชีสิ้นปี</span><span class="sxs-lookup"><span data-stu-id="fd5b6-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="fd5b6-106">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > การตั้งค่าบัญชีแยกประเภท > พารามิเตอร์บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="fd5b6-107">ขยายส่วน **การปิดปีบัญชี**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="fd5b6-108">เลือก 'ใช่' หรือ 'ไม่' สำหรับตัวเลือก **ลบธุรกรรมปิดบัญชีสิ้นปีในระหว่างการโอนย้าย**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="fd5b6-109">ถ้าปิดปีบัญชีแล้ว และดำเนินการปิดบัญชีสิ้นปีอีกครั้ง จำเป็นต้องตั้งค่านี้ </span><span class="sxs-lookup"><span data-stu-id="fd5b6-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="fd5b6-110">ถ้าตั้งค่าเป็น ใช่ ใบสำคัญสำหรับการปิดบัญชีสิ้นปีก่อนหน้านี้จะถูกลบออก และจะมีการสร้างใบสำคัญใหม่สำหรับยอดดุลเมื่อเริ่มต้นในบัญชีทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="fd5b6-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="fd5b6-111">ถ้าตั้งค่าเป็น ไม่ ใบสำคัญก่อนหน้านี้จะยังคงอยู่ และจะสามารถสร้างใบสำคัญใหม่สำหรับการปรับปรุงรายการที่ถูกลงรายการบัญชีหลังจากการปิดบัญชีสิ้นปีเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fd5b6-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="fd5b6-112">เลือก 'ใช่' หรือ 'ไม่' สำหรับตัวเลือก **สร้างธุรกรรมการปิดบัญชีในระหว่างการโอนย้าย**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="fd5b6-113">ถ้าตั้งค่าเป็น ใช่ จะมีการสร้างธุรกรรมสองรายการ </span><span class="sxs-lookup"><span data-stu-id="fd5b6-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="fd5b6-114">ใบสำคัญหนึ่งจะถูกสร้างขึ้นในปีบัญชีที่กำลังจะปิดเพื่อทำให้ยอดดุลของบัญชีแยกประเภท P&L ลงไปถึงศูนย์ และจะสร้างใบสำคัญที่สองในปีบัญชีถัดไปสำหรับยอดดุลต้นงวด</span><span class="sxs-lookup"><span data-stu-id="fd5b6-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="fd5b6-115">ถ้าตั้งค่าเป็น ไม่ จะมีการสร้างใบสำคัญเดียวในปีบัญชีถัดไปสำหรับยอดดุลต้นงวด</span><span class="sxs-lookup"><span data-stu-id="fd5b6-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="fd5b6-116">เลือก 'ใช่' หรือ 'ไม่' สำหรับตัวเลือก **ตั้งค่าสถานะปีบัญชีให้ปิดอย่างถาวร**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="fd5b6-117">ถ้าตั้งค่าเป็น ใช่ สถานะจะถูกตั้งค่าเป็นปิดถาวร </span><span class="sxs-lookup"><span data-stu-id="fd5b6-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="fd5b6-118">เนื่องจากไม่สามารถเปิดปีที่ปิดอย่างถาวรใหม่ได้ จึงควรตั้งค่าตัวเลือกนี้เป็น ไม่</span><span class="sxs-lookup"><span data-stu-id="fd5b6-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="fd5b6-119">เลือก 'ใช่' หรือ 'ไม่' สำหรับตัวเลือก **ต้องมีการกรอกข้อมูลหมายเลขใบสำคัญในระหว่างการปิดบัญชีสิ้นปี**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="fd5b6-120">ถ้าตั้งค่าเป็น ใช่ หมายเลขใบสำคัญจะต้องถูกป้อนด้วยตนเองในระหว่างกระบวนการปิดบัญชีสิ้นปี </span><span class="sxs-lookup"><span data-stu-id="fd5b6-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="fd5b6-121">ไม่มีการใช้ลำดับหมายเลขในการสร้างหมายเลขใบสำคัญนี้ </span><span class="sxs-lookup"><span data-stu-id="fd5b6-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="fd5b6-122">ควรตั้งค่าเป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="fd5b6-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="fd5b6-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fd5b6-123">Close the page.</span></span>
8. <span data-ttu-id="fd5b6-124">ไปที่ **บัญชีแยกประเภททั่วไป > การปิดรอบระยะเวลา > การปิดบัญชีสิ้นปี**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="fd5b6-125">คลิก **สร้าง** เพื่อสร้างเท็มเพลตการปิดบัญชีสิ้นปี</span><span class="sxs-lookup"><span data-stu-id="fd5b6-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="fd5b6-126">สามารถสร้างเท็มเพลตสำหรับกลุ่มของกฎหมายเอนทิตี้ที่จะดำเนินการปิดบัญชีสิ้นปี </span><span class="sxs-lookup"><span data-stu-id="fd5b6-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="fd5b6-127">สามารถนำเท็มเพลตนี้มาใช้ซ้ำในแต่ละปีได้</span><span class="sxs-lookup"><span data-stu-id="fd5b6-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="fd5b6-128">ในฟิลด์ **ชื่อกลุ่ม** ป้อนชื่อเท็มเพลตการปิดบัญชีสิ้นปี</span><span class="sxs-lookup"><span data-stu-id="fd5b6-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="fd5b6-129">ในฟิลด์ **ปฏิทินทางการเงิน** ให้เลือกปีบัญชีที่จะสร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="fd5b6-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="fd5b6-130">สามารถจัดกลุ่มเฉพาะนิติบุคคลที่ใช้ปีบัญชีเดียวกันในเท็มเพลตการปิดบัญชีสิ้นปี </span><span class="sxs-lookup"><span data-stu-id="fd5b6-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="fd5b6-131">ทั้งนี้เนื่องจากการปิดบัญชีสิ้นปีจะเสร็จสิ้นโดยการเลือกปีบัญชี ไม่ใช่วันที่</span><span class="sxs-lookup"><span data-stu-id="fd5b6-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="fd5b6-132">ใน **บานหน้าต่างการดำเนินการ** คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="fd5b6-133">ในส่วน **นิติบุคคล** ให้คลิก **เพิ่ม** เพื่อเลือกนิติบุคคลสำหรับเท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="fd5b6-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="fd5b6-134">สามารถเพิ่มนิติบุคคลได้โดยการเลือกนิติบุคคลหรือลำดับชั้นองค์กร </span><span class="sxs-lookup"><span data-stu-id="fd5b6-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="fd5b6-135">จะสามารถเพิ่มได้เฉพาะนิติบุคคลที่มีลำดับชั้นองค์กรที่มีปฏิทินทางการเงินเดียวกันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fd5b6-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="fd5b6-136">เลือกนิติบุคคลหรือลำดับชั้นองค์กร</span><span class="sxs-lookup"><span data-stu-id="fd5b6-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="fd5b6-137">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-137">Click **OK**.</span></span>
16. <span data-ttu-id="fd5b6-138">เลือก 'ใช่' หรือ 'ไม่ใช่' ใน **ถ่ายโอนมิติงบดุล**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="fd5b6-139">แนวทางปฏิบัติที่ดีที่สุดคือ การตั้งค่าตัวเลือกนี้เป็น ใช่ สำหรับบัญชีงบดุล</span><span class="sxs-lookup"><span data-stu-id="fd5b6-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="fd5b6-140">ซึ่งจะรักษามิติทางการเงินเกี่ยวกับธุรกรรมที่ลงรายการบัญชีเมื่อสร้างยอดดุลเริ่มต้นสำหรับบัญชีงบดุล </span><span class="sxs-lookup"><span data-stu-id="fd5b6-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="fd5b6-141">สำหรับบัญชีกำไรขาดทุน คุณสามารถเลือกที่จะรักษามิติทางการเงิน (ปิดทั้งหมด) เมื่อยอดดุลถูกย้ายไปเป็นกำไรที่ยังไม่ได้จัดสรร หรือคุณสามารถเลือกให้แทนที่มิติทางการเงินด้วยค่ามิติอื่น (ปิดรายการเดียว) ได้ </span><span class="sxs-lookup"><span data-stu-id="fd5b6-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="fd5b6-142">ถ้าคุณเลือก ปิดรายการเดียว คุณสามารถกำหนดค่ามิติเฉพาะสำหรับแต่ละมิติ หรือสามารถเลือกที่จะเว้นว่างไว้ได้</span><span class="sxs-lookup"><span data-stu-id="fd5b6-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="fd5b6-143">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-143">Click **Save**.</span></span>
18. <span data-ttu-id="fd5b6-144">เริ่มต้นการปิดบัญชีสิ้นปีโดยเลือก **รันการปิดรอบบัญชี** บน **บานหน้าต่างการดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="fd5b6-145">ระบบจะดำเนินการปิดบัญชีสิ้นปีสำหรับเท็มเพลตที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fd5b6-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="fd5b6-146">เลือกนิติบุคคลทั้งหมดหรือชุดย่อยจากเท็มเพลตเพื่อดำเนินการปิดบัญชีสิ้นปี</span><span class="sxs-lookup"><span data-stu-id="fd5b6-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="fd5b6-147">ในขณะที่รันการปิดบัญชีสิ้นปีครั้งแรก เพื่อให้ได้ยอดดุลเริ่มต้น องค์กรส่วนใหญ่อาจเลือกที่จะรันการปิดบัญชีสิ้นปีสำหรับนิติบุคคลทั้งหมดภายในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="fd5b6-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="fd5b6-148">ถ้ามีการปรับปรุงรายการหลังจากนั้น คุณอาจเลือกที่จะดำเนินการปิดบัญชีสิ้นปีสำหรับเฉพาะนิติบุคคลที่มีการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="fd5b6-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="fd5b6-149">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-149">Click **OK**.</span></span>
21. <span data-ttu-id="fd5b6-150">เลือกปีบัญชีที่จะดำเนินการปิดบัญชีสิ้นปี</span><span class="sxs-lookup"><span data-stu-id="fd5b6-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="fd5b6-151">ใน **ฟิลด์ใบสำคัญ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="fd5b6-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="fd5b6-152">แนวทางปฏิบัติที่ดีที่สุดคือ การรวมปีบัญชีในหมายเลขใบสำคัญ เพื่อทำให้ง่ายในการค้นหาใบสำคัญการปิดบัญชีสิ้นปีที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="fd5b6-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="fd5b6-153">การปิดบัญชีสิ้นปีจะถูกกำหนดเป็นค่าเริ่มต้นให้ดำเนินการเป็นชุดงาน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="fd5b6-154">แนวทางปฏิบัติที่ดีที่สุดสำหรับกระบวนการที่รันเป็นเวลานานที่จะรันในโหมดชุดงาน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="fd5b6-155">โดยทั่วไปมักเป็นหนึ่งในกระบวนการเหล่านั้น ซึ่งเป็นสาเหตุที่ค่าเริ่มต้นคือการใช้โหมดชุดงาน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="fd5b6-156">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-156">Click **OK**.</span></span>

