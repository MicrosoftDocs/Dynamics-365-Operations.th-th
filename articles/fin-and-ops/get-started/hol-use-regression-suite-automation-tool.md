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
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 8f3cd6a27ba0e09e48c0562aff46791228bb46b5
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703863"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="de3c5-104">ใช้บทช่วยสอน Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="de3c5-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="de3c5-105">ใช้เครื่องมือเบราว์เซอร์อินเทอร์เน็ตของคุณเพื่อดาวน์โหลดและบันทึกหน้านี้ในรูปแบบ pdf</span><span class="sxs-lookup"><span data-stu-id="de3c5-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="de3c5-106">บทช่วยสอนนี้จะแนะนำคุณลักษณะขั้นสูงบางอย่างของ Regression Suite Automation Tool (RSAT) รวมถึงการกำหนดการสาธิต และอธิบายถึงกลยุทธ์และประเด็นการเรียนรู้ที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="de3c5-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="de3c5-107">คุณลักษณะของ RSAT/ตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="de3c5-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="de3c5-108">ตรวจสอบความถูกต้องของค่าฟิลด์</span><span class="sxs-lookup"><span data-stu-id="de3c5-108">Validate a field value</span></span>

<span data-ttu-id="de3c5-109">สำหรับข้อมูลเกี่ยวกับคุณลักษณะนี้ ดู [สร้างการบันทึกงานใหม่ที่มีฟังก์ชันตรวจสอบความถูกต้อง](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function)</span><span class="sxs-lookup"><span data-stu-id="de3c5-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="de3c5-110">ตัวแปรที่บันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="de3c5-110">Saved variable</span></span>

<span data-ttu-id="de3c5-111">สำหรับข้อมูลเกี่ยวกับคุณลักษณะนี้ ดู [ปรับเปลี่ยนการบันทึกงานที่มีอยู่เพื่อสร้างตัวแปรที่บันทึกไว้](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable)</span><span class="sxs-lookup"><span data-stu-id="de3c5-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="de3c5-112">กรณีการทดสอบที่สืบทอดมา</span><span class="sxs-lookup"><span data-stu-id="de3c5-112">Derived test case</span></span>

1. <span data-ttu-id="de3c5-113">เปิด Regression Suite Automation Tool (RSAT) และเลือกกรณีการทดสอบทั้งสองกรณีที่คุณสร้างขึ้นใน [ตั้งค่าและติดตั้ง Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md)</span><span class="sxs-lookup"><span data-stu-id="de3c5-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="de3c5-114">เลือก **สร้าง \> สร้างกรณีการทดสอบที่สืบทอดมา**</span><span class="sxs-lookup"><span data-stu-id="de3c5-114">Select **New \> Create derived test case**.</span></span>

    ![สร้างคำสั่งของกรณีทดสอบที่สืบทอดมาบนเมนูใหม่](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="de3c5-116">คุณได้รับข้อความที่แจ้งว่าจะมีการสร้างกรณีการทดสอบที่สืบทอดมาสำหรับกรณีการทดสอบที่เลือกแต่ละกรณีในชุดการทดสอบปัจจุบัน และกรณีการทดสอบที่สืบทอดมาแต่ละกรณีจะมีสำเนาของไฟล์พารามิเตอร์ Excel ของตนเอง</span><span class="sxs-lookup"><span data-stu-id="de3c5-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="de3c5-117">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="de3c5-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de3c5-118">เมื่อคุณรันกรณีการทดสอบที่สืบทอดมา จะใช้การบันทึกงานของกรณีการทดสอบหลักและสำเนาของไฟล์พารามิเตอร์ Excel ของตนเอง</span><span class="sxs-lookup"><span data-stu-id="de3c5-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="de3c5-119">ด้วยวิธีนี้ คุณสามารถรันการทดสอบเดียวกันด้วยพารามิเตอร์ต่างๆ ได้ โดยไม่ต้องมีการรักษาการบันทึกงานมากกว่าหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="de3c5-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="de3c5-120">กรณีการทดสอบที่สืบทอดมาไม่จำเป็นต้องเป็นส่วนหนึ่งของชุดการทดสอบเดียวกันกับกรณีการทดสอบหลัก</span><span class="sxs-lookup"><span data-stu-id="de3c5-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![กล่องข้อความ](./media/use_rsa_tool_02.png)

    <span data-ttu-id="de3c5-122">มีการสร้างกรณีการทดสอบที่สืบทอดมาเพิ่มเติมสองกรณี และกล่องกาเครื่องหมาย **ได้รับมาหรือไม่?** จะถูกเลือกสำหรับกรณีเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="de3c5-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![มีการสร้างกรณีการทดสอบที่สืบทอดมา](./media/use_rsa_tool_03.png)

    <span data-ttu-id="de3c5-124">มีการสร้างกรณีการทดสอบที่สืบทอดมาโดยอัตโนมัติใน Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="de3c5-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="de3c5-125">นี่เป็นรายการรองของกรณีการทดสอบ **สร้างผลิตภัณฑ์ใหม่** และมีการติดแท็กด้วยคำสำคัญพิเศษ: **RSAT: DerivedTestSteps**</span><span class="sxs-lookup"><span data-stu-id="de3c5-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="de3c5-126">นอกจากนี้ กรณีการทดสอบเหล่านี้จะถูกเพิ่มเข้าไปในแผนการทดสอบโดยอัตโนมัติใน Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="de3c5-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![คำสำคัญ RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="de3c5-128">ถ้า เนื่องจากสาเหตุใดๆ กรณีการทดสอบที่สืบทอดมาที่ถูกสร้างนั้นไม่ได้อยู่ในลำดับที่ถูกต้อง ไปที่ Azure DevOps และจัดลำดับกรณีการทดสอบใหม่ในชุดการทดสอบ เพื่อให้ RSAT สามารถรันได้ในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="de3c5-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="de3c5-129">เลือกกรณีการทดสอบที่สืบทอดมา แล้วจากนั้น เลือก **แก้ไข** เพื่อเปิดไฟล์พารามิเตอร์ Excel ที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="de3c5-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="de3c5-130">แก้ไขไฟล์พารามิเตอร์ของ Excel เหล่านี้ในลักษณะเดียวกับที่คุณแก้ไขไฟล์หลัก</span><span class="sxs-lookup"><span data-stu-id="de3c5-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="de3c5-131">กล่าวอีกอย่างหนึ่งคือ ตรวจสอบให้แน่ใจว่ามีการตั้งค่ารหัสผลิตภัณฑ์ เพื่อให้มีการสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="de3c5-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="de3c5-132">นอกจากนี้ ตรวจสอบให้แน่ใจว่าตัวแปรที่บันทึกไว้ถูกคัดลอกไปยังฟิลด์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="de3c5-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="de3c5-133">บนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel ให้ปรับปรุงค่าของฟิลด์ **บริษัท** เป็น **USSI** เพื่อให้กรณีการทดสอบที่สืบทอดมาจะถูกรันเทียบกับนิติบุคคลอื่นที่ไม่ใช่กรณีการทดสอบหลัก</span><span class="sxs-lookup"><span data-stu-id="de3c5-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="de3c5-134">เมื่อต้องการรันกรณีการทดสอบเทียบกับผู้ใช้ที่ระบุ (หรือบทบาทที่สัมพันธ์กับผู้ใช้ที่ระบุ) คุณสามารถปรับปรุงค่าของฟิลด์ **ผู้ใช้การทดสอบ** ได้</span><span class="sxs-lookup"><span data-stu-id="de3c5-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="de3c5-135">เลือก **รัน** และตรวจสอบความถูกต้องว่าผลิตภัณฑ์ถูกสร้างขึ้นในทั้งนิติบุคคล USMF และนิติบุคคล USSI</span><span class="sxs-lookup"><span data-stu-id="de3c5-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="de3c5-136">ตรวจสอบความถูกต้องของการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="de3c5-136">Validate notifications</span></span>

<span data-ttu-id="de3c5-137">สามารถใช้คุณลักษณะนี้เพื่อตรวจสอบว่าเกิดการดำเนินการขึ้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="de3c5-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="de3c5-138">ตัวอย่างเช่น เมื่อใบสั่งผลิตถูกสร้าง ประมาณการ และจากนั้น เริ่มต้น Microsoft Dynamics 365 for Finance and Operations จะแสดงข้อความ "การผลิต – เริ่มต้น" เพื่อแจ้งให้คุณทราบว่าใบสั่งผลิตเริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="de3c5-138">For example, when a production order is created, estimated, and then started, Microsoft Dynamics 365 for Finance and Operations shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![การผลิต – เริ่มการแจ้งเตือน](./media/use_rsa_tool_05.png)

<span data-ttu-id="de3c5-140">คุณสามารถตรวจสอบความถูกต้องของข้อความนี้ผ่าน RSAT โดยการป้อนข้อความในแท็บ **MessageValidation** ของไฟล์พารามิเตอร์ Excel สำหรับการบันทึกที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="de3c5-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![แท็บการตรวจสอบความถูกต้องของข้อความ](./media/use_rsa_tool_06.png)

<span data-ttu-id="de3c5-142">หลังจากรันกรณีการทดสอบ ข้อความในไฟล์พารามิเตอร์ของ Excel จะถูกเปรียบเทียบกับข้อความที่แสดงอยู่ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="de3c5-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown in Finance and Operations.</span></span> <span data-ttu-id="de3c5-143">ถ้าข้อความไม่ตรงกัน กรณีการทดสอบจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="de3c5-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="de3c5-144">คุณสามารถป้อนข้อความมากกว่าหนึ่งข้อความได้บนแท็บ **MessageValidation** ในไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="de3c5-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="de3c5-145">นอกจากนี้ ข้อความอาจเป็นข้อผิดพลาดหรือข้อความเตือน แทนที่จะเป็นข้อความที่ให้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="de3c5-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="de3c5-146">ตรวจสอบความถูกต้องของค่าโดยใช้ตัวดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="de3c5-146">Validate values by using operators</span></span>

<span data-ttu-id="de3c5-147">ในรุ่นก่อนหน้าของ RSAT คุณสามารถตรวจสอบความถูกต้องของค่าได้ เฉพาะเมื่อค่าการควบคุมเท่ากับค่าที่คาดไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="de3c5-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="de3c5-148">คุณลักษณะใหม่ช่วยให้คุณสามารถตรวจสอบตัวแปรที่ไม่เท่ากับ น้อยกว่า หรือมากกว่า ค่าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="de3c5-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="de3c5-149">เมื่อต้องการใช้คุณลักษณะนี้ เปิดไฟล์ **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ภายใต้โฟลเดอร์การติดตั้ง RSAT (ตัวอย่างเช่น **C:\\Program Files (x86)\\Regression Suite Automation Tool**) และเปลี่ยนค่าในองค์ประกอบต่อไปนี้จาก **เท็จ** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="de3c5-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="de3c5-150">ในไฟล์พารามิเตอร์ Excel ฟิลด์ **ผู้ปฏิบัติงาน** ใหม่ จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="de3c5-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de3c5-151">ถ้าคุณได้ใช้เวอร์ชันที่เก่ากว่าของ RSAT คุณต้องสร้างไฟล์พารามิเตอร์ Excel ใหม่</span><span class="sxs-lookup"><span data-stu-id="de3c5-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![ฟิลด์ตัวดำเนินงาน](./media/use_rsa_tool_07.png)

<span data-ttu-id="de3c5-153">ตัวอย่างต่อไปนี้แสดงวิธีการที่คุณสามารถใช้คุณลักษณะนี้เพื่อตรวจสอบว่าปริมาณคงคลังคงเหลือมากกว่า 0 (ศูนย์) หรือไม่</span><span class="sxs-lookup"><span data-stu-id="de3c5-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="de3c5-154">ในข้อมูลสาธิตในบริษัท **USMF** ให้สร้างการบันทึกงานที่มีขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="de3c5-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="de3c5-155">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="de3c5-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="de3c5-156">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="de3c5-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="de3c5-157">ตัวอย่างเช่น ตัวกรองในค่าของ **1000** สำหรับฟิลด์ **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="de3c5-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="de3c5-158">เลือก **ปริมาณสินค้าคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="de3c5-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="de3c5-159">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="de3c5-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="de3c5-160">ตัวอย่างเช่น ตัวกรองในค่าของ **1** สำหรับฟิลด์ **ไซต์**</span><span class="sxs-lookup"><span data-stu-id="de3c5-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="de3c5-161">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="de3c5-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="de3c5-162">ตรวจสอบความถูกต้องว่าค่าของฟิลด์ **ทั้งหมดที่พร้อมใช้งาน** คือ **411.0000000000000000**</span><span class="sxs-lookup"><span data-stu-id="de3c5-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="de3c5-163">บันทึกการบันทึกงานไปยังไลบรารี BPM และซิงค์กับ Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="de3c5-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="de3c5-164">เพิ่มกรณีการทดสอบไปยังแผนการทดสอบ และโหลดกรณีการทดสอบลงใน RSAT</span><span class="sxs-lookup"><span data-stu-id="de3c5-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="de3c5-165">เปิดไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="de3c5-165">Open the Excel parameter file.</span></span> <span data-ttu-id="de3c5-166">บนแท็บ **InventOnhandItem** คุณจะเห็นส่วน **ตรวจสอบความถูกต้องของ InventOnhandItem** ที่มีฟิลด์ **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="de3c5-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![ฟิลด์ตัวดำเนินงาน](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="de3c5-168">เมื่อต้องการตรวจสอบว่าปริมาณคงคลังคงเหลือจะมากกว่า 0 เสมอหรือไม่ ให้เปลี่ยนค่าของฟิลด์ **ค่า** จาก **411** เป็น **0** และค่าของฟิลด์ **ผู้ปฏิบัติงาน** จากเครื่องหมายเท่ากับ (**=**) เป็นเครื่องหมายมากกว่า (**\>**)</span><span class="sxs-lookup"><span data-stu-id="de3c5-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![ค่าของฟิลด์มูลค่าและผู้ปฏิบัติงานเปลี่ยนแปลง](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="de3c5-170">บันทึกและปิดไฟล์พารามิเตอร์ Excel</span><span class="sxs-lookup"><span data-stu-id="de3c5-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="de3c5-171">เลือก **อัปโหลด** เพื่อบันทึกการเปลี่ยนแปลงที่คุณทำไว้กับไฟล์พารามิเตอร์ Excel เป็น Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="de3c5-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="de3c5-172">ขณะนี้ ถ้าค่าของฟิลด์ **ทั้งหมดพร้อมใช้งาน** สำหรับสินค้าที่ระบุในสินค้าคงคลังมีมากกว่า 0 (ศูนย์) การทดสอบจะผ่าน โดยไม่คำนึงถึงมูลค่าของปริมาณคงคลังคงเหลือจริง</span><span class="sxs-lookup"><span data-stu-id="de3c5-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="de3c5-173">ล็อกตัวสร้าง</span><span class="sxs-lookup"><span data-stu-id="de3c5-173">Generator logs</span></span>

<span data-ttu-id="de3c5-174">คุณลักษณะนี้สร้างโฟลเดอร์ที่มีล็อกของกรณีการทดสอบที่มีการรัน</span><span class="sxs-lookup"><span data-stu-id="de3c5-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="de3c5-175">เมื่อต้องการใช้คุณลักษณะนี้ เปิดไฟล์ **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ภายใต้โฟลเดอร์การติดตั้ง RSAT (ตัวอย่างเช่น **C:\\Program Files (x86)\\Regression Suite Automation Tool**) และเปลี่ยนค่าในองค์ประกอบต่อไปนี้จาก **เท็จ** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="de3c5-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="de3c5-176">หลังจากที่มีการรันกรณีการทดสอบแล้ว คุณสามารถค้นหาไฟล์ล็อกภายใต้ **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**</span><span class="sxs-lookup"><span data-stu-id="de3c5-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![โฟลเดอร์ GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="de3c5-178">ถ้ามีกรณีทดสอบที่มีอยู่ ก่อนที่คุณจะเปลี่ยนแปลงค่าในไฟล์ .config จะไม่มีการสร้างล็อกสำหรับกรณีการทดสอบดังกล่าวจนกว่าคุณจะสร้างไฟล์การดำเนินการทดสอบใหม่</span><span class="sxs-lookup"><span data-stu-id="de3c5-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![คำสั่งสร้างไฟล์การดำเนินการข้อความเท่านั้น บนเมนูใหม่](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="de3c5-180">สแนปช็อต</span><span class="sxs-lookup"><span data-stu-id="de3c5-180">Snapshot</span></span>

<span data-ttu-id="de3c5-181">คุณลักษณะนี้จะจับภาพหน้าจอของขั้นตอนที่ดำเนินการในระหว่างการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="de3c5-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="de3c5-182">เมื่อต้องการใช้คุณลักษณะนี้ เปิดไฟล์ **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ภายใต้โฟลเดอร์การติดตั้ง RSAT (ตัวอย่างเช่น **C:\\Program Files (x86)\\Regression Suite Automation Tool**) และเปลี่ยนค่าขององค์ประกอบต่อไปนี้จาก **เท็จ** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="de3c5-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="de3c5-183">ภายใต้ **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** โฟลเดอร์ที่แยกต่างหากจะถูกสร้างขึ้นสำหรับกรณีการทดสอบแต่ละกรณีที่มีการรัน</span><span class="sxs-lookup"><span data-stu-id="de3c5-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![โฟลเดอร์สแนปช็อตสำหรับกรณีการทดสอบ](./media/use_rsa_tool_12.png)

<span data-ttu-id="de3c5-185">ในโฟลเดอร์เหล่านี้แต่ละโฟลเดอร์ คุณสามารถค้นหาสแนปช็อตของขั้นตอนต่างๆ ที่ดำเนินการ ในขณะที่มีการรันกรณีการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="de3c5-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![ไฟล์สแนปช็อต](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="de3c5-187">การกำหนด</span><span class="sxs-lookup"><span data-stu-id="de3c5-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="de3c5-188">สถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="de3c5-188">Scenario</span></span>

1. <span data-ttu-id="de3c5-189">โปรแกรมออกแบบผลิตภัณฑ์จะสร้างผลิตภัณฑ์ที่นำออกใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="de3c5-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="de3c5-190">ผู้จัดการฝ่ายผลิตเริ่มต้นใบสั่งผลิตเพื่อนำระดับสินค้าคงคลังไปที่สองชิ้น</span><span class="sxs-lookup"><span data-stu-id="de3c5-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="de3c5-191">การผลิตจะเริ่มต้นและสิ้นสุดใบสั่งผลิต และตรวจสอบว่าปริมาณคงคลังคงเหลือคือสองชิ้น</span><span class="sxs-lookup"><span data-stu-id="de3c5-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="de3c5-192">ทีมงานขายได้รับใบสั่งสำหรับผลิตภัณฑ์ใหม่สี่ชิ้น</span><span class="sxs-lookup"><span data-stu-id="de3c5-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="de3c5-193">ดังนั้น ทีมขายจึงปรับปรุงความต้องการสุทธิผ่านแผนแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="de3c5-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="de3c5-194">เนื่องจากไม่มีกำลังการผลิตเพิ่มเติม จะมีการตั้งค่านโยบายใบสั่งเริ่มต้นเป็น "ซื้อแทนที่จะทำ"</span><span class="sxs-lookup"><span data-stu-id="de3c5-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="de3c5-195">ดังนั้น แผนการใบสั่งซื้อจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="de3c5-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="de3c5-196">ผู้ซื้อจะเพิ่มผู้จัดจำหน่าย ยืนยันแผนการใบสั่งซื้อ แล้วจากนั้น ยืนยันใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="de3c5-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="de3c5-197">เมื่อสินค้าที่ซื้อมาถึงที่ร้านค้า ผู้ปฏิบัติงานร้านค้าจะค้นหาใบสั่งซื้อที่เกี่ยวข้อง และรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="de3c5-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="de3c5-198">เนื่องจากใบสั่งนี้เสร็จสมบูรณ์แล้วในขณะนี้ คุณสามารถเบิกสินค้าและบรรจุสินค้าตามใบสั่งขายได้</span><span class="sxs-lookup"><span data-stu-id="de3c5-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="de3c5-199">การเงินลงรายการบัญชีใบแจ้งหนี้การซื้อและใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="de3c5-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="de3c5-200">ภาพประกอบต่อไปนี้แสดงโฟลว์สำหรับสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="de3c5-200">The following illustration shows the flow for this scenario.</span></span>

![โฟลว์สำหรับสถานการณ์จำลองการสาธิต](./media/use_rsa_tool_14.png)

<span data-ttu-id="de3c5-202">ภาพประกอบต่อไปนี้แสดงกระบวนการทางธุรกิจสำหรับสถานการณ์จำลองนี้ใน RSAT</span><span class="sxs-lookup"><span data-stu-id="de3c5-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![กระบวนการทางธุรกิจสำหรับสถานการณ์จำลองการสาธิต](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="de3c5-204">กลยุทธ์ – การเรียนรู้ที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="de3c5-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="de3c5-205">ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="de3c5-205">Data</span></span>

- <span data-ttu-id="de3c5-206">ตรวจสอบให้แน่ใจว่าคุณมีปริมาณข้อมูลของตัวแทน (สำเนาของข้อมูลการตั้งค่าคอนฟิกการผลิต/แบบ golden รวมถึงข้อมูลที่ถูกย้าย)</span><span class="sxs-lookup"><span data-stu-id="de3c5-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="de3c5-207">เมื่อคุณสร้างข้อมูลใหม่ผ่านตัวบันทึกงาน ให้สร้างชื่อการทดสอบที่จะไม่ขัดแย้งกับชื่อที่มีอยู่ (ตัวอย่างเช่น ใช้คำนำหน้า เช่น **RSATxxx**)</span><span class="sxs-lookup"><span data-stu-id="de3c5-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="de3c5-208">ใช้การคืนค่า Azure Point-In-Time เพื่อรันการทดสอบในสภาพแวดล้อมที่ไม่ใช่ระดับ 1 อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="de3c5-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="de3c5-209">ถึงแม้ว่าคุณจะสามารถใช้ฟังก์ชัน Excel **RANDOM** และ **NOW** เพื่อสร้างชุดที่ไม่ซ้ำกันได้ แต่ความพยายามจะสูงอย่างมาก</span><span class="sxs-lookup"><span data-stu-id="de3c5-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="de3c5-210">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="de3c5-210">Here is an example.</span></span>

    ```
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="de3c5-211">ตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="de3c5-211">Task recorder</span></span>

- <span data-ttu-id="de3c5-212">กำหนดสถานการณ์จำลอง ก่อนที่คุณจะเริ่มการบันทึก</span><span class="sxs-lookup"><span data-stu-id="de3c5-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="de3c5-213">โครงการที่มีการจัดการอย่างดีมีสถานการณ์จำลองการทดสอบที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="de3c5-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="de3c5-214">เมื่อต้องการสร้างกรณีการทดสอบ ให้พิจารณาว่าผลลัพธ์ของสถานการณ์จำลองของการทดสอบดังกล่าวสามารถคาดการณ์ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="de3c5-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="de3c5-215">แบ่งการบันทึก ถ้ามีการดำเนินการโดยบทบาทต่างๆ หรือหากมีเวลารอ หรือเหตุการณ์ภายนอกก่อนขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="de3c5-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="de3c5-216">หลีกเลี่ยงการเลือกค่าในรายการ</span><span class="sxs-lookup"><span data-stu-id="de3c5-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="de3c5-217">แต่ใช้รูปแบบข้อความ เช่น **FIFO** **AudioRM** และ **SiteWH** แทน</span><span class="sxs-lookup"><span data-stu-id="de3c5-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="de3c5-218">เมื่อคุณเลือกในรายการ จะมีการบันทึกตำแหน่งของค่าในรายการ ไม่ใช่ตัวค่าเอง</span><span class="sxs-lookup"><span data-stu-id="de3c5-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="de3c5-219">ถ้ามีการเพิ่มสินค้าลงในรายการดังกล่าว ตำแหน่งของมูลค่าอาจเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="de3c5-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="de3c5-220">ดังนั้น การบันทึกของคุณจะใช้พารามิเตอร์ที่แตกต่างกัน และส่วนที่เหลือของสถานการณ์จำลองดังกล่าวอาจได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="de3c5-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="de3c5-221">ลองนึกถึงลักษณะการทำงานของผู้ใช้หลายราย</span><span class="sxs-lookup"><span data-stu-id="de3c5-221">Think about multi-user behavior.</span></span> <span data-ttu-id="de3c5-222">ตัวอย่างเช่น อย่าสันนิษฐานว่าใบสั่งขายที่สร้างขึ้นใหม่ของคุณจะถูกเลือกโดยอัตโนมัติเสมอ</span><span class="sxs-lookup"><span data-stu-id="de3c5-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="de3c5-223">แต่ใช้ตัวกรองเพื่อค้นหาใบสั่งที่ถูกต้องแทนเสมอ</span><span class="sxs-lookup"><span data-stu-id="de3c5-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="de3c5-224">ใช้ฟังก์ชันคัดลอกในตัวบันทึกงานเพื่อบันทึกชื่อของผลิตภัณฑ์ที่สร้างขึ้นใหม่ เพื่อให้สามารถใช้งานได้ในกรณีการทดสอบที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="de3c5-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="de3c5-225">ใช้ฟังก์ชันตรวจสอบความถูกต้องในตัวบันทึกงาน เพื่อตั้งค่าจุดตรวจสอบว่ามีการรันขั้นตอนอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="de3c5-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="de3c5-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="de3c5-226">RSAT</span></span>

- <span data-ttu-id="de3c5-227">เมื่อต้องการรันการทดสอบในบริษัทอื่น คุณสามารถเปลี่ยนบริษัทบนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="de3c5-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="de3c5-228">ตรวจสอบให้แน่ใจว่าการตั้งค่าและข้อมูลพร้อมใช้งานในบริษัทที่เลือกใหม่</span><span class="sxs-lookup"><span data-stu-id="de3c5-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="de3c5-229">คุณสามารถเปลี่ยนผู้ใช้การทดสอบบนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="de3c5-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="de3c5-230">ระบุรหัสอีเมลของผู้ใช้ที่จะรันกรณีการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="de3c5-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="de3c5-231">ในลักษณะนี้ อาจมีการรันกรณีการทดสอบโดยใช้สิทธิ์การรักษาความปลอดภัยของผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="de3c5-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="de3c5-232">เมื่อต้องการรอก่อนที่จะเริ่มต้นการทดสอบ คุณสามารถกำหนดการหยุดชั่วคราวบนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="de3c5-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="de3c5-233">สามารถใช้การหยุดชั่วคราวนี้ในชุดงาน (ตัวอย่างเช่น ถ้าต้องรันลำดับงานก่อนที่จะสามารถดำเนินการขั้นตอนต่อไป)</span><span class="sxs-lookup"><span data-stu-id="de3c5-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="de3c5-234">การเขียนสคริปต์ขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="de3c5-234">Advanced scripting</span></span>

### <a name="command-line"></a><span data-ttu-id="de3c5-235">รายการคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="de3c5-235">Command line</span></span>

<span data-ttu-id="de3c5-236">RSAT สามารถถูกเรียกจากหน้าต่าง **พร้อมต์คำสั่ง**</span><span class="sxs-lookup"><span data-stu-id="de3c5-236">RSAT can be called from a **Command Prompt** window.</span></span>

> [!NOTE]
> <span data-ttu-id="de3c5-237">ตรวจสอบว่าตัวแปรของสภาพแวดล้อม **TestRoot** ถูกตั้งค่าเป็นพาธการติดตั้ง RSAT</span><span class="sxs-lookup"><span data-stu-id="de3c5-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="de3c5-238">(ใน Microsoft Windows เปิด **แผงควบคุม** เลือก **ระบบและการรักษาความปลอดภัย \> ระบบ \> การตั้งค่าระบบขั้นสูง** และจากนั้น เลือก **ตัวแปรของสภาพแวดล้อม** )</span><span class="sxs-lookup"><span data-stu-id="de3c5-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="de3c5-239">เปิดหน้าต่าง **พร้อมต์คำสั่ง** เป็นผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="de3c5-239">Open a **Command Prompt** window as an admin.</span></span>
2. <span data-ttu-id="de3c5-240">รันเครื่องมือจากไดเรกทอรีการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="de3c5-240">Run the tool from the installation directory.</span></span>

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="de3c5-241">แสดงรายการคำสั่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="de3c5-241">List all commands.</span></span>

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a><span data-ttu-id="de3c5-242">ตัวอย่างของ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="de3c5-242">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="de3c5-243">รันกรณีการทดสอบในลูป</span><span class="sxs-lookup"><span data-stu-id="de3c5-243">Run a test case in a loop</span></span>

<span data-ttu-id="de3c5-244">คุณมีสคริปต์การทดสอบที่สร้างลูกค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="de3c5-244">You have a test script that creates a new customer.</span></span> <span data-ttu-id="de3c5-245">โดยการเขียนสคริปต์ อาจมีการรันกรณีการทดสอบนี้ในลูปโดยการสุ่มข้อมูลต่อไปนี้ ก่อนที่จะมีการรันการเกิดซ้ำแต่ละครั้ง:</span><span class="sxs-lookup"><span data-stu-id="de3c5-245">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="de3c5-246">รหัสลูกค้า</span><span class="sxs-lookup"><span data-stu-id="de3c5-246">Customer ID</span></span>
- <span data-ttu-id="de3c5-247">ชื่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="de3c5-247">Customer name</span></span>
- <span data-ttu-id="de3c5-248">ที่อยู่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="de3c5-248">Customer address</span></span>

<span data-ttu-id="de3c5-249">รหัสลูกค้าจะอยู่ในรูปแบบ *ATCUS\<หมายเลข\>* โดยที่ \<หมายเลข\> อยู่ระหว่าง **000000001** และ **999999999**</span><span class="sxs-lookup"><span data-stu-id="de3c5-249">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="de3c5-250">ตัวอย่างต่อไปนี้ใช้พารามิเตอร์ **เริ่มต้น** เพื่อกำหนดหมายเลขแรกที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="de3c5-250">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="de3c5-251">ใช้พารามิเตอร์ที่สอง **nr** เพื่อกำหนดจำนวนของลูกค้าที่ต้องสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="de3c5-251">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="de3c5-252">สำหรับการเกิดซ้ำแต่ละครั้ง จะมีการเปลี่ยนแปลงพารามิเตอร์ในไฟล์พารามิเตอร์ Excel โดยใช้ฟังก์ชัน UpdateCustomer</span><span class="sxs-lookup"><span data-stu-id="de3c5-252">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="de3c5-253">จากนั้น รายการคำสั่ง RSAT ถูกเรียกในฟังก์ชัน RunTestCase</span><span class="sxs-lookup"><span data-stu-id="de3c5-253">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="de3c5-254">เปิด Microsoft Windows PowerShell Integrated Scripting Environment (ISE) ในโหมดผู้ดูแลระบบ และวางรหัสต่อไปนี้ลงในหน้าต่างที่ชื่อ **Untitled1.ps1**</span><span class="sxs-lookup"><span data-stu-id="de3c5-254">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```
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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="de3c5-255">รันสคริปต์ที่ขึ้นอยู่กับข้อมูลใน Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="de3c5-255">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="de3c5-256">ตัวอย่างต่อไปนี้ใช้การเรียก Open Data Protocol (OData) ในการค้นหาสถานะใบสั่งของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="de3c5-256">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="de3c5-257">ถ้าสถานะยังไม่ได้ **ออกใบแจ้งหนี้** คุณสามารถ ตัวอย่างเช่น เรียกใช้กรณีการทดสอบ RSAT ที่ลงรายการบัญชีใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="de3c5-257">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```
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
