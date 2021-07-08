---
title: คำถามที่ถามบ่อยเกี่ยวกับการรายงานทางการเงิน
description: หัวข้อนี้แสดงคําตอบของคําถามที่ถามบ่อยบางส่วนเกี่ยวกับการรายงานทางการเงิน
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266644"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="d4c42-103">คำถามที่ถามบ่อยเกี่ยวกับการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="d4c42-103">Financial reporting FAQ</span></span>

<span data-ttu-id="d4c42-104">หัวข้อนี้แสดงคําตอบของคําถามที่ถามบ่อยเกี่ยวกับการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="d4c42-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="d4c42-105">ฉันจะจํากัดการเข้าถึงรายงานโดยใช้ความปลอดภัยแบบแผนผังได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="d4c42-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="d4c42-106">ตัวอย่างต่อไปนี้แสดงวิธีการจํากัดการเข้าถึงรายงานโดยใช้ความปลอดภัยแบบแผนผัง</span><span class="sxs-lookup"><span data-stu-id="d4c42-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="d4c42-107">บริษัทสาธิต USMF มีรายงาน **งบดุล** ที่ผู้ใช้รายงานทางการเงินบางรายเท่านั้นควรมีสิทธิ์เข้าถึง</span><span class="sxs-lookup"><span data-stu-id="d4c42-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="d4c42-108">คุณสามารถใช้ความปลอดภัยแบบแผนผังเพื่อจํากัดการเข้าถึงรายงานเดียวเพื่อให้ผู้ใช้เฉพาะรายเท่านั้นที่สามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="d4c42-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="d4c42-109">ลงชื่อเข้าใช้ Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="d4c42-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="d4c42-110">เลือก **ไฟล์ \> ใหม่ \> ข้อกำหนดแผนผัง** เพื่อสร้างข้อกำหนดแผนผังใหม่</span><span class="sxs-lookup"><span data-stu-id="d4c42-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="d4c42-111">แตะสองครั้ง (หรือดับเบิลคลิก) รายการ **สรุป** ในคอลัมน์ **ความปลอดภัยของหน่วย**</span><span class="sxs-lookup"><span data-stu-id="d4c42-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="d4c42-112">เลือก **ผู้ใช้และกลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="d4c42-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="d4c42-113">เลือกผู้ใช้หรือกลุ่มที่ต้องเข้าถึงรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="d4c42-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="d4c42-114">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d4c42-114">Select **Save**.</span></span>
7. <span data-ttu-id="d4c42-115">ในข้อกำหนดของรายงาน ให้เพิ่มข้อกำหนดแผนผังใหม่</span><span class="sxs-lookup"><span data-stu-id="d4c42-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="d4c42-116">ในข้อกำหนดของแผนผัง ให้เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="d4c42-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="d4c42-117">จากนั้นภายใต้ **การเลือกหน่วยการรายงาน** ให้เลือก **รวมหน่วยทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="d4c42-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="d4c42-118">ฉันจะระบุได้อย่างไรว่าบัญชีใดไม่ตรงกับยอดดุลของฉัน</span><span class="sxs-lookup"><span data-stu-id="d4c42-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="d4c42-119">หากคุณมีรายงานที่ไม่มียอดดุลตรงกัน ให้ใช้ขั้นตอนต่อไปนี้เพื่อระบุแต่ละบัญชีและส่วนแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="d4c42-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="d4c42-120">ใน Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="d4c42-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="d4c42-121">สร้างข้อกำหนดของแถวใหม่</span><span class="sxs-lookup"><span data-stu-id="d4c42-121">Create a new row definition.</span></span>
2. <span data-ttu-id="d4c42-122">เลือก **แก้ไข \> แทรกแถวจากมิติ**</span><span class="sxs-lookup"><span data-stu-id="d4c42-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="d4c42-123">เลือก **MainAccount**</span><span class="sxs-lookup"><span data-stu-id="d4c42-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="d4c42-124">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d4c42-124">Select **OK**.</span></span>
5. <span data-ttu-id="d4c42-125">บันทึกข้อกำหนดของแถว</span><span class="sxs-lookup"><span data-stu-id="d4c42-125">Save the row definition.</span></span>
6. <span data-ttu-id="d4c42-126">สร้างข้อกำหนดของคอลัมน์ใหม่</span><span class="sxs-lookup"><span data-stu-id="d4c42-126">Create a new column definition.</span></span>
7. <span data-ttu-id="d4c42-127">สร้างข้อกำหนดของรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="d4c42-127">Create a new report definition.</span></span>
8. <span data-ttu-id="d4c42-128">เลือก **การตั้งค่า** และยกเลิกการเลือกตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="d4c42-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="d4c42-129">สร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="d4c42-129">Generate the report.</span></span> 
10. <span data-ttu-id="d4c42-130">ส่งออกรายงานไปยัง Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="d4c42-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="d4c42-131">ใน Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="d4c42-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="d4c42-132">ไปที่ **บัญชีแยกประเภททั่วไป \> การสอบถามและรายงาน \> งบทดลอง**</span><span class="sxs-lookup"><span data-stu-id="d4c42-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="d4c42-133">ตั้งค่าฟิลด์เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="d4c42-133">Set the following fields:</span></span>

    - <span data-ttu-id="d4c42-134">**วันที่เริ่มต้น** – ป้อนวันที่เริ่มต้นของปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="d4c42-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="d4c42-135">**วันที่สิ้นสุด** – ป้อนวันที่ที่คุณสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="d4c42-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="d4c42-136">**มิติทางการเงิน** – ตั้งค่าฟิลด์นี้เป็น **ชุดบัญชีหลัก**</span><span class="sxs-lookup"><span data-stu-id="d4c42-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="d4c42-137">เลือก **คำนวณ**</span><span class="sxs-lookup"><span data-stu-id="d4c42-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="d4c42-138">ส่งออกรายงานไปยัง Excel</span><span class="sxs-lookup"><span data-stu-id="d4c42-138">Export the report to Excel.</span></span>

<span data-ttu-id="d4c42-139">ตอนนี้ คุณจะสามารถคัดลอกข้อมูลจากรายงาน Excel ของ Financial Reporter ไปยังรายงาน **งบทดลอง** เพื่อให้คุณสามารถเปรียบเทียบคอลัมน์ **ยอดดุลการปิดบัญชี** ได้</span><span class="sxs-lookup"><span data-stu-id="d4c42-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="d4c42-140">เมื่อฉันออกแบบรายงานใน Report Designer หรือเมื่อฉันสร้างรายงานทางการเงิน ฉันได้รับข้อความต่อไปนี้: "การดําเนินการไม่เสร็จสมบูรณ์เนื่องจากปัญหาในกรอบงานของตัวให้บริการข้อมูล"</span><span class="sxs-lookup"><span data-stu-id="d4c42-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="d4c42-141">ฉันควรจัดการอย่างไร</span><span class="sxs-lookup"><span data-stu-id="d4c42-141">How should I respond?</span></span>

<span data-ttu-id="d4c42-142">ข้อความดังกล่าวระบุว่าเกิดปัญหาขึ้นเมื่อระบบพยายามดึงข้อมูลเมตาทางการเงินจาก Data Mart ขณะที่คุณใช้การรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="d4c42-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="d4c42-143">การจัดการปัญหานี้มีอยู่สองวิธีดังนี้</span><span class="sxs-lookup"><span data-stu-id="d4c42-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="d4c42-144">ตรวจทานสถานะการรวมของข้อมูลโดยไปที่สถานะ **เครื่องมือ \> สถานะการรวม** ใน Report Designer</span><span class="sxs-lookup"><span data-stu-id="d4c42-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="d4c42-145">ถ้าการรวมไม่สมบูรณ์ ให้รอจนการรวมนั้นเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="d4c42-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="d4c42-146">แล้วลองทำสิ่งที่คุณกำลังดำเนินการเมื่อคุณได้รับข้อความอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="d4c42-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="d4c42-147">ติดต่อฝ่ายสนับสนุนเพื่อค้นหาและแก้ไขปัญหาดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="d4c42-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="d4c42-148">อาจมีข้อมูลไม่สอดคล้องกันในระบบ</span><span class="sxs-lookup"><span data-stu-id="d4c42-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="d4c42-149">วิศวกรสนับสนุนสามารถช่วยคุณระบุปัญหานั้นบนเซิร์ฟเวอร์และค้นหาข้อมูลเฉพาะที่อาจต้องมีการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="d4c42-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
