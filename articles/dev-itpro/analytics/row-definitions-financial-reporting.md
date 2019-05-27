---
title: คำนิยามแถวในผู้ออกแบบรายงานทางการเงิน
description: คำนิยามแถวคือองค์ประกอบของรายงานหรือบล็อคส่วนประกอบที่ระบุเนื้อหาของแต่ละแถวในรายงานทางการเงิน คำนิยามแถวสามารถรวมกับคำนิยามคอลัมน์ คำนิยามแผนภูมิการรายงาน และข้อกำหนดของรายงาน เพื่อสร้างกลุ่มการสร้างบล็อคที่สามารถใช้โดยบริษัทหลายบริษัท
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c829af1da1b3109f4687c9a2536dd156339d5c76
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551612"
---
# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="36c8b-104">คำนิยามแถวในผู้ออกแบบรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="36c8b-104">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36c8b-105">คำนิยามแถวคือองค์ประกอบของรายงานหรือบล็อคส่วนประกอบที่ระบุเนื้อหาของแต่ละแถวในรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="36c8b-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="36c8b-106">คำนิยามแถวสามารถรวมกับคำนิยามคอลัมน์ คำนิยามแผนภูมิการรายงาน และข้อกำหนดของรายงาน เพื่อสร้างกลุ่มการสร้างบล็อคที่สามารถใช้โดยบริษัทหลายบริษัท</span><span class="sxs-lookup"><span data-stu-id="36c8b-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="36c8b-107">การสร้างคำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="36c8b-107">Create a row definition</span></span>

1. <span data-ttu-id="36c8b-108">ใน Report Designer ในบานหน้าต่างนำทาง คลิก **คำนิยามแถว**</span><span class="sxs-lookup"><span data-stu-id="36c8b-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="36c8b-109">บนเมนู **ไฟล์** ให้คลิก **สร้าง** แล้วจึงคลิก **คำนิยามแถว**</span><span class="sxs-lookup"><span data-stu-id="36c8b-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="36c8b-110">ดูข้อมูลเพิ่มเติมเกี่ยวกับเนื้อหาของแต่ละเซลล์ ให้ดู [แก้ไขเซลล์คำนิยามแถว](modify-row-definition-cells-financial-reporting.md)</span><span class="sxs-lookup"><span data-stu-id="36c8b-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="36c8b-111">เปิดคำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="36c8b-111">Open a row definition</span></span>
1. <span data-ttu-id="36c8b-112">ใน Report Designer ในบานหน้าต่างนำทาง คลิก **คำนิยามแถว**</span><span class="sxs-lookup"><span data-stu-id="36c8b-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="36c8b-113">ดับเบิลคลิกชื่อของคำนิยามแถวเพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="36c8b-113">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="36c8b-114">หากต้องการดูบล็อคส่วนประกอบใดๆ ที่เชื่อมโยงกับคำนิยามแถว ให้คลิกขวาที่คำนิยามแถว จากนั้นเลือก **การเชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="36c8b-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="36c8b-115"> เนื้อหาของคำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="36c8b-115">Contents of a row definition</span></span>
<span data-ttu-id="36c8b-116">คำนิยามแถวสามารถประกอบด้วยแถวมิติทางการเงินกว่า 20000 แถว และอาจรวมถึงข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="36c8b-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="36c8b-117">ข้อความอธิบายที่เพิ่มความหมายให้กับรายงาน โดยการสร้างหัวข้อส่วนหัว บรรทัด และเว้นวรรค เช่น **เงินสด** หรือ **รายได้รวม**</span><span class="sxs-lookup"><span data-stu-id="36c8b-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="36c8b-118">ลิงค์ไปยังข้อมูลทางการเงิน ซึ่งสามารถรวมค่ามิติใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="36c8b-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 for Finance and Operations</span></span>

    > [!NOTE]
    > <span data-ttu-id="36c8b-119">คุณสามารถตั้งค่าคำนิยามแถวให้มีการดึงข้อมูลจากระบบมิติทางการเงินทุกครั้งที่มีการสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="36c8b-119">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="36c8b-120">ผลรวมและสูตรของแถวที่ขึ้นอยู่กับข้อมูลทางการเงินที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="36c8b-120">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="36c8b-121">โดยปกติ แต่ละแถวในคำนิยามแถวจะประกอบด้วยชนิดของข้อมูลหนึ่งชนิดดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="36c8b-121">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="36c8b-122">การอ้างอิงไปยังระบบมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="36c8b-122">References to the financial dimensions system</span></span>
- <span data-ttu-id="36c8b-123">ยอดรวมหรือการคำนวณที่อิงตามข้อมูล</span><span class="sxs-lookup"><span data-stu-id="36c8b-123">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="36c8b-124">การจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="36c8b-124">Formatting</span></span>

<span data-ttu-id="36c8b-125">มีสองวิธีสำหรับการป้อนข้อมูลในคำนิยามแถว:</span><span class="sxs-lookup"><span data-stu-id="36c8b-125">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="36c8b-126">ป้อนข้อมูลแถวด้วยตนเองลงในคำนิยามแถวใหม่</span><span class="sxs-lookup"><span data-stu-id="36c8b-126">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="36c8b-127">ดูข้อมูลเพิ่มเติมที่ [แก้ไขเซลล์คำนิยามแถว](modify-row-definition-cells-financial-reporting.md)</span><span class="sxs-lookup"><span data-stu-id="36c8b-127">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="36c8b-128">ใช้ผู้ออกแบบรายงานเพื่อดึงแถวข้อมูลโดยตรงจากมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="36c8b-128">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="36c8b-129">สำหรับข้อมูลเพิ่มเติม ให้ดูส่วน "สูตร/แถว/หน่วย ที่เกี่ยวข้อง" ใน [การแก้ไขเซลล์คำนิยามแถว](modify-row-definition-cells-financial-reporting.md)</span><span class="sxs-lookup"><span data-stu-id="36c8b-129">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="36c8b-130"> เพิ่มมิติในคำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="36c8b-130">Add dimensions in a row definition</span></span>
<span data-ttu-id="36c8b-131">มิติคือส่วนร่วมของข้อมูลและค่า</span><span class="sxs-lookup"><span data-stu-id="36c8b-131">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="36c8b-132">คุณสามารถจัดกลุ่มข้อมูลและค่าด้วยกันในผู้ออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="36c8b-132">You can group data and values in report designer.</span></span> <span data-ttu-id="36c8b-133">จากนั้นคุณสามารถจัดประเภทและวิเคราะห์ธุรกรรมโดยละเอียดมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="36c8b-133">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="36c8b-134">คุณสามารถใช้กล่องโต้ตอบ **แทรกแถวจากมิติ** เพื่อเพิ่มแถวหลายแถวที่มีคำนิยามแถวในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="36c8b-134">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="36c8b-135">กล่องโต้ตอบแสดงคอลัมน์หนึ่งคอลัมน์สำหรับแต่ละมิติ</span><span class="sxs-lookup"><span data-stu-id="36c8b-135">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="36c8b-136">ตารางต่อไปนี้อธิบายข้อมูลที่คุณสามารถระบุสำหรับแต่ละมิติ</span><span class="sxs-lookup"><span data-stu-id="36c8b-136">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="36c8b-137">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="36c8b-137">Option</span></span>                | <span data-ttu-id="36c8b-138">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="36c8b-138">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="36c8b-139">มิติ</span><span class="sxs-lookup"><span data-stu-id="36c8b-139">Dimension</span></span>             | <span data-ttu-id="36c8b-140">รูปแบบซึ่งจะระบุมิติที่จะเพิ่มไปยังคำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="36c8b-140">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="36c8b-141">รูปแบบนี้จะประกอบด้วยเครื่องหมาย (&) หรือเครื่องหมายตัวเลข (\#) สำหรับแต่ละตำแหน่งในมิติ</span><span class="sxs-lookup"><span data-stu-id="36c8b-141">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="36c8b-142">โดยทั่วไป จะใช้เครื่องหมายทั้งหมดสำหรับมิติบัญชีหลักและเครื่องหมายตัวเลขทั้งหมดสำหรับมิติอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="36c8b-142">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="36c8b-143">เริ่มช่วงมิติ</span><span class="sxs-lookup"><span data-stu-id="36c8b-143">Dimension Range Start</span></span> | <span data-ttu-id="36c8b-144">ค่าแรกสำหรับมิตินี้ที่ต้องการเพิ่มไปที่คำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="36c8b-144">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="36c8b-145">สิ้นสุดช่วงมิติ</span><span class="sxs-lookup"><span data-stu-id="36c8b-145">Dimension Range End</span></span>   | <span data-ttu-id="36c8b-146">ค่าสุดท้ายสำหรับมิตินี้เพื่อเพิ่มคำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="36c8b-146">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="36c8b-147">เมื่อต้องการเพิ่มมิติลงในคำนิยามแถว ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="36c8b-147">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="36c8b-148">ในโปรแกรมออกแบบรายงาน คลิก **คำนิยามแถว** แล้วจึงเปิดคำนิยามแถวเพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="36c8b-148">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="36c8b-149">ในเมนู **แก้ไข** คลิก **แทรกแถวจากมิติ**</span><span class="sxs-lookup"><span data-stu-id="36c8b-149">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="36c8b-150">ในกล่องโต้ตอบ **แทรกแถวจากมิติ**ในแถว **มิติ** เลือกเซลล์สำหรับมิติที่จะถูกโอนย้ายไปยังคำนิยามแถว แล้วจึงคลิก **ทั้งหมด & & &**</span><span class="sxs-lookup"><span data-stu-id="36c8b-150">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="36c8b-151">เมื่อต้องการจำกัดคำนิยามแถวให้กับช่วงเฉพาะของค่ามิติ ป้อนค่ามิติเริ่มต้นในเซลล์ **เริ่มต้นช่วงมิติ**จากนั้นป้อนค่ามิติสิ้นสุดในเซลล์ **สิ้นสุดของช่วงมิติ**</span><span class="sxs-lookup"><span data-stu-id="36c8b-151">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="36c8b-152">หากต้องการรวมค่าทั้งหมดสำหรับมิติที่เลือก ให้ปล่อยเซลล์เหล่านี้ให้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="36c8b-152">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="36c8b-153">อักขระตัวแทน (\* or ?) ในช่วงมิติอาจไม่ส่งคืนผลลัพธ์ทั้งหมดที่คุณต้องการ โดยขึ้นอยู่กับวิธีการที่ฐานข้อมูล ERP สอบทานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="36c8b-153">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="36c8b-154">ในฟิลด์ **เริ่มต้นรหัสแถว** ระบุรหัสแถวสำหรับค่ามิติแรกที่จะเพิ่มไปยังคำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="36c8b-154">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="36c8b-155">ในฟิลด์ **เพิ่มแต่ละแถวโดย** ระบุความแตกต่างระหว่างรหัสแถวที่ต่อเนื่องกัน</span><span class="sxs-lookup"><span data-stu-id="36c8b-155">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="36c8b-156">ตัวอย่างเช่น ถ้ารหัสแถวแรกเป็น 100 และค่าที่เพิ่มขึ้นคือ 30 แถวใหม่แถวแรกๆ จะมีรหัส 100, 130, 160, 190 และ 220</span><span class="sxs-lookup"><span data-stu-id="36c8b-156">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="36c8b-157">ใช้ค่าเพิ่มขึ้นที่มีช่องว่างสำหรับการแทรกแถวรูปแบบและสูตรใหม่</span><span class="sxs-lookup"><span data-stu-id="36c8b-157">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="36c8b-158">คลิก **ตกลง** ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="36c8b-158">Click **OK**.</span></span> <span data-ttu-id="36c8b-159">สำหรับค่ามิติที่เลือกแต่ละค่า บรรทัดหนึ่งบรรทัดจะถูกเพิ่มไปยังคำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="36c8b-159">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="36c8b-160"> ปรับปรุงการปัดเศษในคำนิยามแถว</span><span class="sxs-lookup"><span data-stu-id="36c8b-160">Adjust rounding in a row definition</span></span>
<span data-ttu-id="36c8b-161">ถ้าคุณมีงบดุลที่ยอดเงินถูกปัดเศษแล้ว ยอดรวมอาจมีการเสียดุล</span><span class="sxs-lookup"><span data-stu-id="36c8b-161">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="36c8b-162">ปัญหานี้อาจเกิดขึ้นได้ถ้า ตัวอย่างเช่น คุณใช้ตัวเลือกการปัดเศษในรายงานงบดุล และข้อกำหนดของรายงานยังระบุการปัดเศษอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="36c8b-162">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="36c8b-163">คุณสามารถใช้ตัวเลือก **การปรับปรุงการปัดเศษ** ในคำนิยามแถวเพื่อให้ยอดเงินในงบดุลสมดุล</span><span class="sxs-lookup"><span data-stu-id="36c8b-163">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="36c8b-164">คุณสามารถปิดหรือแก้ไขการปัดเศษบนแท็บ **การตั้งค่า** ของข้อกำหนดของรายงานได้</span><span class="sxs-lookup"><span data-stu-id="36c8b-164">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="36c8b-165">ตารางต่อไปนี้แสดงวิธีการปัดเศษยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="36c8b-165">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="36c8b-166">ในตารางนี้ ผลรวมของแถว 100 และ 200 แตกต่างกันเมื่อการปัดเศษถูกเปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="36c8b-166">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="36c8b-167">รหัสแถว</span><span class="sxs-lookup"><span data-stu-id="36c8b-167">Row code</span></span> | <span data-ttu-id="36c8b-168">ยอดเงินโดยไม่มีการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="36c8b-168">Amounts without rounding</span></span> | <span data-ttu-id="36c8b-169">ยอดเงินที่มีการปัดเศษเป็นหลักพันทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="36c8b-169">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="36c8b-170">100</span><span class="sxs-lookup"><span data-stu-id="36c8b-170">100</span></span>      | <span data-ttu-id="36c8b-171">3,600</span><span class="sxs-lookup"><span data-stu-id="36c8b-171">3,600</span></span>                    | <span data-ttu-id="36c8b-172">4 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="36c8b-172">4</span></span>                                       |
| <span data-ttu-id="36c8b-173">200</span><span class="sxs-lookup"><span data-stu-id="36c8b-173">200</span></span>      | <span data-ttu-id="36c8b-174">3,700</span><span class="sxs-lookup"><span data-stu-id="36c8b-174">3,700</span></span>                    | <span data-ttu-id="36c8b-175">4 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="36c8b-175">4</span></span>                                       |
| <span data-ttu-id="36c8b-176">ยอดรวม</span><span class="sxs-lookup"><span data-stu-id="36c8b-176">Total</span></span>    | <span data-ttu-id="36c8b-177">7,300</span><span class="sxs-lookup"><span data-stu-id="36c8b-177">7,300</span></span>                    | <span data-ttu-id="36c8b-178">8</span><span class="sxs-lookup"><span data-stu-id="36c8b-178">8</span></span>                                       |

<span data-ttu-id="36c8b-179">หากต้องการปรับปรุงการปัดเศษในงบดุล ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="36c8b-179">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="36c8b-180">ในโปรแกรมออกแบบรายงาน คลิก **คำนิยามแถว** แล้วจึงเปิดคำนิยามแถวเพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="36c8b-180">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="36c8b-181">บนเมนู **แก้ไข** คลิก **ยอดปรับปรุงรายการที่ปัดเศษ**</span><span class="sxs-lookup"><span data-stu-id="36c8b-181">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="36c8b-182">ในกล่องโต้ตอบ **การปรับปรุงการปัดเศษ** ป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="36c8b-182">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="36c8b-183">**แถวการปรับปรุงการปัดเศษ** – รหัสแถวสำหรับแถวที่ควรถูกปรับปรุงเพื่อปรับดุลแก่งบดุล</span><span class="sxs-lookup"><span data-stu-id="36c8b-183">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="36c8b-184">**แถวสินทรัพย์รวม** – รหัสแถวสำหรับแถวในงบดุลที่ประกอบด้วยสินทรัพย์รวม</span><span class="sxs-lookup"><span data-stu-id="36c8b-184">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="36c8b-185">**แถวหนี้สินและส่วนของผู้ถือหุ้นรวม** – รหัสแถวสำหรับแถวในงบดุลที่ประกอบด้วยหนี้สินและส่วนของผู้ถือหุ้นรวม</span><span class="sxs-lookup"><span data-stu-id="36c8b-185">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="36c8b-186">**ขีดจำกัดยอดเงินการปรับปรุง** – จำนวนเต็มบวกที่ระบุขีดจำกัดในการปรับปรุงโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="36c8b-186">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="36c8b-187">ยอดเงินนี้จะถูกเปรียบเทียบกับค่าจำนวนเต็มของค่าเบี่ยงเบนจากการปัดเศษที่แท้จริง</span><span class="sxs-lookup"><span data-stu-id="36c8b-187">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="36c8b-188">รหัสแถวเหล่านี้ต้องเชื่อมโยงกับข้อมูลการเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="36c8b-188">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="36c8b-189">หรืออีกนัยหนึ่งคือ แถวต้องมีค่ามิติในเซลล์ **ลิงก์ไปยังมิติทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="36c8b-189">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="36c8b-190">. **อย่า** อ้างอิงคำอธิบาย (**DESC**), คำนวณ (**CALC**), หรือรวมแถว (**TOT**)</span><span class="sxs-lookup"><span data-stu-id="36c8b-190">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="36c8b-191">ขณะนี้ยอดเงินในงบดุลของคุณจะสมดุลอย่างสม่ำเสมอเมื่อการปัดเศษเปิดใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="36c8b-191">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="36c8b-192">ขีดจำกัดการปรับปรุงจะถูกปรับใช้ตามตัวเลือก **ความแม่นยำในการปัดเศษ** ที่ระบุสำหรับข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="36c8b-192">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="36c8b-193">ตัวอย่างเช่น ถ้าคุณปัดเศษรายงานของคุณเป็นหน่วยพัน และป้อน **2** ในฟิลด์ **ขีดจำกัดยอดเงินการปรับปรุง** คุณจะได้รับข้อความแจ้งเตือนเมื่อค่าในฟิลด์ **แถวการปรับปรุงการปัดเศษ** เพิ่มหรือลดมากกว่า $2000</span><span class="sxs-lookup"><span data-stu-id="36c8b-193">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="36c8b-194">จัดรูปแบบข้อความแถวและคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="36c8b-194">Format row and column text</span></span>
<span data-ttu-id="36c8b-195">คุณสามารถเลือกกำหนดรูปลักษณ์ของรายงานของคุณ โดยการเปลี่ยนแบบอักษร และการจัดรูปแบบข้อความ</span><span class="sxs-lookup"><span data-stu-id="36c8b-195">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="36c8b-196">ส่วนต่อไปนี้จะอธิบายวิธีการจัดรูปแบบลักษณะของแถวและคอลัมน์ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="36c8b-196">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="36c8b-197">จัดการลักษณะตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="36c8b-197">Manage font styles</span></span>

<span data-ttu-id="36c8b-198">คุณสามารถสร้างและปรับเปลี่ยนลักษณะแบบอักษรสำหรับรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="36c8b-198">You can create and modify font styles for your report.</span></span> <span data-ttu-id="36c8b-199">จากนั้นคุณสามารถใช้ลักษณะเหล่านั้นกับเอกสาร หรือกับแถวหรือคอลัมน์ที่เฉพาะเจาะจงบนรายงาน</span><span class="sxs-lookup"><span data-stu-id="36c8b-199">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="36c8b-200"><strong>สร้างลักษณะตัวอักษร</strong></span><span class="sxs-lookup"><span data-stu-id="36c8b-200"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="36c8b-201">ในโปรแกรมออกแบบรายงาน บนเมนู <strong>รูปแบบ </strong>คลิก <strong>ลักษณะและการจัดรูปแบบ</strong></span><span class="sxs-lookup"><span data-stu-id="36c8b-201">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="36c8b-202">ในกล่องโต้ตอบ <strong>ลักษณะและการจัดรูปแบบ</strong> คลิก <strong>สร้าง</strong>แล้วจากนั้นจึงป้อนชื่อเฉพาะสำหรับลักษณะใหม่</span><span class="sxs-lookup"><span data-stu-id="36c8b-202">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="36c8b-203">ทำการเลือกตัวอักษรของคุณ แล้วจึงคลิก <strong>ตกลง</strong></span><span class="sxs-lookup"><span data-stu-id="36c8b-203">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="36c8b-204"><strong>แก้ไขลักษณะแบบอักษร</strong></span><span class="sxs-lookup"><span data-stu-id="36c8b-204"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="36c8b-205">ในโปรแกรมออกแบบรายงาน บนเมนู <strong>รูปแบบ </strong>คลิก <strong>ลักษณะและการจัดรูปแบบ</strong></span><span class="sxs-lookup"><span data-stu-id="36c8b-205">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="36c8b-206">ในกล่องโต้ตอบ <strong>ลักษณะและการจัดรูปแบบ</strong> เลือกลักษณะเพื่อแก้ไข แล้วจึงคลิก <strong>ปรับเปลี่ยน</strong></span><span class="sxs-lookup"><span data-stu-id="36c8b-206">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="36c8b-207">ทำการเลือกตัวอักษรของคุณ แล้วจึงคลิก <strong>ตกลง</strong></span><span class="sxs-lookup"><span data-stu-id="36c8b-207">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="36c8b-208"><strong>ใช้ลักษณะตัวอักษร</strong></span><span class="sxs-lookup"><span data-stu-id="36c8b-208"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="36c8b-209">ในผู้ออกแบบรายงาน ในคำนิยามหรือคำนิยามคอลัมน์ หรือในส่วนหัวและส่วนท้าย เลือกตั้งแต่หนึ่งเซลล์แถวขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="36c8b-209">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="36c8b-210">ในรายการบนแถบเครื่องมือ <strong>ลักษณะ</strong> เลือกลักษณะตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="36c8b-210">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="36c8b-211">จัดรูปแบบข้อความแถว</span><span class="sxs-lookup"><span data-stu-id="36c8b-211">Format row text</span></span>

<span data-ttu-id="36c8b-212">การจัดรูปแบบที่ระบุไว้ในแถวคำนิยามแทนการจัดรูปแบบที่ระบุในคำนิยามคอลัมน์และข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="36c8b-212">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="36c8b-213">คุณสามารถปรับเปลี่ยนรูปแบบข้อความได้โดยใช้ตัวควบคุมต่างๆ บนแถบเครื่องมือการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="36c8b-213">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="36c8b-214">ตัวควบคุมเหล่านี้เป็นตัวควบคุม Microsoft Windows มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="36c8b-214">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="36c8b-215">ใน Report Designer เปิดคำนิยามแถวเพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="36c8b-215">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="36c8b-216">เลือกเซลล์เพื่อจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="36c8b-216">Select the cells to format.</span></span> <span data-ttu-id="36c8b-217">หากต้องการเลือกหลายๆ เซลล์ ให้กดปุ่ม Ctrl ค้างไว้ในขณะที่คุณเลือกเซลล์</span><span class="sxs-lookup"><span data-stu-id="36c8b-217">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="36c8b-218">คลิกปุ่มแถบเครื่องมือของรูปแบบที่ต้องการเพื่อนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="36c8b-218">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="36c8b-219">ตัวอย่างเช่น ในแถวที่ย่อหน้า เลือกแถว แล้วจึงคลิก **เพิ่มระยะย่อหน้า** ![เพิ่มระยะย่อหน้า](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "เพิ่มระยะย่อหน้า") ในแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="36c8b-219">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="36c8b-220">ปรับปรุงคอลัมน์ในขณะที่คุณออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="36c8b-220">Adjust columns while you design reports</span></span>

<span data-ttu-id="36c8b-221">หากต้องการให้การดูคอลัมน์ที่คุณกำลังทำงานอยู่ในคำนิยามแถวง่ายขึ้น คุณสามารถปรับปรุงความกว้างของคอลัมน์และยังสามารถซ่อน (ย่อเล็กสุด) หรือแสดงคอลัมน์ในบานหน้าต่างมุมมองได้</span><span class="sxs-lookup"><span data-stu-id="36c8b-221">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="36c8b-222">การปรับเปลี่ยนที่คุณทำมีผลกระทบต่อลักษณะของคอลัมน์ที่ปรากฏบนหน้าจอเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="36c8b-222">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="36c8b-223">จะไม่มีผลกับการจัดรูปแบบคอลัมน์ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="36c8b-223">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="36c8b-224">เปลี่ยนความกว้างของคอลัมน์ในบานหน้าต่างมุมมอง</span><span class="sxs-lookup"><span data-stu-id="36c8b-224">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="36c8b-225">ในโปรแกรมออกแบบรายงาน เปิดคำนิยามแถวเพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="36c8b-225">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="36c8b-226">ในเมนู **รูปแบบ** เลือก **ความกว้างของคอลัมน์**</span><span class="sxs-lookup"><span data-stu-id="36c8b-226">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="36c8b-227">ในกล่องโต้ตอบ **ความกว้างของคอลัมน์** ป้อนค่าและจากนั้น คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="36c8b-227">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="36c8b-228">หรือกคุณสามารถลากขอบขวาของเซลล์ส่วนหัวของคอลัมน์เพื่อเปลี่ยนความกว้างของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="36c8b-228">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="36c8b-229">ซ่อนคอลัมน์ในบานหน้าต่างมุมมอง</span><span class="sxs-lookup"><span data-stu-id="36c8b-229">Hide columns in the view pane</span></span>

1. <span data-ttu-id="36c8b-230">ในโปรแกรมออกแบบรายงาน เปิดคำนิยามแถวเพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="36c8b-230">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="36c8b-231">เลือกคอลัมน์อย่างน้อยหนึ่งคอลัมน์เพื่อย่อขนาด</span><span class="sxs-lookup"><span data-stu-id="36c8b-231">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="36c8b-232">คลิกขวา แล้วจึงคลิก **ซ่อน**</span><span class="sxs-lookup"><span data-stu-id="36c8b-232">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="36c8b-233">แสดงคอลัมน์ที่ซ่อนอยู่ทั้งหมดในบานหน้าต่างมุมมอง</span><span class="sxs-lookup"><span data-stu-id="36c8b-233">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="36c8b-234">ในโปรแกรมออกแบบรายงาน เปิดคำนิยามแถวเพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="36c8b-234">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="36c8b-235">คลิกขวาที่คอลัมน์ที่ถูกย่อเพื่อให้แสดงผล แล้วจึงคลิก **ยกเลิกซ่อน**</span><span class="sxs-lookup"><span data-stu-id="36c8b-235">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="36c8b-236">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="36c8b-236">Additional resources</span></span>

[<span data-ttu-id="36c8b-237">การรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="36c8b-237">Financial reporting</span></span>](financial-reporting-intro.md)
