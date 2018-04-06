---
title: "เท็มเพลตการวางแผนงบประมาณสำหรับ Excel"
description: "หัวข้อนี้อธิบายวิธีการสร้างเท็มเพลต Microsoft Excel ที่สามารถใช้ได้กับแผนงบประมาณ"
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 156688b705337331e083ebc19fded57b028acb67
ms.contentlocale: th-th
ms.lasthandoff: 03/26/2018

---

# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="a068e-103">เท็มเพลตการวางแผนงบประมาณสำหรับ Excel</span><span class="sxs-lookup"><span data-stu-id="a068e-103">Budget planning templates for Excel</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a068e-104">หัวข้อนี้อธิบายวิธีการสร้างเท็มเพลต Microsoft Excel ที่สามารถใช้ได้กับแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="a068e-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="a068e-105">หัวข้อนี้แสดงวิธีการสร้างเท็มเพลต Excel ที่จะใช้กับแผนงบประมาณโดยใช้ชุดข้อมูลสาธิตมาตรฐานและล็อกอินของผู้ใช้ที่เป็นผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="a068e-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="a068e-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการวางแผนงบประมาณ ดู [ภาพรวมการวางแผนงบประมาณ](budget-planning-overview-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="a068e-106">For more information about budget planning, see [Budget planning overview.](budget-planning-overview-configuration.md)</span></span> <span data-ttu-id="a068e-107">นอกจากนี้คุณสามารถทำตามบทสอน [การวางแผนงบประมาณ 101](budget-plan.md) เพื่อเรียนรู้หลักการตั้งค่าคอนฟิกและการใช้โมดูลพื้นฐานได้</span><span class="sxs-lookup"><span data-stu-id="a068e-107">You can also follow the [Budget planning 101](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="a068e-108">สร้างแผ่นงานโดยใช้โครงร่างเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="a068e-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="a068e-109">สามารถดูและแก้ไขเอกสารแผนงบประมาณโดยใช้โครงร่างอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="a068e-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="a068e-110">แต่ละโครงร่างสามารถมีเท็มเพลตเอกสารแผนงบประมาณที่เกี่ยวข้องเพื่อดูและแก้ไขข้อมูลแผนงบประมาณในแผ่นงาน Excel</span><span class="sxs-lookup"><span data-stu-id="a068e-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="a068e-111">ในหัวข้อนี้ เท็มเพลตเอกสารแผนงบประมาณจะถูกสร้างขึ้นโดยใช้การตั้งค่าคอนฟิกโครงร่างที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a068e-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="a068e-112">เปิด **รายการแผนงบประมาณ** (**การจัดงบประมาณ** &gt; **แผนงบประมาณ**)</span><span class="sxs-lookup"><span data-stu-id="a068e-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="a068e-113">คลิก **สร้าง** เพื่อสร้างเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="a068e-113">Click **New** to create a new budget plan document.</span></span> 

  <span data-ttu-id="a068e-114">[![รายการแผนงบประมาณ](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="a068e-115">ใช้ตัวเลือกบรรทัด **เพิ่ม** เพื่อเพิ่มบรรทัด</span><span class="sxs-lookup"><span data-stu-id="a068e-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="a068e-116">คลิก **เค้าโครง** เพื่อดูการตั้งค่าคอนฟิกโครงร่างเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="a068e-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

  <span data-ttu-id="a068e-117">[![การเพิ่มแผนงบประมาณ](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="a068e-118">คุณสามารถตรวจทานการตั้งค่าคอนฟิกโครงร่างและปรับตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="a068e-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="a068e-119">ไปที่ **เท็มเพลต** &gt; **สร้าง** เพื่อสร้างไฟล์ Excel สำหรับโครงร่างนี้</span><span class="sxs-lookup"><span data-stu-id="a068e-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="a068e-120">หลังจากที่มีการสร้างเท็มเพลต ไปที่ **เท็มเพลต** &gt; **ดู** เพื่อเปิดและตรวจทานเท็มเพลตเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="a068e-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="a068e-121">คุณสามารถบันทึกไฟล์ Excel ไปที่ไดรฟ์ภายในเครื่องของคุณได้</span><span class="sxs-lookup"><span data-stu-id="a068e-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="a068e-122">[![บันทึกเป็น](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="a068e-123">คุณไม่สามารถแก้ไขโครงร่างเอกสารแผนงบประมาณหลังจากที่มีการเชื่อมโยงกับเท็มเพลต Excel ได้</span><span class="sxs-lookup"><span data-stu-id="a068e-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="a068e-124">เมื่อต้องการปรับเปลี่ยนโครงร่าง ลบไฟล์เท็มเพลต Excel ที่เกี่ยวข้อง และสร้างใหม่</span><span class="sxs-lookup"><span data-stu-id="a068e-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="a068e-125">ซึ่งจำเป็นต้องใช้ในการรักษาฟิลด์ในโครงร่างและแผ่นงานให้ซิงโครไนส์อยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="a068e-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="a068e-126">เท็มเพลต Excel จะประกอบด้วยองค์ประกอบทั้งหมดจากโครงร่างเอกสารแผนงบประมาณ โดยที่คอลัมน์ **พร้อมใช้งานในแผ่นงาน** ถูกตั้งค่าเป็น True</span><span class="sxs-lookup"><span data-stu-id="a068e-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="a068e-127">ไม่อนุญาตให้มีองค์ประกอบที่ซ้อนทับกันในเท็มเพลต Excel</span><span class="sxs-lookup"><span data-stu-id="a068e-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="a068e-128">ตัวอย่างเช่น ถ้าโครงร่างประกอบด้วยคอลัมน์คำขอ Q1 คำขอ Q2คำขอ Q3 และคำขอ Q4 และคอลัมน์คำขอรวมที่แสดงผลรวมของคอลัมน์รายไตรมาสทั้ง 4 เฉพาะคอลัมน์รายไตรมาสหรือคอลัมน์รวมเท่านั้นที่พร้อมใช้งานในเท็มเพลต Excel</span><span class="sxs-lookup"><span data-stu-id="a068e-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="a068e-129">ไฟล์ Excel ไม่สามารถปรับปรุงคอลัมน์ที่ซ้อนทับกันในระหว่างการปรับปรุงได้เนื่องจากข้อมูลในตารางอาจจะล้าสมัยและไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a068e-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

<span data-ttu-id="a068e-130">[![ตัวอย่าง](./media/bpt4-1024x615.png)](./media/bpt4.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-130">[![Example](./media/bpt4-1024x615.png)](./media/bpt4.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="a068e-131">เมื่อต้องการหลีกเลี่ยงปัญหาที่อาจเกิดขึ้นกับการดูและแก้ไขข้อมูลแผนงบประมาณโดยใช้ Excel ผู้ใช้เดียวกันควรเข้าสู่ระบบไปยังทั้ง Microsoft Dynamics 365 for Finance and Operations และ Add-in ของ Office สำหรับ Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="a068e-131">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 for Finance and Operations and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="a068e-132">เพิ่มหัวข้อลงในเท็มเพลตเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="a068e-132">Add a header to budget plan document template</span></span>
<span data-ttu-id="a068e-133">เมื่อต้องการเพิ่มข้อมูลหัวข้อ เลือกแถวบนสุดในไฟล์ Excel และแทรกแถวที่ว่าง</span><span class="sxs-lookup"><span data-stu-id="a068e-133">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="a068e-134">คลิก **ออกแบบ** ใน **ตัวเชื่อมต่อข้อมูล** เพื่อเพิ่มฟิลด์หัวข้อไปยังไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="a068e-134">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="a068e-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span></span> 

<span data-ttu-id="a068e-136">ในแท็บ **ออกแบบ** คลิกฟิลด์ **เพิ่ม** และจากนั้นเลือก **BudgetPlanHeader** เป็นแหล่งข้อมูลของเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="a068e-136">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="a068e-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span></span>

<span data-ttu-id="a068e-138">ชี้เคอร์เซอร์ไปยังตำแหน่งที่ต้องการในไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="a068e-138">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="a068e-139">คลิก **เพิ่มป้ายชื่อ** เพื่อเพิ่มป้ายชื่อฟิลด์ไปยังตำแหน่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a068e-139">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="a068e-140">เลือก **เพิ่มค่า** เพื่อเพิ่มฟิลด์ค่าไปยังตำแหน่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a068e-140">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="a068e-141">คลิก **เสร็จสิ้น** เพื่อปิดตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="a068e-141">Click **Done** to close the designer.</span></span>

## <a name="bpt7mediabpt7pngmediabpt7png"></a><span data-ttu-id="a068e-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="a068e-143">เพิ่มคอลัมน์ที่คำนวณแล้วไปยังตารางเท็มเพลตเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="a068e-143">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="a068e-144">ถัดไป คอลัมน์ที่คำนวณแล้วจะถูกเพิ่มไปยังเท็มเพลตเอกสารแผนงบประมาณที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a068e-144">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="a068e-145">คอลัมน์ **คำขอรวม** ซึ่งสรุปคอลัมน์คำขอ Q1: คำขอ Q4 และคอลัมน์ **การปรับปรุง** ซึ่งคำนวณคอลัมน์ **คำขอรวม** ใหม่ด้วยตัวคูณที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="a068e-145">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="a068e-146">คลิก **ออกแบบ** ใน **ตัวเชื่อมต่อข้อมูล** เพื่อเพิ่มคอลัมน์ไปยังตาราง</span><span class="sxs-lookup"><span data-stu-id="a068e-146">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="a068e-147">คลิก **แก้ไข** ที่อยู่ถัดจากแหล่งข้อมูล **BudgetPlanWorksheet** เพื่อเริ่มเพิ่มคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="a068e-147">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="a068e-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="a068e-149">กลุ่มฟิลด์ที่เลือกแสดงในคอลัมน์ที่มีอยู่ในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="a068e-149">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="a068e-150">คลิก **สูตร** เพื่อเพิ่มคอลัมน์ใหม่</span><span class="sxs-lookup"><span data-stu-id="a068e-150">Click **Formula** to add a new column.</span></span> <span data-ttu-id="a068e-151">กำหนดชื่อให้กับคอลัมน์ใหม่ และวางสูตรลงในฟิลด์ **สูตร**</span><span class="sxs-lookup"><span data-stu-id="a068e-151">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="a068e-152">คลิก **อัพเดต** เพื่อแทรกคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="a068e-152">Click **Update** to insert the column.</span></span>

<span data-ttu-id="a068e-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="a068e-154">เมื่อต้องการกำหนดสูตร ให้สร้างสูตรในแผ่นตารางทำการ และจากนั้นคัดลอกไปยังหน้าต่าง **ออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="a068e-154">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="a068e-155">โดยทั่วไป ตารางขอบเขต Finance and Operations จะถูกตั้งชื่อเป็น "AXTable1"</span><span class="sxs-lookup"><span data-stu-id="a068e-155">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="a068e-156">ตัวอย่างเช่น เมื่อต้องการสรุปคอลัมน์คำขอ Q1 : คำขอ Q4 ในแผ่นตารางทำการ สูตร = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\]</span><span class="sxs-lookup"><span data-stu-id="a068e-156">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="a068e-157">ทำซ้ำขั้นตอนเหล่านี้เพื่อแทรกคอลัมน์ **การปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="a068e-157">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="a068e-158">ใช้สูตร = AxTable1\[Total request\]\*$I$1 สำหรับคอลัมน์นี้</span><span class="sxs-lookup"><span data-stu-id="a068e-158">Use formula = AxTable1\[Total request\]\*$I$1 for this column.</span></span> <span data-ttu-id="a068e-159">ซึ่งจะใช้ค่าในเซลล์ I1 และคูณค่าในคอลัมน์ **คำขอรวม** เพื่อคำนวณยอดการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="a068e-159">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="a068e-160">บันทึกแล้วปืดไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="a068e-160">Save and close the Excel file.</span></span> <span data-ttu-id="a068e-161">กลับไปยัง Finance and Operations และใน **โครงร่าง** คลิก **เท็มเพลต &gt; อัปโหลด** เพื่ออัปโหลดเท็มเพลต Excel ที่บันทึกที่จะใช้สำหรับแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="a068e-161">Return to Finance and Operations, and in **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="a068e-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="a068e-163">ปิดแถบเลื่อน **โครงร่าง**</span><span class="sxs-lookup"><span data-stu-id="a068e-163">Close the **Layouts** slider.</span></span> <span data-ttu-id="a068e-164">ในเอกสาร **แผนงบประมาณ** คลิก **แผ่นงาน** เพื่อดูและแก้ไขเอกสารใน Excel</span><span class="sxs-lookup"><span data-stu-id="a068e-164">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="a068e-165">หมายเหตุว่าเท็มเพลต Excel ที่ปรับปรุงแล้วจะถูกใช้เพื่อสร้างแผ่นงานแผนงบประมาณนี้ และคอลัมน์ที่คำนวณแล้วจะถูกอัพเดตโดยใช้สูตรที่กำหนดไว้ในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="a068e-165">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="a068e-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="a068e-167">คำแนะนำและเคล็ดลับสำหรับการสร้างเท็มเพลตแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="a068e-167">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="a068e-168">ฉันสามารถเพิ่มและใช้แหล่งข้อมูลเพิ่มเติมกับเท็มเพลตแผนงบประมาณได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a068e-168">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="a068e-169">ได้ คุณสามารถใช้เมนู **ออกแบบ** เพื่อเพิ่มเอนทิตีเพิ่มเติมไปยังแผ่นเดียวกันหรือแผ่นอื่นในเท็มเพลต Excel ได้</span><span class="sxs-lookup"><span data-stu-id="a068e-169">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="a068e-170">ตัวอย่างเช่น คุณสามารถเพิ่มแหล่งข้อมูล **BudgetPlanProposedProject** เพื่อสร้างและรักษารายการของโครงการที่นำเสนอในเวลาเดียวกันเมื่อทำงานกับข้อมูลแผนงบประมาณใน Excel</span><span class="sxs-lookup"><span data-stu-id="a068e-170">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="a068e-171">หมายเหตุว่าการรวมแหล่งข้อมูลปริมาณสูงอาจส่งผลกระทบต่อประสิทธิภาพการทำงานของสมุดงาน Excel</span><span class="sxs-lookup"><span data-stu-id="a068e-171">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="a068e-172">คุณสามารถใช้การตัวเลือก **ตัวกรอง** ใน **ตัวเชื่อมต่อข้อมูล** เพื่อเพิ่มตัวกรองที่ต้องการไปยังแหล่งข้อมูลเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="a068e-172">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="a068e-173">ฉันสามารถซ่อนตัวเลือกออกแบบในตัวเชื่อมต่อข้อมูลสำหรับผู้ใช้อื่นได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a068e-173">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="a068e-174">ได้ เปิดตัวเลือก **ตัวเชื่อมต่อข้อมูล** เพื่อซ่อนตัวเลือก **ออกแบบ** จากผู้ใช้รายอื่น</span><span class="sxs-lookup"><span data-stu-id="a068e-174">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="a068e-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="a068e-176">ขยาย **ตัวเลือกตัวเชื่อมต่อข้อมูล** และล้างกล่องกาเครื่องหมาย **เปิดใช้งานการออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="a068e-176">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="a068e-177">ซึ่งจะซ่อนตัวเลือก **ออกแบบ** จาก **ตัวเชื่อมต่อข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="a068e-177">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="a068e-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="a068e-179">ฉันสามารถป้องกันผู้ใช้ไม่ให้ปิดตัวเชื่อมต่อข้อมูลขณะทำงานกับข้อมูลโดยบังเอิญได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a068e-179">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="a068e-180">เราขอแนะนำให้ล็อคเท็มเพลตเพื่อป้องกันไม่ให้ผู้ใช้ปิด</span><span class="sxs-lookup"><span data-stu-id="a068e-180">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="a068e-181">เมื่อต้องการปลดล็อค คลิก **ตัวเชื่อมต่อข้อมูล** ที่มุมขวาด้านบน ลูกศรจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="a068e-181">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="a068e-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="a068e-183">คลิกลูกศรเพื่อดูเมนูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a068e-183">Click the arrow for an additional menu.</span></span> <span data-ttu-id="a068e-184">เลือก **ล็อค**</span><span class="sxs-lookup"><span data-stu-id="a068e-184">Select **Lock**.</span></span>

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a><span data-ttu-id="a068e-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="a068e-186">ฉันสามารถใช้คุณลักษณะอื่นๆ ของ Excel เช่น การจัดรูปแบบเซลล์ สี การจัดรูปแบบตามเงื่อนไข และแผนภูมิกับเท็มเพลตแผนงบประมาณของฉันได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a068e-186">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="a068e-187">ได้ ความสามารถของ Excel มาตรฐานส่วนใหญ่จะทำงานในเท็มเพลตแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="a068e-187">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="a068e-188">เราแนะนำให้ใช้การกำหนดรหัสสีสำหรับผู้ใช้เพื่อแยกความแตกต่างระหว่างคอลัมน์แบบอ่านอย่างเดียวและคอลัมน์ที่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="a068e-188">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="a068e-189">สามารถใช้การจัดรูปแบบตามเงื่อนไขเพื่อเน้นพื้นที่ที่มีปัญหาของงบประมาณได้</span><span class="sxs-lookup"><span data-stu-id="a068e-189">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="a068e-190">สามารถแสดงผลรวมคอลัมน์ได้อย่างง่ายดายโดยใช้สูตร Excel มาตรฐานที่อยู่เหนือตาราง</span><span class="sxs-lookup"><span data-stu-id="a068e-190">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="a068e-191">นอกจากนี้คุณยังสามารถสร้างและใช้ไพว็อทเทเบิลและแผนภูมิสำหรับการจัดกลุ่มและการแสดงภาพข้อมูลเพิ่มเติมของข้อมูลงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="a068e-191">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="a068e-192">บนแท็บ **ข้อมูล** ในกลุ่ม **การเชื่อมต่อ** คลิก **รีเฟรชทั้งหมด** แล้วคลิก **คุณสมบัติการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="a068e-192">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="a068e-193">คลิกแท็บ **การใช้** ภายใต้ **รีเฟรช** เลือกกล่องกาเครื่องหมาย **รีเฟรชข้อมูลเมื่อเปิดไฟล์**</span><span class="sxs-lookup"><span data-stu-id="a068e-193">Click the **Usage** tab. Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 

<span data-ttu-id="a068e-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span><span class="sxs-lookup"><span data-stu-id="a068e-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span></span>




