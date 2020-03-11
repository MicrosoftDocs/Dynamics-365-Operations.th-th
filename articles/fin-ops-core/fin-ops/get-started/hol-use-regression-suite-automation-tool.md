---
title: ใช้บทช่วยสอน Regression Suite Automation Tool
description: หัวข้อนี้จะแสดงวิธีการใช้ Regression Suite Automation Tool (RSAT) ซึ่งจะอธิบายถึงคุณลักษณะต่างๆ และแสดงตัวอย่างที่ใช้การเขียนสคริปต์ขั้นสูง
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070831"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="203b6-104">ใช้บทช่วยสอน Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="203b6-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="203b6-105">ใช้เครื่องมือเบราว์เซอร์อินเทอร์เน็ตของคุณเพื่อดาวน์โหลดและบันทึกหน้านี้ในรูปแบบ pdf</span><span class="sxs-lookup"><span data-stu-id="203b6-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="203b6-106">บทช่วยสอนนี้จะแนะนำคุณลักษณะขั้นสูงบางอย่างของ Regression Suite Automation Tool (RSAT) รวมถึงการกำหนดการสาธิต และอธิบายถึงกลยุทธ์และประเด็นการเรียนรู้ที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="203b6-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="203b6-107">คุณลักษณะของ RSAT/ตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="203b6-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="203b6-108">ตรวจสอบความถูกต้องของค่าฟิลด์</span><span class="sxs-lookup"><span data-stu-id="203b6-108">Validate a field value</span></span>

<span data-ttu-id="203b6-109">สำหรับข้อมูลเกี่ยวกับคุณลักษณะนี้ ดู [สร้างการบันทึกงานใหม่ที่มีฟังก์ชันตรวจสอบความถูกต้อง](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function)</span><span class="sxs-lookup"><span data-stu-id="203b6-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="203b6-110">ตัวแปรที่บันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="203b6-110">Saved variable</span></span>

<span data-ttu-id="203b6-111">สำหรับข้อมูลเกี่ยวกับคุณลักษณะนี้ ดู [ปรับเปลี่ยนการบันทึกงานที่มีอยู่เพื่อสร้างตัวแปรที่บันทึกไว้](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable)</span><span class="sxs-lookup"><span data-stu-id="203b6-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="203b6-112">กรณีการทดสอบที่สืบทอดมา</span><span class="sxs-lookup"><span data-stu-id="203b6-112">Derived test case</span></span>

1. <span data-ttu-id="203b6-113">เปิด Regression Suite Automation Tool (RSAT) และเลือกกรณีการทดสอบทั้งสองกรณีที่คุณสร้างขึ้นใน [ตั้งค่าและติดตั้งบทสอนเกี่ยวกับ Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md)</span><span class="sxs-lookup"><span data-stu-id="203b6-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="203b6-114">เลือก **สร้าง \> สร้างกรณีการทดสอบที่สืบทอดมา**</span><span class="sxs-lookup"><span data-stu-id="203b6-114">Select **New \> Create derived test case**.</span></span>

    ![สร้างคำสั่งของกรณีทดสอบที่สืบทอดมาบนเมนูใหม่](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="203b6-116">คุณได้รับข้อความที่แจ้งว่าจะมีการสร้างกรณีการทดสอบที่สืบทอดมาสำหรับกรณีการทดสอบที่เลือกแต่ละกรณีในชุดการทดสอบปัจจุบัน และกรณีการทดสอบที่สืบทอดมาแต่ละกรณีจะมีสำเนาของไฟล์พารามิเตอร์ Excel ของตนเอง</span><span class="sxs-lookup"><span data-stu-id="203b6-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="203b6-117">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="203b6-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="203b6-118">เมื่อคุณรันกรณีการทดสอบที่สืบทอดมา จะใช้การบันทึกงานของกรณีการทดสอบหลักและสำเนาของไฟล์พารามิเตอร์ Excel ของตนเอง</span><span class="sxs-lookup"><span data-stu-id="203b6-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="203b6-119">ด้วยวิธีนี้ คุณสามารถรันการทดสอบเดียวกันด้วยพารามิเตอร์ต่างๆ ได้ โดยไม่ต้องมีการรักษาการบันทึกงานมากกว่าหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="203b6-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="203b6-120">กรณีการทดสอบที่สืบทอดมาไม่จำเป็นต้องเป็นส่วนหนึ่งของชุดการทดสอบเดียวกันกับกรณีการทดสอบหลัก</span><span class="sxs-lookup"><span data-stu-id="203b6-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![กล่องข้อความ](./media/use_rsa_tool_02.png)

    <span data-ttu-id="203b6-122">มีการสร้างกรณีการทดสอบที่สืบทอดมาเพิ่มเติมสองกรณี และกล่องกาเครื่องหมาย **ได้รับมาหรือไม่?** จะถูกเลือกสำหรับกรณีเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="203b6-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![มีการสร้างกรณีการทดสอบที่สืบทอดมา](./media/use_rsa_tool_03.png)

    <span data-ttu-id="203b6-124">มีการสร้างกรณีการทดสอบที่สืบทอดมาโดยอัตโนมัติใน Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="203b6-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="203b6-125">นี่เป็นรายการรองของกรณีการทดสอบ **สร้างผลิตภัณฑ์ใหม่** และมีการติดแท็กด้วยคำสำคัญพิเศษ: **RSAT: DerivedTestSteps**</span><span class="sxs-lookup"><span data-stu-id="203b6-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="203b6-126">นอกจากนี้ กรณีการทดสอบเหล่านี้จะถูกเพิ่มเข้าไปในแผนการทดสอบโดยอัตโนมัติใน Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="203b6-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![คำสำคัญ RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="203b6-128">ถ้า เนื่องจากสาเหตุใดๆ กรณีการทดสอบที่สืบทอดมาที่ถูกสร้างนั้นไม่ได้อยู่ในลำดับที่ถูกต้อง ไปที่ Azure DevOps และจัดลำดับกรณีการทดสอบใหม่ในชุดการทดสอบ เพื่อให้ RSAT สามารถรันได้ในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="203b6-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="203b6-129">เลือกกรณีการทดสอบที่สืบทอดมา แล้วจากนั้น เลือก **แก้ไข** เพื่อเปิดไฟล์พารามิเตอร์ Excel ที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="203b6-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="203b6-130">แก้ไขไฟล์พารามิเตอร์ของ Excel เหล่านี้ในลักษณะเดียวกับที่คุณแก้ไขไฟล์หลัก</span><span class="sxs-lookup"><span data-stu-id="203b6-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="203b6-131">กล่าวอีกอย่างหนึ่งคือ ตรวจสอบให้แน่ใจว่ามีการตั้งค่ารหัสผลิตภัณฑ์ เพื่อให้มีการสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="203b6-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="203b6-132">นอกจากนี้ ตรวจสอบให้แน่ใจว่าตัวแปรที่บันทึกไว้ถูกคัดลอกไปยังฟิลด์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="203b6-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="203b6-133">บนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel ให้ปรับปรุงค่าของฟิลด์ **บริษัท** เป็น **USSI** เพื่อให้กรณีการทดสอบที่สืบทอดมาจะถูกรันเทียบกับนิติบุคคลอื่นที่ไม่ใช่กรณีการทดสอบหลัก</span><span class="sxs-lookup"><span data-stu-id="203b6-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="203b6-134">เมื่อต้องการรันกรณีการทดสอบเทียบกับผู้ใช้ที่ระบุ (หรือบทบาทที่สัมพันธ์กับผู้ใช้ที่ระบุ) คุณสามารถปรับปรุงค่าของฟิลด์ **ผู้ใช้การทดสอบ** ได้</span><span class="sxs-lookup"><span data-stu-id="203b6-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="203b6-135">เลือก **รัน** และตรวจสอบความถูกต้องว่าผลิตภัณฑ์ถูกสร้างขึ้นในทั้งนิติบุคคล USMF และนิติบุคคล USSI</span><span class="sxs-lookup"><span data-stu-id="203b6-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="203b6-136">ตรวจสอบความถูกต้องของการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="203b6-136">Validate notifications</span></span>

<span data-ttu-id="203b6-137">สามารถใช้คุณลักษณะนี้เพื่อตรวจสอบว่าเกิดการดำเนินการขึ้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="203b6-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="203b6-138">ตัวอย่างเช่น เมื่อใบสั่งผลิตถูกสร้าง ประมาณการ จนถึงเริ่มต้นการผลิต แอปจะแสดงข้อความ "การผลิต – เริ่มต้น" เพื่อแจ้งให้คุณทราบว่าใบสั่งผลิตเริ่มดำเนินการแล้ว</span><span class="sxs-lookup"><span data-stu-id="203b6-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![การผลิต – เริ่มการแจ้งเตือน](./media/use_rsa_tool_05.png)

<span data-ttu-id="203b6-140">คุณสามารถตรวจสอบความถูกต้องของข้อความนี้ผ่าน RSAT โดยการป้อนข้อความในแท็บ **MessageValidation** ของไฟล์พารามิเตอร์ Excel สำหรับการบันทึกที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="203b6-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![แท็บการตรวจสอบความถูกต้องของข้อความ](./media/use_rsa_tool_06.png)

<span data-ttu-id="203b6-142">หลังจากรันกรณีการทดสอบ ข้อความในไฟล์พารามิเตอร์ของ Excel จะถูกเปรียบเทียบกับข้อความที่แสดง</span><span class="sxs-lookup"><span data-stu-id="203b6-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="203b6-143">ถ้าข้อความไม่ตรงกัน กรณีการทดสอบจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="203b6-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="203b6-144">คุณสามารถป้อนข้อความมากกว่าหนึ่งข้อความได้บนแท็บ **MessageValidation** ในไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="203b6-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="203b6-145">นอกจากนี้ ข้อความอาจเป็นข้อผิดพลาดหรือข้อความเตือน แทนที่จะเป็นข้อความที่ให้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="203b6-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="203b6-146">ตรวจสอบความถูกต้องของค่าโดยใช้ตัวดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="203b6-146">Validate values by using operators</span></span>

<span data-ttu-id="203b6-147">ในรุ่นก่อนหน้าของ RSAT คุณสามารถตรวจสอบความถูกต้องของค่าได้ เฉพาะเมื่อค่าการควบคุมเท่ากับค่าที่คาดไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="203b6-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="203b6-148">คุณลักษณะใหม่ช่วยให้คุณสามารถตรวจสอบตัวแปรที่ไม่เท่ากับ น้อยกว่า หรือมากกว่า ค่าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="203b6-149">เมื่อต้องการใช้คุณลักษณะนี้ เปิดไฟล์ **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ภายใต้โฟลเดอร์การติดตั้ง RSAT (ตัวอย่างเช่น **C:\\Program Files (x86)\\Regression Suite Automation Tool**) และเปลี่ยนค่าในองค์ประกอบต่อไปนี้จาก **เท็จ** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="203b6-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="203b6-150">ในไฟล์พารามิเตอร์ Excel ฟิลด์ **ผู้ปฏิบัติงาน** ใหม่ จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="203b6-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="203b6-151">ถ้าคุณได้ใช้เวอร์ชันที่เก่ากว่าของ RSAT คุณต้องสร้างไฟล์พารามิเตอร์ Excel ใหม่</span><span class="sxs-lookup"><span data-stu-id="203b6-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![ฟิลด์ตัวดำเนินงาน](./media/use_rsa_tool_07.png)

<span data-ttu-id="203b6-153">ตัวอย่างต่อไปนี้แสดงวิธีการที่คุณสามารถใช้คุณลักษณะนี้เพื่อตรวจสอบว่าปริมาณคงคลังคงเหลือมากกว่า 0 (ศูนย์) หรือไม่</span><span class="sxs-lookup"><span data-stu-id="203b6-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="203b6-154">ในข้อมูลสาธิตในบริษัท **USMF** ให้สร้างการบันทึกงานที่มีขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="203b6-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="203b6-155">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="203b6-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="203b6-156">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="203b6-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="203b6-157">ตัวอย่างเช่น ตัวกรองในค่าของ **1000** สำหรับฟิลด์ **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="203b6-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="203b6-158">เลือก **ปริมาณสินค้าคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="203b6-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="203b6-159">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="203b6-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="203b6-160">ตัวอย่างเช่น ตัวกรองในค่าของ **1** สำหรับฟิลด์ **ไซต์**</span><span class="sxs-lookup"><span data-stu-id="203b6-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="203b6-161">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="203b6-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="203b6-162">ตรวจสอบความถูกต้องว่าค่าของฟิลด์ **ทั้งหมดที่พร้อมใช้งาน** คือ **411.0000000000000000**</span><span class="sxs-lookup"><span data-stu-id="203b6-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="203b6-163">บันทึกการบันทึกงานไปยังไลบรารี BPM และซิงค์กับ Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="203b6-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="203b6-164">เพิ่มกรณีการทดสอบไปยังแผนการทดสอบ และโหลดกรณีการทดสอบลงใน RSAT</span><span class="sxs-lookup"><span data-stu-id="203b6-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="203b6-165">เปิดไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="203b6-165">Open the Excel parameter file.</span></span> <span data-ttu-id="203b6-166">บนแท็บ **InventOnhandItem** คุณจะเห็นส่วน **ตรวจสอบความถูกต้องของ InventOnhandItem** ที่มีฟิลด์ **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="203b6-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![ฟิลด์ตัวดำเนินงาน](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="203b6-168">เมื่อต้องการตรวจสอบว่าปริมาณคงคลังคงเหลือจะมากกว่า 0 เสมอหรือไม่ ให้เปลี่ยนค่าของฟิลด์ **ค่า** จาก **411** เป็น **0** และค่าของฟิลด์ **ผู้ปฏิบัติงาน** จากเครื่องหมายเท่ากับ (**=**) เป็นเครื่องหมายมากกว่า (**\>**)</span><span class="sxs-lookup"><span data-stu-id="203b6-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![ค่าของฟิลด์มูลค่าและผู้ปฏิบัติงานเปลี่ยนแปลง](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="203b6-170">บันทึกและปิดไฟล์พารามิเตอร์ Excel</span><span class="sxs-lookup"><span data-stu-id="203b6-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="203b6-171">เลือก **อัปโหลด** เพื่อบันทึกการเปลี่ยนแปลงที่คุณทำไว้กับไฟล์พารามิเตอร์ Excel เป็น Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="203b6-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="203b6-172">ขณะนี้ ถ้าค่าของฟิลด์ **ทั้งหมดพร้อมใช้งาน** สำหรับสินค้าที่ระบุในสินค้าคงคลังมีมากกว่า 0 (ศูนย์) การทดสอบจะผ่าน โดยไม่คำนึงถึงมูลค่าของปริมาณคงคลังคงเหลือจริง</span><span class="sxs-lookup"><span data-stu-id="203b6-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="203b6-173">ล็อกตัวสร้าง</span><span class="sxs-lookup"><span data-stu-id="203b6-173">Generator logs</span></span>

<span data-ttu-id="203b6-174">คุณลักษณะนี้สร้างโฟลเดอร์ที่มีล็อกของกรณีการทดสอบที่มีการรัน</span><span class="sxs-lookup"><span data-stu-id="203b6-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="203b6-175">เมื่อต้องการใช้คุณลักษณะนี้ เปิดไฟล์ **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ภายใต้โฟลเดอร์การติดตั้ง RSAT (ตัวอย่างเช่น **C:\\Program Files (x86)\\Regression Suite Automation Tool**) และเปลี่ยนค่าในองค์ประกอบต่อไปนี้จาก **เท็จ** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="203b6-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="203b6-176">หลังจากที่มีการรันกรณีการทดสอบแล้ว คุณสามารถค้นหาไฟล์ล็อกภายใต้ **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**</span><span class="sxs-lookup"><span data-stu-id="203b6-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![โฟลเดอร์ GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="203b6-178">ถ้ามีกรณีทดสอบที่มีอยู่ ก่อนที่คุณจะเปลี่ยนแปลงค่าในไฟล์ .config จะไม่มีการสร้างล็อกสำหรับกรณีการทดสอบดังกล่าวจนกว่าคุณจะสร้างไฟล์การดำเนินการทดสอบใหม่</span><span class="sxs-lookup"><span data-stu-id="203b6-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![คำสั่งสร้างไฟล์การดำเนินการข้อความเท่านั้น บนเมนูใหม่](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="203b6-180">สแนปช็อต</span><span class="sxs-lookup"><span data-stu-id="203b6-180">Snapshot</span></span>

<span data-ttu-id="203b6-181">คุณลักษณะนี้จะจับภาพหน้าจอของขั้นตอนที่ดำเนินการในระหว่างการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="203b6-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="203b6-182">เมื่อต้องการใช้คุณลักษณะนี้ เปิดไฟล์ **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ภายใต้โฟลเดอร์การติดตั้ง RSAT (ตัวอย่างเช่น **C:\\Program Files (x86)\\Regression Suite Automation Tool**) และเปลี่ยนค่าขององค์ประกอบต่อไปนี้จาก **เท็จ** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="203b6-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="203b6-183">ภายใต้ **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** โฟลเดอร์ที่แยกต่างหากจะถูกสร้างขึ้นสำหรับกรณีการทดสอบแต่ละกรณีที่มีการรัน</span><span class="sxs-lookup"><span data-stu-id="203b6-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![โฟลเดอร์สแนปช็อตสำหรับกรณีการทดสอบ](./media/use_rsa_tool_12.png)

<span data-ttu-id="203b6-185">ในโฟลเดอร์เหล่านี้แต่ละโฟลเดอร์ คุณสามารถค้นหาสแนปช็อตของขั้นตอนต่างๆ ที่ดำเนินการ ในขณะที่มีการรันกรณีการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="203b6-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![ไฟล์สแนปช็อต](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="203b6-187">การกำหนด</span><span class="sxs-lookup"><span data-stu-id="203b6-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="203b6-188">สถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="203b6-188">Scenario</span></span>

1. <span data-ttu-id="203b6-189">โปรแกรมออกแบบผลิตภัณฑ์จะสร้างผลิตภัณฑ์ที่นำออกใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="203b6-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="203b6-190">ผู้จัดการฝ่ายผลิตเริ่มต้นใบสั่งผลิตเพื่อนำระดับสินค้าคงคลังไปที่สองชิ้น</span><span class="sxs-lookup"><span data-stu-id="203b6-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="203b6-191">การผลิตจะเริ่มต้นและสิ้นสุดใบสั่งผลิต และตรวจสอบว่าปริมาณคงคลังคงเหลือคือสองชิ้น</span><span class="sxs-lookup"><span data-stu-id="203b6-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="203b6-192">ทีมงานขายได้รับใบสั่งสำหรับผลิตภัณฑ์ใหม่สี่ชิ้น</span><span class="sxs-lookup"><span data-stu-id="203b6-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="203b6-193">ดังนั้น ทีมขายจึงปรับปรุงความต้องการสุทธิผ่านแผนแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="203b6-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="203b6-194">เนื่องจากไม่มีกำลังการผลิตเพิ่มเติม จะมีการตั้งค่านโยบายใบสั่งเริ่มต้นเป็น "ซื้อแทนที่จะทำ"</span><span class="sxs-lookup"><span data-stu-id="203b6-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="203b6-195">ดังนั้น แผนการใบสั่งซื้อจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="203b6-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="203b6-196">ผู้ซื้อจะเพิ่มผู้จัดจำหน่าย ยืนยันแผนการใบสั่งซื้อ แล้วจากนั้น ยืนยันใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="203b6-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="203b6-197">เมื่อสินค้าที่ซื้อมาถึงที่ร้านค้า ผู้ปฏิบัติงานร้านค้าจะค้นหาใบสั่งซื้อที่เกี่ยวข้อง และรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="203b6-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="203b6-198">เนื่องจากใบสั่งนี้เสร็จสมบูรณ์แล้วในขณะนี้ คุณสามารถเบิกสินค้าและบรรจุสินค้าตามใบสั่งขายได้</span><span class="sxs-lookup"><span data-stu-id="203b6-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="203b6-199">การเงินลงรายการบัญชีใบแจ้งหนี้การซื้อและใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="203b6-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="203b6-200">ภาพประกอบต่อไปนี้แสดงโฟลว์สำหรับสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="203b6-200">The following illustration shows the flow for this scenario.</span></span>

![โฟลว์สำหรับสถานการณ์จำลองการสาธิต](./media/use_rsa_tool_14.png)

<span data-ttu-id="203b6-202">ภาพประกอบต่อไปนี้แสดงกระบวนการทางธุรกิจสำหรับสถานการณ์จำลองนี้ใน RSAT</span><span class="sxs-lookup"><span data-stu-id="203b6-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![กระบวนการทางธุรกิจสำหรับสถานการณ์จำลองการสาธิต](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="203b6-204">กลยุทธ์ – การเรียนรู้ที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="203b6-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="203b6-205">ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="203b6-205">Data</span></span>

- <span data-ttu-id="203b6-206">ตรวจสอบให้แน่ใจว่าคุณมีปริมาณข้อมูลของตัวแทน (สำเนาของข้อมูลการตั้งค่าคอนฟิกการผลิต/แบบ golden รวมถึงข้อมูลที่ถูกย้าย)</span><span class="sxs-lookup"><span data-stu-id="203b6-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="203b6-207">เมื่อคุณสร้างข้อมูลใหม่ผ่านตัวบันทึกงาน ให้สร้างชื่อการทดสอบที่จะไม่ขัดแย้งกับชื่อที่มีอยู่ (ตัวอย่างเช่น ใช้คำนำหน้า เช่น **RSATxxx**)</span><span class="sxs-lookup"><span data-stu-id="203b6-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="203b6-208">ใช้การคืนค่า Azure Point-In-Time เพื่อรันการทดสอบในสภาพแวดล้อมที่ไม่ใช่ระดับ 1 อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="203b6-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="203b6-209">ถึงแม้ว่าคุณจะสามารถใช้ฟังก์ชัน Excel **RANDOM** และ **NOW** เพื่อสร้างชุดที่ไม่ซ้ำกันได้ แต่ความพยายามจะสูงอย่างมาก</span><span class="sxs-lookup"><span data-stu-id="203b6-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="203b6-210">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="203b6-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="203b6-211">ตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="203b6-211">Task recorder</span></span>

- <span data-ttu-id="203b6-212">กำหนดสถานการณ์จำลอง ก่อนที่คุณจะเริ่มการบันทึก</span><span class="sxs-lookup"><span data-stu-id="203b6-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="203b6-213">โครงการที่มีการจัดการอย่างดีมีสถานการณ์จำลองการทดสอบที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="203b6-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="203b6-214">เมื่อต้องการสร้างกรณีการทดสอบ ให้พิจารณาว่าผลลัพธ์ของสถานการณ์จำลองของการทดสอบดังกล่าวสามารถคาดการณ์ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="203b6-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="203b6-215">แบ่งการบันทึก ถ้ามีการดำเนินการโดยบทบาทต่างๆ หรือหากมีเวลารอ หรือเหตุการณ์ภายนอกก่อนขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="203b6-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="203b6-216">หลีกเลี่ยงการเลือกค่าในรายการ</span><span class="sxs-lookup"><span data-stu-id="203b6-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="203b6-217">แต่ใช้รูปแบบข้อความ เช่น **FIFO** **AudioRM** และ **SiteWH** แทน</span><span class="sxs-lookup"><span data-stu-id="203b6-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="203b6-218">เมื่อคุณเลือกในรายการ จะมีการบันทึกตำแหน่งของค่าในรายการ ไม่ใช่ตัวค่าเอง</span><span class="sxs-lookup"><span data-stu-id="203b6-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="203b6-219">ถ้ามีการเพิ่มสินค้าลงในรายการดังกล่าว ตำแหน่งของมูลค่าอาจเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="203b6-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="203b6-220">ดังนั้น การบันทึกของคุณจะใช้พารามิเตอร์ที่แตกต่างกัน และส่วนที่เหลือของสถานการณ์จำลองดังกล่าวอาจได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="203b6-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="203b6-221">ลองนึกถึงลักษณะการทำงานของผู้ใช้หลายราย</span><span class="sxs-lookup"><span data-stu-id="203b6-221">Think about multi-user behavior.</span></span> <span data-ttu-id="203b6-222">ตัวอย่างเช่น อย่าสันนิษฐานว่าใบสั่งขายที่สร้างขึ้นใหม่ของคุณจะถูกเลือกโดยอัตโนมัติเสมอ</span><span class="sxs-lookup"><span data-stu-id="203b6-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="203b6-223">แต่ใช้ตัวกรองเพื่อค้นหาใบสั่งที่ถูกต้องแทนเสมอ</span><span class="sxs-lookup"><span data-stu-id="203b6-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="203b6-224">ใช้ฟังก์ชันคัดลอกในตัวบันทึกงานเพื่อบันทึกชื่อของผลิตภัณฑ์ที่สร้างขึ้นใหม่ เพื่อให้สามารถใช้งานได้ในกรณีการทดสอบที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="203b6-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="203b6-225">ใช้ฟังก์ชันตรวจสอบความถูกต้องในตัวบันทึกงาน เพื่อตั้งค่าจุดตรวจสอบว่ามีการรันขั้นตอนอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="203b6-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="203b6-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="203b6-226">RSAT</span></span>

- <span data-ttu-id="203b6-227">เมื่อต้องการรันการทดสอบในบริษัทอื่น คุณสามารถเปลี่ยนบริษัทบนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="203b6-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="203b6-228">ตรวจสอบให้แน่ใจว่าการตั้งค่าและข้อมูลพร้อมใช้งานในบริษัทที่เลือกใหม่</span><span class="sxs-lookup"><span data-stu-id="203b6-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="203b6-229">คุณสามารถเปลี่ยนผู้ใช้การทดสอบบนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="203b6-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="203b6-230">ระบุรหัสอีเมลของผู้ใช้ที่จะรันกรณีการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="203b6-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="203b6-231">ในลักษณะนี้ อาจมีการรันกรณีการทดสอบโดยใช้สิทธิ์การรักษาความปลอดภัยของผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="203b6-232">เมื่อต้องการรอก่อนที่จะเริ่มต้นการทดสอบ คุณสามารถกำหนดการหยุดชั่วคราวบนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="203b6-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="203b6-233">สามารถใช้การหยุดชั่วคราวนี้ในชุดงาน (ตัวอย่างเช่น ถ้าต้องรันลำดับงานก่อนที่จะสามารถดำเนินการขั้นตอนต่อไป)</span><span class="sxs-lookup"><span data-stu-id="203b6-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="203b6-234">การเขียนสคริปต์ขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="203b6-234">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="203b6-235">CLI</span><span class="sxs-lookup"><span data-stu-id="203b6-235">CLI</span></span>

<span data-ttu-id="203b6-236">RSAT สามารถถูกเรียกจากหน้าต่าง **พร้อมต์คำสั่ง** หรือ **PowerShell**</span><span class="sxs-lookup"><span data-stu-id="203b6-236">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="203b6-237">ตรวจสอบว่าตัวแปรของสภาพแวดล้อม **TestRoot** ถูกตั้งค่าเป็นพาธการติดตั้ง RSAT</span><span class="sxs-lookup"><span data-stu-id="203b6-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="203b6-238">(ใน Microsoft Windows เปิด **แผงควบคุม** เลือก **ระบบและการรักษาความปลอดภัย \> ระบบ \> การตั้งค่าระบบขั้นสูง** และจากนั้น เลือก **ตัวแปรของสภาพแวดล้อม** )</span><span class="sxs-lookup"><span data-stu-id="203b6-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="203b6-239">เปิดหน้าต่าง **พร้อมต์คำสั่ง** หรือ **PowerShell** เป็นผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="203b6-239">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="203b6-240">นำทางไปยังไดเรกทอรีการติดตั้ง RSAT</span><span class="sxs-lookup"><span data-stu-id="203b6-240">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="203b6-241">แสดงรายการคำสั่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="203b6-241">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="203b6-242">?</span><span class="sxs-lookup"><span data-stu-id="203b6-242">?</span></span> 
<span data-ttu-id="203b6-243">แสดงวิธีใช้เกี่ยวกับคำสั่งที่มีอยู่ทั้งหมดและพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="203b6-243">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="203b6-244">พารามิเตอร์ที่ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-244">Optional parameters</span></span>

**``command``**


<span data-ttu-id="203b6-245">ที่ซึ่ง ``[command]`` เป็นหนึ่งในคำสั่งที่ระบุไว้ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="203b6-245">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="203b6-246">เกี่ยวกับ</span><span class="sxs-lookup"><span data-stu-id="203b6-246">about</span></span>
<span data-ttu-id="203b6-247">แสดงรุ่นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="203b6-247">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="203b6-248">cls</span><span class="sxs-lookup"><span data-stu-id="203b6-248">cls</span></span>
<span data-ttu-id="203b6-249">ล้างหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="203b6-249">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="203b6-250">ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="203b6-250">download</span></span>
<span data-ttu-id="203b6-251">ดาวน์โหลดเอกสารแนบสำหรับกรณีทดสอบที่ระบุไปยังไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="203b6-251">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="203b6-252">คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-252">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="203b6-253">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**</span><span class="sxs-lookup"><span data-stu-id="203b6-253">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="203b6-254">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-254">Required parameters</span></span>
<span data-ttu-id="203b6-255">**``test_case_id``** แสดงรหัสกรณีทดสอบ</span><span class="sxs-lookup"><span data-stu-id="203b6-255">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="203b6-256">**``output_dir``** แสดงถึงไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="203b6-256">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="203b6-257">ต้องมีไดเรกทอรีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-257">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="203b6-258">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-258">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="203b6-259">แก้ไข</span><span class="sxs-lookup"><span data-stu-id="203b6-259">edit</span></span>
<span data-ttu-id="203b6-260">อนุญาตให้คุณเปิดไฟล์พารามิเตอร์ในโปรแกรม Excel และแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="203b6-260">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="203b6-261">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-261">Required parameters</span></span>
<span data-ttu-id="203b6-262">**``excel_file``** ต้องมีพาธเต็มไปยังไฟล์ Excel ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-262">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="203b6-263">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-263">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="203b6-264">สร้าง</span><span class="sxs-lookup"><span data-stu-id="203b6-264">generate</span></span>
<span data-ttu-id="203b6-265">สร้างการดำเนินการทดสอบและไฟล์พารามิเตอร์สำหรับกรณีทดสอบที่ระบุในไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="203b6-265">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="203b6-266">คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-266">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="203b6-267">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**</span><span class="sxs-lookup"><span data-stu-id="203b6-267">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="203b6-268">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-268">Required parameters</span></span>
<span data-ttu-id="203b6-269">**``test_case_id``** แสดงรหัสกรณีทดสอบ</span><span class="sxs-lookup"><span data-stu-id="203b6-269">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="203b6-270">**``output_dir``** แสดงถึงไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="203b6-270">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="203b6-271">ต้องมีไดเรกทอรีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-271">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="203b6-272">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-272">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="203b6-273">generatederived</span><span class="sxs-lookup"><span data-stu-id="203b6-273">generatederived</span></span>
<span data-ttu-id="203b6-274">สร้างกรณีการทดสอบใหม่ซึ่งสืบทอดมาจากกรณีการทดสอบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-274">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="203b6-275">คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-275">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="203b6-276">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**</span><span class="sxs-lookup"><span data-stu-id="203b6-276">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="203b6-277">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-277">Required parameters</span></span>
<span data-ttu-id="203b6-278">**``parent_test_case_id``** แสดงรหัสกรณีทดสอบหลัก</span><span class="sxs-lookup"><span data-stu-id="203b6-278">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="203b6-279">**``test_plan_id``** แสดงรหัสแผนทดสอบ</span><span class="sxs-lookup"><span data-stu-id="203b6-279">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="203b6-280">**``test_suite_id``** แสดงรหัสชุดทดสอบ</span><span class="sxs-lookup"><span data-stu-id="203b6-280">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="203b6-281">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-281">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="203b6-282">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="203b6-282">generatetestonly</span></span>
<span data-ttu-id="203b6-283">สร้างเฉพาะไฟล์การดำเนินการทดสอบและกรณีทดสอบที่ระบุในไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="203b6-283">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="203b6-284">คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-284">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="203b6-285">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**</span><span class="sxs-lookup"><span data-stu-id="203b6-285">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="203b6-286">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-286">Required parameters</span></span>
<span data-ttu-id="203b6-287">**``test_case_id``** แสดงรหัสกรณีทดสอบ</span><span class="sxs-lookup"><span data-stu-id="203b6-287">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="203b6-288">**``output_dir``** แสดงถึงไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="203b6-288">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="203b6-289">ต้องมีไดเรกทอรีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-289">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="203b6-290">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-290">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="203b6-291">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="203b6-291">generatetestsuite</span></span>
<span data-ttu-id="203b6-292">สร้างกรณีการทดสอบทั้งหมดสำหรับชุดที่ระบุในไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="203b6-292">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="203b6-293">คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-293">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="203b6-294">ใช้ค่าใดๆ จากคอลัมน์เป็นพารามิเตอร์ **test_suite_name**</span><span class="sxs-lookup"><span data-stu-id="203b6-294">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="203b6-295">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-295">Required parameters</span></span>
<span data-ttu-id="203b6-296">**``test_suite_name``** แสดงชื่อชุดทดสอบ</span><span class="sxs-lookup"><span data-stu-id="203b6-296">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="203b6-297">**``output_dir``** แสดงถึงไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="203b6-297">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="203b6-298">ต้องมีไดเรกทอรีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-298">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="203b6-299">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-299">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="203b6-300">วิธีใช้</span><span class="sxs-lookup"><span data-stu-id="203b6-300">help</span></span>
<span data-ttu-id="203b6-301">เหมือนกับ [?](####?)</span><span class="sxs-lookup"><span data-stu-id="203b6-301">Identical to the [?](####?)</span></span> <span data-ttu-id="203b6-302">คำสั่ง</span><span class="sxs-lookup"><span data-stu-id="203b6-302">command</span></span>


#### <a name="list"></a><span data-ttu-id="203b6-303">รายการ</span><span class="sxs-lookup"><span data-stu-id="203b6-303">list</span></span>
<span data-ttu-id="203b6-304">แสดงรายการกรณีที่มีการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-304">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="203b6-305">listtestplans</span><span class="sxs-lookup"><span data-stu-id="203b6-305">listtestplans</span></span>
<span data-ttu-id="203b6-306">แสดงรายการแผนการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-306">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="203b6-307">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="203b6-307">listtestsuite</span></span>
<span data-ttu-id="203b6-308">แสดงรายการกรณีทดสอบสำหรับชุดการทดสอบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-308">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="203b6-309">คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="203b6-310">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **suite_name**</span><span class="sxs-lookup"><span data-stu-id="203b6-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="203b6-311">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-311">Required parameters</span></span>
<span data-ttu-id="203b6-312">**``suite_name``** ชื่อของชุดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="203b6-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="203b6-313">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-313">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="203b6-314">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="203b6-314">listtestsuitenames</span></span>
<span data-ttu-id="203b6-315">แสดงรายการชุดการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-315">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="203b6-316">ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="203b6-316">playback</span></span>
<span data-ttu-id="203b6-317">ย้อนกลับกรณีการทดสอบโดยใช้ไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="203b6-317">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="203b6-318">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-318">Required parameters</span></span>
<span data-ttu-id="203b6-319">**``excel_file``** พาธแบบเต็มไปที่ไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="203b6-319">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="203b6-320">ต้องมีไฟล์อยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-320">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="203b6-321">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-321">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="203b6-322">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="203b6-322">playbackbyid</span></span>
<span data-ttu-id="203b6-323">ย้อนกลับกรณีการทดสอบหลายกรณีพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="203b6-323">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="203b6-324">คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-324">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="203b6-325">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**</span><span class="sxs-lookup"><span data-stu-id="203b6-325">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="203b6-326">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-326">Required parameters</span></span>
<span data-ttu-id="203b6-327">**``test_case_id1``** รหัสของกรณีทดสอบที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-327">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="203b6-328">**``test_case_id2``** รหัสของกรณีทดสอบที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-328">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="203b6-329">**``test_case_idN``** รหัสของกรณีทดสอบที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-329">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="203b6-330">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-330">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="203b6-331">playbackmany</span><span class="sxs-lookup"><span data-stu-id="203b6-331">playbackmany</span></span>
<span data-ttu-id="203b6-332">ย้อนกลับกรณีทดสอบหลายกรณีพร้อมกันโดยใช้ไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="203b6-332">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="203b6-333">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-333">Required parameters</span></span>
<span data-ttu-id="203b6-334">**``excel_file1``** พาธแบบเต็มไปที่ไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="203b6-334">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="203b6-335">ต้องมีไฟล์อยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-335">File must exist.</span></span>  
<span data-ttu-id="203b6-336">**``excel_file2``** พาธแบบเต็มไปที่ไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="203b6-336">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="203b6-337">ต้องมีไฟล์อยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-337">File must exist.</span></span>  
<span data-ttu-id="203b6-338">**``excel_fileN``** พาธแบบเต็มไปที่ไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="203b6-338">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="203b6-339">ต้องมีไฟล์อยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-339">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="203b6-340">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-340">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="203b6-341">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="203b6-341">playbacksuite</span></span>
<span data-ttu-id="203b6-342">ย้อนกลับกรณีทดสอบทั้งหมดจากชุดทดสอบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-342">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="203b6-343">คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="203b6-343">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="203b6-344">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **suite_name**</span><span class="sxs-lookup"><span data-stu-id="203b6-344">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="203b6-345">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-345">Required parameters</span></span>
<span data-ttu-id="203b6-346">**``suite_name``** ชื่อของชุดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="203b6-346">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="203b6-347">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-347">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="203b6-348">ออก</span><span class="sxs-lookup"><span data-stu-id="203b6-348">quit</span></span>
<span data-ttu-id="203b6-349">ปิดแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="203b6-349">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="203b6-350">อัพโหลด</span><span class="sxs-lookup"><span data-stu-id="203b6-350">upload</span></span>
<span data-ttu-id="203b6-351">อัพโหลดไฟล์ทั้งหมดที่เป็นของชุดทดสอบหรือกรณีการทดสอบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-351">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="203b6-352">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-352">Required parameters</span></span>
<span data-ttu-id="203b6-353">**``suite_name``** ไฟล์ทั้งหมดที่เป็นของชุดทดสอบที่ระบุจะถูกอัพโหลด</span><span class="sxs-lookup"><span data-stu-id="203b6-353">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="203b6-354">**``testcase_id``** ไฟล์ทั้งหมดที่เป็นของกรณีทดสอบที่ระบุจะถูกอัพโหลด</span><span class="sxs-lookup"><span data-stu-id="203b6-354">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="203b6-355">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-355">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="203b6-356">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="203b6-356">uploadrecording</span></span>
<span data-ttu-id="203b6-357">อัพโหลดเฉพาะไฟล์การบันทึกที่เป็นของกรณีการทดสอบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-357">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="203b6-358">พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="203b6-358">Required parameters</span></span>
<span data-ttu-id="203b6-359">**``testcase_id``** ไฟล์การบันทึกที่เป็นของกรณีการทดสอบที่ระบุจะถูกอัพโหลด</span><span class="sxs-lookup"><span data-stu-id="203b6-359">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="203b6-360">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="203b6-360">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="203b6-361">การใช้</span><span class="sxs-lookup"><span data-stu-id="203b6-361">usage</span></span>
<span data-ttu-id="203b6-362">แสดงวิธีสองวิธีในการเรียกใช้แอพลิเคชันนี้: วิธีหนึ่งโดยใช้ไฟล์การตั้งค่าเริ่มต้น อีกวิธีหนึ่งให้ไฟล์การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="203b6-362">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="203b6-363">ตัวอย่างของ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="203b6-363">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="203b6-364">รันกรณีการทดสอบในลูป</span><span class="sxs-lookup"><span data-stu-id="203b6-364">Run a test case in a loop</span></span>

<span data-ttu-id="203b6-365">คุณมีสคริปต์การทดสอบที่สร้างลูกค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="203b6-365">You have a test script that creates a new customer.</span></span> <span data-ttu-id="203b6-366">โดยการเขียนสคริปต์ อาจมีการรันกรณีการทดสอบนี้ในลูปโดยการสุ่มข้อมูลต่อไปนี้ ก่อนที่จะมีการรันการเกิดซ้ำแต่ละครั้ง:</span><span class="sxs-lookup"><span data-stu-id="203b6-366">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="203b6-367">รหัสลูกค้า</span><span class="sxs-lookup"><span data-stu-id="203b6-367">Customer ID</span></span>
- <span data-ttu-id="203b6-368">ชื่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="203b6-368">Customer name</span></span>
- <span data-ttu-id="203b6-369">ที่อยู่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="203b6-369">Customer address</span></span>

<span data-ttu-id="203b6-370">รหัสลูกค้าจะอยู่ในรูปแบบ *ATCUS\<หมายเลข\>* โดยที่ \<หมายเลข\> อยู่ระหว่าง **000000001** และ **999999999**</span><span class="sxs-lookup"><span data-stu-id="203b6-370">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="203b6-371">ตัวอย่างต่อไปนี้ใช้พารามิเตอร์ **เริ่มต้น** เพื่อกำหนดหมายเลขแรกที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="203b6-371">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="203b6-372">ใช้พารามิเตอร์ที่สอง **nr** เพื่อกำหนดจำนวนของลูกค้าที่ต้องสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="203b6-372">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="203b6-373">สำหรับการเกิดซ้ำแต่ละครั้ง จะมีการเปลี่ยนแปลงพารามิเตอร์ในไฟล์พารามิเตอร์ Excel โดยใช้ฟังก์ชัน UpdateCustomer</span><span class="sxs-lookup"><span data-stu-id="203b6-373">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="203b6-374">จากนั้น รายการคำสั่ง RSAT ถูกเรียกในฟังก์ชัน RunTestCase</span><span class="sxs-lookup"><span data-stu-id="203b6-374">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="203b6-375">เปิด Microsoft Windows PowerShell Integrated Scripting Environment (ISE) ในโหมดผู้ดูแลระบบ และวางรหัสต่อไปนี้ลงในหน้าต่างที่ชื่อ **Untitled1.ps1**</span><span class="sxs-lookup"><span data-stu-id="203b6-375">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="203b6-376">รันสคริปต์ที่ขึ้นอยู่กับข้อมูลใน Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="203b6-376">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="203b6-377">ตัวอย่างต่อไปนี้ใช้การเรียก Open Data Protocol (OData) ในการค้นหาสถานะใบสั่งของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="203b6-377">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="203b6-378">ถ้าสถานะยังไม่ได้ **ออกใบแจ้งหนี้** คุณสามารถ ตัวอย่างเช่น เรียกใช้กรณีการทดสอบ RSAT ที่ลงรายการบัญชีใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="203b6-378">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
