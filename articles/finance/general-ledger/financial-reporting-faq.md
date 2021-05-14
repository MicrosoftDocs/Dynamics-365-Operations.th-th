---
title: คำถามที่ถามบ่อยเกี่ยวกับการรายงานทางการเงิน
description: หัวข้อนี้แสดงรายการคำถามที่เกี่ยวข้องกับการรายงานทางการเงินที่ผู้ใช้รายอื่นมี
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923036"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="d1742-103">คำถามที่ถามบ่อยเกี่ยวกับการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="d1742-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="d1742-104">หัวข้อนี้แสดงคําตอบของคําถามที่ถามบ่อยเกี่ยวกับการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="d1742-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="d1742-105">ฉันจะจํากัดการเข้าถึงรายงานโดยใช้ความปลอดภัยแบบแผนผังได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="d1742-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="d1742-106">ตัวอย่างต่อไปนี้แสดงวิธีการจํากัดการเข้าถึงรายงานโดยใช้ความปลอดภัยแบบแผนผัง</span><span class="sxs-lookup"><span data-stu-id="d1742-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="d1742-107">บริษัทสาธิต USMF มีรายงานงบดุลที่ผู้ใช้รายงานทางการเงินบางรายเท่านั้นควรมีสิทธิ์เข้าถึง</span><span class="sxs-lookup"><span data-stu-id="d1742-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="d1742-108">หากต้องการจำกัดการเข้าถึง คุณสามารถใช้ความปลอดภัยแบบแผนผังเพื่อจํากัดการเข้าถึงรายงานเดียว เพื่อให้ผู้ใช้บางรายเท่านั้นที่สามารถเข้าถึงรายงานได้</span><span class="sxs-lookup"><span data-stu-id="d1742-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="d1742-109">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อจํากัดการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="d1742-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="d1742-110">ลงชื่อเข้าใช้ Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="d1742-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="d1742-111">สร้างข้อกำหนดของแผนผังใหม่</span><span class="sxs-lookup"><span data-stu-id="d1742-111">Create a new tree definition.</span></span> <span data-ttu-id="d1742-112">ไปที่ **ไฟล์ > ใหม่ > ข้อกำหนดของแผนผัง**</span><span class="sxs-lookup"><span data-stu-id="d1742-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="d1742-113">ดับเบิลคลิกรายการ **สรุป** ในคอลัมน์ **ความปลอดภัยของหน่วย**</span><span class="sxs-lookup"><span data-stu-id="d1742-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="d1742-114">เลือก **ผู้ใช้และกลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="d1742-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="d1742-115">เลือกผู้ใช้หรือกลุ่มที่ต้องเข้าถึงรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="d1742-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="d1742-116">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d1742-116">Select **Save**.</span></span>
7. <span data-ttu-id="d1742-117">ในข้อกำหนดของรายงาน ให้เพิ่มข้อกำหนดแผนผังใหม่</span><span class="sxs-lookup"><span data-stu-id="d1742-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="d1742-118">ในข้อกำหนดของแผนผัง ให้เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="d1742-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="d1742-119">ภายใต้ **การเลือกหน่วยการรายงาน** ให้เลือก **รวมหน่วยทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="d1742-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="d1742-120">ฉันจะระบุได้อย่างไรว่าบัญชีใดไม่ตรงกับยอดดุลของฉัน</span><span class="sxs-lookup"><span data-stu-id="d1742-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="d1742-121">หากคุณมีรายงานที่ไม่มียอดดุลตรงกัน ต่อไปนี้เป็นบางขั้นตอนที่คุณสามารถใช้ระบุแต่ละบัญชีเหล่านั้นและส่วนแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="d1742-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="d1742-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="d1742-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="d1742-123">ใน Financial Reporter Report Designer ให้สร้างข้อกำหนดของแถวใหม่</span><span class="sxs-lookup"><span data-stu-id="d1742-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="d1742-124">เลือก **แก้ไข > แทรกแถวจากมิติ**</span><span class="sxs-lookup"><span data-stu-id="d1742-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="d1742-125">เลือก **MainAccount**</span><span class="sxs-lookup"><span data-stu-id="d1742-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="d1742-126">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d1742-126">Select **OK**.</span></span>
5. <span data-ttu-id="d1742-127">บันทึกข้อกำหนดของแถว</span><span class="sxs-lookup"><span data-stu-id="d1742-127">Save the row definition.</span></span>
6. <span data-ttu-id="d1742-128">สร้างข้อกำหนดของคอลัมน์ใหม่</span><span class="sxs-lookup"><span data-stu-id="d1742-128">Create a new column definition</span></span>
7. <span data-ttu-id="d1742-129">สร้างข้อกำหนดของรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="d1742-129">Create a new report definition.</span></span>
8. <span data-ttu-id="d1742-130">เลือก **การตั้งค่า** และยกเลิกการเลือกตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="d1742-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="d1742-131">สร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="d1742-131">Generate the report.</span></span> 
10. <span data-ttu-id="d1742-132">ส่งออกรายงานไปยัง Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="d1742-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="d1742-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="d1742-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="d1742-134">ใน Dynamics 365 Finance ไปที่ **บัญชีแยกประเภททั่วไป > การสอบถามและรายงาน > งบทดลอง**</span><span class="sxs-lookup"><span data-stu-id="d1742-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="d1742-135">ตั้งค่าพารามิเตอร์ดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d1742-135">Set the following parameters:</span></span>
   - <span data-ttu-id="d1742-136">**วันที่เริ่มต้น** - ป้อนการเริ่มต้นของปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="d1742-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="d1742-137">**วันที่สิ้นสุด** - ป้อนวันที่ที่คุณสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="d1742-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="d1742-138">**มิติทางการเงิน** - ตั้งค่าฟิลด์นี้เป็น **ชุดบัญชีหลัก**</span><span class="sxs-lookup"><span data-stu-id="d1742-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="d1742-139">เลือก **คำนวณ**</span><span class="sxs-lookup"><span data-stu-id="d1742-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="d1742-140">ส่งออกรายงานไปยัง Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="d1742-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="d1742-141">ตอนนี้ คุณจะสามารถคัดลอกข้อมูลจากรายงาน Excel ของโปรแกรมรายงานทางการเงินไปยังรายงานงบทดลอง เพื่อให้คุณสามารถเปรียบเทียบคอลัมน์ **ยอดดุลการปิดบัญชี** ได้</span><span class="sxs-lookup"><span data-stu-id="d1742-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]