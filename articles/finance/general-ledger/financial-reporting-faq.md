---
title: FAQ เกี่ยวกับการรายงานทางการเงิน
description: หัวข้อนี้แสดงรายการคำถามที่เกี่ยวข้องกับการรายงานทางการเงินที่ผู้ใช้รายอื่นมี
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2d49213ea18e09f04b026559bdca49fee1de0ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249322"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="41be4-103">FAQ เกี่ยวกับการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="41be4-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="41be4-104">หัวข้อนี้แสดงรายการคำถามที่เกี่ยวข้องกับการรายงานทางการเงินที่ผู้ใช้รายอื่นมี</span><span class="sxs-lookup"><span data-stu-id="41be4-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="41be4-105">ฉันจะจํากัดการเข้าถึงรายงานโดยใช้ความปลอดภัยแบบแผนผังได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="41be4-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="41be4-106">สถานการณ์จำลอง: บริษัทสาธิต USMF มีรายงานงบดุลซึ่งไม่ต้องการให้ผู้ใช้รายงานทางการเงินทั้งหมดสามารถดูได้ใน D365</span><span class="sxs-lookup"><span data-stu-id="41be4-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="41be4-107">วิธีการ: คุณสามารถใช้ความปลอดภัยแบบแผนผังเพื่อจํากัดการเข้าถึงรายงานเดียว เพื่อให้ผู้ใช้บางรายเท่านั้นที่สามารถเข้าถึงรายงานได้</span><span class="sxs-lookup"><span data-stu-id="41be4-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="41be4-108">ล็อกอินเข้าสู่ตัวออกแบบรายงานของโปรแกรมรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="41be4-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="41be4-109">สร้างข้อกำหนดแผนผังใหม่ (ไฟล์ | สร้าง | ข้อกำหนดแผนภูมิ) a.</span><span class="sxs-lookup"><span data-stu-id="41be4-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="41be4-110">ดับเบิลคลิกรายการ **สรุป** ในคอลัมน์ **ความปลอดภัยของหน่วย**</span><span class="sxs-lookup"><span data-stu-id="41be4-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="41be4-111">i.</span><span class="sxs-lookup"><span data-stu-id="41be4-111">i.</span></span>    <span data-ttu-id="41be4-112">คลิก ผู้ใช้และกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="41be4-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="41be4-113">1.    เลือกผู้ใช้หรือกลุ่มที่ต้องการเข้าถึงรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="41be4-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="41be4-114">[![หน้าจอผู้ใช้](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="41be4-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="41be4-115">[![หน้าจอความปลอดภัย](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="41be4-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="41be4-116">b.</span><span class="sxs-lookup"><span data-stu-id="41be4-116">b.</span></span>    <span data-ttu-id="41be4-117">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="41be4-117">Click **Save**.</span></span>
  
<span data-ttu-id="41be4-118">[![ปุ่มบันทึก](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="41be4-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="41be4-119">ในข้อกำหนดของรายงานของคุณ ให้เพิ่มข้อกำหนดแผนผังใหม่</span><span class="sxs-lookup"><span data-stu-id="41be4-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="41be4-120">[![แบบฟอร์มข้อกำหนดแผนผัง](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="41be4-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="41be4-121">A.</span><span class="sxs-lookup"><span data-stu-id="41be4-121">A.</span></span>  <span data-ttu-id="41be4-122">ขณะอยู่ในข้อกำหนดแผนผัง คลิก ตั้งค่า และภายใต้ "การเลือกหน่วยการรายงาน" เลือก "รวมหน่วยทั้งหมด"</span><span class="sxs-lookup"><span data-stu-id="41be4-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="41be4-123">[![แบบฟอร์มการเลือกหน่วยการรายงาน](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="41be4-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="41be4-124">**ก่อนหน้า:** [![ภาพหน้าจอก่อนหน้า](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="41be4-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="41be4-125">**หลังจาก:** [![ภาพหน้าจอหลังจาก](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="41be4-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="41be4-126">หมายเหตุ: สาเหตุของข้อความข้างต้นคือผู้ใช้ของฉันไม่มีสิทธิ์เข้าถึงรายงานนั้นหลังจากที่ใช้ความปลอดภัยของหน่วย</span><span class="sxs-lookup"><span data-stu-id="41be4-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="41be4-127">ฉันจะหาได้อย่างไรว่าบัญชีใดที่ไม่ตรงกับยอดดุลของฉันใน D365</span><span class="sxs-lookup"><span data-stu-id="41be4-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="41be4-128">เมื่อคุณมีรายงานที่ไม่ตรงกับสิ่งที่คุณคาดไว้ใน D365 ต่อไปนี้เป็นบางขั้นตอนที่คุณสามารถใช้ระบุบัญชีเหล่านั้นและส่วนแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="41be4-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="41be4-129">ในตัวออกแบบรายงานของโปรแกรมรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="41be4-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="41be4-130">สร้างข้อกำหนดของแถว a.</span><span class="sxs-lookup"><span data-stu-id="41be4-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="41be4-131">คลิก แก้ไข | แทรกแถวจากมิติ i.</span><span class="sxs-lookup"><span data-stu-id="41be4-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="41be4-132">เลือก MainAccount [![เลือกหน้าจอหลัก_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="41be4-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="41be4-133">ii.</span><span class="sxs-lookup"><span data-stu-id="41be4-133">ii.</span></span> <span data-ttu-id="41be4-134">คลิก ตกลง b.</span><span class="sxs-lookup"><span data-stu-id="41be4-134">Click Ok b.</span></span>    <span data-ttu-id="41be4-135">บันทึกข้อกำหนดของแถว</span><span class="sxs-lookup"><span data-stu-id="41be4-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="41be4-136">สร้างข้อกำหนดของคอลัมน์ใหม่     [![สร้างข้อกำหนดของคอลัมน์ใหม่](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="41be4-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="41be4-137">สร้างข้อกำหนดของรายงาน a.</span><span class="sxs-lookup"><span data-stu-id="41be4-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="41be4-138">คลิก การตั้งค่า และยกเลิกการเลือก [![แบบฟอร์มการตั้งค่า](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="41be4-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="41be4-139">สร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="41be4-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="41be4-140">ส่งออกรายงานไปยัง Excel</span><span class="sxs-lookup"><span data-stu-id="41be4-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="41be4-141">ใน D365:</span><span class="sxs-lookup"><span data-stu-id="41be4-141">In D365:</span></span> 
1.  <span data-ttu-id="41be4-142">คลิก บัญชีแยกประเภททั่วไป | การสอบถามและรายงาน | งบทดลอง a.</span><span class="sxs-lookup"><span data-stu-id="41be4-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="41be4-143">พารามิเตอร์ i.</span><span class="sxs-lookup"><span data-stu-id="41be4-143">Parameters i.</span></span>  <span data-ttu-id="41be4-144">วันที่เริ่มต้น: เริ่มต้นปีบัญชี ii.</span><span class="sxs-lookup"><span data-stu-id="41be4-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="41be4-145">วันที่สิ้นสุด: วันที่คุณสร้างรายงาน iii.</span><span class="sxs-lookup"><span data-stu-id="41be4-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="41be4-146">ชุดมิติทางการเงิน “ชุดบัญชีหลัก” [![แบบฟอร์มบัญชีหลัก](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="41be4-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="41be4-147">b.</span><span class="sxs-lookup"><span data-stu-id="41be4-147">b.</span></span>    <span data-ttu-id="41be4-148">คลิก คำนวณ</span><span class="sxs-lookup"><span data-stu-id="41be4-148">Click Calculate</span></span>

2.  <span data-ttu-id="41be4-149">ส่งออกรายงานไปยัง Excel</span><span class="sxs-lookup"><span data-stu-id="41be4-149">Export the report to Excel</span></span>

<span data-ttu-id="41be4-150">ตอนนี้ คุณจะสามารถคัดลอกข้อมูลจากรายงาน FR Excel และไปยังรายงานงบทดลอง D365 และเปรียบเทียบคอลัมน์ "ยอดดุลการปิดบัญชี" ได้</span><span class="sxs-lookup"><span data-stu-id="41be4-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]